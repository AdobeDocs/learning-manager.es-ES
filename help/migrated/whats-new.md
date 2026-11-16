---
description: Obtenga más información sobre las nuevas funciones de la versión de diciembre de 2026 de Adobe Learning Manager, como los gráficos de Report Builder y Virtual Coach.
jcr-language: en_us
title: Novedades de la versión de diciembre de 2026 de Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 413b0a29bcacbf1d523990dd7d96fdbb9fad3907
workflow-type: tm+mt
source-wordcount: '4684'
ht-degree: 0%
---

# Novedades de la versión de diciembre de 2026 de Adobe Learning Manager

Esta versión de Adobe Learning Manager presenta una variedad de nuevas funciones y mejoras destinadas a agilizar la plataforma y ampliar sus capacidades. Estas actualizaciones simplifican los flujos de trabajo diarios, mejoran la forma en que se organiza y distribuye el contenido de aprendizaje, y hacen que la experiencia general sea más coherente e intuitiva.

## Gráficos y paneles de Report Builder

Adobe Learning Manager ahora admite gráficos y paneles en Report Builder, lo que permite a los administradores visualizar los datos de los informes directamente en la plataforma. Los administradores pueden crear gráficos a partir de columnas de informes, con agregación y filtrado disponibles en cada gráfico.

Report Builder admite los siguientes tipos de gráficos:

* Gran número
* Gráfico de líneas
* Gráfico de barras
* Gráfico circular
* Tabla dinámica

Un tablero de informes contiene gráficos creados a partir de un informe. Un panel personalizado combina gráficos de varios informes, como datos de inscripción y de usuario, y admite hasta 20 widgets. Los gráficos que pertenecen a un informe se comparten cuando se comparte el informe. Esto ayuda a los administradores a mantener los datos del informe actual en una vista en lugar de volver a ejecutar los informes. Los gráficos muestran hasta 10.000 puntos de datos y las tablas dinámicas muestran hasta 100 filas y 100 columnas. Si un gráfico supera un límite, aplique filtros para reducir los resultados. Los paneles aún no se pueden exportar.

## Informes de Insights Agent en Report Builder

Ahora los administradores pueden seguir trabajando con las respuestas de Insights Agent en Report Builder. Cuando Insights Agent responde a una pregunta, Report Builder asigna la misma consulta a sus propios campos en un paso paralelo. Los administradores pueden abrir, revisar, editar y guardar el informe. Desde allí, puede utilizar las mismas funciones de Report Builder que cualquier otro informe, como las suscripciones.

Si parte de una pregunta no se puede expresar con campos de Report Builder, el informe muestra esa parte como un hueco. Si la parte que falta es central para la pregunta, el informe no se ofrece. Las consultas complejas pueden producir resultados reducidos, por lo que debe revisar cada informe antes de confiar en él.

## Integración con Adobe Experience Manager Assets

Adobe Learning Manager ahora se integra con Adobe Experience Manager Assets, lo que permite a los autores acceder a contenidos de aprendizaje y recursos de imágenes aprobados y utilizarlos directamente desde un repositorio centralizado. Esto elimina el paso de carga y descarga manual entre el equipo que administra los activos en el administrador de activos digitales (DAM) y el equipo que crea cursos en Adobe Learning Manager.

Qué cambia:

* **Acceder a activos aprobados:** Los autores buscan y seleccionan activos de Experience Manager Assets sin salir de Adobe Learning Manager, de modo que los cursos utilizan archivos aprobados actuales en lugar de copias locales que pueden quedar obsoletas.
* **Mantener los activos del curso actualizados:** Cuando un activo cambia en el DAM, la actualización puede fluir a los cursos que lo usan automáticamente, lo que mantiene la coherencia del contenido a medida que se revisan los activos.
* **El acceso sigue los permisos existentes:** Los autores solo ven los activos a los que ya tienen acceso en Experience Manager Assets, por lo que la exploración en Adobe Learning Manager respeta los mismos permisos que el propio DAM.

El resultado es una ruta única y controlada del recurso al alumno, con menos trabajo manual y menos discrepancias de versiones.

## Mejoras de envío de archivos

Los módulos de envío de archivos ahora admiten envíos de equipos y evaluación basada en rúbricas. Una nueva configuración también controla si se requiere la aprobación del instructor para los envíos.

### Envíos de equipo

Los instructores ahora pueden crear equipos para el envío de archivos. Cada equipo envía un archivo para todo el equipo. El instructor evalúa el envío una vez y el resultado se aplica a todos los miembros. Los equipos se forman de dos maneras: Los instructores los crean manualmente o un proceso programado los crea antes de la fecha de inicio de la instancia, en función de los miembros por equipo o número de equipos.

