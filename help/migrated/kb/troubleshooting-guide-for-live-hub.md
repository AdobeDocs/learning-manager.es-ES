---
title: Guía de solución de problemas para Live Hub
description: Mensajes de error comunes y notificaciones que pueden aparecer durante una sesión de Live Hub, sus causas y los pasos para resolverlas.
source-git-commit: 02de0cee632d34c99e1cba12cddb846f7e6cae81
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 2%

---


# Guía de solución de problemas de Live Hub

Durante una sesión de Live Hub, los instructores pueden recibir mensajes de error o notificaciones que impidan que determinadas acciones se completen del modo esperado. En este artículo se describen los errores comunes que afectan al instructor, sus posibles causas y los pasos que puede seguir para resolverlos.

## Problemas de conexión

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| Se ha producido un problema. Vuelva a intentarlo. | Se produce un error general de conectividad o relacionado con la sesión, por ejemplo, al unirse a una sesión o interactuar con ella y la solicitud falla debido a la inestabilidad de la red, una sesión de ALM caducada o un estado del navegador conflictivo, como varias pestañas abiertas en la misma reunión. | <ul><li>Compruebe la conexión de red y garantice un ancho de banda estable sin interferencias de VPN/proxy.</li><li>Confirme que ha iniciado sesión en ALM con una sesión válida. Cierre sesión y vuelva a iniciarla si es posible que la sesión haya caducado.</li><li>Evite unirse a la misma reunión desde varias pestañas al mismo tiempo.</li><li>Pruebe una ventana de incógnito o privada, o borre la caché del navegador si el problema persiste.</li><li>Actualice la página: la mayoría de los errores transitorios se resuelven después de una recarga; si se repite, póngase en contacto con el soporte técnico.</li></ul> |

## Problemas de la pestaña Prueba

Los mensajes siguientes pueden aparecer cuando un instructor crea o inicia una prueba y la prueba no cumple los requisitos necesarios para iniciarla.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| Escriba una pregunta para continuar. | Un instructor intenta iniciar una prueba sin introducir el texto de la pregunta. | Escriba la pregunta, proporcione las opciones de respuesta, seleccione la respuesta correcta y, a continuación, inicie la prueba para los participantes. |
| Las opciones de respuesta no se pueden dejar en blanco. | Un instructor introduce el texto de la pregunta, pero no introduce las opciones de respuesta o deja una o varias opciones de respuesta en blanco. | Escriba la pregunta, proporcione las opciones de respuesta, seleccione la respuesta correcta y, a continuación, inicie la prueba para los participantes. |
| Marque la respuesta correcta. | Un instructor introduce las opciones de pregunta y respuesta, pero no selecciona una opción de respuesta correcta. | Escriba la pregunta, proporcione las opciones de respuesta, seleccione la respuesta correcta y, a continuación, inicie la prueba para los participantes. |

## Problemas de la pestaña Sondeo

Los mensajes siguientes pueden aparecer cuando un instructor duplica, elimina o restablece una encuesta.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| No se pudo duplicar la encuesta. Vuelva a intentarlo. | Un instructor duplica una encuesta existente y el duplicado no se crea. | Cierre el panel Encuestas y cuestionarios y vuelva a intentar duplicar la encuesta. |
| No se pudieron eliminar todas las encuestas. Vuelva a intentarlo. | Un instructor elimina todas las encuestas a la vez mediante Eliminar todo y la eliminación en bloque falla o solo se completa parcialmente. | Cierre el panel Encuestas y cuestionarios y vuelva a intentar eliminar las encuestas mediante Eliminar todas las encuestas. |
| No se pudo eliminar el sondeo. Vuelva a intentarlo. | Un instructor elimina una sola encuesta y la eliminación no se completa. | Cierre el panel Encuestas y cuestionarios y vuelva a intentar eliminar la encuesta. |
| No se pudo restablecer la encuesta. Vuelva a intentarlo. | Un instructor restablece un sondeo ejecutado previamente para que pueda reutilizarse y el restablecimiento no se completa. | Cierre el panel Encuestas y cuestionarios y vuelva a intentar restablecer la encuesta. |

