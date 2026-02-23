---
description: Learner AI Assistant (Beta) es un complemento de chat basado en GenAI en Adobe Learning Manager que ayuda a los alumnos a obtener respuestas rápidas y precisas a partir del contenido de aprendizaje asignado. Mediante el uso de consultas de lenguaje natural, los alumnos pueden recuperar instantáneamente respuestas centradas con citas claras, lo que facilita encontrar la información correcta, verificar las fuentes y aprender de manera eficaz sin buscar en cursos enteros.
jcr-language: en_us
title: Asistente de inteligencia artificial del alumno (beta) en Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 0ef69eb5d95c4203a80cd5b4874b99855ebedcc4
workflow-type: tm+mt
source-wordcount: '2146'
ht-degree: 0%

---

# Introducción

El Asistente de inteligencia artificial (Beta) para alumnos les ayuda a encontrar rápidamente respuestas del contenido de aprendizaje asignado sin tener que explorar cursos completos. Puede hacer preguntas en un lenguaje sencillo y recibir respuestas precisas y centradas con vínculos de origen al contenido relevante del curso.

>[!IMPORTANT]
>
>El Asistente de inteligencia artificial para alumnos está actualmente en fase beta y se está lanzando en una implementación gradual. El acceso puede variar según el usuario.


## ¿Qué es el Asistente de IA?

AI Assistant es un compañero de chat basado en GenAI en Adobe Learning Manager que ofrece respuestas rápidas y precisas a las preguntas de los alumnos mediante el contenido de aprendizaje de confianza disponible para ellos en Adobe Learning Manager. También incluye citas, por lo que los alumnos siempre conocen la fuente de la información.

## ¿Por qué usarla?

* Los alumnos se enfrentan a una sobrecarga de contenido y, a menudo, no saben por dónde empezar ni qué recurso utilizar.

* El catálogo y las reglas de acceso dificultan descubrir qué contenido están disponibles para ellos.

* Los recorridos de aprendizaje están fragmentados en varios formatos y tipos de formación, como cursos, clases virtuales, ayudas de trabajo y evaluaciones.

* No existe una forma fácil y unificada de recuperar información específica de diversos formatos como SCORM, PDF, documentos, vídeos o transcripciones.

* Las diferentes funciones y sectores de los alumnos (p. ej., ventas, marketing, asistencia técnica, operaciones) tienen necesidades de información únicas que requieren respuestas rápidas y contextuales.

## ¿Qué tipos de contenido puede transcribir el Asistente de inteligencia artificial?

El asistente de inteligencia artificial puede encontrar información de todos los tipos de contenido de aprendizaje que tenga asignados, incluidos:

* **Documentos:** PDF, Word, PowerPoint, Excel, HTML

* **Medios:** audio (mp3, wav, m4a), vídeo (mp4, mov, wmv)

* **Contenido interactivo:** SCORM 1.2, SCORM 2004,

* **Tipo de objeto de aprendizaje:** cursos, rutas de aprendizaje, certificaciones, ayudas de trabajo

Adobe transcribe de forma segura su contenido de aprendizaje mediante servicios de procesamiento de terceros de confianza alojados en el entorno VPC privado de Adobe.

**IMPORTANTE**

El Asistente de inteligencia artificial solo consume contenido que:

* Disponible en los catálogos configurados para el Asistente del alumno por administradores y

* Parte de los catálogos internos de Adobe Learning Manager.

Los catálogos compartidos, adquiridos, externos u otros que no sean internos no se admiten como orígenes de contenido para el Asistente de inteligencia artificial en la versión actual.

Si no tiene acceso a un curso, no podrá acceder a los vínculos de citas relacionados. Las bibliotecas de terceros (como LinkedIn Learning o Go1) no se incluyen para recuperar respuestas.

## Capacidades de conversación

El Asistente de inteligencia artificial admite preguntas únicas y conversaciones de varias vueltas. Recuerda sus consultas anteriores dentro de la misma sesión.

