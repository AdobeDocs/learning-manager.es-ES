---
description: El Asistente de inteligencia artificial (Beta) para alumnos es un complemento de chat potenciado por GenAI en Adobe Learning Manager que ayuda a los alumnos a obtener respuestas rápidas y precisas a partir del contenido de aprendizaje asignado. Mediante el uso de consultas de lenguaje natural, los alumnos pueden recuperar instantáneamente respuestas centradas con citas claras, lo que facilita encontrar la información correcta, verificar las fuentes y aprender de manera eficaz sin buscar en cursos enteros.
jcr-language: en_us
title: Asistente de inteligencia artificial para alumnos de Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 64765bdd9f364267f7c7f5d23a03cc576b875be3
workflow-type: tm+mt
source-wordcount: '2008'
ht-degree: 0%

---

# Asistente de IA para los alumnos

El Asistente de inteligencia artificial (Beta) para alumnos les ayuda a encontrar rápidamente respuestas del contenido de aprendizaje asignado sin tener que explorar cursos completos. Puede hacer preguntas en un lenguaje sencillo y recibir respuestas precisas y centradas con vínculos de origen al contenido relevante del curso.

>[!IMPORTANT]
>
>El Asistente de inteligencia artificial para alumnos está disponible actualmente como función beta. Las capacidades, los escenarios compatibles y las limitaciones pueden cambiar a medida que evoluciona la función.


## ¿Qué es el Asistente de IA para alumnos?

El asistente de inteligencia artificial es un compañero de chat con tecnología GenAI en Adobe Learning Manager que ofrece respuestas rápidas y precisas a las preguntas de los alumnos mediante el contenido de aprendizaje de confianza disponible para ellos en Adobe Learning Manager. También incluye citas, por lo que los alumnos siempre conocen la fuente de la información.

### Capacidades clave del Asistente de inteligencia artificial

1. Respuesta inteligente a preguntas
   * Conversaciones de una vuelta y varias vueltas
   * Comprensión del lenguaje natural en inglés
   * Respuestas derivadas de cursos, certificaciones, rutas de aprendizaje y ayudas de trabajo
   * Aclaración inteligente de preguntas cuando las consultas son ambiguas
   * Con funciones de LLM de IA abierta de Azure para generar respuestas
2. Fuentes de contenido y citas
   * Recupera respuestas de los recursos disponibles presentes en los catálogos admitidos.
   * Proporciona citas con vínculos directos a materiales de origen
   * Compatible con todos los formatos de contenido ALM estáticos e interactivos: PDF, DOCX, PPTX, XLSX, Audio (mp3, wav, m4a), Vídeo (mp4, mov, wmv), HTML, SCORM 2004, SCORM 1.2
3. Experiencia de usuario
   * Interfaz del panel lateral accesible desde todas las páginas del alumno
   * Diseño interactivo que se adapta al área de contenido
   * Historial de chat mantenido en la sesión del navegador
   * Limpiar pizarra en nuevo inicio de sesión o actualización de página
   * Tono del profesor o tutor: amable, claro y pedagógicamente sólido
4. Controles del administrador
   * Habilitar o deshabilitar la función en el nivel de cuenta
   * Controlar el acceso de los grupos de usuarios
   * Seleccionar los catálogos que se incluyen para las respuestas de AI
   * Requisito de aceptación de las Condiciones de uso para seguir las directrices de IA de Adobe

## Qué tipos de contenido admite el Asistente de inteligencia artificial

El Asistente de inteligencia artificial recupera información del contenido de aprendizaje asignado a usted, que incluye:

* **Documentos:** PDF, Word, PowerPoint, Excel, HTML
* **Medios:** audio (mp3, wav, m4a), vídeo (mp4, mov, wmv)
* **Contenido interactivo:** SCORM 1.2, SCORM 2004
* **Tipos de objetos de aprendizaje:** cursos, rutas de aprendizaje, certificaciones, ayudas de trabajo

Adobe transcribe de forma segura el contenido de aprendizaje mediante servicios de procesamiento de terceros de confianza alojados en el entorno VPC privado de Adobe.

### Limitaciones de catálogos y fuentes de contenido

El Asistente de inteligencia artificial del alumno solo utiliza contenido de **catálogos internos** configurados explícitamente por los administradores.

Los siguientes orígenes de contenido **no son compatibles** en la versión actual:

