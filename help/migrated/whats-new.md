---
description: Descubra las nuevas funciones y mejoras de la versión de noviembre de 2024 de Adobe Learning Manager
jcr-language: en_us
title: Resumen de nuevas funciones
exl-id: 4dfe0e31-d202-4a6e-8c4f-43851218699f
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '3149'
ht-degree: 2%

---

# Resumen de nuevas funciones {#new-features-summary}

Descubra las nuevas funciones y mejoras de la versión de noviembre de 2024 de Adobe Learning Manager.

* **Búsqueda basada en IA:** Combina la búsqueda léxica y semántica para obtener resultados más inteligentes según el contexto.
* **Webhooks**: se integra con Webhooks para enviar información en tiempo real a direcciones URL específicas.
* **Interoperabilidad de herramientas de aprendizaje (LTI)**: admite LTI para interoperabilidad con otras plataformas de LMS.
* **Integración correcta**: administra y comparte insignias externas mediante Credly.
* **Mejoras en el tablero de cumplimiento**: comparta tableros con otros administradores y establezca widgets de cumplimiento predeterminados en las páginas principales de los alumnos.
* **Compatibilidad con varios idiomas**: cree instancias específicas del idioma para los módulos de clase y clase virtual.
* **Funciones personalizadas**: control mejorado sobre las funciones y los permisos de los usuarios.
* **Comentarios de finalización**: agregue comentarios al marcar alumnos como completados.
* **Informe de grupo de usuarios**: administra grupos de usuarios con informes detallados.
* **Informe de lista de espera**: descarga la lista de alumnos en lista de espera para instancias de curso.
* **Mejoras de accesibilidad**: Compatibilidad con texto alternativo en encabezados y logotipos de empresas.
* **Compatibilidad con hindi**: Compatibilidad con el idioma de la interfaz para hindi.
* **Comprobación de blasfemias**: Bloquear publicaciones sociales que contengan palabras prohibidas.
* **Optimización de plantilla de correo electrónico**: Plantillas de correo electrónico combinadas y optimizadas para asignaciones de instructores y cancelaciones de sesiones.
* **Criterio de finalización de MS Teams**: Establece un tiempo mínimo de asistencia para las sesiones VILT.
* **Nuevos flujos de trabajo de migración**: Los cambios de migración incluyen criterios de finalización para cursos y módulos, y la migración de módulos a carpetas.

## Búsqueda basada en IA en Adobe Learning Manager

Adobe Learning Manager está renovando la forma en que los alumnos buscan cursos o formación. Introduce una capacidad de búsqueda basada en IA que combina la búsqueda léxica y semántica. La búsqueda es ahora más inteligente, ya que busca términos específicos y entiende el contexto y la intención detrás de ellos. La búsqueda avanzada comprende el significado de la consulta y proporciona resultados relevantes. Identifica el foco principal de la búsqueda para ofrecerle el conjunto de resultados más completo.

Consulte este artículo [Búsqueda avanzada](/help/migrated/learners/feature-summary/advanced-search.md) para obtener más información.

## Webhooks

Adobe Learning Manager permite la integración con Webhooks para enviar información en tiempo real, como las inscripciones en cursos, la creación de cursos y otra información, a una dirección URL específica.

Un webhook en ALM permite que una entidad envíe datos automáticamente a otra aplicación a través de HTTP. Permitirá a una aplicación proporcionar información a otras aplicaciones sin solicitarla constantemente. Por ejemplo, si un usuario completa un curso de sistema de gestión de aprendizaje (LMS), un webhook puede enviar automáticamente esa información a otra plataforma, como CRM o herramienta de creación de informes. Los webhooks se suelen utilizar en integraciones para automatizar procesos y reducir la necesidad de actualizaciones manuales entre sistemas. Configure los webhooks proporcionando una URL de devolución de llamada a la que enviar los datos.

Consulte este artículo [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md) para obtener más información.

## Interoperabilidad de herramientas de aprendizaje

