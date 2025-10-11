---
description: Manual de referencia para administradores de integración que desean migrar un LMS existente a Adobe Learning Manager LMS.
jcr-language: en_us
title: Manual de migración
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: 3644e5d14cc5feaefefca85685648a899b406fce
workflow-type: tm+mt
source-wordcount: '3850'
ht-degree: 68%

---

# Manual de migración

Manual de referencia para los administradores de integración que desean migrar un LMS existente al LMS de Learning Manager

<!-- ## Overview {#overview} -->

## Escenario de uso {#usagescenario}

En general, las grandes empresas tienen su LMS interno u otros sistemas de gestión de aprendizaje heredados suministrados por un proveedor. El LMS consta de los datos y el contenido de formación de su empresa. Como empresa, al adquirir Learning Manager, es posible que desee mover los datos y el contenido del LMS existente a Learning Manager para poder aprovechar las ventajas del LMS moderno e intuitivo sin perder ninguno de los datos heredados de su organización.

Learning Manager ofrece las especificaciones y las herramientas necesarias para que el administrador de integración de su empresa pueda configurar y realizar las tareas de migración.

A partir de hoy, los administradores de una empresa pueden acceder a la función Migración en Learning Manager poniéndose en contacto con el equipo de asistencia de Adobe. Para activar la función Migración en su cuenta, puede ponerse en contacto con el equipo de asistencia de Adobe Learning Manager.

## Proceso de migración {#apidescription}

Los requisitos previos para la migración, los pasos clave involucrados en el proceso de migración, los sprints de migración, las especificaciones, los datos y los pasos de migración de contenido se explican en esta sección de la siguiente manera:

### Requisitos previos {#prerequisites}

El equipo de Learning Manager espera que los administradores de la integración de su empresa realicen las tareas siguientes antes de emprender el proceso de migración:

* El administrador de integración extrae los datos y el contenido del LMS en cuestión, y transforma los datos a los formatos de archivo definidos por Learning Manager.
* Learning Manager no admite la importación de usuarios como parte del proceso de migración y espera que la empresa importe los usuarios mediante conectores. Adobe Systems espera que estos conectores estén configurados antes del proceso de migración. Consulte [Ayuda de conectores de Learning Manager](connectors.md) para obtener más información.

Learning Manager recomienda que los administradores prueben el proceso de migración en una cuenta para tal efecto antes de migrar los datos y el contenido al entorno de producción de Learning Manager.

### Pasos clave del proceso de migración {#keystepsofmigrationprocess}

Estos son los pasos clave que conlleva la migración de contenido y datos de un LMS existente a Learning Manager:

1. El administrador o socio de integración evalúa los datos del LMS y el contenido que se debe migrar.
1. El administrador de integración evalúa las herramientas y especificaciones que proporciona Learning Manager para la ingesta de datos y contenido.
1. El administrador de integración escribe el código o realiza un trabajo manual para exportar los datos y el contenido de formación del LMS anterior basándose en la funcionalidad proporcionada por el LMS anterior.
1. Una vez que los datos y el contenido de formación están disponibles, el administrador de integración analiza y asigna los datos y el contenido para que coincidan con las especificaciones de migración de Learning Manager.
1. El administrador de integración utiliza las herramientas proporcionadas por Learning Manager para migrar en el siguiente orden:

   1. Transferir a los alumnos a Learning Manager.
   1. Transfiere contenido de formación a Learning Manager y
   1. Por último, transferir los datos de formación a Learning Manager.

La empresa puede empezar a utilizar el LMS de Learning Manager junto con el contenido heredado.

### Alcance de los objetos de la migración {#scopeofmigrationobjects}

Solo puede migrar contenido para los siguientes objetos de aprendizaje:

* Módulo
* Insignias
* Curso
* Versión del módulo
* Instancia del curso
* Módulo del curso
* Aptitudes
* Nivel de aptitud
* Curso de aptitudes
* Certificación
* Curso de certificación
* Confirmación de certificación
* Programa de aprendizaje
* Curso del programa de aprendizaje
* Instancia del programa de aprendizaje
* Instancia del curso del programa de aprendizaje
* Ayuda de trabajo
* Versión de ayuda de trabajo
* Curso de ayuda de trabajo
* Aptitudes de ayuda de trabajo
* Inscripción
* Inscripción de certificación
* Inscripción en el programa de aprendizaje
* Inscripción de ayuda de trabajo
* Calificaciones del curso del usuario

