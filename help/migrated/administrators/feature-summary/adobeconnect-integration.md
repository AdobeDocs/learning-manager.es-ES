---
jcr-language: en_us
title: Integración de Adobe Connect
description: Los autores pueden crear cursos de clase virtual con Adobe Connect durante el proceso de creación del curso. A fin de habilitar Adobe Connect para su cuenta de Learning Manager, debe ponerse en contacto con el administrador de su empresa.
contentowner: jayakarr
exl-id: 13458f93-9ea7-4aab-8b33-3c4f4dd5886d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 70%

---

# Integración de Adobe Connect

Los administradores de una empresa pueden configurar las opciones de la cuenta de Learning Manager para permitir la integración de Adobe Connect.

## Configurar Adobe Connect {#configureadobeconnect}

1. Tras iniciar sesión como administrador, haga clic en **[!UICONTROL Configuración]** en el panel izquierdo para ver la información básica de la empresa. Haga clic en **[!UICONTROL Adobe Connect]** en el panel izquierdo.

   ![](assets/left-pane.png)

   *Seleccione Adobe Connect en el panel izquierdo*

1. Haga clic en el vínculo **[!UICONTROL Configurar ahora]** en la sección **[!UICONTROL Configuración de Adobe Connect]**.

   <!--![](assets/configure-now-connect.png)-->

1. Indique las credenciales de inicio de sesión y nombre de dominio de Adobe Connect de la empresa.

   ![](assets/adobeconnect-config.png)

   *Agregar nombre de dominio y credenciales*

   URL de Adobe Connect de ejemplo: mycompany.adobeconnect.com\
   Debe proporcionar el ID de correo electrónico del administrador de la cuenta de conexión de Adobe.

   En Learning Manager, solo se admiten cuentas alojadas por Learning Manager. Ejemplo: &#39;.adobeconnect.com&#39;.

1. Haga clic en **[!UICONTROL Integrar].**

   Después de autenticar el ID de correo electrónico, Learning Manager muestra el mensaje cuando Connect se ha integrado correctamente. De este modo, ya puede empezar a ver sus cursos de clase virtual mediante Adobe Connect.

   El administrador de la cuenta de Adobe Connect debe aceptar los términos y condiciones del uso de Adobe Connect. Si no se acepta, su autenticación de inicio de sesión puede fallar. Después de crear la cuenta de Adobe Connect, inicie sesión en la cuenta una vez. La primera vez que se inicia sesión, aparece una página de términos y condiciones.

   <!--![](assets/mail-confirmation.png)-->

## Añadir información sobre la sesión de la clase virtual {#addvirtualclassroomsessioninformation}

Si el autor de un curso de clase virtual no ha proporcionado información sobre la sesión, el administrador puede incluir los datos de la sesión.

Tras iniciar sesión como administrador, haga clic en el nombre del curso de clase virtual. Haga clic en **[!UICONTROL Instancias]** en el panel izquierdo y haga clic en **[!UICONTROL Detalles de la sesión]**.  Haga clic en el icono Editar situado en la esquina derecha de la página Detalles de la sesión para añadir la información de la sesión.

![](assets/session-creation-admin.png)

*Agregar información de sesión de clase virtual*

Con la integración de Adobe Learning Manager y Adobe Connect para la creación de sesiones o módulos de clase virtual, su cuenta de Connect debe admitir salas de reuniones con un número adecuado de salas y usuarios simultáneos para su caso práctico. Estas salas de reuniones se usan para alojar módulos de clase virtual de Learning Manager. Learning Manager crea dinámicamente una sala de reuniones para cada sesión o módulo de aula virtual dentro de Learning Manager.

Adobe Connect se debe adquirir por separado de Adobe Learning Manager.

## Asistencia de los alumnos {#learnersattendance}

Si el anfitrión del curso de clase virtual no asiste a la sesión, la asistencia no se registra automáticamente en relación con los alumnos que asistieron a la sesión. En estos casos, el administrador puede registrar la asistencia manualmente.

Haga clic en el curso de clase virtual, haga clic en Asistencia en el panel izquierdo de la página siguiente y registre la asistencia.