* Catálogos compartidos
* Catálogos adquiridos
* Catálogos externos
* Catálogos predeterminados
* Bibliotecas de contenido de terceros (por ejemplo, LinkedIn Learning o Go1)

Si un alumno no tiene acceso a un curso o una ayuda de trabajo, el Asistente de inteligencia artificial no mostrará la información de ese contenido y no se podrá acceder a los vínculos de citas.

## Casos prácticos de AI Assistant

### Alumno técnico

Sarah es ingeniera de ventas que está aprendiendo sobre tarjetas gráficas. Necesita entender rápidamente las especificaciones técnicas y las ventajas para responder con confianza a las preguntas de los clientes.

El asistente de inteligencia artificial ayuda a Sarah con lo siguiente:

* Explicación técnica clara de la compleja arquitectura de GPU
* Profundizar en el conocimiento de varias tarjetas gráficas y sus diferencias
* Explicación de los ejemplos para que Sarah pueda relacionar las funciones con casos prácticos del mundo real

### Asistencia al cliente

Marcus es un especialista de soporte en una empresa asociada. Necesita respuestas rápidas sobre las funciones de los productos para ayudar a los clientes sin pasar a los equipos de ingeniería.

El asistente de inteligencia artificial ayuda a Marcus con lo siguiente:

* Encontrar contenido de asistencia relevante para las consultas frecuentes de los clientes
* Hacer preguntas aclaratorias cuando la respuesta inicial no es lo suficientemente específica
* Encontrar recomendaciones para cursos de solución de problemas relacionados para mejorar sus habilidades

### Incorporación de nuevos empleados

Jennifer acaba de unirse a la compañía y se siente abrumada por la cantidad de material de entrenamiento. Necesita una forma de encontrar información específica sin revisar cursos enteros.

El asistente de inteligencia artificial ayuda a Jennifer con lo siguiente:

* Obtención de una guía paso a paso sobre el envío de informes de gastos
* Descubrimiento de cursos sobre las políticas de la empresa sin examinar todo el catálogo
* Guiándola a la sección apropiada de un curso sin hacerla ver horas de video

## ¿Cómo utiliza el Asistente de inteligencia artificial el contenido?

El Asistente de inteligencia artificial le ayuda a encontrar respuestas precisas rápidamente mientras aprende. Para utilizarlo de manera eficaz, debe comprender qué contenido utiliza el asistente, qué no utiliza y cómo genera respuestas.

### ¿Qué contenido utiliza el Asistente de inteligencia artificial?

El Asistente de inteligencia artificial responde a las preguntas utilizando únicamente el contenido de aprendizaje activado por el administrador de la cuenta. El contenido del catálogo se indiza.

El asistente de inteligencia artificial analiza el contenido de aprendizaje asignado para generar respuestas específicas y contextuales.

* Cada respuesta incluye citas que hacen referencia al contenido original.
* Puede seleccionar una cita para ir directamente al curso, módulo o documento correspondiente.
* Las citas le ayudan a verificar la información y explorar el contexto adicional cuando sea necesario.

### Respuestas de transmisión

Una respuesta de transmisión por secuencias significa que el Asistente de inteligencia artificial proporciona la respuesta progresivamente a medida que se genera, de modo que los usuarios pueden empezar a leer la respuesta inmediatamente sin esperar a que finalice la carga.

### Citas y transparencia de la fuente

Cada respuesta del asistente de inteligencia artificial incluye citas que se vinculan directamente al curso, módulo u objeto de aprendizaje original. Las citas le permiten:

* Seleccione un número de cita en línea para saltar a la sección de referencia exacta
* Abra la lista de fuentes completa seleccionando Mostrar fuentes en la parte inferior de la respuesta
* Verificar la información y explorar el contexto adicional de la fuente autorizada

>[!IMPORTANT]
>
>El Asistente de inteligencia artificial proporciona respuestas basadas en el contenido habilitado por el administrador, pero si un usuario carece de acceso a un elemento al que se hace referencia, verá un mensaje de error de no admitido al abrirlo.


## Mensajes incorporados

El asistente de inteligencia artificial incluye indicaciones integradas para ayudar a los alumnos a empezar rápidamente con preguntas y situaciones habituales. Estos mensajes guían a los alumnos sobre cómo interactuar con el asistente y muestran los tipos de preguntas que pueden hacer.

![Mensajes incorporados proporcionados por el Asistente del alumno](assets/built-in-prompt-new.png)

