---
description: Obtenga información sobre los informes asociados a la función de administrador en la aplicación Learning Manager.
jcr-language: en_us
title: Informes
contentowner: manochan
exl-id: 31b176b7-4b8f-4851-a0c5-4eee58bceb41
source-git-commit: 0766d751cf37721ee7befada8b66d1bcf583112e
workflow-type: tm+mt
source-wordcount: '7133'
ht-degree: 57%

---

# Informes

Obtenga información sobre los informes asociados a la función de administrador en la aplicación Learning Manager.

Adobe Learning Manager le permite crear diversos informes para supervisar y controlar las actividades de los alumnos. Las actividades de los alumnos se supervisan y se capturan automáticamente en la base de datos. Los informes del responsable y el administrador se generan a partir de la base de datos.

## Información general {#overview}

El proceso de generación de informes es similar para el administrador y el responsable. Los responsables pueden ver los informes correspondientes a sus subordinados, mientras que el administrador puede ver todos los informes en toda la empresa.

Los informes se añaden en un tablero. Un informe debe estar dentro de un tablero. Existe un **[!UICONTROL Panel predeterminado]** de forma predeterminada en la página Informes. Cualquier informe añadido por usted se añade a este tablero predeterminado. Para agregar informes a paneles individuales, usa la flecha desplegable y elige **[!UICONTROL Agregar informe]**. Para obtener más información sobre cómo crear tableros, consulte la sección Tableros en esta página.

## Tipos de informes {#typesofreports}

Adobe Learning Manager admite cuatro tipos principales de informes: de finalización, tiempo dedicado, aptitudes y eficacia. Puede utilizar los siguientes tipos de informe para generar informes de más de 300 variaciones:

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

* **Usuarios registrados:** Este informe proporciona información sobre el número de usuarios registrados en su cuenta semanalmente. En el caso de las cuentas con licencias de unidades activas mensuales, el informe presenta en su lugar las unidades MAU.

* **Informe de visitas de usuarios:** Este informe proporciona información sobre el número de usuarios que acceden diariamente a la plataforma. También está disponible el informe mensual.

* **Informe de tiempo dedicado al aprendizaje:** Este informe proporciona información sobre el tiempo dedicado al aprendizaje en la plataforma diariamente. También está disponible el informe mensual.

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

En este informe, se muestra el total de alumnos que acceden al sistema en un día o un mes. Explorar la plataforma de aprendizaje sin consumir ningún elemento de aprendizaje también se considera como un &quot;acceso&quot; a la plataforma de aprendizaje. Esto ayuda al administrador a conocer el conjunto total de usuarios que acceden al sistema. El primer día del mes, Learning Manager crea un registro del número total de usuarios que acceden a la plataforma durante el mes anterior. También captura la información de los grupos de usuarios de estos usuarios.

Solo se registran los grupos de usuarios configurados por el administrador. Esto también permite a los administradores aplicar filtros en los grupos de usuarios para los datos mensuales históricos. Tenga en cuenta que, en caso de que la configuración de grupos de usuarios se modifique y Learning Manager no haya registrado datos para este grupo de usuarios en meses anteriores, Learning Manager no podrá mostrar los datos de los grupos de usuarios recién configurados de meses anteriores.

Este informe contiene usuarios que acceden a la plataforma mediante todos los formatos, como la Web, la aplicación para dispositivos móviles, las soluciones personalizadas sin encabezado, etc. El gráfico de uso de la aplicación para dispositivos menciona específicamente solo a los usuarios que acceden a la plataforma mediante la aplicación de Learning Manager para dispositivos. Esto ayuda a los administradores a identificar el uso de la aplicación para dispositivos móviles en la cuenta.

![](assets/user-visit-report.png)
*Informe de visitas de usuarios*

### Informe de tiempo dedicado al aprendizaje {#learningtimespentreport}

Aquí puede ver un gráfico de líneas de doble eje que muestra el tiempo total de aprendizaje dedicado por todos los alumnos durante un periodo de 12 meses. El segundo eje representa el tiempo medio dedicado al aprendizaje por parte de un individuo.

El tiempo dedicado a diferentes objetos de aprendizaje, como programas de aprendizaje y certificaciones, se calcula para lo siguiente:

* Curso a ritmo personalizado con contenido estático e interactivo.
* Cursos de actividad con URL.
* Sesiones de fin de semana con el indicador de fin de semana activado.
* Sesión de conexión de clase virtual donde la asistencia se marca automáticamente.
* Tiempo empleado en diferentes objetos de aprendizaje, como programas de aprendizaje y certificaciones.
* Instrucciones xAPI para un curso de actividad xAPI.

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
*Informe de cursos de formación activos*

>[!NOTE]
>
>Los datos no se muestran del modo esperado cuando se seleccionan los filtros **[!UICONTROL Todos los usuarios]** y **[!UICONTROL 12 meses]**, pero sí se muestran al seleccionar **[!UICONTROL Todos los grupos de usuarios internos].**

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
1. Número de alumnos que han valorado el curso.
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

### Generar informes del tablero

