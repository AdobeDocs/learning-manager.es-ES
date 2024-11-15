---
jcr-language: en_us
title: Guía de uso de webhooks
description: Más información sobre el uso de Webhooks, las prácticas recomendadas y las limitaciones
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4b26eddf1285651a13ee9c71fdf677e8b92e6dc3
workflow-type: tm+mt
source-wordcount: '3369'
ht-degree: 1%

---

# Guía de uso de webhooks

Los webhooks son una forma de que las aplicaciones web se comuniquen entre sí automáticamente y en tiempo real.

A diferencia de las API tradicionales, que esperan a que un usuario solicite información, las API en tiempo real comparten datos en el momento en que sucede. Los webhooks actúan como una API en tiempo real y ayudan a compartir los datos inmediatamente cada vez que se produce el evento especificado.

## Entidades

Para entender los eventos de webhooks, primero tenemos que ser conscientes de las entidades involucradas y las condiciones desencadenantes de estos eventos.

### Objetos de aprendizaje

A continuación se indican los eventos admitidos para los objetos de aprendizaje (curso, ruta de aprendizaje o certificaciones).

#### Borrador

Cada vez que se crea un objeto de aprendizaje desde la interfaz de usuario, se inicia en modo **Borrador**. Esto significa que el objeto de aprendizaje aún no se ha publicado y no está disponible para los alumnos. El evento **LEARNING_OBJECT_DRAFT** se desencadena mientras el objeto de aprendizaje siga siendo un borrador. Cualquier actualización sucesiva del borrador también activará este evento.

#### Actualización

Una vez publicado el objeto de aprendizaje, su estado cambia de **Draft** a **Published**. Durante esta transición, Webhook genera el evento **LEARNING_OBJECT_MODIFICATION** porque el objeto de aprendizaje se está modificando de **Borrador** a **Publicado**. Todas las modificaciones y actualizaciones posteriores del objeto de aprendizaje también desencadenarán un evento **LEARNING_OBJECT_MODIFICATION**.

El evento **LEARNING_OBJECT_MODIFICATION** también se activa cuando se retira el objeto de aprendizaje. Esta operación retirada marca las instancias subyacentes como actualizadas, ya que estas instancias se retiran una vez que el objeto de aprendizaje principal está en estado retirado.

#### Eliminar

Al eliminar un objeto de aprendizaje, se genera el evento **LEARNING_OBJECT_DELETION**. Este evento indica que el objeto de aprendizaje se ha eliminado y ya no está disponible para que los alumnos accedan a él.

Además de los eventos en tiempo real, los eventos de objetos de aprendizaje también tienen un homólogo de lote (no en tiempo real), que se activa como parte del evento **LEARNING_OBJECT_MODIFICATION_BATCH**. Este evento se produce durante la creación o modificación de un objeto de aprendizaje a través del flujo de trabajo de migración. Dado que las operaciones de borrado y eliminación de objetos de aprendizaje no se admiten mediante la migración, no hay eventos de borrado o eliminación correspondientes para estas acciones.

### Instancias de objetos de aprendizaje

A continuación se indican los eventos admitidos para las instancias de objetos de aprendizaje.

#### Actualización

Una vez creada una instancia, se genera el evento **LEARNING_OBJECT_INSTANCE_MODIFICATION**. Las instancias de objetos de aprendizaje en Adobe Learning Manager no tienen un estado **Borrador**; por lo tanto, Adobe Learning Manager no admite un evento **LEARNING_OBJECT_INSTANCE_DRAFT**. Este evento se genera siempre que se crea, modifica o retira una instancia.

Además de generarse cuando se crea, actualiza o retira una instancia, este evento también se genera automáticamente cuando su objeto de aprendizaje principal se marca como **Retirado**. Esto se debe a que, cuando se retira un objeto de aprendizaje, las instancias subyacentes también deben marcarse como **Retirado**.

#### Eliminar

Cuando se elimina una instancia, se genera el evento **LEARNING_OBJECT_INSTANCE_DELETION**. Este evento solo se aplica a instancias de curso que contienen módulos con ritmo personalizado, ya que Adobe Learning Manager solo permite a los administradores eliminar instancias de curso en las que el tipo de módulo tiene ritmo personalizado. Adobe Learning Manager no admite eliminaciones explícitas para otros tipos de módulos de curso que no sean instancias de ruta de aprendizaje o instancias de certificación.

