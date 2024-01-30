---
jcr-language: en_us
title: Accesibilidad en Adobe Learning Manager
description: En este documento, se describe la compatibilidad con la accesibilidad proporcionada por el sistema de gestión de aprendizaje Learning Manager para los alumnos con discapacidad. También proporciona a los usuarios opciones de navegación y funciones de accesibilidad de la plataforma.
contentowner: saghosh
preview: true
source-git-commit: 92b3c83ec04de927f9066db6b79e8b19872d2b46
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 71%

---



# Accesibilidad en Adobe Learning Manager

En este documento, se describe la compatibilidad con la accesibilidad proporcionada por el sistema de gestión de aprendizaje Learning Manager para los alumnos con discapacidad. También proporciona a los usuarios opciones de navegación y funciones de accesibilidad de la plataforma.

Learning Manager sigue los estándares de accesibilidad WCAG 2.1 Nivel A y AA de W3C para la plataforma.

La función de alumno de Adobe Learning Manager permite a los alumnos navegar por la plataforma y aprovechar las siguientes funciones de accesibilidad clave:

* Lector de pantalla
* Teclado
* Subtítulos opcionales
* Otros

## Compatibilidad con lectores de pantalla {#supportforscreenreaders}

Adobe Learning Manager admite lectores de pantalla como NVDA, JAWS y VoiceOver en el escritorio, y Talkback y VoiceOver en dispositivos móviles. Con ellos, los alumnos pueden conseguir que el texto se lea en voz alta en la plataforma Learning Manager y desplazarse por ella.

Esta es la combinación de lector de pantalla y navegador que admitimos en el escritorio:

<table> 
 <tbody>
  <tr> 
   <td><p style="text-align: left;"><b>Sistema operativo</b></p></td> 
   <td><p style="text-align: left;"><b>Navegador</b></p></td> 
   <td><p style="text-align: left;"><b>Lector de pantalla</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Windows</p></td> 
   <td><p>Chrome</p></td> 
   <td><p>NVDA</p></td> 
  </tr> 
  <tr> 
   <td><p>Windows</p></td> 
   <td><p>Firefox</p></td> 
   <td><p>Jaws</p></td> 
  </tr> 
  <tr> 
   <td><p>macOS</p></td> 
   <td><p>Safari</p></td> 
   <td><p>VoiceOver</p></td> 
  </tr> 
  <tr> 
   <td><p>Android</p></td> 
   <td><p>Chrome</p></td> 
   <td><p>Talkback</p></td> 
  </tr> 
  <tr> 
   <td><p>iOS</p></td> 
   <td><p>Safari</p></td> 
   <td><p>VoiceOver</p></td> 
  </tr> 
 </tbody>
</table>

## Compatibilidad con la navegación mediante teclado {#supportforkeyboardnavigation}

Los alumnos pueden utilizar teclas estándar para navegar por las páginas con o sin lector de pantalla. De este modo, los alumnos pueden navegar por los elementos de la página y leer el contenido con un lector de pantalla.

Además, Learning Manager admite los siguientes métodos abreviados de teclado:

<table> 
 <tbody>
  <tr> 
   <td><p><b>Función</b></p></td> 
   <td><p><b>Windows</b></p></td> 
   <td><p><b>macOS</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Omitir navegación</p></td> 
   <td><p>Alt + 1</p></td> 
   <td><p>Opción+1</p></td> 
  </tr> 
  <tr> 
   <td><p>Función<br></p></td> 
   <td><p>Windows<br></p></td> 
   <td><p>macOS<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Notificación del usuario<br></p></td> 
   <td><p>Alt + 2<br></p></td> 
   <td><p>Opción+2<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Configuración de perfil<br></p></td> 
   <td><p>Alt + 3<br></p></td> 
   <td><p>Opción+3<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Búsqueda global<br></p></td> 
   <td><p>Alt + 4<br></p></td> 
   <td><p>Opción+4<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Omitir navegación<br></p></td> 
   <td><p>Alt + 1<br></p></td> 
   <td><p>Opción+1<br></p></td> 
  </tr> 
 </tbody>
</table>

## Controles del reproductor

<table> 
 <tbody>
  <tr> 
   <td><p><b>Función</b></p></td> 
   <td><p><b>Windows</b></p></td> 
   <td><p><b>macOS</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Reproducir/pausa</p></td> 
   <td><p>Alt+P</p></td> 
   <td><p>Opción+P</p></td> 
  </tr> 
  <tr> 
   <td><p>Alt + V</p></td> 
   <td><p>Opción+V</p></td> 
   <td><p>Volumen</p></td> 
  </tr> 
  <tr> 
   <td><p>Alt + M</p></td> 
   <td><p>Opción+M</p></td> 
   <td><p>Pantalla completa</p></td> 
  </tr> 
 </tbody>
</table>

## Compatibilidad con otras funciones {#supportforcolorcontrast}

La función de alumno de Learning Manager admite otras funciones de accesibilidad, entre las que se incluyen:

1. Se proporciona una estructura semántica para las páginas de la función de alumno, incluidos el encabezado, el marcado de lista, los títulos descriptivos, etc.
1. La compatibilidad con el zoom del navegador de hasta un 200 % sin pérdida de contenido ni funcionalidad se mantiene durante toda la función de alumno.
1. El contraste de color para elementos de texto y otros se mantiene en la función de alumno. Para obtener una mejor experiencia, utilice el tema [intenso](/help/migrated/administrators/feature-summary/themes.md).
1. Compatibilidad con los patrones de diseño WAI ARIA de W3C para mantener la coherencia y las prácticas recomendadas del sector.