>[!INFO]
>
>En este curso de formación, aprenderá a generar informes de tableros a partir de la base de datos.<br><br>[![botón](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R3B5NPDN&amp;mv=display&amp;mv2=display#/course/8318854)</br></br>


Si no puedes iniciar el entrenamiento, escribe a <almacademy@adobe.com>.

Consulte un informe resumido de todas las actividades de aprendizaje en la plataforma. En esta página, puede ver la siguiente información de resumen del equipo y los perfiles externos del usuario raíz seleccionado. También se puede seleccionar el intervalo de tiempo:

* Resumen de aprendizaje en forma de inscripciones, vistas y finalizaciones
* Aptitudes principales
* Resumen del cumplimiento

![](assets/summary-charts.png)
*Gráficos de resumen*

Si hay administradores internos de nivel raíz, se mostrarán uno tras otro.

Todos los perfiles externos se enumerarán después de los perfiles internos (usuarios internos de nivel raíz).

Si un perfil externo tiene un administrador, la jerarquía de administradores se mostrará en la lista desplegable **[!UICONTROL Mostrar datos para]**. El usuario aparecerá en la jerarquía de responsables en la página de todos los detalles (resumen del aprendizaje, cumplimiento y estado de aptitudes)

Si no es así, todos los detalles de los usuarios individuales se mostrarán en la lista.

Para ver detalles más detallados de las inscripciones de varios equipos internos, haga clic en **[!UICONTROL Detalles del resumen de aprendizaje]**.

![](assets/learning-sunnarydetails.png)
*Detalles del resumen de aprendizaje*

Al hacer clic en cualquier inscripción, puede ver los alumnos de cada responsable y las inscripciones a cada objeto de aprendizaje. También puede ver los detalles de progreso y finalización de cada alumno.

![](assets/learners-for-a-manager.png)
*alumnos asignados a un administrador*

Haga clic en cualquier equipo y exporte la informe como un archivo csv. Un administrador puede exportar el informe para cualquier grupo de usuarios o usuario individual seleccionando el grupo de usuarios o usuario individual y, a continuación, exportar los detalles desde la lista desplegable **[!UICONTROL Acción]**.

Además, puede ver un gráfico de barras con las aptitudes que están en curso y las que se han alcanzado. Puede añadir o quitar las aptitudes que desee incluir en el gráfico.

![](assets/skill-status-stackedbarchart.png)
*Gráfico de barras apiladas de estado de aptitudes*

### Tablero de cumplimiento

**Adobe Learning Manager** ofrece un panel de cumplimiento a todos los administradores y responsables. Los administradores pueden crear un panel de cumplimiento y compartirlo con responsables. Los responsables podrán ver el panel recién compartido en su aplicación y pueden realizar un seguimiento sencillo del cumplimiento de los miembros de su equipo para una formación en particular. El tablero de cumplimiento permite a los administradores clasificar los cursos de cumplimiento personalizado en categorías específicas (por ejemplo, Ventas, Marketing y Legal). Las categorías de cumplimiento personalizadas funcionan con **[!UICONTROL Etiquetas de catálogo]**.

![](assets/compliance-dashboard-admin.png)

_Vista de administrador del panel de cumplimiento_

Los administradores también pueden comprobar el estado de cumplimiento del equipo de cada responsable seleccionando **[!UICONTROL Ir al panel de cumplimiento]**. Los administradores pueden compartir un conjunto de cursos de formación con responsables de forma individual o en grupo. Esto ayuda a los gestores a realizar un seguimiento sencillo del cumplimiento de sus compañeros de equipo para la formación especificada.

#### Flujo de trabajo de administrador

##### Creación de etiquetas de cumplimiento personalizadas

Una etiqueta de conformidad es un tipo de etiqueta de catálogo que clasifica los cursos, las rutas de aprendizaje y las certificaciones como un tipo de conformidad.
Para crear una etiqueta de cumplimiento personalizada, siga estos pasos:

1. En la aplicación del administrador, vaya a **[!UICONTROL Configuración]** > **[!UICONTROL General]**.
1. Seleccione la opción **[!UICONTROL Tipo de cumplimiento personalizado]** para habilitar la etiqueta de cumplimiento personalizado.


   ![](assets/custom-compliance.png)
   _Habilitar cumplimiento personalizado_

   >[!NOTE]
   >
   >Esta nueva etiqueta de catálogo se ha introducido para categorizar los cursos, las rutas de aprendizaje y las certificaciones como un tipo de conformidad. Para habilitar la opción **[!UICONTROL Tipo de cumplimiento personalizado]**, primero debe habilitar la opción **[!UICONTROL Mostrar etiqueta de catálogo]** en la misma página.

1. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Etiqueta de catálogo]** y seleccione el **[!UICONTROL Tipo de cumplimiento]**.
1. Escriba los valores (p. ej., Legal, Ventas) en el cuadro de texto **[!UICONTROL Valor]** y seleccione **[!UICONTROL Agregar valor]**.

   ![](assets/custom-compliance-values.png)
   _Agregar valores para el cumplimiento personalizado_

1. Seleccione **[!UICONTROL Guardar]**.

>[!NOTE]
>
>El autor debe añadir estas etiquetas de cumplimiento al crear o editar cursos en su aplicación. Consulte [Agregar etiquetas de cumplimiento a un curso/ruta de aprendizaje/certificación](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification).

##### Crear y compartir un panel de cumplimiento

Para crear y compartir un tablero de cumplimiento, siga estos pasos:

1. Ve a **[!UICONTROL Informes]** > **[!UICONTROL Resumen del aprendizaje]**.
1. En la sección **[!UICONTROL Panel de cumplimiento]**, seleccione **[!UICONTROL Compartido con responsables]**.
1. Seleccione **[!UICONTROL Compartir panel]** y seleccione las etiquetas creadas en el menú desplegable **[!UICONTROL Seleccionar etiqueta de cumplimiento]**.


   ![](assets/compliance-type.png)
   _Seleccionar el tipo de cumplimiento_

1. Escriba y seleccione el nombre del administrador en el cuadro de texto **[!UICONTROL Compartir con]**.
1. Seleccione **[!UICONTROL Compartir]** para enviar el panel al administrador seleccionado.

>[!NOTE]
>
>Al compartir el nuevo panel, se sobrescribirá el panel existente en la aplicación del administrador seleccionado. Los responsables podrán ver el panel que los administradores han compartido recientemente.

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

Los administradores pueden generar informes específicos mediante la plantilla personalizada disponible en la sección **[!UICONTROL Informes]**.

### Informes de muestra {#samplereports}

La ficha **[!UICONTROL Informes de muestra]** presenta algunos informes indicativos que se basan en puntos de datos de muestra. Explore estos informes para tener una idea de los distintos tipos de informes repletos de funciones que puede generar con los datos de su cuenta.

### Informes de tableros {#dashboardreports}

Un tablero es una colección de informes. Los informes se pueden agrupar en un tablero según su elección. Para ver todos los tableros creados, haga clic en esta ficha del tablero. En la lista desplegable **[!UICONTROL Ver panel]**, puede seleccionar la placa predeterminada o un panel que haya creado.

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

1. Abra **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Informes del curso]**.
1. Se muestra el cuadro de diálogo **[!UICONTROL Informe del curso]**. Seleccione el curso, cuyo informe quiere obtener y haga clic en **[!UICONTROL Mostrar]**.

   ![](assets/course-reports.png)
   *Informes del curso*

