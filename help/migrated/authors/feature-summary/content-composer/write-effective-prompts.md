---
description: El mensaje es la entrada más importante en Compositor de contenido. Un mensaje específico, como asignar un nombre a la audiencia, entre 2 y 3 temas y una señal de ámbito, produce un resumen más preciso, un esquema más claro y menos edición en sentido descendente.
jcr-language: en_us
title: Escribir mensajes eficaces en el compositor de contenido
hide: true
source-git-commit: 2fff90164df5d54a6dbe1bb62bab5fd3da59029c
workflow-type: tm+mt
source-wordcount: '2339'
ht-degree: 0%

---


# Escribir mensajes eficaces en el compositor de contenido

Aprende a escribir indicaciones eficaces en cada fase de Content Composer, desde el indicador de apertura hasta el editor de notas, esquemas y cursos, para producir cursos precisos y bien estructurados generados por IA con menos edición.

El compositor de contenido es muy conversador. La calidad de lo que produce en cada etapa depende de la calidad de lo que le das. En esta guía se explica cómo comunicarse con la IA de forma eficaz en cada una de las cuatro fases: **Inicio**, **Resumen**, **Esquema** y **Curso**.

## Fase 1: Inicio: escriba el mensaje de apertura

El mensaje de apertura es su punto de partida. No tiene por qué ser perfecto. El compositor de contenido lee el mensaje y lo utiliza para abrir una conversación. Incluso un mensaje aproximado pone en marcha el proceso; el asistente hará preguntas de seguimiento en la fase de Brief para llenar lo que falta.

Dicho esto, un mensaje más específico significa que la inteligencia artificial rellena previamente el resumen de forma más precisa, lo que reduce las idas y venidas antes de generar el esquema. Si tienes una idea clara de la audiencia, los temas y el objetivo, ponla en el mensaje.

Un aviso impreciso produce un resumen impreciso. Un resumen vago produce un esquema genérico. Un esquema genérico genera un curso que necesita una edición importante. La especificidad en la etapa inmediata avanza en cascada a través de cada paso subsiguiente.

### ¿Qué espera el Compositor de contenido?

El compositor de contenido espera lo siguiente en una o dos frases:

- **Quiénes** son los alumnos? Asigne un nombre a su función y nivel de experiencia.
  - **Qué** cubrirá el curso? Describir 2-3 áreas temáticas específicas en lugar de un dominio amplio. Por ejemplo, &quot;reconocimiento de phishing, higiene de contraseñas y configuración de MFA&quot; es más útil que &quot;seguridad de TI&quot;.
- **¿Cuál es el objetivo de aprendizaje?** Describa el resultado o el cambio de comportamiento que desea que los alumnos realicen después de completar el curso.

### Anatomía de un mensaje efectivo

**[Nivel de audiencia y experiencia]** + **[2-3 temas específicos]** + **[objetivo de aprendizaje]**

**Ejemplo**:

Quiero crear un curso para nuevos representantes de ventas que cubra nuestros niveles de precios empresariales y el flujo de trabajo de aprobación de descuentos. Al final, deberían poder gestionar con confianza las tres objeciones más comunes de los clientes.

Desglosar esto:

- **Audiencia:** nuevos representantes de ventas

- **Temas:** niveles de precios empresariales, flujo de trabajo de aprobación de descuentos, tres objeciones comunes
  - **Objetivo de aprendizaje**: manejar con confianza las tres objeciones más comunes de los clientes: un resultado de comportamiento medible, no un tema que cubrir

Una vez que seleccione **Comenzar**, Content Composer abrirá el escenario **Brief**. Revise los campos prerrellenados, el título, el perfil del alumno y el objetivo que la IA generó en el mensaje, y perfeccione cualquier elemento que no coincida con sus intenciones antes de generar el esquema.

### Qué hacer y qué no con un mensaje eficaz

