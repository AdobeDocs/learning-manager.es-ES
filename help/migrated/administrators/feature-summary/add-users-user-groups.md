---
description: Obtenga información sobre cómo añadir usuarios o grupos de usuarios en la aplicación Learning Manager.
jcr-language: en_us
title: Añadir usuarios y crear grupos de usuarios
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3913'
ht-degree: 0%

---



# Añadir usuarios y crear grupos de usuarios

Obtenga información sobre cómo añadir usuarios o grupos de usuarios en la aplicación Learning Manager.

<!--![](assets/user-mgmt-new.png)-->

## Resumen {#overview}

En Adobe Learning Manager, puede asumir las siguientes funciones:

* **Administrador:** Un administrador define la estrategia de formación de la organización. Un administrador puede añadir alumnos, buscar las aptitudes necesarias para los alumnos, gestionar y asignar cursos, crear planes de aprendizaje, certificaciones y programas de aprendizaje, y gestionar informes para toda la organización.
* **Autor:** Los autores son diseñadores de instrucciones y creadores de contenido. Un autor puede añadir módulos y cursos a Learning Manager.
* **Responsable:** Un responsable gestiona las actividades de aprendizaje de un equipo. Un responsable puede designar a miembros del equipo para que realicen un curso, aprueben las solicitudes de los miembros del equipo y proporcionen comentarios sobre el rendimiento de los miembros del equipo tras la finalización de la formación. Los responsables también pueden ver los informes de su equipo para realizar un seguimiento de su rendimiento.
* **Alumno:** Los alumnos pueden acceder a los cursos, los programas de aprendizaje y las certificaciones que se les asignan. Los alumnos también pueden examinar todos los cursos disponibles mediante un catálogo e inscribirse en cursos, programas de aprendizaje o certificaciones.

Como administrador, puede añadir usuarios de tres maneras:

* Interno
* Externo
* Grupos de usuarios

## Añadir un único usuario {#addasingleuser}

Para añadir usuarios:

1. Inicie sesión en Adobe Learning Manager como administrador.
1. En la página principal, haga clic en **[!UICONTROL Añadir usuarios]**. En esta página, puede añadir uno o varios usuarios a la vez mediante un archivo CSV. También puede crear un vínculo de registro automático para empleados internos o crear un perfil de alumno externo.
1. Para añadir un solo usuario, haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha y seleccione la opción **[!UICONTROL Usuario único]**.

   ![](assets/single-user.png)
   *Añadir un único usuario interno*

1. En la **[!UICONTROL Añadir usuario]** , introduzca los detalles del alumno. Para el campo **[!UICONTROL Nombre del responsable]**, seleccione el nombre de un usuario existente en el sistema.

   ![](assets/manager.png)
   *Cuadro de diálogo Agregar usuario*

1. Para añadir el nuevo usuario en Learning Manager, haga clic en **[!UICONTROL Añadir]**. Una vez agregado el usuario, este recibe un correo de verificación. A continuación, el alumno activa la cuenta y comienza a utilizar el Administrador de aprendizaje. Este flujo de trabajo es útil si necesita añadir un número limitado de alumnos a su cuenta de Learning Manager. Sin embargo, si tiene previsto inscribir a todos los empleados de una organización grande, puede agregarlos en un solo intento. Para obtener más información, consulte la siguiente sección.

## Añadir usuarios en bloque {#addusersinbulk}

Por lo general, la mayoría de las organizaciones trabajan con un sistema de gestión de recursos humanos (HRMS), que mantiene todos los registros de los empleados, como la designación, la ubicación, la fecha de incorporación o la jerarquía de los empleados. Puede exportar estos datos en formato CSV. Para importar un archivo CSV, siga los pasos que se indican a continuación:

1. Haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha y seleccione la opción **[!UICONTROL Cargar un CSV]**.

   ![](assets/upload-a-csv.png)
   *Cargar un archivo CSV para añadir usuarios en bloque*

