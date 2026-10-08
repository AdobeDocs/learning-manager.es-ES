---
description: Obtenga información sobre cómo los administradores de Learning Manager activan Virtual Coach, supervisan el uso de créditos de la MAU y descargan informes de rendimiento de alumnos
jcr-language: en_us
title: Administrar uso y facturación de Virtual Coach
exl-id: 1f8f6465-51c3-4670-a1c7-9a7dfb091452
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%
---

# Administrar uso y facturación de Virtual Coach

Activa Virtual Coach, supervisa el consumo de créditos del usuario activo mensual (MAU) y descarga informes de rendimiento de alumnos como administrador de Adobe Learning Manager.

## Activar Virtual Coach para su cuenta {#activatevirtualcoach}

Virtual Coach está disponible como complemento de Adobe Learning Manager. Después de la compra, el aprovisionamiento genera una clave de activación que se envía por correo electrónico al administrador de la cuenta.

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Vaya a la página **Facturación** en el panel de navegación izquierdo.
3. En la sección **Entrenador virtual**, introduce la clave de activación que recibiste por correo electrónico.

   ![](/help/migrated/administrators/feature-summary/assets/virtual_coach12.png)
   *Introduzca su clave de activación en la sección Entrenador virtual de la página Facturación para activar la función.*

4. Seleccione **Aplicar**. Virtual Coach está habilitado para su cuenta.

Una vez activada, recibirá una notificación en la aplicación confirmando que la función está activa. Se agregan automáticamente cuatro escenarios de juego de roles de ejemplo a la **biblioteca de contenido** para que los autores puedan comenzar de inmediato.

>[!NOTE]
>
>La clave de activación se genera automáticamente durante el aprovisionamiento y se comparte por correo electrónico. Si no tiene la clave de activación, póngase en contacto con el administrador de éxito de clientes de Adobe Learning Manager.

## Ver saldo de crédito de MAU

Los créditos mensuales de usuario activo (MAU) cuentan el número de alumnos únicos que usan Virtual Coach cada mes.

1. Vaya a la página **Facturación**.
2. En la sección **Entrenador virtual**, seleccione **Ver detalles de uso**.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach22.png)

3. Use el menú desplegable **Seleccionar periodo** para elegir el intervalo de fechas que desea revisar.

   La tabla **Uso general** muestra:

   - **Disponible**: total de créditos MAU comprados.
   - **Usado**: créditos consumidos hasta la fecha.
   - **Restantes**: créditos disponibles para el resto del período del contrato.

   La tabla **Uso mensual** muestra el número de alumnos activos únicos por mes de calendario.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach23.png)

4. Seleccione **Descargar informe detallado** para exportar todos los datos de uso.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach-report-mau-billing-5.png)

## Cómo se consumen los créditos MAU

Un crédito de la unidad MAU se consume cuando un alumno inicia una sesión de Virtual Coach en un mes natural. Las sesiones adicionales del mismo alumno en el mismo mes no consumen créditos adicionales. Los créditos no utilizados al final del período del contrato caducan y no se transfieren.

| Escenario | MAU consumidos |
|---|---|
| Un alumno completa 5 sesiones en enero | 1 |
| El mismo alumno utiliza Virtual Coach en enero y febrero | 2 (1 al mes) |
| 100 alumnos completan cada sesión 1 en enero | 100 |

*Los créditos MAU se cuentan por alumno único y por mes natural, independientemente del número de sesiones que inicie cada alumno.*

**Ejemplo: un solo alumno, varias sesiones.** Sarah lanza cinco sesiones de Entrenador Virtual en enero. Se cuenta como una sola usuaria única para el mes, por lo que se consume 1 MAU independientemente de cuántas veces practique.

**Ejemplo: mismo alumno, varios meses.** Sarah utiliza Virtual Coach tanto en enero (3 sesiones) como en febrero (2 sesiones). Cada mes natural cuenta por separado, por lo que se consumen 2 UMA: 1 para enero y 1 para febrero.

**Ejemplo: varios alumnos, mismo mes.** 100 representantes de ventas inician cada uno una sesión de Entrenador Virtual en enero. Cada alumno único cuenta como un MAU para ese mes, por lo que se consumen 100 MAU.

**Ejemplo: práctica del equipo a lo largo del tiempo.** Tu equipo de 50 personas utiliza Virtual Coach durante todo el año. En un mes en el que solo cinco de las 50 prácticas, se consumen cinco UMA para ese mes; en un mes en el que los 50 vuelven a practicar, 0 UMA adicionales más allá de lo que ya se ha consumido para los alumnos que regresan ese mes, ya que cada alumno solo se cuenta una vez al mes natural, independientemente de cuántas veces practiquen en él.

Para obtener más información sobre los informes de Virtual Coach, vaya a [Informes de Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/virtual-coach-reports.md).
