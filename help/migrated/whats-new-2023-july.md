---
title: Novedades de esta versión (julio de 2023)
description: Obtenga más información sobre las nuevas funciones y mejoras de Adobe Learning Manager
hidefromtoc: true
source-git-commit: c55f9448082c9971c065eec95b59992db95e53dc
workflow-type: tm+mt
source-wordcount: '2052'
ht-degree: 0%

---

# Novedades de esta versión (julio de 2023)

## Recomendaciones mejoradas

Adobe Learning Manager ha introducido un nuevo y mejorado sistema de recomendaciones para los cursos. Esta función de recomendaciones utiliza algoritmos de IA y los intereses de los usuarios, como productos, funciones y niveles, para ofrecer recomendaciones de contenido personalizadas.

Para obtener más información, consulte [Recommendations en Adobe Learning Manager](recommendations-adobe-learning-manager.md).

## Inscripción múltiple

En esta versión de Adobe Learning Manager, presentamos la inscripción múltiple para alumnos que permite a los alumnos inscribirse en más de una instancia de un curso en uno o varios períodos de tiempo.

Para obtener más información, consulte [Múltiples inscripciones](/help/migrated/authors/feature-summary/courses.md).

### Múltiples inscripciones en aplicaciones móviles o inmersivas

Los alumnos no pueden inscribirse en varias instancias desde una aplicación móvil/envolvente. La inscripción múltiple no se admite en aplicaciones móviles ni en la web móvil envolvente.

>[!NOTE]
>
>Al habilitar la inscripción múltiple, se añaden varias filas al informe de transcripciones de alumnos para cada curso (una fila para cada instancia).
>
>Si ha configurado la automatización de informes que solo prevé una fila por curso, debe realizar los ajustes necesarios en la automatización de informes antes de activar la función Inscripción múltiple.

### Formato de las insignias en una instancia de inscripción múltiple

Para admitir insignias en una instancia de inscripción múltiple, el formato de insignia se cambia a `userId_badgeId_COURSE_courseId_courseInstanceId`.

### Iniciar el reproductor en inscripción múltiple mediante un modo sin encabezado

En esta versión, hemos cambiado la biblioteca utilizada para la comunicación con el reproductor descentralizado.

En la inscripción múltiple, debe pasar los argumentos incluidos en un objeto.

```
{{startplayer(argument_object) ,
where
argument_object=
{ loId = <loId>, accountId = <accountId>, userId =<userId>, accessToken = <accessToken>, domId = <elementId>, onModuleLoaded = fn(), isMultiEnrolled=<boolean>, instanceId=<instanceId> }
}}
```

## Rechazo del conector de Exavault

Esta versión de Adobe Learning Manager incluirá un nuevo conector, que utilizará el protocolo SFTP de la familia AWS Transfer.

Este cambio también sustituirá al conector de ExaVault, que ya no estará disponible para nuevos usuarios. Puede utilizar cualquier cliente FTP de código abierto como sustituto de ExaVault. Para obtener más información, consulte [Transición desde el Administrador de FTP de Adobe](transition-from-ftp-manager.md).

## Recordatorios en Outlook para sesiones de clase y virtuales

Las sesiones de clase y de clase virtual creadas a partir de Adobe Learning Manager que se han agregado al calendario de Outlook del alumno ahora admiten recordatorios de Outlook de forma coherente (similar a los recordatorios de reuniones en Outlook).

## Mejoras en la asignación de aptitudes a los cursos

Hemos realizado mejoras en el flujo de trabajo de asignación de aptitudes para autores. La lista Sugerencias de aptitudes de la página Configuración del curso incluye ahora una función de búsqueda de escritura anticipada. Los autores ahora pueden buscar aptitudes escribiendo los primeros caracteres y las sugerencias se mostrarán en la lista desplegable Aptitud en función de la entrada. Con esta mejora, los autores no necesitan desplazarse por la lista completa para buscar y asignar aptitudes a los cursos.

