---
description: Aprenda a integrar el conector de LinkedIn Learning con Adobe Learning Manager
jcr-language: en_us
title: Conector de LinkedIn Learning
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 1%

---


# Conector de linkedIn Learning en Adobe Learning Manager

## Introducción

El conector de LinkedIn Learning le permite integrar perfectamente el contenido de LinkedIn Learning con Adobe Learning Manager. Con este conector, las organizaciones pueden incorporar automáticamente cursos de LinkedIn Learning a Adobe Learning Manager para que los alumnos puedan buscar, inscribirse y completar cursos de LinkedIn directamente en la plataforma.

Cuando se configura, se realiza un seguimiento del progreso del alumno en el contenido de LinkedIn Learning en Adobe Learning Manager, lo que permite a los administradores supervisar las finalizaciones y el tiempo dedicado. Puede programar la sincronización automática del contenido, ejecutar importaciones a petición y filtrar los cursos que se importan al sistema por idioma, biblioteca o etiquetas personalizadas.

>[!NOTE]
>
>Al importar cursos de LinkedIn Learning, Adobe Learning Manager genera ID únicos de objeto de aprendizaje para cada curso. La plataforma LinkedIn informa a Adobe Learning Manager sobre el tiempo de aprendizaje dedicado al contenido de LinkedIn Learning. Si la plataforma LinkedIn no envía estos datos, Adobe Learning Manager no los puede registrar y el tiempo empleado se mostrará como cero.

## Configurar las opciones del portal de LinkedIn Learning

Para configurar las opciones del portal de LinkedIn Learning:

1. Inicie sesión como administrador en **LinkedIn Learning LMS**.
2. Seleccione **Administrador** en el panel de navegación superior.
3. Haga clic en la ficha **Configuración**.
4. En la barra de navegación izquierda, selecciona **Integración de reproducción** y, a continuación, selecciona la pestaña **Integración**.
5. Expanda **Configuración de inicio de contenido de LMS**.
6. Agregue los siguientes nombres de host:

   - learningmanager.adobe.com
   - learningmanagerlrs.adobe.com
   - cpcontents.adobe.com
7. Seleccione **Habilitar integración AICC**.

   ![](assets/linkedin-connector1.png)
   _Seleccione Habilitar integración AICC para configurar el conector de LinkedIn Learning_

## Conectar el aprendizaje de LinkedIn en Adobe Learning Manager

Para configurar el conector de LinkedIn Learning:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el icono de **LinkedIn Learning** y seleccione **Connect**.

   ![](assets/linkedin-connector2.png)
   _Seleccione Conectar para configurar el conector de LinkedIn Learning_

3. En la página de configuración de la conexión:
   - Escriba un **Nombre de conexión**.
   - Escriba **Clave de aplicación** y **Clave secreta**.

   ![](assets/linkedin-connector3.png)
   _Escriba el nombre de conexión, la clave de aplicación y la clave secreta para configurar el conector de LinkedIn Learning_

   >[!NOTE]
   >
   >El administrador de la empresa puede generar estas claves creando una aplicación en el portal de administración de aprendizaje de LinkedIn.

4. Seleccione **Guardar** para agregar la conexión.

Para editar una conexión existente, seleccione **Administrar conexiones** en el icono **LinkedIn Learning**.

>[!IMPORTANT]
>
>La característica **Migración** debe estar habilitada para su cuenta antes de que pueda configurar este conector.


## Administrar conexión y sincronización

Para administrar el conector de LinkedIn Learning:

1. Seleccione **Administrar conexiones** y elija la conexión.
2. En el panel izquierdo, seleccione **Configurar**.
3. Seleccione **Habilitar conexión**.

   ![](assets/linkedin-connector4.png)
   _Seleccione Habilitar conexión en la página Configurar conector de LinkedIn Learning_

4. Seleccione **Editar** para actualizar las credenciales. Use **Restablecer** para deshacer las ediciones.
5. Para automatizar la sincronización, seleccione **Habilitar programación**.
6. Establezca la fecha, hora y frecuencia de inicio (por ejemplo, cada 3 días).
7. Seleccione **Guardar**.

### Sincronización bajo demanda

Para ejecutar la sincronización a petición:

1. Seleccione **Ejecución a petición** en el panel izquierdo.
2. Escriba una **Fecha de inicio**.
3. Seleccione cualquiera de las siguientes opciones para **Habilitar** o **Deshabilitar el acceso** a Adobe Learning Manager durante la ejecución:
   - **Habilitar acceso a Adobe Learning Manager durante la ejecución**: Sin tiempo de inactividad para los usuarios.
   - **Deshabilitar el acceso a Adobe Learning Manager durante la ejecución**: La aplicación no está disponible durante la sincronización.

   ![](assets/linkedin-connector5.png)
   _Seleccionar ejecución a petición para ejecutar la importación_

4. Selecciona **Ejecutar** para importar fuentes de usuario y datos de LinkedIn Learning a partir de esa fecha.

Para supervisar todas las ejecuciones de sincronización:

Seleccione **Estado de ejecución** en el panel izquierdo para ver el historial de todas las sincronizaciones, su duración, tipo (programado o a petición) y estado actual (en curso, completado).

>[!NOTE]
>
>Si elimina y vuelve a crear una conexión, las ejecuciones anteriores se conservan y se muestran en **Estado de ejecución**. Solo puede volver a ejecutar la sincronización más reciente.

## Filtrar contenido de LinkedIn Learning

Al configurar el conector, puede filtrar los cursos de LinkedIn Learning que desea importar.

Para configurar el filtro:

1. Seleccione **Filtro** en el panel izquierdo.
2. Seleccione la opción requerida en **Filtrar cursos de formación mediante**.
   - **Sin filtro**: importar todos los cursos.
   - **Idioma**: filtrar cursos por idiomas específicos.
   - **Biblioteca**: filtrar cursos por bibliotecas de aprendizaje de LinkedIn.
3. Si filtra por **Idioma**, seleccione los idiomas que desee. Por ejemplo, **inglés** y **español**.
4. En **Importar cursos de formación a**, seleccione dónde se importarán los cursos.
5. Elija cómo organizar los cursos importados.
6. Seleccione cualquiera de las opciones siguientes para **Segregar cursos de formación basados en la opción**:

   - **Idioma**: agrupar por idioma.
   - **Biblioteca**: agrupar por biblioteca.
7. En **Importar etiquetas**, seleccione los tipos de etiquetas que desea aplicar a los cursos importados.

   - **Idioma**
   - **Biblioteca**
   - **Asunto**
   - **Tema**
   - **Etiqueta personalizada**
8. En el campo **Etiqueta personalizada**, escriba la etiqueta personalizada que desea asignar. Separe las etiquetas con comas.

   ![](assets/linkedin-connector6.png)
   _Seleccionar opciones de filtro para importar los datos desde el conector de LinkedIn Learning_

9. Si quieres que los alumnos puedan darse de baja de estos cursos, selecciona **Los usuarios pueden darse de baja**.
10. Selecciona **Guardar** para aplicar tu filtro e importar la configuración.
