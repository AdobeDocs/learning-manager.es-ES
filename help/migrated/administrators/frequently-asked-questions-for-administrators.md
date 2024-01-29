---
jcr-language: en_us
title: Preguntas más frecuentes para administradores
description: Preguntas más frecuentes para administradores de Adobe Learning Manager
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 0%

---



# Preguntas más frecuentes para administradores

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Siga leyendo para conocer las preguntas más frecuentes de Learning Manager asociadas a la función de administrador. </p></td>
  </tr>
 </tbody>
</table>

+++¿Puedo añadir usuarios en bloque? ¿Cómo?

Sí, puede añadir usuarios en bloque mediante la función de carga de CSV. Haga clic en  [aquí](/help/migrated/administrators/add-users-in-bulk.md) para obtener más información.

+++

+++Escribí incorrectamente el ID de correo electrónico al crear el inicio de sesión para mis alumnos, ¿cómo lo corrijo?

Para corregir el inicio de sesión del usuario, debe importar CSV en Learning Manager. Se adjunta un archivo CSV de muestra en la parte inferior de esta página como referencia. Como el correo electrónico se considera un identificador único para una persona, no se puede editar. Siga estos pasos:

1. Añada el mismo usuario con el ID de correo electrónico correcto en CSV y asegúrese de que permanezca como responsable de otros usuarios añadiendo su ID de correo electrónico a la columna &quot;Correo electrónico del responsable del empleado&quot; en el CSV de ejemplo.
1. Añadir otros usuarios de la cuenta al CSV, incluido usted mismo
1. Importe este archivo en la aplicación de administración de Learning Manager->Usuarios->Añadir->Importar CSV
1. Asigne todos los campos, como se solicita en el cuadro de diálogo, a las columnas CSV correspondientes.
1. Haga clic en Guardar.

Los usuarios deben añadirse en la página Alumnos.