### Conceptos clave de la migración {#keyconceptsofmigration}

A continuación, se explican brevemente algunos de los conceptos clave del proceso de migración de Learning Manager para su referencia rápida:

**Proyecto de migración**

En Learning Manager, un proyecto de migración consiste en uno o más sprints. También puede tener varios proyectos de migración para su cuenta. El proceso de migración en Learning Manager comienza con la creación de un proyecto de migración.

**Sprint**

En el proceso de migración de Learning Manager, un sprint se define como un conjunto de elementos de migración que ha decidido migrar desde el LMS actual. Un elemento de migración puede ser un módulo de curso, registros de alumnos o un conjunto de cursos. Puede tener varios elementos de datos de aprendizaje en un sprint. En cada sprint, es posible ejecutar trabajos de migración.

**Ejecuciones de sprint**

Una ejecución de sprint es el proceso de iniciar un trabajo de migración de sprint. La ejecución de sprint en cualquier momento del proceso.

**Nuevas ejecuciones de sprint**

Puede volver a ejecutar un sprint de migración después de su finalización en cualquier momento. Esta situación de nueva ejecución o repetición de un sprint ocurre cuando desea agregar datos en un elemento de sprint y volverlo a migrar a la aplicación nuevamente o corregir los errores en CSV.

**Especificación en CSV**