Adobe Learning Manager ahora admite LTI para mejorar la interoperabilidad entre Adobe Learning Manager y otros sistemas de administración de aprendizaje (LMS).

### ¿Qué es LTI?

LTI (Learning Tools Interoperability) es un estándar que permite a herramientas de terceros y proveedores de contenido conectarse con un sistema de administración de aprendizaje (LMS). Los usuarios pueden acceder al contenido de aprendizaje externo de proveedores de contenido externos directamente en su LMS sin iniciar sesión ni navegar a otro LMS.

LTI como proveedor de herramientas: LTI como proveedor de herramientas permite la integración de sistemas externos con un LMS. Adobe Learning Manager actúa como proveedor de herramientas de LTI, lo que permite a otras plataformas de LMS acceder a cursos, certificados o rutas de aprendizaje desde Adobe Learning Manager directamente en su LMS.

LTI como consumidor de herramientas: LTI como consumidor de herramientas permite a LMS integrar herramientas externas a través de la interoperabilidad de las herramientas de aprendizaje (LTI). En este escenario, LMS es un consumidor de servicios proporcionados por herramientas externas. Adobe Learning Manager actúa como consumidor de herramientas de LTI, lo que le permite integrar herramientas de aprendizaje de terceros. Esto permite a los alumnos de Adobe Learning Manager consumir los cursos, certificados o rutas de aprendizaje de las herramientas de terceros en Adobe Learning Manager.

Consulte este artículo [Interoperabilidad de la herramienta de aprendizaje](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md) para obtener más información.

## Con Credibilidad

Con Credly, un administrador de ALM permite a los alumnos gestionar y compartir insignias externas de la plataforma en diversos canales de redes sociales.

### ¿Qué es Credly?

Credly es una plataforma de credenciales digitales que permite a los alumnos y a las organizaciones obtener, compartir y verificar logros profesionales, como insignias o certificaciones. Los alumnos pueden administrar y compartir insignias a través de su perfil de Credly en redes sociales y otros lugares.

### Integra con soltura con Adobe Learning Manager

Primero, agregue el conector de Credly en Adobe Learning Manager (ALM). A continuación, migre las insignias existentes de Credly para garantizar la continuidad de los logros de los alumnos. Por último, cree una aptitud en Adobe Learning Manager en la ruta de aprendizaje adecuada para mejorar el desarrollo y el reconocimiento del alumno.

Consulte este artículo [Credly](/help/migrated/integration-admin/feature-summary/credly-integration.md) para obtener más información

## Tablero de cumplimiento

En esta versión, los administradores ahora pueden compartir el panel con otros administradores, administradores personalizados y responsables de tienda, lo que les proporciona acceso instantáneo a los paneles de cumplimiento. Ahora pueden establecer el widget de cumplimiento predeterminado en la página de inicio del alumno, lo que permite a los alumnos realizar un seguimiento de sus requisitos de cumplimiento. Consulte este artículo [Panel de cumplimiento](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins) para obtener más información.

## Compatibilidad con varios idiomas

Adobe Learning Manager (ALM) ahora permite a los autores crear instancias específicas del idioma mediante el etiquetado de idioma para los módulos Clase y Clase virtual. Los alumnos pueden acceder a los módulos de clase real y virtual en el idioma que prefieran. Por ejemplo, un autor puede crear un módulo de clase real y virtual con dos instancias: una en inglés y otra en francés. Los alumnos pueden seleccionar las instancias en su idioma preferido.

Consulte este artículo [Añadir objetos de aprendizaje en diferentes configuraciones regionales](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging) para obtener más información.

## Funciones personalizadas

Las funciones personalizadas permiten a los administradores definir funciones y responsabilidades específicas para diferentes grupos de usuarios, lo que garantiza una mejor gestión y control. Con esta versión, ALM mejora las funciones personalizadas proporcionando un control más detallado de las siguientes secciones.

* Usuarios
* Cursos
* Rutas de aprendizaje
* Certificaciones
* Ayudas de trabajo
* Catálogos