1. El archivo CSV que cargue consta de los campos, como se muestra a continuación:

   ![](assets/csv.png)
   *Estructura del CSV*

   Debe mantener un archivo CSV maestro y realizar todas las adiciones y eliminaciones en el archivo CSV maestro. El archivo CSV principal contiene los siguientes campos:

   * name &#42;
   * correo electrónico &#42;
   * perfil
   * gerente

   (&#42;) Campo obligatorio.

1. Después de hacer clic en la opción **[!UICONTROL Cargar un CSV]**, se muestra el cuadro de diálogo siguiente.

   ![](assets/upload-a-csv-dialog.png)
   *Cuadro de diálogo Cargar CSV*

1. Elija el archivo CSV o arrastre y suelte el archivo. Una vez que haya elegido el archivo, asigne los campos de datos a los del archivo CSV. Haga clic en el menú desplegable correspondiente y elija el campo adecuado.

   ![](assets/map-data-fields.png)
   *Asignar campos en CSV*

1. Para empezar a importar los usuarios, haga clic en **[!UICONTROL Guardar]**. Puede ver un mensaje de confirmación.

   ![](assets/save-csv.png)
   *Mensaje de confirmación para la carga correcta del archivo CSV*

1. Los nuevos usuarios se añadirán a su cuenta de Adobe Learning Manager. Para seleccionar los nuevos usuarios, seleccione la casilla de verificación junto a los nombres para que todos estén seleccionados.

   ![](assets/select-new-users.png)
   *Nuevos usuarios añadidos*

>[!NOTE]
>
>Para obtener más información, consulte las preguntas frecuentes, [Añadir usuarios en bloque](../add-users-in-bulk.md).

Después de seleccionar los usuarios, puede realizar lo siguiente:

## Registrar un usuario {#registerauser}

Con el usuario seleccionado, haga clic en **[!UICONTROL Acciones]** en la esquina superior derecha y haga clic en **[!UICONTROL Registro]**.

Los usuarios seleccionados recibirán un correo electrónico de bienvenida. Si los alumnos ya tienen un Adobe ID, pueden hacer clic en este vínculo. Si no tienen un Adobe ID existente, pueden hacer clic en el vínculo Bienvenido para crear un Adobe ID y vincularlo a su cuenta de Learning Manager.

## Asignar una función {#assignarole}

Después de añadir alumnos a la cuenta de Adobe Learning Manager, si desea cambiar sus funciones, haga clic en Acciones en la esquina superior derecha de la página. Elija la opción **[!UICONTROL Asignar función]**. Aquí puede decidir si desea conceder acceso de autor o de administrador al alumno. Después de asignar una función, este alumno tiene acceso de autor a la cuenta y puede añadir módulos y crear cursos.

![](assets/assign-a-role.png)
*Asignar una función a un usuario*

## Quitar un rol {#removearole}

También puede eliminar el acceso de autor o administrador de los usuarios. Seleccione uno o más alumnos y haga clic en **[!UICONTROL Acciones]** y seleccione **[!UICONTROL Quitar rol]**. Elija una opción, por ejemplo, **[!UICONTROL Quitar autor]** y se revoca el acceso de autor para este alumno.

>[!NOTE]
>
>No se puede asignar manualmente una función de responsable a alguien del sistema. Obtienen acceso automáticamente al panel del responsable cuando se añaden uno o más empleados debajo de ellos.

## Eliminar un usuario {#deleteauser}

Para eliminar un usuario, haga clic en **[!UICONTROL Acciones]** y elija **[!UICONTROL Eliminar usuario]**. En el cuadro de diálogo de confirmación, haga clic **[!UICONTROL Sí]** y el alumno se elimina.

![](assets/delete-a-role.png)
*Mensaje de confirmación para eliminar un usuario*

## Editar un usuario {#editauser}

En la lista de usuarios, elija un usuario y haga clic en el usuario. En los detalles del usuario, haga clic en **[!UICONTROL Editar]** ( ![](assets/edit-pen.png)). En la **[!UICONTROL Editar usuario]** , realice las ediciones necesarias y, para guardar los cambios, haga clic en **[!UICONTROL Guardar]**.

![](assets/edit-user.png)
*Cuadro de diálogo Editar usuario*

## Flujos de trabajo para campos activos y valores de campos activos que mantienen la distinción entre mayúsculas y minúsculas

En esta versión, Learning Manager conserva la distinción entre mayúsculas y minúsculas del atributo de usuario y su valor. **Por ejemplo**, la distinción entre mayúsculas y minúsculas de un atributo de usuario es &#39;location&#39;; su valor &#39;PARIS&#39; se conservará y se mostrará de la misma manera. En caso de problemas, el administrador puede editar el nombre y los valores de atributo para corregir cualquier error de distinción entre mayúsculas y minúsculas.

El administrador puede hacer esto visitando **[!UICONTROL Aplicación de administración]** > **[!UICONTROL Usuarios]** > **[!UICONTROL Grupos de usuarios]** y haciendo clic en el nombre del grupo.

El administrador puede añadir y actualizar los valores de atributo permitidos para un alumno mediante la interfaz de usuario.

Tipos de campos activos:

* Agrupable: los alumnos se agrupan en función de los valores
* Comunicado: Los grupos de usuarios de informes se crearían en función de los campos activos
* Exportable: Los campos se verán en el informe de grupos de usuarios exportado.

## Crear un vínculo de registro automático {#createaselfregistrationlink}

También puede permitir que los empleados de su organización se registren como alumnos en la cuenta de Adobe de Learning Manager sin tener que recibir ayuda de usted como administrador. El administrador puede crear un vínculo de registro automático y compartirlo con los empleados, que pueden registrarse en el administrador de aprendizaje utilizando sus credenciales de Adobe.

En la esquina superior derecha de la página, haga clic **[!UICONTROL Añadir]** y elija **[!UICONTROL Registro automático]**.

![](assets/self-registration.png)
*Crear vínculo para registrarse como alumno*

La **[!UICONTROL Agregar perfil de registro automático]** se abre. Asigne un nombre a este perfil. A continuación, agregue el nombre del responsable. Es importante saber que el responsable ya debe estar registrado como alumno en Learning Manager.

![](assets/add-self-registrationprofile.png)
*Añadir perfil para el registro automático*

Después de hacer clic **[!UICONTROL Guardar]**, se genera una dirección URL que puede compartir con los alumnos para que puedan hacer clic en ella y registrarse ellos mismos.

## Inscribir alumnos externos {#enrollexternallearners}

En Adobe Learning Manager, también puede crear vínculos de registro para socios externos o agencias con acceso limitado a su cuenta y proporcionarles material de aprendizaje.

Existen algunas diferencias entre los registros internos y externos.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Usuarios internos</b></p></td>
   <td>
    <p><b>Usuarios externos</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Inicie sesión con las credenciales de Adobe ID o SSO.</p></td>
   <td>
    <p>Inicie sesión con cualquier ID de correo electrónico.</p></td>
  </tr>
  <tr>
   <td>
    <p>La interacción está disponible.</p></td>
   <td>
    <p>La interacción no está disponible.</p></td>
  </tr>
  <tr>
   <td>
    <p>Hay disponibles jerarquías de alumnos.</p></td>
   <td>
    <p>Las jerarquías de alumnos no están disponibles.</p></td>
  </tr>
 </tbody>
</table>

Para inscribir usuarios externos, siga los pasos que se indican a continuación:

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Externo]**.

   ![](assets/click-external.png)

   *Inscribir usuarios externos*

