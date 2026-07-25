---
description: Todo sobre el Libro de calificaciones desde la perspectiva del alumno
jcr-language: en_us
title: Libro de calificaciones para alumnos
source-git-commit: c6ad5527fa5156d1a681fa0f21fb259ac3ebf782
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---


# Libro de calificaciones para alumnos

## Iniciar un curso con un libro de calificaciones

Cuando el libro de calificaciones está habilitado y visible para un curso en Adobe Learning Manager, aparece una pestaña **Libro de calificaciones** en la página de descripción general del curso. Utilícelo para ver su puntuación ponderada para cada módulo, su puntuación agregada actual y si ha aprobado o aún necesita completar más del curso.

![](assets/image_0008.png)

## Cuando el libro de calificaciones está disponible

La ficha **Libro de calificaciones** aparece junto a **Módulos**, **Notas** y **Discusiones** en el reproductor del curso cuando el autor o administrador ha habilitado la visibilidad del libro de calificaciones para el curso. Si la ficha no está visible, el libro de calificaciones no se ha habilitado para este curso o el administrador ha deshabilitado la visibilidad del alumno. Las puntuaciones pueden seguir grabándose y ser visibles para el administrador.

Puedes abrir la pestaña **Libro de calificaciones** en cualquier momento durante la inscripción:

![](assets/image_0009.png)

* **Antes de comenzar:** Después de inscribirse, verá la lista completa de módulos puntuables con sus porcentajes de grosor, las marcas máximas para cada uno y los criterios de aprobado establecidos por el autor. Esto le muestra exactamente cómo se califica el curso antes de comenzar.
* **Mientras estás en progreso:** A medida que terminas los módulos y las calificaciones se registran, el libro de calificaciones se actualiza para mostrar tus calificaciones hasta el momento junto con los módulos que aún no se han intentado o que están a la espera de ser calificados.
* **Después de completar:** El libro de calificaciones muestra todas las puntuaciones finales del módulo, la puntuación total del curso calculada y un resultado **Superado** en el encabezado.

## Ver el libro de calificaciones

* En **Mi aprendizaje**, seleccione su curso.
* Seleccione la pestaña **Libro de calificaciones** en la página del curso.

  El encabezado del libro de calificaciones muestra:

  ![](assets/image_0010a.png)

* **Criterio de aprobado:** Puntuación mínima agregada y número de módulos necesarios
* El número de módulos necesarios que ha completado del total
* Tu **puntuación agregada** actual como porcentaje
* Tu estado actual del curso: **No iniciado**, **Finalización pendiente**, **Aprobado** o **Error**

La tabla de módulos debajo del encabezado muestra las siguientes columnas para cada módulo:

| **Columna** | **Lo que muestra** |
|------------|-------------------|
| **Módulo** | El nombre y tipo del módulo |
| **Estado** | El estado de finalización o puntuación de este módulo (consulte la referencia de estado a continuación) |
| **Peso** | El porcentaje que este módulo contribuye a la puntuación agregada |
| **Puntuación** | Su puntuación para este módulo (por ejemplo, 40/100) |
| **Contribución** | Los puntos porcentuales reales que este módulo ha agregado a su puntuación agregada hasta el momento |

## Ver el grosor del módulo desde la ficha Módulos

También puede ver el grosor de cada módulo desde la pestaña **Módulos** sin abrir el libro de calificaciones.

En la página del curso, seleccione la pestaña **Módulos**.

![](assets/image_0011.png)

La ficha **Módulos** muestra el porcentaje de ponderación de cada módulo y el número de módulos necesarios para completar el curso.

## Puntuaciones de módulo con varios intentos

Si un módulo permite varios intentos, la puntuación mostrada en el libro de calificaciones dependerá de cómo lo haya configurado el autor del curso:

* **Máxima:** Se muestra la mejor puntuación de cualquier intento. Una puntuación más baja en un intento posterior no reduce la puntuación grabada.
* **Último:** Siempre se muestra la puntuación del intento más reciente. Una puntuación más baja en un intento posterior sustituye a la anterior.

## Comprender el estado del módulo

Cada módulo del libro de calificaciones muestra uno de los siguientes estados:

![](assets/image_0012.png)

| **Estado** | **Qué significa** |
|------------|-------------------|
| **Completado** | Módulo terminado y puntuación grabada |
| **En curso** | Módulo iniciado pero aún no finalizado |
| **No iniciado** | Módulo aún no abierto |
| **Error** | El módulo anotó y la puntuación no alcanzó el umbral de aprobado del módulo |

## Cómo se calcula la puntuación total

La puntuación total es la suma de la contribución ponderada de cada módulo puntuado:

(Puntuación conseguida ÷ Puntuación máxima) × Peso % = Contribución del módulo

La columna **Contribución** del libro de calificaciones muestra la contribución de cada módulo a su agregado actual. Los módulos marcados con **Sin grosor** se excluyen de este cálculo.

La escala de puntuación no tiene que ser la misma en todos los módulos. Un módulo obtuvo una puntuación de 100 y un módulo obtuvo una puntuación de 10, ambos contribuyen correctamente. La fórmula normaliza cada uno de ellos antes de aplicar el peso.