## Problemas de carga de contenido

El mensaje siguiente puede aparecer cuando un instructor carga un archivo de referencia que el asistente de inteligencia artificial utiliza para responder a preguntas.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| No se pudo procesar el archivo. Vuelva a intentarlo. | Un instructor carga un archivo dañado, vacío o protegido mediante contraseña que no se puede procesar. | Convierta el archivo a un formato compatible (PDF o PPT) y cárguelo de nuevo. |

## Problemas de carga de contenido en toast

Los mensajes siguientes aparecen como notificaciones en forma de brindis cuando un instructor carga un archivo de referencia que utilizará el asistente de inteligencia artificial y el archivo no supera una comprobación de validación específica.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| No se pudo procesar el archivo. Compruebe el archivo e inténtelo de nuevo. | Un instructor carga un archivo dañado. | Compruebe el formato de archivo y conviértalo a un formato compatible (PDF o PPT); a continuación, vuelva a cargarlo. |
| El archivo está protegido por contraseña. Quite la contraseña y vuelva a cargarla. | Un instructor carga un archivo protegido mediante contraseña. | Elimine la protección con contraseña del archivo y vuelva a cargarlo. |
| El archivo no tiene contenido que procesar. Cargue un archivo con contenido de texto. | Un instructor carga un archivo que no tiene contenido que procesar para el asistente de inteligencia artificial. | Cargue un archivo con contenido de texto. |
| &quot;FileName.pdf&quot; supera el límite de 1 MB. | Un instructor carga un archivo de PDF que supera el límite de tamaño de archivo de 1 MB. | Comprima o reduzca el tamaño del archivo del PDF a menos de 1 MB y vuelva a cargarlo. |
| &quot;FileName.pptx&quot; supera el límite de 3 MB. | Un instructor carga un archivo PPT que supera el límite de tamaño de archivo de 3 MB. | Comprima o reduzca el tamaño del archivo PPT a menos de 3 MB y vuelva a cargarlo. |

## Problemas de sesiones en grupo

Los mensajes siguientes pueden aparecer cuando un instructor intenta iniciar una sesión de grupo de trabajo.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| No se puede iniciar la interrupción: la conexión se interrumpe. Inténtelo de nuevo cuando se vuelva a conectar. | Un instructor intenta iniciar salas de grupo de trabajo mientras su conexión se interrumpe o se vuelve a conectar. | Espere a que se estabilice la conexión (observe un indicador de reconexión) y, a continuación, vuelva a iniciar las salas de grupo de trabajo. |
| No se pudo iniciar la separación. Vuelva a intentarlo. | Un instructor inicia las salas de grupo de trabajo y falla la solicitud para iniciarlas. | Vuelva a intentar iniciar salas de grupo de trabajo. Si persiste, cierre el panel Grupos de trabajo e inténtelo de nuevo. |
| No se pudo generar el resumen. | Esto puede ocurrir en las siguientes situaciones: <ul><li>Ningún usuario habló durante la sesión, por lo que no hay contenido de audio que resumir.</li><li>La discusión es de menos de 60 segundos.</li></ul> | Asegúrese de que los participantes hablen activamente durante al menos 60 segundos durante la sesión antes de generar el resumen. Si el problema persiste, espere un momento e inténtelo de nuevo. |

## Problemas de toast de generación de respuestas

El mensaje siguiente puede aparecer cuando un instructor solicita al asistente de inteligencia artificial que genere una respuesta a la pregunta de un participante en el chat.

| Mensaje de error | Escenario | Sugerencias para superar el error |
|---|---|---|
| Esto no se trató en la sesión. | Un alumno hace una pregunta que no se trata en la referencia de contenido cargada. Este comportamiento es normal, no un error. | Responda la pregunta manualmente. |
