---
jcr-language: en_us
title: Configurar usuarios en Learning Manager
contentowner: shhivkum
preview: true
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---



# Configurar usuarios en Learning Manager

## Usuarios internos y externos {#internalandexternalusers}

En cualquier LMS, incluido Learning Manager, la gestión de usuarios es un aspecto importante. Learning Manager permite clasificar usuarios como internos y externos. Los usuarios internos son aquellos usuarios que pertenecen a una organización o grupo específicos. Por lo general, los usuarios de una empresa son usuarios internos. Estos usuarios tienen objetos de aprendizaje específicos con fechas límite específicas, asignadas por sus responsables o el administrador.

Por el contrario, los usuarios externos suelen ser usuarios temporales de una cuenta específica de Learning Manager. Estos usuarios pueden acceder a objetos de aprendizaje específicos haciendo clic en un vínculo externo temporal que reciben por correo electrónico. Los perfiles de usuario externos suelen tener una fecha de caducidad. Por ejemplo, una organización que realiza certificaciones para Java puede tener cualquier usuario que inicie sesión temporalmente para completar los cursos pertinentes y, a continuación, intente la certificación. Por lo general, los cursos de formación en aula y los cursos destinados a usuarios externos también tienen una capacidad limitada.

Siga leyendo para saber cómo añadir usuarios internos y externos en Learning Manager.

## Configurar usuarios externos {#setupexternalusers}

Como administrador, es posible que desee añadir usuarios externos, como empleados de organizaciones asociadas, a su cuenta de Learning Manager. Para añadir usuarios externos:

1. Desde el **[!UICONTROL **Administrador**]**página de inicio de sesión, haga clic en **[!UICONTROL **Usuarios**]** en el panel de navegación izquierdo.
1. En el cuadro **[!UICONTROL **Usuarios**]**página, haga clic en **[!UICONTROL **Externo**]** en el panel de navegación izquierdo. El sistema muestra la página Usuarios externos con una lista de usuarios externos (si procede).
1. Haga clic en **[!UICONTROL **Añadir**]** en la esquina superior derecha de la página.

   ![](assets/set-up-external-users-step3.png)

1. En el cuadro **[!UICONTROL **Añadir usuario**]**cuadro de diálogo emergente, los siguientes campos son obligatorios:

   * **[!UICONTROL **Nombre de perfil**:]**Especifique el nombre del perfil externo que está creando.
   * **[!UICONTROL ** Correo electrónico del responsable **:]** Especifique la dirección de correo electrónico del responsable del usuario externo.
   * **[!UICONTROL ** Asientos asignados **:]** Especifique el número de alumnos que pueden inscribirse en el curso.
   * **[!UICONTROL ** Vencimiento **:]** Especifique la fecha de caducidad tras la cual un usuario externo no puede registrar o consumir el curso.

1. Haga clic en **[!UICONTROL ** Configuración avanzada **.]**
1. Si lo desea, defina las siguientes opciones al crear un perfil externo:

   * **[!UICONTROL ** Agregar imagen **:]** Arrastre y suelte la imagen que desee. Esta imagen se muestra en la página del alumno para los usuarios.
   * **[!UICONTROL ** Requisito de inicio de sesión **:]** Especifique el número de días en los que el usuario debe iniciar sesión. Si el usuario externo supera este período de inicio de sesión, el alumno no puede acceder al objeto de aprendizaje ni utilizarlo.
   * **[!UICONTROL ** Dominios permitidos **:]** Especifique los dominios separados por una coma. Solo los usuarios con los dominios especificados pueden registrarse en la cuenta.
   * **[!UICONTROL ** Verificación por correo electrónico obligatoria **:]** Seleccione esta casilla si desea enviar un correo electrónico de verificación a los usuarios



1. Haga clic en **[!UICONTROL Ahorra un.]**



   ![](assets/set-up-external-users-step7.png)

   Se muestra un cuadro de diálogo emergente con la dirección URL. Puede copiar esta dirección URL y enviarla a los usuarios externos. De forma predeterminada, se envía al usuario un correo electrónico con esta dirección URL.

