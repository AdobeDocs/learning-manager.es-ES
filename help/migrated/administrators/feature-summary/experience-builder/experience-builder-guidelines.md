---
title: Limitaciones y directrices de Experience Builder en Adobe Learning Manager
description: Las directrices y limitaciones de Experience Builder proporcionan sugerencias de contenido y cursos personalizados a los alumnos mediante algoritmos basados en IA.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Limitaciones y directrices de Experience Builder

Experience Builder es una potente herramienta diseñada para ayudar a los usuarios a crear páginas web dinámicas e interactivas con facilidad. Para garantizar un rendimiento, un uso y una seguridad óptimos, es esencial seguir determinadas directrices y recomendaciones al configurar páginas, utilizar widgets y personalizar diseños. Este documento proporciona una descripción general detallada de las notas y puntos importantes que los usuarios deben tener en cuenta al trabajar con Experience Builder.

La información que se describe aquí abarca aspectos clave como las configuraciones de página y widget, las opciones de personalización, la gestión de código personalizado y consideraciones de seguridad. Al cumplir estas recomendaciones, los usuarios pueden maximizar la eficiencia de sus proyectos de Experience Builder, evitar los obstáculos comunes y adaptarse sin problemas a las actualizaciones y los cambios.

## Configuración de página y widget

### Máximo de páginas

Puedes crear hasta 1000 páginas en Experience Builder. Este es el límite superior, pero se recomienda planificar las páginas estratégicamente para evitar una complejidad innecesaria.

### Widgets por página

* **Límite máximo**: se pueden agregar un máximo de 25 widgets a una sola página.
* **Límite recomendado**: para mejorar el rendimiento, se recomienda no usar más de 10 widgets por página.
* **Widgets basados en API**: los widgets que dependen de las API de ALM (por ejemplo, cursos y rutas, categoría, mi aprendizaje, aprendizaje social, calendario, cumplimiento, tabla de posiciones) deben limitarse a 10 por página.
* **Widgets independientes**: los widgets como HTML y cuadro de contenido, que no dependen de las API de ALM, se pueden utilizar hasta el límite máximo de 25 widgets.

### Widgets de un solo uso

Algunos widgets, como Calendario, Aprendizaje social, Cumplimiento y Tabla de posiciones, solo se deben utilizar una vez por página. Su uso varias veces puede provocar problemas de rendimiento, especialmente para los widgets como el calendario, que requieren recursos significativos para cargar las sesiones.

### Directrices de tamaño del widget

Los widgets como Calendario, Tabla de posiciones, Social y Cumplimiento deben colocarse en diseños con un ancho mínimo de un tercio de la página. Los widgets de una sola tarjeta son los más adecuados para esta anchura para garantizar una visualización óptima. Los widgets como Calendario y Cumplimiento (vista expandida) están diseñados para diseños de media anchura con el fin de ofrecer una mejor experiencia de usuario. Para otros tamaños de diseño, los widgets se ajustarán de forma adaptable para ajustarse al espacio disponible y mantener la facilidad de uso.

El uso de widgets dentro de estas directrices de tamaño recomendadas mejora la interacción general del usuario.

## Directrices de personalización

### Distancias de píxeles predeterminadas

**Distancia vertical**: la distancia vertical predeterminada entre los widgets es de 80 píxeles.
**Distancia horizontal**: la distancia horizontal predeterminada entre los widgets es de 20 píxeles.

### CSS personalizado

Los usuarios pueden anular las distancias predeterminadas y otras propiedades visuales mediante CSS personalizado.

Pasos para la personalización:

* Inspect utiliza los elementos de página para identificar las clases de CSS.
* Aplique los cambios a nivel global, de widget o de página.

Por ejemplo, para reducir la distancia vertical entre los widgets, modifique la propiedad CSS de la clase correspondiente.

## Colocación de menús

Los menús se pueden colocar en la parte superior o izquierda de la página. Se pueden realizar más ajustes con CSS personalizado.

## Recomendaciones específicas de funciones

### Widgets de aprendizaje social e interacción

* Si estas funciones están desactivadas, los administradores deben eliminar manualmente los widgets correspondientes de las páginas.
* Las páginas deben rediseñarse para garantizar que sigan siendo funcionales y visualmente intactas después de deshabilitar estas funciones.

## Administración de código personalizado

### Impacto de las actualizaciones

* El código personalizado existente (HTML, CSS, JS) insertado en el motor podría no funcionar del modo esperado después de las actualizaciones de Experience Builder.
* Los usuarios deben volver a escribir su código para alinearse con los nuevos cambios de la interfaz de usuario, como los nombres de clase actualizados.

### Soporte frontal

* Añada código personalizado directamente en el portal de administración mediante widgets de HTML o bloques de CSS/JS de nivel de cuenta.

### Renuncia

* Es posible que el código personalizado no funcione de la forma prevista en futuras versiones, por lo que será necesario realizar ajustes. Prepárate para actualizar el código después de cada versión.

## Recomendaciones generales

### Consideraciones de rendimiento

* Evite exceder los límites recomendados de los widgets para evitar una degradación del rendimiento.
* El uso de widgets que consuman muchos recursos (por ejemplo, un calendario) varias veces en una página puede afectar significativamente a los tiempos de carga de la página.

### Consideraciones de seguridad

* **Widgets de HTML**: Debes asegurarte de que el código maneja problemas de seguridad como los ataques de secuencias de comandos en sitios cruzados (XSS), ya que están fuera del ámbito del control de Experience Builder.
* **Pie de página personalizado**: al personalizar el pie de página mediante HTML o CSS, asegúrese de que el código cumpla las prácticas recomendadas de seguridad.

### Cambios importantes

Las actualizaciones de Experience Builder pueden introducir cambios importantes en las personalizaciones. Usted debe:

* Ajuste el código para que coincida con los nuevos elementos de la IU.
* Pruebe las personalizaciones después de cada actualización.

## Notas adicionales

### Implementación de CSS personalizada

* Puede inspeccionar elementos de página, copiar clases CSS y aplicar las propiedades que desee para personalizar los diseños de forma global, en el nivel de widget o en el nivel de página.

### ID de widget e ID de página

Cada widget y página tiene ID exclusivos que se pueden utilizar para realizar cambios CSS específicos. Esto permite la personalización en diferentes niveles:

* Nivel global: aplique cambios CSS en todas las páginas.
* Nivel de widget: Aplique cambios de CSS a widgets específicos.
* Nivel de página: Aplique cambios CSS a todos los widgets de una página específica.










