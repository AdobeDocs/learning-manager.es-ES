---
description: Obtén eventos webhook en Adobe Learning Manager cuando los instructores editen los detalles de la sesión y mantén al día las notificaciones de los alumnos y los sistemas conectados.
jcr-language: en_us
title: Recibir eventos webhook para ediciones de sesión del instructor
exl-id: 6fa4b71b-a8f4-40a2-ab57-bb7f3016542c
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%
---

# Eventos de webhook para ediciones de instancias de objetos de aprendizaje por instructores

Adobe Learning Manager proporciona eventos webhook que notifican a los sistemas externos cuando se modifica una instancia de objeto de aprendizaje (LO), como una sesión de un curso dirigido por un instructor. Anteriormente, estos eventos se activaban solo cuando un administrador o un autor modificaban una instancia de objeto de aprendizaje. Los eventos de webhook ahora también se activan cuando un instructor edita los detalles de una sesión.

Puede utilizar estos eventos para mantener actualizados con los cambios del instructor los sistemas externos, como los servicios de correo electrónico, los calendarios, las herramientas de creación de informes o las plataformas de análisis. Por ejemplo, puede notificar a los alumnos cuando cambie la hora de una sesión.

Las ediciones del instructor utilizan el evento de modificación de instancia de objeto de aprendizaje existente, por lo que no se introduce ningún tipo de evento nuevo.

>[!NOTE]
>
>Las ediciones del instructor activan un webhook solo si un webhook activo se suscribe al evento de modificación de la instancia del objeto de aprendizaje. Aprenda a [crear y administrar webhooks como administrador de integración](/help/migrated/integration-admin/feature-summary/webhooks.md#create-manage-webhooks).

## Ediciones de instructor admitidas

El evento webhook se activa cuando un instructor edita cualquiera de los siguientes detalles de la sesión:

* Temporización de sesiones

* Créditos

* Zona horaria

* Lugar

* Límite de inscripción

* Límite de lista de espera

* Permitir envíos

## Estructura de carga útil Webhook

Cada solicitud webhook contiene la siguiente estructura de nivel superior:

```json
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

Se utiliza la misma estructura independientemente de quién modifique la instancia de objeto de aprendizaje. La carga no indica si un instructor, un administrador o un autor han realizado el cambio.

Cuando un instructor cambia los detalles de una sesión, como la zona horaria, el límite de inscripción o el límite de la lista de espera, el webhook envía este evento a la dirección URL del listener. Utilice el evento para recuperar los detalles de la sesión más reciente y notificar a los alumnos o actualizar los sistemas externos.

## Recuperar los detalles actualizados de la sesión

El evento webhook identifica la instancia de objeto de aprendizaje modificada. Para obtener los detalles de la sesión actualizada, llame a la API pública de Learning Manager (API de Captivate Prime) mediante `loId` desde el evento:

```http
GET /primeapi/v2/learningObjects/{loId}
```

Busque la instancia que coincide con `loInstanceId` en la respuesta y, a continuación, compárela con los datos almacenados en el sistema.

## Crear integraciones con eventos webhook

Puede utilizar estos eventos webhook para:

* Envía notificaciones a los alumnos a través de un correo electrónico externo o un servicio de mensajería cuando cambien los detalles de la sesión, como la fecha, la hora, la zona horaria o el lugar.

* Sincronizar los datos de sesión con calendarios externos, informes o sistemas de análisis.

* Realizar un seguimiento de los cambios de capacidad cuando se modifica el límite de inscripción o el límite de lista de espera de una sesión.

* Mantén registros de auditoría registrando `eventId`, `timestamp` y `eventInfo` junto con el objeto de aprendizaje y los identificadores de instancia.

Como mínimo, el controlador del webhook debe:

* Valide la carga útil y analice `events[]`.

* Utilice `eventName` para identificar el evento de modificación de la instancia del objeto de aprendizaje.

* Use `loId` y `loInstanceId` para localizar el registro correspondiente en el sistema y llame a la API pública para recuperar los detalles de la sesión actual.

* Use `eventId` para evitar el procesamiento duplicado si el mismo evento se entrega más de una vez.

El mismo evento se envía para que lo editen los instructores, administradores y autores, de modo que la integración pueda recibirlo más a menudo que antes. Compare los detalles de la sesión recuperada con los datos de su sistema antes de enviar una notificación. A continuación, se notifica a los alumnos solo cuando cambian los detalles relevantes.
