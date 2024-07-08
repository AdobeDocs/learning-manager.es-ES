---
description: Obtenga información sobre los informes asociados a la función de administrador en la aplicación Learning Manager.
jcr-language: en_us
title: Informes
contentowner: manochan
exl-id: 31b176b7-4b8f-4851-a0c5-4eee58bceb41
source-git-commit: 7be69e68f3b8970e090c8eccd25771cd2e5e99f1
workflow-type: tm+mt
source-wordcount: '7132'
ht-degree: 57%

---

# Informes

Obtenga información sobre los informes asociados a la función de administrador en la aplicación Learning Manager.

Adobe Learning Manager le permite crear diversos informes para supervisar y controlar las actividades de los alumnos. Las actividades de los alumnos se supervisan y se capturan automáticamente en la base de datos. Los informes del responsable y el administrador se generan a partir de la base de datos.

## Información general {#overview}

El proceso de generación de informes es similar para el administrador y el responsable. Los responsables pueden ver los informes correspondientes a sus subordinados, mientras que el administrador puede ver todos los informes en toda la empresa.

Los informes se añaden en un tablero. Un informe debe estar dentro de un tablero. De manera predeterminada, verá un **[!UICONTROL tablero]** predeterminado en la página Informes. Cualquier informe añadido por usted se añade a este tablero predeterminado. Para añadir informes a tableros individuales, utilice la tecla de flecha desplegable y escoja **[!UICONTROL Añadir informe]**. Para obtener más información sobre cómo crear tableros, consulte la sección Tableros en esta página.

## Tipos de informes {#typesofreports}

Adobe Learning Manager admite cuatro tipos principales de informes: de finalización, tiempo dedicado, aptitudes y eficacia. Puede utilizar los siguientes tipos de informes para generar informes de 300+ variaciones:

* Estadísticas de entrega del curso para alumnos
* Informe sobre la eficacia de los cursos
* Informe basado en las aptitudes del alumno
* Estadísticas de inscripción en el programa de aprendizaje para alumnos
* Tiempo de aprendizaje dedicado por los alumnos
* Recuento de alumnos
* Finalización de la certificación

## Tableros de actividad de usuario {#useractivitydashboards}

Vea un resumen de toda la actividad de los usuarios en la plataforma a lo largo del tiempo. Configure grupos de usuarios y aplique filtros.

En el tablero de actividad de usuario, se muestra la actividad de los usuarios de la cuenta. Los tres informes que se enumeran son:

* **Usuarios registrados:** Este informe proporciona información sobre el número de usuarios registrados en su cuenta semana tras semana. En el caso de las cuentas con licencias de unidades activas mensuales, el informe presenta en su lugar las unidades MAU.

* **Informe de visitas de usuarios:** Este informe proporciona información sobre el número de usuarios que acceden a la plataforma en el día a día. También está disponible el informe mensual.

* **Informe de tiempo de aprendizaje dedicado:** este informe proporciona información sobre el tiempo de aprendizaje dedicado en la plataforma en el día a día. También está disponible el informe mensual.

### Usuarios registrados {#registeredusers}

Learning Manager realiza un recuento del número de usuarios registrados en el sistema cada semana. Los administradores pueden ver este informe para conocer el número de usuarios registrados ese día de la semana. Una vez almacenado, el recuento semanal de usuarios registrados no cambia. Por lo tanto, el recuento registrado histórico no está relacionado con el conjunto actual de alumnos del sistema.

Este informe proporciona información sobre el número de usuarios registrados en la cuenta semanalmente.

En el caso de las cuentas con licencias de unidades activas mensuales, el informe presenta en su lugar las unidades MAU.

![](assets/registered-usersreport.png)
*Informe de usuarios registrados*

***Para las cuentas de unidad de acceso mensual:***

**Informe mensual de usuarios activos**

En este informe, se muestra el recuento de alumnos activos en la plataforma de aprendizaje cada mes. Un usuario se considera activo durante el mes si realiza cualquiera de las acciones de aprendizaje mencionadas aquí. Es el mismo método utilizado para el recuento de las unidades activas mensuales.

Una vez realizado y almacenado, el recuento activo mensual no cambia. Por lo tanto, el recuento histórico mostrado no está relacionado con el conjunto actual de alumnos del sistema.

### Visitas de usuarios {#uservisits}

En este informe, se muestra el total de alumnos que acceden al sistema en un día o un mes. Explorar la plataforma de aprendizaje sin consumir ningún elemento de aprendizaje también se considera como un &quot;acceso&quot; a la plataforma de aprendizaje. Esto ayuda al administrador a conocer el conjunto total de usuarios que acceden al sistema. El primer día del mes, Learning Manager crea un registro del número total de usuarios que acceden a la plataforma durante el mes anterior. También captura la información del grupo de usuarios para estos usuarios.

Solo se registran los grupos de usuarios configurados por el administrador. Esto permite a los administradores aplicar filtros en grupos de usuarios para los datos mensuales históricos. Tenga en cuenta que, en caso de que se modifique la configuración de los grupos de usuarios y el Administrador de aprendizaje no hubiera registrado datos para este grupo de usuarios en meses anteriores, en ese caso el Administrador de aprendizaje no puede mostrar los datos de los grupos de usuarios recién configurados para los meses anteriores.

Este informe contiene usuarios que acceden a la plataforma mediante todos los formatos, como la Web, la aplicación para dispositivos móviles, las soluciones personalizadas sin encabezado, etc. El gráfico de uso de la aplicación para dispositivos menciona específicamente solo a los usuarios que acceden a la plataforma mediante la aplicación de Learning Manager para dispositivos. Esto ayuda a los administradores a identificar el uso de la aplicación para dispositivos móviles en la cuenta.

![](assets/user-visit-report.png)
*Informe de visitas de usuarios*

### Informe de tiempo dedicado al aprendizaje {#learningtimespentreport}

Aquí puede ver un gráfico de líneas de doble eje que muestra el tiempo total de aprendizaje dedicado por todos los alumnos durante un periodo de 12 meses. El segundo eje representa el tiempo medio dedicado al aprendizaje por parte de un individuo.

El tiempo dedicado a diferentes objetos de aprendizaje, como programas de aprendizaje y certificaciones, se calcula para lo siguiente:

* Curso a ritmo personalizado con contenido estático e interactivo.
* Cursos de actividades con url.
* Sesiones de fin de semana con el indicador de fin de semana activado.
* Sesión de conexión de clase virtual donde la asistencia se marca automáticamente.
* Tiempo empleado en diferentes objetos de aprendizaje, como programas de aprendizaje y certificaciones.
* Declaraciones xAPI para un curso de actividad de xAPI.

Puede exportar el gráfico como una hoja de cálculo de Excel.

Se proporciona un filtro para elegir la configuración de grupos de usuarios, que le ayudará a ver los datos en relación con los diferentes grupos de usuarios.

El filtro de fecha y grupo de usuarios seleccionado se aplica a todos los gráficos pertinentes del tablero.

>[!NOTE]
>
>En los informes **[!UICONTROL Visitas de usuarios]** y **[!UICONTROL Tiempo de aprendizaje empleado]**, se mostrarán los datos predeterminados (cuando no se ha configurado ningún grupo de usuarios) de toda la cuenta.

## Tablero de contenido de formación {#trainingcontentdashboard}

El tablero de contenido de formación ofrece información sobre los cursos disponibles en la plataforma. Puede ver los cursos de formación más populares o realizar un seguimiento de todos los cursos disponibles.

### Informe de cursos de formación {#trainingsreport}

Este informe proporciona información sobre el total de cursos de formación disponibles en la plataforma (con el estado Publicado) mensualmente. En él, se indica el número de cursos de formación que se ofrecen a lo largo del tiempo.

![](assets/training-report.png)
*Informe de formación*

### Informe de cursos de formación activos {#activetrainingsreport}