1. En la esquina superior derecha de la página, haga clic **[!UICONTROL Añadir]**.
1. En la **[!UICONTROL Añadir perfil de registro externo]** , añada los siguientes detalles:

   * El nombre de perfil de la organización asociada.
   * La dirección de correo electrónico del responsable de la organización asociada.
   * Límite de puestos para la inscripción externa de este socio.
   * Fecha de caducidad para establecer una fecha límite para dejar de permitir nuevos registros en este grupo. Después de la fecha de caducidad, solo los usuarios registrados existentes pueden acceder a esta formación.

   ![](assets/map-data-fields-2.png)

   *Cuadro de diálogo Añadir perfil de registro externo*

   * En la **[!UICONTROL Configuración avanzada]** , introduzca lo siguiente:

      * **[!UICONTROL Requisito de inicio de sesión]:** Especifique un valor en días. Los alumnos se eliminan si no inician sesión durante el período anterior.
      * **[!UICONTROL Dominios permitidos]:** Una lista separada por comas de nombres de dominio de correo electrónico de la lista blanca.
      * **[!UICONTROL Verificación por correo electrónico obligatoria]:** Seleccione esta opción para que la verificación por correo electrónico sea obligatoria para un alumno.

   ![](assets/email-verificationrequired.png)

   *Introduzca los detalles en la sección Configuración avanzada*