La instancia del objeto de aprendizaje también tiene una contraparte en tiempo no real, expuesta como parte del evento **LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH**. Este evento se activa durante la creación o modificación de una instancia de objeto de aprendizaje a través del flujo de trabajo de migración. Como las operaciones de borrador o eliminación para instancias de objetos de aprendizaje no se admiten en la migración, los eventos de borrador o eliminación correspondientes no están disponibles.

### Inscripción

Una vez que un alumno realiza una acción de inscripción, se activa un evento de inscripción en tiempo real. Según el tipo de objeto de aprendizaje, el evento de inscripción en tiempo real puede pertenecer a una de las siguientes categorías:

* COURSE_ENROLLMENT
* LEARNING_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Los eventos de inscripción tienen homólogos por lotes además de estos eventos en tiempo real. Cada vez que un administrador, un responsable o una plataforma activa una inscripción, se activan eventos de inscripción en tiempo no real. Según el tipo de objeto de aprendizaje, el evento de inscripción por lotes puede ser uno de los siguientes:

* COURSE_ENROLLMENT_BATCH
* LEARNING_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Darse de baja

Cuando un alumno realiza una acción de darse de baja, se activa un evento de darse de baja en tiempo real. Según el tipo de objeto de aprendizaje, el evento de anulación de la inscripción en tiempo real puede clasificarse en una de las siguientes categorías:

* COURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

Además de estos eventos, también hay eventos de desinscripción por lotes. Siempre que un administrador, un responsable o una plataforma marcan una cancelación de la inscripción, se activan eventos de cancelación de la inscripción en tiempo no real. Según el tipo de objeto de aprendizaje, el evento de anulación de la inscripción por lotes puede ser uno de los siguientes:

* COURSE_UNENROLLMENT_BATCH
* LEARNING_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Finalización

El evento de finalización en tiempo real se activa cada vez que un alumno completa un objeto de aprendizaje. En función del tipo de objeto de aprendizaje, el evento de finalización en tiempo real puede pertenecer a una de las siguientes categorías:

* COURSE_COMPLETED
* LEARNING_PATH_COMPLETED
* CERTIFICATION_COMPLETED

Además de estos eventos en tiempo real, también hay eventos de finalización por lotes. Por ejemplo, cuando un administrador, un responsable o una plataforma marcan un objeto de aprendizaje como completado, se activan los eventos de finalización en tiempo no real. En función del tipo de objeto de aprendizaje, el evento de finalización de lote puede pertenecer a una de las siguientes categorías:

* COURSE_COMPLETED_BATCH
* LEARNING_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Progreso del alumno

Siempre que un alumno se inscribe en un objeto de aprendizaje e inicia el módulo, se realiza un seguimiento de su progreso. Estos datos se incluyen en el evento **LEARNER_PROGRESS**. El evento puede retrasarse hasta 15 minutos, ya que el seguimiento del progreso se basa en una lógica de agregación compleja, que no es en tiempo real.

### Estadísticas de CI

El evento en tiempo real **CI_STATS** se activa siempre que haya un cambio en la disponibilidad de la licencia o lista de espera de una instancia de curso. Estos datos se capturan solo en el nivel de instancia. Además, este evento se activa para los cursos y no para otras rutas de aprendizaje o certificaciones, ya que la disponibilidad de puestos y listas de espera son atributos específicos de un curso y su instancia.

## Ordenación de eventos

Adobe Learning Manager garantiza que los eventos se ordenen para cada cuenta. Sin embargo, puede haber discrepancias al correlacionar los mensajes entre los eventos de inscripción o finalización y los eventos de progreso. Esto se produce porque el evento de progreso del alumno se puede retrasar hasta 15 minutos, ya que el seguimiento del progreso se basa en una lógica de agregación compleja, que no es en tiempo real. Además, los eventos de progreso proceden de diferentes orígenes de datos, por lo que no se puede garantizar su orden en relación con los eventos de inscripción y finalización. Por lo tanto, Adobe Learning Manager proporciona las prácticas recomendadas para los clientes cuando escuchan estos eventos.

Si el evento de finalización se produce antes del evento de progreso del alumno, el cliente puede omitir el evento de progreso del alumno. Esto se debe a que el evento de progreso del alumno se puede retrasar hasta 15 minutos, mientras que el evento de finalización se puede activar antes de que se reciba el evento de progreso. Dado que la recepción de un evento de finalización indica que el objeto de aprendizaje ha finalizado, implica que el progreso ha alcanzado el 100 %.

