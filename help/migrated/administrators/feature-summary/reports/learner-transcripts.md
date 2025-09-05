---
description: Las transcripciones de alumnos en Adobe Learning Manager (ALM) permiten a los administradores supervisar el progreso de los alumnos en cursos, módulos, rutas de aprendizaje y certificaciones. Apoya las evaluaciones de rendimiento, la supervisión del cumplimiento, las auditorías y la presentación de informes externos. El informe ofrece un resumen completo de la participación y el rendimiento de un alumno.
jcr-language: en_us
title: Transcripciones de alumnos en Adobe Learning Manager
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '4221'
ht-degree: 8%

---


# Transcripciones de alumnos en Adobe Learning Manager

## Información general

Las transcripciones de alumnos en Adobe Learning Manager (ALM) permiten a los administradores realizar un seguimiento del progreso de los alumnos en un nivel concreto en todos los cursos, módulos, rutas de aprendizaje y certificaciones. Los datos de transcripción ayudan a las revisiones de rendimiento, el seguimiento del cumplimiento, las auditorías y las necesidades de informes externos.

>[!NOTE]
>
>Las transcripciones de alumnos están disponibles para que las descarguen los administradores, administradores personalizados, responsables o alumnos.

En el caso de los alumnos, deben iniciar la configuración de su perfil y luego descargar sus transcripciones de aprendizaje como un archivo de Excel. Esta transcripción, generada para un alumno individual, detalla su recorrido de aprendizaje personal. Incluye los nombres de las rutas de aprendizaje, los cursos, las instancias y los módulos, junto con las fechas clave, como la inscripción, la finalización y las fechas límite. También realiza un seguimiento de su progreso a través del estado, las notas, las puntuaciones de las pruebas (incluidas las puntuaciones y los máximos más altos) y los intentos realizados. Además, muestra los ID de formación, las duraciones, las fechas de darse de baja, los precios y cualquier comentario de envío. Este informe proporciona una descripción general completa de la participación y el rendimiento de un único alumno.

Las organizaciones pueden utilizar las transcripciones de alumnos para añadir los datos de comportamiento de aprendizaje a un almacén de datos de empresa, donde se pueden combinar datos de aprendizaje con otros datos de empresa para analizar las correlaciones entre el comportamiento de aprendizaje y otros datos de proceso.

## Propósito y ventajas

* Crea registros listos para auditoría para los requisitos normativos con marcas de tiempo y pruebas de finalización.
* Conecta las actividades de aprendizaje con el desarrollo y la adquisición de habilidades de los empleados.
* Realiza un seguimiento del estado de certificación de las funciones que requieren formación obligatoria.
* Apoya la medición cuantitativa de la eficacia del programa de aprendizaje.

## Casos prácticos de transcripciones de alumnos

Las transcripciones de alumnos en Adobe Learning Manager hacen un seguimiento de la formación, el cumplimiento normativo y el desarrollo de aptitudes, lo que permite a los departamentos verificar la finalización y evaluar la eficacia de los programas en toda la organización.  A continuación se indican algunos casos de uso que se dirigen a las transcripciones de alumnos:

* Una organización de servicios financieros debe proporcionar pruebas de que todos los empleados orientados al cliente han completado la formación obligatoria sobre cumplimiento antes del plazo reglamentario.
* El departamento de TI debe evaluar las capacidades actuales de programación de Java en relación con los futuros requisitos del proyecto.
* HR desea evaluar la eficacia del nuevo programa de incorporación de empleados en diferentes departamentos.
* El equipo de operaciones debe garantizar que todos los técnicos de campo mantengan las certificaciones de seguridad necesarias.

## Control de acceso y permisos

**Administradores**

* Puede generar transcripciones para todos los alumnos en todos los catálogos.
* Puede acceder a todas las funciones de creación de informes, pero puede tener restricciones de catálogo o grupo de usuarios.
* Administradores personalizados: acceso limitado por el ámbito y los permisos asignados.

**Restricciones basadas en el ámbito**

* Los administradores personalizados solo pueden ver transcripciones de alumnos dentro de sus grupos de usuarios asignados.
* Los informes solo incluirán objetos de aprendizaje de los catálogos a los que el administrador tenga permiso de acceso.

