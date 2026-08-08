---
description: Una referencia completa para todas las propiedades del esquema JSON del tema de Compositor de contenido, incluidos los tokens de paleta, las pilas de fuentes, los tokens de radio y espaciado, los valores de función de texto, las propiedades de componentes y el estilo de evaluación.
jcr-language: en_us
title: Referencia de propiedades JSON del tema Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 5%

---


# Referencia de propiedades JSON del tema Adobe Learning Manager Content Composer

Una referencia completa para cada propiedad de un archivo JSON de tema de Content Composer, con descripciones y valores de ejemplo.

Campos de nivel superior que identifican y describen el tema.

## **Metadatos**

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|--------------|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| id | cadena | Identificador único del tema. Minúsculas, solo guiones, sin espacios ni caracteres especiales. Se utiliza internamente para hacer referencia al tema. | &quot;pizarra&quot; |
| name | cadena | Nombre para mostrar que se muestra en el panel Temas del curso. | &quot;Pizarra&quot; |
| versión | cadena | Número de versión semántica. Utilice &quot;1.0.0&quot; para nuevos temas. | &quot;1.0.0&quot; |
| descripción | cadena | Descripción breve del carácter visual del tema. | &quot;Un tema cálido y autoritativo con fondo crema, acentos de Adobe rojo y el sistema de tipo Roboto Slab + Roboto&quot; |
| autor | cadena | Nombre del creador o equipo del tema. | &quot;Compositor de contenido&quot; |
| origen | cadena | Origen del tema. &quot;enviado&quot; para temas integrados. &quot;personalizado&quot; para temas creados por el usuario. | &quot;personalizado&quot; |
| isDefault | booleano | Si este tema se aplica automáticamente a los nuevos cursos. En la mayoría de los casos, se establece en false. | falso |

## **foundation.palette**

Los siete tokens de color principales que forman la base de color del tema. Todos los valores de elemento hacen referencia a estos tokens mediante var(—tokenName) en lugar de valores hexadecimales codificados.

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|------------------|------------|---------------------------------------------------------------------------------------------------------------------------|-----------------|
| primer plano | color hexadecimal | Color frontal principal para texto, iconos y elementos de la interfaz de usuario colocados en el fondo. | #1A1A1A |
| antecedentes | color hexadecimal | Color de fondo del lienzo y la diapositiva del curso principal. | #FAF7F2 |
| acento | color hexadecimal | Color de énfasis de marca aplicado a botones, estados seleccionados, indicadores de progreso, encabezados de lección y resaltados interactivos. | #E8001C |
| backgroundSutil | color hexadecimal | Color de fondo secundario para tarjetas, paneles, navegación y rellenos de componentes. | #F0EBE1 |
| secundario | color hexadecimal | Borde, divisor y color de elemento de IU inactivo. | #D9D3C9 |
| textPrimary | color hexadecimal | Color del texto principal para todo el contenido del encabezado y del cuerpo. | #1A1A1A |
| textInverse | color hexadecimal | Color del texto para el contenido colocado en fondos oscuros o con acentos, como etiquetas de botón en el color de acento. | #FFFFFF |

## **foundation.fonts**

Se han aplicado dos pilas de fuentes en todas las funciones de texto del tema. Referencia en valores de elemento mediante var(—font-heading) o var(—font-body).

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|--------------|-------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| encabezado | cadena de pila de fuentes | Familia de fuentes para los títulos de las lecciones, los títulos de los temas y los encabezados de visualización. Incluye retrocesos seguros para la Web. | &quot;Roboto Slab, Georgia, &#39;Times New Roman&#39;, serif&quot; |
| carrocería | cadena de pila de fuentes | Familia de fuentes para texto de párrafo, subtítulos, preguntas de prueba y etiquetas de IU. Incluye retrocesos seguros para la Web. | &quot;Roboto, -apple-system, BlinkMacSystemFont, &#39;Segoe UI&#39;, sans-serif&quot; |

