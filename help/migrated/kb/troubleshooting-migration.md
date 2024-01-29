---
description: Este documento contiene sugerencias básicas de solución de problemas para resolver algunos de los problemas habituales que pueden producirse al migrar datos y contenido desde LMS existente a Learning Manager.
jcr-language: en_us
title: Solución de problemas de migración
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---



# Solución de problemas de migración

Este documento contiene sugerencias básicas de solución de problemas para resolver algunos de los problemas habituales que pueden producirse al migrar datos y contenido desde LMS existente a Learning Manager.

## Problemas de migración genéricos {#genericmigrationissues}

### No se puede iniciar sesión en la carpeta FTP o la carpeta de contenido {#unabletologintoftpfolderorcontentfolder}

Asegúrese de que sus cuentas se hayan creado en los servicios FTP y Box. Cuando crea un proyecto de migración, solicita configurar estos dos servicios. Tan pronto como cree los servicios, recibirá correos electrónicos de Exavault y Box para restablecer o configurar las contraseñas. Si no recuerda las contraseñas, puede restablecerlas visitando los sitios web de Exavault y Box.

### Los trabajos no se reflejan incluso después de hacer clic en el botón Actualizar {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Asegúrese de que los archivos CSV se carguen en la carpeta correcta en Exavault FTP. La estructura del trazado debe ser la siguiente:

`code Account>Project>Sprint location`

* Asegúrese de que los nombres de archivo de los archivos CSV se ajusten a los nombres de especificación de CSV:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Se muestran errores para trabajos con registros de error {#failuresareshownforjobswitherrorrecords}

1. Descargue los registros de errores haciendo clic en **Registros de errores de descarga** enlace
1. Corrija los archivos CSV originales en función de los errores notificados, y
1. Vuelva a ejecutar el sprint con los archivos CSV modificados.

La práctica recomendada es ejecutar archivos CSV modificados en un nuevo sprint cuando el número de cambios es menor que el número total de registros.

### No se puede iniciar sesión en la aplicación Learning Manager incluso después de detener la migración de sprint {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Pueden transcurrir entre 10 y 15 minutos hasta que se desbloquea una cuenta una vez que se detiene o completa una ejecución de Sprint. Intente acceder a la aplicación pasados 15 minutos.

### Algunos de los trabajos de migración muestran el estado &quot;En curso&quot; incluso después de que se active &quot;Detener&quot;. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Puede tardar entre 10 y 15 minutos en dejar de ejecutar todos los trabajos una vez que esté en el estado &quot;En curso&quot;. Vuelve a comprobar el estado después de 10 minutos.

### No se puede crear un sprint porque el botón está desactivado {#unabletocreateasprintasthebuttonisdisabled}

Asegúrese de que el sprint actual esté marcado como completado antes de crear un sprint. Haga clic en **[!UICONTROL Marcar sprint como completado]** en la parte superior de la página para completar una migración de Sprint.

### No se puede marcar un proyecto de migración como completado porque el botón está deshabilitado {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Asegúrese de que el sprint actual esté marcado como completado antes de marcar la finalización del proyecto de migración. Haga clic en **[!UICONTROL Marcar sprint como completado]** en la parte superior de la página para completar una migración de Sprint.

## Problemas de CSV {#csvissues}

### La migración del archivo module_version.csv falla y el contenido aún no se ha migrado {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Asegúrese de que el contenido esté disponible en la carpeta Contenido (cuenta de Box en el proyecto de migración especificado, ruta de sprint). Compruebe también que ha seleccionado la opción **Sí** para **¿Va a migrar contenido para este sprint?** pregunta en la página de creación de sprint.

Si olvida seleccionar **Sí** y continúe en este sprint, luego tendrá que esperar hasta que lo termine. Cree otro sprint y asegúrese de hacer clic **[!UICONTROL Sí]**.

### Los registros enrollment.csv o user_course_grade.csv fallan con el mensaje de error &quot;No es un ID de Learning Manager válido&quot; {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Asegúrese de que el ID de correo electrónico proporcionado como parte de los campos userId y assignedByUserID pertenezca a usuarios de Learning Manager válidos. Si no es así, añada el usuario y cree un nuevo sprint con **Sincronizar usuarios** opción seleccionada. Si el usuario no forma parte de la organización, añádalo como usuario eliminado en Learning Manager mediante la especificación CSV Añadir usuarios . A continuación se incluye una especificación de ejemplo de CSV para añadir usuarios eliminados como referencia.

[Users.csv](assets/users.zip) Consulte la **Especificaciones de CSV y ejemplos de CSV** sección en [Manual de migración](../integration-admin/feature-summary/migration-manual.md) para descargar un conjunto completo de especificaciones de CSV y archivos CSV de muestra.

### Los cursos aparecen en blanco o se reproducen módulos incorrectos para un curso migrado {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Asegúrese de que el **moduleOrderInCourse** valor clave para un curso que comienza por **0** y está en orden continuo. El orden en términos de courseModuleType debe ser PRETEST, TESTOUT, CONTENT

Además, asegúrese de que dos versiones de la actividad, la clase y la clase virtual no estén vinculadas al curso existente.

### Recepción de un mensaje como &quot;El módulo ya está vinculado a un curso existente&quot; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager no permite vincular el módulo Actividad/VC/Clase a más de un curso. Asegúrese de que el módulo no esté vinculado a ningún otro curso.

### Todos los cursos muestran la versión más reciente de los módulos Actividad/VC/Clase, aunque los cursos estén vinculados a diferentes versiones de módulos {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

El control de versiones de los módulos Actividad, Clase y Clase virtual no se admite en Learning Manager. Si proporciona versiones a través del archivo moduleVersion.csv, se actualiza el archivo existente en lugar de crear una nueva versión.

### La duración deseada no aparece para un módulo de clase/clase/actividad/clase migrado {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

La duración deseada no es una entrada válida para el módulo Actividad/VC/Clase.

### La URL de hipervínculo no se abre en el administrador de aprendizaje {#hyperlinkurldoesntopenupincaptivateprime}

Asegúrese de que los vínculos proporcionados estén prefijados con &#39;http://&#39; o &#39;https://&#39;

### La migración de moduleVersion falla con errores del tipo &quot;Archivo no encontrado&quot; {#moduleversionmigrationfailswithfilenotfounderrors}

Asegúrese de que el archivo al que se hace referencia esté presente en la carpeta de contenido y de que se haya migrado correctamente.

### La migración de moduleVersion falla con un mensaje de error como &quot;Se ha producido un error interno: para Module : x y moduleVersion : y&quot; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Vuelva a ejecutar el sprint para resolver el problema.
