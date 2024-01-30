---
description: Este documento contiene consejos para la resolución básica de los problemas típicos que pueden producirse al instalar y utilizar la aplicación Adobe Learning Manager para escritorio.
jcr-language: en_us
title: Solución de problemas con la aplicación Adobe Learning Manager para escritorio
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 53%

---



# Solución de problemas con la aplicación Adobe Learning Manager para escritorio

Este documento contiene consejos para la resolución básica de los problemas típicos que pueden producirse al instalar y utilizar la aplicación Adobe Learning Manager para escritorio.

## No es posible efectuar lo siguiente {#iamunabletodothefollowing}

+++No es posible descargar la aplicación de Adobe Learning Manager para escritorio

1. Compruebe la conexión a Internet y la configuración del servidor de seguridad.
1. En Aprendizaje social, haga clic en **[!UICONTROL Nueva publicación]** para crear una publicación. Si no tiene un tablero, cree primero un tablero.
1. Haga clic en cualquiera de las opciones siguientes de publicación que aparecen para crear contenido como Capturar pantalla, Grabar audio, Grabar vídeo o Galería de Learning Manager. Se le redirige a la página de la aplicación Adobe Learning Manager para escritorio; en ella, puede descargar esa aplicación en su equipo.
1. Debe tener una cuenta válida de Adobe Learning Manager con Aprendizaje social activado por el administrador. Es posible que el administrador también haya desactivado las descargas a través del navegador web. Póngase en contacto con su administrador de Adobe Learning Manager para obtener más información sobre cómo descargar la aplicación Adobe Learning Manager para escritorio.

+++

+++No es posible instalar la aplicación de Adobe Learning Manager para escritorio

