---
jcr-language: en_us
title: Instalar paquete de Salesforce
description: Learning Manager ofrece un paquete de la aplicación Salesforce. Una vez instalado y configurado en SFDC, los empleados de ventas pueden realizar sus actividades de formación en el portal de SFDC. Esta aplicación permite a los usuarios de SFDC explorar nuevos cursos de formación, ver recomendaciones y consumirlas directamente en el portal de SFDC. Los usuarios también reciben los anuncios enviados por los administradores en forma de membretes dentro de la aplicación dentro del portal de SFDC.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---



# Instalar paquete de Salesforce

## Resumen

Learning Manager ofrece un paquete de la aplicación Salesforce. Una vez instalado y configurado en SFDC, los empleados de ventas pueden realizar sus actividades de formación en el portal de SFDC. Esta aplicación permite a los usuarios de SFDC explorar nuevos cursos de formación, ver recomendaciones y consumirlas directamente en el portal de SFDC. Los usuarios también reciben los anuncios enviados por los administradores en forma de membretes dentro de la aplicación dentro del portal de SFDC.

### Configurar en la aplicación de Learning Manager

1. Inicie sesión en su cuenta de administrador de Learning Manager como administrador de integración.
1. Haga clic en **[!UICONTROL Aplicaciones]** > **[!UICONTROL Aplicaciones destacadas]**.
1. Haga clic en **[!UICONTROL Salesforce]**.
1. En la página de la aplicación de Salesforce, anote el ID de aplicación (también conocido como ID de cliente) y el secreto de cliente mencionado en la descripción.
1. Haga clic en **[!UICONTROL Aprobar]** y la aplicación debe aprobarse correctamente.
1. Haga clic en **[!UICONTROL Recursos para desarrolladores]** > **[!UICONTROL Tokens de acceso para pruebas y desarrollo]**.
1. En la sección Obtener código de OAuth, el ID de cliente y el ámbito deben establecerse en: admin:read,admin:write. Haga clic en **[!UICONTROL Enviar]**.
1. En Obtener token de actualización, introduzca el ID de cliente y el secreto de cliente. Haga clic en **[!UICONTROL Enviar]** y anote el token de actualización.

### Crear cuenta en la aplicación Salesforce