## **foundation.spacing**

Distintivos de espaciado horizontal y vertical utilizados como línea de base. Los componentes se escalan a partir de estos mediante multiplicadores horizontalesSpacingScale y verticalesSpacingScale.

| **Ruta** | **Tipo** | **Descripción** | **Valor de pizarra** |
|---------------|----------|-------------------------------------|-----------------|
| horizontal.xs | valor px | Unidad de espaciado horizontal más pequeña | 4px |
| horizontal.s | valor px | Unidad de espaciado horizontal pequeña | 8px |
| horizontal.m | valor px | Unidad de espaciado horizontal media | 12px |
| horizontal.l | valor px | Unidad de espaciado horizontal grande | 16px |
| horizontal.xl | valor px | Unidad de espaciado horizontal extra grande | 24px |
| vertical.xs | valor px | Unidad de espaciado vertical más pequeña | 4px |
| vertical.s | valor px | Unidad de espaciado vertical pequeña | 8px |
| vertical.m | valor px | Unidad de espaciado vertical media | 16px |
| vertical.l | valor px | Unidad de espaciado vertical grande | 24px |
| vertical.xl | valor px | Unidad de espaciado vertical de gran tamaño | 32px |

## **foundation.radius**

Tokens de radio de borde que controlan el redondeo de las esquinas para componentes y tarjetas.

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|--------------|----------|---------------------------------------------------------|-----------------|
| ninguno | valor px | Sin redondeo: esquinas afiladas. Siempre &quot;0px&quot;. | 0px |
| s | valor px | Radio pequeño para redondeo de esquina sutil. | 4px |
| m | valor px | Radio medio para el redondeo estándar de tarjetas y componentes. | 8px |
| l | valor px | Radio grande para redondeo prominente. | 16px |
| completo | valor px | Completo en forma de píldora o círculo. Siempre &quot;999px&quot;. | 9999px |

## **foundation.logo**

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|--------------|----------------|----------------------------------------------------------------------------------------------|-----------------|
| logotipo | cadena o null | URL o ruta de archivo de la imagen del logotipo que se muestra en el encabezado del curso. Se establece en null para no logo. | null |

## **elements.text**

Propiedades tipográficas para cada función de texto con nombre del curso. Todas las funciones comparten el mismo conjunto de propiedades.

### **Funciones de texto**

| **Rol** | **Aplicado a** |
|--------------|------------------------------------------------------------------------------|
| classTitle | Título principal de una diapositiva de apertura de una lección |
| topicTitle | Encabezado en la parte superior de cada diapositiva de tema |
| blockHeading | Títulos dentro de componentes de contenido como encabezados de acordeón y títulos de tarjeta |
| subtítulo | Encabezados secundarios dentro de una diapositiva de tema |
| pregunta | Cuestionario y texto de pregunta de comprobación de conocimientos |
| subtítulo | Leyendas debajo de imágenes y bloques de medios |
| párrafo | Texto independiente en diapositivas de contenido |
| buttonLabel | Texto sobre botones y elementos de llamada a la acción |

### **Propiedades de texto compartido**

Las siguientes propiedades se aplican a todas las funciones de texto enumeradas anteriormente.

