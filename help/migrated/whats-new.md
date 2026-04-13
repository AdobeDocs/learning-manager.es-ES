---
description: Descubra las nuevas funciones y mejoras, incluidos los cambios en la API y los webhooks, de la versión de abril de 2026 de Adobe Learning Manager
jcr-language: en_us
title: Novedades de la versión de abril de 2026 de Adobe Learning Manager
source-git-commit: f4ff53bf053b2c8c756961af990505d23ab22db3
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---


# Novedades de la versión de abril de 2026 de Adobe Learning Manager

**Para alumnos:** El reproductor Fluidic muestra ahora el nombre del siguiente módulo y un botón para salir. El idioma del reproductor se puede establecer mediante LTI para una experiencia coherente en todas las plataformas. El nombre del parámetro personalizado es &#39;locale&#39; y acepta el código de configuración regional. Por ejemplo, locale=fr-FR. El contenido de Captivate incluye una tabla de contenido unificada, marcas de finalización a nivel de diapositiva y exportaciones de notas fiables. Hay disponible compatibilidad con varios idiomas para las ayudas de trabajo, las preguntas de la lista de comprobación y las pistas de texto de vídeo (VTT). El Asistente de IA ayuda a los alumnos a obtener respuestas en la experiencia de aprendizaje.

**Para administradores y autores:** El conector de Zoom admite varias sesiones VILT simultáneas. Los cursos compartidos en cuentas de igual a igual muestran el autor real en lugar de &quot;Autor externo&quot;. Los administradores pueden restringir cuándo se pueden iniciar los módulos. Las fechas de caducidad de los objetos de aprendizaje se muestran en las API del alumno. Los módulos de lista de comprobación admiten la puntuación ponderada, el texto de pregunta multilingüe y los comentarios opcionales del revisor. Los certificados personalizados ofrecen un editor de arrastrar y soltar con campos dinámicos y fondos generados por IA. Experience Builder sin conexión te permite crear páginas de aprendizaje públicas sin necesidad de iniciar sesión.

**Para instructores:** Genera códigos QR para la inscripción de instancias y la asistencia a sesiones. Agregue comentarios o sugerencias durante la evaluación de la lista de comprobación.

**Informes y análisis:** El contenido de SCORM ahora puede informar de varios intentos de prueba en los informes de nivel 2. El cálculo del tiempo dedicado al aprendizaje mejora en las transcripciones de alumnos. Se actualizan los informes de transcripciones de aprendizaje para administradores. Hay disponibles mejoras de búsqueda avanzadas.

**Método de inicio de sesión:** Descubre cómo funciona el inicio de sesión de OpenID Connect en Adobe Learning Manager para alumnos, autores y administradores. OpenID Connect (OIDC) es un método de inicio de sesión común creado a partir de estándares web. Muchas organizaciones utilizan
un proveedor de identidades (por ejemplo, Okta, Google Workspace o Microsoft Entra ID) para empleados y socios.

Vea [iniciar sesión con OIDC](/help/migrated/oidc.md) para obtener más información.

## Webhooks y migración en alternativas y equivalentes

### Webhooks

Cuando un alumno finaliza un curso mediante una alternativa o relación, ALM activa un evento webhook que es independiente del webhook de finalización del curso estándar. Esto garantiza que las integraciones puedan responder de forma diferente a las finalizaciones alternativas cuando sea necesario. Los eventos Webhook también se activan cuando se produce la finalización retroactiva o la infinalización retroactiva, lo que abarca las actualizaciones históricas, así como los cambios en las relaciones.

Vea [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-alternates) para obtener más información.

### Migración

