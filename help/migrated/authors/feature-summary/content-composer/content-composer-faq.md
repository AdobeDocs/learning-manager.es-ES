---
description: Encuentre respuestas a preguntas comunes del compositor de contenido sobre la edición de contornos, el comportamiento de las pruebas, la compatibilidad con Captivate, la publicación y Compartir para revisión.
jcr-language: en_us
title: Preguntas frecuentes sobre Adobe Learning Manager Content Composer
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 0%

---


# Preguntas frecuentes sobre Adobe Learning Manager Content Composer

Obtenga respuestas a preguntas frecuentes sobre el uso del compositor de contenido.

**El botón Generar contorno está atenuado. ¿Qué debo hacer?**

Los tres campos **Brief**, **Title**, **Learners** y **Objective** deben contener contenido antes de que se active **Generate Outline**. Busque en el lienzo cualquier campo que siga mostrando texto de marcador de posición en cursiva, como *Escriba el perfil del alumno aquí* o *Introduzca el objetivo de este curso*. Rellene el campo vacío y el botón se activará inmediatamente.

**No puedo seleccionar el esquema para cambiar el nombre de una lección. ¿Por qué?**

La edición de contornos es una tarea conversacional en la versión beta actual. No se puede seleccionar una lección o tema en el lienzo para cambiarle el nombre o reordenarlo. Escriba el cambio en un idioma sencillo en el panel de chat del asistente.

Ejemplos:

- &quot;Cambiar el nombre de la Lección 1 a &#39;Cómo funciona la suplantación de identidad&#39;&quot;

- &quot;Traslade el tema 1.3 para que sea el primer tema de la Lección 2&quot;

- &quot;Eliminar la Lección 4 y distribuir sus temas en la Lección 3&quot;

**El esquema generado no coincide con lo que yo quería. ¿Qué ha fallado?**

El esquema refleja el mensaje y el resumen. Si la estructura no funciona, las causas más comunes son un mensaje que abarca demasiados temas a la vez o un objetivo de aprendizaje que no menciona las aptitudes o comportamientos específicos que debe desarrollar el curso.

**La IA omitió una sección importante de mi archivo cargado. ¿Cómo puedo solucionar esto?**

El compositor de contenido prioriza las secciones del archivo de origen que sean más relevantes para el objetivo de aprendizaje. Si se omitió una sección, es probable que no se reflejara en el objetivo.

Para solucionar este problema:

1. Vuelva al panel **Brief** y actualice el objetivo para asignar un nombre explícito al tema que falta.

2. Pida al ayudante que vuelva a generar el contorno: &quot;Vuelva a generar el esquema, asegurándose de incluir la sección de política de retención de datos&quot;.

También puede agregar manualmente el contenido que falta como un nuevo tema en la conversación de esquema: &quot;Agregue un nuevo tema a la Lección 2 denominado &#39;Política de retención de datos&#39;.&quot;

**¿Puedo usar Compositor de contenido con Adobe Captivate?**

No. Content Composer y Adobe Captivate no comparten un flujo de trabajo de ida y vuelta. No puede abrir proyectos de Compositor de contenido en Captivate ni proyectos de Captivate en Compositor de contenido.

Un archivo MP4 exportado por el Captivate se puede insertar como un componente **Video** en Content Composer.

**¿Puedo usar el compositor de contenido para el cumplimiento o la formación regulada?**

Sí. Este es uno de sus casos más fuertes. Cargue los documentos de su política o procedimiento en Administrar archivos de origen y seleccione Restringir la salida al contenido de los archivos para que la IA se genere únicamente a partir de lo que ha proporcionado, en lugar de complementarlo con conocimientos generales.

**¿Por qué no se califican las comprobaciones de conocimiento?**

Las comprobaciones de conocimientos de Compositor de contenido están diseñadas para reforzar el aprendizaje durante una lección, no para puntuar. Proporcionan comentarios inmediatos al alumno, pero no producen un registro de nota o finalización.

Solo se califican las evaluaciones de las pruebas de fin de lección. Si necesita una evaluación que contribuya a la puntuación de un alumno, utilice la prueba, no un componente de comprobación de conocimientos.

**Las preguntas del cuestionario no coinciden con lo que enseña el curso. ¿Cómo puedo solucionar esto?**

El compositor de contenido utiliza IA para generar preguntas de cuestionario y la salida de IA no es determinista. Es posible que las preguntas no siempre reflejen exactamente lo que espera. Revise todas las preguntas de la prueba después de generar el curso, edite las que necesite ajustar directamente en el editor del curso y verifique que el contenido sea preciso antes de la publicación.

## Acerca de Compartir para revisión

**¿Qué es Compartir para revisión en el compositor de contenido?**

Compartir para revisión le permite distribuir un curso a los revisores para que formulen comentarios antes de publicarlo. Los revisores pueden abrir el curso en un navegador, añadir comentarios en cualquier componente e intentar realizar la prueba sin tener que instalar Content Composer o una suscripción.

**¿Necesitan los revisores una licencia de Content Composer?**

No. Los revisores no necesitan una suscripción o instalación de Content Composer. Cualquier persona que tenga el vínculo de revisión puede abrir el curso en su navegador.

**¿Necesitan los revisores un Adobe ID para participar?**

Sí. La revisión de un curso requiere el inicio de sesión, por lo que se requiere un Adobe ID para participar. Una vez que hayan iniciado sesión, los revisores pueden abrir el curso, añadir comentarios, intentar realizar la prueba y utilizar @menciones para etiquetar al autor o a otros revisores.

**¿Pueden los revisores editar el contenido del curso?**

