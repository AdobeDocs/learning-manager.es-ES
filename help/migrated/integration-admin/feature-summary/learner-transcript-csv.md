---
jcr-language: en_us
title: Interpretar el archivo CSV de transcripciones de alumnos
description: Interpretar el archivo CSV de transcripciones de alumnos
contentowner: saghosh
preview: true
source-git-commit: fcc50e80f94bdcbc8de2cddac92f1a12b55e1e18
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 88%

---



# Interpretar el archivo CSV de transcripciones de alumnos

La transcripción del alumno es uno de los informes más populares utilizados en Adobe Learning Manager. El informe permite obtener casi todos los detalles posibles en un solo informe en formato CSV.

Además de ser un informe que los usuarios pueden obtener para supervisar y analizar los comportamientos de aprendizaje, este también se puede ver con el formato en el que se puede configurar Learning Manager para exportar datos sobre comportamientos de aprendizaje a aplicaciones o sistemas externos.

Como escenario empresarial típico, se puede realizar una exportación periódica de transcripciones de alumnos de Learning Manager, analizarlas para extraer alumnos que estén realizando un programa de aprendizaje importante y realizar un pedido de un vale de regalo para reconocer y recompensar a aquellos alumnos que lo completen de forma oportuna.

Otro caso de uso consiste en añadir los datos de comportamiento de aprendizaje a un almacén de datos de empresa, donde se pueden combinar datos de aprendizaje con otros datos empresariales para analizar las correlaciones entre el comportamiento de aprendizaje y otros datos de proceso.

En el resto del documento, se describe brevemente cómo se puede obtener la transcripción del alumno de Learning Manager y, a continuación, se proporciona información sobre cómo debe interpretarse cada fila y columna del informe.

Esta información puede ser útil para cualquier desarrollador que tenga intención de integrar Learning Manager en otros sistemas mediante el procesamiento de los datos de transcripciones de alumnos exportados.

## Recuperar transcripciones de alumnos desde la interfaz de usuario {#fetchlearnertranscriptfromtheuserinterface}

En Configuración de perfil, un alumno puede descargar su transcripción. Para obtener más información, consulte ***[Descargar transcripciones de alumnos](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md)***.

Los administradores pueden generar transcripciones de alumnos para toda la organización, un conjunto específico de usuarios, un conjunto específico de objetos de aprendizaje o un conjunto específico de ambos. También pueden obtener todos los registros de aprendizaje durante un intervalo de tiempo e indicar si se requiere información de nivel de módulo (de forma predeterminada, se omite esta información). Para obtener más detalles, consulte [***Descargar transcripciones de alumnos***](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md).

<!--Update above link?-->

Los administradores también pueden configurar el sistema para enviar periódicamente por correo electrónico la transcripción del alumno.

La transcripción del alumno generada a través de la interfaz de usuario será un archivo de Excel, que también contiene la &quot;Transcripción de aptitudes&quot;. En este documento, nos referiremos a lo que se genera en formato CSV, un informe que contiene actividades de aprendizaje relacionadas con la inscripción, el inicio, el progreso o la finalización de un objeto de aprendizaje.

## Exportar transcripciones de alumnos {#exportlearnertranscript}

Si un sistema externo debe consumir la transcripción del alumno, Learning Manager proporciona una función denominada Exportar datos, donde la transcripción del alumno es uno de los tipos de datos que se pueden exportar. Como se explica en el preámbulo, esto es necesario para la integración de Learning Manager con un sistema externo que necesita procesar datos de comportamiento de aprendizaje o para rellenar un almacén de datos de empresa con datos de comportamiento de aprendizaje.

Para obtener más información sobre los conectores que admiten la exportación de transcripciones de alumnos, consulte la sección [Exportar datos](/help/migrated/integration-admin/feature-summary/connectors.md) de los conectores para FTP, Box y PowerBI.

Estos conectores tienen como finalidad exportar datos en una aplicación descendente de forma periódica (una vez cada N días). Por lo tanto, estos conectores solo exportan los datos incrementales de comportamiento de aprendizaje en cada ejecución. Tenga en cuenta que estos conectores no permiten obtener registros pertenecientes a un subconjunto específico de usuarios u objetos de aprendizaje; siempre son datos sobre todos los usuarios y todos los objetos de aprendizaje de esa cuenta.

En el caso de PowerBI, el cliente debe proporcionar un espacio de trabajo donde Learning Manager pueda seguir exportando estos datos de forma incremental en un conjunto de datos creado dinámicamente. Este conector solo exporta datos y los clientes deben crear sus propios informes/tableros basados en ese conjunto de datos según sea necesario.

