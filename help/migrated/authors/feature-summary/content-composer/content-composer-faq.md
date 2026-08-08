---
description: Encuentre respuestas a las preguntas más comunes del compositor de contenido, como por qué Generar contorno está atenuado, cómo cambiar el nombre de una lección, por qué las preguntas de las pruebas no están alineadas correctamente y qué hacer cuando Publish está desactivado.
jcr-language: en_us
title: Preguntas frecuentes sobre Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '584'
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