Este informe proporciona información sobre los cursos de formación que están activos durante el intervalo de tiempo seleccionado. Los cursos de formación activos son aquellos que permiten la inscripción, su visualización en un reproductor o su finalización en un periodo determinado.

En los cursos de formación activos, se pueden seleccionar todos los datos de los grupos de usuarios raíz (con función de responsable) si no se ha configurado ningún grupo de usuarios. Además de los grupos de usuarios de usuario raíz, puede configurar otros 10 grupos de usuarios si es necesario.

![](assets/active-trainingsreport.png)
*Informe de entrenamientos activos*

>[!NOTE]
>
>Los datos no se muestran de la forma prevista cuando **[!UICONTROL se seleccionan los filtros Todos los usuarios]** y **[!UICONTROL 12 meses]** , pero sí cuando se selecciona **[!UICONTROL Todo el grupo] de usuarios internos.**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Referencia</b></p></td>
   <td>
    <p><b>Estadística</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Porcentaje del índice de inicio</p></td>
   <td>
    <p>Relación entre el número de alumnos que han iniciado el curso y el número de inscripciones.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Porcentaje del índice de finalización</p></td>
   <td>
    <p>Relación entre el número total de usuarios que han completado el curso y el número total de usuarios que lo han iniciado.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Comentarios del alumno</p></td>
   <td>
    <p>Promedio de todas las respuestas a los comentarios de L1 recibidas en una escala del 1 al 10, redondeado al entero más próximo.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Comentarios del responsable</p></td>
   <td>
    <p>Promedio de todas las respuestas a los comentarios de L3 recibidas en una escala del 1 al 5, redondeado al entero más próximo.<br></p></td>
  </tr>
 </tbody>
</table>

El informe de formación tiene dos columnas adicionales:

1. Valoración media basada en estrellas de un curso.
1. Número de alumnos que han calificado el curso.
1. Ruta incrustada
1. ID de ruta incrustada
1. ID de curso incrustado

>[!NOTE]
>
>El índice de inicio y de finalización, y los comentarios del alumno y del responsable no se ven afectados por los filtros aplicados. Los filtros solo afectan a la inscripción, las vistas y las finalizaciones.

>[!NOTE]
>
>En ambos informes (Contenido de formación y Actividad de usuario), puede configurar un máximo de 10 grupos de usuarios. Pueden transcurrir hasta 24 horas hasta que se complete el procesamiento y se faciliten los filtros recién configurados.

## Tableros de resumen del aprendizaje {#dashboards}

### Generar informes de panel

