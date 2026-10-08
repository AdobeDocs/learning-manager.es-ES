---
description: Aprende a crear, configurar y publicar un juego de rol de Entrenador virtual, desde la configuración de personajes y temas hasta la puntuación y la configuración avanzada
jcr-language: en_us
title: Crear y publicar un juego de roles de entrenador virtual
exl-id: f37e93ef-6d76-4b7c-b4c3-f3f8c57b143c
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '4850'
ht-degree: 0%
---

# Crear y publicar un juego de roles de entrenador virtual

Crea un escenario de juego de roles de IA en Adobe Learning Manager Virtual Coach para que los alumnos puedan practicar conversaciones del mundo real como parte de un curso o una ayuda de trabajo. Este artículo recorre todo el proceso necesario para crear un juego de roles de Virtual Coach, desde la elección de una plantilla hasta la publicación en la biblioteca de contenido.

Antes de comenzar, confirme que Adobe Learning Manager Virtual Coach está habilitado en su cuenta y que ha iniciado sesión como autor. Virtual Coach crea todos los juegos de rol a partir de los materiales y los detalles que proporciones: no incorpora automáticamente el contenido del curso existente en tu organización. Si aún no lo has hecho, [reúne materiales para un juego de roles de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) antes de empezar.

Para crear un escenario de juego de roles de IA en Virtual Coach:
1. En el panel de navegación izquierdo, selecciona **Entrenador virtual** y luego selecciona **Crear ahora**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach1.png)

2. En la sección **Destacados**, elige una plantilla **Individual** o **Multi-Persona**. En este ejemplo, asumimos que este juego de rol se basa en una sola persona. Para conocer los pasos que implican a varios personajes, consulte [juego de roles multipersona](#configure-a-multi-persona-role-play)

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach2.png)

   Se abre la ventana **Crear juego de roles**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach14.png)

3. Si lo desea, cargue el material de origen y, a continuación, seleccione **Crear conjuntamente con IA**.
4. Configure los temas de persona, apertura de conversaciones y evaluación.
5. Seleccione **Editar** en la sección **Temas que cubrir**. Establece los pesos de puntuación y cualquier tema de **Make o Break**.
6. Cada una de las secciones se puede editar de esta manera.
7. Si estás satisfecho con el contenido, selecciona **Aprobar contenido y continúa**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach16.png)

8. Previsualice el juego de roles y, a continuación, **Publish**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach17.png)

## Abre Virtual Coach e inicia un juego de roles

Hay dos formas de crear un juego de roles de entrenador virtual: empieza a partir de una plantilla o crea una desde cero con el asistente de creación conjunta de IA. En esta sección se trata la creación desde cero.

1. Inicie sesión en Adobe Learning Manager como autor.
2. Seleccione **Entrenador virtual** en el panel de navegación izquierdo.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach1.png)
   *Seleccione Entrenador virtual en Crear en el panel de navegación izquierdo para comenzar a crear un juego de roles.*

3. En la página **Entrenador virtual**, selecciona **Crear ahora**.
4. Seleccione una plantilla de la sección **Destacado** o de la sección **Plantillas disponibles**. Las plantillas destacadas incluyen dos opciones para crear desde cero:
   - **Juego de roles personal único (Asistente de IA)**: el alumno interactúa con una persona de IA. Utilícelo para una conversación con el cliente, una conversación sobre liderazgo, una llamada de descubrimiento o una conversación de orientación.
   - **Juego De Roles Multipersonal (Beta)**: el alumno interactúa con hasta cuatro personas de inteligencia artificial en la misma conversación. Utilícelo para una revisión del comité ejecutivo, un panel de adquisiciones, finanzas y asuntos legales o una negociación con el cliente en la que participen varias partes interesadas; por ejemplo, un escenario de preparación para el lanzamiento de un producto en el que un representante deba presentar una nueva oferta a un director financiero, un responsable de adquisiciones, un Director de TI y un campeón de usuario final en una sesión.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach2.png)
   *Elige un juego de roles individual o multipersonal en la sección Destacados para crear un escenario desde cero, o selecciona una plantilla prediseñada a continuación.*

   Para este ejemplo, seleccione **Juego de roles personal único (Asistente de IA)** en la sección **Destacados**. Para comenzar desde un escenario preparado, vea [crear un juego de roles mediante una plantilla de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-role-play-using-virtual-coach-template.md).