1. A medida que añada perfiles externos, se mostrarán en el **[!UICONTROL ** Página Usuarios externos **(** Administrador **>** Usuarios **>** Externo **).]** El límite de licencias, la fecha de caducidad y los requisitos de inicio de sesión también se muestran para estos usuarios.
1. Para editar la configuración de un usuario externo en cualquier momento, haga clic en el nombre de usuario. La **[!UICONTROL Editar inscripción externa]** que aparece. Modifique la configuración y haga clic en **[!UICONTROL ** Guardar **.]**
1. También puede volver a enviar el correo electrónico de bienvenida o copiar la dirección URL en cualquier momento haciendo clic en los iconos de dirección URL de correo electrónico/copia junto al perfil externo.

   ![](assets/set-up-external-users-step10.png)

## Pausar el perfil de usuario externo {#pausetheexternaluserprofile}

Después de añadir un grupo de usuarios externos a Learning Manager, también puede pausar el proceso de registro de usuarios externos. Al pausar, el proceso de registro de usuarios externos se bloquea. Sin embargo, este proceso solo funciona cuando los usuarios aún no se han registrado al aceptar la invitación.

Para pausar los grupos de usuarios externos, haga clic en **[!UICONTROL **Acciones**]** en la esquina superior derecha de la página y seleccione **[!UICONTROL Pausa]**.

## Reanudar perfil de usuario externo {#resumeexternaluserprofile}

En cualquier momento, siempre puede revocar el bloqueo (pausa) eligiendo una opción de Reanudar . Haga clic en **[!UICONTROL **Acciones**]** en la esquina superior derecha de la página y seleccione **[!UICONTROL Currículum]**.

**[!UICONTROL Estados de usuario externos]**

En Learning Manager, los siguientes estados son aplicables a los usuarios externos:

* **Estado inactivo** - En este estado, el registro de usuarios externos ha caducado. Los administradores establecen la fecha de caducidad de los usuarios externos al añadirlos a través del flujo de trabajo Añadir usuario .
* **Estado activo** - En este estado, los usuarios externos pueden registrarse en la aplicación de Learning Manager e iniciar sesión en la aplicación.
* **Pausa** - En este estado, el proceso de registro para usuarios externos está bloqueado. Sin embargo, los usuarios existentes pueden seguir iniciando sesión.

## Configurar usuarios internos {#setupinternalusers}

Como administrador, es posible que desee configurar usuarios para su empresa u organización. Estos usuarios también se denominan usuarios internos. Los usuarios internos pueden iniciar sesión en la aplicación mediante el inicio de sesión único o mediante Adobe ID. Estos usuarios pueden acceder a los objetos de aprendizaje y utilizarlos según sus necesidades. Para configurar usuarios internos de una organización, existen tres formas posibles:

* Añadir usuarios en bloque mediante un CSV
* Adición de usuarios mediante el registro automático
* Añadir un único usuario interno



## Adición de usuarios mediante un archivo CSV {#addingusersusingacsvfile}

Puede elegir este método para añadir usuarios internos si el número de usuarios es grande. Cuando utilice un archivo CSV para agregar usuarios por primera vez, debe asignar el contenido de los datos del archivo CSV a las etiquetas de la aplicación. Posteriormente, cuando se agregan nuevos usuarios o se actualizan los datos de los usuarios, se mantiene la misma asignación. Para añadir usuarios internos en bloque:

1. En la **[!UICONTROL Inicio del administrador]** , haga clic en **[!UICONTROL **Usuarios**]** en el panel de navegación izquierdo.
1. Haga clic en **[!UICONTROL ** Añadir **>** Cargar un CSV **.]**
1. En el cuadro de diálogo emergente, haga clic en **[!UICONTROL ** Importar **.]**
1. Vaya a la ubicación donde haya guardado el archivo CSV. Haga clic en **[!UICONTROL Abrir]**.
1. Importe el archivo CSV y asigne el contenido del archivo CSV con las etiquetas de la aplicación. Este paso solo se aplica cuando carga el archivo CSV por primera vez.
1. Haga clic en **[!UICONTROL **Guardar**]** para guardar la asignación.
1. Haga clic en **[!UICONTROL **Añadir**]** para cargar el archivo CSV que ya está asignado a los datos de la aplicación.

