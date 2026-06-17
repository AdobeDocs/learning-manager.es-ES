---
jcr-language: en_us
title: Introducción a una plantilla de Report Builder
description: Crea un informe rápidamente en Adobe Learning Manager Report Builder a partir de una plantilla prediseñada para casos prácticos habituales.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 1%

---


# Introducción a una plantilla de Report Builder

Las plantillas son configuraciones de informes listas para usar proporcionadas por Adobe Learning Manager. Cada plantilla está diseñada para un caso de uso específico, como el seguimiento de la inscripción y la finalización, los informes de cumplimiento o el rendimiento del instructor. Puede descargar una plantilla directamente o duplicarla para crear una copia editable.

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Selecciona **Informes** en el panel izquierdo y luego selecciona **Report Builder**.
3. Seleccione la ficha **Plantillas**.
4. Examine las plantillas disponibles. Cada plantilla recibe un nombre por su caso de uso.
   ![](assets/image007.png)
5. Seleccione un nombre de plantilla para abrir su vista previa de solo lectura. Para este ejemplo, seleccione Duplicar junto a la plantilla MoM Catálogo inteligente - Recuento de cursos. Revise las columnas, los filtros aplicados y el orden de clasificación. Al duplicar una plantilla, Report Builder abre una copia editable con la configuración existente de la plantilla ya cargada. El nombre del informe, la descripción, las columnas, los filtros y la ordenación se pueden editar antes de guardar.

## Nombre y descripción del informe

1. En el campo **Nombre**, reemplace el nombre predeterminado (por ejemplo, _copia de Catalog Wise_ - _Course Count MoM_) por un nombre único para el informe. Se requiere un nombre.
2. En el campo **Descripción**, escriba un breve resumen de lo que contiene el informe. Esto ayuda a otros administradores a comprender el propósito del informe cuando lo ven o editan.

## Agregar y configurar columnas

La sección **Columns** tiene dos paneles: **Seleccionar columnas** a la izquierda y **Columnas seleccionadas** a la derecha.

### Agregar una columna

1. En el panel **Seleccionar columnas**, expanda un conjunto de datos seleccionando su nombre. Por ejemplo, **Catalog** o **Active Field User Group**.
2. Seleccione el icono **+** junto a la columna que desea agregar. La columna aparece en el panel **Columnas seleccionadas** de la derecha.
   ![](assets/image009.png)
3. Para agregar la misma columna más de una vez. Por ejemplo, para aplicar dos agregados diferentes al mismo campo. Vuelva a seleccionar **+** para esa columna.

### Reordenar columnas

Arrastre el controlador a la izquierda de cualquier fila de columna en el panel **Columnas seleccionadas** para moverlo a una posición diferente. El orden de las columnas del panel coincide con el del informe descargado.

### Cambiar el nombre de una columna

1. Seleccione el icono **edit** (lápiz) en una fila de columna.
   ![](assets/image011.png)
2. Introduzca un alias. El alias aparece como encabezado de columna en el informe descargado en lugar del nombre de campo predeterminado.
   ![](assets/image013.png)

### Quitar una columna

Seleccione el icono **×** en una fila de columna para quitarlo del informe.

## Aplicar grupo por

El control **Agrupar por** aparece en la parte superior del panel **Columnas seleccionadas**.

1. Seleccionar **Agrupar por: Seleccione**.
   ![](assets/image015.png)
2. Seleccione las columnas por las que desea agrupar. Puede seleccionar más de uno. En la captura de pantalla, el informe está agrupado por _catálogo_ y _mes de creación_.
3. Cada columna de agrupación seleccionada aparece como una etiqueta debajo del control Agrupar por . Para quitar una columna de agrupación, seleccione **×** en su etiqueta.

>[!NOTE]
>
>Cuando se aplica agrupar por, cada columna que no sea una columna de grupo debe tener aplicada una función de agregado. Una columna sin agregado producirá un error.

## Aplicación de un agregado a una columna

1. En cualquier columna que no sea agrupar por del panel **Columnas seleccionadas**, seleccione **Agregar por**.
2. Elija una función en el menú desplegable. En la captura de pantalla, **Objeto de aprendizaje** - **Id. de objeto de aprendizaje** usa **Distintivo de recuento**, con el alias de ount_of_course.

Funciones agregadas disponibles:

| Función | Lo que devuelve |
|----------|-----------------|
| Recuento | Número total de filas del grupo |
| Contar distintos | Número de valores únicos en el grupo |
| Contar si | Número de filas que coinciden con un valor especificado |
| Suma | Total de un campo numérico en el grupo |
| min | Valor más bajo del grupo |
| Máx. | Valor más alto del grupo |
| Promedio | Valor medio en todo el grupo |

## Aplicar filtros

La sección **Filters** está debajo de la sección **Columns**. Los filtros restringen las filas que aparecen en el informe.

1. Para agregar un filtro, seleccione el icono **+** situado a la derecha de la sección Filtros.
2. Elija el campo por el que filtrar.
   ![](assets/image017.png)
3. Seleccione un operador e introduzca o elija un valor.

Para editar un filtro existente, seleccione el icono **pencil** en la fila del filtro. Para añadir un grupo de filtros anidado, seleccione el icono + con corchetes a la derecha de una fila de filtros.

## Configurar ordenación

La sección Ordenación se encuentra debajo de la sección Filtros.

1. Seleccione **+ Agregar ordenación** para agregar una ordenación.
2. Elija la columna por la que desea ordenar y seleccione **Ascendente** o **Descendente**.
   ![](assets/image020.png)
3. Repita el proceso para añadir ordenaciones secundarias. Arrastre el controlador a la izquierda de cada fila de ordenación para cambiar la prioridad.

>[!TIP]
>
>Aplique siempre al menos una ordenación. Sin la ordenación, el orden de las filas puede diferir entre las descargas del mismo informe.

## Guardar el informe

Seleccione **Guardar informe** en la esquina superior derecha. El informe se guarda en la pestaña **Informes** y está listo para su descarga.

## Prácticas recomendadas

* Usa alias en todas las columnas para que el informe descargado tenga encabezados significativos en lugar de nombres de campo como _Objeto de aprendizaje_ - _ID de objeto de aprendizaje_.
* Utilice Count Distinct en lugar de Count cuando desee registros únicos, por ejemplo, cursos distintos por catálogo en lugar de filas totales.
* Aplica la ordenación antes de guardar, especialmente en los informes que vas a compartir o a los que te suscribirás.
* Mantenga la descripción actualizada. Otros administradores confían en él para comprender el ámbito del informe sin abrirlo.
