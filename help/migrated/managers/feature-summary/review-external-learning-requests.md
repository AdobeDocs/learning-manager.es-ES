---
jcr-language: en_us
title: Enviar aprendizaje externo en Adobe Learning Manager
description: Los responsables pueden revisar las solicitudes de aprendizaje externas enviadas por los miembros de su equipo, verificar los detalles y cualquier prueba de finalización, y aprobar o rechazar cada solicitud con un comentario opcional. Los envíos aprobados se añaden a la transcripción del alumno.
contentowner: saghosh
source-git-commit: 2495d33fc1595bd962ba07988123e3563d4c69a0
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Revisar solicitudes de aprendizaje externas como responsable

Cuando un alumno de su equipo envíe una solicitud de aprendizaje externo en Adobe Learning Manager, recibirá una notificación en la plataforma. Puede revisar los detalles del envío, aprobar o rechazar la solicitud y añadir un comentario para el alumno.

## Cómo funciona el flujo de trabajo de revisión del responsable

Cuando un alumno envía una solicitud de aprendizaje externa, ocurre lo siguiente:

1. Recibirás una **notificación en la aplicación** que te pedirá que revises el envío. El envío aparece en la pestaña **Aprendizaje externo** en el panel del administrador.
2. Abre un envío, revisa todos los campos y cualquier documento cargado como prueba y selecciona **Aprobar** o **Rechazar**.
3. Puede agregar un **comentario de revisión** que el alumno ve cuando recibe su notificación.
4. El alumno recibe una **notificación en la plataforma** con tu decisión.

Si aprueba un envío, la actividad de aprendizaje externa se agrega a **Transcripción del alumno administrador** y aparece en el registro de transcripciones del alumno.

<!--You can also change a previously **Rejected** submission to **Approved** if the circumstances change.-->

## Revisar y aprobar o rechazar un envío

1. Inicie sesión en Adobe Learning Manager como responsable.

2. Seleccione **Aprendizaje externo** en el panel de navegación izquierdo.

3. En la lista de envíos, seleccione la solicitud que desea revisar. Los envíos se ordenan por fecha de envío, apareciendo arriba lo más reciente.

4. Revise la presentación completa:

   - Título, descripción, fechas, duración y puntuación

   - Cualquier campo personalizado configurado por el administrador

   - El documento de prueba adjunto, si se proporciona. Seleccione el archivo adjunto para verlo o descargarlo

5. Seleccione **Aprobar** o **Rechazar**.

6. En el campo **Comentario de revisión**, escriba las notas para el alumno. Esto es opcional, pero se recomienda al rechazar una solicitud, para que el alumno entienda qué corregir.

7. Seleccione **Enviar**.

El alumno recibe una notificación en la aplicación de su decisión. Si ha aprobado el envío, ahora aparece en la transcripción del alumno.

## Administrar la cola de envíos

La cola de aprendizaje externo muestra todos los envíos pendientes y pasados de los informes directos.

**Filtrar por estado**

Use el filtro **Estado** para reducir la lista:

- **Todos**- muestra todos los envíos independientemente del estado

- **Pendiente de revisión-** solo muestra los envíos pendientes de revisión

- **Aprobado-** muestra los envíos que ya has aprobado

- **Rechazado-** muestra los envíos que has rechazado

**Buscar y ordenar**

- Utilice el campo **Buscar** para buscar envíos por nombre de alumno.

- Los envíos se ordenan por fecha de envío de forma predeterminada, apareciendo en la parte superior la más reciente.

### Reglas de enrutamiento de aprobación

De forma predeterminada, los envíos de aprendizaje externos se dirigen al responsable directo de un alumno. Las siguientes reglas se aplican cuando un alumno no tiene asignado un responsable directo:

| **El alumno tiene un responsable** | **El alumno es administrador** | **El envío se enruta a** |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Sí | No | Administrador directo (caso predeterminado) |
| Sí | Sí | Administrador directo (caso predeterminado) |
| No | No | Usuario de la cuenta raíz, si el usuario de la cuenta raíz tiene una función de administrador; de lo contrario, el envío se aprueba automáticamente. |
| No | Sí | Usuario de la cuenta raíz, si el usuario de la cuenta raíz tiene una función de administrador; de lo contrario, el envío se envía al alumno. |

Si tiene alguna pregunta sobre la asignación de responsable de un alumno específico, póngase en contacto con el administrador de cuentas.

## Informes de aprendizaje externo y cambios en las transcripciones

Cuando se aprueba el envío de aprendizaje externo de un alumno en Adobe Learning Manager, la actividad se añade al sistema de informes y aparece tanto en la transcripción del alumno administrador como en la transcripción del alumno.

### Aspecto del aprendizaje externo en transcripciones de alumnos

**Nota:** Al habilitar el aprendizaje externo, se agregan las siguientes columnas nuevas a la transcripción del alumno administrador: **Nombre de aprendizaje externo**, **Comentario de finalización** y una columna dinámica para cada campo personalizado. Las columnas de campos personalizados siempre aparecen al final de la exportación. Si los datos de la transcripción del alumno se transmiten a las herramientas de informes automatizados o de IE, asegúrese de que esas canalizaciones se actualicen para gestionar las columnas adicionales.

Solo aparecen en las transcripciones **envíos de aprendizaje externos aprobados**. Los envíos en estado **Pendiente de aprobación** o **Rechazado** no se incluyen en las exportaciones de transcripciones.

La transcripción del alumno administrador y la transcripción del alumno tratan el título de aprendizaje externo de forma diferente:

- En **Transcripciones de alumnos administradores**, el título de aprendizaje externo se coloca en la columna **Programa de aprendizaje/Certificación/Curso** existente, lo que mantiene la estructura de columnas coherente con otros tipos de actividad de aprendizaje.

- En la **Transcripción del alumno** (generada por el alumno), se agrega una nueva columna denominada **Nombre de aprendizaje externo** inmediatamente después de la columna **Módulo**.

Los campos personalizados configurados por el administrador aparecen como columnas dinámicas al final de ambas exportaciones de transcripciones una vez que se aprueba un envío.

El filtrado basado en fechas de la transcripción del alumno administrador para filas de aprendizaje externas se basa en la **fecha de finalización**, que corresponde a la fecha de aprobación.