>[!INFO]
>
>En esta formación, aprenderá a generar informes de paneles a partir de la base de datos.<br><br>[![botón](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R3B5NPDN&amp;mv=display&amp;mv2=display#/course/8318854)</br></br>


Si no puede iniciar el entrenamiento, escriba a <almacademy@adobe.com>.

Ver un informe resumido de todas las actividades de aprendizaje en la plataforma. En esta página, puede ver la siguiente información de resumen para el equipo y los perfiles externos del usuario raíz seleccionado. El rango de tiempo también se puede seleccionar:

* Resumen de aprendizaje en forma de inscripciones, vistas y finalizaciones
* Aptitudes principales
* Resumen de cumplimiento

![](assets/summary-charts.png)
*Gráficos de resumen*

Si hay administradores internos de nivel raíz, se mostrarán uno tras otro.

Todos los perfiles externos aparecerán después de los perfiles internos (usuarios internos de nivel raíz).

Si un perfil externo tiene un responsable, la jerarquía del responsable se mostrará en la **[!UICONTROL lista desplegable Mostrar datos para]** . El usuario aparecerá en la jerarquía del responsable en toda la página de detalles (Resumen de aprendizaje, cumplimiento y estado de aptitud)

De lo contrario, todos los detalles de los usuarios individuales se mostrarán en la lista.

Para ver detalles más detallados de las inscripciones de varios equipos internos, haga clic en **[!UICONTROL Detalles]** del resumen de aprendizaje.

![](assets/learning-sunnarydetails.png)
*Detalles del resumen de aprendizaje*

Al hacer clic en cualquier inscripción, puede ver los alumnos de cada responsable y la inscripción a qué objetos de aprendizaje. También puede ver los detalles de progreso y finalización de cada alumno.

![](assets/learners-for-a-manager.png)
*Alumnos asignados a un responsable*

Haga clic en cualquier equipo y exporte la informe como un archivo csv. Un administrador puede exportar el informe para cualquier grupo de usuarios o usuario individual seleccionando el grupo de usuarios o un usuario individual y, a continuación, exportar los detalles de la **[!UICONTROL lista desplegable Acción]** .

Además, puede ver una vista de gráfico de barras de las habilidades que están en curso y se han conseguido. Puede añadir o quitar las aptitudes que desee incluir en el gráfico.

![](assets/skill-status-stackedbarchart.png)
*Gráfico de barras apiladas de estado de aptitudes*

### Tablero de cumplimiento

**Adobe Learning Manager** ofrece un tablero de cumplimiento a todos los administradores y gerentes. Los administradores pueden crear un tablero de cumplimiento y compartirlo con los gerentes. Los responsables podrán ver el nuevo panel compartido en su aplicación y podrán realizar fácilmente un seguimiento del cumplimiento por parte de los miembros de su equipo para una formación concreta. El tablero Cumplimiento permite a los administradores clasificar los cursos de cumplimiento personalizados en categorías específicas (por ejemplo, Ventas, Marketing y Asuntos legales). Las categorías de cumplimiento personalizadas se utilizan mediante etiquetas de **[!UICONTROL catálogo.]**

![](assets/compliance-dashboard-admin.png)

_Tablero de cumplimiento: vista de administrador_

Los administradores también pueden comprobar el estado de cumplimiento del equipo de cada responsable seleccionando **[!UICONTROL Ir al tablero de cumplimiento]**. Los administradores pueden compartir un conjunto de cursos de formación con los responsables individualmente o con un grupo. Esto ayuda a los gerentes a rastrear fácilmente el cumplimiento de sus compañeros de equipo para la capacitación especificada.

#### Flujo de trabajo de administración

##### Crear etiquetas de cumplimiento personalizadas

Una etiqueta de cumplimiento es un tipo de etiqueta de catálogo que clasifica cursos, rutas de aprendizaje o certificaciones como un tipo de cumplimiento.
Para crear una etiqueta de cumplimiento personalizada, siga estos pasos:

1. En la aplicación Administrador, vaya a **[!UICONTROL Configuración]** > **[!UICONTROL General]**.
1. Seleccione **[!UICONTROL la opción Tipo de cumplimiento]** personalizado para habilitar la etiqueta de cumplimiento personalizado.


   ![](assets/custom-compliance.png)
   _Habilitar cumplimiento personalizado_

   >[!NOTE]
   >
   >Esta nueva etiqueta de catálogo se ha introducido para categorizar los cursos, las rutas de aprendizaje y las certificaciones como un tipo de cumplimiento. Para habilitar la **[!UICONTROL opción de tipo]** Cumplimiento personalizado, primero debe habilitar la opción Mostrar etiqueta ]**de**[!UICONTROL  catálogo en la misma página.

1. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Etiqueta]** de catálogo y seleccione el tipo ]**de**[!UICONTROL  cumplimiento.
1. Escriba los valores (p. ej., Legal, Ventas) en el cuadro de **[!UICONTROL texto Valor]** y seleccione **[!UICONTROL Añadir valor]**.

   ![](assets/custom-compliance-values.png)
   _Adición de valores para el cumplimiento personalizado_

1. Seleccione **[!UICONTROL Guardar]**.

>[!NOTE]
>
>El autor debe agregar estas etiquetas de cumplimiento al crear o editar los cursos en su aplicación. Consulte Añadir [etiquetas de cumplimiento a un curso, una ruta de aprendizaje o una certificación](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification).

##### Crear y compartir un tablero de cumplimiento

Para crear y compartir un tablero de cumplimiento, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** > **[!UICONTROL Resumen]** de aprendizaje.
1. En la **[!UICONTROL sección Tablero]** de cumplimiento, seleccione **[!UICONTROL Compartido con responsables]**.
1. Seleccione **[!UICONTROL el panel]** Compartir y seleccione las etiquetas creadas en el **[!UICONTROL menú desplegable Cumplimiento]** personalizado.


   ![](assets/compliance-type.png)
   _Seleccione el tipo de cumplimiento_

1. Escriba y seleccione el nombre del responsable en el **[!UICONTROL cuadro de texto Compartir con]** .
1. Seleccione Compartir **** para enviar el tablero al administrador seleccionado.

>[!NOTE]
>
>Al compartir el nuevo tablero, se sobrescribirá el tablero existente en la aplicación del administrador seleccionado. Los responsables podrán ver el nuevo tablero compartido por los administradores.

<!--In the final visualization, you can check the compliance status of learners, and take appropriate action.

Also, an Admin can view individual training data in the **[!UICONTROL Compliance Dashboard]**.

For instance, the Administrator has identified three trainings to track compliance. Learning Manager provides the compliance snapshot for all three trainings at once.

Now an Admin can click on any training and quickly view the compliance for the selected training.

![](assets/compliance-dashboard.png)
*View Compliance dashboard*

You can also see the compliance status for each internal team.

Click the link **[!UICONTROL Compliance Status Details]** on the bottom of the visualization. 

You can see that, for a team, the number of learners in the team are violating or honoring the learning compliance.

![](assets/compliance-statusofateam.png)
*Compliance status of a team*

### Share training with managers

Learning Manager offers compliance dashboard to all Administrators and Managers. Managers find it very useful to track compliance of their team members for a particular training. At the same time, Administrators would like all Managers to add compliance trainings to their dashboard and track it. 

In Learning Manager, the **[!UICONTROL Share with Managers]** workflow allows Administrators to share training with Managers, so that they can get added to a manager's Compliance Dashboard. Thus, Managers do not need to take any action and can start tracking compliance immediately. 

An Administrator can share a set of training courses with managers individually or with a group. This sharing can help a manager easily track the compliance of his/her team for the specified training.

The Administrator can "push" a default list of compliance training to be viewed in the manager's compliance dashboard.

### Share training

1. In **[!UICONTROL Reports]** > **[!UICONTROL Learning Summary]**, scroll down, and click the tab **[!UICONTROL Share with Managers]**. 

   ![](assets/share-with-managers.png)
   *Share training with managers*

1. To add training or multiple training, click **[!UICONTROL Share more]**.   

1. In the **[!UICONTROL Share with Managers]** dialog, choose the training(s) and the manager(s).

   ![](assets/select-training.png)
   *Select training to share with managers*

1. Click **[!UICONTROL Share]**.

The training is now shared with the specified manager.

### View training

In the list of shared training, click **[!UICONTROL View]**. You can view the training that is assigned to a manager or some managers.

### Withdraw training

1. To withdraw training from a manager, click **[!UICONTROL Withdraw]**.  

1. Click **[!UICONTROL Proceed]**. This withdraws previously shared training from the Manager's compliance dashboard.-->

## Informes personalizados

Los administradores pueden generar informes específicos utilizando la plantilla personalizada disponible en la **[!UICONTROL sección Informes]** .

### Informes de muestra {#samplereports}

La ficha **[!UICONTROL Informes de muestra]** presenta algunos informes indicativos que se basan en puntos de datos de muestra. Explore estos informes para tener una idea de los distintos tipos de informes repletos de funciones que puede generar con los datos de su cuenta.

### Informes de tableros {#dashboardreports}

Un tablero es una colección de informes. Los informes pueden agruparse en un tablero según su elección. Haga clic en la ficha de este tablero para ver todos los tableros creados por usted. En la **[!UICONTROL lista desplegable Ver tablero]** , puede seleccionar el tablero predeterminado o cualquiera de los tableros creados por usted.

### Informes de Excel {#excelreports}

La ficha **[!UICONTROL Informes de Excel]** permite exportar informes con formato de archivo XLS.

A continuación, se muestran los tipos de informes disponibles para la descarga.

* Informes del curso
* Transcripciones de alumnos
* Informe de anuncios
* Informe de ayudas de trabajo
* Registro de auditoría de contenido
* Registro de auditoría de usuarios
* Informe de inicio de sesión o de acceso
* Transcripciones de interacciones
* Registro de auditoría de interacción

### Transcripciones de alumnos {#learnertranscripts}

Las transcripciones de alumnos en informes de Excel muestran las columnas Créditos necesarios y Créditos obtenidos en números decimales.

### Informes del curso {#coursereports}

Como administrador, puede descargar informes de cursos. Siga estos pasos:

1. Abra **[!UICONTROL informes]** > **[!UICONTROL informes]** personalizados > **[!UICONTROL informes]** de Excel > **[!UICONTROL informes de curso.]**
1. Se muestra el cuadro de diálogo **[!UICONTROL Informe del curso]**. Seleccione el curso, cuyo informe quiere obtener y haga clic en **[!UICONTROL Mostrar]**.

   ![](assets/course-reports.png)
   *Informes del curso*

1. Se le redirige a la página del curso. Puede exportar la puntuación de prueba por usuario y por pregunta en función de cada inscripción eligiendo el tipo de inscripción correspondiente.
1. Seleccione **[!UICONTROL Exportar puntuación de prueba]** para exportar el informe. Aparece el cuadro de diálogo **[!UICONTROL Generando solicitud de informe]**. Haga clic en **[!UICONTROL OK]** para confirmar.

   ![](assets/generating-reportrequest.png)
   *Generando solicitud de informe*

   >[!NOTE]
   >
   >El informe de puntuaciones de pruebas exportado contendrá datos de puntuación de cualquier intento si el módulo tiene activada la opción Varios intentos.

### Transcripciones de alumnos {#LearnerTranscripts-1}

Adobe Learning Manager permite a los administradores de una empresa generar transcripciones asociadas a los alumnos. El informe de transcripciones de alumnos muestra lo siguiente:

1. Transcripciones de alumnos: Tablero de actividades de aprendizaje
1. Aptitud: Tablero de aptitudes
1. Tablero de cumplimiento

Las transcripciones de alumnos en informes de Excel muestran las columnas Créditos necesarios y Créditos obtenidos en números decimales.

Para obtener información sobre cómo generar informes de Transcripciones de alumnos y más información, consulte [Transcripciones](learner-transcripts.md) de alumnos.

### Informes de anuncios {#announcementsreports}

Como administrador, puede generar un informe de todos los anuncios que envíe. El informe contiene datos relativos a los aspectos siguientes:

* Tipo de anuncio
* Nombre del anuncio
* Fecha del anuncio
* Estado del anuncio
* Nombre del alumno

Para descargar un informe, siga cualquiera de estos pasos:

1. Abra **[!UICONTROL informes]** > **[!UICONTROL informes]** personalizados > **[!UICONTROL informes de Excel]** > **[!UICONTROL el informe]** de anuncios. Se abre el cuadro de diálogo **[!UICONTROL Generando solicitud de informe]**. Haga clic en Aceptar.
1. [!UICONTROL **Anuncios**] > [!UICONTROL **acciones**] > [!UICONTROL **informe**] de exportación.

   ![](assets/announcements.png)
   *Informe de anuncios*

1. Puede extraer un informe de un anuncio específico haciendo clic en **[!UICONTROL Exportar informe]** debajo del icono de configuración.

   ![](assets/announcements-specific-report.png)
   *Informe de anuncios específicos*

### Informe de ayudas de trabajo {#jobaidsreport}

Las ayudas de trabajo consisten en contenido de formación al que puede tener acceso un alumno sin inscribirse en ningún objeto de aprendizaje concreto como un curso o un programa de aprendizaje. Los administradores puedan extraer y descargar el informe de ayudas de trabajo.

El informe extraído incluye información sobre lo siguiente:

* Nombre
* Tipo de ayuda de trabajo
* Estado de la ayuda de trabajo (publicado o retirado)
* Fecha de inscripción
* Fecha de finalización
* Fecha de descarga
* Nombre del alumno
* Nombre del responsable
* Autor

Para descargar un informe, realice una de las siguientes acciones:

* Abra informes > informes personalizados > informes ]**de Excel >**[!UICONTROL  informes ]**de ayudas de**[!UICONTROL  trabajo.]********[!UICONTROL  Aparece el cuadro de diálogo **[!UICONTROL Generando solicitud de informe]**. Haga clic en **[!UICONTROL Aceptar]**.
* Abrir **[!UICONTROL ayuda]** de trabajo >]****[!UICONTROL  acciones > **[!UICONTROL informe]** de exportación.

![](assets/job-aids.png)
*Informe de ayudas de trabajo*

* También puede extraer un informe de una ayuda de trabajo específica haciendo clic en **[!UICONTROL Exportar informe]** debajo del icono de configuración.

![](assets/job-aid-specific-download.png)
*Informe de una ayuda de trabajo concreta*

### Informe de ayudas de trabajo

Después de seleccionar **[!UICONTROL Informe]** de ayudas de trabajo en la lista, verá dos opciones:

![Informe](assets/job-aids-new.png)
*de ayudas de trabajo Descargar informe de inscripción de usuarios de ayudas de trabajo*

**Todas las ayudas** de trabajo: si el número de ayudas de trabajo de la cuenta es inferior a 10 millones, el informe generado contendrá información de inscripción de todas las ayudas de trabajo. Esta será la selección predeterminada. Si el número de filas supera los 10 millones, se mostrará un error y deberá seleccionar manualmente las ayudas de trabajo necesarias.

**Ayudas de trabajo seleccionadas**: si selecciona esta opción, puede introducir las ayudas de trabajo para las que desea generar el informe. Puede seleccionar un máximo de 10 ayudas de trabajo. Adobe Learning Manager comprueba si el número de ayudas de trabajo supera los 10 millones.

![Informe de ayudas de trabajo Inscripción](assets/job-aids-2-new.png)
*Seleccione una ayuda de trabajo*

**Informe de ayudas de trabajo**

Si selecciona esta opción, se descargarán los detalles de todas las ayudas de trabajo presentes en el sistema, junto con sus metadatos y formación.

El informe descargado consta de los siguientes campos:

* Nombre de ayuda de trabajo
* Idioma(s)
* ID
* Tipo
* Duración (minutos)
* Estado
* Fecha de publicación (zona horaria UTC)
* Creado por nombre
* Creado por correo electrónico
* Creado por ID exclusivo de usuario
* Catálogo(s)
* Ruta(s) de aprendizaje
* Curso(s)
* Etiqueta(s)
* Aptitud(es)

**Informe de inscripción de usuarios de ayudas de trabajo**

El informe de inscripción contiene detalles sobre la inscripción de usuarios y otra información.

El informe descargado consta de los siguientes campos:

* Nombre de ayuda de trabajo
* Tipo
* Estado
* Fecha de inscripción (zona horaria UTC)
* Fecha de finalización (zona horaria UTC)
* Fecha de descarga (zona horaria UTC)
* Nombre del alumno
* Correo electrónico
* ID exclusivo de usuario
* Nombre del responsable
* Correo electrónico del responsable
* ID exclusivo de usuario responsable
* Asignado por nombre
* Asignado por correo electrónico
* Asignado por ID exclusivo de usuario
* Creado por nombre
* Creado por correo electrónico
* Creado por ID exclusivo de usuario
* Código de trabajo
* Nuevo campo
* Perfil

### Informes de registro de auditoría de contenido {#contentaudittrailreports}

Utilice el generador del **[!UICONTROL informe de registro de auditoría]** de contenido para generar un informe sobre todos los cambios y modificaciones habidos en un curso durante su duración en el sistema. El informe generado muestra la información siguiente recopilada:

* ID de objeto
* Nombre del objeto
* Tipo de objeto
* Tipo de modificación
* Descripción
* ID de objeto de referencia
* Nombre de objeto de referencia
* Modificado por nombre de usuario
* Modificado por UUID de usuario
* Fecha de modificación (zona horaria UTC)

En la columna Tipo de **modificación** , obtendrá los siguientes detalles:

| Tipo de modificación | Descripción |
| --- | --- |
| Crear | Curso creado |
| Añadir certificación | Certificación añadida al catálogo |
| Eliminación de certificaciones | Certificación eliminada del catálogo |
| Adición de contenido | Contenido añadido al módulo |
| Añadir curso | Curso añadido a la ruta de aprendizaje |
| Eliminación de curso | Curso eliminado del programa de formación |
| Adición de etiqueta personalizada | Etiqueta personalizada añadida al catálogo |
| Eliminación de etiquetas personalizadas | Etiqueta personalizada eliminada del catálogo |
| Eliminar | Catálogo eliminado |
| Adición de ayuda de trabajo | Ayuda de trabajo añadida al catálogo |
| Eliminación de ayuda de trabajo | Ayuda de trabajo eliminada del catálogo |
| Añadir ruta de aprendizaje | Ruta de aprendizaje añadida al catálogo |
| Eliminar ruta de aprendizaje | Ruta de aprendizaje eliminada del catálogo |
| Adición de contenido del módulo | Módulo añadido al curso (sección Contenido) |
| Eliminación de contenido del módulo | Módulo eliminado del curso (sección Contenido) |
| Publicado | Curso o ruta de aprendizaje publicado y añadido al catálogo predeterminado |
| Republicado | Curso republicado |
| Adición de recursos | Recurso añadido al curso |
| Eliminación de recursos | Recurso eliminado del curso |
| Retirado | Curso retirado |
| Añadir catálogo compartido | Catálogo compartido con el catálogo |
| Eliminar catálogos compartidos | Uso compartido de catálogos eliminado del catálogo |
| Actualización del catálogo compartido | Estado de uso compartido del catálogo: activo |
| Actualización | Actualización del curso o programa de aprendizaje |
| Añadir grupo de usuarios | Grupo de usuarios añadido al catálogo |
| Quitar grupo de usuarios | Grupo de usuarios eliminado del catálogo |

La información relativa a metadatos no se recopila en el informe generado.

Para generar un informe de registro de auditoría de un curso, siga estos pasos.

1. Seleccione Informe **** > informes ]**de**[!UICONTROL  Excel > **[!UICONTROL Registro de auditoría del]** curso. Aparece el cuadro de diálogo **[!UICONTROL Registro de auditoría de contenido]**.

   ![](assets/course-audit-trial.png)
   *Registro de auditoría de curso*

1. Seleccione el curso, el programa de aprendizaje y la certificación de los que desea descargar el informe. Si no se especifica, de manera predeterminada se descargan todos los informes.
1. Seleccione un intervalo de fechas para el informe y haga clic en **[!UICONTROL Generar]**.
1. El informe se genera y se le notifica que el informe de auditoría de contenido está listo. Puede descargar el informe.

### Informes de registro de auditoría de usuarios {#useraudittrailreports}

El registro de auditoría de usuarios captura el ciclo de vida de usuarios, grupos de usuarios y perfiles de registro automático. Se captura la adición y eliminación de usuarios, y los cambios del responsable. Se registra la creación y eliminación de perfiles de registro automático. El registro automático también se puede pausar y reanudar.

Durante el registro automático puede añadir, habilitar, deshabilitar, pausar o reanudar en perfiles externos. También se capturan las cargas de CSV.

1. Seleccione  **[!UICONTROL Informe > Informe de Excel > Registro de auditoría]** de usuarios. Aparecerá el cuadro de diálogo Registro de auditoría de usuarios.
1. Se muestra el cuadro de diálogo Registro de auditoría de usuarios. Seleccione el intervalo de fechas en el menú emergente. Puede elegir entre generar el informe de la última semana, el último mes o seleccionar una fecha personalizada.

   ![](assets/user-audit-trail.png)
   *Registro de auditoría de usuarios*

1. Haga clic en **[!UICONTROL Generar]** para generar el informe.

Hay dos filtros en el cuadro de diálogo **[!UICONTROL Informe de seguimiento de auditoría de usuarios]**.

**Filtro Frecuencia por fecha:** elija el intervalo de fechas para el que desea generar el informe. Hay tres opciones:

* Última semana
* Último mes
* Fecha personalizada

Seleccionar filtro de alumnos: busca un usuario o un grupo de usuarios.

El informe exportado contendrá datos de los usuarios que cumplan los dos criterios de búsqueda especificados.

![](assets/user-audit-trail.png)
*Registro de auditoría de usuarios*

>[!NOTE]
>
>Cuando se asigna o se elimina una aptitud, se puede realizar un seguimiento de la aptitud en el Informe de auditoría de usuarios, tanto si se asigna como si se elimina.

### Informe de configuración de extensiones

Este informe proporciona información sobre los detalles de configuración de todas las extensiones nativas añadidas, incluido su estado de activación. Aprenda a descargar el informe de extensión, consulte [Descargar informe](native-extensibility.md#download-extension-report) de extensión.

### Informe de actividad de xAPI

Este informe proporciona datos de todas las declaraciones de xAPI registradas y generadas durante los módulos de actividad de xAPI.

Para descargar este informe, siga estos pasos:

1. Seleccione  **[!UICONTROL Informe > informe de Excel > Informe]** de actividad de xAPI. Aparece el cuadro de diálogo Informe de actividad de xAPI.
1. Seleccione el intervalo de fechas en el menú emergente. Puede elegir entre generar el informe de la última semana, el último mes o seleccionar una fecha personalizada.
1. Seleccione los alumnos y la actividad en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]** para generar el informe.

### Informes de interacciones {#gamification}

Los administradores pueden descargar la transcripción de interacción en formato .csv. Puede descargar el informe para usuarios individuales o para grupos de usuarios. En el informe se obtienen el nombre de usuario, el correo electrónico del usuario, el UUID del usuario, los puntos totales obtenidos por el usuario, el desglose de los puntos obtenidos, el nombre de los grupos en los que el usuario interacciona, el nombre del responsable y los valores de los campos activos. Los administradores pueden usar este informe para evaluar y comprender las clasificaciones de usuarios en el nivel de la empresa o para un grupo específico.

1. Seleccione Informe > informe de Excel > Informe de interacción.

   ![](assets/gamification.png)
   *Informe de interacciones*

1. Aparece el cuadro de diálogo Transcripciones de interacciones. Seleccione alumnos usando su nombre, perfil, grupos de usuarios, ID de correo electrónico o UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Cuadro de diálogo Transcripciones de interacciones*

1. Haga clic en  **[!UICONTROL Generar]** para generar el informe.

   Después de generar el informe de un alumno, debe poder exportar la información actual y de nivel logrado para todos los usuarios (internos, externos o eliminados) de la cuenta. También puede consultar las fechas de los niveles alcanzados por un alumno:

   * Fecha de obtención de Bronce
   * Fecha de obtención de Plata
   * Fecha de obtención de Oro
   * Fecha de obtención de Platino

   Estas columnas contienen las fechas en que se alcanzó el nivel por primera vez. La columna **[!UICONTROL Nivel]** actual muestra el nivel actual del alumno.

   Cuando el administrador restablece la interacción, todos los puntos del alumno se restablecen en consecuencia.

### Informe de registro de auditoría de interacciones {#gamification-audit-trail}

Este informe contiene el historial y los motivos de los puntos de interacción de los alumnos ganados por cada regla.

### Descargar el informe

1. Seleccione la URL del seguimiento de auditoría de interacciones.
1. En la ventana emergente Registro de auditoría **de** interacciones, seleccione el intervalo de fechas.
1. Seleccione **Generar**.

El informe se descarga en forma de archivo CSV. El archivo contiene las siguientes columnas:

* Nombre
* Correo electrónico/ UUID,
* Estado
* Acción
* Puntos
* Puntos de saldo
* Regla/Tarea
* Subtarea Regla/Tarea,
* Detalles de la regla/tarea
* Tipo
* Nombre
* Nombre de instanciaFecha alcanzada (zona horaria UTC)
* Hora de inicio de la regla/tarea
* Tiempo de fin de regla/tarea

### Informe de inscripción y baja {#enrollmentandunenrollmentreport}

Los administradores y los responsables pueden extraer un informe de los alumnos que se han inscrito y se han dado de baja. Como administrador, puede ver a cualquier alumno, administrador o responsable que se ha inscrito o dado de baja de una instancia de curso, programa de aprendizaje o certificación, y exportar el informe. Ahora bien, como responsable, solo puede obtener un informe de los miembros de su equipo. Como responsable, no puede ver a los alumnos eliminados ni su propio nombre en la aplicación del responsable como alumno inscrito o que se ha dado de baja.

Para descargar un informe, siga estos pasos: Abra el curso, programa **[!UICONTROL de aprendizaje o certificación]** > **[!UICONTROL informe]** Alumnos ]**>**[!UICONTROL  Acción ]**>**[!UICONTROL  exportación.

![](assets/unenrollment.png)
*Informe de darse de baja*

### Informe de comentarios {#feedback-report}

Como administrador, ahora puede obtener comentarios del alumno (L1) y del responsable (L3) en relación con los cursos de formación seleccionados durante un periodo especificado.

Puede exportar los datos desde la interfaz de usuario o a través del conector de PowerBI para un análisis más detallado.

Los informes de comentarios de L1 y L3 ofrecen la opción de descargar un informe de comentarios consolidado para las respuestas de L1 y L3 para formaciones seleccionadas para un **intervalo de un año** o para un máximo de 10 formaciones seleccionadas para cualquier intervalo de fechas.

Inicie sesión como administrador, haga clic **[!UICONTROL en Informes]** > **[!UICONTROL Informes]** personalizados y, en la lista de informes, haga clic **[!UICONTROL en Informe de comentarios]**.

![](assets/download-feedbackreport.png)
*Descargar informe de comentarios*

Al hacer clic en descargar después de seleccionar los filtros, recibirá una notificación para descargar el informe en formato CSV.

El informe descargado contendrá detalles como el nombre y el tipo de formación, el nombre de la instancia, el nombre y el correo electrónico del alumno, el tipo de comentarios: L1 o L3, las fechas de los comentarios enviados para los datos nuevos.

Para los datos existentes antes de la implementación de esta función, se mostrará la fecha de finalización de objetos de aprendizaje, la fecha de finalización de objetos de aprendizaje, la pregunta de comentarios de L1 Texto real con ritmo personalizado y el texto de clase en columnas diferentes, las respuestas respectivas de comentarios de L1, el nombre y el correo electrónico del responsable, el valor de comentarios de L3 y la fecha de envío, Campos activos.

También puede exportar los datos desde la interfaz de usuario o Power BI, que admite todos los entrenamientos para cualquier intervalo de fechas para un análisis más detallado

### Informe de cursos de formación {#training-report}

El responsable de aprendizaje admite el informe de formación, que permite a los administradores descargar detalles de formación y los metadatos asociados, como el autor, la fecha de publicación, las aptitudes, las etiquetas del catálogo, etc.

En la aplicación Administrador, haga clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informe de Excel]** > **[!UICONTROL Formación]**.

