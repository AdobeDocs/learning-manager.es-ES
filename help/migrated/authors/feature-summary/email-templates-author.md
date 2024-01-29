---
description: Lea este artículo para saber cómo configurar plantillas de correo electrónico para eventos relacionados con todos los objetos de aprendizaje.
jcr-language: en_us
title: Plantillas de correo electrónico
source-git-commit: fda58bc18bee6d21ee904a442884e4759587d053
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---



# Plantillas de correo electrónico

Lea este artículo para saber cómo configurar plantillas de correo electrónico para eventos relacionados con todos los objetos de aprendizaje.

La aplicación Learning Manager envía notificaciones por correo electrónico a varios roles de usuarios en función de los eventos.

Como autor, puede personalizar las plantillas de correo electrónico agregando o modificando el contenido y enviando notificaciones a los usuarios para varios eventos desencadenados por actividades de alumnos, responsables y autores. Por ejemplo, puede enviar un correo electrónico personalizado cada vez que un alumno se inscriba en el curso. Al inscribirse, el alumno recibirá automáticamente el correo electrónico específico del curso.

También puede optar por no enviar notificaciones por correo electrónico para determinados eventos deshabilitando la opción de plantilla de correo electrónico.

## Configuración de notificaciones por correo electrónico {#settingemailnotifications}

1. En la aplicación de autor, haga clic en el objeto de aprendizaje para el que desea configurar la plantilla de correo electrónico. Por ejemplo, Cursos.
1. En la página Objeto de aprendizaje, haga clic en el curso, la certificación o el programa de aprendizaje en el que desea configurar las opciones de correo electrónico.
1. En la página de detalles del objeto de aprendizaje, haga clic en Plantillas de correo electrónico.

   Puede ver la lista de plantillas disponibles para el objeto de aprendizaje elegido.

   ![](assets/email-templates-forlearningprograms.png)
   *Lista de plantillas*

1. Haga clic en el nombre del evento para ver la plantilla en el modo de vista previa.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Ver vista previa de plantilla*

   Puede personalizar cada plantilla haciendo clic en el texto del cuerpo de la plantilla. Puede insertar variables en el texto haciendo clic en los iconos correspondientes, como se muestra en la captura de pantalla. Pase el ratón por cada icono para ver los nombres.

   ![](assets/insert-variable.png)
   *Insertar una variable*

   Están disponibles las siguientes variables:

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   Puede restablecer el contenido predeterminado del mensaje haciendo clic en el vínculo Volver a original encima de la plantilla.

   Como puede ver en la parte superior de la plantilla, puede personalizar la plantilla para varias funciones (responsable, alumno, etc.) en función del tipo de notificación por correo electrónico.

1. Haga clic en Guardar en la parte inferior de la página de plantillas.
1. En la página Plantillas de correo electrónico, haga clic en el botón circular Sí/No para enviar o deshabilitar la notificación.

![](assets/email-notification-e1437624109719.png)
*Habilitar o deshabilitar la notificación por correo electrónico*

Si el círculo del botón de notificación junto a cada nombre de evento es adyacente a Sí (con un fondo azul), la notificación está habilitada. Si está en gris y el círculo es adyacente a No, la notificación está deshabilitada.

Cada vez que se configura una plantilla de correo electrónico en el nivel del curso, tiene prioridad sobre la configuración del nivel de administrador de ese curso en particular.