Los mensajes incorporados se pueden personalizar por cuenta. Las organizaciones pueden adaptarlos para reflejar sus objetivos de aprendizaje, las funciones de los alumnos, la terminología o casos prácticos específicos. Los administradores pueden trabajar con su administrador de éxito de clientes (CSM) para configurar o actualizar las solicitudes integradas.

La personalización de solicitudes se gestiona en el nivel de cuenta y no se puede configurar directamente en la interfaz de usuario de Adobe Learning Manager en la versión actual.

## Configuración de administrador: Activar el Asistente de IA para alumnos

![Asistente para alumnos con IA](assets/learner-ai-assistant-new.png)

Los administradores seleccionan qué grupos de usuarios y catálogos internos pueden acceder a la función Asistente de IA. Deben asegurarse de que los catálogos asignados incluyan solo el contenido de aprendizaje que sea adecuado para aparecer en las respuestas y citas de IA, y de que dichos catálogos sean predeterminados, internos, no compartidos, adquiridos o externos.

Antes de configurar el asistente de IA, confirme que tiene credenciales de administrador y que ha identificado qué grupos de usuarios y catálogos deben tener acceso a la función.

### Configuración del acceso al asistente de IA

Para habilitar el asistente de inteligencia artificial aplicada al alumno:

1. Inicie sesión en Adobe Learning Manager como administrador.

2. Seleccione **Configuración** de la página principal.
   ![Consola de administrador con la opción Configuración en el panel izquierdo](assets/settings-menu.png)

3. Seleccione **Asistente de IA del alumno (Beta)** en el menú **Configuración**.
   ![La consola de administrador muestra la opción Asistente de inteligencia artificial aplicada al alumno en el panel izquierdo](assets/learner-assistant-ai-beta.png)

4. Seleccione el conmutador a fin de habilitar el **Asistente de IA del alumno (Beta)**.
   ![La consola de administradores muestra la opción habilitada para el asistente de IA del alumno](assets/learner-assistant-toggle.png)

5. Seleccione uno o más grupos de usuarios de la opción **Grupos de usuarios aptos**.

6. Seleccione **Guardar** para aplicar la configuración del grupo de usuarios.

7. Seleccione uno o más catálogos de la opción **Catálogos aptos**.

8. Seleccione **Guardar** para aplicar la configuración del catálogo.

>[!IMPORTANT]
>
>El asistente de IA solo admite catálogos internos. Si se selecciona un catálogo compartido, adquirido, externo u otro catálogo no interno, el asistente de IA no mostrará su contenido, aunque el catálogo aparezca en la lista Catálogos aptos.

## Guía del alumno: inicio del asistente de IA

### Inicio del asistente de IA

Para iniciar el asistente de IA:

1. Inicie sesión en Adobe Learning Manager como alumno.

2. Seleccione **Preguntar al asistente de IA** en la página de inicio.
   ![Se muestra la página de inicio del alumno. Solicite al asistente de IA que seleccione y abra el panel del asistente de IA del alumno](assets/ask-ai-assistant.png)