En el caso poco frecuente de que el evento de inscripción se produzca después del evento de progreso del alumno, el cliente puede omitir el evento de inscripción. Esto se debe a que solo se puede realizar un seguimiento del progreso después de que el alumno se haya inscrito en el objeto de aprendizaje. En otras palabras, recibir un evento de progreso indica que el objeto de aprendizaje se ha iniciado, lo que solo ocurre después de una inscripción correcta.

## Eventos en tiempo real frente a eventos por lotes

Algunos eventos tienen homólogos en tiempo real y no en tiempo real, como se ha mencionado anteriormente. Puede haber preguntas sobre cuándo suscribirse a eventos en tiempo real y cuándo suscribirse a eventos no en tiempo real. Las siguientes son directrices que pueden seguirse en función de las entidades descritas anteriormente.

### Eventos en tiempo real

| S.No | Eventos de webhook | Descripción |
|---|---|---|
| 1 | CI_STATS | Se activa cuando hay un cambio en la disponibilidad de la licencia o lista de espera de una instancia de curso. |
| 2 | COURSE_ENROLLMENT | Se activa cuando un alumno se inscribe en un curso. |
| 3 | COURSE_COMPLETED | Se activa cuando un alumno finaliza un curso. |
| 4 | LEARNING_PATH_ENROLLMENT | Se activa cuando un alumno se inscribe en una ruta de aprendizaje. |
| 5 | LEARNING_PATH_COMPLETED | Se activa cuando un alumno completa una ruta de aprendizaje. |
| 6 | CERTIFICATION_ENROLLMENT | Se activa cuando un alumno se inscribe en una certificación. |
| 7 | CERTIFICATION_COMPLETED | Se activa cuando un alumno completa una certificación. |
| 8 | COURSE_UNENROLLMENT | Se activa cuando un alumno se da de baja de un curso. |
| 9 | LEARNING_PATH_UNENROLLMENT | Se activa cuando un alumno se da de baja de una ruta de aprendizaje. |
| 10 | CERTIFICATION_UNENROLLMENT | Se activa cuando un alumno se da de baja de una certificación. |
| 11 | LEARNING_OBJECT_DRAFT | Se activa durante la creación de un objeto de aprendizaje en estado de borrador. |
| 12 | LEARNING_OBJECT_DELETION | Se activa al eliminar un objeto de aprendizaje. |
| 13 | LEARNING_OBJECT_MODIFICATION | Se activa durante la modificación de un objeto de aprendizaje. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Se activa durante la creación o modificación de una instancia de objeto de aprendizaje.<div><b>Nota:</b> Se recomienda utilizar instancias de curso solo después de publicar el curso.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Se activa durante la eliminación de una instancia de objeto de aprendizaje. |

### Eventos en tiempo no real

| S.No | Eventos de webhook | Descripción |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma inscribe alumnos en un curso. |
| 2 | COURSE_COMPLETED_BATCH | Se activa cuando un administrador, responsable o plataforma marca un curso como completado. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma inscribe alumnos en una ruta de aprendizaje. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Se activa cuando un administrador o responsable marca una ruta de aprendizaje como completada. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma inscribe alumnos en una certificación. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Se activa cuando un administrador, administrador o plataforma marca una certificación como completada. |
| 7 | LEARNER_PROGRESS | Realiza un seguimiento del progreso de un alumno cuando se completa un módulo. |
| 8 | COURSE_UNENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma da de baja a los alumnos de un curso. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma da de baja a los alumnos de una ruta de aprendizaje. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Se activa cuando un administrador, responsable o plataforma da de baja a los alumnos de una certificación. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Se activa durante la modificación de un objeto de aprendizaje mediante el flujo de trabajo de migración. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Se activa durante la creación o modificación de una instancia de objeto de aprendizaje mediante el flujo de trabajo de migración. |

### Objetos de aprendizaje y sus instancias

* Suscríbase a eventos en tiempo real siempre que desee escuchar los cambios en los objetos de aprendizaje realizados mediante acciones de interfaz de usuario mediante funciones como administrador, autor, etc.
* Suscríbase a eventos en tiempo no real o por lotes siempre que desee escuchar los cambios en los objetos de aprendizaje realizados a través de los flujos de trabajo de migración.

### Inscripción, cancelación de la inscripción y finalización

* Suscríbase a eventos en tiempo real siempre que desee recibir inscripciones, cancelaciones de inscripciones o finalizaciones realizadas por alumnos.
* Suscríbase a eventos en tiempo no real o por lotes siempre que desee recibir inscripciones, cancelaciones de inscripciones o finalizaciones marcadas por el administrador, el responsable, la plataforma, etc.

