---
jcr-language: en_us
title: Personalizar una plantilla de Report Builder duplicada
description: Edite una copia de una plantilla de Report Builder de Adobe Learning Manager para que coincida con sus necesidades específicas de clasificación, filtros y columnas.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# Personalizar una plantilla de Report Builder duplicada

Después de duplicar una plantilla, puede agregar o quitar columnas, actualizar filtros, cambiar el nombre de las columnas y ajustar la ordenación antes de guardar y descargar\. Este artículo trata cada paso de personalización\.

Antes de empezar, duplica una plantilla de la pestaña **Plantillas**.

## Agregar y quitar columnas

1. En la vista de edición, busque el conjunto de datos que contiene la columna que desea agregar.
2. Seleccione **+** junto al nombre de la columna. La columna aparece en el lienzo del informe.
3. Para agregar la misma columna más de una vez, por ejemplo, para contar dos valores de estado diferentes. Vuelva a seleccionar **+** para esa columna.
4. Para eliminar una columna, selecciónela en el lienzo y, a continuación, seleccione el icono de eliminación.

## Reordenar y cambiar el nombre de columnas

1. Arrastre una columna a la posición deseada en el lienzo. El orden del lienzo coincide con el orden de las columnas del archivo descargado.
2. Para cambiar el nombre de una columna, seleccione su campo de alias e introduzca el nombre que desea que aparezca como encabezado de columna en el informe.

## Actualizar filtros

1. Para cambiar un valor de filtro existente, seleccione la fila de filtro, edite el valor y, a continuación, confirme.
2. Para agregar un nuevo filtro, seleccione **Agregar filtro**.
3. Elija el campo por el que desea filtrar.
4. Seleccione un operador. Los operadores disponibles dependen del tipo de datos del campo.
5. Introduzca o seleccione un valor:
   * En los campos de cadena, escriba para buscar y seleccionar entre las sugerencias.
   * Para los campos de lista, seleccione uno o varios valores en el selector.
   * Para los campos de fecha, introduzca una fecha o elija un intervalo relativo como los últimos 90 días.
6. Para eliminar un filtro, seleccione el icono de eliminación en esa fila de filtros.

## Actualizar ordenación

1. Seleccione el icono de ordenación en la columna por la que desea ordenar.
2. Seleccione **Ascendente** o **Descendente**.
3. Para ordenar por columnas adicionales, repita para cada columna. La primera columna ordenada es primaria; se aplican ordenaciones adicionales dentro de los vínculos.

>[!TIP]
>
>Aplique siempre al menos una ordenación. Sin la ordenación, el orden de las filas puede diferir entre las descargas del mismo informe.

## Guardar y descargar

1. Seleccione Guardar para guardar los cambios en la pestaña **Informes**.
2. Seleccione **Descargar** para generar el informe. Recibirá una notificación en la aplicación cuando el archivo esté listo.
