---
description: Aprenda a importar un archivo JSON de tema personalizado en el compositor de contenido y a guardarlo como un nuevo tema personalizado disponible en el panel Temas del curso.
jcr-language: en_us
title: Importar un tema
source-git-commit: f8687710f5b73e8b7cf8d56057cac25483f38cdc
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Importar un tema

Importe un archivo JSON personalizado para aplicar los cambios como un nuevo tema en Composición de contenido.

1. Seleccione **Temas** en la barra de herramientas.

2. Seleccione **Importar** en las opciones de **tema del curso**.
   ![](../assets/48_course_themes_import_button_updated.png)

3. Elija el archivo JSON personalizado de su equipo.

4. Seleccione **Guardar como nuevo** para crear un nuevo tema personalizado.

## Descripción general de la estructura JSON del tema

Un archivo JSON de tema tiene cinco áreas principales:

| Sección | Controles |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metadatos (id., nombre, versión, descripción, autor, origen, isDefault) | Identidad de tema e información de visualización |
| foundation.palette | Los 7 tokens de color principales (primer plano, fondo, acento, fondo, sutil, secundario, textPrimary, textInverse) a los que se hace referencia en todo el tema mediante var(—tokenName) |
| foundation.fonts | Pilas de fuentes de encabezado y cuerpo |
| foundation.spacing y foundation.radius | Escala de espaciado horizontal/vertical y tokens de radio de vértice |
| elements | Tipografía y estilo estructural para cada función de texto (lecciónTítulo, temaTítulo, bloqueEncabezado, subencabezado, pregunta, título, párrafo, botónEtiqueta) y cada componente (párrafoBloque, imagenBloque, vídeoBloque, imagenCuadrícula, acordeón, carrusel, flipCard, pestañas, cronología, evaluación) |

Como la mayoría de los valores hacen referencia a tokens de paleta que utilizan var(—tokenName), la actualización de un único token, como el acento, se produce automáticamente en cascada, lo que cambia en todos los elementos que hacen referencia a él. No es necesario buscar valores de color individuales.