1. Después de hacer clic **[!UICONTROL Guardar]**, aparece el siguiente mensaje de confirmación. Debe compartir la dirección URL con su socio externo.

   ![](assets/save-and-share-urlwithexternalusers.png)

## Habilitar un perfil externo {#enableanexternalprofile}

Después de crear un perfil externo, debe habilitar su estado. En la lista de perfiles externos, elija el perfil requerido y active el botón de estado.

![](assets/choose-required-profiles.png)
*Habilitar un perfil externo*

Esto habilita el vínculo Inscripción externa. Se enviará automáticamente un correo electrónico de bienvenida al socio. También puede copiar el vínculo y compartirlo con ellos haciendo clic en el icono Copiar URL (), o puede volver a enviar el correo electrónico de bienvenida a la organización asociada haciendo clic en el icono Correo ().

El gestor de socios puede compartir el enlace con los empleados que deben realizar la formación en PreLearning Manager. Al hacer clic en el vínculo, pueden inscribirse ellos mismos después de completar algunos detalles para crear su perfil en Learning Manager. Estos usuarios no aparecerán en la ficha Alumnos junto con los empleados internos. Puede ver sus nombres debajo de la **[!UICONTROL Alumnos externos]** .

## Pausar un perfil externo {#pause}

Después de añadir un grupo de usuarios externos a Learning Manager, también puede pausar el proceso de registro de usuarios externos. Al pausar, se bloquea el proceso de registro de los usuarios externos. Sin embargo, este proceso solo funciona cuando los usuarios aún no se han registrado al aceptar la invitación.

Para pausar los grupos de usuarios externos, elija uno o varios grupos, haga clic en **[!UICONTROL Acciones]** en la esquina superior derecha de la página y haga clic en **[!UICONTROL Pausa]**.

## Reanudar un perfil externo {#resumeanexternalprofile}

En cualquier momento, siempre puede revocar el estado de pausa de un socio externo y reanudar los servicios normales. Haga clic en **[!UICONTROL Acciones]** en la esquina superior derecha de la página y seleccione **[!UICONTROL Currículum]**.

Los siguientes estados son aplicables a los usuarios externos:

* **Estado inactivo** - En este estado, el registro de los usuarios externos ha caducado. Los administradores establecen la fecha de caducidad de los usuarios externos al añadirlos a través del flujo de trabajo Añadir usuario .
* **Estado activo** - En este estado, los usuarios externos pueden registrarse en la aplicación de Learning Manager e iniciar sesión en la aplicación.
* **Pausa** - En este estado, el proceso de registro para usuarios externos está bloqueado. Sin embargo, los usuarios existentes pueden seguir iniciando sesión.

## Comprobar asientos usados {#checkusedseats}

En la lista de perfiles externos, haga clic en **[!UICONTROL Asientos usados]**. Puede ver el número de alumnos de la organización asociada que se han añadido.

![](assets/seats-used.png)
*Comprobar asientos usados*

## Eliminar un usuario {#Deleteauser-1}

Elija un usuario y, en la esquina superior derecha, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Eliminar usuario]**.

## Cambiar perfil {#changeprofile}

Para mover un usuario a otro perfil externo, elija un usuario. En la esquina superior derecha, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Cambiar perfil]**. En la lista de perfiles, elija un perfil y haga clic en **[!UICONTROL Cambiar]**.

## Asignar una función {#Assignarole-1}

Elija un usuario y, en la esquina superior derecha, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Asignar función]** > **Crear`<role>`**. El usuario obtiene una nueva función.

## Quitar un rol {#Removearole-1}