**Ejemplo de conversación:**

Usted: &quot;¿Cuál es la política de reembolso?&quot;
Ayudante: Proporciona resumen
Usted: &quot;¿Y los reembolsos después de 30 días?&quot;
Ayudante: Devuelve información más específica

## Casos prácticos de AI Assistant

### Asistencia para el aprendizaje Just-in-time (todos los alumnos)

Los alumnos suelen necesitar respuestas rápidas al trabajar, no reproducciones de cursos completos. El asistente de inteligencia artificial permite la recuperación instantánea de información precisa del contenido de aprendizaje asignado.

**En qué ayuda:**

* Obtenga respuestas directas a preguntas específicas de cursos, ayudas de trabajo y documentos

* Ir a secciones de referencia exactas mediante citas

* Reducir el tiempo dedicado a la búsqueda en varios objetos de aprendizaje

![Asistencia para el aprendizaje Just-in-time con el Asistente del alumno](assets/just-in-time.png)

### Capacitación de ventas y conversaciones con los clientes

Los equipos de ventas necesitan información rápida y precisa sobre los productos y procesos durante las interacciones con los clientes en directo. El asistente de inteligencia artificial actúa como un compañero de conocimientos bajo demanda.

**En qué ayuda:**

* Recuperar las funciones y la posición actualizadas del producto

* Genera scripts de ventas o puntos de discusión rápidos a partir del contenido de formación

* Comparar versiones u ofertas de productos mediante material de aprendizaje asignado

* Refuerza el conocimiento de ventas sin volver a realizar cursos completos

![Habilitación de ventas mediante el Asistente del alumno](assets/sales-enablement.png)

**Ejemplo 2**

**Propósito:** Demostrar que el Asistente de IA puede ayudar a los representantes de ventas a responder preguntas de comparación de clientes al instante.

**Mensaje recomendado:** Compara Adobe Learning Manager y un LMS tradicional para la formación empresarial. Mostrar la comparación en formato de tabla.

![Salida tabular en el Asistente del alumno](assets/tabular-format.png)

### Preparación de campañas y marketing

Los equipos de marketing suelen necesitar refrescantes rápidos antes de las revisiones, lanzamientos o debates con los responsables de departamento. El asistente de IA resume el contenido de aprendizaje complejo en información procesable.

**En qué ayuda:**

* Resume cursos o vídeos largos en puntos clave

* Actualizar el conocimiento del proceso o del producto antes de las reuniones

* Descubre contenido de aprendizaje relacionado para profundizar en la experiencia

![Preparación de campañas y marketing mediante el Asistente del alumno](assets/marketing-readiness.png)

### Aclaración operativa y de procesos

Los equipos internos, de asistencia y de operaciones dependen de una documentación de procesos precisa. El Asistente de IA ayuda a aclarar las políticas y los flujos de trabajo al instante.

**En qué ayuda:**

* Encuentre respuestas sobre procesos internos, SOP y directrices de cumplimiento

* Aclarar detalles de nivel de paso sin examinar documentos largos

* Reducir la dependencia de las pymes para las preguntas repetitivas

![Documentación operativa y de procesos con el Asistente del alumno](assets/operational-process.png)

### Incorporación y transiciones de funciones más rápidas

Los nuevos empleados que se incorporan a nuevas funciones a menudo tienen dificultades para navegar por los grandes catálogos de aprendizaje. El asistente de IA acelera el aumento guiándolos a las respuestas relevantes.

**En qué ayuda:**

* Responder a preguntas habituales de incorporación desde contenido asignado

* Proporcionar explicaciones rápidas de conceptos específicos de funciones

* Apoya el aprendizaje autodirigido sin sobrecarga de información

![Empleados de incorporación](assets/onboarding.png)

### Actualización del conocimiento y aprendizaje continuo

