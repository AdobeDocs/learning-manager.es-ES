---
jcr-language: en_us
title: Report Builder - conceptos y terminología
description: Comprender los conceptos clave de Report Builder, incluidos conjuntos de datos, columnas, agrupamientos, filtros y agregados, antes de crear el primer informe.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Report Builder: Conceptos y terminología

## Plantillas e informes

**Las plantillas** son configuraciones de informe precompiladas proporcionadas por Adobe Learning Manager. Están diseñados para casos prácticos habituales, seguimiento de inscripciones y finalizaciones, informes de cumplimiento normativo, rendimiento del instructor y están listos para su descarga inmediata. Las plantillas son de sólo lectura; no se pueden editar ni sobrescribir.
![](assets/image003.png)

**Informes** son tus propias configuraciones guardadas. Puede crear un informe desde cero o duplicando una plantilla y editando la copia. Al duplicar una plantilla, la copia se convierte en un informe en la ficha Informes.

Tanto las plantillas como los informes aparecen en Report Builder, pero en fichas independientes.

## Conjuntos de datos

Un conjunto de datos es un grupo con nombre de columnas relacionadas en Report Builder. Cuando se agregan columnas a un informe, se elige entre estos conjuntos de datos. Piense en cada conjunto de datos como una tabla de información sobre un aspecto de los datos de aprendizaje.

El siguiente es un ejemplo de conjuntos de datos disponibles en Report Builder:

* **Usuario:** datos de perfil de alumno, incluidos los campos activos
* **Transcripción:** registros de inscripción y finalización
* **Objeto de aprendizaje:** datos de curso, ruta de aprendizaje y certificación
* **Instancia de objeto de aprendizaje:** detalles a nivel de instancia
* **Catálogo:** datos de etiquetas de catálogo y catálogo
* **Grupo de usuarios:** pertenencia y jerarquía de grupos de usuarios
* **Sesión de módulo:** datos de clase y sesión virtual, incluidos los detalles del módulo de aprendizaje electrónico

>[!NOTE]
>
>Los conjuntos de datos se pueden unir selectivamente. No todas las combinaciones están disponibles en un solo informe.

## Columnas y el botón Agregar

Cada columna que agregue aparecerá como una fila en el lienzo del informe y se convertirá en una columna en el archivo descargado. Puede agregar la misma columna más de una vez. Esto resulta útil cuando desea medir dos valores diferentes del mismo campo. Por ejemplo, puede agregar la columna Estado dos veces: una para contar las inscripciones y una para contar los alumnos en curso mediante el recuento si es agregado.
![](assets/image005.png)

También puede cambiar el nombre de cualquier columna introduciendo un alias. El alias aparece como encabezado de columna en el informe descargado.

## Agrupar por y agregación

Agrupar por resume los datos por un campo seleccionado en lugar de mostrar filas individuales. Por ejemplo, al agrupar por nombre de instructor, se obtiene una fila por instructor en lugar de una fila por inscripción.

Agrupar por sigue el comportamiento estándar de la base de datos: una vez aplicado agrupar por en una columna, cada dos columnas del informe deben tener aplicada una función de agregado. No se pueden mezclar datos de filas individuales con datos agrupados. Las **funciones** de agregado disponibles son:

* **Recuento:** Número total de filas
* **Contar si:** Número de filas en las que el campo coincide con un valor especificado
* **Suma:** total de un **campo** numérico
* **Mín.:** valor más bajo en un campo numérico
* **Máximo:** el valor más alto de un campo numérico
* **Promedio:** valor medio de un campo numérico

Si ha utilizado tablas dinámicas en Excel, agrupar por funciona de la misma manera en el nivel de columna.

## Filtros

Los filtros restringen las filas que aparecen en el informe. Puede aplicar varios filtros y combinarlos con la lógica Y u O.

Los operadores de filtro dependen del tipo de datos de la columna:

* **Campos de cadena:** Contiene, es igual a, comienza por (búsqueda de escritura anticipada disponible para valores reconocidos)
* **Campos numéricos:** Mayor que, menor que, igual a, entre
* **Campos de fecha:** Es igual a, antes, después, entre e intervalos relativos (por ejemplo, últimos 90 días)
* **Campos de enumeración (lista):** Está en, no está en (selector de valor de selección múltiple)

## Lógica AND/OR y grupos de filtros anidados

Varios filtros tienen como valor predeterminado la lógica AND. Todas las condiciones deben ser verdaderas para que aparezca una fila. Puede cambiar el operador entre dos filtros cualesquiera a O. También puede agrupar filtros mediante Agregar como grupo, lo que crea un corchete. Los filtros dentro del grupo se evalúan juntos antes de combinarse con filtros fuera de él.

Esto le permite crear condiciones como:

(catálogo = Seguridad O catálogo = Higiene) Y la fecha de finalización está en los últimos 90 días.

Puede anidar grupos dentro de otros grupos para admitir una lógica compleja de varios niveles.

## Ordenación

Puede ordenar por una o varias columnas. La primera columna por la que se ordena es la ordenación principal. Se aplican ordenaciones adicionales dentro de los vínculos de la columna principal.

Aplique siempre al menos una ordenación cuando necesite un resultado coherente. Dado que la generación de informes se ejecuta en un sistema distribuido, no se garantiza el orden de filas entre dos descargas del mismo informe a menos que se aplique la ordenación.

## Datos de tendencias frente a datos de instantáneas

Cualquier informe que utilice un agregador de tendencias, como mes a mes o semana a semana, refleja los datos de instantáneas actuales agrupados por fecha. No refleja el estado histórico de los datos en cada fecha pasada.

Por ejemplo, una tendencia de inscripción agrupada por mes muestra cuántas inscripciones existen actualmente, distribuidas entre los meses en que se crearon. No tiene en cuenta a los alumnos que más tarde cancelaron su inscripción o cambiaron de grupo de usuarios. Esos cambios no se aplican retroactivamente a los meses pasados.

## Alumnos eliminados y campos activos

El Report Builder admite la inclusión de alumnos eliminados en los informes y la recuperación de los valores de campo activos. Use la columna **Fecha de eliminación** del conjunto de datos **Usuario** para crear el informe.

## Prácticas recomendadas

* Lea la referencia de los conjuntos de datos disponibles antes de crear un informe desde cero. Saber qué conjunto de datos contiene los campos que necesita ahorra un tiempo de configuración considerable.
* Aplicar la ordenación antes de suscribirse a un informe programado. Esto garantiza un orden de fila coherente en todas las entregas.
* Si ve filas duplicadas inesperadas, compruebe si el informe incluye un campo que puede tener varios valores por fila, como el nombre de un instructor para una sesión con varios instructores.
