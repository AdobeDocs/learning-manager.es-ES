---
description: Descubra las nuevas funciones y mejoras, incluidos los cambios en la API y los webhooks, de la versión de agosto de 2026 de Adobe Learning Manager
jcr-language: en_us
title: Novedades de la versión de agosto de 2026 de Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 3cb62ec615254bdda4103527eb953d3433363785
workflow-type: tm+mt
source-wordcount: '2940'
ht-degree: 0%

---

# Novedades de la versión de agosto de 2026 de Adobe Learning Manager

>[!IMPORTANT]
>
>Las funciones descritas en este artículo están disponibles como parte de la versión beta. Las funciones beta de Adobe Learning Manager se proporcionan con fines de evaluación y se pueden modificar, limitar o eliminar antes de la versión de disponibilidad general. Los nombres de funciones, el comportamiento y las opciones de configuración están sujetos a cambios sin previo aviso.


## Cursos adaptables

Los cursos adaptativos te permiten ofrecer formación personalizada controlando qué módulos ve cada alumno y cuáles son necesarios, en función de los grupos de usuarios a los que pertenecen. Un solo curso presenta de forma dinámica el contenido adecuado a la persona adecuada de forma automática.

Los autores configuran cada módulo con **Optional** y **Obligatorio** para las reglas de grupos de usuarios. Los alumnos de diferentes grupos de usuarios pueden completar conjuntos de módulos completamente diferentes y seguir completando el mismo curso. Los límites de puestos para las sesiones de clase y las sesiones de clase virtual ahora se aplican en el nivel de módulo, de modo que un alumno puede inscribirse en un curso mientras está en lista de espera solo en una sesión específica. Para obtener más información, consulte [Cursos adaptables - Autor](/help/migrated/authors/feature-summary/adaptive-course-author.md)

Capacidades clave:

* Reglas de visibilidad y finalización a nivel de módulo por grupo de usuarios
* Lógica de combinación OR: si algún grupo hace que un módulo sea obligatorio, es obligatorio para ese alumno
* Lista de espera de nivel de módulo para sesiones de clase y clase virtual
* La finalización de la actualización se activa cuando cambia el perfil de un alumno
* Compatible con rutas de aprendizaje y certificaciones con limitaciones documentadas para certificaciones recurrentes

Más información sobre los cursos adaptables.

## Gradebook

Un libro de calificaciones en Adobe Learning Manager añade una puntuación ponderada a los cursos, lo que permite a los autores asignar un porcentaje de contribución a cada módulo puntuado y establecer una puntuación agregada mínima para la finalización del curso. Los alumnos pueden realizar un seguimiento de sus notas a lo largo del curso, y los administradores pueden ver las puntuaciones finales y descargar las transcripciones pertinentes.

### Qué hace el libro de calificaciones

Un curso habilitado para libro de calificaciones calcula la puntuación final de cada alumno combinando las puntuaciones de cada módulo según el porcentaje de ponderación asignado a cada módulo. Esto proporciona una medida precisa y ponderada del rendimiento en lugar de una simple suma de puntuaciones o un marcador de aprobado/suspenso basado únicamente en la finalización.

El libro de calificaciones admite dos modelos de finalización:

* **Sólo módulos requeridos**: el curso se completa cuando todos los módulos obligatorios han finalizado. Las notas del libro de calificaciones aún se calculan y son visibles, pero la puntuación agregada no contribuye a los criterios de aprobación.

* **Módulos necesarios más puntuación agregada**: el alumno debe completar todos los módulos necesarios y obtener una puntuación total igual o superior al umbral mínimo de aprobado. Ambas condiciones deben cumplirse para obtener una calificación de aprobado.

### Cómo se calculan las notas del curso

Para cada módulo puntuable, la contribución a la puntuación total del curso es:

(Puntuación conseguida ÷ Puntuación máxima) × Peso % = Contribución del módulo

La puntuación total del curso es la suma de todas las contribuciones al módulo. Los porcentajes de ponderación en todos los módulos puntuables deben sumar exactamente 100. La configuración del libro de calificaciones no se puede guardar hasta que se cumpla esta condición.

La puntuación total del curso es la suma de todas las contribuciones al módulo. Los porcentajes de ponderación en todos los módulos puntuables deben sumar exactamente 100. La configuración del libro de calificaciones no se puede guardar hasta que se cumpla esta condición.