## Cómo generar transcripciones de alumnos

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **[!UICONTROL Informes]** en el menú de navegación izquierdo.
3. Selecciona **[!UICONTROL Informes personalizados]** en Informes y luego selecciona **[!UICONTROL Informes de Excel]**.
4. Seleccione **[!UICONTROL Transcripciones de alumnos]**.

   ![] ()

5. Seleccione **[!UICONTROL Generar nuevo]**.
6. Seleccione el intervalo de fechas para el que necesita generar la transcripción. De forma predeterminada, la fecha **[!UICONTROL Desde]** es la fecha de registro del alumno, y la fecha **[!UICONTROL Hasta]** siempre es la fecha actual. Solo puede modificar la fecha de inicio &quot;desde&quot; cuando necesita los datos.
7. Seleccione lo siguiente:
a. Seleccione los nombres de los alumnos en la sección **[!UICONTROL Seleccionar alumnos]**. Puede seleccionar usuarios o grupos de usuarios, o puede copiar y pegar las direcciones de correo electrónico de los alumnos para los que desea generar transcripciones. Consulte la sección [Generar transcripción del alumno](#generate-learner-transcript-using-copy-paste) usando copiar y pegar para obtener más información.
b. Seleccione catálogos específicos en la lista desplegable **[!UICONTROL Seleccionar catálogos]**. La transcripción solo se descarga para los catálogos especificados.\
   c. Seleccione el **[!UICONTROL Estado de inscripción]**. Esta lista desplegable contiene las siguientes opciones:

       * Seleccionar todo
       * Completado
       * En curso
       * No iniciado
       * Dado de baja
   &#x200B;8. Opciones avanzadas: seleccione **[!UICONTROL Opciones avanzadas]** para descargar las transcripciones e incluir lo siguiente:

   a. Descargue transcripciones de alumnos que se han eliminado de una cuenta seleccionando la casilla de verificación **[!UICONTROL Incluir alumnos eliminados]**.
b. Descargue información del nivel de módulo en la transcripción del alumno activando la casilla de verificación **[!UICONTROL Habilitar información del nivel de módulo]**. En este caso, los nombres de los módulos y el tiempo empleado en cada módulo se obtienen como parte de la transcripción si esta opción está activada.
c. Descargue datos de aptitudes y hojas de resumen activando la casilla de verificación **[!UICONTROL Incluir datos de aptitudes y hojas de resumen]**. Consulte la sección Informes de Excel para obtener más información.
&#x200B;9. También puede seleccionar los valores de columna que se van a rellenar en el informe. Esto proporciona flexibilidad para descargar informes con valores de columna específicos según sea necesario. Seleccione las columnas en el menú desplegable.

   

Las transcripciones se generan y se descargan en el equipo como archivos .zip cuando no se incluyen los datos de aptitudes. Si la casilla Datos de aptitudes está activada, las transcripciones se generan y se descargan como . archivos xlsx.

### Generar una transcripción de alumno mediante copiar y pegar

La obtención de transcripciones de alumnos se convierte en un proceso tedioso, ya que solo se puede obtener para un alumno o un grupo de usuarios cada vez. Aquí, con la función de copiar y pegar, puede copiar la lista de ID de correo electrónico del alumno y pegarla de una sola vez.

1. Seleccione la pestaña **[!UICONTROL ID de correo electrónico]** para introducir la lista copiada de ID de correo electrónico únicos.

   

2. Pegue los ID de correo electrónico exclusivos de los alumnos que desea añadir, separados por una coma, un punto y coma o un salto de línea.
3. Selecciona **[!UICONTROL Validar ID de correo electrónico]** para comprobar si el ID de correo electrónico que has introducido es válido. En caso de que el ID de correo electrónico introducido sea incorrecto, se resaltará en rojo junto con un mensaje de validación.

   >[!NOTE]
   >
   >El botón Generar permanecerá desactivado a menos que todos los ID de correo electrónico introducidos sean correctos.

4. Seleccione **[!UICONTROL Generar]** para generar transcripciones de alumnos para todos los ID de correo electrónico mencionados.

   >[!NOTE]
   >
   >La generación de transcripciones de alumnos se puede combinar para los ID de correo electrónico introducidos en la ficha Usuarios e ID de correo electrónico .

### ¿Qué contiene el informe Transcripciones de alumnos?

El informe de transcripciones de alumnos es una combinación de información relacionada con el usuario, la inscripción y los objetos de aprendizaje.
En las tablas siguientes se describe cada tipo:

**Información relacionada con el usuario**

Las siguientes columnas identifican al alumno.

| Campo | Descripción |
|---|---|
| Nombre | El nombre del alumno. |
| Correo electrónico | Dirección de correo electrónico del alumno. |
| Adobe ID | Este campo se rellena solo cuando los usuarios inician sesión con su Adobe ID. Si acceden a Adobe Learning Manager a través de un [inicio de sesión único (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) definido por la organización, el campo de Adobe ID permanecerá en blanco. |
| ID exclusivo de usuario | El ID exclusivo de usuario es un ID externo generado por las cuentas en caso de que no tengan ID de correo electrónico de todos los usuarios o ID de correo electrónico exclusivos de todos los usuarios. <br>El campo Id. único de usuario es un campo opcional que se puede habilitar para una cuenta. El propósito principal del campo es permitir que las cuentas etiqueten a cada usuario con un ID exclusivo para realizar un seguimiento, actualizar los registros de usuario mediante API, auditar o sincronizar datos en flujos de trabajo automatizados. El etiquetado de cada usuario se realiza mediante la importación de usuarios mediante CSV.</br><br>Si una cuenta ha optado por un ID de usuario único, los informes, como las transcripciones de alumnos, Adobe Learning Manager proporciona la columna en los informes.</br> |

**Información relacionada con la inscripción**

Las siguientes columnas capturan la actividad, el progreso o los intentos.

| Campo | Descripción |
|---|---|
| Fecha de inscripción (zona horaria UTC) | Marca de fecha y hora de inscripción del alumno en el tipo de objeto de aprendizaje, que es curso, certificación o ruta de aprendizaje. |
| Marcar fecha de finalización (zona horaria UTC) | Marca de fecha y hora del momento en que un instructor marca una sesión o módulo como completada. Tenga en cuenta que si no se ha producido una sesión, la columna aparece en blanco en el informe. Además, si se ha producido una sesión y el instructor no la ha marcado como completa, la columna aparece en blanco en el informe. |
| Fecha de inicio (zona horaria UTC) | Fecha y hora en que el alumno inició el objeto de aprendizaje. Si está vacía, esto indica que el alumno no ha iniciado aún este objeto de aprendizaje. |
| Fecha de finalización (zona horaria UTC) | Fecha y hora en que el alumno completó este objeto. Si está vacío, significa que el alumno aún no lo ha completado. |
| Plazo (zona horaria UTC) | Fecha y hora en las que se espera que el alumno complete este objeto de aprendizaje. Si está vacía, esto implica que no hay ningún plazo para este objeto de aprendizaje. |
| Vencido | Estado vencido actual del alumno inscrito en el objeto de aprendizaje. Sí/No |
| Estado | Indica el estado del alumno al realizar el curso, la certificación o la ruta de aprendizaje.  Los estados disponibles son No iniciado, Dado de baja, En curso o Completado. |
| Progreso % | Progreso actual % del alumno que realiza el curso, certificación o ruta de aprendizaje. |
| Tiempo empleado (minutos) | El tiempo de aprendizaje empleado por el alumno en el objeto de aprendizaje, las filas del nivel de módulo muestran el tiempo de aprendizaje empleado del módulo individual. Las filas del nivel Curso/Ruta de aprendizaje/Certificado muestran el tiempo de aprendizaje agregado dedicado. |
| Nota | Indica el éxito del alumno. &quot;Aprobado&quot;, si el usuario ha cumplido los criterios de éxito de este objeto de aprendizaje; de lo contrario, &quot;Suspendido&quot;. |
| Puntuación_de_prueba | La puntuación de prueba más reciente obtenida por el alumno. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba, o si el administrador o el instructor no ha asignado ninguna puntuación. |
| Puntuación_máx_de_prueba | La puntuación máxima de prueba más reciente posible para el módulo. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba. |
| Puntuación_más_alta_de_prueba | La puntuación de prueba más alta obtenida por el alumno en varios intentos. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba, o si el administrador o el instructor no han asignado ninguna puntuación. |
| Puntuación_más_alta_de_prueba_máx | Las puntuaciones máximas de prueba más altas posibles para el módulo. Puede estar vacía si el alumno no ha intentado realizar la prueba o si el contenido no contiene ninguna prueba. |
| Intentos realizados | El número total de intentos realizados por el alumno para este módulo hasta la fecha actual. |
| Máximo de intentos permitidos | El número máximo de intentos permitido para que el alumno consuma el módulo. |
| Comentarios del envío | Comentarios del responsable de un alumno después de completar un objeto de aprendizaje.<br>Los datos de comentarios de envío proporcionados por el instructor se incluyen en el módulo de envío de archivos . Vea <a href="https://experienceleague.adobe.com/es/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules">Modules-Adobe Learning Manager para obtener más información.</a></br> |
| Origen de finalización | <b>Nota:</b> En los flujos de trabajo de asistencia del conector de clase virtual, cuando un alumno se marca como asistido automáticamente, el origen mostrará &quot;SELF, (learner_email)&quot;. |
| Comentario de finalización | Los comentarios realizados por el administrador cuando marcan a un alumno como completado después de completar un curso, una certificación o una ruta de aprendizaje. El administrador puede añadir comentarios de finalización para uno o varios alumnos. Consulte <a href="https://experienceleague.adobe.com/es/docs/learning-manager/using/admin/courses#completion-comments">Comentarios de finalización</a> para obtener más información. |

**Información relacionada con objetos de aprendizaje**

Se refieren a cursos, módulos, rutas de aprendizaje, certificaciones, etc.

| Campo | Descripción |
|---|---|
| Nombre del plan de aprendizaje | Título del plan de aprendizaje. |
| Programa de aprendizaje/Certificación/Curso | Título del objeto de aprendizaje. |
| Tipo | El tipo de objeto de aprendizaje en el que se inscribió el usuario. Por ejemplo,<ul><li>Ruta de aprendizaje</li><li>Certificación</li><li>Curso</li></ul> |
| Ruta incrustada | Una ruta incrustada es un tipo de ruta de aprendizaje que se incluye como parte de otro curso     o una ruta de aprendizaje. El campo indica que un alumno está completando esa ruta de aprendizaje como parte de otra ruta de aprendizaje, en lugar de como una asignación independiente. |
| Curso | Nombre del curso en el que está inscrito el usuario. Si está vacía, la fila representa una certificación o una ruta de aprendizaje. <br><b>Nota:</b> Aunque rutas de aprendizaje y certificaciones    se componen de cursos individuales o rutas de aprendizaje anidadas, cada componente conserva su propio registro independiente. Esto garantiza que el seguimiento de los datos de progreso, finalización y generación de informes se realice por separado para los elementos primarios y secundarios.</br> |
| ID exclusivo de objetos | El ID exclusivo del objeto de aprendizaje. Es necesario si el cliente tiene el objeto de aprendizaje en un sistema externo que tiene su propio identificador. Esto resulta útil si desea asignar el identificador de objeto de aprendizaje del sistema externo y el objeto de aprendizaje de Adobe Learning Manager.<br>Un administrador puede habilitar la opción Identificadores únicos de objetos de aprendizaje en la página Configuración. Cuando está activada, Adobe Learning Manager asigna un ID exclusivo a un objeto de aprendizaje cada vez que un autor crea un curso, una certificación o una ruta de aprendizaje. </br> |
| Instancia | El nombre de la instancia del usuario del objeto de aprendizaje en el que se inscribe. |
| Criterios de selección | Base de la inscripción (cómo se inscribió este alumno en este objeto de aprendizaje).<br>En Adobe Learning Manager, los alumnos pueden inscribirse en objetos de aprendizaje mediante varios métodos: Inscripción nominada por responsable: los responsables nominan a los alumnos para cursos específicos. Los alumnos no pueden inscribirse automáticamente en estos cursos.</br><ul><li>Inscripción aprobada por el responsable: los alumnos se inscriben en los cursos, pero la inscripción requiere la aprobación del responsable.</li><li>Inscripción automática: los alumnos se inscriben directamente en los cursos sin necesidad de aprobación.</li><li>Inscritos por el administrador: los administradores inscriben manualmente a los alumnos en los cursos.</li></ul> |
| Módulo | Nombre del módulo de los cursos. En el informe sólo aparecen los módulos con el estado Completado o En curso. Si el estado es No iniciado o Dado de baja, la columna Módulo permanece vacía.<br>Descargue información de nivel de módulo en la transcripción del alumno marcando la casilla de verificación <b>Habilitar información de nivel de módulo</b>. En este caso, los nombres de los módulos y el tiempo empleado en cada módulo se obtienen como parte de la transcripción si esta opción está habilitada.</br> |
| ID de módulo | El ID exclusivo del módulo.<br><b>Nota:</b> La columna Id. de módulo aparece en el informe solo si ha seleccionado la casilla de verificación Incluir información de módulo al generar la transcripción.</br> |
| Versión | La versión del módulo hace referencia a la versión específica de un módulo con la que ha interactuado un alumno. Esto resulta especialmente útil cuando un módulo se ha actualizado o modificado, ya que permite a los administradores realizar un seguimiento de la versión del módulo a la que ha accedido el alumno.<br>Cuando un autor carga una nueva versión de un módulo, Adobe Learning Manager la trata como una nueva versión del módulo existente. Esto permite actualizar el contenido sin interrumpir la actividad de todos los alumnos.</br><br>La versión aparece si se seleccionó la casilla de verificación <b>Habilitar información de nivel de módulo</b> al generar el informe.</br><br>Consulte <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" />Actualización de un módulo en Adobe Learning Manager</a> para obtener más información.</br> |
| Tipo de entrega | Indica cómo se proporciona el módulo: Combinado, Clase o Clase virtual. |
| Idioma | Idioma en el que el alumno consume el módulo. Esta columna muestra el valor solo para los módulos de aprendizaje electrónico. |
| Vencido | Estado vencido actual del alumno inscrito en el objeto de aprendizaje. Sí/No |
| Nota | Indica el éxito del alumno. &quot;Aprobado&quot;, si el usuario ha cumplido los criterios de éxito de este objeto de aprendizaje; de lo contrario, &quot;Suspendido&quot;. |

>[!INFO]
>
>Las siguientes columnas están ocultas en las transcripciones de alumnos:
>
>* Recuento de inscripciones
>* Recuento iniciado
>* Recuento de finalización
>* Vencimiento en N días
>* Vencimiento en N días para el usuario
>* Recuento de (progreso superior a N %)
>* Recuento de (progreso superior a N %) para el usuario
>
>Estas columnas solo aparecen si ha seleccionado Incluir datos de aptitudes y hojas de resumen al generar la transcripción. Estas columnas se utilizan para calcular los detalles de resumen de un alumno inscrito en un objeto de aprendizaje.

| Campos | Descripción |
|---|---|
| ID del curso de formación | Un identificador único generado por el sistema y asignado a la inscripción de cada alumno en un curso, certificación o ruta de aprendizaje específicos. Si un alumno se vuelve a inscribir en el mismo curso, se generará un nuevo ID de formación. Un alumno puede tener varios ID de formación para el mismo curso. |
| Duración del módulo o el curso de formación (min) | Esta columna muestra la duración esperada (en minutos) de un curso, módulo o actividad de formación tal y como se define al crear el curso. No es el tiempo real que pasa un alumno, sino la duración configurada o asignada lo que representa el tiempo que se supone que debe tomar la formación. <br>Esta columna muestra la duración total (en minutos) del elemento de aprendizaje asignado, que puede ser una ruta de aprendizaje o un curso individual.</br><br><b>Duración de la ruta de aprendizaje:<b> Si el elemento de aprendizaje es una ruta de aprendizaje, su duración se calcula como la suma de las duraciones de todos los cursos incluidos en la ruta de aprendizaje.</br><br>Ejemplo: si el curso 1 = 50 minutos y el curso 2 = 60 minutos, la duración de la ruta de aprendizaje = 110 minutos.</br><br><b>Duración del curso individual:</b>Si el elemento de formación es un curso individual (no parte de una ruta de aprendizaje), la duración refleja el tiempo necesario solo para ese curso.</br> |
| Embedded_Course_ID | El ID del curso que forma parte de una ruta de aprendizaje o de cualquier otro curso.<br>La columna se rellena cuando la fila representa una ruta de aprendizaje o la propia certificación. Muestra los ID de los cursos individuales incrustados en la ruta de aprendizaje o la certificación. No se rellena cuando la fila en sí es un curso en ly, ya que no hay elementos incrustados.</br> |
| ID de ruta incrustada | Identificador de la ruta de acceso en la que existe el curso incrustado.<br>La columna identifica el ID exclusivo de las rutas de aprendizaje incrustadas. Ayuda a realizar un seguimiento de los cursos en las rutas de aprendizaje y proporciona visibilidad de la estructura jerárquica de las rutas de aprendizaje.</br> |
| Fecha de baja (zona horaria UTC) | Fecha de cancelación de la inscripción del alumno en el tipo de objeto de aprendizaje. |
| Precio($) | El precio del objeto de aprendizaje para el que se ha adquirido en el catálogo de cursos. Para que esta columna aparezca en la transcripción del alumno, el administrador debe activar la casilla de verificación Habilitar precios para cursos/rutas de aprendizaje/certificaciones en la configuración de la cuenta. |

## Informes de Excel

El cuadro de diálogo Transcripciones de alumnos también permite descargar datos de aptitudes y hojas de resumen como archivos de Excel. Marque la casilla de verificación **[!UICONTROL Incluir datos de aptitudes y hojas de resumen]** y, a continuación, seleccione **[!UICONTROL Generar]** para descargar un archivo de Excel con las siguientes hojas:

* Resumen de aprendizaje I
* Resumen de aprendizaje II
* Resumen del cumplimiento
* Transcripción de aptitudes
* Resumen de aptitudes I
* Resumen de aptitudes II



### ¿Qué contiene la hoja Resumen del aprendizaje?

Realiza un seguimiento de las rutas de aprendizaje, los cursos o las certificaciones que se utilizan de forma activa. Realiza un seguimiento de la actividad en curso, así como de las fechas de vencimiento próximas para la formación.

* Número de alumnos inscritos: indica cuántos alumnos se han inscrito en un objeto de aprendizaje concreto (curso, ruta de aprendizaje o certificación), independientemente de si lo han iniciado o no.
* Número de alumnos que han comenzado: muestra el número de alumnos que han iniciado o iniciado el curso, la certificación o la ruta de aprendizaje.
* Número de alumnos que han completado: muestra cuántos alumnos han completado correctamente el curso de formación y han cumplido todos sus criterios de finalización.
* Número de alumnos que han progresado ≥ N%: Refleja el recuento de alumnos que han alcanzado al menos el umbral de progreso especificado (p. ej., 70%) en el curso de formación, incluso aunque no lo hayan completado.
* Número de alumnos con fecha de vencimiento en n días: indica cuántos alumnos tienen formación prevista en los próximos &quot;N&quot; días (p. ej., 7 días), lo que resulta útil para identificar las próximas fechas límite.

### Cómo interpretar los datos

Este informe de resumen de aprendizaje realiza un seguimiento de dos rutas de aprendizaje asignadas al alumno.
Del ejemplo,



* El usuario se ha inscrito en dos rutas de aprendizaje y ha iniciado ambas.
* Ninguno de los caminos de aprendizaje se ha completado todavía.
* El alumno aún no ha superado el umbral del 70 % en ninguna de las rutas.
* No hay fechas de vencimiento en los próximos siete días para ninguno de los dos cursos de formación.

### ¿Qué contiene la hoja Resumen de aprendizaje II?

Haz un seguimiento de la actividad de aprendizaje por alumno. Realiza un seguimiento de las inscripciones, la actividad en curso y las fechas de vencimiento de los alumnos.

* Número de objetos de aprendizaje inscritos: número total de objetos de aprendizaje (LO) en los que se inscribe el alumno en cada curso, certificación o ruta de aprendizaje. cuenta por separado .
* Número de objetos de aprendizaje iniciados: indica cuántos de los objetos de aprendizaje inscritos ha iniciado o comenzado el alumno.
* Número de objetos de aprendizaje completados: Muestra el número de objetos de aprendizaje iniciados que el alumno ha completado.
* Número de objetos de aprendizaje que han progresado ≥ N%: Refleja el número de objetos de aprendizaje en los que el alumno ha alcanzado al menos el umbral de progreso especificado (en este caso, el 70%).
* Número de objetos de aprendizaje con fecha de vencimiento en N días: identifica los objetos de aprendizaje que vencen en el siguiente número de días establecido (en este caso, 7 días), lo que ayuda a realizar un seguimiento de los plazos que se acercan.

### Cómo interpretar los datos

Del ejemplo,



* El alumno se inscribe en dos objetos de aprendizaje y ha iniciado ambos.
* No se ha completado ningún objeto de aprendizaje.
* El alumno aún no ha alcanzado el 70 % de progreso en ninguno de ellos.
* Ninguno de los objetos de aprendizaje vencerá en los próximos 7 días.

### ¿Qué contiene la hoja Resumen de conformidad?

Realiza un seguimiento de los alumnos con fechas de vencimiento próximas para cursos, rutas de aprendizaje o certificaciones clave.

| Columna | Descripción |
|---|---|
| Tipo | El tipo de objeto de aprendizaje para el que la tabla Resumen de aprendizaje debe mostrar datos. |
| Etiquetas de fila (columna del lado izquierdo) | El nombre del alumno con la lista de objetos de aprendizaje en los que se ha inscrito el alumno. |

### ¿Qué contiene la hoja Transcripción de aptitudes?

| Columna | Descripción |
|---|---|
| Nombre | El nombre completo del alumno asociado a la transcripción de la aptitud. |
| Correo electrónico | Dirección de correo electrónico del alumno. |
| ID exclusivo de usuario | Identificador único definido por la organización para el alumno. |
| Aptitud | El nombre de la aptitud asignada al alumno (por ejemplo, Programación Java, Liderazgo). |
| Nivel de aptitud | El nivel de experiencia dentro de la aptitud que se espera que alcance el alumno (por ejemplo, principiante, intermedio, avanzado). |
| Créditos requeridos | Número de créditos de aprendizaje necesarios para alcanzar el nivel de aptitud asignado. |
| Créditos obtenidos | El número de créditos que el alumno ha obtenido para completar el nivel de aptitud asignado. |
| Porcentaje de finalización | El porcentaje de créditos necesarios que ha completado el alumno. |
| Fecha de asignación (UTC) | La fecha en la que se asignó la aptitud al alumno. |
| Fecha de obtención (UTC) | La fecha en la que el alumno obtuvo los créditos necesarios y cumplió los criterios de nivel de aptitud. |
| Nombre del responsable | El nombre del responsable del alumno que supervisa el progreso del aprendizaje. |

### ¿Qué contiene la hoja Resumen de aptitudes I?

| Columna | Descripción |
|---|---|
| Después | Representa el número de alumnos que obtuvieron una aptitud antes de un período definido (en días), más allá del cual la aptitud se considera obsoleta o debe actualizarse. Resulta útil para identificar a los alumnos con logros de aptitudes próximos o caducados.<br>Consulte <a href="https://experienceleague.adobe.com/es/docs/learning-manager/using/admin/skills-levels">niveles de aptitud</a> para obtener más información. |
| Nombre | El nombre completo del alumno al que se asigna la aptitud. |
| Nombre del responsable | El nombre del responsable de informes del alumno. |
| Etiquetas de fila | El nombre de aptitud específico asignado a los alumnos que aparecen en esta fila. Se utiliza como encabezado de agrupación para resumir los datos de aptitudes de los alumnos en cada categoría de aptitud. |
| Número de usuarios que deben tener esta aptitud | Número total de alumnos a los que se ha asignado la aptitud específica. |
| Número de usuarios que han conseguido esta aptitud | Número de alumnos que han completado correctamente los objetos de aprendizaje necesarios para obtener la aptitud. |
| Cantidad de alumnos que deben poner al día la aptitud | El número de alumnos cuyas fechas de logro de aptitudes superan el umbral de actualización definido. |
| Porcentaje de cumplimiento (según aptitud conseguida) | Tasa de cumplimiento o adopción de la aptitud. |


### ¿Qué contiene la hoja Resumen de aptitudes II?

| Columna | Descripción |
|---|---|
| Después | Número de aptitudes obtenidas por el alumno antes del umbral de actualización definido (en días). Esto identifica las aptitudes que pueden estar obsoletas y que es necesario actualizar. |
| Aptitud | Nombre de la aptitud o aptitudes asignadas a los alumnos. Este puede estar vinculado a uno o varios objetos de aprendizaje, como cursos, certificaciones o rutas de aprendizaje. |
| Nombre del responsable | El nombre del responsable directo del alumno. |
| Etiquetas de fila | El nombre completo del alumno. Para cada alumno, las aptitudes y el progreso se muestran en columnas posteriores. |
| El número de aptitudes que debe tener cada usuario. | Número total de aptitudes asignadas al alumno. |
| El número de aptitudes que tiene cada usuario. | Número total de aptitudes que el alumno ha alcanzado correctamente al completar los objetos de aprendizaje asociados. |
| El número de aptitudes que se deben actualizar. | El número de aptitudes obtenidas que han superado la duración de la actualización y que ahora requieren revalidación. Este valor ayuda a realizar un seguimiento de las necesidades de renovación de formación para el cumplimiento o el desarrollo continuo. |
| Porcentaje de cumplimiento | Indica el nivel de cumplimiento general del alumno en función del logro de aptitudes. |

## Historial de descargas de transcripciones de alumnos

El historial de descargas de transcripciones de alumnos permite a los administradores realizar un seguimiento de quién ha descargado las transcripciones de cada alumno y a qué usuarios han accedido. Esta función resulta especialmente útil en entornos centrados en la empresa y el cumplimiento normativo, en los que varios responsables de departamento pueden tener que ver los registros de aprendizaje.

Después de descargar una transcripción del alumno, la página Transcripciones de alumnos muestra todas las transcripciones generadas por cualquier persona en la plataforma.



La lista muestra los siguientes atributos:

* Desde y Hasta: Duración de las transcripciones que se van a descargar.
* Generado por: El correo electrónico del usuario que ha descargado el informe o ha solicitado la descarga.
* Alumnos: Los alumnos o grupos de alumnos cuyas transcripciones se van a descargar.
* Filtros aplicados: Los filtros que se aplicaron para el estado de inscripción.
* Datos adicionales incluidos: Los datos adicionales (alumnos eliminados, información del módulo, datos de aptitudes y hojas de resumen) que el administrador había solicitado en la opción Avanzadas en el modo Agregar transcripción de alumno.
* Estado: Descargado, En Cola o En curso.
* Cancelar: se cancela la generación del informe en cualquier momento.

## Consideraciones adicionales para transcripciones de alumnos

Las transcripciones de alumnos incluyen varios comportamientos que los administradores deben tener en cuenta:

**Ruta de aprendizaje y visualización del progreso del curso**

Todos los cursos que formen parte de una ruta de aprendizaje (LP) aparecerán en la transcripción del alumno, aunque este solo haya progresado en uno de los cursos. Esto garantiza la visibilidad completa de una ruta de aprendizaje, incluso si el progreso se ha completado parcialmente.

**Datos de alumnos eliminados**

Si se ha eliminado un alumno de la plataforma, su transcripción no mostrará sus registros en ningún informe generado para el grupo de usuarios del que formaba parte. Esto significa que los registros de los alumnos eliminados se excluirán de cualquier informe filtrado creado mediante filtros de grupos de usuarios.

Sin embargo, puede seguir descargando los datos de los alumnos eliminados. Si ha seleccionado la opción **[!UICONTROL Incluir alumnos eliminados]** al establecer los filtros para generar el informe, puede descargar el informe de los alumnos eliminados.



**Comportamiento de los administradores personalizados**

Los administradores personalizados con un ámbito definido (por ejemplo, limitado a catálogos o grupos de usuarios específicos) verán los datos de transcripción filtrados en función de su ámbito:

* Ámbito de grupo de usuarios: en el informe solo se incluirán los alumnos del grupo de usuarios del ámbito del administrador personalizado.
* Ámbito del catálogo: en el informe solo se incluirán los objetos de aprendizaje (cursos, certificaciones y rutas de aprendizaje) asignados a los catálogos del ámbito.
* Columnas filtradas: Las columnas permanecen igual. Solo se asignará un ámbito a las filas en función de los ámbitos de los catálogos y los grupos de usuarios.

Esto garantiza que los administradores personalizados del ámbito vean solo los datos y el contenido de aprendizaje del alumno para el que están autorizados a administrar.

**Compatibilidad con conectores**

Se puede acceder al informe de transcripciones de alumnos a través de la interfaz de usuario del administrador, [FTP, Box, API de trabajos o Power BI](/help/migrated/integration-admin/feature-summary/connectors.md). No se incluye en los informes unificados de Salesforce, Power BI y Marketo Engage.

Los informes unificados descargados de Salesforce, Marketo Engage y Power BI contienen menos columnas que las transcripciones de alumnos.