## Mejoras en el flujo de trabajo de cursos aprobados por responsables

Los cursos aprobados por el responsable ahora proporcionan la información de error adecuada tanto a los responsables como a los alumnos.

![mensajes de error](assets/error-messages.png)

Los responsables ahora pueden ver los mensajes de error relevantes con información (por ejemplo, el plazo de inscripción ha pasado) cuando no pueden aprobar una solicitud de inscripción de curso. A los alumnos se les muestra el error y las medidas correctivas.

## Nuevo informe de plan de aprendizaje

Los administradores/administradores personalizados ahora pueden exportar una lista de todos los planes de aprendizaje de la cuenta y metadatos, como el estado, los grupos de usuarios aplicables, la información de activación, los cursos/rutas de aprendizaje incluidos en el plan de aprendizaje y la información de recordatorio.

## Informe para hacer un seguimiento de las próximas instancias retiradas

El informe de cursos de formación incluye una columna adicional para mostrar la fecha límite de finalización de las instancias presentes en los cursos o las rutas de aprendizaje, de modo que los administradores y los autores sepan qué instancias se retirarán y puedan tomar las medidas necesarias.

## Mejoras para capturar las valoraciones de los cursos de los alumnos

Aparecerá una ventana emergente para capturar la valoración basada en estrellas de un curso en cuanto el usuario complete el último módulo del curso.

![calificaciones](assets/ratings.png)

## Personalizar plantillas de correo electrónico

Las plantillas de correo electrónico de Learning Manager ahora incluyen secciones totalmente editables, lo que proporciona una mayor flexibilidad para personalizar las comunicaciones por correo electrónico en función de las preferencias de mensajería y marca.

