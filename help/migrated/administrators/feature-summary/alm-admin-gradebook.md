---
description: Todo sobre cómo activar el Libro de calificaciones y hacerlo visible para autores y alumnos
jcr-language: en_us
title: Libro de calificaciones para administradores
source-git-commit: 588cb5209168b605405a4b3d6949006344b5468b
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 0%

---


# Habilitar la visibilidad del libro de calificaciones para su cuenta

## Información general

Para que los autores puedan mostrar el libro de calificaciones a los alumnos de un curso, un administrador debe habilitar la configuración de visibilidad del libro de calificaciones en el nivel de cuenta. Esta configuración actúa como un conmutador maestro: cuando está desactivada, los alumnos no pueden ver el libro de calificaciones en ningún curso, independientemente de cómo estén configurados los cursos individuales.

## Qué controla esta configuración

La configuración de **visibilidad del libro de calificaciones** en **Configuración** > **General** determina si los autores pueden exponer el libro de calificaciones a los alumnos en el nivel del curso.

Para obtener más información, vea [Visibilidad del libro de calificaciones](/help/migrated/administrators/feature-summary/settings/basic-settings.md#gradebookvisibility).

| Configuración del estado | Efecto |
| --- | --- |
| Activado | Los autores pueden controlar la visibilidad del libro de calificaciones por curso mediante la opción **Mostrar libro de calificaciones a los alumnos** en el editor del curso. Los alumnos ven la ficha **Libro de calificaciones** en los cursos en los que el autor lo ha habilitado. |
| Desactivado | Los alumnos no pueden ver el libro de calificaciones en ningún curso. Si está desactivada, la configuración del curso no tendrá la opción de mostrar el libro de calificaciones a los alumnos. |

Esto significa que la configuración de nivel de cuenta y la configuración de nivel de curso funcionan juntas. Ambos deben estar activados para que un alumno pueda ver el libro de calificaciones.

## Habilitar la visibilidad del libro de calificaciones

1. Inicie sesión en Adobe Learning Manager como administrador.
2. En la barra de navegación izquierda, seleccione **Configuración**.
3. Seleccione **General**.
4. Desplácese hasta la sección **Visibilidad del libro de calificaciones**.
5. Seleccione la casilla de verificación **Habilitar vista Libro de calificaciones para alumnos**.

   ![](assets/gradebook-admin-1.png)

Los autores ahora pueden configurar la visibilidad del libro de calificaciones por curso.

## Incidencia en los flujos de trabajo de autor

Cuando esta configuración de nivel de cuenta está habilitada, el conmutador **Mostrar libro de calificaciones a los alumnos** en el editor del curso pasa a estar disponible. Los autores utilizan este botón de alternancia para decidir, por curso, si los alumnos pueden ver la ficha **Libro de calificaciones**.

Cuando esta configuración de nivel de cuenta está deshabilitada:

* El botón de alternancia **Mostrar libro de calificaciones a los alumnos** del editor del curso puede seguir apareciendo, pero se invalida cualquier configuración del nivel del curso. Los alumnos no verán el libro de calificaciones.
* Las puntuaciones del libro de calificaciones y los cálculos ponderados siguen ejecutándose en segundo plano a efectos de informes del administrador.
* Los administradores y los administradores personalizados pueden seguir descargando transcripciones de alumnos con datos del libro de calificaciones.

>[!NOTE]
>
>Al deshabilitar esta configuración en el nivel de cuenta, no se elimina ninguna configuración o puntuación del libro de calificaciones. Si vuelve a activarla, se restauran inmediatamente todas las configuraciones del libro de calificaciones de nivel de curso configuradas anteriormente.

## Cómo interactúan los dos ajustes

| Configuración de nivel de cuenta | Configuración del nivel del curso | Lo que ve el alumno |
| --- | --- | --- |
| Activado | Mostrar el libro de calificaciones a los alumnos: **El** | Ficha **Libro de calificaciones** visible en el reproductor del curso |
| Activado | Mostrar el libro de calificaciones a los alumnos: **Desactivado** | No hay ficha Libro de calificaciones; puntuaciones calculadas solo internamente |

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