1. Se le redirige a la página del curso. Puede exportar la puntuación de la prueba por usuario y por pregunta en función de cada inscripción seleccionando el tipo de inscripción específico.
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

Para obtener información sobre cómo generar informes de transcripciones de alumnos, consulte [Transcripciones de alumnos](learner-transcripts.md).

### Informes de anuncios {#announcementsreports}

Como administrador, puede generar un informe de todos los anuncios que envíe. El informe contiene datos relativos a los aspectos siguientes:

* Tipo de anuncio
* Nombre del anuncio
* Fecha del anuncio
* Estado del anuncio
* Nombre del alumno

Para descargar un informe, siga cualquiera de estos pasos:

1. Abra **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Informe de anuncios]**. Se abre el cuadro de diálogo **[!UICONTROL Generando solicitud de informe]**. Haga clic en Aceptar.
1. [!UICONTROL **Anuncios**] > [!UICONTROL **Acciones**] > [!UICONTROL **Informe de exportación**].

   ![](assets/announcements.png)
   *Informe de anuncios*

1. Puedes extraer un informe de un anuncio específico haciendo clic en **[!UICONTROL Exportar informe]** debajo del icono de configuración.

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

* Abra **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Informes de ayudas de trabajo]**. Aparece el cuadro de diálogo **[!UICONTROL Generando solicitud de informe]**. Haga clic en **[!UICONTROL Aceptar]**.
* Abra **[!UICONTROL Ayuda de trabajo]** > **[!UICONTROL Acciones]** > **[!UICONTROL Informe de exportación]**.

![](assets/job-aids.png)
*Informe de ayudas de trabajo*

* También puede extraer un informe de una ayuda de trabajo específica haciendo clic en **[!UICONTROL Exportar informe]** debajo del icono de configuración.

![](assets/job-aid-specific-download.png)
*Informe de ayuda de trabajo específica*

### Informe de ayudas de trabajo

Después de seleccionar **[!UICONTROL Informe de ayudas de trabajo]** en la lista, verá dos opciones:

![informe de ayudas de trabajo](assets/job-aids-new.png)
*Descargar informe de inscripción de usuarios de ayudas de trabajo*

**Todas las ayudas de trabajo**: si el número de ayudas de trabajo de la cuenta es inferior a 10 millones, el informe generado contendrá la información de inscripción de todas las ayudas de trabajo. Esta será la selección predeterminada. Si el número de filas supera los 10 millones, se mostrará un error y deberá seleccionar manualmente las ayudas de trabajo necesarias.

**Ayudas de trabajo seleccionadas**: Si selecciona esta opción, puede especificar las ayudas de trabajo para las que desea generar el informe. Puede seleccionar un máximo de 10 ayudas de trabajo. Adobe Learning Manager comprueba si el número de ayudas de trabajo supera los 10 millones.

![registro de informe de ayudas de trabajo](assets/job-aids-2-new.png)
*Seleccionar una ayuda de trabajo*

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

Utilice el generador de informes **[!UICONTROL Registro de auditoría de contenido]** para generar un informe de todos los cambios y modificaciones realizados en un curso durante su duración en el sistema. El informe generado muestra la información siguiente recopilada:

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

En la columna **Tipo de modificación**, obtendrá los siguientes detalles:

| Tipo de modificación | Descripción |
| --- | --- |
| Crear | Curso creado |
| Adición de certificación | Certificación añadida al catálogo |
| Eliminación de certificación | Certificación eliminada del catálogo |
| Añadir contenido | Contenido añadido al módulo |
| Agregar curso | Curso añadido a la ruta de aprendizaje |
| Eliminar curso | Curso eliminado de la ruta de aprendizaje |
| Agregar etiqueta personalizada | Etiqueta personalizada añadida al catálogo |
| Quitar etiqueta personalizada | Etiqueta personalizada quitada del catálogo |
| Eliminar | Catálogo eliminado |
| Agregar ayuda de trabajo | Ayuda de trabajo añadida al catálogo |
| Eliminar ayuda de trabajo | Ayuda de trabajo eliminada del catálogo |
| Agregar ruta de aprendizaje | Ruta de aprendizaje añadida al catálogo |
| Eliminar ruta de aprendizaje | Ruta de aprendizaje quitada del catálogo |
| Adición de contenido de módulo | Módulo añadido al curso (sección Contenido) |
| Quitar contenido del módulo | Módulo eliminado del curso (sección Contenido) |
| Publicado | Curso o ruta de aprendizaje publicados y añadidos al catálogo predeterminado |
| Republicado | Curso republicado |
| Adición de recursos | Recurso añadido al curso |
| Eliminación de recurso | Recurso eliminado del curso |
| Retirado | Curso retirado |
| Añadir catálogo compartido | Catálogo compartido a catálogo |
| Quitar catálogo compartido | Uso compartido de catálogos eliminado del catálogo |
| Actualización del catálogo compartido | Estado de uso compartido de catálogos : activo |
| Actualización | Actualización de la ruta del curso o aprendizaje |
| Añadir grupo de usuarios | Grupo de usuarios añadido al catálogo |
| Quitar grupo de usuarios | Grupo de usuarios eliminado del catálogo |

La información relativa a metadatos no se recopila en el informe generado.

Para generar un informe de registro de auditoría de un curso, siga estos pasos.

1. Seleccione **[!UICONTROL Informe]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Registro de auditoría del curso]**. Aparece el cuadro de diálogo **[!UICONTROL Registro de auditoría de contenido]**.

   ![](assets/course-audit-trial.png)
   *Seguimiento de auditoría del curso*

1. Seleccione el curso, el programa de aprendizaje y la certificación de los que desea descargar el informe. Si no se especifica, de manera predeterminada se descargan todos los informes.
1. Seleccione un intervalo de fechas para el informe y haga clic en **[!UICONTROL Generar]**.
1. El informe se genera y se le notifica que el informe de auditoría de contenido está listo. Puede descargar el informe.

### Informes de registro de auditoría de usuarios {#useraudittrailreports}

El seguimiento de auditoría de usuarios captura el ciclo de vida de los usuarios, los grupos de usuarios y los perfiles de registro automático. Se captura la adición y eliminación de usuarios, y los cambios del responsable. Se registra la creación y eliminación de perfiles de registro automático. El registro automático también se puede pausar y reanudar.

Durante el registro automático puede añadir, habilitar, deshabilitar, pausar o reanudar en perfiles externos. También se capturan las cargas de CSV.

1. Seleccione **[!UICONTROL Informe > Informe de Excel > Registro de seguimiento de usuario]**. Aparece el cuadro de diálogo Registro de auditoría de usuarios.
1. Se muestra el cuadro de diálogo Registro de auditoría de usuarios. Seleccione el intervalo de fechas en el menú emergente. Puede elegir entre generar el informe de la última semana, el último mes o seleccionar una fecha personalizada.

   ![](assets/user-audit-trail.png)
   *Seguimiento de auditoría de usuarios*

1. Haga clic en **[!UICONTROL Generar]** para generar el informe.

Hay dos filtros en el cuadro de diálogo **[!UICONTROL Informe de seguimiento de auditoría de usuarios]**.

**Filtro de intervalo de fechas:** Elija el intervalo de fechas para el que desea generar el informe. Hay tres opciones:

* Última semana
* Último mes
* Fecha personalizada

Seleccionar filtro de alumnos: Buscar un usuario o un grupo de usuarios.

El informe exportado contendrá datos de los usuarios que cumplan los dos criterios de búsqueda especificados.

![](assets/user-audit-trail.png)
*Registro de auditoría de usuarios*

>[!NOTE]
>
>Cuando se asigna o se elimina una aptitud, se puede realizar un seguimiento de la aptitud en el Informe de auditoría de usuarios, tanto si se asigna como si se elimina.

### Informe de configuración de extensiones

Este informe proporciona información sobre los detalles de configuración de todas las extensiones nativas agregadas, incluido su estado de activación. Obtenga información sobre cómo descargar el informe de extensión. Consulte [Descargar informe de extensión](native-extensibility.md#download-extension-report).

### Informe de actividad de xAPI

Este informe proporciona los datos de todas las instrucciones de xAPI registradas y generadas durante los módulos de actividad de xAPI.

Para descargar este informe, siga estos pasos:

1. Seleccione **[!UICONTROL Informe > Informe de Excel > Informe de actividad de xAPI]**. Aparece el cuadro de diálogo Informe de actividad de xAPI.
1. Seleccione el intervalo de fechas en el menú emergente. Puede elegir entre generar el informe de la última semana, el último mes o seleccionar una fecha personalizada.
1. Seleccione los alumnos y la actividad en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]** para generar el informe.