### Progreso del alumno

* Suscríbase al evento siempre que desee escuchar los cambios de progreso de un alumno.

>[!NOTE]
>
>En los escenarios anteriores (inscripción, anulación de inscripción, finalización y progreso), los compuestos de atributos que constan de userId y loInstanceId pueden identificar un registro de forma exclusiva.

### Estadísticas de instancia del curso

* Suscríbase al evento **CI_STATS** en tiempo real siempre que desee escuchar los cambios en la disponibilidad de la licencia o la lista de espera.

## Carga del evento Webhook

Como parte de la carga útil de respuesta Webhooks, Adobe Learning Manager emitirá los atributos necesarios para identificar de forma exclusiva una entidad. Estos se emitirán en el mismo formato y de acuerdo con los estándares utilizados por la API pública, lo que garantiza que los datos de webhook estén sincronizados con los datos de la API pública. Vea [Ejemplos de cargas](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) para ver las cargas de los distintos eventos.

## Uso de webhooks para crear una base de datos externa o un servicio de notificación

Uno de los casos de uso que hemos escuchado donde Webhooks podría ser útil es para construir una base de datos del lado del cliente. Adobe Learning Manager tiene su propia base de datos y esquema, pero los clientes no tienen acceso a ellos.

La pregunta es: ¿cómo pueden los clientes crear una base de datos utilizando eventos de webhooks?

Como Adobe Learning Manager no expone directamente los registros de tabla y el esquema, los clientes pueden confiar en la solución Webhooks para crear una base de datos externa consumiendo los eventos para rellenarla. En esta versión, proporcionamos eventos para objetos de aprendizaje, instancias de objetos de aprendizaje, inscripción, cancelación de inscripción, finalización, progreso y estadísticas de instancias de cursos.

### Creación de una base de datos a partir de eventos de objetos de aprendizaje

Los eventos del objeto de aprendizaje exponen `loId` y `loType` para identificar una entidad. Sin embargo, estos atributos por sí solos no son suficientes para crear una base de datos de objetos de aprendizaje externa. Los clientes necesitarán campos adicionales para describir con más detalle el objeto de aprendizaje.
Existen dos métodos para obtener los datos adicionales:

#### Generar un informe de datos de formación para obtener todos los datos

Este enfoque debe utilizarse cuando los objetos de aprendizaje se crean en bloque mediante flujos de trabajo como la migración. El objetivo aquí es generar el informe **[!UICONTROL Training Data]** con todos los objetos de aprendizaje ingestados como parte del flujo de trabajo de migración. Para optimizar el proceso de importación, se recomienda establecer la hora de inicio de la exportación en el momento en que se activó la migración. De este modo, se garantiza que solo se exporten en el informe los objetos de aprendizaje incorporados mediante la migración, ya que los datos históricos ya estarán disponibles en la base de datos del cliente.

#### Consulte la información de la API pública /learningObjects: ámbito de administración.

Este enfoque debe utilizarse cuando se crean objetos de aprendizaje mediante flujos de trabajo en tiempo real. El cliente debe tener su propia capa de almacenamiento en caché para agrupar los objetos de aprendizaje emitidos a través de los eventos y, a continuación, consultar la API `GET /learningObjects` pasando estos ID de objeto de aprendizaje. El motivo de tener una capa de almacenamiento en caché es garantizar que no se superen los límites de velocidad de la API pública. Actualmente, tenemos límites de velocidad de administración establecidos en 500 solicitudes por hora para ` GET /learningObject` API. Si se excede este límite, el servicio de API pública responderá con un mensaje **HTTP 429 Too Many Requests**.

### Creación de bases de datos a partir de instancias de objetos de aprendizaje y eventos CI_STATS

El evento Instance del objeto de aprendizaje emite los atributos `loInstanceId`, `loId` y `loType` para los cursos y las rutas de aprendizaje. Del mismo modo, el evento **CI_STATS** solo se aplica a los cursos, ya que `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability`, etc., solo se aplican a los cursos.

En determinados casos de uso, se requieren datos de instancia adicionales, como el nombre de la instancia, el estado, etc. Para obtener datos de instancia adicionales, se debe seguir el siguiente enfoque:

#### Consulte la información de los objetos de aprendizaje/GET de la API pública: ámbito de administración

