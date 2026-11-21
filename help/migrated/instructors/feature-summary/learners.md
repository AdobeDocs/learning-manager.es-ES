---
description: Lea este artículo para obtener información sobre cómo administrar a los asistentes, enviar correos electrónicos relacionados con el curso y recordatorios de las sesiones.
jcr-language: en_us
title: Administrar a los alumnos de la sesión
contentowner: shhivkum
exl-id: 2f4f8589-2350-4683-a141-809084d6309a
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 73a56c810d5222b6ab6f128db9661ff7fb6d2c93
workflow-type: tm+mt
source-wordcount: '3424'
ht-degree: 26%
---
# Administrar a los alumnos de la sesión

Lea este artículo para obtener información sobre cómo administrar a los asistentes, enviar correos electrónicos relacionados con el curso y recordatorios de las sesiones.

## Ver sesiones o módulos con revisiones pendientes {#pending}

Como instructor, puede ver las sesiones o los módulos que tienen revisiones pendientes.

En la página Sesiones/Módulos, se muestra la columna **Revisiones pendientes**; en ella, se indica la cantidad de revisiones pendientes de la sesión/actividad correspondiente.

## Administrar la lista de espera de la sesión {#managewaitlistforyoursession}

A medida que los alumnos se inscriben en el módulo, en la página Lista de espera puede ver el estado más actual de la inscripción y de la lista de espera.

1. En la aplicación del instructor, seleccione Sesiones futuras > Lista de espera en el panel de navegación izquierdo.

   Puede ver los valores del límite de puestos, la cantidad de puestos rellenados y de puestos libres. En una tabla figuran los alumnos que están en lista de espera. Si está en blanco, significa que no hay ninguna lista de espera.

   ![](assets/waitlist.png)
   *Ver alumnos en lista de espera*

1. En la tabla Lista de espera, seleccione a los alumnos que quiera confirmar.
1. Seleccione Acciones > Confirmar alumnos.

   Los alumnos que haya confirmado se incorporan a la lista de alumnos confirmados.

Los instructores tienen la capacidad de dar de baja de las sesiones a los alumnos. Esto también les da de baja de los correspondientes aprendizajes. Seleccione la ficha **[!UICONTROL Lista de espera]**. Con la casilla de verificación, seleccione los alumnos a los que dar de baja. Para cancelar la inscripción, seleccione **[!UICONTROL Acciones]** > **[!UICONTROL Dar de baja a los alumnos]**.

![](assets/unenroll-learners.png)
*Dar de baja a los alumnos*

### Informe de lista de espera

El nuevo **[!UICONTROL informe de lista de espera]** de Adobe Learning Manager permite a los instructores descargar la lista de alumnos en lista de espera para todas las instancias de un curso. Los instructores pueden acceder a este informe desde la sección **[!UICONTROL Lista de espera]** de la página **[!UICONTROL Descripción general de la sesión]**.

Siguiendo las columnas disponibles en el informe de lista de espera:

* Nombre del curso
* Nombre de instancia
* ID de instancia
* Estado de la instancia
* Nombre de usuario
* Correo electrónico
* ID exclusivo de usuario
* Fecha de inscripción (zona horaria UTC)
* Estado
* Número de lista de espera
* Límite de lista de espera
* Límite de puestos

Para descargar el informe desde la sección Instructor :

1. Inicie sesión como **[!UICONTROL Instructor]**.
2. Seleccione cualquier sesión de la página principal.
3. Seleccione la opción **[!UICONTROL Lista de espera]** en la página **[!UICONTROL Introducción a la sesión]**.
4. Selecciona **[!UICONTROL Acciones]** > **[!UICONTROL Informe de exportación]** para descargar el informe de **[!UICONTROL lista de espera]**.

## Marcar la asistencia de la sesión {#markattendanceforyoursession}

En la página Alumnos, puede ver la cantidad de alumnos confirmados que asisten a la sesión, sus nombres, el estado de asistencia y demás datos.

