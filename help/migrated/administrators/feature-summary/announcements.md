---
jcr-language: en_us
title: Anuncios
description: Un anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador emite a un conjunto definido de usuarios.
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---



# Anuncios

Un anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador emite a un conjunto definido de usuarios.

El administrador puede difundir anuncios a los alumnos para informarles de la ocurrencia de un evento o una actividad. Los anuncios pueden ser una combinación de texto, imágenes o vídeos. Puede vincular objetos de aprendizaje como cursos, programas de aprendizaje y certificaciones a un anuncio.

Hay cuatro tipos de anuncios:

* Notificación
* Cabeza
* Recomendación
* Correo electrónico

## Notificación {#notification}

1. Como usuario administrador, haga clic en Anuncios en el panel izquierdo.
1. Haga clic en Añadir en la esquina superior derecha de la página.
1. En la lista desplegable Tipo, seleccione la opción **Como notificación**.
1. En el campo Mensaje , añada el mensaje del anuncio. También puede agregar una dirección URL para los anuncios aquí. Sin embargo, debe agregar la dirección URL en el formulario de HTML.

   Por ejemplo,  `code <a href="http://www.w3schools.com" target="_blank">Visit W3Schools</a>.`

   Cuando se especifica el destino como en blanco, cuando un usuario hace clic en la dirección URL del anuncio, el vínculo se abre en una nueva ficha. Si no se especifica el destino, el vínculo se abre en el mismo navegador.

1. Si lo desea, puede añadir archivos adjuntos, como imágenes o archivos de vídeo, al anuncio.
1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y selecciónelo en la lista desplegable. Del mismo modo, elija el curso de formación escribiendo el nombre del objeto en el cuadro de texto.

1. Haga clic en Configuración avanzada en el cuadro de diálogo. Puede realizar las siguientes acciones:

   * Convierta este anuncio en un anuncio adhesivo seleccionando la casilla de verificación Habilitar anuncio adhesivo.
   * Seleccione la hora de entrega del anuncio.

1. Seleccionar **[!UICONTROL En una fecha]** si desea programar el anuncio para una fecha posterior y hacer clic en el área de texto adyacente. Aparece una ventana emergente de calendario, en la que puede elegir la fecha de inicio. Elija la fecha de finalización siguiendo los mismos pasos.
1. Haga clic en **[!UICONTROL Guardar]**.
1. En la ficha Borrador, haga clic en el icono de configuración junto a un anuncio y haga clic en Enviar.

Si el archivo adjunto multimedia es de gran tamaño, puede tardar algún tiempo en cargarse. Después de hacer clic en Guardar, aparecerá un mensaje emergente cuando se procese la carga. Recibirá una notificación después de que el archivo adjunto se cargue correctamente.

## Cabeza {#masthead}

Al seleccionar esta opción, cualquier archivo multimedia que elija se mostrará como cabecera en la página de inicio del alumno. La cabecera actúa como una llamada a la acción para los alumnos a los que está destinada.

![](assets/masthead-announcement.png)

*Personalizar la cabecera*

1. Busque y elija una imagen que represente la cabecera. El tamaño recomendado es de 1280 x 360 px.
1. Elija la configuración regional a la que desea añadir una cabecera. Para cada idioma, debe elegir un recurso de cabecera.
1. En la **[!UICONTROL Botón Acción]** , añada una url para que cuando los alumnos hagan clic en el botón de la cabecera, se les redirija a la url. Éste es un campo opcional.
1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y selecciónelo en la lista desplegable. Del mismo modo, elija el curso de formación escribiendo el nombre del objeto en el cuadro de texto.

1. En la **[!UICONTROL Configuración avanzada]** , dispone de las siguientes opciones:

   * Haga clic en **[!UICONTROL De inmediato]** si desea que el anuncio se publique en ese momento.
   * Haga clic en **[!UICONTROL Nunca]** si no desea que caduque el anuncio.
   * Seleccione la **[!UICONTROL Inicio]** y **[!UICONTROL Fin]** fechas del anuncio.

   ![](assets/advanced-settings.png)

   *Establecer el tiempo que debe mostrar una cabecera*

**¿Existe un límite en el número de anuncios de cabecera en directo?**

Solo verá los 10 anuncios de cabecera más recientes.

## Recomendación {#recommendation}

Al seleccionar esta opción, cualquier curso de formación que elija se recomendará a los grupos de usuarios especificados. Las recomendaciones se basan en un algoritmo de aprendizaje automático.

![](assets/recommendation-announcement.png)

*Seleccione la formación recomendada que se mostrará a un alumno*

1. Elija la formación que desee recomendar a los alumnos. Puede añadir hasta 10 cursos de formación.

   Los alumnos solo verán los cursos de formación para los que se ha dado de baja en Recomendación por organización. En función de la visibilidad del catálogo, el alumno tiene acceso para ver la formación.

1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y selecciónelo en la lista desplegable. Del mismo modo, elija el curso de formación escribiendo el nombre del objeto en el cuadro de texto.

1. En la sección Configuración avanzada, tiene las siguientes opciones:

   * Haga clic en **[!UICONTROL De inmediato]** si desea que el anuncio se publique en ese momento.
   * Haga clic en **[!UICONTROL Nunca]** si no desea que caduque el anuncio.
   * Seleccione la **[!UICONTROL Inicio]** y **[!UICONTROL Fin]** fechas del anuncio.

   <!--![](assets/advanced-settings.png)-->

Al hacer clic en **[!UICONTROL Guardar]**, puede publicar el anuncio de inmediato o más tarde. El anuncio, hasta entonces, estará en estado de borrador.

* Las cabeceras/Recommendations no activan ninguna notificación.
* Las cabeceras/Recommendations no aparecen en el informe de anuncios.

## Lista de borrador, programada y enviada {#draftscheduledandsentlist}

En el inicio de sesión del administrador, puede ver todos los anuncios en tres pestañas, como Borrador, Programado y Enviado.

<!--![](assets/three-tabs-announcement1.png)-->

### Draft {#draft}

En la ficha Borrador, puede ver todos los anuncios creados por un administrador pero que aún no se han difundido o que aún no se han programado para difundirse.

De forma predeterminada, todos los anuncios se establecen para su difusión inmediata. Si elige la opción configuración > enviar para un anuncio no programado, se emite inmediatamente. Para programar la difusión de un anuncio, debe elegir la fecha de inicio y la fecha de finalización en Configuración avanzada.

### Programado {#scheduled}

En la ficha Programado, puede ver todos los anuncios programados para su difusión en una fecha posterior.

### Enviado {#sent}

En la ficha Enviado, puede ver todos los anuncios que ya se han difundido.

## Como correo electrónico

Utilice esta opción para enviar correos electrónicos ad hoc específicos a los alumnos de un grupo de usuarios seleccionado o a los alumnos inscritos en un curso de formación específico.

![El administrador crea un anuncio por correo electrónico](assets/email-announcement-admin.png)

*Enviar correos electrónicos ad hoc específicos a los alumnos*

*El administrador crea un anuncio por correo electrónico*

1. Seleccionar **[!UICONTROL Escribir como correo electrónico]**.
1. Introduzca el asunto del correo electrónico y el cuerpo del mensaje.
1. En la sección Destino, puede:

   * Seleccione un grupo de usuarios O
   * Seleccione un curso. Si el curso tiene varias instancias, puede seleccionar la instancia necesaria.

1. Haga clic en **[!UICONTROL Guardar]**.