5. De manera opcional, selecciona **Cargar archivos** para agregar documentos complementarios, como una hoja de datos de producto, un libro de estrategias o una grabación de llamadas. El Asistente de creación conjunta de IA los utiliza para crear un escenario más preciso. Omita este paso si no tiene archivos relevantes.
6. Seleccione **Co-Create With AI**. Cuando aparezca el mensaje de confirmación, seleccione **Generar**.
7. Escriba una descripción para el juego de roles. Utilice una descripción que describa el escenario, como `Handling price objections in enterprise sales` o `Pitching our new product to a buying committee`.
8. Continúe la conversación con el asistente de inteligencia artificial y añada más contexto sobre el escenario. El asistente explica que un juego de roles tiene tres componentes principales: **Información general** (contexto de título y conversación), **Persona de IA** (nombre, organización, rol, antecedentes, preocupaciones, etc.) y **Temas de evaluación** (los criterios utilizados para puntuar a los alumnos), y le pregunta si desea crear estos elementos paso a paso o generarlos todos a la vez.
9. Continúa añadiendo información o selecciona **Aprobar contenido y continúa** cuando estés satisfecho.

## Configurar las opciones de juego de roles

Después de crear un juego de roles de entrenador virtual mediante el Asistente de creación conjunta de inteligencia artificial, se abre la pantalla **Editar juego de roles**. El progreso se guarda automáticamente, como muestra el indicador **Guardados** en la esquina superior derecha. Puede salir y volver a esta pantalla en cualquier momento sin perder su trabajo.

Desde esta pantalla, tiene tres opciones:

- **Preview** ejecuta una sesión de prueba en vivo para que puedas experimentar el juego de roles como alumno antes que nadie. Utilice esta opción para comprobar que el personaje suena natural y que los temas fluyen correctamente.
- **Guardar** guarda el estado actual sin publicar. El juego de roles se agrega a la sección **Plantillas disponibles** de tu biblioteca Virtual Coach, donde puedes volver para editarlo más adelante.
- **Publish** agrega el juego de roles a la **biblioteca de contenido** para que se pueda asignar a un curso o ayuda de trabajo.

Para realizar cambios en el contenido generado sin editar los campos manualmente, seleccione **Editar con IA** a la derecha. Esto abre la interfaz de chat de AI y le permite describir los cambios que desea en lenguaje sencillo, por ejemplo, `make the persona more formal` o `add a topic about pricing objections`.

>[!NOTE]
>
>Esto es diferente de la edición por secciones. La opción de edición por secciones le da acceso a todas las secciones al mismo tiempo. La interfaz de chat de AI, por otro lado, le da una opción para describir libremente exactamente lo que desea cambiar.

Seleccione **Editar** junto al **título del juego de roles** para cambiar el título.

## Personaliza tu simulación de Virtual Coach

Define el contexto de la conversación, los antecedentes personales y las preocupaciones de la persona para que tu escenario de juego de roles sea realista y desafiante. Cuantos más detalles proporcione en cada campo, más precisa y coherente se comportará el personaje de IA durante la simulación.

Si has utilizado **Crear conjuntamente con IA** o **Generar automáticamente el juego de funciones**, estos campos se rellenan previamente según tus entradas. Revíselas y perfecciónelas antes de publicarlas.

### Contexto de conversación

El campo **Contexto de conversación** establece el escenario para el alumno. Le dice al personaje de IA el trasfondo y el propósito del juego de roles para que entienda por qué la conversación está ocurriendo y cuál debería ser el enfoque principal.

>[!NOTE]
>
>Este campo está escrito para el alumno de la IA, no para el alumno. No incluya aquí instrucciones o directrices destinadas al alumno. Utilice el campo **Abridor de instructores de inteligencia artificial**, que se describe más adelante en este artículo, para el contexto orientado al alumno.

Al escribir el contexto de conversación:

- **Explique la situación.** Describa qué tipo de conversación es esta, como una llamada de descubrimiento de ventas, una llamada en frío o un discurso de presentación, y quién la inició.
- **Describir la posición del personaje de IA.** Explique quién es la persona en relación con el alumno. Por ejemplo, un cliente que evalúa un producto, un director financiero que revisa una propuesta presupuestaria o un empleado que recibe comentarios.
- **Usar &quot;el alumno&quot; de forma coherente.** Cuando te refieras a la persona con la que está hablando la persona, escribe siempre &quot;el alumno&quot;. Evita etiquetas como &quot;el agente&quot;, &quot;el vendedor&quot; o &quot;el representante&quot;, que pueden causar un comportamiento personal incoherente.
- **Mantén la concisión.** Incluir sólo la información relevante para la configuración de la conversación. Guarde los detalles específicos del personaje en **Información personal de fondo**.

