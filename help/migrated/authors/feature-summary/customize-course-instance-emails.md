---
description: Personalice los correos electrónicos de nivel de curso y de instancia en Adobe Learning Manager con Email Builder y el diseño que le proporcione su administrador.
jcr-language: en_us
title: Personalización de correos electrónicos de curso e instancia en Email Builder
exl-id: 06499e3f-0610-4983-83f2-3e8b578fc8bf
source-git-commit: 172889a4ff67e54c8e7b9a39ef5f393af0a1d703
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%
---

# Personalización de correos electrónicos de curso e instancia en Email Builder

Como autor, puede personalizar los mensajes de correo electrónico de un curso o de una instancia específica de un curso. Ambos procedimientos parten de un diseño que proporciona el administrador.

## Personalizar un correo electrónico de nivel de curso

1. Abra el curso.
2. Seleccione **Plantillas de correo electrónico**.
3. Seleccione **Diseño de correo electrónico del curso**.
4. Personalizar el contenido del correo electrónico. Para definir fuentes, colores, filas y botones.
5. Guarde la plantilla.
6. Publish el curso.

## Personalizar un correo electrónico a nivel de instancia

Utilice un correo electrónico de instancia cuando diferentes cohortes necesiten mensajes diferentes. Estas cohortes se gestionan mediante instancias de curso.

1. Abra la instancia del curso.
2. Abra **Email Builder**.
3. Seleccione un diseño disponible o herede el diseño que la instancia ya utiliza.
4. Actualice el contenido del mensaje.
5. Guarde la plantilla.

>[!NOTE]
>
>Cuando ambos existen, los correos electrónicos a nivel de instancia anulan las plantillas a nivel de curso.

## Utilizar la variable Title y una imagen para los encabezados de correo electrónico

Utilice la variable Title con un componente Image para crear el encabezado del correo electrónico en lugar del componente Banner. La imagen del componente Banner no aparece en algunos clientes de correo electrónico, como Outlook.

La variable Title, EmailTitle, funciona como la variable ChannelName existente. Cada correo electrónico tiene su propio valor de título predeterminado.

Para agregar un encabezado de título:

1. Añada un componente Image para la imagen de encabezado.
2. Agregue un componente de texto e inserte la variable title desde el menú desplegable de variables en el panel de configuración del componente.
3. Alinee al centro el componente de texto. En el diseño global, colóquelo en el encabezado superior.

   Los correos electrónicos individuales utilizan el encabezado del diseño global de forma predeterminada. En un correo electrónico individual, puede editar el componente de texto para:

4. Reemplace la variable por texto personalizado
5. Agregue texto antes o después de la variable y mantenga `EmailTitle`

Si agrega una imagen al componente Banner, Email Builder muestra una advertencia que indica que la imagen podría no aparecer correctamente en algunos clientes de correo electrónico. La advertencia sugiere utilizar un componente Image y la variable title en su lugar.

## Resolución de problemas

**No se puede seleccionar un diseño.**
La herencia de diseños depende de los diseños principales disponibles. Pida al administrador que cree un diseño de cuenta.

**El correo electrónico no muestra los cambios de diseño recientes.**
Es posible que la plantilla se desvincule de su diseño. Las plantillas desvinculadas ya no reciben actualizaciones de diseño.

**Los alumnos de una instancia reciben un correo electrónico diferente al del curso.**
Los correos electrónicos de instancia anulan las plantillas de nivel de curso. Revise la plantilla de nivel de instancia.

**No se ve el generador de correo electrónico para los mensajes de correo electrónico del curso o la instancia.**
Adobe habilita el Generador de correo electrónico en fases. Pida al administrador que confirme que Email Builder está habilitado para su cuenta.

**La imagen del banner no aparece en el correo electrónico.**
Algunos clientes de correo electrónico, como Outlook, no muestran la imagen del componente Banner. Quite el componente Banner, añada un componente Image y añada un componente Text que utilice la variable title.