### Informes de interacciones {#gamification}

Los administradores pueden descargar la transcripción de interacción en formato .csv. Puede descargar el informe para usuarios individuales o grupos de usuarios. El nombre de usuario, el correo electrónico del usuario, el UUID del usuario, el total de puntos de usuario obtenidos, la agrupación de puntos recopilados, el nombre de los grupos en los que el usuario interviene, el nombre del responsable y los valores de los campos activos se obtienen en el informe. Los administradores pueden usar este informe para evaluar y comprender las clasificaciones de usuarios en el nivel de la empresa o para un grupo específico.

1. Seleccione Informe > Informe de Excel > Informe de interacción.

   ![](assets/gamification.png)
   *Informe de interacción*

1. Aparece el cuadro de diálogo Transcripciones de interacciones. Seleccione alumnos usando su nombre, perfil, grupos de usuarios, ID de correo electrónico o UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Cuadro de diálogo Transcripciones de interacciones*

1. Haga clic en **[!UICONTROL Generar]** para generar el informe.

   Después de generar el informe de un alumno, debe poder exportar la información actual y del nivel alcanzado para todos los usuarios (internos, externos o eliminados) de la cuenta. También puede consultar las fechas de los niveles alcanzados por un alumno:

   * Fecha de obtención de Bronce
   * Fecha de obtención de Plata
   * Fecha de obtención de Oro
   * Fecha de obtención de Platino

   Estas columnas contienen las fechas en que se alcanzó el nivel por primera vez. La columna **[!UICONTROL Nivel actual]** muestra el nivel actual del alumno.

   Cuando el administrador restablece la interacción, todos los puntos del alumno se restablecen en consecuencia.

### Informe de seguimiento de auditoría de interacción {#gamification-audit-trail}

Este informe contiene el historial y los motivos de los puntos de interacción de los alumnos obtenidos para cada regla.

### Descargar el informe

1. Seleccione la URL de seguimiento de auditoría de interacción.
1. En el elemento emergente **Seguimiento de auditoría de interacción**, seleccione el intervalo de fechas.
1. Seleccione **Generar**.

El informe se descarga como archivo CSV. El archivo contiene las siguientes columnas:

* Nombre
* Correo electrónico/UUID,
* Estado
* Acción
* Puntos,
* Puntos de saldo
* Regla/ Tarea
* Subtarea de regla/tarea,
* Detalles de regla/tarea
* Tipo,
* Nombre,
* Nombre de instanciaFecha de obtención (zona horaria UTC)
* Hora de inicio de regla/tarea
* Hora de finalización de regla/tarea

### Informe de inscripción y baja {#enrollmentandunenrollmentreport}

Los administradores y responsables pueden extraer un informe de los alumnos que se han inscrito y se han dado de baja. Como administrador, puede ver a cualquier alumno, administrador o responsable que se ha inscrito o dado de baja de una instancia de curso, programa de aprendizaje o certificación, y exportar el informe. Mientras que, como responsable, solo puede obtener un informe de los miembros del equipo. Como responsable, no puede ver a los alumnos eliminados ni su propio nombre en la aplicación del responsable como alumno inscrito o que se ha dado de baja.

Para descargar un informe, sigue estos pasos: abre el **[!UICONTROL curso/programa de aprendizaje/certificación]** > **[!UICONTROL alumnos]** > **[!UICONTROL Acción]** > **[!UICONTROL Informe de exportación]**.

![](assets/unenrollment.png)
*Informe de cancelación de inscripción*

### Informe de comentarios {#feedback-report}

Como administrador, ahora puede obtener comentarios del alumno (L1) y del responsable (L3) en relación con los cursos de formación seleccionados durante un periodo especificado.

Puede exportar los datos desde la interfaz de usuario o a través del conector de Power BI para realizar un análisis más detallado.

Los informes de comentarios de L1 y L3 ofrecen la opción de descargar un informe de comentarios consolidado para las respuestas de L1 y L3 de los cursos de formación seleccionados durante el intervalo de **un año** o de hasta 10 cursos de formación seleccionados para cualquier intervalo de fechas.

Inicie sesión como administrador, haga clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** y, en la lista de informes, haga clic en **[!UICONTROL Informe de comentarios]**.

![](assets/download-feedbackreport.png)
*Descargar informe de comentarios*

Al hacer clic en Descargar después de seleccionar los filtros, recibirá una notificación para descargar el informe en formato CSV.

El informe descargado incluirá detalles como el nombre y el tipo de curso de formación, el nombre de la instancia, el nombre y el correo electrónico del alumno, el tipo de comentarios: L1 o L3, las fechas de los comentarios enviados para los nuevos datos.

Para los datos existentes antes de la implementación de esta función, se mostrará la fecha de finalización del objeto de aprendizaje, el texto real de ritmo personalizado de la pregunta de comentarios de L1 y el texto de clase en diferentes columnas, las respuestas respectivas de los comentarios de L1, el nombre y el correo electrónico del responsable, el valor de los comentarios de L3 y la fecha de envío, y los campos activos.

También puede exportar los datos desde la interfaz de usuario o en Power BI, que admite todos los cursos de formación de cualquier intervalo de fechas, para realizar un análisis más detallado