Learning Manager proporciona un conjunto de [especificaciones CSV estándar](migration-manual.md#main-pars_header_140933605). El procedimiento recomendado es revisar estas especificaciones CSV antes de comenzar con el proceso de migración. El administrador de integración de su organización puede analizar los formatos de datos existentes y asignarlos para que coincidan con los elementos de plantilla CSV proporcionados por Learning Manager.

**Etiquetas del proyecto de migración**

Adobe Systems recomienda utilizar un conjunto de palabras clave como etiquetas para identificar fácilmente sus proyectos de migración dentro de la aplicación Learning Manager. Estas etiquetas le permiten identificar sus proyectos internamente en la aplicación Learning Manager en cualquier momento.

**Módulo sin contenido**

Learning Manager le permite cargar un módulo sin contenido. Adobe Systems lo considera un módulo sin contenido en Learning Manager. En un escenario en el que desee migrar algunos de los datos heredados de su LMS sin necesidad de ningún contenido, puede cargar el archivo module_version.csv sin referencia a la URL.

## Especificaciones y ejemplos de CSV {#csv}

A continuación, encontrará las especificaciones de CSV estándar que puede usar para correlacionar con los datos de migración de LMS. Haga clic en csv-specifications y sample-csvs para descargar los archivos zip. El archivo csv-specifications.zip descargado contiene siete archivos de hojas cálculo de Excel. Dichos archivos son especificaciones con descripciones para que comprenda cómo rellenar los archivos .csv. Los archivos .csv correspondientes deben contener los datos de cada campo en el formato prescrito tal como se explica en estos archivos .xlsx.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>N.º</b></p></th>
   <th>
    <p><b>Nombre de archivo</b></p></th>
   <th>
    <p><b>Descripción del contenido</b></p></th>
   <th>
    <p>Notas</p></th>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>module.xlsx</p></td>
   <td>
    <p>Metadatos para module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>badge.xlsx</p></td>
   <td>
    <p>Metadatos para badge.xlsx</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>course.xlsx</p></td>
   <td>
    <p>Metadatos para course.csv</p></td>
   <td>
    <p>Mencione un nombre de autor para un curso determinado, ya que a veces, si hay varios nombres de autor, no se muestran correctamente en la aplicación después de la migración. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Metadatos para module_version.csv</p></td>
   <td>
    <p>Proporcione la ruta URL de la carpeta de la cuenta de Box donde cargó el contenido. </p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>course_instance.xlsx</p></td>
   <td>
    <p>Metadatos para course_instance.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>session.xlsx</p></td>
   <td>
    <p>Metadatos para session.csv</p></td>
   <td>
    <p>Asegúrese de que cada entrada de session.csv esté asociada al menos con un módulo de clase/clase virtual</p></td>
  </tr>
  <tr>
   <td>
    <p>7</p></td>
   <td>
    <p>course_module.xlsx</p></td>
   <td>
    <p>Metadatos para course_module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>8</p></td>
   <td>
    <p>skill.xlsx</p></td>
   <td>
    <p>Metadatos para skill.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skill_level.xlsx</p></td>
   <td>
    <p>Metadatos para skill_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skill_course.xlsx</p></td>
   <td>
    <p>Metadatos para skill_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>11</p></td>
   <td>
    <p>certification.xlsx</p></td>
   <td>
    <p>Metadatos para Certification.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>12</p></td>
   <td>
    <p>certification_course.xlsx</p></td>
   <td>
    <p>Metadatos para certification_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>13</p></td>
   <td>
    <p>certification_commit.xlsx</p></td>
   <td>
    <p>Metadatos para certification_commit.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>14</p></td>
   <td>
    <p>learning_program.xlsx</p></td>
   <td>
    <p>Metadatos para learning_program.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>15</p></td>
   <td>
    <p>learning_program_course.xls </p></td>
   <td>
    <p>Metadatos para learning_program_course.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>16</p></td>
   <td>
    <p>learning_program_instance.xlsx </p></td>
   <td>
    <p>Metadatos para learning_program_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>17</p></td>
   <td>
    <p>learning_program_instance_course_instance.xlsx </p></td>
   <td>
    <p>Metadatos para learning_program_instance_course_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>18</p></td>
   <td>
    <p>job_aid.xlsx</p></td>
   <td>
    <p>Metadatos para job_aid.csv</p></td>
   <td>
    <p>Cada job_aid migrado debe tener una o más versiones de job_aid.</p></td>
  </tr>
  <tr>
   <td>
    <p>19</p></td>
   <td>
    <p>Job_aid_version.xlsx</p></td>
   <td>
    <p>Metadatos para job_aid_version.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>20</p></td>
   <td>
    <p>job_aid_course.xlsx</p></td>
   <td>
    <p>Metadatos para job_aid_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>21</p></td>
   <td>
    <p>job_aid_skills.xlsx</p></td>
   <td>
    <p>Metadatos para job_aid_skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>22</p></td>
   <td>
    <p>enrollments.xlsx</p></td>
   <td>
    <p>Metadatos para enrollments.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>23</p></td>
   <td>
    <p>certification_enrollement.xlsx</p></td>
   <td>
    <p>Metadatos para certification_enrollement.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>24</p></td>
   <td>
    <p>learning_program_enrollment.xlsx</p></td>
   <td>
    <p>Metadatos para learning_program_enrollment.csv<br><br></p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>25</p></td>
   <td>
    <p>job_aid_enrollment.xlsx</p></td>
   <td>
    <p>Metadatos para job_aid_enrollment.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>26</p></td>
   <td>
    <p>user_course_grade.xlsx</p></td>
   <td>
    <p><br>
      Metadatos para user_course_grade.csv</p></td>
   <td>
    <p>Proporcione los datos necesarios de registros de alumnos en el archivo .csv aunque no sean obligatorios. Sin esta información, aunque el archivo .csv se procese para la migración, es posible que la aplicación Learning Manager no refleje ningún dato. El archivo sample-csvs.zip contiene siete archivos .csv con una convención de nomenclatura similar a la anterior.</p></td>
  </tr>
  <tr>
   <td>
    <p>27</p></td>
   <td>
    <p>user_skill.xlsx</p></td>
   <td>
    <p><br>
      Metadatos para user_skill.csv</p></td>
   <td>
    <p> </p></td>
  </tr>
 </tbody>
</table>

Learning Manager admite valores de fecha y hora solo en formato UTF 8 y de 32 bits. Es posible que aparezcan errores durante la migración si menciona la fecha en archivos CSV con una fecha fuera de rango, como 2038-07-17T08:53:21.000Z o 1980-04-17T08:13:25.322Z.

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_specifications.zip](assets/csv-specifications.zip)

Debe tener en cuenta las siguientes dependencias en los archivos .csv durante la importación:

* module_version.csv depende de module.csv
* course_instance.csv depende de course.csv
* course_module.csv depende de course.csv, module.csv y module_version.csv
* course_instance.csv depende de course.csv
* session.csv depende de course.csv y module.csv
* enrollment.csv depende de course.csv
* user_course_grade.csv depende de course.csv y module.csv
* skill_course.csv depende de course.csv
* skill_level.csv depende de skill.csv
* learning_program_instance.csv depende de learning_program y learning_program_course.csv
* learning_program_course.csv depende de learning_program.csv
* learning_program_enrollment.csv depende de learning_program y learning_program_instance.csv
* learning_program_instance_course_instance.csv depende de learning_program.csv, learning_program_instance.csv y course_instance.csv.
* certification_course.csv depende de certification.csv y course.csv
* certification_commit.csv depende de certification.csv y certification_course.csv
* certification_enrollment.csv depende de certification.csv, certification_course.csv y certification_enrollment.csv

## Proceso de migración {#migrationprocedure}

Antes de comenzar con el procedimiento de migración, es importante tener en cuenta los siguientes puntos:

* Solo puede haber un proyecto de migración activo en una cuenta en cualquier momento dado. Dentro de un proyecto, solo puede haber un sprint activo en cualquier momento dado.
* No puede deshacer una ejecución que ya está en proceso de migración. Sin embargo, puede usar la opción de eliminación que hay dentro de cada función de Learning Manager para deshacer cualquier migración de datos o contenido.
* Tan pronto como se inicia el proyecto de migración, pasa al estado &quot;En proceso de migración&quot;. Durante la migración, la función de administrador de integración es la única que puede iniciar sesión en Learning Manager.

### Crear cuentas de FTP y Box {#creatingftpandboxaccounts}

Es muy importante planificar el proyecto de migración. Se recomienda dividir los proyectos en varios sprints e identificar claramente lo que se desea migrar en cada sprint. Incluso puede ser buena idea hacer una validación después de cada sprint para tener seguridad sobre los datos migrados en ese sprint, en lugar de una validación a gran escala al final del proyecto. Antes de comenzar el sprint como parte del proyecto de migración, debe cargar archivos CSV de datos y contenido en servidores de FTP y Box, respectivamente. Si no tiene cuentas para FTP y Box personalizados, puede crearlas.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Crear una cuenta de Box**

Cree una carpeta de carga de contenido en un proceso similar al de la creación de la carpeta FTP. Haga clic en Migración en el panel izquierdo; a continuación, haga clic en Solicitar una carpeta de carga de contenido en la parte inferior de la página que se abre.

Recibirá un correo de Box con un vínculo a la carpeta compartida. Si no tiene ninguna cuenta de Box, haga clic en Registrar y cree una. Las instrucciones de inicio de sesión se envían al ID de correo electrónico del administrador de la integración.

**Cargar datos (archivos .csv) en carpetas de FTP o de Box**

Crear una cuenta de FTP o de Box es un requisito previo para la creación de un proyecto de migración. Por lo tanto, en esta fase puede crear un proyecto de migración y un sprint en la aplicación Learning Manager.  Consulte la sección **Procedimiento de migración de datos y contenido** de esta página para crear el proyecto de migración.

En la cuenta de FTP o de Box, haga clic en el nombre de la carpeta del proyecto y haga clic en el nombre del sprint. Dentro de la carpeta de sprints, puede cargar los archivos de datos .csv que desea migrar. Para cargar, haga clic en el botón Cargar archivos en la parte superior del servidor FTP o Box y suelte los archivos .csv. A continuación se muestra una captura de pantalla de ejemplo después de cargarla en FTP como referencia.

<!--![](assets/exavault-upload.png)-->

Puede volver al proyecto de migración de Learning Manager, hacer clic en **[!UICONTROL Actualizar]** y ver todos los tipos de datos .csv que se enumeran para el sprint de migración.

**Cargar contenido de formación en las carpetas de contenido**

Suba el contenido de formación del LMS a su cuenta de Box. Si ya ha creado el proyecto de migración y el sprint, la cuenta de Box rellena el proyecto de migración y el nombre de sprint. Puede cargar el contenido en la misma ruta. Consulte la sección **Procedimiento de migración de datos y contenido** de esta página para crear el proyecto de migración.

Puede arrastrar y soltar los archivos de contenido, o bien hacer clic en **[!UICONTROL Cargar]** y seleccionar los archivos en el escritorio. Si el tamaño del archivo de su contenido es muy grande, puede experimentar algún retraso en la carga de los archivos. Según el tamaño del archivo, el tiempo que se tarda en cargar los archivos en la cuenta de Box varía.