Para obtener más información, consulte [Personalizar plantilla de correo electrónico](/help/migrated/administrators/feature-summary/email-templates.md#flexibility-in-customizing-the-templates).

## Mejoras en el asistente de programación

Perfecciona el proceso de selección de un instructor para sesiones de clase o virtuales. Se ha añadido un filtro de Grupo de usuarios al campo Instructor en el Asistente de programación. Los autores ahora pueden filtrar los instructores en función de sus &quot;Aptitudes del instructor&quot; y de cualquier parámetro adicional, como la ubicación, el idioma, la designación, etc.

Para obtener más información, consulte [Filtro Grupo de usuarios en el Ayudante de programación](/help/migrated/authors/feature-summary/courses.md#user-group-filter).

## Mejoras en el flujo de trabajo de retirada de objetos de aprendizaje

Los autores ahora pueden proporcionar un **Retirar automáticamente** fecha de un curso. Esto ayuda a evitar la inflación de catálogos a lo largo del tiempo y la necesidad de volver y retirar manualmente los cursos.

Los administradores también pueden decidir a nivel de cuenta la naturaleza del acceso a los objetos de aprendizaje &quot;retirados&quot;.

El informe de formación incluye una nueva columna, **Fecha de jubilación automática**, para mostrar la fecha de baja de cada objeto de aprendizaje (si se ha definido).

## Valores de etiquetas de catálogo por autores

Ahora, los autores pueden añadir sus valores para las etiquetas de catálogo al crear o editar un curso. Los administradores pueden habilitar esta función en el nivel de cuenta. Cuando un autor añade un nuevo valor de etiqueta de catálogo, este pasa a formar parte de la búsqueda de escritura anticipada.

![seleccionar catálogo](assets/select-catalog.png)

## Mejoras en la búsqueda de cursos para las funciones de administrador, autor y responsable

Se han realizado mejoras en la búsqueda de funciones de administrador, autor y responsable. Ahora podrán buscar los títulos con palabras clave. Esto se aplica a cursos, rutas de aprendizaje y certificaciones.

## Notificaciones de errores de migración

Los administradores de integración reciben una notificación por correo electrónico si se produce un error en alguna operación de importación o exportación durante la migración o al utilizar conectores de datos como PowerBI, FTP, Box, etc.

## Configuración de varios administradores mediante API

Se ha agregado una nueva API al conjunto de API de Managed Office para admitir la configuración de varios administradores.

## Mejoras en la API de inscripción

Se han realizado mejoras en la API de inscripción para admitir y optimizar las inscripciones masivas a gran escala.

## Aplicación móvil: visualización de contenido sin conexión

Los alumnos pueden descargar y utilizar contenido sin conexión. Las rutas de aprendizaje anidadas y flexibles no se admiten para la visualización sin conexión.

*En esta versión, la visualización de contenido sin conexión solo se admite para el contenido en inglés.*

## Accesibilidad

Se han implementado varias mejoras para mejorar la accesibilidad, incluidas mejoras para optimizar la legibilidad por parte de los lectores de pantalla.

## Compatibilidad con aplicaciones móviles

Con la próxima versión principal, la aplicación móvil de Adobe Learning Manager solo admitirá las tres versiones más recientes del sistema operativo móvil.

## Contenido en LinkedIn

El contenido de linkedIn no se carga del modo esperado en la aplicación envolvente del navegador Safari. Como solución alternativa, haga lo siguiente:

1. En el dispositivo, seleccione **[!UICONTROL Configuración]** > **[!UICONTROL Safari]**.
1. Desactivar **Evitar el seguimiento entre sitios**.
1. Desactivar **Bloquear todas las cookies**.
1. Inicie sesión en la aplicación envolvente.
1. Reproduzca el contenido.
1. Permitir los elementos emergentes.

## Otras mejoras

### Cambiar instancias en MS Teams

Un alumno puede cambiar a otra instancia de curso hasta que se complete y conservar el progreso del curso.

### Compatibilidad con varias inscripciones en MS Teams

Un alumno puede inscribirse en otra instancia de curso independientemente del estado de finalización de cualquier instancia anterior. Si lo hace, el alumno se inscribirá en varias instancias del mismo curso.

### Las notas del curso admiten la inscripción múltiple en MS Teams

Las notas del curso están disponibles en el nivel de instancia del curso para admitir la inscripción múltiple.

## Cambios en la API

Para obtener más información sobre los cambios en la API, consulte la [Referencia de API de Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

### Compatibilidad de API con nuevas recomendaciones

**GET/cuenta**

Devuelve si prlRecommendations está habilitado.

**Solicitar**

`https://learningmanagerstage1.adobe.com/primeapi/v2/account`

**GET /data?filter.recommendationCriteria=product**

Devuelve una lista de productos/temas. Los resultados dependen de la configuración de la cuenta, que confirma si todos los productos estarán visibles para el alumno o para el catálogo visible para los productos o temas.

**Solicitar**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=product&filter.showAllRecommenda`

**`GET /data?filter.recommendationCriteria=role`**

Devuelve una lista de roles recomendados.

**Solicitar**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=role&filter.showAllRecommendationCriteria=false`

**`GET /data?filter.recommendationCriteria=level`**

Devuelve una lista de roles recomendados.

**Solicitar**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=level&filter.showAllRecommendationCriteria=false`

**POST /search/query**

La búsqueda también incluye productos y parámetros de función en la consulta. No hay cambios en la consulta y el cuerpo. Añadiremos nuevas opciones de clasificación

**Solicitar**

`https://learningmanagerstage1.adobe.com/primeapi/v2/search/query?...`

**GET /learningObjects**

El modelo de objetos de aprendizaje devuelve recomendaciones con la etiqueta de autor si la recomendación PRL está activa.

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects?sort=recommendationScore&filter.recommendationProducts=...&filter.recommendationRoles=...&filter.excludeIgnoredRecommendations=true`

POST /learningObjects/query

Se admiten los siguientes atributos en el cuerpo de la llamada de consulta:

```javascript {line-numbers="true"}
{
  "filter.announcedGroups": [
    "string"
  ],
  "filter.bookmarks": true,
  "filter.catalogIds": [
    "string"
  ],
  "filter.cityName": [
    "string"
  ],
  "filter.duration.range": [
    "string"
  ],
  "filter.effectiveModifiedDate.fromDate": "string",
  "filter.effectiveModifiedDate.toDate": "string",
  "filter.excludeIgnoredRecommendations": true,
  "filter.ignoreEnhancedLP": true,
  "filter.ignoreHigherOrderLOEnrollment": true,
  "filter.lang.subLOs": true,
  "filter.lang.twoLetterCode": true,
  "filter.learnerState": [
    "string"
  ],
  "filter.loFormat": [
    "string"
  ],
  "filter.loTypes": [
    "string"
  ],
  "filter.price": "string",
  "filter.priceRange": [
    "string"
  ],
  "filter.recommendationLevels": [
    "string"
  ],
  "filter.skill.level": [
    "string"
  ],
  "filter.skillName": [
    "string"
  ],
  "filter.tagName": [
    "string"
  ],
  "language": [
    "string"
  ],
  "preferredSortPartitionOrder": [
    "string"
  ],
  "showLoContentSource": true,
  "useCache": true,
  "filter.recommendationProducts": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ],
  "filter.recommendationRoles": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ]
}
```

**GET /recommendationProducts**

Recupera el producto PRL por recomendación e Id. de producto.

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationProducts`

GET /recommendationRoles

Recupera el producto PRL por recomendación e Id. de producto. Solo se devolverán las funciones visibles de (objetos de aprendizaje).

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/prlRecommendations/roles`

`POST /users/{id}/recommendationPreferences`

Crea/vuelve a crear (anula) las preferencias de recomendación de PRL. Ejemplo de carga útil:

```javascript {line-numbers="true"}
{
    "data": {
        "id": "userRecommendationPreferences:14755328",
        "type": "userRecommendationPreferences",
        "attributes": {
            "products": [
                {
                    "id": "recommendationProduct:1",
                    "dateCreated": "2023-05-07T20:00:00.000Z"
                },
                {
                    "id": "recommendationProduct:37",
                    "dateCreated": "2023-05-07T21:00:00.000Z"
                }
            ],
            "roles": [
                {
                    "id": "recommendationRole:23",
                    "dateCreated": "2023-05-07'T'21:00:00.000'Z'"
                },
                {
                    "id": "recommendationRole:1",
                    "dateCreated": "2023-05-07'T'20:01:00.000'Z'"
                },
                {
                    "id": "recommendationRole:2",
                    "dateCreated": "2023-05-07'T'19:02:00.000'Z'"
                },
                 {
                    "id": "recommendationRole:3",
                    "dateCreated": "2023-05-07'T'18:02:00.000'Z'"
                },
                {
                    "id": "recommendationRole:20",
                    "dateCreated": "2023-05-07'T'17:02:00.000'Z'",
                    "levels": [
                        "INTERMEDIATE"
                    ]
                }
            ]
        }
    }
}
```

**`GET /users/{id}/recommendationPreferences`**

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2//users/123/recommendationPreferences`

**`DELETE /users/{id}/recommendationPreferences`**

Elimina las preferencias de usuario de recomendación de PRL para un producto o función.

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/users/123/recommendationPreferences?ids=recommendationRole:123,recommendationRole:234`

Parámetros :

Ids = Lista de ID que se van a eliminar

**PATCH /users/{id}/recommendationPreferences**

Adición/Actualización Parcial. Ejemplo de carga útil:

```javascript {line-numbers="true"}
{
  "data": {
    "id": "userRecommendationPreferences:<USER_ID>",
    "type": "userRecommendationPreferences",
    "attributes": {
      "roles": [
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "INTERMEDIATE"
            ]
          }
        },
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "ADVANCED"
            ]
          }
        }
      ]
    }
  }
}
```

**POST /recommendationPreferences/learningObjects/{id}/ignore**

Agregar objeto de aprendizaje a las recomendaciones bloqueadas.

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`DELETE /recommendationPreferences/learningObjects/{id}/ignore`**

Elimina objetos de aprendizaje de las recomendaciones bloqueadas.

**URL de solicitud**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`GET /users/{id}/recommendationStrips`**

Recupera todas las tiras que se utilizarán para mostrar las recomendaciones de prl

### Compatibilidad con varias inscripciones para API

**GET /primeapi/v2/account**

Se han añadido dos nuevos atributos:

* instanceSwitchEnabled
* multiEnrollmentEnabled

**GET /usuarios/{userId}/userNotifications**

Se ha añadido el ID de instancia de curso en las notificaciones del nuevo atributo de metadatos.

**GET /learningObjects**

La relación de inscripción muestra sólo la inscripción primaria, es decir, la primera inscripción o la primera finalización.

**`GET /learningObjects/{id}`**

La relación de inscripción muestra sólo la inscripción primaria, es decir, la primera inscripción o la primera finalización.

**`GET /learningObjects/{loId}/instances/{loInstanceId}`**

Se añade una nueva relación al modelo de instancia de objeto de aprendizaje.

**`GET /enrollments/{id}`**

Recuperar la inscripción de cursos con varias inscripciones.

**`DELETE /enrollments/{id}`**

Anula la inscripción de una determinada instancia de objeto de aprendizaje.

**POST /inscripciones**

Admite la inscripción en diferentes instancias.

**GET/inscripciones**

Obtiene las inscripciones sólo para las inscripciones principales del objeto de aprendizaje.

**`GET /learningObjects/{id}/note`**

Recupera una lista de notas de un curso.

**`GET /learningObjects/{lo_id}/instances/{loi_id}/note`**

Recupera una lista de notas para un curso y la instancia.

**`GET /learningObjects/{id}/resources/{loResourceId}/note`**

Recupera una lista de notas de un recurso en un curso.

**`POST /learningObjects/{id}/resources/{loResourceId}/note`**

Agrega una nota en un módulo para un curso de un curso determinado.

**`DELETE /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Elimina notas específicas de un módulo determinado en una instancia específica (parte de loResource Id).

