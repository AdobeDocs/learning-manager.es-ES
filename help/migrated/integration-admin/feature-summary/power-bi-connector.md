---
description: Aprenda a integrar el conector de Power BI con Adobe Learning Manager
jcr-language: en_us
title: Conector de Power BI
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# Conector de Power BI en Adobe Learning Manager

## Introducción

El conector de Power BI le permite integrar Adobe Learning Manager con Microsoft Power BI (licencia comercial) para que pueda analizar, visualizar y compartir sus datos de aprendizaje.

Con esta integración, el administrador de integración puede exportar automáticamente conjuntos de datos en directo, como transcripciones de alumnos, aptitudes de usuarios e informes de actividad de xAPI, directamente a un espacio de trabajo de Power BI seleccionado.

Una vez conectado, puede utilizar todas las capacidades de Power BI para crear paneles e informes personalizados. Esto ayuda a tu organización a obtener información más detallada sobre el progreso de los alumnos, los logros en habilidades y la eficacia de la formación, así como a tomar decisiones fundamentadas basadas en datos de aprendizaje en tiempo real.

>[!NOTE]
>
>Adobe Learning Manager solo se integra con la versión comercial de Microsoft Power BI. No se admite la integración con la versión de Government Cloud.

## Requisitos previos

- Solo se admite la Power BI de Microsoft con **licencia comercial**.
- Asegúrese de tener permiso para crear aplicaciones y espacios de trabajo de Power BI.
- Obtenga su **Nombre de inquilino**, **Id. de cliente de aplicación**, **Secreto de cliente de aplicación** y **Id. de área de trabajo** (opcional).

## Configurar el conector de Power BI

Para conectar ALM con Power BI:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el icono del conector **Power BI** y seleccione **Conectar**.

   ![](assets/power-bi-connector1.png)
   _Seleccionar Conectar para configurar el conector de Power BI_

3. Escriba los siguientes datos:

   - ID de cliente
   - Secreto de cliente
   - Nombre del inquilino
   - Id. de espacio de trabajo (opcional)

   ![](assets/power-bi-connector2.png)
   _Escriba los detalles necesarios para configurar Power BI_

4. Seleccione **Conectar**.

## Registrar la aplicación de Power BI

Para registrar la aplicación de Power BI:

1. Vaya a [Registrar la aplicación de Power BI](https://app.powerbi.com/embedsetup).
2. Selecciona **Incrustar para tu organización** e inicia sesión en tu cuenta de Microsoft.
3. Escriba un nombre para la aplicación.
4. Seleccione **Aplicación web del servidor** en **Tipo de aplicación**.
5. En la sección **URL de redirección**, selecciona **Usar una URL personalizada** y escribe [esta URL](https://learningmanager.adobe.com/ctr/app/azure/_callback): (Reemplace el dominio si es necesario para su entorno.)
6. En el campo **URL principal**, escriba [esta dirección URL](https://learningmanager.adobe.com/).
7. En la sección **Permisos**, seleccione **Leer todos los conjuntos de datos** y **Leer y escribir todos los conjuntos de datos**.
8. Póngase en contacto con el administrador del Power BI para obtener el **nombre del inquilino**.
9. Si no dispone de un ID de espacio de trabajo, cree un espacio de trabajo en Power BI (requiere Power BI Pro) y copie el ID de la URL.
10. Seleccione **Registrar aplicación** y guarde el **ID de cliente** y el **Secreto de cliente** para su uso posterior.

>[!NOTE]
>
>Si necesita volver a autorizar la conexión más adelante, cree una nueva aplicación de Power BI y use la dirección URL de redirección correcta para su entorno.

## Exportar informes a Power BI

Después de configurar la conexión, puede exportar estos informes:

- **Transcripciones de alumnos**
- **Aptitudes del usuario**
- **Informes de actividad de xAPI**
- **Informes unificados** (una combinación de varios informes)

### Transcripciones de alumnos

#### Programar exportaciones

1. Seleccione **Transcripciones de alumnos** en el panel izquierdo.
2. Seleccione **Habilitar programación** en la página Exportar.
3. Seleccione **fecha de inicio** y **hora**.
4. Defina el **intervalo** para la frecuencia con la que debe repetirse la exportación (diaria, semanal, etc.).

   ![](assets/power-bi-connector3.png)
   _Habilitar la exportación programada para la transcripción del alumno_

5. Seleccione **Guardar**.

#### Exportar a petición

- Puede generar informes manualmente especificando la **fecha de inicio** y ejecutando una exportación a petición.
- El informe incluirá datos desde la fecha especificada hasta el presente.

### Aptitudes del usuario

#### Programar exportaciones

1. Seleccione **Aptitudes del usuario** en el panel izquierdo.
2. Seleccione **Habilitar programación** en la página Exportar.
3. Seleccione **fecha de inicio** y **hora**.
4. Defina el **intervalo** para la frecuencia con la que debe repetirse la exportación (diaria, semanal, etc.).

   ![](assets/power-bi-connector4.png)
   _Habilitar la exportación programada del informe de aptitudes de usuarios_

5. Seleccione **Guardar**.

#### Exportar a petición

- Puede generar informes manualmente especificando la **fecha de inicio** y ejecutando una exportación a petición.
- El informe incluirá datos desde la fecha especificada hasta el presente.

### Administrar informes de actividad de xAPI

**Las instrucciones xAPI** también se pueden exportar a Power BI.

#### Configurar exportaciones de xAPI

1. Seleccione **Exportar informe de actividad de xAPI**.
2. Seleccione **Configuración** en el panel izquierdo.

   - Rellene los campos de la ruta JSON para que coincidan con sus columnas CSV.
   - Seleccione **Agregar** para incluir más rutas.
   - Use **Editar** para actualizar los campos.
3. Seleccione **Guardar**.

#### Programar exportaciones

1. Seleccione **Configurar programación**.
2. Seleccione **Habilitar exportación de instrucciones xAPI usando esta conexión**.
3. Establezca la **fecha de inicio**, **hora** e **intervalo**.
4. Seleccione **Guardar**.

#### Exportación a petición

1. Seleccione **A petición**.
2. Especifique la **fecha de inicio**.
3. Seleccione **Ejecutar**.

>[!NOTE]
>
>Si algunas instrucciones xAPI del almacén de registros de aprendizaje (LRS) carecen de rutas JSON configuradas, sus valores aparecerán como N/A en Power BI.

#### Ver estado de ejecución

- Utilice **Estado de ejecución** para ver el historial de exportaciones, incluidas la hora de inicio, la duración y el estado.
- Un icono de advertencia indica ejecuciones con errores. Haga clic en el vínculo para descargar informes de errores como .CSV.

### Informes unificados

**Informes unificados** combinan datos de:

- Transcripciones de alumnos
- Interacción
- Informe de comentarios
- Inicio de sesión/Acceso
- Aptitud de usuario
- Informe de usuario
- Informe de curso de formación

Esto le ayuda a crear paneles más eficaces mediante la combinación de datos en Power BI.

#### Crear configuración de informe unificada

1. Seleccione **Informes unificados** y, a continuación, seleccione **Configuración**.
2. Escriba un nombre único en el campo **Nombre del conjunto de datos**.
3. Seleccione uno o varios informes que desee incluir en este conjunto de datos en **Seleccionar informes para exportación de datos**.

   - Transcripciones de alumnos
   - Inicio de sesión/Acceso
   - Informe de curso de formación
   - Interacción
   - Aptitud de usuario
   - Informe de comentarios
   - Informe de usuario
4. Utilice el campo **Agregar filtros de grupos de usuarios** para seleccionar los datos de grupos de usuarios que desea exportar. De forma predeterminada, se selecciona **Todos los usuarios**.
5. Utilice el campo **Agregar filtros de catálogo de contenido** para filtrar informes por catálogo de contenido.
6. La tabla de filtros muestra qué informes admiten los filtros **Grupo de usuarios**, **Catálogo** o **Hora**.

   ![](assets/power-bi-connector5.png)
   _Crear una configuración para informes unificados_

7. Después de seleccionar informes y filtros, selecciona **Guardar** en la parte superior derecha.

#### Filtrar transcripciones de alumnos por estado

- **Todos:** Todos los registros del intervalo de fechas
- **Completado:** Solo actividades de aprendizaje completadas
- **En curso:** Solo actividades en curso
- **No iniciado:** Excluye los registros que aún no se han iniciado
- **Dado de baja:** Incluye registros dados de baja

## Descargar plantillas de Power BI

Adobe proporciona plantillas de Power BI listas para usar que le ayudarán a empezar rápidamente.

- Descargue plantillas, importe sus informes y personalícelos según sea necesario.
- Utiliza plantillas para crear paneles atractivos sin empezar desde cero.

## Configuración relacionada con la ruta de aprendizaje

El aspecto de **rutas de aprendizaje** en los informes depende de la configuración del administrador:

- **Conexiones existentes:**

   - Si **Ruta de aprendizaje** está deshabilitada, no se incluyen filas ni columnas relacionadas.
   - Si se habilita, el informe incluye la ruta de aprendizaje (nivel superior) de los alumnos inscritos.

- **Nuevas conexiones:**

   - Si Ruta de aprendizaje está desactivada, las columnas muestran:

      - **Ruta incrustada:** nombre del programa de aprendizaje.
      - **Id. de ruta incrustada:** Id. del programa de aprendizaje.
      - **ID de curso incrustado:** ID de cursos en la ruta de aprendizaje.
   - Si está habilitada, la columna **Tipo** usa la ruta de aprendizaje (nivel superior) donde corresponda.
   - Para las nuevas conexiones, los cambios se aplican después de 30 días.

### Dónde ver los datos**

Todos los datos exportados aparecen como conjuntos de datos en su cuenta de Power BI. Úsalos para crear paneles y visualizaciones personalizados.