### Consideraciones al crear el archivo CSV para la carga: {#considerationswhencreatingthecsvfileforupload}

Al crear el archivo CSV para cargar usuarios internos, a continuación se indican algunos de los campos obligatorios para los que debe introducir datos: Nombre del empleado, Correo electrónico del empleado, Perfil o designación del empleado y Jerarquía del responsable.

El nombre y el correo electrónico de cada empleado se pueden asignar directamente a los datos de la aplicación. Tenga en cuenta que debe especificar un correo electrónico que se especifique en el archivo CSV, como correo electrónico del responsable. Puede definir el ID de responsable al crear el archivo CSV o especificar el ID de correo electrónico que corresponda al ID de responsable al cargar el archivo CSV.

***Antes de añadir un ID como ID de responsable de un empleado, asegúrese de que el responsable se añade como empleado en el archivo CSV.***

***Asegúrese de que no haya espacios adicionales entre las entradas para cargar correctamente el archivo CSV.***

Vea una captura de pantalla de ejemplo de un archivo CSV aquí:

![](assets/considerations-whencreatingthecsvfileforupload.png)

Para descargar un archivo CSV de muestra, descargue `<give link to zip file>`.

<!--Zip file reference, no source file-->

### Configuración del usuario raíz {#settinguprootuser}

Automatizar la importación masiva de usuarios.

## Adición de usuarios mediante el registro automático {#addingusersthroughselfregistration}

Además de añadir usuarios internos de forma masiva, también puede añadir usuarios mediante el registro automático. Puede usar el registro automático para permitir que los empleados se registren como alumnos en su cuenta de Learning Manager. Al crear un perfil de registro automático, se crea una dirección URL única. Comparta esta dirección URL con el empleado para permitirle registrarse en Learning Manager.

1. En la **[!UICONTROL Inicio del administrador]** página, haga clic en **[!UICONTROL Usuarios]** en el panel de navegación izquierdo.
1. Haga clic en **[!UICONTROL ** Añadir **>** Registro automático **.]**

   ![](assets/adding-users-throughself-registration-step2.png)

1. En la **[!UICONTROL Añadir usuario]** cuadro de diálogo emergente, especifique el nombre del empleado en el **[!UICONTROL Nombre de perfil]** campo.
1. En la **[!UICONTROL Nombre del responsable]** , introduzca el nombre del responsable del empleado.
1. Si lo desea, puede añadir la imagen de perfil del empleado mediante la **[!UICONTROL Agregar imagen]** campo.
1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/adding-users-throughself-registration-step6.png)

   El sistema muestra otro cuadro de diálogo emergente con el mensaje de que el perfil se ha creado correctamente. En este cuadro de diálogo también se genera una dirección URL única.

1. Comparta esta dirección URL con el empleado para permitir que este se registre como alumno.

   ![](assets/adding-users-throughself-registration-step7.png)

## Añadir usuarios individuales en Learning Manager {#addsingleusersincaptivateprime}

Añadir usuarios individuales es el tercer método con el que puede añadir usuarios internos a su cuenta. Cuando se desea añadir algunos usuarios, este procedimiento es ideal. Para agregar un solo usuario:

1. En la **[!UICONTROL Inicio del administrador]** página, haga clic en **[!UICONTROL Usuarios]** en el panel de navegación izquierdo.
1. Haga clic en **[!UICONTROL ** Añadir **>** Usuario único **.]**