| **Propiedad** | **Tipo** | **Valores aceptados** | **Descripción** |
|--------------------|-----------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| fontFamily | CSS var o pila de fuentes | var(—font-heading), var(—font-body) o una cadena de pila de fuentes completa | Familia de fuentes para esta función de texto. |
| fontSize | valor px | Cualquier valor de píxel | Tamaño de fuente. |
| fontWeight | cadena | Solo &quot;bold&quot; o &quot;normal&quot;: no se admiten valores numéricos. | Grosor de fuente. |
| fontStyle | cadena | &quot;normal&quot; o &quot;cursiva&quot; | Estilo de fuente. |
| color | CSS var o hex | Cualquier distintivo de paleta mediante var(—tokenName) o un valor hexadecimal directo | Color del texto. |
| textAlign | cadena | &quot;left&quot;, &quot;center&quot; o &quot;right&quot; | Alineación de texto horizontal. |
| letterSpacing | cadena | &quot;normal&quot;, valor px o valor em | Espacio entre caracteres. |
| lineHeight | cadena | Un porcentaje o un valor sin unidades | Height de línea. |
| textDecoration | cadena | &quot;none&quot;, &quot;underline&quot; o &quot;line-through&quot; | Decoración del texto. |
| textTransform | cadena | &quot;none&quot;, &quot;uppercase&quot;, &quot;lowercase&quot; o &quot;capitalize&quot; | Transformación de mayúsculas y minúsculas de texto |
| paddingInlineStart | valor px | Cualquier valor de píxel | Relleno izquierdo aplicado al bloque de texto. |
| ParagraphSpacing | valor px | Cualquier valor de píxel | Espacio añadido debajo de cada párrafo dentro del bloque de texto. |

### **Valores de función de texto: tema de pizarra**

| **Rol** | **fontFamily** | **fontSize** | **fontWeight** | **fontStyle** | **color** | **textAlign** | **letterSpacing** | **lineHeight** | **textTransform** |
|--------------|---------------------|--------------|----------------|---------------|--------------------|---------------|-------------------|----------------|-------------------|
| classTitle | var(—font-heading) | 48px | audaz | normal | var(—textPrimary) | centro | -0,01em | 130% | ninguno |
| topicTitle | var(—font-heading) | 40px | normal | normal | var(—textPrimary) | el | 0 | 135% | ninguno |
| blockHeading | var(—font-heading) | 24px | audaz | normal | var(—textPrimary) | el | 0 | 140% | ninguno |
| subtítulo | var(—font-body) | 20px | audaz | normal | var(—textPrimary) | el | 0,01em | 150% | ninguno |
| pregunta | var(—font-heading) | 24px | normal | normal | var(—textPrimary) | el | 0 | 150% | ninguno |
| subtítulo | var(—font-body) | 13px | normal | normal | var(—textPrimary) | el | 0,02 em | 170% | ninguno |
| párrafo | var(—font-body) | 16px | normal | normal | var(—textPrimary) | el | 0,01em | 190% | ninguno |
| buttonLabel | var(—font-body) | 14px | audaz | normal | var(—textInverse) | centro | 0,06 em | 125% | mayúscula |

## **elementos - superficies estructurales**

Propiedades que controlan el fondo y el borde de las superficies de diseño fijas del curso.

| **Elemento** | **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|--------------|--------------|-------------------|---------------------------------------------------|----------------------------|
| lienzo | antecedentes | CSS var | Color de fondo del lienzo del curso principal | var(—background) |
| encabezado | antecedentes | CSS var | Color de fondo de la barra de encabezado del curso | var(—background) |
| encabezado | borde | Cadena de borde CSS | Borde inferior de la barra de encabezado del curso | 1px solid var(—secondary) |
| footer | antecedentes | CSS var | Color de fondo de la barra de pie de curso | var(—background) |
| footer | borde | Cadena de borde CSS | Borde superior de la barra del pie de página del curso | 1px solid var(—secondary) |
| UNIDADesección | antecedentes | CSS var | Color de fondo del área del encabezado del título de la lección | var(—acento) |
| tema | antecedentes | CSS var | Color de fondo de cada diapositiva de tema | var(—background) |
| tema | borde | Cadena de borde CSS | Borde alrededor del contenedor de diapositivas de tema | 1px solid var(—secondary) |
| navegación | antecedentes | CSS var | Color de fondo del panel de navegación de la lección | var(—backgroundSubtle) |
| navegación | borde | Cadena de borde CSS | Borde en el panel de navegación de la lección | 1px solid var(—secondary) |
| botón | antecedentes | CSS var | Color de fondo de los botones de acción principales | var(—acento) |
| paginación | antecedentes | CSS var | Color de fondo del control de paginación | var(—backgroundSubtle) |