Los instructores administran los equipos en una nueva página de **administración de equipos** y revisan el trabajo en una página de envíos de equipos. Los instructores también pueden retirar un envío aprobado para desbloquear el equipo cuando se requieran cambios, como cuando un miembro del equipo se va. Un equipo tiene hasta 100 miembros. Los alumnos pueden ver su equipo, sus miembros y el resultado de la evaluación. Los módulos de equipo no se pueden añadir ni eliminar después de publicar un curso.

### Evaluaciones basadas en rúbricas

Los autores ahora pueden definir una rúbrica, denominada plan de evaluación, para los módulos de envío de archivos. Una rúbrica apoya preguntas objetivas con opciones puntuadas y preguntas subjetivas con revisión escrita.

Los autores también pueden configurar las siguientes opciones:

* Si los alumnos ven las preguntas de evaluación basadas en la rúbrica antes de enviar
* Si la puntuación es una puntuación global o una puntuación para cada criterio

Cada pregunta se puede marcar como necesaria y configurar para permitir los comentarios del revisor. Una evaluación basada en rúbricas tiene capacidad para 100 preguntas y los autores introducen preguntas por separado para cada configuración regional. Después de publicar un curso, solo puede cambiar el texto de la pregunta.

### Aprobación del instructor o finalización automática

Los autores ahora pueden elegir si los envíos de archivos requieren la aprobación del instructor o se completan automáticamente. Este ajuste es independiente del plan de evaluación.

## Model Context Protocol server for Learner Assistant

ALM permite a los alumnos acceder al aprendizaje en las herramientas que ya utilizan a través de un servidor de Protocolo de contexto de modelo (MCP). Los alumnos pueden acceder a Learning Manager desde cualquier lugar, incluidos ChatGPT, Claude y agentes personalizados. Configure el servidor en la aplicación de administración de integración para dar a los administradores acceso a seis herramientas básicas para los alumnos. Estas incluyen dos herramientas de Asistente del alumno: Agente de respuestas y ruta de aprendizaje personalizada

El servidor proporciona las siguientes capacidades:

* Buscar
* Enumerar inscripciones
* Obtener objeto de aprendizaje
* Obtener perfil de usuario
* Responder a pregunta de contenido de aprendizaje
* Ruta de aprendizaje personalizada

Los administradores pueden editar la descripción de cada herramienta para añadir ejemplos específicos de la organización. Los clientes leen los detalles de autorización de los metadatos del servidor, por lo que la instalación solo necesita un ID y un secreto de cliente.

## Tiras personalizadas de edición y marca de rutas de aprendizaje

Los alumnos ahora pueden eliminar los temas o cursos sugeridos en un solo paso, además de la opción existente para perfeccionar las listas de temas y cursos a través del chat.

Ahora los administradores pueden cambiar la posición de la tira de rutas de aprendizaje personalizadas en la página de inicio del alumno a través de la página Marca.

## Practica habilidades con el juego de roles en Virtual Coach

Adobe Learning Manager ahora ofrece Virtual Coach, una solución de orientación y juego de roles basada en IA que permite a los alumnos practicar conversaciones realistas en el lugar de trabajo antes de enfrentarse a ellos en el trabajo. Algunos ejemplos son las objeciones de ventas, las ampliaciones de clientes y las revisiones del rendimiento.

Los autores crean escenarios a partir de sus propios materiales de referencia mediante plantillas o un asistente de IA, y los alumnos hablan con un personaje de IA que se adapta a sus respuestas en tiempo real. Después de cada sesión, los alumnos obtienen una puntuación instantánea y comentarios de orientación sobre los conocimientos y el estilo de comunicación, medidos en función de los criterios definidos por el autor.

Virtual Coach admite nueve idiomas y se puede utilizar como ayuda de trabajo independiente o incrustarse en un curso.

## Citas de rutas de aprendizaje en el Asistente del alumno

Las respuestas del Asistente del alumno ahora indican la ruta de aprendizaje que contiene un curso de origen, junto con el propio curso. Los alumnos abren la página Resumen del curso o Ruta de aprendizaje de la cita. Las respuestas extraídas de una ayuda de trabajo incluyen un vínculo de descarga. Esto ayuda a los alumnos a encontrar la formación que responda a sus preguntas.

## Configuraciones del Asistente de IA

El Asistente del administrador ofrece dos agentes: Agente de información y agente de conocimientos. Se pueden configurar individualmente. El Asistente del alumno ofrece tres agentes: Agente de conocimiento, Agente de respuesta y Agente de ruta de aprendizaje. Se pueden configurar junto con la configuración del catálogo.

## Webhooks para ediciones de instructores en instancias de objetos de aprendizaje