Puede descargar informes para lo siguiente:

* Cursos de formación seleccionados (límite de 10): permite elegir uno o varios cursos de formación (hasta 10) de cualquier catálogo
* Cursos de formación de los catálogos seleccionados (límite de 5): se pueden seleccionar hasta cinco catálogos.
* Todos los cursos de formación: todos los cursos de formación de la cuenta.

![](assets/download-trainingreport.png)
*Descargar informe de formación*

En la sección Opciones avanzadas, están disponibles las siguientes opciones:

* Incluir asignaciones de cursos con programa de aprendizaje/certificación
* Incluir información en el nivel de módulo

Después de seleccionar los filtros y hacer clic en Descargar, recibirá una notificación para que descargue el informe en formato CSV.

El informe tendrá los siguientes campos:

*Nombre del catálogo, Tipo de formación, ID de formación, ID exclusivo de la formación, Nombre de la formación, Subformación, Módulos, Duración de la formación o del módulo, Formato, Estado de la formación, Aptitudes, Autor, Fecha de última publicación, Fecha de finalización última, Recuento de inscripciones de instructores, Recuento iniciado, Recuento de finalización, Puntuación media de L1, Puntuación media de L2, Puntuación media de L3, Respuestas de L1 recibidas, Respuestas de L2 recibidas, Respuestas de L3 recibidas, Etiquetas de catálogo y etiquetas.*