## **elements - propiedades de componente compartido**

Estas propiedades aparecen en todos los componentes del bloque de contenido: ParagraphBlock, videoBlock, imageGrid, accordion, carousel, flipCard y timeline.

| **Propiedad** | **Tipo** | **Descripción** |
|------------------------|-------------------|---------------------------------------------------------------------------------------------------|
| antecedentes | Variación o color de CSS | Fondo exterior del bloque de componentes. Típicamente &quot;transparente&quot;. |
| cardBackgroundColor | Variación o color de CSS | Relleno de fondo de tarjetas individuales dentro del componente. |
| cardBorder | Cadena de borde CSS | Borde aplicado a cada tarjeta. Método abreviado de CSS completo, por ejemplo &quot;1px solid var(—secondary)&quot;. |
| cardShadowOffset | cadena | Desplazamiento X e Y de la sombra paralela de la tarjeta, por ejemplo &quot;0px 2px 6px&quot;. |
| cardShadowColor | Variación o color de CSS | Color de la sombra paralela de la tarjeta. |
| cardShadowOpacity | cadena de porcentaje | Opacidad de la sombra paralela de la tarjeta. Establezca esta opción en &quot;0%&quot; para eliminar la sombra. |
| horizontalSpacingScale | cadena numérica | Multiplicador aplicado a tokens de espaciado horizontal para este componente. &quot;1&quot; utiliza el espaciado predeterminado. |
| verticalSpacingScale | cadena numérica | Multiplicador aplicado a tokens de espaciado vertical para este componente. &quot;1&quot; utiliza el espaciado predeterminado. |
| radiusScale | cadena numérica | Multiplicador aplicado a tokens de radio para este componente. &quot;1&quot; utiliza el radio predeterminado. |
| nestedAccentColor | Variación o color de CSS | Color de énfasis para elementos anidados dentro del componente. Se aplica sólo a ParagraphBlock. |

### **Valores de componentes compartidos: tema de pizarra**

| **Componente** | **cardBackgroundColor** | **cardBorder** | **cardShadowOpacity** |
|----------------|-----------------------------|----------------------------|---------------------------|
| bloquePárrafo | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| videoBlock | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| imageGrid | var(—backgroundSubtle) | 1px solid var(—highlight) | 8% |
| acordeón | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| carrusel | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| flipCard | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| cronología | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |

## **elements: propiedades específicas de componentes**

Propiedades exclusivas de tipos de componentes individuales.

| **Componente** | **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|----------------|--------------------------|----------|------------------------------------------------------------------|-------------------------|
| bloquePárrafo | nestedAccentColor | CSS var | Color de énfasis para elementos anidados dentro del bloque de párrafo | var(—acento) |
| flipCard | cardFrontBackgroundColor | CSS var | Color de fondo de la cara frontal de la tarjeta | var(—backgroundSubtle) |
| flipCard | cardBackBackgroundColor | CSS var | Color de fondo de la cara posterior de la tarjeta - el color de revelación | var(—acento) |
| flipCard | arrowColor | CSS var | Color del icono de flecha del indicador de volteo | var(—textInverse) |
| pestañas | activeBg | CSS var | Color de fondo de la ficha seleccionada actualmente | var(—acento) |
| pestañas | inactiveBg | CSS var | Color de fondo de las fichas no seleccionadas | var(—backgroundSubtle) |
| pestañas | containerBg | CSS var | Color de fondo del contenedor de la barra de fichas | var(—backgroundSubtle) |
| cronología | trackColor | CSS var | Color de la línea de conexión entre los nodos de la cronología | var(—secondary) |
| cronología | progressCompletedBg | CSS var | Color de relleno de los marcadores de progreso completados de la cronología | var(—acento) |
| cronología | progressCurrentBorder | CSS var | Color de borde del marcador de progreso de la cronología actual | var(—acento) |
| cronología | progressUnachedBg | CSS var | Color de relleno de los marcadores de línea de tiempo aún no alcanzado | var(—secondary) |
| cronología | progressUnachedBorder | CSS var | Color de borde de marcadores de línea de tiempo aún no alcanzado | var(—backgroundSubtle) |