El webhook de modificación de instancias de objetos de aprendizaje ahora se activa cuando un instructor edita una sesión de clase virtual, además de los cambios de administrador y autor. Los cambios, como los intervalos de sesión, el lugar de celebración y el límite de inscripción, lo activan. Los clientes sin periféricos pueden recuperar los detalles de la sesión a través de la API pública y pasar las actualizaciones a los alumnos.

## Cursos con varios inscritos en el widget de cumplimiento

El widget de cumplimiento muestra ahora todas las instancias de un curso de inscripción múltiple que debe completar un alumno. Cada entrada muestra el nombre de la instancia. Si una instancia tiene una fecha límite, se oculta cualquier instancia sin fecha límite. El punto final de inscripciones de la API pública admite el mismo comportamiento mediante un parámetro opcional.

## Reenviar invitaciones a sesiones de clase virtual

Ahora, los administradores con permiso de edición de curso pueden volver a enviar una invitación de sesión desde la página de instancias. Seleccione **Reenviar**, busque el alumno y envíelo. La opción está disponible para sesiones de clase virtual actuales y futuras. En el caso de los alumnos de varias instancias, la invitación solo se dirige a la instancia seleccionada. A los alumnos que no estén inscritos en la sesión se les omitirá una advertencia.

## Asistencia automática desde las vistas de grabación de Adobe Connect

Adobe Learning Manager ahora marca la asistencia cuando un alumno reproduce la grabación de una sesión de clase virtual perdida. Una integración programada extrae los datos del visor de Adobe Connect y compara el tiempo de reproducción con los criterios de finalización establecidos para la cuenta. Los administradores establecen la programación en la aplicación de administración de integración. Adobe Learning Manager solo tiene en cuenta el tiempo de visualización real al determinar la asistencia, por lo que omitir una grabación no cuenta en los criterios de finalización.

## Email Builder para cursos e instancias

Email Builder en Adobe Learning Manager permite a administradores y autores crear plantillas de comunicación de alumno de marca. En la versión de diciembre de 2026 de Learning Manager, la experiencia completa de Email Builder está disponible para los correos electrónicos de nivel de curso y de instancia. Los autores pueden personalizar estos mensajes de correo electrónico heredando los diseños y el formato definidos por los administradores.

Con Email Builder, puedes hacer lo siguiente:

* Crear diseños de correo electrónico reutilizables
* Aplicar marca de organización
* Personalizar banners y firmas
* Definir fuentes y colores predeterminados
* Estandarizar la comunicación entre cursos y programas de aprendizaje

Los administradores crean plantillas y diseños de correo electrónico para toda la cuenta. Los autores personalizan los correos electrónicos en los niveles de curso e instancia sin volver a crear plantillas desde cero.

La configuración de banners y firmas se ha movido. Anteriormente, esta configuración aparecía en una ficha **Configuración** independiente. Esa pestaña se ha quitado y **Banner** y **Firma** aparecen ahora en **Diseño global**.

### Jerarquía de Email Builder

Email Builder utiliza una jerarquía. Cada nivel hereda de su nivel primario y permite la personalización local.

| **Nivel** | **Lo que proporciona** | **Quién lo personaliza** |
|-------------------|---------------------------------------------------------------------------------------------------------------------|-----------------------|
| Diseño de cuenta | Marca, fuentes, colores y estructura de encabezado y pie de página | Administradores |
| Plantilla de cuenta | Estilo global del correo electrónico, componentes de mensajería comunes y marca compartida | Administradores |
| Plantilla del curso | Correos electrónicos específicos del curso, como mensajes de inscripción, recordatorios de cursos, correos electrónicos de finalización y notificaciones de sesiones | Autores |
| Plantilla de instancia | El nivel más alto de personalización, como mensajes específicos de la cohorte, específicos de la sesión o regionales | Autores |

Todos los cursos pueden heredar de las plantillas de cuenta. Los correos electrónicos de los cursos heredan el diseño de la organización y permiten la personalización del contenido.

### Herencia de diseño

Una plantilla se vincula al diseño disponible más cercano. Una plantilla de nivel de instancia se vincula a un diseño de nivel de instancia, si existe. Si no existe ninguna, la plantilla se vincula al diseño principal más cercano. Puede ver de qué nivel procede un diseño.

Cuando una plantilla está vinculada a un diseño:

* La promoción de marca fluye en la plantilla automáticamente.
* Los autores actualizan solo el contenido.
* El diseño reduce la duplicación entre mensajes.

Puede desvincular una plantilla de su diseño. Después de desvincular una plantilla:

* La plantilla mantiene su diseño existente.
* Las futuras actualizaciones de diseño no afectarán a la plantilla.
* La plantilla se puede editar de forma independiente.