1. En el panel de navegación izquierdo, haga clic en Sesiones futuras > Alumnos.
1. En la lista de asistentes, seleccione a uno o más alumnos, y efectúe una de las acciones siguientes:

   * Para marcar la asistencia, haga clic en Acciones > Marcar asistencia. Cuando el estado se marca como Ha asistido, no se puede cambiar.
   * Para marcar la no asistencia, haga clic en Acciones > No ha asistido.
   * Para eliminar un alumno por cancelación u otros motivos, haga clic en Acciones > Eliminar alumnos.

   Un alumno no puede completar un módulo a menos que su estado de asistencia sea Ha asistido.

   ![](assets/markattendance.png)
   *Marcar la asistencia del alumno*

### Descargar códigos QR de inscripción y asistencia de alumnos

Los instructores pueden descargar códigos QR para sus sesiones asignadas, de modo que los alumnos puedan inscribirse en una instancia del curso y marcar la asistencia o la finalización mediante el análisis del código QR.

Esto permite a los instructores administrar la participación en la sesión de forma independiente, sin necesidad de asistencia del administrador.

Los siguientes pasos son adecuados para ambos:

* Sesiones de clase física
* Sesiones de clase en línea

Para una sesión de clase física, como instructor, debe generar el código QR correcto y pegarlo en la clase (o pasarlo) donde asisten los alumnos a la sesión para que puedan escanear el código QR y marcar su inscripción o asistencia, o ambas cosas, en función del código QR.

Para una sesión de clase en línea, como instructor, puede enviar el código QR generado por correo, un sistema de mensajería o cualquier otro medio para que los alumnos puedan escanear el código QR y marcar su inscripción o asistencia, o ambas cosas, en función del código QR.


#### Descargar códigos QR para una sesión

1. Inicie sesión en Adobe Learning Manager con la función **Instructor**.
2. Vaya al **tablero del instructor**.
3. Abra la **instancia del curso** correspondiente.
4. Seleccione la ficha **Sesiones**.
5. Elija una sesión que tenga asignada.
6. Seleccione **Código QR de sesión**.
   ![](assets/instructor-QR-code.png)

Puede descargar los siguientes códigos QR:

* **Código QR de inscripción**: permite a los alumnos inscribirse en la instancia del curso
* **Código QR de asistencia**: marca la asistencia a la sesión
* **Inscripción + código QR de asistencia**: inscribe a los alumnos y marca la asistencia en una sola digitalización

El código QR se descarga como PDF y puede compartirse digitalmente o mostrarse durante la sesión.

#### Qué sucede cuando los alumnos analizan el código QR

* Los alumnos escanean el código QR con un dispositivo móvil.
* Adobe Learning Manager valida la sesión y el alumno.
* Según el tipo de código QR:
  * Los alumnos se inscriben en la instancia del curso, o
  * Se registra la asistencia y la finalización del período de sesiones

Todas las actualizaciones se reflejan automáticamente en los registros, transcripciones e informes de los alumnos.

#### Notas

* Los códigos QR solo están disponibles para los instructores asignados a la sesión.
* Se seguirán aplicando las reglas de inscripción, asistencia y finalización configuradas para el curso y la sesión.
* El progreso del alumno y los flujos de trabajo de informes existentes no cambian.

#### Casos de uso

* Las organizaciones que ejecutan grandes volúmenes de sesiones in situ (por ejemplo, formación sobre productos para profesionales) pueden permitir a los instructores imprimir códigos QR específicos de la sesión que inscriben y marcan la asistencia con una digitalización.

* En la formación en venta, fabricación y atención sanitaria, en la que los alumnos suelen unirse a las sesiones directamente desde la planta o sin preinscripción, se puede colocar un código QR de &quot;Inscripción + Asistencia&quot; en la puerta. Esto permite a los alumnos realizar autoservicio de inscripción y asistencia a través de sus teléfonos.

* Los eventos de formación para socios o clientes permiten que el formador in situ se adapte fácilmente a los cambios en la sala, sesiones adicionales o asistentes adicionales sin necesidad de consultar al administrador para obtener nuevos códigos QR.

### Invitaciones de calendario {#calendarinvites}

* Cuando un alumno o instructor se inscribe en una sesión de clase o de clase virtual, Learning Manager envía una invitación de calendario (archivo ICS).
* La invitación de calendario incluye:

  * Fecha y hora de la sesión
  * Detalles de sesión
  * **Vínculo para unirse a la sesión directa** en la descripción del calendario

  ![](assets/calendar-invite-session.png)