## **elements.assessment**

Propiedades de los componentes de prueba y comprobación de conocimientos.

| **Propiedad** | **Tipo** | **Descripción** | **Valor de pizarra** |
|----------------------------|----------------|------------------------------------------------------------------------------|-------------------------|
| antecedentes | CSS var | Antecedentes exteriores del bloque de evaluación | transparente |
| optionTextColor | CSS var | Color de texto de las etiquetas de opciones de respuesta | var(—textPrimary) |
| optionIndicatorColor | CSS var | Color del botón de opción o indicador de la casilla de verificación | var(—acento) |
| optionSelectedColor | CSS var | Color aplicado al indicador de opción seleccionado | var(—acento) |
| optionCheckmarkColor | CSS var | Color del icono de marca de verificación mostrado en una opción seleccionada | var(—textInverse) |
| optionBackgroundColor | CSS var | Color de fondo de cada opción de respuesta | var(—background) |
| optionHoverBackgroundColor | CSS var | Color de fondo de una opción de respuesta al pasar el cursor | var(—backgroundSubtle) |
| buttonBackgroundColor | CSS var | Color de fondo del botón Enviar o Comprobar respuesta | var(—acento) |
| buttonTextColor | CSS var | Color de texto de la etiqueta del botón Enviar o Comprobar respuesta | var(—textInverse) |
| buttonHoverBackgroundColor | CSS var | Color de fondo del botón al pasar el cursor | var(—acento) |
| comentarioCorregirColor | color hexadecimal | Color de fondo del panel de comentarios de la respuesta correcta | #D7F7E1 |
| comentarioColorIncorrecto | color hexadecimal | Color de fondo del panel de comentarios de respuestas incorrectas | #FEBE8 |
| comentarioTextoColor | color hexadecimal | Color del texto dentro del panel Comentarios | #111111 |
| optionBorderCorrectColor | color hexadecimal | Color de borde en la opción de respuesta correcta después de revelar la respuesta | #079355 |
| optionBorderIncorrectColor | color hexadecimal | Color de borde en una opción seleccionada incorrectamente después de mostrar la respuesta | #D73220 |
| horizontalSpacingScale | cadena numérica | Multiplicador para el espaciado horizontal dentro del componente de evaluación | &quot;1&quot; |
| verticalSpacingScale | cadena numérica | Multiplicador del espaciado vertical dentro del componente de evaluación | &quot;1&quot; |
| radiusScale | cadena numérica | Multiplicador del radio de borde dentro del componente de evaluación | &quot;1&quot; |

## **Referencia var() del token de paleta**

Utilice estas expresiones var() en valores de elemento para hacer referencia a tokens de paleta. Al actualizar un distintivo de paleta, se actualizan automáticamente todos los elementos que lo utilizan.

| **Expresión** | **Referencias** |
|-------------------------|-------------------------------------|
| var(—primer plano) | foundation.palette.primer plano |
| var(—background) | foundation.palette.background |
| var(—acento) | foundation.palette.acted |
| var(—backgroundSubtle) | foundation.palette.backgroundSubtle |
| var(—secondary) | foundation.palette.secondary |
| var(—textPrimary) | foundation.palette.textPrimary |
| var(—textInverse) | foundation.palette.textInverse |
| var(—font-heading) | foundation.fonts.heading |
| var(—font-body) | foundation.fonts.body |

## Ejemplo de un json de tema

