---
description: Establezca una ventana de tiempo durante la cual los alumnos puedan iniciar un módulo.
jcr-language: en_us
title: Control de tiempo de acceso al módulo
contentowner: mmanuel
source-git-commit: 6423fd5c0853705a28c6c67b6936d93e68cbca20
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 1%

---

# Control de tiempo de acceso al módulo

## Información general

La mejora permite a los autores y administradores de Adobe Learning Manager definir una ventana de tiempo durante la cual los alumnos pueden iniciar un módulo. Fuera de la ventana de inicio/finalización configurada, el módulo permanece visible en la estructura del curso, pero los alumnos no pueden iniciarlo.

Esta capacidad es fundamental para los usuarios que necesitan un control más estricto sobre cuándo está disponible determinado contenido o deben dejar de iniciarse, por ejemplo, en programas cronometrados, formación basada en cohortes o ejercicios urgentes.

## Novedades del sector

Los autores ahora pueden configurar, en el nivel de módulo de un curso, una fecha/hora de inicio y una fecha/hora de finalización que determine cuándo se permite a los alumnos iniciar ese módulo. En esta ventana, el módulo se comporta de la forma habitual; antes de la hora de inicio o después de la hora de finalización, el alumno ve el módulo en el esquema del curso, pero no puede iniciarlo.
La configuración aparece en la interfaz de usuario de creación del curso como controles de programación adicionales para tipos de módulos específicos, como contenido con ritmo personalizado, pruebas o actividades. Los administradores pueden utilizar estos controles para crear módulos que se abran en fases o para evitar inicios tardíos en programas en los que se debe consumir contenido dentro de un período de tiempo definido.

## Principales ventajas

La principal ventaja es la capacidad de controlar cuándo se puede acceder a los módulos. Los equipos de formación pueden sincronizar la disponibilidad de los módulos con eventos reales, como los lanzamientos de nuevos productos, los plazos reglamentarios y los programas internos. Esto garantiza que los alumnos completen el contenido de los requisitos previos antes de poder acceder a los módulos posteriores.
Por ejemplo, la cohorte 1 puede acceder al módulo 2 solo en la semana 2, mientras que el módulo 3 permanecerá bloqueado hasta la semana 3, lo que elimina la necesidad de ocultar y mostrar manualmente el contenido o crear versiones de cursos independientes.
Esto mejora la experiencia del alumno: en lugar de módulos opuestos a los que se puede acceder técnicamente, pero que no deberían estar en ese momento (o que ya deberían estar completados), los alumnos ven una estructura de curso en la que los módulos que se les permite iniciar están claramente alineados con el programa previsto.

## Casos de uso

**Programa de habilitación basado en cohorte**: En este programa, cada semana se abre un nuevo módulo. El contenido de la Semana 1 está disponible inmediatamente, mientras que la Semana 2 está visible, pero no se puede iniciar hasta una fecha especificada. La semana 3 sigue el mismo proceso de control. Los alumnos pueden ver la ruta de aprendizaje completa, pero el sistema controla cuándo pueden empezar realmente cada paso.
**Formación sobre productos o campañas con plazos determinados**: los equipos de marketing o de productos pueden crear un módulo de formación al que solo se debe acceder mientras una campaña está activa o cuando una versión específica de un producto aún está disponible. Esta ventana de inicio designada garantiza que los alumnos no inicien un módulo sobre una versión del producto interrumpida después de la hora de finalización especificada.
**Entornos de evaluación o examen**: las organizaciones pueden abrir un módulo (como una prueba) para una ventana corta y bien definida (por ejemplo, &quot;puede comenzar el examen en cualquier momento entre 9:00 y 12:00 en una fecha determinada&quot;). Los alumnos no pueden comenzar el examen fuera de esa ventana, lo que permite una programación equitativa en las zonas horarias y cohortes.

## Configurar tiempo de acceso al módulo

1. Inicie sesión en Adobe Learning Manager como autor.
2. Vaya a la sección **Aprendizaje** > **Cursos**. ALM muestra una lista de cursos.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time1.png)
3. Seleccione el curso para el que desea establecer la restricción.
4. Seleccione **Instancias**. ALM muestra una lista de instancias.
5. Seleccione **Módulos** en la sección de instancias para la que desee establecer el límite de acceso. Aparece el botón **Editar**.![texto alternativo](/help/migrated/administrators/feature-summary/assets/module-access-time2.png) ![texto alternativo](/help/migrated/administrators/feature-summary/assets/module-access-time3.png)
6. Seleccione **Editar**. Las secciones relevantes relacionadas con el módulo se abren en la parte inferior de la página.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time4.png)
7. Para cada sección, seleccione una fecha de inicio, una hora de inicio, una fecha final y una hora final.
8. Seleccione **Guardar**. ALM muestra un mensaje que indica: &quot;La asignación se guardó correctamente&quot;.










