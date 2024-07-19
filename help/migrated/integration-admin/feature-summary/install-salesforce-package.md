---
jcr-language: en_us
title: Instalar paquete de Salesforce
description: Learning Manager ofrece un paquete de la aplicación Salesforce. Una vez instalado y configurado en SFDC, los empleados de ventas pueden realizar sus actividades de formación en el portal de SFDC. Esta aplicación permite a los usuarios de SFDC explorar nuevas formaciones, ver recomendaciones y consumirlas directamente en el portal de SFDC. Los usuarios también reciben los anuncios enviados por los administradores en forma de membretes dentro de la aplicación dentro del portal de SFDC.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: fb946ae98dce45156e2f4c1cf992319405403ea9
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 47%

---

# Instalar paquete de Salesforce

## Información general

Learning Manager ofrece un paquete de la aplicación Salesforce. Una vez instalado y configurado en SFDC, los empleados de ventas pueden realizar sus actividades de formación en el portal de SFDC. Esta aplicación permite a los usuarios de SFDC explorar nuevas formaciones, ver recomendaciones y consumirlas directamente en el portal de SFDC. Los usuarios también reciben los anuncios enviados por los administradores en forma de membretes dentro de la aplicación dentro del portal de SFDC.

### Configurar en la aplicación Learning Manager

1. Inicie sesión en su cuenta de administrador de Learning Manager como administrador de integración.
1. Haga clic en **[!UICONTROL Aplicaciones]** > **[!UICONTROL Aplicaciones destacadas]**.
1. Haga clic en **[!UICONTROL Salesforce]**.
1. En la página de la aplicación de Salesforce, anote el ID de aplicación (también conocido como ID de cliente) y el secreto de cliente mencionado en la descripción.
1. Haz clic en **[!UICONTROL Aprobar]** y la aplicación debe aprobarse correctamente.
1. Haga clic en **[!UICONTROL Recursos de desarrolladores]** > **[!UICONTROL Tokens de acceso para pruebas y desarrollo]**.
1. En la sección Obtener código de OAuth, el ID de cliente y el ámbito deben establecerse en: admin:read,admin:write. Haga clic en **[!UICONTROL Enviar]**.
1. En Obtener token de actualización, introduzca el ID de cliente y el secreto de cliente. Haga clic en **[!UICONTROL Enviar]** y anote el token de actualización.

### Crear cuenta en la aplicación Salesforce

1. Cree una cuenta en la página de registro de Salesforce. Debe crear una cuenta de Salesforce en la edición para desarrolladores o empresas.  [URL de registro de desarrollador](https://developer.salesforce.com/signup). Asegúrese de que debe utilizar el ID de correo electrónico para registrarse en Salesforce que había utilizado para Learning Manager.
1. Compruebe su cuenta mediante el correo electrónico de verificación.
1. Cree una contraseña e inicie sesión en Salesforce.
1. Anote la URL de Salesforce después de iniciar sesión (por ejemplo, site.lightning.force.com)

### Instalar paquete de Learning Manager

Si desea instalar el paquete, primero debe eliminar el paquete existente en Salesforce. Antes de la desinstalación, debe activar la configuración, como se muestra a continuación. La aplicación de esta configuración es obligatoria; de lo contrario, no podrá instalar el paquete.

![](assets/uninstall-package.png)

*Instalar el paquete de Learning Manager*

>[!NOTE]
>
>La aplicación de Adobe Learning Manager solo se admite en la vista de Salesforce Lightning.

1. Inicie la [URL del paquete de Learning Manager](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP).
1. En la página **Inicio de sesión**, haga clic en **[!UICONTROL Usar dominio personalizado]**.

1. Introduzca la dirección URL del paquete y haga clic en **[!UICONTROL Continuar]**. La página de instalación debe tener seleccionada la opción Instalar solo para administradores . No cambie esta opción.
1. Haga clic en **Install**. Una vez instalado el paquete, haz clic en **[!UICONTROL Hecho]**. Se le guiará a la página Paquetes instalados y podrá ver el paquete instalado de Adobe Learning Manager.

1. Vaya al Iniciador de aplicaciones (junto a Configuración) y busque Adobe Learning Manager.
1. Para configurar la aplicación, haga clic en **[!UICONTROL Configurar]**.
1. Haga clic en **[!UICONTROL Nuevo]** y agregue los siguientes detalles:

   * **Configuración:** introduzca el nombre que desee.
   * **ClientID**: escriba el valor obtenido en la primera sección.
   * **Secreto de cliente:** Escriba el valor obtenido en la primera sección.
   * **Token de actualización:** Escriba el valor obtenido en la primera sección.
   * **LearningManagerBaseURL:** Dirección URL del sitio en el que se aloja Learning Manager.
   * **Desactivar redirección:** desactive la redirección a la página de inicio del alumno en Learning Manager.

>[!NOTE]
>
>Solo puede crear una configuración única. Si intenta añadir otra configuración, aparecerá un mensaje de error. La configuración asigna la cuenta de Salesforce a la cuenta del alumno.

### Agregar configuración de sitio remoto

1. En la esquina superior derecha de la página, haga clic en **[!UICONTROL Configuración]**.
1. En **Búsqueda rápida**, busque Configuración del sitio remoto.
1. Haga clic en **[!UICONTROL Nuevo sitio remoto]**.
1. Introduzca los detalles:

   1. **Nombre del sitio remoto:** introduzca el nombre que desee.
   1. **URL del sitio remoto:** la dirección URL del sitio en el que se aloja Learning Manager.

1. Inicie Learning Manager.

### Añadir el dominio de Adobe a las direcciones URL de confianza de Salesforce

Para añadir el dominio de Adobe a direcciones URL de confianza, siga estos pasos:

1. En la consola de Salesforce, vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Búsqueda rápida]**.
1. Busque **[!UICONTROL URL fiables]** y seleccione **[!UICONTROL Nueva URL de confianza]**.
1. Escriba un nombre en el campo **[!UICONTROL Nombre de API]**.
1. Escriba `*.adobe.com` en el campo URL.
1. Seleccione todas las casillas de verificación en **Directivas CSP** y guarde los cambios.
1. Edite el token de actualización de la aplicación de Salesforce y guárdelo.
1. Vuelva a iniciar la aplicación de Salesforce.