A continuación se muestra una captura de pantalla de la cuenta de Box después de cargar contenido para su referencia:

![](assets/box-account.png)

*Archivos en la cuenta de Box*

Una vez que los archivos se cargan en su cuenta de Box, asegúrese de mencionar la ruta relativa de este archivo de contenido de Box en el archivo module_version.csv. Es un paso obligatorio para que indique la ruta del contenido del módulo.

Después de iniciar sesión en los servidores de FTP y Box y de cargar el contenido, las ubicaciones de CSV aparecen como se muestra en la captura siguiente en Learning Manager.

![](assets/after-setup.jpg)

*Ubicaciones CSV en la cuenta de Box*

## Procedimiento de migración de datos y contenido {#dataandcontentmigrationprocedure}

El procedimiento para migrar los datos y el contenido del LMS empresarial a Learning Manager se explica a continuación:

Revise los requisitos previos del proceso de migración antes de comenzar con la migración. Consulta la sección [Especificaciones de CSV y ejemplos de CSV](migration-manual.md#main-pars_header_140933605) en esta página y prepara los CSV para la migración de datos y contenido.

1. Inicie sesión en la aplicación Learning Manager como administrador de integración y haga clic en **[!UICONTROL Migración]** en el panel izquierdo.

   Aparece la página de inicio de los proyectos de migración. Si su empresa ya ha creado proyectos de migración, puede ver la lista de todos los proyectos de migración en esta página.

1. Haga clic en **[!UICONTROL Nuevo]** en la esquina superior derecha de la página para crear un proyecto de migración. También puede hacer clic en el vínculo **[!UICONTROL Crear un proyecto de migración]** en la página para crear un proyecto de migración. Aparece la página Crear un proyecto de migración.

   Si aún no ha creado una carpeta FTP, se le pedirá que cree una carpeta FTP en la cuenta. Es un paso obligatorio para poder crear un proyecto de migración.

   ![](assets/create-project.png)
   *Crear carpeta FTP*

   Proporcione el nombre del proyecto, la etiqueta del proyecto, el catálogo del curso y la descripción de su proyecto de migración. Haga clic en **[!UICONTROL Crear]**.

   Los elementos de datos de migración se identifican utilizando esta etiqueta de proyecto de migración. Si no tiene ningún catálogo de cursos concreto, elija el catálogo predeterminado en el menú desplegable. Todos los cursos que migre utilizando un proyecto de migración se incluirán en el catálogo que elija en esta etapa. Si no elige ningún catálogo, todos los cursos migrados serán parte del catálogo predeterminado.

1. La página de configuración de sprints aparece como se muestra en la siguiente captura de pantalla. Debe crear un sprint como parte del proyecto de migración. Seleccione el nombre de sprint y escriba una breve descripción. Puede elegir Sí para migrar contenido como parte de este sprint. Haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/users-modified-sprint.png)
   *Migración de sprint*

   Seleccione la casilla de verificación con el título **Se han agregado o modificado usuarios desde la última ejecución** para sincronizar la lista de usuarios con la aplicación de Learning Manager. Si está migrando el contenido y los datos a la aplicación Learning Manager, esto quizá no sea necesario. Sin embargo, si transcurre un tiempo entre la migración de sprints anterior y la última, se recomienda sincronizar la lista de usuarios. Este paso permite que la base de datos de Learning Manager esté sincronizada con los usuarios del LMS.

   Se recomienda realizar este paso de sincronización cuando se migran enrollment.csv y user_course_grade.csv. Este paso permite que la base de datos de Learning Manager esté sincronizada con su base de datos de migración y garantiza que todos los usuarios cuyos registros para migrar al sprint estén disponibles en la base de datos de migración.

