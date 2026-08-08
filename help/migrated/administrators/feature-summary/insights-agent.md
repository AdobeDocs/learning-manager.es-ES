---
description: Insights Agent es una función impulsada por IA de Adobe Learning Manager que permite a los administradores consultar datos de los alumnos mediante lenguaje natural.
jcr-language: en_us
title: Insights Agent (beta) en Adobe Learning Manager
source-git-commit: ed7e51ce51aa57144b8e519cb24a95ffbc436504
workflow-type: tm+mt
source-wordcount: '2632'
ht-degree: 1%

---


# Qué es Insights Agent

Insights Agent es una función impulsada por IA de Adobe Learning Manager que permite a los administradores consultar datos de aprendizaje mediante lenguaje natural. En lugar de descargar informes y manipular hojas de cálculo, escriba una pregunta, como &quot;¿Cuántos cursos se han creado en los últimos 3 meses en la cuenta? Dame un informe mensual&quot;, y Insights Agent recupera y presenta los datos directamente. Puede ver los resultados como texto, viñetas o tablas, o descargarlos como un archivo CSV.

Insights Agent está diseñado para reducir los pasos entre tener una pregunta de datos y obtener una respuesta. Los administradores que actualmente dependen de tablas dinámicas de Excel, equipos de IE o varios informes combinados pueden utilizar Insights Agent para obtener respuestas más rápido.

## Qué puede hacer Insights Agent

Puede utilizar Insights Agent para:

- Comprobar las métricas de finalización y cumplimiento normativo por región, departamento o grupo de usuarios
- Analizar tendencias de inscripción en cursos o rutas de aprendizaje
- Ver datos de progreso de un curso o ruta de aprendizaje específicos

Cada consulta devuelve una tabla con formato o un archivo CSV descargable, junto con una explicación en lenguaje sencillo de cómo se calcularon los resultados.

## Qué datos no admite Insights Agent

Los siguientes tipos de datos están fuera del ámbito de esta versión:

- Comentarios y datos de la encuesta
- Puntos e insignias de interacción
- Historial de auditoría y registros de cambios

Las consultas que hacen referencia a estos tipos de datos no devuelven resultados. Por ejemplo, &quot;¿Cuántos puntos de interacción se otorgaron el último trimestre?&quot; o &quot;¿Qué alumnos han obtenido una insignia de cumplimiento?&quot; devolverá un error o datos incompletos.

## Cómo funciona Insights Agent

Al introducir una pregunta, Insights Agent la procesa en cuatro etapas:

1. **Interpretación**: El agente analiza su pregunta para identificar qué datos se necesitan. Si alguna parte de la pregunta es ambigua, el agente le hace una pregunta aclaratoria antes de continuar

2. **Método**: El agente describe los pasos que tomó para encontrar su respuesta. Esta sección le ayuda a comprobar que los datos se recuperaron de la forma prevista, especialmente para consultas complejas.

3. **Resultados**: El agente presenta los datos como texto, viñetas o una tabla en función de la naturaleza de los resultados. Con los resultados se incluye un resumen en lenguaje sencillo. Cuando los resultados contienen 50 filas o menos, el resumen incluye información analítica sobre los datos. Cuando los resultados contienen más de 50 filas, el resumen proporciona estadísticas de nivel de columna.

4. **Descargar**: Puede descargar los resultados como un archivo CSV. Los informes de gran tamaño pueden tardar más tiempo; el agente le notifica cuando el archivo está listo.

La sección **Approach** es especialmente útil para consultas complejas. Muestra la lógica utilizada por el agente, similar a la que explicaría un analista de BI si ejecutara la consulta manualmente. La revisión del enfoque le ayuda a confirmar que el resultado es fiable antes de actuar en consecuencia.

## Hacer preguntas con Insights Agent

Utilice Insights Agent en Adobe Learning Manager para consultar datos de aprendizaje con preguntas en un lenguaje sencillo y obtener resultados como texto, tablas o archivos CSV descargables.

Insights Agent está disponible para los administradores en el panel de asistentes de IA en Learning Manager. El panel es redimensionable. Puede expandirlo para facilitar la lectura de los resultados. De forma predeterminada, el modo **Obtener información** está seleccionado al abrir el panel. También hay disponible un modo de **aprendizaje** independiente para preguntas de instrucciones sobre cómo usar el producto. El modo **Aprender** responde preguntas instructivas sobre cómo usar Learning Manager. Por ejemplo, &quot;¿Cómo puedo crear una ruta de aprendizaje?&quot; No consulta datos de alumnos.

