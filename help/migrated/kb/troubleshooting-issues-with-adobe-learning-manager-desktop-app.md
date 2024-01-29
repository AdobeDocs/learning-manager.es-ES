---
description: Este documento contiene sugerencias básicas para solucionar algunos de los problemas habituales que se producen al instalar y utilizar la aplicación de Adobe Learning Manager para escritorio.
jcr-language: en_us
title: Solución de problemas con la aplicación de Adobe Learning Manager para escritorio
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 0%

---



# Solución de problemas con la aplicación de Adobe Learning Manager para escritorio

Este documento contiene sugerencias básicas para solucionar algunos de los problemas habituales que se producen al instalar y utilizar la aplicación de Adobe Learning Manager para escritorio.

## No puedo hacer lo siguiente {#iamunabletodothefollowing}

+++No es posible descargar la aplicación de Adobe Learning Manager para escritorio

1. Compruebe la conexión a Internet y la configuración del firewall.
1. En Aprendizaje social, haga clic en **[!UICONTROL Nueva publicación]** para crear una publicación. Si no tiene un tablero, cree primero un tablero.
1. Haga clic en cualquiera de las siguientes opciones del botón Publicar que aparecen para crear contenido como Captura de pantalla, Grabar audio, Grabar vídeo o Galería de Learning Manager. Se le redirigirá a la página de la aplicación de Adobe Learning Manager para escritorio, desde la que puede descargar la aplicación de Adobe Learning Manager para escritorio.
1. Necesita una cuenta válida de Adobe Learning Manager que tenga habilitado Aprendizaje social. Es posible que el administrador también haya deshabilitado las descargas a través del explorador web. Póngase en contacto con el administrador de Adobe Learning Manager para obtener más información sobre la descarga de la aplicación de Adobe Learning Manager para escritorio.

+++

+++No es posible instalar la aplicación de Adobe Learning Manager para escritorio