Los alumnos experimentados necesitan actualizadores rápidos en lugar de un reciclaje completo. El asistente de inteligencia artificial ayuda al aprendizaje continuo en el flujo de trabajo.

**En qué ayuda:**

* Actualizar el conocimiento a petición sin volver a ver los cursos

* Reforzar los resultados del aprendizaje tras la finalización de la formación

* Fomenta una interacción frecuente y de poco esfuerzo con el contenido de aprendizaje

![Respuesta de actualización de conocimientos en el Asistente del alumno](assets/knowledge-refresh.png)

## Cómo utiliza el contenido el asistente de inteligencia artificial del alumno

El asistente de inteligencia artificial para alumnos le ayuda a encontrar respuestas precisas rápidamente mientras aprende. Para utilizarlo de manera eficaz, debe comprender qué contenido utiliza el asistente, qué no utiliza y cómo genera respuestas.

### ¿Qué contenido utiliza el Asistente de inteligencia artificial?

El asistente de inteligencia artificial del alumno responde a las preguntas utilizando solo el contenido de aprendizaje asignado en Adobe Learning Manager.

* El asistente utiliza contenido de los catálogos internos que el administrador habilita para el asistente de inteligencia artificial del alumno.

* El asistente respeta su función, pertenencia a grupos y permisos de catálogo al recuperar información.

### ¿Qué contenido no utiliza el Asistente de inteligencia artificial?

El Asistente de inteligencia artificial para alumnos limita las respuestas al ámbito de aprendizaje asignado.

* No utiliza contenido de catálogos predeterminados, compartidos, adquiridos, externos u otros catálogos que no sean internos.

* No recupera información de bibliotecas de contenido de terceros como LinkedIn Learning o Go1.

* No navega por Internet ni accede a sitios web externos para generar respuestas.

### Cómo genera respuestas el Asistente de inteligencia artificial

El asistente de inteligencia artificial del alumno analiza el contenido de aprendizaje asignado para generar respuestas específicas y contextuales.

* Cada respuesta incluye citas que hacen referencia al contenido original.

* Puede seleccionar una cita para ir directamente al curso, módulo o documento correspondiente.

* Las citas le ayudan a verificar la información y explorar el contexto adicional cuando sea necesario.

### Utilizar el Asistente de IA de forma responsable

Utilice el asistente de inteligencia artificial de alumno como ayuda de aprendizaje para explorar, actualizar y reforzar conocimientos.

* Trata las respuestas como una guía basada en el contenido de aprendizaje disponible.

* Consulte el material fuente citado para obtener información completa y autorizada.

### Cómo controlan los administradores el acceso

Los administradores gestionan el acceso al Asistente de inteligencia artificial del alumno y controlan el contenido que utiliza.

* Los administradores asignan el asistente a grupos de usuarios específicos.

* Los administradores seleccionan los catálogos internos que el asistente puede utilizar como orígenes de contenido.

* Estos controles garantizan que el asistente solo muestra contenido de aprendizaje aprobado y relevante.

## Acerca de los mensajes incorporados

El Asistente para inteligencia artificial de alumno incluye un conjunto de mensajes integrados que ayudan a los alumnos a familiarizarse rápidamente con preguntas y situaciones comunes. Estos mensajes guían a los alumnos sobre cómo interactuar con el asistente y muestran los tipos de preguntas que pueden hacer.

![Mensajes incorporados proporcionados por el Asistente del alumno](assets/built-in-prompts.png)

Los mensajes incorporados se pueden personalizar por cuenta. Las organizaciones pueden adaptar estos mensajes para reflejar sus objetivos de aprendizaje, las funciones de los alumnos, la terminología o casos prácticos específicos.

Los administradores pueden trabajar con su administrador de éxito de clientes (CSM) para configurar, modificar o actualizar las solicitudes integradas de su cuenta. La personalización de solicitudes se gestiona en el nivel de cuenta y no se puede configurar directamente en la interfaz de usuario de Adobe Learning Manager en la versión actual.