La escala de puntuación no tiene por qué ser coherente en todos los módulos. Una sesión de clase obtuvo una puntuación de 100 y un módulo SCORM obtuvo una puntuación de 10 puede coexistir en el mismo libro de calificaciones. La fórmula normaliza cada contribución antes de aplicar la ponderación.

**Módulos con y sin puntuación**

Solo los módulos que producen una puntuación son elegibles para la ponderación. Entre los tipos de módulos puntuables se incluyen:

* Contenido SCORM, AICC y xAPI con puntuación activada
* Paquetes de contenido de Captivate
* Cuestionarios nativos en Adobe Learning Manager
* Sesiones de clase y de clase virtual en las que el instructor o el administrador introduce una puntuación
* Módulos de actividad puntuados por un instructor o administrador

Los tipos de módulos no puntuables, los archivos de PDF, los archivos de vídeo, los archivos de audio, las presentaciones de PowerPoint, los documentos de Word, los archivos de Excel y el contenido de HTML no se pueden asignar a un porcentaje de ponderación ni contribuyen a la puntuación agregada. Estos módulos pueden seguir siendo necesarios para la finalización del curso. Cuando la opción Incluir módulos que no contribuyen al grado final está activada, aparecen en el libro de calificaciones sin un valor de grosor.

Para obtener más información, consulte [Libro de calificaciones para autores](/help/migrated/authors/feature-summary/alm-author-gradebook.md)

## Carpetas de contenido jerárquico

La biblioteca de contenido ahora admite hasta tres niveles de jerarquía de carpetas privadas. Los administradores crean la estructura de carpetas y controlan qué funciones personalizadas pueden acceder a qué carpetas de nivel 1. Acceder en cascada automáticamente a todas las subcarpetas de una carpeta de nivel 1.

Los autores pueden copiar y mover contenido entre carpetas, filtrar la biblioteca de contenido por carpeta y examinar la jerarquía al añadir módulos a un curso.

Capacidades clave:

* Hasta tres niveles de anidamiento (máximo de 25 subcarpetas por elemento principal)
* Acceso basado en funciones asignado sólo en el nivel 1
* El contenido puede aparecer en varias carpetas sin duplicación
* Las carpetas públicas y la estructura de carpetas privadas se excluyen mutuamente
* Experiencia Examinar carpetas al seleccionar módulos en la creación de cursos

