---
jcr-language: en_us
title: Preguntas más frecuentes para administradores
description: Preguntas más frecuentes para administradores de Adobe Learning Manager
contentowner: manochan
exl-id: 8b113a4e-73f4-4cd5-982a-cefdf5388e91
source-git-commit: b128a2adb1d0655078d79b6d46c00612f4ddb996
workflow-type: tm+mt
source-wordcount: '2515'
ht-degree: 52%

---

# Preguntas más frecuentes para administradores

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Continúe leyendo para conocer las preguntas más frecuentes de Learning Manager asociadas con la función de administrador. </p></td>
  </tr>
 </tbody>
</table>

+++¿Puedo añadir usuarios en bloque? ¿Cómo lo hago?

Puede añadir usuarios en bloque con la función de carga del archivo .csv. Haga clic [aquí](/help/migrated/administrators/feature-summary/add-users-user-groups.md#bulk-upload-internal-users) para obtener más información.

+++

+++Escribí incorrectamente el ID de correo electrónico al crear el inicio de sesión para mis alumnos, ¿cómo lo corrijo?

Para corregir el inicio de sesión de usuario, debe importar el archivo CSV en Learning Manager. Un archivo .csv de muestra se adjunta al final de esta página para su referencia. Como el correo electrónico se considera un identificador exclusivo de una persona, no se puede editar. Siga estos pasos:

1. Añada el mismo usuario con el ID de correo electrónico correcto en CSV y asegúrese de que permanezca como responsable de otros usuarios añadiendo su ID de correo electrónico a la columna &quot;Correo electrónico del responsable del empleado&quot; en el CSV de ejemplo.
1. Añada otros usuarios de su cuenta al archivo .csv, incluido usted mismo.
1. Importe este archivo en la aplicación del administrador de Learning Manager > Usuarios >Añadir > Importar CSV.
1. Asigne todos los campos, como se solicita en el cuadro de diálogo, a las columnas CSV correspondientes.
1. Haga clic en Guardar.

Los usuarios deben añadirse en la página Alumnos.

[Ejemplo de Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++¿Cómo configuro las alertas?

En la versión 1.0 de Adobe Learning Manager, puede crear notificaciones. Consulte [pregunta de notificaciones](/help/migrated/administrators/feature-summary/user-notifications.md) para obtener más información.

+++

+++¿Cómo añado certificados para los cursos?

Adobe Learning Manager no proporciona certificados para los cursos. Sin embargo, el administrador puede crear insignias para cada curso haciendo clic en la ficha Insignias en el panel izquierdo. Cuando el administrador inscribe a los alumnos en un curso, también puede asociarle una insignia.

+++

+++¿Cómo se importan las firmas de los certificados?

En Adobe Learning Manager, no hay ninguna función para importar firmas para la certificación o la insignia.

+++

+++¿Puedo configurar un calendario para los cursos? ¿Cómo lo hago?

En la versión Adobe Learning Manager 1.0, no hay ninguna disposición para configurar el calendario de los cursos.

+++

+++¿Cómo inscribo directamente a los alumnos en lista de espera?

Los alumnos se colocan en una lista de espera para los cursos de clase cuando la capacidad es limitada, según el orden de inscripción. Los administradores pueden seleccionar los alumnos en lista de espera y asignar puestos reemplazando el límite de puestos de cualquier curso de clase. Los alumnos se inscriben en el curso tan pronto como el administrador asigna un lugar.

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador.
1. En la lista de cursos disponibles, haga clic en el nombre del curso de cualquier curso de clase que desee. Aparece una nueva página con información detallada sobre el curso.
1. Haga clic en Lista de espera en el panel izquierdo de la página Detalles del curso. En la página aparece una lista de alumnos en lista de espera.
1. Seleccione los alumnos y haga clic en Asignar puestos para inscribir a los alumnos directamente en los cursos reemplazando el límite de plazas.

Para obtener más información, consulte la función [lista de espera y asistencia](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md).

+++

+++¿Cómo registro la asistencia de los alumnos al módulo de clase?

Puede registrar la asistencia siguiendo estos pasos:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador.
1. En la lista de cursos disponibles, haga clic en el nombre del curso de cualquier módulo o curso de clase que quiera. Aparece una nueva página con información detallada sobre el curso.
1. Seleccione los alumnos y haga clic en Guardar para registrar la finalización del curso.

Si un curso consta de varios módulos y el alumno solo ha completado uno de ellos, puede seleccionar un módulo y hacer clic en Guardar para marcar su finalización para el alumno. Si este completa todos los módulos de un curso, puede hacer clic en la opción Seleccionar todo y después en Guardar.

Para obtener más información, consulte la función [lista de espera y asistencia](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md).

+++

+++¿Cómo incluyo la opción de comentarios de L3?

Puede añadir comentarios de L3 mientras inscribe a los alumnos en los cursos. Añada la pregunta de los comentarios de L3 siguiendo los pasos a continuación:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. Las listas de todos los cursos aparecen en la página derecha.
1. Haga clic en el mosaico del curso para el que desee agregar comentarios de L3.
1. Haga clic en la instancia predeterminada en el panel izquierdo.
1. Haga clic en el círculo del botón de alternancia junto a Comentarios sobre el cambio de comportamiento en L3 para seleccionarlo.
1. Añada la pregunta de comentarios de L3 en el área de texto debajo de Pregunta de L3.

+++

+++¿Cómo busco la nominación del responsable para un curso nominado al responsable?

Como administrador, puede buscar la nominación de responsable para los cursos siguiendo los pasos que se indican a continuación:

1. Haga clic en Cursos en el panel izquierdo.
1. Coloque el ratón sobre cualquier curso con nominación de responsable y haga clic en **[!UICONTROL Buscar nominación de responsable]**.

1. En la lista de instancias, haga clic en el vínculo **[!UICONTROL Administradores nominados]** seguido del vínculo **[!UICONTROL Agregar responsables]**.

1. Añada el nombre del responsable, el número de puestos asignados y haga clic en la marca de verificación para guardar los cambios.

Al crear los cursos, el autor elige el tipo de curso con responsable nominado.

+++

+++¿Cómo puedo inscribir a un alumno en un curso concreto?

Inscriba a los alumnos en los cursos siguiendo los pasos a continuación:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. La lista de todos los cursos aparece en la página derecha.
1. Elija el curso para el cual desea añadir alumnos y coloque el ratón sobre él.
1. Haga clic en Inscribir alumnos y añada el nombre de los alumnos. **Nota:** Puede agregar uno o varios alumnos a la vez.

+++

+++Cómo asignar alumnos a una aptitud concreta

Asigne los alumnos a competencias siguiendo los pasos que se detallan a continuación:

1. Haga clic en **[!UICONTROL Aptitudes]** en el panel izquierdo después de iniciar sesión como administrador.
1. Seleccione una o varias aptitudes haciendo clic en las casillas de verificación de cada competencia y haga clic en el menú desplegable **[!UICONTROL Acciones]** en la esquina superior derecha de la página.
1. Haga clic en Asignar a usuarios.
1. Empieza a escribir el nombre del usuario, elige en la lista desplegable y haz clic en **[!UICONTROL Guardar]**.

   >[!NOTE]
   >
   >Puede inscribir a varios alumnos en aptitudes. Para ello, haga clic en Añadir más usuarios y repita el cuarto paso.

+++

+++¿Cómo se crea una sesión de programa de aprendizaje?

Para crear un programa de aprendizaje, siga los pasos a continuación:

1. Haga clic en Programa de aprendizaje en el panel izquierdo. La página de programas de aprendizaje aparece con una lista de programas de aprendizaje ya creados.
1. Haga clic en Añadir en la esquina superior derecha de la página.\
   Introduzca el nombre del programa, información general, descripción y haga clic en Guardar.
1. Haga clic en Cursos en el panel izquierdo.
1. Agregue uno o varios cursos haciendo clic en + en cada icono de curso.

   >[!NOTE]
   >
   >Debe publicar el programa de aprendizaje antes de inscribir alumnos o una instancia.

1. Haga clic en Instancias en el panel izquierdo y haga clic en **[!UICONTROL Agregar nuevas instancias]** en la esquina derecha de la página para incluir detalles de la instancia.

Para obtener más información sobre los programas de aprendizaje, consulte [Programas de aprendizaje.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++¿Cómo modifico o personalizo informes para todas las funciones?

Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para editarlo o modificarlo. Haga clic en Guardar después de completar los cambios y ver el informe modificado.

+++

+++¿Cómo modifico cursos, programas de aprendizaje y perfil de empresa?

Puede editar cursos o programas de aprendizaje incluso después de publicarlos. Para obtener más información, consulte el contenido de ayuda de [Cursos](/help/migrated/administrators/feature-summary/courses.md) y [programas de aprendizaje](/help/migrated/administrators/feature-summary/learning-programs.md).

Para modificar el perfil de la empresa, haz clic en **[!UICONTROL Configuración]** en el panel izquierdo y haz clic en **[!UICONTROL Cambiar]** en la esquina superior derecha de la página.

+++

+++¿Cómo busco los cursos?

Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. Aparece una lista de todos los cursos disponibles.

Puede buscar cursos de dos formas:

1. Haga clic en el icono de búsqueda que aparece en la esquina superior derecha. Aparece un campo de búsqueda. Escriba el nombre del curso o de cualquier palabra clave asociada con los cursos para encontrar los cursos.
1. Filtrando la lista de cursos mediante los filtros.

Puede filtrar los cursos por estado, como Todos, Publicados o Retirado, haciendo clic en cada una de estas opciones. También puede buscar por competencias haciendo clic en Competencias y eligiendo cada una de ellas.

Según su elección, puede ver la lista filtrada de cursos y seleccionar los cursos requeridos.

+++

+++¿Puedo cambiar los temas de la aplicación? ¿Cómo lo hago?

Sí, puede cambiar los temas y la marca de la aplicación Learning Manager en función de los requisitos de su organización. Se proporciona un conjunto de cinco imágenes representativas para previsualizar los cambios en el tema de color antes de aplicarlos a su aplicación. Navegue a través de estas imágenes haciendo clic en los símbolos &lt; y > en el lado izquierdo y derecho de las imágenes, respectivamente, para obtener una vista previa.

Haz clic en **[!UICONTROL Marca]** en el panel izquierdo para actualizar el nombre de tu organización, cambiar el subdominio, registrar estilos y temas. Haga clic en **[!UICONTROL Editar]** junto a cada uno de estos temas para modificar el contenido.

Consulte [Ayuda sobre temas de color y marcas](/help/migrated/administrators/feature-summary/themes.md) para obtener más información.

+++

+++¿Cómo configuro insignias para los cursos?

1. Haga clic en Insignias en el panel izquierdo después de iniciar sesión como administrador.
1. Haga clic en Añadir en la esquina superior derecha de la página que se muestra en pantalla.
1. Añada el nombre a la insignia.
1. Cargue la insignia haciendo clic en Cargar insignia y haga clic en Guardar.

+++

+++¿Cómo configuro puntos de interacción para los cursos?

Puede configurar puntos de interacción para los alumnos siguiendo los pasos a continuación:

1. Haga clic en Interacción después de iniciar sesión como administrador. Aparece una lista con los niveles Bronce, Plata, Oro y Platino, así como los puntos que se necesitan para conseguir cada nivel. Hay disponible una lista de tareas con sus puntos correspondientes.
1. Haga clic en el icono Editar junto a cada tarea para configurar o modificar los puntos.

Consulte [Función de interacción](/help/migrated/administrators/feature-summary/gamification.md) para obtener más información.

+++

+++¿Cómo creo informes para responsables y alumnos?

Puede crear informes siguiendo los pasos a continuación:

1. Haga clic en Informes en el panel de la izquierda. Aparece la página Resumen de informes.
1. En la página Informes, haga clic en **[!UICONTROL Agregar]** en la esquina superior derecha.

   Aparece el cuadro de diálogo **[!UICONTROL Agregar informe]**.

1. Rellene todos los campos obligatorios y haga clic en Guardar.

Solo los administradores y los responsables pueden crear o ver informes. Consulte [característica Informes](/help/migrated/administrators/feature-summary/reports.md) para obtener más información.

+++

+++¿Cómo cambio a las funciones de alumno, responsable y autor?

Puede cambiar el inicio de sesión de su cuenta a otras funciones como alumno, responsable y autor sin necesidad de cerrar la sesión de su cuenta.

1. En la esquina superior derecha de la página, haga clic en la flecha desplegable junto la foto de su perfil.\
   Aparece un menú emergente.
1. Seleccione cada función disponible para obtener acceso a las respectivas cuentas de funciones.

+++

+++¿Cómo incluyo notificaciones para los usuarios?

Los responsables, autores y alumnos pueden ver las notificaciones basadas en las actividades del curso. El administrador puede habilitar y deshabilitar las notificaciones para todos los usuarios siguiendo los pasos a continuación:

1. Haga clic en Plantillas de correo electrónico en el panel izquierdo y seleccione las pestañas General, Inscripciones de usuario, Finalizaciones y Comentarios.
1. De los eventos que se enumeran a continuación, haga clic en los botones de alternar No/Sí junto a **cada evento &#x200B;** y seleccione Sí para habilitar la notificación. Haga clic en No para deshabilitar el envío de notificaciones para un determinado evento.

+++

+++¿Cómo permito la inscripción externa en los cursos?

Adobe Learning Manager le brinda la posibilidad de inscribir miembros de departamentos externos o empleados externos de su empresa en la aplicación.

1. Haga clic en **[!UICONTROL Usuarios]** en el panel izquierdo.
1. Haga clic en **[!UICONTROL Externo]** en el panel izquierdo.
1. Haga clic en **[!UICONTROL Agregar]** en la esquina superior derecha de la página.

   Aparece el cuadro de diálogo Añadir usuario.

1. Añada el nombre del perfil, el correo electrónico del responsable, los puestos asignados y la información de vencimiento. También puede añadir una imagen al perfil externo.
1. Haga clic en **[!UICONTROL Guardar]**.

 El administrador puede copiar la URL de registro y enviarla al grupo de inscripción externo. Los usuarios externos se pueden registrar en la aplicación Learning Manager y acceder a sus cursos.

+++

+++¿Cómo añado el cuestionario para los comentarios de L1?

Cree un cuestionario de comentarios que lo puedan utilizar los alumnos después de completar los cursos. De forma predeterminada, hay disponibles tres preguntas. Siga los pasos a continuación para crear un cuestionario.

1. Haga clic en Comentarios en el panel izquierdo. Aparece una ventana del cuestionario de comentarios.
1. Haga clic en **[!UICONTROL Editar]** para agregar o modificar el cuestionario.

Puede añadir un conjunto de cuestionarios y elegir no mostrarlos si no los necesita. Haga clic en la casilla de verificación para habilitar o deshabilitar una pregunta en particular.

+++

+++¿Cómo configuro las habilidades y los niveles?

1. Haga clic en Competencias en el panel izquierdo de la ventana del administrador.
1. Haga clic en Añadir para añadir competencias nuevas.
1. Indique el nombre de la competencia, la descripción y los créditos correspondientes a cada nivel.

   De forma predeterminada, un único nivel con 0 créditos estará disponible para cada competencia.

1. Haga clic en [!UICONTROL **Agregar nivel**] para agregar un nuevo nivel a cada competencia y haga clic en Guardar. Puede añadir hasta cinco niveles.

Una vez que se guarda la competencia, no puede eliminar los niveles de la competencia. El administrador también puede asignar alumnos a una determinada competencia y a un nivel concreto.

+++

+++¿Cómo configuro el sistema de facturación para los cursos de mi organización?

1. Haga clic en [!UICONTROL **Facturación**] en el panel izquierdo.

   La información de facturación aparece en la página.

1. Haga clic en la pestaña [!UICONTROL **Suscribirse**].
1. Escriba la cantidad de paquetes que desea pedir en el campo Paquetes de aprendizaje; a continuación, haga clic en Colocar orden en la esquina superior derecha de la página.

   Elija el número de paquetes en función del número de alumnos de su organización y realice el pedido. Para un proceso controlado por un pedido de compra, escríbenos a [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Proporcione su información de contacto, elija el tipo de tarjeta de crédito, especifique los datos de la tarjeta de crédito y haga clic en Completar orden.

Consulte la función [Administración de facturación](/help/migrated/administrators/feature-summary/billing-management.md) para obtener más información.

+++

+++¿Puedo personalizar el diseño del certificado? ¿Cómo lo hago?

En Adobe Learning Manager, puede reconocer alumnos emitiendo insignias. Consulte Insignias para obtener más información.  Consulte también la función Certificación.

+++

+++¿Cómo configuro mi perfil de empresa?

1. Después de iniciar sesión como administrador, haga clic en **[!UICONTROL Información de la empresa]** en el panel izquierdo.
1. Añada el perfil de la empresa, el subdominio y el logotipo haciendo clic en las opciones pertinentes en la página.

+++

+++¿Cómo añado cursos?

Para añadir cursos, debe cambiar su función a la de autor. Solo puede ver la lista de cursos disponibles según su estado: **[!UICONTROL Completado]**, **[!UICONTROL Publicado]** y **[!UICONTROL Retirado]**.

Para ver los cursos, haga clic en **[!UICONTROL Cursos]** en el panel izquierdo. Consulte [Creación de cursos](/help/migrated/administrators/feature-summary/courses.md)para obtener más información

+++

+++¿Cómo añado diferentes funciones a la aplicación?

Para añadir nuevos usuarios, siga los pasos a continuación:

1. Haga clic en Usuarios en el panel izquierdo después de iniciar sesión como administrador. También puede añadir usuarios haciendo clic en Introducción en el panel izquierdo de la ventana y haciendo clic en Añadir usuarios.
1. Para añadir usuarios nuevos, haga clic en Añadir en la esquina superior derecha de la página.

De forma predeterminada, la función de alumno se asigna a todos los usuarios nuevos. Puedes asignar funciones de administrador o autor a los alumnos haciendo clic en **[!UICONTROL Acciones]** en la esquina superior derecha de la página y eligiendo **[!UICONTROL Asignar función]** > **[!UICONTROL Convertir en autor]** o **[!UICONTROL Convertir en administrador]**.

Consulte la función [Añadir nuevos usuarios](/help/migrated/administrators/feature-summary/add-users-user-groups.md) para obtener información detallada sobre cómo añadir alumnos, autores y administradores.

+++

+++Cómo cambiar una imagen de fondo de un alumno?

Póngase en contacto con el equipo de asistencia de Learning Manager.

+++

++¿Dónde puedo encontrar el ID de mi cuenta de Learning Manager?

Puede obtener el ID de cuenta desde el navegador en el que está abierto Learning Manager.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++

+++¿Hay algún informe que pueda obtener o uno que alguien pueda obtener por mí que me muestre una lista de todos los cursos del LMS?

Sí, puedes obtener un **[!UICONTROL informe de formación]** que contenga todos los cursos, el programa de aprendizaje y la certificación del LMS. Para descargar el informe, sigue estos pasos:

1. Inicie sesión como administrador.
2. Haz clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Informe de cursos de formación]**.
3. Seleccione **[!UICONTROL Todos los cursos de formación]** en el menú desplegable.
4. Haga clic en **[!UICONTROL Descargar]**.

+++

+++ ¿Dónde puedo descargar la versión de escritorio de la aplicación?

Siga los pasos que se indican a continuación para descargar la versión de escritorio:

1. Inicie sesión como administrador.
2. Haz clic en **[!UICONTROL Aprendizaje social]** > **[!UICONTROL Configuración]**.
3. En **[!UICONTROL Configuración de descarga]**, haga clic en el hipervínculo en función de su sistema operativo.

+++
