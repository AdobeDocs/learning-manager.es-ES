---
description: Lea este artículo para obtener información sobre cómo crear cursos, certificaciones y programas de aprendizaje en Learning Manager.
jcr-language: en_us
title: Creación, modificación y publicación de cursos
contentowner: manochan
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '6843'
ht-degree: 0%

---



# Creación, modificación y publicación de cursos

Lea este artículo para obtener información sobre cómo crear cursos, certificaciones y programas de aprendizaje en Learning Manager.

Los autores pueden crear objetos de aprendizaje como cursos, certificaciones y planes de aprendizaje. Los alumnos pueden consumir estos objetos de aprendizaje, mientras que los administradores pueden realizar un seguimiento del progreso de los alumnos.

## Cursos en Learning Manager {#coursesincaptivateprime}

Adobe Learning Manager permite a los autores crear cursos utilizando uno o varios módulos relacionados con la formación virtual, la formación con ritmo personalizado, la formación en aula y las actividades. Los administradores pueden seguir utilizando estos cursos para crear instancias de curso, inscribir alumnos, asignar insignias y activar los comentarios de estos cursos. También pueden crear programas de aprendizaje, planes de aprendizaje y certificaciones mediante estos cursos.

Los autores pueden utilizar contenido de aprendizaje electrónico creado con cualquier herramienta de aprendizaje electrónico. Otros formatos de curso admitidos son archivos de vídeo, PDF, doc, docx, PPT y PPTX.

## Crear un curso: flujo de trabajo básico {#createacoursebasicworkflow}

Para crear un curso, siga los pasos que se indican a continuación:

1. Inicie sesión en Adobe Learning Manager como autor, ya que solo los autores tienen derechos para crear cursos. Ahora, en la página Introducción, haga clic en **[!UICONTROL Crear cursos]**.
1. En la **Resumen del curso** , introduzca el nombre del curso. Ahora, introduzca una breve descripción de este curso, que se muestra en la tarjeta del curso. Esta descripción no debe superar los 140 caracteres. A continuación, introduzca la información general detallada del curso, que se muestra en la página Detalles del curso . La descripción no debe superar los 1500 caracteres.

   Como autor, puede ver la descripción de los módulos al añadir el módulo a un curso.

1. Para que el curso esté disponible en otros idiomas, haga clic en Añadir nuevo idioma en la esquina superior izquierda de la página. Seleccione el idioma o los idiomas en los que desea que esté disponible el curso. Haga clic en **[!UICONTROL Guardar]**. Para obtener más información, consulte [Añadir contenido para diferentes idiomas](/help/migrated/authors/feature-summary/content-library.md).
1. **Modificar la configuración del curso**-

   1. En la página Configuración del curso, elija una aptitud para el curso. En la lista desplegable Aptitud , elija la aptitud requerida. A continuación, en la lista desplegable Nivel, elija el nivel requerido.
   1. Elija las aptitudes del curso, el nivel y establezca los créditos de la aptitud. Añada más aptitudes, si es necesario.
   1. Desde el **Tipo de inscripción** , elija el tipo de inscripción.

   Estos son los tipos de inscripciones:

   * **Con nominación de responsable:** Solo los responsables pueden nominar estos cursos. Un alumno no puede inscribirse en este tipo de cursos.
   * **Aprobado por responsable:** Los responsables aprueban estos cursos. Los alumnos pueden inscribirse en estos cursos, pero no se inscriben directamente en ellos sin la aprobación del responsable. Se envía una solicitud de notificación a los responsables cuando los alumnos se inscriben en este tipo de cursos. Tras la aprobación del responsable, estos cursos se muestran como inscritos para los alumnos.
   * **Inscripción automática:** Los alumnos pueden inscribirse directamente en este tipo de cursos.

1. Para guardar los cambios, haga clic en **[!UICONTROL Guardar]**. Para publicar el curso, haga clic en **[!UICONTROL Publicar]**.

## Crear un curso: flujo de trabajo avanzado {#createacourseadvancedworkflow}

1. Inicie sesión en Adobe Learning Manager como autor, ya que solo los autores tienen derechos para crear cursos. Ahora, en la página Introducción, haga clic en **[!UICONTROL Crear cursos]**.
1. En la **Resumen del curso** , introduzca el nombre del curso. Ahora, introduzca una breve descripción de este curso, que se muestra en la tarjeta del curso. Esta descripción no debe superar los 140 caracteres. A continuación, introduzca la información general detallada del curso, que se muestra en la página Detalles del curso . La descripción no debe superar los 1500 caracteres.
1. Para que el curso esté disponible en otros idiomas, haga clic en Añadir nuevo idioma en la esquina superior izquierda de la página. Seleccione el idioma o los idiomas en los que desea que esté disponible el curso. Haga clic en **[!UICONTROL Guardar]**. Para obtener más información, consulte [Añadir contenido para diferentes idiomas](/help/migrated/authors/feature-summary/content-library.md).
1. **Modificar la configuración del curso**-

   1. En la página Configuración del curso, elija una aptitud para el curso. En la lista desplegable Aptitud , elija la aptitud requerida. A continuación, en la lista desplegable Nivel, elija el nivel requerido.
   1. Elija las aptitudes del curso, el nivel y establezca los créditos de la aptitud. Añada más aptitudes, si es necesario.
   1. Desde el **Tipo de inscripción** , elija el tipo de inscripción.

   Estos son los tipos de inscripciones:

   * **Con nominación de responsable:** Solo los responsables pueden nominar estos cursos. Un alumno no puede inscribirse en este tipo de cursos.
   * **Aprobado por responsable:** Los responsables aprueban estos cursos. Los alumnos pueden inscribirse en estos cursos, pero no se inscriben directamente en ellos sin la aprobación del responsable. Se envía una solicitud de notificación a los responsables cuando los alumnos se inscriben en este tipo de cursos. Tras la aprobación del responsable, estos cursos se muestran como inscritos para los alumnos.
   * **Inscripción automática:** Los alumnos pueden inscribirse directamente en este tipo de cursos.

1. Elija si quiere fijar un precio para su curso o hacerlo gratuito. Si desea que el curso sea de pago, elija la opción **[!UICONTROL Pagado]** y especifique un precio. El precio aparecerá entonces en la tarjeta del curso y en la página Resumen del curso de un alumno.

   NOTA: Esto solo se activa cuando se configura el conector de Adobe Commerce.

