---
jcr-language: en_us
title: No se puede publicar en el dominio de la UE de Learning Manager
description: No se puede publicar desde Adobe Captivate en el dominio de la UE de Adobe Learning Manager en Adobe Learning Manager.
contentowner: nluke
exl-id: fb8ae1af-9902-4901-8263-fb3ebff98fbc
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 83%

---

# No se puede publicar en el dominio de la UE de Learning Manager {#unable-to-publish-to-learning-manager-eu-domain}

## Problema

No se puede publicar desde Adobe Captivate en el dominio de la UE de Adobe Learning Manager.

## Error

No se ha encontrado ninguna cuenta

## Descripción

Hay situaciones en las que los autores intentan publicar un curso de Adobe Captivate en Adobe Learning Manager. Sin embargo, no pueden realizar esta acción porque aparece un mensaje de error, &quot;No se ha encontrado ninguna cuenta&quot;.

## Causa

Este problema se produce porque Adobe Captivate está configurado de forma predeterminada para publicar contenido en el dominio de EE. UU. de Adobe Learning Manager.

## Solución:

Aspectos que debe tener en cuenta:

* Si está abierta, cierre la aplicación Adobe Captivate.
* Para realizar los pasos que se indican a continuación, deberá disponer de acceso de administrador en el equipo. En caso de que no tenga acceso de administrador, póngase en contacto con su equipo de TI para obtener ayuda.

Realice los pasos siguientes:

1. Vaya al directorio de instalación de Adobe Captivate.

   Por ejemplo, `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 es la versión de Captivate). Esta varía si utiliza una versión diferente de Adobe Captivate).

1. Copie el archivo de configuración **AdobeCaptivate.ini** en el escritorio.

   ![](assets/cp-captivate.ini.png)
   *Ver el archivo de configuración*

1. Abra el archivo copiado en el escritorio en un Bloc de notas.
1. Cambie el valor de LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` a LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *Ver PrimeBaseURL*

1. Guarde los cambios realizados en el Bloc de notas.
1. Copie el archivo guardado que ha modificado y péguelo de nuevo en la ruta de archivo. Reemplazar el archivo original en `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. A continuación, inicie Adobe Captivate e intente publicar en Adobe Learning Manager.
