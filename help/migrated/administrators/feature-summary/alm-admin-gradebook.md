---
description: Todo sobre cómo activar el Libro de calificaciones y hacerlo visible para autores y alumnos
jcr-language: en_us
title: Libro de calificaciones para administradores
source-git-commit: 971576b95ab0f75b9d28a7f3d1d62440927925f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Habilitar la visibilidad del libro de calificaciones para su cuenta

## Información general

Para que los autores puedan mostrar el libro de calificaciones a los alumnos de un curso, un administrador debe habilitar la configuración de visibilidad del libro de calificaciones en el nivel de cuenta. Esta configuración actúa como un conmutador maestro: cuando está desactivada, los alumnos no pueden ver el libro de calificaciones en ningún curso, independientemente de cómo estén configurados los cursos individuales.

## Qué controla esta configuración

La configuración de **visibilidad del libro de calificaciones** en **Configuración** > **General** determina si los autores pueden exponer el libro de calificaciones a los alumnos en el nivel del curso.

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