Para obtener más información, consulte:

* [Informe de conformidad de accesibilidad para un alumno](https://www.adobe.com/accessibility/compliance/adobe-captivate-prime-web-2019-learner-portal-acr.html)
* [Informe de conformidad de accesibilidad para todas las funciones](https://www.adobe.com/accessibility/compliance/adobe-captivate-prime-web-2019-acr.html)

## Flujos de trabajo principales de Learning Manager (función Alumno) {#captivateprimetopworkflowslearnerrole}

Veamos cómo las funciones de accesibilidad le ayudan a navegar por algunas funciones clave para los alumnos en Learning Manager.

Utilice la `kbd Tab`para desplazarse por los elementos de la página. Utilice la `kbd Shift + Tab` para invertir la dirección de navegación. La selección del teclado se indica mediante un contorno azul que se muestra alrededor de un elemento. Un lector de pantalla debe leer en voz alta el texto del elemento que está resaltado.

## Buscar un curso de formación en Learning Manager {#searchforatrainingincaptivateprime}

1. Use estas indicaciones para navegar y acceder al cuadro Buscar en la esquina superior derecha de la página de inicio.
1. Escriba texto con el teclado. Aparecerán los resultados de la búsqueda.
1. Utilizar el teclado `kbd Up/Down` para navegar por los resultados o pulsar `kbd ENTER`para ver todos los resultados.

1. Una vez identificado el entrenamiento, presione `kbd ENTER`para acceder a la página de formación.

## Consumir formación en Adobe Learning Manager {#consumeatraininginadobecaptivateprime}

1. Una vez que se identifica un curso de formación, utilice `kbd Tab`o `kbd Shift + Tab` para ir al botón Inscribirme/Iniciar. El estado del botón depende del estado de inscripción de esa formación.

1. Golpe `kbd ENTER`para comenzar el entrenamiento.
1. A continuación se indican los controles que aparecen independientemente del tipo de contenido:

   * Índice
   * Notas
   * Botón Reproducir/Pausa
   * Pantalla completa
   * Botón Cerrar
   * Configuración
   * Etiqueta de nombre del módulo

1. A continuación se indican los controles que aparecen según el tipo de contenido:

   * Contenido de VÍDEO: controles de avance, retroceso y regulador.
   * Contenido de documento: número de página, retroceder página, avanzar página, acercar, alejar.
   * Aprendizaje electrónico: botón Subtítulos opcionales.

1. Pulsar los controles del teclado `kbd Tab`o `kbd Shift + Tab` para navegar por los controles y pulsar `kbd ENTER`para habilitar o deshabilitar cualquier control.

1. Para tipo de documento, utilice los controles de flecha como `kbd UP/DOWN` para desplazarse por el documento.

## Compatibilidad con la accesibilidad para necesidades concretas

Veamos las funciones de accesibilidad que los alumnos pueden utilizar según sus necesidades específicas.

### Usuarios sordos o con problemas de audición

* Use subtítulos opcionales disponibles en el contenido creado con la herramienta de creación de Adobe Captivate.
* En los vídeos, los autores pueden codificarlos con texto de subtítulos. Dichos vídeos tienen subtítulos opcionales incrustados que los alumnos pueden utilizar.
* Learning Manager permite cargar archivos WebVTT de subtítulos opcionales para contenido de vídeo. Para obtener más información, consulte  [*Cargar archivo WebVTT de subtítulos opcionales*](/help/migrated/authors/feature-summary/content-library.md).

### Usuarios ciegos o con visión reducida

* Utilice los métodos abreviados de teclado y los comandos estándar para desplazarse por la página.
* Uso de lectores de pantalla como los mencionados anteriormente para leer en voz alta la información de la página web.
* Uso de lupas de pantalla para ampliar la pantalla y mejorar la legibilidad, además de aumentar la vista del navegador al 200 % para leer el contenido.

### Usuarios que tienen dificultades con los colores

La función Alumno de Adobe Learning Manager procura dotar a los usuarios de una interfaz clara y legible que se ajusta a los estándares WCAG 2.1.

Para obtener una mejor experiencia en la página del alumno, utilice el [tema intenso](/help/migrated/administrators/feature-summary/themes.md).

### Usuarios con movilidad y alcance limitados

Adobe Learning Manager considera prioritaria la accesibilidad. Tiene previsto mejorar las prestaciones actuales para que los alumnos naveguen mejor por el sistema.

### Compatibilidad con subtítulos opcionales en vídeos

Al crear un curso, los autores pueden cargar archivos webVTT junto con los archivos de vídeo. A continuación, los alumnos pueden ver los subtítulos opcionales durante la reproducción de los vídeos.

## Aspectos que se tendrán en cuenta en una versión futura {#whatwillbeaddressedinafuturerelease}

* Compatibilidad con subtítulos opcionales en vídeos. Los autores deberán tener la capacidad de cargar archivos SRT con los archivos de vídeo. Los alumnos deberán poder ver subtítulos opcionales para vídeos.