Las solicitudes que se muestran a los alumnos pueden variar según la configuración definida con Adobe.

## Habilitar el asistente de inteligencia artificial de alumno

![Asistente para alumnos con IA](assets/learner-ai-assistant.png)

El Asistente de IA (versión beta) proporciona asistencia basada en IA para ayudar a los alumnos a descubrir contenido e interactuar con él de forma más eficaz. Los administradores controlan el acceso asignando la función a grupos de usuarios y catálogos específicos. Solo deben utilizarse catálogos internos al configurar el Asistente de IA. El contenido de los catálogos Compartido, Adquirido, Externo u otro catálogo que no sea interno no se admite para su aparición en las respuestas y citas del Asistente de inteligencia artificial.

Los administradores seleccionan qué grupos de usuarios y catálogos internos pueden acceder a la función Asistente de IA. Deben asegurarse de que los catálogos asignados incluyan solo el contenido de aprendizaje que sea adecuado para aparecer mediante respuestas y citas de IA, y de que dichos catálogos sean internos, no compartidos, adquiridos o externos.

Antes de configurar el Asistente de IA (Beta), confirme que tiene credenciales de administrador y que ha identificado los grupos de usuarios y catálogos que deben tener acceso a la función.

### Configurar el acceso del Asistente del alumno

Para activar el Asistente de inteligencia artificial del alumno:

&#x200B;1. Inicie sesión en Adobe Learning Manager como administrador.

&#x200B;2. Seleccione **Configuración** en la página principal.

![Consola de administrador con la opción Configuración en el panel izquierdo](assets/settings-menu.png)

&#x200B;3. Seleccione **Asistente de inteligencia artificial del alumno (beta)** en el menú **Configuración**.

![La consola del administrador muestra la opción Asistente de inteligencia artificial del alumno en el panel izquierdo](assets/learner-assistant-ai-beta.png)

&#x200B;4. Seleccione el conmutador para habilitar el **Asistente de inteligencia artificial del alumno (beta)**.

![La consola de administradores muestra el conmutador habilitado para el Asistente de inteligencia artificial del alumno](assets/learner-assistant-toggle.png)

&#x200B;5. Seleccione uno o más grupos de usuarios en la opción **Grupos de usuarios elegibles**.

&#x200B;6. Seleccione **Guardar** para aplicar la configuración del grupo de usuarios.

&#x200B;7. Seleccione uno o varios catálogos en la opción **Catálogos aptos**.

&#x200B;8. Seleccione **Guardar** para aplicar la configuración del catálogo.

>[!IMPORTANT]
>
>El Asistente de IA solo admite catálogos internos. Si se selecciona un catálogo compartido, adquirido, externo u otro que no sea interno, el Asistente de AI no mostrará su contenido, aunque el catálogo aparezca en la lista Catálogos aptos.

## Acceder al asistente de inteligencia artificial para alumnos en Adobe Learning Manager

La versión beta del asistente de inteligencia artificial para alumnos de Adobe Learning Manager le ayuda a encontrar respuestas rápidamente mientras aprende. Esta herramienta inteligente responde directamente a sus preguntas sobre cursos, contenido y funciones de la plataforma, todo ello desde su cuenta de alumno.

El Asistente de AI solo puede utilizar contenido de catálogos internos que el administrador haya activado para el Asistente del alumno. No se incluye el contenido que solo se encuentre en catálogos compartidos, adquiridos o externos.

El Asistente de inteligencia artificial del alumno (beta) solo está disponible para alumnos seleccionados.

### Iniciar el Asistente de IA

Para iniciar el Asistente de IA del alumno:

&#x200B;1. Inicie sesión en Adobe Learning Manager como alumno.

&#x200B;2. Selecciona **Preguntar al asistente de inteligencia artificial** en la página principal.