### Informe de cursos de formación {#training-report}

Learning Manager admite el informe de formación, que permite a los administradores descargar detalles de formación y sus metadatos asociados, como el autor, la fecha de publicación, las aptitudes, las etiquetas de catálogo, etc.

En la aplicación de administración, haz clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Informe de cursos de formación]**.

Puede descargar informes para lo siguiente:

* Cursos de formación seleccionados (límite de 10): permite elegir uno o varios cursos de formación (hasta 10) de cualquier catálogo
* Cursos de formación de los catálogos seleccionados (límite de 5): se pueden seleccionar hasta cinco catálogos.
* Todos los cursos de formación: todos los cursos de formación de la cuenta.

![](assets/download-trainingreport.png)
*Descargar informe de formación*

En la sección Opciones avanzadas, están disponibles las siguientes opciones:

* Incluir asignaciones de cursos con programa de aprendizaje/certificación
* Incluir información en el nivel de módulo

Después de seleccionar los filtros y hacer clic en Descargar, recibirá una notificación para descargar el informe en formato CSV.

El informe tendrá los siguientes campos:

*Nombre del catálogo, Tipo de curso de formación, ID del curso de formación, ID exclusivo del curso de formación, Nombre del curso de formación, Subcursos de formación, Módulos, Duración del curso de formación o módulo, Formato, Estado del curso de formación, Aptitudes, Autor, Fecha de la última publicación, Fecha de la última finalización, Recuento de inscripciones de instructores, Cantidad de iniciados, Cantidad de finalizaciones, Puntuación L1 media, Puntuación L2 media, Puntuación L3 media, Respuestas L1 recibidas, Respuestas L2 recibidas, Respuestas L3 recibidas, Etiquetas de catálogo y Etiquetas.*

![](assets/more-options.png)
*Opciones adicionales*

### Informe de resumen de sesión {#session-summary-report}

El informe de resumen de sesión contiene todas las sesiones planificadas para un alumno en una fecha especificada.

Esto permite al administrador exportar todos los detalles de la sesión virtual y de clase que estén dentro del intervalo de fechas especificado. El administrador también puede exportar el informe de la sesión con respecto a determinados instructores o formadores.

Esto también ayudará al administrador a comprender las sesiones programadas mensualmente e identificar el horario de los instructores y las sesiones ya realizadas.

Como administrador, haga clic en **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informe de resumen de sesión]**.

En el cuadro de diálogo que aparece a continuación, elija el intervalo de fechas y el instructor o la formación para un resumen.

![](assets/session-summary-report.png)
*Informe de resumen de sesión*

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

Para descargar el informe, haz clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informe de uso del instructor]**.

Seleccione uno o varios instructores y el intervalo de fechas.

![Descargar informe de uso del instructor](assets/utilization-report.png)
*Descargar informe de uso del instructor*

El informe descargado contiene los siguientes campos:

* Nombre del instructor
* ID del instructor
* Nivel de competencia
* Fechas como columnas. Si el instructor se utiliza en una fecha, se muestra el número de sesiones. Si no se utiliza el instructor en un día, el valor muestra cero.

El informe contiene registros de tres meses a partir del mes seleccionado.

Para recuperar los registros de todos los instructores, deje el campo Instructor en blanco.

Además, un administrador personalizado con permiso para generar informes puede recuperar este informe.

### Informe de registro de auditoría de usuarios

Este informe captura información sobre los alumnos que cambiaron instancias, &quot;de instancia&quot; a &quot;instancia&quot;, cambiaron por hora, fecha, etc.

Seleccione los alumnos o un grupo de usuarios.

Para descargar el informe, haz clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informe de seguimiento de auditoría de usuarios]**.

![Descargar informe de seguimiento de auditoría de usuarios](assets/user-audit-report.png)

*Descargar informe de seguimiento de auditoría de usuarios*

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
>En este curso de formación, aprenderá a configurar suscripciones de correo electrónico para informes de tableros.<br><br>[![botón](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PLHRQ62N&amp;mv=display&amp;mv2=display#/course/8318927)</br></br>


Si no puedes iniciar el entrenamiento, escribe a <almacademy@adobe.com>.

En la página **[!UICONTROL Informes]**, haga clic en la pestaña **[!UICONTROL Suscripción]**. Aparece la página de suscripción a informes.

Para seleccionar el nombre del informe en la lista desplegable, empiece a escribir el nombre del informe en el campo Informes. Seleccione la frecuencia del correo electrónico en la lista desplegable. Puede añadir el asunto del correo electrónico y proporcionar un ID de correo electrónico alternativo.

Puede editar y eliminar las suscripciones.

## Informes históricos

Los informes históricos de Adobe Learning Manager (ALM) hacen referencia a los informes que capturan los datos históricos y las actividades dentro de la plataforma de aprendizaje. Estos informes proporcionan información sobre actividades de alumnos anteriores, contenido de formación, rendimiento de grupos de usuarios y otros datos relevantes. Los informes históricos permiten a los administradores hacer un seguimiento, supervisar y analizar el progreso y la eficacia de las iniciativas de aprendizaje a lo largo del tiempo.

### Informes de acceso al curso

Los informes de acceso al curso proporcionan información sobre la revisión de cada curso.

Para descargar este informe, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes históricos]**.
1. Seleccione **[!UICONTROL Informe de acceso al curso]**. Se abre el cuadro de diálogo Generando solicitud de informe.
1. Seleccione el año y el trimestre en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]**.