| **Incluir** | **Evitar** |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Una función de audiencia específica (&quot;nuevos representantes de ventas&quot;, &quot;gestores de primera línea&quot;) | Audiencias vagas (&quot;todo el personal&quot;, &quot;todos&quot;, &quot;usuarios&quot;) |
| 2-3 áreas temáticas concretas | Más de 6 temas en un mensaje: producen contornos sobrecargados; divida en cursos independientes |
| Una señal de ámbito: duración, profundidad o resultado del alumno | Objetivos genéricos (&quot;enseñarles todo sobre X&quot;, &quot;cubrir todos los aspectos de&quot;) |
| Contexto que da forma al tono o la profundidad (&quot;para el cumplimiento normativo&quot;, &quot;para una audiencia no técnica&quot;, &quot;basado en escenarios&quot;) | Hacer preguntas sobre la IA El mensaje es breve, no una conversación |
| Lo que los alumnos podrán hacer después del curso | Contenido del curso (deje la estructura en la fase de esquema) |

### Mensajes de inicio por tipo de curso

| **Tipo de curso** | **Mensaje de inicio** |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Formación de cumplimiento** | &quot;Quiero crear un curso para todos los empleados sobre el manejo de datos del RGPD, que abarque lo que se considera datos personales, cómo almacenarlos y compartirlos correctamente, y qué hacer si se produce una infracción&quot;. |
| **Incorporación** | &quot;Deseo crear un módulo de incorporación para la nueva \[función\] que abarque \[tema 1\], \[tema 2\] y \[tema 3\]. |
| **Habilidades técnicas** | &quot;Quiero crear un curso para ingenieros de software junior sobre prácticas de codificación seguras, como la prevención de inyecciones de código SQL, la validación de entradas y cómo leer un informe SAST&quot;. |
| **Habilidades sociales** | &quot;Quiero crear un curso para los gerentes de primera línea sobre cómo dar comentarios constructivos, como cubrir el modelo de SBI, cómo prepararse para una conversación de feedback y cómo hacer un seguimiento&quot;. |
| **Directiva y procedimiento** | &quot;Quiero crear un curso para el personal del almacén sobre procedimientos de manipulación manual, como la técnica de elevación correcta, cuándo usar el equipo y cómo informar de una falta inminente&quot;. |
| **Formación sobre productos** | &quot;Deseo crear un curso para los agentes del servicio de atención al cliente sobre nuestra política de devoluciones, como la cobertura de los criterios de elegibilidad, cómo procesar una devolución en \[system\] y cómo gestionar las ampliaciones&quot;. |
| **Habilitación de ventas** | &quot;Quiero crear un curso para ejecutivos de cuentas de nivel medio sobre la negociación de acuerdos empresariales, por ejemplo, que abarque cómo identificar a los responsables de la toma de decisiones, cómo gestionar las objeciones de precios utilizando nuestro marco de valor y cuándo recurrir a un director de ventas&quot;. |
| **Desarrollo del liderazgo** | &quot;Quiero crear un curso para gestores de personas por primera vez que cubra cómo realizar un examen semanal individualizado de manera eficaz, como establecer una agenda, ofrecer reconocimiento y abordar el rendimiento inferior de forma temprana&quot;. |
| **Formación de sistemas y herramientas** | &quot;Quiero crear un curso para los coordinadores de RR. HH. que son nuevos en Workday, por ejemplo, para saber cómo crear una solicitud de trabajo, pasar a un candidato a través de las fases de contratación y generar un informe de recuento&quot;. |
| **Salud y seguridad** | &quot;Quiero crear un curso de actualización para todo el personal del sitio sobre procedimientos de seguridad contra incendios, por ejemplo, que cubra la ruta de evacuación para cada zona del edificio, cómo usar un extintor de incendios y qué hacer si descubre un incendio fuera de las horas de trabajo&quot;. |

## Fase 2: Resumen: Perfeccione las sugerencias de la IA

