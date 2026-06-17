---
jcr-language: en_us
title: Ordenar columnas de informe en Report Builder
description: Aplique la ordenación de una o varias columnas en Adobe Learning Manager Report Builder para controlar el orden de fila de los informes descargados.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Ordenar columnas de informe en Report Builder

La ordenación determina el orden de las filas en el archivo de informe descargado\. Aplique la ordenación siempre que sea importante una salida coherente.

## Agregar una ordenación

En este ejemplo, encontrará los cursos que tienen las finalizaciones más altas.

1. Inicie Report Builder y seleccione **Crear informe**.
2. Escriba el nombre y la descripción del informe.
3. Seleccione las siguientes columnas: `<dataset>:<column name>`
a. Objeto de aprendizaje: Nombre del objeto de aprendizaje
b. Objeto de aprendizaje: Estado del objeto de aprendizaje
c. Objeto de aprendizaje: recuento de finalización
4. En la sección Ordenación, seleccione **Agregar ordenación**.
5. Seleccione **Objeto de aprendizaje - Recuento de finalización**.
6. Seleccione un orden de clasificación **Ascendente** o **Descendente**.
   ![](assets/image032.jpg)
7. Seleccione **Agregar**.
8. Seleccione **Guardar informe** y seleccione **Acciones** > **Descargar** para descargar el informe.

El informe descargado muestra una lista de todos los registros, ordenados por el número de finalizaciones del curso.

## Agregar ordenación de varias columnas

En este ejemplo, generará un informe para medir el rendimiento de los administradores.

Para ordenar por varias columnas:

1. Inicie **Report Builder** y seleccione **Crear informe**.
2. Escriba el nombre y la descripción del informe.
3. Seleccione las siguientes columnas: `<dataset>:<column name>`
a. Usuario: nombre
b. Usuario: nombre del responsable
c. Transcripción del módulo: estado
d. Transcripción del módulo: porcentaje de progreso
4. Añada los siguientes agregados:
a. Agrupar por usuario: nombre del responsable
b. Recuento de Usuario Distinto - Nombre
c. Count If=COMPLETED Transcripción del módulo - Estado
d. Transcripción Media Del Módulo: Porcentaje De Progreso
   ![](assets/image033.png)
5. En la sección **Sort**, agregue la siguiente ordenación de varias columnas:
a. Transcripción del módulo - Estado: Descendente
b. Usuario - Nombre del responsable: Ascendente
   ![](assets/image034.jpg)
6. Seleccione Guardar informe y elija Acciones > Descargar para descargar el informe.

El informe descargado proporciona un resumen del rendimiento según el responsable en el que se muestran distintos recuentos de alumnos, recuentos de inscripciones basados en el estado y porcentajes medios de progreso. Se destacan los niveles de participación y el progreso de la formación en los diferentes grupos de gestores.