3. Cuando aparezca la pantalla **Asistente de IA del alumno**, seleccione **Introducción**.
   ![Seleccione Comenzar para iniciar el Asistente para alumnos](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Al iniciar el asistente de IA por primera vez, debe proporcionar su consentimiento antes de utilizarlo. El cuadro de diálogo de consentimiento solo aparecerá durante este inicio inicial. Para todos los inicios posteriores, se le dirigirá directamente al Asistente de inteligencia artificial para introducir sus indicaciones.

&#x200B;4. Escriba el mensaje en el campo de texto.

![Escribir mensaje en el Asistente del alumno](assets/type-prompt-new.png)

&#x200B;5. Pulse **Intro** para recibir una respuesta. Revisar la respuesta, las fuentes y las recomendaciones.

Puede realizar lo siguiente:

* Seleccione el número de cita en línea para ir directamente a la sección de referencia exacta
* Abra la lista completa de orígenes seleccionando **Mostrar orígenes** en la parte inferior de la respuesta

![Mostrar orígenes en la respuesta](assets/show-sources-latest.png)

El asistente de inteligencia artificial incluye citas con cada respuesta para mostrar de dónde procede la información. Cada cita se vincula directamente al curso, módulo u objeto de aprendizaje original utilizado para generar la respuesta.

Puede seleccionar cualquier cita para abrir la página del curso real en Adobe Learning Manager y revisar todo el contenido en contexto. Las citas le ayudan a verificar la información, explorar detalles adicionales y seguir aprendiendo de la fuente autorizada.

## Acceder al Asistente de inteligencia artificial mediante la búsqueda

También puede iniciar el Asistente de inteligencia artificial directamente desde la barra de búsqueda. Escriba su pregunta en el campo de búsqueda y, a continuación, seleccione **Preguntar al asistente de inteligencia artificial** en las opciones que aparecen para obtener respuestas del contenido de aprendizaje asignado. El contenido de aprendizaje asignado.

![Acceder al Asistente del alumno desde la barra de búsqueda](assets/learner-assistant-search-new.png)


## Proporcionar comentarios sobre las respuestas del Asistente de inteligencia artificial del alumno

Sus comentarios sobre las respuestas generadas por el Asistente de inteligencia artificial del alumno (Beta) ayudan a mejorar su precisión, relevancia y rendimiento general.

### Indicar si una respuesta le gusta o no

* Selecciona **Pulgares arriba**, elige lo que te haya parecido útil en la respuesta, agrega comentarios de manera opcional y luego selecciona **Enviar**.

![Seleccionar Pulgares hacia arriba para votar a favor de una respuesta](assets/la-feedback.png)

* Selecciona **Pulgares abajo**, elige la razón por la que la respuesta no fue útil, añade comentarios y luego selecciona **Enviar**.

## Iniciar una nueva conversación en el Asistente para inteligencia artificial

Iniciar un nuevo chat permite al usuario iniciar una nueva conversación, borrando el contexto anterior para que el asistente pueda centrarse en el nuevo tema sin hacer referencia a interacciones anteriores. Esto es importante al cambiar de tema o buscar respuestas que no estén relacionadas con preguntas anteriores.

Borrar la conversación actual e iniciar una nueva conversación en cualquier momento.

Seleccione **Nuevo chat** en la pantalla del Asistente de inteligencia artificial y, a continuación, seleccione **Sí**.

![Iniciar una nueva conversación en el Asistente del alumno](assets/start-new-chat.png)

El asistente de inteligencia artificial proporciona a los alumnos respuestas rápidas y contextuales, admite varios tipos de contenido y ofrece citas en línea para la transparencia. Los administradores pueden controlar el acceso, lo que garantiza que el asistente de inteligencia artificial se adapte a las necesidades de la organización y mejore la experiencia de aprendizaje.


## Resolución de problemas

>[!NOTE]
>
>Después de configurar un nuevo catálogo, espere entre 4 y 5 horas para que el contenido se indexe y esté disponible para las respuestas del Asistente de inteligencia artificial.

### Escenario 1: sin acceso al contenido

Problema: el alumno tiene acceso al Asistente del alumno, pero recibe las respuestas &quot;No tengo respuesta a esta pregunta&quot;.

**Posibles causas**

* Los catálogos del alumno no se incluyen al configurar el Asistente para inteligencia artificial
* El contenido relacionado con la pregunta no está en los catálogos seleccionados o los catálogos están en blanco
* El alumno no tiene visibilidad del contenido relevante

**Solución**

* Comprobar el acceso al catálogo del alumno
* Comprobar qué catálogos están activados en la configuración del Asistente del alumno
* Asegurarse de que haya contenido relevante en esos catálogos
* Espere unas horas después de agregar contenido nuevo para que se indexe

### Caso 2: Respuestas irrelevantes o de mala calidad

**Problema**: el Asistente para inteligencia artificial proporciona respuestas que no coinciden con la pregunta o son de baja calidad.

**Posibles causas**

* La pregunta es demasiado amplia o ambigua
* El contenido relevante tiene metadatos deficientes (descripciones, etiquetas)
* La estructura del contenido dificulta la extracción de información

**Solución**

* Anima a los alumnos a hacer preguntas más específicas
* Revisar y mejorar descripciones y metadatos de cursos
* Asegúrate de que el contenido tiene encabezados y estructura claros
* Revise el informe de uso detallado para identificar patrones
* Considerar la creación de ayudas de trabajo para las preguntas frecuentes

### Escenario 3: preguntas fuera del ámbito

**Problema**: el alumno hace preguntas no relacionadas con el contenido de formación.

**Ejemplos**:

* Preguntas de conocimiento general (&#39;¿Quién es el presidente?&#39;)
* Opiniones personales (&#39;¿Qué piensas de X?&#39;)
* Contenido inapropiado