**`GET /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Recupera una nota específica en un módulo de un curso para una instancia determinada (parte de loResourceId).

**`PATCH /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Actualiza notas específicas de un módulo determinado respecto a una instancia específica (parte de loResource Id).

**Cambios en la API de administración**

* GET /usuarios/{id}/enrollments
* POST /users/{id}/enrollments
* DELETE /users/{id}/enrollments/{enrollmentId}
* PATCH /users/{id}/enrollments/{enrollmentId}

### Campos obligatorios para puntos finales

Los productos y las funciones solo se cargan cuando se aplican.

Ejemplo de solicitud

* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course%3A7418798?enforcedFields[learningObject]=products`
* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/users/11255638/userBadges?include=model&page[offset]=0&page[limit]=10&sort=dateAchieved&enforcedFields[learningObject]=products,roles`

### Buscar cambios en la API relacionados con la implementación (idioma inglés)

La derivación es el proceso de reducir una palabra a su forma raíz. Esto garantiza que las variantes de una palabra coincidan durante una búsqueda. Por ejemplo, caminar y caminar se puede derivar a la misma palabra raíz: caminar. Una vez obtenida, una aparición de cualquiera de las palabras coincidiría con la otra en una búsqueda.

En esta versión, hemos añadido la segmentación para las configuraciones regionales en inglés, que incluye las siguientes variantes: en_US, en_AU, en_GB.