![](assets/more-options.png)
*Opciones adicionales*

### Informe de resumen de sesión {#session-summary-report}

El informe de resumen de la sesión contiene todas las sesiones planificadas para un alumno en una fecha especificada.

Esto permite al administrador exportar todos los detalles de la sesión virtual y de clase dentro del intervalo de fechas especificado. El administrador también puede exportar el informe de la sesión con respecto a determinados cursos de formación o instructores.

Esto también ayudará al administrador a comprender las sesiones planificadas mensualmente e identificar el horario de los instructores y las sesiones ya realizadas.

Como administrador, haga clic en **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informe]** de resumen de sesión.

En el cuadro de diálogo que aparece a continuación, elija el intervalo de fechas y el instructor o la formación para un resumen.

![](assets/session-summary-report.png)
*Informe resumido de la sesión*

El informe csv contiene los siguientes campos:

* Fecha y hora de inicio
* Fecha y hora de finalización

* Nombre de módulo
* Duración de la sesión (en minutos)
* Recuento de puestos
* Ubicación
* Nombre de la instancia
* Nombre del curso
* Id. del curso
* Nombre del instructor
* Correo electrónico del instructor
* Recuento de inscripciones
* Tipo de sesión
* Límite de lista de espera
* N.º en lista de espera
* Mensajes de correo electrónico de usuario de la lista de espera
* Información de ubicación
* Región de la ubicación