**Ejemplo:** &quot;Esta es una llamada de detección de ventas. El alumno se ha puesto en contacto para programar una llamada introductoria con Karen Mitchell, Director de Asuntos Médicos de una red hospitalaria de tamaño medio. Karen aceptó una llamada de 15 minutos para aprender más sobre la plataforma de aprendizaje. Tiene poco tiempo y evalúa si la plataforma cumple con los estándares de calidad de contenido clínico antes de involucrar a su equipo&quot;.

### Información de antecedentes personales

El campo **Información personal de fondo** le da personalidad al personaje de IA. Cuantos más detalles introduzcas, más precisas y coherentes serán las respuestas de la persona a lo largo de la simulación.

Incluye:

- **Detalles básicos**: el nombre, la edad, la función y la situación actual de la persona en relación con el tema y el objetivo del juego de roles.
- **Motivaciones y objetivos**: lo que la persona se preocupa, lo que quiere lograr o lo que quiere cambiar, y sus puntos débiles.
- **Creencias y actitudes**: cómo se siente el alumno sobre el tema de la conversación y sobre la organización del alumno.
- **Comportamientos y hábitos**: tendencias que dan forma a la Perspectiva de la persona, como una toma de decisiones cautelosa o un afán por adoptar nuevas herramientas.
- **Criterios de decisión**: lo que convence al usuario de avanzar y cualquier restricción dentro de la que esté trabajando, como el tiempo, el presupuesto o los procesos de aprobación.

>[!TIP]
>
>Los detalles específicos ayudan a la persona a responder de una manera natural y creíble. Los fondos genéricos producen un comportamiento genérico.

### Preocupaciones personales

Las **preocupaciones personales** definen los problemas, preocupaciones o preguntas específicos que plantea la persona durante la conversación. Estas preocupaciones impulsan el flujo del juego de roles y garantizan que el alumno tenga que responder a desafíos realistas.

- **Lista de tres a cinco preocupaciones.** Frase cada uno como una preocupación o pregunta, y que sea específico y procesable. Evite preocupaciones vagas como &quot;preocuparse por el costo&quot;; escribe &quot;preocupado de que el costo anual de la licencia exceda el presupuesto discrecional del departamento sin la aprobación del CFO&quot;.
- **Centra cada problema en un solo tema.** Una preocupación por tema mantiene la conversación manejable y asegura que cada desafío sea evaluado claramente.
- **Especifique cuándo aparece el problema.** Indica el punto de la conversación en el que la persona lo plantea.
- **Define qué es lo suficientemente bueno para continuar.** Describa lo que permitiría que la conversación avanzara. Por ejemplo, el alumno tranquiliza al alumno, proporciona una referencia u ofrece documentación.

Escriba cada problema usando esta estructura: **preocupación → cuando surge → qué es lo suficientemente bueno para avanzar.**

**Ejemplo:** &quot;Preocupación — Precisión del contenido clínico: aparece cuando el alumno describe el proceso de creación de contenido. Suficientemente bueno: El alumno afirma explícitamente que el contenido lo crean profesionales médicos, lo revisan otros colegas y se vincula a la literatura primaria o a directrices clínicas reconocidas&quot;.

Una vez que hayas rellenado la información relevante, selecciona **Guardar**.

>[!TIP]
>
>Plazo de problema de la prueba con **Preview**. Una preocupación que aparece demasiado pronto o demasiado tarde interrumpe el flujo de la conversación.

>[!NOTE]
>
>Los cambios en la configuración personal surten efecto inmediatamente para cualquier juego de roles no publicado. Si edita un juego de roles que ya está publicado y asignado a los alumnos, vuelva a publicarlo para aplicar el personaje actualizado a futuras sesiones.

## Configurar una presentación para la simulación

Utilice la sección **Configuración de presentación** para adjuntar una presentación a la simulación del juego de roles. Cuando se adjunta una presentación, los alumnos pueden verla durante la sesión como referencia o como ayuda interactiva. Por ejemplo, un paquete de descripción del producto utilizado durante una simulación de discurso de ventas.

1. Seleccione **Cargar PDF o PPTX** en **Detalles de la presentación**.
2. Selecciona tu archivo. Se admiten los formatos PDF y PPTX, con un tamaño de archivo máximo de 100 MB.
3. Una vez cargado, el nombre del archivo aparece debajo del botón y confirma el archivo adjunto.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach3.png)
   *Adjunte una presentación para que los alumnos puedan hacer referencia a ella como ayuda para hablar durante la simulación.*

4. Seleccione **Listo** para guardar la configuración y volver a la configuración del juego de roles.

Una vez que cargues una presentación, la opción **Permitir a los alumnos cargar su propia presentación** se activa automáticamente. También puede descargar o eliminar el archivo adjunto mediante los botones de la derecha.

