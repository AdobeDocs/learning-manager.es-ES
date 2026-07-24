---
description: Todo sobre el Libro de calificaciones desde la perspectiva del alumno
jcr-language: en_us
title: Libro de calificaciones para alumnos
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '1391'
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
| **Revisión pendiente** | Módulo completado pero a la espera de una puntuación de un instructor o administrador |
| **Sin grosor** | El tipo de módulo no admite la puntuación (PDF, vídeo y similares); no contribuye al agregado |

## Cómo se calcula la puntuación total

La puntuación total es la suma de la contribución ponderada de cada módulo puntuado:

(Puntuación conseguida ÷ Puntuación máxima) × Peso % = Contribución del módulo

La columna **Contribución** del libro de calificaciones muestra la contribución de cada módulo a su agregado actual. Los módulos marcados con **Sin grosor** se excluyen de este cálculo.

La escala de puntuación no tiene que ser la misma en todos los módulos. Un módulo obtuvo una puntuación de 100 y un módulo obtuvo una puntuación de 10, ambos contribuyen correctamente. La fórmula normaliza cada uno de ellos antes de aplicar el peso.

## Ver e informar sobre las puntuaciones del libro de calificaciones

Los administradores de Adobe Learning Manager pueden ver las puntuaciones ponderadas del libro de calificaciones de todos los alumnos inscritos en un curso, obtener detalles del rendimiento individual del alumno por módulo, descargar una transcripción del alumno filtrada y realizar un seguimiento de los cambios de configuración del libro de calificaciones en el informe de seguimiento de auditoría de contenido.

## Ver el libro de calificaciones de un curso

Cuando el libro de calificaciones está habilitado para un curso, aparece una nueva sección **Comentarios de L2 - Libro de calificaciones** en la barra de navegación izquierda en **Informes** al abrir el curso.

* Inicie sesión en Adobe Learning Manager como administrador.
* En la barra de navegación izquierda, seleccione **Cursos** y abra el curso que desea revisar.
* En la navegación del curso, en **Informes**, seleccione **Comentarios de L2 - Libro de calificaciones**. Se abre la página **Libro de calificaciones de comentarios activos**.

![](assets/image_0013.png)

Se muestra:

1. Los criterios de aprobación del curso (módulos mínimos requeridos y puntuación mínima agregada)
2. Una fila de filtro para ver a los alumnos por grado: **Aprobado**, **Error** o **Finalización pendiente**
3. La fórmula de puntuación agregada: Puntuación agregada = \ (Puntuación lograda ÷ Puntuación máxima) × Ponderación, para cada módulo
4. Una lista de alumnos que muestra la **puntuación agregada** de cada alumno y su puntuación para cada módulo puntuable
5. Menú desplegable de instancias para cambiar entre instancias de cursos cuando un curso tiene varias instancias

Los alumnos que aún no han intentado ningún módulo puntuado muestran guiones en las columnas de puntuación. Los módulos que no admiten puntuación, PDF, vídeo, audio y similares no aparecen como columnas de puntuación.

## Ver las puntuaciones de un alumno individual

En el **Libro de calificaciones de comentarios activos**, selecciona el nombre de un alumno.

![](assets/image_0014.png)

La vista individual del alumno muestra:

1. El nombre, el correo electrónico y el estado del alumno (**Finalización pendiente**, **Aprobado** o **Error**)
2. La puntuación agregada y cuántos módulos necesarios ha completado el alumno.
3. Una tabla de módulos que muestra: nombre del módulo, tipo, si es necesario, estado, ponderación, puntuación obtenida y contribución al agregado

La tabla de módulos incluye todos los módulos puntuables y no puntuables. Los módulos puntuables muestran su puntuación y contribución. Los módulos no puntuables muestran guiones en las columnas Puntuación y Contribución.

## Módulos de partitura

El comportamiento de puntuación para administradores e instructores no cambia con respecto al flujo de trabajo actual:

* **Los módulos de prueba SCORM, AICC, xAPI y nativos** se puntúan automáticamente cuando el contenido subyacente informa de una puntuación.
* Las **sesiones de clase, las sesiones de clase virtual y los módulos de actividad** las califican instructores o administradores de la página **Asistencia y puntuación**.

## Descargar la transcripción del alumno de un curso

Puede descargar una transcripción de alumno filtrada a este curso directamente desde la página del libro de calificaciones de una de las dos formas siguientes:

* En el **Libro de calificaciones de comentarios activos**, seleccione **Descargar transcripciones de alumnos** en la esquina superior derecha de la página.
* En la página principal del administrador, seleccione **Informes** y, a continuación, seleccione **Informes personalizados**. Seleccione **Transcripciones de alumnos** en la lista de informes disponibles.

Consulte Informes de cambios en la versión para obtener más información.

## Eventos de seguimiento de auditoría de contenido

El seguimiento de auditoría de contenido captura dos eventos de configuración específicos del libro de calificaciones:

| **Evento** | **Cuando aparece** |
|-----------|---------------------|
| **Libro de calificaciones actualizado** | Cuando un autor habilita o deshabilita el libro de calificaciones de un curso |
| **Peso del módulo actualizado** | Cuando un autor cambia el porcentaje de grosor de un módulo |

Consulte Informes de cambios en la versión para obtener más información.

Utilice estas entradas para realizar un seguimiento de quién ha cambiado la configuración del libro de calificaciones y cuándo, especialmente en entornos en los que varios autores colaboran en el mismo curso.

## Resolución de problemas

**La sección Comentarios de L2 - Libro de calificaciones no aparece en la navegación del curso**

El autor del curso debe habilitar el libro de calificaciones al crear el curso. Confirme que el autor ha habilitado el libro de calificaciones para la creación de cursos. Si el curso se creó antes de que el libro de calificaciones estuviera disponible, no se puede agregar retroactivamente. Se requiere una nueva versión del curso.

**La puntuación total de un alumno es 0 a pesar de los módulos completados**

Confirme que el curso tiene al menos un módulo puntuable con un valor de grosor asignado. Si todos los módulos que ha completado el alumno no son puntuables (PDF, vídeo, audio), no se calcula la puntuación total. Además, confirme que los módulos puntuados aún no se encuentran en el estado **Revisión pendiente**. Los módulos sin graduar se excluyen del agregado hasta que un instructor introduce una puntuación.

**Falta la columna Ponderación en la transcripción del alumno descargada**

Esta columna sólo aparece cuando el libro de calificaciones está activado y al menos un módulo tiene guardado un valor de grosor. Confirme que el autor activó el libro de calificaciones y guardó los valores de grosor en un total del 100 %.

**Un alumno ha completado todos los módulos necesarios, pero muestra Finalización pendiente**

Es posible que uno o más módulos aún estén esperando una puntuación de un instructor o administrador (**Estado de revisión pendiente**). El curso no se puede completar hasta que todos los módulos necesarios tengan una finalización y una puntuación registradas. Introduzca la puntuación pendiente de **Asistencia y Puntuación** para borrar el estado pendiente.
