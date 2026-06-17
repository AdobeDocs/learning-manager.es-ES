---
jcr-language: en_us
title: Crear un informe personalizado en Report Builder
description: Cree un informe totalmente personalizado en Adobe Learning Manager Report Builder seleccionando sus propias columnas, filtros, configuración de agrupar por y ordenando desde un lienzo en blanco.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---


# Crear un informe personalizado en Report Builder

La creación desde cero funciona mejor cuando tiene una imagen clara de las columnas y la salida que necesita, y ninguna plantilla existente coincide con su caso de uso. Si es la primera vez que utiliza Report Builder, considere la posibilidad de empezar con una plantilla.

En este ejemplo, identificará a los alumnos de cada responsable que están en riesgo de recibir cursos de cumplimiento.

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **Informes** y, a continuación, seleccione **Report Builder**.
3. Selecciona la pestaña **Informes** y luego selecciona **Crear informe**.
4. Introduzca un nombre de informe. Se requiere un nombre. También puede introducir una descripción.
   ![](assets/image011.png)
5. En el panel de columnas, seleccione los siguientes conjuntos de datos y amplíelos:
a. Usuario
b. Objeto de aprendizaje
c. Estado de cumplimiento del usuario
6. Seleccione **+** junto a las siguientes columnas que desee incluir. Las columnas seleccionadas aparecen en el lienzo del informe.
a. Usuario\Nombre
b. Usuario\Nombre del responsable
c. Objeto de aprendizaje\Nombre del objeto de aprendizaje
d. Estado de cumplimiento del usuario\% de finalización
e. Estado de cumplimiento del usuario\Cumplimiento %
!   [&#128279;](assets/image012.png)
7. Reorganice las columnas arrastrándolas en el lienzo.
8. Para cambiar el nombre de una columna, introduzca un nombre en el campo de alias de la columna. El alias aparece como encabezado de columna en el archivo descargado.
9. Seleccione **Guardar informe**.

## Descargar el informe

1. Seleccione **Acciones** en la esquina superior derecha.
   ![](assets/image013.png)
2. Seleccione Descargar. Puede descargar el informe desde el icono de notificaciones cuando esté listo.

El informe descargado en la extensión de archivo .csv contiene las siguientes columnas:

1. name
2. managerName
3. name
4. completedPct
5. compliancePct

## Aplicar agrupar por, filtros y ordenación

### Filtro

Una vez descargado el informe, aplique un filtro en el que el valor de completedPct O compliancePct sea igual a 100.

1. Abra el informe y seleccione **Editar** en la esquina superior derecha.
2. Seleccione **Agregar filtro** y busque en las columnas donde desee aplicar los filtros.
   ![](assets/image014.png)
3. Seleccione **Agregar**.
4. Combine los filtros con la lógica AND/OR; seleccione el operador alternar entre filas de filtro.
   ![](assets/image015.png)
5. Seleccione **Guardar informe** y descargue el informe.

El informe descargado contiene registros en los que completedPct O compliancePct es igual a 100.

### Agrupar por

Agrupar los registros por responsable en:

* Agregar datos de alumnos por responsable
* Calcular promedios a nivel de responsable
* Contar alumnos en cada responsable

1. Abra el informe y seleccione **Editar** en la esquina superior derecha.
2. Seleccione **Agrupar por:Select** y seleccione la columna **Nombre del administrador de usuarios**.
   ![](assets/image016.png)
3. Agregue las siguientes columnas:
a. Usuario\Nombre
b. Objeto de aprendizaje\Nombre del objeto de aprendizaje
4. Seleccione **Count** como una función de agregado para las columnas.
   ![](assets/image017.png)
5. Repita el proceso para Objeto de aprendizaje\Nombre de objeto de aprendizaje.
   ![](assets/image018.png)
6. Seleccione **Guardar informe** y descargue el informe.

El informe descargado contiene un resumen del rendimiento de la formación del alumno según el responsable. Muestra las tasas medias de finalización, las puntuaciones medias de cumplimiento y los recuentos totales de alumnos de cada responsable. Los datos indican la finalización universal de la formación en todos los grupos, mientras que el rendimiento de la conformidad varía significativamente entre los gestores.

### Ordenar

Ordene el informe en orden descendente por el número de alumnos de cada responsable.

1. Abra el informe y seleccione **Editar** en la esquina superior derecha.
2. Seleccione **Agregar ordenación**.
3. Busque el nombre de usuario y seleccione **Usuario\Nombre**.
4. Seleccione **Descendente**.
   ![](assets/image019.png)
5. Seleccione **Agregar**.
6. Seleccione **Guardar informe** y descargue el informe.

El informe descargado contiene el número de alumnos por responsable en orden descendente.