Los clientes pueden utilizar la API `GET /learningObjects` como se ha mencionado anteriormente, junto con instancias incluidas para obtener la información sobre las instancias. Deben seguir el enfoque mencionado en la [sección](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) para garantizar que no se incumplan los límites de tasas.


>[!NOTE]
>
>1. Las certificaciones no tienen el concepto de instancias en ALM.
>2. No es necesario obtener datos adicionales para CI_STATS, ya que la misma información ya se habría obtenido como parte de los eventos de instancia del objeto de aprendizaje.

### Creación de una base de datos a partir de eventos de inscripción, desinscripción, finalización y progreso

La inscripción de alumnos, la darse de baja, la finalización y el progreso se emiten como eventos independientes en Adobe Learning Manager. El alumno se identifica mediante el atributo `userId`. Sin embargo, puede haber ciertos casos en los que se requiera información adicional del alumno, como el nombre, el correo electrónico, etc., para los flujos de trabajo descendentes en el lado del cliente. Para obtener estos datos, los clientes pueden seguir el enfoque que se describe a continuación:

#### Exportar el informe de usuarios desde administradores o conectores

Este enfoque debe seguirse siempre que se utilicen flujos de trabajo masivos, como la inscripción masiva, la cancelación masiva de la inscripción, etc. El informe de usuarios de Adobe Learning Manager contiene toda la información relativa a un usuario. Al correlacionar el `userId` obtenido del evento webhook, los clientes pueden consultar este informe (que puede exponerse en el lado del cliente como una base de datos, caché o extremo de API) para obtener detalles adicionales como el nombre, el correo electrónico, el UUID, etc. Este enfoque se puede utilizar para sincronizar usuarios de forma semanal o diaria.

#### Consultar información de usuarios/GET de API públicas: ámbito de administración

Este enfoque se puede seguir cuando los usuarios no están disponibles en el informe anterior. La combinación de los enfoques 1 y 2 garantiza que todos los usuarios existentes que se crearon en el pasado puedan incluirse en el **[!UICONTROL Informe de usuarios]**, mientras que los usuarios recién creados aún se pueden obtener desde la API. Si el **[!UICONTROL Informe de usuario]** no tiene los datos, el cliente puede enviar los ID de usuario como argumentos de entrada a la API `GET /users` para obtener información del usuario. Esta información debe almacenarse en caché en el lado del cliente para evitar invocaciones repetidas de la API pública para el mismo conjunto de usuarios. Tenga en cuenta que actualmente los límites de las tasas de administración están establecidos en 500 solicitudes por hora para las API de GET/usuarios. Cualquier solicitud que supere este límite dará como resultado una respuesta de **HTTP 429 Demasiadas solicitudes**.

## Tolerancia a fallos

La tolerancia a errores del sistema webhook de ALM proporciona recomendaciones para que los suscriptores gestionen posibles problemas, como la pérdida de eventos, los eventos duplicados y la entrega fuera de orden.

ALM tiene un tiempo de espera de conexión configurado de 10 segundos y un tiempo de espera de socket configurado de 5 segundos. Se espera que el cliente reconozca el mensaje en cuanto lo reciba. Esto garantiza que el cliente no se retrase al procesar los mensajes. En caso de que se produzca algún procesamiento posterior que requiera mucho tiempo, el cliente debe seguir reconociendo el evento al instante y, a continuación, gestionar el procesamiento posterior al final.

### Retención de datos

Los eventos se mantienen durante 7 días. Si no se procesan en este plazo, se pierden de forma permanente. Si la recuperación se produce el último día y se necesita más tiempo, el sistema no ampliará el período de retención.
Si los eventos se producen más rápido de lo que se consumen, algunos eventos pueden perderse. Aunque esto es poco común, los suscriptores deben supervisar para evitar que se convierta en un problema a largo plazo.

### Desactivación de webhooks

Cuando un suscriptor no responde a los eventos de webhook, el sistema ALM reintenta los webhooks utilizando una desconexión exponencial para evitar saturar al suscriptor.

El proceso de reintento comienza con un intervalo inicial de 5 segundos. Si el suscriptor no responde, el tiempo de espera se duplica a 10, 20, 40 y 80 segundos, y finalmente aumenta a un máximo de 5 minutos. Una vez que llega a los 5 minutos, el sistema continuará reintentando cada 5 minutos hasta que termine el período de retención de 7 días. Si el suscriptor sigue sin responder durante todo este período, el webhook se deshabilitará automáticamente. Se enviará un correo electrónico de recordatorio al suscriptor a intervalos regulares.

