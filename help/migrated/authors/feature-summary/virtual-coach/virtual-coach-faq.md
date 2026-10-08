---
description: Encuentre respuestas a preguntas habituales sobre la creación, la concesión de licencias, la seguridad, la privacidad de los datos, la puntuación y la experiencia del alumno en Virtual Coach
jcr-language: en_us
title: Preguntas frecuentes sobre Virtual Coach
exl-id: b8955b04-4655-413a-b570-a05b1f76285c
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 0%
---

# Preguntas frecuentes sobre Virtual Coach

## Creación

Obtenga respuestas a preguntas habituales sobre la creación, configuración y solución de problemas de un juego de roles de Virtual Coach.

1. **¿Por qué mi juego de rol obtuvo cero aunque cubrí la mayoría de los temas?**
Compruebe si uno de los temas tiene **Make o Break** habilitado. Si un alumno no aborda ningún tema de tipo Make o Break durante la conversación, la puntuación final de la simulación es 0, independientemente de lo bien que haya funcionado en todo lo demás. Reserve Make or Break para uno o dos temas genuinamente no negociables para evitar que esto suceda en un intento razonable. Para obtener una configuración completa, consulte [crear y publicar un juego de roles de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

2. **¿Cuántos personajes puede incluir un juego de roles multipersona?**
Hasta cuatro personas en un solo escenario, cada una configurada individualmente con su propia **función**, **personalidad** y **preocupaciones personales**. Utilícelo cuando un alumno necesite navegar por más de un responsable de departamento en la misma conversación, como un discurso en un comité de compra o una revisión del panel ejecutivo.

3. **¿Cómo puedo elegir entre voz, chat y vídeo para un juego de rol?**
Esto depende del tipo de persona que seleccione. **System Personas** solo admite **Voice &amp; Video** (un avatar animado con voz hablada) o **Voice**. **Personas personalizadas** admiten la interacción de voz, y puedes habilitar **Video Avatar** por separado para los perfiles que admitan el modo Voz y Vídeo. Elija Voz y vídeo para obtener la simulación más realista, o Voz solo para escenarios en los que no sea necesario un avatar visual, como la formación por teléfono.

4. **¿Cómo puedo escribir un buen mensaje para el Asistente de creación conjunta de IA?**
Escriba una breve descripción que describa el escenario, como `Handling price objections in enterprise sales` o `Pitching our new product to a buying committee`. A continuación, el asistente de inteligencia artificial le hace preguntas de seguimiento para ayudarle a crear los temas de información general, personalidad de inteligencia artificial y evaluación. Proporciona todo el contexto que puedas sobre la situación, el papel y las preocupaciones del personaje, y cómo quieres medir el éxito: más detalles en tu descripción inicial significa menos idas y venidas en el chat. Consulta [recopilar materiales para un juego de roles de entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) para obtener una plantilla de solicitud más completa.

5. **¿Puedo editar un juego de roles después de publicarlo?**
Sí. Los cambios en la configuración personal, los temas y otras configuraciones surten efecto inmediatamente para cualquier juego de roles no publicado. Si ya se ha publicado un juego de funciones y se ha asignado a los alumnos, vuelva a publicarlo después de realizar cambios para que los alumnos vean la versión más reciente.

Para preguntas generales sobre productos, licencias y administración, consulta las [Preguntas frecuentes de Adobe Learning Manager Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).

## Formación y cumplimiento normativo

1. **¿Cómo protege Virtual Coach los datos de los clientes y alumnos?**
Los datos de los clientes se almacenan utilizando el cifrado AES-256, se protegen en tránsito mediante TLS 1.3+ y se separan de forma lógica mediante identificadores de clientes únicos para garantizar el aislamiento entre los entornos de los clientes. Estos controles se validan mediante pruebas anuales de penetración de terceros.

2. **¿Dónde se almacenan y procesan los datos de Virtual Coach?**
Los datos de los clientes se almacenan en los centros de datos de la UE, lo que facilita su alineación con los requisitos europeos de privacidad.

3. **¿Cuánto tiempo conserva Virtual Coach los datos de los clientes y alumnos y se pueden eliminar?**
Los datos de sesión se pueden conservar durante la duración del acuerdo de servicio y los clientes pueden configurar políticas de retención específicas de la empresa. Los usuarios individuales pueden eliminar sus propias grabaciones, los administradores pueden realizar eliminaciones masivas y los datos se pueden exportar antes de la eliminación. También se admiten los mecanismos de eliminación automática y el registro de auditoría.

4. **¿Se utiliza el contenido cargado por el cliente para otros fines que no sean la generación del juego de roles, como la formación en IA o la mejora del producto?**
No, los datos de los clientes no se utilizan para la formación en inteligencia artificial.

5. **¿Cómo usa Virtual Coach la IA y qué salvaguardias existen para las respuestas generadas por la IA?**
Virtual Coach utiliza IA generativa para crear experiencias interactivas de juego de roles. Existen múltiples salvaguardias, incluidos filtros de contenido de Azure OpenAI para categorías como violencia, discurso de odio, contenido sexual y autolesiones; barandillas de nivel rápido; y controles contextuales que mantienen la IA centrada en los casos prácticos de aprendizaje y desarrollo. También se llevan a cabo pruebas de seguridad de IA y se utilizan salvaguardias como la transformación rápida basada en la seguridad y el comportamiento de aclarar y luego rechazar para las solicitudes confidenciales. Además, los compromisos contractuales requieren la divulgación de los resultados generados por la IA y el cumplimiento de las normativas de IA aplicables.

6. **¿Qué estándares de privacidad y cumplimiento admite Virtual Coach?**
Virtual Coach admite protecciones de privacidad relacionadas con el RGPD, controles de retención configurables, registro de auditoría, capacidades de eliminación de usuarios y alojamiento de datos basado en la UE. El acuerdo contractual también requiere el cumplimiento de las leyes y regulaciones aplicables, incluidas la Ley de IA de la UE y la Ley de Transparencia de IA de California (SB-942).

7. **¿A quién pertenece el contenido cargado en Virtual Coach y el contenido generado durante una sesión?**
El cliente es propietario del contenido cargado en Virtual Coach y del contenido generado durante una sesión.

8. **¿Dónde residen los datos de Virtual Coach, en Adobe Learning Manager o con el proveedor de servicios de Virtual Coach?**
Los datos de los juegos de rol se almacenan en la infraestructura en la nube del proveedor de servicios de Virtual Coach y se alojan en los centros de datos de la UE.

## Producto

1. **¿Cómo se activa Virtual Coach para un cliente existente de Adobe Learning Manager?**
Consulte [Activación de Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md#activatevirtualcoach)

2. **¿Durante cuánto tiempo es válida la activación de Virtual Coach y cómo se renueva?**
La activación de Virtual Coach en Adobe Learning Manager es válida mientras dure el contrato de suscripción del complemento. No es automáticamente permanente. En su lugar, la validez se alinea con el período de suscripción.

   **Renovación:** Para seguir utilizando Virtual Coach después de que finalice el período de contrato, debes renovar la suscripción. En el momento de la compra, Adobe proporciona una clave de activación, que el administrador de la cuenta utiliza para habilitar Virtual Coach en la sección Facturación. Si renueva su contrato, recibirá instrucciones y una nueva clave de activación si es necesario para mantener un acceso ininterrumpido.

   También se asignan créditos mensuales de usuario activo (MAU) para cada período de contrato. Los créditos no utilizados al final del contrato caducan. No se trasladan a un período renovado o nuevo. Su activación dura mientras esté activa su suscripción de pago a Virtual Coach y se produzca la renovación ampliando la suscripción, tal y como se gestiona a través de su cuenta de Adobe.

3. **¿Qué sucede con los documentos de origen cargados y los datos de sesión generados después de crear o completar un juego de funciones?**
Los documentos de origen cargados se pueden utilizar para crear y configurar escenarios de juego de roles, perfiles y criterios de evaluación. Una vez que los alumnos completan un juego de roles, Virtual Coach genera resultados de evaluación, puntuaciones, comentarios de orientación e información de finalización para respaldar las actividades de aprendizaje e informes. Los datos asociados con los juegos de rol siguen estando disponibles según el ciclo de vida del contenido aplicable y las políticas de retención.

4. **¿Pueden los alumnos reintentar un juego de roles?**
Sí. Los alumnos pueden repetir una sesión de juego de roles varias veces para practicar sus habilidades, aplicar comentarios de orientación y mejorar su rendimiento. Después de completar un juego de roles, los alumnos pueden revisar sus comentarios e iniciar otro intento de continuar desarrollando sus habilidades.

## General

1. **¿Qué es el entrenador virtual?**
Virtual Coach es una función de orientación y juego de roles basada en IA e integrada en Adobe Learning Manager. Permite a los alumnos practicar conversaciones del mundo real con un personaje de IA que responde de forma inteligente en tiempo real y, a continuación, recibir un informe de rendimiento instantáneo que abarca lo que dijeron y cómo lo dijeron. Para obtener una explicación completa, consulta [qué es Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md).

2. **¿Quién usa Virtual Coach?**
Las organizaciones usan Virtual Coach para formar a representantes de ventas, equipos de servicio al cliente, agentes de centros de llamadas, gerentes y líderes, nuevos empleados, partners y empleados que aprenden nuevos productos o procesos. Virtual Coach está disponible para todos los alumnos, autores y administradores en una cuenta de Adobe Learning Manager en la que se ha activado. Los alumnos acceden a las sesiones de juego de funciones y las completan, los autores crean y publican escenarios de juego de funciones y los administradores gestionan los créditos y ven informes.

3. **¿Virtual Coach utiliza automáticamente mi contenido de Adobe Learning Manager existente?**
No. Los autores deben proporcionar materiales de referencia, como libros de estrategias, presentaciones de ventas, transcripciones y rúbricas de puntuación, o un aviso por escrito, para cada juego de rol que creen. Virtual Coach utiliza esos materiales y definiciones personales cargados para dirigir la conversación; no se basa automáticamente en el contenido que ya se encuentra en la biblioteca de contenido o en los cursos. Consulta [reunir materiales para un juego de roles de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) para saber qué preparar.

4. **¿Qué tipos de juegos de rol hay disponibles?**
Virtual Coach admite tres dominios: Capacitación de ventas, desarrollo del liderazgo y evaluación de habilidades. Los autores eligen entre plantillas prediseñadas que cubren escenarios como llamadas de descubrimiento B2B, llamadas en frío, gestión de objeciones, opiniones difíciles y reducción de las quejas de los clientes. Los autores también pueden crear escenarios personalizados desde cero utilizando el asistente de IA. Vea [crear y publicar un juego de roles de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

5. **¿Qué idiomas admite Virtual Coach?**
Virtual Coach está disponible en nueve idiomas tanto para la interfaz como para el contenido de simulación: alemán (Alemania), español (LATAM), español (España), francés (Francia), italiano (Italia), portugués (Portugal), portugués (Brasil), neerlandés (Países Bajos) e inglés.

6. **¿Cómo se obtiene la licencia y se factura a Virtual Coach?**
Virtual Coach está disponible como suscripción adicional a Adobe Learning Manager. El uso se mide en usuarios activos mensuales (MAU). Un crédito de la unidad MOU se consume cuando un alumno inicia un curso en un mes natural; las sesiones adicionales del mismo alumno de ese mes no consumen créditos adicionales. Los créditos no utilizados al final del vencimiento del contrato anual. Consulte [Administrar el uso y la facturación de Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md).

7. **¿Cómo se calcula la puntuación de un alumno?**
Cada sesión produce una puntuación de conocimiento y una puntuación de estilo. La puntuación de conocimientos refleja si el alumno ha abordado los temas necesarios y ha proporcionado información precisa. La puntuación de estilo refleja la forma en la que el alumno se comunicó, incluidos el ritmo, la claridad, las palabras que rellenan, la intensidad de la oración y la energía vocal. Los autores establecen el peso de cada componente al configurar el escenario; una configuración común es 70% Conocimiento y 30% Estilo. Consulte [comprender el informe de rendimiento de Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

8. **¿Pueden los alumnos descargar su informe de rendimiento?**
Sí. Además de ver el informe en pantalla, los alumnos pueden descargarlo como PDF para conservarlo en sus propios registros o compartirlo con un responsable.

9. **¿Puede un alumno reintentar un juego de funciones?**
Sí. Los alumnos pueden intentar desempeñar una función tantas veces como quieran. Cada intento es una sesión nueva e independiente y genera un nuevo informe de rendimiento. Sólo la primera sesión de un mes civil consume un crédito de la UMA.

10. **¿Pueden los alumnos enviar sus sesiones para revisión humana?**
No.

11. **¿Está disponible Virtual Coach en dispositivos móviles?**
Virtual Coach es compatible con la web de escritorio y móvil de Adobe Learning Manager, así como con las API. No está disponible en la aplicación móvil de Adobe Learning Manager (iOS/Android) en la versión actual.

12. **¿Se usan los datos del alumno para entrenar la IA?**
No. Virtual Coach se aloja en una infraestructura compatible con el RGPD y no se utilizan datos personales de alumnos para formar modelos de IA.

13. **¿Cuál es la diferencia entre una ayuda de trabajo y un módulo de curso para Virtual Coach?**
Una ayuda de trabajo es un recurso independiente y bajo demanda al que los alumnos pueden acceder directamente desde el catálogo en cualquier momento sin estar inscritos en un curso. Se accede a un módulo de curso como parte de una secuencia estructurada de cursos con inscripción, seguimiento de la finalización y evaluación formal. Se puede publicar el mismo juego de roles como ayuda de trabajo y agregarlo a varios cursos simultáneamente. Consulte [agregar un juego de roles de entrenador virtual a un curso](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md).

14. **¿Cómo debemos empaquetar Virtual Coach al lanzar un nuevo proceso o producto?**
Empaquete el juego de roles dentro de un curso o viaje de aprendizaje junto con el contenido de formación relacionado, y distribuya el vínculo del curso por correo electrónico u otras comunicaciones de administración de cambios. Virtual Coach funciona mejor posicionado como la última milla de formación: el punto de control justo después de que los alumnos completen el contenido relacionado, donde demuestran que pueden aplicarlo, en lugar de como una actividad independiente.

15. **¿Es compatible Virtual Coach con implementaciones descentralizadas o de API?**
Las API públicas para obtener cursos y ayudas de trabajo también obtienen cursos de formación virtual y ayudas de trabajo. El filtro `jobAidType` está disponible para obtener ayudas de trabajo de Virtual Coach específicamente. El contenido de Virtual Coach se admite en el reproductor descentralizado, y los cursos y las ayudas de trabajo que contienen Virtual Coach funcionan en el reproductor Fluidic.

Si tiene alguna pregunta sobre la creación y configuración de un juego de roles, consulte esta página de preguntas frecuentes.