En la siguiente sección, se proporciona información sobre cómo un sistema descendente debe interpretar los registros de la transcripción del alumno.

## Interpretar la transcripción del alumno {#interpretthelearnertranscript}

Cada fila de una transcripción de alumno se puede considerar como un comportamiento de aprendizaje capturado en Learning Manager en un período de tiempo específico. Normalmente, los conectores exportan &quot;datos incrementales&quot;, por lo que las filas representan actividades de aprendizaje que se produjeron entre la última ejecución del conector y la ejecución actual.

Por supuesto, los conectores también permiten obtener la transcripción del alumno a petición y, en este caso, el usuario puede especificar la fecha de inicio y la de finalización, que se presupone que es la fecha actual. Normalmente, esto se debe realizar una vez inicialmente y, a continuación, se configuraría el conector para que exporte la transcripción incremental del alumno a una hora específica del día, una vez cada N días (el valor predeterminado de N es 1).

Ahora vamos a definir qué se entiende por la transcripción del alumno incremental.

En la transcripción del alumno, cada fila representa una actividad concreta relacionada con un alumno y un objeto de aprendizaje específicos. Nos interesa principalmente qué estado tiene un alumno con respecto al objeto de aprendizaje: **Inscrito**, **Iniciado**, **En curso** y **Completado**. Por lo tanto, la transcripción del alumno captura también las cuatro fechas correspondientes.

Ahora hay tres tipos de objetos de aprendizaje en los que Learning Manager realiza un seguimiento del progreso del alumno y los datos exportados contienen información de progreso en el nivel de módulo, que es la unidad de contenido más detallada que un alumno puede experimentar en Learning Manager.

* **Curso**: una composición de uno o más módulos
* **Programa de aprendizaje**: un conjunto de uno o más cursos
* **Certificación**: un conjunto de uno o varios cursos.

Cada fila de la transcripción del alumno podría estar relacionada con la participación de un usuario específico en un módulo, curso, programa de aprendizaje o certificación. Cuando un usuario se inscribe en un programa de aprendizaje, la transcripción indica que el usuario

Las columnas de la transcripción del alumno proporcionan información relativa a cada actividad de aprendizaje; en las siguientes tablas, se describe la semántica de cada columna.

