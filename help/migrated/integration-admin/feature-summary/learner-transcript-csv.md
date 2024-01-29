---
jcr-language: en_us
title: Interpretar el archivo CSV de transcripciones de alumnos
description: Interpretar el archivo CSV de transcripciones de alumnos
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 0%

---



# Interpretar el archivo CSV de transcripciones de alumnos

La transcripción del alumno es uno de los informes más populares utilizados en Adobe Learning Manager. El informe permite obtener casi todos los detalles posibles en un solo informe en formato CSV.

Además de ser un informe que los usuarios pueden obtener para realizar un seguimiento y analizar los comportamientos de aprendizaje, el informe también se puede ver como el formato en el que se puede configurar Learning Manager para exportar datos sobre comportamientos de aprendizaje a aplicaciones o sistemas externos.

Un escenario empresarial típico es realizar una exportación periódica de transcripciones de alumnos para Learning Manager, analizarlas para extraer alumnos que estén completando un programa de aprendizaje importante y realizar un pedido de un vale de regalo para reconocer y recompensar las finalizaciones oportunas.

Otro caso de uso consiste en añadir los datos de comportamiento de aprendizaje a un almacén de datos de empresa, donde se pueden combinar datos de aprendizaje con otros datos de empresa para analizar las correlaciones entre el comportamiento de aprendizaje y otros datos de proceso.

En el resto del documento, se describe brevemente cómo se puede obtener la transcripción del alumno de Learning Manager y, a continuación, se proporciona información sobre cómo debe interpretarse cada fila y columna del informe.

Esta información puede ser útil para cualquier desarrollador que tenga la intención de integrar Learning Manager con otros sistemas mediante el procesamiento de los datos de transcripciones de alumnos exportados.

## Recuperar transcripciones de alumnos desde la interfaz de usuario {#fetchlearnertranscriptfromtheuserinterface}

En Configuración de perfil, un alumno puede descargar su transcripción. Para obtener más información, consulte *** [Descargar transcripciones de alumnos](../../administrators/feature-summary/learner-transcripts.md)***.

