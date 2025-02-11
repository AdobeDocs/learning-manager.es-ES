---
jcr-language: en_us
title: Documentación de la API de interacción de Embedded Player
description: Obtenga más información sobre las diversas API para escuchar eventos y activar acciones en el reproductor incrustado
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# Documentación de la API de interacción de Embedded Player

Adobe Learning Manager proporciona una biblioteca que se puede integrar en una aplicación. Esta biblioteca proporciona varias API para escuchar eventos y activar acciones en el reproductor incrustado.

Con las API proporcionadas, puede reproducir, pausar y realizar otras acciones en el reproductor.

## Cargar la biblioteca

La biblioteca está disponible en esta [ubicación](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js).

Para cargar la biblioteca, siga los pasos que se indican a continuación:

1. Cargue el archivo js en la aplicación de consumidor.
2. Al cargar la biblioteca, se rellenará window.cpPlayerLib.

>[!NOTE]
>
>Si no utiliza prod US, configure los parámetros cpPlayerLib.env y cpPlayerLib.sourceOrigin según su env.

Los valores predeterminados son:

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Métodos disponibles

La biblioteca cpPlayerLib consta de las siguientes funciones:

**startPlayer**

<table>
<tbody>
<tr>
<td>Nombre de método</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Descripción</td>
<td>Carga un reproductor en la aplicación.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>loId: El ID del objeto de aprendizaje.</li><li>accountId: El ID de cuenta de la cuenta de ALM.</li><li>userId: El seudónimo.</li><li>tokenDeAcceso: El token de acceso.</li><li>domRefId: El ID del contenedor div en el que se debe procesar el reproductor.</li><li>onModuleLoaded: Esta función se invocará cuando se carguen los módulos con los siguientes detalles.</li><br><li>contentType</li><li>loId</li><li>moduleId</li><li>completado</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAavailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Devoluciones</td>
<td>Devuelve una promesa. En la resolución de la promesa, se pasará un playerObj.</td>
</tr>
<tr>
<td>Excepción</td>
<td>La promesa resultará en una excepción.</td>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then((playerObj) =&gt; {//playerObj tiene las api para interactuar con el reproductor}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Descripción</td>
<td>Devuelve todos los objetos de reproductor de la página actual.</td>
</tr>
<tr>
<td>Parámetros</td>
<td>Ninguno</td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Descripción</td>
<td>Devuelve un objeto de reproductor con el ID de objeto de aprendizaje especificado.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>loId: El ID del objeto de aprendizaje.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Descripción</td>
<td>Vaya al siguiente módulo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>moduleId: el ID del módulo.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**siguiente**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>siguiente</td>
</tr>
<tr>
<td>Descripción</td>
<td>Vaya al siguiente módulo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**anterior**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>anterior</td>
</tr>
<tr>
<td>Descripción</td>
<td>Vaya al módulo anterior.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Descripción</td>
<td>Active el panel del índice en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**toggleNotes**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Descripción</td>
<td>Active el panel de notas en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Descripción</td>
<td>Active o desactive la visualización de subtítulos opcionales en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Descripción</td>
<td>Cambie el idioma del contenido en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>idioma: El código de idioma que se va a especificar.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Descripción</td>
<td>Cierre el reproductor y quítelo de la página. </td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Descripción</td>
<td>Alterne entre reproducir y pausar el contenido en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>setVolume</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ajuste el volumen del reproductor. El valor debe estar entre 0 y 1.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>volumen: El valor del volumen. El intervalo válido es 0-1. </li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Descripción</td>
<td>Establezca la velocidad de reproducción en el reproductor.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>velocidad: Valor de la velocidad que se va a especificar. Los valores válidos son .25, .5, .75, 1, 1.25, 1.5, 1.75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**seek**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>buscar</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ve a cualquier momento del vídeo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>hora: El momento para saltar. El tiempo es en segundos.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**reenviar**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>adelante</td>
</tr>
<tr>
<td>Descripción</td>
<td>Avanza 10 segundos en el vídeo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**hacia atrás**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>atrasado</td>
</tr>
<tr>
<td>Descripción</td>
<td>Retroceder 10 segundos en el vídeo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ir a la página especificada en PPT/PDF.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>pageNumber: El número de página al que saltar.</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**nextPage**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>nextPage</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ir a la página siguiente en el PPT/PDF.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**previousPage**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>previousPage</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ir a la página anterior en el PPT/PDF.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**acercar**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>acercar</td>
</tr>
<tr>
<td>Descripción</td>
<td>Aumente el contenido en un PPT/PDF.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**zoomOut**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>alejarZoom</td>
</tr>
<tr>
<td>Descripción</td>
<td>Reducir el contenido en un PPT/PDF.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Descripción</td>
<td>Descargar una ayuda de trabajo de un curso.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPlullout**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Descripción</td>
<td>Si desea o no descargar una ayuda de trabajo.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**fullScreen**

<table>
<tbody>
<tr>
<td>Nombre del método</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Descripción</td>
<td>Ajuste el reproductor al modo de pantalla completa.</td>
</tr>
<tr>
<td>Parámetros</td>
<td><li>Ninguno</li></td>
</tr>
</tr>
<tr>
<td>Código de ejemplo</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Lista de eventos

**onPlayerEvents(callBack)**

Al registrar la función de devolución de llamada se invoca en todos los eventos del reproductor. Los nombres de los eventos son los siguientes:

* REPRODUCCIÓN (Vídeo/Audio/CP)
* PAUSA (Vídeo/Audio/CP)
* ACTUALIZACIÓN DE TIEMPO (Vídeo/Audio/CP)
* CAMBIO DE PÁGINA (PPT/ PDF)
* NOTA AÑADIDA (Todo el contenido)
* LANZADO (Todo el contenido)
* INICIADO (Todo el contenido)
* COMPLETADO (Todo el contenido)
* PASADO (Todo el contenido)
* FALLIDO (Todo el contenido)

**onStreamingEvents(callBack)**

Al registrar la función de devolución de llamada se invoca en todas las declaraciones de reproductor que se envían para realizar un seguimiento de la actividad del usuario.
