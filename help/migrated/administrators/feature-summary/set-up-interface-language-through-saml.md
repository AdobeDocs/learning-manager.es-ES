---
description: Aprenda a configurar el idioma de la interfaz con SAML
jcr-language: en_us
title: Configurar el idioma de la interfaz mediante SAML
contentowner: chandrum
exl-id: 726cb45e-1c37-42b1-924a-565c84c82852
source-git-commit: 7b84a4565ccf109ed4789f4963d6e250f5d0a852
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Configurar el idioma de la interfaz mediante SAML

Adobe Learning Manager (ALM) ahora acepta un atributo SAML para el idioma. A continuación, este atributo se asigna a la interfaz del usuario y a la configuración de idioma de contenido, lo que garantiza una interacción fluida con el LMS en el idioma que prefiera. La configuración de estas opciones de idioma se administra a través de la plataforma de administración de identidades y accesos (IAM), utilizando SAML para inicio de sesión único (SSO). Esto admite inicios de sesión iniciados por el proveedor de servicios (SP) e iniciados por el proveedor de identidades (IdP), lo que permite a los usuarios ver la interfaz y el contenido en el idioma elegido. El flujo de trabajo es el siguiente:

1. Crear una aplicación en Okta
2. Añadir un usuario en Okta
3. Configurar SSO en ALM

## Crear una aplicación en Okta

Para crear una aplicación en Okta, siga estos pasos:

1. Cree una cuenta de desarrollador en Okta utilizando el correo electrónico de su empresa e inicie sesión en su cuenta.
2. Seleccione **[!UICONTROL Aplicaciones]** > **[!UICONTROL Crear integración de aplicaciones]**.
3. Seleccione **[!UICONTROL SAML 2.0]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.
4. Escriba un nombre para la aplicación y seleccione Siguiente.
5. Configure los siguientes campos:

   * **[!UICONTROL URL de inicio de sesión único]**: escriba la dirección URL del dominio específico al que desea vincular la aplicación (por ejemplo, [https://learningmanagerstage.adobe.com/saml/SSO](https://learningmanagerstage.adobe.com/saml/SSO)). Cambie la URL del entorno si es necesario.
   * **[!UICONTROL URI de audiencia (ID de entidad de SP)]**: usa la misma URL de entorno que la anterior.
   * **[!UICONTROL Formato de Id. de nombre]**: seleccione la dirección de correo electrónico.
   * **[!UICONTROL Nombre de usuario de la aplicación]**: seleccione el nombre de usuario de Okta.

6. En Sentencias de atributo, agregue lo siguiente (o campos adicionales según sea necesario):
   * **Nombre**: configuración regional
   * **Formato De Nombre**: No Definido
   * **Valor**: user.locale

7. Seleccione Siguiente y, a continuación, Finalizar.
8. Una vez hecho esto, desplácese hacia abajo hasta Certificados de firma de SAML:

   * Busque la fila cuyo estado sea **[!UICONTROL Activo]**.
   * Seleccione **[!UICONTROL Acciones]** > **[!UICONTROL Ver metadatos de IdP]**.
   * Esto abrirá un archivo XML en una nueva pestaña. Copie el código XML y guárdelo como archivo .xml localmente.

## Añadir un usuario en Okta

Para crear un usuario en Okta, siga estos pasos:

1. Seleccione **[!UICONTROL Directorio]** > **[!UICONTROL Personas]** y, a continuación, seleccione **[!UICONTROL Agregar persona]**.
2. Escriba los detalles necesarios para el usuario y seleccione **[!UICONTROL Guardar]**.
3. Busque y seleccione el nombre del usuario nuevo.
4. Seleccione **[!UICONTROL Asignar aplicación]**.
5. Seleccione la aplicación que creó anteriormente y, a continuación, seleccione **[!UICONTROL Guardar]**.
6. Vaya al perfil del usuario y seleccione **[!UICONTROL Editar]**.
7. En el campo de configuración regional, escriba el valor requerido (por ejemplo, fr_FR, en_US) y seleccione **[!UICONTROL Guardar]**.

## Configurar SSO en ALM

Para configurar el SSO en ALM, siga estos pasos:

1. Inicie sesión como administrador.
2. Seleccione **[!UICONTROL Configuración]** > **[!UICONTROL Métodos de inicio de sesión]**.
3. Vaya a la pestaña **[!UICONTROL Configuración de inicio de sesión único (SSO)]**.
4. Seleccione **[!UICONTROL Agregar nueva configuración de SSO]**.

   ![](assets/sso-add.PNG)
   _Agregar SSO en ALM_

5. Configure los siguientes detalles y seleccione Guardar.
   * Escriba un nombre para la configuración.
   * Seleccione **[!UICONTROL IDP iniciado]** en el menú desplegable **[!UICONTROL Configuración de inicio de sesión único (SSO)]**.
   * Para **[!UICONTROL URL de autenticación iniciada por IDP]**:

      * Abra el archivo XML de metadatos que descargó anteriormente.
      * Busque el valor de ubicación y cópielo.
      * Pegue este valor en el campo URL de autenticación iniciada por IDP.

   * Para el **[!UICONTROL archivo XML de metadatos]**: cargue el archivo .xml que descargó anteriormente.

6. Vuelva a la ficha **[!UICONTROL Configuración]**.
7. En el menú desplegable, seleccione **[!UICONTROL Configuración de inicio de sesión único]**.
8. En el menú desplegable **[!UICONTROL Configuración de SSO]**, seleccione el nombre de configuración que creó anteriormente.
9. Seleccione **[!UICONTROL Guardar]**.

## Configuración de idioma e inicio de sesión del usuario

Cuando un usuario inicia sesión utilizando las credenciales a través de SSO, el atributo de idioma pasado desde el IDP se asigna a la interfaz del usuario y a los campos de idioma de contenido en ALM. La configuración de idioma se refleja inmediatamente en la interfaz de usuario y en el contenido sin ningún tiempo de almacenamiento en caché.

Los usuarios pueden actualizar manualmente su configuración de idioma en la sección perfil de usuario. Estas preferencias de idioma actualizadas manualmente permanecerán en vigor y no serán anuladas por la configuración de IDP durante futuros inicios de sesión.

Si un usuario se elimina suavemente de ALM, la configuración de idioma se conservará en la base de datos. Cuando se vuelva a agregar el mismo usuario, se restaurará el idioma establecido anteriormente.

Los administradores pueden consultar los informes Actividad de usuario, Resumen de aprendizaje y Tablero de cumplimiento para obtener detalles específicos del idioma.

## Actualización de las preferencias de idioma del usuario al iniciar sesión mediante SAML

Adobe Learning Manager es una plataforma multilingüe que admite las preferencias de idioma de los alumnos de varias maneras, a través de la interfaz, el contenido y los módulos del curso, todos disponibles en varios idiomas.

Con esta mejora, Adobe Learning Manager mejora el aprovisionamiento de usuarios Just-in-time para usuarios de plataformas nativas. Cuando los nuevos usuarios crean cuentas e inician sesión por primera vez, sus preferencias de idioma se capturan con precisión y se aplican automáticamente.

### Principales ventajas

* Actualiza automáticamente las preferencias de idioma de los usuarios al iniciar sesión.
* Ofrece una experiencia personalizada al mostrar la interfaz y el contenido en el idioma preferido del usuario.
* Se integra perfectamente con el proceso de autenticación de SAML.

Cuando los usuarios inician sesión a través de SAML, su preferencia de idioma (idioma de interfaz y contenido) se comprueba y actualiza en función de la información proporcionada durante el proceso de inicio de sesión.

La función se integra con el proceso de inicio de sesión de SAML para capturar y actualizar las preferencias de idioma del usuario sin problemas.
