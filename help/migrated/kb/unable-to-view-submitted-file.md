---
jcr-language: en_us
title: No se pueden ver los envíos de archivos en Adobe Learning Manager
description: Los instructores no pueden ver los archivos que los alumnos han cargado en el módulo de actividad de envío.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 50%

---



# No se pueden ver los envíos de archivos en Adobe Learning Manager

## El problema

Un instructor no puede ver los envíos de archivos que ha cargado un alumno.

## Descripción

Los instructores no pueden ver los archivos que los alumnos han cargado en el **Módulo de actividad de envío**.

Por ejemplo, un alumno se ha inscrito en una instancia denominada **Instancia de prueba** de un curso, como se muestra a continuación:

![](assets/test-instance.png)

*Ver instancia*

A continuación, el alumno abre el curso y carga un archivo en el módulo Actividad.

Al intentar aprobar un envío, el instructor no puede realizar esta acción.

![](assets/activity.png)

*Cargar un archivo en el módulo de actividad*

## Causa

Si no hay ningún instructor en la instancia del curso en el que está inscrito el alumno, se produce el problema.

## Resolución

Para comprobar si se ha añadido un instructor a la instancia del curso, siga los pasos que se indican a continuación:

1. Vaya a la configuración del curso.
1. En la **Gestionar** , haga clic en **[!UICONTROL Instancias].**
1. En la instancia en la que el alumno está inscrito, haga clic en **[!UICONTROL Sesiones]**.

   ![](assets/check-instructor.png)

   *Seleccione Sesiones en la instancia*

   No hay ningún instructor asignado a esta sesión.

1. Haga clic en **[!UICONTROL Editar]**. Añada el instructor que aprueba el envío del archivo.

   ![](assets/assign-instructor.png)

   *Añadir el instructor*
1. Guarde los cambios.

