---
jcr-language: en_us
title: Requisitos del sistema
description: Requisitos del sistema para Adobe Learning Manager
contentowner: dvenkate
exl-id: 3bf9818a-4b86-47e9-9b86-1c32b8bfee3a
source-git-commit: f964dd3f1adeadb76f4843c9af229ce5f09afde1
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 62%

---

# Requisitos del sistema para Adobe Learning Manager

## Escritorio

### Sistema operativo

Windows 10 y 11, macOS X 10.12, 10.13, 10.14, 10.15

### Procesador

Intel® CoreTM i5 o superior.

### RAM

Se requieren 8 GB como mínimo.

### Resolución de pantalla

1366 x 768 píxeles

### Espacio en disco

5 GB como mínimo de espacio disponible en el disco duro.

### Grabación

Se requiere un micrófono para la grabación de audio y una cámara web para la grabación de vídeo.

## Aplicación móvil

### Dispositivos

* iOS: últimas dos versiones principales.
* Android: últimas dos versiones principales.

### Navegadores

* Chrome en Android.
* Safari en iOS.

### Velocidad de red

* 1 Mbps

### CPU, dispositivos de memoria (min)

* Qualcomm® Snapdragon™ 695 5G o equivalente, 6 GB de memoria

### Se requiere escáner de código QR/espacio en disco

* 250 MB

>[!NOTE]
>
>El explorador para dispositivos móviles solo admite la función de alumno en **diseño envolvente**.

>[!NOTE]
>
>La aplicación Learning Manager para dispositivos móviles solo admite la función de alumno.

## Varios

Se requiere una conexión a Internet activa y una cuenta de alumno de Adobe Learning Manager para utilizar la aplicación.

## Especificaciones del navegador

La página principal de diseño envolvente no es compatible con los navegadores IE 11.

* Google Chrome versión 43 y superior
* Versiones más recientes de Edge, Safari (versión 13 y posterior) y Firefox.
* Internet Explorer versión 11 y superior

## Tamaño recomendado de las imágenes {#recommendedsizeofimages}

* Cabecera:
   * Para configuraciones tan grandes: 1280 x 360 PX
   * Para configuraciones como medio: 1280 x 273 PX
   * Para configuraciones tan pequeñas: 1280 x 187 PX
* Imagen en la tarjeta del catálogo: 280 x 100 px
* Tamaño de la tarjeta de formación: 300 x 240 px
* Banner de redes sociales: 1600 x 240 px

## Tamaño máximo de contenido {#maximumcontentsize}

El tamaño de archivo máximo que se puede cargar es de 600 MB.

>[!NOTE]
>
>Si el tamaño del archivo *user.csv* es superior a 100 MB, importarlo puede provocar comportamientos inesperados en el navegador. Este problema se produce porque el navegador se queda sin memoria.

Se recomienda importar archivos *user.csv* de tamaño grande mediante el flujo de trabajo automatizado de Box/Exavault. Para obtener más información, consulte [Migración de archivos](/help/migrated/integration-admin/feature-summary/migration-manual.md).


## Formatos de contenido admitidos

### Carga del módulo {#moduleupload}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Tipo de contenido</b></p></td>
   <td>
    <p><b>Extensiones</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Documentos</p></td>
   <td>
    <p>"pdf", "docx", "doc", "xls", "xlsx"</p></td>
  </tr>
  <tr>
   <td>
    <p>Presentaciones de PowerPoint</p></td>
   <td>
    <p>"pptx", "ppt"</p></td>
  </tr>
  <tr>
   <td>
    <p>Vídeos</p></td>
   <td>
    <p>"mp4", "wmv", "3gp", "3g2", "3gp2", "asf", "avi", "f4v", "h264", "mpe", "mpeg", "mpg", "mpg2", "m4v", "mov", "wmv"</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 1.2</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 2004</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>CAPI</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>AICC</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>Audio</p></td>
   <td>
    <p>"mp3", "wav", "aac", "m4a", "wma", "vorbis", "pcm", "eac3", "amr", "ac3"</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p><strong>Insignias</strong></p></td>
   <td>
    <p>"png", "jpg", "jpeg", "gif"</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Imagen de perfil de usuario</strong></p></td>
   <td>
    <p>"png", "jpg", "jpeg", "gif"</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Logotipo de empresa</strong></p></td>
   <td>
    <p>"png", "jpg", "jpeg", "bmp", "gif"</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Carga de certificaciones</strong></p></td>
   <td>
    <p> "png", "jpg", "jpeg", "pdf", "doc", "docx", "gif"</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Archivos adjuntos de cursos/recursos</strong></p></td>
   <td>
    <p> Todos los formatos de archivo</p></td>
  </tr>
 </tbody>
