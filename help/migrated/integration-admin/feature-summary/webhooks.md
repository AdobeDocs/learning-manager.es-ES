---
jcr-language: en_us
title: Webhooks
description: Obtenga más información sobre Webhooks para enviar información en tiempo real, como inscripciones en cursos, creación de cursos y otra información, a una dirección URL específica
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Webhooks

Un webhook permite a una entidad enviar automáticamente datos o notificaciones en tiempo real a otra entidad cuando se produce un evento específico. Permitirá a una aplicación proporcionar información a otras aplicaciones sin solicitarla constantemente. Por ejemplo, si un usuario completa un curso de Sistema de gestión de aprendizaje (LMS), un webhook puede enviar automáticamente esa información a otra plataforma, como CRM o herramienta de creación de informes. Los webhooks se suelen utilizar en integraciones para automatizar procesos y reducir la necesidad de actualizaciones manuales entre sistemas. Configure los webhooks proporcionando una URL de devolución de llamada a la que enviar los datos.

## Webhooks frente a API

Los webhooks y las API ayudan a los sistemas a comunicarse entre sí, pero funcionan de formas diferentes. Con las API, la información se comparte solo cuando el usuario la solicita. Por ejemplo, si un alumno requiere datos de progreso del curso, envía una solicitud a la API, que, a continuación, proporciona la información. Por otro lado, los webhooks envían datos automáticamente inmediatamente cuando se produce un evento. Por ejemplo, si un alumno completa un curso, enviará los datos inmediatamente a la dirección URL del listener sin ninguna solicitud manual.

## ¿Qué son las API en tiempo real?

Las API en tiempo real permiten a las aplicaciones intercambiar datos instantáneamente cuando se produce un evento. A diferencia de las API tradicionales, que esperan a que un usuario solicite información, las API en tiempo real comparten datos en el momento en que sucede. Los webhooks actúan como una API en tiempo real y ayudan a compartir los datos inmediatamente cada vez que se produce el evento especificado. La API en tiempo real garantiza que esta transferencia de datos se produzca inmediatamente sin necesidad de ninguna solicitud manual, lo que permite que los sistemas se mantengan actualizados al instante.

## Eventos de Webhook

Los eventos Webhook son acciones específicas que se producen en un sistema que envía automáticamente datos a una dirección URL del listener. Por ejemplo, cuando un alumno se inscribe en un curso, se activa un evento webhook que envía los detalles de inscripción a la dirección URL del listener.
Los eventos Webhook se clasifican en dos categorías:

* **Eventos en tiempo real**: los eventos se procesan y se envían en tiempo real a una dirección URL de destino
* **Eventos en tiempo no real**: los eventos se procesan en lotes y se envían a horas especificadas en lugar de en tiempo real

## URL del Listener

Una dirección URL de Listener es un extremo o destino que recibe información de datos cuando se produce un evento. Siempre que se produce un evento específico, como un usuario que se inscribe en un curso, el sistema envía automáticamente los detalles a esta dirección URL sin ninguna solicitud manual. La URL del listener es la dirección en la que se entregan todas estas actualizaciones.
Webhook envía la información relevante en formato JSON. A continuación se muestra un ejemplo de carga para un evento activado en Adobe Learning Manager:

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Crear y administrar webhooks: administrador de integración

Siga los pasos que se indican a continuación para crear la integración de Webhooks en Adobe Learning Manager:

1. Inicie sesión como **[!UICONTROL administrador de integración]**.
2. En la página principal, seleccione **[!UICONTROL Webhooks]** > **[!UICONTROL Agregar Webhook]**.

   ![](assets/create-webhook.png)
   _Agregar un webhook_

3. Escriba el **[!UICONTROL Nombre]** y la **[!UICONTROL Descripción]** del webhook.
4. Escriba la dirección URL del agente de escucha como **[!UICONTROL dirección URL de destino]** a la que desea pasar los datos del evento.
5. Seleccione cualquiera de los métodos de autenticación:
La autenticación en Webhooks es un método de seguridad para asegurarse de que los datos enviados a la dirección URL de un agente de escucha proceden de una fuente de confianza.
   * **[!UICONTROL Ninguno]**: no se requiere autenticación.
   * **[!UICONTROL Básico]**: esta es una autenticación basada en credenciales. Introduzca el nombre de usuario y la contraseña.
   * **[!UICONTROL Firma]**: el sistema crea una firma especial y la agrega a los datos de webhook. El servidor receptor comprueba este código para asegurarse de que los datos son reales y no se han modificado. Genera una firma y utilízala para la autenticación. Descargue la firma como JSON.
6. Seleccione los eventos Webhook en el menú desplegable **[!UICONTROL Eventos desencadenantes]**.

   >[!NOTE]
   >
   >También puede probar los webhooks seleccionando la opción Probar webhooks de la página Añadir webhook.

7. Seleccione el botón de alternancia **[!UICONTROL Estado de activación]** para habilitar el webhook. Una vez habilitado, los datos se pasarán siempre que se produzcan los eventos seleccionados.

>[!NOTE]
>
>Puede crear y administrar hasta 5 webhooks.

### Editar webhooks: administrador de integración

Siga estos pasos para editar webhooks desde Adobe Learning Manager:

1. Inicie sesión como **[!UICONTROL administrador de integración.]**
2. Seleccione **[!UICONTROL Webhooks]** en la página principal.
3. Seleccione el webhook que desea editar.

   ![](assets/edit-webhook.png)
   _Editar el webhook_
4. Seleccione **[!UICONTROL Editar]** para modificar los detalles del webhook y seleccione **[!UICONTROL Guardar]**.

### Eliminar webhooks: administrador de integración

Siga estos pasos para editar webhooks desde Adobe Learning Manager:

1. Inicie sesión como **[!UICONTROL administrador de integración]**.
2. Seleccione **[!UICONTROL Webhooks]** en la página principal.
3. Seleccione el webhook que desea eliminar.
4. Seleccione **[!UICONTROL Eliminar]** para quitar los webhooks.

![](assets/delete-webhooks.png)
_Quitar el webhook_

### Retirar webhooks: administrador de integración

Siga estos pasos para retirar los webhooks:

1. Inicie sesión como **[!UICONTROL administrador de integración]**.
2. Seleccione **[!UICONTROL Webhooks]** en la página principal.
3. Seleccione el webhook que desea editar.
4. Seleccione **[!UICONTROL Editar]** y deshabilite el **[!UICONTROL Estado de activación]** para retirar el webhook.

![](assets/retire-webhook.png)
_Retirar el webhook_