## Transcripciones de alumnos

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Nombre de la columna</b></p></th> 
   <th width="160" valign="bottom"><p><b>Tipo de valor</b></p></th> 
   <th width="306" valign="bottom"><p><b>Descripción</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Nombre</b></p></td> 
   <td><p>No puede estar nunca vacía.</p></td> 
   <td><p>El nombre del alumno.</p></td> 
  </tr> 
  <tr> 
   <td><p><b>correo electrónico</b></p></td> 
   <td><p>No puede estar nunca vacía.</p></td> 
   <td><p>La dirección de correo electrónico del alumno.</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Puede estar vacía.</td> 
   <td valign="bottom">Adobe ID del alumno</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID exclusivo de usuario</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">ID exclusivo de usuario del alumno. Esta columna se basa en la configuración de back-end si está activada o desactivada en el nivel de cuenta.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nombre del plan de aprendizaje</b></p></td> 
   <td valign="middle"><p>Puede estar vacía.</p></td> 
   <td valign="middle">Nombre del plan de aprendizaje (si lo hay), a través del cual se ha asignado automáticamente al usuario.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Programa de aprendizaje/Certificación/Curso</b></p></td> 
   <td valign="middle"><p>No puede estar nunca vacía.</p></td> 
   <td valign="middle"><p>El nombre del programa de aprendizaje, la certificación o el curso.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Tipo</b></p></td> 
   <td valign="middle">No puede estar nunca vacía.</td> 
   <td valign="middle"><p>El tipo de objeto de aprendizaje en el que se ha inscrito el usuario.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Curso</b></p></td> 
   <td valign="middle"><p>Puede estar vacía.</p></td> 
   <td valign="middle">Nombre del curso al que se ha inscrito el usuario. Si está vacía, la fila representa una certificación o un programa de aprendizaje. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID exclusivo de objetos</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Identificador exclusivo del objeto de aprendizaje del objeto de aprendizaje. Esta columna se basa en la configuración de activar o desactivar en el nivel de cuenta</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instancia  </b></p></td> 
   <td valign="middle">No puede estar nunca vacía.</td> 
   <td valign="middle">El nombre de la instancia del objeto de aprendizaje en el que se ha inscrito el usuario. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Criterios de selección</b></p></td> 
   <td valign="middle"><p>No puede estar nunca vacía.</p></td> 
   <td valign="middle"><p>Base de la inscripción (cómo se inscribió este alumno en este objeto de aprendizaje).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Módulo</b></p></td> 
   <td valign="middle"><p>Puede estar vacía.</p></td> 
   <td valign="middle">Nombre del módulo dentro de los cursos. Si esta fila está vacía, representa un curso, un programa de aprendizaje o una certificación.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Versión</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Versión del módulo</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Tipo de entrega</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Tipo de entrega del módulo: aprendizaje electrónico, F2F, VC, Actividad.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Idioma</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Idioma en el que el alumno consume el módulo. Esta columna muestra el valor solo para los módulos de aprendizaje electrónico.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Comentario</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Comentarios añadidos por el administrador, el instructor del alumno al marcar la asistencia del usuario.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de inscripción (zona horaria Asia/Calcuta)</b></td> 
   <td height="19" width="283">No puede estar nunca vacía.</td> 
   <td height="19" width="728">Fecha de inscripción del alumno en el tipo de objetos de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de inicio (zona horaria Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía.</p></td> 
   <td height="19" width="728">Fecha en la que el alumno inició el aprendizaje. Si está vacía, esto indica que el alumno no ha iniciado aún este objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha de finalización (zona horaria Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía.</p></td> 
   <td><p>La fecha en la que el alumno completó este objeto. Si está vacío, significa que el alumno aún no lo ha completado.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Fecha límite (zona horaria Asia/Calcuta)</b></td> 
   <td><p>Puede estar vacía.</p></td> 
   <td height="19" width="728">La fecha en la que se espera que el alumno complete este objeto de aprendizaje. Si está vacía, esto implica que no hay ningún plazo para este objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Vencido</b></td> 
   <td height="19" width="283">Sí/No</td> 
   <td height="19" width="728">Estado vencido actual del alumno inscrito en el objeto de aprendizaje. Sí/No</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Estado</b></p></td> 
   <td valign="middle">No iniciado/completado/En curso/Sin inscribir</td> 
   <td valign="middle">Porcentaje de progreso actual del alumno inscrito en el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Progreso %</b></p></td> 
   <td valign="middle">Puede estar vacía.</td> 
   <td valign="middle"><p>Indica hasta qué punto el alumno ha completado este objeto de aprendizaje.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Tiempo empleado (minutos)</b></td> 
   <td height="38" width="283">Puede estar vacía.</td> 
   <td height="38" width="728">Tiempo de aprendizaje dedicado por el alumno en el aprendizaje, las filas de nivel de módulo muestran el tiempo de aprendizaje dedicado en cada módulo. Las filas de nivel Curso/Programa/Certificado muestran el tiempo de aprendizaje agregado dedicado.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nota</b></p></td> 
   <td valign="middle">Aprobado/suspenso</td> 
   <td valign="middle">Indica el éxito del alumno. "Aprobado", si el usuario ha cumplido los criterios de éxito de este objeto de aprendizaje; de lo contrario, "Suspendido".</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Puntuación de prueba</b></p></td> 
   <td valign="middle">Puede estar vacía.</td> 
   <td valign="middle">La puntuación de prueba más reciente obtenida por el alumno. Puede estar vacío si el alumno no ha intentado la prueba o el contenido no tiene ninguna prueba o si el administrador o el instructor no ha asignado ninguna puntuación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Puntuación_máx_de_prueba</b></td> 
   <td height="38" width="283">Puede estar vacía.</td> 
   <td height="38" width="728">La puntuación máxima de prueba más reciente posible para el módulo. Puede estar vacío si el alumno no ha intentado la prueba o si el contenido no tiene ninguna prueba.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Puntuación_más_alta_de_prueba</b></td> 
   <td height="38" width="283">Puede estar vacía.</td> 
   <td height="38" width="728">La puntuación de prueba más alta obtenida por el alumno en varios intentos. Puede estar vacío si el alumno no ha intentado la prueba o el contenido no tiene ninguna prueba o si el administrador o el instructor no han asignado ninguna puntuación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Puntuación_más_alta_de_prueba_máx</b></td> 
   <td height="38" width="283">Puede estar vacía.</td> 
   <td height="38" width="728">La puntuación de prueba máxima más alta posible para el módulo. Puede estar vacío si el alumno no ha intentado la prueba o si el contenido no tiene ninguna prueba.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Intentos realizados</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">El número total de intentos realizados por alumno para este módulo hasta la fecha actual.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Máximo de intentos permitidos</b></td> 
   <td height="19" width="283">Puede estar vacía.</td> 
   <td height="19" width="728">Número máximo de intentos permitidos para que el alumno consuma el módulo.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Estado del usuario</b></p></td> 
   <td valign="middle">No puede estar nunca vacía.</td> 
   <td valign="middle">Estado del usuario del alumno: Activo/Eliminado/Suspendido.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Campo activo agrupable</b></td> 
   <td height="38" width="283">Puede estar vacía.</td> 
   <td height="38" width="728">Para cada campo activo agrupable, habrá una columna, donde el nombre de columna será el de ese campo activo y el valor será el valor específico que tiene el alumno para ese campo.</td> 
  </tr> 
  <tr> 
   <td><p><b>Nombre del responsable</b></p></td> 
   <td><p><i>Puede estar vacía.</i></p></td> 
   <td height="19" width="728">El nombre del responsable del alumno.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de inscripciones</b></td> 
   <td height="38" width="283">1 ó 0</td> 
   <td height="38" width="728">Recuento de inscripciones del alumno para el objeto de aprendizaje. La fila de objetos de aprendizaje de nivel más alto muestra un valor = '1'. Las subformaciones muestran un valor 0.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Recuento iniciado</b></td> 
   <td height="19" width="283">1 ó 0</td> 
   <td height="19" width="728">Se inició el recuento del alumno para el objeto de aprendizaje. La fila de objetos de aprendizaje de nivel más alto muestra un valor = '1'. Las subformaciones muestran un valor 0.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Recuento de finalización</b></td> 
   <td height="58" width="283">1 ó 0</td> 
   <td height="58" width="728">Recuento de finalización del alumno para el objeto de aprendizaje. La fila de objetos de aprendizaje de nivel más alto muestra un valor = '1' si el alumno está pendiente de finalización en esa formación. Las subformaciones muestran un valor 0 incluso cuando están en estado Pendiente. La fila de objetos de aprendizaje de nivel más alto muestra un valor = '0', si el alumno ha completado la formación.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vencimiento en N días</b></td> 
   <td height="38" width="283">1 ó 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0', dependiendo de la fecha límite de la instancia a la que se inscriba el alumno de formación. Depende del valor introducido en la hoja Resumen de aprendizaje I &gt; campo "Fecha de vencimiento".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vencimiento en N días para el usuario</b></td> 
   <td height="38" width="283">1 ó 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0', dependiendo de la fecha límite de la instancia a la que se inscriba el alumno de formación. Depende del valor introducido en la hoja Resumen de aprendizaje II &gt; campo 'Fecha de vencimiento próximamente'.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de (progreso superior a N %)</b></td> 
   <td height="38" width="283">1 ó 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0' en función del progreso del alumno en la formación. Depende del valor introducido en la hoja Resumen de aprendizaje I &gt; campo "Progreso mayor que".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Recuento de (progreso superior a N %) para el usuario</b></td> 
   <td height="38" width="283">1 ó 0</td> 
   <td height="38" width="728">Esto muestra un valor de '1' o '0' en función del progreso del alumno en la formación. Depende del valor introducido en la hoja Resumen de aprendizaje II &gt; campo "Progreso mayor que".</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID de formación</b></td> 
   <td height="19" width="283">No puede estar nunca vacía.</td> 
   <td height="19" width="728">ID de formación de la formación.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Duración del módulo o el curso de formación (min)</b></td> 
   <td height="20" width="283">No puede estar nunca vacía.</td> 
   <td height="20" width="728">Duración total de la formación o del módulo (minutos) de la instancia predeterminada de la formación.</td> 
  </tr> 
 </tbody> 
</table>

### Resumen de aprendizaje I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Nombre de la columna<br></th> 
   <th>Tipo de valor</th> 
   <th>Descripción</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Tipo</td> 
   <td height="19" width="253">Todos, Programa de aprendizaje, Certificado, Curso.</td> 
   <td height="19" width="412">Tipo de objetos de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Campo agrupable(perfil)</td> 
   <td height="19" width="253">No puede estar nunca vacía.</td> 
   <td height="19" width="412">Perfil para el que la tabla de resumen de aprendizaje debe mostrar datos.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Nombre del responsable</td> 
   <td height="38" width="253">No puede estar nunca vacía.</td> 
   <td height="38" width="412">El nombre del responsable cuyos datos de participación en objetos de aprendizaje de los subordinados deben mostrarse en la tabla Resumen de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Etiquetas de fila</td> 
   <td height="19" width="253">No puede estar nunca vacía.</td> 
   <td height="19" width="412">El nombre del objeto de aprendizaje con la lista de alumnos inscritos en el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos inscritos</td> 
   <td height="19" width="253">No puede estar nunca vacía.</td> 
   <td height="19" width="412">Número de alumnos inscritos en el acuerdo de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos que han comenzado</td> 
   <td height="19" width="253">No puede estar nunca vacía.</td> 
   <td height="19" width="412">Número de alumnos que han iniciado el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alumnos que han finalizado</td> 
   <td height="19" width="253">No puede estar nunca vacía.</td> 
   <td height="19" width="412">Número de alumnos que han completado el objeto de aprendizaje.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Número de alumnos que han progresado &gt;= N %</td> 
   <td height="38" width="253">No puede estar nunca vacía.</td> 
   <td height="38" width="412">Número de alumnos que han progresado &gt;= N % (valores).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Número de alumnos con fecha de vencimiento en N días</td> 
   <td height="39" width="253">No puede estar nunca vacía.</td> 
   <td height="39" width="412">Número de alumnos con fecha de vencimiento en N días (valores).</td> 
  </tr> 
 </tbody> 
</table>

### Resumen de aprendizaje II

| Nombre de la columna | Tipo de valor | Descripción |
|---|---|---|
| Tipo | Todos, Programa de aprendizaje, Certificado, Curso. | Tipo de objetos de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos. |
| Campo agrupable(perfil) | No puede estar nunca vacía. | Perfil para el que la tabla de resumen de aprendizaje debe mostrar datos. |
| Nombre del responsable | No puede estar nunca vacía. | El nombre del responsable cuyos datos de participación en objetos de aprendizaje de los subordinados deben mostrarse en la tabla Resumen de aprendizaje. |
| Etiquetas de fila | No puede estar nunca vacía. | Se ha inscrito el nombre del alumno con la lista de alumnos de objetos de aprendizaje. |
| Número de objetos de aprendizaje inscritos | No puede estar nunca vacía. | Número de objetos de aprendizaje a los que se ha inscrito el alumno. |
| Número de objetos de aprendizaje iniciados | No puede estar nunca vacía. | Número de objetos de aprendizaje que ha iniciado el alumno. |
| Número de objetos de aprendizaje completados | No puede estar nunca vacía. | Número de objetos de aprendizaje completados por el alumno. |
| Número de objetos de aprendizaje que han progresado >= N % | No puede estar nunca vacía. | Número de objetos de alumno que han progresado >= N %. |
| Número de objetos de aprendizaje con fecha de vencimiento en N días | No puede estar nunca vacía. | Número de objetos de aprendizaje con fecha de vencimiento en N días. |

### Resumen del cumplimiento

| Nombre de la columna | Tipo de valor | Descripción |
|---|---|---|
| Tipo | Todos, Programa de aprendizaje, Certificado, Curso. | Tipo de objetos de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos. |
| Etiquetas de fila (columna del lado izquierdo) | No puede estar nunca vacía. | Se ha inscrito el nombre del alumno con la lista de alumnos de objetos de aprendizaje. |
| Etiquetas de fila (columna del lado izquierdo) | No puede estar nunca vacía. | Se ha inscrito el nombre del alumno con la lista de alumnos de objetos de aprendizaje. |

### Transcripción de aptitudes

| .Nombre de la columna | Tipo de valor | Descripción |
|---|---|---|
| Nombre | No puede estar nunca vacía. | El nombre del alumno. |
| correo electrónico | No puede estar nunca vacía. | La dirección de correo electrónico del alumno. |
| Adobe ID | Puede estar vacía. | Adobe ID del alumno |
| ID exclusivo de usuario | Puede estar vacía. | ID exclusivo de usuario del alumno. Esta columna se basa en la configuración de back-end si está activada o desactivada en el nivel de cuenta. |
| Aptitud | No puede estar nunca vacía. | Se ha asignado el nombre de la aptitud al alumno. |
| Nivel de aptitud | No puede estar nunca vacía. | Nivel de aptitud asignado al alumno. |
| Créditos requeridos | No puede estar nunca vacía. | Créditos totales requeridos por el alumno para conseguir la aptitud. |
| Créditos obtenidos | No puede estar nunca vacía. | Créditos totales obtenidos por el alumno para la aptitud. |
| Porcentaje de finalización | No puede estar nunca vacía. | Porcentaje de progreso para lograr la aptitud. |
| Fecha asignada (zona horaria UTC) | No puede estar nunca vacía. | Fecha en la que se asignó la aptitud al alumno. |
| Fecha de logro (zona horaria UTC) | No puede estar nunca vacía. | Fecha en la que el alumno adquirió la aptitud. |
| Estado del usuario | No puede estar nunca vacía. | Estado del usuario del alumno: Activo/Eliminado/Suspendido. |
| Campo activo agrupable | Puede estar vacía. | Para cada campo activo agrupable, habrá una columna, donde el nombre de columna será el de ese campo activo y el valor será el valor específico que tiene el alumno para ese campo. |
| Nombre del responsable | Puede estar vacía. | Nombre del responsable del alumno. |

### Resumen de aptitudes I

| Nombre de la columna | Tipo de valor | Descripción |
|---|---|---|
| Después | No puede estar nunca vacía. | Número de alumnos que obtuvieron la aptitud antes del número de días introducido (valor) que debe actualizarse. |
| Nombre | Todo o cualquier nombre de alumno | El nombre del alumno que tiene asignada una aptitud. |
| Nombre del responsable | No puede estar nunca vacía. | El nombre del responsable cuyos datos de participación en aptitudes de los subordinados deben mostrarse en la tabla Resumen de la aptitud. |
| Etiquetas de fila | No puede estar nunca vacía. | El nombre de la aptitud con la lista de alumnos asignados a la aptitud. |
| Número de usuarios que deben tener esta aptitud | No puede estar nunca vacía. | Número de alumnos asignados a la aptitud. |
| Número de usuarios que han conseguido esta aptitud | No puede estar nunca vacía. | Número de alumnos que han alcanzado la aptitud. |
| Cantidad de alumnos que deben poner al día la aptitud | No puede estar nunca vacía. | El número de alumnos cuya aptitud se debe actualizar. |
| Porcentaje de cumplimiento (según aptitud conseguida) | No puede estar nunca vacía. | El porcentaje de progreso de la aptitud asignada. |

### Resumen de aptitudes II

| Nombre de la columna | Tipo de valor | Descripción |
|---|---|---|
| Después | No puede estar nunca vacía. | Número de alumnos que obtuvieron la aptitud antes del número de días introducido (valor) que debe actualizarse. |
| Aptitud | Todos o cualquier nombre de aptitud | Los nombres de las aptitudes asignadas a los alumnos. |
| Nombre del responsable | No puede estar nunca vacía. | El nombre del responsable cuyos datos de participación en aptitudes de los subordinados deben mostrarse en la tabla Resumen de la aptitud. |
| Etiquetas de fila | No puede estar nunca vacía. | El nombre del alumno con la lista de aptitudes asignadas. |
| El número de aptitudes que debe tener cada usuario. | No puede estar nunca vacía. | El número de aptitudes asignadas al alumno. |
| El número de aptitudes que tiene cada usuario. | No puede estar nunca vacía. | El número de aptitudes obtenidas por el alumno. |
| El número de aptitudes que se deben actualizar. | No puede estar nunca vacía. | El número de alumnos cuya aptitud se debe actualizar. |
| Porcentaje de cumplimiento | No puede estar nunca vacía. | El porcentaje de progreso de la aptitud asignada. |

* A veces, los administradores pueden marcar la finalización de un objeto de aprendizaje manualmente (especialmente para los cursos en clase) mucho después de que haya finalizado la clase. En ese caso, si la opción Exportar datos se ha configurado para que exporte diariamente transcripciones de alumnos, es posible que la fecha real de finalización ya haya pasado y, por lo tanto, la exportación nunca obtendrá esos registros de finalización marcados como completados mucho después de que haya terminado la clase. Cuando esto se detecte, considere la posibilidad de exportar la transcripción desde una fecha de inicio determinada hasta la fecha (a petición) en la interfaz de usuario; a continuación, llévela a la aplicación descendente para un &quot;procesamiento posterior&quot;. Al hacer esto, es posible que deba omitir los registros que ya se han procesado.
* Varios intentos para un módulo dependen de si está activado para ese objeto de aprendizaje. Si está activado, lo que aparece ahora en una fila del archivo CSV relacionada con un módulo es un intento. No se pueden notificar todos los intentos de un día, por lo que puede que aparezca un incremento superior a uno en el número total de intentos. Además, un intento no tiene por qué mejorar necesariamente una puntuación; en un momento dado, solo recibirá la mejor puntuación.