Para obtener más información sobre las funcionalidades de nivel de administrador, consulte [Carpetas de contenido jerárquico](/help/migrated/administrators/feature-summary/settings/advanced-settings.md#content-folder). Para obtener más información sobre las funcionalidades de nivel de autor, consulte [Carpetas de contenido jerárquico](/help/migrated/authors/feature-summary/content-library.md#add-content-to-a-folder).

Si está migrando el contenido de aprendizaje de otra plataforma a Adobe Learning Manager y desea conservar la organización de carpetas existente, puede utilizar archivos CSV para crear una estructura de carpetas jerárquica y asociar los archivos de contenido a las carpetas adecuadas. Más información sobre la migración en [Migrar la jerarquía de carpetas de contenido](/help/migrated/integration-admin/feature-summary/migration-manual.md#migratecontentfolderhierarchy)

## Centro en vivo

Live Hub es una experiencia de formación virtual basada en IA en Adobe Learning Manager que ayuda a las organizaciones a ofrecer un aprendizaje en directo atractivo e impactante. Con funciones inteligentes como las encuestas basadas en IA, la organización de salas de grupo de trabajo, los espacios de aprendizaje persistentes y la asistencia basada en IA, Live Hub aumenta la productividad del instructor al tiempo que reduce la complejidad de la entrega de sesiones.

Puntos más destacados:

* Mejora el aprendizaje en directo con una experiencia nativa de Adobe Learning Manager que mejora la calidad educativa y los resultados de los alumnos.
* Ofrece a tus instructores un cofacilitador con tecnología de IA que impulse la participación mediante encuestas inteligentes, asistencia en preguntas y respuestas e información de las salas de grupo de trabajo.
* Ayuda a tus alumnos a sacar más partido a cada sesión con resúmenes generados por IA y grabaciones de sesiones en las que se pueden realizar búsquedas por temas.
* Mide lo que importa con análisis de participación que van más allá de la asistencia para revelar una participación real en el aprendizaje.
* Ayude a los autores a utilizar el buscador de instructores basado en IA para adaptar el instructor a sus aptitudes, disponibilidad, horas preferidas, zona horaria y utilización actual.

>[!NOTE]
>
>Live Hub está actualmente en versión beta y estará disponible con la próxima versión de agosto de Adobe Learning Manager. La documentación de Live Hub estará disponible una vez que se publique la función.


## Generador de plantillas de correo electrónico basado en componentes

Ahora, las organizaciones pueden crear notificaciones de correo electrónico de marca de nivel empresarial en Adobe Learning Manager mediante un editor de componentes WYSIWYG moderno. Los administradores pueden crear un diseño global una vez, con elementos de encabezado, pie de página y marca reutilizables, y aplicarlo en todas las plantillas de correo electrónico en el nivel de cuenta. Las plantillas individuales se pueden personalizar a nivel de curso o instancia, heredando el diseño principal de forma predeterminada y reemplazándolo solo cuando sea necesario.

Capacidades clave:

* Editor WYSIWYG con una biblioteca de componentes reutilizables (texto, imagen, botón, divisor, encabezado y pie de página)
* Compatibilidad con variables: insertar campos dinámicos como el nombre del alumno, el nombre del curso y la fecha de vencimiento
* Jerarquía de plantillas vinculadas y no vinculadas: los cambios realizados en una plantilla vinculada se propagan a todas las plantillas secundarias; las plantillas no vinculadas se pueden editar independientemente
* Compatibilidad con plantillas en varios idiomas
* Previsualizar y probar-enviar antes de publicar
* Retrocompatibilidad: las plantillas de correo electrónico existentes siguen funcionando

Para obtener más información, consulte [Generador de correo electrónico basado en componentes](/help/migrated/administrators/feature-summary/email-builder.md)

## Apoyo al aprendizaje externo

Los alumnos ahora pueden enviar formación fuera de la plataforma, como certificaciones, talleres, conferencias y cursos externos, para su aprobación por parte del responsable directamente desde su panel de alumnos. Los envíos aprobados aparecen en la transcripción del alumno.

Capacidades clave:

* Formulario de envío configurable con campos estándar y personalizados
* Flujo de trabajo de revisión y aprobación de responsables con compatibilidad de comentarios
* Los envíos aprobados aparecen en la transcripción del alumno con metadatos completos
* El administrador puede configurar campos obligatorios, incluidos los personalizados
* Nuevas columnas en transcripciones de administradores y alumnos: Columnas Nombre de aprendizaje externo, Comentario de finalización y campo personalizado
* Compatibilidad con API: cinco nuevos puntos finales con ámbito de alumno para crear, recuperar y actualizar envíos

Para obtener más información a nivel de administrador, consulte [Soporte de aprendizaje externo](/help/migrated/administrators/feature-summary/settings/basic-settings.md). Para obtener más información a nivel de administrador, consulte [Soporte de aprendizaje externo](/help/migrated/managers/feature-summary/review-external-learning-requests.md). Para obtener más información a nivel de alumno, consulte [Soporte de aprendizaje externo](/help/migrated/learners/feature-summary/submit-external-learning.md).

## Funciones de IA

### Asistente de IA para los alumnos

El asistente de inteligencia artificial para alumnos ahora admite cuatro nuevas funciones, además de responder a preguntas del contenido de aprendizaje asignado:

* **Resúmenes de los cursos**: utilice el comando / para seleccionar un elemento de catálogo y generar un resumen sin abrir el curso
* **Comparación de objetos de aprendizaje**: seleccione hasta dos objetos de aprendizaje con el comando / y pida al asistente que los compare
* **Adobe Experience League responde**: el asistente ahora obtiene respuestas a preguntas de procedimiento de la documentación de ayuda de Adobe Learning Manager
* **Consultas de contenido de terceros**: Se puede consultar el contenido del catálogo de Go1 y LinkedIn Learning (solo metadatos; Sólo en inglés; la ingesta dura de 1 a 2 horas después de añadir el catálogo)

Para obtener más información, consulte [Asistente de inteligencia artificial para alumnos](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

### agente de ruta de aprendizaje

Los alumnos ahora pueden mantener una conversación guiada con el Asistente de IA para generar una ruta de aprendizaje personalizada y secuenciada en función de sus objetivos, antecedentes y tiempo disponible. La ruta de aprendizaje se crea automáticamente y el alumno se inscribe.

Capacidades clave:

* La conversación de varias vueltas guía al alumno a través de la selección de temas, la revisión de cursos y la confirmación de rutas
* Hasta cinco temas de aprendizaje sugeridos por conversación
* Selección de cursos de catálogos asignados
* Un máximo de 10 rutas de aprendizaje personalizadas visibles en la página de inicio del alumno
* Las rutas completadas se pueden compartir con los compañeros

Para obtener más información, consulte [Agente de ruta de aprendizaje](/help/migrated/learners/feature-summary/learning-path-agent.md).

### Agente de información

Insights Agent ayuda a los administradores a analizar los datos de aprendizaje mediante consultas de lenguaje natural. Haz preguntas sobre las tendencias de inscripción, las tasas de finalización, la participación de los alumnos y las carencias de habilidades. El agente genera reportes y visualizaciones en respuesta.

Para obtener más información, consulte [Insights Agent](/help/migrated/administrators/feature-summary/insights-agent.md)

### Créditos de IA de generación

Adobe Learning Manager integra funciones impulsadas por IA gestionadas mediante un sistema basado en créditos vinculado a las licencias de Agent Orchestrator. Este sistema requiere que los administradores activen funciones, establezcan límites de crédito y supervisen el uso a través de la página Facturación. La vinculación de la cuenta de Adobe Learning Manager a una organización de Adobe Admin Console con una licencia de Agent Orchestrator activa es esencial para activar las funciones de IA general.

Para obtener más información, consulte [Créditos de generación de inteligencia artificial](/help/migrated/administrators/feature-summary/billing-management.md#genaicredits)

## Canales

Los canales proporcionan una forma centralizada de organizar, publicar y descubrir contenido de vídeo desde páginas web y de confluencia. Los administradores pueden crear y administrar canales conectando páginas web compatibles o páginas de confluencia, configurando la configuración de los canales, controlando la visibilidad y sincronizando contenido desde el origen. Los alumnos pueden examinar los canales disponibles, suscribirse a canales de interés y ver contenido de vídeo seleccionado desde una única ubicación.

Para obtener más información, consulte [Crear canales](/help/migrated/administrators/feature-summary/create-channels.md)

## Generador de informes

Report Builder ofrece a los administradores una herramienta de creación de informes flexible y de autoservicio que va más allá de los tipos de informes fijos disponibles en otros lugares de Adobe Learning Manager. En lugar de limitarse a estructuras de informes predefinidas, los administradores pueden combinar campos de varios conjuntos de datos, como Usuarios, Grupos de usuarios, Cursos y rutas de aprendizaje, Módulos, Transcripciones, Catálogos y mucho más, en un único informe personalizado adaptado a las necesidades de datos específicas de su organización.

Los informes se crean una vez y se guardan para un uso repetido. No es necesario reconstruir filtros, volver a aplicar agrupaciones ni volver a unir conjuntos de datos en cada descarga. Los informes guardados se pueden descargar a petición, compartir con otros administradores o configurarse con una suscripción para que los destinatarios reciban informes actualizados automáticamente a intervalos regulares.

Para obtener más información, vea [Report Builder](/help/migrated/administrators/feature-summary/alm-report-builder.md).

## Cambios de funciones personalizadas

A los administradores personalizados se les pueden otorgar ahora capacidades de administración de usuarios ampliadas a través del nivel de permisos Avanzado en Usuarios en una definición de función personalizada.

Hay dos niveles de acceso disponibles:

| Nivel de acceso | Qué puede hacer el administrador personalizado |
|---|---|
| **Solo lectura** | Ver todas las funciones personalizadas, registros de importación y usuarios eliminados; descargar el informe de funciones personalizadas |
| **Control total** | Todas las funciones de solo lectura, además de lo siguiente: crear, editar, eliminar y asignar funciones personalizadas; importar usuarios mediante CSV; purgar usuarios eliminados |

### limitaciones

**Sólo roles creados manualmente**: Las funciones de administración de funciones personalizadas ampliadas se aplican únicamente a las funciones creadas a través de la interfaz de administrador de Adobe Learning Manager. No se admiten las funciones importadas mediante carga de CSV.

Obtenga más información sobre los cambios de función personalizados. Para obtener más información, consulta [Qué desbloquea el permiso de usuario avanzado](/help/migrated/administrators/feature-summary/custom-role.md#whatadvanceduserpermissionunlocks)

## Vínculo profundo LTI

Los administradores de integración ahora pueden habilitar la vinculación profunda de LTI para las configuraciones de la herramienta LTI, lo que permite a los autores de cursos examinar e incrustar cursos de Adobe Learning Manager directamente desde un LMS externo sin copiar manualmente las direcciones URL de los cursos.

Una vez habilitado, los autores ven un botón **Seleccionar contenido** en la configuración de actividad de LMS externo. Pueden examinar los catálogos aprobados, seleccionar cursos y confirmar la selección, con todos los campos rellenados automáticamente.

Para obtener más información, consulte [vínculos profundos LTI](/help/migrated/integration-admin/feature-summary/lti-deep-links.md).

## Ubicaciones de clases

Las ubicaciones de clase ahora admiten un **formato de ubicación de cuatro campos** estructurado, que incluye País, Estado, provincia o región, Ciudad y Nombre de ubicación, lo que facilita la administración y organización de ubicaciones de formación en todas las regiones. La actualización incluye una migración única desde el formato antiguo de campo único y agrega compatibilidad multilingüe para los campos **Nombre de ubicación** e **Información de la sala**, lo que habilita los detalles de la clase traducidos para los alumnos.

Para obtener más información, vea [Ubicaciones de clase](/help/migrated/administrators/feature-summary/classroom.md)

## Próximamente: Adobe Learning Manager Content Composer

Adobe Learning Manager Content Composer es una próxima herramienta de creación de cursos de inteligencia artificial en Adobe Learning Manager que le ayuda a crear un curso listo para publicar en apenas tiempo.

Un asistente de inteligencia artificial le guiará a través de todo el proceso: Mensaje, Resumen, Esquema y Curso, para que pueda mantener el control en cada paso, revisando y perfeccionando antes de continuar. Podrá incluir contenido en sus propios documentos de origen, aplicar temas de cursos instantáneos y compartir o exportar cursos finalizados mediante SCORM o la publicación directa en Adobe Learning Manager.

## Notificación de cambios en la versión

Obtén más información sobre los [cambios en los informes de la versión de agosto de 2026 de Adobe Learning Manager](/help/migrated/reporting-changes-august-2026.md).

## Cambios en la API en la versión

Obtén más información sobre los [cambios en la API en la versión de agosto de 2026 de Adobe Learning Manager](/help/migrated/api-changes-august-2026.md).

## Otras mejoras de la versión

| Mejora | Descripción |
|---|---|
| **MQA: Puntuación más reciente frente a la más alta** | En los módulos con varios intentos, los autores ahora pueden elegir si la puntuación de intento más reciente o más alta se registra en la transcripción del alumno y se utiliza en los cálculos del libro de calificaciones. La opción Más reciente era el valor predeterminado existente y sigue siéndolo cuando la configuración no está configurada. Para obtener más información, consulte [Libro de calificaciones para autores](/help/migrated/authors/feature-summary/alm-author-gradebook.md#configurescoresettingsmultipleattempts). |
| **Vista previa de contenido en biblioteca de contenido** | Ahora, los autores pueden obtener una vista previa de los archivos de contenido cargados directamente en la biblioteca de contenido antes de añadirlos a los cursos. Para obtener más información, consulte [Biblioteca de contenido de vista previa](/help/migrated/authors/feature-summary/content-library.md#previewcontentlibrary). |
| **Informe incremental de usuarios** | Un nuevo informe de usuario basado en API devuelve solo los usuarios creados o modificados desde la última solicitud, lo que reduce la transferencia de datos para cuentas grandes mediante flujos de trabajo automatizados de sincronización de usuarios. Para obtener más información, consulte [Informe de usuarios incrementales](/help/migrated/incremental-user-report.md). |
| **11 nuevos idiomas en el reproductor Fluidic** | El reproductor Fluidic ahora admite 11 idiomas adicionales, incluida la compatibilidad con scripts de derecha a izquierda (RTL). Para obtener más información, consulte [Reproductor Fluidic](/help/migrated/learners/feature-summary/fluidic-player.md). |
| **Migración del módulo LTI** | Los módulos existentes de LTI 1.1 ahora se pueden migrar a LTI 1.3 usando la herramienta de migración. Para obtener más información, consulte [Migración de módulos LTI](/help/migrated/integration-admin/feature-summary/migration-manual.md#migrationofltimodules). |
| **Generador de correo electrónico: Compatibilidad con el editor de texto enriquecido** | Las plantillas de correo electrónico de Adobe Learning Manager ahora admiten formato de texto enriquecido, archivos adjuntos y automatizaciones personalizadas. Para obtener más información, consulte [Generador de correo electrónico](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Generador de correo electrónico: Función de vista previa** | Puede comprobar el correo electrónico redactado para ver qué aspecto tendría en el final del destinatario mediante la opción Vista previa . Para obtener más información, consulte [Generador de correo electrónico](/help/migrated/administrators/feature-summary/email-builder.md). |
| Estandarización de la marca de tiempo **Webhook** | Todos los campos de fecha y hora del objeto `data` de las cargas webhook ahora tienen segundos establecidos en `00`, lo que proporciona una precisión de nivel de minutos coherente con los informes de transcripciones de alumnos. |
| **Mejoras de Connect** | actualizaciones del conector de Azure Data Lake Storage (ADLS); compatibilidad con nombres de sala persistentes para sesiones de clase virtual periódicas; seguimiento de la asistencia basado en la vista de grabación. |
| **Mejoras en el rendimiento del reproductor** | El reproductor de cursos fluídicos se ha optimizado para tiempos de carga más rápidos y transiciones más fluidas entre módulos. |
| **Advertencia de impacto antes de retirar cursos o programas de aprendizaje** | El autor/administrador verá una lista de advertencias de objetos de aprendizaje dependientes antes de que se pueda retirar un curso o una ruta de aprendizaje. Notifica al autor que se ha retirado un objeto de aprendizaje constitutivo. Los administradores reciben este mensaje si han creado el objeto de aprendizaje pero no tienen la función de autor. |
| **Módulo CR/VC: Duración esperada** | Los autores ahora pueden establecer una duración esperada para los módulos de clase y clase virtual, independiente de la hora de sesión programada. Este valor aparece en informes e información del curso dirigida al alumno. |
| **Confirmación antes de editar los cursos adquiridos** | Los administradores de cuentas de igual a igual ahora ven un cuadro de diálogo de confirmación antes de editar un curso adquirido a través del uso compartido de catálogos, lo que evita cambios no deseados en el contenido compartido. |
| **URL de sesión con ID de instancia** | Las direcciones URL de inicio de sesión para sesiones de Microsofts Teams, Adobe Connect y Zoom ahora incluyen el ID de instancia, lo que garantiza que los alumnos se dirijan a la sesión correcta cuando existen varias instancias. |
| **Advertencia para anuncios de gran audiencia** | Al enviar un correo electrónico de anuncio ad hoc a más de un umbral de destinatarios configurable, los administradores ahora ven una advertencia de volumen antes de enviar. |
| **Plantillas de correo electrónico: URL de cuenta para alumnos externos** | Ahora, las plantillas de notificación por correo electrónico pueden incluir una dirección URL de cuenta independiente específicamente para alumnos externos, lo que les permitirá acceder a la experiencia de inicio de sesión correcta. |
| **AEM Sites** | Ahora solo hay un botón **Editar** en la sección **Tu perfil** > Tus áreas de interés para editar tus preferencias de productos y roles y habilidades. Esto también forma parte del gestor de aprendizaje nativo. |
| **AEM Sites** | Antes había dos botones **Editar**, pero ahora el botón **Editar** es un botón consolidado para modificar tus preferencias de productos y roles y aptitudes. |
| **Zona horaria** | Se ha añadido un nuevo cuadro de búsqueda justo debajo del campo Zona horaria en Configuración de perfil del usuario que ha iniciado sesión. El cuadro de búsqueda se puede utilizar para buscar directamente una zona horaria en lugar de desplazarse por toda la lista de zonas horarias disponibles. Si desea cambiar la zona horaria existente, seleccione una nueva zona horaria y seleccione Guardar. Se guarda la nueva zona horaria. El botón Guardar sólo aparece cuando se selecciona una zona horaria. |

## Requisitos del sistema

Ver [requisitos del sistema de Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de la versión

Consulta las [notas de la versión](/help/migrated/release-note/release-notes.md) para ver las últimas actualizaciones de la versión.

## Versiones anteriores de Adobe Learning Manager

* [Versión de abril de 2026 de Adobe Learning Manager](/help/migrated/whats-new-april-2026.md)
* [Versión de octubre de 2025 de Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