1. Cree una cuenta en la página de registro de Salesforce . Debe crear una cuenta de Salesforce en la edición para desarrolladores o empresas.  [URL de registro de desarrollador](https://developer.salesforce.com/signup). Asegúrese de que debe utilizar el ID de correo electrónico para registrarse en Salesforce que había utilizado para Learning Manager.
1. Verifique su cuenta a través del correo electrónico de verificación.
1. Cree una contraseña e inicie sesión en Salesforce.
1. Anote la URL de Salesforce después de iniciar sesión (por ejemplo, site.lightning.force.com)

### Instalar paquete de Learning Manager

Si desea instalar el paquete, primero debe eliminar el paquete existente en Salesforce. Antes de la desinstalación, debe habilitar los ajustes, como se muestra a continuación. La aplicación de esta configuración es obligatoria; de lo contrario, no podrá instalar el paquete.

![](assets/uninstall-package.png)

*Instalar el paquete de Learning Manager*

>[!NOTE]
>
>La aplicación Adobe Learning Manager solo se admite en la vista de Salesforce Lightning.

1. Inicie el  [URL del paquete de Learning Manager](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. En la **Inicio de sesión** página, haga clic en **[!UICONTROL Usar dominio personalizado]**.

1. Introduzca la URL del paquete y haga clic en **[!UICONTROL Continuar]**. La página de instalación debe tener seleccionada la opción Instalar solo para administradores . No cambie esta opción.
1. Haga clic en **Insalto**. Una vez instalado el paquete, haga clic en **[!UICONTROL Hecho]**. Se le guiará a la página Paquetes instalados y podrá ver el paquete instalado de Adobe Learning Manager.

1. Vaya al Iniciador de aplicaciones (junto a Configuración) y busque Adobe Learning Manager.
1. Para configurar la aplicación, haga clic en **[!UICONTROL Configurar]**.
1. Haga clic en **[!UICONTROL Nuevo]** y añada los siguientes detalles:

   * **Configuración:** Introduzca el nombre que desee.
   * **ClientID**: introduzca el valor obtenido en la primera sección.
   * **SecretoDeCliente:** Introduzca el valor obtenido en la primera sección.
   * **Token de actualización:** Introduzca el valor obtenido en la primera sección.
   * **URLbase de LearningManager:** La dirección URL del sitio en el que se aloja Learning Manager.
   * **Desactivar redirección:** Desactive la redirección a la página de inicio del alumno en Learning Manager.

>[!NOTE]
>
>Solo puede crear una configuración única. Si intenta agregar otra configuración, verá un mensaje de error. La configuración asigna la cuenta de Salesforce a la cuenta de alumno.

### Agregar configuración de sitio remoto

1. En la esquina superior derecha de la página, haga clic en **[!UICONTROL Configuración]**.
1. En **Búsqueda rápida**, busque Configuración del sitio remoto.
1. Haga clic en **[!UICONTROL Nuevo sitio remoto]**.
1. Introduzca los detalles:

   1. **Nombre del sitio remoto:** Introduzca el nombre que desee.
   1. **URL del sitio remoto:** La dirección URL del sitio en el que se aloja Learning Manager.

1. Inicie Learning Manager.

### Habilitar notificaciones para la aplicación Learning Manager

1. En la esquina superior derecha, haga clic en **Configuración**.
1. Busque Notificaciones personalizadas.
1. Haga clic en **[!UICONTROL Nuevo]**.
1. Introduzca los siguientes datos:

   1. **Nombre de notificación personalizado:** NotificaciónDeLearningManager
   1. **Nombre de API:** NotificaciónDeLearningManager

1. Seleccione ambos **Escritorio** y **Móvil** como canales compatibles.

1. Haga clic en **[!UICONTROL Guardar]**.
1. Para habilitar las notificaciones automáticas para dispositivos móviles, siga los pasos que se indican a continuación:

   1. Instale la aplicación móvil de Salesforce en su teléfono móvil.
   1. Inicie sesión en la aplicación usando sus credenciales.
   1. Vaya a **Configuración** > **Configuración de entrega de notificaciones**.
   1. Añada Salesforce para iOS y Android.

### Desinstalar Learning Manager de Salesforce

1. En la aplicación Salesforce, vaya a Paquetes instalados.
1. Haga clic en **[!UICONTROL Desinstalar]**.

## Configurar Learning Manager para usuarios de Salesforce

La aplicación Learning Manager también está disponible para los usuarios que estén presentes en cualquier cuenta de Salesforce. El administrador de Salesforce puede añadir usuarios en función de los perfiles. Los perfiles de Salesforce son similares a los del Administrador de aprendizaje. Por ejemplo, administrador, administrador de integración, instructor, etc. El administrador de Salesforce también puede crear un perfil personalizado.

### Perfil

Como administrador de Salesforce, puede asignar los perfiles a los usuarios o crear un perfil personalizado.

>[!NOTE]
>
>Los usuarios deben estar presentes tanto en Salesforce como en Learning Manager.

![](assets/create-profile.png)

*Asignar un perfil a un alumno*

Al añadir un alumno, debe asignarle un perfil específico. A continuación, vaya a ese perfil y conceda el acceso requerido.

Para que los alumnos vean la aplicación de Learning Manager, debe activarla para todos los alumnos.

El siguiente paso es proporcionar permiso para acceder a la aplicación de Learning Manager.

![](assets/permission-set.png)

*Añadir permisos para acceder a la aplicación de Learning Manager*

Al instalar el paquete, se crea un nuevo conjunto de permisos, **Usuario de Adobe Learning Manager**. Vaya al conjunto de permisos y, a continuación, agregue los usuarios.

Seleccione los usuarios y asigne los permisos correspondientes. Los alumnos ahora pueden acceder a la aplicación de Learning Manager.

A continuación, seleccione un perfil, por ejemplo, Perfil estándar de un usuario, y haga clic en el perfil. Haga clic en **[!UICONTROL Editar]** y en el **Configuración personalizada de la aplicación** , active la casilla de verificación **Adobe Learning Manager**. Esto hace que la aplicación sea accesible para el usuario.

En la **Ajustes de pestaña personalizados** , en la sección **Inicio del alumno** lista desplegable, seleccione la opción **[!UICONTROL Predeterminado en]**.

Debe hacer que la aplicación esté visible para todos los perfiles.

Haga clic en **[!UICONTROL Guardar]** y los alumnos que pertenezcan a todos los perfiles accederán a la aplicación de Learning Manager.
