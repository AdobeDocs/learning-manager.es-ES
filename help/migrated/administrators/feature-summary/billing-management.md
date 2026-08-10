---
description: Administre la facturación de Learning Manager, realice pedidos con una tarjeta de crédito, suscríbase con una orden de compra o con un plan de usuarios activos mensuales.
jcr-language: en_us
title: Administrar pedidos y facturación de Learning Manager
contentowner: manochan
exl-id: 91635ef7-dbb9-4bb1-98f9-129f6fd5b6b4
source-git-commit: 2f1ca19ec3b94f975bd78ed92b48621eec6d5a22
workflow-type: tm+mt
source-wordcount: '2471'
ht-degree: 53%

---


# Administrar pedidos y facturación de Learning Manager

La compra basada en tarjeta de crédito solo está disponible en la [región de EE. UU.](http://learningmanager.adobe.com/).

Administre la facturación de Learning Manager, realice pedidos con una tarjeta de crédito, suscríbase con una orden de compra o con un plan de usuarios activos mensuales.

Adobe Learning Manager tiene modelos de precios flexibles, cómodos para el cliente y uno de los modelos de precios más adecuados para satisfacer las necesidades de su empresa. Para obtener más información, consulte la página de [Learning Manager](https://www.adobe.com/products/learningmanager.html).

Los administradores de su empresa son los únicos que pueden ocuparse de la facturación.

Si desea ponerse en contacto con Adobe para obtener más información sobre la facturación y la suscripción a Learning Manager, escríbanos a [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

## La página Facturación

Para acceder a la página Facturación, inicie sesión en Adobe Learning Manager como administrador y seleccione **[!UICONTROL Facturación]** en el panel de navegación izquierdo.

La página Facturación contiene las siguientes pestañas:

| Pestaña | Propósito |
|---|---|
| **Suscripción** | Consulte los detalles de la cuenta, los derechos de licencia y el consumo de licencias. Administrar la activación del plan. |
| **Historial de pedidos** | Revisar los pedidos pasados realizados en la cuenta. |

### Pestaña Suscripción

**Detalles de la cuenta**

La tarjeta **Detalles de cuenta** situada en la parte superior de la pestaña **Suscripción** muestra cuatro identificadores de solo lectura para tu cuenta.

| Campo | Descripción |
|---|---|
| **ECCID** | Número de referencia del Adobe para su cuenta. Cítelo al contactar con el servicio de asistencia del Adobe. |
| **Id. de cuenta** | El identificador único de tu cuenta de Adobe Learning Manager. |
| **Nombre de cuenta** | El nombre para mostrar de su cuenta de Adobe Learning Manager. |
| **Id. de organización de IMS** | La organización de Adobe Admin Console vinculada a esta cuenta. Está en blanco si aún no está vinculado. |

**Licencias**

La sección **Licencias** muestra todas las licencias o derechos activos de la cuenta. Cada bloque muestra el nombre de la licencia, una descripción del plan cuando corresponda y una fila de estadísticas que muestra las cifras de consumo del período de contrato actual.

Las columnas de la fila Estadísticas varían según el tipo de licencia:

| Tipo de licencia | Columnas mostradas |
|---|---|
| Licencia de pago (por ejemplo, Adobe Learning Manager Ultimate) | Adquirido / Utilizado / Utilizado por cuentas de igual a igual / Restante |
| Licencia de prueba (por ejemplo, Virtual Coach) | Disponible / Usado / Restante |

Seleccione **[!UICONTROL Ver detalles de uso]** debajo de la fila de estadísticas para expandir un desglose en línea. La sección expandida muestra:

- Un menú desplegable **Seleccionar período** para filtrar por período de contrato, incluidos los períodos históricos
- Una tabla **Uso general** con columnas: Adquirido / Utilizado por esta cuenta / Utilizado por cuentas de igual a igual / Restante
- Un vínculo **Ver desglose de cuentas** para ver el uso distribuido entre cuentas de igual a igual individuales
- Un vínculo **Descargar informe detallado** para exportar datos de uso como un archivo

**Bloque de licencias de Agent Orchestrator**

Cuando se vincula una licencia de Agent Orchestrator, la fila de estadísticas muestra:

| Columna | Descripción |
|---|---|
| **Adquirido** | Créditos totales adquiridos para el período del contrato. |
| **Usado** | Créditos consumidos en todos los servicios que utilizan esta licencia. |
| **Usado por ALM** | Créditos consumidos específicamente por Adobe Learning Manager. |
| **Restantes** | Créditos aún disponibles. |

Si su organización utiliza cuentas primarias y secundarias, la sección **Licencias** de la cuenta principal muestra la columna **Utilizado por cuentas secundarias**, que refleja el consumo de crédito en todas las cuentas secundarias vinculadas. Las cuentas secundarias muestran su asignación como **Puestos sancionados** en lugar de Comprados.

## Vincule su cuenta de Adobe Learning Manager a Adobe Admin Console

Para que las funciones de IA general puedan activarse, su cuenta de Adobe Learning Manager debe estar conectada a una organización de Adobe Admin Console. Una vez vinculada, Adobe Learning Manager detecta la licencia de Agent Orchestrator y pone a su disposición la pestaña **Créditos**.

La vinculación se establece automáticamente cuando se adquiere su cuenta mediante el proceso de pedidos estándar de Adobe o cuando activa su cuenta mediante una clave de activación. Puede verificar el vínculo en la pestaña **Suscripción**: si el campo **ID de organización de IMS** en **Detalles de cuenta** está lleno, la cuenta ya está vinculada.

### Vincular la cuenta manualmente

Si su cuenta se configuró de forma independiente y el campo **ID de organización de IMS** está en blanco, vincule manualmente.

**Requisitos previos:**
- Debe ser administrador de la cuenta de Adobe Learning Manager.
- Debe tener la función de administrador del sistema en la organización de Adobe Admin Console que desee vincular.
- La organización Adobe Admin Console debe tener una licencia de Agent Orchestrator activa.

1. Seleccione **[!UICONTROL Facturación]** y, a continuación, seleccione la pestaña **[!UICONTROL Suscripción]**.
2. En la tarjeta **Detalles de la cuenta**, seleccione **[!UICONTROL Vincular organización IMS]**.
3. Se abre una ventana de inicio de sesión. Introduzca las credenciales de su cuenta de Adobe y seleccione su organización en la lista. Adobe Learning Manager confirma que el inicio de sesión de la cuenta tiene la función de administrador del sistema en la organización Adobe Admin Console y que la misma cuenta tiene la función de administrador en Adobe Learning Manager.
4. Si ambas comprobaciones se superan, se establece el vínculo. El campo **ID de organización de IMS** se actualiza con el identificador de su organización, y el saldo acreedor aparece en la sección **Licencias**.
5. Si falla alguna de las comprobaciones, se muestra un mensaje de error. Confirme los requisitos previos anteriores e inténtelo de nuevo.

### Desvincular la cuenta

Después de la desvinculación, las funciones de generación de inteligencia artificial se deshabilitan para todos los alumnos y la pestaña **Créditos** no está disponible hasta que la cuenta se vincule de nuevo.

1. Seleccione **[!UICONTROL Facturación]** y, a continuación, seleccione la pestaña **[!UICONTROL Suscripción]**.
2. En la tarjeta **Detalles de la cuenta**, seleccione **[!UICONTROL Desvincular organización IMS]**.
3. Vuelva a iniciar sesión para confirmar su función de administrador en la organización.
4. El vínculo se elimina. El campo **ID de organización de IMS** vuelve a estar en blanco y la pestaña **Créditos** está oculta.

Para restaurar el acceso, repita los pasos de vinculación manual anteriores.

## Realizar pedidos con tarjetas de crédito {#placeordersusingcreditcards}

Puede comprar una suscripción para un máximo de 3500 alumnos mediante cualquier orden de pago con tarjeta de crédito. El primer pedido de la cuenta debe ser para un mínimo de 10 alumnos.

1. En el panel de navegación izquierdo de la aplicación del administrador, haga clic en **[!UICONTROL Facturación]**.

   ![](assets/billing.png)

   *Iniciar facturación de Adobe Learning Manager*

1. En la página **[!UICONTROL Información de facturación]**, agregue el número de usuarios en el campo **[!UICONTROL Agregar usuarios]**. Al utilizar una tarjeta de crédito para suscripciones de prepago, puede ver la cantidad de usuarios que puede añadir para la suscripción. El número de usuarios que puede añadir no debe superar el número indicado en la sección Restante.1.

   ![](assets/billing-page-to-manageyoursubscriptionandorders.png)

   *Agregar número de usuarios*

1. Tras indicar la cantidad de usuarios que añadir, haga clic en Realizar pedido en la esquina superior derecha de la página.

   ![](assets/billing2.png)

1. Examine la estimación que aparece en la pantalla.

   ![](assets/pricing-estimate.png)

   *Realizar un pedido*

   La tarifa de suscripción anual se calcula según el número de usuarios que se añaden para la suscripción. Por ejemplo, si se añaden cuatro usuarios, la tarifa anual se calcula con la expresión 4 usersX$4X$12, que devuelve $192.

   Haga clic en **[!UICONTROL Continuar]**.

   *Revisar la estimación*

1. En la página Detalles del pago, puede ver el precio estimado del pedido. La moneda aparece según la configuración regional actual.

   ![](assets/payment-details.png)

   *Ver detalles de pago*

   También puede cambiar la configuración regional seleccionando el país en la lista desplegable.

   ![](assets/change-locale.png)

   *Seleccione el país de facturación*

1. Proporcione su información de contacto, elija el tipo de tarjeta de crédito y especifique los datos de la tarjeta de crédito. Después de introducir los detalles necesarios, haz clic en **[!UICONTROL Completar pedido]**.
1. Después de realizar el pedido, para ver los paquetes pedidos recientemente, haz clic en la pestaña **[!UICONTROL Historial de pedidos]** en la página **[!UICONTROL Facturación]**.

   ![](assets/order-history.png)

   *Ver historial de pedidos*

## Comprobar el estado de los pedidos {#checkorderstatus}

Todos los pedidos pueden tener uno de los cuatro estados siguientes:

**Activo:** un pedido está activo y los usuarios se registran correctamente.

**Suspendido:** Un pedido pasa a tener este estado en los siguientes casos:

- Cuando hay algún retraso en el recibo del pago de la tarjeta de crédito.
- Cuando caduca la tarjeta de crédito.
- El pago se rechaza en cualquier ciclo de pago recurrente.

**Inicio de cancelación:** un pedido pasa a tener este estado cuando el administrador de Learning Manager desactiva la cuenta. Posteriormente, el pedido pasa al estado Cancelado después de recibir la confirmación de cancelación del pedido.

## Actualizar datos de la suscripción {#updatesubscriptiondetails}

1. En la lista de pedidos, haga clic en **[!UICONTROL Editar]**.

   ![](assets/update-subsciptiondetailsclickedit.png)

   *Actualizar detalles de suscripción*

1. En la página Datos de la suscripción, haga clic en **[!UICONTROL Editar suscripción]**.
1. Elija el elemento que desea editar:

   - Forma de pago: Utilice esta opción para actualizar los datos de pago como, por ejemplo, la tarjeta de crédito.
   - Dirección: Utilice esta opción para actualizar los detalles de la dirección.

## Cancelar una suscripción {#cancelasubscription}

Para cancelar un pedido:

1. En el panel izquierdo de la página Administrador, haga clic en Facturación.
1. En la página Facturación, en la esquina superior derecha, elija **[!UICONTROL Acciones]** > **[!UICONTROL Desactivar cuenta]**.
1. Cuando el administrador desactiva la cuenta, se cancelan todos los pedidos a partir del siguiente ciclo de facturación.

Cuando el cliente desactiva una cuenta, pasa a un estado de prueba durante los 30 días siguientes. El propietario de la cuenta recibe tres recordatorios por correo electrónico para reactivar la cuenta. Si no la reactiva, ninguno de los usuarios podrá acceder a Learning Manager, excepto el propietario.

## Realizar pedidos con una orden de compra {#placeordersusingpurchaseorder}

El proceso de orden de compra es un método de pago alternativo. Como requisito previo, la cuenta de su organización debe estar registrada con Adobe. Este proceso se carga en la cuenta de su empresa. La cuenta se carga en función de las actividades de un alumno. Solo se cobran las actividades relacionadas con objetos de aprendizaje. Para realizar un pedido mediante una orden de compra:

1. Envíe un correo electrónico a [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com) e indique la cantidad de alumnos requeridos.
1. El equipo de Learning Manager le envía una clave de activación.
1. En la página Facturación de la aplicación Administrador, indique la clave de activación.
1. Haga clic en Activar en la esquina superior derecha de la página.

## Comprobar estado de la cuenta {#checkaccountstatus}

Tras la activación, una cuenta puede tener uno de los estados siguientes:

- **Prueba**: puedes crear una cuenta de Adobe Learning Manager y usarla sin ningún pago durante un período de 30 días. Durante el período de prueba, no hay límite en la cantidad de alumnos registrados.
- **Activo**: en este estado, la cuenta tiene suscripciones de alumno activas con pagos mensuales recurrentes según el pedido de suscripción.
- **Inactivo**: una cuenta pasa a este estado en los siguientes casos:

  - Después del período de prueba si no hay pedidos de suscripción activos en la cuenta.
  - El administrador desactiva la cuenta, lo que hace que se cancelen todos los pedidos existentes en una cuenta a partir del siguiente ciclo de facturación de la suscripción.
  - El pago se rechaza para los pedidos activos de una cuenta, incluso después de los recordatorios.

Un estado inactivo no cancela su cuenta con efecto inmediato. Recibirá al menos un par de recordatorios del equipo de Learning Manager en los que se le solicitará que proporcione la información más reciente sobre su tarjeta de crédito si ha caducado. En estado inactivo, solo un administrador puede iniciar sesión en la cuenta de Adobe Learning Manager. Los demás usuarios no tienen acceso a la cuenta.

- **Se requiere activación**: tu cuenta pasa a este estado cuando el administrador de Learning Manager decide desactivar la cuenta. Se cancelan todos los pedidos de esta cuenta. El cobro de pagos de estos pedidos no se produce en el próximo ciclo de facturación. La cuenta se mantiene en este estado hasta la fecha del último ciclo de facturación. En este estado, todos los usuarios pueden continuar utilizando la aplicación sin problema hasta el final de la última fecha de pago recurrente.

## Cancelar una suscripción {#Cancelasubscription-1}

Para cancelar una suscripción activa, póngase en contacto con el equipo de asistencia de Learning Manager.

## Tarifa de cancelación de la cuenta {#accountterminationfee}

Si desea cancelar la suscripción antes de que finalice el período anual, se cobrará una tarifa de cancelación anticipada. La tarifa de cancelación equivale al 50 % del precio de la suscripción del período de permanencia restante.

## Plan de usuario activo mensual {#monthlyactiveusersmauplan}

Puede optar por un plan de usuarios activos mensuales como opción preferida de facturación. Esta opción genera la facturación a partir de la cantidad de usuarios activos exclusivos mensuales. Los usuarios activos exclusivos mensuales se añaden de manera acumulativa por un período de 12 meses a partir del mes activación del plan. Este número se utiliza para la facturación durante el período.

Utilice el ejemplo siguiente para saber cómo se calcula un plan de usuarios activos mensuales.

Supongamos que hay un caso en el que el número de usuarios por mes es el siguiente:

- Mes 1 = 50
- Mes 2 = 500
- Mes 3 = 5000
- Mes 4 a 12 = 10

Total de usuarios activos mensuales que se facturan = Mes 1 + Mes 2 + Mes 3 + Mes 4 a 12 = 50 + 500 + 5000 + 90 = 5640.

La facturación del periodo es para 5640 usuarios.

Al final del período de 12 meses, la cantidad de utilizaciones se restablece a cero y comienza otro período del plan de usuario exclusivo mensual. Puede añadir varias claves de activación para incrementar la cantidad de licencias adquiridas.

Cualquier usuario que efectúe las acciones siguientes o consiga finalizaciones debido a acciones realizadas por otros usuarios se considera un usuario activo exclusivo de ese mes.

- Consumir un curso, un programa de aprendizaje o una certificación.
- Consumir, descargar una ayuda de trabajo o archivos adjuntos del curso.
- Consumir, descargar o crear notas personales.
- Participar en Aprendizaje social creando tableros, publicaciones o comentarios.
- Conseguir finalizaciones debido a aprobaciones de envío de certificados externos o a la asistencia a sesiones de clase o de clase virtual.

## Ver detalles de uso {#viewusagedetails}

1. Para ver la cantidad de usuarios activos por mes, haga clic en **[!UICONTROL Ver detalles de uso]**.

   ![](assets/report-request-usage.png)

   *Ver usuarios activos por mes*

1. En la página que se muestra, puede ver el contenido siguiente:

   - **Uso general:** Puede comprobar el número total de usuarios activos, los usuarios que consumen Learning Manager en un mes y el número de usuarios que aún no se han registrado en ningún curso.
   - **Uso mensual:** Puede ver una tabla de usuarios activos únicos al mes.

## Descargar informe de uso {#downloadusagereport}

También puede descargar los datos de la cantidad de usuarios activos por mes y año. Para descargar, haga clic en **[!UICONTROL Descargar informe detallado]**.

En el cuadro de diálogo **Generar solicitud de informe**, indique los meses y el año correspondientes; a continuación, haga clic en **[!UICONTROL Generar]**.

![](assets/generate-report-request.png)

*Descargar informe de uso activo*

Si cierra la ventana del navegador, la descarga se inicia la próxima vez que visite Learning Manager.

Los informes se guardan en la carpeta Descargas del navegador.

## Cancelar una suscripción

Para cancelar una suscripción activa, póngase en contacto con el equipo de asistencia de Learning Manager.

<!--
## Gen AI credits {#genaicredits}

### How Gen AI credits work

Gen AI credits are consumed each time a learner interacts with an AI-powered feature — for example, when asking a question through the AI Assistant or generating a personalized learning recommendation. Before each interaction begins, Adobe Learning Manager checks that credits are available. If credits are available, the interaction proceeds. If the balance has been exhausted, the learner sees a message that the feature is temporarily unavailable.

Credits are purchased as part of an Adobe Experience Platform Agent Orchestrator license. That license is managed in your Adobe Admin Console, and Adobe Learning Manager connects to it automatically to detect available credits.

**Credit priority rule:** If your Adobe Learning Manager plan includes bundled Gen AI credits and you also have an Agent Orchestrator license, the bundled credits are consumed first. Agent Orchestrator credits are used only after the bundled credits are exhausted.

**Shared credit pools:** If your organization has multiple Adobe Learning Manager accounts all linked to the same Adobe Admin Console organization, all accounts draw from a single shared credit pool.

>[!IMPORTANT]
>
>All Gen AI features are turned off by default. You must enable each feature and set a credit usage limit before learners can access it.

### Access the Gen AI Credits tab

1. Select **[!UICONTROL Admin]** > **[!UICONTROL Billing]**.
2. Select the **[!UICONTROL Credits]** tab.

The **Credits** tab is visible only when Gen AI credits have been purchased or were historically active on the account. If the tab is not visible, verify that your account is linked to an Adobe Admin Console organization that has an active Agent Orchestrator license.

### Gen AI Features table

The **Gen AI Features** table lists every AI feature available on the account.

| Column | Description |
|---|---|
| **Feature Name** | Name of the AI feature. Select the name to go to that feature's settings page. |
| **Status** | Whether the feature is on or off. Toggle the feature from its settings page. |
| **Max Credits Usage Limit** | Maximum credits this feature can consume during the contract period. Must be set before the feature can be enabled. Applies to learner-facing features only. |
| **Credits Used** | Total credits consumed by this feature since the contract start date, updated in real time. |

### Enable a Gen AI feature

1. On the **[!UICONTROL Credits]** tab, locate the feature in the **Gen AI Features** table.
2. In the **Max Credits Usage Limit** column, enter the maximum number of credits this feature can consume during the contract period.
3. Select the feature name to go to its **Feature Settings** page.
4. On the **Feature Settings** page, toggle the feature on.
5. Complete any additional configuration, such as assigning learners and catalogs to the AI Assistant.

### What happens when credits run out

- If a feature reaches its **Max Credits Usage Limit**, learners see a message that the feature is temporarily unavailable. Raise the limit at any time from the **Credits** tab.
- If overall account credits are exhausted, all Gen AI features stop working for learners until additional credits are purchased. Usage reports and credit metrics remain accessible to admins.
- If a learner is mid-interaction when credits are exhausted, that interaction completes. All subsequent interactions are blocked.
- Admins can set a credit limit higher than the number of purchased credits. Over-allocation is permitted, and a true-up can happen at renewal.

### Monthly Credits Usage chart

Below the Gen AI Features table, a **Monthly Credits Usage** chart shows credits consumed per feature per month. By default, the chart shows the current contract year period based on the Agent Orchestrator contract start date. Select **[!UICONTROL Download]** to export the monthly report for the selected period. Report generation is asynchronous — you receive an in-app notification and email when the file is ready.

### Gen AI usage reports

Adobe Learning Manager provides two Gen AI usage reports under **[!UICONTROL Reports]** > **[!UICONTROL AI Reports]**.

**Monthly credits usage report**

Shows credits consumed per feature per month. Useful for budget planning and contract renewal.

- **Columns:** Month | Feature | Credits Used
- **Filter:** Select a date range spanning one or more contract periods
- **Download:** Asynchronous — you receive an in-app notification and email when the file is ready

**Learner Gen AI credits usage report**

An audit trail showing which learners used which features and how many credits each interaction consumed.

- **Columns:** Date | Learner Name | Learner Email | Feature | Credits Used
- **Filter:** Select the date range you want to audit
- **Download:** Asynchronous — you receive an in-app notification and email when the file is ready

### Credit usage alerts

Adobe Learning Manager automatically notifies you when credit consumption crosses key thresholds. Notifications are delivered both in-app and by email.

| Trigger | Notification |
|---|---|
| Account credits reach 90% of total purchased | Warning — credits are nearly exhausted at the account level |
| Account credits reach 100% of total purchased | Alert — all credits are consumed and Gen AI features stop for learners |
| A feature reaches its individual Max Credits Usage Limit | Alert — names the specific feature; that feature stops for learners |

When you receive a 90% warning, contact your Adobe account team to purchase additional credits before the 100% threshold is reached.
-->

## Preguntas más frecuentes {#frequentlyaskedquestions}

**Cómo agregar o quitar suscripciones de una cuenta?**

Para añadir suscripciones a una cuenta, añada el número de usuarios para los que desee adquirir suscripciones. A continuación, en la esquina superior derecha, haga clic en **[!UICONTROL Realizar pedido]**. Revise la estimación y haga clic en **[!UICONTROL Continuar]**. Introduzca los datos de su cuenta y también los de su tarjeta de crédito. A continuación, para adquirir las suscripciones, haga clic en **[!UICONTROL Completar pedido]**.

Para eliminar una suscripción activa, póngase en contacto con el equipo de asistencia de Learning Manager.


**Cómo cambiar una tarjeta de crédito para suscripciones?**

En la pestaña **[!UICONTROL Historial de pedidos]**, para una cuenta activa, haz clic en **[!UICONTROL Editar]**. A continuación, en la página Datos de la suscripción, haga clic en **[!UICONTROL Editar suscripción]**. Introduzca los datos de la nueva tarjeta de crédito y haga clic en **[!UICONTROL Actualizar método de pago]**.

![](assets/credit-card-details.png)

*Ver detalles de la tarjeta de crédito*


**Cómo actualizar la información de facturación en Learning Manager?**

Para actualizar la información de facturación, siga los pasos que se indican a continuación:

1. Inicie sesión como **administrador** y haga clic en **[!UICONTROL Facturación]**.
1. En la lista de pedidos, haga clic en **[!UICONTROL Editar]**.
1. En la página Datos de la suscripción, haga clic en **[!UICONTROL Editar suscripción]**.

Elija el elemento que desea editar:

1. **[!UICONTROL Método de pago]:** Utilice esta opción para actualizar los datos de pago como, por ejemplo, la tarjeta de crédito.
1. **[!UICONTROL Dirección]:** Use esta opción para actualizar los detalles de la dirección.


**¿Puedo cancelar parcialmente una suscripción?**

No, no se puede cancelar parcialmente una suscripción. Si necesita reducir el número de puestos que ha adquirido, puede cancelar la suscripción al final del ciclo de facturación y, a continuación, adquirir el número de puestos necesarios.


**¿Cómo puedo obtener una factura de los pagos con tarjeta de crédito?**

Póngase en contacto con [FastSpring](https://fastspring.com/) para obtener una factura de sus pagos mediante una de las siguientes formas:

- Cree una solicitud de servicio con FastSpring mediante el vínculo `https://questionacharge.com`.
- Envíe un correo electrónico a FastSpring el `orders@fastspring.com` solicitando la factura.


<!--
## Troubleshoot Gen AI credit issues

| Issue | Solution |
|---|---|
| **Credits tab is not visible** | Gen AI credits have not been purchased or applied to this account. Verify your Agent Orchestrator license in your Adobe Admin Console, then confirm an organization is linked under **[!UICONTROL Billing]** > **[!UICONTROL Subscription]** > **Account details**. |
| **IMS Org ID field is blank** | Your account is not yet linked. Select **[!UICONTROL Link IMS Org]** in the **Account details** card and follow the linking steps above. |
| **Linking fails with an error** | Confirm that you have the Administrator role in both Adobe Learning Manager and the Adobe Admin Console organization you are trying to link. Both checks must pass for the link to be established. |
| **IMS Org ID field is blank after applying an activation key** | Automatic linking occurs only for accounts activated through Adobe's standard ordering flow. For independently set-up accounts, complete the manual linking steps above after activating the key. |
| **After unlinking, Gen AI features are unavailable** | Unlinking removes access to all Gen AI features and hides the Credits tab. Re-link your account to an Adobe Admin Console organization with an active Agent Orchestrator license to restore access. |
-->

<!-- 
# Manage Learning Manager orders and billing

Credit card-based purchase is only available in the [US region](http://learningmanager.adobe.com/).

Manage Learning Manager billing, place orders by using a credit card, subscribe using a Purchase Order, or via a Monthly Active Users plan.

Adobe Learning Manager has a flexible, customer-friendly, and one of the best pricing models to cater to your organization needs. For more information, see the [Learning Manager](https://www.adobe.com/products/learningmanager.html) page.

Only the Administrators of your organization can manage billing.

If you want to contact Adobe for more information about Learning Manager subscription and billing, write to us at [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

## Place orders using credit cards {#placeordersusingcreditcards}

You can buy a subscription for a maximum of 3500 learners through any single credit card payment order. The first order in the account must be for a minimum of 10 learners.

1. On the Administrator app, click **[!UICONTROL Billing]** on the left navigation pane.

   ![](assets/billing.png)

   *Launch Adobe Learning Manager billing*

1. On the **[!UICONTROL Billing Information]** page, add the number of users in the **[!UICONTROL Add Users]** field. When using a credit card for pre-paid subscriptions, you can see the number of users that you can add for the subscription. The number of users you can add must not exceed the number mentioned in the section Remaining.1. 

   ![](assets/billing-page-to-manageyoursubscriptionandorders.png)

   *Add number of users*

1. After specifying the number of users to add, click Place Order in the upper-right corner of the page.

   ![](assets/billing2.png)

1. Review the estimate that appears on the screen.

   ![](assets/pricing-estimate.png)

   *Place an order*

   The annual subscription fee is calculated based on the number of users who are added for the subscription. For example, if four users are being added, the annual fee is calculated using the expression 4 usersX$4X$12, which returns $192.

   Click **[!UICONTROL Proceed]**.

   *Review the estimate*

1. On the Payment Details page, you can view the estimated price of the order. The currency appears based on the current locale.

   ![](assets/payment-details.png)

   *View payment details*

   You can also change the locale by choosing the country from the drop-down list.

   ![](assets/change-locale.png)

   *Select the country of billing*

1. Enter your contact information, choose the credit card type, and provide the details of the credit card. After you've entered the required details, click **[!UICONTROL Complete Order]**.
1. After you've placed the order, to see the recently ordered packages, click the **[!UICONTROL Order History]** tab on the **[!UICONTROL Billing]** page.

   ![](assets/order-history.png)

   *View order history*

## Check order status {#checkorderstatus}

All orders can have one of the four statuses:

**Active:** An order is active, and users are registered successfully.

**Suspended:** An order moves into suspended state in the following scenarios:

* Delay in receipt of payment from the credit card
* Expiry of the credit card.
* Payment is declined for any recurring payment cycle.

**Canceled initiated:** An order moves into this state when the Learning Manager Administrator deactivates the account. The order then moves into a canceled state after receiving the cancellation confirmation of the order.

## Update subscription details {#updatesubscriptiondetails}

1. In the list of orders, click **[!UICONTROL Edit]**.

   ![](assets/update-subsciptiondetailsclickedit.png)

   *Update subscription details*

1. In the Subscription details page, click **[!UICONTROL Edit Subscription]**.
1. Choose the item that you want to edit:

   * Payment method: Use this option to update payment details, such as, credit card.
   * Address: Use this option to update address details.

## Cancel a subscription {#cancelasubscription}

To cancel an order:

1. In the left pane of the Administrator page, click Billing.
1. In the Billing page, on the upper-right corner, choose **[!UICONTROL Actions]** > **[!UICONTROL Deactivate Account]**.
1. Once the Administrator deactivates the account, all existing orders in the account are canceled from the next billing cycle.

When an account is deactivated by the customer, it enters a trial state for the next 30 days. The account owner receives three reminder emails to revive the account. If the owner does not reactivate the account, none of the users are able to access Learning Manager apart from the owner.

## Place orders using Purchase Order {#placeordersusingpurchaseorder}

You can choose purchase order process as an alternative mode of payment. As a pre-requisite, your organization's account must be registered with Adobe. Your organization account is charged for this process. The account is charged based on a learner's activities. Only Learning Object-level activities are charged. To place an order using PO:

1. Send an email to [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com) and mention the number of required learners.
1. The Learning Manager team sends you an activation key.
1. In the Billing page of the Administrator app, enter the activation key.
1. Click Activate in the upper-right corner of the page.

## Check account status {#checkaccountstatus}

After an account gets activated, the account can be in any of the following states:

* **Trial** - You can create an Adobe Learning Manager account and use it without any payment for a period of 30 days. There is no limit on the number of learners registered during the trial period.
* **Active** - In this state, the account has active learner subscriptions with recurring monthly payment as per the subscription order.
* **Inactive** - An account moves into inactive state in the following scenarios:

  * After the trial period if there are no active subscription orders in the account.
  * Administrator deactivates the account, which results in canceling all the existing orders in an account from the next billing cycle of subscription.
  * Payment is declined for active orders in an account even after reminders.

An inactive state does not cancel your account with immediate effect. You receive at least a couple of reminders from the Learning Manager team asking you to provide the latest information about

your credit card if it has expired. In an inactive state, only an administrator can log in to the Captivate

Learning Manager account. All other users cannot access the account.

* **Activation required** - Your account moves into this state when the Learning Manager administrator chooses to deactivate the account. All the orders of this account get canceled. The collection of payment for these orders does not happen from the next billing cycle. The status of the account remains in this state until the day of the last billing cycle. In this state, all users can continue to use the application without any impact until the end of the last recurring payment date.

## Cancel a subscription {#Cancelasubscription-1}

To cancel an active subscription, contact the Learning Manager support team.

## Account termination fee {#accountterminationfee}

If you want to cancel the subscription before the completion of the annual term, an early termination fee is charged. The termination fee is equivalent to 50% of the subscription price of the remaining commitment period.

## Monthly Active Users (MAU) plan {#monthlyactiveusersmauplan}

You can choose a MAU plan as your preferred way of billing. This option generates billing based on the number of monthly unique active users. The monthly unique active users are added cumulatively for a period of 12 months starting from the month of plan activation. This number is used for billing for the period.

Use the following example to understand how MAU is calculated.

Let there be a case where the number of users per month are as follows:

* Month 1 = 50
* Month 2 = 500
* Month 3 = 5000
* Month 4 to 12 = 10

Total Monthly Active Users that are billed = Month 1 + Month 2 + Month 3 + Month 4 to 12 = 50 + 500 + 5000 + 90 = 5640.

The billing for the period would be for 5640 users.

At the end of the 12-month period, the usage count is reset back to zero and a new period for MAU plan starts. You can add multiple activation keys to increase the purchased number of seats.

Any user who performs the following actions or achieves completions due to actions taken by others is considered as a monthly unique active user for that calendar month.

* Consuming a course, learning program or certification.
* Consuming, downloading a Job Aid or course attachments.
* Consuming, downloading or creating personal notes.
* Participating in Social Learning by creating Boards, posts or comments.
* Achieving completions due to External Certificate submission approvals or attendance for a classroom/virtual classroom sessions.

## View usage details {#viewusagedetails}

1. To view the number of active users by month, click **[!UICONTROL View Usage Details]**.

   ![](assets/report-request-usage.png)

   *View active users by month*

1. On the page that displays, you can view the following:

   * **Overall usage:** You can check the total number of active users, users who are consuming Learning Manager in a month, and the number of users who have not yet signed up for any course.

   * **Monthly usage:** You can see a table of unique active users per month.

## Download usage report {#downloadusagereport}

You can also download the data of the number of active users by month and year. To download, click **[!UICONTROL Download Detailed Report]**.

On the **Generate Report Request** dialog, enter the required months and year, and click **[!UICONTROL Generate]**.

![](assets/generate-report-request.png)

*Download active usage report*

If you close the browser window, the download starts the next time you visit Learning Manager.

The reports are saved in the Downloads folder of your browser.

## Cancel a subscription

To cancel an active subscription, contact the Learning Manager support team.

## Frequently Asked Questions {#frequentlyaskedquestions}

+++How to add/remove subscriptions from an account?

To add subscriptions in an account, add the number of users for who you'd like to purchase subscriptions. Then on the upper-right corner, click **[!UICONTROL Place Order]**. Review the estimate and click **[!UICONTROL Proceed]**. Enter your account details and also your credit card details. Then to purchase the subscriptions, click **[!UICONTROL Complete Order]**.

To remove an active subscription, contact the Learning Manager support team.
+++

+++How to change a credit card for subscriptions?

In the **[!UICONTROL Order History]** tab, for an active account, click **[!UICONTROL Edit]**. Then on the Subscription Details page, click **[!UICONTROL Edit Subscription]**. Enter your new credit card details and click **[!UICONTROL Update Payment Method]**.

![](assets/credit-card-details.png)

*View credit card details*
+++

+++How to update the Billing information on Learning Manager?

To update the billing information, follow the steps below:

1. Log in as **Admin** and click **[!UICONTROL Billing]**.
1. In the list of orders, click **[!UICONTROL Edit]**.
1. In the Subscription details page, click **[!UICONTROL Edit Subscription]**.

Choose the item that you want to edit:

1. **[!UICONTROL Payment method]:** Use this option to update payment details, such as, credit card.
1. **[!UICONTROL Address]:** Use this option to update address details.
+++

+++Can I partially cancel a subscription?

No, you cannot cancel a subscription partially. If you need to reduce the number of seats that you have purchased, you can cancel the subscription at the end of the billing cycle and then purchase the number of seats required.
+++

+++How do I get an Invoice for my Credit card payments?

Contact [FastSpring](https://fastspring.com/) to get an invoice for your payments, using one of the following ways:

* Create a service request with FastSpring using the link `https://questionacharge.com`.
* Send an email to FastSpring on `orders@fastspring.com` requesting for the invoice.
-->
