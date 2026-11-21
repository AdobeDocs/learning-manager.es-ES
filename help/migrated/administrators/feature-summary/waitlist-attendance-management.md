---
jcr-language: en_us
title: Gestión de la lista de espera y la asistencia
description: Los administradores pueden gestionar la lista de espera y la asistencia a los cursos de los alumnos.
contentowner: manochan
exl-id: 257ed196-d6a7-4d6c-bd90-33d658f6ba55
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 38%
---
# Gestión de la lista de espera y la asistencia

Los administradores pueden gestionar la lista de espera y la asistencia a los cursos de los alumnos.

## Gestión de la lista de espera {#waitlistmanagement}

Los alumnos se ponen en lista de espera para un curso en clase cuando las plazas son limitadas, en función del orden de inscripción. Cuando se rellenan todos los puestos reservados para un grupo de usuarios, los miembros adicionales de ese grupo se colocan en la lista de espera del grupo. Los alumnos que no pertenecen a los grupos de usuarios se colocan en **Abrir lista de espera**.

Los administradores pueden revisar la lista de espera y administrar los alumnos en lista de espera. Adobe Learning Manager también puede ascender a alumnos en lista de espera automáticamente cuando haya un puesto disponible.

Para administrar alumnos en lista de espera:

1. Seleccione **Cursos** en el panel izquierdo.
1. Seleccione el nombre de un curso de clase de los cursos disponibles.

   Aparece una nueva página con información detallada sobre el curso.

1. Seleccione **Lista de espera** en el panel izquierdo de la página de detalles del curso.

   Se abre la página de lista de espera con el siguiente **estado de lista de espera**:

   * **Límite de puestos:** Número total de puestos disponibles para la sesión.
   * **Rellenado:** Número de puestos ocupados actualmente.
   * **En lista de espera:** Número de alumnos pendientes de inscripción.

1. Seleccione las siguientes pestañas de la página **Lista de espera**:

   1. **Lista de espera por grupo de usuarios**: Muestra los alumnos en lista de espera de cada grupo de usuarios.

   >[!NOTE]
   >
   >Esta pestaña solo aparece si la configuración **Inscripción de grupo** está habilitada.

   1. **Abrir lista de espera**: Muestra los alumnos en lista de espera que no están reservados para ningún grupo de usuarios.

   ![Página de lista de espera con la ficha Lista de espera por grupo de usuarios](assets/waitlist-by-user-group-tab.png "Página de lista de espera con la ficha Lista de espera por grupo de usuarios")

1. Junto a un alumno, seleccione una de las siguientes acciones:

   | **Acción** | **Descripción** |
   |---|---|
   | **Confirmar** | Inscribe al alumno en lista de espera en la sesión y lo elimina de la lista de espera. |
   | **Dar de baja** | Elimina al alumno de la lista de espera y actualiza las posiciones de los alumnos restantes de la lista de espera. |

## Gestión de la asistencia {#attendancemanagement}

Esta función es aplicable solo a los cursos de clase y clase virtual. Puede registrar la asistencia siguiendo estos pasos:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador.
1. En la lista de cursos disponibles, haga clic en el nombre del curso de cualquier módulo o curso de clase que quiera. Aparece una nueva página con información detallada sobre el curso.
1. Haga clic en la ficha Asistencia, seleccione los alumnos y haga clic en Guardar para marcar la asistencia.

>[!NOTE]
>
>Si hay varios módulos en un curso y el alumno ha completado solo uno de ellos, puede seleccionar un solo módulo y hacer clic en Guardar. Si este completa todos los módulos de un curso, puede hacer clic en la opción Seleccionar todo y después en Guardar.

La asistencia a la sesión de clase virtual basada en Adobe Connect se marca automáticamente entre 2 y 3 horas después de la sesión. La finalización del curso de clase virtual del alumno se marca solo después de que se haya marcado la asistencia.