La herencia de diseños depende de los diseños principales disponibles. Cuando existen ambos niveles, los mensajes de correo electrónico de nivel de instancia reemplazan las plantillas de nivel de curso.

### Flujo de trabajo de administrador y autor

Los administradores utilizan plantillas de nivel de cuenta para mantener la coherencia de los mensajes en toda la cuenta, que gestionan creando un diseño y una plantilla y, a continuación, publicando la marca.

Los autores utilizan plantillas de nivel de instancia cuando las cohortes necesitan mensajes diferentes, que gestionan a través de instancias de curso.

### Disponibilidad de Email Builder para correos electrónicos de curso e instancia

Si el Generador de correo electrónico ya está habilitado para su cuenta, recibirá los nuevos cambios automáticamente y no tendrá que hacer nada. La funcionalidad de correo electrónico existente sigue funcionando independientemente de las actividades de migración de Email Builder.

## Atributos personalizados de alumnos en la interoperabilidad de herramientas de aprendizaje

Adobe Learning Manager ahora lee los atributos del alumno personalizados a través del extremo opcional de Names and Role Provisioning Services de Learning Tools Interoperability. También las lee de la solicitud de inicio. Los atributos como país o ciudad se almacenan en campos de perfil agrupables. Los parámetros de inicio requieren un prefijo para que Adobe Learning Manager los reconozca. Algunos sistemas de aprendizaje, como Moodle, no admiten este punto final.

## Notificaciones del instructor del foro de debate

Los clientes descentralizados ahora pueden enviar a los instructores y responsables de cohorte un resumen de la actividad del panel de debates. Con la API, puede añadir suscriptores a un tablero. Reciben nuevas publicaciones, comentarios y respuestas en un solo correo electrónico, en el intervalo que establezca. Los me gusta y no me gusta no están incluidos. La función se activa a través de la API.

## Clasificación de relevancia en la búsqueda del catálogo del administrador

La búsqueda por catálogo en la vista de administrador ahora clasifica los resultados por relevancia, utilizando el mismo servicio de búsqueda que para el alumno y el administrador en otro lugar. Primero aparece una coincidencia exacta, como un nombre de catálogo con una fecha específica, seguido de coincidencias parciales. La lista de sugerencias al escribir sigue el mismo orden.

## Sincronización de cancelación de sesión desde Adobe Workfront

Las sesiones canceladas en Adobe Workfront se transfieren a Adobe Learning Manager a través del proceso de migración, sin pasos manuales. La migración agrega una columna opcional **Estado** que acepta **Activo** o **Cancelado**. Un valor en blanco no cambia la sesión. Una cancelación realizada mediante migración se comporta como una realizada en la interfaz de Learning Manager. Los alumnos, instructores, administradores, autores y responsables reciben los mismos mensajes de correo electrónico de cancelación.

Se aplican dos comportamientos a las sesiones canceladas:

* La migración no aplica los cambios de detalle a una sesión cancelada y devuelve un error de validación para esas filas.
* Si establece el estado en Activo, se reactivará la sesión y, a continuación, podrá actualizar sus detalles o cancelarla de nuevo.

Las actualizaciones de sesión siguen funcionando como antes.

## Límite de caracteres para los nombres

Adobe Learning Manager ahora acepta nombres de hasta 255 caracteres, frente a los 63. Esto se aplica a los usuarios añadidos en la interfaz, a través de la importación de CSV y en el registro automático, de modo que las sincronizaciones de usuarios de otros sistemas ya no fallan en nombres largos.

Esto resulta especialmente útil cuando migra usuarios desde un sistema externo o automatiza la creación de usuarios.

A partir de la versión de diciembre de 2026, el campo de nombre acepta hasta 255 caracteres. Las versiones anteriores aceptaban un máximo de 63 caracteres.

>[!NOTE]
>
>El límite se aplica a todos los usuarios de su cuenta, independientemente de su función. Este cambio no afecta a los usuarios existentes ni a sus nombres.

Puede introducir nombres largos al añadir o editar usuarios de las siguientes maneras:

* Añadir un solo usuario en la interfaz de administración
* Editar un usuario existente
* Importar usuarios con un archivo CSV
* Registro de usuarios mediante el registro automático
* Agregar usuarios externos

Los nombres largos pueden ser más anchos que el espacio disponible en algunas partes de la interfaz. Para que el diseño sea legible, Adobe Learning Manager acorta los nombres largos en las siguientes áreas compactas:

* Celdas de tabla
* Elementos de la lista desplegable
* Resultados de la búsqueda

Para ver el nombre completo, pase el puntero sobre el nombre abreviado.