1. En el cuadro de diálogo emergente Añadir usuario, especifique los siguientes detalles para los usuarios:

   * **[!UICONTROL Nombre]** **[!UICONTROL :]** Especifique el nombre del empleado o usuario interno. Este campo es obligatorio.

   * **[!UICONTROL Correo electrónico]** **[!UICONTROL :]** Especifique el ID de correo electrónico del empleado. Este campo es obligatorio.

   * **[!UICONTROL Perfil]** **[!UICONTROL :]** Especifique la designación o el puesto del empleado.

   * **[!UICONTROL ** Nombre del responsable **:]** Especifique el nombre del responsable. El responsable ya debe agregarse a la base de datos que se va a especificar aquí.
   * **[!UICONTROL ** DOJ **:]** Especifique la fecha de incorporación del empleado.
   * **[!UICONTROL **Ubicación**:]**Especifique la ubicación del empleado. Por ejemplo, si tiene su organización en varias ubicaciones geográficas, especifique la ubicación en la que se encuentra el empleado.



   ![](assets/add-single-usersincaptivateprime-step3.png)

1. Haga clic en **[!UICONTROL Añadir]**.
1. El sistema muestra un mensaje que indica que el usuario se ha añadido correctamente. El usuario recibe un vínculo de verificación en el ID de correo electrónico especificado. El usuario puede hacer clic en este vínculo para activar su cuenta y comenzar a acceder a Learning Manager.

   ![](assets/add-single-usersincaptivateprime-step5.png)

## Administración de grupos de usuarios en Learning Manager {#managingusergroupsincaptivateprime}

El grupo de usuarios no es más que un conjunto de usuarios pertenecientes a una categoría definida. Como administrador, puede utilizar grupos de usuarios para seleccionar alumnos rápidamente en función de sus atributos. Además, puede asignar rápidamente logotipos o catálogos al grupo de usuarios y generar informes personalizados sobre su progreso.

Hay dos tipos de grupos de usuarios en Learning Manager: Personalizados y Generados automáticamente. Al añadir alumnos a su cuenta, se crean automáticamente algunos grupos predeterminados en función de las funciones y propiedades de los usuarios de su cuenta. Estos grupos son los que se generan automáticamente. Por ejemplo, un grupo con todos los alumnos o todos los autores.

***No se puede editar el nombre y la descripción de los grupos generados automáticamente.***

Para ver los grupos de usuarios generados automáticamente en Learning Manager, en el panel izquierdo, haga clic en **[!UICONTROL Generado automáticamente]**. La aplicación muestra una lista de todos los grupos de usuarios generados automáticamente disponibles para su cuenta.

También puede crear grupos personalizados con una lista seleccionada de usuarios en Learning Manager. Los grupos personalizados permiten especificar un nombre, una descripción y los atributos del grupo de usuarios. Los grupos personalizados creados en Learning Manager son de naturaleza dinámica. Es decir, si se agregan nuevos usuarios con atributos similares, se agregan automáticamente a estos grupos de usuarios.

## Crear grupos de usuarios personalizados {#createcustomusergroups}

1. En la página de inicio del administrador de Learning Manager, haga clic en **[!UICONTROL Usuarios]**.
1. En la página Grupos de usuarios personalizados, haga clic en **[!UICONTROL **Añadir**]** en la esquina superior derecha de la página.

   El sistema muestra la **[!UICONTROL Añadir grupo de usuarios]** del cuadro de diálogo.

   ![](assets/creating-custom-usergroups.png)

1. Especifique el nombre y la descripción del grupo de usuarios. Por ejemplo, Dev-Users, que incluye usuarios del equipo de desarrollo de productos.
1. Añada usuarios al grupo de usuarios personalizado introduciendo el nombre de usuario o el perfil del usuario en el **[!UICONTROL ** Añadir usuarios **campo.]**
1. Para añadir más usuarios al grupo personalizado, haga clic en **[!UICONTROL ** Añadir más usuarios **.]**
1. Después de añadir a todos los usuarios, haga clic en **[!UICONTROL Guardar]** para guardar el grupo de usuarios personalizado.