1. Si desea permitir que los alumnos puedan darse de baja del curso, active la casilla de verificación **Los alumnos pueden darse de baja ellos mismos**.
1. **Configuración de instancia**

   Si activa esta opción, los alumnos con el estado En curso pueden visitar otras instancias e inscribirse en ellas. A continuación, un alumno puede conservar el progreso de la instancia anterior.

   Después de publicar el curso, si vuelve a la página Configuración, la opción ya no se puede editar.

   Puede activar la opción para los siguientes tipos de curso:

   * Con ritmo personalizado
   * Classroom
   * Actividad
   * Mezclado

   Nota: Al duplicar un curso, si ha activado la opción Configuración de instancia en el curso de origen, la opción permanece desactivada en el curso de destino.

   **El conmutador de instancia no es compatible con**:

   * Cursos de pago
   * Cursos de tipo de inscripción con nominación de responsable.

   La configuración del conmutador de instancias no se propagará a las cuentas de igual a igual si se comparte a través del catálogo. La opción permanece desactivada en el curso de destino.

1. **Múltiples inscripciones**

   De este modo, puede inscribir alumnos en más de una instancia del curso en uno o varios períodos.

   Activar el conmutador **Inscripción múltiple** para cambiar entre varias inscripciones de curso de un alumno. Si ha habilitado el Cambio de instancia, no puede usar la inscripción múltiple.

1. Seleccione los requisitos previos de cursos que deben completarse antes de realizar el curso. Haga clic en el campo Cursos y elija una opción de la lista de cursos.
1. Habilite la **Habilitar** **Requisitos previos** casilla de verificación si desea que los requisitos previos del curso sean obligatorios.
1. Añada palabras clave como etiquetas relacionadas con el curso. Estas etiquetas ayudan a los alumnos a encontrar fácilmente su curso durante la búsqueda. Todas estas etiquetas se añaden automáticamente en función de los módulos que hemos añadido. Si tiene otras etiquetas que desee añadir a este curso, puede seguir adelante e introducirlas.
1. Añada palabras clave como etiquetas relacionadas con el curso. Estas etiquetas ayudan a los alumnos a encontrar fácilmente su curso durante la búsqueda. Todas estas etiquetas se añaden automáticamente en función de los módulos que hemos añadido. Si tiene otras etiquetas que desee añadir a este curso, puede seguir adelante e introducirlas.
1. En el campo Retirar automáticamente , seleccione una fecha en la que se retira el curso. El administrador debe activar primero la opción Retirar automáticamente.
1. Para guardar los cambios, haga clic en **[!UICONTROL Guardar]**. Para publicar el curso, haga clic en **[!UICONTROL Publicar]**.

## Puntos de interacción

Puede asignar puntos de interacción en los niveles de curso e instancia de curso. Con esto, puede asignar puntos a diferentes cursos o instancias. Se incentiva a los alumnos a realizar cursos específicos o a preferir una instancia de curso determinada sobre otras.

1. En el nivel de instancia del curso, seleccione **[!UICONTROL Puntos de interacción]**.

![puntos de interacción](assets/select-gamification-points-new.png)

*Establecer puntos para interacción*

1. Seleccionar **[!UICONTROL Editar]**.
1. Si selecciona Usar configuración de nivel de curso, se muestran las siguientes opciones:

   * **[!UICONTROL Al finalizar]**: seleccione este botón de alternancia si desea que el alumno obtenga 100 puntos al completar un curso.
   * **Más reglas**

      * **[!UICONTROL Finalización anticipada]**: si selecciona esta opción, los 30 primeros alumnos recibirán 100 puntos al completar un curso.
      * **[!UICONTROL Finalización oportuna]**: si selecciona esta opción, se conceden 100 puntos a los alumnos que completen un curso en un plazo de 99 días.

1. Si selecciona **[!UICONTROL Usar configuración personalizada]**, se muestran las siguientes opciones:

   * **[!UICONTROL Al finalizar]**: seleccione este botón de alternancia si desea que el alumno obtenga 100 puntos al completar un curso.
   * **Más reglas**

      * **[!UICONTROL Finalización anticipada]**: si selecciona esta opción, puede determinar a cuántos alumnos se les concederán puntos específicos.
      * **[!UICONTROL Finalización oportuna]**: si selecciona esta opción, puede determinar el número de puntos que se otorgarán a los alumnos que completen un curso en un tiempo especificado.

   ![puntos de interacción](assets/gamification-custom-settings.png)

   *Establecer finalización anticipada y oportuna*

1. Seleccionar **[!UICONTROL Guardar]**.

## Recursos de aprendizaje agregados

Un autor puede decidir si desea agregar los recursos de aprendizaje en el nivel de plan de aprendizaje o dejar que permanezcan en un nivel de curso individual.

Como autor, seleccione **[!UICONTROL Ruta de aprendizaje]** > **[!UICONTROL Configuración]**. Haga clic en **[!UICONTROL Editar]**.

En la **[!UICONTROL Recursos]** , la casilla de verificación Mostrar recursos de curso constitutivos agregados en el nivel de ruta de aprendizaje muestra si los recursos presentes en el nivel de curso se mostrarán en el nivel de ruta de aprendizaje.

>[!NOTE]
>
>En la página Configuración de una ruta de aprendizaje, un administrador también puede activar esta opción, que muestra los recursos presentes en el nivel del curso que se mostrarían en el nivel de ruta de aprendizaje.

## Asistente de programación

Gestiona conflictos en instructores de reservas y aulas. Si desea saber a qué hora y fecha está disponible un instructor antes de asignarlo al curso, utilice el Ayudante de programación.

Al crear un curso, para un curso de clase virtual o real, haga clic en Asistente de programación.

![Seleccione Asistente de Programación](assets/scheduling-assistant.png)

*Iniciar asistente de programación*

Se abrirá la ventana Asistente de Programación.

![Pantalla del Asistente de programación](assets/scheduling-assistant-window.png)

*Cuadro de diálogo Asistente de programación*

En el Asistente para programación, puede:

* Buscar instructores por sus nombres.
* Buscar instructores por sus aptitudes.

### Buscar instructores por sus nombres

En el campo Instructor , escriba el nombre del instructor o busque un nombre parcial de instructor. Aparecerá una lista de instructores, en la que puede elegir uno.

![Buscar instructores por nombre](assets/search-instructor.png)

*Buscar instructores*

Se pueden seleccionar varios instructores, pero solo se puede asignar uno a la vez. La hora seleccionada se resaltará en la ventana de conflicto de tiempo. Junto al instructor, aparece un icono de cruz en el que puede hacer clic para quitarlo.

![Seleccionar varios instructores](assets/busy-times.png)

*Buscar varios instructores*

### Buscar instructores por aptitudes

Busque un instructor con una o varias aptitudes. La búsqueda utiliza el operador AND.

Las aptitudes se pueden buscar solo por nombre de aptitud parcial o completo, no por nivel de aptitud.

En el Ayudante, introduzca el nombre del instructor, la ubicación y el límite de puestos.

Además, puede buscar la aptitud, que se mostraría después de hacer clic en el icono de filtro que aparece en el lado derecho del cuadro de búsqueda del instructor. La captura de pantalla siguiente muestra el botón.

![Introducción de aptitudes para el instructor](assets/scheduling-assistant-instructor-skill.png)

*Buscar instructores por aptitudes*

### Filtro de grupo de usuarios