El atributo stemmed menciona si se requiere stemming en los resultados de búsqueda. De forma predeterminada, esta opción está establecida en False

### Eliminación de los puntos finales de la versión 1

Las API V1 dejarán de funcionar en esta versión. Para obtener más información, consulte la [Manual del desarrollador](/help/migrated/integration-admin/feature-summary/developer-manual.md).

### Notificaciones de inscripción o cancelación de inscripción en cursos

Esta versión introduce la compatibilidad con el ID de instancia del curso con las notificaciones en el nuevo atributo de metadatos.

### Compatibilidad con comentarios de L1

Permite al alumno proporcionar comentarios en cada nivel de instancia de la función de inscripción múltiple.

**API:** `POST /enrollments/{id}/l1Feedback`

### Lista de campos obligatorios de objeto de aprendizaje

En esta versión, debe enviar secciones, prequisiteConstraints, prerrequisitoLOs, subLOs, suplementarioResources, suplementarioLOs, instance, catalogLabels al learningObject de forma explícita.

Por ejemplo,

`enforcedFields[learningObject]=prerequisiteLOs,instances`

### Aviso de obsolescencia para la próxima versión

* Anular indicador para API de alumno.
* Cambiaremos el valor predeterminado para highlightResults=false. Además, cambiaremos el valor predeterminado de snippetType=courseName.
* Eliminaremos matchType=bool en el punto final de búsqueda.
* autoCompleteMode tiene el [Obsoleto] y para proporcionar la misma funcionalidad de autoCompleteMode =false, se ha añadido un matchType denominado Match.