Los participantes pueden abrir el evento del calendario y unirse a la sesión directamente desde su calendario.

#### Unirse a una sesión desde Gmail

1. Abra **Google Calendar**.
2. Seleccione el evento de sesión.
3. En los detalles del evento, haga clic en **vínculo de unión a sesión**.
4. La sesión se abre directamente en Adobe Learning Manager o en la herramienta de clase virtual configurada.

No es necesario abrir el correo electrónico original para acceder al vínculo de la sesión.

#### Unirse a una sesión de otros clientes del calendario

El vínculo de la sesión se incluye en el cuerpo del evento del calendario y se puede acceder a él desde:

* Microsoft Outlook
* Calendario de Apple
* Otras aplicaciones de calendario que admiten archivos ICS

#### Notas

* Learning Manager genera automáticamente las invitaciones de calendario.
* La información de zona horaria de la invitación del calendario se ajusta en función de la zona horaria seleccionada por el alumno.
* Esta mejora se aplica a las invitaciones de calendario recién generadas.
* Los administradores o instructores no necesitan ninguna configuración adicional.


## Marcar como correcto para los alumnos

Los instructores pueden marcar el estado de éxito de cada alumno como Aprobado o Suspenso directamente desde la página Alumnos. Esta función permite a los instructores registrar con precisión el resultado de las sesiones de clase o de clase virtual en función del rendimiento del alumno.

Para marcar el éxito para los alumnos:

1. Inicie sesión en Adobe Learning Manager como instructor.
2. Seleccione **[!UICONTROL Próximas sesiones]** en el panel de navegación izquierdo.
3. Seleccione **[!UICONTROL Alumnos]**.
4. Seleccione a los alumnos y, a continuación, seleccione **[!UICONTROL Acciones]**.
5. Seleccione cualquiera de las siguientes opciones para marcar el éxito de los alumnos seleccionados:

   * **[!UICONTROL Marcar como asistido y aprobar]**: Los alumnos marcados como Aprobados han completado correctamente el módulo.
   * **[!UICONTROL Marcar como asistido o suspenso]**: Los alumnos marcados como Suspenso han completado el módulo, pero no lo han aprobado.

   ![El menú desplegable Acciones resalta las opciones &quot;Marcar como asistido y aprobado&quot; y &quot;Marcar como asistido y suspenso&quot; para que los instructores establezcan el estado de éxito de cada alumno](/help/migrated/instructors/feature-summary/assets/mark-success-instructor.png)
   _Página de alumnos que muestra el menú Acciones con las opciones Marcar como asistido y Aprobado y Marcar como asistido y Suspenso resaltadas para registrar los resultados de los alumnos_

6. Seleccione **[!UICONTROL Sí]** en el mensaje de confirmación.

## Enviar correos electrónicos a alumnos {#sendemailstolearners}

Puede enviar correos electrónicos a uno o a todos los asistentes a la sesión. La función de envío de correo electrónico es muy útil para confirmar la asistencia de alumnos o para enviar comunicados relativos a la sesión. También se puede activar la función enviar correo electrónico a todos para enviar la asignación y material de la sesión, o comunicados a todos los alumnos.

Para enviar correos electrónicos a los alumnos, en la página Alumnos de la aplicación del instructor, efectúe una de las acciones siguientes:

* Para enviar correos electrónicos a determinados asistentes, seleccione el asistente y haga clic en Acciones > Enviar correo electrónico a los seleccionados.
* Para enviar correos electrónicos a fin de enviar material del curso o una asignación, haga clic en Acciones > Enviar correo electrónico a todos.

## Capturar respuestas de invitación

Los instructores pueden capturar las respuestas de invitación de los alumnos solo cuando el administrador de ACAP ha habilitado la opción **[!UICONTROL Invitar respuesta]**. Para habilitar esta característica, los administradores deben ponerse en contacto con el equipo de soporte técnico en [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com).

Una vez hecho esto, puede ver las respuestas de la invitación en la sección **[!UICONTROL Alumnos]**. Ve a cualquier sesión, selecciona **[!UICONTROL Alumnos]** y selecciona la respuesta a la invitación en el menú desplegable.

![](assets/invitation-status.png)

## Exportar lista de alumnos {#exportinglearnerslist}

