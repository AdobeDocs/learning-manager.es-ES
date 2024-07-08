---
description: Obtenga más información sobre las nuevas funciones y mejoras de la versión de marzo de 2024 de Adobe Learning Manager
jcr-language: en_us
title: Resumen de nuevas funciones
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Resumen de nuevas funciones {#new-features-summary}

Obtenga más información sobre las nuevas funciones y mejoras de la versión de marzo de 2024 de Adobe Learning Manager.

Explore algunas de las funciones más recientes de Adobe Learning Manager, como:

1. Importar aptitudes de fuentes externas
1. Compatibilidad con varias marcas
1. Módulo de actividad de reevaluación de la lista de verificación
1. Aplicación de aprendizaje móvil de marca blanca

>[!NOTE]
>
>Consulte este [seminario web](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) para obtener más información sobre las nuevas funciones de esta versión.


## Novedades de esta versión {#whatsnewandchanged}

### Importar aptitudes de fuentes externas

Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, utilizando los conectores correspondientes. Esta mejora es parte del objetivo de la capacidad del Administrador de aprendizaje para integrarse con Skills Cloud y sistemas de gestión de talento externos. Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en el Administrador de aprendizaje y estarán disponibles para los autores durante el flujo de trabajo de creación del curso. También se han realizado mejoras en la funcionalidad de búsqueda de aptitudes en toda la plataforma para proporcionar una mejor experiencia de búsqueda cuando la cuenta tiene un gran número de aptitudes.

Consulta [Aptitudes de importación](administrators/feature-summary/import-skills-external-sources.md) para obtener más información.

### Personalización de marca

Ahora podrá personalizar determinados elementos de la interfaz de usuario: el nombre de la empresa, el logotipo y el tema de la interfaz de usuario, en función de los grupos de usuarios disponibles en la cuenta. Por ejemplo, una organización con varias divisiones puede configurar un logotipo personalizado y un tema de interfaz de usuario para mostrar para cada división.

>[!NOTE]
>
>Esta función de marca múltiple no se aplica a la vista del administrador. Siempre verán la marca a nivel de empresa en su cuenta. Esto se debe a que se trata de una función orientada al alumno y es posible que los administradores no la quieran en su cuenta.

Consulte [Varias marcas](administrators/feature-summary/themes.md#multiple-branding) personalizadas para obtener más información.


## Cambios para cuentas con una base de usuarios grande

### Páginas Curso o Ruta de aprendizaje de administración

Si hay un gran número de alumnos inscritos en el curso, por ejemplo, más de 50.000, la lista de alumnos no se mostrará. Puede buscar a un alumno en la *barra de búsqueda Buscar alumnos* o seleccionar el **vínculo Descargar** en la parte superior de la barra de búsqueda para descargar la lista de alumnos.

### Página Administradores - Alumnos

Cuando se busca un usuario, las **opciones Descargar alumno** y **Exportar** descargan el mismo informe. Mientras tanto, mientras busca un grupo de usuarios, ahora puede descargar usuarios filtrados de ese grupo de usuarios. Al buscar en un grupo de usuarios,
La **lista** de alumnos Descargar cambia a Descargar lista de alumnos para grupos de usuarios **La** opción Exportar **vuelve a** descargar la lista completa.

### Página Administrador- Usuarios

#### Usuarios internos

Si el número de usuarios supera, por ejemplo, 50,000, habrá un mensaje para descargar los datos para un análisis más detallado más adelante. La barra de búsqueda ahora es prominente y muestra a un usuario en el formato *Nombre, correo electrónico | UUID.*

>[!NOTE]
>
>El UUID se muestra solo si UUID está habilitado para la cuenta.

#### Usuarios externos

Para los usuarios externos, se aplica el mismo comportamiento. Si el número de usuarios es grande, puede descargar los usuarios y también recuperar los detalles de un usuario después de una búsqueda en el formato *Nombre, correo electrónico | UUID.*

#### Página Limpieza de usuarios

En la página Limpieza de usuarios, hemos eliminado la capacidad de ordenación en **Fecha de eliminación**. Solo puede ordenar en los UUID.

### Páginas de instancia de administración

#### Curso o programa de formación

Si el número de inscripciones es grande, Adobe Learning Manager no mostrará el número de alumnos. En su lugar, habrá un icono que puede seleccionar, ver la cantidad de alumnos y navegar a la página Alumnos.

El número de alumnos se mostrará como un valor aproximado. Por ejemplo, si el número de alumnos es mayor que 50,000, el valor se mostrará como 50K+.

### Páginas Admin- L1/L3

En la página Comentarios de L1, si el número de inscripciones en los cursos es grande, no se muestra la lista de alumnos. En su lugar, puede exportar la lista de usuarios para un análisis más detallado más adelante.

La búsqueda admite la escritura anticipada y los resultados se limitan a la instancia seleccionada.

#### Página de asistencia y puntuación

En la página, cuando busca un usuario, la búsqueda se ejecuta en todas las instancias disponibles. Sin embargo, el resultado será para la instancia seleccionada.

En la página Asistencia, si busca un grupo de usuarios y el número de usuarios supera los 10 000 en el grupo de usuarios, independientemente de la inscripción, solo puede realizar acciones de nivel masivo. No podrás ver la lista de usuarios.

Si el número de usuarios del grupo de usuarios es inferior a 10 000, puede realizar acciones individuales a nivel de usuario junto con acciones a nivel de grupo. En este caso, la lista de usuarios no se desactiva.

### Página Administrador - Certificaciones

En las versiones actuales de Adobe Learning Manager, si hay un gran número de usuarios inscritos en una certificación, no puede ver los alumnos que se han dado de baja porque el **menú desplegable Estado** está desactivado.

En esta versión de Adobe Learning Manager, si el número de usuarios inscritos es grande, el **menú desplegable Estado** solo muestra dos opciones: **Inscrito y** Darse **de baja**. La opción **Inscrito** está seleccionada de forma predeterminada. Si selecciona **Darse de baja**, aparece la lista de alumnos que se han dado de baja.

#### Cambios en los grupos de usuarios

En el caso de un grupo de usuarios, si el número de usuarios del grupo de usuarios es menor, por ejemplo, de 50 000, el **menú desplegable Estado** muestra todas las opciones: Certificado, Asignado y Caducado.

Si la cantidad de usuarios de un grupo de usuarios es grande, el **menú desplegable Estado** solo muestra dos opciones: **Inscrito** y **Darse de baja**, según el nuevo diseño.

### Tabla comparativa

<table>
    <tbody>
        <tr>
            <td><b>Página</b></td>
            <td><b>Antes del cambio de umbral</b></td>
            <td><b>Tras el cambio de umbral</b></td>
        </tr>
        <tr>
            <td>Administrador: Instancia del curso</td>
            <td>Las instancias se muestran tal y como están diseñadas con lo siguiente:
            <ul>
                <li>Módulos</li>
                <li>Alumnos inscritos</li>
                <li>Sesiones</li>
                <li>Insignia</li>
                <li>Comentarios de L1 activados</li>
                <li>Alertas de notificación</li>
                <li>Puntos de interacción</li>
                <li>Código QR</li>
                <li>Extensión del trazado de aprendizaje</li>
            </ul>
            <td>
                <ul>
                    <li>Si el número de inscripciones supera el umbral predefinido, ALM no mostrará el recuento; reemplazará el recuento por un icono que, al hacer clic en él, muestra el número real de alumnos y un vínculo para acceder a la página Alumnos.</li>
                    <li>El número de inscripciones se mostrará en formato aproximado. Por ejemplo, si el número es más de 50,000, el recuento se mostrará como 50K + en el nivel del curso.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Administradores - Alumnos</td>
            <td>
                    <ul>
                        <li>La lista de alumnos aparece para cada instancia.</li>
                        <li>Puede buscar un usuario o un grupo de usuarios inscritos en un curso.</li>
                        <li>El informe exportado no incluye ningún filtro para grupos de usuarios.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia está deshabilitada.</li>
                    <li>Descargar lista de alumnos también descarga los mismos datos, excepto en un caso. Si busca un grupo de usuarios y luego selecciona la lista de alumnos Descargar, se descargarán los datos del grupo de usuarios.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador: página de comentarios de L1/L3</td>
            <td>
                <p>No se ha producido ningún cambio en el comportamiento existente</p>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia está deshabilitada.</li>
                    <li>Si la inscripción en un curso es superior a 50K, ALM no enumera los alumnos y solo muestra la barra de búsqueda. Si la inscripción es inferior a 50 K, ALM muestra tanto la lista de alumnos como la barra de búsqueda.</li>
                    <li>El anuncio está desactivado de forma predeterminada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Administración: asistencia y puntuación</td>
            <td>
                <p>No se ha producido ningún cambio en el comportamiento existente</p>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia se desactiva al buscar un usuario.</li>
                    <li>Si el número de usuarios supera, por ejemplo, 50,000, habrá un mensaje adicional para descargar los datos para un análisis más detallado más adelante. La barra de búsqueda ahora es prominente y muestra a un usuario en el formato Nombre, correo electrónico | UUID.</li>
                    <li>Si el número de usuarios en el grupo de usuarios es inferior a 10 000, independientemente de la inscripción, puede realizar acciones individuales a nivel de usuario junto con acciones a nivel de grupo. En este caso, la lista de usuarios no se desactiva.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador: página Puntuación de prueba de L2</td>
            <td>
                    <ul>
                        <li>También se implementa la búsqueda de usuarios.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>También se implementa la búsqueda de usuarios. Mientras se realiza la búsqueda con escritura anticipada en el nivel de objeto de aprendizaje, la lista se filtra a la instancia seleccionada actualmente.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Administrador- Usuarios (internos, externos)</td>
            <td>
                    <ul>
                        <li>El ID de correo electrónico se muestra al buscar un usuario.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Si el número de usuarios supera, por ejemplo, 50,000, habrá un mensaje adicional para descargar los datos para un análisis más detallado más adelante. La barra de búsqueda ahora es prominente y muestra a un usuario en el formato Nombre, correo electrónico | UUID.</li>
                    <li>En la página Limpieza de usuarios, hemos eliminado la capacidad de ordenación en **Fecha de eliminación**. Solo puede ordenar en los UUID.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instructores- Presentación</td>
            <td>
                    <ul>
                        <li>Paginación de los módulos a presentar.</li>
                        <li>Como instructor, ahora puede filtrar los envíos de archivos de los alumnos según el estado, la finalización de revisión, el envío pendiente, el aprobado y el suspendido. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>En ese caso, solo puede buscar usuarios, no grupos de usuarios.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Contar con la vista previa como página de alumno</td>
            <td>
                    <ul>
                        <li>El recuento incluye los datos de la inscripción de orden superior.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>El recuento excluye los datos de inscripciones de orden superior.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Capacidades de búsqueda avanzadas

En esta versión, hemos mejorado la experiencia de búsqueda. Los resultados de la búsqueda se obtienen en función no solo de los metadatos, sino también de la búsqueda semántica y en el contenido para derivar resultados basados en la precisión, la actualidad y el contenido relevante.

Este cambio se refleja en lo siguiente:

* Catálogo y página Mi aprendizaje: se ha eliminado la acción de pasar por encima del curso, la ruta de aprendizaje y la certificación.
* El aspecto de la barra de búsqueda.
* Se agregaron etiquetas de filtro en la aplicación de aprendizaje.

Para habilitar las funciones de búsqueda, póngase en contacto con el equipo de CSAM de Adobe Learning Manager.

## Cambios en la interfaz de usuario {#ui-changes}

### Página de creación del curso

Al asignar los cursos a un nivel de aptitud, la búsqueda de la lista de aptitudes es lo primero. En otras palabras, busque habilidades y verá una lista de habilidades que coinciden con el término buscado.

### Grupos de usuarios

#### Administrador: página Alumnos

Cuando se busca un usuario, las **opciones Descargar alumno** y **Exportar** descargan el mismo informe. Mientras tanto, mientras busca un grupo de usuarios, ahora puede descargar usuarios filtrados de ese grupo de usuarios. Al buscar en un grupo de usuarios, la lista **Descargar alumno cambia a Descargar lista de alumnos para el** grupo **de usuarios La** opción Exportar **vuelve a** descargar la lista completa.

## Cambios en los informes

* Las columnas Etiquetas y Aptitud en Informe de formación se cambian a Etiqueta y aptitudes.
* Se ha agregado el informe [Gamification Audit Trail](administrators/feature-summary/reports.md#gamification-audit-trail).
* Si una cuenta contiene más de 280000 alumnos asignados a una aptitud, el informe de alumno se descarga como archivo .csv comprimido.
Si la cuenta tiene menos de 250000 alumnos, el mismo informe se descarga como archivo CSV.
En la página Administrador, seleccione **Administrador** > **Aptitudes** > **Aptitudes** > **alumnos**. El informe se descarga en forma de CSV.
* El [informe](administrators/feature-summary/reports.md#session-summary-report) Resumen de la sesión tiene dos nuevas columnas: Información de ubicación y Región de ubicación.

## Cambios en la creación de aulas

En función de la [configuración](administrators/feature-summary/classroom.md#classroom-settings) del administrador, usted, como autor, puede [crear, modificar y eliminar ubicaciones](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>Al agregar etiquetas de ubicación y de catálogo, los autores (en la página de creación del curso) y los administradores (en la página de instancia) verán una lista de ubicaciones y etiquetas de catálogo que se rellenan automáticamente, respectivamente.

Como administrador, puede imponer restricciones a un autor para modificar o eliminar una ubicación de aula. Consulte [la configuración del](administrators/feature-summary/classroom.md#classroom-settings) aula para obtener más información.

## Cambios en la ruta de aprendizaje flexible

Todas las cuentas (antiguas y nuevas) que se inicien, incluidas la fecha límite de inscripción, la fecha límite de darse de baja y el límite de puestos en la aplicación del alumno para un programa de aprendizaje flexible.
Los alumnos ahora podrán inscribirse en Ruta de aprendizaje flexible sin seleccionar ninguna instancia del curso.

## Nuevo activador de planes de aprendizaje

Se ha añadido un nuevo activador a la página de configuración del plan de aprendizaje. Los autores y los administradores ahora pueden activar acciones cuando un alumno suspende un módulo de un curso.

Vea [los planes](administrators/feature-summary/learning-plans.md) de aprendizaje para obtener más información.

## Nuevo estado de envío

Como instructor, ahora puede filtrar los envíos de archivos de los alumnos según el estado, la finalización de revisión, el envío pendiente, el aprobado y el suspendido.

Ver [el estado de](instructors/feature-summary/learners.md#filter-file-submissions) envío para obtener más información.

## Mejoras en la lista de comprobación

En la versión de marzo de 2024 de Adobe Learning Manager, las mejoras realizadas en el flujo de trabajo de las listas de comprobación son las siguientes:

### No permitir el progreso al suspender una lista de comprobación

Al crear una lista de comprobación, un autor puede seleccionar **Activar** en la sección Lista de comprobación obligatoria. Al hacerlo, se evita que un alumno continúe en el módulo si no pasa la lista de comprobación. Solo pueden continuar si pasan la lista de verificación.

Los revisores de la lista de verificación, es decir, los instructores o los gerentes, pueden verificar el estado de la lista de verificación. Asimismo, los revisores pueden revisar la lista de comprobación de un alumno sin orden.

### Reevaluación de una lista de verificación

Al crear una lista de comprobación, un autor puede seleccionar **Activar** en la sección Reevaluación. De esta manera, un responsable o instructor puede volver a evaluar a un alumno hasta que apruebe la lista de verificación.

Si el módulo es obligatorio, la casilla de verificación de reevaluación está seleccionada de forma predeterminada.

Un instructor o gerente también puede cambiar el estado de una lista de verificación de No aprobado a Aprobado cuando la reevaluación está habilitada.

En la página Lista de comprobación, un instructor puede ver la cantidad de alumnos en el estado Pendiente. Como instructor, puede evaluar a un alumno y aprobarlo o suspenderlo. Si un alumno se encuentra en estado de suspenso, solo puede ver la lista de verificación cuando la reevaluación no está activada.

Esto significa que la **casilla Activar** no se seleccionó en la sección Reevaluación al crear la lista de comprobación. Si se selecciona esta casilla de verificación, aparece el botón Ver/Reevaluar en la página Lista de comprobación del instructor.

Seleccionar el botón permite volver a evaluar a un alumno y marcar que aprueba o suspende.

>[!NOTE]
>
>Ambas características, Reevaluación y Hacer que la lista de verificación sea obligatoria, solo se aplican a los módulos recién creados. Una vez que se publica un curso, no se pueden activar ni desactivar.


Ver [Crear una lista](authors/feature-summary/courses.md#checklist-fail) de comprobación para obtener más información.

## Otras mejoras

### Notificaciones por correo electrónico relacionadas con la sesión

En versiones anteriores de Adobe Learning Manager, un alumno no enviaba correos electrónicos relacionados con la sesión, Actualización de detalles de la sesión, Invitación a sesión y Recordatorio de sesión cuando:

* Los alumnos han completado un curso,
* Se añaden nuevas sesiones a un curso o
* Hay cambios en las sesiones existentes.

En la versión de marzo de 2024 de Adobe Learning Manager, a continuación se indican los nuevos cambios:

* Actualización de los detalles de la sesión e invitación a sesión (para alumno e instructor)
   * En futuras sesiones, los correos electrónicos de actualización de **los detalles****de la sesión y la invitación** a sesión de los alumnos inscritos y los instructores actuales quedarán en desuso. En sesiones anteriores, los correos electrónicos actualizados de los detalles **de la sesión y** de **la invitación** de sesión de los alumnos inscritos y los instructores actuales se mantendrán como están.
* Mensajes de correo electrónico de recordatorio (para el administrador y el alumno)
   * Para futuras sesiones, solo **se enviarán correos electrónicos de recordatorio** de sesión.

>[!NOTE]
>
>Los correos no dependen de la finalización de la sesión y del curso.


### Cambios en el sitio de referencia de AEM

En un sitio de referencia de AEM, hemos agregado compatibilidad para agregar el token de actualización del administrador al token de acceso del alumno.

### Ocultar envíos a los instructores

Después de que los alumnos cargan sus archivos mediante el flujo de trabajo de envío de archivos, si un instructor no realiza ninguna acción (aprueba o rechaza) en el envío, la URL de envío se oculta en la vista después de un número de días predefinido. Póngase en contacto con los equipos de CSAM de Adobe Learning Manager para establecer o modificar el número de días.

### Cambios en la terminología del producto

Hemos añadido las columnas *Instancia* y *Alumno* al vocabulario de terminología del producto.

### Cambios en la aplicación móvil

En esta versión de la aplicación móvil, los alumnos pueden programar y administrar recordatorios de cursos vencidos. Al hacer clic en una notificación de recordatorio vencida, podrá acceder a las siguientes opciones:

* Cancelar
* Ir al curso
* Recuérdamelo de nuevo en 3 días
* Recuérdame de nuevo en una semana

En Android: Al hacer clic en la notificación push, se le dirigirá a la página de resumen **del**curso.
En iOS: al hacer clic en la notificación push, se le dirigirá a la página de inicio de la aplicación. Esta es una limitación conocida en iOS.

### Cambios en la lista de comprobación de la aplicación de alumno en Salesforce

Si un alumno suspende una lista de verificación, no puede pasar al siguiente módulo o curso. Cuando se selecciona la casilla Lista de comprobación obligatoria, el alumno no puede avanzar en un curso si suspende la lista.

Al igual que con la aplicación web, si un alumno suspende una lista de comprobación en la aplicación Salesforce, verá un mensaje y no avanzará.

### Cambios en Connect VC

En las versiones actuales de Adobe Learning Manager, un alumno se marca **como No asistido** cuando se inscribe en una sesión de Connect VC, pero no cumple los criterios de finalización.

En esta versión, el estado cambia a **Aún por marcar**.

### Etiquetado blanco en Adobe Learning Manager

La aplicación móvil Adobe Learning Manager ahora admite la etiqueta blanca, lo que significa que ahora puede lanzar la aplicación con su propia marca.

Vea Etiquetado blanco en la [aplicación](white-label.md) móvil Adobe Learning Manager para obtener más información.

### Nueva columna en los CSV de migración

En esta versión, hay una nueva columna opcional, uniqueLoId, en los siguientes archivos .csv de migración.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>La **columna uniqueLoId** es opcional.


Si realiza una migración para actualizar un curso, un plan de aprendizaje o una certificación existentes, el curso, el plan de aprendizaje o la certificación con los **LOId** exclusivos se agregan a la aplicación de autor.

Durante la migración, debe actualizar los **valores exclusivos de LOId** en los CSV para curso, plan de aprendizaje o certificación, aunque se trate de una columna opcional.

Si no se añade la **columna uniqueLoId** antes de realizar la migración mientras se actualiza el curso existente o el plan de aprendizaje o la certificación que contiene **uniqueLOId**, tras la migración, los **valores uniqueLOId** se anularán con valores NULL.

>[!NOTE]
>
>La columna, **uniqueLoId**, no se aplica al archivo CSV de ayuda de trabajo.


>[!IMPORTANT]
>
>Los valores de columna deben ser exclusivos en toda la cuenta. No se puede usar el mismo valor con un curso o certificación.

Descargue los CSV del [Manual](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs) de migración.


### Valoración de la aplicación

Un alumno puede facilitar sus comentarios sobre la aplicación Adobe Learning Manager para mejorar aún más la experiencia con la aplicación. Si el alumno califica con cuatro estrellas o más, aparece un mensaje emergente que solicita al alumno que califique la aplicación en Play Store o App Store.

### Bluejeans ha llegado a su final de vida (EOL) en febrero de 2024

Queremos informarle que Bluejeans ha llegado a su final de vida (EOL) en febrero de 2024. Después de febrero de 2024, Bluejeans ya no recibirá actualizaciones ni soporte. Nuestros equipos de CSAM y soporte le ayudarán con cualquier pregunta o inquietud que pueda tener durante este período de transición.

Vea [los conectores en Adobe Learning Manager](integration-admin/feature-summary/connectors.md) para obtener más información sobre cómo configurar conectores.

### Cambios en el informe de acceso de inicio de sesión

El informe de acceso de inicio de sesión estará disponible solo durante los últimos cinco trimestres. Si algún administrador de integración solicita la descarga a petición de la exportación unificada con **acceso de inicio de sesión** marcado, Adobe Learning Manager mostrará un mensaje de error. Sin embargo, no hay impacto en otros informes.

### Cambios en ADFS

Los campos Tipo de empleado e ID de empleado de ADFS ya están disponibles en Adobe Learning Manager, según las asignaciones.

## Cambios en las API de esta versión

### API de alumno

En esta versión, hemos añadido compatibilidad con la API para que los alumnos vean el logotipo de marca y los temas personalizados en el nivel de grupo de usuarios.

Las API /account y /user?include=account devuelven cuatro campos, que se sustituyen específicamente en función del campo activo del usuario que pertenece a logoUrl, logoStylish y themeData.

### Nuevos atributos

Un nuevo atributo, isExpiredSubmission, en learningObjectResource, que muestra si el envío del recurso ha caducado o no.

* API GET /account: devuelve el nuevo atributo **expireSubmissionDuration** X, donde X es el número de días establecido. Si no se establece lo contrario, se devolverá 0.
* GET /LO API con el recurso incluye el nuevo atributo **isExpiredSubmission**&quot; True o False.
   * True, si el envío ha caducado y no se muestra &quot;submissionUrl&quot;.
   * Si es False, el envío no ha caducado y se obtiene &quot;submissionUrl&quot;.

### Cambios en la API en la lista de comprobación

Un curso puede constar de varios módulos, de los cuales Lista de comprobación es un tipo de módulo. Este módulo de lista de comprobación lo evalúa el instructor y se puede marcar como Suspendido o Aprobado, según una evaluación.

Pero en ambos casos el estado de la lista de verificación se marca como Completado y, de esta manera, el curso se marca como Completado.

En esta versión, la API de objetos de aprendizaje incluye el parámetro *isChecklistMandatory*. Si el valor es True, la lista de comprobación es obligatoria.

### Compatibilidad con varias configuraciones regionales

Ahora, un administrador puede descargar el informe de comentarios de L1 en el idioma que desee. Sin embargo, todavía no puede descargar los informes de comentarios de L1 para Power BI. En la solicitud de API, utilice el parámetro preferredLocale para especificar la configuración regional que desee.

### Cambios en el recuento de Resumen de instancias

Esto se aplica a las cuentas en las que las inscripciones en un curso de clase o clase virtual son superiores a 1000.

Si el número es menor que 1000, las inscripciones invalidan la caché y devuelven los valores actualizados en una llamada a la API GET Summary, como el número de inscripción, la finalización y seatLimit.

Si la cuenta está habilitada para esta función y el número de inscripciones es superior a 1000, los valores se recuperan de la memoria caché.

### Trazados en desuso

En la actualidad, las API de Learning Manager siguen una estructura de datos de gráficos, que le permite obtener datos atravesando el modelo de API a través de includes. Aunque puede atravesar una API hasta siete niveles, obtener los datos mediante una sola llamada a la API es costoso desde el punto de vista informático.

Recomendamos que todos los clientes existentes y nuevos hagan pequeñas llamadas varias veces en lugar de una llamada grande. Este enfoque evitará que se carguen datos no deseados en la llamada.

#### ¿Qué trazados están en desuso?

Las siguientes rutas están en desuso:

* /learningObjects
   * Trazados en desuso:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Rutas existentes:
      * enrollment.loInstance
      * instances.loResources
* /objetos de aprendizaje/{id}
   * Ruta en desuso:
      * enrollment.instances.subLoInstances.learningObject
   * Ruta existente:
      * enrollment.instances.subLoInstances
* /Inscripciones
   * Ruta en desuso:
      * loInstance.learningObject.enrollment
   * Nuevo trazado:
      * loInstance.learningObject
* /objetos de aprendizaje/{id}
   * Ruta en desuso:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nuevo trazado:
      * instance.subLoInstances

### Acceso de inicio de sesión y cambios en el archivo del informe de auditoría de usuarios para la API de trabajo

Con esta versión, la API de trabajo conservará el informe de acceso de inicio de sesión hasta cinco trimestres y el informe de auditoría de usuario durante seis meses. Si desea descargar los datos anteriores a este período de tiempo, debe pasar el parámetro de archivo, especificando el trimestre y el año. Consulte la carga útil de muestra.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Si intenta descargar el informe Acceso de inicio de sesión **que va más allá de** los cinco trimestres, aparece un mensaje de error. Si intenta descargar el informe de auditoría **del usuario, aparece un mensaje de error similar que supera los** seis meses.

### API en desuso

Vea [las desfasiones de API en Adobe Learning Manager](api-deprecations-list.md) para obtener una lista acumulativa de todas las API en desuso en el producto.

## Errores solucionados en esta actualización {#bug-fixes}

* Cuando un alumno se inscribe en un curso y luego intenta inscribirse en otro curso, aparece un mensaje de advertencia.
* Un grupo de usuarios, incluso después de ser eliminado, es visible en la búsqueda.
* Cuando los usuarios activan una gran cantidad de transcripciones de alumnos con una gran cantidad de datos, la cola de transcripciones de alumnos se bloquea e impide una nueva solicitud.
* Si una cuenta secundaria solicita a su cuenta principal que comparta un informe, la cuenta principal no puede hacerlo.
* Las direcciones URL de un curso y de una ruta de aprendizaje redirigen a ubicaciones incorrectas.
* Un alumno ve intermitentemente la instancia del curso de un curso diferente al hacer clic en el vínculo del curso en la página del catálogo.
* El **botón Darse de baja** no se muestra de la forma prevista después de la primera inscripción, pero se muestra después de una actualización.
* No puede guardar contenido ni una prueba que tenga un espacio en blanco en el nombre.
* En los cursos aprobados por el responsable, puede volver a inscribir a los alumnos en un grupo de usuarios.
* En algunos casos, si intenta agregar un campo activo adicional, aparece el mensaje de error &quot;No se han podido guardar los campos activos&quot;.
* El texto se desborda en el nombre de un curso dentro de una tarjeta de curso en la sección Cursos relacionados.
* Después de cambiar una instancia e inscribir a un alumno en ella, las instancias antiguas aún existen en el calendario de Outlook.
* Cuando un alumno de una cuenta de igual a igual intenta seleccionar la miniatura de un curso, aparece un mensaje de error.
* Cuando los alumnos se inscriben en un curso, reciben varias notificaciones de la inscripción.
* Si un usuario cambia manualmente el nombre de los catálogos creados en un conector, se crean nuevos catálogos y los cursos se publican en los catálogos incorrectos.
* Los usuarios que pertenezcan a cuentas inactivas siguen recibiendo correos electrónicos de suscripción.

### Correcciones de errores relacionadas con la API

* La API GET/users no recupera los detalles de un responsable.
* En una cuenta, los usuarios se crearon a través de una importación de usuarios FTP programada durante un tiempo de inactividad programado.
* En la aplicación móvil o en el modo inmersivo, después de eliminar o retirar una instancia de curso y seleccionar la siguiente instancia activa, se muestra el **botón Registrar interés** en lugar de **Inscribirme**.
* Cuando un alumno de una cuenta de igual a igual intenta seleccionar la miniatura de un curso utilizando la API del objeto de aprendizaje, aparece el error 403 Prohibido.

## Requisitos del sistema

Vea [los requisitos](system-requirements.md) del sistema de Adobe Learning Manager.

## Versiones anteriores de Adobe Learning Manager

* [Versión de noviembre de 2023](whats-new-november-2023.md)
* [Versión de julio de 2023](whats-new-2023-july.md)