Los administradores pueden asignar permisos precisos en función de las responsabilidades del usuario, lo que garantiza que cada grupo solo tenga acceso a las funciones y el contenido relevantes. Estos controles mejorados permiten una gestión más detallada de las secciones clave.

Inicie sesión como administrador y vaya a **[!UICONTROL Usuarios]** > **[!UICONTROL Funciones personalizadas]** para crear y administrar las funciones personalizadas.

Consulte este artículo [Funciones personalizadas](/help/migrated/administrators/feature-summary/custom-role.md) para obtener más información.

## Comentarios de finalización

Los administradores ahora pueden añadir comentarios al marcar a los alumnos como completados en cursos, rutas de aprendizaje o certificaciones. Los administradores pueden añadir comentarios para uno o varios alumnos al mismo tiempo, y los comentarios aparecen en el informe [Transcripciones de alumnos](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts).

Consulte este artículo [Comentarios de finalización](/help/migrated/administrators/feature-summary/courses.md#completion-comments) para obtener más información.

## Informe de grupo de usuarios

El nuevo **[!UICONTROL Informe de grupo de usuarios]** de Adobe Learning Manager ayuda a administrar grupos de usuarios al proporcionar visibilidad en los grupos que no se administran cuando los administradores se van. Los administradores pueden acceder a los informes en la sección **[!UICONTROL Usuarios]** > **[!UICONTROL Grupo de usuarios]**. Proporciona información detallada sobre cada grupo, incluyendo:

* Tipo de grupo de usuarios
* Nombre del grupo
* Descripción
* Creado por (nombre)
* Creado por (correo electrónico)
* Creado el (zona horaria UTC)
* Número de usuarios

Consulte este artículo [Informe de grupo de usuarios](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report) para obtener más información.

## Informe de lista de espera

El nuevo **[!UICONTROL informe de lista de espera]** de Adobe Learning Manager permite a los administradores descargar la lista de alumnos en lista de espera para todas las instancias de un curso. Los administradores e instructores pueden acceder a este informe desde la sección **[!UICONTROL Lista de espera]** de la página **[!UICONTROL Curso]** o **[!UICONTROL Descripción general de la sesión]**. El informe de lista de espera se puede descargar desde las secciones Administrador e Instructor .

Siguiendo las columnas disponibles en el informe de lista de espera:

* Nombre del curso
* Nombre de la instancia
* ID de instancia
* Estado de la instancia
* Nombre de usuario
* Correo electrónico
* ID exclusivo de usuario
* Fecha de inscripción (zona horaria UTC)
* Estado
* Número de lista de espera
* Límite de lista de espera
* Límite de puestos

Consulte estos artículos [Informe de lista de espera (administrador)](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) e [Informe de lista de espera (instructores)](/help/migrated/instructors/feature-summary/learners.md#waitlist-report) para descargar el informe de la sección de administradores e instructores.

## Accesibilidad en la página de inicio del alumno

Adobe Learning Manager ahora admite texto alternativo en todas las cabeceras para mejorar la accesibilidad de los alumnos. Esto permite a los alumnos con necesidades especiales utilizar lectores de pantalla para leer el texto alternativo y comprender la imagen. Puede seleccionar varios idiomas y proporcionar texto alternativo para cada idioma. Asegúrese de añadir el texto alternativo en los idiomas respectivos. Asegúrese de que el logotipo de la empresa de su cuenta también incluya texto alternativo con el nombre de la empresa.
Consulte este artículo [Anuncio](/help/migrated/administrators/feature-summary/announcements.md#masthead) para obtener más información.

## Compatibilidad con hindi

Adobe Learning Manager presenta ahora el hindi como uno de los idiomas de interfaz de la plataforma y apoya el crecimiento de la plataforma en India. La compatibilidad con hablantes nativos de hindi garantiza que todos los usuarios puedan acceder a todas las funciones, informes y la experiencia del usuario en general.

>[!NOTE]
>
>Los certificados de insignia generados por el sistema en formato de PDF no admiten hindi.

Para cambiar el idioma de la interfaz, siga estos pasos:

1. Inicie sesión como **[!UICONTROL administrador]**.
2. Vaya a **[!UICONTROL Configuración de perfil]** > **[!UICONTROL Idioma de interfaz]**.
3. Seleccione **[!UICONTROL Hindi]** como idioma de interfaz.


## Comprobación de blasfemias para publicaciones sociales

Adobe Learning Manager ahora bloquea las publicaciones en redes sociales de la aplicación del alumno que contengan palabras prohibidas. Esto ayuda a mantener las cosas profesionales y conformes con las normativas, especialmente en campos sensibles como la atención sanitaria.

## Optimización de plantillas de correo electrónico

### Enviar alumnos por correo electrónico cuando se asigne un instructor

Los correos electrónicos existentes **[!UICONTROL Se le ha agregado como instructor]** y **[!UICONTROL Detalles de la sesión de VCProvider]** se han combinado en un correo electrónico **[!UICONTROL Se le ha agregado como UserType]**. **[!UICONTROL UserType]** será **[!UICONTROL Instructor]** u **[!UICONTROL Organizador]**, según la función del usuario. Estos correos electrónicos no estaban disponibles en la interfaz de usuario antes. Ahora se han combinado en un solo correo electrónico y se han añadido a la interfaz de usuario. Los administradores pueden acceder a esta plantilla en la sección **[!UICONTROL Plantilla de correo electrónico]**. Se habilitará de forma predeterminada para todas las cuentas nuevas y existentes, pero los administradores pueden deshabilitarla o habilitarla desde la misma sección. Este correo electrónico se enviará siempre que se cree una sesión y se asigne un instructor, ya sea para sesiones como Zoom, Teams, Connect u otros servicios.

### Enviar un correo electrónico a los alumnos cuando se cancele una sesión

Los instructores que se eliminen de una sesión recibirán ahora solo un correo electrónico de cancelación de sesión. Anteriormente, recibían un correo electrónico de cancelación y actualización. Los instructores que permanezcan en una sesión recibirán un correo electrónico de actualización de la sesión junto con una nueva invitación para la sesión.

## Criterios de finalización de MS Teams

Actualmente, los alumnos se marcan como asistentes aunque se unan a una sesión de formación virtual con instructor (VILT) durante unos segundos. Con esta versión, hemos introducido criterios de finalización para los módulos de equipos para garantizar una asistencia más precisa. Los autores ahora pueden establecer un tiempo mínimo que los alumnos deben pasar en una sesión VILT para que se cuente su asistencia.

Se trata de una función de backend que está desactivada de forma predeterminada. Póngase en contacto con su CSM para que lo habilite.

## Cambios de migración

Se realizan los siguientes cambios en el flujo de trabajo de migración:

* Migrar módulos a carpetas específicas.
* Se han añadido criterios de finalización para los módulos.
* Se han añadido criterios de finalización para los cursos

### Cambios en la migración de módulos

Al migrar módulos a ALM, se guardarán en la carpeta pública de forma predeterminada. En esta versión, hemos agregado una nueva columna llamada `folder` en el archivo [module_version.csv](assets/module_version.csv). Los administradores pueden utilizar esta columna para especificar el nombre de la carpeta a la que deben ir los módulos después de la migración. Los administradores también pueden colocar un solo módulo en varias carpetas mostrando los nombres de las carpetas separados por comas.

La columna carpeta utiliza el tipo de datos cadena y es una columna opcional. A continuación se indican las condiciones de la columna de carpeta:

* El nombre de carpeta que agregue debe ser una carpeta de contenido existente en la cuenta de ALM.
* Los valores deben ser una cadena separada por comas.
* Si agrega un nuevo nombre de carpeta para un módulo que ya está presente en una carpeta diferente, el nuevo valor no sobrescribirá ni reemplazará la carpeta asignada. El módulo se agregará a la nueva carpeta y también permanecerá disponible en la carpeta existente.
* Si el valor está en blanco, la carpeta se establecerá de forma predeterminada en **[!UICONTROL Public]**.

Consulte el archivo csv spec](assets/4-module_version.xlsx) de [module_version para obtener más información.

### Cambios en la migración de módulos: criterios de finalización

Los administradores pueden especificar los criterios de finalización de los módulos durante la migración de módulos. En esta versión, hemos agregado nuevas columnas `completionCriteria`, `viewPercent` y `quizData` en [module_version.csv](assets/module_version.csv).

A continuación se indican las condiciones de las nuevas columnas:

1. `completionCriteria`:

   * El tipo de datos debe ser una cadena de valores y los valores admitidos son:
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Añada criterios de finalización en el nivel de módulo solo para los tipos de módulos con ritmo personalizado.
   * Los valores admitidos para el contenido estático son `LAUNCH_CONTENT` y `VIEW_PERCENT`.
   * Los valores admitidos para el contenido interactivo son `LAUNCH_CONTENT`, `VIEW_PERCENT` y `QUIZ`.
   * Los valores admitidos para el contenido de HTML5 son `LAUNCH_CONTENT` y `MARK_COMPLETE`.

2. `viewPercent`:

   * El tipo de datos de esta columna debe ser un entero y el valor debe estar entre 0 y 100.
   * Cuando criterioDeFinalización está establecido en `VIEW_PERCENT`, escriba el porcentaje de vista requerido en esta columna o déjelo en blanco.

3. `quizData`:

   * El tipo de datos debe ser una cadena de valores y los valores admitidos son `QUIZ_ATTEMPTED`, `QUIZ_PASSED` y `QUIZPASSED_OR_LIMITREACHED`.
   * Cuando `completionCriteria` esté establecido en `QUIZ`, escriba el valor de prueba adecuado en la columna `quizData`.

Consulte el archivo csv spec](assets/4-module_version.xlsx) de [module_version para obtener más información.

### Cambios en la migración de cursos: criterios de finalización

Los administradores pueden especificar los criterios de finalización de los cursos durante la migración del curso. En esta versión, hemos agregado una nueva columna llamada `completionCriteria` en [course.csv](assets/course.csv).

A continuación se indican las condiciones de la columna `completionCriteria`:

* El tipo de datos debe ser una cadena o un número, y es un campo opcional.
* Los valores deben ser `ALL`, `X` y `SELECTEDMODULES`.
* X es un valor entero que debe ser mayor que 0 y menor que el número total de módulos.
* Si establece `completionCriteria` en `SELECTEDMODULES`, debe marcar los módulos obligatorios en el archivo [course_module.csv](assets/course_module.csv).
* En la columna `optionalCriteria`, escriba `TRUE` o `FALSE`. Si establece el valor como `TRUE`, el módulo será obligatorio.

Consulte el archivo [course csv spec](assets/3-course.xlsx) y el archivo [course_module csv spec](assets/6-course_module.xlsx) para obtener más información.

## Cambios en la API

Estos son los cambios en la API:

* **API de búsqueda**:
   * Nuevo filtro de modo con opciones: classicSearch y advancedSearch.
   * Nueva opción loMetadata para snippetTypes.
* **API de anuncio**:
   * Incluye el atributo altText para las descripciones de cabecera.
* **API de instancia**:
   * Nuevo atributo de configuración regional para recuperar los detalles de configuración regional.
* **Comprobación de profanidad**:
   * API actualizadas para comprobar si hay palabras prohibidas en los comentarios y las respuestas en las publicaciones de redes sociales:
* **RPM y límite de ráfaga**:
   * Se han añadido RPM (solicitudes por minuto) y límites de fragmentación para todas las API.
* **API de insignia**:
   * Nuevo atributo externalProvider para recuperar información sobre insignias externas.
* **API de trabajos**:
   * Descargue el informe de grupos de usuarios y el informe de auditoría de funciones personalizadas mediante la API de trabajos.

### Cambios en la API de búsqueda

La API de búsqueda ahora tiene un nuevo filtro de modo con dos opciones: `classicSearch` y `advanceSearch`. También hay una nueva opción `loMetadata` para `snippetTypes`. Para obtener los mejores resultados, incluya `loMetadata` en `snippetTypes` al usar el modo `advanceSearch`.

### Cambios en la API de anuncios

`GET /announcements API` incluye ahora el atributo `altText` para proporcionar la descripción de la cabecera.

#### Ejemplo de solicitud con cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Ejemplo de respuesta:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Cambios en las API de instancias

El nuevo atributo `locale` se ha agregado a las siguientes API para recuperar los detalles de la configuración regional.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Ejemplo de solicitud con cURL:

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Ejemplo de solicitud:

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Cambios en la API pública para la comprobación de blasfemias

Las siguientes API se han actualizado para realizar comprobaciones profanas de comentarios y respuestas en publicaciones de redes sociales.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Si se encuentra una palabra restringida en la publicación, se enviará la siguiente respuesta.

#### Ejemplo de respuesta:

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Cambios en RPM y limitación de ráfagas

En esta versión, se han añadido RPM (solicitudes por minuto) y límites de ráfaga para todas las API. El RPM máximo para cada API se puede comprobar en la página Swagger.

RPM es el número de solicitudes que puede enviar al servidor de API en un minuto. El límite de ráfaga permite un mayor número de solicitudes durante un breve tiempo, superando el límite de velocidad habitual. Por ejemplo, la API `learningObject` permite un máximo de 15 solicitudes por minuto. Si se supera este límite, la API devolverá un mensaje de error.

### Cambios en las API de insignias

El nuevo atributo `externalProvider` se ha agregado a las siguientes API para recuperar información sobre insignias externas, incluidos el identificador de insignia y el nombre del proveedor.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Ejemplo de solicitud con cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Ejemplo de respuesta:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Descargar informes de auditoría de grupos de usuarios y funciones personalizadas mediante la API de trabajos

El usuario puede descargar el **[!UICONTROL Informe de grupo de usuarios]** y el **[!UICONTROL Informe de auditoría de funciones personalizadas]** mediante `Job API`.

#### Ejemplo de solicitud de descarga del informe de grupo de usuarios:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Ejemplo de solicitud de descarga del informe de auditoría de funciones personalizadas:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Mensaje de error sin cuerpo de solicitud

Hemos introducido mensajes de error específicos para los casos en los que el cuerpo de la solicitud es obligatorio, pero no se proporciona en la API.

#### Ejemplo de mensaje de error:

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Mejoras en la elaboración de informes

Los administradores pueden encontrar estos cambios de informes en la sección **Administración** > **Informes**.

### Informe Transcripciones de aprendizaje

El informe **[!UICONTROL Transcripciones de aprendizaje]** contendrá dos nuevas columnas:

* **[!UICONTROL Id. de módulo]**: muestra el identificador único de cada módulo. Esta nueva columna se ha agregado después de la columna **[!UICONTROL Module]** existente.
* **[!UICONTROL Id. de instancia del curso]**: muestra el identificador único de cada instancia del curso. Esta nueva columna se ha agregado después de la columna **[!UICONTROL Instancia]** existente.
* **[!UICONTROL Comentario de finalización]**: esta columna captura los comentarios introducidos por el administrador al marcar la finalización del usuario. Esta nueva columna se ha agregado al final del informe.


### Informe de resumen de sesión

El informe **[!UICONTROL Resumen de sesión]** contendrá tres nuevas columnas:

* Se agregó la columna **[!UICONTROL ID de módulo]** antes de la columna **[!UICONTROL Nombre de sesión]**.
* Se agregó la columna **[!UICONTROL Id. de sesión]** antes de la columna **[!UICONTROL Nombre de sesión]**.
* Se agregó la columna **[!UICONTROL Id. de instancia del curso]** después de la columna **[!UICONTROL Nombre de instancia]**.
* Se agregó la columna **[!UICONTROL Recuento de finalizaciones]** después de la columna **[!UICONTROL Recuento de inscripciones]**.

## Errores solucionados en esta actualización

* Se ha corregido el error que se producía al cargar vídeos desde el módulo de actividad durante el envío de archivos en dispositivos Android y iOS.
* Se ha corregido el problema con la apertura de cursos en la aplicación móvil; la versión web funciona correctamente.
* Se ha corregido el problema con la visualización de las ayudas de trabajo y otros recursos en Safari.
* Se ha corregido el problema que impedía a los usuarios descargar ayudas de trabajo en la aplicación móvil.
* Se ha corregido el error en la documentación de la API de usuario de Patch.
* Se ha corregido el problema por el que los organizadores no recibían notificaciones por correo electrónico cuando se eliminaba una sesión del curso.
* Se ha corregido el problema por el que los organizadores no recibían correos electrónicos de cancelación de sesiones cuando se eliminaba un módulo del curso y se volvía a publicar.
* Se ha agregado la posibilidad de incluir caracteres especiales &quot;+&quot; y &quot;-&quot; en las direcciones de correo electrónico durante la creación de usuarios externos.
* Se ha corregido el problema por el que la sincronización de informes unificados del conector de Marketo fallaba si el informe de aptitudes del usuario contenía comillas dobles en el valor de registro CSV
* Se ha corregido el problema por el que el extremo `/skills` devolvía el estado correcto para la API de administración, pero la API del alumno mostraba sistemáticamente datos incorrectos o almacenados en caché.
* Se ha corregido el problema con la incorporación de Go1 para cursos gratuitos que fallaba cuando la cuenta no tenía configurado el conector de Go1.
* Se ha corregido el problema por el que no se podía acceder a los cursos en la ruta de aprendizaje (LP) mediante la migración si el alumno ya había completado el programa de aprendizaje.
* Se ha corregido el problema por el que el archivo CSV de usuarios incrementales fallaba cuando tanto el administrador del usuario como el administrador de niveles de omisión se establecían como SU (superusuario) en lugar de administrador y no se incluían en el archivo CSV.
* Se han corregido los problemas de ámbito de los administradores de almacén en los informes del tablero.
* Se ha corregido el problema por el que xapi_iri no se eliminaba al eliminar un borrador de curso.
* Se ha corregido el problema que impedía la adición de un ID de objeto de aprendizaje único en determinados casos.
* Se ha corregido el problema por el que la propiedad IsEmbeddable del plan de aprendizaje no se actualizaba correctamente en los planes de aprendizaje compartidos.
* Se ha corregido el problema que afectaba a la visualización de la duración total de las rutas de aprendizaje en la vista del alumno.
* Se ha corregido el problema que permitía a los alumnos registrarse o registrarse a través de los vínculos de registro automático incluso después de que se hubieran eliminado sus cuentas.
* Se ha solucionado el problema por el que se eliminaba `www` al añadir vínculos en la descripción del curso durante la creación del curso.
* Se ha corregido el problema por el que las ayudas de trabajo para ocultar información y descargar no funcionaban correctamente.
* Se ha corregido el problema por el que el inicio de sesión único (SSO) no funcionaba para los nuevos usuarios añadidos mediante el vínculo de registro automático con un ID IP.
* Se ha corregido el problema por el que los datos del mensaje de notificación no se recuperaban después de eliminar un anuncio.
* Se ha corregido el problema de los resultados de búsqueda insuficientes al buscar usuarios por correo electrónico.

## Requisitos del sistema

Ver [requisitos del sistema de Adobe Learning Manager](/help/migrated/system-requirements.md).

## Versiones anteriores de Adobe Learning Manager

* [Versión de julio de 2024](/help/migrated/whats-new-july-2024.md)
* [Versión de marzo de 2024](/help/migrated/whats-new-march-2024.md)