Elija un usuario y, en la esquina superior derecha, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Quitar rol]** > **Quitar`<role>`**. El rol seleccionado se elimina de la lista de roles asignados al usuario.

## Crear grupos de usuarios {#createusergroups}

Un grupo de usuarios es un conjunto de usuarios relacionados con una categoría. Los grupos de usuarios ayudan a los administradores a seleccionar alumnos en su organización en función de sus atributos y, a continuación, les asignan contenido de aprendizaje. Además, estos grupos de usuarios permiten a los administradores asignar logotipos y catálogos personalizados a los alumnos y mostrar informes personalizados sobre su progreso.

Para acceder a Grupos de usuarios, en el panel de navegación izquierdo, haga clic en **[!UICONTROL Grupos de usuarios]**.

![](assets/user-groups.png)
*Crear grupos de usuarios*

Hay dos tipos de grupos en Adobe Learning Manager: Personalizados y Generados automáticamente. Al añadir alumnos a su cuenta, algunos grupos se crean automáticamente en función de sus propiedades comunes.

Para ver los grupos creados automáticamente, haga clic en la ficha **[!UICONTROL Generado automáticamente]**.

![](assets/auto-generated.png)
*Ver grupos generados automáticamente*

Puede ver que hay diferentes grupos, como Todos los usuarios internos, Todos los responsables, grupos basados en el Centro de costes, en función del departamento y en función de los equipos de los responsables.

Además de los grupos generados automáticamente, puede crear grupos personalizados. Para añadir un nuevo grupo personalizado, en la esquina superior derecha, haga clic en **[!UICONTROL Añadir]**.

1. Introduzca el nombre y la descripción del grupo.
1. Introduzca el nombre de usuario o el perfil en el campo de búsqueda según escribe y selecciónelo en la lista desplegable para añadir usuarios.
1. Para añadir más alumnos, haga clic en **[!UICONTROL Añadir más usuarios].**
1. Para crear el grupo de usuarios, haga clic en **[!UICONTROL Guardar]**.

Este grupo personalizado se crea y se añade al perfil. Los grupos de usuarios que cree son de naturaleza dinámica. Si se añaden nuevos usuarios con atributos similares, se añaden automáticamente al grupo de usuarios.

## Exclusión de grupos de usuarios

A veces, es posible que desee excluir un pequeño conjunto de usuarios de un grupo de usuarios grande. Esto es necesario para inscribir este conjunto específico de usuarios en la formación mediante planes de aprendizaje o para configurar la visibilidad correcta de los catálogos. En esta versión de Learning Manager, puede excluir alumnos o grupos de usuarios al crear un grupo de usuarios personalizado. En el cuadro de diálogo Añadir grupo de usuarios, la sección Excluir alumnos le permite hacerlo.

![](assets/exclude-user-groups.png)
*Excluir grupos de usuarios*

Por ejemplo, si desea configurar un plan de aprendizaje para que se inscriban todos los usuarios que pertenezcan a la ubicación = California, excepto Store-5 (ubicada en California).

## Configuración avanzada {#advancedsettings}

## Orígenes de datos {#datasources}

Puede utilizar esta función cuando desee importar o sincronizar los usuarios o los datos de aprendizaje de la base de datos de su organización en la aplicación Learning Manager. También puede configurar la frecuencia de esta sincronización.

Haga clic en **[!UICONTROL Orígenes de datos]** en el panel izquierdo debajo de **[!UICONTROL Avanzado]** sección.

![](assets/data-sources-add-users.png)

*Orígenes de datos para importar o sincronizar usuarios*

Elija el tipo de origen de datos de la **[!UICONTROL Source]** , seleccione la frecuencia de actualización y haga clic en **[!UICONTROL Sincronizar ahora]** si necesita sincronizar inmediatamente o hacer clic en **[!UICONTROL Guardar].** Los tipos de orígenes de datos son SFDC, FTP, etc., para usuarios internos.

Puede agregar varios orígenes de datos.

## Campos activos {#activefields}

Esta función permite a los administradores añadir más campos activos además de lo que se ha proporcionado durante el registro del usuario.

Haga clic en **Campos activos** disponible en la página usuarios. Los alumnos solo pueden elegir entre los valores proporcionados en valores personalizados.