```
{
  "id": "slate",
  "name": "Slate",
  "version": "1.0.0",
  "description": "A warm, authoritative theme with cream background, Adobe red accents, and the Roboto Slab + Roboto type system",
  "author": "Content Composer",
  "source": "custom",
  "isDefault": false,
  "foundation": {
    "palette": {
      "foreground": "#1A1A1A",
      "background": "#FAF7F2",
      "accent": "#E8001C",
      "backgroundSubtle": "#F0EBE1",
      "secondary": "#D9D3C9",
      "textPrimary": "#1A1A1A",
      "textInverse": "#FFFFFF"
    },
    "fonts": {
      "heading": "Roboto Slab, Georgia, 'Times New Roman', serif",
      "body": "Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    },
    "spacing": {
      "horizontal": {
        "xs": "4px",
        "s": "8px",
        "m": "12px",
        "l": "16px",
        "xl": "24px"
      },
      "vertical": {
        "xs": "4px",
        "s": "8px",
        "m": "16px",
        "l": "24px",
        "xl": "32px"
      }
    },
    "radius": {
      "none": "0px",
      "s": "4px",
      "m": "8px",
      "l": "16px",
      "full": "9999px"
    },
    "logo": null
  },
  "elements": {
    "text": {
      "lessonTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "48px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "center",
        "letterSpacing": "-0.01em",
        "lineHeight": "130%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "topicTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "40px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "135%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "blockHeading": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "140%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "subheading": {
        "fontFamily": "var(--font-body)",
        "fontSize": "20px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "question": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "caption": {
        "fontFamily": "var(--font-body)",
        "fontSize": "13px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.02em",
        "lineHeight": "170%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "paragraph": {
        "fontFamily": "var(--font-body)",
        "fontSize": "16px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "190%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "buttonLabel": {
        "fontFamily": "var(--font-body)",
        "fontSize": "14px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textInverse)",
        "textAlign": "center",
        "letterSpacing": "0.06em",
        "lineHeight": "125%",
        "textDecoration": "none",
        "textTransform": "uppercase",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      }
    },
    "canvas": {
      "background": "var(--background)"
    },
    "header": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "footer": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "lessonHeader": {
      "background": "var(--accent)"
    },
    "topic": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "navigation": {
      "background": "var(--backgroundSubtle)",
      "border": "1px solid var(--secondary)"
    },
    "button": {
      "background": "var(--accent)"
    },
    "pagination": {
      "background": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "paragraphBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "nestedAccentColor": "var(--accent)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageBlock": {
      "background": "transparent",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "videoBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageGrid": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--accent)",
      "cardShadowOffset": "0px 2px 8px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "accordion": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "carousel": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "flipCard": {
      "background": "transparent",
      "cardFrontBackgroundColor": "var(--backgroundSubtle)",
      "cardBackBackgroundColor": "var(--accent)",
      "arrowColor": "var(--textInverse)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "tabs": {
      "background": "transparent",
      "activeBg": "var(--accent)",
      "inactiveBg": "var(--backgroundSubtle)",
      "containerBg": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "timeline": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "trackColor": "var(--secondary)",
      "progressCompletedBg": "var(--accent)",
      "progressCurrentBorder": "var(--accent)",
      "progressUnreachedBg": "var(--secondary)",
      "progressUnreachedBorder": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "assessment": {
      "background": "transparent",
      "optionTextColor": "var(--textPrimary)",
      "optionIndicatorColor": "var(--accent)",
      "optionSelectedColor": "var(--accent)",
      "optionCheckmarkColor": "var(--textInverse)",
      "optionBackgroundColor": "var(--background)",
      "optionHoverBackgroundColor": "var(--backgroundSubtle)",
      "buttonBackgroundColor": "var(--accent)",
      "buttonTextColor": "var(--textInverse)",
      "buttonHoverBackgroundColor": "var(--accent)",
      "feedbackCorrectColor": "#D7F7E1",
      "feedbackIncorrectColor": "#FFEBE8",
      "feedbackTextColor": "#111111",
      "optionBorderCorrectColor": "#079355",
      "optionBorderIncorrectColor": "#D73220",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    }
  }
}
```