### Informe de utilización del instructor

Este informe captura el tiempo (en minutos) que un instructor dedica diariamente a impartir las sesiones asignadas. El informe se puede descargar durante un período de tres meses a partir de la fecha de inicio seleccionada.

Para descargar el informe, haga clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informe]** de utilización del instructor.

Seleccione uno o varios instructores y el intervalo de fechas.

![Descargar informe](assets/utilization-report.png)
*de utilización de instructores Descargar informe de utilización de instructores*

El informe descargado contiene los siguientes campos:

* Nombre del instructor
* ID del instructor
* Nivel de competencia
* Fechas como columnas. Si el instructor se utiliza en una fecha, se muestra el número de sesiones. Si no se utiliza el instructor en un día, el valor muestra cero.

El informe contiene registros de tres meses a partir del mes seleccionado.

Para recuperar los registros de todos los instructores, deje el campo Instructor en blanco.

Además, un administrador personalizado con permiso para generar informes puede recuperar este informe.

### Informe de registro de auditoría de usuarios

Este informe recopila información sobre los alumnos que cambiaron de instancia, &quot;de instancia&quot; a &quot;a instancia&quot;, cambiados por hora, fecha, etc.

Seleccione los alumnos o un grupo de usuarios.

Para descargar el informe, haga clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informe]** de registro de auditoría de usuarios.

![Descargar informe de registro de auditoría de usuarios](assets/user-audit-report.png)

*Descargar informe de registro de auditoría de usuarios*

### Informe de plan de aprendizaje

Este informe contiene información detallada sobre todos los planes de aprendizaje de una cuenta, por ejemplo, los grupos de usuarios relacionados, el estado y la información sobre activadores.

El informe contiene los siguientes campos:

* Nombre del plan de aprendizaje
* Tipo (se produce cuando)
* Formación (finalizada)
* Aptitud (conseguida)
* Fecha (en fecha)
* Acción
* Estado, creado por
* Fecha de creación
* Fecha de la última modificación
* Grupo de usuarios (se aplica a)
* Grupo de usuarios (añadir a)
* Inscribirse después de
* Tipos de elemento de aprendizaje
* Elementos de aprendizaje
* Instancias de elemento de aprendizaje
* Elemento de aprendizaje
* Fecha de finalización
* Recordatorio de elemento de aprendizaje
* Ámbito: catálogo
* Ámbito: grupo de usuarios

## Suscripciones de correo electrónico {#emailsubscriptions}

Puede recibir sus informes favoritos por correo electrónico mediante una suscripción.

### Configurar suscripciones de correo electrónico

>[!INFO]
>
>En esta formación, aprenderá a configurar suscripciones por correo electrónico para informes de paneles.<br><br>[![botón](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PLHRQ62N&amp;mv=display&amp;mv2=display#/course/8318927)</br></br>


Si no puede iniciar el entrenamiento, escriba a <almacademy@adobe.com>.

En **[!UICONTROL la página Informes]** , haga clic en la  **[!UICONTROL ficha Suscripción]** . Aparece la página de suscripción a informes.

Comience a escribir el nombre del informe en el campo Informes para seleccionar el nombre del informe de la lista desplegable. Seleccione la frecuencia del correo electrónico en la lista desplegable. Puede añadir el asunto del correo electrónico y proporcionar un ID de correo electrónico alternativo.

Puede editar y eliminar las suscripciones.

## Informes históricos

Los informes históricos en Adobe Learning Manager (ALM) hacen referencia a los informes que capturan los datos históricos y las actividades dentro de la plataforma de aprendizaje. Estos informes proporcionan información sobre las actividades pasadas de los alumnos, el contenido de la formación, el rendimiento de los grupos de usuarios y otros datos relevantes. Los informes históricos permiten a los administradores realizar un seguimiento, supervisar y analizar el progreso y la eficacia de las iniciativas de aprendizaje a lo largo del tiempo.

### Informes de acceso al curso

Los informes de acceso al curso proporcionan información sobre la repetición de cada curso.

Para descargar este informe, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** > **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informes]** históricos.
1. Seleccione **[!UICONTROL Informe]** de acceso al curso. Se abre el cuadro de diálogo Generando solicitud de informe.
1. Seleccione el año y el trimestre en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]**.

### Informes de inicio de sesión o de acceso

Los informes de inicio de sesión y de acceso proporcionan información sobre los inicios de sesión y el acceso de los usuarios. Puede generar informes con datos de tres meses a la vez.

Para descargar este informe, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** > **[!UICONTROL Informes]** personalizados > **[!UICONTROL Informes]** históricos.
1. Seleccione **[!UICONTROL Informe de inicio de sesión o de acceso]**. Se abre el cuadro de diálogo Generando solicitud de informe.
1. Seleccione el año y el trimestre en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]**.

## Crear un tablero {#createadashboard}

1. Haga clic en Añadir tablero en la parte derecha de la página para comenzar a crear sus propios tableros.

   ![](assets/add-dashboards.png)
   *Añadir tableros*

1. Proporcione un nombre y una descripción para el tablero.
1. Si desea compartir el tablero con cualquier responsable, elíjalo en **[!UICONTROL el campo Compartir con]** . Puede usar cualquier criterio de selección normal para esta operación.
1. Haga clic en **[!UICONTROL Guardar].**

Puede ver el tablero creado recientemente en la ficha **[!UICONTROL Informes de tableros]**.

Para añadir informes a su tablero, haga clic en la lista desplegable en la esquina superior derecha de la ventana de su tablero y luego haga clic en **[!UICONTROL Añadir informe]**. El informe que crea de este modo se asocia con su tablero.

>[!NOTE]
>
>Los informes que crea haciendo clic en Añadir en la esquina superior derecha de la página Informes se añaden a su tablero predeterminado.

## Tableros compartidos {#shareddashboards}