![](assets/active-fields.png)
*Campos activos*

### Configurar campos {#configurefields}

**Usuarios internos**

Puede agregar un valor personalizado para los campos de usuario de los usuarios internos.

Para añadir valores personalizados, siga estos pasos:

1. Haga clic en  **[!UICONTROL Modificar valores]** para un usuario interno.

   ![](assets/modify-values.png)
   *Modificar valores para usuarios internos*

1. La **Valores del campo Personalizado** que aparece.

   ![](assets/values-in-customfields.png)
   *Valores del cuadro de diálogo Campos personalizados*

1. Seleccione el valor que desea añadir en el **[!UICONTROL Seleccionar campo]** del menú desplegable.
1. Introduzca nuevos valores en el **[!UICONTROL Nuevo valor]** campo.
1. Haga clic en **[!UICONTROL Hecho]**.
1. Haga clic en Guardar en la esquina superior derecha para **[!UICONTROL Guardar]** cambios.

**Usuarios externos**

Añada valores personalizados similares a los de los usuarios internos.

![](assets/modify-values-forexternalusers.png)
*Modificar valores para usuarios externos*

### Configuración {#settings}

**Visualización de usuario**

Si la opción **Mostrar solo campos sin rellenar al iniciar sesión como alumno** está habilitada, un usuario solo ve los campos en blanco al iniciar sesión.

![](assets/settings-tab.png)
*Mostrar campos sin rellenar*

Con esta opción, un administrador puede decidir si desea mostrar los campos u ocultarlos una vez que se hayan rellenado.

## Restringir campos activos en informes {#restrictactivefields}

Learning Manager 27.7 presenta dos nuevas opciones: **[!UICONTROL Comunicado]** y **[!UICONTROL Exportable]**, para Campos activos.

![](assets/options-in-activefields.png)
*Opciones de Campos activos*

Para los campos CSV y los campos añadidos manualmente, si un campo activo se marca como **[!UICONTROL Comunicado]**, el campo activo se puede buscar en un filtro dentro de un informe de tablero.

![](assets/filters-in-a-dashboardreport.png)
*Filtros en un informe de tablero*

Si un campo activo se marca como **[!UICONTROL Exportable]**, el campo activo aparece en el archivo de Excel al descargar cualquier informe de Excel.

Estas opciones aparecen para los campos activos internos y externos.

Solo puede eliminar un campo activo personalizado.

## Visualización de usuario

Puede ocultar toda la página &quot;Completar su perfil&quot; a los alumnos. La página no aparecerá cuando el alumno inicie sesión.

Tenga en cuenta que el comportamiento predeterminado existente no cambia. Esta es una capacidad opcional que ahora están disponibles para los administradores.

Active las opciones siguientes:

![](assets/user-display.png)
*Sección Visualización de usuario*

## Compatibilidad con campos CSV manuales mediante conectores de FTP y Box {#import-connector}

A menudo, los usuarios desean que los campos activos se proporcionen manualmente cuando un alumno inicie sesión en Learning Manager. Esto es posible en Learning Manager en este momento, cuando el usuario importa un archivo CSV manualmente.

Es posible que el archivo CSV no contenga todos los campos activos. Para todos los campos activos que no se actualizan en el archivo CSV cargado, el usuario debe introducir los datos de dichos campos activos.

Actualmente, todos los campos activos deben asignarse a algún campo desde el CSV de origen.

Sucede que, a veces, un usuario no desea asignar un campo activo a un campo especificado en el CSV. En estos casos, el usuario puede asignar el campo Activo al valor **[!UICONTROL DontImportFromSource]**. Seleccione este valor en la lista desplegable al importar usuarios desde conectores de FTP y Box.

## Funciones personalizadas {#customroles}

Añada cualquier campo que desee como parte de la información del usuario y haga clic en **[!UICONTROL Guardar]**. Después de agregar los campos, también puede comprobar la disponibilidad de los campos en el **[!UICONTROL Editar usuarios]** diálogo.