1. Puede comenzar la migración del sprint con los datos y el contenido que ha cargado. Haga clic en el vínculo **[!UICONTROL Actualizar]** antes de iniciar la ejecución del sprint para sincronizar las carpetas de FTP y contenido con la aplicación Learning Manager.

   ![](assets/sprint1-filesupload.png)
   *Iniciar migración de sprint*

   Haga clic en **[!UICONTROL Inicio]** en la esquina superior derecha de la página. Puede hacer clic en **[!UICONTROL Detener]** en cualquier momento durante el proceso de migración del sprint para anular la migración del sprint.

   El estado de la migración se muestra en cada elemento y contenido de los datos del sprint. Compruebe la cantidad de elementos correctos y fallidos como parte de la ejecución del sprint de migración.

   Si está cargando contenido del módulo, asegúrese de que la ruta de la carpeta de contenido esté indicada en module_version.csv. Si olvida este paso, puede recibir errores durante la migración. Por ejemplo, si está cargando contenido de un módulo con ritmo personalizado, por ejemplo vídeos, debe especificar la ruta relativa de la URL de Box en module_version.csv. Para el contenido del módulo de actividad, puede especificar el nombre de la URL.

   A continuación se proporciona una captura de pantalla de ejemplo del cuadro de diálogo de progreso. Como se muestra en la captura, puede ver el número de registros procesados para cada elemento de datos de migración, junto con el estado de elementos correctos y fallidos. Haga clic en Descargar registros de errores para los elementos fallidos a fin de descargar y ver los registros de errores. Puede solucionar los errores en CSV y cargarlos de nuevo en FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Ver progreso de sprint*

   Haga clic en la lista de sprints en el panel izquierdo para ver la lista de todos los sprints de un proyecto de migración. Puede ver una lista de todos los sprints, el número de ejecuciones que ejecutó para cada sprint, la fecha de inicio, la duración y el estado de finalización, como se muestra en la captura de pantalla de ejemplo a continuación.

   ![](assets/sprint-list.png)
   *Ver lista de sprints*

1. Después de cargar los últimos archivos .csv actualizados, puede hacer clic en Volver a ejecutar en la esquina superior derecha de la página. La nueva ejecución vuelve a procesar todos los elementos de datos y omite los elementos en los que no se haya realizado ningún cambio. Cuando esté satisfecho con la migración de los elementos de datos en un sprint, marque la migración del sprint como completada haciendo clic en el botón en la parte superior de la página. Puede comenzar un nuevo sprint con más elementos de datos más adelante. Una vez marcado un sprint como completado, no es posible volver a ejecutarlo. Asimismo, en un proyecto de migración puede tener cualquier cantidad de sprints. Una vez que esté satisfecho con el estado de migración de todos los sprints, puede marcar el proyecto de migración como completado haciendo clic en el vínculo **Marcar proyecto completado** en la página Lista de sprints.

   Antes de marcar el proyecto de migración como completado, debe asegurarse de haber completado todos los sprints del proyecto. Una vez que haya marcado el proyecto de migración como completado, no podrá volver atrás, crear sprints en dicho proyecto ni realizar modificaciones en él. Deberá crear otro proyecto de migración y añadirle sprints.

## Verificación de la migración {#registration}

Después de migrar los datos y el contenido de aprendizaje del LMS heredado de la empresa, puede verificar dichos datos y contenido importados utilizando diferentes funciones de los objetos de aprendizaje. Por ejemplo, puede iniciar sesión en la aplicación Learning Manager como administrador y verificar la disponibilidad de los datos y el contenido de los cursos y módulos importados.

### Verificación de la migración mediante API

Una nueva API de migración, `runStatus`, permite a los administradores de integración realizar un seguimiento del progreso de las ejecuciones de migración desencadenadas a través de la API.

La API `runStatus` también proporciona un vínculo directo para descargar registros de errores en formato CSV para las ejecuciones completadas. El vínculo de descarga permanece activo durante siete días y los registros se conservan durante un mes.

**Curl de muestra**

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

Además, la respuesta de API `startRun` ahora incluye el id. del proyecto de migración, el id. de sprint y el id. de ejecución de sprint, que son necesarios para consultar el nuevo extremo de estado.

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

## Readaptación de la migración {#retrofittinginmigration}

Esta función de integración le permite adaptar datos históricos para un objeto de aprendizaje de un sistema de gestión de aprendizaje antiguo a un curso activo que se crea en Learning Manager.

A continuación, encontrará las especificaciones de CSV estándar que puede usar para correlacionar con los datos de migración de LMS. Haga clic en csv-specifications y sample-csvs para descargar los archivos zip. El archivo csv-specifications.zip descargado contiene cuarto archivos de hojas de cálculo de Excel. Dichos archivos son especificaciones con descripciones para que comprenda cómo rellenar los archivos .csv. Los archivos .csv correspondientes deben contener los datos de cada campo en el formato prescrito tal como se explica en estos archivos .xlsx.

