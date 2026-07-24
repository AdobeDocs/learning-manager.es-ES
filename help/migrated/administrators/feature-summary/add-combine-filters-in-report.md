---
jcr-language: en_us
title: Agregar y combinar filtros en un informe
description: Restrinja los datos del informe en Adobe Learning Manager Report Builder mediante filtros únicos, lógica AND/OR y grupos de filtros anidados.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---


# Agregar y combinar filtros en un informe

## Información general

Los filtros le permiten definir el ámbito del informe exactamente en los registros que necesita. Puede aplicar un solo filtro, combinar varios filtros con la lógica AND u OR y crear grupos anidados para condiciones complejas.

## Agregar un filtro

Utilice filtros para limitar el informe a un subconjunto específico de datos en lugar de verlo todo.

Por ejemplo, es posible que desee comprender cuántos alumnos se han inscrito en los cursos en los últimos 365 días. En este caso, se aplica un filtro de fecha en la fecha de inscripción para incluir únicamente la actividad reciente.

1. Inicie Report Builder y seleccione **Crear informe**.
2. Escriba el nombre y la descripción del informe.
3. Seleccione las siguientes columnas: <dataset>:<column name>

   * Inscripción - Fecha de inscripción
   * Usuario: nombre

   ![](assets/report-builder-0024.png)

4. En la sección Informes, seleccione **Agregar filtro**.
5. Busque o busque el campo por el que desea filtrar. En este ejemplo, seleccione **Inscripción - Fecha de inscripción**.

   ![](assets/report-builder-0025.png)

6. Seleccione **Agregar**.
7. Seleccione un operador. Los operadores disponibles dependen del tipo de datos del campo:

   * Campos de cadena: contiene, es igual a, empieza por
   * Campos numéricos: mayor que, menor que, igual a, entre
   * Campos de fecha: es igual a los últimos N días, antes, después, entre
   * Campos de lista (enum): está en, no está en

8. En este caso, seleccione **en el último año**.

   ![](assets/report-builder-0026.png)

9. Seleccione **Guardar informe** y seleccione **Acciones** > **Descargar** para descargar el informe.

El informe descargado muestra una lista de todos los usuarios que se han inscrito en un objeto de aprendizaje en los últimos 365 días.

## Añadir varios filtros con la lógica Y/O

Cuando se agrega un segundo filtro, la relación predeterminada entre filtros es AND; ambas condiciones deben ser verdaderas para que aparezca una fila.

Por ejemplo, puede que desee identificar a los alumnos que se han inscrito en cursos en los últimos 365 días Y enviar un informe a un responsable específico. En este caso, ambas condiciones deben ser verdaderas, por lo que los filtros se combinan usando la lógica AND.

1. Inicie Report Builder y seleccione **Crear informe**.
2. Escriba el nombre y la descripción del informe.
3. Seleccione las siguientes columnas: <dataset>:<column name>

   * Usuario: nombre
   * Usuario: nombre del responsable
   * <span class="mark">Inscripción - Fecha de inscripción</span>

4. Agrupar por la columna **Nombre del administrador de usuarios**.
5. En la sección Filtro, seleccione los siguientes filtros:

   * Inscripción: fecha de inscripción i **s en el último año**
   * Usuario: el nombre del administrador **empieza por** N
   * Usuario: el nombre del administrador **no está vacío**

     ![](assets/report-builder-0027.png)

6. Seleccione **Guardar informe** y seleccione **Acciones** > **Descargar** para descargar el informe.

El informe descargado muestra todos los usuarios que se han inscrito en un objeto de aprendizaje en los últimos 365 días **y** informes a un administrador cuyo nombre empieza por N.

## Crear grupos de filtros anidados

Los grupos anidados permiten crear condiciones con varios niveles lógicos, equivalentes a corchetes en una fórmula. Por ejemplo: (Catálogo = Seguridad O Catálogo = Higiene) Y la fecha de finalización está en los últimos 90 días.

Utilice grupos de filtros anidados cuando la lógica incluya una mezcla de condiciones AND y OR que se deben evaluar juntas.

Por ejemplo, utilice una lógica de filtros anidada para identificar las inscripciones incompletas en las que los alumnos tienen un progreso inferior al 50 % o formación vencida, lo que demuestra cómo las condiciones Y y O funcionan en conjunto.

1. Inicie Report Builder y seleccione **Crear informe**.
2. Escriba el nombre y la descripción del informe.
3. Seleccione las siguientes columnas: <dataset>:<column name>

   * Inscripción - Estado
   * Inscripción - Porcentaje de progreso
   * Inscripción - Vencida

     ![](assets/report-builder-0028.png)

4. En la sección **Filtro**, seleccione los siguientes filtros:

   * Inscripción: el estado **no es igual a ninguno de los** completados.
   * Seleccione +.
   * Busque Porcentaje de progreso de inscripción.
   * Seleccione el filtro.
   * Seleccione **Agregar como grupo**.

     ![](assets/report-builder-0029.png)

5. Agregar inscripción: porcentaje de progreso **inferior a** 50.

   ![](assets/report-builder-0030.png)

6. Seleccione +.
7. Busque **Inscripción vencida**.
8. Seleccione el filtro.
9. Seleccione **Agregar como grupo**.

   ![](assets/report-builder-0031.png)

10. Add Enrollment-Overdue es igual a TRUE.
11. Cambie el AND anidado a OR.

    ![](assets/report-builder-0032.png)

12. Seleccione **Guardar informe** y seleccione **Acciones** > **Descargar** para descargar el informe.

El informe descargado enumera todas las inscripciones que están en curso o que no se han iniciado, cuyo porcentaje de progreso es inferior al 50 % o que han vencido.
