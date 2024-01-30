---
jcr-language: en_us
title: Notificaciones
description: La función Notificaciones es aplicable a todos los usuarios de Adobe Learning Manager. Sin embargo, cada usuario, según su función, recibe distintos tipos de notificaciones en distintos escenarios.
contentowner: manochan
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 69%

---



# Notificaciones

La función Notificaciones es aplicable a todos los usuarios de Adobe Learning Manager. Sin embargo, según la función de cada usuario, se obtienen distintos tipos de notificaciones en diferentes situaciones. Todas las alertas y notificaciones a los usuarios se muestran en cuadros de diálogo emergentes de notificaciones.

## Notificaciones de acceso {#accessnotifications}

Los usuarios pueden ver las notificaciones si hacen clic en el icono de notificaciones en la esquina superior derecha de la ventana. Este cuadro de diálogo emergente muestra resaltadas todas las notificaciones junto con la hora en que se produjeron con una barra de desplazamiento. Para ver más información sobre todas las notificaciones, haga clic en Mostrar todas las notificaciones en la parte inferior del cuadro de diálogo emergente. Aparece la página de notificaciones.

Puede saber la cantidad de notificaciones más recientes según el número resaltado en el icono de notificaciones. Por ejemplo, si tiene cinco notificaciones recientes después del inicio de sesión anterior, puede ver que el número 5 aparece en el icono de notificaciones. Estos números desaparecen cuando lee todas las notificaciones recientes.

## Tipos de notificaciones para administradores {#typesofnotificationsforadministrators}

Los administradores reciben notificaciones en los casos siguientes:

* Siempre que se carga correctamente una lista csv de usuarios.
* Siempre que la carga de una lista csv de usuarios no sea correcta. El administrador recibe un mensaje con el motivo del error.
* El administrador también puede configurar alertas de notificación en el nivel de instancia para los cursos y los programas de aprendizaje. En este caso, el administrador recibe las notificaciones según la frecuencia seleccionada en el nivel de instancia.

>[!NOTE]
>
>Si un administrador tiene privilegios de autor o responsable además de su función, el administrador recibe notificaciones relativas a cada función.

En la siguiente captura de pantalla se muestra un ejemplo de ventana de notificación para la función de administrador:

![](assets/admin-notification.png)

*Ver notificaciones del administrador*

Esta ventana emergente muestra resaltadas todas las notificaciones junto con la hora de aparición y una barra de desplazamiento. Puede obtener la cantidad de notificaciones más recientes según el número resaltado en el icono de notificaciones. Por ejemplo, si tiene cinco notificaciones recientes después del inicio de sesión anterior, puede ver que el número 5 aparece en el icono de notificaciones. Estos números desaparecen cuando lee todas las notificaciones recientes.

Haga clic en **[!UICONTROL Mostrar todas las notificaciones]** situado en la parte inferior de la ventana emergente de notificaciones para ver todas las notificaciones en una página independiente.

## Configuración de notificaciones de escalación multinivel {#setupmultilevelescalationnotifications}

Los correos electrónicos de escalación cuando los alumnos no cumplen los plazos se pueden enviar al administrador y al administrador de omisión. Puede configurar notificaciones de escalación de múltiples niveles para la no finalización del curso durante el proceso de creación de un curso, o incluso después de que se haya creado. Las notificaciones de escalación se pueden configurar para que se envíen con una frecuencia determinada a un administrador o a un administrador de omisión.

1. Inicie sesión como administrador o autor y haga clic en Cursos.
1. Seleccione el curso para el que desea modificar las notificaciones de escalación y haga clic en **[!UICONTROL Ver curso]**.

   ![](assets/view-courses.png)

   *Seleccione la opción Ver curso*

1. Haga clic en **[!UICONTROL Instancias]** > **[!UICONTROL Alertas de notificación]**.

   ![](assets/notification-alert.png)

   *Seleccione la opción Alertas de notificación*

1. Se abre un calendario que indica el plazo establecido para el curso resaltado en rojo. Haga clic en la fecha resaltada para ver los recordatorios configurados para el alumno.

   ![](assets/deadline-calender.png)

   *Ver recordatorios de fechas límite*

1. Establezca los recordatorios seleccionando fechas anteriores al vencimiento. Esto permite configurar recordatorios para el alumno sobre la fecha límite que se aproxima.

   ![](assets/deadline-reminder.png)

   *Establecer una fecha de recordatorio de fecha límite*

1. Seleccione una fecha después de la fecha límite para configurar un calendario de recordatorios para las notificaciones del alumno y de escalación al administrador.

   ![](assets/set-reminders-andescalation.png)

   *Establecer recordatorios y fechas de escalación*

1. Si el alumno sigue sin completar el curso incluso después de la escalación al responsable, la configuración le permite escalar al responsable de omisión del alumno. Haga clic en una fecha posterior a la fecha límite ampliada, seleccione la periodicidad de los recordatorios, el número de días para la programación y seleccione **Responsable y responsable de nivel de omisión** en el **Escalación** menú desplegable. Haga clic en la marca de verificación azul para guardar la configuración de notificaciones.

   ![](assets/reminder-to-managerandskipmanager.png)

   *Guardar la configuración de notificaciones*

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++Cómo configurar notificaciones de recordatorio en la instancia?

En una instancia, haga clic en Alertas de notificación. Se abre un calendario que indica el plazo establecido para el curso resaltado en rojo. Haga clic en la fecha resaltada para ver los recordatorios configurados para el alumno. Establezca los recordatorios, como se describe en este [sección](user-notifications.md#Setupmultilevelescalationnotifications).
+++