### Informes de inicio de sesión/acceso

Los informes de inicio de sesión/acceso proporcionan información sobre los inicios de sesión y el acceso de los usuarios. Puede generar informes que contengan datos de tres meses a la vez.

Para descargar este informe, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes históricos]**.
1. Seleccione **[!UICONTROL Informe de inicio de sesión/acceso]**. Se abre el cuadro de diálogo Generando solicitud de informe.
1. Seleccione el año y el trimestre en el menú desplegable.
1. Seleccione **[!UICONTROL Generar]**.

## Crear un tablero {#createadashboard}

1. Para comenzar a crear sus propios tableros, haga clic en Agregar tablero en el lado derecho de la página.

   ![](assets/add-dashboards.png)
   *Agregar paneles*

1. Proporcione un nombre y una descripción para el tablero.
1. Si desea compartir el panel con cualquier responsable, elíjalo en el campo **[!UICONTROL Compartir con]**. Puede usar cualquier criterio de selección normal para esta operación.
1. Haga clic en **[!UICONTROL Guardar].**

Puede ver el tablero creado recientemente en la ficha **[!UICONTROL Informes de tableros]**.

Para añadir informes a tu tablero, haz clic en el menú desplegable situado en la esquina superior derecha de la ventana de tu tablero y haz clic en **[!UICONTROL Añadir informe]**. El informe que crea de este modo se asocia con su tablero.

>[!NOTE]
>
>Los informes que cree haciendo clic en Agregar en la esquina superior derecha de la página Informes se agregan al panel predeterminado.

## Tableros compartidos {#shareddashboards}

Los tableros compartidos son una colección de informes que otros usuarios de la empresa han compartido con usted. Cualquier informe que añada a un tablero compartido se comparte automáticamente con otros usuarios que tengan acceso a dicho tablero.

Puede compartir el tablero de dos formas:

* Introduciendo usuarios en el campo **[!UICONTROL Compartir con]** con los que se comparte el panel.
* Elija Editar tablero en la lista desplegable e indique los detalles del usuario para compartir el tablero.

>[!NOTE]
>
>Un responsable solo puede ver los informes de los miembros de su equipo desde un tablero compartido.

## Descargas {#downloads}

La hoja exportada de informes del tablero proporciona información detallada en lugar de un resumen del informe. El informe descargado tiene el formato de una transcripción de alumno.

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
1. Seleccione los criterios del eje X**** apropiados para el informe en las opciones desplegables. Si se selecciona la fecha como eje X, está disponible la opción de agrupar los criterios del eje X por día, mes, trimestre y año.
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

1. Haga clic en **[!UICONTROL Guardar]** para completar la creación de un informe.

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
*Mover un informe a un panel*

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

**Curso** Puedes filtrar tu informe según cualquier curso seleccionándolos en el menú desplegable.

![](assets/sample-report-admin.png)
*Filtrar un informe*

Sobre la leyenda del gráfico, puede ver un cuadro para aumentar el tamaño. Mueva el cursor sobre él, haga clic y arrastre el cursor sobre cualquier parte del área gráfica del cuadro que desee aumentar.

Puede ver los valores secundarios del eje Y en forma de línea a través de las barras del gráfico. Por ejemplo, en la muestra especificada anteriormente, puede ver los valores de Eficacia en una línea gris a través del gráfico.

## Informes de grupos de usuarios {#user-group-reporting}

Controle la manera en que los grupos de usuarios, como los departamentos, los socios externos y las funciones, se desempeñan en comparación con otros grupos de usuarios u otros objetivos del aprendizaje.

### Grupos de usuarios {#usergroups}

Para generar informes basados en grupos de usuarios, elija **[!UICONTROL Grupo de usuarios]** en el eje X entre las opciones de la lista desplegable, como se muestra en la captura de pantalla a continuación.

![](assets/user-group-reports.png)
*Informes de grupos de usuarios*

Para seleccionar un grupo de usuarios, escriba el nombre del grupo. Puede ver los grupos sugeridos que se muestran conforme a la cadena de texto que escribe. Cuando vea una lista de grupos, seleccione el grupo de usuarios apropiado.

También puede seleccionar varios grupos de usuarios mediante la búsqueda de escritura anticipada.

Una vez que guarda y genera este informe, si ha seleccionado varios grupos de usuarios, el informe se genera con todos los grupos de usuarios representados en el gráfico de barras uno al lado del otro en el eje X.

Este informe del grupo de usuarios le permite comparar el rendimiento de un departamento/división/función con otro para evaluar sus logros de aprendizaje.

### Atributos personalizados de los usuarios/grupos de usuarios {#customusergroupsuserattributes}

También puede crear grupos de usuarios personalizados con la función Añadir usuarios/grupos de usuarios en Learning Manager. Después de crear los grupos de usuarios, puede generar informes para los grupos de usuarios personalizados con la ayuda de una lista de atributos, por ejemplo ubicación o sucursal.

En el eje X, elija la opción Atributos de usuario y seleccione el atributo en la lista desplegable **select** que está a su lado. Para crear un informe de grupo de usuarios personalizado basado en estos atributos, también debe elegir el grupo de usuarios adecuado en el filtro.