</table>

## Especificación de altura y anchura para cargar elementos {#heightandwidthspecificationforuploadingelements}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Elementos</b></p></td>
   <td>
    <p><b>Tamaño</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Insignia en el tablero de logros del alumno</p></td>
   <td>
    <p>40x40 píxeles</p></td>
  </tr>
  <tr>
   <td>
    <p>Insignia ampliada en la aplicación del alumno</p></td>
   <td>
    <p>90x90 píxeles</p></td>
  </tr>
  <tr>
   <td>
    <p>Imagen de perfil de usuario en los logros del alumno</p></td>
   <td>
    <p>100x100 píxeles</p></td>
  </tr>
  <tr>
   <td>
    <p>Imagen de perfil de usuario en el menú desplegable de cierre de sesión</p></td>
   <td>
    <p>42x42 píxeles</p></td>
  </tr>
  <tr>
   <td>
    <p>Logotipo de empresa en el encabezado</p></td>
   <td>
    <p>45 píxeles de alto; la anchura se calcula en consecuencia.</p></td>
  </tr>
  <tr>
   <td>
    <p>Logotipo de empresa en la página de inicio de Learning Manager</p></td>
   <td>
    <p>100 píxeles de altura; la anchura se calcula en consecuencia.</p></td>
  </tr>
 </tbody>
</table>

## Accesibilidad

### Navegadores y lectores de pantalla compatibles

Se admiten las siguientes combinaciones:

* Chrome + NVDA
* Edge + Narrator
* Mac Safari + VoiceOver

### Compatibilidad con la experiencia móvil envolvente

Se admiten los siguientes:

* Android + Talkback
* iOS + VoiceOver

## Requisitos de red {#networkrequirements}

Asegúrese de que los siguientes dominios de terceros estén incluidos en la lista blanca si se encuentra en cualquier red que tenga restricciones.

* &#42;.adobe.com
* &#42;.boltdns.net
* &#42;.brightcove.com
* &#42;.amazon.com
* &#42;.adobedtm.com
* &#42;.typekit.net
* &#42;.demdex.net
* &#42;.brightcove.net
* &#42;.zencdn.net
* &#42;.cloudflare.com
* bam.nr-data.net
* &#42;.akamaihd.net


### Casos ampliados específicos {#specificextendedcases}

<table>
 <tbody>
  <tr>
   <th>Función</th>
   <th>Servicios utilizados</th>
  </tr>
  <tr>
   <td>Conector de FTP</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Migración</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Conector de Lynda</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.lynda.com/" target="_blank">www.lynda.com</a></td>
  </tr>
  <tr>
   <td>Conector de Harvard ManageMentor</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://myhbp.org" target="_blank">www.myhbp.org</a></td>
  </tr>
  <tr>
   <td>Conector de getAbstract</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.getabstract.com/en/" target="_blank">www.getabstract.com </a></td>
  </tr>
  <tr>
   <td>Conector de Box</td>
   <td>Zonas de Box ubicadas en Frankfurt</td>
  </tr>
  <tr>
   <td>Conector de Mini Orange</td>
   <td>Mini Orange</td>
  </tr>
  <tr>
   <td>Conector de Workday</td>
   <td>Workday</td>
  </tr>
  <tr>
   <td>Conector de Blue Jeans<br></td>
   <td>Blue Jeans</td>
  </tr>
  <tr>
   <td>Microsoft Power BI</td>
   <td>Licencia comercial de Power BI solo admitida.</td>
  </tr>
 </tbody>
</table>

## Resumen técnico {#technicaloverview}

[Resumen técnico de Learning Manager](assets/learning-manager-technicaloverview.pdf)

## Informe técnico sobre seguridad de ALM

[Informe técnico de ALM](assets/alm-security-whitepaper-2024.pdf)