Los tableros compartidos son una colección de informes que otros usuarios de la empresa han compartido con usted. Cualquier informe que añada a un tablero compartido se comparte automáticamente con otros usuarios que tengan acceso a dicho tablero.

El tablero se puede compartir de dos formas:

* Especificando los usuarios en el **[!UICONTROL campo Compartir con]** con con los que se debe compartir el tablero.
* Elija Editar tablero en la lista desplegable e indique los detalles del usuario para compartir el tablero.

>[!NOTE]
>
>Un responsable solo puede ver los informes de los miembros de su equipo desde un tablero compartido.

## Descargas {#downloads}

La hoja exportada de informes del tablero proporciona información detallada en lugar del resumen de informes. El informe descargado tiene el formato de una transcripción de alumno.

## Crear informes {#report}

1. Haga clic en Informes en el panel de la izquierda. Aparece la página Resumen de informes.

   >[!NOTE]
   >
   >De manera predeterminada, aparecen al menos tres informes de muestra en la ficha del tablero de ejemplo. Solo puede ver estos informes de muestra para hacerse una idea de cómo los crearía y los personalizaría.

1. En la esquina superior derecha de la página, haga clic en **[!UICONTROL Agregar]**.
1. En el cuadro de diálogo **[!UICONTROL Añadir informe]**, en la lista desplegable Tipo, puede seleccionar uno de los informes predefinidos o bien **[!UICONTROL Personalizado]**. Si selecciona un informe predefinido, verá que el formulario ya está rellenado. Puede efectuar cambios en algunos campos y hacer clic en **[!UICONTROL Guardar]**. Esta acción incorpora el informe a su tablero predeterminado.

   ![](assets/create-report.png)
   *Crear informe*

   En **[!UICONTROL Tipo de informe]**, puede seleccionar un conjunto de informes predefinidos o valores personalizados. Puede ver los siguientes informes como parte del conjunto de informes predefinidos:

   * Aptitudes asignadas y obtenidas
   * Cursos en los que me inscribí y que finalicé
   * Eficacia de los cursos
   * Programas de aprendizaje en los que me inscribí y que finalicé
   * Tiempo de aprendizaje dedicado a cada curso
   * Tiempo de aprendizaje dedicado por trimestre
   * Finalización de la certificación

1. En las opciones desplegables, seleccione **[!UICONTROL Eje Y]** para su informe. En algunos de los criterios seleccionados, puede elegir uno o varios estados en las opciones de Estados. Por ejemplo, para el criterio principal Estadísticas de inscripción en el curso, los estados pueden ser Finalizado, Incompleto e Inscrito. Los datos del intervalo principal se representan en forma de gráfico de barras en el informe.

   ![](assets/axes-for-reports.png)
   *Ejes para informes*

1. En las opciones desplegables, seleccione el criterio o intervalo **[!UICONTROL Eje Y]** para su informe. Por ejemplo, en la opción de inscripción en programas de aprendizaje, elija uno o varios estados de la lista Estados. Los datos del intervalo secundario se representan en forma de gráfico de líneas.
1. Seleccione los criterios apropiados del eje X** para su informe entre las opciones desplegables. Si se selecciona la fecha como eje X, está disponible la opción de agrupar los criterios del eje X por día, mes, trimestre y año.
1. En la sección Intervalo, seleccione la opción correspondiente en la lista desplegable. Opciones disponibles:

   * Último mes
   * Trimestre
   * Año
   * Trimestre hasta la fecha (últimos 90 días)
   * Año hasta la fecha (últimos 365 días)
   * Intervalo de fecha En los campos de fecha **[!UICONTROL Desde]** y **[!UICONTROL Hasta]**, proporcione valores.

   ![](assets/time-filter-for-report.png)

1. **Sección Filtros**

   Los filtros aparecen en el cuadro de diálogo Añadir informe en la parte inferior en función de los tipos de informes que ha seleccionado. Algunos de los filtros prominentes se mencionan a continuación.

   * **Responsable:** Puede elegir cualquiera de los responsables según la jerarquía. Algunos responsables pueden tener responsables subordinados y varios empleados que informen a cada responsable subordinado.
   * **Perfil:** Seleccione la designación de su empleado. Ayudaría en la visualización de informes de empleados según su perfil/designación. Por ejemplo, técnico informático o ingeniero.
   * **Grupo de usuarios:** Seleccione el grupo de usuarios teniendo en cuenta para cuál desea filtrar informes. Learning Manager busca los grupos de usuarios definidos para su cuenta según la función Usuarios.
   * **Contenido:** Puede filtrar su informe por cualquier curso si lo selecciona en la lista desplegable.

   Expanda esta sección y elija los filtros necesarios.

   ![](assets/choose-filters.png)
   *Elegir filtros*

1. Haga clic en **[!UICONTROL Guardar]** para terminar de crear un informe.

   ![](assets/sample-report.png)
   *Informe de muestra*

## Editar un informe {#editareport}

En el informe, haga clic en la flecha desplegable y seleccione la opción **[!UICONTROL Editar informe]**.

![](assets/edit-a-report-1.png)
*Editar un informe*

Realice los cambios necesarios en el informe. Para guardar los cambios, haga clic en **[!UICONTROL Guardar]**.

## Mover un informe a un tablero {#moveareporttoadashboard}

Seleccione esta opción para trasladar un informe a un tablero. Para mover el informe, haga clic en la opción **[!UICONTROL Mover al tablero]**.

![](assets/move-a-report.png)
*Mover un informe a un tablero*

Seleccione el tablero al que desea trasladar el informe; a continuación, haga clic en **[!UICONTROL Mover]**.

## Crear una copia de un informe {#createacopyofareport}

Para crear una copia del informe, seleccione la opción **[!UICONTROL Crear una copia]**.

![](assets/copy-a-report.png)
*Crear una copia de un informe*

Seleccione el tablero en el que desea copiar el informe. Para comenzar a copiar, haga clic en **[!UICONTROL Copiar]**.

## Eliminar un informe {#deleteareport}

Para eliminar un informe, seleccione la opción **[!UICONTROL Eliminar informe]**. Después de eliminar el informe, no puede restaurarlo. El proceso es irreversible. Vaya con precaución al eliminar un informe.

![](assets/delete-a-report.png)
*Eliminar un informe*

## Descargar un informe {#downloadareport}

Para descargar un informe, seleccione la opción **[!UICONTROL Descargar informe]**.

![](assets/download-a-report.png)
*Descargar un informe*

## Cambiar el tamaño de un informe {#resizeareport}

El tamaño de los informes se puede cambiar a 1×1 (medio) y 1×2 (grande). De esta manera, podrá visualizar mejor los informes. Además, los informes se pueden encuadrar y ampliar fácilmente.

## Filtros {#filters}

Los filtros aparecen en el cuadro de diálogo **[!UICONTROL Añadir]** informe en la parte inferior en función de los tipos de informes que ha seleccionado. Algunos de los filtros prominentes se mencionan a continuación.

**Responsable** Puede elegir cualquiera de los responsables según la jerarquía. Algunos responsables pueden tener responsables subordinados y varios empleados que informen a cada responsable subordinado.

**Perfil** Seleccione la designación de su empleado. Ayudaría en la visualización de informes de empleados según su perfil/designación. Por ejemplo, técnico informático o ingeniero.

**Grupo de usuarios** Seleccione el grupo de usuarios teniendo en cuenta para cuál desea filtrar informes. Learning Manager busca los grupos de usuarios definidos para su cuenta según la función Usuarios.

**Curso** Puede filtrar su informe según cualquier curso si lo selecciona de la lista desplegable.

![](assets/sample-report-admin.png)
*Filtrar un informe*

Sobre la leyenda del gráfico, puede ver un cuadro para aumentar el tamaño. Mueva el cursor sobre él, haga clic y arrastre el cursor sobre cualquier parte del área gráfica del cuadro que desee aumentar.