### Activar las notificaciones para la aplicación Learning Manager

1. En la esquina superior derecha, haga clic en **Configuración**.
1. Buscar notificaciones personalizadas.
1. Haga clic en **[!UICONTROL Nuevo]**.
1. Introduzca los siguientes datos:

   1. **Nombre de notificación personalizado:** LearningManagerNotification
   1. **Nombre de API:** LearningManagerNotification

1. Seleccione **Escritorio** y **Móvil** como canales compatibles.

1. Haga clic en **[!UICONTROL Guardar]**.
1. Para habilitar las notificaciones push para dispositivos móviles, siga los pasos que se indican a continuación:

   1. Instale la aplicación móvil de Salesforce en su teléfono móvil.
   1. Inicie sesión en la aplicación utilizando sus credenciales.
   1. Vaya a **Configuración** > **Configuración de entrega de notificaciones**.
   1. Añada Salesforce para iOS y Android.

### Desinstalar Learning Manager de Salesforce

1. En la aplicación Salesforce, vaya a Paquetes instalados.
1. Haga clic en **[!UICONTROL Desinstalar]**.

## Configurar Learning Manager para usuarios de Salesforce

La aplicación Learning Manager también está disponible para los usuarios que estén presentes en cualquier cuenta de Salesforce. El administrador de Salesforce puede añadir usuarios en función de los perfiles. Los perfiles de Salesforce son similares a los de Learning Manager. Por ejemplo, Administrador, Administrador de integración, Instructor, etc. El administrador de Salesforce también puede crear un perfil personalizado.

### Perfil

Como administrador de Salesforce, puede asignar los perfiles a los usuarios o crear un perfil personalizado.

>[!NOTE]
>
>Los usuarios deben estar presentes tanto en Salesforce como en Learning Manager.

![](assets/create-profile.png)

*Asignar un perfil a un alumno*

Al añadir un alumno, debe asignarle un perfil específico. A continuación, vaya a ese perfil y conceda el acceso requerido.

Para que los alumnos vean la aplicación de Learning Manager, debe activarla para todos los alumnos.

El siguiente paso es proporcionar el permiso para acceder a la aplicación Learning Manager.

![](assets/permission-set.png)

*Agregar permisos para obtener acceso a la aplicación de Learning Manager*

Al instalar el paquete, se crea un nuevo conjunto de permisos, **Usuario de Adobe Learning Manager**. Vaya al conjunto de permisos y, a continuación, agregue los usuarios.

Seleccione los usuarios y asigne los permisos correspondientes. Los alumnos ya pueden acceder a la aplicación Learning Manager.

A continuación, seleccione un perfil, por ejemplo, Perfil estándar de un usuario, y haga clic en el perfil. Haga clic en **[!UICONTROL Editar]** y, en la sección **Configuración de aplicación personalizada**, habilite la casilla de verificación **Adobe Learning Manager**. Esto hace que la aplicación sea accesible para el usuario.

En la sección **Ajustes de pestaña personalizados**, en la lista desplegable **Página de inicio del alumno**, seleccione la opción **[!UICONTROL Por defecto en]**.

Debe hacer que la aplicación esté visible para todos los perfiles.

Haga clic en **[!UICONTROL Guardar]** y los alumnos que pertenezcan a todos los perfiles tendrán acceso a la aplicación Learning Manager.