Los administradores pueden generar transcripciones de alumnos para toda la organización, un conjunto específico de usuarios, un conjunto específico de objetos de aprendizaje o un conjunto específico de usuarios y objetos de aprendizaje. También pueden obtener todos los registros de aprendizaje durante un intervalo de tiempo e indicar si se requiere información del nivel de módulo (de forma predeterminada, se omite esta información). Para obtener más información, consulte [***Descargar transcripciones de alumnos***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Los administradores también pueden configurar el sistema para enviar periódicamente por correo electrónico la transcripción del alumno.

La transcripción del alumno generada a través de la interfaz de usuario será un archivo de Excel, que también contiene la &quot;Transcripción de aptitudes&quot;. En este documento, nos referiremos a lo que se genera en formato CSV, un informe que contiene actividades de aprendizaje relacionadas con la inscripción, el inicio, el progreso o la finalización de un objeto de aprendizaje.

## Exportar transcripciones de alumnos {#exportlearnertranscript}

Cuando un sistema externo debe consumir la transcripción del alumno, Learning Manager proporciona una función denominada Exportar datos, donde la transcripción del alumno es uno de los tipos de datos que se pueden exportar. Como se explica en el preámbulo, esto es necesario para la integración de Learning Manager con un sistema externo que necesita procesar datos de comportamiento de aprendizaje o para rellenar un almacén de datos de empresa con datos de comportamiento de aprendizaje.

Para obtener más información sobre los conectores compatibles con la exportación de transcripciones de alumnos, consulte la [Sección Exportar datos](/help/migrated/integration-admin/feature-summary/connectors.md) en los conectores de FTP, Box y PowerBI.

El propósito de estos conectores es exportar datos a una aplicación descendente periódicamente (una vez cada N días). Por lo tanto, estos conectores solo exportan los datos incrementales de comportamiento de aprendizaje en cada ejecución. Tenga en cuenta que estos conectores no permiten obtener registros pertenecientes a un subconjunto específico de usuarios u objetos de aprendizaje; siempre son datos sobre todos los usuarios y todos los objetos de aprendizaje de esa cuenta.

En el caso de PowerBI, el cliente debe proporcionar un espacio de trabajo donde Learning Manager pueda seguir exportando estos datos de forma incremental en un conjunto de datos creado dinámicamente. Este conector simplemente exporta datos y los clientes deben crear sus propios informes/paneles basados en este conjunto de datos según sea necesario.

La siguiente sección proporciona detalles sobre cómo un sistema descendente debe interpretar los registros de la transcripción del alumno.

## Interpretar transcripciones de alumnos {#interpretthelearnertranscript}

Cada fila de una transcripción de alumno se puede considerar como un comportamiento de aprendizaje capturado en Learning Manager en un período de tiempo específico. Normalmente, los conectores exportan &quot;datos incrementales&quot;, por lo que las filas representan actividades de aprendizaje que se produjeron entre la última ejecución del conector y la ejecución actual.

Por supuesto, los conectores también permiten obtener la transcripción del alumno a petición y, en este caso, el usuario puede especificar una fecha de inicio y la fecha de finalización, que se supone que es ahora. Normalmente, esto se suele hacer una vez inicialmente y, a continuación, se configura el conector para que exporte la transcripción incremental del alumno a una hora específica del día, una vez cada N días (el valor predeterminado de N es 1).

Ahora vamos a definir qué se entiende por la transcripción incremental del alumno

En la transcripción del alumno, cada fila representa una actividad específica que implica a un alumno específico y un objeto de aprendizaje específico. Nos interesa principalmente qué estado tiene un alumno con respecto al objeto de aprendizaje: **Inscrito**, **Iniciado**, **En curso**, y **Completado**. Por lo tanto, la transcripción del alumno captura también las cuatro fechas correspondientes.

Ahora hay tres tipos de objetos de aprendizaje en los que Learning Manager realiza un seguimiento del progreso del alumno y los datos exportados contienen información de progreso en el nivel de módulo, que es la unidad de contenido más detallada que un alumno puede experimentar en Learning Manager.

* **Curso** - una composición de uno o varios módulos
* **Programa de aprendizaje** - un conjunto de uno o varios cursos
* **Certificación** - un conjunto de uno o varios cursos.

Cada fila de la transcripción del alumno podría estar relacionada con la participación de un usuario específico en un módulo, curso, programa de aprendizaje o certificación. Cuando un usuario se inscribe en un programa de aprendizaje, la transcripción indicará que el usuario está

Las columnas de la transcripción del alumno proporcionan información relativa a cada actividad de aprendizaje, y las siguientes tablas describen la semántica de cada columna.

## Transcripciones de alumnos

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Nombre de columna</b></p></th> 
   <th width="160" valign="bottom"><p><b>Tipo de valor</b></p></th> 
   <th width="306" valign="bottom"><p><b>Descripción</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Nombre</b></p></td> 
   <td><p>Nunca vacías</p></td> 
   <td><p>Nombre del alumno</p></td> 
  </tr> 
  <tr> 
   <td><p><b>correo electrónico</b></p></td> 
   <td><p>Nunca vacías</p></td> 
   <td><p>Dirección de correo electrónico del alumno</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Puede estar vacía</td> 
   <td valign="bottom">Adobe ID del alumno</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID único de usuario</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">ID exclusivo de usuario del alumno. Esta columna se basa en la configuración de back-end tanto si está activada como desactivada en el nivel de cuenta.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nombre del plan de aprendizaje</b></p></td> 
   <td valign="middle"><p>Puede estar vacía</p></td> 
   <td valign="middle">El nombre del plan de aprendizaje (si lo hay), a través del cual se ha asignado automáticamente al usuario.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Programa de aprendizaje/certificación/curso</b></p></td> 
   <td valign="middle"><p>Nunca vacías</p></td> 
   <td valign="middle"><p>Nombre del programa de aprendizaje, certificación o curso</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Tipo</b></p></td> 
   <td valign="middle">Nunca vacío</td> 
   <td valign="middle"><p>El tipo de objeto de aprendizaje en el que se inscribió el usuario.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Curso</b></p></td> 
   <td valign="middle"><p>Puede estar vacía</p></td> 
   <td valign="middle">Nombre del curso en el que se ha inscrito el usuario. Si está vacía, la fila representa una certificación o un programa de aprendizaje. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID único de objeto de aprendizaje</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">ID exclusivo del objeto de aprendizaje del objeto de aprendizaje. Esta columna se basa en la configuración de si está activado o desactivado en el nivel de cuenta</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instancia  </b></p></td> 
   <td valign="middle">Nunca vacío</td> 
   <td valign="middle">Nombre de la instancia del objeto de aprendizaje en el que se inscribe el usuario. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Criterios de selección</b></p></td> 
   <td valign="middle"><p>Nunca vacías</p></td> 
   <td valign="middle"><p>Base de la inscripción (cómo se inscribió este alumno en este objeto de aprendizaje).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Módulo</b></p></td> 
   <td valign="middle"><p>Puede estar vacía</p></td> 
   <td valign="middle">Nombre del módulo dentro de los cursos. Si está vacía, esta fila representa un curso, un programa de aprendizaje o una certificación.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Versión</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">Versión del módulo</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Tipo de entrega</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">Tipo de entrega del módulo: aprendizaje online, F2F, VC, actividad.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Idioma</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">Idioma en el que el alumno consume el módulo. Esta columna muestra el valor solo para los módulos de aprendizaje online.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Comentario</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">Comentarios añadidos por el administrador, el instructor del alumno al marcar la asistencia del usuario.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de inscripción (zona horaria de Asia/Calcuta)</b></td> 
   <td height="19" width="283">Nunca vacío</td> 
   <td height="19" width="728">Fecha de inscripción del alumno en el tipo de objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de Inicio (Zona Horaria de Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía</p></td> 
   <td height="19" width="728">Fecha en la que el alumno inició el objeto de aprendizaje. Vacío implica que el alumno aún no ha iniciado este proceso.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de finalización (zona horaria de Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía</p></td> 
   <td><p>La fecha en la que el alumno completó este objeto. Si está vacío, significa que el alumno aún no lo ha completado.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha límite (zona horaria de Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía</p></td> 
   <td height="19" width="728">Fecha en la que se espera que el alumno complete este objeto de aprendizaje. Vacío implica que no hay un plazo para esto.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Vencido</b></td> 
   <td height="19" width="283">Sí/ No</td> 
   <td height="19" width="728">Estado vencido actual del alumno inscrito en el objeto de aprendizaje. Sí/No</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Estado</b></p></td> 
   <td valign="middle">No iniciado/Completado/En curso/Dado de baja</td> 
   <td valign="middle">Progreso actual % del alumno inscrito en el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Progreso %</b></p></td> 
   <td valign="middle">Puede estar vacía</td> 
   <td valign="middle"><p>Indica el grado en que el alumno ha completado este objeto.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Tiempo empleado (minutos)</b></td> 
   <td height="38" width="283">Puede estar vacía</td> 
   <td height="38" width="728">El tiempo de aprendizaje empleado por el alumno en el objeto de aprendizaje, las filas del nivel de módulo muestran el tiempo de aprendizaje empleado del módulo individual. Las filas del nivel Curso / Programa / Certificado muestran el tiempo de aprendizaje agregado dedicado.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Grado</b></p></td> 
   <td valign="middle">Aprobado/ Suspendido</td> 
   <td valign="middle">Indica el éxito del alumno. 'Aprobado', si el usuario ha cumplido los criterios de éxito para esto, 'Suspendido' en caso contrario.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Puntuación de prueba</b></p></td> 
   <td valign="middle">Puede estar vacía</td> 
   <td valign="middle">La puntuación de prueba más reciente obtenida por el alumno. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba o el administrador o instructor no ha asignado ninguna puntuación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Puede estar vacía</td> 
   <td height="38" width="728">La puntuación máxima de prueba más reciente posible para el módulo. Puede estar en blanco si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Puede estar vacía</td> 
   <td height="38" width="728">La puntuación de prueba más alta obtenida por el alumno en varios intentos. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no incluye ninguna prueba o si el administrador o el instructor no han asignado ninguna puntuación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Puede estar vacía</td> 
   <td height="38" width="728">La puntuación máxima de prueba más alta posible para el módulo. Puede estar en blanco si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Intentos Realizados</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">El número total de intentos realizados por el alumno para este módulo hasta la fecha actual.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Máximo de intentos permitidos</b></td> 
   <td height="19" width="283">Puede estar vacía</td> 
   <td height="19" width="728">El número máximo de intentos permitidos para que el alumno consuma el módulo.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Nunca vacío</td> 
   <td valign="middle">Estado de usuario del alumno: Activo/Eliminado/Suspendido.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Campo activo agrupable</b></td> 
   <td height="38" width="283">Puede estar vacía</td> 
   <td height="38" width="728">Para cada campo activo agrupable de la cuenta, habrá una columna, donde el nombre de la columna será el de campo activo y el valor será el valor específico que tiene el alumno para ese campo.</td> 
  </tr> 
  <tr> 
   <td><p><b>Nombre del responsable</b></p></td> 
   <td><p><i>Puede estar vacía</i></p></td> 
   <td height="19" width="728">Nombre del responsable del alumno</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de inscripciones</b></td> 
   <td height="38" width="283">1 o 0</td> 
   <td height="38" width="728">Recuento de inscripciones del alumno para el objeto de aprendizaje. La fila de objetos de aprendizaje de nivel superior muestra un valor = '1'. Los subcursos de formación muestran un valor 0.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Recuento iniciado</b></td> 
   <td height="19" width="283">1 o 0</td> 
   <td height="19" width="728">Recuento iniciado del alumno para el objeto de aprendizaje. La fila de objetos de aprendizaje de nivel superior muestra un valor = '1'. Los subcursos de formación muestran un valor 0.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Recuento de finalización</b></td> 
   <td height="58" width="283">1 o 0</td> 
   <td height="58" width="728">Recuento de finalización del alumno para el objeto de aprendizaje. La fila del objeto de aprendizaje de nivel superior muestra un valor = '1' si el alumno está pendiente de finalización en ese curso de formación. Los subcursos de formación muestran un valor 0 aunque se encuentren en estado Pendiente. La fila del objeto de aprendizaje de nivel superior muestra un valor = '0' si el alumno ha completado el curso de formación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vencimiento en N días</b></td> 
   <td height="38" width="283">1 o 0</td> 
   <td height="38" width="728">Esto muestra un valor de "1" o "0" en función de la fecha límite de la instancia en la que se inscribe el alumno en la formación. Depende del valor introducido en la hoja Resumen de aprendizaje I &gt; campo "Fecha de vencimiento próxima a".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vencimiento en N días para el usuario</b></td> 
   <td height="38" width="283">1 o 0</td> 
   <td height="38" width="728">Esto muestra un valor de "1" o "0" en función de la fecha límite de la instancia en la que se inscribe el alumno en la formación. Depende del valor introducido en la hoja Resumen de aprendizaje II &gt; en el campo Fecha de vencimiento próxima en.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de (Progreso mayor que N %)</b></td> 
   <td height="38" width="283">1 o 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0' en función del progreso del alumno en el curso de formación. Depende del valor introducido en la hoja Resumen de aprendizaje I &gt; campo "Progreso mayor que".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de (Progreso mayor que N %) para el usuario</b></td> 
   <td height="38" width="283">1 o 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0' en función del progreso del alumno en el curso de formación. Depende del valor introducido en la hoja Resumen de aprendizaje II &gt; campo "Progreso mayor que".</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>ID de formación</b></td> 
   <td height="19" width="283">Nunca vacío</td> 
   <td height="19" width="728">ID del curso de formación.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Duración del módulo o curso de formación (minutos)</b></td> 
   <td height="20" width="283">Nunca vacío</td> 
   <td height="20" width="728">Duración total del módulo o el curso de formación (minutos) de la instancia predeterminada del curso de formación.</td> 
  </tr> 
 </tbody> 
</table>

### Resumen de aprendizaje I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Nombre de columna<br></th> 
   <th>Tipo de valor</th> 
   <th>Descripción</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Tipo</td> 
   <td height="19" width="253">Todo, programa de aprendizaje, certificado, curso.</td> 
   <td height="19" width="412">El tipo de objeto de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Campo agrupable(perfil)</td> 
   <td height="19" width="253">Nunca vacío</td> 
   <td height="19" width="412">El perfil para el que la tabla de resumen de aprendizaje debe mostrar datos.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Nombre del responsable</td> 
   <td height="38" width="253">Nunca vacío</td> 
   <td height="38" width="412">El nombre del responsable, cuyos datos de participación de objetos de aprendizaje subordinados se mostrarán en la tabla Resumen de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Etiquetas de fila</td> 
   <td height="19" width="253">Nunca vacío</td> 
   <td height="19" width="412">El nombre del objeto de aprendizaje con la lista de alumnos inscritos en el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos inscritos</td> 
   <td height="19" width="253">Nunca vacío</td> 
   <td height="19" width="412">Número de alumnos inscritos en el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos que han iniciado</td> 
   <td height="19" width="253">Nunca vacío</td> 
   <td height="19" width="412">Número de alumnos que han iniciado el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos que han completado</td> 
   <td height="19" width="253">Nunca vacío</td> 
   <td height="19" width="412">Número de alumnos que han completado el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Número de alumnos que han progresado &gt;= N %</td> 
   <td height="38" width="253">Nunca vacío</td> 
   <td height="38" width="412">Número de alumnos que han progresado &gt;= N % (valores).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Número de alumnos con fecha de vencimiento en N días</td> 
   <td height="39" width="253">Nunca vacío</td> 
   <td height="39" width="412">Número de alumnos con fecha de vencimiento en N días (valores).</td> 
  </tr> 
 </tbody> 
</table>

### Resumen del aprendizaje II

| Nombre de columna | Tipo de valor | Descripción |
|---|---|---|
| Tipo | Todo, programa de aprendizaje, certificado, curso. | El tipo de objeto de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos. |
| Campo agrupable(perfil) | Nunca vacío | El perfil para el que la tabla de resumen de aprendizaje debe mostrar datos. |
| Nombre del responsable | Nunca vacío | El nombre del responsable, cuyos datos de participación de objetos de aprendizaje subordinados se mostrarán en la tabla Resumen de aprendizaje. |
| Etiquetas de fila | Nunca vacío | El nombre del alumno con la lista de objetos de aprendizaje en los que se inscribe el alumno. |
| Número de objetos de aprendizaje inscritos | Nunca vacío | Número de objetos de aprendizaje en los que se inscribe el alumno. |
| Número de objetos de aprendizaje iniciados | Nunca vacío | Número de objetos de aprendizaje que ha iniciado el alumno. |
| Número de objetos de aprendizaje completados | Nunca vacío | Número de objetos de aprendizaje completados por el alumno. |
| Número de objetos de aprendizaje que han progresado >= N % | Nunca vacío | Número de objetos de alumno que el alumno ha progresado >= N %. |
| Número de objetos de aprendizaje con fecha de vencimiento en N días | Nunca vacío | Número de objetos de aprendizaje con fecha de vencimiento en N días. |

### Resumen de cumplimiento

| Nombre de columna | Tipo de valor | Descripción |
|---|---|---|
| Tipo | Todo, programa de aprendizaje, certificado, curso. | El tipo de objeto de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos. |
| Etiquetas de fila (columna del lado izquierdo) | Nunca vacío | El nombre del alumno con la lista de objetos de aprendizaje en los que se inscribe el alumno. |
| Etiquetas de fila (columna del lado izquierdo) | Nunca vacío | El nombre del alumno con la lista de objetos de aprendizaje en los que se inscribe el alumno. |

### Transcripción de aptitudes

| .Nombre de columna | Tipo de valor | Descripción |
|---|---|---|
| Nombre | Nunca vacío | Nombre del alumno |
| correo electrónico | Nunca vacío | Dirección de correo electrónico del alumno |
| Adobe ID | Puede estar vacía | Adobe ID del alumno |
| ID único de usuario | Puede estar vacía | ID exclusivo de usuario del alumno. Esta columna se basa en la configuración de back-end tanto si está activada como desactivada en el nivel de cuenta. |
| Aptitud | Nunca vacío | Se ha asignado un nombre de aptitud al alumno. |
| Nivel de aptitud | Nunca vacío | Nivel de aptitud asignado al alumno. |
| Créditos necesarios | Nunca vacío | Créditos totales necesarios para que el alumno adquiera la aptitud. |
| Créditos obtenidos | Nunca vacío | Créditos totales obtenidos por el alumno para la aptitud. |
| Porcentaje de finalización | Nunca vacío | Porcentaje de progreso para obtener la aptitud. |
| Fecha asignada (zona horaria UTC) | Nunca vacío | Fecha en la que se asignó la aptitud al alumno. |
| Fecha de obtención (zona horaria UTC) | Nunca vacío | Fecha en la que el alumno adquirió la aptitud. |
| userState | Nunca vacío | Estado de usuario del alumno: Activo/Eliminado/Suspendido. |
| Campo activo agrupable | Puede estar vacía | Para cada campo activo agrupable de la cuenta, habrá una columna, donde el nombre de la columna será el de campo activo y el valor será el valor específico que tiene el alumno para ese campo. |
| Nombre del responsable | Puede estar vacía | Nombre del responsable del alumno. |

### Resumen de aptitudes I

| Nombre de columna | Tipo de valor | Descripción |
|---|---|---|
| Después | Nunca vacío | Número de alumnos que han obtenido la aptitud antes del número de días introducido (valor) que debe actualizarse. |
| Nombre | Todos o cualquier nombre de alumno | El nombre del alumno que tiene una aptitud asignada. |
| Nombre del responsable | Nunca vacío | El nombre del responsable, cuyos datos de participación en aptitudes de los subordinados se mostrarán en la tabla Resumen de aptitudes. |
| Etiquetas de fila | Nunca vacío | El nombre de la aptitud con la lista de alumnos asignados a ella. |
| Número de usuarios que deben tener esta aptitud | Nunca vacío | Número de alumnos asignados a la aptitud. |
| Número de usuarios que han obtenido esta aptitud | Nunca vacío | Número de alumnos que han alcanzado la aptitud. |
| Número de alumnos cuya aptitud debe actualizarse | Nunca vacío | Número de alumnos cuya aptitud se debe actualizar. |
| Porcentaje de cumplimiento (basado en la aptitud obtenida) | Nunca vacío | El porcentaje de progreso de la aptitud asignada. |

### Resumen de aptitudes II

| Nombre de columna | Tipo de valor | Descripción |
|---|---|---|
| Después | Nunca vacío | Número de alumnos que obtuvieron la aptitud antes del número de días introducido (valor) que debe actualizarse. |
| Aptitud | Todo o cualquier nombre de aptitud | Los nombres de las aptitudes que se asignan a los alumnos. |
| Nombre del responsable | Nunca vacío | El nombre del responsable, cuyos datos de participación en aptitudes de los subordinados se mostrarán en la tabla Resumen de aptitudes. |
| Etiquetas de fila | Nunca vacío | El nombre del alumno con la lista de aptitudes asignadas. |
| Número de aptitudes que debe tener cada usuario | Nunca vacío | Número de aptitudes asignadas al alumno. |
| Número de aptitudes que tiene cada usuario | Nunca vacío | Número de aptitudes obtenidas por el alumno. |
| Número de aptitudes que se deben actualizar | Nunca vacío | Número de alumnos cuya aptitud se debe actualizar. |
| Porcentaje de cumplimiento | Nunca vacío | El porcentaje de progreso de la aptitud asignada. |

* En ocasiones, los administradores pueden marcar la finalización de un objeto de aprendizaje de forma manual (especialmente para los cursos de clase) mucho después de la clase. En este caso, si Exportar datos está configurado para exportar diariamente el LT, es posible que la fecha real de finalización ya haya pasado y, por lo tanto, la exportación nunca obtendrá esos registros de finalización marcados como completados mucho después de que haya finalizado la clase. Cuando esto se detecte, considere la posibilidad de exportar la transcripción desde una fecha de inicio determinada hasta la fecha (a petición) en la interfaz de usuario; a continuación, llévela a la aplicación descendente para un &quot;procesamiento posterior&quot;. Al hacer esto, es posible que deba omitir los registros que ya se han procesado.
* Varios intentos para un módulo dependen de si está activado para ese objeto de aprendizaje. Cuando está activado, lo que aparece ahora en una fila del archivo CSV relacionada con un módulo es un intento. Puede que no se notifiquen todos los intentos de un día, por lo que puede que el número total de intentos aparezca incrementado en más de uno. Además, un intento no necesariamente puede mejorar una puntuación, y en cualquier momento dado solo se obtiene la mejor puntuación.