## Visualización de informes {#viewingreports}

En la página Informes, puede ver todos los informes. Puede minimizar cada informe si hace clic en el icono menos (-) situado en la esquina superior derecha de cada informe. Haga clic en el icono (+) para ver su informe nuevamente.

## Vista rápida con fechas diferentes {#quickviewwithdifferentdates}

Puede cambiar el intervalo/valor de fecha para cualquier informe y obtener una vista rápida de una fecha diferente sin tener que modificar y guardar el informe. Haga clic en el icono de edición (como se muestra con una flecha en la captura de pantalla siguiente) junto al intervalo de fechas, como SAT, del último año. Seleccione el nuevo valor en el menú emergente y haga clic en la marca de verificación para confirmar el cambio. Para cancelar el cambio, haga clic en la marca X.

>[!NOTE]
>
>Los valores de fecha que utiliza para ver el informe son temporales. Esta vista del informe no se descarga cuando selecciona la opción Descargar. Esta vista solo es temporal.

![](assets/learner-count-report.png)
*Ver recuento de alumnos*

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


Si no puedes iniciar el entrenamiento, escribe a <almacademy@adobe.com>.

Puede ver los informes específicos de cada curso siguiendo estos pasos:

1. Haga clic en el vínculo **[!UICONTROL Ver informes de cursos]** en la ficha Mis paneles de la página Informes.\
   Aparecerá un cuadro de diálogo emergente. Aparece un campo de entrada de texto donde puede introducir el curso requerido y los nombres de los cursos sugeridos aparecen en la lista desplegable. Elija el curso de la lista que se muestra.

   ![](assets/view-course-report-300x117.png)

   *Ver informes de cursos*

1. Seleccione el curso que desee en la lista desplegable y haga clic en Mostrar.
1. Se le redirige a la página de resultados Puntuación de prueba del curso seleccionado para ver el informe del curso en cuestión.

**Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes**

Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para ver opciones desplegables como Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes.

![](assets/edit-options-dashboard-300x126.png)

*Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes*

**[!UICONTROL Editar]** Para volver a los valores iniciales al modificar los datos, haga clic en Restablecer. Haga clic en Guardar después de modificar los valores.

**[!UICONTROL Mover al panel]** Puede mover el informe actual a otro panel, que se elige de la lista de paneles.

**[!UICONTROL Crear una copia]** Puede copiar el informe en el mismo panel o en otro distinto, que se elija en la lista de paneles.

**[!UICONTROL Eliminar]** Haga clic en Eliminar para quitar el informe. Aparece un mensaje de advertencia/confirmación antes de que se elimine el informe.

**[!UICONTROL Cambiar tamaño]** Puedes cambiar el tamaño de tus informes en tamaños 1×1 (mediano) y 2×2 (grande).

## Generar y ver informes para cuentas de igual a igual {#generateandviewreportsforpeeraccount}

Como administrador, además de generar informes para su cuenta, puede generar y ver informes para cuentas de igual a igual que haya definido.

Cuando ha definido una cuenta de igual a igual con otro usuario, puede ver los informes de esa cuenta de igual a igual desde la página **[!UICONTROL Informes]**. Cuando crea un informe, buscará el campo **[!UICONTROL Seleccionar cuenta]**. En la lista desplegable que enumera todas las cuentas de igual a igual a las que está asociado, seleccione la cuenta cuyos informes compartidos desea ver.

Al crear una cuenta de igual a igual, si no se había seleccionado la opción Compartir catálogo, no puede ver esa cuenta de igual a igual en esta lista.

![](assets/acc1-jpg.png)
*Administrar informes para cuentas de igual a igual*

1. Seleccione el eje X y el eje Y de este informe, y seleccione la fecha de este informe.
1. Observe el campo de filtros: el botón Catálogos compartidos se habilita automáticamente. Es obligatorio. Si el botón Catálogos compartidos no está habilitado, implica que no puede generar ni ver informes para la cuenta de igual a igual.
1. En la lista desplegable debajo de Catálogos compartidos, seleccione el catálogo compartido cuyo informe desea ver.
1. Haga clic en [!UICONTROL **Guardar**].

   ![](assets/acc2.png)
   *Seleccionar catálogo compartido para cuenta de igual a igual*

1. Después de hacer clic en **[!UICONTROL Guardar]**, puedes ver la representación gráfica de tus informes en tu panel predeterminado. En este tablero, puede filtrar aún más el informe por responsable para la cuenta de igual a igual en cuestión.
1. Si en su lado se realizan cambios en el catálogo, se reflejan inmediatamente en los informes y en el tablero generados por el igual. Ahora bien, si el igual modifica el catálogo, los cambios no se muestran automáticamente en su tablero.
1. Si desea que su tablero se actualice automáticamente, el igual debe enviarle una nueva solicitud de igual.

   >[!NOTE]
   >
   >Los responsables no pueden ver los informes de los iguales.

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++Cómo compartir un panel personalizado con un responsable

Al crear un tablero, introduzca el nombre y la descripción. Para compartirlo con responsables, introduzca el nombre del responsable en el campo **[!UICONTROL Compartir con]**.

![](assets/share-dashboard-manager.png)
*Compartir un panel*
+++
