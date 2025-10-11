---
description: Descubra las nuevas funciones y mejoras de la versión de octubre de 2025 de Adobe Learning Manager
jcr-language: en_us
title: Novedades de la versión de octubre de 2025 de Adobe Learning Manager
source-git-commit: 5d50bd56b6663b26fc6db0ff33d19ad809e9bf6a
workflow-type: tm+mt
source-wordcount: '5638'
ht-degree: 0%

---


# Novedades de la versión de octubre de 2025 de Adobe Learning Manager

La versión de octubre de 2025 de Adobe Learning Manager presenta importantes mejoras diseñadas para mejorar la precisión de los informes, expandir las capacidades de integración y mejorar la experiencia de aprendizaje para administradores, autores y alumnos.

* Experience Builder: diseña portales de aprendizaje totalmente de marca y basados en funciones que se adapten a las necesidades de tu organización. Crea portales de aprendizaje basados en funciones y de marca con widgets, menús y páginas.
* Etiquetado social en tableros de aprendizaje: los alumnos ahora pueden etiquetar a sus compañeros con @username en publicaciones y comentarios, lo que permite la colaboración dirigida y las notificaciones dentro de las comunidades de aprendizaje social.
* Permisos de anuncios con ámbito: los administradores personalizados pueden crear anuncios limitados a sus grupos de usuarios o catálogos asignados, lo que garantiza una comunicación dirigida y reduce la sobrecarga de información.
* Seguimiento del progreso basado en el idioma: El progreso del alumno ahora se guarda de forma independiente para cada configuración regional, lo que permite un cambio fluido entre los idiomas sin perder el progreso.
* Administración incremental de funciones personalizadas: los administradores ahora pueden administrar funciones personalizadas de forma más eficaz con compatibilidad para importaciones incrementales y multiincrementales en Adobe Learning Manager.
* API mejoradas para el análisis y la migración: las API nuevas y mejoradas proporcionan un mejor seguimiento del rendimiento de las pruebas, supervisión del estado de la migración y compatibilidad con el etiquetado de usuarios en el aprendizaje social.

## Experience Builder

>[!IMPORTANT]
>
>Nos complace anunciar que Experience Builder, la innovadora herramienta para crear portales de aprendizaje personalizables, estará disponible tras la versión de octubre de 2025 de Adobe Learning Manager.
>
>Mantente atento a más actualizaciones a medida que nos acercamos a la fecha de lanzamiento. Esperamos ver cómo utilizas Experience Builder para transformar tus portales de aprendizaje.
>
>Si tiene alguna pregunta o desea obtener información adicional, póngase en contacto con el administrador de éxito de clientes.

Experience Builder es una herramienta sin código/de código bajo en Adobe Learning Manager que te ayuda a crear portales de aprendizaje personalizados. Te permite diseñar portales de aprendizaje de marca y fáciles de usar sin necesidad de conocimientos técnicos o amplios conocimientos de codificación.
Con Experience Builder, los administradores pueden crear páginas, menús y widgets con facilidad para ofrecer experiencias de aprendizaje personalizadas adaptadas a su audiencia.

Antes de utilizar Experience Builder, las organizaciones se enfrentaban a varios desafíos:

1. **Personalización limitada**: los portales tenían diseños fijos con pocas opciones para reflejar tu marca. Los administradores solo podían realizar cambios básicos, como modificar encabezados, pies de página o colores, lo que limitaba la capacidad de crear experiencias únicas.
2. **Costo**: para crear portales personalizados, se requieren desarrolladores caros y cronologías largas, que a menudo tardan de 6 a 9 meses en completarse. Este enfoque aumentó el costo total de propiedad y el retraso en el despliegue.
3. **Experiencias genéricas**: Todos vieron el mismo contenido, incluso si no era relevante para su función o necesidades. Esta falta de personalización redujo la participación y la satisfacción del alumno.
4. **Barreras técnicas**: Los administradores no técnicos tuvieron problemas para crear o actualizar portales porque necesitaban conocimientos de codificación o asistencia externa.

Experience Builder resuelve estos problemas proporcionando una solución sencilla, sin código y código bajo para crear portales personalizados y de marca.

Permite a los administradores diseñar portales que satisfagan las necesidades de su organización sin tener que recurrir a expertos técnicos o desarrolladores externos.

**Casos prácticos**

* **Portales de marca**: Crea un portal que combine el sitio web de tu empresa con logotipos, colores y diseños. Por ejemplo, una empresa del sector sanitario puede diseñar un portal que refleje su marca corporativa mientras distribuye contenido de aprendizaje.
* **Aprendizaje basado en funciones**: Crea páginas adaptadas a funciones específicas. Los equipos de ventas pueden ver la formación sobre los productos, mientras que los ingenieros acceden a los cursos técnicos.
* **Formación sobre productos**: configura páginas dedicadas para diferentes productos, como Photoshop o Illustrator, con widgets que muestren cursos, certificaciones y recursos relacionados.

Consulta [Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/overview.md) para obtener más información sobre la creación de páginas personalizadas mediante widgets.

## Progreso del alumno basado en el idioma

Actualmente, Adobe Learning Manager solo realiza el seguimiento del progreso del alumno para el idioma local seleccionado, lo que provoca una pérdida de progreso significativa al cambiar de idioma o configuración regional en el reproductor. Esta limitación puede provocar una experiencia de usuario deficiente, ya que los alumnos pueden perder su progreso al acceder al contenido en diferentes idiomas. El progreso de cada módulo del reproductor se supervisa tanto en el nivel de usuario como en el de módulo. Esto da lugar a una situación en la que el progreso de un usuario se anula cuando vuelve a una configuración regional utilizada anteriormente para el mismo módulo.

Por ejemplo, si un alumno consigue un progreso del 75 % en la configuración regional A (inglés) y, a continuación, cambia a la configuración regional B (español), al volver a la configuración regional A, el progreso se restablece en el 0 % en lugar de reanudarse a partir del 75 %.

Para resolver estas limitaciones, la función se ha mejorado para admitir el seguimiento del progreso específico de la configuración regional:

* **Almacenamiento específico de la configuración regional**: cuando un alumno cambia la configuración regional (por ejemplo, de la configuración regional A a la B) dentro del reproductor, ahora Adobe Learning Manager guarda el estado de progreso por separado para cada configuración regional del contenido.
* **Reanudación del progreso**: cuando el usuario vuelve a una configuración regional utilizada anteriormente (de la configuración regional B a la A), el contenido se reanuda desde el punto en el que se detuvo en esa configuración regional específica.
* **Seguimiento independiente del progreso**: cada configuración regional mantiene su propio estado de progreso, lo que permite a los alumnos explorar el contenido en varios idiomas sin perder el progreso individual en cada idioma.

Los siguientes tipos de contenido no se admiten para el progreso del alumno según el idioma:

* El contenido de vídeo y audio no es compatible.
* El contenido de terceros, incluidos Go1, LinkedIn Learning, getAbstract y Harvard ManageMentor, no es compatible.
* El progreso del contenido que no envía datos al almacén de registros de aprendizaje (LRS) no se registrará ni se guardará.
* Los usuarios de aplicaciones móviles no pueden realizar un seguimiento del progreso de esta función en modo sin conexión.

Consulta [Mi aprendizaje](/help/migrated/learners/feature-summary/courses.md#language-based-progress-management) para obtener más información sobre el progreso de los alumnos según el idioma.

## Compatibilidad incremental y multiincremental para funciones personalizadas

Adobe Learning Manager ahora admite importaciones incrementales y multiincrementales para roles personalizados y asignaciones de roles. Con las importaciones incrementales, los administradores solo pueden cargar registros nuevos, actualizados o eliminados de los usuarios en lugar de volver a cargar el archivo CSV completo.

Las importaciones multiincrementales amplían esta capacidad al permitir a las grandes organizaciones dividir los archivos incrementales por región o departamento (por ejemplo, EE. UU., UE, APAC) y procesarlos en paralelo. Adobe Learning Manager también admite hasta 20 archivos CSV de usuarios incrementales y sus correspondientes funciones personalizadas, lo que los hace escalables para grandes operaciones.

Los administradores ahora pueden cargar archivos de roles y roles de usuario (role.csv y user_role.csv) de forma incremental, junto con archivos de usuario (user.csv), en lugar de realizar siempre cargas completas. Cada importación de usuarios (user1.csv) está vinculada con sus propios archivos de asignación de funciones (user1_role.csv, user1_user_role.csv), almacenados en carpetas FTP independientes.

Se han añadido las siguientes tres columnas adicionales a los siguientes archivos CSV:

* Estado de registro del usuario (user.csv): indica el estado de registro actual del usuario en el sistema (por ejemplo, activo, inactivo o eliminado).
* Estado de la función (role.csv): indica si una función personalizada está activa o inactiva en la cuenta.
* Estado de la función de usuario (user_role.csv): define el estado de la asignación entre un usuario y una función, y muestra si la asignación está activa o se ha eliminado.

Ahora, Adobe Learning Manager captura las acciones de adición, actualización y eliminación en los informes de auditoría de usuarios y de funciones personalizadas, lo que proporciona a los administradores una mayor visibilidad de los cambios.

>[!NOTE]
>
>Estos cambios solo se aplican a las cuentas que utilizan usuarios incrementales.

Vea [Compatibilidad incremental y multiincremental para funciones personalizadas](/help/migrated/integration-admin/feature-summary/configure-role-csv-files.md#incremental-and-multi-incremental-support-for-custom-roles) para obtener más información sobre la compatibilidad incremental y multiincremental para funciones personalizadas.

## Mejoras en la integración con Go1

La integración de Go1 se ha mejorado para permitir la selección directa de cursos de Go1 para crear programas de aprendizaje (LP) en Adobe Learning Manager. Esta actualización admite la inclusión de cursos de Go1 en certificaciones recurrentes e introduce una nueva versión de la experiencia del centro de contenido de Go1, lo que permite una gestión de cursos más eficaz.

* Cree y administre listas de reproducción directamente en Go1 mediante la asistencia por chat de IA o la selección manual.
* Incluye cursos de Go1 en ciclos de certificación recurrentes con restablecimiento automático del progreso. Vea [Certificaciones](/help/migrated/administrators/feature-summary/certifications.md) para obtener más información sobre la creación de certificados.
* Se ha actualizado la interfaz de detección de contenido para mejorar la exploración y la selección de contenido.

**Notas importantes**

* Todas las funciones de Go1 requieren una licencia de Go1 activa.
* El contenido gratuito anterior de Go1 se retirará. Las organizaciones deben obtener una vista previa y comprar los paquetes de contenido necesarios.
* Los administradores y los autores pueden crear y administrar listas de reproducción; los alumnos mantienen el acceso de solo vista.

Consulte [Conservar cursos de Go1 en la ruta de aprendizaje](/help/migrated/administrators/feature-summary/content-marketplace/curate-go1-playlist.md) para obtener más información sobre cómo agregar cursos de Go1 a la ruta de aprendizaje.

## Compatibilidad con URL de vídeo en el módulo de actividad

El módulo Actividad ahora admite la incrustación de direcciones URL de Vimeo, de forma similar a las incrustaciones de YouTube. Esta mejora permite a los administradores añadir vínculos de vídeo de Vimeo directamente en el módulo de actividad. Cuando los autores crean un curso y agregan un módulo de actividad, ahora ven una opción para incluir una URL de Vimeo. De forma similar a como se añaden los vínculos de YouTube, los autores pueden pegar un vínculo de Vimeo directamente en la configuración del módulo. Una vez publicado, los alumnos pueden reproducir el vídeo de Vimeo sin problemas dentro de la aplicación del alumno sin que se les redirija fuera de la plataforma.

Vea [Agregar módulos](/help/migrated/authors/feature-summary/courses.md#add-modules) para obtener más información sobre cómo agregar módulos a los cursos.

## Información de zona horaria para los módulos de clase real y virtual

Los detalles de la zona horaria se muestran ahora para los módulos de clase (CR) y clase virtual (VC) en la página Resumen del curso, página Instancia, página Vista previa del alumno y en el widget de calendario. Los alumnos y los administradores pueden ver claramente la zona horaria asociada a las sesiones programadas en las páginas clave y las invitaciones del calendario. Los alumnos pueden planificar mejor las sesiones y unirse a ellas sin malentendidos sobre la zona horaria. Esta mejora solo está disponible en la aplicación Envolvente del alumno.

Los alumnos de diferentes regiones pueden confirmar la hora de la sesión en la zona horaria correcta. Mostrar la zona horaria claramente ayuda a evitar sesiones perdidas y garantiza una programación precisa del calendario.

## Rellenar automáticamente el nombre del autor al crear un curso

Durante la creación del curso, el campo **[!UICONTROL Autores]** ahora se rellena automáticamente con el nombre de los autores que están creando el curso. Los autores ya no necesitan introducir manualmente sus propios nombres. Los autores adicionales se pueden añadir o actualizar según sea necesario.

En el caso de las organizaciones con reglas estrictas de propiedad de contenido, el rellenado automático garantiza que los autores siempre se atribuyan correctamente. Al editar un curso existente, los autores pueden actualizar o añadir coautores sin perder la entrada rellenada automáticamente.

Vea [Crear un curso](/help/migrated/authors/feature-summary/courses.md#create-a-course---advanced-workflow) para obtener más información sobre cómo crear un curso.

## Buscar perfiles externos al cambiar el perfil

Anteriormente, los administradores se desplazaban por toda la lista de perfiles externos y seleccionaban manualmente el perfil deseado al reasignar a los alumnos. Esto hizo que el proceso llevara mucho tiempo, especialmente para las cuentas con muchos perfiles. Con esta mejora, los administradores y los administradores personalizados ahora pueden buscar perfiles externos directamente en la pestaña durante el flujo de trabajo de cambio de perfil.

**Casos prácticos**

* En cuentas con cientos de perfiles externos (por ejemplo, ubicaciones de franquicias, empresas asociadas o grupos regionales), los administradores ahora pueden localizar el perfil exacto al instante mediante la búsqueda, lo que reduce los errores y ahorra tiempo.
* Durante los cambios organizativos, como las fusiones o la reorganización de departamentos, es posible que los alumnos deban moverse en bloque a nuevos perfiles externos. La reasignación basada en búsquedas hace que esta tarea sea más fluida y precisa.

Vea [Cambiar el perfil externo](/help/migrated/administrators/feature-summary/add-users-user-groups.md#change-profile) para obtener más información sobre cómo cambiar el perfil.

## Añadir un coorganizador para las sesiones de Microsofts Teams

Anteriormente, los autores solo podían asignar un único organizador a las sesiones de Microsofts Teams. Con esta mejora, los administradores ahora pueden añadir coorganizadores a una sesión. Se ha introducido un nuevo campo, **[!UICONTROL Co-Organizer]**, en las sesiones de Microsofts Teams, lo que permite a los autores asignar organizadores adicionales junto con el organizador principal.

Los autores pueden asignar varios coorganizadores para cada sesión de Microsofts Teams. Los coorganizadores tienen el mismo acceso y los mismos permisos que el organizador principal. Los autores pueden añadir hasta 10 organizadores por sesión, lo que proporciona una mayor flexibilidad y mejora la gestión de la sesión.

**Caso de uso**

Al realizar sesiones a gran escala con muchos alumnos, los coorganizadores pueden ayudar a gestionar la asistencia, moderar los debates y supervisar el chat, mientras que el organizador principal se centra en impartir la formación.

Consulte el artículo [Añadir módulos](/help/migrated/authors/feature-summary/courses.md#add-modules) para obtener más información sobre cómo añadir sesiones de clase real y virtual a los cursos.

## Descargar informe de alumnos interesados

Cuando un administrador retira todas las instancias de curso (por ejemplo, al final del ciclo de vida del curso), el botón **[!UICONTROL Inscribir]** de la página **[!UICONTROL Resumen del curso]** se reemplaza por una opción [!UICONTROL Registrar interés]. Los alumnos pueden seleccionar esta opción para expresar su interés en realizar el curso. Ahora los administradores pueden ver y exportar una lista de alumnos que han registrado interés en un curso.

Los administradores pueden acceder a esta lista y descargarla como un informe. Se ha agregado un botón **[!UICONTROL Alumnos interesados]** a la página del curso cuando no hay instancias activas disponibles. Muestra el nombre del alumno y la fecha en que registró su interés en la interfaz de usuario del administrador.

Los administradores pueden seleccionar **[!UICONTROL Acciones]** y, a continuación, seleccionar **[!UICONTROL Exportar informe]** para exportar el **[!UICONTROL informe de alumnos interesados]**.

![](assets/register-interest.png)
_Sección de información general del curso donde los alumnos pueden ver la opción Registrar interés_

Vea [Descargar el alumno interesado](/help/migrated/administrators/feature-summary/courses.md#download-the-interested-learner-report) para obtener más información.

## Restablecer recomendaciones en la aplicación de Salesforce

Anteriormente, los alumnos que utilizaban la aplicación Adobe Learning Manager Salesforce solo podían seleccionar funciones y preferencias de recomendación una vez. Si su función cambiaba, tenían que cambiar a la aplicación nativa de Adobe Learning Manager para actualizar su perfil y recibir recomendaciones de cursos relevantes. Con la última mejora, los alumnos ahora pueden restablecer rápidamente sus preferencias directamente en la aplicación Salesforce cada vez que cambian su función laboral, equipo o responsabilidades.

Este proceso agilizado garantiza que sigan recibiendo recomendaciones de cursos actualizadas y relevantes sin salir de Salesforce. Los administradores se benefician de tasas de finalización de aprendizaje más altas y una mejor alineación entre las funciones de usuario y el contenido recomendado, todo ello sin proporcionar asistencia ni orientación adicionales sobre el cambio de plataformas.

Adobe Learning Manager ahora incluye el botón **[!UICONTROL Restablecer intereses]** en la aplicación de Salesforce. Los alumnos ahora pueden restablecer sus funciones y preferencias de aprendizaje sin necesidad de salir de Salesforce o iniciar sesión en la aplicación nativa de Adobe Learning Manager.

Consulte [Restablecer recomendaciones en la aplicación de Salesforce](/help/migrated/learners/feature-summary/sfdc-app.md#reset-recommendations-in-salesforce-app) para obtener más información sobre las recomendaciones de restablecimiento en la aplicación de Salesforce.

## Mejora del widget de calendario

Ahora los alumnos pueden ver las sesiones pasadas y futuras en el widget de calendario. Pueden desplazarse por el calendario hasta cualquier fecha y comprobar los detalles de la sesión. Esto significa que pueden revisar las sesiones que ya han tenido lugar, lo que les ayuda a realizar un seguimiento de lo que no vieron o a lo que asistieron. También pueden ver todas las próximas sesiones de los próximos 24 meses, incluido el mes actual, lo que facilita la planificación anticipada y la gestión de sus horarios.

Vea [Calendario](/help/migrated/learners/feature-summary/learner-home-page.md#calendar) para obtener más información sobre el widget de calendario.

## Etiquetar usuarios en tableros sociales

Los tableros sociales ahora admiten la funcionalidad de etiquetado de usuarios, lo que permite debates más específicos y una mejor colaboración en las comunidades de aprendizaje. Los alumnos pueden etiquetarse en publicaciones y comentarios de aprendizaje social mediante la aplicación del alumno, las API y el sitio de referencia de Adobe Learning Manager.

Los usuarios fuera del ámbito del tablero no se pueden etiquetar, lo que evita notificaciones no deseadas. Si se elimina un usuario etiquetado del sistema, su mención aparece como &quot;anónimo&quot;. No se permite etiquetar grupos de usuarios o &quot;@all&quot; para evitar el spam de notificaciones.

* Etiquetado de **@nombre_usuario**: los usuarios pueden etiquetar a otros miembros del tablero usando el formato &quot;@nombre_usuario&quot;.
* **Etiquetado con ámbito restringido**: solo se pueden etiquetar los usuarios con acceso al tablero específico, lo que garantiza la privacidad y la relevancia.
* **Notificaciones multicanal**: Los usuarios etiquetados reciben notificaciones en la aplicación y por correo electrónico con vínculos directos a publicaciones o comentarios relevantes.

**Casos prácticos**

* Profesionales de la salud que buscan comentarios de colegas específicos sobre casos médicos: el etiquetado permite a los médicos y enfermeros notificar rápidamente a los especialistas adecuados, lo que garantiza un asesoramiento oportuno y preciso sobre casos complejos de pacientes.
* Expertos en la materia que se consultan sobre temas especializados: Al etiquetar a los expertos, los equipos pueden involucrar directamente a las personas adecuadas, reduciendo el tiempo de respuesta y mejorando la toma de decisiones para consultas técnicas o de nicho.
* Debates en equipo que requieren aportaciones de interesados específicos: El etiquetado de interesados garantiza que los responsables de la toma de decisiones pertinentes estén al tanto de las actualizaciones y puedan aportar sus opiniones, manteniendo los proyectos en curso y alineados con los objetivos empresariales.

Vea [Etiquetado de usuarios en tableros sociales](/help/migrated/learners/feature-summary/social-learning-web-user.md#tag-users-in-social-board-posts) para obtener más información sobre el etiquetado de usuarios en tableros sociales.

## Permisos de anuncios con ámbito para administradores personalizados

Los administradores personalizados ahora pueden crear anuncios, pero solo para sus grupos de usuarios o catálogos asignados. Esto evita la comunicación involuntaria entre las fronteras de la organización. Los administradores personalizados solo pueden crear anuncios para los usuarios dentro de su ámbito asignado. Los anuncios se pueden definir como ámbito para grupos de usuarios o catálogos específicos. Los administradores completos mantienen la visibilidad y el control sobre todos los anuncios, incluidos los creados por los administradores personalizados del ámbito.

**Principales ventajas**

* Comunicación dirigida que garantiza que los anuncios lleguen solo a las audiencias relevantes.
* Se ha reducido la sobrecarga de información al evitar que las notificaciones irrelevantes lleguen a usuarios no deseados.
* Mantiene los límites de la organización y evita la comunicación cruzada accidental.

**Notas importantes**

* Si cambia el ámbito de un administrador personalizado, los anuncios afectados muestran un icono de advertencia y requieren restablecimientos de ámbito individuales.
* Cada anuncio debe actualizarse individualmente cuando se produzcan cambios en el ámbito.
* El informe [Anuncio de notificación](/help/migrated/administrators/feature-summary/announcements.md) solo muestra a los alumnos dentro del ámbito asignado por el administrador personalizado.

**Casos prácticos**

* Organizaciones de franquicias en las que los gestores regionales solo necesitan comunicarse con sus franquiciados.
* Grandes organizaciones con administradores regionales o departamentales que dirigen los anuncios a sus equipos.

Vea [Crear anuncio para el ámbito asignado](/help/migrated/administrators/feature-summary/announcements.md#create-announcement-for-the-assigned-scope) para obtener más información sobre cómo crear anuncio para el ámbito asignado.

## Seleccionar función personalizada al publicar contenido desde Adobe Captivate

Al publicar contenido de Adobe Captivate en Adobe Learning Manager, si un usuario tiene varias funciones personalizadas, se le pedirá que seleccione la función personalizada específica con la que se debe publicar el curso. Esto garantiza que se aplican la propiedad de la función y los permisos correctos al curso publicado.

Vea [Función personalizada](/help/migrated/administrators/feature-summary/custom-role.md) para obtener más información sobre la creación de funciones personalizadas para los usuarios.

## Mejoras en el widget Guardados por mí

Anteriormente, al seleccionar la tira **[!UICONTROL Guardados por mí]**, se mostraban todos los cursos disponibles en el catálogo. Ahora, los alumnos solo ven sus cursos marcados en la tira **[!UICONTROL Guardados por mí]** en la página principal del alumno. Al seleccionar esta tira, los alumnos pasan a la página del catálogo, donde solo se muestran los cursos que han guardado.

En el catálogo, los alumnos pueden aplicar filtros adicionales para perfeccionar su búsqueda. Cuando se aplica un filtro, solo se muestran los cursos que cumplen los criterios seleccionados. Los cursos marcados anteriormente solo aparecen si coinciden con el filtro aplicado.

Vea [Configurar widgets de cursos guardados en AEM sitios](/help/migrated/integrate-aem-learning-manager.md#configure-my-saved-courses-widgets-in-aem-sites) para obtener más información sobre el widget de cursos guardados en AEM sitios.

## Compatibilidad para mostrar los nombres de los autores en cursos compartidos

Anteriormente, cuando se compartía un curso con una [cuenta de igual a igual](/help/migrated/administrators/feature-summary/peer-account.md), el autor aparecía como autor externo. Ahora, los cursos muestran el nombre del autor, tanto si es un usuario interno de la cuenta principal como si es un autor heredado (es decir, cualquier nombre introducido como cadena en el campo Autores durante la creación del curso). Al seleccionar un autor, se muestra el número de cursos que han compartido con la cuenta de igual a igual; sin embargo, estos autores no son usuarios reales en la cuenta de igual a igual.

Si se elimina a un usuario de la cuenta principal, sus datos se eliminan allí, pero la información del autor permanece en cualquier cuenta de igual a igual en la que se haya compartido su contenido.

>[!NOTE]
>
>Esta es una característica basada en indicadores. Póngase en contacto con nuestro equipo de Asistencia al cliente en [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) para habilitar esta opción.

Vea [Cuenta de igual a igual](/help/migrated/administrators/feature-summary/peer-account.md) para obtener más información sobre el uso compartido de contenido con la cuenta de igual a igual.

## Visibilidad de búsqueda para objetos de aprendizaje de orden inferior

Anteriormente, los resultados de la búsqueda no mostraban de forma coherente los cursos individuales cuando formaban parte de objetos de aprendizaje de orden superior, como rutas de aprendizaje o certificaciones. Si un alumno se inscribía solo en una ruta de aprendizaje o certificación, la búsqueda solo mostraba la estructura de orden superior, no el curso individual.

Con esta mejora, los alumnos ahora pueden ver cursos individuales en los resultados de búsqueda, incluso cuando esos cursos forman parte de rutas de aprendizaje o certificaciones. Se ha introducido una nueva configuración de administrador, **[!UICONTROL Mostrar todos los cursos inscritos en los resultados de búsqueda]**. Cuando está activada, esta configuración garantiza que al buscar un curso específico siempre se muestre el propio curso junto con las rutas de aprendizaje o certificaciones relacionadas.

Vea [Configuración](/help/migrated/administrators/feature-summary/settings.md#general-settings) para obtener más información sobre la configuración general.

## Cambios en la API

### Mejoras de la API de migración

Adobe Learning Manager ahora admite la migración de varios objetos de datos a una cuenta a través del proceso de migración. Este proceso se puede iniciar a través de las API y la interfaz de usuario. Cuando se produce un error en la migración, los errores están disponibles para su descarga a través de la interfaz. Estos errores son útiles para depurar errores de migración y administrar las ejecuciones de migración.

Con esta versión, los registros de errores también estarán disponibles para descargar a través de las API para realizar un seguimiento de errores y una depuración eficaces y programáticos.

**Cambios en la API**

Hay una nueva API de migración, `runStatus`, que permite a los administradores de integración comprobar el estado de las ejecuciones de migración desencadenadas a través de la API, algo que no era posible en versiones anteriores de Adobe Learning Manager.

Además, la API `runStatus` ahora proporciona un vínculo directo a los registros de errores de descarga (CSV) para las ejecuciones completadas. Tenga en cuenta que el vínculo solo es válido durante siete días y los registros se conservan durante un mes.

La respuesta de la API `startRun` se ha actualizado para incluir el id. del proyecto de migración, el id. de sprint y el id. de ejecución de sprint, que son necesarios para consultar el nuevo extremo de estado.

#### API runStatus

**Descripción**

Recupera el estado de una ejecución de migración existente.

**Punto final**

```
GET /bulkimport/runStatus
```

**Parámetros**

* **migrationProjectId**: (obligatorio). Identificador único de un proyecto de migración. Un proyecto de migración se utiliza para transferir datos y contenido de un sistema de gestión de aprendizaje (LMS) existente a Adobe Learning Manager. Cada proyecto de migración puede constar de varios sprints, que son unidades más pequeñas de tareas de migración.

* **sprintId**: (obligatorio). Identificador único de un sprint dentro de un proyecto de migración. Un sprint es un subconjunto de tareas de migración que incluye elementos de aprendizaje específicos (por ejemplo, cursos, módulos o registros de alumnos) que se migran de un LMS existente a Adobe Learning Manager. Cada sprint se puede ejecutar de forma independiente, lo que permite la migración por fases.

* **sprintRunId**: (obligatorio). Identificador único utilizado para hacer un seguimiento de la ejecución de un sprint específico dentro de un proyecto de migración. Se asocia con el proceso de migración real de los elementos definidos en un sprint. El sprintRunId ayuda a supervisar, solucionar problemas y administrar el trabajo de migración.

**Respuesta**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### API startRun

La respuesta de la API `startRun` se actualizó para incluir tres campos adicionales: migrationProjectId, sprintId y sprintRunId. Estos campos permiten a los usuarios realizar un seguimiento y consultar el estado de ejecuciones de migración específicas mediante la nueva API runStatus.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Produce la siguiente respuesta. La respuesta contiene:

* `migrationId`
* `sprintId`
* `sprintRunId`

**Respuesta**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

Consulta el [manual de migración](/help/migrated/integration-admin/feature-summary/migration-manual.md) para obtener más información sobre la migración de contenido desde el LMS existente.

### Cambios en la API social (etiqueta de usuario, comentarios y respuestas)

Adobe Learning Manager ahora admite la funcionalidad de etiquetado @user en los tableros sociales, lo que permite a los alumnos mencionar y notificar a sus compañeros en las publicaciones, los comentarios y las respuestas. Esta función mejora la colaboración y el descubrimiento de contenido en toda la plataforma.

Esta versión presenta nuevas funciones de API para admitir menciones de usuarios, incluidos puntos finales de POST y GET mejorados, así como una nueva funcionalidad de búsqueda para usuarios etiquetados.

**Introducción a los cambios en la API**

* API de POST actualizadas para crear publicaciones, comentarios y respuestas con menciones de usuarios
* API de GET actualizadas con datos de menciones de usuarios en las respuestas

**Formato de menciones de usuario**

Se menciona a un usuario con el formato: @(usuario:userId)

#### Crear publicación con menciones

**Punto final**

```
POST /primeapi/v2/posts
```

**Descripción**

Crea una nueva publicación de aprendizaje social con menciones de usuarios.

**Cuerpo de solicitud**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Respuesta**

Respuesta estándar posterior a la creación con datos de mención incluidos en la relación _userMentions_.

#### Crear comentario con menciones

**Punto final**

```
POST /primeapi/v2/comments
```

**Descripción**

Añadir un comentario a una publicación con menciones de usuarios.

**Cuerpo de solicitud**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Crear respuesta con menciones

**Punto final**

```
POST /primeapi/v2/replies
```

**Descripción**

Responder a un comentario con menciones del usuario.

**Cuerpo de solicitud**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Recuperar publicaciones con menciones

**Punto final**

```
GET /primeapi/v2/posts/{id}
```

**Descripción**

Recuperar detalles de la publicación, incluidos los usuarios mencionados.

**Respuesta**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Cambios en la API social (búsqueda de usuarios)

**Punto final**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Descripción**

Busque usuarios disponibles para etiquetar según la configuración del ámbito social.

**Parámetros de solicitud**


* q (obligatorio): Término de búsqueda (mínimo 3 caracteres).
* context: establézcalo en &quot;etiquetado&quot; para que los usuarios puedan recibir menciones.
* boardId (opcional): ID de tablero para filtrar usuarios en función de los permisos de acceso.

**Respuesta**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### Mejoras de la API del alumno para el seguimiento del rendimiento de pruebas

La API `GET /loResourceGrades` se ha mejorado para proporcionar datos detallados del rendimiento de las pruebas, lo que permite análisis más sofisticados y toma de decisiones automatizada.

La respuesta de la API ahora incluye dos campos adicionales:

* **[!UICONTROL puntuación más alta]**: la mejor puntuación obtenida por un alumno en todos los intentos de prueba
* **[!UICONTROL maxScore]**: La puntuación total posible de la prueba

**Ejemplo de respuesta de API**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

En respuesta, **course:15067_30122_41715_1_3400468** es el identificador del grado de recurso del objeto de aprendizaje para el que se solicita la información. El `learningObjectResourceGrad`e id se puede obtener de la API `GET /enrollments/{id}`.

### Las respuestas de la API admiten la distinción de mayúsculas y minúsculas para nombres de autor

La respuesta de la API ahora proporciona las mayúsculas y minúsculas exactas de los nombres de autor heredados, tal y como se introdujeron durante la creación o actualización del curso. Esto garantiza que los nombres aparezcan de forma coherente en la interfaz de usuario del alumno y las API públicas.

* Cuando se agrega un nuevo nombre de autor, la incidencia se almacena y se devuelve exactamente como se introdujo.
* Si se elimina un nombre de autor existente y se vuelve a añadir con una incidencia diferente, la incidencia actualizada se respetará y se reflejará en todos los cursos que utilicen ese nombre de autor.
* No se realizará ninguna migración automática para los nombres almacenados anteriormente; solo los nombres recién agregados o actualizados seguirán este comportamiento.

### Mejora de la API de Calendar

El calendario ahora carga sesiones para el mes seleccionado por el usuario. Para obtener sesiones pasadas y futuras a través de la API, se ha agregado un nuevo parámetro `year` al extremo del alumno `GET /users/{id}/calendar`. Los parámetros `month` y `year` se deben proporcionar juntos para recuperar los detalles de la sesión.

**Curl de muestra**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth a4ae04eb9f06f4bf88abcde17' 'https://abc.adobe.com/primeapi/v2/users/12345678/calendar?month=7&year=2025&currentMonthOnly=false&filter.allSessions=false'
```

### Compatibilidad con la finalización de marcas a través de la API de administrador

Anteriormente, la API pública no admitía el marcado de finalización basado en instancias en escenarios de inscripción múltiple. Con esta mejora, ahora puede incluir el ID de instancia del curso en el cuerpo de la solicitud de `POST /users/{userId}/userModuleGrade` y el administrador puede marcar la finalización de una instancia específica.

### Definir la preferencia de ID de usuario para los informes SCORM

Algunos clientes requieren el UUID (Universally Unique Identifier) del alumno en lugar del user_id predeterminado para la finalización del contenido de SCORM. El uso del UUID proporciona un seguimiento más preciso en los programas de aprendizaje y evita la duplicación del uso de licencias en las cuentas de MAU (usuario activo mensual).

Para admitir esto, se ha agregado una nueva configuración de nivel de cuenta, `reporting_userid_preference`. Cuando está activada, esta configuración envía el UUID en lugar de user_id siempre que los alumnos completan el contenido de SCORM.

>[!NOTE]
>
> Póngase en contacto con nuestro equipo de Asistencia al cliente en [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) para configurar esta opción.

Se ha introducido el nuevo atributo `reportingUserIdPreference` para que `get /account` realice un seguimiento de las preferencias de ID de usuario.

### Información del autor en cursos compartidos

En la API de objetos de aprendizaje, se ha actualizado la forma en que se devuelve la información del autor para distinguir entre los cursos con cuentas principales y los cursos compartidos con cuentas de igual a igual:

* Cursos compartidos (cuenta de igual a igual): los detalles del autor ahora se devuelven con un nuevo atributo, `authorDetails`. Este atributo proporciona el nombre de autor aunque el curso se origine en otra cuenta.

* Cursos de cuenta principal: la información del autor sigue devolviéndose bajo el atributo `authors` existente, sin cambios en el comportamiento actual.

Este cambio garantiza la coherencia en la forma en que los datos del autor se exponen a través de la API para los cursos principales y compartidos, al tiempo que conserva la compatibilidad para las integraciones existentes.

## Cambios en los webhooks

### Registrar webhooks de LinkedIn Learning mediante el conector

Anteriormente, los administradores tenían que registrar manualmente los webhooks de LinkedIn Learning en Adobe Learning Manager mediante API. Con esta mejora, el conector de LinkedIn Learning (LIL) ahora admite el registro de webhook automáticamente durante la nueva configuración de conexión en ALM. La **URL del servidor OAuth** y la **URL del servidor de inquilinos** se rellenarán automáticamente en la página de configuración de LinkedIn Learning.

Consulta [LinkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md#linkedin-learning-connector) para obtener más información sobre la integración de LinkedIn Learning.

### Cambios en el uso de licencias de MAU en LinkedIn Learning

Anteriormente, para las cuentas MAU (usuarios activos mensuales), cuando un alumno completaba un curso de LinkedIn Learning directamente en la plataforma LinkedIn Learning, Adobe Learning Manager no contaba el uso de licencias. El consumo de licencias se activó solo para los cursos realizados a través del reproductor de Adobe Learning Manager, lo que dio como resultado un seguimiento inexacto de los usuarios activos mensuales (MAU).

Con esta mejora, Adobe Learning Manager ahora genera un webhook externo cada vez que un alumno consume un curso en la plataforma de aprendizaje de LinkedIn. Cuando Adobe Learning Manager recibe este webhook, calcula el uso de la licencia para garantizar un seguimiento preciso en ambas plataformas.

## Cambios en los informes

### Finalizaciones marcadas por el instructor en transcripciones de alumnos

Las transcripciones incrementales de alumnos ahora capturan las finalizaciones marcadas por el instructor, incluso si la asistencia se registra después de la fecha de la sesión.
Esta mejora corrige una laguna crítica en las transcripciones incrementales de alumnos, donde antes no se cumplían las finalizaciones marcadas por el instructor si la asistencia se registraba después de la fecha original de la sesión.

Las transcripciones incrementales de alumnos son informes programados que capturan solo los cambios (como finalizaciones o actualizaciones de progreso) que se producen dentro de un período especificado, en lugar de proporcionar un volcado de datos históricos completo. Se suelen utilizar para automatización, paneles e integraciones, lo que permite a los usuarios realizar un seguimiento eficaz de las actividades de aprendizaje recientes sin procesar todo el historial de transcripciones en cada ocasión.

* **Marcar fecha de finalización (zona horaria UTC), columna**: una nueva columna de marca de tiempo que captura la fecha y hora exactas cuando un instructor marca una sesión o módulo como completada.
* **Seguimiento mejorado del origen de finalización**: realiza un seguimiento del instructor y el módulo específicos (por ejemplo, &quot;Clase&quot;) en los que se registraron las finalizaciones.

Estos cambios garantizan que las finalizaciones marcadas después de la fecha de la sesión se reflejen con precisión en las transcripciones incrementales de alumnos.

**Casos prácticos**

* Organizaciones con sesiones de clase en las que los instructores pueden marcar los días de asistencia después de la sesión real.
* Sistemas automatizados o paneles que dependen de transcripciones incrementales de alumnos para el cumplimiento normativo o la creación de informes.

![Informes de transcripciones de alumnos que muestran fechas de finalización marcadas (resaltadas en amarillo) para el seguimiento de la finalización del curso en Aprendizaje Adobe](/help/migrated/assets/mark-completion-column.png)
_El informe de transcripciones de alumnos muestra una nueva columna en amarillo en la que se resaltan las fechas de finalización individuales de cada usuario_

Consulte [Transcripciones de alumnos](/help/migrated/administrators/feature-summary/learner-transcripts.md) para obtener más información sobre el informe de transcripciones de alumnos.

### Informe de usuario mejorado con campos de datos ampliados

El informe de usuarios ahora incluye campos adicionales para mejorar el seguimiento de los usuarios y la asignación de la organización. Estas actualizaciones simplifican la identificación de usuarios, admiten la integración con los flujos de trabajo de administración de usuarios descendentes, mejoran la comprensión de las relaciones de creación de informes y mantienen los límites de la organización para evitar la comunicación cruzada accidental.

* Columna ID de usuario interno: proporciona identificadores internos únicos para facilitar el seguimiento de usuarios en diferentes sistemas y puntos finales de API.
* Columna Correo electrónico del responsable: incluye información de contacto del responsable directo para el seguimiento de la jerarquía organizativa.

![Informe de usuario que muestra las columnas de correo electrónico del administrador e ID de usuario interno resaltadas en amarillo](/help/migrated/assets/user-report-columns.png)
_Informes de usuarios que destacan los ID de usuario internos y las direcciones de correo electrónico del administrador para agilizar la administración de usuarios_

Vea [Descargar el informe de usuarios](/help/migrated/administrators/feature-summary/add-users-user-groups.md#download-the-user-report) para obtener más información sobre el informe de usuarios.

### Informe del usuario en FTP, FTP personalizado y Box

**Información general**

El informe de usuario ahora está disponible para los conectores de Box, FTP y FTP personalizado, además de para las API de trabajos existentes. Estos informes proporcionan información detallada sobre el ID de usuario interno, el correo electrónico del usuario, el nombre, el correo electrónico del responsable, el tipo de usuario y otros.

Los informes pueden generarse bajo demanda o programarse, con datos almacenados en el respectivo conector para facilitar el acceso y el análisis. Esta mejora mejora la supervisión y la auditoría de las actividades de los usuarios, lo que mejora la seguridad y el seguimiento del cumplimiento normativo.

Estos informes están disponibles junto con los informes existentes, como el registro de usuarios, el acceso de inicio de sesión, la interacción y la formación, lo que permite a los administradores acceder a todos los informes esenciales desde una única ubicación para agilizar la gestión y el análisis de los datos.

Vea [Conector](/help/migrated/integration-admin/feature-summary/connectors.md) para obtener más información sobre FTP, FTP personalizado y conector de Box.

### Incluir usuarios suspendidos en transcripciones de alumnos

**Información general**

Ahora, las organizaciones pueden incluir usuarios suspendidos (aquellos con perfiles externos deshabilitados) en transcripciones de alumnos, lo que garantiza una retención completa de los datos de aprendizaje históricos.

* Indicador de nivel de cuenta para configurar la visibilidad de los usuarios suspendidos, lo que permite que los usuarios suspendidos aparezcan en transcripciones de alumnos.
* Retención de datos históricos incluso después de la desactivación de perfiles externos suspendidos.

**Requisitos de implementación**

* Póngase en contacto con el administrador de éxito de clientes (CSM) para activar el indicador de nivel de cuenta.

>[!NOTE]
>
>Este indicador está desactivado de forma predeterminada para las cuentas existentes y debe solicitarse explícitamente para las nuevas cuentas.

Vea el artículo [Transcripciones de alumnos](/help/migrated/administrators/feature-summary/learner-transcripts.md) para obtener más información.

### Informe de ayudas de trabajo con vínculos de acceso directo

**Información general**

El informe Ayudas de trabajo se ha mejorado para incluir vínculos de descarga directa a las ayudas de trabajo, lo que simplifica la administración de contenido y los procesos de auditoría para administradores y autores. Esta mejora proporciona descargas directas de archivos y acceso a direcciones URL desde el informe. Elimina el esfuerzo manual de localizar y descargar ayudas de trabajo para auditorías de conformidad o accesibilidad.

* Columna Vínculo de ayuda de trabajo: acceso directo a archivos de ayuda de trabajo y direcciones URL externas desde el informe.
* Control de acceso basado en funciones: la accesibilidad de los vínculos depende de las funciones del usuario y de los permisos del catálogo.
* Las ayudas de trabajo eliminadas siguen siendo accesibles si siguen vinculadas a cursos activos.

**Casos prácticos**

* Los autores o los administradores realizan auditorías de accesibilidad periódicas en las ayudas de trabajo, según sea necesario para las grandes organizaciones.
* Cualquier escenario en el que se necesite un acceso rápido y basado en funciones a los archivos de ayuda de trabajo para la revisión o el cumplimiento.

![](/help/migrated/assets/job-aid-report.png)
El _Informe de ayudas de trabajo muestra vínculos de descarga directa, lo que facilita el acceso y la descarga de ayudas de trabajo en Adobe Learning Manager_

Vea [Informe de ayudas de trabajo](/help/migrated/administrators/feature-summary/reports.md#job-aids-report) para obtener más información sobre el informe de ayudas de trabajo.

## Errores solucionados en esta actualización

* Las puntuaciones de las pruebas de L2 ahora se generan correctamente para pruebas no interactivas, incluidos los detalles de los usuarios que las completaron.
* Ahora la firma se envía correctamente al host de destino cuando el mecanismo de autenticación se establece en Firma durante la configuración de la conexión.
* Los usuarios ficticios creados durante las sesiones de Adobe Connect no se eliminaron al finalizar la sesión. La canalización de SnapLogic ahora elimina correctamente a estos usuarios, incluso cuando la API `principals-delete` devolvió anteriormente una respuesta 200 sin eliminarlos.
* `null` `eventDetail` objetos en respuestas de API ya no causan excepciones. El sistema ahora omite las entradas nulas y procesa toda la matriz, lo que garantiza grabaciones completas.
* La columna Fecha de comentarios de los informes de comentarios ahora muestra la fecha correcta. Anteriormente, los segundos se pasaban incorrectamente al constructor Date, que espera milisegundos, lo que hace que las fechas aparezcan como enero de 1970. Esto se ha corregido para garantizar una visualización precisa de la fecha al generar informes de comentarios.
* Los alumnos ahora pueden actualizar la inscripción en una ruta de aprendizaje de Flex aunque se haya retirado una de las instancias del curso. Anteriormente, al seleccionar una nueva instancia, se producía un error de consola (No se pueden leer las propiedades de no definido) que impedía la actualización.
* Los nombres de recursos de las rutas de aprendizaje ahora se muestran correctamente sin romper la palabra media.
* Los webhooks de linkedIn Learning ahora están activados desde el conector LIL al crear conexiones para nuevos usuarios. El sistema también registra la cuenta a través de la API privada y muestra información de configuración adicional (URL de OAuth y URL de inquilino) en la página de configuración de LinkedIn Learning.
* Los valores de atributos de usuario actualizados mediante flujos de trabajo de SAML (`UpdateUserWorkerTask`) ahora se guardan con sus mayúsculas y minúsculas originales en lugar de convertirse a minúsculas.
* Al reordenar módulos en un curso, ya no se restablece el número de módulos obligatorios en &quot;Todos&quot;; el recuento ahora permanece tal y como está configurado.
* Las canalizaciones Go1 ahora controlan los códigos de idioma de forma coherente asignando códigos de dos letras a códigos de cuatro letras, de forma similar a las canalizaciones de LinkedIn Learning.
* En las cuentas de Retirar+, los alumnos veían anteriormente &quot;Este curso no existe&quot; al iniciar un curso de la ruta de aprendizaje después de darse de baja de una certificación. Los orígenes de inscripción ahora se actualizan correctamente, lo que permite que los cursos de las rutas de aprendizaje se inicien sin errores.
* Cuando el archivo module_version.csv contiene campos contentType con valores en blanco o nulos, la creación del curso ahora funciona sin problemas.
* Los cursos ahora aparecen correctamente al filtrar por catálogo o etiqueta de catálogo. Anteriormente, al aplicar estos filtros en la página del curso, no se mostraban los cursos, aunque estuvieran asociados al catálogo.
* En la aplicación del alumno, al pulsar TAB en el reproductor Fluidic, se bloqueaba el botón &quot;Introducir pantalla completa&quot;. La navegación con teclado ahora se desplaza correctamente por todos los elementos de la pantalla.
* Al pasar el ratón por encima de los nombres largos de curso en el tablero de cumplimiento de la aplicación del responsable, ahora se muestra el nombre completo de los cursos en los que se ha inscrito o que cumplen la normativa.
* Solo se aceptan elementos Compartidos u OCULTOS para la columna de visibilidad del módulo en module.csv. Cualquier otro valor activará un error durante la migración, lo que evitará errores en el back-end.
* La creación de un nuevo administrador con un correo electrónico con varias mayúsculas y minúsculas ya no genera entradas de usuario duplicadas cuando se deshabilita el UUID. El sistema ahora gestiona de forma coherente la protección del correo electrónico para evitar duplicados.
* Los PDF de notas ahora se muestran correctamente para los cursos en idiomas como árabe, griego, hebreo, hindi, tailandés y ucraniano. Anteriormente, los caracteres aparecían distorsionados en el PDF descargado aunque se mostraran correctamente en el reproductor.

## Requisitos del sistema

Ver [requisitos del sistema de Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de la versión

Consulta las [notas de la versión](/help/migrated/release-note/release-notes.md) para ver las últimas actualizaciones de la versión.

## Versiones anteriores de Adobe Learning Manager

* [Versión de mayo de 2025 de Adobe Learning Manager](/help/migrated/whats-new-may-2025.md)
* [Versión de noviembre de 2025 de Adobe Learning Manager](/help/migrated/whats-new-nov-24.md)
