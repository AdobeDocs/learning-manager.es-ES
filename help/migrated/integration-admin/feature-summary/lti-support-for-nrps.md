---
description: Aprenda cómo Adobe Learning Manager utiliza NRPS para sincronizar atributos de alumno personalizados de una plataforma LTI 1.3 en perfiles de alumno como campos activos
jcr-language: en_us
title: Compatibilidad de LTI con NRPS
exl-id: 4c972319-b8ce-4f2d-9ccb-1b93c6cc6ac0
source-git-commit: 92be9eb8ece6d083efe595894a492540cd96eead
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%
---

# Compatibilidad de LTI con NRPS

## Información general

Adobe Learning Manager admite la especificación de servicios de aprovisionamiento de nombres y funciones (NRPS) cuando actúa como herramienta de interoperabilidad de herramientas de aprendizaje (LTI) 1.3. Cuando un alumno inicia Learning Manager desde un sistema de gestión de aprendizaje externo (la plataforma), Learning Manager recupera el registro de abono del alumno desde la plataforma. A continuación, copia los atributos personalizados de ese registro, como el ID de departamento o empleado, en el perfil del alumno como campos activos.

## Casos de uso

* **Enriquecer perfiles de alumnos automáticamente.** Importa atributos como el departamento, el ID de empleado o los metadatos personalizados de tu plataforma a Learning Manager sin introducir los datos manualmente ni realizar importaciones independientes.
* **Analiza de dónde vienen tus alumnos.** Captura atributos de ubicación, como el país y la ciudad, para crear una imagen de la geografía de la que proceden tus alumnos. Utilice los campos de perfil resultantes para el análisis en Learning Manager.
* **Mantener los datos del perfil alineados con la plataforma de origen.** La plataforma sigue siendo la fuente de la verdad. Learning Manager actualiza los valores cada vez que se inicia un alumno.
* **Admite varias plataformas en una sola cuenta.** Los prefijos de espacio de nombres mantienen separados los atributos de diferentes plataformas, incluso cuando las plataformas utilizan el mismo nombre de atributo.

Con la sincronización de campos personalizados de NRPS, Learning Manager hace lo siguiente al iniciarse:

1. Detecta que la plataforma admite NRPS.
2. Solicita el registro de abono del alumno de inicio desde la plataforma.
3. Extrae los atributos personalizados de ese registro.
4. Escribe los atributos en el perfil del alumno como campos activos. Cada nombre de campo lleva un prefijo `<namespace>`, por lo que los atributos de diferentes plataformas no entran en conflicto.
5. Learning Manager reutiliza el token de credenciales de cliente de OAuth 2.0 que ya utiliza para Assignment and Grades Services (AGS). No es necesario configurar un nuevo extremo de token.

>[!NOTE]
>
>NRPS es una especificación opcional en LTI Advantage. La compatibilidad con NRPS y atributos personalizados varía según la plataforma. Asegúrese de que su plataforma expone NRPS 2.0 antes de planear el uso de esta función.

## Funciones principales

* **Compatibilidad con notificaciones de NRPS:** Learning Manager comprueba cada inicio de LTI 1.3 para la notificación de NRPS. Si la notificación no existe, el inicio continúa normalmente sin errores y sin repercusiones en el alumno.
  * Esta reclamación proporciona la siguiente información:
    * **Extremo de pertenencia:** `context_memberships_url `identifica la dirección URL de servicio del curso o contexto de aprendizaje desde el que el alumno inició ALM.
    * **Versiones compatibles:** `service_versions` muestra las versiones de NRPS disponibles en ese extremo.
      Esta función es compatible con NRPS 2.0.
  * **Infraestructura de tokens compartidos:** Learning Manager agrega el ámbito de NRPS a su solicitud de tokens de AGS existente y reutiliza la caché de tokens de registro previo existente.
