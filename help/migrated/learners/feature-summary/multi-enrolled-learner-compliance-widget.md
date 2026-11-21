---
description: Obtenga información sobre cómo el widget de cumplimiento del alumno enumera cada instancia de inscripción de un curso de inscripción múltiple con fecha límite y cómo la API lo admite
jcr-language: en_us
title: Los cursos de varios inscritos aparecerán en el widget de cumplimiento del alumno
exl-id: 6484c815-ecae-4a75-ba10-ef42e4ff50a6
source-git-commit: d762bc8f199b703169878acbb52d0d7e3e0d6973
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%
---

# Cursos de varios inscritos en el widget de cumplimiento del alumno

En Adobe Learning Manager, un alumno puede inscribirse en más de una instancia del mismo curso. El widget de cumplimiento del alumno ahora muestra todas las instancias inscritas que tienen una fecha límite, de modo que los alumnos ven cada fecha de vencimiento en lugar de solo la instancia principal.

## ¿Qué cambios hay en los cursos de inscripción múltiple?

Antes de este cambio, el widget de cumplimiento solo mostraba la instancia principal de un curso con varios alumnos inscritos. Un alumno que se había inscrito en varias instancias no podía ver las fechas límite de los demás en el widget.

Ahora, el widget Cumplimiento muestra todas las instancias que cumplen todas estas condiciones:

* El alumno se inscribe en la instancia.
* La instancia tiene un plazo.
* El alumno no ha completado la instancia.

Cada entrada muestra el nombre de la instancia, de modo que los alumnos pueden diferenciar instancias del mismo curso. Cuando un alumno selecciona una entrada, Adobe Learning Manager abre esa instancia directamente.

Por ejemplo, un alumno completa un curso de formación inicial. Un administrador inscribe posteriormente al alumno en las ediciones de septiembre, octubre y noviembre del mismo curso, cada una de ellas con una fecha límite. El widget de cumplimiento enumera las tres ediciones.

El widget cuenta cada instancia por separado en cada categoría de conformidad: **Vencido**, **Próximo plazo en los próximos 30 días** y **En pista**.

## Instancias que aparecen en el widget de cumplimiento

En la siguiente tabla se describe cómo trata el widget cada situación de inscripción.

| Situación de inscripción | Aparece en el widget | Notas |
|--------------------------------------------------|-----------------------------------|---------------------------------------|
| Inscrito, la instancia tiene una fecha límite, no completada | Sí | Se muestra con el nombre de instancia |
| Inscrito, la instancia no tiene fecha límite | No | Solo aparecen instancias con una fecha límite |
| Instancia completada | No | No se muestra una instancia completada |
| Completado en todas las instancias inscritas | No | El curso ya no aparece |
| Una instancia con fecha límite y otra sin fecha | Solo la instancia con una fecha límite |                                       |
| Solo una instancia inscrita | Sí | El widget muestra esa instancia |

Consulte [Compatibilidad con API para instancias de inscripción múltiple en la aplicación del alumno](/help/migrated/api-changes-dec-2026.md#multi-enrolled-compliance-widget) para obtener información sobre la API.
