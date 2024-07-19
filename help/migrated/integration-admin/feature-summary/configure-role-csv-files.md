---
jcr-language: en_us
title: Administrar funciones personalizadas mediante archivos CSV
description: El administrador de integración puede añadir funciones personalizadas en bloque a su cuenta a través de CSV, así como asignar esas mismas funciones a varios usuarios. Este enfoque automatiza el proceso de creación de funciones personalizadas.
contentowner: saghosh
exl-id: fce2f457-2834-491a-8331-64086f5a51b5
source-git-commit: f328076016d8c41455cad71f00d1dc9a1531e007
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 81%

---

# Administrar funciones personalizadas mediante archivos CSV

El administrador de integración puede añadir funciones personalizadas en bloque a su cuenta a través de CSV, así como asignar esas mismas funciones a varios usuarios. Este enfoque automatiza el proceso de creación de funciones personalizadas.

Puede configurar las funciones a través de los conectores de FTP y Box de Learning Manager.

Después de iniciar sesión en su cuenta de almacenamiento de Box, el administrador de integración puede añadir los siguientes archivos CSV a la cuenta:

* user.csv
* role.csv
* user_role.csv

En primer lugar, descargue el archivo CSV y cambie los valores en función de sus requisitos.

* Archivo de muestra: [role.csv](assets/role.csv)
* Archivo de muestra: [user_role.csv](assets/user_role.csv)

**role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nombre de la columna</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
   <td>
    <p><b>Valores de ejemplo</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Nombre</p></td>
   <td>
    <p>Identifique la función en el CSV que se asignará a los usuarios.</p></td>
   <td>
    <p>Autor de ventas</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifique el tipo de acceso (FULL, WRITE, ENROLL, REPORT, NONE) para cada tipo de entidad, como COURSE, CATALOG, etc.</p></td>
   <td>
    <p>COMPLETO</p>
    <p>NINGUNO</p>
    <p>ESCRITURA | INFORME</p>
    <p>Los nombres de columna se corresponden con los nombres de tipos de entidad, como Catálogo, Curso, Plan de aprendizaje, etc.</p>
    <p>En el CSV habrá una columna para cada tipo de entidad. Las entidades para las que no sea necesario dar ningún permiso deben incluirse con el valor NINGUNO.</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de ámbito del catálogo</p></td>
   <td>
    <p>Nombre de catálogo o lista separada por BARRAS VERTICALES (|) de los nombres de catálogo que determinan el ámbito de esta función.</p></td>
   <td>
    <p>Catálogo de ventas | Catálogo general</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de ámbito de grupo de usuarios</p></td>
   <td>
    <p>Nombre del atributo del grupo de usuarios y valor que determinan el ámbito de los usuarios de esta función.</p>
    <p>Consulte la sección siguiente para obtener información sobre los ámbitos.</p></td>
   <td>
    <p>location=London</p></td>
  </tr>
  <tr>
   <td>
    <p>Descripción</p></td>
   <td>
    <p>Descripción sencilla opcional para facilitar la comprensión del objetivo de la función y para futura referencia.</p></td>
   <td>
    <p>Acceso completo del autor a los objetos de aprendizaje del catálogo de ventas</p></td>
  </tr>
 </tbody>
</table>

Todas las columnas excepto Descripción son obligatorias.

## Definir el ámbito de los grupos de usuarios {#definescopeofusergroups}

Puede especificar los ámbitos de los grupos de usuarios para varios tipos de grupos, del modo siguiente:

* Nombre del grupo de usuarios tal cual (por ejemplo, Todos los autores, Mi grupo personalizado)
* Valor y atributo de la hoja (por ejemplo, Department=HR)
* Grupos de perfiles de registro automático (self_registration=profilename)
* Grupos de perfiles de registro externo (ext_registration=profilename)
* Equipo de un responsable de subordinado directo (manager_direct=`<emailid>`)
* Organización completa de un administrador (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nombre de la columna</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
   <td>
    <p><b>Comentario</b></p></td>
  </tr>
  <tr>
   <td>
    <p>ID</p></td>
   <td>
    <p>ID de correo electrónico del usuario al que se asignará una función configurable.</p></td>
   <td>
    <p>Si el usuario ya tiene una función configurable asignada, la función se sustituye por otra función nueva especificada en el CSV. No se genera ningún error.</p></td>
  </tr>
  <tr>
   <td>
    <p>Función personalizada</p></td>
   <td>
    <p>Nombre de la función configurable que se asignará al usuario.</p></td>
   <td>
    <p>El nombre de la función debe corresponder a una función existente especificada en el CSV. Aquí se pueden usar las funciones creadas por el administrador a través de la IU.</p></td>
  </tr>
 </tbody>
</table>

**Funciones de ámbito completo**

Siempre que se asigna permiso completo a cualquiera de las funciones siguientes (del nivel Cuenta), las opciones Ámbito del grupo de usuarios y Ámbito del catálogo se consideran que tienen permiso COMPLETO, puesto que el usuario no puede tener acceso limitado a dichas funciones.

Si en el archivo CSV se proporcionan nombres de catálogos o de grupos de usuarios, se sobrescriben mediante el permiso COMPLETO.

* Anuncios
* Aptitudes
* Interacción
* Usuarios
* Planes de aprendizaje
* Plantillas de correo electrónico

## Añadir los archivos CSV de funciones en la cuenta {#addtherolecsvsintheaccount}

En la cuenta de Box, seleccione **Importar > usuario > interno** y cargue los archivos role.csv y user_role.csv.

* Los archivos role.csv y user_role.csv deben copiarse en la carpeta **Import** > **user** > **internal** > **user_role**.
* El archivo user.csv debe copiarse en la carpeta **Import** > **user** > **internal**.

Ambos archivos CSV deben cargarse solo a través de Box y no pueden cargarse a través de la interfaz de usuario.

>[!NOTE]
>
>El archivo CSV de usuarios es obligatorio, pero los archivos CSV de funciones personalizadas son opcionales. Se procesan todos los archivos que están presentes y se omiten otros.

Las funciones personalizadas que se creen con el archivo CSV no están visibles para los administradores de la IU. Estas funciones no están relacionadas con las funciones creadas (o que se vayan a crear) con la IU, ni se ven afectadas por ellas.

Las funciones personalizadas creadas por un archivo .csv se pueden administrar completamente a través del propio archivo .csv. Esto incluye agregar, modificar y eliminar roles.

Las funciones asignadas se pueden revocar eliminando las entradas de asignación de user_role csv. Ahora bien, esto no afecta a las asignaciones realizadas desde la interfaz de usuario del administrador.

Para asignar y revocar una función personalizada, cargue los archivos CSV.

## Sincronización de las funciones de personalizadas {#synchronizationofcustomroles}

Una vez que el administrador de integración carga los CSV basados en funciones en el almacenamiento del conector, el administrador puede habilitar la sincronización con los CSV. Cada vez que se actualiza, se añade o se elimina una función personalizada en los archivos CSV, el administrador puede sincronizar la información en los archivos y actualizar la lista de funciones.

En la página Introducción del panel Administrador, haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Orígenes de datos]**.

En la sección Configuración de sincronización, habilite la opción **[!UICONTROL Activar sincronización automática]**.

![](assets/sync-settings.png)

*Seleccione la opción Habilitar sincronización automática*

Si selecciona esta opción, puede programar el momento de la sincronización, a la hora exacta que indique en el campo Hora de sincronización. Si configura las 12:00 h como hora de sincronización, las funciones personalizadas se actualizan todos los días exactamente a la hora especificada.

Si desea sincronizar los datos bajo demanda, haga clic en **[!UICONTROL Sincronizar ahora]**.

## Restricciones en la configuración de funciones {#constraintswhileconfiguringroles}

En cualquier cuenta, el nombre de una función debe ser exclusivo. Por tanto, una función creada mediante la IU o un CSV no debe tener el mimo nombre que otra función ya creada por la IU o un CSV.

De modo similar, en la IU del administrador, no es posible asignar a un usuario una función configurable que se haya creado mediante CSV, ya que estas funciones no estarán disponibles.

Sin embargo, se puede utilizar un CSV de asignación para asignar funciones creadas por la IU.