Como instructor, puede marcar fácilmente la asistencia de todos sus alumnos exportando la lista de asistentes en formato pdf. Para exportar la lista de asistentes, vaya al alumno en el panel izquierdo. Haga clic en Acciones > Exportar lista de alumnos (PDF).

Tras confirmar la lista de asistentes a la sesión, puede exportarla como archivo PDF. Este PDF fácil de imprimir muestra a los alumnos en forma de tabla. Luego puede marcar la asistencia o proporcionar puntuaciones, así como crear notas para los alumnos, todo ello en el mismo PDF.

Observe el código QR en la esquina superior derecha de este PDF. Esta funcionalidad permite a los alumnos individuales escanear el código mediante la aplicación Learning Manager para dispositivos móviles para que marquen su asistencia.

![](assets/exportpdf.png)
*Analizar el código QR para marcar la asistencia*

## Aprobar o rechazar envíos {#approveorrejectsubmissions}

Si los alumnos han cargado documentos como asignaciones, informes o evaluaciones para la sesión, los documentos figuran en la página de envíos. Puede utilizar los materiales para calificar al alumno, así como para aprobar o rechazar el envío.

1. En el panel izquierdo, haga clic en Sesiones futuras o Sesiones pasadas, según el horario de la sesión.
1. Haga clic en el curso cuyos envíos desea ver.

   En el panel izquierdo, haga clic en Envíos.

1. Puede ver los envíos de los alumnos relativos a la sesión que ha seleccionado. Seleccione el envío que quiere aprobar o rechazar; a continuación, haga clic en Aprobar o Rechazar.

   Según la acción elegida, el estado del envío pasa a ser Aprobado o Rechazado.

## Configurar recordatorios de la sesión {#configureremindersforyoursession}

1. En el panel izquierdo, haga clic en Sesiones futuras.
1. Haga clic en el curso para el cual desea definir el recordatorio. En el panel izquierdo, haga clic en Recordatorios.
1. En el mosaico Seleccionar recordatorio, haga clic en Establecer recordatorio.

   ![](assets/setreminder.png)
   *Configurar recordatorios para tu sesión*

1. Realice lo siguiente:

   * En el cuadro de diálogo de configuración de recordatorios, defina la opción relativa al momento de enviar el recordatorio a los alumnos: antes del plazo, según el plazo o después del plazo.
   * En el campo de días antes del plazo, indique el número de días antes del plazo que desea enviar el recordatorio a los alumnos.
   * Establezca la periodicidad del recordatorio.

   ![](assets/remindersettings.png)
   *Ver configuración de recordatorio*

1. Elija una de las opciones siguientes:

   * Haga clic en la marca de verificación para guardar el recordatorio.
   * Haga clic en la cruz para cancelar el recordatorio.

   Un recordatorio automatizado del curso se envía a todos los alumnos en la fecha establecida en la configuración del recordatorio.

   Si ya ha definido recordatorios de las sesiones, aparecen en los mosaicos de recordatorios existentes. Asimismo, puede añadir recordatorios a los ya creados.

   Para eliminar un recordatorio, haga clic en él. En el menú emergente, haga clic en el icono de eliminar (icono de papelera) para suprimir el recordatorio.

## Creación y gestión de equipos en Adobe Learning Manager

Cree equipos manualmente de los alumnos en una instancia de curso y, a continuación, añada, mueva, elimine, cambie el nombre o elimine equipos hasta que se bloquee un equipo.

Como instructor, puede crear equipos para cada instancia de un curso que tenga un módulo de envío basado en el equipo. Cualquier instructor asignado a la instancia puede administrar sus equipos. Adobe Learning Manager también puede crear equipos automáticamente. Una vez formados los equipos, los alumnos pueden enviar su trabajo y usted puede evaluar los envíos del equipo.

### Abra la página de administración de equipos

1. En la aplicación del instructor, seleccione **Equipos** en el panel de navegación izquierdo. En la página, se muestran las instancias de curso basadas en equipo a las que se asignan los alumnos.

   Opción ![Equipos en el panel de navegación izquierdo](assets/Group-Team-submission-and-rubric-based-assessments-image17.png "Página de administración de equipos")

1. Para encontrar un curso, búsquelo u ordene la lista por la fecha de la última actualización.

