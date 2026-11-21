---
description: Aprenda cómo los instructores y los responsables de cohorte reciben resúmenes por correo electrónico de la actividad del foro de debate y cómo administrar la configuración y los suscriptores con API
jcr-language: en_us
title: Notificaciones del instructor del foro de debate
exl-id: 370c9add-5572-4555-8a95-ddb470c230f4
source-git-commit: 650ec8159a4291189dfc38b03701b7b96932233d
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Notificaciones del instructor del foro de debate

## Información general

Las notificaciones del instructor del foro de debate proporcionan a los instructores, administradores de cohorte y administradores un resumen por correo electrónico de la actividad reciente en los foros de debate que supervisan. Esto resulta útil para los instructores que gestionan varias cohortes y participan en varios tableros al mismo tiempo.

Un responsable de cohorte es la persona que gestiona un grupo de alumnos (una cohorte) que realizan un curso o un programa juntos en el mismo programa.

En lugar de abrir cada tablero individualmente, los instructores reciben alertas en tiempo real en la aplicación y un resumen por correo electrónico, con la frecuencia que configure, para los tableros a los que están suscritos. Puede administrar las suscripciones al tablero y la configuración de notificaciones mediante la [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence) y la [API de suscriptores](api-changes-dec-2026.md#api-get-subscribers).

## Capacidades clave

* Puede suscribir usuarios activos de Adobe Learning Manager a paneles de discusión seleccionados mediante la API de suscriptores ([`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users), ámbito `admin:write`). Un usuario debe tener acceso al tablero cuando se envían notificaciones.
* Los usuarios reciben notificaciones en tiempo real en la aplicación para los tipos de eventos activados y un resumen por correo electrónico agrupado por tablero. Los tipos de eventos están controlados por la configuración de nivel de cuenta (`notifyNewPost`, `notifyComment` y `notifyReply`) en la [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence).
* La ventana de resumen es el período de tiempo cuya actividad se recopila en un correo electrónico de resumen. Se establece en el nivel de cuenta con el atributo `digestFrequencyHours`, de 1 a 168 horas (por ejemplo, 24 horas para un resumen diario). Se aplica a todos los usuarios de la cuenta.
* Puede suscribir usuarios por ID de usuario o dirección de correo electrónico, y puede agregar varios usuarios en una solicitud ([suscripciones en bloque](api-changes-dec-2026.md#bulk-subscriptions)). Los usuarios se crean primero en Learning Manager de la forma habitual.
* El correo electrónico de resumen enumera cada nueva publicación, comentario y respuesta para los tipos de evento habilitados, con el nombre del tablero, el nombre y la dirección de correo electrónico del autor y un vínculo directo. También muestra un recuento de las actualizaciones desde el inicio del período de resumen.
* La API `boardSubscriptionSettings` y la API de suscriptores son API públicas, por lo que puedes administrar la configuración y las suscripciones sin una interfaz de usuario (integraciones basadas en API).

## Casos de uso

En los siguientes casos prácticos se muestra cómo ayudan las notificaciones del instructor:

| Caso de uso | Cómo ayuda la notificación |
|---|---|
| Supervisar varias cohortes | Un instructor responsable de varias cohortes puede recibir una actividad resumida de los tableros asociados a esas cohortes. |
| Revisar la participación del alumno | Un administrador de cohorte puede supervisar las nuevas contribuciones e identificar los debates activos sin comprobar cada tablero por separado. |
| Seguimiento de conversaciones de seguimiento | Los comentarios y respuestas incluidos en el compendio ayudan a los instructores a identificar los debates que pueden requerir orientación o moderación. |

## Consideraciones importantes

* Un usuario debe poder acceder a un tablero cuando se envía una notificación. El acceso se comprueba de nuevo en el momento de la entrega, no solo cuando el usuario está suscrito. Si un suscriptor pierde el acceso a un tablero, la suscripción se mantiene, pero se omiten las notificaciones de dicho tablero.
* El resumen se envía como un correo electrónico, por lo que un tablero ocupado puede hacerlo muy largo. Por ejemplo, una cohorte de unos 40 alumnos podría publicar varios cientos de comentarios en seis horas.
* Si los tableros están muy activos, utilice una frecuencia de resumen más corta, como cada seis horas, para que cada correo electrónico sea gestionable. Establezca la frecuencia con `digestFrequencyHours` en la [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-create-settings).
* El número de publicaciones en el resumen de correo electrónico está limitado a 20 por tablero y por resumen. El mismo límite máximo se aplica independientemente a los comentarios (20) y respuestas (20) por tablero. Sólo se truncan las listas mostradas; los recuentos de encabezados y subencabezados reflejan siempre la actividad real y no truncada de la ventana.
* El número de suscriptores está limitado a 200 por tablero.
* Dado que el contenido se envía directamente en el correo electrónico en lugar de como datos adjuntos, el cuerpo del mensaje de correo electrónico también tiene un límite de tamaño.

## Modelo de suscripción, permisos y elegibilidad

* Un suscriptor es un usuario que recibe notificaciones de un tablero. Una suscripción al tablero es independiente de la relación de seguimiento existente con el usuario del tablero.
* Cualquier persona que se autentique con OAuth y tenga los ámbitos `admin:read` y `admin:write` puede usar la configuración de suscripción y las API de suscriptores. `admin:read` te permite enumerar suscriptores y leer la configuración. `admin:write` te permite agregar o quitar suscriptores y cambiar la configuración.
* Puede suscribirse a cualquier usuario de Learning Manager, pero el usuario debe existir, estar activo y tener acceso al tablero para recibir notificaciones. El acceso se vuelve a comprobar cuando se envían notificaciones y resúmenes.
* Si un usuario pierde el acceso, se omitirá la entrega para ese tablero y se conservará la suscripción. La entrega se reanuda si vuelve el acceso.
* Puede añadir varios usuarios a un tablero en una sola solicitud (suscripciones en bloque). Si un usuario ya está suscrito, la solicitud se sigue realizando correctamente y no se crea ningún duplicado. Consulte [Suscripciones en bloque](api-changes-dec-2026.md#bulk-subscriptions) para ver el formato de la solicitud, la respuesta de varios estados de 2017 y los casos de error.

## Contenido de resumen

### Eventos incluidos

El resumen incluye nuevas publicaciones, comentarios y respuestas cuando la configuración coincidente es `true` en la [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-create-settings): `notifyNewPost`, `notifyComment` y `notifyReply`. Los estableció con `POST` o `PATCH /boardSubscriptionSettings`. De forma predeterminada, todas las configuraciones son `false`.

### Eventos excluidos

El resumen excluye los eventos cuya configuración coincidente en la API [`boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings) (por ejemplo, `notifyComment`) es `false`. No se envía ningún resumen cuando no hay ninguna actividad elegible.

### Diseño de correo electrónico de resumen de muestra

Se envía un correo electrónico de resumen por cada tablero suscrito que haya realizado una actividad elegible. Se estructura de la siguiente manera:

* **Línea de resumen:** El correo electrónico se abre con el número total de actualizaciones del tablero (por ejemplo, siete actualizaciones) y un desglose por tipo (por ejemplo, nuevas publicaciones y comentarios), junto con el tiempo desde el que se cuenta la actividad.
* **Sección de tablero:** La actividad se agrupa bajo el nombre del tablero. Cada publicación aparece debajo de ella.
* **Detalles del elemento:** Cada publicación, comentario o respuesta muestra el nombre y la dirección de correo electrónico del usuario que lo creó, además de un vínculo al elemento.
* **Vínculos:** Al seleccionar un vínculo, se abre la publicación, el comentario o la respuesta directamente. El destinatario debe haber iniciado sesión para que se abra el vínculo.
* **Comentarios y respuestas:** Aparecen en el mismo correo electrónico que las publicaciones, por lo que los instructores pueden ver conversaciones de seguimiento junto con nuevos temas.

## Configurar notificaciones

### Configurar opciones mediante API

Las notificaciones se administran mediante dos API públicas: la [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence), que se aplica en el nivel de cuenta, y la [API de suscriptores](api-changes-dec-2026.md#api-get-subscribers), que se aplica por placa. Ambos utilizan los ámbitos de OAuth `admin:read` y `admin:write`. Llámelos en esta secuencia:

1. Establezca la configuración de nivel de cuenta con [`POST /boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings).
1. Cambie la configuración más tarde, cuando sea necesario, con [`PATCH /boardSubscriptionSettings`](api-changes-dec-2026.md#api-update-settings).
1. Recupere la configuración de nivel de cuenta con [`GET /boardSubscriptionSettings`](api-changes-dec-2026.md#api-get-settings).
1. Enumere los usuarios suscritos a un tablero con [`GET /boards/{id}/subscribers`](api-changes-dec-2026.md#api-get-subscribers).
1. Suscribir usuarios a un tablero con [`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users).
1. Cancelar la suscripción de un usuario de un tablero con [`DELETE /boards/{id}/subscribers/{userId}`](api-changes-dec-2026.md#api-unsubscribe-user).

Use la API `boardSubscriptionSettings` para establecer la frecuencia de resumen en horas y para activar o desactivar publicaciones, comentarios y respuestas para el resumen. Por ejemplo, una cuenta con una frecuencia de resumen de 1 hora recibe un correo electrónico de resumen cada hora. De forma predeterminada, toda la configuración de eventos es `false`.

### Administrar suscriptores

Utilice la API de suscriptores para elegir a qué usuarios de Learning Manager activos se suscriben y a qué tableros. Una suscripción es independiente de la relación de seguimiento del tablero existente. Un usuario debe tener visibilidad de un tablero para recibir sus notificaciones, lo que significa que el usuario debe estar conectado. La pérdida de visibilidad suprime la entrega, pero no elimina la suscripción.

### Activar la función

Para habilitar las notificaciones del instructor, cree la configuración de nivel de cuenta y, a continuación, suscriba a los usuarios a los tableros, como se describe en [Cambios en la API en noviembre de 2026](api-changes-dec-2026.md). Después de eso, el sistema recopila las nuevas publicaciones, comentarios y respuestas creadas durante el intervalo configurado. Al final del intervalo, los suscriptores reciben una notificación resumida que cubre la actividad elegible en los tableros suscritos.

Obtén más información sobre los cambios en la API en [cambios en la API en diciembre de 2026](api-changes-dec-2026.md).
