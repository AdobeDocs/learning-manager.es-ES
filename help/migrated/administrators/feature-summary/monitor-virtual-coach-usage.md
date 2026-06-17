---
jcr-language: en_us
title: Supervisar el uso de Virtual Coach
description: Supervise cómo utiliza Virtual Coach su cuenta.
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 2%

---


# Supervisar el uso de Virtual Coach

Visualiza los datos de uso de Virtual Coach, realiza un seguimiento del consumo de créditos del usuario activo mensual (MAU) y accede a los informes de rendimiento de los alumnos en Adobe Learning Manager.

## Activar Virtual Coach para su cuenta

Virtual Coach está disponible como complemento de Adobe Learning Manager. Después de la compra, el aprovisionamiento genera una clave de activación que se envía por correo electrónico al administrador de la cuenta.

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Vaya a la página **Facturación** en el panel de navegación izquierdo.
3. En la sección **Entrenador virtual**, introduce la clave de activación que recibiste por correo electrónico.
4. Seleccione **Aplicar**. Virtual Coach está habilitado para su cuenta.
   ![](assets/virtual-coach-037.png)

Una vez activada, recibirá una notificación en la aplicación confirmando que la función está activa. Se añaden automáticamente cuatro escenarios de reproducción de roles de ejemplo a la biblioteca de contenido para que los autores puedan empezar de inmediato.

>[!NOTE]
>
>La clave de activación se genera automáticamente durante el aprovisionamiento y se comparte por correo electrónico. Si no dispone de la clave de activación, póngase en contacto con su administrador de éxito de clientes (CSM) de Adobe Learning Manager.

## Ver el saldo de crédito de MAU

Los créditos mensuales de usuario activo (MAU) cuentan el número de alumnos únicos que usan Virtual Coach cada mes.

1. Vaya a la página **Facturación**.
2. En la sección **Entrenador virtual**, seleccione **Ver detalles de uso**.
3. Use el menú desplegable **Seleccionar periodo** para elegir el intervalo de fechas que desea revisar.
   ![](assets/virtual-coach-038.png)

   La tabla **Uso general** muestra:

   a. **Disponible:** Créditos de MAU comprados\
   b. **Usado:** Créditos consumidos hasta la fecha\
   c. **Créditos restantes:** Créditos disponibles para el resto del período del contrato

   La tabla **Uso mensual** muestra el número de alumnos activos únicos por mes de calendario.

4. Seleccione **Descargar informe detallado** para exportar todos los datos de uso.

## Cómo se consumen los créditos MAU

El crédito de la unidad MAU se consume cuando un alumno finaliza una sesión de Virtual Coach en un mes natural. Las sesiones adicionales del mismo alumno en el mismo mes no consumen créditos adicionales.

| Escenario | MAU consumidos |
|----------|--------------|
| Un alumno completa 5 sesiones en enero | 1 |
| El mismo alumno utiliza Virtual Coach en enero y febrero | 2 (1 al mes) |
| 100 alumnos completan cada sesión 1 en enero | 100 |

_Los créditos MAU se cuentan por alumno único y por mes natural, independientemente del número de sesiones que complete cada alumno._

Los créditos no utilizados al final del período del contrato caducan y no se transfieren.

### Ejemplo 1: Un solo alumno, varias sesiones

Escenario: Sarah completa cinco sesiones de Entrenador Virtual en enero.

* Sesiones en enero: 5
* UMA consumidas: 1
* Por qué: Sarah se cuenta como un único usuario único para el mes de enero, independientemente de cuántas veces practique.

### Ejemplo 2: El mismo alumno, varios meses

Escenario: Sarah utiliza Virtual Coach tanto en enero como en febrero.

* Sesiones en enero: 3
* Sesiones en febrero: 2
* UMA consumidas: 2 (1 para enero + 1 para febrero)
* Por qué: Cada mes natural cuenta por separado.

### Ejemplo 3: Varios alumnos, el mismo mes

Escenario: 100 representantes de ventas completan cada una de las sesiones de Virtual Coach en enero.

* Total de sesiones: CIEN
* UMA consumidas: CIEN
* Por qué: Cada alumno único cuenta como un MAU para ese mes.

### Ejemplo 4: Práctica de equipo a lo largo del tiempo

Escenario: Tu equipo de 50 personas utiliza Virtual Coach durante todo el año.

| Mes | Alumnos activos | MAU consumidos este mes | UMA acumulativos |
|------|----------------|--------------------------|-----------------|
| enero | 0 | 0 | 0 |
| febrero | 5 (5 personas no practicaron) | 5 | 5 |
| Marzo | 0 (todos los 50 ganancia practicada) | 0 | 45 |
| Abril | 0 | 0 | 75 |

## Ver informes de Virtual Coach

La página **Administrar** sección > **Informes** sección > **Informes de AI** proporciona datos de uso y rendimiento para todas las actividades de Virtual Coach en su organización. Hay dos informes disponibles bajo el encabezado **Entrenador virtual**.

Todos los informes se exportan en formato CSV. La generación de informes puede tardar varios minutos, dependiendo del tamaño de los datos.

### Resumen de uso del alumno

Contiene datos de uso mensuales de todos los alumnos. Utilice este informe para realizar un seguimiento de cuántos alumnos utilizan Virtual Coach cada mes, supervisar el consumo de créditos de la UMA e identificar las tendencias de participación a lo largo del tiempo.

### Detalles de la sesión

Contiene datos de nivel de sesión de todos los alumnos durante los últimos 90 días. Utilice este informe para revisar las puntuaciones de sesiones individuales, la cobertura de temas y las métricas de estilo de la población de alumnos, así como para identificar carencias de habilidades que puedan requerir formación o contenido adicional.

## Acceso y descarga de un informe

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **Informes** en el panel de navegación izquierdo.
3. Seleccione **Informes de inteligencia artificial**.
4. En la sección **Entrenador virtual**, seleccione el informe que desea descargar, **Resumen de uso del alumno** o **Detalles de la sesión**.
   ![](assets/virtual-coach-039.png)
5. Seleccione el intervalo de fechas cuando se le solicite y, a continuación, seleccione **Continuar**.
6. El informe se descarga automáticamente como archivo CSV.