1. Asegúrese de que el sistema cumpla los requisitos mínimos. Consulte [Requisitos del sistema de la aplicación Adobe Learning Manager para escritorio](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Elimine cualquier instalación anterior de la aplicación Adobe Learning Manager para escritorio. Para obtener más información, consulte  [Cómo limpiar instalaciones anteriores](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) para obtener más información.
1. Para ver los errores durante el proceso de instalación, consulte [Cómo buscar registros de aplicaciones](#howtofindapplicationlogs). Póngase en contacto con el administrador de la aplicación Adobe Learning Manager para escritorio a fin de obtener más ayuda.

+++

+++No es posible iniciar la aplicación de Adobe Learning Manager para escritorio

1. Compruebe que haya descargado e instalado la aplicación Adobe Learning Manager para escritorio.
1. En Aprendizaje social, haga clic en **[!UICONTROL Nueva publicación]**. Si no tiene un tablero, créelo. Haga clic en cualquiera de las siguientes opciones del botón Publicar que aparecen: Realizar una captura de pantalla, Grabación de audio, Grabación de vídeo, Galería de Adobe de Learning Manager. Se le redirige una página en la que puede iniciar la aplicación Adobe Learning Manager para escritorio.
1. Si la aplicación no se abre, también puede abrirla desde el menú Inicio de Windows o en el Launchpad de macOS X.

+++

+++No es posible iniciar sesión en mi cuenta en la aplicación de Adobe Learning Manager para escritorio

1. Compruebe que tenga conexión a Internet y que la configuración del servidor de seguridad no bloquee la aplicación Adobe Learning Manager para escritorio.
1. Compruebe que disponga de una cuenta válida de alumno de Adobe Learning Manager y que Aprendizaje social esté activado.
1. Si continúa sin poder iniciar sesión, cierre y vuelva a iniciar la aplicación Adobe Learning Manager para escritorio, e inténtelo de nuevo.
1. Para obtener más información, póngase en contacto con el administrador de Adobe Learning Manager.

+++

+++No puedo ver mi cámara web/micrófono en la aplicación de escritorio de Adobe Learning Manager

1. Asegúrese de que la cámara web o el micrófono estén bien conectados al sistema y que funcionen correctamente.
1. Asegúrese de haber instalado los controladores más recientes para su cámara web o micrófono. Algunos dispositivos no funcionan correctamente sin controladores dedicados.
1. Restablezca las preferencias de la aplicación, inicie de nuevo aplicación Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener más información, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Si se utiliza macOS X Mojave 10.14, conceda permisos de acceso a la cámara web o al micrófono a la aplicación Adobe Learning Manager para escritorio. Para obtener más información, consulte [Cómo definir permisos para la cámara web o el micrófono en macOS Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++No puedo publicar mis publicaciones desde la aplicación de Adobe Learning Manager para escritorio

1. Compruebe que disponga de una cuenta válida de alumno de Adobe Learning Manager y que el administrador de Adobe Learning Manager haya activado Aprendizaje social.
1. Restablezca las preferencias de la aplicación, inicie de nuevo aplicación Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener más información, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Para detectar errores al publicar, habilite el registro avanzado. Para obtener más información, consulte [Cómo activar la generación de registros avanzados](#howtoenableadvancedlogging), reinicie la aplicación Adobe Learning Manager para escritorio y reproduzca los pasos que producen el error. Envíe los registros más recientes de la aplicación al administrador de Adobe Learning Manager para obtener ayuda. Para obtener más información, consulte [Cómo buscar los registros de la aplicación](#howtofindapplicationlogs).

+++

+++No puedo ver ni abrir proyectos más antiguos

1. Solo es posible ver los proyectos creados con la cuenta de Adobe Learning Manager en el mismo equipo en el que se crearon.
1. Restablezca las preferencias de la aplicación, inicie de nuevo aplicación Adobe Learning Manager para escritorio e inténtelo de nuevo. Para obtener ayuda, consulte [Cómo restablecer las preferencias de la aplicación](#howtoresetapplicationpreferences).
1. Para ver los errores al abrir proyectos, habilite el registro avanzado. Para obtener más información, consulte [Cómo habilitar el registro avanzado](#howtoenableadvancedlogging). Reinicie la aplicación Adobe Learning Manager para escritorio y reproduzca los pasos que producen el error. Envíe los registros más recientes de la aplicación al administrador de Adobe Learning Manager para obtener ayuda. Para obtener más información, consulte [Cómo buscar los registros de la aplicación](#howtofindapplicationlogs).

+++

## ¿Cómo restablecer las preferencias de la aplicación? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Para abrir el cuadro de diálogo Ejecutar, pulse la tecla **Windows + R** las llaves.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` y pulse Intro.
1. Elimine los archivos **preferences.json** y **preferences.xml**.

### MAC OS X {#macosx}

1. Abra el Finder.
1. Para abrir el **Ir a** cuadro de diálogo de carpeta, Prensa **Cmd + Mayús + G** las llaves.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` y pulse Intro.
1. Elimine los archivos **preferences.json** y **preferences.xml**.

## Cómo buscar los registros de la aplicación {#howtofindapplicationlogs}

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
1. Efectúe una copia de seguridad del archivo **preferences.json** y ábralo en un editor de texto.
1. Buscar la clave **debugMode** y cambie la propiedad value de esta clave a &quot;**verdadero**&quot; (sin comillas)

## ¿Cómo se configuran los permisos de cámara web / micrófono en Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Haga clic en **[!UICONTROL Preferencias del sistema]** en el Dock.
1. Haga clic en **[!UICONTROL Seguridad y privacidad]** > **[!UICONTROL Privacidad].**
1. Haga clic en **[!UICONTROL Cámara web o en Micrófono]** y compruebe que esté seleccionada la casilla Adobe Learning Manager. Si no aparece Adobe Learning Manager, instale e inicie la aplicación Adobe Learning Manager para escritorio.

## Cómo limpiar la memoria caché de actualizaciones de Adobe Learning Manager para escritorio {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` y pulse Intro.
1. Elimine la carpeta **updates**.

### MAC OS X {#MacOSX-3}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G**.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` y pulse Intro.
1. Elimine la carpeta **updates**.

## Cómo limpiar la carpeta de archivos temporales de Adobe Learning Manager para escritorio {#howtocleanupadobecaptivateprimefordesktoptempfolder}

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

## Cómo buscar proyectos de Adobe Learning Manager para escritorio {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Para abrir el cuadro de diálogo Ejecutar, pulse **Tecla Windows + R**.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (sin comillas) y pulse Intro.
1. Es posible que usted o el administrador de Adobe Learning Manager hayan cambiado la ubicación predeterminada de la carpeta de proyectos. Póngase en contacto con el administrador para obtener más ayuda para localizar y limpiar proyectos.

### MAC OS X {#MacOSX-5}

1. Abra el Finder.
1. Para abrir el **Ir a la carpeta** diálogo, presione **Cmd + Mayús + G** las llaves.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (sin comillas) y pulse Intro.

   Es posible que usted o el administrador de Adobe Learning Manager hayan cambiado la ubicación predeterminada de la carpeta de proyectos. Póngase en contacto con el administrador para obtener más ayuda a fin de localizar y limpiar proyectos.

## Cómo eliminar instalaciones anteriores de la aplicación Adobe Learning Manager para escritorio {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Para abrir el **Cuadro de diálogo Ejecutar,** prensa **Teclas Windows + R**.
1. Escriba regedit y busque &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (sin comillas) o &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (sin comillas) y pulse Intro.
1. Busque la carpeta Adobe Learning Manager y la instalación anterior. Elimine la entrada del Registro.  Puede encontrar la tecla pulsando la tecla F3.

### MAC OS X {#MacOSX-6}

Mueva los archivos de la siguiente ruta &quot;**/Aplicaciones/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**&quot; para tirar la basura y luego vaciar la basura.