[Ejemplo de Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++¿Cómo configuro las alertas?

En la versión Adobe Learning Manager 1.0, puede crear notificaciones. Consulte  [pregunta de notificaciones](/help/migrated/administrators/feature-summary/user-notifications.md) para obtener más información.

+++

+++¿Cómo añado certificados para los cursos?

Adobe Learning Manager no proporciona certificados para los cursos. Sin embargo, el administrador puede crear insignias para cada curso haciendo clic en la ficha Insignias en el panel izquierdo. Cuando el administrador inscribe alumnos en un curso, también puede asociarles una insignia.

+++

+++¿Cómo se importan las firmas de los certificados?

En Adobe Learning Manager no hay ninguna función para importar firmas para la certificación o insignia.

+++

+++¿Puedo configurar un calendario para los cursos? ¿Cómo?

En la versión Adobe Learning Manager 1.0, no hay ninguna disposición para configurar el calendario de los cursos.

+++

+++¿Cómo inscribo directamente a los alumnos en lista de espera?

Los alumnos se muestran en una lista de espera para cualquier curso de clase cuando las plazas son limitadas, en función del orden de inscripción. Los administradores pueden seleccionar los alumnos en lista de espera y asignar puestos reemplazando el límite de puestos de cualquier curso de clase. Los alumnos se inscriben en el curso en cuanto el administrador asigna una licencia.

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador.
1. En la lista de cursos disponibles, haga clic en el nombre del curso de cualquier curso de clase de su elección. Aparecerá una nueva página con información detallada sobre el curso.
1. Haga clic en Lista de espera en el panel izquierdo de la página de detalles del curso. En la página aparece una lista de alumnos en lista de espera.
1. Seleccione a los alumnos y haga clic en Asignar puestos para inscribir a los alumnos directamente en los cursos, reemplazando el límite de puestos.

Para obtener más información, consulte  [lista de espera y asistencia](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) función.

+++

+++¿Cómo registro la asistencia de los alumnos al módulo de clase?

Sí, puede registrar la asistencia siguiendo los pasos que se indican a continuación:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador.
1. En la lista de cursos disponibles, haga clic en el nombre del curso de cualquier módulo o curso de clase de su elección. Aparecerá una nueva página con información detallada sobre el curso.
1. Seleccione a los alumnos y haga clic en Guardar para registrar la finalización del curso.

Si hay varios módulos en un curso y el alumno ha completado solo uno de ellos, puede seleccionar un solo módulo y hacer clic en Guardar para marcar la finalización para el alumno. Si el alumno completa todos los módulos de un curso, puede hacer clic en la opción Seleccionar todo y, a continuación, hacer clic en Guardar.

Para obtener más información, consulte  [lista de espera y asistencia](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) función.

+++

+++¿Cómo incluyo la opción de comentarios de L3?

Puede añadir comentarios de L3 mientras inscribe a los alumnos en los cursos. Añada la pregunta de comentarios de L3 siguiendo los pasos que se indican a continuación:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. Las listas de todos los cursos aparecen en la página derecha.
1. Haga clic en el mosaico del curso para el que desee agregar comentarios de L3.
1. Haga clic en Instancia predeterminada en el panel izquierdo.
1. Haga clic en el círculo del botón de alternancia junto a Comentarios sobre el cambio de comportamiento en L3 para seleccionarlo.
1. Añada la pregunta de comentarios de L3 en el área de texto debajo de Pregunta de L3.

+++

+++¿Cómo busco la nominación del responsable para un curso nominado al responsable?

Como administrador, puede buscar la nominación de responsable para los cursos siguiendo los pasos que se indican a continuación:

1. Haga clic en Cursos en el panel izquierdo
1. Coloque el ratón sobre cualquier curso con nominación de responsable y haga clic en **[!UICONTROL Nominación de responsable de búsqueda]**.

1. En la lista de instancias, haga clic en **[!UICONTROL Gestores nominados]** vínculo seguido de **[!UICONTROL Añadir responsables]** vínculo.

1. Añada el nombre del responsable, el número de puestos asignados y haga clic en la marca de verificación para guardar los cambios.

Al crear los cursos, el autor elige el tipo de curso con nominación de responsable.

+++

+++¿Cómo puedo inscribir a un alumno en un curso concreto?

Inscriba a los alumnos en los cursos siguiendo los pasos que se indican a continuación:

1. Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. La lista de todos los cursos aparece en la página derecha.
1. Elija el curso para el que desea añadir alumnos y pase el ratón sobre él.
1. Haga clic en Inscribir alumnos y añada el nombre de los alumnos. **Nota:** Puede añadir uno o varios alumnos a la vez.

+++

+++Cómo asignar alumnos a una aptitud concreta

Asigne alumnos a competencias siguiendo los pasos que se indican a continuación:

1. Haga clic en **[!UICONTROL Aptitudes]** en el panel izquierdo después de iniciar sesión como administrador.
1. Seleccione una o varias aptitudes. Para ello, haga clic en las casillas de verificación de cada competencia y haga clic en **[!UICONTROL Acciones]** situado en la esquina superior derecha de la página.
1. Haga clic en Asignar a usuarios.
1. Empiece a escribir el nombre del usuario, selecciónelo en la lista desplegable y haga clic en **[!UICONTROL Guardar]**.

   >[!NOTE]
   >
   >Puede inscribir a varios alumnos en aptitudes. Para ello, haga clic en Añadir más usuarios y repita el cuarto paso.

+++

+++¿Cómo se crea una sesión de programa de aprendizaje?

Para crear un programa de aprendizaje, siga los pasos que se indican a continuación:

1. Haga clic en Programa de aprendizaje en el panel izquierdo. Aparece la página Programas de aprendizaje con una lista de los programas de aprendizaje existentes.
1. Haga clic en Añadir en la esquina superior derecha de la página.\
   Introduzca el nombre del programa, información general, descripción y haga clic en Guardar.
1. Haga clic en Cursos en el panel izquierdo.
1. Agregue uno o varios cursos haciendo clic en + en cada icono de curso.

   >[!NOTE]
   >
   >Debe publicar el programa de aprendizaje antes de inscribir alumnos o una instancia.

1. Haga clic en Instancias en el panel izquierdo y haga clic en **[!UICONTROL Añadir nuevas instancias]** en la esquina derecha de la página para incluir detalles de la instancia.

Para obtener más información sobre los programas de aprendizaje, consulte  [Función de programas de aprendizaje.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++¿Cómo modifico o personalizo informes para todas las funciones?

Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para editar o modificar informes. Haga clic en Guardar después de completar los cambios y ver el informe modificado.

+++

+++¿Cómo modifico cursos, programas de aprendizaje y perfil de empresa?

Puede editar cursos o programas de aprendizaje incluso después de publicarlos. Para obtener más información, consulte  [Cursos](/help/migrated/administrators/feature-summary/courses.md) y  [programas de aprendizaje](/help/migrated/administrators/feature-summary/learning-programs.md) Contenido de ayuda.

Para modificar el perfil de la empresa, haga clic en **[!UICONTROL Configuración]** en el panel izquierdo y haga clic en **[!UICONTROL Cambiar]** en la esquina superior derecha de la página.

+++

+++¿Cómo busco los cursos?

Haga clic en Cursos en el panel izquierdo después de iniciar sesión como administrador. Aparecerá una lista de todos los cursos disponibles.

Puede buscar cursos de dos formas:

1. Haga clic en el icono de búsqueda que se muestra en la esquina superior derecha. Aparece un campo de búsqueda. Escriba el nombre del curso o cualquier palabra clave asociada a los cursos para encontrar los cursos.
1. Filtrando la lista de cursos mediante los filtros.

Puede filtrar los cursos por estado, como Todos, Publicados o Retirado, haciendo clic en cada una de estas opciones. También puede buscar por competencias haciendo clic en Competencias y eligiendo cada una de ellas.

En función de su elección, puede ver la lista filtrada de cursos y seleccionar los cursos requeridos.

+++

+++¿Puedo cambiar los temas de la aplicación? ¿Cómo?

Sí, puede cambiar los temas y la marca de la aplicación Learning Manager en función de los requisitos de su organización. Se proporciona un conjunto de cinco imágenes representativas para obtener una vista previa de los cambios del tema de color antes de aplicarlos a la aplicación. Examine estas imágenes haciendo clic en los símbolos &lt; y > situados en el lado izquierdo y derecho de las imágenes, respectivamente, para previsualizarlas.

Haga clic en **[!UICONTROL Branding]** en el panel izquierdo para actualizar el nombre de su organización, cambie el subdominio, registre estilos y temas. Haga clic en **[!UICONTROL Editar]** junto a cada uno de estos temas para modificar el contenido.

Consulte la  [Ayuda de temas de color y marca](/help/migrated/administrators/feature-summary/themes.md) para obtener más información.

+++

+++¿Cómo configuro insignias para los cursos?

1. Haga clic en Insignias en el panel izquierdo después de iniciar sesión como administrador.
1. Haga clic en Añadir en la esquina superior derecha de la página que aparece.
1. Agregar nombre de insignia.
1. Cargue la insignia haciendo clic en Cargar insignia y haga clic en Guardar.

+++

+++¿Cómo configuro puntos de interacción para los cursos?

Puede configurar puntos de interacción para los alumnos siguiendo los pasos que se indican a continuación:

1. Haga clic en Interacción después de iniciar sesión como administrador. Aparece una página con una lista de los niveles de bronce, plata, oro y platino y los puntos necesarios para alcanzar correspondientes a cada nivel. Hay disponible una lista de tareas y los puntos correspondientes.
1. Haga clic en el icono Editar junto a cada tarea para configurar/modificar los puntos.

Consulte  [Función de interacción](/help/migrated/administrators/feature-summary/gamification.md) para obtener más información.

+++

+++¿Cómo creo informes para responsables y alumnos?

Puede crear informes siguiendo los pasos que se indican a continuación:

1. Haga clic en Informes en el panel izquierdo. Aparece la página Resumen del informe.
1. En la página Informes, haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha.

   **[!UICONTROL Agregar informe]** se abre.

1. Rellene todos los campos obligatorios y haga clic en Guardar.

Solo los administradores y los responsables pueden crear o ver informes. Consulte la [característica informes](/help/migrated/administrators/feature-summary/reports.md) para obtener más información.

+++

+++¿Cómo cambio a las funciones de alumno, responsable y autor?

Puede cambiar el inicio de sesión de su cuenta a otras funciones, como alumno, responsable y autor, sin cerrar la sesión de su cuenta.

1. Haga clic en la flecha desplegable junto a su imagen de perfil en la esquina superior derecha de la página.\
   Aparece un menú emergente.
1. Seleccione cada función disponible para obtener acceso a las cuentas de función respectivas.

+++

+++¿Cómo incluyo notificaciones para los usuarios?

Los responsables, autores y alumnos pueden ver notificaciones basadas en las actividades del curso. El administrador puede activar o desactivar las notificaciones para todos los usuarios siguiendo los pasos que se indican a continuación:

1. Haga clic en Plantillas de correo electrónico en el panel izquierdo y seleccione las pestañas General, Inscripciones de usuario, Finalizaciones y Comentarios.
1. De los eventos que se enumeran a continuación, haga clic en los botones de alternar No/Sí junto a **cada evento **y seleccione Sí para habilitar la notificación. Haga clic en No para desactivar el envío de notificaciones para un evento concreto.

+++

+++¿Cómo permito la inscripción externa en los cursos?

Adobe Learning Manager le ofrece la posibilidad de inscribir miembros externos del departamento o empleados externos de su organización en la aplicación.

1. Haga clic en **[!UICONTROL Usuarios]** en el panel izquierdo.
1. Haga clic en **[!UICONTROL Externo]** en el panel izquierdo.
1. Haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha de la página.

   Aparece el cuadro de diálogo Añadir usuario.

1. Añada el nombre del perfil, el correo electrónico del responsable, los puestos asignados y la información de caducidad. También puede añadir una imagen al perfil externo.
1. Haga clic en **[!UICONTROL Guardar]**.

El administrador puede copiar la URL de registro y enviarla al grupo de inscripción externo. Los usuarios externos pueden registrarse, iniciar sesión en la aplicación Learning Manager y acceder a sus cursos.

+++

+++¿Cómo añado el cuestionario para los comentarios de L1?

Cree un cuestionario de comentarios que puedan utilizar los alumnos después de completar los cursos. De forma predeterminada, hay disponibles tres preguntas de ejemplo. Siga los pasos que se indican a continuación para crear el cuestionario.

1. Haga clic en Comentarios en el panel izquierdo. Aparece una ventana del cuestionario de comentarios.
1. Haga clic en **[!UICONTROL Editar]** para agregar o modificar el cuestionario.

Puede agregar un conjunto de cuestionarios y elegir no mostrarlos si no los necesita. Haga clic en la casilla de verificación para activar o desactivar una pregunta en particular.

+++

+++¿Cómo configuro las habilidades y los niveles?

1. Haga clic en Competencias en el panel izquierdo de la ventana del administrador.
1. Haga clic en Añadir para añadir nuevas competencias.
1. Añada el nombre de la competencia, la descripción y los créditos correspondientes a cada nivel.

   De forma predeterminada, un solo nivel con 0 créditos estará disponible para cada competencia.

1. Haga clic en [!UICONTROL **Añadir nivel**] para añadir un nuevo nivel a cada competencia y haga clic en Guardar. Puede añadir hasta 5 niveles.

Una vez guardada la competencia, no se pueden eliminar niveles de la competencia. El administrador también puede asignar alumnos a una competencia y un nivel determinados.

+++

+++¿Cómo configuro el sistema de facturación para los cursos de mi organización?

1. Haga clic en [!UICONTROL **Factura**] en el panel izquierdo.

   La información de facturación aparece en la página.

1. Haga clic en [!UICONTROL **Suscribirse**] .
1. Escriba el número de paquetes que desea pedir en el campo Paquetes de alumnos y haga clic en Colocar orden en la esquina superior derecha de la página.

   Elija el número de paquetes en función del número de alumnos de su organización y realice el pedido. Para un proceso controlado por un pedido de compra, escríbenos a  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Introduzca su información de contacto, elija el tipo de tarjeta de crédito, proporcione los datos de la tarjeta de crédito y haga clic en Completar pedido.

Consulte [Gestión de facturación](/help/migrated/administrators/feature-summary/billing-management.md) para obtener más información.

+++

+++¿Puedo personalizar el diseño del certificado? ¿Cómo?

En Adobe Learning Manager, puede reconocer a los alumnos emitiendo insignias. Consulte Insignias para obtener más información.  Consulte también la función Certificación.

+++

+++¿Cómo configuro mi perfil de empresa?

1. Después de iniciar sesión como administrador, haga clic en **[!UICONTROL Información de empresa]** en el panel izquierdo.
1. Añada el perfil de empresa, el subdominio y el logotipo haciendo clic en cada una de estas opciones de la página.

+++

+++¿Cómo añado cursos?

Para añadir cursos, debe cambiar su función de autor. Solo puede ver la lista de cursos disponibles en función de su estado **[!UICONTROL Completar]**, **[!UICONTROL Publicado]**, y **[!UICONTROL Retirado]**.

Para ver los cursos, haga clic en **[!UICONTROL Cursos]** en el panel izquierdo. Consulte  [Creación de cursos](/help/migrated/administrators/feature-summary/courses.md)para obtener más información

+++

+++¿Cómo añado diferentes funciones a la aplicación?

Para añadir nuevos usuarios, siga los pasos que se indican a continuación:

1. Haga clic en Usuarios en el panel izquierdo después de iniciar sesión como administrador. También puede agregar usuarios haciendo clic en Introducción en el panel izquierdo de la ventana y haciendo clic en Agregar usuarios.
1. Para añadir nuevos usuarios, haga clic en Añadir en la esquina superior derecha de la página.

De forma predeterminada, todos los nuevos usuarios tienen asignada una función de alumno. Puede asignar funciones de administrador o autor a los alumnos haciendo clic en **[!UICONTROL Acciones]** en la esquina superior derecha de la página y eligiendo **[!UICONTROL Asignar función]** > **[!UICONTROL Convertir en autor]** o **[!UICONTROL Convertir en administrador]**.

Consulte  [Añadir nuevos usuarios](/help/migrated/administrators/feature-summary/add-users-user-groups.md) para obtener información detallada sobre cómo añadir alumnos, autores y administradores.

+++

+++Cómo cambiar una imagen de fondo de un alumno?

Póngase en contacto con el equipo de asistencia de Learning Manager.

+++

++¿Dónde puedo encontrar el ID de mi cuenta de Learning Manager?

Puede obtener el ID de cuenta en el navegador donde esté abierto Learning Manager.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++
