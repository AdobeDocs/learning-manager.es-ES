---
description: Obtenga información sobre cómo cancelar y reactivar las sesiones ILT y VILT en Adobe Learning Manager configurando el estado de la sesión en los datos de migración de Workfront
jcr-language: en_us
title: Cancelación de ALM Workfront
exl-id: 01500cf2-6e39-4ac3-84e2-823a5215f6cf
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '2112'
ht-degree: 1%
---

# Activador de cancelación/actualización de ALM-Workfront

## Información general

Adobe Learning Manager (Learning Manager) ahora puede cancelar y reactivar las sesiones con instructor y las sesiones con instructor virtual (ILT/VILT) en función de los cambios realizados en Workfront. Si su organización programa sesiones en Workfront y las introduce en Learning Manager mediante la migración de Workfront a Learning Manager, puede establecer el estado de cada sesión en Activo o Cancelado en los datos de migración. A continuación, Learning Manager aplica el cambio como si un administrador hubiera cancelado la sesión en la interfaz de usuario.

Cancelar una sesión mediante la migración se comporta del mismo modo que cancelarla desde la interfaz de usuario de Learning Manager. La única diferencia es la reactivación, que se describe en [Reactivar una sesión cancelada](#reactivate-a-cancelled-session).

### El requisito

Las actualizaciones de una sesión, como la fecha y la hora, el instructor, la ubicación o el vínculo, y la capacidad, ya se transmiten de Workfront a Learning Manager a través de la migración. Las cancelaciones no lo hicieron. Cuando se cancelaba una sesión en Workfront, Learning Manager no tenía forma de saberlo, lo que provocaba los problemas siguientes:

* Los alumnos permanecían inscritos en una sesión que ya no se ejecutaba, lo que provocaba confusión y la imposibilidad de presentarse.
* Los administradores tuvieron que repetir la cancelación manualmente en Learning Manager.
* Workfront y Learning Manager dejaron de estar sincronizados, lo que debilitó a Workfront como fuente de confianza para la programación.

### Cómo funciona

1. Un administrador de entregas cancela una sesión en Workfront.
1. La fila de sesión de los datos de migración incluye la nueva columna de estado de sesión, establecida en Cancelado.
1. Un administrador de sistemas ejecuta la migración a través de la API.
1. Learning Manager marca la sesión coincidente como cancelada y envía las mismas notificaciones que envía una cancelación desde la interfaz de usuario.

>[!NOTE]
>
>Esta función amplía el proceso de migración existente en lugar de añadir una segunda ruta de integración en tiempo real.

### Flujo de trabajo integral

El siguiente diagrama muestra cómo se mueve una fila de sesión de Workfront a Learning Manager.

![Diagrama de flujo que muestra una fila de sesión de Workfront en proceso de migración para crear, actualizar o cancelar la sesión coincidente](assets/alm-workfront-cancellation-visual1.png "Flujo de trabajo de estado de sesión de Workfront a Learning Manager")

## Casos de uso

Las siguientes funciones están implicadas en una cancelación que comienza en Workfront.

### Funciones implicadas

| Función | Descripción |
|---|---|
| Administrador de entregas | Programa y gestiona el calendario de formación en Workfront, incluida la cancelación de sesiones. Los responsables de entrega no utilizan la interfaz de usuario de Learning Manager. La migración es la única ruta por la que su cancelación llega a Learning Manager. |
| Administrador de sistemas | Ejecuta la migración mediante la API. Esta función gestiona la canalización de Workfront a Learning Manager y es independiente del administrador de entregas y del administrador de Learning Manager. |
| Administrador | Administra los datos de cursos y sesiones en la interfaz de usuario de Learning Manager. Los administradores ya no tienen que cancelar las sesiones manualmente después de que se les informe de un cambio en Workfront. |
| Autor | Es el propietario del curso y del contenido de la sesión en la interfaz de usuario de Learning Manager. |
| El instructor | Se asigna a las sesiones. Los instructores ven el estado de sesión correcto y reciben una notificación cuando se cancela una sesión que instruyen. |
| Administración | Se inscribe en una sesión mediante Learning Manager. Se informa a los alumnos de inmediato cuando se cancela su sesión. |

### Escenarios comunes

| Escenario | Lo que haces | Resultado |
|---|---|---|
| Una sesión se cancela en Workfront, por ejemplo porque un recurso no está disponible o un proveedor tiene un problema. | Establezca el estado de la sesión en Cancelado en la fila de migración de la sesión y ejecute la migración. | La sesión se cancela en Learning Manager y se notifica a las personas afectadas. |
| Los detalles de una sesión activa cambian en Workfront. | Incluya los valores modificados en la fila de migración. Establezca el estado de la sesión en Activo o déjelo en blanco. | La sesión se actualiza. Learning Manager envía un correo electrónico actualizado por la sesión. |
| Una sesión cancelada se restablece en Workfront. | Establezca el estado de la sesión en Activo en la fila de migración y ejecute la migración. | La sesión se activa y se puede modificar y cancelar de nuevo. |
| Los detalles actualizados se envían para una sesión cancelada sin establecer el estado en Activo. | No se requiere ninguna acción por parte del usuario. | La sesión permanece cancelada, la fila devuelve un error de validación y no se cambia ningún detalle. |
| Una fila de migración no incluye un estado de sesión. | Deje la columna en blanco u omítala. | El estado actual de la sesión en Learning Manager no se modifica. |

## Funciones principales

* **Columna de estado de sesión.** El esquema de migración incluye un campo de estado de sesión opcional que admite Activo y Cancelado.
* **Cancelación mediante migración.** Cuando una fila tiene el estado Cancelado, se cancela la sesión coincidente en Learning Manager. Learning Manager utiliza la misma clave coincidente que la migración ya utiliza para crear y actualizar sesiones.
* **No hay trabajo manual en Learning Manager.** Los administradores no necesitan cancelar la sesión de nuevo en la interfaz de usuario.
* **El mismo comportamiento que cancelar en la interfaz de usuario.** La gestión de inscripciones, la visibilidad de cara al alumno, los informes, el seguimiento de auditoría y las notificaciones coinciden con una cancelación desde la interfaz de usuario.
* **Reactivación.** Puede volver a establecer una sesión cancelada en Activa estableciendo el estado explícitamente en los datos de migración.
* **Protección para sesiones canceladas.** La migración no cambia los detalles de una sesión cancelada a menos que la fila establezca explícitamente el estado en Activo.
* **Compatibilidad con versiones anteriores.** La columna de estado es opcional, por lo que los archivos de migración existentes siguen funcionando sin cambios.
* **Notificaciones completas.** Los alumnos, instructores, administradores, autores y responsables reciben los mismos mensajes de correo electrónico de cancelación que reciben para una cancelación desde la interfaz de usuario.

## Estados de sesión

Cada sesión de Learning Manager se encuentra en uno de los dos estados.

| Estado | Significado |
|---|---|
| Activo | El estado predeterminado. La sesión está en directo y los alumnos pueden inscribirse y asistir. |
| Cancelado | La sesión se cancela. Se notifica a los alumnos, administradores, autores y responsables inscritos, así como a los alumnos y responsables de la cancelación desde la interfaz de usuario. |

### Normas de transición de los Estados para la migración

En la tabla siguiente se muestra lo que sucede cuando se procesa una fila de migración. Learning Manager identifica la sesión mediante la clave coincidente que la migración ya utiliza para crear y actualizar.

| Estado actual de Learning Manager | Estado de la sesión en la fila de migración | Resultado |
|---|---|---|
| La sesión no existe | Activo o en blanco | La sesión se crea como activa. |
| Activo | Activo o en blanco | La sesión permanece activa. Se aplican los valores modificados de la fila. |
| Activo | Cancelado | La sesión se cancela y se envían notificaciones. |
| Cancelado | Cancelado | Se omitirá la fila. Una sesión cancelada no se puede volver a cancelar. |
| Cancelado | Activo | La sesión se reactivará. Se aplican los valores modificados de la fila. |
| Cancelado | En blanco | La sesión permanece cancelada. Si la fila ha cambiado los valores, se devuelve un error de validación y no se cambia ningún detalle. |

### Reglas para la columna de estado de sesión

* La columna es opcional en todas las filas.
* Cuando la columna esté vacía, la sesión se actualizará a Activa.
* Una sesión se vuelve a activar a través de la migración solo cuando la columna indica explícitamente Activo.

Utilice uno de los siguientes valores en la columna de estado de sesión:

* `state = Active`
* `state = Cancelled`

>[!NOTE]
>
>Se confirman el encabezado de columna exacto y los valores aceptados. Utilice los nombres que especifique en la documentación de migración.

## Actualizaciones de las sesiones canceladas

No puede actualizar los detalles de una sesión cancelada mediante la migración. Si una fila de una sesión cancelada contiene valores modificados y no establece el estado en Activo, Learning Manager devuelve un error de validación, deja la sesión cancelada y no aplica ni almacena los detalles modificados. Learning Manager no envía un correo electrónico actualizado por la sesión para el intento.

### Cancelar una sesión mediante la migración

Utilice este procedimiento cuando se haya cancelado una sesión en Workfront y desee que Learning Manager refleje el cambio.

**Antes de comenzar**

* La sesión ya existe en Learning Manager, y se ha importado mediante la migración de Workfront a Learning Manager.
* Conozca la clave coincidente que utiliza la migración para identificar la sesión.

1. En **Workfront**, cancele la sesión.
1. En el archivo CSV de sesión que utilice para la migración, busque la fila de la sesión. Asegúrese de que la clave coincidente es la misma que la utilizada cuando se creó la sesión.
1. En la columna de estado de sesión, escriba **Cancelado**.
1. Ejecute la migración a través de la API.
1. En Learning Manager, compruebe que la sesión se ha cancelado.

Learning Manager marca la sesión como cancelada, gestiona a los alumnos inscritos del mismo modo que lo hace para una cancelación desde la interfaz de usuario y envía las notificaciones de cancelación. No se requiere ninguna acción en la interfaz de usuario de Learning Manager.

>[!NOTE]
>
>Si la sesión ya se ha cancelado, Learning Manager omite la fila.

### Actualizar una sesión activa

Para una sesión activa, el comportamiento de actualización de migración existente sigue estando disponible. Establezca el estado de la sesión en Activo o déjelo en blanco e incluya los valores modificados en la fila. Puede seguir actualizando detalles como la fecha y la hora, el instructor, la ubicación o el vínculo, y la capacidad a través de la canalización de migración.

Activo mantiene el comportamiento existente de creación y actualización. Cancelado invoca la misma cancelación de sesión que proporciona la interfaz de usuario, mediante la migración de CSV de sesión.

### Reactivar una sesión cancelada

Una sesión cancelada vuelve al estado activo sólo cuando se establece el estado en Activo explícitamente. Puede reactivar una sesión mediante la migración o editándola en la interfaz de usuario.

1. En el archivo CSV de sesión, busque la fila de la sesión cancelada. Asegúrese de que la clave coincidente es la misma que la utilizada cuando se creó la sesión.
1. En la columna Estado de la sesión, introduzca Activo.
1. (Opcional) Actualice cualquier otro valor de la fila que desee cambiar, como la fecha y la hora, el instructor, la ubicación o el vínculo, o la capacidad.
1. Ejecute la migración a través de la API.

La sesión se activa y sus detalles se pueden modificar. Una sesión que se reactiva a través de la migración o de la interfaz de usuario se puede cancelar de nuevo a través de cualquiera de las rutas.

>[!IMPORTANT]
>
>Si envía detalles de sesión actualizados para una sesión cancelada sin establecer el estado en Activo, la sesión permanece cancelada y la fila devuelve un error de validación.

## Notificaciones

Learning Manager envía todos los correos electrónicos que envía para una cancelación desde la interfaz de usuario cuando se cancela una sesión mediante migración. La cobertura de los destinatarios no se reduce y el contenido utiliza la misma plantilla, por lo que los destinatarios no pueden saber cómo se inició la cancelación.

Los destinatarios, según corresponda a la sesión, son los siguientes.

| Destinatario | Notificación |
|---|---|
| Alumnos | Se informa a los alumnos inscritos en la sesión de que la sesión se ha cancelado. |
| Instructores | Se notifica la cancelación a los instructores asignados a la sesión. |
| Responsables | Los responsables reciben la notificación de cancelación. |

### Correos electrónicos para sesiones canceladas

Una sesión cancelada no genera correos electrónicos actualizados por la sesión. Mientras se cancela una sesión, los cambios en la fecha y la hora, el instructor, la ubicación o el vínculo, así como la capacidad, no activan el correo electrónico actualizado de la sesión. Solo las notificaciones de cancelación y reactivación se aplican a una sesión cancelada.

## Consideraciones y limitaciones

* Dado que la función utiliza la migración, una cancelación realizada en Workfront llega a Learning Manager cuando se ejecuta la migración. No se admite la cancelación en tiempo real basada en webhook.
* La migración no puede cambiar los detalles de una sesión cancelada. Para cambiarlos, primero establezca el estado en Activo.
* La columna de estado de sesión es opcional. Las filas que lo omiten nunca cambian el estado de una sesión.
* La función amplía la integración de migración existente. No añade una segunda ruta de integración en tiempo real.
* La programación o el activador de la migración dependen de las herramientas que utilice su organización para ejecutarla. Esta guía no define una programación fija.
* Los gestores de entrega solo funcionan en Workfront. No necesitan acceder a la interfaz de usuario de Learning Manager para cancelar una sesión.

## Medidas de éxito

| Medida | Target |
|---|---|
| Cancelaciones que los administradores o el servicio de atención al cliente replican manualmente | Se ha reducido a 0 en un ciclo de lanzamiento completo después del inicio. |
| Cancelaciones de Workfront reflejadas en Learning Manager | 100 % de los eventos de cancelación procesados en un ciclo de migración. |
| Paridad de notificación entre la interfaz de usuario y las cancelaciones de migración | 0 brechas en la cobertura de destinatarios (administradores, autores, responsables y alumnos) y 0 correos electrónicos de actualización innecesarios para las sesiones canceladas. |

## Resolución de problemas

| Problema | Causa prevista o posible | Acción |
|---|---|---|
| Una sesión permanece activa después de cancelarse en Workfront. | La migración aún no ha procesado la cancelación o la fila de migración no tiene el estado Cancelado explícito. | Compruebe la entrada de migración y el resultado del procesamiento. |
| Los detalles de una sesión cancelada no cambian. | El comportamiento esperado mientras la sesión permanece cancelada. | Reactive la sesión estableciendo el estado en Activo y, a continuación, aplique los cambios. |
| No se envía ningún correo electrónico actualizado de la sesión para una sesión cancelada. | Comportamiento esperado. Los correos electrónicos de actualización ordinarios se suprimen para las sesiones canceladas. | Utilice el ciclo de vida de cancelación y reactivación en lugar de una actualización solo de detalles. |
| Se omitirá una fila de cancelación. | La sesión coincidente en Learning Manager ya se ha cancelado. | No es necesaria ninguna otra cancelación. Reactive la sesión primero si debe volver a estar activa. |
| Un destinatario recibió el mismo correo electrónico de cancelación que para una cancelación de la interfaz de usuario. | Comportamiento esperado. La cancelación de la migración está diseñada para coincidir con la interfaz de usuario. | No se requiere ninguna acción. |
| El comportamiento no está claro cuando el estado de la sesión está en blanco. | Los requisitos de origen entran en conflicto con el control de estado en blanco. | Confirme el comportamiento de liberación antes de utilizar un estado en blanco para cualquier transición. |