Después de agregar los campos, puede observar que los campos marcados con una marca de verificación proceden del origen de datos o del archivo CSV, como se indica en la captura de pantalla siguiente. El administrador puede editar estos campos de origen habilitando o deshabilitando los campos.

**Valores de campos activos en Learning Manager**

Los valores de los campos activos se obtienen de las siguientes maneras:

1. La aplicación Learning Manager importa metadatos de orígenes de datos asociados a su cuenta.
1. Metadatos capturados desde el archivo CSV importado manualmente.
1. Los alumnos rellenan metadatos al iniciar sesión
1. El administrador introduce los datos de los usuarios.

>[!NOTE]
>
>La aplicación Learning Manager crea grupos de usuarios automáticamente a partir de estos metadatos.

**Añadir valor personalizado**

Puede agregar un valor personalizado para los campos de usuario en los campos Usuario interno y Usuario externo.

Para añadir valores personalizados, siga estos pasos:

Los campos personalizados se pueden agregar y eliminar; son aplicables a todos los usuarios. Los campos CSV se pueden habilitar o deshabilitar; solo se aplican al cargar el archivo CSV después de realizar las modificaciones en los campos activos. Todos los campos activos internos son aplicables a todos los tipos de usuarios internos. Los campos externos solo se aplican a usuarios externos. Si un campo personalizado está presente en CSV, en la próxima carga se convierte automáticamente en un campo CSV y está habilitado.

## Valores para campos CSV {#valuesforcsvfields}

Los usuarios solo pueden elegir entre campos predefinidos para campos CSV si la **[!UICONTROL Restringir selección]** la casilla de verificación está activada.

![](assets/value-field-for-csv.png)
*Casilla de verificación Restringir selección*

## Importar registros {#importlogs}

En este espacio, puede ver el historial de importación de CSV para los usuarios que el administrador ha añadido mediante la función de importación en bloque. También puede hacer clic en **Añadir** en la esquina superior derecha de la página para añadir usuarios mediante la función de carga de CSV.

## Campos activos multivalor

Con esta función, puede tener más de un campo para un campo activo. En una cuenta, puede haber como máximo tres campos activos multivalor. Los campos activos multivalor están disponibles para usuarios internos y externos.

Una vez marcado un campo activo como multivalor, no puede volver a convertirlo en un solo valor. Esto es irreversible.

Un campo de un solo valor existente no se puede marcar como campo de varios valores.

Para crear un campo activo multivalor, siga los pasos que se indican a continuación:

1. Agregar un campo activo.

   ![Agregar un campo activo](assets/add-active-field.png)
   *Agregar un campo activo*

1. Haga clic en Agregar.
1. En la ficha Configuración, marque el nuevo campo como multivalor.

   ![Marcar como multivalor](assets/mark-multi-valued.png)
   *Marcar como multivalor*

   Hay otra casilla de verificación, **[!UICONTROL Configurable por el alumno]**, que cuando está desactivada, el alumno no podrá ver el campo en la página Perfil.

1. Añada los valores mediante un archivo CSV o haciendo clic en Modificar valores.

   ![Agregar valores](assets/add-values.png)
   *Agregar valores*

1. Haga clic en [!UICONTROL **Hecho**].

>[!NOTE]
>
>Una vez creado el grupo de usuarios y rellenado el campo, no se pueden convertir varios valores en valores individuales y viceversa.

### Agregar un campo activo multivalor mediante CSV

Siga estos pasos:

1. Cree un archivo CSV con los nuevos campos activos como columnas (valores separados por comas o valores individuales).
1. Importe el archivo CSV.
1. Marque los campos como multivalor en el cuadro de diálogo Valores en campos personalizados .
1. Vuelva a importar el archivo CSV.

El archivo CSV debe tener una columna con el mismo nombre que la de un campo activo marcado como multivalor.

El archivo CSV contiene los campos:

* **[!UICONTROL Usuario]**: grupos de usuarios creados como funciones.
* **[!UICONTROL Funciones]**: Campo activo multivalor con valores.

Si el archivo CSV se vuelve a cargar con nuevos valores o se eliminan valores, los campos y grupos activos también se actualizan en consecuencia.

### Informes

Todos los informes incluyen los campos activos multivalor y sus valores.