## Información de insignia para cursos y rutas de aprendizaje

Cuando los autores añaden un curso o una ruta de aprendizaje, aparece una ventana con información sobre insignias en la que se enumeran los cursos y las rutas de aprendizaje existentes. La ventana muestra el nombre, el tipo (curso o ruta de aprendizaje), el estado de la publicación y el formato del curso, por ejemplo, con ritmo personalizado, virtual, de clase o mixto.

## Mejoras no registradas

Learning Manager ahora permite el acceso controlado al contenido de aprendizaje sin necesidad de que los usuarios inicien sesión. Los administradores pueden especificar qué catálogos son públicos, mientras que los autores pueden determinar qué cursos y módulos están disponibles sin una cuenta. El contenido público se publica como páginas rastreables y legibles por IA, lo que hace que la academia sea descubrible a través de los motores de búsqueda y los asistentes de IA, como Claude y ChatGPT. Se realiza un seguimiento del uso anónimo por visitante y se informa por separado del uso al que se ha iniciado sesión.

### Consumo de contenido sin iniciar sesión

Los visitantes de tu academia pública ahora pueden reproducir el contenido seleccionado directamente desde la página de resumen del curso, sin necesidad de tener cuenta, correo electrónico ni formulario.

* **Activar o desactivar el acceso sin inicio de sesión:** Los administradores pueden activar o desactivar el consumo de contenido sin inicio de sesión en toda la cuenta.
* **Hacer que los cursos o módulos estén disponibles sin iniciar sesión:** Los autores pueden hacer que un curso completo esté disponible sin iniciar sesión o abrir solo módulos específicos, como un módulo de introducción gratuito antes del contenido avanzado cerrado.
* **Heredar la configuración de los cursos:** Las certificaciones y rutas de aprendizaje siguen la configuración de los cursos que contienen, sin necesidad de configuración adicional.
* **Ver contenido sin iniciar sesión:** Los alumnos no autenticados pueden ver el contenido disponible sin iniciar sesión en su cuenta.
* **Solo contenido con ritmo personalizado:** El contenido con licencia de terceros y el contenido del catálogo adquirido no pueden estar disponibles sin iniciar sesión.
* **Informes sobre consumo anónimo:** Se puede generar un informe sobre consumo mensual no registrado.
* **Habilitar aprendizaje sin inicio de sesión en todas las plataformas:** El consumo de contenido sin inicio de sesión es compatible con Adobe Learning Manager nativo en la web y dispositivos móviles, en implementaciones descentralizadas y en academias basadas en widgets de Adobe Experience Manager Sites.

### Elegir qué catálogos son públicos

Los administradores ahora pueden elegir los catálogos específicos que aparecen en la academia pública. Solo los visitantes anónimos pueden explorar esos catálogos e indexarlos los motores de búsqueda y los asistentes de inteligencia artificial, por lo que los cursos de pruebas o el contenido interno siguen siendo privados.
 
### Buscar en motores de búsqueda y asistentes de inteligencia artificial (Beta)

Adobe Learning Manager ahora puede hacer que tu academia pública sea descubrible por motores de búsqueda como Google y por asistentes de inteligencia artificial como ChatGPT, Claude y Gemini. Los cursos pueden aparecer entonces en los resultados de búsqueda y en las respuestas generadas por IA, que se atribuyen a la academia.

* Los controles de nivel de cuenta permiten a los administradores decidir si los rastreadores pueden acceder a la academia pública y si su contenido se puede indizar.
* Cada academia recibe su propio mapa del sitio y robots.txt, generado automáticamente a partir de los catálogos que has hecho públicos.
* Las páginas se preprocesan para los rastreadores, por lo que los asistentes de inteligencia artificial que no ejecutan JavaScript pueden leerlas.
* Los rastreadores solo ven lo que un visitante puede acceder. El contenido cerrado nunca se expone.
* Meta title, description y datos estructurados: Adobe Learning Manager los genera automáticamente para cada curso, ruta de aprendizaje y certificación, en función de los metadatos de aprendizaje.

>[!NOTE]
>
>El descubrimiento de inteligencia artificial y búsquedas en Adobe Learning Manager nativo requiere un dominio personalizado. Las implementaciones descentralizadas tendrán que implementar partes de la configuración en su propio entorno.

## Retirar un curso sin dejar inaccesible una ruta de aprendizaje

Un curso retirado o una ruta de aprendizaje anidada se elimina del objeto de aprendizaje de nivel superior, que permanece abierto para nuevas inscripciones. Retirar un curso ya no hace que la ruta de aprendizaje sea inaccesible.

## URL de página no conectada para perfiles de autorregistro

