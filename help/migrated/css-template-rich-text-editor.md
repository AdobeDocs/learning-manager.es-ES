---
jcr-language: en_us
title: Plantilla CSS para el Editor de texto enriquecido
description: Plantilla CSS para el Editor de texto enriquecido
contentowner: saghosh
preview: true
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 72%
---


# Plantilla CSS para el Editor de texto enriquecido

## ¿Por qué se necesita una CSS?

El texto enriquecido se compone de formato HTML. Si se procesa el marcado tal y como está, el navegador aplica un estilo predeterminado. A menudo esto no se ajusta a las directrices de estilo de la empresa. Se requiere una CSS para cumplir las directrices.

## Estilo predeterminado

La hoja de estilos CSS adjunta contiene el estilo aplicado por Learning Manager. El estilo se ha modificado teniendo en cuenta la mayoría de los casos de uso. Descargue el archivo CSS adjunto e impórtelo a la aplicación web según sus convenciones y sistema de compilación. Las clases CSS definidas tienen un espacio entre los nombres en la clase de editor de SQL y no interfieren con los estilos existentes.

## Personalización de estilos

Es posible que el estilo predeterminado no satisfaga las necesidades de todos. Las personalizaciones se pueden realizar mediante la modificación del CSS proporcionado. Todo el estilo se ajusta en el editor de SQL como selectores descendientes. Se utilizan las clases siguientes:

* **Sangría**: li.ql-guión-$number. $number varía de 1 a 9.
* **tamaño**: ql-size-small, ql-size-large, ql-size-huge
* **alineación**: ql-align-center, ql-align-justify, ql-align-right
* **color**: ql-color-$color. $color = blanco, rojo, naranja, amarillo, verde, azul, púrpura
* **fondo**: ql-bg-$color. $color = negro, rojo, naranja, amarillo, verde, azul, púrpura
* **etiquetas html**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Archivo CSS que se va a utilizar para la personalización.](assets/ql-headless.css)