### Haz una pregunta

Cuando el modo **Obtener información** está seleccionado de forma predeterminada, puedes empezar inmediatamente a consultar los datos de aprendizaje sin necesidad de ajustar el modo cada vez que accedas al asistente. Sin embargo, si alguna vez cambias al modo **Aprendizaje** para preguntas instructivas, asegúrate de volver a seleccionar **Obtener información** antes de enviar una consulta.

1. Seleccione el icono de asistente de AI en Learning Manager para abrir el panel de asistentes. La opción **Obtener información** ya está seleccionada de forma predeterminada.
   ![](assets/ask-question.png)

2. Escriba su pregunta en el campo de texto. Use un lenguaje sencillo. Por ejemplo: **¿Cuántos cursos se han creado en los últimos 3 meses?**

3. Selecciona **Enviar** o pulsa **Entrar** para enviar tu pregunta.

### Revisar la respuesta

Después de enviar la pregunta, Insights Agent procesa la solicitud y devuelve una respuesta con hasta cuatro partes:

1. **Desambiguación (si es necesario):** Si la pregunta contiene un término ambiguo, como &quot;actividad de aprendizaje&quot; o &quot;rendimiento&quot;, o &quot;Proporcionarme datos de rendimiento de los últimos 3 meses&quot;, el asistente muestra una lista de opciones y le pide que seleccione una antes de continuar. Seleccione la opción que mejor se adapte a lo que está buscando. Después de la pregunta inicial, no puede escribir instrucciones adicionales. La selección de una de las opciones proporcionadas es la única interacción disponible hasta que se inicia una nueva consulta mediante la interfaz de consulta. Solo puede responder a la desambiguación seleccionando una de las opciones proporcionadas; el seguimiento de texto libre no está disponible en esta versión.
   ![](assets/disambiguation.png)

2. **Método:** En la sección **Método** se describen los pasos que el agente ha seguido para recuperar los datos. Aparece como un panel desplazable debajo de la pregunta. Seleccione el icono de expansión para ver la aproximación completa. Si revisa esta sección, podrá confirmar que la lógica coincide con sus intenciones, especialmente para consultas complejas. Por ejemplo, si solicita &quot;todos los alumnos inscritos en el último año&quot;, el agente puede devolver la inscripción más reciente de cada alumno en lugar de todos los registros de inscripción. La sección **Método** explica las decisiones que tomó el agente al recuperar los datos. Si la lógica no coincide con su intención, inicie una nueva consulta con términos más específicos.
   ![](assets/approach.png)

3. **Resultados:** Insights Agent genera resultados como texto o tabla. Para los puntos de datos que se interpretan mejor en formato tabular, Insights Agent devuelve una tabla. Insights Agent no genera tablas ni gráficos. Para visualizar los datos, descargue el archivo CSV y ábralo en su herramienta preferida. Con los resultados se incluye un resumen en lenguaje sencillo. Cuando los resultados contienen 50 filas o menos, el resumen incluye información analítica sobre los datos. Cuando los resultados contienen más de 50 filas, el resumen proporciona estadísticas de nivel de columna. Por ejemplo, &quot;¿Qué cursos no tienen menos de 5 inscripciones que se hayan creado en el último año y quiénes son los autores?&quot;
   ![](assets/results.png)

Y la respuesta contiene el siguiente resumen:

***Resumen***

- *Cursos coincidentes: 102*
- *Intervalo de recuento de inscripciones: del 24 al 2019*
- *Promedio de inscripciones por curso coincidente: 589,6*
- *Inscripciones medias por curso coincidente: 553,5*

*Cuando la exportación esté lista, se proporcionará un vínculo de descarga para el informe completo.*

>[!NOTE]
>
>El formato del resumen varía en función de la naturaleza de los datos. A continuación se muestra un ejemplo de una respuesta de resumen. El resumen real variará en función de la consulta.


>[!NOTE]
>
>Insights Agent es probabilístico. Si ejecuta la misma consulta dos veces, la formulación de la respuesta o el orden de los resultados pueden variar ligeramente.


### Descargar el informe

Selecciona **Descargar informe** para exportar los resultados como archivo CSV. En el caso de conjuntos de resultados grandes, la descarga puede tardar más tiempo. El agente muestra un mensaje cuando el archivo está listo; también recibirá una notificación.

