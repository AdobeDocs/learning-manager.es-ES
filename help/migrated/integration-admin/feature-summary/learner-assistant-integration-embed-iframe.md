---
description: Aprenda a incrustar el Asistente del alumno en la aplicación mediante un iframe, incluidos la configuración y el control de eventos
jcr-language: en_us
title: Integrar el asistente del alumno incrustando iFrame
source-git-commit: 1549a4592b7a930631dcff6b2e75ec3a3d4f5592
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

---


# Incrustación del Asistente del alumno mediante un iframe

## Información general

Los usuarios de Adobe Learning Manager (ALM) pueden incrustar **Learner Assistant** directamente en sus propias aplicaciones orientadas al alumno (por ejemplo, portales personalizados, interfaces de usuario de LMS, centros de aprendizaje, etc.) usando un HTML estándar `<iframe>`.

Cuando se incrusta mediante iFrame, el Asistente del alumno proporciona acceso a todas las funciones del Asistente del alumno, entre las que se incluyen:

* Orchestrator
* Agente de respuesta
* Agente de conocimientos
* Agente de rutas de aprendizaje

>[!IMPORTANT]
>
>La incrustación de iFrame proporciona a la aplicación acceso completo a los agentes subyacentes del Asistente del alumno. Sin embargo, su aplicación (la &quot;aplicación principal&quot;) es responsable de controlar los eventos que el asistente emite. Por ejemplo, cuando un alumno hace clic en una cita o en un vínculo de curso dentro de la respuesta del asistente, este emite un evento y la aplicación principal debe controlar dicho evento y realizar la exploración real. El Asistente del alumno no puede navegar en nombre de la aplicación.

## Requisitos previos

Antes de comenzar, asegúrese de que tiene:

* Un inquilino de ALM con el Asistente del alumno activado. Configure los catálogos requeridos desde la página de configuración del administrador.
* Un token de acceso válido para autenticar la sesión del alumno (o administrador). Para generar un token de acceso, siga las instrucciones de la página [Autenticación mediante OAuth 2.0](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20) . La página incluye los pasos necesarios para autenticar y generar el token de acceso necesario para continuar.
* La capacidad de incrustar un `<iframe>` en la aplicación y comunicarse con él a través de la API postMessage del explorador.
* Propiedad de código front-end de la aplicación principal, ya que la aplicación debe escuchar y responder a los mensajes del iFrame incrustado.

## Parámetros de configuración del Asistente de aprendizaje

| Nombre del parámetro | Valor | Descripción |
|---|---|---|
| nombreDeHost | learningmanager.adobe.com | Especifica el dominio host de la aplicación. |
| tokenDeAcceso | token123 (token de acceso real) | Token utilizado para autenticar y autorizar la sesión del usuario. |

## Inicializar iFrame

Pase la configuración al Asistente del alumno mediante la API postMessage, utilizando un enlace de configuración de iFrame incrustado.

1. La aplicación principal incrusta el Asistente de aprendizaje como `<iframe>`.
2. Si no se encuentra ninguna configuración basada en URL, el Asistente de aprendizaje envía un evento ALM_CHAT_REQUEST_CONFIG a la aplicación principal.
3. La aplicación principal responde con un evento ALM_CHAT_CONFIG que contiene la carga de configuración. Por ejemplo:

   ```json
   {
     "hostName": "learningmanager.adobe.com",
     "accessToken": "token123",
     "openByDefault": false,
     "isAdmin": false
   }
   ```

4. Una vez finalizada la inicialización, el Asistente del alumno se procesa y está listo para utilizarse.

## Resumen de eventos de iFrame

El Asistente del alumno y la aplicación principal se comunican mediante eventos postMessage en ambas direcciones.

### Eventos salientes (del iFrame del Asistente del alumno a la aplicación principal)

| Nombre del evento | Descripción | Parámetros pasados |
|---|---|---|
| ALM_CHAT_OPENED | Se activa cuando se abre el chat. | -- |
| ALM_CHAT_CLOSED | Se activa cuando se cierra el chat. | -- |
| ALM_CHAT_LO_REDIRECT | Acceda a la página de resumen personalizada de la ruta de aprendizaje. | loId, loType, instanceId |
| ALM_CHAT_URL_REDIRECT | Se activa cuando se hace clic en un vínculo externo en el mensaje de chat. | url |
| ALM_CHAT_REQUEST_CONFIG | Solicita la configuración de la aplicación principal. | -- |
| ALM_CHAT_WAITING_FOR_REPLY | Indica que el asistente está procesando una solicitud o esperando una respuesta. | isWaitingForReply |
| ALM_CHAT_PERSONALIZED_PATH_CREATED | Se activa al guardar una ruta de aprendizaje. | -- |

### Eventos entrantes (de la aplicación principal al alumno)

| Nombre del evento | Descripción | Carga útil |
|---|---|---|
| ALM_CHAT_CONFIG | Envía la carga útil de configuración necesaria para inicializar el asistente. | Objeto Configuration |
| ALM_CHAT_OPEN | Abre el Asistente del alumno. | Ninguno |
| ALM_CHAT_CLOSE | Cierra el Asistente del alumno. | Ninguno |
| ASK_AI_ASSISTANT_QUERY | Abre la ventana de chat y envía una consulta al asistente. | { query: &quot;Texto de la pregunta&quot; } |

## Requisitos de control de eventos en la aplicación principal

La incorporación del asistente del alumno a través de iFrame no lo convierte en un widget totalmente autónomo. La aplicación principal debe escuchar activamente los eventos salientes y realizar las acciones adecuadas. Como mínimo, la aplicación debe:

* Escuche ALM_CHAT_REQUEST_CONFIG y responda con ALM_CHAT_CONFIG para que el asistente pueda inicializarse.
* Control ALM_CHAT_LO_REDIRECT: cuando un alumno hace clic en una cita o fuente en la respuesta del asistente, su aplicación recibe los valores loId, loType e instanceId, y es responsable de navegar al alumno hasta el curso u objeto de aprendizaje correcto.
* Control ALM_CHAT_URL_REDIRECT: cuando un alumno hace clic en un vínculo externo de un mensaje de chat, su aplicación recibe la url y es responsable de abrirla o de desplazarse a ella (por ejemplo, en una nueva pestaña).
* Si lo desea, puede realizar un seguimiento de ALM_CHAT_OPENED / ALM_CHAT_CLOSED / ALM_CHAT_WAITING_FOR_REPLY para reflejar el estado del asistente en su propia interfaz de usuario (por ejemplo, mostrar un indicador de carga mientras isWaitingForReply es true).
* Si lo desea, utilice ALM_CHAT_OPEN / ALM_CHAT_CLOSE / ASK_AI_ASSISTANT_QUERY para controlar el asistente mediante programación. Por ejemplo, abrir el asistente y rellenar previamente una consulta desde un botón **Ayuda** en cualquier parte de la aplicación.

## ¿Necesita ayuda?

Póngase en contacto con su responsable de éxito de clientes de Adobe para configurar un tutorial técnico.
