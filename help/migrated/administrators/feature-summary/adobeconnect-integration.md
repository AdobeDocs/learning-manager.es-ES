---
jcr-language: en_us
title: Integración con Adobe Connect
description: Los autores pueden crear cursos de clase virtual con Adobe Connect durante el proceso de creación del curso. Para habilitar Adobe Connect en su cuenta de Learning Manager, debe ponerse en contacto con el administrador de su organización.
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---



# Integración con Adobe Connect

Los administradores de una empresa pueden configurar los ajustes de la cuenta de Learning Manager para habilitar la integración de Adobe Connect.

## Configurar Adobe Connect {#configureadobeconnect}

1. En el inicio de sesión del administrador, haga clic en **[!UICONTROL Configuración]** en el panel izquierdo para ver la información básica de su empresa. Haga clic en **[!UICONTROL Adobe Connect]** en el panel izquierdo.

   ![](assets/left-pane.png)

   *Seleccione Adobe Connect en el panel izquierdo*

1. Haga clic en **[!UICONTROL Configurar ahora]** enlace de entrada **[!UICONTROL Configuración de Adobe Connect]** sección.

   <!--![](assets/configure-now-connect.png)-->

1. Indique las credenciales de inicio de sesión y nombre de dominio de Adobe Connect de la empresa.

   ![](assets/adobeconnect-config.png)

   *Agregar nombre de dominio y credenciales*

   URL de Adobe Connect de ejemplo: mycompany.adobeconnect.com\
   Debe proporcionar el ID de correo electrónico del administrador de la cuenta de conexión de Adobe.

   Solo se admiten cuentas de conexión alojadas en el Adobe en Learning Manager. Ejemplo: &#39;.adobeconnect.com&#39;.

1. Haga clic en **[!UICONTROL Integrar].**

   Después de autenticar el ID de correo electrónico, Learning Manager muestra el mensaje cuando Connect se ha integrado correctamente. Puede empezar a ver sus cursos de clase virtual automáticamente con Adobe Connect.

   El administrador de la cuenta de Adobe Connect debe aceptar los Términos y condiciones de uso de Adobe Connect. Si esto no se acepta, su autenticación de inicio de sesión puede fallar. Después de crear la cuenta de Adobe Connect, inicie sesión en la cuenta una vez. Durante el primer inicio de sesión, aparece una página de términos y condiciones.

   <!--![](assets/mail-confirmation.png)-->

## Agregar información de sesión de clase virtual {#addvirtualclassroomsessioninformation}

Si el autor de un curso de clase virtual no ha proporcionado la información de la sesión, el administrador puede incluir los detalles de la sesión.

En el inicio de sesión del administrador, haga clic en el nombre del curso de clase virtual. Haga clic en **[!UICONTROL Instancias]** en el panel izquierdo y haga clic en **[!UICONTROL Detalles de sesión]**.  Haga clic en el icono Editar situado en la esquina derecha de la página Detalles de la sesión para añadir la información de la sesión.

![](assets/session-creation-admin.png)

*Agregar información de sesión de clase virtual*

Con la integración de Adobe Learning Manager y Adobe Connect para la creación de sesiones o módulos de clase virtual, su cuenta de Connect debe admitir salas de reuniones con un número adecuado de salas y usuarios simultáneos para su caso de uso. Estas salas de reuniones se utilizan para alojar módulos de clase virtual de Learning Manager. Learning Manager crea dinámicamente una nueva sala de reuniones de Connect para cada módulo de clase virtual o sesión de Learning Manager.

Debe adquirir Adobe Connect por separado, además de Adobe Learning Manager.

## Asistencia de alumnos {#learnersattendance}

Si el anfitrión del curso de clase virtual no asiste a la sesión, la asistencia no se registra automáticamente para los alumnos que asistieron a la sesión. En estos casos, el administrador puede registrar la asistencia manualmente.

Haga clic en el curso de clase virtual, haga clic en Asistencia en el panel izquierdo de la página siguiente y registre la asistencia.
