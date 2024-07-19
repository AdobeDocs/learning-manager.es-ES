---
jcr-language: en_us
title: Integración de Okta Active Directory con Adobe Learning Manager
description: Integración de Okta Active Directory con Adobe Learning Manager
contentowner: nluke
exl-id: 6d7711a9-7a7f-49b7-8948-9a42407463b3
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 57%

---

# Integración de Okta Active Directory con Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

En este documento, aprenderá a integrar Adobe Learning Manager con Okta Active Directory (AD). Al integrar Adobe Learning Manager con Okta AD, puede:

* Compruebe y controle el acceso de los usuarios de Learning Manager en Okta AD.
* Permita que los usuarios inicien sesión automáticamente en Adobe Learning Manager con sus cuentas de Okta AD.
* Administre sus cuentas en una ubicación central: el portal de Okta.

Adobe Learning Manager admite SSO iniciado por el proveedor de identidades (IdP) y el proveedor de servicios (SP).

## Creación de una aplicación en OKTA

1. Inicie sesión como administrador en Okta AD.
1. Haga clic en **[!UICONTROL Aplicaciones]**. Se abrirá Application Store en Okta.

   ![](assets/cp-application-store.png)

   *Ver almacén de aplicaciones en Okta*

1. Haga clic en **[!UICONTROL Crear integración de aplicaciones]**.

   ![](assets/cp-app-integrations.png)

   *Seleccione Crear integración de aplicaciones*

1. Seleccione **[!UICONTROL SAML 2.0]** en la nueva ventana de integración de aplicaciones.

   ![](assets/cp-saml2.0.png)

   *Seleccionar la opción SAML2.0*

1. Seleccione **[!UICONTROL Crear integración de SAML]** > **[!UICONTROL Página de configuración general]**. Introduzca un nombre de aplicación.

   Tenga en cuenta que puede ser cualquier nombre para identificar de forma exclusiva la aplicación. Una vez hecho esto, haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/cp-saml-integration.png)

   *Escriba el nombre de la aplicación*

1. Realice los pasos siguientes en la página Configurar SAML:

   **Para la configuración de IDP:**

   1. En el campo URL de inicio de sesión único, escriba la dirección URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. En el campo URL de audiencia, escriba la dirección URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. En el cuadro desplegable **Formato de ID de nombre**, selecciona **Dirección de correo electrónico**.
   1. En el menú desplegable **Nombre de usuario de la aplicación**, seleccione Nombre de usuario de Okta.
   1. Si desea pasar atributos adicionales, puede agregar los atributos en la **instrucción Attributes** (opcional)

   ![](assets/cp-saml-integration-step1.png)

   *Agregar atributos de SAML*

   **Para la configuración del SP:**

   1. En el campo URL de inicio de sesión único, escriba la dirección URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. En el campo URL de audiencia, escriba la dirección URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. En el cuadro desplegable Formato de ID de nombre, seleccione **Dirección de correo electrónico**.
   1. En el menú desplegable Aplicación, seleccione el nombre de usuario de Okta.
   1. Haga clic en **Mostrar opciones avanzadas**.
   1. En **Algoritmo de firma**, seleccione RSA-SHA256
   1. En el **Algoritmo de aserción**, seleccione SHA256
   1. En el cuadro desplegable **Encriptado de aserción**, seleccione **Cifrado**.

   1. En la opción **Certificado de cifrado**, cargue el archivo de certificado compartido por Adobe.
   1. Si desea pasar atributos adicionales, puede agregar los atributos en la **instrucción Attributes** (opcional).

   ![](assets/cp-saml-integration-step2.png)

   *Agregar atributos adicionales*

   Una vez hecho esto, haga clic en **[!UICONTROL Siguiente]**.

1. La ficha **Comentarios** es opcional. Una vez que haya seleccionado las opciones y haya proporcionado sus comentarios, haga clic en **[!UICONTROL Finalizar]**.

   ![](assets/cp-saml-integration-step3.png)

   *Configuración completa de SAML*

## Extraer archivo de metadatos y URL iniciado por IDP

Para ver la URL y el archivo de metadatos iniciados por IdP/SP, realice los siguientes pasos:

1. Abra la aplicación que haya creado.
1. En la ficha **Inicio de sesión único**, haga clic en **[!UICONTROL Ver instrucciones]**.

   ![](assets/cp-prime-sso.png)

   *Seleccionar ficha SSO*

   **Para IDP:**

   1. La URL de inicio de sesión único del proveedor de identidades es la URL iniciada por el IdP.
   1. Copie todo el texto que está presente en el campo **Opcional**.
   1. Abra un nuevo documento del bloc de notas y pegue el texto copiado.
   1. Haga clic en **[!UICONTROL Archivo]** > **[!UICONTROL Guardar como]** > &quot;filename.xml&quot;. Este será el archivo de metadatos.

   **Para SP:**

   1. La URL de inicio de sesión único del proveedor de identidades es la URL iniciada por el IdP.
   1. El emisor del proveedor de identidad es el ID de entidad.
   1. Copie todo el texto que está presente en el campo **Opcional**.
   1. Abra un nuevo documento del bloc de notas y pegue el texto copiado.
   1. Haga clic en **[!UICONTROL Archivo]** > **[!UICONTROL Guardar como]** > **[!UICONTROL nombre de archivo.xml]**. Este será el archivo de metadatos.

   ![](assets/cp-saml-integration-step4.png)

   *Guardar archivo XML de SP*

   Debe guardar este archivo en formato XML.

## Configuración de inicio de sesión único (SSO) de Adobe Learning Manager

Para configurar el inicio de sesión único de Adobe Learning Manager, siga los pasos que se indican en el artículo siguiente.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->
