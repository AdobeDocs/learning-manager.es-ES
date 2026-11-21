---
title: Crear una sesión de Live Hub
description: Aprenda a crear un curso de Live Hub, añadir instancias de cursos, asignar instructores con el buscador de instructores, inscribir alumnos y personalizar la marca de la sala.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 9d05ad4a059bd1fec6e64f050070dae336ba2d1b
workflow-type: tm+mt
source-wordcount: '1617'
ht-degree: 0%
---

# Crear una sesión de Live Hub

Use Live Hub para impartir formación en directo con instructor en un curso de Adobe Learning Manager. Puede combinar sesiones de Live Hub con contenido con ritmo personalizado para crear una experiencia de aprendizaje mixta.

Cuando añada un módulo de clase virtual a un curso, seleccione la herramienta de formación virtual que alojará la sesión en directo. Puedes elegir **Live Hub**, la solución integrada de formación virtual con tecnología de IA de Adobe, o usar un proveedor externo como **Adobe Connect**.

>[!NOTE]
>
> Live Hub aparece como una opción de Live Virtual Training Tool solo si el administrador lo ha activado en la configuración de Live Hub. Si no está habilitado, utilice en su lugar un proveedor externo como Adobe Connect. Vea [Habilitar Live Hub](../administrators/feature-summary/enable-live-hub.md) para obtener más información.

Al crear un curso de Live Hub, puede:

* Añada una o más sesiones de Live Hub a un curso.

* Seleccione Instructores manualmente o utilice las recomendaciones de instructores asistidos por IA.

* Configure el curso con una única instancia predeterminada o cree varias instancias para diferentes programaciones o audiencias.

En este artículo se explica cómo crear un curso de Live Hub, asignar instructores y configurar instancias del curso.

## Crear un curso de Live Hub

Se crea automáticamente una instancia predeterminada al añadir un módulo de clase virtual. Esto resulta útil cuando se desea distribuir una sesión única o una programación estándar para todos los alumnos.

Para crear un curso de Live Hub:

1. Inicie sesión en Adobe Learning Manager como autor.

1. Seleccione **Crear cursos**.

1. En la página **Catálogo de cursos**, seleccione **Agregar** y, a continuación, introduzca los siguientes detalles:

   1. Nombre del curso

   1. Breve descripción

   ![Agregar descripción del nombre del curso](assets/add-course-name-description.png)
   *Escriba el nombre del curso y una breve descripción antes de agregar módulos al curso.*

1. Seleccione **Contenido** > **Agregar módulos** en la sección **Módulos**. <br> Aparece la ventana emergente **Seleccionar tipo de módulo**.

1. Selecciona **Clase virtual** e introduce los detalles del curso, como el título, la descripción, la zona horaria, la fecha de inicio y finalización, y la hora de inicio y finalización.

1. Seleccione **Centro de actividades** en **Herramientas de formación virtual en vivo**.

   ![Seleccionar herramienta Centro activo](assets/select-live-hub-tool.png)
   *Seleccione Live Hub para habilitar las recomendaciones de instructores con tecnología de inteligencia artificial para la sesión.*