Seleccione **Permitir a los alumnos cargar su propia presentación** si desea que cada alumno practique con su propia versión de una presentación en lugar de una compartida. Esto resulta útil cuando se evalúa a los alumnos en una presentación que han preparado personalmente, como una reseña empresarial o un discurso de ventas personalizado. Este botón deslizante está desactivado de forma predeterminada; cuando se activa, los alumnos ven un mensaje de carga al inicio de la sesión.

>[!NOTE]
>
>Asegúrate de que todas las presentaciones que cargues estén accesibles. Usa suficiente contraste de color, incluye texto alternativo para las imágenes y evita contenido que se base solo en el color para transmitir significado.

## Configurar el personaje de IA

La sección **Configuración personal de IA** controla con quién habla el alumno durante la simulación, así como su apariencia, voz, función y personalidad de comportamiento. Una de las partes más importantes de la forma de crear un escenario de juego de roles de IA es corregir esta sección, ya que un personaje de avatar de IA bien configurado hace que el juego de roles se sienta realista y garantiza que la IA se comporte de forma coherente con el escenario que has diseñado.

### Elegir un personaje

Hay dos fichas disponibles: **Personas del sistema** y **Personas personalizadas**.

**System Personas** son caracteres prediseñados proporcionados por Adobe. Cada uno tiene un nombre, una foto y uno o dos modos de interacción admitidos: **Voz y vídeo** (el personaje aparece como un avatar animado con voz hablada) o **Voz** (solo voz hablada, sin avatar de vídeo). Seleccione un personaje del sistema seleccionando su icono.

**Personas personalizadas** son personas que has creado anteriormente. Seleccione esta pestaña para reutilizar un personaje de avatar de IA de un juego de roles anterior en lugar de crear uno desde cero.

![](/help/migrated/authors/feature-summary/assets/virtual_coach4.png)
*Reutilizar un personaje personalizado de un juego de roles anterior en lugar de crear uno nuevo desde cero.*

Puede reutilizar un personaje de dos formas: edita sus detalles directamente para convertirlo en un personaje diferente, o selecciona **Duplicar** para crear una copia y cambiar sus detalles. Para ver ambas opciones, seleccione el icono de puntos suspensivos verticales (**⋮**) que aparece en la esquina superior derecha de la imagen de un personaje al pasar el puntero sobre él o seleccionarlo.

### Configurar los detalles personales y la personalidad

Después de seleccionar un personaje, rellena los campos **Detalles personales de AI**:

1. Escriba la **función** del personaje: su cargo tal y como debe aparecer en la simulación, por ejemplo, Director de asuntos médicos.
2. Especifique la **organización** del usuario, es decir, la empresa o institución para la que trabaja. Por ejemplo, Northgate Health.
3. Seleccione una **Personalidad** que coincida con el nivel de desafío y el contexto del escenario:

   | Personalidad | Comportamiento |
   |---|---|
   | Escéptico | Cuestiona todo y exige pruebas |
   | Indiferente | Descomprometido y difícil de excitar |
   | Entusiasta | Entusiasmados con la solución y listos para participar |
   | Orientado a relaciones | Valora sobre todo la confianza y la conexión personal |
   | Neutro | Mantiene el equilibrio y evalúa las opciones sin sesgo |
   | Asertivo | Contundente, acelerada y que tiende a desafiar a otros |

4. Opcionalmente, habilita **Permitir a los alumnos seleccionar esta opción antes de que comience el juego de roles** para permitir que los alumnos elijan la personalidad del personaje antes de iniciar la sesión. Esto resulta útil para escenarios en modo de práctica en los que los alumnos desean controlar la dificultad.
5. Seleccione **Listo** para guardar la configuración de persona.

>[!TIP]
>
>Haz coincidir la personalidad con el reto del escenario. Un escenario de llamada en frío se beneficia de una persona **escéptica** o **indiferente** para simular una perspectiva difícil. Un escenario de comentarios de directivos funciona bien con **Assertive** o **Relationship Oriented** para reflejar una dinámica realista entre el administrador y el empleado.

### Crear un personaje personalizado

Si los perfiles de sistema no encajan en tu escenario, crea uno nuevo desde la pestaña **Personalizados**.

1. Selecciona **Personas personalizadas** y luego **Crear nueva persona**.
2. Cargue una fotografía de la persona. La imagen debe tener un tamaño mínimo de 640 x 360 píxeles y un tamaño máximo de 1 MB.
3. Escriba el **Nombre** del personaje.
4. Seleccione una **Voz** en el menú desplegable para establecer la voz que habla la IA.
5. Ajuste el regulador **Velocidad de voz** para controlar la velocidad de voz, de -100 (más lenta) a +100 (más rápida). El valor predeterminado es 0 (espacio neutro). Seleccione **Probar voz** para obtener una vista previa del sonido de la voz antes de guardarla.
6. Seleccione **Crear persona**. El nuevo personaje se guarda en la pestaña **Personas personalizadas** y está disponible para su uso en cualquier juego de roles futuro.

