---
description: Más información sobre cómo la configuración de integración conecta Adobe Learning Manager con soluciones de terceros
jcr-language: en_us
title: Configuración de integración en Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 4%

---


# Configuración de integración en Adobe Learning Manager

## Métodos de inicio de sesión

Adobe Learning Manager proporciona varios métodos de inicio de sesión para garantizar un acceso seguro y flexible para usuarios internos y externos. Los administradores pueden configurar estos métodos de inicio de sesión en función de los requisitos organizativos.

Los métodos de inicio de sesión disponibles son:

* ID de Adobe Learning Manager
* Adobe ID
* Inicio de sesión único

### Usuarios internos

La sección Usuarios internos le permite configurar opciones de inicio de sesión específicas para usuarios internos. Los usuarios internos pueden acceder a la cuenta mediante Adobe ID o el inicio de sesión único (SSO).

**Adobe ID:**

* Los usuarios internos pueden iniciar sesión con sus credenciales de Adobe ID.
* Adecuado para organizaciones que ya utilizan servicios de Adobe.

**Inicio de sesión único (SSO):**

* Permite el SSO para que los usuarios internos utilicen el proveedor de identidades (IdP) de la organización.
* Admite autenticación basada en SAML 2.0 para experiencias de inicio de sesión perfectas.

Para permitir inicios de sesión de SSO para usuarios internos, seleccione Habilitar inicio de sesión único múltiple (SSO) para el inicio de sesión y comience a configurar SSO.

El **[!UICONTROL Campo activo de SSO]** en Adobe Learning Manager se utiliza para asignar configuraciones de inicio de sesión único (SSO) a atributos o grupos de usuarios específicos. Puede configurar este campo para habilitar varias configuraciones de SSO para usuarios internos en función de su organización, ubicación u otros criterios.

### Usuarios externos

La sección Usuarios externos de Adobe Learning Manager le permite administrar a los alumnos externos, como socios o agencias, que requieren acceso limitado a la cuenta de Adobe Learning Manager. Esta sección proporciona herramientas para crear perfiles de registro, administrar grupos de usuarios externos y configurar opciones específicas para alumnos externos.

Los usuarios externos pueden iniciar sesión de la siguiente manera:

* Adobe ID: los usuarios externos pueden iniciar sesión con sus credenciales de Adobe ID.
* Inicio de sesión único (SSO): los usuarios externos pueden iniciar sesión a través de SSO si así lo ha configurado el administrador.
* Adobe Learning Manager ID: los usuarios externos pueden crear un nombre de usuario y una contraseña de Learning Manager para acceder a la plataforma.

**Puntos clave:**

* Puede habilitar uno o varios métodos de inicio de sesión para usuarios externos.
* Si se selecciona Adobe Learning Manager ID, los usuarios externos deben crear sus propias credenciales.
* SSO se puede configurar para usuarios externos en función de las necesidades de la organización.

### Configuración de SSO en Adobe Learning Manager

Adobe Learning Manager admite el inicio de sesión único (SSO) para permitir a los usuarios autenticarse una vez y obtener acceso a varias aplicaciones. Los administradores pueden configurar SSO tanto para usuarios internos como externos mediante proveedores basados en SAML 2.0.

Consulte [Inicios de sesión único en Adobe Learning Manager](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) para obtener más información.

>[!NOTE]
>
>* Se pueden añadir hasta 20 configuraciones de SSO a una cuenta.
>* Póngase en contacto con el servicio de asistencia al Adobe para obtener ayuda con los proveedores de SSO basados en SAML 2.0.

## Fuentes de datos

Los orígenes de datos permiten que los administradores de integración o usted integren sistemas externos para importar y sincronizar datos de aprendizaje y de usuario. Esta función garantiza una gestión y sincronización de datos perfectas con sistemas como HRMS, Salesforce, FTP y otros.

**Ejemplos de tipos de origen de datos**

* **Conectores de FTP**: los orígenes de datos basados en FTP permiten a las organizaciones cargar archivos de datos de usuario directamente en Adobe Learning Manager mediante protocolos de transferencia de archivos seguros. Estas conexiones son especialmente útiles para la importación por lotes de información de usuario, inscripciones de cursos y otras operaciones de datos en bloque.
* **Integraciones de terceros**: Adobe Learning Manager admite la integración con varios sistemas empresariales mediante conectores prediseñados. Estas integraciones pueden incluir sistemas de gestión de RR. HH., plataformas de gestión de relaciones con los clientes y otros sistemas de gestión del aprendizaje.
*** Integración con Salesforce**: el conector de Salesforce permite la sincronización directa de los datos de usuario, la información del curso y los registros de aprendizaje entre Salesforce y Adobe Learning Manager.

Consulte [Conectores en Adobe Learning Manager](/help/migrated/integration-admin/feature-summary/connectors.md) para obtener más información.

## Cuentas de igual a igual

Las cuentas de igual a igual en Adobe Learning Manager le permiten compartir puestos adquiridos y ver informes entre cuentas asociadas. Esta función es útil para las organizaciones que necesitan colaborar o compartir recursos entre diferentes cuentas.

Consulte [Cuentas de igual a igual](/help/migrated/administrators/feature-summary/peer-account.md) en Adobe Learning Manager para obtener más información.