Seleccione el filtro en el campo Instructor. Hay una **[!UICONTROL Grupo de usuarios]** filtrar un autor o un autor personalizado puede encontrar el instructor adecuado utilizando los valores del grupo de usuarios.

Si se aplican ambos filtros, aparecerá una lista de instructores que pertenecen al grupo de usuarios y que tienen las aptitudes seleccionadas.

Esto se aplica al Asistente de Programación en la página Cursos o Instancias.

![asistente programación](assets/scheduling-assistant-2.png)

*Filtrar por grupos de usuarios*

### Página Instancia

También puede acceder al Asistente de Programación desde la página Instancia, como se muestra a continuación.

El Asistente de programación también está disponible en la página Instancia para administradores y administradores/autores personalizados.

![Asistente de Programación desde la página Instancia](assets/instances-scheduling.png)

*Planificar instructores desde la página Instancias*

### Buscar una ubicación

Puede buscar una ubicación especificando el nombre de la clase y el nombre de la región de ubicación en las páginas del módulo y del Ayudante de programación.

## Formato de texto enriquecido

Al crear un curso, un programa de aprendizaje, una certificación o una ayuda de trabajo, los autores pueden introducir diferentes tipos de contenido, como texto o imágenes, o aplicar varias opciones de formato de texto.

Al crear un curso, puede ver el Editor de texto enriquecido en el campo Resumen del curso . Puede dar formato al contenido, agregar imágenes, agregar hipervínculos, etc.

![](assets/rich-text-editor-author.png)

*Iniciar el Editor de texto enriquecido*

Del mismo modo, puede utilizar el Editor de texto enriquecido para modificar la descripción al crear:

**Programa de aprendizaje**

![](assets/lp-rte-new.png)

*Usar el Editor de texto enriquecido para un programa de aprendizaje*

**Certificación**

![](assets/cert-rte-new.png)

*Usar el Editor de texto enriquecido para una certificación*

**Ayuda de trabajo**

![](assets/job-aid-rte-new.png)

*Usar el editor de texto enriquecido para una ayuda de trabajo*

Además, puede utilizar el Editor de texto enriquecido para otros idiomas.

## Compatibilidad con descripciones de texto enriquecido para la interfaz de usuario sin encabezado

### ¿Por qué se requiere CSS?

El texto enriquecido se compone de formato de HTML. Si se procesa el marcado tal cual, el navegador aplica un estilo predeterminado. A menudo, esto no se ajusta a las directrices de estilo de la empresa. Se requiere un CSS para cumplir las directrices.

### Estilo predeterminado

La hoja de estilos CSS adjunta contiene el estilo que aplica Learning Manager. El estilo se ha modificado teniendo en cuenta la mayoría de los casos de uso. Descargue el archivo CSS adjunto e impórtelo a su aplicación web según sus convenciones y sistema de compilación. Las clases CSS definidas tienen un espacio entre nombres en la clase de editor de SQL y no interfieren con los estilos existentes.

### Personalizar estilos

Es posible que el estilo predeterminado no satisfaga las necesidades de todos. Las personalizaciones se pueden realizar mediante la modificación del CSS proporcionado. Todo el estilo se ajusta en el editor de SQL como selectores descendientes. Se utilizan las clases siguientes:

* Sangría: **li.ql-guión-$number**. $number varía de 1 a 9
* tamaño: **ql-size-small**, **ql-size-large**, **ql-size-huge**

* alineación: **ql-align-center**, **ql-align-justify**, **ql-align-right**

* color: **ql-color-$color**. $color = blanco, rojo, naranja, amarillo, verde, azul, púrpura
* antecedentes: **ql-bg-$color**. $color = negro, rojo, naranja, amarillo, verde, azul, púrpura
* etiquetas html: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Archivo CSS que se va a utilizar para la personalización.](assets/ql-headless.css)

### CAMBIOS EN LA API PARA HABILITAR EL PROCESAMIENTO DE DESCRIPCIONES GENERALES DE TEXTO ENRIQUECIDO