>[!NOTE]
>
>Los personajes personalizados admiten la interacción de voz. Confirme que la velocidad de voz suena natural en el escenario antes de la publicación. Una velocidad muy rápida o muy lenta puede hacer que la simulación parezca poco natural y afectar a la puntuación de ritmo del alumno.

Al habilitar **Avatar de vídeo**, se agrega un avatar de vídeo de IA con realismo fotográfico al juego de roles. Hay avatares de vídeo disponibles para perfiles que admiten el modo **Voz y vídeo**. Cada alumno recibe 300 minutos de juego de roles de vídeo al mes; una vez alcanzado este límite, la experiencia cambia a un avatar estático.

### Configurar un juego de roles multipersona

Utilice un juego de roles multipersona cuando el alumno necesite navegar por una conversación que implique a más de una parte interesada en la misma sesión. Por ejemplo, presentar un nuevo producto a un comité de compra formado por un director financiero, un responsable de adquisiciones, un Director de TI y un campeón de usuario final. Los juegos de roles multipersona admiten **hasta cuatro personajes** en un único escenario.

1. Seleccione **Juego de roles multipersonal** como plantilla al iniciar el juego de roles.
2. Añada cada persona y asígnele una función distinta. Por ejemplo, CFO, Administrador de adquisiciones, Director de TI y Campeón.
3. Configura una personalidad independiente para cada persona, siguiendo los mismos pasos de **Detalles personales de IA** descritos anteriormente.
4. Defina preocupaciones únicas para cada persona, usando la misma estructura de preocupaciones descrita en **preocupaciones personales.** Cada persona hace preguntas y plantea objeciones desde su propia Perspectiva, por lo que el alumno tiene que adaptar su mensaje para cada responsable de departamento en lugar de dar un discurso genérico.

## Configurar la apertura de la conversación

La sección **Apertura de conversación** controla las dos primeras cosas que escucha un alumno cuando se inicia una simulación: una breve declaración contextual del instructor de inteligencia artificial, seguida de la línea de apertura del personaje de inteligencia artificial.

![](/help/migrated/authors/feature-summary/assets/virtual_coach5.png)
*El instructor de inteligencia artificial prepara el escenario en primer lugar y, a continuación, el personaje de inteligencia artificial abre la conversación en carácter.*

**AI Trainer Opener** es un mensaje corto que habla el instructor, no la persona, antes de que comience la conversación. Le dice al alumno con quién está a punto de hablar, cuál es el objetivo y el contexto relevante en el que debe trabajar. Seleccione **Editar** para actualizar el texto. Hazlo breve y directo. Para escenarios más exigentes, incluya el objetivo de forma explícita, por ejemplo: &quot;Estás a punto de hacer una llamada en frío a un jefe de adquisiciones. Tu objetivo es asegurar una reunión de seguimiento&quot;.

**AI Persona Opener** es la primera línea que el personaje de IA entrega al alumno, iniciando la conversación. Debe reflejar la personalidad de la persona y poner al alumno en el lugar desde el primer intercambio. Seleccione **Editar** para actualizar el texto.

| Escenario | Ejemplo de dispositivo de apertura |
|---|---|
| Llamada en frío | &quot;¿Hola? ¿Quién es este?&quot; |
| Llamada de detección programada | &quot;Hola, gracias por ponerte en contacto con nosotros. ¿Qué querías cubrir hoy?&quot; |
| Comentarios y conversación | &quot;¿Tienes un minuto? Quería hablar de la semana pasada&quot;. |
| Presentación ejecutiva | &quot;Solo tengo diez minutos. ¿Qué tienes para mí?&quot; |

Seleccione **Vista previa** para escuchar a los dos abridores reproducidos en secuencia, exactamente como el alumno los verá al comienzo de una sesión.

>[!TIP]
>
>Si AI Trainer Opener y AI Persona Opener tienen un tono demasiado similar, la transición entre ellos puede resultar confusa. Mantenga el dispositivo de apertura del dispositivo de entrenamiento neutral e instructivo; deja que el abrelatas lleve la personalidad.

## Configurar temas y criterios de evaluación

La sección **Temas que tratar** define lo que el alumno debe abordar durante la simulación y cómo la IA evalúa su rendimiento en cada tema: esta es la rúbrica de puntuación del juego de roles de IA. Cada tema que se añade se convierte en un componente puntuado en el informe de conocimientos del alumno.