Después de enviar el mensaje, Compositor de contenido abre la fase Breve y rellena previamente tres campos: el título del curso, el perfil del alumno y el objetivo de aprendizaje. La IA hace preguntas de seguimiento para enfocar cada campo antes de generar el contorno.

Esta es una etapa de conversación. La calidad de las respuestas a las preguntas de la IA determina directamente la calidad del esquema que produce.

### Título del curso

La IA sugiere dos opciones de título. Seleccione la que encaje o escriba la suya propia. Si ninguno de los dos es correcto, describa la brecha:

&quot;Ninguno. El curso trata específicamente del flujo de trabajo de aprobación, no de los precios generales&quot;.

Un buen título está orientado al alumno. Describe lo que el alumno podrá hacer, no lo que cubre el curso.

### Perfil del alumno

La IA pregunta por la función, el nivel de experiencia y con qué se enfrentan actualmente los alumnos. Sé específico tanto sobre lo que saben como sobre lo que no:

| Menos útil | Más útil |
|---|---|
| &quot;Todos los empleados&quot; | &quot;Los desarrolladores de software de mitad de carrera están familiarizados con la agilidad pero sin experiencia en el cumplimiento de la seguridad empresarial&quot; |
| &quot;Nuevo en el tema&quot; | &quot;Los gerentes de carrera temprana ascendieron desde papeles individuales de contribuidor sin formación formal de gerencia&quot; |
| &quot;Nuestro equipo de ventas&quot; | &quot;Los ejecutivos de las nuevas cuentas en sus primeros 90 días, cómodos con las herramientas de CRM, pero poco familiarizados con las estructuras de precios empresariales&quot; |

### Objetivo de aprendizaje

La IA pregunta qué pueden hacer los alumnos en el trabajo después de completar el curso. Este es el campo Resumen más importante: controla lo que la IA prioriza en los archivos de origen, cómo se estructura el esquema y qué pruebas de las pruebas.

Escriba el objetivo como un comportamiento que empiece con un verbo de acción:

| Objetivo débil | Fuerte objetivo |
|---|---|
| &quot;Comprensión de la protección de datos&quot; | &quot;Identificar datos personales, aplicar prácticas correctas de almacenamiento e intercambio, e informar de una supuesta infracción utilizando el proceso de elaboración de informes de la organización&quot; |
| &quot;Más información sobre la gestión de objeciones&quot; | &quot;Responde a las tres objeciones más comunes de los clientes utilizando el marco de mensajería aprobado, sin pasar a un director de ventas&quot; |
| &quot;Conoce el proceso de incorporación&quot; | &quot;Complete la lista de comprobación de la incorporación durante la primera semana, envíe los formularios de cumplimiento requeridos y acceda a las herramientas necesarias para su función sin asistencia de TI&quot;. |

>[!IMPORTANT]
>
>**Antes de generar el esquema:** El esquema se ha creado completamente a partir del resumen, no a partir del mensaje original. Antes de seleccionar **Generar esquema**, confirme que el título es orientado al alumno, el perfil del alumno asigna un nombre de función y nivel de experiencia específicos y el objetivo de aprendizaje describe un comportamiento cuantificable en el trabajo. Un resumen bien definido produce un esquema bien estructurado. Si algún campo sigue siendo genérico, afinarlo ahora.  Ahorra una edición considerable más tarde.

### Firma que el Brief necesita más trabajo

- El perfil del alumno indica &quot;empleados que desean aprender sobre X&quot; en lugar de nombrar una función y un nivel de experiencia específicos
- El objetivo de aprendizaje describe un área temática en lugar de un comportamiento cuantificable en el trabajo
- El título es una etiqueta de tema (&quot;Seguridad de TI&quot;) en lugar de un resultado orientado al alumno (&quot;Identificar intentos de suplantación de identidad y responder a ellos&quot;)

## Fase 3: Contorno - editar a través de conversación