El modelo de datos basado en CSV y el comportamiento de la migración para introducir la equivalencia de objetos de aprendizaje (LO) en el sistema se describen en [Webhooks](/help/migrated/integration-admin/feature-summary/migration-manual.md#migration-for-alternates-and-equivalents).

## Purga automática de usuarios eliminados

La purga automática de usuarios eliminados es una función que purga los datos de los usuarios que ya se han eliminado en ALM. La purga se produce después de un período de retención configurable, centrado en las operaciones en bloque para que las cuentas de clientes de gran tamaño puedan gestionarse de forma eficaz sin perjudicar el rendimiento.

Vea [Purga automática de usuarios eliminados](/help/migrated/administrators/feature-summary/purge-users.md#auto-purge-of-deleted-users) para obtener más información.

## Establecer control de tiempo de acceso al módulo

La mejora permite a los autores y administradores de Adobe Learning Manager definir una ventana de tiempo durante la cual los alumnos pueden iniciar un módulo. Fuera de la ventana de inicio/finalización configurada, el módulo permanece visible en la estructura del curso, pero los alumnos no pueden iniciarlo.

Vea [Establecer control de tiempo de acceso al módulo](/help/migrated/administrators/feature-summary/module-access-time-control.md) para obtener más información.

## Cambios en las transcripciones de alumnos

Esta versión mejora el informe de transcripciones de aprendizaje (LT) con una compatibilidad y una auditabilidad más claras.

* Una nueva columna Método de finalización en el LT de administrador muestra si las finalizaciones fueron directas, alternativas o revocadas, mientras que las finalizaciones alternativas ahora influyen en el estado, la fecha de finalización y el origen de finalización mediante las fechas heredadas de los cursos de formación de origen y la actualización cuando se revocan los orígenes o se producen finalizaciones directas.
* Las alternativas revocadas ajustan automáticamente el estado, la fecha de finalización y el origen de finalización cuando se eliminan todas las relaciones de aptitud con la opción retroactiva incompleta activada.
* Los comentarios del revisor de los módulos de lista de comprobación se estandarizan en la columna Comentarios del revisor, que ahora tiene el nombre cambiado, en los LT de administrador y alumno y en todos los canales de exportación.
* Por último, los cálculos del tiempo de aprendizaje ahora distinguen mejor el tiempo activo frente al tiempo inactivo, lo que mejora la precisión de los informes de compromiso y cumplimiento.

Consulte [Cambios en el informe de transcripciones de alumnos](/help/migrated/administrators/feature-summary/reports/changes-in-learner-transcript.md) para obtener más información.

## Lista de comprobación con capacidad de comentario para el revisor

Esta función permite a los revisores añadir comentarios u opiniones durante la evaluación de la lista de comprobación. Puede proporcionar comentarios personalizados y procesables para cada alumno. También puede optar por mostrar su nombre con sus comentarios para mayor transparencia. Todos los comentarios se guardan en la transcripción del alumno y se incluyen en los informes de la lista de comprobación.

Vea [Configurar lista de comprobación con comentarios](/help/migrated/authors/feature-summary/courses.md#checklist-with-commenting) para obtener más información.

## Compatibilidad con varios idiomas para la lista de comprobación

Esta función permite crear y administrar módulos de lista de comprobación en varios idiomas. Cada pregunta, instrucción y criterio de evaluación de la lista de comprobación puede traducirse para que los revisores y los alumnos interactúen con la lista de comprobación en el idioma que prefieran. El sistema muestra la lista de comprobación en el idioma de contenido seleccionado por el usuario, lo que mejora la accesibilidad y el cumplimiento normativo para los equipos globales.

Ver [Crear lista de comprobación en varios idiomas en los módulos](/help/migrated/authors/feature-summary/courses.md#create-a-multi-language-checklist)

## Ponderación de preguntas de lista de comprobación para evaluaciones de instructores

Esta función le permite asignar puntuaciones máximas diferentes (ponderación) a cada pregunta de la lista de comprobación. Puede reflejar la diversa importancia o dificultad de cada pregunta, lo que permite realizar evaluaciones más precisas y significativas. El sistema calcula la puntuación total en función de los datos introducidos y determina si el alumno supera o no los criterios establecidos.

Ver [Crear preguntas de lista de comprobación ponderada](/help/migrated/authors/feature-summary/courses.md#how-to-create-a-weighted-checklist)

## Certificados personalizados

Los certificados personalizados en Adobe Learning Manager (ALM) permiten a los administradores y autores diseñar, administrar y emitir certificados personalizados para los alumnos.

La función incluye un editor con función de arrastrar y soltar, campos dinámicos, asistencia multilingüe y fondos generados por IA, lo que permite a las organizaciones crear certificados de marca sin conocimientos técnicos.

Ver [Diseñar certificados personalizados](/help/migrated/administrators/feature-summary/create-customize-certificate.md)

## Experiencia sin sesión iniciada en Experience Builder

La experiencia sin iniciar sesión en Experience Builder permite a las organizaciones mostrar su contenido de aprendizaje y páginas del portal a todos los visitantes, incluidos los que no han iniciado sesión. Esta función está diseñada para atraer, informar e interactuar con posibles alumnos, ya que ofrece una vista previa fluida y de marca de sus ofertas de formación antes de solicitarles que inicien sesión o se inscriban.

Ver la experiencia de [inicio de sesión no registrado en Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-experience.md)

## Mejoras de búsqueda avanzadas

Los resultados de búsqueda en la búsqueda avanzada son ahora más precisos y relevantes. Las coincidencias exactas de palabras clave ocupan un puesto más alto en la búsqueda de contenido y los metadatos, lo que facilita a los alumnos encontrar exactamente lo que están buscando.

Los alumnos ahora también pueden ver los objetos de aprendizaje inscritos en los resultados de búsqueda, incluso si no forman parte de un catálogo accesible, lo que garantiza que no se pierda ningún contenido relevante. Además, la clasificación de las ayudas de trabajo se ha mejorado tanto en la búsqueda avanzada como en la búsqueda dentro del contenido, lo que permite descubrir los recursos más relevantes más rápido.

## Ayudas de trabajo multilingües

Las ayudas de trabajo multilingües en Adobe Learning Manager (ALM) permiten a los autores y administradores proporcionar documentos de apoyo, guías o recursos en varios idiomas dentro de una única entrada de ayuda de trabajo. Los alumnos de diferentes regiones pueden acceder a los materiales relevantes en su idioma preferido, lo que mejora la comprensión, el cumplimiento normativo y la experiencia del usuario.

Vea [Agregar ayudas de trabajo multilingües](/help/migrated/authors/feature-summary/job-aids.md#create-a-multilingual-job-aid) para obtener más información.

## Compatibilidad con pistas de vídeo y texto multilingües (VTT) (para autores)

La compatibilidad con las pistas de vídeo y texto (VTT) multilingües en Adobe Learning Manager permite a los autores proporcionar subtítulos y pies de ilustración para contenido de vídeo y audio en varios idiomas. Esta función agiliza la localización, al hacer que la formación sea accesible para una audiencia global y al garantizar el cumplimiento de los estándares de accesibilidad. Los autores pueden generar, traducir, revisar y editar automáticamente archivos VTT directamente en la plataforma.

Vea [Compatibilidad con VTT multilingüe](/help/migrated/authors/feature-summary/content-library.md#multi-lingual-vtt-support) para obtener más información.

## Mostrar el autor original de los cursos compartidos en cuentas de igual a igual

Cuando se comparte un curso a través del catálogo en una cuenta de igual a igual, Adobe Learning Manager etiqueta actualmente al autor como &quot;autor externo&quot; en las vistas de alumno, administrador y autor de la cuenta receptora. Esto puede crear problemas para los alumnos y los administradores, especialmente en las grandes empresas, ya que se hace difícil identificar y ponerse en contacto con el propietario del contenido adecuado cuando surgen problemas o preguntas.

La mejora garantiza que la información del autor se conserve y aparezca en los cursos compartidos en cuentas de igual a igual, en lugar de sustituirse por un marcador de posición genérico.

### Novedades...

Mostrar el nombre del autor real de los cursos compartidos en cuentas de igual a igual

Para los cursos compartidos a través de catálogos externos o de igual a igual, el nombre del autor original de la cuenta de origen ahora se muestra en la cuenta de destino en lugar de &quot;Autor externo&quot;.

Esto se aplica a:

* Aplicación del alumno (tarjeta del curso o detalles del curso).
* Vistas de administrador y de autor al previsualizar como alumno.

Vea [Visualización del nombre del autor de los cursos compartidos](/help/migrated/administrators/feature-summary/peer-account.md#author-name-display-for-shared-courses-including-previously-acquired-courses) para obtener más información.

## Equivalentes y suplentes

Ofrece una experiencia de aprendizaje impecable y elimina la formación redundante con equivalentes y alternativos en ALM. Esta nueva capacidad permite a los administradores configurar reglas unidireccionales (alternativas) o bidireccionales (equivalentes), en las que, al completar un curso de formación, se concede automáticamente una finalización alternativa a otro. Esta función, diseñada para optimizar los grandes ecosistemas de aprendizaje, garantiza que los alumnos omitan el contenido que ya dominan y que las organizaciones reducen drásticamente las solicitudes de asistencia técnica de los administradores, eliminan las modificaciones manuales y mantienen un registro de alumno más limpio y preciso.

Vea [Equivalentes y alternativas](/help/migrated/administrators/feature-summary/alternates-equivalence.md) para obtener más información.

## Códigos QR de instructor para la inscripción de instancias y la asistencia a sesiones

Los instructores pueden generar códigos QR por sí mismos para:

* Inscripción de instancias de cursos,
* Asistencia a la sesión, o
* Inscripción + asistencia juntos

a nivel de sesión. Se ha diseñado para situaciones en las que los alumnos entran en una clase física o híbrida y requieren una opción rápida de autoservicio para inscribirse y registrar su asistencia mediante un código QR.

Vea [Descargar códigos QR de inscripción y asistencia de alumnos](/help/migrated/instructors/feature-summary/learners.md#download-qr-codes-for-learner-enrollment-and-attendance) para obtener más información.

## Invitaciones de calendario (ICS) con vínculos a sesiones

Adobe Learning Manager incluye el **vínculo de unión a sesión directamente en las invitaciones de calendario (archivos ICS)** enviadas a alumnos e instructores. Esto permite a los participantes unirse a las sesiones directamente desde su calendario sin buscar el correo electrónico de la sesión.

Esta mejora mejora la experiencia de los clientes de calendario como **Gmail** y **Outlook**.

Vea [Invitaciones de calendario con vínculos de sesión](/help/migrated/instructors/feature-summary/learners.md#joining-a-session-from-gmail) para obtener más información.

## Asistente de IA para los alumnos

El Asistente de inteligencia artificial (Beta) para alumnos les ayuda a encontrar rápidamente respuestas del contenido de aprendizaje asignado sin tener que explorar cursos completos. Puede hacer preguntas en un lenguaje sencillo y recibir respuestas precisas y centradas con vínculos de origen al contenido relevante del curso.

Las capacidades, los escenarios compatibles y las limitaciones pueden cambiar a medida que evoluciona la función. El Asistente de IA es un compañero de chat generativo basado en IA en Adobe Learning Manager que ofrece respuestas rápidas y precisas utilizando su contenido de aprendizaje de confianza. Incluye citas para que siempre conozca la fuente de la información.

Ver [Asistente de inteligencia artificial para alumnos](/help/migrated/learners/feature-summary/learner-ai-assistant.md)


## Cambios en la API en la versión

La versión de abril de 2026 de Adobe Learning Manager introduce mejoras específicas en la API pública en torno a alternativas y equivalentes, acceso al contenido con ventana de tiempo, intentos de cuestionario basados en contenido, experiencias sin inicio de sesión y gestión de ayudas de trabajo. Los cambios están diseñados para ser en gran medida compatibles con versiones anteriores, al tiempo que permiten integraciones más precisas.

Ver [cambios en la API en la versión de abril](/help/migrated/api-changes-alm.md)

## Requisitos del sistema

Ver [requisitos del sistema de Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de la versión

Consulta las [notas de la versión](/help/migrated/release-note/release-notes.md) para ver las últimas actualizaciones de la versión.

## Versiones anteriores de Adobe Learning Manager

* [Versión de octubre de 2025 de Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
* [Versión de mayo de 2025 de Adobe Learning Manager](/help/migrated/whats-new-may-2025.md)