1. Asegúrese de que el sistema cumpla los requisitos mínimos del sistema. Consulte [Requisitos del sistema de la aplicación Adobe Learning Manager para escritorio](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Corrija cualquier instalación anterior de la aplicación de Adobe Learning Manager para escritorio. Para obtener más información, consulte  [Cómo limpiar instalaciones anteriores](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) para obtener más información.
1. Para ver los errores durante el proceso de instalación, consulte [Cómo buscar registros de aplicaciones](#howtofindapplicationlogs). Póngase en contacto con el administrador de la aplicación de Adobe de Learning Manager para obtener más ayuda.

+++

+++No es posible iniciar la aplicación de Adobe Learning Manager para escritorio

1. Asegúrese de que la aplicación de Adobe Learning Manager para escritorio se haya descargado e instalado.
1. En Aprendizaje social, haga clic en **[!UICONTROL Nueva publicación]** (si no tiene un tablero, cree un tablero). Haga clic en cualquiera de las siguientes opciones del botón Publicar que aparecen: Realizar una captura de pantalla, Grabación de audio, Grabación de vídeo, Galería de Adobe de Learning Manager. Se le redirige a una página desde la que puede iniciar la aplicación de Adobe Learning Manager para escritorio.
1. En caso de que la aplicación no se inicie, también puede iniciarla desde el menú Inicio en Windows o desde Launchpad en Mac OS X.

+++

+++No es posible iniciar sesión en mi cuenta en la aplicación de Adobe Learning Manager para escritorio

1. Asegúrese de estar conectado a Internet y de que la configuración del firewall no bloquee la aplicación de Adobe Learning Manager para escritorio.
1. Asegúrese de tener una cuenta de alumno válida de Adobe Learning Manager con Aprendizaje social activado.
1. Si sigue sin poder iniciar sesión, salga y vuelva a iniciar la aplicación de Adobe Learning Manager para escritorio y vuelva a intentarlo.
1. Para obtener más ayuda, póngase en contacto con el administrador de Adobe Learning Manager.

+++

+++No puedo ver mi cámara web/micrófono en la aplicación de escritorio de Adobe Learning Manager

1. Asegúrese de que la cámara web o el micrófono estén correctamente conectados al sistema y funcionen correctamente.
1. Asegúrese de haber instalado los controladores más recientes para su cámara web o micrófono. Algunos dispositivos no funcionan correctamente sin controladores dedicados.
1. Restablezca las preferencias de la aplicación; a continuación, reinicie la aplicación de Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener más información, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Si está en Mac OS X Mojave 10.14, conceda permisos a la aplicación de Adobe Learning Manager para escritorio para acceder a su cámara web o micrófono. Para obtener más información, consulte [Cómo establecer permisos de cámara web / micrófono en OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++No puedo publicar mis publicaciones desde la aplicación de Adobe Learning Manager para escritorio

1. Asegúrese de tener una cuenta de alumno válida de Adobe Learning Manager con Aprendizaje social activado por el administrador de Adobe Learning Manager.
1. Restablezca las preferencias de la aplicación; a continuación, reinicie la aplicación de Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener más información, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Para detectar errores al publicar, habilite el registro avanzado. Para obtener más información, consulte [Cómo habilitar el registro avanzado](#howtoenableadvancedlogging), reinicie la aplicación de Adobe de Learning Manager para escritorio y repita los pasos anteriores que causaron el error. Envíe los registros de la aplicación más recientes al administrador de Adobe Learning Manager para obtener ayuda. Para obtener más información, consulte [Cómo buscar registros de aplicaciones](#howtofindapplicationlogs).

+++

+++No puedo ver ni abrir proyectos más antiguos

1. Solo puede ver los proyectos creados con su cuenta de Adobe Learning Manager en el mismo equipo en el que se crearon.
1. Restablezca las preferencias de la aplicación; a continuación, reinicie la aplicación de Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener ayuda, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Para ver los errores al abrir proyectos, habilite el registro avanzado. Para obtener más información, consulte [Cómo habilitar el registro avanzado](#howtoenableadvancedlogging). Reinicie la aplicación de Adobe de Learning Manager para escritorio y rehaga los pasos que causan el error. Envíe los registros de la aplicación más recientes al administrador de Adobe Learning Manager para obtener ayuda. Para obtener más información, consulte [Cómo buscar registros de aplicaciones](#howtofindapplicationlogs).

+++

## ¿Cómo restablecer las preferencias de la aplicación? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Para abrir el cuadro de diálogo Ejecutar, pulse la tecla **Windows + R** las llaves.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` y pulse Intro.
1. Elimine los archivos con nombre **preferences.json** y **preferences.xml**.

### MAC OS X {#macosx}

1. Abra el Finder.
1. Para abrir el **Ir a** cuadro de diálogo de carpeta, Prensa **Cmd + Mayús + G** las llaves.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` y pulse Intro.
1. Elimine los archivos con nombre **preferences.json** y **preferences.xml**.

## ¿Cómo se encuentran los registros de la aplicación? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Para abrir el cuadro de diálogo Ejecutar, presione **Windows + R** las llaves.
1. Tipo `**%TEMP%\\elthor**` y pulse Intro.
1. Ordenar las carpetas por **Fecha de modificación** y abra la carpeta más reciente. Esta carpeta contiene los registros de la aplicación más recientes.

### MAC OS X {#MacOSX-1}

1. Abrir **Finder**.
1. Para abrir el **Ir a la carpeta** , presione **Cmd + Mayús + G** las llaves.
1. Tipo &quot;**/var/folders**&quot; (sin comillas) y pulse Intro.
1. Buscar &quot;**elthor**&quot; en la barra de búsqueda y abra la carpeta.
1. Ordene las carpetas por **Fecha de modificación **y abra la carpeta más reciente. Esta carpeta contiene los registros de la aplicación más recientes.

## ¿Cómo se activa el registro avanzado? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.****
1. Tipo &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (sin comillas) y pulse Intro.****
1. Realizar una copia de seguridad del archivo **preferences.json** y luego ábralo en un editor de texto.****
1. Buscar la clave **debugMode** y cambie la propiedad value de esta clave a &quot;**verdadero**&quot; (sin comillas).

### MAC OS X {#MacOSX-2}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G**.
1. Tipo &quot;**~/Biblioteca/Application Support/Adobe/Learning Manager 1.0**&quot; (sin comillas) y pulse Intro.
1. Realizar una copia de seguridad del archivo **preferences.json** y, a continuación, ábralo en un editor de texto.
1. Buscar la clave **debugMode** y cambie la propiedad value de esta clave a &quot;**verdadero**&quot; (sin comillas)

## ¿Cómo se configuran los permisos de cámara web / micrófono en Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Haga clic en **[!UICONTROL Preferencias del sistema]** en el Dock.
1. Haga clic en **[!UICONTROL Seguridad y privacidad]** > **[!UICONTROL Privacidad].**
1. Haga clic en **[!UICONTROL Opciones de cámara web y micrófono]** y asegúrese de que la casilla de verificación Adobe Learning Manager esté seleccionada. Si no ve la lista Adobe Learning Manager, instale e inicie primero la aplicación de Adobe Learning Manager para escritorio.

## ¿Cómo limpiar la memoria caché de Adobe Learning Manager para actualizaciones de escritorio? {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` y pulse Intro.
1. Elimine la carpeta denominada **actualizaciones**.

### MAC OS X {#MacOSX-3}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G**.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` y pulse Intro.
1. Elimine la carpeta denominada **actualizaciones**.

## ¿Cómo se limpia la carpeta temporal de Adobe Learning Manager para escritorio? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.
1. Tipo &quot;**%TEMP%**&quot; (sin comillas) y pulse Intro.
1. Elimine la carpeta denominada &quot;**elthor**&quot;.

### MAC OS X {#MacOSX-4}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G** las llaves.
1. Tipo &quot;**/var/folders**&quot; (sin comillas) y pulse Intro.
1. Buscar &quot;**elthor**&quot; en la barra de búsqueda.
1. Elimine la carpeta denominada &quot;**elthor**&quot;.

## ¿Cómo se encuentra Adobe Learning Manager para proyectos de escritorio? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (sin comillas) y pulse Intro.
1. Es posible que usted o el administrador de Adobe Learning Manager hayan cambiado la ubicación predeterminada de la carpeta de proyectos. Póngase en contacto con el administrador para obtener más ayuda para localizar y limpiar proyectos.

### MAC OS X {#MacOSX-5}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G** las llaves.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (sin comillas) y pulse Intro.

   Es posible que usted o el administrador de Adobe Learning Manager hayan cambiado la ubicación predeterminada de la carpeta de proyectos. Póngase en contacto con el administrador para obtener más ayuda para localizar y limpiar proyectos.

## ¿Cómo se limpian las instalaciones anteriores de la aplicación de Adobe Learning Manager para escritorio? {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Para abrir el **Cuadro de diálogo Ejecutar,** prensa **Teclas Windows + R**.
1. Escriba regedit y busque &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (sin comillas) o &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (sin comillas) y pulse Intro.
1. Busque la carpeta denominada Adobe Learning Manager y busque la instalación anterior. Elimine la entrada del Registro.  Puede encontrar la tecla pulsando la tecla F3.

### MAC OS X {#MacOSX-6}

Mueva los archivos de la siguiente ruta &quot;**/Aplicaciones/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**&quot; para tirar la basura y luego vaciar la basura.