No. El acceso de revisión es solo para comentarios. Los revisores pueden añadir comentarios, responder a ellos, resolverlos y filtrarlos, pero no pueden cambiar el texto, las imágenes ni la estructura del curso.

¿Dónde se almacenan los archivos de revisión? Los archivos de revisión se alojan en la nube de Adobe. Los autores no necesitan administrar el almacenamiento de archivos ni enviar los archivos del curso directamente a los revisores.

### Uso compartido y acceso

**¿Quién puede tener acceso a un vínculo de revisión?**

De forma predeterminada, solo las personas que invite por nombre o correo electrónico pueden acceder al proyecto. Verifique esto en la sección Quién tiene acceso del panel Compartir proyecto antes de enviar el vínculo.

**¿Puedo invitar a responsables externos que no sean usuarios de Adobe?**

Sí, puede invitar a cualquier persona por correo electrónico. Sin embargo, necesitan una cuenta de Adobe para iniciar sesión y revisar el curso.

**¿Puedo agregar revisores después de que la revisión ya haya comenzado?**

Sí. Abra el panel Compartir proyecto en cualquier momento, añada nombres o direcciones de correo electrónico y seleccione Invitar a comentarios. Los nuevos revisores recibirán una invitación inmediatamente.

**¿Puedo quitar un revisor después de compartir?**

Sí. En el panel Compartir proyecto, busque el revisor en ¿Quién tiene acceso? y elimínelo. Si intentan abrir el curso mediante un vínculo compartido anteriormente, verán un mensaje de acceso denegado.

**¿Qué sucede si un revisor pierde el acceso?**

Pueden seleccionar Solicitar acceso en la pantalla de acceso denegado. El propietario del curso recibe una notificación para restaurar el acceso.

### Comentarios y sugerencias

¿Pueden los revisores comentar sobre una parte específica del curso?

Sí. Los revisores seleccionan cualquier componente del curso (un bloque de texto, una imagen o una pregunta de prueba) y añaden un comentario directamente en ese elemento. Los comentarios permanecen contextualmente vinculados al componente en el que se agregaron.

**¿Pueden varios revisores comentar al mismo tiempo?**

Sí. Todos los revisores pueden ver los comentarios de los demás en el panel Comentarios y pueden responder, resolver o @mencionarse entre sí.

**¿Puedo filtrar comentarios para encontrar comentarios no resueltos?**

Sí. Utilice el filtro Resuelto del panel Comentarios para mostrar solo los comentarios no resueltos. También puede filtrar por Revisores para ver los comentarios de una persona específica, o por Tiempo para encontrar los comentarios más recientes.

**¿Cómo puedo etiquetar a otro revisor en un comentario?**

Escriba @ seguido del nombre o la dirección de correo electrónico y selecciónelos en el menú desplegable. Los usuarios etiquetados reciben una notificación. Para ello, es necesario que el revisor inicie sesión con un Adobe ID.

#### Prueba y acceso de alumno

**¿Pueden los revisores intentar la prueba?**

Sí. Los revisores pueden intentar realizar la prueba hasta el número de reintentos especificado. Sus puntuaciones no se registran y no afectan al curso ni a ningún informe del LMS.

**¿Cuál es la diferencia entre compartir para revisión y compartir para alumnos?**

Compartir para revisión concede acceso al curso con el panel de comentarios activado, destinado a los compañeros y partes interesadas que proporcionan comentarios. Compartir para alumnos da acceso al curso sin comentarios, dirigido a alumnos que no se han inscrito a través de un LMS. Las puntuaciones de los alumnos tampoco se registran mediante un vínculo directo.

### Actualización y cierre de una revisión

**¿Tengo que crear una nueva revisión después de realizar cambios?**

No. La URL de revisión permanece igual después de actualizar el curso. Seleccione **Compartir** para notificar a los revisores que hay una versión actualizada disponible.

**¿Se notificará a los revisores cuando actualice el curso?**
Los revisores ven un banner de notificación cuando abren el vínculo de revisión después de una actualización. Pueden seleccionar Volver a cargar para ver la última versión.

**¿Permanecen los comentarios antiguos después de actualizar un curso?**

Sí. Los comentarios existentes persisten entre las actualizaciones. Los revisores y los autores pueden seguir resolviendo los comentarios de la versión actualizada.

**¿Qué sucede con un vínculo de alumno después de actualizar el curso?**

El vínculo existente del alumno sigue mostrando la versión anterior. Genera un nuevo vínculo después de cada actualización y compártelo con los alumnos para garantizar que acceden al contenido más reciente.

**Cómo ver las actualizaciones de los proyectos?**

Si el autor actualiza el curso mientras lo está revisando, se muestra una notificación.

![](../assets/68_newer_version_available_reload_notification.png)

- Seleccione **Recargar** para cargar la última versión o descarte la notificación para continuar revisando la versión actual. La recarga es segura: tus comentarios existentes persisten incluso después de actualizar el proyecto, por lo que no perderás ningún comentario que ya hayas añadido.

## Intentar la prueba como revisor

Como revisor, puede intentar realizar la prueba hasta el número de veces especificado, pero las puntuaciones no se registran.

- Seleccione **INICIAR PRUEBA** para intentar la prueba.

  ![](../assets/66_final_quiz_start_screen_attempts_info.png)

- Al finalizar, se muestran los resultados. Desde aquí, puede seleccionar Revisar respuestas para ver qué preguntas aciertan o se equivoquen, o Repetir prueba para volver a intentarlo.

  ![](../assets/67_quiz_results_attempts_remaining_reviewer.png)




