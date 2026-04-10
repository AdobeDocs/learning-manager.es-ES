---
description: Instalar el conector de Microsoft Teams en Adobe Learning Manager
jcr-language: en_us
title: Instalar el conector de Microsoft Teams en Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: 864c3a4e60cf1bf1c049838fb2ba46ebbcb28ddf
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 52%

---

# Instalar el conector de Microsoft Teams en Adobe Learning Manager

## Información general

Microsoft Teams® es una plataforma de colaboración persistente basada en chat que es totalmente compatible con el uso compartido de documentos, reuniones en línea y otras funciones para las comunicaciones empresariales.

Adobe Learning Manager utiliza un conector de clase virtual que se puede utilizar para integrar reuniones de Microsoft Teams en Learning Manager.

El conector de Microsoft Teams conecta los sistemas Learning Manager y Microsoft Teams para activar la sincronización automática de reuniones virtuales. En la siguiente lista, se describen las funciones del conector de Microsoft Teams:

**Configurar sesiones virtuales mediante Microsofts Teams**

Este conector ayuda a integrar su cuenta de Adobe Learning Manager con su cuenta de Microsoft Teams. Una vez integrado, el conector permite que un autor en Learning Manager utilice Microsoft Teams como proveedor de servicios de tecnología para los módulos de clase virtual creados en Learning Manager.

**Permitir que los Microsofts Teams autentiquen a los alumnos al entrar en una clase virtual**

Este conector ayuda a configurar el organizador de reuniones de Microsoft Teams desde Learning Manager mientras se crea una reunión. El organizador de reuniones puede gestionar el punto de encuentro para restringir o admitir la entrada a la reunión, así como controlar las otras opciones de la reunión proporcionadas por Microsoft Teams.

**Usar sincronización automatizada de finalización de usuarios**

El proceso automatizado de sincronización de finalización de usuarios permite que un administrador de Learning Manager obtenga automáticamente los registros de finalización y la URL de registro para la reunión de Microsoft Teams.

## Funciones en Microsoft Teams

Si organiza una reunión con varios participantes, puede asignar funciones a cada uno de ellos para determinar las acciones que puede llevar a cabo en la sesión.

Hay dos funciones para elegir: **presentador** y **asistente**.