**Antes de comenzar:** Complete primero la sección **Personalizar la simulación**. La inteligencia artificial utiliza el contexto de la conversación y el fondo personal para generar directrices de evaluación precisas para cada tema.

Cada fila de la tabla de temas representa un área de conversación necesaria:

| Columna | Propósito |
|---|---|
| Tema | El nombre del área de conversación que debe cubrir el alumno. |
| Directrices de evaluación | Los criterios que utiliza la Inteligencia artificial para evaluar si el tema se abordó adecuadamente; estas directrices también aparecen como comentarios en la página de análisis del alumno |
| Grosor | El porcentaje de la puntuación de conocimiento que aporta este tema; todos los pesos de temas deben ser del 100% |
| Vídeo de ejemplo | Un vídeo opcional que el alumno puede ver en su página de análisis para ver cómo se debe tratar el tema |
| Vínculo útil | Una URL opcional que se muestra en la página de análisis del alumno junto con los criterios de evaluación. |
| Crear o romper | Cuando está activada, si el alumno no aborda este tema, la puntuación final de la simulación es 0, independientemente del rendimiento de otros temas |

![](/help/migrated/authors/feature-summary/assets/virtual_coach6.png)
*Cada fila de tema define qué evaluar, cuánto vale y si es necesario aprobar.*

### Agregar un tema

1. Seleccione **Editar** en la sección **Temas que cubrir** para abrir la tabla de temas.
2. Seleccione **Agregar tema**. Aparece una nueva fila con campos vacíos.
3. Escriba el nombre del tema en el campo **Tema**. Utilice una etiqueta breve y descriptiva que refleje el área de conversación, por ejemplo, `Opening and Rapport`, `Handling Objections` o `Agreeing Next Steps`.
4. Escriba las directrices de evaluación en el campo **Directrices de evaluación**. Escríbalas como una instrucción de finalización que empiece por: &quot;Para tratar este tema correctamente, el alumno debe...&quot;
5. Escriba un porcentaje en el campo **Grosor**. Distribuir grosores en todos los temas para que el total sea igual al 100 %.
6. Opcionalmente, selecciona **Hacer clic para agregar vídeo** para adjuntar un vídeo de ejemplo, o **Hacer clic para agregar URL** para adjuntar un enlace útil, como un artículo de la base de conocimiento o un localizador de producto.
7. Opcionalmente, habilite **Make or Break** para temas no negociables.
8. Repita el proceso para cada tema que desee incluir y, a continuación, seleccione **Hecho**.

### Edición o eliminación de un tema

- Para editar cualquier campo de una fila de tema existente, seleccione el campo directamente y actualice el texto o el valor.
- Para volver a generar las directrices de evaluación con IA según su persona y contexto, seleccione el icono de actualización (**↻**) en la celda **Directrices de evaluación**.
- Para quitar un tema, seleccione el menú de opciones (**⋮**) al final de la fila y seleccione **Eliminar tema**.
- Para duplicar un tema y utilizarlo como base para otro similar, seleccione **Duplicar tema** en el mismo menú.

### Directrices para escribir temas eficaces

Una sólida rúbrica de puntuación del juego de roles de IA marca la diferencia entre un juego de roles que se siente justo y uno que se siente arbitrario. Tenga en cuenta estas directrices:

- **Asignar nombre a los temas después de las fases de conversación, no a las características del producto.** Temas como `Opening and Rapport`, `Needs Discovery` y `Agreeing Next Steps` reflejan la estructura de una conversación real.
- **Escribir instrucciones de evaluación como acciones observables.** La IA evalúa lo que ha dicho el alumno, por lo que las directrices deben describir comportamientos específicos y audibles, no intenciones. Compare &quot;el alumno debe entender las preocupaciones del personaje&quot; (débil) con &quot;el alumno necesita pedirle que nombre su preocupación principal y confirme que lo ha escuchado antes de responder&quot; (fuerte).
- **Usar Make o Break con moderación.** Reserve para uno o dos temas en los que la omisión total haría que la conversación fuera un claro fracaso, como no presentarse a sí mismo en una llamada fría. Si se aplica a demasiados temas, a los alumnos les resulta difícil pasar incluso un intento razonable.
- **Equilibra los pesos para reflejar la importancia de la conversación.** Un tema que ocupa la mayor parte de una conversación típica, como el descubrimiento de necesidades en una llamada de ventas, debe tener un peso mayor que un breve inicio o cierre.
- **Agregar vínculos útiles a temas de baja puntuación.** Si los alumnos obtienen sistemáticamente una puntuación baja en un tema concreto en todas las sesiones, adjunte un vínculo de recurso para que tengan algo que estudiar entre intentos.

## Configurar opciones de idioma

