---
jcr-language: en_us
title: Anuncios
description: Un anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador difunde entre un determinado conjunto de usuarios.
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 70%

---



# Anuncios

Un anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador difunde entre un determinado conjunto de usuarios.

El administrador puede difundir anuncios a los alumnos para informarles de la ocurrencia de un evento o una actividad. Los anuncios pueden ser una combinación de texto, imágenes o vídeos. Puede vincular objetos de aprendizaje como cursos, programas de aprendizaje y certificaciones con un anuncio.

Hay cuatro tipos de anuncios:

* Notificación
* Cabecera
* Recomendación
* Correo electrónico

## Notificación {#notification}

1. Como usuario administrador, haga clic en Anuncios en el panel izquierdo.
1. Haga clic en Añadir en la esquina superior derecha de la página.
1. En la lista desplegable Tipo, seleccione la opción **Como notificación**.
1. En el campo Mensaje, añada el mensaje para el anuncio. Aquí también puede agregar una URL para anuncios. Sin embargo, la URL debe añadirse en formato HTML.

   Por ejemplo,  `code <a href="http://www.w3schools.com" target="_blank">Visit W3Schools</a>.`

   Si especifica el destino en blanco, cuando un usuario hace clic en la URL del anuncio, el vínculo se abre en una nueva ficha. Si no especifica el destino, el vínculo se abre en el mismo navegador.

1. Si lo desea, puede añadir archivos adjuntos al anuncio, por ejemplo archivos de imagen o de vídeo.
1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y seleccione en la lista desplegable. También puede elegir el curso de formación especificando el nombre del objeto en el cuadro de texto.

1. Haga clic en Configuración avanzada en el cuadro de diálogo. Puede realizar las acciones siguientes:

   * Convertir este anuncio en fijo seleccionando la casilla de verificación Activar anuncios fijos.
   * Seleccionar la hora de entrega del anuncio.

1. Seleccionar **[!UICONTROL En una fecha]** si desea programar el anuncio para una fecha posterior y hacer clic en el área de texto adyacente. En pantalla aparece un calendario en que seleccionar la fecha de inicio. Elija la fecha de finalización aplicando los mismos pasos.
1. Haga clic en **[!UICONTROL Guardar]**.
1. En la ficha Borrador, haga clic en el icono de configuración junto a un anuncio y haga clic en Enviar.

Si el elemento adjunto multimedia es de gran tamaño, puede tardar en cargarse. Después de hacer clic en Guardar, aparecerá un mensaje emergente cuando se procese la carga. Cuando el elemento adjunto se haya cargado correctamente, recibirá una notificación.

## Cabecera {#masthead}

Al seleccionar esta opción, cualquier archivo multimedia que elija se mostrará como cabecera en la página de inicio del alumno. La cabecera actúa como una llamada a la acción para los alumnos a los que está destinada.

![](assets/masthead-announcement.png)

*Personalizar la cabecera*

1. Busque y elija una imagen que represente la cabecera. El tamaño recomendado es de 1280 x 360 px.
1. Elija la configuración regional a la que desea añadir una cabecera. Para cada idioma, debe elegir un recurso de cabecera.
1. En el campo **[!UICONTROL Botón Acción]**, añada una URL para que cuando los alumnos hagan clic en el botón de la cabecera, se les redirija a la URL. Se trata de un campo opcional.
1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y seleccione en la lista desplegable. También puede elegir el curso de formación especificando el nombre del objeto en el cuadro de texto.

1. En la **[!UICONTROL Configuración avanzada]** , dispone de las siguientes opciones:

   * Haga clic en **[!UICONTROL De inmediato]** si desea que el anuncio se publique en ese momento.
   * Haga clic en **[!UICONTROL Nunca]** si no desea que caduque el anuncio.
   * Seleccione la **[!UICONTROL Inicio]** y **[!UICONTROL Fin]** fechas del anuncio.

   ![](assets/advanced-settings.png)

   *Establecer el tiempo que debe mostrar una cabecera*

**¿Hay un límite en el número de anuncios de cabecera en directo?**

Solo verá los 10 anuncios de cabecera más recientes.

## Recomendación {#recommendation}

Al seleccionar esta opción, cualquier curso de formación que elija se recomendará a los grupos de usuarios especificados. Las recomendaciones se basan en un algoritmo de aprendizaje automático.

![](assets/recommendation-announcement.png)

*Seleccione la formación recomendada que se mostrará a un alumno*

1. Elija el curso de formación que desea recomendar a los alumnos. Puede añadir hasta 10 cursos de formación.

   Los alumnos solo verán los cursos de formación de los que se hayan dado de baja en Recomendación por organización. En función de la visibilidad del catálogo, el alumno tiene acceso para ver la formación.

1. Elija los grupos de usuarios de destino o los objetos de aprendizaje de destino. Solo puede elegir uno de ellos para un anuncio.

   Empiece a escribir el nombre del grupo de usuarios en el cuadro de texto y seleccione en la lista desplegable. También puede elegir el curso de formación especificando el nombre del objeto en el cuadro de texto.

1. En la sección Configuración avanzada, tiene las siguientes opciones:

   * Haga clic en **[!UICONTROL De inmediato]** si desea que el anuncio se publique en ese momento.
   * Haga clic en **[!UICONTROL Nunca]** si no desea que caduque el anuncio.
   * Seleccione la **[!UICONTROL Inicio]** y **[!UICONTROL Fin]** fechas del anuncio.

   <!--![](assets/advanced-settings.png)-->

Al hacer clic en **[!UICONTROL Guardar]**, puede publicar el anuncio en ese momento o más tarde. El anuncio estará hasta ese momento en estado de borrador.

* Las cabeceras/recomendaciones no activan ninguna notificación.
* Las cabeceras/recomendaciones no aparecen en el informe de anuncios.

## Lista de Borrador, Programado y Enviado {#draftscheduledandsentlist}

En el inicio de sesión del administrador, puede ver todos los anuncios en tres pestañas, como Borrador, Programado y Enviado.

<!--![](assets/three-tabs-announcement1.png)-->

### Borrador {#draft}

En la ficha Borrador, puede ver todos los anuncios creados por un administrador pero que aún no se han difundido o que aún no se han programado para difundirse.

De forma predeterminada, todos los anuncios se definen para difundirse inmediatamente. Si elige la opción Configuración > Enviar para un anuncio que no está programado, se difunde de inmediato. Para programar la difusión de un anuncio, en Configuración avanzada se debe seleccionar una fecha de inicio y una fecha de finalización.

### Programado {#scheduled}

En la ficha Programado, puede ver todos los anuncios que están programados para difundirse más adelante.

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
