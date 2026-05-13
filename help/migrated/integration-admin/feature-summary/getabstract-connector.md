---
description: Conector de getAbstract en Adobe Learning Manager
jcr-language: en_us
title: Conector de getAbstract
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 1%

---


# conector de getAbstract para Adobe Learning Manager

## Introducción

El **conector de getAbstract** está diseñado para clientes empresariales de [getAbstract.com](https://www.getabstract.com/). Permite a los alumnos descubrir y consumir contenido de getAbstract directamente a través de Adobe Learning Manager. El conector también permite a los administradores importar datos de participación de usuarios y realizar el seguimiento de los registros de finalización de alumnos automáticamente.

Adobe Learning Manager quiere ofrecer a los alumnos oportunidades de aprendizaje autodirigidas y continuas centradas en el liderazgo y las habilidades sociales y sociales. En lugar de desarrollar todo el contenido internamente, el administrador conecta la cuenta de getAbstract de la organización a Adobe Learning Manager mediante el conector de getAbstract.

- Importa automáticamente contenido de getAbstract a Adobe Learning Manager.
- Realiza un seguimiento del consumo de cursos y rutas de aprendizaje por parte del alumno.

Este artículo describe los pasos para configurar y administrar el conector de getAbstract en Adobe Learning Manager.

## Requisitos previos

- Asegúrese de que la característica **Migración** esté habilitada para su cuenta antes de configurar el conector.
- Obtenga el **ID de cliente** y el **Secreto de cliente** de su representante de cuentas de getAbstract. Estas credenciales son necesarias para recuperar los metadatos del curso y los datos de consumo del usuario.

## Configurar el conector de getAbstract

El conector de getAbstract permite a los administradores de Adobe Learning Manager mejorar la experiencia de aprendizaje mediante la integración de contenido seleccionado de alta calidad de getAbstract.

Para configurar el conector de getAbstract:

1. Inicie sesión como administrador de integración.
2. Seleccione **getAbstract** en la página principal.
3. Seleccione una de las siguientes opciones en el mosaico **Connector**:

   - **Introducción**: Descripción general del conector.
   - **Conectar**: Cree una nueva conexión.
   - **Administrar conexiones**: Ver o modificar conexiones existentes.

   ![](assets/getabstract-connector1.png)
   El mosaico _getAbstract muestra tres opciones de configuración_

## Crear una nueva conexión

Para crear una nueva conexión:

1. Seleccione **Conectar**.

   ![](assets/getabstract-connector2.png)
   _Seleccione Conectar en el icono getAbstract para crear una nueva conexión_

2. Escriba un **Nombre de conexión**.
3. Escriba el **ID de cliente** y el **Secreto de cliente**.

   ![](assets/getabstract-connector3.png)
   _Escriba la conexión, ID de cliente y secreto de cliente en la página de conexión getAbstract_

4. Seleccione **Guardar** para crear la conexión.

## Administrar el conector de getAbstract

Antes de importar datos, debe configurar el conector y una programación de sincronización. Una vez configurado, el conector extrae automáticamente los datos de uso, lo que le permite supervisar el progreso del alumno e incluir contenido de getAbstract en los planes e informes de aprendizaje.

### Habilitar la conexión

Para habilitar la conexión:

1. Seleccione **Administrar conexiones** en el mosaico **getAbstract**.

   ![](assets/getabstract-connector4.png)
   _Administrar conexiones para configurar y programar la importación de datos_

2. Seleccione la conexión.
3. Seleccione **Configurar** en el panel de navegación izquierdo.
4. Seleccione **Habilitar conexión** y, a continuación, seleccione **Guardar**.

   ![](assets/getabstract-connector5.png)
   _Habilite la conexión para importar los datos de getAbstract en Adobe Learning Manager_

### Editar la conexión

Para editar la conexión:

1. Seleccione **Administrar conexiones** en el mosaico **getAbstract**.
2. Seleccione la conexión.
3. Seleccione **Configurar** en el panel de navegación izquierdo.
4. Seleccione **Editar** para actualizar el **Id. de cliente** y el **Secreto de cliente**.

   ![](assets/getabstract-connector6.png)
   _Edite las credenciales, incluido el ID y el secreto de cliente_

5. Seleccione **Guardar**.

### Programar sincronización

Para programar la sincronización:

1. Seleccione **Administrar conexiones** en el mosaico **getAbstract**.
2. Seleccione la conexión.
3. Seleccione **Configurar** en el panel de navegación izquierdo.
4. Seleccione **Habilitar programación** en la sección **Programar sincronización**.

   ![](assets/getabstract-connector7.png)
   _Programar la importación de datos de getAbstract en Adobe Learning Manager_

5. Seleccione la fecha y hora de inicio en UTC.
6. Escriba el número de días tras los cuales debe repetirse la sincronización.
7. Seleccione **Guardar**.

La configuración de sincronización se guarda. El conector se ejecutará según la programación e importará datos de getAbstract en Adobe Learning Manager.

## Ejecutar sincronización a petición

La opción **Sincronización a petición** le permite importar manualmente datos de getAbstract en Adobe Learning Manager. Esto resulta útil cuando desea actualizar los datos de actividad del alumno inmediatamente, sin esperar a la siguiente sincronización programada.

Para ejecutar la importación de datos a petición:

1. Seleccione **Administrar conexiones** en el mosaico **getAbstract**.
2. Seleccione la conexión.
3. Seleccione **Ejecución a petición** en el panel izquierdo.
4. Seleccione **Fecha de inicio**.

   ![](assets/getabstract-connector8.png)
   _Ejecutar la solicitud a petición para importar datos inmediatamente de getAbstract a Adobe Learning Manager_

5. Seleccione una de las opciones siguientes:

   - **Deshabilitar el acceso a Adobe Learning Manager durante la ejecución**: Se recomienda si la sincronización puede causar tiempo de inactividad.
   - **Habilitar acceso a Adobe Learning Manager durante la ejecución**: Recomendado para evitar la interrupción del servicio.
6. Seleccione **Ejecutar** para importar todos los datos desde la fecha de inicio hasta el presente.

### Ver historial de ejecución

La página **Estado de ejecución** muestra todas las ejecuciones de sincronización en orden. Si una ejecución tiene errores, aparece un icono de advertencia. Puede comprobar el registro de errores, corregir el archivo CSV y volver a ejecutar la sincronización más reciente si es necesario.

Para ver el historial de ejecuciones:

1. Seleccione **Estado de ejecución** en el panel izquierdo.
2. Puede ver las siguientes columnas:
   - **Ejecutar**
   - **Fecha de inicio**
   - **Duración**
   - **Tipo** (Programado o Bajo demanda)
   - **Estado** (En curso o Completado)

   ![](assets/getabstract-connector9.png)
   _Ver el estado de ejecución de las importaciones bajo demanda y programadas_

>[!NOTE]
>
>Si elimina y vuelve a crear una conexión, el historial de ejecución de las ejecuciones anteriores seguirá siendo visible. Sólo puede volver a ejecutar la última sincronización.

### Requisitos para una sincronización correcta

Para asegurarse de que la sincronización funciona correctamente:

- Un archivo de fuente de usuario válido debe estar en la carpeta FTP de getAbstract para las fechas de sincronización especificadas.
- El archivo debe tener el siguiente formato de nombre:
   - report_export_yyyy_MM_dd_HHmmss.xlsx o,
   - report_export_yyyy_MM_dd.xlsx

Descargue un [archivo de fuente de usuario de getAbstract de muestra](https://experienceleague.adobe.com/docs/learning-manager/assets/report-export-20170401175342.xlsx?lang=es) para comprender el formato.
