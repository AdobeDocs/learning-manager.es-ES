---
description: Adobe Learning Manager admite varios métodos de inicio de sesión a través de varias configuraciones de SSO para usuarios internos y externos.
title: Varios métodos de inicio de sesión único (SSO)
contentowner: saghosh
exl-id: 398816e8-a144-459b-8c39-6517ce4573b4
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 39%

---

# Varios métodos de inicio de sesión único (SSO) {#multiple-sso-logins}

Un administrador puede configurar varios métodos de inicio de sesión tanto para usuarios internos como externos. Adobe Learning Manager admite varios inicios de sesión único (SSO) que ayudarán a los administradores a configurar el método de inicio de sesión según sus necesidades y casos prácticos.

El objetivo es permitir a los administradores configurar diferentes métodos de SSO para diversos grupos de usuarios en función de su ubicación, organización, etc.

Se pueden añadir hasta 20 configuraciones de SSO a una cuenta. Estas se pueden utilizar para configurar el SSO tanto para usuarios internos como externos.

>[!NOTE]
>
>Al habilitar el inicio de sesión único múltiple, puede elegir valores o grupos de usuarios en el perfil de registro automático. Al elegir un valor, se crea un grupo de usuarios con cero usuarios. Este tipo de grupo de usuarios no tiene ningún usuario. Cuando se importe el siguiente archivo CSV, este grupo de usuarios se eliminará.

## Activar varios métodos de inicio de sesión único (SSO)

Para habilitar varios SSO, seleccione **Configuración** > **Métodos de inicio de sesión**.

En la página de configuración, seleccione la casilla de verificación Habilitar el inicio de sesión único múltiple (SSO) para usuarios internos o externos.

Cuando se habilita el inicio de sesión único múltiple, el método de inicio de sesión seleccionado para &quot;Método de inicio de sesión predeterminado&quot; se convierte en el tipo de inicio de sesión predeterminado para los grupos de usuarios o perfiles que no están vinculados a ninguna configuración de inicio de sesión único. El inicio de sesión predeterminado puede ser Adobe ID, SSO o ALM ID (usuarios externos).

Para configurar un SSO, siga los pasos que se indican a continuación:

1. Haga clic en Configurar inicio de sesión único (SSO).
1. Haga clic en Añadir nueva configuración de SSO.
1. En el cuadro de diálogo Configuración de SSO, añada lo siguiente:

   * Introduzca el nombre del SSO.
   * Seleccione el tipo de SSO: iniciado por IdP p SP.

      * Si ha seleccionado IDP iniciado, introduzca la URL de IDP. Esta será la dirección URL que se utilizará como identificador único de su aplicación y es la información que proporciona su proveedor de servicios de IdP. Esta es la URL a la que se redirigirá a todos los usuarios de Adobe Learning Manager después de iniciar sesión.
      * Cargue el documento XML de metadatos de IDP de su proveedor IdP. Este archivo contiene información sobre el IdP que permite a Adobe Learning Manager aceptar aserciones SAML de él.
      * Si ha seleccionado SP iniciado, introduzca el ID de entidad. El ID de entidad es una dirección URL que proporciona el proveedor de servicios (SP).
      * Introduzca la dirección URL de inicio de sesión del SP. Los usuarios utilizan esta dirección URL para iniciar sesión en la aplicación.

1. La configuración de SSO se agrega a la lista.

## Configurar el SSO para usuarios internos

### Usuarios de un archivo CSV

Siga los pasos mostrados a continuación:

1. Importe el archivo CSV que contiene los campos activos y sus valores.
1. Haga clic en Configuración > Métodos de inicio de sesión.
1. Active la casilla de verificación Habilitar inicio de sesión único múltiple (SSO) para el inicio de sesión.
1. Asigne las configuraciones de SSO a los valores del campo activo.
1. Guarde la configuración. Vuelva a importar el archivo CSV.

### Usuario único

Siga los pasos mostrados a continuación:

1. Haga clic en Configuración > Métodos de inicio de sesión.
1. Active la casilla de verificación Habilitar inicio de sesión único múltiple (SSO) para el inicio de sesión.
1. Seleccione un campo activo para un SSO.
1. Vincule las configuraciones de SSO a los valores del campo.
1. Guarde la configuración. Agregue un solo usuario y asigne un valor para el campo activo.

### Usuarios registrados automáticamente

Siga los pasos mostrados a continuación:

1. Haga clic en Configuración > Métodos de inicio de sesión.
1. Active la casilla de verificación Habilitar inicio de sesión único múltiple (SSO) para el inicio de sesión.
1. Vincule las configuraciones de SSO a los valores del campo.
1. Guarde la configuración. Agregue un solo usuario y asigne un valor para el campo activo.
1. Añada un perfil de registro automático.
1. Seleccione un valor para el campo SSO configurado.

Después de guardar la configuración del perfil, la URL copiada redirige a los usuarios al SSO vinculado al valor elegido para el perfil.

### Configurar el SSO para usuarios externos

Siga los pasos mostrados a continuación:

1. Cree un perfil externo.
1. Haga clic en Configuración > Métodos de inicio de sesión.
1. Active la casilla de verificación Habilitar inicio de sesión único múltiple (SSO) para el inicio de sesión.
1. Vincule la configuración de SSO al perfil externo creado.
1. Guarde la configuración.

Después de guardar la configuración del perfil, una vez guardada, la URL de perfil externo copiada redirigirá a los usuarios al SSO vinculado al perfil.

## Preguntas más frecuentes

+++ ¿Quién puede habilitar varios SSO para usuarios?

Tanto el administrador como el administrador personalizado pueden habilitar varios SSO.
+++

+++¿Puedo utilizar un campo activo de un solo valor nuevo o uno existente?

Sí, puede utilizar un campo activo de un solo valor nuevo o uno existente para configurar varios SSO.
+++

+++Si hay campos desactivados en un CSV, ¿fallará la configuración de varios SSO?

No, no afectará a la configuración de los SSO. Los usuarios se redirigirán a un SSO configurado.
+++

+++¿Puede un administrador añadir nuevos valores al campo activo de la página al configurar Multi-SSO?

Sí, un administrador puede añadir nuevos valores a los campos activos.
+++

+++¿Puedo deshabilitar o eliminar campos vinculados a SSO?

Sí, puede deshabilitar o eliminar campos vinculados a SSO hasta que desvincule los campos de la página de configuración de SSO.
+++
