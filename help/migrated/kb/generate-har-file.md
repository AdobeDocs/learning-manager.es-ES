---
description: Obtenga información sobre cómo generar archivos HAR en Google Chrome.
jcr-language: en_us
title: Genere un archivo HAR
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 65%
---
# Genere un archivo HAR

Obtenga información sobre cómo generar archivos HAR en Google Chrome.

Para generar un archivo HAR, siga estos pasos:

1. Abra una ventana de Google Chrome y abra una ficha nueva.
1. Abra las herramientas de desarrollador de la página, haga clic con el botón derecho y seleccione Inspeccionar.
1. Abra la ficha **[!UICONTROL Red]**. Asegúrese de que el botón rojo de grabación esté activo. Active la casilla de verificación **[!UICONTROL Guardar registro]**.

   ![](assets/preserve-log-checkbox.png)

   *Seleccione la casilla de verificación Conservar registro en la pestaña Red*

1. Inicie sesión en [Learning Manager](https://learningmanager.adobe.com/acapindex.html) con sus credenciales y realice el curso. Efectúe todas las operaciones que acabarán produciendo el problema.
1. En las herramientas de desarrollador, haga clic con el botón derecho y seleccione **Guardar todo como HAR con contenido**.

   En algunas versiones de Google Chrome, es posible que tengas que seleccionar **[!UICONTROL Copiar]** > **[!UICONTROL Copiar todo como HAR]**.

   ![](assets/copy-hra.png)

   *Copiar todos los archivos HAR*

1. Pegue el contenido copiado en un archivo del Bloc de notas. Guárdelo en el escritorio como **logs.har** y envíelo por correo electrónico al Adobe.