## Iniciar una nueva consulta

Cada sesión de Insights Agent gestiona una pregunta a la vez. Después de revisar los resultados, selecciona **Nueva pregunta** para hacer una pregunta diferente. También puedes seleccionar **Nuevo chat** en cualquier momento, incluso antes de recibir una respuesta, si deseas abandonar la consulta actual y comenzar de nuevo. No se puede escribir una pregunta de seguimiento en la misma sesión ni pedir al agente que perfeccione o amplíe los resultados devueltos.
![](assets/new-question.png)

>[!TIP]
>
>Si desea explorar datos relacionados, inicie una nueva consulta que incorpore lo aprendido en la primera. Por ejemplo, después de ver los totales de inscripción por región, inicie una nueva consulta para profundizar en las regiones de menor rendimiento.

## Proporcionar comentarios

Después de cada respuesta, seleccione el icono de miniaturas hacia arriba o hacia abajo para valorar el resultado. También puede especificar si el resultado fue inexacto, difícil de entender o tardó demasiado en devolverse. Estos comentarios ayudan a mejorar el agente con el tiempo.
![](assets/feedback.png)

## Prácticas recomendadas

- Empiece con una pregunta específica en lugar de una pregunta amplia. &quot;¿Cuál es la tasa de finalización del curso de formación sobre seguridad en el grupo de usuarios de Norteamérica?&quot; devuelve resultados más útiles que \&quot;Mostrar datos de finalización.&quot;
- Utilice términos exactos de Adobe Learning Manager al asignar nombres a contenido y grupos de alumnos. La guía de escritura de consultas enumera los términos correctos que se deben utilizar.
- Si el agente hace una pregunta aclaratoria, trátela como una señal para perfeccionar su consulta original la próxima vez. Cuanto más específica sea tu pregunta, menos aclaraciones serán necesarias.
- Revise la sección **Método** antes de actuar sobre los resultados para confirmar que la lógica del agente coincide con su intención.
- **Especifique si desea incluir o excluir alumnos en lista de espera**. De forma predeterminada, las consultas de recuento de inscripciones incluyen a los alumnos que están en una lista de espera junto con las inscripciones activas y confirmadas. Si solo necesita participantes activos, excluya explícitamente a los alumnos en lista de espera en la consulta. Por ejemplo: &quot;¿Cuántos alumnos se inscriben directamente en el curso de formación sobre seguridad, excepto los que están en lista de espera?&quot; El agente revelará en la sección Método que se aplicó la exclusión. Sin esta instrucción, los totales de inscripción pueden incluir una proporción significativa de alumnos en lista de espera que aún no han iniciado el contenido.
- **Recuentos de inscripción directa e indirecta**: Al consultar los datos de inscripción o finalización de un curso o una ruta de aprendizaje, Insights Agent distingue entre inscripciones directas (alumnos inscritos específicamente en ese curso o ruta de aprendizaje) e inscripciones indirectas (alumnos que accedieron al mismo contenido como parte de una ruta de aprendizaje o certificación). Si solicita específicamente inscripciones directas o indirectas, el agente devuelve el recuento correcto para cada tipo. Si la consulta no especifica directa o indirectamente, el agente puede devolver un recuento combinado. Para obtener recuentos separados, incluya la distinción explícitamente en la consulta. Por ejemplo: &quot;¿Cuántos alumnos están inscritos directamente o indirectamente en el curso de formación sobre seguridad?&quot;


## Diferencia entre Insights Agent y Report Builder

Ambas funciones utilizan los mismos datos de aprendizaje subyacentes, pero funcionan de forma diferente. Insights Agent es conversacional. Usted describe lo que desea y el agente lo recupera. El Report Builder está estructurado. Puede seleccionar conjuntos de datos, columnas y filtros para generar informes reutilizables.

| **Caso de uso** | **Recomendación** |
|---|---|
| Haz una pregunta rápida sobre los datos | Agente de información |
| Explorar datos sin conocer el esquema | Agente de información |
| Crear un informe estructurado y repetible | Generador de informes |
| Combinar varios conjuntos de datos con uniones personalizadas | Generador de informes |
| Programar suscripciones de informes | Generador de informes |
| Combinar conjuntos de datos con uniones personalizadas o modelado de datos avanzado | Generador de informes |

## Escribir consultas eficaces para Insights Agent