Cuando los clientes crean una interfaz descentralizada, tienen la necesidad de mostrar los objetos de aprendizaje en la interfaz de usuario personalizada que están desarrollando. Para ello, se suele utilizar el [GET /learningObjects](https://learningmanagereu.adobe.com/docs/primeapi/v2/#!/learning_object/get_learningObjects) API que se muestra. Ahora que Learning Manager admite la captura de &quot;texto enriquecido&quot; para el campo de información general, el modelo de datos de objetos de aprendizaje en las respuestas de la API también muestra lo mismo. Consulte el campo denominado &quot;richTextOverview&quot; en el fragmento del modelo en la respuesta de la API que aparece a continuación. Tenga en cuenta también que el campo expuesto anteriormente (&quot;descripción general&quot;) no cambia para la compatibilidad con versiones anteriores.

```
{ 
 "data": [ 
 { 
 "id": "string", 
 "type": "string", 
 "attributes": { 
 … 
 "localizedMetadata": [ 
 { 
 "description": "string", 
 "locale": "string", 
 "name": "string", 
 "overview": "string", 
 "richTextOverview": "string" 
 } 
 ], 
 … 
 }, 
 "relationships": { 
 … 
 } 
 } 
 } 
 ] 
} 
```

Los clientes que ya utilizan el campo de descripción general no se ven afectados en su interfaz descentralizada, ya que solo verán texto sin formato como antes. Si los clientes desean aprovechar la información general de texto enriquecido, tendrán que crear descripciones generales con formato enriquecido para sus objetos de aprendizaje en la interfaz de usuario de autor. Después, Learning Manager comenzará a devolver también la información general de texto enriquecido, además del texto sin formato (como antes) en el modelo de respuesta de la API.

Sin embargo, para representar este texto enriquecido en su interfaz de usuario, el cliente deberá incluir un CSS. Esto se explica detalladamente en las siguientes secciones.

## Permitir varios intentos {#allowmultipleattempts}

Una vez que el administrador haya activado varios intentos, como autor puede configurar varios intentos para un módulo de aprendizaje electrónico interactivo en el nivel de curso o módulo.

![](assets/allow-multipe-attempts.png)

*Configurar varios intentos para un módulo de aprendizaje electrónico interactivo*

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Opción</b></p></td>
   <td>
    <p><b>Descripción</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Establecer intentos en</p></td>
   <td>
    <p>Puede establecer el número de intentos de un módulo en infinito o proporcionar un límite definido.<span style="font-size: 0.8125rem;">La información de intentos se mostrará al alumno una vez que se active. El alumno puede optar por volver a intentar el módulo haciendo clic en el botón Reintentar.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Detener el nuevo intento una vez que el módulo se complete y apruebe</p></td>
   <td>
    <p>Para configurar cuándo se debe impedir que los alumnos seleccionen la opción de nuevo intento, marque la casilla de verificación Detener el nuevo intento una vez que el módulo se complete y apruebe. La opción Reintentar se eliminará de la vista del alumno una vez que complete el módulo correctamente.</p></td>
  </tr>
  <tr>
   <td>
    <p>Bloquear módulo entre intentos 0:0:1 Formato: Días/Horas/Minutos</p></td>
   <td>
    <p>Puede bloquear módulos durante un intervalo de tiempo específico activando la casilla de verificación "<b>Bloquear módulo entre intentos 0:0:1 Formato: Días/Horas/Minutos</b>". Cuando un módulo está bloqueado, el alumno no puede visitarlo hasta que haya transcurrido el tiempo de bloqueo proporcionado. </p>
    <p>Puede definir los criterios de finalización de un intento seleccionando la opción '<b>Cierre del reproductor</b>' o '<b>Finalización</b>' casillas de verificación.</p></td>
  </tr>
  <tr>
   <td>
    <p>Cierre del reproductor</p></td>
   <td>
    <p>Cada inicio de módulo se trata como un nuevo intento si los criterios se seleccionan como '<b>Cierre del reproductor</b>'. Se solicita al alumno que proporcione los detalles del bloqueo del módulo e intente cerrar el reproductor.</p></td>
  </tr>
  <tr>
   <td>
    <p>Finalización</p></td>
   <td>
    <p>Si el final de un intento se basa en <b>Finalización</b>, luego se calculará en función de los criterios de contenido correcto. Los alumnos no pueden volver a intentar el módulo hasta que el contenido envíe la información de finalización. Los detalles del bloqueo del módulo y los intentos se comunican al alumno una vez que finaliza un intento.</p></td>
  </tr>
  <tr>
   <td>
    <p>Definir límite de tiempo para completar el módulo</p></td>
   <td>
    <p>Los autores pueden establecer un límite de tiempo para completar un módulo activando la casilla de verificación ",<b>Definir límite de tiempo para completar el módulo</b>".</p>
    <p>Cada inicio de reproductor se considera un nuevo intento, y al alumno se le indican los detalles de tiempo durante el inicio.</p>
    <p><b>Nota:</b><span style="font-size: 0.8125rem;">El intento finalizará automáticamente una vez que haya transcurrido el tiempo. Si se cierra el reproductor, el intento actual también se cerrará.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Varios intentos a nivel de módulo</p></td>
   <td>
    <p>Si selecciona un intento en el nivel Módulo en la lista desplegable Definir intento en, podrá configurar las opciones en el nivel de módulo individual.</p></td>
  </tr>
 </tbody>
</table>

## Módulos del curso {#coursemodules}

### Añadir módulos {#addmodules}

Ahora puede añadir módulos de contenido, trabajo previo y prueba. **Contenido** Los módulos son los módulos principales que componen el curso. **Trabajo Previo** Los módulos incluyen información básica que puede ayudar a los alumnos a prepararse para el curso. Estos módulos no son obligatorios para que los alumnos los completen. **Testout** Los módulos ayudan a los alumnos a omitir el contenido y realizar la prueba si ya conocen el contenido y desean realizar la prueba para cumplir los requisitos de cumplimiento.

Para añadir un módulo de contenido, siga los pasos que se indican a continuación:

1. Haga clic en **[!UICONTROL Añadir módulos]**. Puede ver cuatro opciones para añadir módulos. La primera opción es añadir Módulos con ritmo personalizado. Estos son los módulos que se crean y se añaden a la biblioteca de módulos en Adobe Learning Manager. Esta segunda opción es configurar la clase virtual. El tercero es configurar un módulo de clase y el cuarto es el módulo de actividad.

   ![](assets/select-module-type.png)

   *Añadir un módulo a un curso*

   **Módulo con ritmo personalizado:** En este modo, puede iniciar y completar un módulo de curso a su propio ritmo. Puedes establecer tu propio horario.

   Después de hacer clic en la opción, puede ver la lista de módulos con ritmo personalizado que ya se han añadido a la biblioteca de módulos. Aquí puede desplazarse por la lista y seleccionar los que desea agregar, o puede buscar los módulos escribiendo el nombre del módulo en el campo de búsqueda o las etiquetas del módulo.

   Una vez seleccionados los módulos, haga clic en **[!UICONTROL Añadir]**. Estos módulos aparecen ahora en la sección Contenido.

   También puede reorganizar los módulos. Arrastre cualquier módulo, muévalo hacia arriba o hacia abajo y organice los módulos en la secuencia adecuada.

   **Módulo de clase virtual:** En este modo, los alumnos pueden asistir a conferencias en línea en directo, facilitadas por un instructor formado. Introduzca el título, la descripción y establezca la duración de la sesión. También puede especificar la dirección URL de la conferencia y los instructores que dirigirán la sesión. Para guardar los cambios, haga clic en **[!UICONTROL Hecho]**.

   ![](assets/1st-image.png)

   *Añadir un módulo de clase virtual*

   Al crear un curso mediante el cuadro de diálogo de configuración de Clase virtual, defina la **Sistema de conferencia** a la conexión de equipos que haya creado. Seleccione si desea un organizador de reuniones para el evento.

   Si selecciona **Sí** para un organizador de reuniones, debe escribir el nombre del organizador. Escriba el nombre y seleccione el organizador.

   **Evasión del vestíbulo**

   * Si selecciona **Sí**, cualquier alumno puede unirse a la reunión.
   * Si selecciona **No**, se envía una solicitud al organizador para permitir o evitar que el alumno se una a la reunión.

   **Nota:** Un alumno debe estar disponible en Microsofts Teams. Sin embargo, el alumno puede unirse a Learning Manager como invitado.

   **Módulo de clase:** En este modo, los alumnos asisten a conferencias en persona, facilitadas por un instructor capacitado. Introduzca el título, la descripción y establezca la duración de la sesión. También puede especificar la ubicación de la clase y los instructores que dirigirán la sesión. Para guardar los cambios, haga clic en **[!UICONTROL Hecho]**.

   ![](assets/classroom-module.png)

   *Añadir un módulo de clase*

   Al crear un curso, en el cuadro de diálogo Configuración de clase virtual, establezca el sistema de conferencia en la conexión de Microsofts Teams que haya creado. Seleccione si desea un organizador de reuniones para el evento.

   Si selecciona Sí para un organizador de reuniones, debe escribir el nombre del organizador. Escriba el nombre del organizador y seleccione el organizador.

   **Evasión del vestíbulo**

   * Si selecciona Sí, cualquier alumno puede unirse a la reunión.
   * Si selecciona No, se envía una solicitud al organizador para permitir o evitar que el alumno se una a la reunión.

   **Nota:** Si un alumno desea unirse a Microsofts Teams como invitado, debe introducir el correo electrónico. El correo electrónico debe estar incluido en Learning Manager.

   **Módulo de actividad:** En este modo, los alumnos deben completar un conjunto de actividades, como talleres, ejercicios, cuestionarios y otras actividades de aprendizaje. Introduzca el título, la descripción y la URL externa como referencia. Para guardar los cambios, haga clic en **[!UICONTROL Hecho]**.

   ![](assets/activity-module.png)

   *Añadir un módulo de actividad*

   Puede especificar la duración al añadir un módulo de actividad en un curso para el tipo de actividad Envío de archivos y módulos basados en xAPI.

1. Del mismo modo, añada módulos para los modos de trabajo previo y de prueba.
1. Elija el tipo de secuencia para los módulos como Ordenado o Sin ordenar según sus preferencias.

   Si elige **Ordenado**, los módulos aparecen en la misma secuencia en la que se crearon. Si elige **Sin Ordenar**, los módulos no se secuencian. Los alumnos pueden completar los módulos en cualquier orden.

1. En la lista desplegable Módulos obligatorios, elija el número de módulos que debe realizar el alumno para completar el curso.
1. Añada una imagen de portada y el banner del curso. El administrador crea los catálogos. Para obtener más información, consulte [Catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

   **Nota:** Las dimensiones recomendadas son:

   * **Imagen de portada:** 300 x 300 px
   * **Imagen del banner:** 1600 x 140 px

1. En la esquina superior derecha de la página, haga clic en **[!UICONTROL Guardar]**.

## Lista de comprobación {#create-checklist}

La evaluación es un aspecto importante de cualquier sistema de gestión de aprendizaje. Las evaluaciones en línea son una de las principales formas de evaluar la comprensión de un tema por parte del alumno. Pero a menudo, es necesario evaluar la comprensión de una persona mientras está en el trabajo observando que lleva a cabo las tareas necesarias.

Consideremos a los empleados de las tiendas o a los trabajadores de los almacenes que están siendo evaluados para las tareas que se supone que deben llevar a cabo día a día. Podría tratarse de los pasos llevados a cabo para reparar una máquina de café o los pasos implicados en el embalaje de un material. Los instructores pueden evaluar a los empleados en relación con estas tareas según una lista de comprobación y calificar su labor como Aprobado o Suspenso en la actividad de evaluación.

### Crear una lista de comprobación {#createachecklist}

Solo un autor puede crear una lista de comprobación. Una lista de comprobación es un tipo de módulo de actividad. Al configurar un módulo de actividad, usted, como autor, puede seleccionar una actividad como **Lista de comprobación**, como se muestra a continuación:

![](assets/checklist-option.png)

*Crear una lista de comprobación*

Una vez que haya seleccionado la opción **Lista de comprobación**, verá algunas opciones adicionales.

**Tipo de lista de comprobación:** Elija cualquier opción, **Sí/No** o **1-5**. Si elige Sí/No, la lista de comprobación contendrá preguntas que sólo se pueden responder con Sí o No. Si elige 1-5, puede ver una lista de comprobación de tipo Likert, en la que puede calificar una pregunta en una escala de cinco puntos.

**Criterios para aprobar:**

<table>
 <tbody>
  <tr>
   <td>
    <p>Si hubiera elegido <b>Sí/No</b>Entonces...</p></td>
   <td>
    <p>Si hubiera elegido <b>1-5</b>Entonces...</p></td>
  </tr>
  <tr>
   <td>
    <p>Establezca los criterios para aprobar como el número de respuestas como Sí. Por ejemplo, si introduce 3, el alumno aprobará el curso si recibe al menos tres <b>Sí </b>respuestas, cuando las evalúa un instructor.</p></td>
   <td>
    <p>Establezca los criterios para aprobar como un umbral de cualquier número entre 1 y 5. Por ejemplo, si introduce 2 y 4, el alumno aprobará el curso si obtiene al menos <b>dos </b>evaluaciones que tengan una puntuación mayor o igual que <b>cuatro</b>.</p></td>
  </tr>
 </tbody>
</table>

Elija uno o varios instructores que evalúen al alumno.

Además, si tiene algo que comentar o una nota, puede añadirlo en el **Nota para el instructor** campo de texto.

Ahora, agregue las preguntas de la lista de comprobación. Haga clic en **[!UICONTROL Añadir]**. Solo puede añadir hasta 150 preguntas.

![](assets/add-checklist-questions.png)

*Añadir preguntas de lista de comprobación*

Para añadir más preguntas, haga clic en **[!UICONTROL Añadir más]**.

Guarde los cambios, añada el módulo y publique el curso.

### Añadir aptitudes {#addskills}

En esta página, introduzca los siguientes detalles:

1. Elija las aptitudes del curso, el nivel y establezca los créditos de la aptitud. Añada más aptitudes, si es necesario.

   ![](assets/course-skills.png)

   *Añadir aptitudes para un curso*

1. Elija el tipo de inscripción. Estas son las opciones:

   * **Con nominación de responsable:** Solo los responsables pueden nominar estos cursos. Un alumno no puede inscribirse en este tipo de cursos.
   * **Aprobado por responsable:** Los responsables aprueban estos cursos. Los alumnos pueden inscribirse en estos cursos, pero no se inscriben directamente en ellos sin la aprobación del responsable. Se envía una solicitud de notificación a los responsables cuando los alumnos se inscriben en este tipo de cursos. Tras la aprobación del responsable, estos cursos se muestran como inscritos para los alumnos.
   * **Inscripción automática:** Los alumnos pueden inscribirse directamente en este tipo de cursos.

1. Si desea permitir que los alumnos puedan darse de baja del curso, active la casilla de verificación **Los alumnos pueden darse de baja ellos mismos**.
1. Seleccione los requisitos previos de cursos que deben completarse antes de realizar el curso. Haga clic en el campo Cursos y elija una opción de la lista de cursos.

   ![](assets/prerequisite-courses.png)

   *Añadir cursos de requisitos previos*

1. Habilite la **Requisitos previos** casilla de verificación si desea que los requisitos previos del curso sean obligatorios.
1. Añada palabras clave como etiquetas relacionadas con el curso. Estas etiquetas ayudan a los alumnos a encontrar fácilmente su curso durante la búsqueda. Todas estas etiquetas se añaden automáticamente en función de los módulos que hemos añadido. Si tiene otras etiquetas que desee añadir a este curso, puede seguir adelante e introducirlas.
1. Añada los perfiles de su público objetivo para este curso haciendo clic en el área de texto y eligiendo los perfiles entre las sugerencias.
1. Agregue archivos de recursos para el curso como material adicional. Arrastre materiales como archivos de texto, vídeo o audio.
1. Este curso estará disponible para los alumnos que tengan estos perfiles como curso recomendado. También puede adjuntar recursos adicionales para sus alumnos en esta sección. Los alumnos podrán descargar estos archivos para consultarlos más adelante. Cuando haya terminado con todos estos cambios, haga clic en **[!UICONTROL Guardar]** en la esquina superior derecha. Esto guardará el curso como borrador. De forma predeterminada, el curso se guarda como borrador.

## Asignar instructores para módulos {#assigninstructorsformodules}

1. Después de crear módulos para el curso, puede asignar instructores a los módulos. En el tablero de autor, haga clic en **[!UICONTROL Catálogo de cursos]**.
1. Haga clic en el curso a cuyo módulo desea asignar instructores.
1. Desde el **Añadir módulos** , haga clic en el módulo al que desee asignar un instructor.
1. En la **Instructor** , especifique el nombre del usuario al que desea asignar la función de instructor.

   ![](assets/instructor-field.png)

   *Asignar una función de instructor a un usuario*

1. Para volver a publicar el curso con las actualizaciones, haga clic en **[!UICONTROL Volver a publicar]**.

## Lista de verificación de observaciones

Los responsables, además de los instructores, ahora pueden revisar un módulo Lista de comprobación. Los gestores de personal, así como los no jerárquicos, como los gestores de tienda o los gestores de ubicación, pueden revisar y completar la lista de comprobación.

Los autores del curso pueden añadir responsables de personal y responsables no jerárquicos (si procede) como revisores seleccionando estas opciones de función en la sección &quot;Revisores&quot; al configurar un módulo de lista de comprobación. Esto se puede hacer a nivel de instancia de curso.

![Lista de comprobación para responsables](assets/manager-checklist.png)

*Añadir revisores en un módulo de actividad*

Seleccionar el icono &quot;**[!UICONTROL +Administradores]**&quot; activará automáticamente el responsable de un alumno en la jerarquía de la organización para que revise la lista de comprobación. No es necesario buscar y agregar nombres de responsables individualmente.

Si el administrador de cuentas ha configurado funciones de administrador no jerárquicas (como administradores de ubicación o administradores de sitio) mediante la opción Campos activos, dichas funciones de administrador estarán disponibles para que pueda seleccionarlas y habilitarlas para revisar la lista de comprobación.

No es necesario buscar y agregar nombres de responsables individualmente. Cuando los alumnos se inscriben en el curso de lista de comprobación, se envía automáticamente una notificación a los responsables/responsables de la tienda para que la revisen junto con el instructor seleccionado. Este flujo de trabajo facilita que los autores no mencionen los nombres de los responsables individuales.

En la captura de pantalla de ejemplo proporcionada anteriormente, seleccione el icono &quot;**[!UICONTROL +Administradores de tienda]**&quot; activará automáticamente el responsable no jerárquico alineado con el alumno para revisar la lista de comprobación. Tenga en cuenta que &quot;store&quot; aquí será reemplazado por el campo activo definido por el administrador.

Las actualizaciones del módulo de lista de comprobación también incluyen notificaciones a los instructores y responsables cuando un alumno se inscribe en un curso que tiene un módulo de lista de comprobación. El revisor recibirá una notificación en el centro de notificaciones de Learning Manager, así como en el tablero del instructor/responsable, de que debe realizarse una acción de lista de comprobación.

<!--![View notification for enrollment](assets/checklist-notification.png)-->

El revisor podrá ver información sobre todos los elementos de revisión de listas de comprobación pendientes en el menú Listas de comprobación, así como en el menú Notificaciones, cuando inicie sesión como instructor/responsable.

![Aprobaciones de certificados](assets/pending-task-managers.png)

*Aprobaciones de certificación*

Después de hacer clic en Revisar lista de comprobación, el revisor puede completar la evaluación.

![Revisar elementos de revisión de lista de comprobación pendientes](assets/evaluation-checklist.png)

*Revisar elementos de revisión de lista de comprobación pendientes*

Los informes se pueden descargar en listas de comprobación, que incluyen información detallada sobre la evaluación del alumno, el nombre del revisor, la función y el correo electrónico.

El archivo CSV del informe de lista de comprobación tiene los campos nuevos y actualizados:

* Nombre del revisor en lugar de Nombre del instructor
* Correo electrónico del revisor en lugar de Correo electrónico del instructor
* Función del revisor: los valores posibles son Responsable, Administrador de almacén/ubicación, Instructor

## Vista previa de un curso {#previewacourse}

Una vez creado y guardado el curso como borrador, puede previsualizarlo como alumno y, a continuación, publicarlo para que esté disponible en el catálogo del curso.

Para obtener una vista previa del curso, haga clic en **[!UICONTROL Vista previa como alumno]**.

![Vista previa de un curso como alumno](assets/preview-as-a-learner.png)

*Vista previa de un curso como alumno*

Se abre el curso. **Resumen** para que pueda ver los módulos, su orden y otros detalles relacionados con el curso.

![](assets/overview-page.png)

*Ver módulos y otros detalles relacionados*

Para ver cómo los alumnos pueden experimentar este curso, haga clic en cada uno de estos módulos para empezar a reproducirlo. Esto comienza a reproducir el curso en el reproductor Fluidic.

## Publicar un curso {#publishacourse}

Después de previsualizar el curso como alumno, puede publicarlo para que esté disponible para que lo consuman los alumnos. Tenga en cuenta que el curso todavía está en modo de borrador.

El ciclo de vida de un curso típico es el siguiente:

* **Draft** - Cuando un autor termina de crear un curso y lo guarda. En este estado, el curso aún no está disponible para los alumnos.
* **Publicado** - Cuando un autor finaliza la publicación de un curso. En este estado, el curso está disponible para que los alumnos se inscriban. También puede editar un curso en este estado.
* **Retirado** - Después de publicar un curso, un autor puede moverlo al estado retirado si no desea que el curso aparezca en el catálogo de cursos para los alumnos.
* **Eliminado** - Un curso en estado eliminado se elimina por completo de la aplicación Adobe Learning Manager. Solo los autores pueden eliminar cursos cuando están en estado Borrador o Retirado .

![](assets/typical-course-lifecycle.png)

*Flujo de trabajo del ciclo de vida de un curso*

Para publicar el curso creado, haga clic en **[!UICONTROL Publicar]** en la esquina superior derecha de la página.

![](assets/publish-a-course.png)

*Publicar un curso*

En el mensaje emergente de confirmación que aparece, haga clic en **[!UICONTROL OK]**.

El curso ya está disponible en el catálogo de cursos.

## Ver un curso {#viewacourse}

Puede ver una lista de todos los cursos disponibles como autor. Para ver todos los cursos en la cuenta de Learning Manager, haga clic en Catálogo de cursos. Para ver todos los cursos creados en Learning Manager, haga clic en **[!UICONTROL Mis cursos]**.

En la tarjeta del curso, desplace el cursor sobre las opciones y haga clic en **[!UICONTROL Ver curso]**.

![](assets/view-a-course.png)

*Ver un curso*

Aparece la ventana de información del curso. El curso está en modo de solo lectura. Para modificar el curso, haga clic en **[!UICONTROL Editar]**.

## Retirar un curso {#retireacourse}

Si retira un curso, no puede inscribir nuevos alumnos en el curso. Los alumnos que ya se han inscrito pueden realizar el curso.

Para retirar un curso, en la tarjeta del curso, desplace el cursor sobre las opciones y haga clic en Retirar curso.

![](assets/retiring-course.png)

*Retirar un curso*

En la ventana emergente de confirmación que aparece, haga clic en **[!UICONTROL Sí]**.

## Duplicar un curso {#duplicateacourse}

Puede crear una copia del curso y, a continuación, modificarlo. Si desea realizar una copia de seguridad del curso, puede duplicarlo.

## Buscar cursos {#searchforcourses}

Adobe Learning Manager le facilita la búsqueda rápida de los cursos que desee. Puede buscar los cursos de las siguientes maneras:

**Campo de búsqueda:** Haga clic en la barra de búsqueda en la esquina superior derecha de la **Catálogo de cursos** página. Escriba el nombre del curso o cualquier palabra clave asociada a los cursos. También puede buscar mediante etiquetas que se añaden durante la creación del curso. Las etiquetas se pueden buscar en el campo Buscar cursos , lo que significa que las etiquetas se muestran en el campo de búsqueda mientras escribe.

![](assets/search-field.png)

*Buscar cursos*

**Filtrar lista de cursos:** Puede filtrar los cursos por estado, como Todos, Publicados, Borrador y Retirado. En función de su elección, puede ver la lista filtrada de cursos y seleccionar los cursos requeridos.

Como autor, también puede ordenar los cursos para encontrar mejor el curso requerido. Haga clic en **[!UICONTROL Ordenar por]** y elija orden alfabético ascendente, orden alfabético descendente, fecha de creación del curso, fecha de actualización del curso y eficacia de los cursos.

![](assets/filter-list-of-courses.png)

*Filtrar lista de cursos*

## Inscribir alumnos en un curso {#enrolllearnersinacourse}

Para inscribir alumnos en los cursos o permitir que los responsables designen alumnos para los cursos, debe cambiar al modo de administrador, ya que solo los administradores tienen derechos para inscribir alumnos en los cursos.

Para cambiar al modo de administrador,

1. Haga clic en la imagen de perfil y, a continuación, seleccione Administrador.
1. En el modo de administrador, haga clic en **[!UICONTROL Cursos]** en el panel izquierdo. En esta página, puede ver todos los cursos creados por todos los autores en su cuenta de Learning Manager.
1. Para inscribir a los alumnos, pase el ratón sobre la tarjeta del curso y verá la opción **Inscribir alumnos**. Haga clic en esta opción

   ![](assets/enroll-learners.png)

   *Inscribir alumnos en un curso*

1. En el cuadro de diálogo Inscribir alumnos, en la esquina superior derecha puede ver que la opción **Instancia predeterminada** está seleccionado. Tan pronto como un autor crea un curso, se crea una instancia predeterminada del curso.

   ![](assets/default-instance.png)

   *Ver la instancia predeterminada de un curso*

1. Comience a escribir el nombre de un alumno en el campo Incluir alumnos y elija un alumno. También puede añadir grupos de usuarios aquí. Si desea inscribir a todos los alumnos en su cuenta de Learning Manager, empiece a escribir todos. También puede inscribir alumnos en un equipo.

   ![](assets/include-learners.png)

   *Añadir alumnos a un curso*

1. Si desea excluir a cualquier alumno del curso, introduzca el nombre del alumno en el **Excluir alumnos** campo.
1. Después de inscribir a los alumnos, haga clic en **[!UICONTROL Continuar]**. En el cuadro de diálogo Inscribir alumnos, puede ver el resumen de la inscripción.

   ![](assets/summary-of-enrollment.png)

   *Ver resumen de inscripción de cursos*

1. Para inscribir a todos los alumnos en el curso, haga clic en **[!UICONTROL Inscribir]**. Estos alumnos se han inscrito correctamente en este curso. Los alumnos recibirán una notificación para continuar y realizar el curso. Para inscribir a más alumnos, repita el procedimiento de inscripción.

## Cambios en la página Instancia del curso para los módulos de clase virtual de Connect {#connect-vc}

Al recuperar un curso de Connect, puede crear dos tipos de salas:

* Dinámico
* Persistente

Siempre se corrige una URL persistente. Sin embargo, para los usuarios que no tengan Connect y su propia sala de reuniones, deben utilizar una sala de reuniones dinámica en tiempo de ejecución. Las personas pueden unirse a su reunión.

![](assets/dynamic-room-options.png)

*Opciones dinámicas de sala de reuniones*

Ahora puede cambiar la dirección URL de la sala permanente en el **Instancia del curso** página.

<!--| ![](assets/persistentroomdropdown.png) | ![](assets/courseinstancepage-persistentroom.png) |
|---|---|-->

## Dar de baja a alumnos de un curso {#unenrolllearnersfromacourse}

Al crear un curso, un autor puede activar esta opción **Los alumnos pueden darse de baja ellos mismos**, para que los alumnos que realizan el curso puedan desinscribirse del curso.

Un administrador también puede dar de baja a los alumnos del curso.

![](assets/unenroll-learners.png)

*Dar de baja a alumnos de un curso*

Para obtener más información, consulte [Dar de baja alumnos](/help/migrated/administrators/feature-summary/courses.md).

## Añadir módulos de curso para Captivate y presentador {#addcoursemodulesforcaptivateandpresenter}

También puede publicar los módulos del curso en Learning Manager desde Adobe Captivate y Adobe Presenter mediante el menú Publicar.

1. En Captivate, haga clic en **[!UICONTROL Publicar]** > **[!UICONTROL Publicar en Learning Manager]**.
1. Indique el nombre del subdominio o el ID de correo electrónico y haga clic en **[!UICONTROL Enviar]**. Si tiene varias cuentas, se le pedirá que elija la cuenta.
1. Inicie sesión con las credenciales de Adobe. Si no tiene un ID de Adobe, haga clic en **[!UICONTROL Crear cuenta]**. Después de la autorización, se le dirigirá a la página de publicación del módulo.
1. Proporcione toda la información básica sobre el módulo y haga clic en Publicar.

Puede ver el módulo publicado en la página de módulos de Learning Manager. Para obtener más información, consulte [Publicación de proyectos en Adobe Learning Manager](https://helpx.adobe.com/captivate/classic/publish-project-to-captivate-prime.html).

## Eficacia del curso {#courseeffectiveness}

La puntuación de eficacia del curso ayuda a los autores a evaluar los cursos que no funcionan según las necesidades de los alumnos y a modificarlos en consecuencia. La eficacia del curso se evalúa para comprender la utilidad de un curso para el alumno. Se trata de una combinación de resultados de los comentarios de los alumnos sobre el contenido del curso. Los resultados de las pruebas del curso de un alumno y los comentarios del responsable que evalúan a un alumno en función del aprendizaje del curso.

En **Mis cursos**, un autor puede ver la clasificación de la eficacia del curso en las miniaturas de los cursos, como se muestra en la captura de pantalla siguiente. Puede ver la clasificación de este curso como 100.

<!--![](assets/course-rating.png)-->

El valor de valoración de la eficacia del curso se obtiene considerando los valores de comentarios de L1, L2 y L3. Para ver el desglose de cada comentario, haga clic en el valor de eficacia del curso. Aparece un menú emergente como se muestra a continuación.

![](assets/how-course-effectivenessiscalculated.png)

*Cálculo de la eficacia del curso*

En esta captura de pantalla de ejemplo, 1 de 1 usuario recibió los tres tipos de comentarios, de ahí que la puntuación sea 100/100. En esta tabla, puede comprender los comentarios que faltan para mejorar la eficacia general. Para ver cómo se calcula la eficacia del curso, haga clic en la flecha hacia abajo situada en la esquina inferior derecha del menú emergente.

<!--![](assets/how-course-effectivenessiscalculated1.png)-->

Según el gráfico circular mostrado anteriormente, se da más peso a los comentarios de L3 del gerente.

## Certificaciones y programas de aprendizaje {#certificationsandlearningprograms}

Tanto el autor como el administrador pueden crear certificaciones y programas de aprendizaje para los alumnos desde la aplicación de autor. En la página de inicio, haga clic en Certificaciones o Programas de aprendizaje para crear los objetos de aprendizaje respectivos.

Para obtener información sobre cómo crear y administrar certificaciones y programas de aprendizaje, consulte  [Certificaciones](/help/migrated/administrators/feature-summary/certifications.md) y  [Programas de aprendizaje](/help/migrated/administrators/feature-summary/learning-programs.md).

## Cursos obligatorios para certificación externa {#mandatorycoursesforexternalcertification}

En versiones anteriores de Learning Manager, la finalización del curso por parte del alumno en certificación externa no era obligatoria para completar un certificado.

Ahora puede hacer que los cursos sean obligatorios habilitando la opción **Definir los cursos requeridos como obligatorios para la finalización del certificado** en la ficha Programa.

![](assets/set-required-coursesasmandatory.png)

*Definir cursos obligatorios para completar un certificado*

Cuando los cursos se establecen como obligatorios:

* La página de envío del responsable muestra una lista de los alumnos solo después de que estos hayan completado los cursos.
* El alumno solo puede cargar un archivo después de completar el curso.

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++Cómo eliminar la opción Buscar nominación de responsable para un curso

Realice los siguientes pasos:

1. Inicie sesión en Learning Manager como autor.
1. Abra el curso.
1. En el panel izquierdo, haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Editar]**.
1. En la **Tipo de inscripción** lista desplegable, cambiar el tipo de inscripción de **Nominado como responsable** para **Aprobado por responsable** o **Inscripción automática**.

1. Cuando haya cambiado el tipo de inscripción, vuelva a publicar el curso.

+++

+++¿Cómo combinar cursos?

Puede combinar cursos mediante un programa de aprendizaje.

1. Inicie sesión en Learning Manager como administrador.
1. En el panel izquierdo, haga clic en **[!UICONTROL Programas de aprendizaje]**.
1. Para añadir un programa de aprendizaje, haga clic en **[!UICONTROL Añadir]**.
1. Introduzca los detalles del programa de aprendizaje. Para guardarlo, haga clic en **[!UICONTROL Guardar]**.
1. Después de crear el programa de aprendizaje, haga clic en **[!UICONTROL Catálogo]**.
1. En una tarjeta de curso, haga clic en **[!UICONTROL Añadir]**, como se muestra a continuación. Repita el proceso para todos los cursos que desee añadir al programa de aprendizaje.

![](assets/add-catalog.png)

Una vez que haya añadido todos los cursos requeridos en el programa de aprendizaje, haga clic en **[!UICONTROL Publicar]**.

En un programa de aprendizaje, solo puede añadir cursos de inscripción automática, no cursos con nominación de responsable o aprobados por responsable. Este es un comportamiento predeterminado en Learning Manager.

+++

+++Cómo asegurarse de que todos los alumnos no puedan ver todos los cursos

Para ello, puede utilizar catálogos. Un catálogo predeterminado contiene todos los cursos añadidos a Learning Manager de forma predeterminada.

Debe desactivar el catálogo predeterminado y crear catálogos personalizados.

1. Inicie sesión en Learning Manager como administrador.
1. En el panel izquierdo, haga clic en **[!UICONTROL Catálogos]**.
1. Cree un catálogo haciendo clic en **[!UICONTROL Crear]**. Introduzca los detalles y haga clic en **[!UICONTROL Guardar]**.

1. En las opciones de Catálogo recién creadas, puede seleccionar diferentes tipos de aprendizaje que puede añadir, por ejemplo, programa de aprendizaje, certificación o curso.
1. En la sección Programa de aprendizaje, haga clic en **[!UICONTROL Añadir contenido]**.
1. En el panel izquierdo, haga clic en **[!UICONTROL Compartir internamente]** o **[!UICONTROL Compartir externamente]** dependiendo de la audiencia a la que quieras dirigirte.

1. Para añadir un grupo de usuarios, haga clic en **[!UICONTROL Añadir grupos de usuarios]**.
1. En la página Catálogos, desactive la **D[!UICONTROL Catálogo predeterminado]** y active el catálogo que ha creado.

![](assets/enable-custom-catalog.png)

+++

+++Cómo volver a inscribirse en un curso completado

La finalización de un curso no se puede revertir. Un alumno **no se puede volver a inscribir** a un curso completado.

+++

+++¿Cómo pueden ver los alumnos el curso aunque lo hayan completado?

Un alumno puede ver un curso después de completarlo haciendo clic en el botón Regresar del curso.

Siga estos pasos:

1. Inicie sesión como alumno.
1. Abra el curso que ha completado.
1. Haga clic en **[!UICONTROL Regresar]**.

+++

+++Cómo añadir un archivo de recursos en el curso?

Al crear un curso, puede añadir archivos de vídeo, audio, PDF o texto al curso que sean relevantes para el curso para que el alumno pueda acceder a material de formación adicional.

![](assets/add-resources.png)

+++

+++Cómo definir varios intentos en el módulo?

**Requisito previo:** El administrador debe activar la opción **Varios intentos** en **Configuración > General** en la aplicación de administración.

Como autor, en la página Resumen del curso, active la opción **Permitir varios intentos**.

Para obtener más información, consulte la [sección sobre varios intentos](courses.md#Allowmultipleattempts).

+++

+++¿Puede descargar el contenido que se ha cargado en Adobe Learning Manager para modificarlo?

No, el contenido cargado en Learning Manager es un archivo zip publicado y no es el archivo de origen. Por lo tanto, aunque se descargue el contenido, este no se puede editar en una herramienta de creación. Es necesario un archivo de origen para editar el contenido.

+++