![La página de inicio del alumno muestra Solicitar al Asistente de inteligencia artificial que seleccione y abra el panel Asistente de inteligencia artificial del alumno](assets/ask-ai-assistant.png)

&#x200B;3. Cuando aparezca la pantalla **Asistente de inteligencia artificial del alumno (beta)**, seleccione **Introducción**.

![Seleccione Introducción para iniciar el Asistente del alumno](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Al iniciar AI Assistant por primera vez, debe dar su consentimiento antes de utilizarlo. El cuadro de diálogo de consentimiento solo aparecerá durante este inicio inicial. Para todos los inicios posteriores, se le dirigirá directamente al Asistente de inteligencia artificial para introducir sus indicaciones.

&#x200B;4. Escriba el mensaje en el campo de texto.

![Escribir mensaje en el Asistente del alumno](assets/type-prompt.png)

&#x200B;5. Pulse **Intro** para recibir una respuesta. Revisar la respuesta, las fuentes y las recomendaciones.

Adobe permite una personalización rápida en el nivel de cuenta. Para configurar o actualizar las solicitudes integradas, póngase en contacto con el administrador de éxito de clientes (CSM) de Adobe.

Las respuestas del asistente de inteligencia artificial incluyen citas con cada respuesta para que los alumnos puedan verificar fácilmente de dónde proviene la información. Cada referencia citada se vincula al módulo del curso original, la ayuda de trabajo u otro contenido de aprendizaje.

Los alumnos pueden:

* Seleccione el número de cita en línea para ir directamente a la sección de referencia exacta

* Abra la lista completa de orígenes seleccionando **Mostrar orígenes** en la parte inferior de la respuesta

![Mostrar orígenes en la respuesta](assets/show-sources.png)

El Asistente del alumno incluye citas con cada respuesta para mostrar el origen de la información. Cada cita se vincula directamente al curso, módulo u objeto de aprendizaje original utilizado para generar la respuesta.

Puede seleccionar cualquier cita para abrir la página del curso real en Adobe Learning Manager y revisar todo el contenido en contexto. Las citas le ayudan a verificar la información, explorar detalles adicionales y seguir aprendiendo de la fuente autorizada.

## Acceder al Ayudante de AI mediante la búsqueda

Los administradores también pueden iniciar el Asistente de inteligencia artificial directamente desde la barra de búsqueda. Solo tienes que escribir tu pregunta y seleccionar **Ask AI Assistant** en las opciones que aparecen a continuación para obtener respuestas del contenido de aprendizaje asignado.

![Acceder al Asistente del alumno desde la barra de búsqueda](assets/learner-assistant-search.png)

## Proporcionar comentarios sobre las respuestas del Asistente para inteligencia artificial (Beta) del alumno

Sus comentarios sobre las respuestas generadas por el Asistente de inteligencia artificial del alumno (Beta) ayudan a mejorar su precisión, relevancia y rendimiento general.

### Indicar si una respuesta le gusta o no

* Selecciona **Pulgares arriba**, elige lo que te haya parecido útil en la respuesta, agrega comentarios de manera opcional y luego selecciona **Enviar**.

![Seleccionar Pulgares hacia arriba para votar a favor de una respuesta](assets/thumbs-up.png)

* Selecciona **Pulgares abajo**, elige la razón por la que la respuesta no fue útil, añade comentarios y luego selecciona **Enviar**.

![Seleccionar Pulgares abajo para votar a la baja una respuesta](assets/thumbs-down.png)

## Iniciar nuevo chat en el Asistente de IA

Los alumnos pueden borrar la conversación actual e iniciar una nueva conversación en cualquier momento.

* Seleccione **Nuevo chat** en la pantalla del Asistente de inteligencia artificial y, a continuación, seleccione **Sí**.

![Iniciar una nueva conversación en el Asistente del alumno](assets/start-new-chat.png)