### Duplicar eventos

Si un suscriptor tarda más de 5 segundos en responder después de procesar un evento, el sistema podría intentar procesar el mismo evento de nuevo. Se recomienda utilizar los ID de evento para realizar un seguimiento de los eventos que ya se han procesado. Además, si el webhook se bloquea después de enviar el evento pero antes de guardar que se ha procesado, puede que se vuelva a intentar el mismo grupo de eventos. Se recomienda utilizar ID de lote o ID de evento individuales para reconocer e ignorar cualquier duplicado.

### Recomendación de tolerancia a fallos

Para evitar estos errores, los suscriptores deben supervisar activamente los eventos de webhook y configurar alertas para problemas como eventos perdidos, entregas duplicadas o secuencias fuera de orden.

## Directrices específicas para eventos webhook

1. Si obtiene primero un evento LEARNER_PROGRESS, omita los eventos que se enumeran a continuación:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Omita el evento LEARNER_PROGRESS si se produce después de los eventos siguientes:

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Utilice el campo de marca de tiempo para determinar si se debe ignorar o procesar el evento, excepto para el evento LEARNER_PROGRESS.

## Prácticas recomendadas para el consumo de Webhooks Events

* La solución webhook se utiliza para gestionar sistemas de alto rendimiento en los que la velocidad y la baja latencia son esenciales. Por lo tanto, el cliente debe asegurarse de que el evento sea reconocido tan pronto como sea recibido. Incluso si se necesita un procesamiento adicional por parte del cliente (como obtener datos de informes, API o realizar otras acciones), el acuse de recibo debe enviarse en cuanto se reciba el evento y corresponde al cliente procesar el evento más adelante.
* Si no se reconoce el hecho lo antes posible, podría repercutir en la naturaleza en tiempo real de los hechos, ya que los hechos posteriores sólo se emitirán una vez que se reciba el reconocimiento anterior.
* Los clientes pueden responder con un código de estado HTTP 202 Aceptado para confirmar que el evento se ha aceptado.

## limitaciones

* Las ayudas de trabajo no se tienen en cuenta para los eventos de Webhook en la categoría de objetos de aprendizaje, ya que se suelen utilizar para ayudar a los alumnos a completar otros objetos de aprendizaje.
* La retirada de una instancia de objeto de aprendizaje se consideraría un evento de actualización. No habría un evento de eliminación para una instancia, ya que solo se puede retirar, no eliminar.
* Los cambios de sesión se capturarían como parte del evento de actualización de la instancia. Esto solo se aplica a los cursos. No habrá propagación hacia arriba desde entidades de nivel inferior para instancias de ruta de aprendizaje o instancias de certificación.
* Si una ruta de aprendizaje contiene un curso y un alumno lo completa a través de la ruta de aprendizaje, se generarán dos eventos **LearnerProgress**: uno para el curso y otro para la ruta de aprendizaje.
* Algunos flujos de trabajo calculan atributos de objetos de aprendizaje, como la duración y el tipo de entrega, de forma asincrónica. Por lo tanto, los eventos para estos objetos de aprendizaje se generarán una vez que el trabajo cron finalice el procesamiento.
* Si un curso se inscribe a través de un programa de aprendizaje o certificación principal, los eventos de inscripción, cancelación de inscripción y finalización solo se activarán para el programa de aprendizaje o la certificación principal. Estos eventos no se activarán para el curso secundario, ya que la inscripción se produjo indirectamente.
* Los webhooks solo se admiten para cuentas con el estado **[!UICONTROL ACTIVO]**. No están disponibles para las cuentas **[!UICONTROL TRIAL]** o **[!UICONTROL INACTIVE]**.

## Ejemplos de cargas para los eventos

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
    ]
}
```

+++

+++RUTA_DE_APRENDIZAJE_INSCRIPCIÓN

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++RUTA_DE_APRENDIZAJE_LOTE_DE_INSCRIPCIÓN

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++RUTA_DE_APRENDIZAJE_COMPLETADA

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++RUTA_DE_APRENDIZAJE_COMPLETADA_LOTE

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++PROGRESO_DEL_ALUMNO

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++RUTA_DE_APRENDIZAJE_DARSE DE BAJA

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
      }
    }
]
}
```

+++

+++RUTA_DE_APRENDIZAJE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++ELIMINACIÓN_OBJETO_APRENDIZAJE

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++MODIFICACIÓN_OBJETO_DE_APRENDIZAJE

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++