El administrador puede añadir campos activos generados automáticamente y configurar la actividad del usuario y los informes de formación.

El informe Transcripciones de alumnos contiene todos los campos activos y valores separados por comas. A continuación, el administrador puede filtrar los datos en consecuencia.

## Preguntas más frecuentes {#faq}

+++Cómo registrar usuarios en Learning Manager

Después de agregar un usuario y asignarle una función, puede registrarlo realizando los pasos que se indican a continuación:

1. Con el usuario o los usuarios seleccionados, haga clic en **[!UICONTROL Acciones]** en la esquina superior derecha y haga clic en **[!UICONTROL Registro]**.

1. En la ventana emergente, haga clic en **[!UICONTROL Sí]**.

Los usuarios seleccionados recibirán un correo electrónico de bienvenida. Si los alumnos ya tienen un Adobe ID, pueden hacer clic en este vínculo. Si no tienen un Adobe ID existente, pueden hacer clic en el vínculo Bienvenido para crear un Adobe ID y vincularlo a su cuenta de Learning Manager.

Es obligatorio que los alumnos hagan clic en uno de estos vínculos para que Learning Manager verifique sus cuentas.

+++

+++Cómo editar datos de usuarios?

Para editar un usuario, siga los pasos que se indican a continuación:

1. En la lista de usuarios, haga clic en el usuario cuyos datos desea editar.
1. Haga clic en el icono del lápiz, como se muestra a continuación.

![](assets/edit-user-data.png)

En la **[!UICONTROL Editar usuario]** , actualice los campos en consecuencia. Para guardar los cambios, haga clic en **[!UICONTROL Guardar]**.

+++

+++Cómo pausar y reanudar un usuario externo en Learning Manager

En la lista de usuarios externos, elija el usuario que desea eliminar. En la esquina superior derecha, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Pausa]**.

Para obtener más información, consulte [Pausar un perfil externo](add-users-user-groups.md#pause).

Después de pausar un perfil, el perfil externo muestra el estado como ***En pausa***.

+++

+++Cómo enviar el correo electrónico de bienvenida al perfil externo recién creado?

Al añadir un usuario externo, en el **[!UICONTROL Añadir perfil de registro externo]** , introduzca el correo electrónico del responsable externo. Al hacer clic en Guardar, también se envía un correo electrónico de bienvenida a la dirección de correo electrónico especificada. Si desea volver a enviar el correo de bienvenida, haga clic en el icono del sobre, como se muestra a continuación:

![](assets/send-welcome-mail.png)

+++

+++Cómo crear grupos de usuarios personalizados

Haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Grupos de usuarios]** y en la página Grupos de usuarios, haga clic en **[!UICONTROL Añadir]**. En el cuadro de diálogo Añadir grupo de usuarios, añada los usuarios de forma individual y como un equipo.

![](assets/custom-user-group.png)

+++

+++Cómo deshabilitar los campos activos ya rellenados?

Si desea que los alumnos solo vean los campos activos que no han rellenado, siga los pasos que se indican a continuación:

1. Haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Campos activos]**.

1. Haga clic en **[!UICONTROL Configuración]** y activar la opción **[!UICONTROL Mostrar solo campos sin rellenar al iniciar sesión como alumno]**.

1. Haga clic en **[!UICONTROL Guardar]**.

+++

+++Cómo evitar que los alumnos introduzcan valores aleatorios en los campos activos.

Puede restringir la selección de los alumnos para que solo puedan seleccionar los valores predefinidos y no introducir valores aleatorios. Siga estos pasos:

1. Haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Campos activos]**.
1. En la sección **[!UICONTROL Configurar campos]**, haga clic en **[!UICONTROL Modificar valores]**.

1. Active la opción **[!UICONTROL Restringir selección]**.
1. Haga clic en **[!UICONTROL Hecho]**.

+++

+++ ¿Cómo diferencio los campos activos de CSV de los campos activos personalizados?

Solo puede habilitar o deshabilitar los campos activos de CSV, pero no puede eliminarlos. Por otro lado, no puede habilitar ni deshabilitar campos activos personalizados.

+++