1. Seleccione la instancia del curso. La página Instancia muestra los alumnos no asignados y los equipos.

### Crear equipos con una regla

1. En la página Instancia, seleccione los alumnos no asignados que se van a dividir en equipos.

1. Elija una regla. Seleccione **Acción** > **Formar un solo equipo** o **Formar varios equipos**.

   ![Menú Acción con reglas de formación de equipo](assets/Group-Team-submission-and-rubric-based-assessments-image18.png "Menú Acción")

1. Si selecciona **Formar varios equipos**, indique el número de alumnos de cada equipo. El valor debe ser 1 o superior. La página muestra cuántos equipos se crearán. Por ejemplo, con 94 alumnos y 2 alumnos por equipo, se crean 47 equipos. Si el número es mayor que el número de alumnos inscritos, aparece un mensaje de error. Introduce un número más pequeño.

   ![Número de alumnos por equipo y número resultante de equipos](assets/Group-Team-submission-and-rubric-based-assessments-image19.png "Alumnos por equipo")

   Si introduce un valor mayor que el número de alumnos inscritos, aparecerá un mensaje de error.

   ![Mensaje de error para un valor mayor que el número de alumnos inscritos](assets/Group-Team-submission-and-rubric-based-assessments-image20.png "Mensaje de error")

1. Seleccione **Crear equipos**. Los equipos aparecen en la pestaña **Equipos**.

   ![Pestaña Equipos con los equipos creados](assets/Group-Team-submission-and-rubric-based-assessments-image21.png "Equipos creados")

1. Confirme y guarde. Los equipos aparecen en la pestaña **Equipos**.

La regla solo se aplica a los alumnos no asignados que seleccione. Para reagrupar a todos, elimine primero los equipos existentes. Los alumnos vuelven a la lista sin asignar.

![Opción Eliminar para equipos existentes](assets/Group-Team-submission-and-rubric-based-assessments-image22.png "Eliminar equipos")

Después de seleccionar **Eliminar**, aparece el siguiente cuadro de diálogo de confirmación:

![Cuadro de diálogo de confirmación Eliminar equipos](assets/Group-Team-submission-and-rubric-based-assessments-image23.png "Confirmación de eliminación")

Seleccione **Eliminar equipos**. Todos los alumnos vuelven a la lista sin asignar.

### Crea un solo equipo

1. Seleccione los alumnos no asignados que desea incluir en el equipo.

1. Seleccione **Acción** > **Formar un solo equipo**. Se crea un equipo con el número especificado de alumnos.

   ![Formar una sola opción de equipo](assets/Group-Team-submission-and-rubric-based-assessments-image24.png "Formar un solo equipo")

1. Salva al equipo. Un equipo necesita al menos un alumno, que puede pertenecer a un solo equipo en la instancia.

1. Repita los pasos para crear equipos uno a uno.

### Añadir alumnos a un equipo existente

1. Seleccione los alumnos no asignados que desea añadir.

1. Elija asignarlos a un equipo existente y, a continuación, seleccione el equipo.

   ![Asignar alumnos no asignados a un equipo existente](assets/Group-Team-submission-and-rubric-based-assessments-image25.png "Asignar a un equipo existente")

1. Confirme su elección. Seleccione **Asignar alumno**.

### Mover o eliminar alumnos

1. Abra la pestaña **Equipos** y, a continuación, expanda un equipo para ver sus miembros.

1. Seleccione los alumnos que desea mover.

   ![Miembros del equipo seleccionados para mover](assets/Group-Team-submission-and-rubric-based-assessments-image26.png "Mover alumnos")

1. Elija moverlos y, a continuación, seleccione el equipo de destino.

1. Para eliminar a un alumno de un equipo, seleccione al alumno y elimínelo. El alumno vuelve a la lista sin asignar.

Cuando a un equipo no le quedan alumnos, el equipo se elimina automáticamente.

### Cambiar el nombre de un equipo

1. En la pestaña **Equipos**, selecciona el equipo y luego elige cambiarle el nombre.

1. Seleccione **Acción** > **Cambiar nombre**.

   ![Cambiar nombre de opción en el menú Acción](assets/Group-Team-submission-and-rubric-based-assessments-image27.png "Cambiar nombre de opción")