La calidad de la consulta afecta directamente a la calidad de los resultados que devuelve Insights Agent. Una consulta bien formada incluye tres ingredientes: contexto, por ejemplo, qué contenido y qué alumnos, ámbito, por ejemplo, estado, intervalo de tiempo y estado de usuario, y columnas, por ejemplo, los campos exactos que desea en la salida. Aprenda a utilizar la terminología, la estructura de consulta y las consultas de ejemplo correctas como puntos de partida.

### La fórmula de consulta de tres partes

Cada consulta eficaz de Insights Agent contiene estos tres componentes:

| **Componente** | **Qué podría significar** | **Ejemplo** |
|---|---|---|
| **Contexto** | El contenido y los alumnos sobre los que pregunta | &quot;...la ruta de aprendizaje de incorporación de nuevos empleados para alumnos de Sales Associate en la ubicación 101...&quot; |
| **Ámbito** | Estado de inscripción, intervalo de tiempo y estado del usuario | &quot;...que se hayan inscrito pero aún no se hayan completado, en los últimos 90 días...&quot; |
| **Columnas** | Todos los campos que desee incluir en la salida | &quot;...mostrar nombre, correo electrónico, ubicación y fecha de inscripción&quot; |

La ausencia de cualquiera de estos componentes puede dar lugar a resultados ambiguos o a una pregunta aclaratoria del agente.

### Utilizar los términos de ALM correctos

Insights Agent compara su consulta con el modelo de datos de Adobe Learning Manager. El uso de un término incorrecto puede devolver resultados incorrectos o ningún resultado. Utilice los términos de la columna de la izquierda a continuación.

| **Usar este término** | **No este** |
|---|---|
| **Ruta de aprendizaje** | Programa / seguimiento / plan de estudios |
| **Curso** | Módulo / clase / lección |
| **Certificación** | Insignia/certificado |
| **Alumno** | Estudiante/empleado |
| **Sesión** | Clase / fecha programada |
| **Grupo de usuarios** | Equipo / departamento / cohorte |
| **Campo activo** | Campo/atributo personalizado |
| **Inscripción** | Registro / asignación |
| **Finalización** | Terminado / terminado / pasado |
| **Etiqueta de catálogo** | Categoría/grupo de etiquetas |

Insights Agent no distingue entre mayúsculas y minúsculas, pero la coincidencia exacta de términos mejora la precisión.

### Anclar el contenido

Proporcionar un anclaje de contenido ayuda al agente a saber qué elementos de aprendizaje desea ver. Puede anclar mediante cualquiera de las siguientes opciones:

| **Tipo de anclaje** | **Ejemplo** |
|---|---|
| Nombre | &quot;...la ruta de aprendizaje de la incorporación de nuevos empleados&quot; |
| Widget | &quot;...todas las rutas de aprendizaje del catálogo de incorporación&quot; |
| Etiqueta de catálogo | &quot;...todos los cursos en los que la etiqueta de catálogo Region = North&quot; |
| Etiqueta | &quot;...todos los cursos etiquetados Cumplimiento&quot; |
| Aptitud | &quot;...todos los cursos asignados a la aptitud de Servicio al cliente&quot; |
| Etiqueta de cumplimiento | &quot;...todas las certificaciones con etiqueta de cumplimiento&quot; |
| Tipo de contenido | &quot;...todos los cursos publicados&quot; / &quot;...todas las certificaciones&quot; |

### Anclar a los alumnos

Si una consulta está relacionada con un alumno, utilice uno de estos métodos:

- **Valor del campo activo**: &quot;alumnos cuyo campo activo Puesto = Asociado de ventas&quot; o &quot;alumnos cuyo campo activo Ubicación = 101&quot;
- **Grupo de usuarios**: &quot;alumnos del grupo de usuarios de Sales Associates&quot;
- **Sesión**: &quot;Alumnos inscritos en la sesión del 15 de junio del curso sobre seguridad en el lugar de trabajo&quot;

### Definir el ámbito

La omisión de detalles del ámbito puede dar lugar a resultados más amplios que los previstos.

| **Tipo de ámbito** | **Opciones** |
|---|---|
| Estado de inscripción | inscrito / completado / no inscrito / vencido |
| Intervalo de tiempo | todo el tiempo / últimos 30 días / últimos 90 días / intervalo de fechas específico |
| Estado del usuario | solo usuarios activos (predeterminado) / añadir &quot;incluir usuarios eliminados&quot; para usuarios inactivos |