1. Añada instructores mediante una de las siguientes opciones:

   1. Escriba los nombres de los instructores en el campo **Instructores**.

   1. Seleccione **Buscar instructores usando IA** para ver los instructores recomendados por IA. Vea [Agregar instructores mediante el buscador de instructores](#add-instructors-using-instructor-finder) para obtener más información.

1. Seleccione **Agregar** > **Guardar**.

1. Seleccione las aptitudes requeridas en la sección **Aptitudes del curso**.

1. Seleccione **Nivel de aptitud** y, a continuación, revise o actualice **Créditos máximos**.

   ![Asignar nivel de aptitud del curso](assets/assign-course-skill-level.png)
   *Asigne una aptitud y un nivel de aptitud para definir los créditos que obtienen los alumnos al completar el curso.*

1. Seleccione **Guardar** > **Publish**. El curso se crea correctamente en Adobe Learning Manager.

## Crear una instancia de curso

Un administrador puede crear una o más instancias de un curso para ofrecerlo a diferentes audiencias, programaciones o ubicaciones. Cada instancia tiene sus propios detalles de la sesión, por lo que puede asignar diferentes instructores, recomendaciones del buscador de instructores y intervalos a cada instancia del mismo curso.

Para crear una instancia de curso:

1. Inicie sesión en Adobe Learning Manager como autor.

1. Abra el curso y, a continuación, seleccione **Instancias** en el panel izquierdo.

   Página ![Instancia predeterminada](assets/default-instance-page.png)
   *La instancia predeterminada se crea automáticamente al agregar un módulo de clase virtual.*

1. Seleccione **Agregar nueva instancia**.

1. Escriba el **Nombre de instancia**, la **Fecha de inicio** y la **Fecha límite de finalización**. Seleccione **Mostrar más opciones** para configurar opciones adicionales.

   ![Agregar nuevo formulario de instancia](assets/add-new-instance-form.png)
   *Especifique un nombre de instancia, una fecha de inicio y una fecha límite de finalización para crear una nueva instancia de curso.*

1. Seleccione **Guardar**. <br> La nueva instancia se agrega a la lista **Instancias**.

   ![Instancias Lista Nueva Instancia](assets/instances-list-new-instance.png)
   *La nueva instancia aparece junto a la instancia predeterminada en la lista Instancias.*

1. Seleccione el número en **Sesiones** para ver los **Detalles de la sesión**.

   Icono De Edición De Detalles De Sesión ![](assets/session-details-edit-icon.png)
   *Los detalles de la sesión muestran qué campos de tiempo, instructor y ubicación aún deben configurarse.*

1. Seleccione el icono de editar (lápiz) situado junto a los detalles de la sesión para abrir el panel de configuración de la sesión.

   ![Panel de configuración de sesión](assets/session-configuration-panel.png)
   *Configurar la programación, el instructor y la ubicación para una instancia de sesión específica.*

1. En el campo **Instructores**, escribe los nombres manualmente o selecciona **Buscar instructores usando IA** para instructores recomendados por IA. Vea [Agregar instructores mediante el buscador de instructores](#add-instructors-using-instructor-finder) para obtener más información.

1. Indique los detalles de **Ubicación** y, a continuación, seleccione **Guardar**. La sesión se actualiza con los detalles de intervalos, instructor y ubicación configurados.

## Añadir instructores mediante el buscador de instructores

En lugar de buscar y añadir instructores manualmente, usa **Instructor Finder** para recibir recomendaciones de instructores basadas en IA para la sesión. El buscador de instructores busca instructores en función de los detalles del curso y las aptitudes requeridas, al tiempo que tiene en cuenta el calendario de vacaciones de la organización, la disponibilidad del instructor y la utilización del instructor para sugerir a los instructores más adecuados. Vea [Agregar y administrar instructores](./instructor-management.md) para obtener más información.

>[!NOTE]
>
> El Buscador de instructores solo aparece si el administrador ha activado el Ayudante del Buscador de instructores en la configuración de Live Hub. Vea [Habilitar Live Hub](../administrators/feature-summary/enable-live-hub.md) para obtener más información.

Para añadir instructores mediante el buscador de instructores:

1. Vaya a la sección **Instructores** en el módulo **Clase virtual**.

1. Seleccione **Buscar instructores usando IA**. <br> El panel **AI Assistant** se abre en el lado derecho.

   ![Recommendations de instructor de panel del Ayudante de AI](assets/ai-assistant-panel-instructor-recommendations.png)
   *Use el panel Asistente de inteligencia artificial para obtener recomendaciones del instructor y de la franja horaria según los detalles de la sesión.*

1. Revise la lista de instructores recomendados.

1. Desplácese hasta el instructor que desee asignar y, a continuación, seleccione **Agregar**. <br> El instructor seleccionado se agrega al campo **Instructores** como una etiqueta.

## Crear un curso para sesiones grandes {#create-large-session}

Live Hub admite sesiones grandes de hasta 5000 asistentes. Al crear un curso con esta capacidad, Live Hub configura automáticamente la sala para un público grande y aplica las restricciones de funciones correspondientes.

Para crear una sesión grande:

1. Inicie sesión en ALM como **autor**.
1. Seleccione **Agregar** en la página **Catálogo de cursos**.
1. Introduzca el nombre y la descripción del curso.
1. Seleccione **Contenido** > **Agregar módulos** en la sección **Módulos**. Aparece la ventana emergente **Seleccionar tipo de módulo**.
1. Selecciona **Clase virtual** e introduce los detalles del curso, como el título, la descripción, la zona horaria, la fecha de inicio y finalización, y la hora de inicio y finalización.
1. Seleccione **Centro de actividades** en **Herramientas de formación virtual en vivo**.
1. Seleccione **Habilitar 5000 asistentes**. Si no activa esta opción, la sesión admite hasta 100 asistentes.

   ![Cuadro de diálogo de clase virtual con Live Hub seleccionado y la opción Habilitar capacidad de 5000 asistentes](assets/virtual-classroom-enable-5000-attendee-capacity.png "Cuadro de diálogo de clase virtual con Live Hub seleccionado y la opción Habilitar capacidad de 5000 asistentes")

1. Seleccione **Guardar** > **Publish**.

### Funciones disponibles en sesiones grandes

Cuando un instructor abre la sesión, la configuración de la sala muestra que se aplican restricciones de sesiones grandes.

| Función | Comportamiento en una sesión grande |
|---|---|
| **Asistentes** | Una sesión grande admite hasta 5000 asistentes. Una vez que la sesión alcanza este límite, los asistentes adicionales no pueden unirse. |
| **Cámaras** | Hasta 10 instructores pueden encender sus cámaras simultáneamente. Los alumnos no pueden encender sus cámaras. Si se alcanza el límite de la cámara, aparece un mensaje cuando otro instructor intenta encender la cámara.<p>Las solicitudes de cámara realizadas al mismo tiempo se procesan como un lote. Como resultado, el número de cámaras activas puede exceder el límite configurado. Sin embargo, la información sobre herramientas del botón de cámara sigue mostrando el límite configurado. |
| **Micrófonos** | Hasta 20 asistentes pueden activar el silencio de sus micrófonos simultáneamente. Si se alcanza el límite del micrófono, aparece un mensaje cuando otro asistente intenta reactivar el audio.<p>Las solicitudes de micrófono realizadas al mismo tiempo se procesan como un lote. Como resultado, el número de asistentes que no se silencian puede exceder temporalmente el límite configurado. |
| **Salas para grupos de trabajo** | El icono de la sala de grupo de trabajo permanece visible, pero los instructores no pueden iniciar las salas de grupo de trabajo. Aparece un mensaje cuando intentan iniciar uno. |
| **Uso compartido de pantalla y pizarra** | Solo los instructores pueden compartir sus pantallas y utilizar la pizarra. Los instructores no pueden proporcionar estos permisos a los alumnos. |
| **Chat privado** | Los alumnos pueden enviar mensajes privados a los instructores, pero no pueden enviar mensajes privados a otros alumnos. |
| **Indicador de escritura** | El indicador de escritura no aparece en sesiones grandes. |
| **Charla, reacciones, preguntas y manos levantadas** | El sistema procesa estas interacciones en lotes, por lo que pueden aparecer tras un breve retraso. Live Hub también agrupa las reacciones y muestra un número limitado a la vez. |
| **Historial de chat** | El sistema elimina automáticamente los mensajes de chat antiguos cuando el historial de chat se hace demasiado grande para mantener la estabilidad de la sesión. |
| **Encuestas, cuestionarios, grabación y asistencia** | Estas funciones funcionan de la misma manera que en las sesiones regulares. |
| **Características de IA** | <ul><li>El sistema detecta las preguntas en el chat y las muestra en el panel **Preguntas**, aunque pueden aparecer tras un breve retraso.</li><li>Las funciones de inteligencia artificial asociadas a las salas de grupo de trabajo no están disponibles porque las sesiones grandes no admiten salas de grupo de trabajo.</li><li>Otras funciones de inteligencia artificial funcionan del mismo modo que en las sesiones regulares.</li></ul> |

>[!NOTE]
>
>Sin la opción **Habilitar capacidad de 5000 asistentes**, una sesión normal admite hasta 1100 asistentes, 50 cámaras y 20 participantes sin silenciar.

## Inscribir alumnos en el curso

Los alumnos pueden inscribirse en un curso de Live Hub de las dos formas siguientes:

1. Un **administrador** inscribe alumnos en el curso según los requisitos de la organización. Vea [Crear instancias de curso y rutas de aprendizaje](https://experienceleague.adobe.com/es/docs/learning-manager/using/admin/courses) para obtener más información.

1. Los alumnos pueden inscribirse directamente en el curso desde la página **Catálogo**. Si el curso está configurado para la inscripción automática, los alumnos se inscriben inmediatamente y pueden acceder al curso desde **My Learnings**. Vea [Mis aprendizajes](https://experienceleague.adobe.com/es/docs/learning-manager/using/learner/courses) para obtener más información.

Después de inscribirse, los alumnos se añaden al curso y reciben una notificación en su cuenta de Adobe Learning Manager. Según la configuración de notificaciones por correo electrónico de la cuenta, los alumnos también pueden recibir una invitación para unirse al curso por correo electrónico.

## Personalizar la marca de la sala Live Hub

Los administradores pueden personalizar el aspecto de las salas de Live Hub para adaptarlo a la marca de su organización. Usa la configuración de **Temas** en Adobe Learning Manager para aplicar colores de marca, logotipos y estilos visuales en las sesiones de Live Hub.

La construcción de marca personalizada ayuda a crear una experiencia de aprendizaje coherente y garantiza que las sesiones de formación en vivo reflejen la identidad de su organización.

Para obtener más información sobre la configuración de temas, consulte el artículo [Temas de color](../administrators/feature-summary/themes.md#color-themes).
