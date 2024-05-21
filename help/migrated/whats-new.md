---
description: Descubra las nuevas funciones y mejoras de la versión de marzo de 2024 de Adobe Learning Manager
jcr-language: en_us
title: Resumen de nuevas funciones
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: 90ebde8049357a4798aa9b23edfa57b8667d6232
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Resumen de nuevas funciones {#new-features-summary}

Descubra las nuevas funciones y mejoras de la versión de marzo de 2024 de Adobe Learning Manager.

Explora algunas de las últimas funciones de Adobe Learning Manager, como:

1. Importar aptitudes desde orígenes externos
1. Compatibilidad con varias marcas
1. Módulo de actividad de reevaluación de la lista de comprobación
1. Aplicación de aprendizaje móvil con etiqueta blanca

>[!NOTE]
>
>Mira esto [seminario web](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) para obtener más información sobre las nuevas funciones de esta versión.


## Novedades de esta versión {#whatsnewandchanged}

### Importar aptitudes desde orígenes externos

Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, mediante los conectores correspondientes. Esta mejora forma parte del objetivo de integrar Learning Manager con Skills Cloud y Talent Management Systems externos. Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en Learning Manager y estarán disponibles para los autores durante el flujo de trabajo de creación del curso. También se han realizado mejoras en la funcionalidad de búsqueda de aptitudes en toda la plataforma para proporcionar una mejor experiencia de búsqueda cuando la cuenta tiene un gran número de aptitudes.

Ver [Importar aptitudes](administrators/feature-summary/import-skills-external-sources.md) para obtener más información.

### Construcción de marca personalizada

Ahora podrá personalizar determinados elementos de la interfaz de usuario: el nombre de la organización, el logotipo y el tema de la interfaz de usuario en función de los grupos de usuarios disponibles en la cuenta. Por ejemplo, una organización con varias divisiones puede configurar un logotipo personalizado y un tema de la interfaz de usuario para que se muestren en cada división.

>[!NOTE]
>
>Esta función de varias marcas no se aplica a la vista del administrador. Siempre verán la marca a nivel de organización en su cuenta. Esto se debe a que se trata de una función que el alumno afronta y los administradores pueden no desearla en su cuenta.

Ver [Varias marcas personalizadas](administrators/feature-summary/themes.md#multiple-branding) para obtener más información.


## Cambios para cuentas con una base de usuarios grande

### Administrador: páginas del curso o de la ruta de aprendizaje

Si un gran número de alumnos se inscribe en el curso, por ejemplo, más de 50 000, no se mostrará la lista de alumnos. Puede buscar un alumno en el *Buscar alumnos* o seleccione la barra de búsqueda **Descargar** en la parte superior de la barra de búsqueda para descargar la lista de alumnos.

### Administrador: página de alumnos

Al buscar cualquier usuario, el **Descargar alumno** y **Exportar** opciones descargar el mismo informe. Mientras tanto, al buscar un grupo de usuarios, ahora puede descargar usuarios filtrados de ese grupo de usuarios. Al buscar en un grupo de usuarios, el **Descargar lista de alumnos** cambios en **Descargar lista de alumnos para grupos de usuarios** La **Exportar** de nuevo descarga toda la lista.

### Página Administrador: Usuarios

#### Usuarios internos

Si el número de usuarios supera, por ejemplo, los 50 000, se mostrará un mensaje para descargar los datos y realizar un análisis más detallado más adelante. La barra de búsqueda ahora está visible y muestra un usuario en el formato *Nombre, correo electrónico | UUID*.

>[!NOTE]
>
>El UUID solo se muestra si el UUID está habilitado para la cuenta.

#### Usuarios externos

Para los usuarios externos, se aplica el mismo comportamiento. Si el número de usuarios es grande, puede descargar los usuarios y también recuperar los detalles de un usuario después de una búsqueda en el formato *Nombre, correo electrónico | UUID*.

#### Página Limpieza de usuarios

En la página Limpieza de usuarios, para los usuarios eliminados, hemos eliminado la capacidad de ordenación en **Fecha de eliminación**. Solo puede ordenar por los UUID.

### Páginas Admin- Instancia

#### Ruta del curso o aprendizaje

Si el número de inscripciones es grande, Adobe Learning Manager no mostrará el número de alumnos. En su lugar, aparecerá un icono que puede seleccionar, ver el número de alumnos e ir a la página Alumnos.

El número de alumnos se mostrará como un valor aproximado. Por ejemplo, si el número de alumnos es superior a 50 000, el valor se mostrará como más de 50 000.

### Páginas L1/L3 para administradores

En la página Comentarios de L1, si el número de inscripciones de cursos es grande, no se muestra la lista de alumnos. En su lugar, puede exportar la lista de usuarios para un análisis más detallado más adelante.

La búsqueda admite escritura anticipada y los resultados se restringen a la instancia seleccionada.

#### Página Asistencia y Puntuación

En la página, al buscar un usuario, la búsqueda se ejecuta en todas las instancias disponibles. Sin embargo, el resultado es para la instancia seleccionada.

En la página Asistencia, si busca un grupo de usuarios y el número de usuarios supera los 10 000 en el grupo de usuarios, independientemente de la inscripción, solo puede realizar acciones en bloque. No podrá ver la lista de usuarios.

Si el número de usuarios en el grupo de usuarios es inferior a 10 000, puede realizar acciones individuales a nivel de usuario junto con acciones a nivel masivo. En este caso, la lista de usuarios no está deshabilitada.

### Página Administrador: Certificaciones

En las versiones actuales de Adobe Learning Manager, si hay un gran número de usuarios inscritos en una certificación, no es posible ver a los alumnos que se han dado de baja desde el **Estado** el menú desplegable está desactivado.

En esta versión de Adobe Learning Manager, si el número de usuarios inscritos es grande, la **Estado** el menú desplegable solo muestra dos opciones: **Inscrito** y **Dado de baja**. La opción **Inscrito** está seleccionado de forma predeterminada. Si selecciona **Dado de baja**, se muestra la lista de alumnos que se han dado de baja.

#### Cambios en el grupo de usuarios

En el caso de un grupo de usuarios, si el número de usuarios en el grupo de usuarios es menor que, por ejemplo, 50 000, el **Estado** El menú desplegable muestra todas las opciones: Certificado, Asignado y Caducado.

Si el número de usuarios de un grupo de usuarios es grande, el **Estado** el menú desplegable solo muestra dos opciones: **Inscrito** y **Dado de baja**, según el nuevo diseño.

### Tabla de comparación

<table>
    <tbody>
        <tr>
            <td><b>Página</b></td>
            <td><b>Antes del cambio de umbral</b></td>
            <td><b>Después del cambio de umbral</b></td>
        </tr>
        <tr>
            <td>Administrador: instancia del curso</td>
            <td>Las instancias se muestran tal y como se han diseñado con lo siguiente:
            <ul>
                <li>Módulos</li>
                <li>Alumnos inscritos</li>
                <li>Sesiones</li>
                <li>Insignia</li>
                <li>Comentarios de L1 activados</li>
                <li>Alertas de notificación</li>
                <li>Puntos de interacción</li>
                <li>Código QR</li>
                <li>Extensión Ruta de aprendizaje</li>
            </ul>
            <td>
                <ul>
                    <li>Si el número de inscripciones supera el umbral predefinido, ALM no mostrará el recuento; sustituirá el recuento por un icono que, al hacer clic en él, muestra el número real de alumnos y un vínculo para llevarle a la página Alumnos.</li>
                    <li>El número de inscripciones se mostrará en un formato aproximado. Por ejemplo, si el número es superior a 50 000, el recuento se mostrará como 50 000 en el nivel del curso.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador: página de alumnos</td>
            <td>
                    <ul>
                        <li>Se muestra la lista de alumnos de cada instancia.</li>
                        <li>Puede buscar un usuario o un grupo de usuarios inscritos en un curso.</li>
                        <li>El informe exportado no consta de ningún filtro para Grupo de usuarios.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia está desactivada.</li>
                    <li>La lista Descargar alumno también descarga los mismos datos, excepto en un caso. Si busca un grupo de usuarios y, a continuación, selecciona Descargar lista de alumnos, se descargarán los datos de ese grupo de usuarios.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página de comentarios del administrador de L1/L3</td>
            <td>
                <p>Sin cambios en el comportamiento existente</p>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia está desactivada.</li>
                    <li>Si la inscripción en un curso es superior a 50 000, ALM no muestra a los alumnos y solo muestra la barra de búsqueda. Si la inscripción es inferior a 50 000, ALM muestra la lista de alumnos y la barra de búsqueda.</li>
                    <li>El anuncio está desactivado de forma predeterminada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador: página Asistencia y Puntuación</td>
            <td>
                <p>Sin cambios en el comportamiento existente</p>
            </td>
            <td>
                <ul>
                    <li>La selección de instancia se desactiva al buscar un usuario.</li>
                    <li>Si el número de usuarios supera, por ejemplo, los 50 000, se mostrará un mensaje adicional para descargar los datos y realizar un análisis más detallado más adelante. La barra de búsqueda ahora está visible y muestra un usuario con el formato Nombre, correo electrónico | UUID.</li>
                    <li>Si el número de usuarios del grupo de usuarios es inferior a 10 000, independientemente de la inscripción, puede realizar acciones individuales a nivel de usuario junto con acciones a nivel masivo. En este caso, la lista de usuarios no está deshabilitada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Administrador: Puntuación de prueba de L2</td>
            <td>
                    <ul>
                        <li>También se implementa la búsqueda de usuarios.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>También se implementa la búsqueda de usuarios. Mientras que la búsqueda de escritura anticipada se realiza en el nivel de objeto de aprendizaje, el listado se filtra a la instancia seleccionada actualmente.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador: página Usuarios (internos, externos)</td>
            <td>
                    <ul>
                        <li>El ID de correo electrónico se muestra al buscar un usuario.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Si el número de usuarios supera, por ejemplo, los 50 000, habrá un mensaje adicional para descargar los datos y realizar un análisis más detallado más adelante. La barra de búsqueda ahora está visible y muestra un usuario con el formato Nombre, correo electrónico | UUID.</li>
                    <li>En la página Limpieza de usuarios, para los usuarios eliminados, hemos eliminado la función de ordenación en **Fecha de eliminación**. Solo puede ordenar por los UUID.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instructores: envío</td>
            <td>
                    <ul>
                        <li>Paginación de los módulos que deben presentarse.</li>
                        <li>Como instructor, ahora puede filtrar los envíos de archivos de los alumnos en función del estado, la finalización de la revisión, el envío pendiente, el aprobado y el suspenso. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>En esa instancia, solo puede buscar usuarios, no grupos de usuarios.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Contar con la vista previa como página del alumno</td>
            <td>
                    <ul>
                        <li>Count incluye los datos de una inscripción de pedidos superior.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Count excluye datos de inscripciones de pedidos superiores.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Funciones de búsqueda avanzadas

En esta versión, hemos mejorado la experiencia de búsqueda. Los resultados de la búsqueda se obtienen no solo en función de los metadatos, sino también de la búsqueda semántica y en el contenido para obtener resultados basados en la precisión, la actualidad y el contenido relevante.

Este cambio se refleja en lo siguiente:

* Página Catálogo y Mi aprendizaje: Se ha eliminado la acción de pasar el cursor en el curso, la ruta de aprendizaje y la certificación.
* Apariencia de la barra de búsqueda.
* Se han añadido etiquetas de filtro en la aplicación de aprendizaje.

Para habilitar las funciones de búsqueda, póngase en contacto con el equipo de CSAM de Adobe Learning Manager.

## Cambios en la interfaz de usuario {#ui-changes}

### Página de creación del curso

Al asignar los cursos a un nivel de aptitud, la lista de aptitudes es la búsqueda. En otras palabras, busque aptitudes y verá una lista de aptitudes que coinciden con el término buscado.

### Grupos de usuarios

#### Página Administrador: Alumnos

Al buscar cualquier usuario, el **Descargar alumno** y **Exportar** opciones descargar el mismo informe. Mientras tanto, al buscar un grupo de usuarios, ahora puede descargar usuarios filtrados de ese grupo de usuarios. Al buscar en un grupo de usuarios, el **Descargar lista de alumnos** cambios en **Descargar lista de alumnos para grupos de usuarios** La **Exportar** de nuevo descarga toda la lista.

## Cambios en los informes

* Las columnas Etiquetas y Aptitudes del informe de cursos de formación se han cambiado a Etiquetas y aptitudes.
* Se ha añadido el informe [Seguimiento de auditoría de interacción](administrators/feature-summary/reports.md#gamification-audit-trail).
* Si una cuenta contiene más de 280 000 alumnos asignados a una aptitud, el informe de aptitud-alumno se descarga como un archivo .csv comprimido.
Si la cuenta tiene menos de 250 000 alumnos, se descarga el mismo informe como CSV.
En la página Administrador, seleccione **Administrador** > **Aptitudes** > **Aptitud** > **Alumnos**. El informe se descarga como CSV.
* La [Informe de resumen de sesión](administrators/feature-summary/reports.md#session-summary-report) tiene dos nuevas columnas: Información de Ubicación y Región Ubicación.

## Cambios en la creación de clases

Según [Configuración de administrador](administrators/feature-summary/classroom.md#classroom-settings), como autor, puede [crear, modificar y eliminar ubicaciones](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>Al añadir etiquetas de ubicación y de catálogo, los autores (en la página de creación del curso) y los administradores (en la página de instancia) verán una lista de ubicaciones y etiquetas de catálogo rellenada automáticamente, respectivamente.

Como administrador, puede imponer restricciones a un autor para modificar o eliminar una ubicación de clase. Ver [Configuración de clase](administrators/feature-summary/classroom.md#classroom-settings) para obtener más información.

## Cambios en la ruta de aprendizaje flexible

Todas las cuentas (antiguas y nuevas) de empezarán a incluir la fecha límite de inscripción, la fecha límite de cancelación de inscripción y el límite de puestos en la aplicación del alumno para una ruta de aprendizaje flexible.
Los alumnos ahora podrán inscribirse en la ruta de aprendizaje flexible sin seleccionar ninguna instancia del curso.

## Nuevo desencadenador para planes de aprendizaje

Se ha añadido un nuevo activador a la página de configuración del plan de aprendizaje. Los autores y los administradores ahora podrán activar acciones cuando un alumno suspenda un módulo de un curso.

Ver [Planes de aprendizaje](administrators/feature-summary/learning-plans.md) para obtener más información.

## Nuevo estado de envío

Como instructor, ahora puede filtrar los envíos de archivos de los alumnos en función del estado, la finalización de la revisión, el envío pendiente, el aprobado y el suspenso.

Ver [Estado del envío](instructors/feature-summary/learners.md#filter-file-submissions) para obtener más información.

## Mejoras de lista de comprobación

En la versión de marzo de 2024 de Adobe Learning Manager, las mejoras realizadas en el flujo de trabajo de lista de comprobación son las siguientes:

### No permitir el progreso en el error de una lista de comprobación

Al crear una lista de comprobación, un autor puede seleccionar **Habilitar** en la sección Lista de comprobación obligatoria. Al hacerlo, se impide que un alumno continúe en el módulo si no supera la lista de comprobación. Sólo pueden continuar si pasan la lista de comprobación.

Los revisores de la lista de comprobación, es decir, los instructores o responsables, pueden comprobar el estado de la lista de comprobación. Los revisores también pueden revisar la lista de comprobación de un alumno sin ordenar.

### Reevaluación de una lista de comprobación

Al crear una lista de comprobación, un autor puede seleccionar **Habilitar** en la sección Reevaluación. De este modo, un responsable o un instructor pueden volver a evaluar a un alumno hasta que apruebe la lista de comprobación.

Si el módulo es obligatorio, la casilla de verificación de reevaluación estará seleccionada de forma predeterminada.

Un instructor o responsable también puede cambiar el estado de una lista de comprobación de No superado a Aprobado cuando la reevaluación está habilitada.

En la página Lista de comprobación , un instructor puede ver el número de alumnos que están en estado Pendiente. Como instructor, puede evaluar a un alumno y aprobarlo o suspenderlo. Si un alumno se encuentra en estado suspendido, solo podrá ver la lista de comprobación cuando la reevaluación no esté activada.

Esto significa que el **Habilitar** no se seleccionó la casilla de verificación en la sección Reevaluación al crear la lista de comprobación. Si esta casilla de verificación está seleccionada, aparecerá el botón Ver/Volver a evaluar en la página Lista de comprobación del instructor .

Al seleccionar el botón, puede volver a evaluar a un alumno y marcarlo como aprobado o suspendido.

>[!NOTE]
>
>Ambas funciones (Volver a evaluar y Convertir la lista de comprobación en obligatoria) solo se aplican a los módulos recién creados. Una vez publicado un curso, no se puede activar ni desactivar.


Ver [Crear una lista de comprobación](authors/feature-summary/courses.md#checklist-fail) para obtener más información.

## Otras mejoras

### Notificaciones por correo electrónico relacionadas con la sesión

En versiones anteriores de Adobe Learning Manager, un alumno no enviaba correos electrónicos relacionados con la sesión, actualizaba los detalles de la sesión, invitaba a la sesión y recordaba la sesión cuando:

* Los alumnos han completado un curso,
* Se añaden nuevas sesiones a un curso, o
* Hay cambios en las sesiones existentes.

En la versión de marzo de 2024 de Adobe Learning Manager, los nuevos cambios son los siguientes:

* Detalles de la sesión actualizada e invitación de sesión (para alumno e instructor)
   * Para sesiones futuras, correos electrónicos para **Detalles de sesión actualizados**, **Invitación de sesión** para alumnos inscritos y los instructores actuales quedarán obsoletos. Para sesiones anteriores, correos electrónicos para **Detalles de sesión actualizados** y **Invitación de sesión** para los alumnos inscritos Los alumnos y los instructores actuales se mantendrán tal cual.
* Correos electrónicos de recordatorio (para administradores y alumnos)
   * Sólo para futuros períodos de sesiones **Recordatorio de sesión** se enviarán correos electrónicos.

>[!NOTE]
>
>Los correos electrónicos no dependen de la finalización de la sesión y del curso.


### AEM Cambios en el sitio de referencia

En un sitio de referencia de AEM, hemos añadido compatibilidad para añadir el token de actualización de administrador al token de acceso de alumno.

### Ocultar envíos de instructores

Después de que los alumnos carguen sus archivos mediante el flujo de trabajo de envío de archivos, si un instructor no realiza ninguna acción (aprobar o rechazar) en el envío, la URL de envío se oculta de la vista tras un número de días predefinido. Póngase en contacto con los equipos de CSAM de Adobe Learning Manager para definir o cambiar el número de días.

### Cambios en la terminología del producto

Hemos añadido las columnas *Instancia* y *Alumno* al vocabulario terminológico del producto.

### Cambios en aplicaciones móviles

En esta versión de la aplicación móvil, los alumnos pueden programar y administrar recordatorios de cursos vencidos. Al hacer clic en una notificación de recordatorio vencida, podrá acceder a las siguientes opciones:

* Cancelar
* Ir al curso
* Recuérdame de nuevo en 3 días
* Recuérdame de nuevo en una semana

En Android: al hacer clic en la notificación push, accederá al **Resumen del curso** página.
En iOS: Hacer clic en la notificación push le dirigirá a la página de inicio de la aplicación. Esta es una limitación conocida en iOS.

### Cambios en la lista de comprobación de la aplicación del alumno en Salesforce

Si un alumno no supera una lista de comprobación, no puede pasar al siguiente módulo o curso. Cuando se selecciona la casilla de verificación Lista de comprobación obligatoria , el alumno no puede avanzar en un curso si no supera la lista de comprobación.

Al igual que con la aplicación web, si un alumno falla en una lista de comprobación de la aplicación de Salesforce, verá un mensaje y no seguirá adelante.

### Cambios en Connect VC

En las versiones actuales de Adobe Learning Manager, se marca a un alumno **No asistido** cuando se inscriben en una sesión de clase virtual de Connect, pero no cumplen los criterios de finalización.

En esta versión, el estado cambia a **Aún por marcar**.

### Etiquetado de blancos en Adobe Learning Manager

La aplicación móvil de Adobe Learning Manager ahora admite el etiquetado blanco, lo que significa que ahora puede publicar la aplicación con su propia marca.

Ver etiquetado blanco en [Aplicación móvil de Adobe Learning Manager](white-label.md) para obtener más información.

### Nueva columna en archivos CSV de migración

En esta versión, hay una nueva columna opcional, uniqueLoId, en los siguientes archivos CSV de migración.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>La **uniqueLoId** es opcional.


Si realiza una migración para actualizar un curso o plan de aprendizaje o certificación existente, el curso o plan de aprendizaje o certificación con el **uniqueLOId** s se añade a la aplicación de autor.

Durante la migración, debe actualizar el **uniqueLOId** en los archivos CSV del curso, el plan de aprendizaje o la certificación, aunque sea una columna opcional.

Si el **uniqueLoId** no se añade antes de realizar la migración al actualizar el curso, el plan de aprendizaje o la certificación existentes que tienen **uniqueLOId** s y, después de la migración, el **uniqueLOId** los valores se reemplazarán por valores NULL.

>[!NOTE]
>
>La columna, **uniqueLoId**, no es aplicable al archivo CSV de ayudas de trabajo.


>[!IMPORTANT]
>
>Los valores de columna deben ser únicos en toda la cuenta. No puede utilizar el mismo valor con un curso o certificación.

Descargue los archivos CSV de la [Manual de migración](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### Clasificación de aplicaciones

Un alumno puede proporcionar sus comentarios en la aplicación de Adobe Learning Manager para mejorar aún más la experiencia de la aplicación. Si el alumno valora cuatro estrellas o más, aparece un mensaje emergente que solicita al alumno que valore la aplicación en Play Store o App Store.

### Bluejeans ha llegado a su final de vida (EOL) en febrero de 2024

Queremos informarte de que BlueJeans ha llegado a su final de vida (EOL) en febrero de 2024. Después de febrero de 2024, BlueJeans ya no recibirá actualizaciones ni asistencia técnica. Nuestro CSAM y los equipos de asistencia le ayudarán con cualquier pregunta o duda que pueda tener durante este período de transición.

Ver [Conectores en Adobe Learning Manager](integration-admin/feature-summary/connectors.md) para obtener más información sobre la configuración de conectores.

### Cambios en el informe Acceso de inicio de sesión

El informe Acceso de inicio de sesión solo estará disponible durante los últimos cinco trimestres. Si algún administrador de integración solicita la descarga a petición de la exportación unificada con **Acceso de inicio de sesión** marcado, Adobe Learning Manager mostrará un mensaje de error. Sin embargo, no hay repercusiones en otros informes.

### Cambios de ADFS

Los campos Tipo de empleado e Id. de empleado de ADFS ahora están disponibles en Adobe Learning Manager, según las asignaciones.

## Cambios en las API de esta versión

### API de alumno

En esta versión, hemos añadido compatibilidad con API para que los alumnos vean el logotipo de la marca y los temas personalizados en el nivel de grupo de usuarios.

Las API /account y /user?include=account devuelven cuatro campos, que se reemplazan de forma específica en el campo activo del usuario que pertenece a logoUrl, logoStyling y themeData.

### Nuevos atributos

Un nuevo atributo, isExpiredSubmission, en learningObjectResource, que muestra si el envío del recurso ha caducado o no.

* API de GET/cuenta: devuelve un nuevo atributo **expireSubmissionDuration** X, donde X es el número de días establecidos. Si no se establece, se devolverá 0
* La API de GET/LO con el recurso incluye un nuevo atributo **isExpiredSubmission**&quot; True o False.
   * True, si el envío ha caducado y no se muestra &quot;submitUrl&quot;.
   * Si es False, el envío no caduca y se obtiene &quot;submitUrl&quot;.

### Cambios en la API en Lista de comprobación

Un curso puede constar de varios módulos, de los que Checklist es un tipo de módulo. El instructor evalúa este módulo de lista de comprobación y puede marcarlo como Suspendido o Correcto en función de la evaluación.

Sin embargo, en ambos casos, el estado de la lista de comprobación se marca como Completado y, de esta manera, el curso se marca como Completado.

En esta versión, la API de objeto de aprendizaje incluye el parámetro *isChecklistObligatorio*. Si el valor es True, la lista de comprobación es obligatoria.

### Compatibilidad con varias configuraciones regionales

Un administrador puede descargar ahora el informe de comentarios de L1 en el idioma que prefiera. Sin embargo, aún no puede descargar informes de comentarios de L1 para Power BI. En la solicitud de API, utilice el parámetro preferredLocale para especificar la configuración regional que desee.

### Cambios en el resumen de recuento de instancias

Esto es aplicable a las cuentas en las que las inscripciones para un curso de clase o clase virtual sean superiores a 1000.

Si el número es menor que 1000, las inscripciones invalidan la memoria caché y devuelven los valores actualizados en una llamada a la API de resumen de GET, como el número de inscripciones, la finalización y el límite de licencias.

Si la cuenta está activada para esta función y el número de inscripciones es superior a 1000, los valores se recuperan de la caché.

### Rutas en desuso

En la actualidad, las API de Learning Manager siguen una estructura de datos de gráficos, que le permite obtener datos a través del modelo de API mediante includes. Aunque se puede recorrer una API de hasta siete niveles, obtener los datos mediante una sola llamada de API resulta computacionalmente caro.

Recomendamos que todos los clientes nuevos y existentes realicen llamadas pequeñas varias veces en lugar de una llamada grande. Este enfoque evitará que se carguen datos no deseados en la llamada.

#### ¿Qué rutas están obsoletas?

Las siguientes rutas están en desuso:

* /learningObjects
   * Rutas obsoletas:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Rutas existentes:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Ruta obsoleta:
      * enrollment.instances.subLoInstances.learningObject
   * Ruta existente:
      * enrollment.instances.subLoInstances
* /enrollments
   * Ruta obsoleta:
      * loInstance.learningObject.enrollment
   * Nueva ruta:
      * loInstance.learningObject
* /learningObjects/{id}
   * Ruta obsoleta:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nueva ruta:
      * instance.subLoInstances

### Cambios de archivado de acceso de inicio de sesión e informe de auditoría de usuarios para la API de trabajos

Con esta versión, la API de trabajos conservará el informe de acceso de inicio de sesión hasta cinco trimestres y el informe de auditoría de usuarios durante seis meses. Si desea descargar los datos anteriores a este período de tiempo, debe pasar el parámetro de archivo, especificando trimestre y año. Consulte la carga útil de ejemplo.

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

Si intenta descargar el **Acceso de inicio de sesión** informe que va más allá de cinco trimestres, aparece un mensaje de error. Aparecerá un mensaje de error similar si intenta descargar el **Auditoría de usuarios** informe que va más allá de seis meses.

### API en desuso

Ver [Obsoletaciones de API en Adobe Learning Manager](api-deprecations-list.md) para obtener una lista acumulativa de todas las API obsoletas del producto.

## Errores solucionados en esta actualización {#bug-fixes}

* Cuando un alumno se inscribe en un curso y luego intenta inscribirse en otro curso, se muestra un mensaje de advertencia.
* Un grupo de usuarios, incluso después de eliminarlo, es visible en la búsqueda.
* Cuando los usuarios activan muchas transcripciones de alumnos con una gran cantidad de datos, la cola Transcripciones de alumnos se bloquea e impide una nueva solicitud.
* Si una cuenta secundaria solicita a su cuenta principal que comparta un informe, la cuenta principal no puede hacerlo.
* Las direcciones URL de un curso y una ruta de aprendizaje se redirigen a ubicaciones incorrectas.
* Un alumno ve de forma intermitente la instancia de curso de un curso diferente al hacer clic en el vínculo del curso en la página del catálogo.
* La **Dar de baja** El botón no se muestra del modo esperado después de la primera inscripción, pero aparece después de actualizar.
* No se puede guardar contenido o una prueba que tenga un espacio en blanco en el nombre.
* En los cursos aprobados por el responsable, puede volver a inscribir a los alumnos en un grupo de usuarios.
* En algunos casos, si intenta agregar un campo activo adicional, aparece el mensaje de error &quot;No se pudieron guardar los campos activos&quot;.
* El texto se desborda en el nombre de un curso dentro de una tarjeta de curso en la sección Cursos relacionados .
* Después de cambiar una instancia e inscribir a un alumno en la instancia, las instancias anteriores siguen existiendo en el calendario de Outlook.
* Cuando un alumno de una cuenta de igual a igual intenta seleccionar la miniatura de un curso, se muestra un mensaje de error.
* Cuando los alumnos se inscriben en un curso, reciben varias notificaciones de inscripción.
* Si un usuario cambia manualmente el nombre de los catálogos creados en un conector, se crean nuevos catálogos y los cursos se publican en los catálogos incorrectos.
* Los usuarios que pertenecen a cuentas inactivas siguen recibiendo correos electrónicos de suscripción.

### Correcciones de errores relacionados con la API

* Los usuarios/GET de la API no recuperan los detalles de un responsable.
* En una cuenta, los usuarios se crearon a través de una importación de usuarios de FTP programada durante un tiempo de inactividad programado.
* En la aplicación móvil o en el modo inmersivo, después de eliminar o retirar una instancia de curso y seleccionar la siguiente instancia activa, el **Registrar interés** aparece en lugar de **Inscribir**.
* Cuando un alumno de una cuenta de igual a igual intenta seleccionar la miniatura de un curso mediante la API de objeto de aprendizaje, se muestra el error 403 Prohibido.

## Requisitos del sistema

Ver [Requisitos del sistema de Adobe Learning Manager](system-requirements.md).

## Versiones anteriores de Adobe Learning Manager

* [Versión de noviembre de 2023](whats-new-november-2023.md)
* [Versión de julio de 2023](whats-new-2023-july.md)
