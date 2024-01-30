---
jcr-language: en_us
title: Plantilla CSS para el Editor de texto enriquecido
description: Plantilla CSS para el Editor de texto enriquecido
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 70%

---



# Plantilla CSS para el Editor de texto enriquecido

## ¿Por qué se necesita una CSS?

El texto enriquecido se compone de formato HTML. Si se procesa el marcado tal y como está, el navegador aplica un estilo predeterminado. A menudo esto no se ajusta a las directrices de estilo de la empresa. Se requiere una CSS para cumplir las directrices.

## Estilo predeterminado

La hoja de estilos CSS adjunta contiene el estilo aplicado por Learning Manager. El estilo se ha modificado teniendo en cuenta la mayoría de los casos de uso. Descargue el archivo CSS adjunto e impórtelo a la aplicación web según sus convenciones y sistema de compilación. Las clases CSS definidas tienen un espacio entre nombres en la clase de editor de SQL y no interfieren con los estilos existentes.

## Personalización de estilos

Es posible que el estilo predeterminado no satisfaga las necesidades de todos. Las personalizaciones se pueden realizar mediante la modificación del CSS proporcionado. Todo el estilo se ajusta en el editor de SQL como selectores descendientes. Se utilizan las clases siguientes:

* **Sangría**: li.ql-guión-$number. $number varía de 1 a 9.
* **talla**: ql-size-small, ql-size-large, ql-size-huge
* **alineación**: ql-align-center, ql-align-justify, ql-align-right
* **color**: ql-color-$color. $color = blanco, rojo, naranja, amarillo, verde, azul, púrpura
* **antecedentes**: ql-bg-$color. $color = negro, rojo, naranja, amarillo, verde, azul, púrpura
* **etiquetas html**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Archivo CSS que se va a utilizar para la personalización.](assets/ql-headless.css)
