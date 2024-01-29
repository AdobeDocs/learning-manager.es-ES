---
title: Novedades de esta versión (noviembre de 2022)
description: Obtenga más información sobre las nuevas funciones y mejoras de Adobe Learning Manager
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 0%

---

# Novedades de esta versión (noviembre de 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Configuración de SSO múltiple

Adobe Learning Manager admite actualmente un método de inicio de sesión para usuarios internos y otro para usuarios externos. Esto crea limitaciones en los casos en los que los clientes tienen sus empleados y sus propios clientes y socios de canal en la misma cuenta.

Con la intención de admitir varios tipos de grupos de usuarios que inicien sesión en la plataforma, Adobe Learning Manager ahora admite varios métodos de inicio de sesión a través de varias configuraciones de SSO tanto para usuarios internos como externos.

Para obtener más información, consulte [Varios inicios de sesión de SSO](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

## Compatibilidad con funciones no registradas

El portal nativo de Adobe Learning Manager ahora admite el acceso no registrado a un portal de formación.

Los alumnos ahora pueden descubrir el sitio de formación y acceder a él, consultar los distintos cursos y contenidos disponibles y decidir iniciar sesión para consumir los cursos.

Esta función facilita la creación de un portal de aprendizaje orientado al cliente, en el que los alumnos pueden explorar varios cursos sin tener que iniciar sesión inicialmente.

Para obtener más información, consulte [Experiencia de inicio de sesión no registrado para alumnos](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md).

## Mejoras de la página Resumen de formación

La página Resumen de formación ahora incluye una interfaz de usuario renovada para que los alumnos tengan una experiencia mejorada mientras consumen un curso.

Otras mejoras incluyen:

* Marcar un curso de formación.
* Recomendación de cursos relacionados.
* Información de rutas de aprendizaje para cursos y rutas de aprendizaje.
* Nombres de autores en los que se puede hacer clic.
* Rastros para facilitar la navegación.

## Mejoras de la página Resumen de formación

La página Resumen de formación ahora incluye una interfaz de usuario renovada para que los alumnos tengan una experiencia mejorada mientras consumen un curso.

Otras mejoras incluyen:

* Marcar un curso de formación.
* Recomendación de cursos relacionados.
* Información de rutas de aprendizaje para cursos y rutas de aprendizaje.
* Nombres de autores en los que se puede hacer clic.
* Rastros para facilitar la navegación.

## Página Perfil de autor

La página de perfil del autor muestra toda la formación creada por un autor determinado.

Los alumnos pueden encontrar fácilmente información específica del autor y todos los cursos de formación creados por este.

## Cursos de formación marcados

Los alumnos pueden guardar (con el botón Guardar) o marcar cursos de formación para ellos desde el mosaico del curso o la página de resumen. Todos los cursos marcados están disponibles en la página de inicio del alumno.

## Personalización del reproductor

En esta versión, puede personalizar el reproductor Fluidic para que coincida con los requisitos de marca de un curso.

Puede mostrar y ocultar varias opciones y ajustes del reproductor en función de los requisitos de contenido y otorgar control a los alumnos en función del tipo de contenido. Puede aplicar este cambio a las implementaciones nativas y descentralizadas.

Las opciones que puede cambiar son las siguientes:

* Alternar tabla de contenido
* Notas
* Idioma
* Velocidad
* Leyenda
* Volumen
* Controles de reproducción

## Suplantación del alumno y el responsable

Los administradores pueden iniciar una sesión suplantada en la que pueden iniciar sesión en nombre de cualquier usuario de su cuenta con la función de alumno y responsable.

Para obtener más información, consulte [Suplantación del alumno y el responsable](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md).

## Otras mejoras

### Registro de auditoría de correos electrónicos

Los administradores ahora pueden acceder a todos los registros de correo electrónico enviados desde el sistema mediante un informe de seguimiento de auditoría de correo electrónico.

Este registro captura todos los datos relacionados con los correos electrónicos enviados en los últimos 30 días y se actualiza todos los días. Además, el informe contiene información, por ejemplo, estado entregado, remitente, receptor, asunto y metadatos de contenido.

Descargue el informe desde Informes > Informes personalizados > Informes de Excel > Informe de correos electrónicos. Aparece una notificación a través de la cual puede descargar el informe.

Este informe consta de los siguientes campos:

* Hora desencadenada por correo electrónico (zona horaria UTC)
* Hora del último estado del evento (zona horaria UTC)
* Estado de entrega
* Correo electrónico del receptor
* Seudónimo del remitente
* Email Subject
* Tipo de entidad
* Nombre de entidad
* ID de entidad

### Notificación de alumno en lista de espera

Cuando un autor añade una nueva instancia, puede activar un correo electrónico para notificar a los alumnos en lista de espera de otras instancias. Los alumnos recibirán un correo electrónico del cambio.

### Plantillas de correo electrónico de nivel de instancia

Puede personalizar los mensajes de correo electrónico para cada instancia de un curso de formación.

Siempre que se permita al autor o al administrador añadir una nueva instancia, se podrá editar la plantilla de una instancia individual.

Por ejemplo, si un curso tiene diferentes tipos de audiencia, puede cambiar la plantilla de correo electrónico según corresponda.

![plantillas de correo electrónico](assets/email-template.png)

La prioridad de la plantilla se enumera a continuación:

1. Plantilla de nivel de instancia
2. Plantilla de nivel de formación
3. Plantilla de nivel de cuenta

### Comentarios del instructor al aceptar envíos

Los instructores ahora pueden añadir comentarios al aceptar los envíos realizados por los alumnos. El alumno recibe una notificación por correo electrónico y una notificación en la aplicación (si se activa) una vez que el instructor aprueba el envío. Los comentarios relacionados con el envío están presentes en las transcripciones de alumnos tanto para el administrador como para el alumno.

### Mejoras relacionadas con la búsqueda

Aparece el historial de búsquedas recientes de un alumno para que pueda ver todas las búsquedas anteriores.

Los resultados de la búsqueda son ahora consistentes en todo el aprendizaje formal e informal (aprendizaje social). Los resultados incluyen formación, aprendizaje social y correspondencia de la tienda de contenidos.

La búsqueda está más centrada y orientada, y puede ver los resultados de búsqueda en tres lugares: aprendizaje formal, aprendizaje social y Mercado de contenido.

![buscar](assets/search-image.png)

#### Búsqueda basada en frases

En esta versión de Adobe Learning Manager, hemos sustituido la búsqueda de escritura anticipada por la búsqueda basada en frases.

#### Búsquedas recientes de

Un alumno solo puede ver sus búsquedas recientes en la sesión actual.

### Catálogo de cursos gratuitos de Content Marketplace

Ya está disponible en la tienda de contenido un conjunto de 50 cursos gratuitos, seleccionados y de alta calidad, para que los alumnos puedan verlos.

### Compatibilidad con el idioma indonesio

Bahasa Indonesia se ha añadido como idioma de interfaz en las aplicaciones de alumno y responsable.

### Campo Autor obligatorio

Al crear un curso, el campo Autor es obligatorio.

### Cambios en Mercado de contenido

* Las cuentas de prueba recién creadas enumerarán un nuevo catálogo para 50 cursos gratuitos en Mercado de contenido, que están disponibles para los usuarios.
* Un alumno puede ver ahora el número de resultados de búsqueda y vínculos incrustados para redirigir a Mercado de contenido.

### Cambios envolventes en dispositivos móviles

En esta versión, los usuarios web envolventes de dispositivos móviles pueden realizar las tareas que se indican a continuación:

* Crear: publicaciones de encuesta
* Editar publicación: todos los tipos, RTE
* Flujo de trabajo de comercio electrónico.
* Vista previa de un módulo: los alumnos tendrán la función Vista previa del módulo en Envolvente para dispositivos móviles. Este cambio permitirá a los alumnos obtener una vista previa del módulo antes de inscribirse en un curso.
* Copiar una URL.
* Eliminar un tablero.

### Cambios en el conector de Zoom

El tipo de aplicación JWT dejará de utilizarse en junio de 2023. Le recomendamos que cree aplicaciones de OAuth o OAuth de servidor a servidor para reemplazar la funcionalidad de una aplicación JWT en su cuenta.

### Informe de interacción

En esta versión, obtendrá acceso a un informe que muestra varios cursos en los que se ha habilitado la interacción.

### Importar preferencias de idioma mediante CSV

Al importar un archivo CSV, el archivo CSV contiene los campos Idioma de la interfaz, Idioma del contenido y Zona horaria.

El administrador también puede exportar el informe, que contiene los mismos campos anteriores.

* Idioma de interfaz
* Idioma del contenido
* Zona horaria

Además de los administradores, un administrador personalizado también puede exportar este informe.

![informe de idioma](assets/language-report.png)

#### Impacto en la localización

* Los nombres de columna no se pueden localizar y deben ser como son (idioma de interfaz, idioma de contenido, zona horaria).
* Los códigos locales no distinguen entre mayúsculas y minúsculas.
* Si bien no hay restricciones a la hora de proporcionar el código de país, solo puede especificar el código de idioma. Por ejemplo, tanto &quot;it_IT&quot; como &quot;it&quot; son válidos.
* Si hay alguna discrepancia en el informe debido a un código de configuración regional incorrecto, el procesamiento del archivo .csv continúa, como de costumbre, y no afecta a los demás registros del archivo .csv. La preferencia de configuración regional del usuario con una configuración regional incorrecta no se actualiza. El resto de los datos se actualizan.

## Cambios y mejoras de la API

### Conectores de VC

Si se utiliza un ID de correo electrónico de administrador para configurar el conector de clase virtual, ese administrador en particular debe tener permiso para lo siguiente:

* Creación de una reunión
* Actualizar una reunión
* Obteniendo informe de asistencia

Al crear o actualizar la reunión de clase virtual, los instructores deben FINALIZAR la reunión en un plazo de 30 minutos desde la hora de finalización programada de la reunión.

### Marcadores

Se han añadido las siguientes API para marcar un curso en la página Resumen de formación:

* Obtener todos los marcadores: `primeapi/v2/bookmarks`
* Crear un marcador: `primeapi/v2/learningObjects/{id}/bookmark`
* Eliminar un marcador: `primeapi/v2/learningObjects/{id}/bookmark`

### Compatibilidad con contenido y metadatos multicocales mediante la migración

Para todos los tipos de formación admitidos en la plataforma (curso, rutas de aprendizaje, módulos, certificaciones y ayudas de trabajo), ahora se puede admitir la migración de varios idiomas a través de archivos CSV utilizando columnas adicionales para idiomas adicionales.

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

#### Especificación de CSV

Adobe Learning Manager le proporciona un conjunto de especificaciones CSV estándar para la migración habilitada en varias configuraciones regionales. La práctica recomendada es revisar estas especificaciones de CSV antes de comenzar con el proceso de migración. El administrador de integración de su organización puede analizar los formatos de datos existentes y asignarlos para que coincidan con los elementos de plantilla CSV proporcionados por Learning Manager.

#### Cambios con compatibilidad multilocal

* La columna module_version no se admite en module_version.csv ni course_module.csv.
* No se puede actualizar module_version en la misma ejecución (en la misma ejecución, el módulo no se puede migrar con dos versiones con el mismo módulo).
* La actualización de contenido o metadatos se considera una actualización de la versión del módulo desde module_version.csv.
* No se puede admitir la actualización de Job_Aid_Version mediante job_aid_version.csv

### Revocar tokens de autenticación y cookies

Una aplicación de LMS descentralizada se hace con el token_de_actualización la primera vez que se inicia sesión. Posteriormente, refresh_token se utiliza para generar access_token para que sus aplicaciones cliente realicen llamadas a la API. Del mismo modo, la reproducción de contenido utiliza el extremo de OAuth para generar cookies para administrar la reproducción, lo que implica varios archivos de contenido y llamadas de API invocadas por esos archivos mediante cookies. La cookie generada por oauth tiene la misma validez que access_token, que es de siete días. Una vez generada la cookie, no hay forma de borrarla, a diferencia del típico cierre de sesión de la aplicación web. La cookie de Oauth y la cookie de la aplicación web son dos cookies diferentes y no se conocen entre sí.

Por lo tanto, para borrar la cookie, hemos introducido un nuevo punto final, que revoca el token de actualización, la cookie y tanto la cookie como el token de actualización.

**Detalles**

**Extremo**

`POST oauth/o/revoke`

**Parámetros de consulta**

* `cookie=true|false` - indica que la cookie debe ser revocada
* `refresh_token=true|false` - indica que actualizar

**Cuerpo de solicitud**

Cuerpo necesario para revocar el token de actualización o (token de actualización y cookie)

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

### API hechas públicas

En esta versión, hemos hecho públicas algunas API.

| API | Tipo | Descripción |
|---|---|---|
| /social/search | GET | Busca en redes sociales. |
| /anuncios | GET | Obtenga información detallada sobre el anuncio en la cabecera asignada al alumno. |
| /anuncios/`{id}` | GET | Obtenga información detallada sobre el anuncio en la cabecera asignada al alumno. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | URL de carga del archivo para loResource de resourceType &#39;Activity&#39; donde se requiere el envío del archivo. |
| /jobAid/`{jobAidId}`/jobAidDownloaded | GET | Establecer informe de descarga de ayuda de trabajo. |
| /bulkimport/startrun | POST | Ejecute la importación masiva. |
| /bulkimport/cansync | GET | Sincroniza la importación masiva. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Obtener información relacionada con la actualización de contenido. |
| /uploadSigner | GET | Obtenga la firma del contenido de to_sign. |
| /avatar | POST | Actualiza la imagen del avatar del alumno con una nueva imagen. |
| /avatar | DELETE | Elimina la imagen de avatar del alumno. |

### Aplicación Salesforce

La **Omitir pedido superior LO** Esta opción debe estar activada en la aplicación Salesforce para que todos los cursos, programas de aprendizaje y certificados se puedan ver al mismo tiempo.

### API para la personalización de reproductores

En esta versión, hemos proporcionado API para personalizar un reproductor. Puede:

* Inicie o cargue el reproductor.
* Desplácese a un módulo determinado.
* Alternar tabla de contenido.
* Cambiar idioma.
* Cierre el reproductor.
* Reproducir, pausar, avanzar, retroceder, buscar, cambiar volumen o cambiar velocidad.
* Capturar eventos emitidos por el reproductor.

### Mostrar la posición de la lista de espera de un alumno

La GET /enrollments/{id}La API /waitlistPosition de la API LO recupera la posición de lista de espera de un usuario para una inscripción especificada.

### Fecha de finalización de envío en certificaciones externas

La API /primeapi/v2/learningObjects/certification:xxxxx tendrá el atributo &quot;completedDateSameAsApprovalDate&quot; para indicar que el certificado tiene habilitada la &quot;Fecha de finalización de certificación&quot; para el alumno, o no, junto con el indicador verdadero/falso.

### Obtener datos de vista previa de objetos

El GET /preview/learningObjects/{id} La API se añade a Obtener información de vista previa sobre un objeto de aprendizaje.

### Mover usuarios externos dentro de perfiles

La `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` Esta llamada ayuda a mover un usuario a otro perfil externo especificando un nuevo id. de perfil externo.

### Añadir usuarios a perfiles externos

La `POST /externalProfiles/{id}/users` añade usuarios externos a un perfil externo.

## Notas de la versión

Para obtener información sobre las versiones actuales y anteriores de la aplicación web y para dispositivos de Learning Manager, consulte la [Notas de la versión](/help/migrated/release-note/release-notes.md).

## Correcciones de errores

Para ver los errores que se han solucionado en esta actualización, consulte la [Lista de errores corregidos](release-note/release-notes.md#bugs-fixed-in-this-release).

## Requisitos del sistema

[Requisitos del sistema de Learning Manager](/help/migrated/system-requirements.md)