1. Escriba un nombre único, como Alpha de equipo.

   ![Cuadro de diálogo Cambiar nombre de equipo](assets/Group-Team-submission-and-rubric-based-assessments-image28.png "Cuadro de diálogo Cambiar nombre de equipo")

1. Seleccione **Cambiar nombre del equipo**.

Los nombres no se pueden repetir y no se puede utilizar el formato generado por el sistema, como Team-1.

### Eliminar equipos

1. En la pestaña **Equipos**, selecciona uno o más equipos.

1. Seleccione **Acción** > **Eliminar**.

1. Seleccione **Eliminar equipo**.

   ![Cuadro de diálogo Eliminar confirmación de equipo](assets/Group-Team-submission-and-rubric-based-assessments-image29.png "Eliminar equipo")

1. Confirme. Los alumnos de los equipos eliminados vuelven a la lista sin asignar.

### Gestionar inscripciones tardías y cancelaciones de inscripciones

* Un alumno que se inscribe una vez formados los equipos aparece en la lista sin asignar. Añadir el alumno a un equipo.
* Si todos los equipos están bloqueados, cree un nuevo equipo para el alumno.
* Un alumno que se da de baja se elimina automáticamente de su equipo. El equipo continúa y se elimina un equipo vacío.

### Resolución de problemas

**No puede seleccionar un equipo ni mover a sus miembros.** Un equipo se bloquea después de su primer envío y el bloqueo se aplica a todos los módulos del equipo de la instancia. Para desbloquear el equipo, anule el envío. Ver **Evaluar y cancelar el envío de envíos de equipo**.

**No se puede cambiar el nombre de un equipo.** El nombre ya está en uso o coincide con el formato generado por el sistema. Escriba un nombre diferente.

**Aparece un error al crear equipos.** Un equipo no puede tener más de 100 miembros. Reducir el número de miembros por equipo.

**No se puede abrir Administración de equipos para una instancia.** Es posible que se esté ejecutando la creación automática de equipos. Access regresa cuando finaliza.

**Se rechaza la operación de guardar y se vuelve a cargar la página.** Otro instructor o el trabajo automático guardado cambia primero. Revise los equipos actualizados y luego rehaga el cambio.

**Desapareció un equipo.** Un equipo sin alumnos se elimina automáticamente.

## Evaluar y cancelar el envío de envíos de equipo

Revisar el archivo enviado de un equipo, completar el plan de evaluación, aprobar o rechazar el trabajo, o cancelar el envío para que el equipo pueda volver a enviarlo.

Cuando se evalúa un envío de equipo, el resultado se aplica a todos los miembros del equipo y cada miembro recibe una notificación. Solo los instructores asignados a la instancia pueden evaluar. Los pasos son los mismos para envíos individuales, excepto que los envíos individuales no tienen detalles de equipo. Asegúrate de que los equipos existan primero. Ver **Crear y administrar equipos**.

Los equipos que se formaron automáticamente se pueden editar de la misma manera que los equipos manuales.

### Buscar un envío

1. En la aplicación del instructor, abre el área de envíos y, a continuación, selecciona **Envíos del equipo**. Seleccione **envíos individuales** para módulos de un solo alumno.

1. Para buscar un módulo, busque por nombre de sesión o módulo.

1. Seleccione el nombre del módulo.

   ![Lista de módulos en el área de envíos](assets/Group-Team-submission-and-rubric-based-assessments-image35.png "Lista de módulos")

1. Para reducir la lista, filtre por estado: **Envío pendiente**, **Revisión pendiente**, **Aprobado**, **Rechazado** o **Completado**.

1. Para ver los miembros del equipo, expanda el equipo. Se muestran los nombres y las direcciones de correo electrónico, y el alumno que envió el archivo tiene una etiqueta **Remitente**.

1. Para descargar el archivo enviado, seleccione la opción de descarga para el equipo.

### Evaluar un envío

1. Buscar el equipo con el estado **Revisión pendiente**.

1. Abra el archivo enviado y revise el contenido.

1. Seleccione **Acción** > **Evaluar**.

   ![Opción Evaluar en el menú Acción](assets/Group-Team-submission-and-rubric-based-assessments-image36.png "Opción Evaluar")

