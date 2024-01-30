---
title: Novedades de esta versión (noviembre de 2022)
description: Obtenga información sobre las funciones nuevas y las mejoras de Adobe Learning Manager.
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 77%

---

# Novedades de esta versión (noviembre de 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Configuración de varios inicios de sesión únicos (SSO)

Adobe Learning Manager admite actualmente un método de inicio de sesión para usuarios internos y otro para usuarios externos. Esto crea limitaciones en los casos en los que los clientes tienen a sus empleados y sus propios clientes y socios de canal en la misma cuenta.

Con la intención de admitir varios tipos de grupos de usuarios que inicien sesión en la plataforma, Adobe Learning Manager admite ahora varios métodos de inicio de sesión a través de diversas configuraciones de SSO para usuarios internos y externos.

Para obtener más información, consulte [Varios métodos de inicio de sesión único (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

## Compatibilidad con la función de sesión no iniciada

El portal nativo de Adobe Learning Manager admite actualmente el método de acceso a un portal de formación sin iniciar sesión.

Los alumnos ahora pueden descubrir el sitio de formación y acceder a él, consultar los distintos cursos y contenidos disponibles y decidir si desean iniciar sesión para consumir los cursos.

Esta función facilita la creación de un portal de aprendizaje orientado al cliente, en el que los alumnos pueden explorar varios cursos sin tener que iniciar sesión desde el principio.

Para obtener más información, consulte [Experiencia sin inicio de sesión para alumnos](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md).

## Mejoras de la página de información general de formación

La página de información general de formación ahora incluye una interfaz de usuario actualizada para que los alumnos tengan una experiencia mejorada al consumir un curso.

Entre otras mejoras, se incluyen las siguientes:

* Inclusión de un curso de formación en los marcadores.
* Recomendación de cursos relacionados.
* Información de rutas de aprendizaje para cursos y rutas de aprendizaje.
* Nombres de autores en los que se puede hacer clic.
* Rutas para facilitar la navegación.

## Mejoras de la página de información general de formación

La página de información general de formación ahora incluye una interfaz de usuario actualizada para que los alumnos tengan una experiencia mejorada al consumir un curso.

Entre otras mejoras, se incluyen las siguientes:

* Inclusión de un curso de formación en los marcadores.
* Recomendación de cursos relacionados.
* Información de rutas de aprendizaje para cursos y rutas de aprendizaje.
* Nombres de autores en los que se puede hacer clic.
* Rutas para facilitar la navegación.

## Página de perfil del autor

En la página de perfil del autor, se muestra toda la formación creada por un determinado autor.

Los alumnos pueden encontrar fácilmente información específica del autor y todos los cursos de formación creados por este.

## Cursos de formación incluidos en marcadores

Los alumnos pueden guardar (con el botón Guardar) o marcar los cursos de formación en el mosaico de cursos o la página de información general. Todos los cursos marcados estarán disponibles en la página de inicio del alumno.

## Personalización del reproductor

En esta versión, puede personalizar el reproductor Fluidic para que coincida con los requisitos de marca de un curso.

Puede visualizar y ocultar varias opciones y ajustes del reproductor en función de los requisitos del contenido y otorgar control a los alumnos en función del tipo de contenido. Puede aplicar este cambio en las implementaciones nativas y sin encabezado.

Puede cambiar las siguientes opciones:

* Alternar índice
* Notas
* Idioma
* Velocidad
* Leyenda
* Volumen
* Controles de reproducción

## Suplantación del alumno y el responsable

Los administradores pueden ejecutar una sesión suplantada en la que pueden iniciar sesión en nombre de cualquier usuario de su cuenta con la función de alumno y responsable.

Para obtener más información, consulte [Suplantación del alumno y el responsable](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md).

## Otras mejoras

### Registro de auditoría de correo electrónico

Los administradores ahora pueden acceder a todos los registros de correo electrónico enviados desde el sistema mediante un informe de seguimiento de auditoría de correo electrónico.

Este registro captura todos los datos relacionados con los mensajes de correo electrónico enviados en los últimos 30 días y se actualiza diariamente. Además, el informe contiene diversos detalles como, por ejemplo, el estado de entrega, el remitente, el receptor, el asunto y los metadatos del contenido.

Descargue el informe desde Informes > Informes personalizados > Informes de Excel > Informe de correos electrónicos. Aparece una notificación mediante la que puede descargar el informe.

Este informe consta de los siguientes campos:

* Hora de activación del correo electrónico (zona horaria UTC)
* Hora de estado del último evento (zona horaria UTC)
* Estado de entrega
* Correo electrónico del destinatario
* ID de usuario del remitente
* Asunto de correo electrónico
* Tipo de entidad
* Nombre de entidad
* ID de entidad

### Notificación de alumnos en lista de espera

Cuando un autor añade una nueva instancia, puede activar un mensaje de correo electrónico para enviar una notificación a los alumnos en lista de espera de otras instancias. Los alumnos recibirán un mensaje de correo electrónico sobre el cambio.

### Plantillas de correo electrónico de nivel de instancia

Puede personalizar los mensajes de correo electrónico para cada instancia de un curso de formación.

Siempre que se permita al autor o el administrador añadir una nueva instancia, se podrá editar la plantilla de una instancia individual.

Por ejemplo, si un curso tiene diferentes tipos de público, puede cambiar la plantilla de correo electrónico según corresponda.

![plantillas de correo electrónico](assets/email-template.png)

La prioridad de la plantilla se enumera a continuación:

1. Plantilla de nivel de instancia
2. Plantilla de nivel de formación
3. Plantilla de nivel de cuenta

### Comentarios del instructor al aceptar envíos

Los instructores ahora pueden añadir comentarios al aceptar los envíos realizados por los alumnos. Una vez que el instructor aprueba el envío, el alumno recibe una notificación por correo electrónico y otra en la aplicación (si se ha activado esta opción). Los comentarios relacionados con el envío están presentes en las transcripciones de alumnos tanto para el administrador como para el alumno.

### Mejoras relacionadas con la búsqueda

Aparece el historial de búsquedas recientes de un alumno para que pueda ver todas las búsquedas anteriores.

Los resultados de la búsqueda ahora son coherentes entre todo el aprendizaje formal e informal (Aprendizaje social). Los resultados incluyen cursos de formación, Aprendizaje social y correspondencias de la Tienda de contenido.

La búsqueda está más centrada y orientada, y puede ver los resultados de búsqueda en tres ubicaciones: Aprendizaje formal, Aprendizaje social y Tienda de contenido.

![buscar](assets/search-image.png)

#### Búsqueda basada en frases

En esta versión de Adobe Learning Manager, hemos sustituido la búsqueda de escritura anticipada por la búsqueda basada en frases.

#### Búsquedas recientes

Un alumno solo puede ver sus búsquedas recientes en la sesión actual.

### Catálogo de cursos gratuitos de la Tienda de contenido

La Tienda de contenido pone a disposición de los alumnos un conjunto gratuito de 50 cursos de alta calidad seleccionados.

### Compatibilidad con el idioma indonesio

La lengua indonesia se incluye ahora como idioma de interfaz en las aplicaciones del alumno y el responsable.

### Campo Autor obligatorio

Al crear un curso, el campo Autor es obligatorio.

### Cambios en la Tienda de contenido

* Las cuentas de prueba recién creadas enumerarán un nuevo catálogo para 50 cursos gratuitos en Mercado de contenido, que están disponibles para los usuarios.
* Un alumno puede ver ahora el número de resultados de búsqueda y vínculos incrustados para redirigir a Mercado de contenido.

### Cambios en la experiencia móvil envolvente

En esta versión, los usuarios web de la experiencia móvil envolvente pueden realizar las tareas indicadas a continuación:

* Crear: publicaciones de encuestas.
* Editar publicación: todos los tipos, RTE.
* Flujo de trabajo de comercio electrónico.
* Vista previa de un módulo: los alumnos tendrán la función Vista previa del módulo en Envolvente para dispositivos móviles. Este cambio permitirá a los alumnos obtener una vista previa del módulo antes de inscribirse en un curso.
* Copiar una URL.
* Eliminar un tablero.

### Cambios en el conector de Zoom

El tipo de aplicación JWT dejará de utilizarse en junio de 2023. Es recomendable que cree aplicaciones de OAuth o de OAuth de servidor a servidor para reemplazar la funcionalidad de una aplicación JWT en la cuenta.

### Informe de interacción

En esta versión, obtendrá acceso a un informe que muestra varios cursos en los que se ha activado la interacción.

### Importar preferencias de idioma mediante CSV

Al importar un archivo CSV, el archivo CSV contiene los campos Idioma de la interfaz, Idioma del contenido y Zona horaria.

El administrador también puede exportar el informe, que contiene los mismos campos indicados anteriormente.

* Idioma de la interfaz
* Idioma del contenido
* Zona horaria

Además de los administradores, también puede exportar este informe un administrador personalizado.

![informe de idioma](assets/language-report.png)

#### Efectos en la localización

* Los nombres de columna no se pueden localizar y deben ser aparecer tal cual (&quot;Interface Language&quot;, &quot;Content Language&quot; y &quot;Timezone&quot;).
* Los códigos de configuración regional no distinguen entre mayúsculas y minúsculas.
* Aunque no hay restricciones a la hora de proporcionar el código de país, solo puede especificar el código de idioma. Por ejemplo, tanto &quot;it_IT&quot; como &quot;it&quot; son válidos.
* Si hay alguna discrepancia en el informe debido a un código de configuración regional incorrecto, el procesamiento del archivo CSV continuará con normalidad y no afectará a los demás registros del mismo. La preferencia de configuración regional del usuario con una configuración regional incorrecta no se actualiza. El resto de los datos sí se actualizan.

## Cambios y mejoras de las API

### Conectores de clase virtual

Si se utiliza un ID de correo electrónico de administrador para configurar el conector de clase virtual, ese administrador debe tener permiso para lo siguiente:

* Crear una reunión
* Actualizar una reunión
* Obtener informes de asistencia

Al crear o actualizar la reunión de clase virtual, los instructores deben FINALIZAR la reunión en un plazo de 30 minutos desde la hora de finalización programada de la reunión.

### Uso de marcadores

Se han añadido las siguientes API para marcar un curso en la página de información general de formación:

* Obtener todos los marcadores: `primeapi/v2/bookmarks`
* Crear un marcador: `primeapi/v2/learningObjects/{id}/bookmark`
* Eliminar un marcador: `primeapi/v2/learningObjects/{id}/bookmark`

### Compatibilidad con contenido y metadatos de varias configuraciones regionales mediante la migración

Para todos los tipos de formación admitidos en la plataforma (cursos, rutas de aprendizaje, módulos, certificaciones y ayudas de trabajo), ahora se admite la migración de varios idiomas mediante archivos CSV utilizando columnas extra para los idiomas adicionales.

#### Requisitos previos

Cree el proyecto de migración como administrador de integración y, a continuación, comparta migrationProjectId con el equipo de asistencia de ALM, para que se pueda habilitar el indicador de varias configuraciones regionales desde el back-end.

#### Ámbito de los objetos de migración multilocale

* Módulo
* Curso
* Versión del módulo
* Certificación
* Programa de aprendizaje
* Ayuda de trabajo
* Versión de ayuda de trabajo

#### Especificación en CSV

Adobe Learning Manager proporciona un conjunto de especificaciones de CSV estándar para la migración habilitada para varias configuraciones regionales. El procedimiento recomendado es revisar estas especificaciones de CSV antes de comenzar con el proceso de migración. El administrador de integración de su empresa puede analizar los formatos de datos existentes y asignarlos para que coincidan con los elementos de la plantilla CSV proporcionada por Learning Manager.

#### Cambios con compatibilidad con varias configuraciones regionales

* La columna module_version no se admite en module_version.csv ni course_module.csv.
* No se puede actualizar module_version en la misma ejecución (no se puede realizar la migración con dos versiones que tengan el mismo módulo en la misma ejecución).
* La actualización de contenido o metadatos se considera una actualización de la versión del módulo desde el archivo module_version.csv.
* No se puede admitir la actualización de Job_Aid_Version mediante job_aid_version.csv

### Revocar tokens de autenticación y cookies

Una aplicación de LMS sin encabezamiento obtienen refresh_token durante el primer inicio de sesión. Posteriormente, refresh_token se utiliza para generar access_token a fin de que sus aplicaciones cliente realicen llamadas de API. Del mismo modo, la reproducción de contenido utiliza el punto final oauth para generar cookies de administración de la reproducción, lo que implica varios archivos de contenido y llamadas de API realizadas por esos archivos mediante cookies. La cookie generada por oauth tiene la misma validez que access_token, que es de siete días. Una vez generada la cookie, no hay forma de borrarla, a diferencia del típico cierre de sesión de la aplicación web. La cookie de oauth y la cookie de la aplicación web son dos cookies diferentes y no tienen relación entre sí.

Por lo tanto, para borrar la cookie, hemos introducido un nuevo punto final, que revoca refresh_token, la cookie y ambos.

**Detalles**

**Punto final**

`POST oauth/o/revoke`

**Parámetros de consulta**

* `cookie=true|false` - indica que la cookie debe ser revocada
* `refresh_token=true|false` - indica que actualizar

**Cuerpo de solicitud**

Cuerpo necesario para revocar refresh_token o (refresh_token y la cookie)

```
{
      "client_id": <>,
      "client_secret": <>,
      "refresh_token": <>
}
Body required for revoking oauth cookie only
{
      "access_token": <>
}
```

### API convertidas en públicas

En esta versión, hemos hecho públicas algunas API.

| API | Tipo | Descripción |
|---|---|---|
| /social/search | GET | Realice búsquedas en las redes sociales. |
| /anuncios | GET | Obtenga información detallada sobre el anuncio en la cabecera asignada al alumno. |
| /anuncios/`{id}` | GET | Obtenga información detallada sobre el anuncio en la cabecera asignada al alumno. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | URL de carga del archivo para loResource de resourceType &#39;Activity&#39; donde se requiere el envío del archivo. |
| /jobAid/`{jobAidId}`/jobAidDownloaded | GET | Establecer informe de descarga de ayuda de trabajo. |
| /bulkimport/startrun | POST | Ejecute una importación en bloque. |
| /bulkimport/cansync | GET | Sincronice la importación en bloque. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Obtener información relacionada con la actualización de contenido. |
| /uploadSigner | GET | Obtenga la firma del contenido de to_sign. |
| /avatar | POST | Actualiza la imagen del avatar del alumno con una nueva imagen. |
| /avatar | ELIMINAR | Elimina la imagen de avatar del alumno. |

### Aplicación Salesforce

La **Omitir pedido superior LO** Esta opción debe estar activada en la aplicación Salesforce para que todos los cursos, programas de aprendizaje y certificados se puedan ver al mismo tiempo.

### API para la personalización del reproductor

En esta versión, hemos proporcionado una API para personalizar el reproductor. Puede realizar lo siguiente:

* Inicie o cargue el reproductor.
* Desplácese a un módulo específico.
* Active o desactive el índice.
* Cambie el idioma.
* Cierre el reproductor.
* Reproduzca, pause, avance, retroceda, busque, o cambie el volumen o la velocidad.
* Capture eventos emitidos por el reproductor.

### Mostrar la posición de la lista de espera de un alumno

La API GET /enrollments/{id}/waitlistPosition de la API de objetos de aprendizaje recupera la posición de lista de espera de un usuario para una inscripción especificada.

### Fecha de finalización de envío en certificaciones externas

La API /primeapi/v2/learningObjects/certification:xxxxx presentará el atributo &quot;completionDateSameAsApprovalDate&quot; para indicar si el certificado tiene activada la &quot;Fecha de finalización de la certificación&quot; para el alumno o no, junto con el indicador &quot;true&quot; (verdadero)/&quot;false&quot; (falso).

### Obtener datos de vista previa de objetos de aprendizaje

El GET /preview/learningObjects/{id} La API se añade a Obtener información de vista previa sobre un objeto de aprendizaje.

### Mover usuarios externos en perfiles

La `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` Esta llamada ayuda a mover un usuario a otro perfil externo especificando un nuevo id. de perfil externo.

### Añadir usuarios a perfiles externos

La `POST /externalProfiles/{id}/users` añade usuarios externos a un perfil externo.

## Notas de la versión

Para obtener información sobre las versiones actuales y anteriores de la aplicación web y para dispositivos de Learning Manager, consulte la [Notas de la versión](/help/migrated/release-note/release-notes.md).

## Correcciones de errores

Para ver los errores que se han solucionado en esta actualización, consulte la [Lista de errores corregidos](release-note/release-notes.md#bugs-fixed-in-this-release).

## Requisitos del sistema

[Requisitos del sistema de Learning Manager](/help/migrated/system-requirements.md)