### Formato de identificación de insignia con inscripción múltiple

Para admitir insignias de instancia de inscripción múltiple, estamos cambiando el formato de las insignias de curso de `userId_badgeId_COURSE_courseId to userId_badgeId_COURSE_courseId_courseInstanceId` para identificar insignias de forma exclusiva.

## Notas de la versión

Para obtener información sobre las versiones actuales y anteriores de la aplicación web y para dispositivos de Learning Manager, consulte la [Notas de la versión](/help/migrated/release-note/release-notes.md).

## Limitaciones o problemas conocidos de esta versión

Estas son las limitaciones de esta versión:

### Visualización de contenido sin conexión en la aplicación móvil

Los siguientes elementos no se admiten al ver contenido sin conexión en la aplicación:

* Cursos, planes de aprendizaje o certificaciones de Flex.
* Cursos mejorados, planes de aprendizaje o certificaciones.
* Cursos, planes de aprendizaje o certificaciones habilitados para varias pruebas.
* Harvard Manage Mentor, Content Marketplace, GetAbstract o LinkedIn Courses, Learning Plans, or Certifications.
* Planes de aprendizaje y certificados con requisitos previos activados.
* Cursos retirados, planes de aprendizaje o certificaciones.
* Cursos, planes de aprendizaje o certificaciones cuyo plazo ha vencido.
* Certificados externos.
* Cursos, planes de aprendizaje o certificaciones habilitados para el comercio electrónico.

Las siguientes rutas de aprendizaje, cursos o certificaciones tienen algunos problemas con la sincronización sin conexión:

* Todas Las Rutas De Aprendizaje
* Todos los certificados internos.
* Contenido con llamadas de POST.

### Recommendations

En el nuevo sistema de recomendaciones no se admiten los siguientes elementos para Producto/Función/Nivel:

* Adobe Experience Manager, Teams, SFDC y Sin sesión iniciada.
* La aplicación móvil no admite la edición de productos y funciones en la página Recomendación .
* La asignación no se puede realizar durante la migración.
* Etiquetado automático de LinkedIn, Tienda de contenido y otros cursos, planes de aprendizaje o certificaciones externos.
* Volver a basado en aptitudes o clásico después de activar.
* El menú de búsqueda para Productos y Funciones en la aplicación del alumno.
* Asignación masiva de cursos, planes de aprendizaje o certificaciones y usuarios en la aplicación de administración.

## Requisitos del sistema

[Requisitos del sistema de Learning Manager](/help/migrated/system-requirements.md)