Los perfiles de registro automático permiten a los usuarios externos, como socios o miembros de varias organizaciones, crear sus propias cuentas de Adobe Learning Manager. Cada perfil ahora puede tener su propia URL de menú no conectado que se puede compartir, integrada en Experience Builder.

Cuando los usuarios seleccionan **Registrarse** en una página a la que se accede a través de esa dirección URL, se agregan al perfil al que pertenece la dirección URL. Esto mantiene a los usuarios de diferentes organizaciones, como agencias independientes o empresas asociadas, en perfiles independientes.

## Almacenar fechas de último acceso para inscripciones de rutas de aprendizaje

Adobe Learning Manager ahora le permite adjuntar metadatos personalizados, como la fecha del último acceso, a una inscripción de ruta de aprendizaje. Puede configurarlo y leerlo a través de la API, que le ayuda a realizar un seguimiento del acceso con límite de tiempo a las rutas de aprendizaje que asigne.

Las inscripciones a los cursos ya admiten una fecha de último acceso a través de la API, que controla el tiempo durante el que un alumno puede acceder al curso. Las inscripciones de rutas de aprendizaje ahora ofrecen un campo de metadatos genérico, por lo que puede almacenar una fecha de último acceso o cualquier otro valor del que desee realizar un seguimiento.

## Exportación de informes del Report Builder con la API de trabajos

Esta versión de Adobe Learning Manager agrega un nuevo tipo de trabajo de API de trabajos, `generateCustomReport`. Pase un ID de informe para exportar automáticamente cualquier informe que haya creado en Report Builder.

Combinado con el nuevo conjunto de datos de pruebas de L2 en Report Builder, ahora puede:

* Exporta datos de cuestionarios de nivel de pregunta (L2) en varios cursos y módulos en un solo informe, en lugar de ejecutar `generateQuizReport` una vez por curso.
* Automatiza las exportaciones periódicas, como una exportación incremental diaria a tu almacén de datos o herramienta de inteligencia empresarial.

Los tipos de trabajo existentes, incluido `generateQuizReport`, no se modifican.

## Cambios de encabezado de columna en informes descargados

El Report Builder ahora incluye el nombre del conjunto de datos en los encabezados de columna predeterminados de los informes descargados, por lo que Nombre del conjunto de datos del objeto de aprendizaje aparece como **Objeto de aprendizaje - Nombre** en lugar de **Nombre**. Para las columnas agregadas, el encabezado también incluye la función, como **Recuento del objeto de aprendizaje - ID**. Si escribe un nombre personalizado en el campo **Alias** de una columna, ese alias se utiliza como encabezado y no cambia.

Después de la actualización, los informes existentes sin alias personalizados muestran los encabezados actualizados, mientras que los datos de informes, los filtros y las programaciones no se ven afectados. Si los scripts, hojas de cálculo, paneles de inteligencia empresarial o integraciones hacen referencia a columnas por encabezado, actualícelos con los nuevos nombres o establezca un alias personalizado para mantener un encabezado específico.

## Centro en vivo

Live Hub ahora está disponible de forma general para los clientes de Ultimate y permanece en versión beta para los clientes de Prime.

## Compatibilidad multilingüe para subtítulos opcionales en Live Hub

Los subtítulos opcionales en Live Hub se han mejorado para admitir más idiomas. Los instructores ahora pueden seleccionar el idioma de los subtítulos en **Configuración de la sala**, en función del idioma que se hable durante la sesión.

Los subtítulos se generan automáticamente en el idioma seleccionado y se muestran en un panel dedicado que se actualiza continuamente a medida que habla el instructor. Todos los participantes ven los subtítulos en el idioma seleccionado por el instructor.

Esta mejora mejora mejora la accesibilidad para los participantes en diferentes idiomas y les ayuda a seguir las sesiones en directo de forma más eficaz.

## Interfaz Live Hub localizada y reproductor de grabación

La interfaz de Live Hub aparece ahora en el idioma seleccionado para la interfaz de usuario de Learning Manager. Las etiquetas y los encabezados a lo largo de la sesión, incluidos el chat, los asistentes, las encuestas, las salas de grupo de trabajo y la configuración, aparecen en el idioma elegido por el usuario. Live Hub admite los mismos 18 idiomas de interfaz que Learning Manager, incluido el inglés. El reproductor de grabación también está localizado, por lo que elementos como las encuestas aparecen en el idioma del curso. Por ejemplo, una grabación de un curso de alemán muestra la interfaz del reproductor en alemán.

Esto proporciona a los participantes globales una experiencia coherente en toda la plataforma y en las grabaciones de las sesiones.

## Sesiones de Live Hub con hasta 5000 asistentes

