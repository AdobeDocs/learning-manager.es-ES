---
jcr-language: en_us
title: Administrar funciones personalizadas mediante archivos CSV
description: El administrador de integración puede añadir varias funciones personalizadas a su cuenta en bloque mediante CSV, así como asignar las mismas funciones a varios usuarios. Este enfoque automatiza el proceso de creación de funciones personalizadas.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---



# Administrar funciones personalizadas mediante archivos CSV

El administrador de integración puede añadir varias funciones personalizadas a su cuenta en bloque mediante CSV, así como asignar las mismas funciones a varios usuarios. Este enfoque automatiza el proceso de creación de funciones personalizadas.

Puede configurar funciones mediante los conectores FTP y Box de Learning Manager.

Después de iniciar sesión en su cuenta de almacenamiento de Box o ExaVault, el administrador de integración puede añadir los siguientes archivos CSV a la cuenta:

* role.csv
* user_role.csv

Para empezar, descargue los archivos CSV y cambie los valores según sus necesidades.

**role.csv**
[Archivo de muestra: role.csv](assets/role.csv) [Archivo de muestra: user_role.csv](assets/user-role.csv)

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nombre de columna</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
   <td>
    <p><b>Valores de ejemplo</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Nombre</p></td>
   <td>
    <p>Identifique la función en el archivo CSV para asignarla a los usuarios.</p></td>
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
    <p>ESCRIBIR | INFORME</p>
    <p>Los nombres de columna se corresponderán con nombres de tipos de entidad como Catálogo, Curso, Plan de aprendizaje, etc.</p>
    <p>En el CSV estará presente una columna por cada tipo de entidad. Las entidades para las que no se conceda permiso deben incluirse con un valor NINGUNO</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de ámbito de catálogo</p></td>
   <td>
    <p>Un solo nombre de catálogo o una lista separada por PIPE (|) de nombres de catálogo que determinan el ámbito de esta función.</p></td>
   <td>
    <p>Catálogo de ventas | Catálogo general</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de ámbito de grupo de usuarios</p></td>
   <td>
    <p>Grupo de usuarios Nombre y valor de atributo que determinan el ámbito de los usuarios de esta función.</p>
    <p>Consulte los ámbitos en la sección siguiente.</p></td>
   <td>
    <p>location=Londres</p></td>
  </tr>
  <tr>
   <td>
    <p>Descripción</p></td>
   <td>
    <p>Descripción opcional fácil de usar para ayudar a comprender el propósito de la función y la referencia posterior.</p></td>
   <td>
    <p>Acceso completo del autor a los objetos de aprendizaje en el catálogo de ventas</p></td>
  </tr>
 </tbody>
</table>

Todas las columnas excepto Descripción son obligatorias.

## Definir ámbito de grupos de usuarios {#definescopeofusergroups}

Puede especificar ámbitos para grupos de usuarios para varios tipos de grupos de las siguientes maneras:

* Nombre del grupo de usuarios tal como está (por ejemplo, Todos los autores, Mi grupo personalizado)
* Atributo y valor de hoja (por ejemplo, Department=HR)
* Grupos de perfiles de autorregistro (self_registration=profilename)
* Grupos de perfiles de registro externos (ext_registration=profilename)
* El equipo de un responsable de informes directos (manager_direct=`<emailid>`)
* Una organización completa del responsable (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nombre de columna</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
   <td>
    <p><b>Comentario</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Id</p></td>
   <td>
    <p>ID de correo electrónico del usuario al que se va a asignar una función configurable.</p></td>
   <td>
    <p>Si el usuario ya tiene asignada una función configurable, la función se reemplaza por una nueva función especificada en el archivo CSV. No se notifica ningún error.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Nombre de la función configurable que se va a asignar al usuario</p></td>
   <td>
    <p>El nombre de la función debe ser una función existente tal y como se especifica en el CSV. Las funciones creadas por el administrador a través de la interfaz de usuario se pueden utilizar aquí.</p></td>
  </tr>
 </tbody>
</table>

**Funciones de ámbito completo**

Cada vez que se asigna el permiso completo para cualquiera de las siguientes funciones (funciones de nivel de cuenta), el ámbito de grupo de usuarios y el ámbito de catálogo se toman automáticamente como COMPLETOS, ya que el usuario no puede tener acceso limitado a estas funciones.

Si en el CSV se proporciona algún nombre de catálogo o de grupo de usuarios, se sobrescribe con el permiso COMPLETO.

* Anuncios
* Aptitudes
* Interacción
* Usuarios
* Planes de aprendizaje
* Plantillas de correo electrónico

## Añadir los archivos CSV de funciones en la cuenta {#addtherolecsvsintheaccount}

En su cuenta de Box, elija **Importar > usuario > interno** y cargue los archivos: role.csv y user_role.csv.

* Los archivos CSV de funciones personalizadas se deben copiar en la carpeta &quot;import->user->internal->user_role&quot;
* El archivo CSV de usuarios debe copiarse en la carpeta &quot;import->user->internal&quot;.

Ambos archivos CSV deben cargarse solo a través de Box o FTP y no pueden cargarse a través de la interfaz de usuario.

>[!NOTE]
>
>El archivo CSV de usuarios es obligatorio, pero los archivos CSV de funciones personalizadas son opcionales. Todos los archivos presentes se procesan y los demás se omiten.

Los administradores de la interfaz de usuario no pueden ver las funciones personalizadas creadas con el archivo csv. Estos roles no se relacionarán ni se verán afectados por los roles creados (o que se vayan a crear posteriormente) por la interfaz de usuario.

Las funciones personalizadas creadas por un archivo .csv se pueden administrar completamente a través del propio archivo .csv. Esto incluye agregar, modificar y eliminar roles.

Las funciones asignadas se pueden revocar eliminando entradas de asignación del archivo csv user_role. Sin embargo, esto no afecta a las tareas realizadas a través de la IU de administración.

Para asignar y revocar una función personalizada, actualice los archivos csv.

## Sincronización de funciones personalizadas {#synchronizationofcustomroles}

Después de que el administrador de integración cargue los archivos CSV basados en funciones en el almacenamiento del conector, el administrador puede habilitar la sincronización en los archivos CSV. Cada vez que se actualiza, añade o elimina una función personalizada en los archivos CSV, el administrador puede sincronizar la información de los archivos y actualizar la lista de funciones.

En la página Introducción del panel Administrador, haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Orígenes de datos]**.

En la sección Ajustes de sincronización , habilite la opción **[!UICONTROL Habilitar la sincronización automática]**.

![](assets/sync-settings.png)

*Seleccione la opción Activar sincronización automática*

Al seleccionar esta opción, puede programar la hora de sincronización en el momento exacto que especifique en el campo Hora de sincronización. Si especifica la hora de sincronización como 12:00 a.m., las funciones personalizadas se actualizan todos los días exactamente a la hora especificada.

Si desea sincronizar los datos a petición, haga clic en **[!UICONTROL Sincronizar ahora]**.

## Restricciones al configurar roles {#constraintswhileconfiguringroles}

En cualquier cuenta, el nombre de una función debe ser único. Por lo tanto, una función creada a través de la interfaz de usuario o CSV no debe tener el mismo nombre que otra función ya creada mediante la interfaz de usuario o CSV.

En líneas similares, en la IU de administración, no se puede asignar a un usuario una función configurable creada mediante CSV, ya que estas funciones no estarán disponibles.

Sin embargo, el archivo CSV de asignación de usuarios se puede utilizar para asignar funciones creadas por la interfaz de usuario.
