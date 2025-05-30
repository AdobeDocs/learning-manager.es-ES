---
description: Obtenga información sobre cómo integrar Salesforce con Learning Manager mediante conectores, cómo integrar FTP con Learning Manager y cargar el archivo .csv automáticamente mediante el conector de FTP.
jcr-language: en_us
title: Conectores de Learning Manager
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '6293'
ht-degree: 72%

---



# Conectores de Learning Manager

Obtenga información sobre cómo integrar Salesforce con Learning Manager mediante conectores, cómo integrar FTP con Learning Manager y cargar el archivo .csv automáticamente mediante el conector de FTP.

Las empresas tienen otras aplicaciones y sistemas que pueden necesitar integrar con Learning Manager. Los conectores son utilidades que ayudan a realizar integraciones basadas en datos, como importar datos en Learning Manager desde sistemas externos o exportar datos a sistemas externos desde Learning Manager. En la versión de julio de 2016, los conectores solo tienen la capacidad de importar usuarios en bloque para Learning Manager desde sistemas externos.

Learning Manager ofrece conectores de Salesforce y FTP. Con el conector de Salesforce, los administradores de integración de una empresa integran su aplicación Salesforce con Learning Manager. En calidad de integrador, el conector de FTP también puede utilizarse para importar automáticamente un conjunto de usuarios en la aplicación empresarial.

Learning Manager también proporciona los conectores de Lynda, getAbstract y Harvard Management System, que permiten a los alumnos acceder y consumir cursos de Lynda.com, getAbstract y Harvard ManageMentor, respectivamente.

Siga leyendo para saber cómo configurar y usar cada uno de estos conectores en Learning Manager.

![](assets/connectorslist.jpg)

## Conector de Salesforce {#sfconnector}

El conector de Salesforce conecta las cuentas de Learning Manager y Salesforce para automatizar la sincronización de datos. Las funciones del conector de Salesforce son las siguientes:

### Asignación de atributos

El administrador de integración puede seleccionar columnas de Salesforce y asignarlas a los correspondientes atributos agrupables de Learning Manager. Es una acción que se efectúa una sola vez. Tras finalizar la asignación, la misma asignación se aplica en las posteriores importaciones de usuarios. Se puede volver a configurar si el administrador quiere otra asignación para importar usuarios.

### Importación automatizada de usuarios

El proceso de importación de usuarios permite que el administrador de Learning Manager obtenga datos de los usuarios de Salesforce y los importe automáticamente a Learning Manager. Esta automatización evita la creación y la carga manuales del archivo .csv en Learning Manager.

### Programación automática

El uso de la programación automática junto con la importación automática de usuarios puede ser eficaz. El administrador de Learning Manager puede configurar la programación conforme a los requisitos de la empresa. Los usuarios de la aplicación Learning Manager pueden estar actualizados según la programación. La sincronización se puede realizar a diario en la aplicación Learning Manager.

### Filtrar usuarios

El administrador de Learning Manager puede aplicar filtros en los usuarios antes de importarlos. Por ejemplo, el administrador de Learning Manager puede optar por importar todos los usuarios en la jerarquía bajo uno o más responsables específicos.

## Configurar el conector de Salesforce {#configuresalesforceconnector}

Obtenga información sobre el proceso de integrar Learning Manager con Salesforce.

### Requisitos previos {#prerequisites}