Live Hub ahora admite sesiones a gran escala con hasta 5000 asistentes, lo que permite a las organizaciones realizar sesiones de formación a gran escala. Los autores pueden elegir una capacidad de 5000 asistentes al añadir un módulo de clase virtual a un curso. Live Hub configura automáticamente la sala en función del tamaño de la audiencia y aplica restricciones de interacción específicas.

En sesiones grandes, se aplican las siguientes capacidades y comportamientos:

* El acceso a la cámara, el uso compartido de la pantalla y la funcionalidad de la pizarra están limitados a los instructores.
* Las salas de grupo de trabajo no están disponibles.
* Grandes volúmenes de mensajes de chat simultáneos, reacciones y preguntas se distribuyen en lotes escalonados.
* Otras interacciones y capacidades, como las encuestas, los cuestionarios, la grabación y el seguimiento de la asistencia, funcionan como lo hacen en las sesiones regulares.

Esto permite a las organizaciones llevar a cabo grandes sesiones de formación en la misma plataforma, con una sala que se pueda ajustar al tamaño de audiencia previsto.

## Canales

Los canales ahora están disponibles de forma general para todos los clientes.

## Reserva de inscripción de grupo y administración de listas de espera

La reserva de inscripción de grupo y la administración de listas de espera proporcionan a los autores un control más preciso sobre quién puede inscribirse en los cursos de clase y clase virtual. Los autores pueden asignar puestos a grupos de usuarios específicos y establecer fechas abiertas de inscripción independientes para esos grupos y para todos los demás alumnos. También pueden activar la promoción automática de la lista de espera con una fecha límite, de modo que un puesto disponible pase al siguiente alumno apto. Reservar todos los puestos restringe un curso a los grupos seleccionados.

## Compatibilidad con varias conexiones de Zoom

Adobe Learning Manager ahora admite varias conexiones de Zoom en una sola cuenta, lo que permite a las organizaciones administrar sesiones de clase virtual en diferentes cuentas de Zoom.

Los administradores de integración pueden configurar varias conexiones de Zoom y asignarlas a funciones o grupos de usuarios específicos. Al crear o editar una sesión de curso, los autores pueden seleccionar las conexiones de Zoom disponibles para ellos, y cada sesión utilizará una conexión.

Esta mejora proporciona una mayor flexibilidad para las organizaciones que utilizan varias cuentas de Zoom, especialmente en los siguientes casos:

* **Formación específica del departamento**: Administre cuentas de Zoom independientes para diferentes departamentos o equipos dentro de la misma cuenta de Learning Manager.
* **Formación externa y de partners**: Asigne conexiones de Zoom dedicadas a socios o grupos de usuarios específicos para respaldar sus sesiones de formación.
* **Acceso controlado**: Restrinja la disponibilidad de las conexiones de Zoom según las funciones o los grupos de usuarios, lo que garantiza que los autores puedan seleccionar solo las conexiones asignadas a ellos.
* **Administración de conexiones simplificada**: Permite a los administradores de integración administrar de forma centralizada varias conexiones de Zoom sin que esto afecte a las sesiones existentes.

## Integración del Explorador de exámenes seguro para los cuestionarios

Adobe Learning Manager ahora se integra con el navegador de exámenes seguro para pruebas nativas, lo que proporciona un entorno seguro y controlado para realizar las evaluaciones. Los administradores pueden habilitar la integración en el nivel de cuenta y cargar un archivo de configuración del Explorador de exámenes seguros (.seb) para definir las restricciones de evaluación. A continuación, los autores pueden elegir qué pruebas individuales requieren un navegador de exámenes seguro.

Cuando los alumnos intentan realizar una prueba que requiere el Explorador de examen seguro, se les solicita que inicien el explorador. Esto bloquea el acceso a otros navegadores y aplicaciones mientras dure la evaluación, de acuerdo con las restricciones definidas por el administrador. Se solicita a los alumnos que no lo tengan instalado que lo descarguen.

**Dónde ayuda:**

* **Evaluaciones de certificación:** Realiza pruebas en las que sea importante restringir el acceso a los recursos externos.
* **Formación de cumplimiento:** Asistencia para evaluaciones controladas de requisitos normativos y de formación obligatorios.
* **Evaluaciones de alto riesgo:** Reducir las oportunidades de acceso a aplicaciones o recursos no autorizados durante evaluaciones importantes.
* **Administración flexible de la evaluación:** Permite a los autores solicitar el Explorador de examen seguro solo para los cuestionarios que necesiten restricciones adicionales.

## Correcciones de accesibilidad en Live Hub

Las correcciones de accesibilidad de Live Hub mejoran la experiencia de los usuarios de tecnologías de asistencia y la navegación mediante el teclado.