1-enrollment.xlsx-contiene descripciones de los metadatos requeridos para el archivo retrofit_enrollment.csv.

2-certification_enrollment.xlsx-contiene descripciones de los metadatos requeridos para el archivo retrofit_certification_enrollment.csv.

3-learning_program_enrollment.xlsx-contiene descripciones de los metadatos requeridos para el archivo retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-contiene descripciones de los metadatos necesarios para el archivo retrofit_user_course_grades.csv.
[csv-specifications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>El UUID (Universally Unique Id) también es una columna en el archivo .csv de migración.


## Solución de problemas de migración {#troubleshootingmigrationissues}

Consulte este [artículo](../../kb/troubleshooting-migration.md) para obtener información sobre la solución a los problemas a los que se enfrentan los administradores de integración al migrar datos y contenido de su LMS existente a la aplicación Learning Manager.

## Consejos para la administración de usuarios {#usermanagement}

En este tema, encontrará algunos consejos para comprender cómo se consideran y administran los usuarios en Learning Manager. Estos conceptos le ayudarán a administrar mejor los usuarios utilizando la importación de CSV, los conectores y las funciones de migración de Learning Manager.

## ID de Learning Manager {#captivateprimeids}

Learning Manager proporciona dos tipos de ID únicos para los usuarios:

* ID de correo electrónico
* UUID (identificador único universal)

Learning Manager admite UUID para ofrecer flexibilidad a las empresas en el control de las cuentas de usuarios. Como administrador, si tiene un UUID de usuarios en una cuenta, puede modificar los ID de correo electrónico de los usuarios de esa cuenta.

**Escenario de uso de UUID en una empresa**

Supongamos que un empleado A se une a una empresa denominada Learning Manager como contratista. Durante el período de contrato, es posible que la empresa de Learning Manager no proporcione el ID de correo electrónico de la empresa como ```A@example.com```. En su lugar, la empresa puede considerar solo la cuenta de correo electrónico personal del empleado, por ejemplo, ```A@gmail.com```. Después de completar 6 meses del período de contrato, si el mismo empleado A se une a Learning Manager como empleado a tiempo completo, es posible que Learning Manager desee cambiar su ID de correo electrónico a su ID de correo electrónico de empresa: ```A@example.com```.

Tener acceso UUID a la cuenta de usuario beneficiará a la empresa Learning Manager en el escenario mencionado anteriormente. La empresa de Learning Manager puede sustituir fácilmente el ID de correo electrónico personal del empleado A por un ID de correo electrónico oficial. Este cambio no afectará a los registros del empleado correspondientes a esta cuenta.

## Identificación de usuario único {#singleuseridentification}

Learning Manager identifica y recuerda cómo se le añade un usuario único, por ejemplo mediante el registro automático, cargando un archivo .csv o añadiendo un solo usuario mediante la interfaz de usuario o una API.

* Si se añade un solo usuario mediante la interfaz de usuario (IU) o una API, puede eliminar ese tipo de usuarios individuales mediante la interfaz de usuario o la API.
* Puede actualizar usuarios individuales utilizando el proceso de carga de CSV, pero debe recordar que estos usuarios únicos se tratan como usuarios CSV y se aplican los flujos de trabajo CSV a dichos usuarios.

## Asignar la función de responsable {#assigningmanagerrole}

No puede asignar una función de responsable directamente a ningún usuario en Learning Manager. Un usuario X puede convertirse en administrador de aprendizaje solo cuando se establece un atributo de administrador de cualquier usuario (por ejemplo, Y) de esa cuenta como X.

En el supuesto de que X es el responsable de los usuarios, por ejemplo A, B y C, si X abandona la empresa, debe asegurarse de que el atributo Responsable de A, B y C esté configurado en el nuevo responsable. Una alternativa es establecer el atributo Responsable de estos usuarios como ROOT temporalmente y asignar el nuevo nombre de responsable más adelante.

Para obtener más información sobre este tema, consulte el siguiente contenido de la Ayuda:

* [Preguntas más frecuentes sobre la carga de CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md#bulk-upload-internal-users/)
* [Ayuda sobre la función de añadir usuarios](/help/migrated/administrators/feature-summary/add-users-user-groups.md)