### Asignar nombre a cada columna de resultados

Si no especifica columnas, Insights Agent las selecciona automáticamente. Asigne un nombre a todos los campos que desee incluir en la salida.

| **Vago** | **Específico** |
|---|---|
| &quot;Mostrar números de ubicación&quot; | &quot;Para cada ubicación: total de alumnos, recuento de inscritos, recuento de no inscritos&quot; |
| &quot;Mostrar tasas de finalización&quot; | &quot;Para cada ruta de aprendizaje: nombre, total inscrito, total completado, % de finalización&quot; |
| &quot;Muéstrame quién falló&quot; | &quot;Mostrar el nombre del alumno, el correo electrónico, el nombre del curso y el estado de finalización de los alumnos que han suspendido&quot; |

### Consultas de ejemplo

Utilícelos como puntos de partida. Adaptarlos reemplazando los nombres de contenido, los grupos de usuarios y los intervalos de tiempo aplicables a su cuenta.

**Finalización y cumplimiento**

- &quot;¿Cuál es la tasa de finalización del curso de formación sobre seguridad en el grupo de usuarios de Norteamérica?&quot;
- &quot;Mostrar índice de finalización por grupo de usuarios para todos los cursos de cumplimiento. Incluya el nombre del grupo de usuarios, el total de inscritos, el total completado y el % de finalización.&quot;
- &quot;¿Cuál es el porcentaje de cumplimiento para todos los alumnos cuyo puesto de trabajo de campo activo = VP?&quot;

**Análisis de inscripción**

- &quot;¿Cuántos alumnos se han inscrito en la ruta de aprendizaje de incorporación de nuevos empleados, por ubicación?&quot;
- &quot;Mostrar inscripciones por región durante los últimos 90 días. Incluir el nombre de la región y el recuento de inscripciones.&quot;
- &quot;Mostrar una lista de todos los alumnos inscritos en el curso de Seguridad en el lugar de trabajo que aún no se han completado: incluir el nombre, el correo electrónico y la fecha de inscripción&quot;.

**Progreso del programa y del curso**

- &quot;¿Cuál es el desglose del estado de finalización de la ruta de aprendizaje del desarrollo del liderazgo? Mostrar cuentas completadas, en curso y no iniciadas&quot;.
- &quot;¿Cuántos alumnos completaron el curso sobre privacidad de datos el mes pasado?&quot;

**Vistas de organización**

- &quot;Mostrar tasa de finalización para todas las certificaciones con etiquetas de tipo de cumplimiento, agrupadas por departamento. Incluye el nombre del departamento, el total de inscritos y el porcentaje de finalización.&quot;
- &quot;¿Cuál es la distribución de la inscripción por región en los últimos 30 días?&quot;

### Errores comunes que se deben evitar

| **Evitar** | **Haga esto en su lugar** |
|---|---|
| Sin anclaje de contenido (&quot;mostrarme todo&quot;) | Asigne un nombre a la ruta, curso, catálogo, etiqueta o aptitud específicos |
| Métrica vaga (&quot;¿por qué son bajas las finalizaciones?&quot;) | Haz una pregunta medible: &quot;¿Qué rutas de aprendizaje tienen una tasa de finalización inferior al 30 %, por ubicación?&quot; |
| No se especifica el estado del usuario | Añada explícitamente &quot;solo usuarios activos&quot; o &quot;incluir usuarios eliminados&quot; |
| Pedir predicciones | Pregunte qué muestran los datos actuales, no qué pasará |
| Solicitud de datos no admitidos (comentarios, aptitudes, insignias) | Usar informes existentes en la sección Informes |
| Hacer varias preguntas en una consulta (&quot;Mostrar inscripciones por región y también enumerar quién no ha completado el Entrenamiento de Seguridad&quot;) | Formule una pregunta específica por consulta. El agente puede responder solo una parte de una consulta compuesta, sin ninguna garantía de que se aborde el resto. |

## Limitaciones en la versión

**No se admiten las consultas enviadas en scripts no latinos**

Insights Agent admite consultas escritas en inglés y en idiomas con alfabeto latino, como el francés y el español. Las consultas enviadas con secuencias de comandos no latinas, como japonés, chino, árabe, coreano, hindi y ruso, no se pueden procesar y el agente mostrará un mensaje que indica que la consulta no se ha podido completar. Si envía una consulta en uno de estos idiomas, inicie una nueva consulta y vuelva a formularla en inglés.