* **Lectores de pantalla**: Los controles y el contenido ahora se anuncian correctamente con NVDA, JAWS, VoiceOver y TalkBack.
* **Desplazamiento con teclado**: Se puede acceder a cada elemento interactivo en un orden de tabulación lógico con un indicador de enfoque visible, el enfoque ya no se detiene y hay disponible un vínculo de omisión de navegación.
* **Subtítulos opcionales**: Las sesiones en directo muestran subtítulos en tiempo real, las grabaciones admiten la carga y el cambio de subtítulos, y el conmutador de subtítulos se puede utilizar desde el teclado.
* **Contraste de color**: Los componentes de texto y de interfaz de usuario ahora cumplen las proporciones de contraste requeridas, y hay disponible un tema de alto contraste.
* **Zoom y reflujo**: El contenido y la funcionalidad se conservan con un zoom del navegador del 200 %, y Live Hub funciona con lupas de pantalla.

## Cambios en la API de la versión de diciembre de 2026 de Adobe Learning Manager

### Ordenación de API de marcadores y gestión de contenido retirado

Los alumnos pueden marcar cursos de formación para volver a consultarlos más adelante. Anteriormente, las API de marcadores devolvían los cursos de formación guardados sin un orden específico, lo que impedía que las integraciones descentralizadas mostraran primero los cursos de formación guardados más recientemente. Los marcadores de objetos de aprendizaje retirados también permanecían en la lista y generaban errores de tipo &quot;Página no encontrada&quot;.

Esta actualización corrige ambos problemas:

* Los marcadores ahora se devuelven primero el más reciente.
* Los marcadores de objetos de aprendizaje retirados ya no se devuelven.

No se añaden nuevos puntos finales, parámetros ni atributos de respuesta, por lo que las integraciones existentes siguen funcionando sin cambios.

### API para notificaciones del instructor del foro de debate

Esta versión incluye nuevas API compatibles con las notificaciones del instructor del foro de debate. Utilícelos para suscribir instructores y responsables de cohorte a paneles de debate y para controlar qué actividad aparece en los mensajes de correo electrónico de resumen.

### Compatibilidad con API para instancias de varias inscripciones en la aplicación del alumno

La API de inscripciones ahora admite instancias de varias inscripciones en la aplicación del alumno. Agregue el parámetro opcional `includeMultiInstanceEnrollments=true` a `GET /enrollments` para incluirlos. El valor predeterminado es `false`, por lo que las integraciones existentes, incluidas las implementaciones descentralizadas, siguen funcionando sin cambios.

### Fecha del último acceso para la inscripción en la ruta de aprendizaje

Ahora puede almacenar metadatos personalizados, como una fecha de último acceso, en una inscripción de ruta de aprendizaje y establecerlos y leerlos a través de la API. Esto le ayuda a realizar un seguimiento del acceso con plazos concretos a las rutas de aprendizaje que asigne.

* Establezca los metadatos en una inscripción existente o al inscribir un alumno, utilizando un token de administrador.
* Léalo con un token de administrador o de alumno.

Los metadatos son para su propio seguimiento. No controla el acceso y no se aplica a los cursos de la ruta.

### Tipo de trabajo de API de trabajos para exportaciones de Report Builder

La API de trabajos tiene un nuevo tipo de trabajo, `generateCustomReport`, que exporta cualquier informe de Report Builder guardado cuando se pasa su identificador de informe. Con el nuevo conjunto de datos de pruebas de L2, puede exportar datos de pruebas de nivel de pregunta en varios cursos en un informe y automatizar las exportaciones recurrentes.

Los tipos de trabajo existentes, incluido `generateQuizReport`, no se modifican.

### API para el conector de Zoom

Utilice estas API para ver y administrar conectores de Zoom en Adobe Learning Manager. Utilícelos para recuperar conexiones de Zoom existentes, guardar credenciales de Zoom, crear o actualizar conexiones y administrar permisos de acceso para grupos de usuarios y funciones personalizadas.

**Secuencia de API**

Utilice las API en esta secuencia:

| **Paso** | **API** | **Propósito** | **Autenticación** |
|------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------|
| 1 | `POST /ctr/authcred/uuid/20012    ` | Guarde las credenciales de Zoom. | Sesión del administrador de integración |
| 2 | `POST /ctr/app/esconnect  ` | Cree una conexión de Zoom o actualice una existente. | Sesión del administrador de integración |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Establezca los grupos de usuarios y las funciones personalizadas que pueden utilizar la conexión. | Sesión del administrador de integración |

**Autenticación y permisos**

Estas API utilizan la autenticación basada en sesión y requieren que el usuario inicie sesión como administrador de integración en Adobe Learning Manager.