* **Sincronizar parámetros personalizados con perfiles de alumnos**
  * **Campos activos con prefijo de espacio de nombres:** Cada atributo personalizado se asigna a un campo activo denominado `<namespace>_<field_name>`.
  * **Creación automática de campos:** Si no existe ningún campo activo coincidente, Learning Manager crea uno con el tipo **Texto** y el estado **Activo**.
  * **La plataforma como fuente de confianza:** Learning Manager sobrescribe los valores de perfil existentes con los valores más recientes de la plataforma. Los alumnos y los administradores no pueden editar estos campos.
  * **Comportamiento sin bloqueo:** Los errores de NRPS no impiden que los alumnos inicien contenido de aprendizaje.
  * **Varios orígenes para atributos personalizados:** Learning Manager puede leer atributos personalizados desde el extremo de NRPS y desde parámetros personalizados en el token de inicio de LTI. Obtenga más información sobre [atributos personalizados en el token de inicio](#custom-attributes-in-the-launch-token).

## Configuraciones admitidas

| Elemento | Asistencia |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| Función de administrador de aprendizaje | Herramienta LTI 1.3 |
| Versión LTI | LTI 1.3 |
| Versión del servicio NRPS | 2.0 |
| Plataformas (formato de campo personalizado compatible con especificaciones) | Moodle, D2L Brightspace, Blackboard (Anthology), Sakai |
| Tipo de campo personalizado | Texto |
| Desencadenador | Cada lanzamiento de LTI 1.3 |

La compatibilidad con plataformas depende del modelo de serialización de campos personalizados utilizado en el registro de miembros de NRPS. Pueden coexistir varios patrones, pero Learning Manager solo procesa los patrones admitidos en la versión activa.

## Cómo funciona

### Flujo de lanzamiento

1. Un alumno inicia Learning Manager desde la plataforma.
2. Learning Manager lee la notificación NRPS en el token de inicio de LTI 1.3. Si la notificación muestra la versión 2.0 del servicio NRPS, Learning Manager almacena `context_memberships_url` para la sesión y el contexto LTI (curso).
3. Learning Manager solicita un token de acceso que incluye el ámbito de NRPS `https://purl.imsglobal.org/spec/lti-nrps/scope/contextmembership.readonly`.
4. Learning Manager llama a `context_memberships_url?rlid=<lti_user_id>` con el token de portador para recuperar el registro de inicio del alumno. Si la plataforma omite el filtro `rlid` y devuelve la lista completa, Learning Manager busca al alumno por `user_id`.
5. Learning Manager extrae los campos personalizados del registro.
6. Learning Manager asigna cada campo personalizado a un campo activo y escribe los valores en el perfil del alumno.
7. Alternativamente, ALM también admite la extracción de parámetros personalizados para sincronizarlos con el perfil del alumno durante el inicio de la herramienta, si los parámetros personalizados están prefijados con el campo identificable de ALM `ALMfield`.

### Formato de campo personalizado

La especificación NRPS 2.0 define los datos personalizados como una matriz `message` en el registro miembro. Learning Manager lee los datos personalizados de la notificación personalizada de LTI dentro de esa matriz. En esta versión, Learning Manager admite la representación de patrones compatibles con especificaciones.

```json
{
  "user_id": "abc123",
  "message": [
    {
      "https://purl.imsglobal.org/spec/lti/claim/custom": {
        "department": "Engineering",
        "employee_id": "E4567"
      }
    }
  ]
}
```

### Atributos personalizados en el token de inicio

Las plataformas también pueden enviar atributos personalizados como parámetros personalizados en el token de inicio de LTI. Learning Manager recopila atributos tanto del token de inicio como del extremo de NRPS y los almacena en el perfil del alumno.

Para los atributos del token de inicio, el nombre del parámetro debe comenzar con el prefijo `almfield-` que requiere Learning Manager. Sin el prefijo, Learning Manager no puede distinguir estos parámetros de otros parámetros personalizados y no los importa. Los atributos recuperados del extremo de NRPS no necesitan este prefijo. Este prefijo solo es necesario si se importan parámetros personalizados en el token de inicio de ALM para identificar el campo que debe sincronizar con los campos activos del alumno.

>[!NOTE]
>
>Confirme el prefijo exacto requerido con su representante de Learning Manager antes de configurar parámetros personalizados en la plataforma.

### Asignación y nomenclatura de campos activos

Learning Manager crea el nombre del campo activo como `<namespace>_<field_name>`. Por ejemplo, el campo `department` del espacio de nombres `https://purl.imsglobal.org/spec/lti/claim/custom` se convierte en `https://purl.imsglobal.org/spec/lti/claim/custom_department`.

Learning Manager aplica las siguientes reglas:

* **Longitud del nombre:** Si el nombre supera el límite de caracteres del nombre del campo activo, Learning Manager acorta primero la parte del espacio de nombres y mantiene el nombre del campo.
* **Conflictos de nombres:** Después de acortarlos, Learning Manager comprueba si hay conflictos con campos activos existentes de otro origen. Si hay un conflicto, ajusta la longitud de acortamiento hasta que encuentre un nombre único. Si no encuentra un nombre único, omite el campo y registra un error.
* **Coincidencia:** La coincidencia de nombres de campo no distingue entre mayúsculas y minúsculas.
* **Campo existente y habilitado:** Learning Manager escribe el valor en el perfil del alumno.
* **Campo existente y deshabilitado:** Learning Manager omite el campo sin registrar ningún error.
* **Ningún campo existente:** Learning Manager crea un campo de **texto** con el estado **Activo**.

### Escribir valores en el perfil

* En cada inicio en el que Learning Manager recupera datos NRPS, escribe todos los valores de campo personalizados resueltos en el perfil del alumno que los inicia. No se cambia ningún otro perfil de alumno.
* Si un campo ya tiene un valor, Learning Manager lo sobrescribe con el valor más reciente de la plataforma.
* Si el valor de plataforma está vacío o es nulo, Learning Manager mantiene el valor de perfil existente.
* Un error al escribir un campo no bloquea el inicio ni las escrituras de otros campos.
* Learning Manager aplica las actualizaciones de campo en la misma transacción de inicio siempre que sea posible.
* Los alumnos no pueden editar campos de origen NRPS en su página de perfil y los administradores no pueden editar estos valores en nombre de un alumno.

## Configurar la sincronización de campos personalizados de NRPS

### Requisitos previos

* Su plataforma está registrada en Learning Manager como una herramienta LTI 1.3. Esta función no es compatible con LTI 1.1 o LTI 1.2.
* Su plataforma es compatible con la versión 2.0 del servicio NRPS y expone atributos personalizados en el formato `message` compatible con especificaciones.
* El token de inicio de LTI contiene la notificación `namesroleservice`.
* La notificación proporciona `context_memberships_url`, que identifica el extremo de NRPS específico del curso.
* El valor `service_versions` de la notificación incluye `2.0`.
* Tiene acceso de administrador al registro de herramientas de la plataforma.

### Otorgar el ámbito NRPS a Learning Manager

Los nuevos registros que incluyen el ámbito NRPS no requieren ninguna configuración adicional en Learning Manager.

Los nuevos registros que incluyen el ámbito NRPS funcionan sin más cambios en Learning Manager. Para un registro existente, el administrador de la plataforma debe actualizar el registro de la herramienta en el lado de la plataforma.

>[!NOTE]
>
>No es necesario cambiar el punto final del token, el ID de cliente o la clave privada en Learning Manager. Se reutiliza la configuración del AGS existente. Si la plataforma no concede el ámbito NRPS, Learning Manager omite NRPS sin que ello afecte al AGS ni al inicio.

### Exponer atributos del alumno en la plataforma

La plataforma controla qué atributos del alumno comparte. Los pasos exactos dependen de la plataforma. Por ejemplo, en Moodle:

1. Añada Learning Manager como una herramienta externa mediante LTI 1.3.
2. Active la configuración de privacidad que permite a la plataforma compartir información del alumno con la herramienta.
3. Defina los atributos personalizados que desea enviar. Puede utilizar variables de plataforma o valores predefinidos.
4. Si también envía atributos como parámetros personalizados en el token de inicio, añada el prefijo que Learning Manager necesite a cada nombre de parámetro.

>[!NOTE]
>
>Exponga solo los atributos necesarios para el caso de uso de aprendizaje. Learning Manager trata la plataforma como la fuente de confianza y no ofrece controles de consentimiento o privacidad independientes en esta versión.

### Comprobar la sincronización

1. Inicie Learning Manager en la plataforma como alumno de prueba.
2. Confirme que el inicio se completa normalmente.
3. En la aplicación de administración de Learning Manager, abra la página de campos activos.
4. Confirme que los campos aparecen con el prefijo del espacio de nombres, con el tipo **Texto** y el estado **Activo**.
5. Abra el perfil del alumno de la prueba y confirme que los valores coinciden con la plataforma.
6. Confirme que los campos de origen NRPS son de sólo lectura. Ni el alumno ni un administrador pueden editar manualmente los valores sincronizados.
7. Reinicie el programa después de cambiar un valor de origen no vacío y compruebe que Learning Manager sobrescribe el valor de perfil existente con el último valor de NRPS.

>[!TIP]
>
>Si un campo existe pero está desactivado, Learning Manager no escribe en él. Habilite el campo si desea que se rellene.

## Gestión de errores y registro

Learning Manager nunca bloquea a un alumno debido a un problema de NRPS. No se vuelve a intentar. Registra el error y omite la sincronización de NRPS para ese inicio. El siguiente inicio lo intenta de nuevo.

| Condición | Resultado |
|------------------------------------------------------------------|-------------------------------------------------------|
| La notificación de NRPS está ausente del token de inicio | Se omite el NRPS. El lanzamiento continúa. |
| Solo está presente la versión 1.0 del servicio NRPS | Se omite el NRPS. El lanzamiento continúa. |
| La solicitud de token falla o la plataforma no concede el ámbito NRPS | Se omite el NRPS. El AGS y el inicio no se ven afectados. |
| La llamada NRPS falla (timeout, 4xx o 5xx) | Se registra el error. El lanzamiento continúa. |
| El alumno no se encuentra en la respuesta de NRPS | La sincronización de campos se omite. El lanzamiento continúa. |
| No hay campos personalizados en la respuesta NRPS | La sincronización de campos se omite sin errores. |
| No se puede resolver un conflicto de nombre de campo | El campo se omite y se registra un error. |
| Error de escritura en un solo campo | Se siguen escribiendo otros campos. El lanzamiento continúa. |

Cada entrada de registro incluye la marca de tiempo, el ID de registro de plataforma, el ID de alumno y el motivo del error. Los administradores del sistema de Learning Manager pueden acceder a los registros.

## Notas

* Solo se sincroniza el registro de inicio del alumno. Learning Manager no sincroniza la lista completa de cursos.
* Solo se admite la versión 2.0 del servicio NRPS.
* Todos los campos sincronizados tienen el tipo **Texto**. Learning Manager no deduce tipos de valores. No se admiten los tipos de campo Número, Fecha y Booleano.
* Learning Manager actúa como herramienta LTI. No actúa como una plataforma NRPS y no proporciona un punto final de la lista a otras herramientas.
* La sincronización de campos personalizados se produce durante el inicio de LTI.