1. Completar el plan de evaluación:

   * Responde a todas las preguntas que quieras.
   * Para preguntas objetivas, seleccione una opción. Con la puntuación basada en criterios, la puntuación se actualiza a medida que se selecciona.
   * Para preguntas subjetivas, introduzca su respuesta.
   * Cuando se permitan observaciones, añádanse a la pregunta o a toda la evaluación.

   ![Plan de evaluación con preguntas objetivas y subjetivas](assets/Group-Team-submission-and-rubric-based-assessments-image37.png "Plan de evaluación")

1. Si el módulo requiere la aprobación del revisor, seleccione **Aprobar** o **Rechazar**. Añade un comentario cuando lo rechaces, para que el equipo sepa qué solucionar.

   ![Opciones de aprobación y rechazo](assets/Group-Team-submission-and-rubric-based-assessments-image38.png "Aprobar o rechazar")

1. Si el módulo utiliza la puntuación manual, introduzca la puntuación general.

   ![Campo de puntuación global para la puntuación manual](assets/Group-Team-submission-and-rubric-based-assessments-image39.png "Puntuación general")

   **Opcional**: Escriba una nota privada seleccionando el botón de alternancia **Agregar una nota privada al marcador**. Una nota privada solo está visible para los instructores asignados a la instancia. Los alumnos no pueden verlo, incluso cuando selecciona **Mostrar comentario**.

1. Envíe la evaluación. Seleccione **Enviar**. El estado del envío cambia a **Aprobado**.

   ![Opción Enviar para la evaluación](assets/Group-Team-submission-and-rubric-based-assessments-image40.png "Enviar evaluación")

Otros instructores también pueden evaluar el mismo envío, siempre que no se haya aprobado aún. Una evaluación posterior sustituye a otra anterior hasta que se aprueba el envío.

Si el módulo no requiere la aprobación del revisor, el módulo se completa para todos los miembros del equipo cuando el equipo realiza el envío. Solo aparece la opción Enviar y no podrá editar la puntuación o los comentarios posteriormente.

Después de aprobar o rechazar el envío de un equipo, un alumno puede ver el estado del envío y el resultado de la evaluación.

![Vista del alumno del estado del envío y del resultado de la evaluación](assets/Group-Team-submission-and-rubric-based-assessments-image41.png "Vista del alumno del estado")

Al seleccionar el resultado de la evaluación, se muestran los parámetros de evaluación y los comentarios del instructor.

![Parámetros de evaluación y comentarios en el resultado de la evaluación](assets/Group-Team-submission-and-rubric-based-assessments-image42.png "Resultado de la evaluación")

## Revisar o cambiar una evaluación

1. Buscar un equipo con el estado **Rechazado**.

1. Para abrir la evaluación finalizada, seleccione **Ver evaluación**.

1. Para volver a evaluar, seleccione la opción Volver a evaluar y envíe los cambios. Puede hacer esto solo para envíos rechazados. **No se pueden cambiar los envíos aprobados**.

### Cancelar el envío

Anule el envío de un envío cuando el equipo necesite enviarlo de nuevo, cuando la evaluación deba comenzar de nuevo o cuando necesite cambiar un equipo bloqueado. En el caso de un envío individual, también puede utilizar esta opción para corregir una evaluación introducida para el alumno incorrecto.

1. Busque un equipo o alumno que tenga un envío.

1. Seleccione **Anular envío**.

   ![Opción de no envío para un envío](assets/Group-Team-submission-and-rubric-based-assessments-image43.png "Opción de no envío")

1. Escriba sus comentarios y, a continuación, seleccione **No enviar envío**.

   ![Anular envío: cuadro de diálogo con un campo de comentarios](assets/Group-Team-submission-and-rubric-based-assessments-image44.png "Anular envío: cuadro de diálogo")

Se quitará el envío y el estado volverá a **Envío pendiente**. El equipo se desbloquea para que pueda editar sus miembros. Los miembros del equipo reciben una notificación y un correo electrónico. Cualquier miembro puede volver a enviarlo y el nuevo archivo reemplaza al anterior. La nueva evaluación reemplaza a la anterior y no se conserva ningún historial.

No se puede cancelar el envío una vez completado el curso para un miembro del equipo, ya que la finalización no se puede revertir.