Compruebe que disponga de la URL de la empresa de Salesforce. Por ejemplo, si su empresa se llama **myorg**, la URL de Salesforce podría ser [https://myorg.salesforce.com](https://myorg.salesforce.com/). Es lo único que debe indicarse para conectar la cuenta de Salesforce con Learning Manager.

Asimismo, compruebe que tenga las credenciales adecuadas para iniciar sesión en la cuenta.

## Crear una conexión {#createaconnection}

1. En la página principal de Learning Manager, coloque el cursor sobre la tarjeta/miniatura de Salesforce. Aparece un menú. Haga clic en la opción **[!UICONTROL Conectar]** del menú.

   ![](assets/mouserover-salesforce.png)

1. Un cuadro de diálogo le solicita la URL de la empresa. Haga clic en **[!UICONTROL Conectar]** después de proporcionar la dirección URL.
1. Tras conectarse correctamente, aparece la página de información general.

## Asignación de atributos {#mapattributes}

Una vez que la conexión se establece correctamente, puede asignar columnas de Salesforce a los atributos correspondientes de Learning Manager. Este paso es obligatorio.

1. En la página de asignaciones, en el lado izquierdo se muestran las columnas de Learning Manager y en el derecho, las de Salesforce. Seleccione el nombre de columna adecuado que corresponda al nombre de columna del administrador de aprendizaje.

   ![](assets/sfdc-map-columns.png)

   Los datos de columna de Learning Manager que se muestran a la izquierda se obtienen de los campos activos. El campo **manager** debe asignarse necesariamente a un campo de tipo de dirección de correo electrónico. Asignar todas las columnas es obligatorio antes de poder usar el conector.

1. Haga clic en **[!UICONTROL Guardar]** después de completar la asignación.
1. El conector ya está listo para utilizarse. La cuenta que se ha configurado ahora aparece como una fuente de datos dentro de la aplicación del administrador, para que el administrador programe la importación o la sincronización a petición.

## Uso del conector de Salesforce {#usingsalesforceconnector}

El conector de Salesforce se conecta a Salesforce.com para buscar a los usuarios según su configuración y añadirlos a Learning Manager.

## Conector FTP de Learning Manager {#ftpconnector}

Con el conector de FTP, es posible integrar Learning Manager con sistemas externos arbitrarios para automatizar la sincronización de datos. En principio, los sistemas externos pueden exportar datos en formato CSV y colocarlos en la carpeta apropiada de la cuenta de FTP de Learning Manager. Las funciones del conector de FTP son las siguientes:

También puede utilizar el conector de Box para la migración de datos, la importación de usuarios y la exportación de datos. Para obtener más información, consulte [Conector de Box.](third-party-connectors.md#main-pars_header_302653946)

## Importación de datos {#dataimport}

El proceso de importación de usuarios permite que el administrador de Learning Manager obtenga datos del servicio de FTP de Learning Manager y los importe automáticamente a Learning Manager. Esta función permite integrar varios sistemas colocando el archivo .csv generado por dichos sistemas en las carpetas correspondientes de las cuentas de FTP. Learning Manager recopila los archivos .csv, los combina e importa los datos conforme a la programación. Consulte la función Programación para obtener más información.

**Asignación de atributos**

El administrador de integración puede seleccionar las columnas del archivo .csv y asignarlas a los atributos agrupables de Learning Manager. Esta asignación es una acción que se efectúa una sola vez. Tras finalizar la asignación, la misma asignación se aplica en las posteriores importaciones de usuarios. La asignación se puede volver a configurar si el administrador desea tener una asignación diferente para importar usuarios.

## Exportación de datos {#exportdata}

La opción Exportación de datos permite exportar aptitudes de usuarios a una ubicación de FTP para su integración con cualquier otro sistema de terceros.

## Programación {#scheduling}

El usuario puede configurar tareas de programación conforme a los requisitos de la empresa y los usuarios de Learning Manager están al día según la programación. Asimismo, el administrador de integración puede programar la exportación de aptitudes de manera oportuna para integrarse con un sistema externo. La sincronización se puede realizar a diario en la aplicación Learning Manager.

## Configurar el conector FTP de Learning Manager {#configurecaptivateprimeftpconnector}

Obtenga información sobre el proceso de integrar Learning Manager con el conector de FTP.

### Crear una conexión {#Createaconnection-1}

1. En la página principal de Learning Manager, coloque el cursor sobre la tarjeta/miniatura de FTP. Aparece un menú. Haga clic en la opción **[!UICONTROL Conectar]** del menú.

   ![](assets/mouseover-ftpconnector.png)

1. Un cuadro de diálogo le solicita el ID de correo electrónico. Indique el ID de correo electrónico de la persona responsable de administrar la cuenta de FTP de Learning Manager para la organización. Haga clic en **[!UICONTROL Conectar]** después de proporcionar el ID de correo electrónico.
1. Learning Manager le envía un mensaje de correo electrónico solicitando al usuario que restablezca la contraseña antes de acceder al FTP por primera vez. El usuario debe restablecer la contraseña y usarla para acceder a la cuenta de FTP de Learning Manager.

   Solo se puede crear una cuenta de FTP de Learning Manager para una determinada cuenta de Learning Manager.

   En la página de información general, puede especificar el nombre de conexión de su integración. Elija la acción que desea efectuar de las siguientes opciones:

   * Importar usuarios internos
   * Exportar usuarios externos: Configurar una programación
   * Exportar usuarios externos: A petición

   ![](assets/connectors-overview.png)

## Importar

+++Usuario interno

La opción de importación de usuarios internos le permite programar la generación del informe de importación de usuarios automáticamente. Los informes que se generan se le envían como archivos .csv.

+++

+++Asignar atributos

Una vez que la conexión se establece correctamente, puede asignar columnas de archivos .csv que se colocarán en la carpeta FTP para los atributos correspondientes de Learning Manager. Este paso es obligatorio.

1. En la página Asignar atributos, en el lado izquierdo, se muestran las columnas esperadas de Learning Manager, mientras que en el derecho, se muestran los nombres de las columnas de CSV. Al principio, en el lado derecho, hay un cuadro de selección vacío. Importe cualquier archivo .csv de plantilla haciendo clic en **Elegir archivo**.
1. El paso anterior rellena la lista desplegable seleccionada de la derecha con todos los nombres de columnas de CSV. Seleccione el nombre de columna adecuado que corresponda al nombre de columna del administrador de aprendizaje.

   *El campo de responsable debe asignarse necesariamente a un campo de tipo de dirección de correo electrónico. Asignar todas las columnas es obligatorio antes de poder usar el conector.*

1. Haga clic en **[!UICONTROL Guardar]** después de completar la asignación.

   El conector ya está listo para utilizarse. La cuenta que se ha configurado ahora aparece como una fuente de datos dentro de la aplicación del administrador, para que el administrador programe la importación o la sincronización a petición.



+++

+++Uso del conector FTP de Learning Manager

1. Los archivos CSV de sistemas externos deben colocarse en la ruta siguiente:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Nota:** En la versión de julio de 2016, solo se permite la importación de usuarios. Por lo tanto, para utilizar el conector de FTP, debe asegurarse de que los archivos CSV se coloquen en la carpeta siguiente:

   `code Home/import/user/internal/*.csv`

1. El conector de FTP toma todas las filas de los archivos CSV, por lo que es importante que la fila correspondiente a un usuario en un archivo CSV no aparezca en ningún otro archivo CSV.
1. Todos los archivos CSV deben contener las columnas especificadas en la asignación.
1. Todos los archivos CSV necesarios deben estar presentes en la carpeta antes de que comience el proceso.

Al importar usuarios a Learning Manager, el administrador también necesita saber cómo se administran los usuarios en Learning Manager. Consulte [Ayuda de administración de usuarios](../integration-admin/feature-summary/migration-manual.md#usermanagement) para obtener más información.

+++

## Exportar

+++Aptitudes

Existen dos opciones para exportar informes de aptitudes de usuarios.

**[!UICONTROL Aptitudes del usuario: a petición]**: puede especificar la fecha de inicio y exportar el informe usando la opción. El informe se extraerá desde la fecha especificada hasta el presente.

![](assets/user-skills-on-demand.png)

**[!UICONTROL Aptitudes del usuario: Configurar]**: esta opción le permite programar la extracción del informe. Seleccione la casilla de verificación Activar programación y especifique la fecha y la hora de inicio. También puede especificar el intervalo en el que desea que se genere y se envíe el informe.

![](assets/user-skills-configure.png)

+++

Para abrir la carpeta Export donde se colocarán los archivos exportados en la ubicación del FTP, abra el vínculo a la carpeta de FTP que se proporciona en la página Aptitudes del usuario, como se muestra a continuación.

![](assets/ftp-folder.png)

Los archivos exportados automáticamente estarán presentes en la ubicación **Home/export/&#42;ubicación_FTP&#42;**

Los archivos exportados automáticamente estarán disponibles con el título **skill_achievements_&#42;date from &#42;_to_&#42;date to&#42;.csv**

![](assets/exported-csvs.png)

## Conector de Lynda {#lyndaconnector}

El conector Lynda puede ser válido para clientes empresariales de Lynda.com que desean que sus alumnos descubran y consuman cursos de Lynda desde Learning Manager. El conector se puede configurar para obtener cursos de Lynda.com de manera periódica con la clave de API. Después de crear un curso en Learning Manager, los usuarios lo pueden buscar y consumir. Después, se puede seguir el progreso del alumno desde Learning Manager.

### Configurar el conector de Lynda {#configurethelyndaconnector}

1. En el tablero del administrador de integración, haga clic en Lynda.

   Verá el mosaico con tres opciones: Introducción, Connect y Administrar conexiones.

1. Si configura el conector de Lynda por primera vez, haga clic en Conectar.

   Debe configurar la cuenta de FTP de Exavault antes de configurar este conector.

1. En la página de conexión, especifique un nombre para el conector. Indique la Appkey y la clave secreta de la conexión.

   Póngase en contacto con su proveedor para obtener Appkey y la clave secreta.

1. Haga clic en Guardar.

   La configuración se guarda y se agrega la conexión de Lynda para su cuenta. Ahora puede hacer clic en Administrar conexiones en la página Inicio y editar su configuración en cualquier momento.

1. Si ya tiene una conexión establecida, haga clic en Administrar conexiones para ver todas sus conexiones.

   La función de migración debe estar habilitada para su cuenta antes de configurar este conector.

1. Haga clic en la conexión que desea editar.
1. En el panel izquierdo, haga clic en Configurar. Elija una de las opciones siguientes:

   * Vea o edite los detalles de su cuenta y el calendario de sincronización desde esta ventana. Debe seleccionar la casilla de verificación Habilitar conexión si desea habilitar esta cuenta.
   * Haga clic en Editar y edite sus credenciales. Haga clic en Restablecer para deshacer sus actualizaciones en este campo.
   * Haga clic en Habilitar programación para programar su sincronización. Puede indicar la hora y la fecha de inicio; a continuación, especifique ingresar la frecuencia de su programa de sincronización en días. Por ejemplo, habilite la sincronización cada 3 días.

   Haga clic en Guardar para guardar sus cambios.

   ![](assets/lynda.png)

1. En el panel izquierdo, haga clic en Ejecución a petición. Esta opción le permite importar fuentes de usuario y otros datos relevantes de Lynda. Indique la fecha de inicio para la ejecución a petición y haga clic en Ejecutar para ejecutar la sincronización. Se importan todos los datos desde la fecha de inicio hasta el presente.

   * Puede hacer clic en Deshabilitar acceso a Learning Manager durante la ejecución en la que la aplicación tendrá un tiempo de inactividad durante la sincronización.
   * Si hace clic en Habilitar acceso a Learning Manager durante la ejecución, no hay interrupción en el servicio durante la sincronización.

   ![](assets/lynda-ondemand.png)

1. También puede hacer clic en Estado de la ejecución en el panel izquierdo en cualquier momento para ver el resumen de todas las ejecuciones de este conector, en orden cronológico. Puede ver la fecha de inicio y la duración de la sincronización, el tipo de sincronización (si se trata de sincronización a petición) y el estado de la sincronización (si la sincronización está en curso o está completa).

   Cuando elimina y vuelve a crear una conexión, vuelven a aparecer las ejecuciones anteriores del conector. Puede ver todas las ejecuciones antes de eliminar la conexión.

   Puede repetir una ejecución solo de la última sincronización.

   ![](assets/lynda-executionstatus.png)

## Conector de getAbstract {#getabstractconnector}

El conector de getAbstract es válido para clientes empresariales de getAbstract.com que desean que sus alumnos descubran y consuman cursos de getAbstract. El conector se puede configurar para obtener datos de uso de manera periódica en función de los registros de finalización de alumno que se creen en Learning Manager. Siga leyendo para saber cómo configurar y usar este conector en Learning Manager.

### Configurar el conector de getAbstract {#configurethegetabstractconnector}

1. En el tablero del administrador de integración, haga clic en getAbstract.

   En el mosaico, verá tres opciones: Introducción, Connect y Administrar conexiones.

1. Si configura el conector de getAbstract por primera vez, haga clic en Conectar.

   Debe configurar la cuenta de FTP de Exavault antes de configurar este conector.

   Asegúrese de compartir estas credenciales de FTP con su proveedor de contenido para acceder a las fuentes.

1. En el campo Nombre de conexión, asigne un nombre a la conexión.

   Indique las claves pertinentes en los campos ID y Secreto de cliente. Quizá deba ponerse en contacto con su proveedor para obtener las claves adecuadas para este conector.

   Las claves son necesarias para obtener los metadatos de curso para los cursos consumidos por el cliente.

1. Si ya tiene una conexión establecida, en la página de inicio, haga clic en getAbstract > Administrar conexiones para ver y editar su configuración.

   La función de migración debe estar habilitada para su cuenta antes de configurar este conector.

1. Haga clic en la conexión cuya configuración desea ver o editar.

   ![](assets/getabstractschedulepage.png)

1. En el panel izquierdo, haga clic en Configurar. Elija una de las opciones siguientes:

   * Vea o edite los detalles de su cuenta y el calendario de sincronización desde esta ventana. Debe seleccionar la casilla de verificación Habilitar conexión si desea habilitar esta cuenta.
   * Haga clic en Editar y edite sus credenciales. Haga clic en Restablecer para deshacer sus actualizaciones en este campo.
   * Haga clic en Habilitar programación para programar su sincronización. Puede indicar la hora y la fecha de inicio; a continuación, especifique ingresar la frecuencia de su programa de sincronización en días. Por ejemplo, habilite la sincronización cada 3 días.

1. Haga clic en Guardar.

   La configuración se guarda y se agrega la conexión de getAbstract para su cuenta.

1. En el panel izquierdo, haga clic en Ejecución a petición. Esta opción le permite importar fuentes de usuario y otros datos relevantes de getAbstract. Indique la fecha de inicio para la ejecución a petición y haga clic en Ejecutar para ejecutar la sincronización. Se importan todos los datos desde la fecha de inicio hasta el presente.

   * Puede hacer clic en Deshabilitar acceso a Learning Manager durante la ejecución en la que la aplicación tendrá un tiempo de inactividad durante la sincronización.
   * Si hace clic en Habilitar acceso a Learning Manager durante la ejecución, no hay interrupción en el servicio durante la sincronización.

1. También puede hacer clic en Estado de la ejecución en el panel izquierdo en cualquier momento para ver el resumen de todas las ejecuciones de este conector, en orden cronológico. Puede ver la fecha de inicio y la duración de la sincronización, el tipo de sincronización (si se trata de sincronización a petición) y el estado de la sincronización (si la sincronización está en curso o está completa).

   Cuando elimina y vuelve a crear una conexión, vuelven a aparecer las ejecuciones anteriores del conector. Puede ver todas las ejecuciones antes de eliminar la conexión.

   Puede repetir una ejecución solo de la última sincronización.

   Para que funcione cualquier tipo de sincronización, debe asegurarse de que la fuente del usuario esté presente en la carpeta FTP de getAbstract para las fechas especificadas en la sincronización.

   Consulte la siguiente hoja de Excel, que es un archivo de fuente de usuario de muestra de getAbstract. El nombre del archivo debe tener el formato:**&#x200B; report_export_yyyy_MM_dd_HHmmss.xlsx** o **report_export_yyyy_MM_dd.xlsx**.
   [hoja de Excel de ejemplo de fuente de usuario de getAbstract](assets/report-export-20170401175342.xlsx)

## Conector de Harvard ManageMentor {#hmmconnector}

El conector de Harvard ManageMentor es válido para clientes empresariales de Harvard ManageMentor que desean que sus alumnos descubran y consuman cursos de Harvard ManageMentor. El conector ayuda a crear cursos en Learning Manager; se puede configurar para obtener datos sobre el progreso de los alumnos de forma periódica. Para configurar este conector, realice el procedimiento siguiente:

### Configurar el conector de Harvard ManageMentor {#configuretheharvardmanagermentorconnector}

1. En el tablero del administrador de integración, haga clic en Harvard ManageMentor.

   En el mosaico, verá tres opciones: Introducción, Connect y Administrar conexiones.

1. Si configura el conector de Harvard ManageMentor por primera vez, haga clic en Conectar.

   También debe configurar la cuenta de FTP de Exavault antes de configurar este conector.

   Asegúrese de compartir estas credenciales de FTP con su proveedor de contenido para acceder a las fuentes.

1. En el campo Nombre de conexión, asigne un nombre a la conexión. Haga clic en Conectar para guardar esta conexión.
1. Si ya tiene una conexión establecida, en la página de inicio, haga clic en Harvard ManageMentor > Administrar conexiones. Haga clic en la conexión que desea editar para editar la configuración.

   La función de migración debe estar habilitada para su cuenta antes de configurar este conector.

   ![](assets/hmm.png)

1. En el panel izquierdo, haga clic en Configurar. Elija una de las opciones siguientes:

   * Vea o edite los detalles de su cuenta y el calendario de sincronización desde esta ventana. Debe seleccionar la casilla de verificación Habilitar conexión si desea habilitar esta cuenta.
   * Haga clic en Habilitar programación para programar su sincronización. Puede indicar la hora y la fecha de inicio; a continuación, especifique ingresar la frecuencia de su programa de sincronización en días. Por ejemplo, habilite la sincronización cada 3 días.

1. En el panel izquierdo, haga clic en Ejecución a petición. Esta opción le permite importar fuentes de usuario y otros datos relevantes de Harvard ManageMentor. Indique la fecha de inicio para la ejecución a petición y haga clic en Ejecutar para ejecutar la sincronización. Se importan todos los datos desde la fecha de inicio hasta el presente para esta conexión.

   * Puede hacer clic en Deshabilitar acceso a Learning Manager durante la ejecución en la que la aplicación tendrá un tiempo de inactividad durante la sincronización.
   * Si hace clic en Habilitar acceso a Learning Manager durante la ejecución, no hay interrupción en el servicio durante la sincronización.

   Si desea automatizar la sincronización cada pocos días, especifique el número de días en el campo Repetir número de días. La sincronización garantiza que su cuenta se actualice con la última versión de los resúmenes de Harvard ManageMentor.

1. También puede hacer clic en Estado de la ejecución en el panel izquierdo en cualquier momento para ver el resumen de todas las ejecuciones de este conector, en orden cronológico. Puede ver la fecha de inicio y la duración de la sincronización, el tipo de sincronización (si se trata de sincronización a petición) y el estado de la sincronización (si la sincronización está en curso o está completa).

   Cuando elimina y vuelve a crear una conexión, vuelven a aparecer las ejecuciones anteriores del conector. Puede ver todas las ejecuciones antes de eliminar la conexión.

   Puede repetir una ejecución solo de la última sincronización.

   Para que la sincronización sea correcta, debe asegurarse de que al menos uno de los siguientes archivos esté presente en la carpeta FTP de Harvard ManageMentor:

   hmm12_metadata.xlsx: este archivo proporciona los metadatos de cursos para el conector de Harvard ManageMentor. Asegúrese de seguir la convención de nomenclatura cuando cargue el archivo.

   client_hmm12_20150125.xlsx: esta es la fuente de usuario para el conector de Harvard ManageMentor. La convención de nomenclatura de archivos que debe seguir es **cliente_hmm12_aaaaMMdd.xlsx.**

   Vea los dos ejemplos siguientes de fuente de usuario y de siguientes de curso para este conector:
   [Archivo de metadatos del curso para el conector de Harvard ManageMentor](assets/hmm12-metadata.xlsx) [Fuente de usuario para el conector de Harvard ManageMentor](assets/client-hmm12-20170304.xlsx)

## Conector de Workday {#workdayconnector}

Con el conector de Workday, puede integrar Learning Manager con el inquilino de Workday para automatizar la sincronización de datos.

### Importar

#### Asignación de atributos

El administrador de integración puede seleccionar columnas de Workday y asignarlas a los correspondientes atributos agrupables de Learning Manager. Es una acción que se efectúa una sola vez. Tras finalizar la asignación, la misma asignación se aplica en las posteriores importaciones de usuarios. Se puede volver a configurar si el administrador quiere otra asignación para importar usuarios.

#### Importación automatizada de usuarios

El proceso de importación de usuarios permite que el administrador de Learning Manager obtenga datos de los usuarios de Workday y los importe automáticamente a Learning Manager.

#### Filtrar usuarios

El administrador de Learning Manager puede aplicar filtros en los usuarios antes de importarlos. Por ejemplo, el administrador de Learning Manager puede optar por importar todos los usuarios en la jerarquía bajo uno o más responsables específicos.

## Exportar

La opción Exportación de aptitudes de usuario permite exportar aptitudes de usuarios a Workday automáticamente.

Las aptitudes de varias cuentas de Learning Manager no se pueden exportar simultáneamente con la misma cuenta de Workday.

## Programación {#Scheduling-1}

El usuario puede configurar tareas de programación conforme a los requisitos de la empresa y los usuarios de Learning Manager están al día según la programación. Asimismo, el administrador de integración puede programar la exportación de aptitudes de manera oportuna para integrarse con un sistema externo. La sincronización se puede realizar a diario en la aplicación Learning Manager.

## Configurar el conector de Workday {#configureworkdayconnector}

**Requisito previo**: solicite el administrador de Workday de su empresa para crear un usuario de sistema de integración con los permisos definidos en el documento ISU_Permissions. Descargue una copia del vínculo siguiente.
[Descargar una copia de la seguridad del usuario del sistema de integración (ISU).](assets/isu-permissions-v1.pdf) Obtenga información sobre el proceso de integrar Learning Manager con el conector de Workday.

1. En la página de inicio de Learning Manager, pase el ratón sobre el icono de Workday. Aparece un menú. Haga clic en la opción **[!UICONTROL Conectar]** del menú.

   ![](assets/workday-tile.png)

1. Un cuadro de diálogo le solicita las credenciales de la nueva conexión. Es preciso rellenar los campos siguientes antes de efectuar la conexión.

   * Nombre de conexión: proporcione un nombre de conexión según su preferencia.
   * URL de host: el administrador de integración puede obtener los detalles de URL de host del administrador de Workday correspondiente.
   * Inquilino: el inquilino es interno de su empresa. Su administrador de Workday le proporcionará los detalles del inquilino.
   * Nombre de usuario y contraseña: el administrador de Workday crea un usuario del sistema integrado (ISU) con los privilegios de seguridad necesarios y lo comparte con el administrador de integración.

   Nota: Learning Manager usa la versión 28.1 de la API de Workday.

   ![](assets/configure-connector.png)

1. Haga clic en Conectar después de proporcionar información en todos los campos pertinentes.

   También puede tener varias conexiones de Workday sincronizadas con su cuenta de Learning Manager.

En la página de información general, puede especificar el nombre de conexión de su integración. Elija la acción que desea efectuar de las siguientes opciones:

* Importar usuarios internos
* Exportar usuarios externos: Configurar una programación
* Exportar usuarios externos: A petición

![](assets/overview.png)

## Importar

### Asignación de atributos {#MapAttributes-1}

Con el conector de Workday, puede integrar Learning Manager y Workday para automatizar la sincronización de datos. Puede importar todos los usuarios activos de Workday a Learning Manager. Los usuarios pueden importarse de diversas fuentes de datos, incluidos FTP y Salesforce.

Los atributos de usuario de Learning Manager y Workday deben asignarse antes de importar usuarios. En la página Descripción general, use la opción Usuarios internos en Importar para proporcionar la asignación de atributos.

Introduzca las credenciales de Adobe Learning Manager en la columna Adobe Learning Manager. Use los menús desplegables a fin de seleccionar las credenciales correctas para las columnas en Workday.

Actualmente, Learning Manager admite la importación de 44 atributos de usuario de Workday. Añada más atributos mediante los campos activos de Learning Manager.

![](assets/map-attributes.png)

Workday tiene cuatro niveles de jerarquía, mientras que Learning Manager tiene dos. Los cuatro niveles de Workday son categoría de perfil de aptitud, perfil de aptitud, categoría de elemento de aptitud y elemento de aptitud. El nombre de la aptitud y el nivel de Learning Manager se asignarán en Workday en el elemento de aptitud.

+++Lista de atributos de Workday compatibles

wd:User_ID\
wd:Worker_ID\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Formatted_Address\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Formatted_Phone\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number\
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Gender_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID\
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID\
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$\
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Formatted_Address\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active_Status_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirado\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminated\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$\
wd:Qualification_Data.wd:Education.0.wd:School_Name\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company\
wd:Management_Chain_Data.wd:Worker_Supervisory_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID

+++

## Exportar

Puede exportar todas las aptitudes logradas por un usuario de Learning Manager a Workday. Tenga en cuenta que solo se exportan todas las aptitudes de usuario activas; Learning Manager no exporta aptitudes retiradas. También puede conectar varias cuentas de Learning Manager al mismo conector de Workday. Si los nombres de las aptitudes son los mismos en dos cuentas de Learning Manager, se asignan a la misma aptitud en Workday. Se recomienda actualizar los nombres de aptitudes en todas las cuentas de Learning Manager antes de actualizar la aptitud en Workday en caso de que dos cuentas de Learning Manager utilicen la misma cuenta de Workday.

+++Aptitudes del usuario: Configurar

Esta opción le permite programar la extracción del informe. Asegúrese de que la casilla de verificación Habilitar exportación de aptitudes de usuario con esta conexión esté habilitada. Seleccione la casilla de verificación Activar programación y especifique la fecha y la hora de inicio. También puede especificar el intervalo en el que desea que se genere y se envíe el informe. Seleccione la casilla de verificación Habilitar programación; a continuación, indique valores para Fecha de inicio, Hora y Repetir después de &#39;n&#39; cantidad de días. Una vez hecho esto, haga clic en Guardar.

![](assets/configure-schedule.png)

+++

+++Aptitudes del usuario: a petición

Puede especificar la fecha de inicio y exportar el informe usando la opción. El informe se extraerá desde la fecha indicada hasta el presente. Especifique la fecha a partir de la cual desea comenzar a generar el informe y haga clic en Ejecutar.

![](assets/on-demand-report.png)

+++

+++Aptitudes del usuario: estado de ejecución

Aquí puede ver el resumen de todas las tareas y obtener su informe de estado. Puede descargar informes de errores haciendo clic en el vínculo del informe de errores.

![](assets/execution-status.png)

+++

## Conector de miniOrange {#miniorangeconnector}

Con el conector de miniOrange, se puede integrar Learning Manager con el inquilino de miniOrange para automatizar la sincronización de datos.

### Importar

#### Asignación de atributos

El administrador de integración puede elegir atributos de miniOrange y asignarlos a los atributos agrupables de Learning Manager correspondientes. Es una acción que se efectúa una sola vez. Tras finalizar la asignación, la misma asignación se aplica en las posteriores importaciones de usuarios. Se puede volver a configurar si el administrador quiere otra asignación para importar usuarios.

#### Importación automatizada de usuarios

El proceso de importación de usuarios permite al administrador de Learning Manager obtener detalles de los empleados de miniOrange e importarlos automáticamente en Learning Manager.

#### Filtrar usuarios

El administrador de Learning Manager puede aplicar filtros en los usuarios antes de importarlos. Por ejemplo, el administrador de Learning Manager puede optar por importar todos los usuarios en la jerarquía bajo uno o más responsables específicos.

Para configurar   miniOrange   , póngase en contacto con el equipo de CSM de Learning Manager.

## Configurar el conector de miniOrange {#configureminiorangeconnector}

1. En la página de inicio de Learning Manager, pase el ratón sobre la tarjeta/miniatura miniOrange. Aparece un menú. Haga clic en la opción **[!UICONTROL Conectar]** en el menú.

   ![](assets/miniorange-tile.png)

1. Haga clic en Conectar para establecer una nueva conexión. Aparece la página del conector de miniOrange. Ingrese los detalles de la cuenta que desea asignar.

   ![](assets/establish-connection.png)

1. Si desea importar el usuario de miniOrange directamente como usuario interno de Learning Manager, utilice la opción **[!UICONTROL Importar usuarios internos]**.

   ![](assets/import-users.png)

1. En la página de asignación, a la izquierda   en el lado derecho se ven las columnas de Learning Manager   lateral se pueden ver las miniColumnas naranja. Seleccione el nombre de columna adecuado que corresponda al nombre de columna del administrador de aprendizaje.

   ![](assets/map-attributes.png)

1. Para ver y editar la fuente de datos, como administrador, haga clic en **[!UICONTROL Configuración > Fuente de datos]**.

   Se enumerará la fuente establecida de miniOrange. Si necesitas editar el filtro, haz clic en **[!UICONTROL Editar]**.

   ![](assets/data-source.png)

1. Cuando termine la importación, recibirá una notificación. Para ver o editar el registro de importación, haga clic en **[!UICONTROL Usuarios > Registro de importación.]**

### Eliminar una conexión {#deleteaconnection}

Siga estos pasos para eliminar una conexión miniOrange establecida.

## Conector de BlueJeans {#bluejeansconnector}

Ahora puede integrar Learning Manager con el conector de BlueJeans y utilizar BlueJeans para alojar clases. BlueJeans le permite iniciar llamadas de audio y videoconferencia, chats de video y seminarios web.

Siga estos pasos para configurar y usar el conector.

1. En la página de inicio de Learning Manager, pase el ratón sobre la tarjeta/miniatura de BlueJeans. Aparece un menú. Haga clic en la opción **[!UICONTROL Conectar]** del menú.

   ![](assets/miniorange.png)

1. Se abre la página del conector de BlueJeans. Introduzca los detalles de la cuenta en los campos respectivos para integrar Learning Manager y BlueJeans para la sincronización de la fuente de usuario. Puede obtener los detalles del administrador de su cuenta de BlueJeans.

   ![](assets/bluejeans-connecotrpage.png)

   Como alumno, mientras habilita el conector, use el mismo ID de correo electrónico que usó para su cuenta de Learning Manager para volver a habilitar las fuentes de usuario en Learning Manager.

1. Una vez establecida la conexión, como autor, cree un curso de clase virtual con BlueJeans como el sistema de conferencia.

   ![](assets/conferencing-systems.png)

1. Los administradores, responsables y alumnos pueden inscribir alumnos en el curso creado. Después de la inscripción, el alumno recibe un correo electrónico. El alumno puede iniciar sesión en su cuenta de Learning Manager para ver los detalles del programa y realizar el curso.
1. Cuando se completa el curso, se envía el informe de finalización a Learning Manager. El administrador puede ver el informe de finalización para verificar la asistencia y la puntuación de los alumnos.

   ![](assets/-attendence-and-scoringreport.png)

## Conector de Box {#boxconnector}

Con el conector de BOX, se puede integrar Learning Manager con sistemas externos arbitrarios para automatizar la sincronización de datos. Se espera que los sistemas externos puedan exportar datos en formato CSV y colocarlos en la carpeta adecuada de la cuenta de Box de Learning Manager. Las capacidades del conector de Box son las siguientes:

También puede utilizar el conector de FTP para la migración de datos, la importación de usuarios y la exportación de datos. Para obtener más información, consulte [Conector FTP de Learning Manager.](third-party-connectors.md#main-pars_header_1427405935)

## Importación de datos {#DataImport-1}

El proceso de importación de usuarios permite que el administrador de Learning Manager obtenga datos del servicio de Box de Learning Manager y los importe automáticamente a Learning Manager. Esta función permite integrar varios sistemas colocando el archivo .csv generado por dichos sistemas en las carpetas correspondientes de las cuentas de Box. Learning Manager recopila los archivos .csv, los combina e importa los datos conforme a la programación. Consulte la función Programación para obtener más información.

**Asignación de atributos**

El administrador de integración puede seleccionar las columnas del archivo .csv y asignarlas a los atributos agrupables de Learning Manager. Esta asignación es una tarea que se realiza una sola vez. Después de finalizar la asignación, la misma asignación se aplica en las importaciones de usuarios posteriores. La asignación se puede volver a configurar si el administrador desea tener una asignación diferente para importar usuarios.

## Exportación de datos {#dataexport}

La opción Exportación de datos permite exportar aptitudes de usuarios a una ubicación de Box para su integración con cualquier otro sistema de terceros.

## Programar informes {#schedulereports}

El usuario puede configurar tareas de programación conforme a los requisitos de la empresa y los usuarios de Learning Manager están al día según la programación. Asimismo, el administrador de integración puede programar la exportación de aptitudes de manera oportuna para integrarse con un sistema externo. La sincronización se puede realizar a diario en la aplicación Learning Manager.

## Configurar el conector de Box {#configureboxconnector}

Obtenga información sobre el proceso de integrar Learning Manager con el conector de Box.

1. En la página de inicio de Learning Manager, pase el ratón sobre la tarjeta/miniatura de Box. Aparece un menú. Haga clic en el elemento Conectar del menú.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

1. Un cuadro de diálogo le solicita el ID de correo electrónico. Indique el ID de correo electrónico de la persona responsable de administrar la cuenta de Learning Manager Box para la organización. Haga clic en Conectar después de indicar el ID de correo electrónico.

1. Learning Manager le envía un mensaje de correo electrónico solicitando al usuario que restablezca la contraseña antes de acceder a Box por primera vez. El usuario debe restablecer la contraseña y utilizarla para acceder a la cuenta de Box de Learning Manager.

   Solo se puede crear una cuenta de Learning Manager Box para una cuenta de Learning Manager determinada.

   En la página de información general, puede especificar el nombre de conexión de su integración. Elija la acción que desea efectuar de las siguientes opciones:

   * Importar usuarios internos
   * Exportar usuarios externos: Configurar una programación
   * Exportar usuarios externos: A petición

## Importar

+++Usuario interno

La opción de importación de usuarios internos le permite programar la generación del informe de importación de usuarios automáticamente. Los informes que se generan se le envían como archivos .csv.

+++

+++Asignar atributos

Una vez establecida correctamente una conexión, puede asignar las columnas de archivos CSV que se colocarán en la carpeta de Box a los atributos correspondientes de Learning Manager. Este paso es obligatorio.

1. En la página Asignar atributos, a la izquierda   En el lado derecho, se muestran las columnas de Learning Manager.   En el lateral puede ver los nombres de columna de CSV. Al principio, en el lado derecho, hay un cuadro de selección vacío. Importe cualquier archivo .csv de plantilla haciendo clic en Elegir archivo.

1. El paso anterior rellena la lista desplegable seleccionada de la derecha con todos los nombres de columnas de CSV. Seleccione el nombre de columna adecuado que corresponda al nombre de columna del administrador de aprendizaje.

   *El campo de responsable debe asignarse necesariamente a un campo de tipo de dirección de correo electrónico. Asignar todas las columnas es obligatorio antes de poder usar el conector.*

1. Tras completar la asignación, haga clic en Guardar .

   El conector ya está listo para utilizarse. La cuenta que se ha configurado ahora aparece como una fuente de datos dentro de la aplicación del administrador, para que el administrador programe la importación o la sincronización a petición.

+++

+++Uso del conector de Learning Manager Box

1. Los archivos CSV de sistemas externos deben colocarse en la ruta siguiente:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Nota:** En la versión de julio de 2016, solo se permite la importación de usuarios. Por lo tanto, para utilizar el conector de Box, debe asegurarse de que los archivos CSV se coloquen en la carpeta siguiente:\
   `code Home/import/user/internal/*.csv`

1. El conector de Box toma todas las filas de los archivos CSV, por lo que es importante que la fila correspondiente a un usuario en un archivo CSV no aparezca en ningún otro archivo CSV.
1. Todos los archivos CSV deben contener las columnas especificadas en la asignación.
1. Todos los archivos CSV necesarios deben estar presentes en la carpeta antes de que comience el proceso.

Al importar usuarios a Learning Manager, el administrador también necesita saber cómo se administran los usuarios en Learning Manager. Consulte [Ayuda de administración de usuarios](../integration-admin/feature-summary/migration-manual.md#usermanagement) para obtener más información.

+++

## Exportar

+++Aptitudes

Existen dos opciones para exportar informes de aptitudes de usuarios.

Aptitudes del usuario: A petición: puede especificar la fecha de inicio y exportar el informe mediante esta opción. El informe se extraerá desde la fecha de entrada hasta el presente

**[!UICONTROL Aptitudes del usuario: Configurar]**: esta opción le permite programar la extracción del informe. Seleccione la casilla de verificación Activar programación y especifique la fecha y la hora de inicio. También puede especificar el intervalo en el que desea que se genere y se envíe el informe.

+++

Para abrir la carpeta Export donde se colocarán los archivos exportados en la ubicación de Box, abra el vínculo a la carpeta de Box que se proporciona en la página Aptitudes del usuario, como se muestra a continuación.

Los archivos exportados automáticamente estarán presentes en la ubicación **Home/export/&#42;Box_location&#42;**

Los archivos exportados automáticamente estarán disponibles con el título **skill_achievements_&#42;date from &#42;_to_&#42;date to&#42;.csv**

El cliente debe administrar los permisos de acceso y el contenido de la carpeta de Box compartida por el equipo de Learning Manager.  Tenga en cuenta también que el contenido de la carpeta se almacenará físicamente en la región de Frankfurt.

## Conector de LinkedInLearning {#linkedinlearningconnector}

El conector LinkedInLearning es válido para clientes empresariales de LinkedIn.com que desean que sus alumnos descubran y consuman cursos desde Learning Manager. El conector se puede configurar para obtener cursos de manera periódica con la clave de API. Después de crear un curso en Learning Manager, los usuarios lo pueden buscar y consumir. Después, se puede seguir el progreso del alumno desde Learning Manager.

### Configurar el conector de LinkedIn {#configurelinkedinconnector}

1. En el tablero del administrador de integración, haga clic en LinkedInLearning.

   Verá el mosaico con tres opciones: Introducción, Connect y Administrar conexiones.

1. Si va a configurar el conector de LinkedInLearning por primera vez, haga clic en Conectar.

   Debe configurar la cuenta de FTP de Exavault antes de configurar este conector.

1. En la página de conexión, especifique un nombre para el conector. Indique la Appkey y la clave secreta de la conexión.

   Debe ponerse en contacto con su proveedor para obtener Appkey y la clave secreta .

1. Haga clic en Guardar.

   La configuración se guarda y se agrega la conexión de LinkedInLearning para su cuenta. Ahora puede hacer clic en Administrar conexiones en la página Inicio y editar su configuración en cualquier momento.

1. Si ya tiene una conexión establecida, haga clic en Administrar conexiones para ver todas sus conexiones.

   La función de migración debe estar habilitada para su cuenta antes de configurar este conector.

1. Haga clic en la conexión que desea editar.
1. En el panel izquierdo, haga clic en Configurar. Elija una de las opciones siguientes:

   * Vea o edite los detalles de su cuenta y el calendario de sincronización desde esta ventana. Debe seleccionar la casilla de verificación Habilitar conexión si desea habilitar esta cuenta.
   * Haga clic en Editar y edite sus credenciales. Haga clic en Restablecer para deshacer sus actualizaciones en este campo.
   * Haga clic en Habilitar programación para programar su sincronización. Puede indicar la hora y la fecha de inicio; a continuación, especifique ingresar la frecuencia de su programa de sincronización en días. Por ejemplo, habilite la sincronización cada 3 días.

   Haga clic en Guardar para guardar sus cambios.

1. En el panel izquierdo, haga clic en Ejecución a petición. Esta opción le permite importar fuentes de usuario y otros datos relevantes de LinkedIn. Introduzca la fecha de inicio de la ejecución a petición y haga clic en Ejecutar para ejecutar la sincronización. Se importan todos los datos desde la fecha de inicio hasta el presente.

   * Puede hacer clic en Deshabilitar acceso a Learning Manager durante la ejecución en la que la aplicación tendrá un tiempo de inactividad durante la sincronización.
   * Si hace clic en Habilitar acceso a Learning Manager durante la ejecución, no hay interrupción en el servicio durante la sincronización.

1. También puede hacer clic en Estado de la ejecución en el panel izquierdo en cualquier momento para ver el resumen de todas las ejecuciones de este conector, en orden cronológico. Puede ver la fecha de inicio y la duración de la sincronización, el tipo de sincronización (si se trata de sincronización a petición) y el estado de la sincronización (si la sincronización está en curso o está completa).

   Cuando elimina y vuelve a crear una conexión, vuelven a aparecer las ejecuciones anteriores del conector. Puede ver todas las ejecuciones antes de eliminar la conexión.

   Puede repetir una ejecución solo de la última sincronización.