Puede ver los valores secundarios del eje Y en forma de línea a través de las barras del gráfico. Por ejemplo, en la muestra especificada anteriormente, puede ver los valores de Eficacia en una línea gris a través del gráfico.

## Informes de grupos de usuarios {#user-group-reporting}

Controle la manera en que los grupos de usuarios, como los departamentos, los socios externos y las funciones, se desempeñan en comparación con otros grupos de usuarios u otros objetivos del aprendizaje.

### Grupos de usuarios {#usergroups}

Para generar informes basados en grupos de usuarios, seleccione **[!UICONTROL Grupo]** de usuarios en el eje X entre las opciones de la lista desplegable, como se muestra en la captura de pantalla siguiente.

![](assets/user-group-reports.png)
*Informes de grupos de usuarios*

Para seleccionar un grupo de usuarios, escriba el nombre del grupo. Puede ver los grupos sugeridos que se muestran conforme a la cadena de texto que escribe. Cuando vea una lista de grupos, seleccione el grupo de usuarios apropiado.

También puede seleccionar varios grupos de usuarios mediante la búsqueda de escritura anticipada.

Una vez que guarda y genera este informe, si ha seleccionado varios grupos de usuarios, el informe se genera con todos los grupos de usuarios representados en el gráfico de barras uno al lado del otro en el eje X.

Este informe del grupo de usuarios le permite comparar el rendimiento de un departamento/división/función con otro para evaluar sus logros de aprendizaje.

### Atributos personalizados de los usuarios/grupos de usuarios {#customusergroupsuserattributes}

También puede crear grupos de usuarios personalizados con la función Añadir usuarios/grupos de usuarios en Learning Manager. Después de crear los grupos de usuarios, puede generar informes para los grupos de usuarios personalizados con la ayuda de una lista de atributos, por ejemplo ubicación o sucursal.

En el eje X, elija la opción Atributos de usuario y seleccione el atributo en la **** lista de opciones. Para crear un informe personalizado del grupo de usuarios basado en estos atributos, también debe seleccionar el grupo de usuarios correspondiente en el filtro.

## Visualización de informes {#viewingreports}

En la página Informes, puede ver todos los informes. Puede minimizar cada informe si hace clic en el icono menos (-) situado en la esquina superior derecha de cada informe. Haga clic en el icono (+) para ver su informe nuevamente.

## Vista rápida con fechas diferentes {#quickviewwithdifferentdates}

Puede cambiar el intervalo/valor de fecha para cualquier informe y obtener una vista rápida de una fecha diferente sin tener que modificar y guardar el informe. Haga clic en el icono Editar (como se muestra con una flecha en la instantánea a continuación) junto al intervalo de fecha, por ejemplo, trimestre hasta la fecha, último año. Seleccione el nuevo valor en el menú emergente y haga clic en la marca de verificación para confirmar el cambio. Para cancelar el cambio, haga clic en la marca X.

>[!NOTE]
>
>Los valores de fecha que utiliza para ver el informe son temporales. Esta vista del informe no se descarga cuando selecciona la opción Descargar. Esta vista solo es temporal.

![](assets/learner-count-report.png)
*Ver el recuento de alumnos*

## Vista rápida con responsables diferentes {#quickviewwithdifferentmanagers}

Si varios responsables le informan a usted, podrá ver los informes rápidamente para cada responsable. Seleccione el nombre del responsable en la lista desplegable a fin de ver un informe único para cada responsable.

>[!NOTE]
>
>Los valores de responsable que utiliza para ver el informe son temporales. Esta vista del informe no se descarga cuando selecciona la opción Descargar. Esta vista solo es temporal.

## Ver informes de cursos {#viewcoursereports}

### Generar informes de cursos

>[!INFO]
>
>En esta formación, aprenderá a exportar informes de cursos y a configurar suscripciones por correo electrónico para estos informes.<br><br>[![botón](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R726NKNM&amp;mv=display&amp;mv2=display#/course/8318904)</br></br>


Si no puede iniciar el entrenamiento, escriba a <almacademy@adobe.com>.

Puede ver los informes específicos de cada curso siguiendo estos pasos:

1. Haga clic **[!UICONTROL en el vínculo Ver informes]** de cursos en la ficha Mis tableros en la página Informes.\
   Aparecerá un cuadro de diálogo emergente. Aparece un campo de entrada de texto donde puede indicar el curso requerido y los nombres de los cursos sugeridos aparecen en la lista desplegable. Elija el curso de la lista que se muestra.

   ![](assets/view-course-report-300x117.png)

   *Ver informes de cursos*

1. Seleccione el curso que desee en la lista desplegable y haga clic en Mostrar.
1. Se le redirige a la página de resultados Puntuación de prueba del curso seleccionado para ver el informe del curso en cuestión.

**Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes**

Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para ver opciones desplegables como Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes.

![](assets/edit-options-dashboard-300x126.png)

*Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes*

**[!UICONTROL Editar]** Mientras modifica datos, regrese a los valores iniciales y haga clic en Restablecer. Haga clic en Guardar después de modificar los valores.

**[!UICONTROL Mover al tablero]** Puede mover el informe actual a otro tablero, que se elige entre la lista de tableros.

**[!UICONTROL Crear una copia]** Puede copiar el informe al mismo tablero o a otro, que se selecciona de la lista de tableros.

**[!UICONTROL Eliminar]** Haga clic en Eliminar para eliminar el informe. Aparece un mensaje de advertencia/confirmación antes de que se elimine el informe.

**[!UICONTROL Cambiar tamaño]** Puede cambiar el tamaño de sus informes a los tamaños 1×1 (grande) y 2×2 (medio).

## Generar y ver informes para cuentas de igual a igual {#generateandviewreportsforpeeraccount}

Como administrador, además de generar informes para su cuenta, puede generar y ver informes para cuentas de igual a igual que haya definido.

Cuando ha definido una cuenta de igual a igual con otro usuario, puede ver los informes de esa cuenta de igual a igual desde la página **[!UICONTROL Informes]**. Cuando crea un informe, buscará el campo **[!UICONTROL Seleccionar cuenta]**. En la lista desplegable que enumera todas las cuentas de igual a igual a las que está asociado, seleccione la cuenta cuyos informes compartidos desea ver.

Al crear una cuenta de igual a igual, si no se había seleccionado la opción Compartir catálogo, no puede ver esa cuenta de igual a igual en esta lista.

![](assets/acc1-jpg.png)
*Gestionar informes para cuentas de igual a igual*

1. Seleccione el eje X y el eje Y de este informe, y seleccione la fecha de este informe.
1. Observe el campo de filtros: el botón Catálogos compartidos se habilita automáticamente. Es obligatorio. Si el botón Catálogos compartidos no está habilitado, implica que no puede generar ni ver informes para la cuenta de igual a igual.
1. En la lista desplegable debajo de Catálogos compartidos, seleccione el catálogo compartido cuyo informe desea ver.
1. Haga clic en [!UICONTROL **Guardar**].

   ![](assets/acc2.png)
   *Seleccionar Catálogos compartidos para cuentas de igual a igual*

1. Después de hacer clic en **[!UICONTROL Guardar]**, puede ver la representación gráfica de los informes en el tablero predeterminado. En este tablero, puede filtrar aún más el informe por responsable para la cuenta de igual a igual en cuestión.
1. Si en su lado se realizan cambios en el catálogo, se reflejan inmediatamente en los informes y en el tablero generados por el igual. Ahora bien, si el igual modifica el catálogo, los cambios no se muestran automáticamente en su tablero.
1. Si desea que su tablero se actualice automáticamente, el igual debe enviarle una nueva solicitud de igual.

   >[!NOTE]
   >
   >Los responsables no pueden ver los informes de los iguales.

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++¿Cómo compartir un panel personalizado con un responsable?

Al crear un tablero, introduzca el nombre y la descripción. Para compartirlo con responsables, introduzca el nombre del responsable en el campo **[!UICONTROL Compartir con]**.

![](assets/share-dashboard-manager.png)
*Compartir un tablero*
+++
