---
description: Este documento contiene consejos para la resolución básica de los problemas típicos que pueden presentarse al migrar datos y contenido de los LMS existentes a Learning Manager.
jcr-language: en_us
title: Solución de problemas de migración
contentowner: jayakarr
exl-id: b9f17644-f237-4701-86e9-8496db941920
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 43%

---

# Solución de problemas de migración

Este documento contiene consejos para la resolución básica de los problemas típicos que pueden presentarse al migrar datos y contenido de los LMS existentes a Learning Manager.

## Problemas de migración genéricos {#genericmigrationissues}

### No es posible iniciar sesión en la carpeta FTP o la carpeta de contenido {#unabletologintoftpfolderorcontentfolder}

Asegúrese de que las cuentas se hayan creado en los servicios FTP y Box. Cuando cree un proyecto de migración, solicite la configuración de estos dos servicios. En cuanto cree los servicios, recibirá mensajes de correo electrónico de Exavault y Box para restablecer o configurar las contraseñas. Si no recuerda las contraseñas, puede restablecerlas visitando los sitios web de Exavault y Box.

### Los trabajos no se reflejan después de hacer clic en el botón Actualizar {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Asegúrese de que los archivos CSV se carguen en la carpeta correcta en el FTP de Exavault. La ruta debe ser la siguiente:

`code Account>Project>Sprint location`

* Asegúrese que los nombres de los archivos CSV se especifican teniendo en cuenta los nombres de la especificación CSV:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Se producen errores para los trabajos con registros de errores {#failuresareshownforjobswitherrorrecords}

1. Descargue los registros de errores haciendo clic en el vínculo **Descargar registros de errores**
1. Corrija los archivos CSV originales según los errores notificados, y
1. Vuelva a ejecutar el sprint con los archivos CSV modificados.

La práctica recomendada es ejecutar archivos CSV modificados en un nuevo sprint cuando el número de cambios es menor que el número total de registros.

### No es posible iniciar sesión en la aplicación Learning Manager, ni siquiera después de detener la migración de Sprint {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

El desbloqueo de una cuenta después de detener o completar una ejecución de Sprint puede llevar 10-15 minutos. Intente acceder a la aplicación pasados 15 minutos.

### Algunos de los trabajos de migración muestran el estado &quot;En curso&quot; incluso después de que se active &quot;Detener&quot;. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Puede tardar entre 10 y 15 minutos en dejar de ejecutar todos los trabajos una vez que esté en el estado &quot;En curso&quot;. Vuelve a comprobar el estado después de 10 minutos.

### No es posible crear un Sprint porque el botón está desactivado {#unabletocreateasprintasthebuttonisdisabled}

Asegúrese de que el sprint actual esté marcado como completado antes de crear un sprint. Haga clic en **[!UICONTROL Marcar sprint completado]** en la parte superior de la página para completar una migración de sprint.

### No es posible marcar un proyecto de migración como completado porque el botón está desactivado {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Asegúrese de que el sprint actual esté marcado como completado antes de marcar la finalización del proyecto de migración. Haga clic en **[!UICONTROL Marcar sprint completado]** en la parte superior de la página para completar una migración de sprint.

## Problemas de CSV {#csvissues}

### La migración del archivo module_version.csv falla y el contenido no se migra {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Asegúrese de que el contenido esté disponible en la carpeta Contenido (cuenta de Box en el proyecto de migración especificado, ruta de sprint). Además, asegúrese de haber seleccionado la opción **Sí** para **¿Va a migrar contenido para este sprint?Pregunta** en la página de creación de sprint.

Si olvida seleccionar **Sí** y continúa en este Sprint, debe esperar a que se complete. Cree otro sprint y asegúrese de hacer clic en **[!UICONTROL Sí]**.

### Los registros enrollment.csv o user_course_grade.csv fallan con el mensaje de error &quot;No es un ID de Learning Manager válido&quot; {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Asegúrese de que el ID del correo electrónico proporcionado como parte de los campos userId, assignedByUserID corresponda a usuarios válidos de Learning Manager. Si no es así, añada el usuario y cree un nuevo Sprint con la opción **Sincronizar usuarios** seleccionada. Si el usuario no forma parte de la organización, añádalo como usuario eliminado en Learning Manager mediante la especificación CSV Añadir usuarios . A continuación se incluye una especificación de ejemplo de CSV para añadir usuarios eliminados como referencia.

[Usuarios.csv](assets/users.zip) Consulte la sección **Especificaciones de CSV y ejemplos de CSV** en el [Manual de migración](../integration-admin/feature-summary/migration-manual.md) para descargar un conjunto completo de especificaciones de CSV y archivos CSV de muestra.

### Los cursos aparecen en blanco o se reproducen módulos incorrectos para un curso migrado {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Asegúrese de que el valor de clave **moduleOrderInCourse** de un curso comience por **0** y esté en orden continuo. El orden en términos de courseModuleType debe ser PRETEST, TESTOUT, CONTENT

Además, asegúrese de que dos versiones de la actividad, la clase y la clase virtual no estén vinculadas al curso existente.

### Recepción de un mensaje como &quot;El módulo ya está vinculado a un curso existente&quot; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager no permite vincular el módulo Actividad/Clase virtual/Clase con más de un curso. Asegúrese de que el módulo no esté vinculado a ningún otro curso.

### Todos los cursos muestran la versión más reciente de los módulos Actividad/Clase virtual/Clase, aunque los cursos estén vinculados con diferentes versiones de módulos. {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Learning Manager no admite versiones de los módulos Actividad, Clase ni Clase virtual. Si proporciona versiones a través del archivo moduleVersion.csv, se actualiza el archivo existente en lugar de crear una nueva versión.

### La duración deseada no aparece para un módulo de clase/clase/actividad/clase migrado {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

La duración deseada no es una entrada válida para el módulo Actividad/VC/Clase.

### La URL de hipervínculo no se abre en el administrador de aprendizaje {#hyperlinkurldoesntopenupincaptivateprime}

Asegúrese de que los vínculos proporcionados estén prefijados con &#39;http://&#39; o &#39;https://&#39;

### La migración de moduleVersion falla con errores del tipo &quot;Archivo no encontrado&quot; {#moduleversionmigrationfailswithfilenotfounderrors}

Asegúrese de que el archivo al que se hace referencia esté presente en la carpeta de contenido y de que se haya migrado correctamente.

### La migración de moduleVersion falla con un mensaje de error como &quot;Se ha producido un error interno: para Module : x y moduleVersion : y&quot; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Vuelva a ejecutar el sprint para resolver el problema.
