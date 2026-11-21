---
description: Aprenda a activar la inscripción múltiple para cursos adaptables, administrar los límites de puestos y las listas de espera, y comprender las reglas de inscripción en las rutas de aprendizaje
jcr-language: en_us
title: Inscripción múltiple para cursos adaptables
exl-id: e2a52964-fe9d-4a71-a020-68201f75f9f0
hide: true
source-git-commit: e056f1a655efd7c999856e2b54b28e676e67afc6
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Inscripción múltiple para cursos adaptables

## Información general

La inscripción múltiple permite a un alumno inscribirse en más de una instancia del mismo curso al mismo tiempo. En Adobe Learning Manager, ahora puede activar la inscripción múltiple para cursos adaptables.

## Acerca de la inscripción múltiple en un curso adaptable

Un curso adaptable muestra a cada alumno solo los módulos que coinciden con sus grupos de usuarios. Con la inscripción múltiple activada, un alumno puede realizar varias instancias de ese curso, como sesiones en diferentes meses.

Los cursos adaptables realizan el seguimiento de las listas de espera en el nivel de módulo, no en el nivel de instancia. Un alumno puede estar en curso en algunos módulos y en lista de espera en otros al mismo tiempo. Por ejemplo, un curso tiene dos instancias y cada instancia tiene un límite de puestos de una. El primer alumno se inscribe en ambas instancias y ocupa ambos puestos. Un segundo alumno que se inscribe en ambas instancias aparece en la lista de espera en ambas.

## Habilitar la inscripción múltiple para un curso adaptable

1. Inicie sesión en Adobe Learning Manager como autor.
2. En la barra de navegación izquierda, seleccione **Cursos**. Abra un curso adaptable o cree uno.
3. Añada los módulos. Para cada módulo de contenido, selecciona **Agregar reglas** para establecer los grupos de usuarios que pueden verlo y los grupos de usuarios para los que es obligatorio.
4. Seleccione **Guardar**. La opción de inscripción múltiple pasa a estar disponible.
5. Active el conmutador **Inscripción múltiple**.
6. Cree las instancias que necesite. Para las sesiones de clase y las sesiones de clase virtual, establezca los límites de puestos.
7. Seleccione **Publish**.

Los alumnos ahora pueden inscribirse en más de una instancia del curso.

## Comportamiento de límite de puestos y lista de espera

Los cursos adaptables imponen límites de puestos para cada sesión de clase o de clase virtual. Un alumno se inscribe inmediatamente y solo se muestra en lista de espera en las sesiones que están completas. El alumno puede iniciar el resto de módulos de inmediato.

| Condición | Resultado |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Todas las sesiones visibles tienen asientos disponibles | El alumno se inscribe con acceso completo a todos los módulos. |
| Una o más sesiones visibles están llenas | El alumno se ha inscrito y está en lista de espera solo en las sesiones completas. |
| Puede añadir una sesión obligatoria sin puestos a un curso con alumnos inscritos | El alumno está en lista de espera en la nueva sesión. El progreso y el acceso existentes no se ven afectados. |
| Un cambio de grupo de usuarios elimina una sesión de los módulos visibles del alumno | Adobe Learning Manager libera el puesto inmediatamente. |
| Un alumno cambia a otra instancia | Los módulos completados permanecen completados. Los puestos se utilizan solo para los módulos visibles que el alumno no ha completado. |

## Reglas de inscripción y finalización de rutas de aprendizaje adaptables

Los autores ahora pueden añadir cursos adaptables a rutas de aprendizaje adaptables en Adobe Learning Manager. La inscripción, la lista de espera y la finalización siguen reglas que combinan la configuración de la sección y la configuración del curso que configuran los autores.

### Cómo una ruta de aprendizaje adaptable evalúa a un alumno

Adobe Learning Manager evalúa la visibilidad en el nivel de sección y en el nivel de curso. La regla de sección decide si un alumno ve una sección y los cursos adaptables que contiene. Las reglas del módulo de cada curso adaptable deciden si el alumno está inscrito en el curso.

Los alumnos se inscribirán automáticamente siempre que haya un cambio de UG con respecto al curso adaptable en el programa de aprendizaje adaptable. Por lo mismo, los alumnos recibirán notificaciones de inscripción automática y correos electrónicos.

### Reglas de evaluación de inscripción

Cuando inscribe a un alumno en una ruta de aprendizaje adaptable, Adobe Learning Manager comprueba la ruta en este orden:

| Orden | Verificar | Resultado |
|-----------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Visibilidad de la sección | Adobe Learning Manager comprueba la inscripción de un curso solo si su sección está visible para el alumno. |
| 2 | Requisitos del curso | Si el curso no tiene ningún módulo obligatorio para el alumno, este no se inscribe en el curso. El curso no cuenta para la finalización de la ruta de aprendizaje. |
| 3 | Secciones sin curso elegible | Si una sección solo contiene cursos adaptables y el alumno no puede optar a ninguno, Adobe Learning Manager omite la sección. |
| 4 | Inscripción de ruta de aprendizaje | Si ninguna de las secciones obligatorias se aplica al alumno, este no se inscribe en la ruta de aprendizaje. |

Si el alumno ya está inscrito en una instancia del curso que pertenece a la instancia de la ruta de aprendizaje, Adobe Learning Manager utiliza esa inscripción.

Después de la inscripción, se aplican las siguientes reglas:

* Un alumno que omitió un curso inicialmente debido a la visibilidad puede inscribirse automáticamente si el curso adaptable es visible debido a los cambios de visibilidad/regla obligatoria que se producen más adelante.
* Un cambio de grupo de usuarios o un cambio de curso puede dar de baja a un alumno de un curso adaptable. Si no queda contenido obligatorio en la ruta, el alumno se da de baja de la ruta.
* Para los cambios de sección, el alumno no recibirá ninguna notificación de inscripción automática ni ningún correo electrónico. Simplemente al volver a cargar la página, el alumno puede ver los cambios.

### Comportamiento de lista de espera en rutas de aprendizaje adaptables

Las listas de espera funcionan en el nivel de sesión, no en el nivel de instancia. Esto también se aplica a los cursos adaptables en rutas de aprendizaje.

| Escenario | Comportamiento |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Ningún curso adaptable de la ruta tiene un módulo de clase o de clase virtual | No hay lista de espera. |
| Un curso adaptable tiene un módulo de clase o de clase virtual y no se selecciona ninguna instancia | El valor predeterminado del curso es **Ninguna instancia**. El alumno puede inscribirse en cualquier instancia y está en lista de espera solo en las sesiones que están completas. |
| Se selecciona una instancia antes de la inscripción | El alumno se inscribe en esa instancia y solo se muestra en lista de espera en las sesiones que están completas. |

Para administrar alumnos en lista de espera, abra el curso adaptable y seleccione la pestaña **Alumnos** > **Lista de espera**. Para un curso adaptable en una ruta de aprendizaje flexible y una ruta de aprendizaje adaptable, los alumnos en lista de espera solo aparecen en la pestaña **Lista de espera** del curso y no en la ruta de aprendizaje.

### Actualice el comportamiento de finalización y reversión

Adobe Learning Manager no revoca la finalización automáticamente cuando cambian los grupos de usuarios o las reglas. Un alumno completado permanece completado hasta que se actualiza el proceso de finalización.

* Ejecute **Actualizar finalización** en la ruta de aprendizaje. Un curso adaptable no se puede actualizar por sí solo para los alumnos que lo siguen.

* En primer lugar, cada curso adaptable se recalcula en función de los módulos obligatorios actuales del alumno. A continuación, la ruta de aprendizaje se recalcula en función de las secciones obligatorias actuales y los estados del curso actualizado.

* Si el curso o la ruta ya no se completan, el estado del alumno cambia a En curso. La finalización original permanece en la transcripción del alumno como un registro histórico.

* Una restauración de finalización busca los cursos adaptables cuyos módulos han cambiado debido a un cambio de grupo de usuarios o una nueva publicación. Recalcula esos cursos y, a continuación, la ruta de aprendizaje. El estado del trabajo muestra **Correcto** cuando finaliza la restauración.

Se realiza un seguimiento de las listas de espera en el nivel de módulo. Se puede poner en lista de espera a un alumno en una sesión completa en más de una instancia. Por ejemplo, un curso tiene dos instancias con un límite de puestos de una cada una. El primer alumno se inscribe en ambas instancias y ocupa ambos puestos. Aparece un segundo alumno que se inscribe en ambas instancias en la ficha **Lista de espera** de cada instancia.

### Asignar puestos a alumnos en lista de espera

Cuando un alumno se da de baja, un autor aumenta un límite de puestos o un alumno cambia de instancias, Adobe Learning Manager borra la lista de espera en el orden de fecha de inscripción. También puede asignar puestos manualmente.

1. Abra el curso adaptable.
2. Seleccione la pestaña **Alumnos** > **Lista de espera**.
3. Seleccione la casilla de verificación junto a cada alumno para el que desee asignar puestos.
4. Seleccione **Asignar puestos**.

Adobe Learning Manager borra a la vez cada alumno seleccionado de la lista de espera en todas las sesiones en lista de espera, no solo en la sesión que está visualizando. El sistema supone que ha organizado la licencia para el alumno.
