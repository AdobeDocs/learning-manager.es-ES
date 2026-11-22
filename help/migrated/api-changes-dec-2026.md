---
description: Aprenda a utilizar la configuración de suscripción del tablero y las API de suscriptores para configurar los mensajes de correo electrónico de resumen y administrar suscriptores del tablero
jcr-language: en_us
title: Cambios en la API en noviembre de 2026
exl-id: 9b2d3856-810c-4352-bf18-667f698d4d70
source-git-commit: 4234f3cc3b9d77a7f9d197d2df2160ec62edd6d6
workflow-type: tm+mt
source-wordcount: '5724'
ht-degree: 4%
---

# Cambios en la API en diciembre de 2026

## API para notificaciones del instructor del foro de debate {#api-discussion-board-instructors}

En este artículo se describen las nuevas API compatibles con las notificaciones del instructor del foro de debate. Utilícelos para suscribir instructores y responsables de cohorte a paneles de debate y para controlar qué actividad aparece en los mensajes de correo electrónico de resumen.

### Secuencia de API {#api-sequence}

Las API se dividen en dos grupos. La API `boardSubscriptionSettings` funciona en el nivel de cuenta. La API de suscriptores funciona a nivel de tablero. Utilice las API en esta secuencia:

| Paso | API | Propósito | Ámbito |
|---|---|---|---|
| 1 | [`POST /boardSubscriptionSettings`](#api-create-settings) | Establezca la configuración de nivel de cuenta. | `admin:write` |
| 2 | [`PATCH /boardSubscriptionSettings`](#api-update-settings) | Actualice la configuración de nivel de cuenta. | `admin:write` |
| 3 | [`GET /boardSubscriptionSettings`](#api-get-settings) | Recupere la configuración de nivel de cuenta. | `admin:read` |
| 4 | [`GET /boards/{id}/subscribers`](#api-get-subscribers) | Obtener la lista de usuarios suscritos a un tablero. | `admin:read` |
| 5 | [`POST /boards/{id}/subscribers`](#api-subscribe-users) | Suscribir usuarios a un tablero. | `admin:write` |
| 6 | [`DELETE /boards/{id}/subscribers/{userId}`](#api-unsubscribe-user) | Cancelar la suscripción de un usuario a un tablero. | `admin:write` |

### Autenticación y permisos

Cualquiera que se autentique con OAuth y tenga los ámbitos `admin:read` y `admin:write` puede llamar a estas API. Las API utilizan los siguientes ámbitos de OAuth:

* `admin:read`: Enumerar suscriptores y leer la configuración de notificaciones (`GET` solicitudes).
* `admin:write`: Cree o cambie la configuración de notificaciones y agregue o quite suscriptores (`POST`, `PATCH` y `DELETE` solicitudes).

>[!NOTE]
>
>El acceso al tablero se vuelve a comprobar cuando se envía una notificación. Si un suscriptor pierde el acceso a un tablero, se omite la entrega para ese tablero, pero se mantiene la suscripción. La entrega se reanuda si vuelve el acceso.

### Límites y consideraciones

* El número de suscriptores que se pueden añadir está limitado.
* El resumen se envía como un único correo electrónico sin paginación y el cuerpo del mensaje tiene un límite de tamaño. En el caso de los tableros con mucha actividad, elige una frecuencia de resumen que permita gestionar cada correo electrónico, como cada 6 horas.
* Los vínculos de resumen solo abren la publicación, el comentario o la respuesta para los usuarios que han iniciado sesión.

## API para crear configuraciones de nivel de cuenta {#api-create-settings}

### Propósito de la API {#purpose-create-settings}

Utilice esta API para establecer la configuración de nivel de cuenta para las notificaciones de suscripción de tablero por primera vez. La configuración controla cómo se generan los resúmenes de notificación en toda la cuenta:

* Qué eventos del panel de discusión generan notificaciones.
* Frecuencia con la que se envían los mensajes de resumen.
* Si se incluyen las publicaciones, los comentarios, las respuestas y los votos.

Para cambiar la configuración posteriormente, use [`PATCH /boardSubscriptionSettings`](#api-update-settings).

### Punto final {#endpoint-create-settings}

```http
POST /primeapi/v2/boardSubscriptionSettings
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:write` |
| Formato de solicitud | `application/vnd.api+json;charset=UTF-8` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Cuerpo de la solicitud {#request-body-create-settings}

Enviar la configuración como atributos de un recurso `boardSubscriptionSettings`.

| Campo | Tipo | Descripción |
|---|---|---|
| `notifyNewPost` | booleano | Si se notifica a los suscriptores cuando se agrega una nueva publicación a un tablero. |
| `notifyComment` | booleano | Si se notifica a los suscriptores cuando se agrega un comentario a una publicación. |
| `notifyReply` | booleano | Si se notifica a los suscriptores cuando se agrega una respuesta a un comentario. |
| `digestFrequencyHours` | entero | Con qué frecuencia, en horas, se envía el correo electrónico de resumen. Los valores válidos están comprendidos entre 1 y 168 (una semana). Por ejemplo, 24 envía un resumen diario y 168 envía un resumen semanal. |

### Ejemplo de solicitud {#example-request-create-settings}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyNewPost": true,
      "notifyComment": true,
      "notifyReply": true,
      "digestFrequencyHours": 24
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Ejemplo de respuesta - 201 Creado {#example-response-create-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Códigos de respuesta {#response-codes-create-settings}

| Estado | Significado |
|---|---|
| 201 | La solicitud se realizó correctamente. Se creó la configuración de nivel de cuenta. |
| 400 | Error de solicitud erróneo genérico. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |

## API para actualizar la configuración de nivel de cuenta {#api-update-settings}

### Propósito de la API {#purpose-update-settings}

Use esta API para actualizar la configuración de nivel de cuenta que creó con [`POST /boardSubscriptionSettings`](#api-create-settings). Por ejemplo, cambie la frecuencia de resumen o active o desactive un tipo de evento.

### Punto final {#endpoint-update-settings}

```http
PATCH /primeapi/v2/boardSubscriptionSettings
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:write` |
| Formato de solicitud | `application/vnd.api+json;charset=UTF-8` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Cuerpo de la solicitud {#request-body-update-settings}

Envíe los atributos que desee cambiar, en el mismo formato que la API de creación: `notifyNewPost`, `notifyComment`, `notifyReply` y `digestFrequencyHours`. Los atributos que no se envían mantienen sus valores actuales. Para obtener la descripción de cada atributo, consulte [API para crear la configuración de nivel de cuenta](#api-create-settings).

### Ejemplo de solicitud {#example-request-update-settings}

```bash
curl -X PATCH \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyReply": true,
      "digestFrequencyHours": 12
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Ejemplo de respuesta - 200 OK {#example-response-update-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 12,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Códigos de respuesta {#response-codes-update-settings}

| Estado | Significado |
|---|---|
| 200 | La solicitud se realizó correctamente. Se actualizó la configuración de nivel de cuenta y la respuesta contiene la configuración actual. |
| 400 | Error de solicitud erróneo genérico. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |

## API para recuperar la configuración de nivel de cuenta {#api-get-settings}

### Propósito de la API {#purpose-get-settings}

Cuando los usuarios se suscriben a un tablero, Adobe Learning Manager puede notificarles sobre la actividad en ese tablero mediante mensajes de correo electrónico de resumen. La configuración de nivel de cuenta determina qué tipos de actividad activan una notificación y con qué frecuencia se envía el resumen.

Esta API le permite recuperar dicha configuración. Utilícelo para mostrar la configuración de notificación actual en la aplicación o para comprobar la configuración antes de generar características que dependan de ella.

### Punto final {#endpoint-get-settings}

```http
GET /primeapi/v2/boardSubscriptionSettings
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:read` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Ejemplo de solicitud {#example-request-get-settings}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Ejemplo de respuesta - 200 OK {#example-response-get-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Esquema de recursos {#resource-schema-get-settings}

**`boardSubscriptionSettings`atributos**

| Campo | Tipo | Descripción |
|---|---|---|
| `notifyNewPost` | booleano | Si se notifica a los suscriptores cuando se agrega una nueva publicación a un tablero. |
| `notifyComment` | booleano | Si se notifica a los suscriptores cuando se agrega un comentario a una publicación. |
| `notifyReply` | booleano | Si se notifica a los suscriptores cuando se agrega una respuesta a un comentario. |
| `digestFrequencyHours` | entero | Con qué frecuencia, en horas, se envía el correo electrónico de resumen. Los valores válidos están comprendidos entre 1 y 168 (una semana). Utilice este valor para indicar a los usuarios la frecuencia con la que deben recibir el correo electrónico de resumen. Por ejemplo, mostrar &quot;Daily&quot; cuando el valor es 24 y &quot;Weekly&quot; cuando el valor es 168. |

### Códigos de respuesta {#response-codes-get-settings}

| Estado | Significado |
|---|---|
| 200 | La solicitud se realizó correctamente. La respuesta contiene la configuración de suscripción de tablero a nivel de cuenta. |
| 400 | Error de solicitud erróneo genérico. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |

### Utilice esta API en su integración {#integration-get-settings}

Un caso de uso común es una pantalla de preferencias de notificación que muestra cómo se configuran los correos electrónicos de suscripción al tablero para la cuenta.

1. Cuando se cargue la pantalla de preferencias de notificación de la aplicación, llame a `GET /boardSubscriptionSettings`.
1. Muestra qué tipos de actividad activan una notificación y con qué frecuencia se envía el correo electrónico de resumen, utilizando los valores de la respuesta.

## API para recuperar suscriptores del tablero {#api-get-subscribers}

### Propósito de la API {#purpose-get-subscribers}

Recuperar la lista de usuarios que están suscritos a un tablero específico. A los usuarios que estén suscritos a un tablero se les notificará la nueva actividad en él. Esta API devuelve los usuarios que están actualmente suscritos a un tablero determinado, junto con detalles sobre cuándo y por quién se creó cada suscripción.

Utilice esta API para mostrar una lista de suscriptores en la aplicación, para auditar quién recibe las actualizaciones de una tarjeta o para sincronizar los datos de suscripción de la tarjeta con un sistema externo.

La respuesta está paginada. Use los parámetros de consulta `page[offset]` y `page[limit]` para desplazarse por las listas de suscriptores grandes. Los datos devueltos están sujetos a los permisos del usuario que realiza la llamada en el tablero solicitado.

### Punto final {#endpoint-get-subscribers}

```http
GET /primeapi/v2/boards/{id}/subscribers
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:read` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Parámetros {#parameters-get-subscribers}

| Parámetro | En | Obligatorio | Predeterminado | Descripción |
|---|---|---|---|---|
| `id` | path | Sí | N/D | El ID del tablero cuyos suscriptores desea recuperar. El acceso está sujeto a los permisos del autor de la llamada en el tablero. |
| `page[offset]` | consulta | No | 0 | Posición inicial de los registros que se van a devolver. |
| `page[limit]` | consulta | No | 10 | Número de suscriptores que se van a devolver por página. El valor máximo permitido es 200. |

### Ejemplo de solicitud {#example-request-get-subscribers}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers?page[offset]=0&page[limit]=50'
```

### Ejemplo de respuesta - 200 OK {#example-response-get-subscribers}

```json
{
  "data": [
    {
      "id": "1234:5678",
      "type": "boardSubscriber",
      "attributes": {
        "boardId": 1234,
        "dateSubscribed": 1757000000000,
        "subscribedByUserId": 5678,
        "user": {
          "id": "5678",
          "name": "Jane Doe",
          "email": "jane.doe@example.com",
          "avatarUrl": "https://example.com/avatars/5678.png",
          "bio": "Learning enthusiast",
          "contentLocale": "en-US",
          "uiLocale": "en-US",
          "timeZoneCode": "PST",
          "userType": "INTERNAL",
          "state": "ACTIVE",
          "profile": "Learner",
          "roles": ["Learner"],
          "gamificationEnabled": true,
          "pointsEarned": 120,
          "pointsRedeemed": 20,
          "enrollOnClick": true,
          "preferredResolution": "720p",
          "lastLoginDate": "2026-09-23T18:12:04.000Z"
        }
      }
    }
  ]
}
```

### Esquema de recursos {#resource-schema-get-subscribers}

La respuesta incluye un nuevo recurso, `boardSubscriber`. Sus atributos incluyen `boardId`, `dateSubscribed`, `subscribedByUserId` y `user`. El objeto de usuario incrustado tiene información del suscriptor, como el ID de usuario, el nombre, el correo electrónico, el perfil, las funciones y otros metadatos de usuario.

**`boardSubscriber`atributos**

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | cadena | ID de suscripción opaco. |
| `type` | cadena | Tipo de recurso. |
| `boardId` | Días | ID del tablero al que está suscrito el usuario. |
| `dateSubscribed` | Días | Marca de tiempo del momento en que el usuario se suscribió al tablero. |
| `subscribedByUserId` | Días | ID del usuario que creó la suscripción. |
| `user` | objeto | Detalles del usuario suscrito (incrustado, consulte a continuación). |

**`user`(incrustado, dentro de un suscriptor)**

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | cadena | ID de usuario opaco. |
| `name` | cadena | Nombre para mostrar del usuario. |
| `email` | cadena | Dirección de correo electrónico del usuario. |
| `avatarUrl` | cadena | URL de la imagen de perfil del usuario. |
| `bio` | cadena | Breve biografía del usuario. |
| `binUserId` | cadena | Identificador interno del usuario. |
| `userUniqueId` | cadena | Identificador único del usuario en la cuenta. |
| `userType` | cadena | Tipo de usuario, por ejemplo, interno o externo. |
| `state` | cadena | Estado actual de la cuenta de usuario. |
| `profile` | cadena | Perfil asignado al usuario. |
| `roles` | conjunto de cadenas | Funciones desempeñadas por el usuario. |
| `contentLocale` | cadena | Configuración regional en la que el usuario prefiere ver el contenido. |
| `uiLocale` | cadena | Configuración regional utilizada para la interfaz de usuario. |
| `timeZoneCode` | cadena | Zona horaria configurada para el usuario. |
| `preferredResolution` | cadena | Resolución de vídeo preferida del usuario. |
| `enrollOnClick` | booleano | Si el usuario se inscribe automáticamente al seleccionar un objeto de aprendizaje. |
| `gamificationEnabled` | booleano | Si la interacción está activada para el usuario. |
| `pointsEarned` | Días | Total de puntos de interacción obtenidos por el usuario. |
| `pointsRedeemed` | Días | Puntos de interacción totales canjeados por el usuario. |
| `lastLoginDate` | cadena | Fecha y hora del inicio de sesión más reciente del usuario. |
| `fields` | objeto | Campos de usuario personalizados y sus valores. |
| `metadata` | objeto | Metadatos adicionales asociados al usuario. |

### Códigos de respuesta {#response-codes-get-subscribers}

| Estado | Significado |
|---|---|
| 200 | La solicitud se realizó correctamente. La respuesta contiene los suscriptores de la junta. |
| 400 | Error de solicitud erróneo genérico. Por ejemplo, el ID del tablero o un valor de paginación no están bien formados. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |

### Utilice esta API en su integración {#integration-get-subscribers}

Un caso de uso común es una vista de administrador o moderador que muestra a todos los usuarios que reciben actualizaciones de un tablero.

1. Cuando se cargue la vista, llame a este extremo con el Id. de placa y un valor `page[limit]` adecuado para su diseño (hasta 200).
1. Mostrar los valores `user.name`, `user.email` y `dateSubscribed` de cada suscriptor.
1. Si el número de registros devuelto es igual a `page[limit]`, puede haber más suscriptores. Vuelva a llamar al extremo, aumentando `page[offset]` por el tamaño de página, hasta que una página devuelva menos registros de los solicitados.

## API para suscribir usuarios a un tablero {#api-subscribe-users}

### Propósito de la API {#purpose-subscribe-users}

Suscribir uno o más usuarios a un panel de discusión para que reciban mensajes de correo electrónico de resumen sobre él. Identifique a los usuarios por ID de usuario, por dirección de correo electrónico (se resuelven en ID de usuario dentro de la cuenta), o por ambos conceptos. Puede añadir varios usuarios en una sola solicitud. Consulte [Suscripciones en bloque](#bulk-subscriptions).

### Punto final {#endpoint-subscribe-users}

```http
POST /primeapi/v2/boards/{id}/subscribers
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:write` |
| Formato de solicitud | `application/vnd.api+json;charset=UTF-8` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Parámetros {#parameters-subscribe-users}

| Parámetro | En | Obligatorio | Descripción |
|---|---|---|---|
| `id` | path | Sí | El ID del tablero al que suscribir usuarios. |

### Cuerpo de la solicitud {#request-body-subscribe-users}

Enviar los usuarios como atributos de un recurso `boardSubscriberBulkRequest`. Se requiere al menos uno de `userIds` o `emails`.

| Campo | Tipo | Descripción |
|---|---|---|
| `data.attributes.userIds` | conjunto de números | Los ID de los usuarios que se van a suscribir. |
| `data.attributes.emails` | conjunto de cadenas | Las direcciones de correo electrónico de los usuarios que se van a suscribir. Cada dirección se resuelve en un ID de usuario dentro de la cuenta. |

### Ejemplo de solicitud {#example-request-subscribe-users}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriberBulkRequest",
    "attributes": {
      "userIds": [
        1234,
        5678
      ],
      "emails": [
        "abc@xyz.com"
      ]
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1010/subscribers'
```

### Ejemplo de respuesta - 207 Multi-Status {#example-response-subscribe-users}

```json
{
  "added": [
    {
      "userId": "12345",
      "status": "SUCCESS"
    }
  ],
  "failed": [
    {
      "userId": "78910",
      "errorCode": "NO_BOARD_ACCESS"
    }
  ]
}
```

**Atributos de respuesta**

| Campo | Tipo | Descripción |
|---|---|---|
| `added` | matriz | Los usuarios que estaban suscritos. Cada entrada tiene `userId` y `status`. Los usuarios que ya estaban suscritos también se notifican aquí como exitosos. |
| `failed` | matriz | Los usuarios que no se pudieron suscribir. Cada entrada tiene `userId` y `errorCode`, por ejemplo `NO_BOARD_ACCESS`. |

### Códigos de respuesta {#response-codes-subscribe-users}

| Estado | Significado |
|---|---|
| 207 | Multi-Status. Se procesó la solicitud y la respuesta muestra el resultado de cada usuario en `added` y `failed`. |
| 400 | Error de solicitud erróneo genérico. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |
| 404 | No se encontró el recurso solicitado, como el tablero. |
| 409 | El tablero está inactivo, eliminado o retirado, por lo que se rechaza toda la solicitud. |

### Suscripciones en bloque {#bulk-subscriptions}

Utilizar la suscripción en bloque para agregar varios usuarios a un panel de discusión en una sola solicitud. La suscripción en bloque ayuda a reducir el número de llamadas de API que necesita para administrar suscriptores. Resulta útil cuando:

* Un instructor gestiona varias cohortes.
* Un administrador de cohorte necesita tener acceso a muchos paneles de discusión.
* Un sistema externo sincroniza las suscripciones de placa en lote.
* Es necesario suscribirse a varios instructores durante la creación de la cohorte.

#### Añadir comportamiento en bloque

Una solicitud en bloque puede contener identificadores de usuario, direcciones de correo electrónico o una combinación de ambos. Cada usuario se procesa de forma independiente.

#### Comportamiento idempotente

La adición en bloque es idempotente. Si un usuario ya está suscrito al tablero, la solicitud se realiza correctamente, no se crea ninguna suscripción duplicada y la suscripción existente permanece sin cambios. Esto permite a los clientes reintentar las solicitudes de forma segura.

#### Éxito parcial

Algunos usuarios pueden suscribirse, mientras que otros no superan la validación. La operación no falla porque uno o más usuarios no son válidos.

| Caso | Resultado |
|---|---|
| El usuario existe y tiene acceso al tablero | Correcto |
| El usuario ya está suscrito | Correcto |
| El usuario no tiene acceso al tablero | Error (`NO_BOARD_ACCESS`) |
| El usuario no existe | Fracaso |
| El usuario está inactivo | Fracaso |
| El usuario se ha eliminado | Fracaso |

#### Formato de respuesta

La suscripción en bloque devuelve HTTP 207 Multi-Status con un resultado `added` y un resultado `failed` para cada usuario, como en el [ejemplo de respuesta](#example-response-subscribe-users).

#### Errores de validación comunes

* **El usuario no tiene acceso al tablero.** Si un usuario no tiene visibilidad del tablero, se devuelve `NO_BOARD_ACCESS` para ese usuario. Los demás usuarios se seguirán procesando normalmente.
* **El tablero está inactivo, eliminado o retirado.** Si el tablero no cumple los requisitos para suscripciones, la solicitud se rechaza con Conflicto HTTP 409.
* **El usuario no es válido.** Si una cuenta de usuario no existe, está inactiva o se eliminó, la operación devuelve una entrada de error para ese usuario.

## API para cancelar la suscripción de un usuario de un tablero {#api-unsubscribe-user}

### Propósito de la API {#purpose-unsubscribe-user}

Cancelar la suscripción de un usuario de un panel de discusión. Una vez eliminada la suscripción, el usuario ya no recibirá notificaciones ni mensajes de correo electrónico de resumen para ese tablero.

### Punto final {#endpoint-unsubscribe-user}

```http
DELETE /primeapi/v2/boards/{id}/subscribers/{userId}
```

| Propiedad | Valor |
|---|---|
| Ámbito | `admin:write` |
| Formato de respuesta | `application/vnd.api+json;charset=UTF-8` |

### Parámetros {#parameters-unsubscribe-user}

| Parámetro | En | Obligatorio | Descripción |
|---|---|---|---|
| `id` | path | Sí | El ID del tablero. |
| `userId` | path | Sí | El ID del usuario al que se va a cancelar la suscripción. |

### Ejemplo de solicitud {#example-request-unsubscribe-user}

```bash
curl -X DELETE \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers/5678'
```

### Ejemplo de respuesta - 204 Sin contenido {#example-response-unsubscribe-user}

La respuesta no tiene cuerpo.

### Códigos de respuesta {#response-codes-unsubscribe-user}

| Estado | Significado |
|---|---|
| 204 | La solicitud se realizó correctamente. Se canceló la suscripción del usuario al tablero. |
| 400 | Error de solicitud erróneo genérico. |
| 401 | A la solicitud le faltan credenciales válidas o el acceso se denegó debido a credenciales no válidas. |
| 404 | No se encontró el recurso solicitado, como el tablero o la suscripción. |

## Ordenación de API de marcadores y gestión de contenido retirado {#bookmark-api-ordering-retired-content}

### Propósito de la API

Los alumnos marcan los cursos de formación que desean volver a consultar. Antes de este cambio, las API de marcadores no devolvían marcadores en ningún orden concreto. Las integraciones, especialmente las implementaciones descentralizadas, no podían mostrar primero los marcadores guardados más recientemente. Los alumnos con muchos marcadores tuvieron que desplazarse por los elementos más antiguos para buscar los más recientes.

Los marcadores de objetos de aprendizaje retirados también permanecían en la lista. Al seleccionar uno, aparece el error &quot;Página no encontrada&quot;.

Este cambio mejora las API de marcadores de dos formas:

* Los marcadores se devuelven en orden cronológico, primero el más reciente.
* Los marcadores de objetos de aprendizaje retirados ya no se devuelven.

No se introducen nuevos puntos finales, parámetros ni atributos de respuesta. Las integraciones existentes siguen funcionando sin cambios.

### URL base y convenciones

Las API de marcadores utilizan la siguiente ruta de base y convenciones:

| Elemento | Valor |
|---|---|
| Ruta base | `/primeapi/v2` |
| Tipo de contenido | `application/vnd.api+json` |
| Autenticación | Token de OAuth con acceso de lectura del alumno |
| Orden predeterminado | Marcador más reciente primero |
| Nuevos parámetros | Ninguno |
| Estructura de respuesta | Inalterado |

### Puntos finales

#### Puntos finales que devuelven marcadores

Los siguientes puntos finales devuelven marcadores en el nuevo orden:

| Punto final | Devoluciones |
|---|---|
| `GET /primeapi/v2/learningObjects?filter.bookmarks=true` | Objetos de aprendizaje que el alumno tiene marcados |
| `GET /primeapi/v2/bookmarks` | Marcadores del alumno |

#### Ordene los objetos de aprendizaje marcados

`GET /primeapi/v2/learningObjects?filter.bookmarks=true`

<!-- Content Review by Claude: Please confirm the endpoint list. The dev-to-QE hand-off confirms ordering for GET /learningObjects?filter.bookmarks=true. The PRD (ALMER-442) also lists GET /primeapi/v2/bookmarks. Please also confirm the OAuth scope. -->

Devuelve los objetos de aprendizaje marcados por el alumno que realiza la llamada. El elemento marcado más recientemente es el primero y el más antiguo es el último.

**Ámbito:** acceso de lectura del alumno

El extremo acepta el siguiente parámetro de consulta:

| Parámetro | En | Obligatorio | Descripción |
|---|---|---|---|
| `filter.bookmarks` | consulta | Sí | Se establece en `true` para devolver solo los objetos de aprendizaje marcados por el alumno |

**Ejemplo de solicitud**

```http
GET /primeapi/v2/learningObjects?filter.bookmarks=true
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

**Ejemplo 200 Respuesta correcta**

El alumno marcó en primer lugar la Introducción a Adobe Analytics, en segundo lugar la Creación de proyectos de espacio de trabajo y en último lugar la Segmentación avanzada en Adobe Analytics. La respuesta los enumera de más recientes a más antiguos. Se omiten otros atributos por brevedad.

```json
{
  "data": [
    {
      "id": "course:2400162",
      "type": "learningObject",
      "attributes": {
        "name": "Advanced Segmentation in Adobe Analytics"
      }
    },
    {
      "id": "course:2400160",
      "type": "learningObject",
      "attributes": {
        "name": "Building Workspace Projects"
      }
    },
    {
      "id": "course:2400159",
      "type": "learningObject",
      "attributes": {
        "name": "Getting Started with Adobe Analytics"
      }
    }
  ]
}
```

>[!NOTE]
>
>El nuevo orden es el comportamiento predeterminado y se aplica a todas las cuentas.

### Ordenación de marcadores

#### Cómo se ordenan los marcadores

Los marcadores se ordenan por la fecha en que el alumno los guardó, de más recientes a más antiguos. Por ejemplo, si un alumno marca el curso A, luego el curso B y, por último, el curso C, la respuesta muestra el curso C en primer lugar, el curso B en segundo y el curso A en último lugar.

Si un objeto de aprendizaje con marcador que aparece en la décima posición, por ejemplo, &quot;no se guarda&quot; y se vuelve a marcar posteriormente, aparecerá como reciente con marcador y al principio en la lista.

Las integraciones que anteriormente ordenaban los marcadores en el cliente pueden eliminar esa lógica y mostrar los resultados en el orden devuelto.

### Gestión de contenido retirado

#### Cómo se gestionan los objetos de aprendizaje retirados

Los marcadores de objetos de aprendizaje retirados no se devuelven en la respuesta, independientemente de si el alumno está inscrito en el objeto de aprendizaje.

Los objetos de aprendizaje retirados marcados no aparecerán a menos que el alumno se haya inscrito en ellos.

Los alumnos ya no ven marcadores que provocan el error &quot;Página no encontrada&quot;. El marcador se oculta en los resultados, no se elimina.

### Compatibilidad

Este cambio no afecta a los consumidores de API existentes:

* Los puntos finales y sus parámetros no cambian.
* La estructura de respuesta no se modifica y no se agregan ni eliminan atributos.
* Solo el orden de los resultados y la exclusión de los objetos de aprendizaje retirados difieren del comportamiento anterior.

### Utilice esta API en su integración

Un caso de uso común es una lista &quot;Guardados para más tarde&quot; en una experiencia de alumno sin encabezado. Desea que los alumnos vean primero sus marcadores más recientes, sin vínculos a contenido retirado.

1. Llame a `GET /primeapi/v2/learningObjects?filter.bookmarks=true` cuando el alumno abra la lista.
2. Muestre los objetos de aprendizaje en el orden devuelto. El primer elemento es el marcador más reciente.
3. Elimine cualquier ordenación del lado del cliente o filtrado de contenido retirado que haya agregado como solución alternativa.
4. Mostrar un recuento de marcadores usando el número de elementos de la respuesta. Los marcadores de objetos de aprendizaje retirados ya no se incluyen.

### Compatibilidad de API con instancias de inscripción múltiple en el widget de cumplimiento del alumno en la aplicación del alumno {#api-multienrolled-instances-lc-widget}

La API pública admite este comportamiento a través de un parámetro de consulta opcional en el extremo de inscripciones existente. Si se omite el parámetro, la API devolverá los mismos resultados que antes, por lo que las integraciones existentes, incluidas las implementaciones descentralizadas, seguirán funcionando sin cambios.

**Punto final**

GET /primeapi/v2/enrollments

**Parámetro de consulta**

includeMultiInstanceEnrollments (opcional)

**Consulta**

https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&filter.loTypes=course&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&sort=dateEnrolled

**Valor**

es cierto. False de forma predeterminada.

**Cuerpo de respuesta**

{

&quot;links&quot;: {

&quot;yo&quot;: &quot;[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true)&quot;,

&quot;siguiente&quot;: &quot;[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true&amp;page\[cursor\]=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmluZ1dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&page%5bcursor%5d=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmluZ1Byb2dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9)&quot;

},

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:15067_30122_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;completedDeadline&quot;: &quot;2026-02-24T10:50:45.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:15067&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:15067_30122&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:15067_3012_41715_1_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:1108800_1997400_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;SELF_ENROLL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:108800&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:1108800_1997400&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:108800_1997400_2174574_0_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2027668_3707328_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2027668&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:202768_3707328&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2027668_3707328_2665897_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2030067_3709862_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2030067&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2030067_3709862&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2030067_3709862_2668467_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:3081896_574915_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:3081896&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:3081896_5749155&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:3081896_5749155_3737554_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

},

{

&quot;id&quot;: &quot;course:3081896_5749155_373755_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037893_3717940_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037893&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037893_3717940&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2037893_3717940_3676856_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:3049434_5713130_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;completedDeadline&quot;: &quot;2020-05-05T18:29:59.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:3049434&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:3049434_5713130&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:3049434_5713130_3693595_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2001397_3679403_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2001397&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2001397_3679403&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2001397_3679403_2635974_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037862_371790_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;PENDING_APPROVAL&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037862&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037862_3717900&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2037862_3717900_3676816_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037837_3717863_3400468&quot;,

&quot;tipo&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;atributos&quot;: {

&quot;completedDeadline&quot;: &quot;2020-02-29T18:29:59.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;SELF_ENROLL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;puntuación&quot;: 0,

&quot;estado&quot;: &quot;OTROS&quot;

},

&quot;relaciones&quot;: {

&quot;alumno&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;3400468&quot;

&quot;tipo&quot;: &quot;usuario&quot;

}

},

&quot;learningObject&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037837&quot;,

&quot;tipo&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;datos&quot;: {

&quot;id&quot;: &quot;course:2037837_3717863&quot;,

&quot;tipo&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;datos&quot;: \[

{

&quot;id&quot;: &quot;course:2037837_3717863_3597363_0_340468&quot;,

&quot;tipo&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

}

\]

}

## Fecha del último acceso para la inscripción en la ruta de aprendizaje {#api-last-access-date-lp-enrollment}

Adobe Learning Manager le permite almacenar metadatos personalizados, como la fecha del último acceso, en una inscripción de ruta de aprendizaje. Puede definir y leer los metadatos a través de la API. Esto le ayuda a realizar un seguimiento del acceso con plazos determinados a las rutas de aprendizaje que asigne.

## Acerca de los metadatos de inscripción de ruta de aprendizaje

Ya puede establecer una fecha de último acceso para la inscripción de un curso mediante la API. Esa fecha controla el tiempo que un alumno puede acceder al curso. Las inscripciones de rutas de aprendizaje ahora admiten un campo de metadatos genérico, por lo que puede almacenar una fecha de último acceso o cualquier otro valor del que desee realizar un seguimiento.

No es necesario activar el campo ni enviar un encabezado especial. El campo está vacío hasta que lo establezca.

>[!NOTE]
>
>Los metadatos son para su propio seguimiento. Adobe Learning Manager no la actualiza cuando los alumnos abren una ruta de aprendizaje o sus cursos, ni controla el acceso a la misma. Tampoco se propaga a los cursos de la ruta. Cada curso mantiene su propia fecha de último acceso, por lo que los cursos de la misma ruta pueden tener fechas diferentes. Continúe administrando la caducidad de acceso a nivel de curso por separado.

### Reglas de metadatos {#metadata-rules}

* El valor debe ser un objeto JSON. Una cadena, número, booleano o matriz devuelve un error 400 con el mensaje `metadata must be a JSON object`.
* Puede utilizar cualquier tecla. Adobe Learning Manager no valida claves o valores y no exige un formato de fecha. Los ejemplos de este artículo utilizan milisegundos de época, el mismo formato que las fechas de los cursos.
* Una solicitud de PATCH reemplaza todo el objeto de metadatos. No se combina con los valores existentes, por lo que las teclas que no se incluyen se eliminan.
* Al establecer `"metadata": null`, se borran todos los metadatos y se devuelven 200.
* Una solicitud con un objeto `attributes` vacío, o sin una clave `metadata`, no cambia los metadatos almacenados.
* Cuando no se establece ningún metadato, o después de borrarlo, la clave `metadata` no está en la respuesta.

## Definir metadatos en una inscripción existente

Utilice un token de administrador.

Envíe una solicitud de PATCH al siguiente extremo, donde `{enrollmentId}` es el Id. de inscripción de ruta de aprendizaje con el formato `learningProgram:<lpId><instanceId><userId>`:

```
PATCH /primeapi/v2/users/{userId}/enrollments/{enrollmentId}
```

Utilice este cuerpo de la solicitud:

```json
{
  "data": {
    "id": "<enrollmentId>",
    "type": "learningObjectInstanceEnrollment",
    "attributes": {
      "metadata": {
        "lastAccessDate": 1745337600000
      }
    }
  }
}
```

### Definir metadatos al inscribir a un alumno

Utilice un token de administrador.

Envía una solicitud de POST con la ruta de aprendizaje y los ID de instancia. Incluya un objeto `metadata` opcional en el cuerpo de la solicitud.

```
POST /primeapi/v2/users/{userId}/enrollments?loId=<lpId>&loInstanceId=<instanceId>
```

* Si `metadata` no es un objeto JSON, la solicitud devuelve 400 y el usuario no está inscrito.
* Si el usuario ya está inscrito, la solicitud devuelve 200 y no cambia nada. Para cambiar los metadatos de una inscripción existente, utilice la solicitud de PATCH.
* La respuesta no incluye los metadatos. Envíe una solicitud de GET para leerla.

### Recuperar metadatos

Puede recuperar metadatos con un token de administrador o de alumno. Las solicitudes difieren según el tipo de token.

| Token | Obtener una inscripción | Enumerar inscripciones de rutas de aprendizaje |
|---|---|---|
| Administrador | `GET /primeapi/v2/users/{userId}/enrollments/{enrollmentId}` | `GET /primeapi/v2/users/{userId}/enrollments?filter.loTypes=learningProgram` |
| Administración | `GET /primeapi/v2/enrollments/{enrollmentId}`<br>`GET /primeapi/v2/learningObjects/{id}?include=enrollment` | `GET /primeapi/v2/enrollments?filter.loTypes=learningProgram` |

>[!NOTE]
>
>El parámetro `include=enrollment` solo funciona con un token de alumno. No se admite para la función de administrador.

La respuesta devuelve el objeto `metadata` con la inscripción de la ruta de aprendizaje.

### Uso de metadatos en portales externos y descentralizados

Los portales externos y las integraciones utilizan las mismas llamadas de API. Utilice la solicitud que coincida con el distintivo que utiliza el portal.

* **Mostrar el valor en el portal:** Envíe la solicitud de GET para su tipo de token de la tabla anterior y lea el objeto `metadata` de la respuesta.
* **Actualice el valor desde un sistema externo, como una plataforma comercial:** Envíe la solicitud del PATCH con un token de administrador.

## API de trabajos: Exportar informes del Report Builder con generateCustomReport {#api-job-report-builder-exports}

La versión de diciembre de 2026 de Adobe Learning Manager agrega un nuevo tipo de trabajo, `generateCustomReport`, a la API de trabajos. Utilícelo para exportar cualquier informe que haya creado en Report Builder, de forma automatizada, pasando el ID del informe.

Combinado con el nuevo conjunto de datos de pruebas de L2 en Report Builder, ahora puede:

* Exporta datos de cuestionarios de nivel de pregunta (L2) en varios cursos y módulos en un solo informe, en lugar de ejecutar `generateQuizReport` una vez por cada curso.
* Automatiza las exportaciones recurrentes, por ejemplo, una exportación incremental diaria a tu almacén de datos o herramienta de BI.

Los tipos de trabajo existentes, incluido `generateQuizReport`, no se modifican.

### Antes de comenzar

* Debe ser administrador. El tipo de trabajo `generateCustomReport` no está disponible para otras funciones.
* Cree y guarde primero el informe en Report Builder. Para los datos de prueba de L2, cree el informe a partir del conjunto de datos de prueba de L2 e incluya los campos de nivel de pregunta que necesite, como el texto de la pregunta, la respuesta del alumno, la puntuación, el número de intento y la fecha de respuesta.
* Anote el ID del informe. Se pasa en la solicitud como `reportId`.

### Crear un trabajo

**Punto final**

```
POST /primeapi/v2/jobs
```

**Cuerpo de solicitud**

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "description": "Daily L2 quiz export",
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      }
    }
  }
}
```

**Atributos**

| Atributo | Obligatorio | Descripción |
|---|---|---|
| `jobType` | Sí | Debe ser `generateCustomReport`. |
| `payload.reportId` | Sí | El identificador del informe del Report Builder guardado, como una cadena. Debe ser un entero positivo, pasado como una cadena, por ejemplo `"1478"`. Enviar un número, 0, un negativo, un decimal o un valor vacío devuelve un error. |
| `description` | No | Una descripción de su elección para el trabajo. |
| `callbackUrl` | No | Dirección URL a la que se llamará cuando finalice el trabajo. Funciona igual que para otros tipos de trabajos. |
| `payload.filters` | No | Consulte la sección siguiente. |

### Anular el filtro de fecha (opcional) {#override-date-filter}

```json
"payload": {
  "reportId": "1478",
  "filters": [
    { "columnName": "L2 Quiz - Response - Timestamp", "operator": "gte", "val": "2026-11-15T00:00:00.000Z" }
  ]
}
```

* Reemplaza el filtro de fecha guardado del informe sólo para esta ejecución. La exportación abarca `val` (inclusive) hasta el momento en que se ejecuta el trabajo.
* `columnName` usa el formato `<Dataset name> - <Field name>`. Debe coincidir con un filtro de fecha que ya existe en el informe. No distingue entre mayúsculas y minúsculas, pero el espaciado y los guiones deben coincidir exactamente.
* `operator` es opcional y solo se permite `gte`.
* `val` es una hora UTC ISO 8601 en los últimos 7 días. Los tiempos se truncan al segundo.
* Puede modificar varias columnas. Una lista vacía significa que se utilizan los filtros guardados.
* Caso práctico: una exportación incremental diaria que comienza donde finalizó la anterior.

### Errores devueltos al crear un trabajo

| Causa | Mensaje |
|---|---|
| Falta `reportId` | `reportId is required` |
| `reportId` no es una cadena entera positiva | `reportId must be a positive integer string` |
| Fecha que no está en formato ISO | `filters.val must be in ISO format, e.g. 2020-01-01T18:30:00.000Z` |
| Fecha anterior a 7 días o futura | `filters.val must be within the last 7 days` |
| Operador distinto de `gte` | `filters.operator must be gte` |
| La misma columna dada dos veces | `Duplicate filter column: <column>` |
| La columna no es un filtro en el informe | `Unsupported custom report filter column: <column>` |
| Se sigue ejecutando un trabajo para el mismo informe | `There exists an similar job with id = <jobId> which has not finished yet` |

Sólo se detectan problemas con la definición de informe guardada cuando se ejecuta el trabajo. En ese caso, el estado del trabajo se convierte en `Failed` y no se devuelve ningún motivo.

### Requisitos de informes

El trabajo falla con un mensaje de error si el informe no cumple estas condiciones:

* La definición del informe incluye un filtro de fecha relativa, por ejemplo, los últimos 7 días.
* Cada filtro de fecha del informe debe abarcar 7 días o menos, no solo uno.
* No se admiten los intervalos de fechas fijos, con una fecha de inicio y una fecha de finalización establecidas, y el trabajo falla.
* Un informe sin filtro de fecha genera un error. Esto incluye los informes generados en conjuntos de datos que no tienen campos de fecha.

>[!NOTE]
>
>La solicitud del POST se valida inmediatamente. Una solicitud no válida se rechaza con HTTP 400 y el motivo está en `source.info`.

### Comprobar el estado del trabajo y descargar el informe

**Punto final**

```
GET /primeapi/v2/jobs/{jobId}
```

La respuesta utiliza la misma estructura que otros tipos de trabajo. Cuando se complete el trabajo, `status.code` es `Completed` y `status.data.s3Url` contiene el vínculo de descarga.

```json
{
  "data": {
    "type": "job",
    "id": "12345",
    "attributes": {
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      },
      "status": {
        "code": "Completed",
        "data": {
          "s3Url": "valid for 7 days"
        }
      }
    }
  }
}
```

La API devuelve `Submitted`, `Completed` y `Failed`. El archivo es un único archivo CSV denominado `report.csv`.

>[!NOTE]
>
>La URL de descarga es válida durante siete días. Descargue el archivo en cuanto finalice el trabajo.

>[!IMPORTANT]
>
>Cualquier persona que disponga del vínculo puede descargar el archivo sin iniciar sesión. Controle el vínculo como lo haría con los datos que contiene.

**Ejemplo de trabajo erróneo**

```json
"status": { "code": "Failed" }
```

### Límites

Solo se puede ejecutar un trabajo de `generateCustomReport` para un informe a la vez. Se rechaza una segunda solicitud hasta que finalice la primera.

### Salida del informe de pruebas de L2

Cuando se genera un informe a partir del conjunto de datos de pruebas L2 en Report Builder y se exporta con `generateCustomReport`, el resultado tiene las siguientes características:

* El resultado es un único archivo CSV denominado `report.csv`. El módulo es una columna del archivo. Si selecciona un curso, el informe devuelve solo sus módulos de prueba.
* Cada fila representa la respuesta de un alumno a una pregunta en un intento.
* Los datos se actualizan en el intervalo estándar del Report Builder (aproximadamente cada 15 minutos).
* Los valores de fecha y hora se encuentran en la zona horaria de su cuenta. El encabezado de columna muestra la zona horaria, por ejemplo, `L2 Quiz - Response - Timestamp (America/Argentina/Salta)`.

### Campos del conjunto de datos de pruebas L2

| Categoría | Campos |
|---|---|
| Administración | ID de usuario |
| Curso | ID del curso, ID de instancia del curso, nombre del curso |
| Módulo | ID de módulo, nombre de módulo, versión de módulo |
| Pregunta | ID de pregunta, texto de pregunta, respuesta correcta, tipo de interacción |
| Respuesta | Respuesta La Respuesta, Puntuación Alcanzada, Puntuación Máxima Posible, Es Correcta, Marca De Tiempo De Respuesta |
| Intentar | Número de intentos |

>[!NOTE]
>
>El conjunto de datos de pruebas L2 no está vinculado a otros conjuntos de datos de Report Builder. Los atributos de nombre, correo electrónico, responsable y personalizados del alumno no están disponibles en este informe. Para hacer coincidir una fila con un alumno, utilice el ID de usuario.

También puede exportar informes generados en otros conjuntos de datos de Report Builder con `generateCustomReport`. Los campos disponibles en el resultado dependen del conjunto de datos.

## API para crear y administrar el conector de Zoom

Utilice estas API para administrar las conexiones de Zoom en Adobe Learning Manager. Puede recuperar conexiones existentes, guardar credenciales de Zoom, crear o actualizar conexiones, configurar permisos de acceso para grupos de usuarios y funciones personalizadas, y habilitar o deshabilitar una conexión.

### Configurar las API del conector de Zoom

La configuración y administración de un conector de Zoom requiere cuatro llamadas a la API. Hazlas en este orden:

| Paso | API | Qué hace |
|---|---|---|
| 1 | `POST /ctr/authcred/uuid/20012` | Guarda las credenciales de Zoom. |
| 2 | `POST /ctr/app/esconnect` | Crea la conexión de Zoom o actualiza una existente. |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Establece los grupos de usuarios y las funciones personalizadas que pueden utilizar la conexión. |
| 4 | `POST /ctr/xtsas/{connectionId}/enable` | Habilita o deshabilita la conexión. |

>[!NOTE]
>
>Estas API utilizan la sesión del administrador de integración que ha iniciado sesión. No utilizan una clave de API ni un token de OAuth.

### URL base y convenciones

Las API del conector de Zoom utilizan las siguientes convenciones:

| Elemento | Valor |
|---|---|
| URL básica | `https://learningmanagerstage1.adobe.com` |
| Tipo de contenido | `application/json` |
| Autenticación | Sesión de un administrador de integración que ha iniciado sesión |
| Encabezados requeridos | `content-type`, `accept`, `x-acap-caller-role: ROLE_INTEGRATIONADMIN`, `x-csrf-token` y `Cookie` |
| UUID del catálogo de integración para Zoom | `20012` |
| Límite de conexiones | 50 Conexiones de zoom |

El valor `x-csrf-token` está incrustado en el HTML de la página Administrador de integración como `csrfToken`. El encabezado `Cookie` contiene las cookies de sesión del administrador que ha iniciado sesión.

### Antes de comenzar

- Inicie sesión como administrador de integración.
- Cree una aplicación OAuth de servidor a servidor de Zoom. Anote el ID de cliente, el secreto de cliente y el ID de cuenta. También necesita la dirección de correo electrónico del superadministrador de Zoom.
- Llamar a `GET /ctr/xtsas/canCreateAccount/25`. Devuelve `true` si puede crear otra conexión de Zoom.

### Paso 1: Guarde las credenciales de Zoom {#save-credentials}

Llame a esta API antes de crear o actualizar una conexión. Almacena las credenciales que utiliza el conector para conectarse a Zoom.

```
POST /ctr/authcred/uuid/20012
```

Para actualizar una conexión existente, agregue el parámetro de consulta `connectionId`:

```
POST /ctr/authcred/uuid/20012?connectionId={connectionId}
```

El cuerpo de la solicitud son las credenciales como texto JSON. Es una cadena JSON que contiene JSON, no un objeto anidado. Incluya las comillas exteriores.

| Clave | Descripción |
|---|---|
| `clientId` | El ID de cliente de la aplicación Zoom. |
| `clientSecret` | El secreto de cliente de la aplicación Zoom. Este valor es confidencial. |
| `accountId` | El ID de cuenta de Zoom. |
| `superAdmin` | La dirección de correo electrónico del superadministrador de Zoom. |

Cuerpo de solicitud de muestra:

```
"{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}"
```

Ejemplo de respuesta `200 OK`:

```json
{
  "code": 0,
  "description": "Success"
}
```

`code: 0` significa que se guardaron las credenciales.

### Paso 2: Crear o actualizar la conexión de Zoom {#create-connection}

Esta API crea una conexión de Zoom. El mismo extremo también actualiza una conexión existente.

```
POST /ctr/app/esconnect
```

El cuerpo de la solicitud tiene los siguientes campos:

| Campo | Obligatorio | Descripción |
|---|---|---|
| `UUID` | Sí | El UUID del catálogo de integración. Usar `20012` para Zoom. |
| `listOfConnections` | Sí | Conexiones que se van a crear. Enviar un elemento. |
| `listOfConnections[].name` | Sí | El nombre para mostrar del conector, por ejemplo `Zoom_Partner_X`. |
| `listOfConnections[].tag` | Sí | Enviar una cadena vacía (`""`) al crear un conector. Omítala cuando actualices una. |
| `listOfConnections[].credentialsJson` | Sí | Las credenciales son texto JSON. Utilice la misma cadena que envió en el paso 1. |
| `listOfConnections[].schedules` | Sí | Programación de la sincronización. Enviar `objectUUID` 10002, `priority` 1 y `type` 1. |
| `listOfConnections[].id` | Actualizar solo | Id. de la conexión que se va a actualizar, por ejemplo `3474737`. |

Cuerpo de solicitud de muestra:

```json
{
  "UUID": 20012,
  "listOfConnections": [
    {
      "name": "Zoom_Example",
      "tag": "",
      "credentialsJson": "{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}",
      "schedules": [
        { "objectUUID": 10002, "priority": 1, "type": 1 }
      ]
    }
  ]
}
```

Ejemplo de respuesta `200 OK`:

```json
[3474737]
```

La respuesta es una matriz JSON que contiene el identificador de la nueva conexión. Utilice este ID en los pasos 3 y 4, así como en cualquier llamada de seguimiento.

### Comparación de creación y actualización

| Diferencia | Crear | Actualización |
|---|---|---|
| `listOfConnections[].id` | No enviado | El ID de conexión |
| `listOfConnections[].tag` | `""` | No enviado |
| Llamada de credenciales en el paso 1 | `POST /ctr/authcred/uuid/20012` | `POST /ctr/authcred/uuid/20012?connectionId={id}` |

### Paso 3: Establecer quién puede utilizar la conexión {#set-access}

Esta API define qué grupos de usuarios y funciones personalizadas pueden utilizar la conexión.

```
PUT /ctr/xtsa/{connectionId}/access
```

La ruta de acceso usa el singular `xtsa` para una conexión. El plural `xtsas` es la colección de conexiones.

El cuerpo de la solicitud es una matriz JSON. Cada elemento concede acceso a un grupo de usuarios o función personalizada.

| Campo | Obligatorio | Descripción |
|---|---|---|
| `accessType` | Sí | `USER_GROUP` o `CUSTOM_ROLE`. |
| `accessId` | Sí | El ID del grupo de usuarios o función personalizada, como una cadena. |

Cuerpo de solicitud de muestra:

```json
[
  { "accessType": "USER_GROUP", "accessId": "<groupId>" },
  { "accessType": "CUSTOM_ROLE", "accessId": "<roleId>" }
]
```

La API devuelve `204 No Content` sin cuerpo cuando se guarda la lista de acceso.

>[!NOTE]
>
>La solicitud reemplaza toda la lista de acceso. No se adjunta a ella. Cualquier cosa que no esté en el cuerpo pierde el acceso. Para quitar todo el acceso, envíe una matriz vacía (`[]`).

### Paso 4: Habilitar o deshabilitar la conexión {#enable-disable}

Esta API activa o desactiva una conexión. Utilícelo después de crear la conexión, siempre que necesite cambiar su estado.

```
POST /ctr/xtsas/{connectionId}/enable
```

La ruta de acceso usa el plural `xtsas`, como las llamadas de lista y eliminación. La llamada de acceso del paso 3 utiliza el singular `xtsa`.

| Parámetro de ruta | Tipo | Descripción |
|---|---|---|
| `connectionId` | Número | Id. de la conexión. Es el `id` devuelto por `GET /ctr/xtsas` y el ID devuelto en el paso 2. |

El cuerpo de la solicitud tiene los siguientes campos:

| Campo | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `objectUUID` | Número | Sí | Objeto de sincronización de la conexión. Use `10002`, el mismo valor que envió en `schedules[].objectUUID` en el paso 2. |
| `operation` | Número | Sí | Enviar `1`. |
| `val` | Booleano | Sí | El nuevo estado de la conexión. Envíe `false` para deshabilitar la conexión. Enviar `true` para habilitarlo. |

Cuerpo de solicitud de muestra para deshabilitar una conexión:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": false
}
```

Cuerpo de solicitud de muestra para habilitar una conexión:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": true
}
```

Ejemplo de solicitud para deshabilitar una conexión:

```bash
curl -X POST 'https://learningmanagerstage1.adobe.com/ctr/xtsas/<connectionId>/enable' \
  -H 'accept: application/json' \
  -H 'content-type: application/json' \
  -H 'x-acap-caller-role: ROLE_INTEGRATIONADMIN' \
  -H 'x-csrf-token: <CSRF_TOKEN>' \
  -H 'Cookie: <SESSION_COOKIES>' \
  --data '{"objectUUID":10002,"operation":1,"val":false}'
```

Para confirmar el nuevo estado, llame a `GET /ctr/xtsas`, busque la conexión por `id` y compruebe su indicador `enabled`.

>[!NOTE]
>
>El encabezado `x-acap-caller-role` debe coincidir con la función del perfil activo. Para estas API, use `ROLE_INTEGRATIONADMIN`.

### Administrar la conexión después de crearla

Puede utilizar las siguientes llamadas con el identificador de conexión:

| Propósito | Llamar |
|---|---|
| Habilitar o deshabilitar una conexión | `POST /ctr/xtsas/{connectionId}/enable` |
| Leer la lista de acceso de una conexión | `GET /ctr/xtsa/{connectionId}/access` |
| Acceso de lectura para todas las conexiones de Zoom | `GET /ctr/xtsas/access?UUID=20012` |
| Enumerar todas las conexiones. Las conexiones de zoom tienen `extsysRefId` 25. | `GET /ctr/xtsas` |
| Ver una conexión | `GET /ctr/app/connection/{id}/object/10002` |
| Eliminar una conexión de forma permanente | `DELETE /ctr/xtsas/{id}` |

>[!NOTE]
>
>La llamada a view devuelve el secreto de cliente en texto no cifrado. Trate el secreto de cliente como confidencial y gírelo si se muestra. No confirme ni comparta cookies de sesión, tokens CSRF ni credenciales, incluidos los archivos HAR y los comandos cURL copiados.

### Utilice estas API en su integración

Un caso de uso común es la configuración automatizada de un conector de Zoom para una nueva cuenta o socio.

1. Llame a `GET /ctr/xtsas/canCreateAccount/25` para confirmar que puede crear otra conexión.
2. Llame a `POST /ctr/authcred/uuid/20012` con las credenciales de Zoom.
3. Llame a `POST /ctr/app/esconnect` con el nombre del conector, la misma cadena de credenciales y la programación de sincronización. Lea el ID de conexión de la respuesta.
4. Llame a `PUT /ctr/xtsa/{connectionId}/access` con los grupos de usuarios y las funciones personalizadas que pueden usar la conexión.
5. Llame a `POST /ctr/xtsas/{connectionId}/enable` con `val` establecido en `true` o `false` para habilitar o deshabilitar la conexión. A continuación, llame a `GET /ctr/xtsas` y compruebe el indicador `enabled` para confirmar el estado.
6. Para cambiar las credenciales más adelante, repita los pasos 2 y 3 con el ID de conexión.