La sección **Configuración de idioma** controla si los alumnos pueden elegir el idioma en el que practican al iniciar la simulación. Habilita **Permitir a los alumnos elegir su idioma de práctica** para que cada alumno pueda seleccionar su idioma preferido al comienzo de la sesión. Deje esto desactivado si desea que todos los alumnos practiquen en el idioma en el que se creó el juego de roles, la configuración recomendada para las evaluaciones formales en las que la coherencia del idioma forma parte de los criterios de evaluación.

>[!NOTE]
>
>Virtual Coach admite contenido de simulación en nueve idiomas. La selección de idioma del alumno solo es significativa si el contenido del escenario y el perfil están escritos para admitir el uso multilingüe; Si las directrices de evaluación y los antecedentes personales están escritos en un solo idioma, activar esta configuración puede producir respuestas de IA incoherentes para los alumnos que seleccionan un idioma diferente.

## Configurar el análisis de acciones en pantalla

La sección **Análisis de acciones en pantalla** te permite cargar un vídeo de prácticas recomendadas que muestra a la IA cómo puntuar las acciones que realiza un alumno durante el juego de roles. Esto resulta especialmente útil en simulaciones en las que se espera que el alumno muestre acciones específicas de forma visible en la pantalla, como navegar por una interfaz de software, rellenar un formulario o seguir un proceso definido paso a paso.

>[!NOTE]
>
>Esta opción está deshabilitada si solo ha cargado archivos de PowerPoint o PDF en la sección **Configuración de presentación**.

1. Seleccione **Seleccionar archivo** para abrir el explorador de archivos.
2. Seleccione el archivo de vídeo y confirme la carga.
3. Una vez cargado, el nombre del archivo aparece en la fila de resumen **Análisis de acciones en pantalla**.

El vídeo debe cumplir estos requisitos:

| Requisito | Especificación |
|---|---|
| Formato del archivo | WEBM, MP4, WMV o MPEG |
| Tamaño máximo de archivo | 200 MB |
| Resolución mínima | 1280 x 720 píxeles |
| Tasa de marco mínima | 5 FPS |
| Proporción de aspecto | Entre 4:3 y 21:9 |

Cuando grabe un vídeo según las prácticas recomendadas, describa todas las acciones en audio y en pantalla al mismo tiempo. Por ejemplo, supongamos que selecciono el botón Enviar mientras lo hago, ya que la IA se basa tanto en la narración como en la acción visual. Mantén la grabación centrada en la tarea, elimina las notificaciones y el contenido no relacionado, y ajusta el vídeo a las directrices de evaluación para que muestre cada acción necesaria en el punto del flujo de trabajo donde se espera que ocurra.

## Configurar opciones de puntuación

**Puntuación de aprobado** es la puntuación global mínima que debe obtener un alumno para que la simulación se marque como aprobada y se aplique a la combinación ponderada de puntuaciones de estilo y conocimientos. Escriba un número entre 1 y 100 en el campo **Puntuación de aprobado** (el valor predeterminado es 80) y seleccione **Hecho**.

>[!TIP]
>
>Para las evaluaciones formales, una puntuación de aprobado de 75 a 80 es típica. Para los juegos de rol de modo de práctica en los que el objetivo es el desarrollo de habilidades en lugar de la certificación, considere un umbral inferior o habilite el **Modo de práctica**.