Después de confirmar el resumen, el compositor de contenido genera una estructura de lección y tema. Puede revisarlo y solicitar cambios a través del panel de chat antes de generar el curso completo.

En la versión actual, la edición de esquemas es completamente conversacional. No se puede seleccionar una lección o tema en el lienzo para cambiarle el nombre o reordenarlo. Todos los cambios se realizan escribiendo solicitudes en lenguaje sencillo.

Esta es también la etapa más eficiente para realizar cambios estructurales. La edición del contorno tarda segundos. La reestructuración de un curso generado tarda mucho más tiempo.

### Cómo redactar solicitudes de edición de esquemas de frase

Sé directo y específico. Asigne un nombre a la lección o al tema por su título actual, describa el cambio que desee y, opcionalmente, explique por qué.

**Cambiar nombre:**

- &quot;Cambie el nombre de la Lección 1 a &#39;Cómo funcionan los ataques de phishing&#39;.&quot;
- &quot;Cambie el nombre del tema 2.3 a &#39;Rutas de escalación y líneas de tiempo&#39;.&quot;

**Agregar:**

- &quot;Añada un nuevo tema a la Lección 2 sobre suplantación de identidad mediante código QR&quot;.
- &quot;Agregue una lección sobre la respuesta al incidente después de la Lección 4&quot;.

**Quitar:**

- &quot;Eliminar el tema 1.3.&quot;
- &quot;Eliminar lección 5. Ese contenido se trata en un curso independiente&quot;.

**Reordenar:**

- &quot;Mueve la Lección 3 para que sea la segunda lección.&quot;
- &quot;Traslade el tema 2.1 al final de la Lección 2.&quot;

**Dividir:**

- &quot;Dividir la lección 3 en dos lecciones, una que cubra los filtros de spam y otra que cubra la administración de parches&quot;.

**Combinar:**

- &quot;Fusiona las lecciones 4 y 5 en una sola lección llamada &#39;Respuesta ante incidentes y recuperación&#39;&quot;.

**Volver a generar:**

- &quot;Regenera el esquema con un enfoque más fuerte en la higiene de las contraseñas y el MFA&quot;.
- &quot;Regenera el esquema: la estructura actual es demasiado técnica para una audiencia que no sea técnica&quot;.

### Qué no puede hacer la fase de esquema

- La jerarquía se ha fijado como Lecciones > Temas. No se pueden crear subtemas ni estructuras de tres niveles.
- No se pueden establecer objetivos de lección individuales en esta fase: el objetivo de aprendizaje general del resumen se aplica al curso completo.
- No puede añadir componentes ni medios en esta fase. Estos se añaden en el editor del curso.

### Cuándo regenerar frente a cuándo editar

| Utilizar la edición de conversación cuando... | Regenerar cuando... |
|---|---|
| La estructura general es correcta, pero los nombres o temas individuales deben ajustarse | La estructura general no coincide en absoluto con su intención |
| Desea agregar o quitar elementos específicos | El Brief se perfeccionó significativamente después de generar el primer esquema |
| Hay que dividir o combinar una lección | El esquema parece genérico y carece del contexto específico de su organización |

## Fase 4: Curso: Perfeccionar contenido mediante el asistente

Después de aprobar el esquema y generar el curso, el panel **Crear con compositor de contenido** permanece abierto en el lado derecho de la pantalla. Puede utilizarlo para perfeccionar, ampliar o ajustar cualquier parte del curso generado a través de la conversación.

El asistente del Editor del curso está diseñado para tareas de edición de contenido. Para preguntas de procedimiento sobre el producto, utilice esta documentación de ayuda en lugar de preguntar al asistente.

### Cómo formular solicitudes de edición de cursos

**Reescribir o ajustar una sección específica:**

- &quot;Reescribe el párrafo en la segunda sección de la Lección 1 para que sea más conciso: busca tres oraciones&quot;.
- &quot;Hacer que el contenido del tema 2.1 sea menos técnico. El público no tiene experiencia en TI&quot;.
- &quot;Añade un ejemplo real a la introducción de la lección 1&quot;.

