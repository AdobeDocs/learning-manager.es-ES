---
description: Obtenga información sobre cómo generar archivos HAR en Google Chrome.
jcr-language: en_us
title: Genere un archivo HAR
contentowner: dvenkate
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 57%

---



# Genere un archivo HAR

Obtenga información sobre cómo generar archivos HAR en Google Chrome.

Para generar un archivo HAR, siga estos pasos:

1. Abra una ventana de Google Chrome y abra una ficha nueva.
1. Abra las herramientas de desarrollador de la página, haga clic con el botón derecho y seleccione Inspeccionar.
1. Abra la ficha **[!UICONTROL Red]**. Asegúrese de que el botón de registro rojo esté activo. Habilite la **[!UICONTROL Conservar registro]** .

   ![](assets/preserve-log-checkbox.png)

   *Seleccione la casilla de verificación Conservar registro en la ficha Red*

1. Inicie sesión en [Learning Manager](https://learningmanager.adobe.com/acapindex.html) con sus credenciales y realice el curso. Efectúe todas las operaciones que acabarán produciendo el problema.
1. En las herramientas de desarrollador, haga clic con el botón derecho y seleccione **Guardar todo como HAR con contenido**.

   En algunas versiones de Google Chrome, es posible que deba seleccionar **[!UICONTROL Copiar]** > **[!UICONTROL Copiar todo como HAR]**.

   ![](assets/copy-hra.png)

   *Copiar todos los archivos HAR*

1. Pegue el contenido copiado en un archivo del Bloc de notas. Guárdelo en el escritorio como **logs.har** y envíelo por correo electrónico al Adobe.