**Grosores de puntuación de IA** establecen en qué medida el componente Conocimiento (si el alumno ha tratado los temas necesarios y ha proporcionado información precisa) y el componente Estilo (ritmo, claridad, palabras para rellenar, longitud de frase, energía) contribuyen cada uno a la puntuación general. Arrastre el regulador para ajustar el equilibrio; los dos valores siempre suman el 100 % y el valor predeterminado es Conocimiento 70 % / Estilo 30 %. Para obtener orientación sobre cómo los alumnos interpretan estas puntuaciones, consulte [comprender el informe de rendimiento de Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

| Tipo de escenario | Proporción recomendada | Razón |
|---|---|---|
| Evaluación o certificación de aptitudes | 80% Conocimiento / 20% Estilo | La precisión del contenido es la medida principal |
| Capacitación de ventas | 60% Conocimiento / 40% Estilo | La entrega importa tanto como el mensaje en las conversaciones con los clientes |
| Desarrollo del liderazgo | 70% Conocimiento / 30% Estilo | Equilibrado: tanto el contenido como el tono son esenciales en las conversaciones de las personas |
| Entrenamiento de comunicación | 40% Conocimiento / 60% Estilo | El estilo es el objetivo principal del aprendizaje |

**Habilitar el modo de práctica para los alumnos** permite a los alumnos solicitar sugerencias durante la simulación para ayudarles a mantenerse al día, lo que resulta útil para el aprendizaje en las primeras etapas. Cuando está habilitada, puede establecer **Sugerencias máximas por sesión** (valor predeterminado de 5, ajustable de 1 a 10) y la duración de la visibilidad de la sugerencia (valor predeterminado de 30 segundos).

>[!NOTE]
>
>Las sugerencias no están disponibles durante las evaluaciones formales. Si utiliza este juego de roles como evaluación graduada, desactive el modo de práctica para que todos los alumnos se evalúen en las mismas condiciones.

**Ocultar puntuación** impide que los alumnos vean su puntuación numérica después de la sesión; todavía reciben retroalimentación cualitativa y análisis a nivel de tema. Utilícelo cuando el juego de roles sea solo para práctica, cuando solo un evaluador responsable deba ver el resultado o cuando desee reducir la ansiedad de la puntuación en las primeras etapas de aprendizaje.

## Configurar opciones avanzadas de juego de funciones

Estos ajustes opcionales controlan cómo y cuándo finaliza la simulación y cómo se configura el entorno de sesión.

**Permitir que la IA finalice el juego de roles.** De forma predeterminada, solo el alumno puede finalizar una simulación seleccionando **Finalizar simulación**. Active este botón de alternancia y describa la condición en la que el usuario debe cerrar la conversación de forma natural, por ejemplo: &quot;Cuando el alumno programa correctamente una reunión de seguimiento o el usuario rechaza tres veces, el usuario debe finalizar la llamada educadamente&quot;. Utilícelo para escenarios avanzados donde el punto final natural de la conversación, no un temporizador, debe determinar cuándo se cierra la sesión.

**Límite de tiempo de simulación.** Escriba un número entre 1 y 59 minutos para establecer una duración máxima de la sesión; cuando se alcanza, la simulación finaliza automáticamente y el alumno se dirige a la página de análisis.

| Tipo de escenario | Límite sugerido |
|---|---|
| Llamada en frío o breve práctica de apertura | 3-5 minutos |
| Llamada de detección o evaluación de necesidades | 10-15 minutos |
| Conversación completa sobre ventas o liderazgo | 15-20 minutos |
| Evaluación formal con varios temas | Coincide con la duración esperada de la conversación en el mundo real |

**Sanción por sesión corta** disuade a los alumnos de finalizar las sesiones demasiado rápido aplicando una reducción de puntuación si la sesión está por debajo de la duración mínima establecida. Utilícelo cuando la duración de la sesión sea significativa para el objetivo de aprendizaje. Por ejemplo, en una llamada de descubrimiento en la que el alumno debe dedicar tiempo suficiente a descubrir necesidades antes de proponer una solución.

>[!NOTE]
>
>No utilice Penalización de sesión corta en juegos de rol en modo de práctica en los que los alumnos aún están creando confianza, ya que penalizar las salidas tempranas puede aumentar la ansiedad y desalentar los intentos repetidos.

**Habilitar el uso compartido de pantalla** permite a los alumnos compartir su pantalla durante la simulación. Esto es relevante para escenarios que incluyen un componente **Análisis de acciones en pantalla**. Está deshabilitado de manera predeterminada si solo ha cargado documentos de PowerPoint o de PDF en **Configuración de presentación**.

**Habilitar subtítulos personales de inteligencia artificial** muestra en pantalla el texto de lo que dice el personal de inteligencia artificial en tiempo real. Habilite esta opción para los alumnos con dificultades auditivas o que practiquen en un segundo idioma, para entornos ruidosos o para escenarios en los que leer las palabras exactas del personaje sea importante para comprender las objeciones con matices.

## Publish: el juego de roles del entrenador virtual

Después de configurar todas las secciones, seleccione **Publish**.

![](/help/migrated/authors/feature-summary/assets/virtual_coach7.png)
*Complete los detalles de publicación y seleccione Guardar para agregar su juego de roles a la biblioteca de contenido.*

1. Introduzca el título del juego de roles.
2. Seleccione la carpeta en la que desea agregar el juego de roles.
3. Si lo desea, añada etiquetas y una fecha de caducidad.
4. Seleccione **Guardar**. El juego de roles se agrega a la **biblioteca de contenido**.

Ahora ha creado un juego de roles de Entrenador virtual de principio a fin en Adobe Learning Manager Virtual Coach. Continúe con [agregar un juego de roles de entrenador virtual a un curso](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md) para que esté disponible para los alumnos. Para obtener respuestas a preguntas de creación habituales, como por qué un juego de roles podría marcar cero, cuántos perfiles admite un juego de roles multipersona y cómo escribir un buen mensaje para el Asistente de creación conjunta de IA, consulta las [preguntas frecuentes de Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).