**Ajustar tono:**

- &quot;Reescribe la lección 2 en un tono más conversacional&quot;.
- &quot;Aumentar la autoridad del contenido del tema 3.2: se trata de un curso de cumplimiento&quot;.

**Expandir o agregar contenido:**

- &quot;Añada un ejemplo basado en el escenario al tema 1.3 que muestre el aspecto que podría tener un correo electrónico de suplantación de identidad&quot;.
- &quot;Expanda la sección de MFA para incluir instrucciones para configurarlo en dispositivos móviles&quot;.

**Reducir o simplificar:**

- &quot;Acorte el texto de la diapositiva 5 a tres viñetas&quot;.
- &quot;Resumir el segundo párrafo del tema 2.2 en una sola oración.&quot;

**Ajustar la prueba:**

- &quot;Regenera el cuestionario para la lección 2 con preguntas más complicadas&quot;.
- &quot;Reemplace la pregunta 3 por una pregunta basada en escenarios sobre el reconocimiento de un intento de ingeniería social&quot;.
- &quot;Añade dos preguntas más al cuestionario de la lección 1 centrado en la configuración de MFA&quot;.

**Ajustar imágenes:**

- &quot;Reemplace la imagen del tema 2.2 por algo que muestre un escenario de ingeniería social&quot;.
- &quot;Genere una imagen para el tema 1.1 que ilustre un correo electrónico de suplantación de identidad (phishing) en una pantalla de un portátil&quot;.

**Agregar o modificar componentes:**

- &quot;Añada una carta de presentación al tema 3.1 con las tres definiciones de los niveles de precios&quot;.
- &quot;Añada un acordeón al tema 2.3 con los pasos de escalación: un panel por paso&quot;.
- &quot;Convertir la lista de viñetas del tema 1.2 en un componente de la línea de tiempo.&quot;

### Qué no puede hacer el Ayudante del curso

- Cambie el nombre de las lecciones o temas directamente en el lienzo. Utilice el asistente: &quot;Cambie el nombre de la Lección 2 a &#39;Higiene de contraseñas&#39;.&quot;
- Cree ramificaciones o trazados adaptables. La estructura del curso es lineal.
- Agregue nuevas lecciones o reestructure el esquema. Los cambios estructurales requieren volver a la fase Esquema.

## Prácticas recomendadas en todas las fases

- **Describa lo que desea generar antes de abrir Content Composer.** Una oración redactada de antemano tiende a ser más clara que una escrita bajo la presión del campo de entrada.
- **Invierte tiempo en el objetivo de aprendizaje.** El objetivo del resumen controla la estructura del esquema, la priorización del archivo de origen y la alineación de las pruebas. Un objetivo específico centrado en el comportamiento reduce la edición en cada fase posterior.
- **Restringir el resumen antes de generar el esquema.** El esquema se crea a partir del resumen, no del mensaje original. Un resumen bien definido con un perfil de alumno específico y un objetivo de aprendizaje genera un esquema estructurado y relevante.
- **Edite el esquema antes de generar el curso.** Los cambios estructurales en la fase de esquema tardan segundos. Los mismos cambios después de la generación del curso tardan mucho más tiempo.
- **Usar el Asistente para cursos para contenido, no para estructura.** Los cambios estructurales, la adición de lecciones, la reordenación de temas, pertenecen a la etapa Esquema. Utilice el Asistente del curso para ajustar texto, tono, ejemplos y preguntas de prueba.
- **Sea específico en cada solicitud.** Asigne un nombre a la lección, tema, diapositiva o pregunta que desea cambiar. &quot;Mejora&quot; no da a la IA nada con lo que actuar. &quot;Haz que el tema 2.1 sea más conciso y añade un ejemplo real&quot;.