Para obtener más información, consulte [Funciones en una reunión de equipos: Microsoft](https://support.microsoft.com/es-es/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Configurar el conector de Microsoft Teams

>[!NOTE]
>
>Los elementos marcados como &lt;Desarrollador/Opcional> a continuación son opcionales y se usan principalmente para configurar inquilinos de versiones de prueba o desarrolladores con Microsoft en caso de que el usuario no tenga un inquilino de producción. Estos son opcionales, ya que la mayoría de ellos ya los habría realizado el administrador del equipo.

## Crear una cuenta de desarrollador de E5 de Microsoft &lt;Desarrollador/Opcional>

Puede acceder al conector de Microsoft Teams si dispone de Office 365 E3 u Office 365 E5. La opción recomendada es Office 365 E5.

* Visita la [página de planes de Microsoft](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&lnkd=Google_O365SMB_Brand&gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE). En la página web, puede comprar una cuenta E3 o E5 o hacer clic en Prueba gratis.
* Proporcione la información necesaria y cree una cuenta.

>[!NOTE]
>
>La cuenta debe usar el formato `<username>@<company name>.onmicrosoft.com`.

## Crear aplicación para el conector de Microsofts Teams

1. Visite el [portal de Microsoft Azure®](https://portal.azure.com/).
1. Inicie sesión en la cuenta de E5 de Microsoft que ha creado en la sección anterior.
1. Busque **Azure Active Directory**.
1. Haga clic en **[!UICONTROL Registros de aplicaciones]**.
1. Haga clic en **[!UICONTROL Nuevo registro]**, introduzca los siguientes detalles y registre la aplicación:

   1. **Nombre**: cualquier nombre de su elección.
   1. **Tipos de cuenta admitidos**: cuentas de cualquier directorio de la organización (cualquier Azure Active Directory - multitenant).
   1. **URI de redirección (opcional)**: campo opcional que indica la URL de respuesta.

1. En la columna **Aspectos esenciales**, anote los siguientes ID, que se usarán más durante la integración:

   1. **Id. de aplicación (cliente)**
   1. **Id. de directorio (inquilino)**

1. Busque las credenciales de cliente y haga clic en **[!UICONTROL Agregar un certificado o secreto]**.
1. Haga clic en **[!UICONTROL Nuevo secreto de cliente]** y añada los siguientes detalles:

   1. **Descripción**: escriba un nombre.
   1. **Caduca**: se establece en cualquier valor (el valor recomendado es de 24 meses). Asegúrese de que se generen nuevas credenciales de cliente una vez que caduquen las anteriores).

Anote el secreto de cliente, que se utilizará más adelante durante la integración.

## Obtener permiso de acceso al conector de Microsoft Teams

1. Visita el [portal de Microsoft Azure](https://portal.azure.com/).
1. Inicie sesión con la cuenta de E5 de Microsoft que ha creado anteriormente.
1. Busque **Azure Active Directory**.
1. Haga clic en **[!UICONTROL Registros de aplicaciones]**.
1. Haga clic en la aplicación que ha creado en la sección anterior.
1. Haga clic en **[!UICONTROL Permisos de API]**.
1. Haga clic en **[!UICONTROL Agregar un permiso]**.
1. Seleccione **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Permisos de la aplicación]** y agregue los permisos siguientes:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All
   1. OnlineMeetingRecording.Read.All

1. Haga clic en **[!UICONTROL Grant admin access for Adobe]**.
1. Haga clic en **[!UICONTROL Funciones de la aplicación]** > **[!UICONTROL Crear función de aplicación]**.
1. Introduzca los siguientes valores:

   1. **Nombre para mostrar**: nombre de la API/nombre de permiso (por ejemplo, Calendars.ReadWrite).

   1. **Tipos de miembros permitidos**: especifique tanto usuarios como aplicaciones (Usuarios/Grupos + Aplicaciones).

   1. **Valor**: nombre de la API/nombre de permiso (por ejemplo, Calendars.ReadWrite).

   1. **Descripción**: nombre de la API/nombre de permiso (por ejemplo, Calendars.ReadWrite).

   1. **¿Desea habilitar esta función de aplicación?** - Seleccione esta casilla de verificación.

1. Repita los pasos anteriores para las nueve API/permisos que se han añadido.

## Configurar la directiva de acceso mediante scripts de PowerShell

Para configurar la directiva de acceso a la aplicación para el conector de Microsofts Teams mediante la ejecución de scripts de PowerShell, siga el procedimiento descrito en este [documento](https://docs.microsoft.com/es-es/graph/cloud-communication-online-meeting-application-access-policy).

Esto permite al conector acceder a las reuniones en línea de Microsoft Teams.

>[!NOTE]
>
>En el documento anterior, ejecute el paso 5 opcional para garantizar que a cualquier usuario activo se le pueda otorgar la función de organizador desde la aplicación de autor de Learning Manager. Si no se ejecuta este paso, los usuarios no tendrán los permisos de acceso necesarios para ser organizadores y la creación de la reunión no se completará (las API de Microsoft consideran que el organizador es el creador de una reunión de Teams).

## Configurar el conector de Microsofts Teams en Learning Manager

1. Inicie sesión en Learning Manager como **administrador de integración**.

1. En la página Conectores, selecciona Conector de Microsofts Teams y haz clic en **[!UICONTROL Conectar]**.

1. Introduzca estos valores:

   1. **Nombre de conexión**: proporcione el nombre que el autor verá al crear la sesión.

   1. **Id. de inquilino de Microsofts Teams**: introduzca el valor determinado anteriormente.

   1. **Id. de cliente Microsoft Teams**: escriba el valor determinado anteriormente.

   1. **Secreto de cliente de Microsofts Teams**: introduzca el valor determinado anteriormente.

   1. **Correo electrónico del usuario administrador de Microsofts Teams**: introduce el correo electrónico predeterminado del organizador. Este usuario (normalmente, un usuario del servicio) sería el creador de la reunión en caso de que no se seleccionara ningún organizador explícito en la aplicación de autor de Learning Manager.

## Asignar licencias a usuarios &lt;Desarrollador/Opcional>

1. Visita [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Usuarios activos]**.
1. Haga clic en **[!UICONTROL Más acciones para usuarios]** para los usuarios a los que desee proporcionar acceso a Microsofts Teams.
1. Haga clic en **[!UICONTROL Administrar licencias de productos]**.
1. Habilitar licencia para Office 365 E5 sin audioconferencia.

<!--
## Record a session

The API used for recording a session is a protected API. To access the API, you must request access from Microsoft. For more information, see this  [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

In the document,

*"To request access to these protected APIs, complete the following  [request form](https://aka.ms/teamsgraph/requestaccess). We review access requests every Wednesday and deploy approvals every Friday, except during major holiday weeks in the U.S. Submissions during those weeks will be processed the following non-holiday week. To verify whether your request has been approved, test your application access on the next applicable Monday."*

For learners, the recording URL is displayed on the VC course overview page.

After 30 minutes of completing a course, the attendance for the learner gets marked. 
-->

## Preguntas más frecuentes

+++¿Qué es un organizador y un presentador?

Consulte la [documentación](https://support.microsoft.com/es-es/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) de Microsoft para obtener información sobre las diferentes funciones y capacidades admitidas por los Microsofts Teams.

+++

+++¿Debe un organizador ser un usuario registrado tanto en Learning Manager como en Microsoft Teams? 

Sí, el organizador también debería formar parte tanto de Learning Manager como de Microsoft Teams. Además, el organizador debe formar parte del mismo inquilino de Microsoft, que se configura en la aplicación de administración de integración.

+++

+++¿Debe un presentador ser un usuario registrado tanto en Learning Manager como en Microsoft Teams? 

Sí, el presentador también debería formar parte tanto de Learning Manager como de Microsoft Teams. El presentador debe tener un ID de Azure Active Directory (puede formar parte del mismo inquilino que el organizador o de cualquier otro). Además, incluso los usuarios anónimos (usuarios que inician sesión solo con el nombre de usuario y no forman parte de Active Directory) también pueden ser nombrados presentadores por el organizador o los presentadores existentes durante la reunión.

+++

+++Microsoft Teams incluye reuniones, seminarios web y eventos en directo. ¿Cuáles admite el conector de Teams? 

Por el momento, el conector de Teams solo admite reuniones en Microsoft Teams. Para obtener más información, vea este [documento](https://docs.microsoft.com/es-es/microsoftteams/quick-start-meetings-live-events).

+++
