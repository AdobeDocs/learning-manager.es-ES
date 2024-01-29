---
jcr-language: en_us
title: Añadir ubicaciones de clase
description: Ahora los administradores pueden configurar una biblioteca de ubicaciones de clase. Para cada ubicación de clase, los administradores pueden establecer los metadatos que incluyen el nombre de la ubicación, el límite de puestos, así como información adicional como la dirección URL de la ubicación. A continuación, los autores y los administradores pueden utilizar estas ubicaciones de clase preconfiguradas para configurar eventos de formación dirigidos por un instructor (módulos de clase).
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---



# Classroom

## Resumen

Ahora los administradores pueden configurar una biblioteca de ubicaciones de clase. Para cada ubicación de clase, los administradores pueden establecer los metadatos que incluyen el nombre de la ubicación, el límite de puestos, así como información adicional como la dirección URL de la ubicación. A continuación, los autores y los administradores pueden utilizar estas ubicaciones de clase preconfiguradas para configurar eventos de formación dirigidos por un instructor (módulos de clase).

Puede utilizar las dos maneras siguientes para agregar una ubicación de clase.

## Añadir clase mediante la interfaz de usuario

Puede agregar una ubicación de clase mediante la interfaz de usuario:

1. En la aplicación de administración (la IU para las funciones de administrador), haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]**.

1. Haga clic en **[!UICONTROL Añadir más]** botón.

1. En la **[!UICONTROL Ubicación de clase]** , introduzca la siguiente información:

   * Escriba el **[!UICONTROL Nombre de ubicación de clase]**. Utilice un nombre único. De lo contrario, Learning Manager muestra un mensaje de error.
   * Escriba la descripción de la ubicación en la **[!UICONTROL Información de ubicación]** campo. Este campo es opcional.
   * Escriba el **[!UICONTROL URL de ubicación]**. El alumno puede ver esta información en los detalles de la clase. La dirección URL también puede ser una dirección URL de ubicación de mapas, si es necesario. Éste es un campo opcional.
   * Escriba el número de puestos disponibles en el **[!UICONTROL Límite de asientos]** campo. Esto indica la capacidad del asiento de la clase. Este valor se puede cambiar al crear el evento de formación real dirigido por el instructor.

   ![](assets/add-classroom-location.png)

   *Añadir una ubicación de clase*

Después de añadir la ubicación, el **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]** muestra una lista de las salas de reuniones:

![](assets/list-meeting-rooms.png)

*Ver todas las salas de reuniones*

La lista tiene los siguientes campos:

**[!UICONTROL Nombre de ubicación]** - Nombre de la ubicación de la clase.

**[!UICONTROL Sesiones futuras]** - Número de eventos que se producirán en la ubicación correspondiente. Haga clic en el número para ver los detalles en un cuadro de diálogo.

![](assets/sessions-list.png)

*Ver sesiones futuras*

El cuadro de diálogo muestra los detalles de cada sesión, incluido el nombre de la sesión, el nombre de la formación que incluye la sesión y la programación de la sesión. La hora mostrada se alinea con la zona horaria del sistema del alumno.

La **[!UICONTROL Sesiones futuras]** visualizaciones de campo **cero** cuando la clase no se utiliza para ninguna sesión o cuando la clase está asociada a sesiones anteriores.

**URL de ubicación** - URL que proporcionó al crear la ubicación de clase.

**Información de ubicación** - La información de clase que proporcionó al crear la clase.

## Añadir clase mediante CSV

Como alternativa, puede agregar una o varias ubicaciones de clase importando un archivo CSV que contenga la información de la clase.

En **[!UICONTROL Aplicación de administración]** > **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]**, haga clic en el **[!UICONTROL Importar archivos CSV de ubicaciones]** botón. Vaya a la ubicación que contenga el archivo CSV y seleccione el archivo.

El archivo CSV utiliza estos campos para almacenar detalles sobre una o varias ubicaciones de clase:

* name
* información
* url
* seatLimit

Puede personalizar los encabezados.

El archivo CSV debe contener obligatoriamente todas las columnas en el mismo orden que se especifica aquí.

Después de que el sistema importe el archivo CSV, las ubicaciones se añaden a la biblioteca.

## Buscar clases

Un autor o administrador puede empezar a escribir el nombre de la ubicación para ver los resultados relevantes que empiezan a aparecer. A continuación, un autor o un administrador puede seleccionar una ubicación entre los resultados mostrados. Si no se muestra ninguna ubicación en los resultados de escritura anticipada, el usuario puede agregar el nuevo nombre de ubicación de clase. Tenga en cuenta que este nombre de ubicación creado mediante el flujo de trabajo de creación de sesiones no se añade a la biblioteca de ubicaciones creada por el administrador.

Cuando se añade una clase, la plataforma de aprendizaje también indica si la clase ya está reservada para el período de tiempo mencionado. Incluso proporciona franjas horarias alternativas como sugerencias. Por lo tanto, esto permite al autor ajustar la hora de la reunión si decide utilizar la misma ubicación de clase.

![](assets/classroom-search.png)

*Buscar clases*

## Limitar a una lista predeterminada de instructores

Actualmente, los usuarios pueden agregar cualquier usuario registrado como instructor al crear una sesión de clase o de clase virtual. Esta funcionalidad no se ha modificado en esta versión.

Sin embargo, ahora los administradores tienen una opción adicional para controlar mejor quién se asigna como instructor en la plataforma de aprendizaje. Esto evita que se añada accidentalmente un nuevo instructor al crear una sesión.

## Administrador

Un administrador puede seleccionar la **[!UICONTROL Gestión de instructores]** opción (disponible en **[!UICONTROL Aplicación de administración]** > **[!UICONTROL Configuración]** > **[!UICONTROL General]**) para garantizar que solo los usuarios que sean instructores predeterminados puedan añadirse como instructores para una sesión.

Para configurar un instructor, los administradores pueden seleccionar **[!UICONTROL ADMINISTRAR]** > **[!UICONTROL Usuarios]** para abrir la página Administración de usuarios, seleccione un usuario y, a continuación, asigne la función de instructor al usuario (mediante **[!UICONTROL Acciones]** > **[!UICONTROL Asignar función]**).

## Autor

Si el administrador selecciona la **[!UICONTROL Gestión de instructores]** , un autor solo puede buscar y añadir los usuarios con la función de instructor a las sesiones de clase, las sesiones de clase virtual, las listas de comprobación y los módulos de envío de archivos.

Además, un autor puede:

* Agregar y quitar instructores de las sesiones existentes.
* Añada instructores a las sesiones existentes que ya tengan uno o más instructores.

Por lo tanto, después de que un administrador active la **[!UICONTROL Gestión de instructores]** , solo se pueden añadir como instructores los usuarios con la función de instructor.

>[!NOTE]
>
>Esto no es aplicable al migrar sesiones mediante el archivo CSV de sesiones. En este caso, se puede añadir como instructor a un usuario que no tenga la función de instructor.

## Cancelar la sesión existente

Un autor o administrador puede cancelar una sesión y volver a programarla, si es necesario.

Cuando un usuario cancela una sesión, el sistema envía un correo electrónico de cancelación de la reunión a todos los alumnos e instructores inscritos. El correo electrónico incluye los detalles actualizados de la sesión.

Hay una plantilla llamada **[!UICONTROL Cancelación de sesión]** que ayuda a cancelar una sesión.

En la **[!UICONTROL Instancia del curso]** , cada sesión enumerada en una instancia de curso incluye una opción para cancelar la sesión.

![](assets/cancel-session.png)

*Cancelar una sesión existente*

Al hacer clic en **[!UICONTROL Cancelar sesión]** , aparece un mensaje de advertencia.

En el cuadro de diálogo del mensaje de advertencia, si hace clic en **[!UICONTROL Continuar]**, el sistema cancela la sesión.

El sistema también borra los siguientes detalles después de cancelar una sesión:

* Fecha de inicio de la sesión
* Fecha de finalización del período de sesiones
* Hora de inicio de la sesión
* Hora de finalización de la sesión
* Instructores añadidos a la sesión
* URL de clase virtual
* Ubicación/lugar añadido a la sesión
* Límite de lista de espera añadido por el instructor

## Administrador

En la **[!UICONTROL Instancia del curso]** , un administrador puede cancelar una o varias sesiones. Una vez que el administrador cancela una sesión, el sistema borra todos los detalles de la sesión, excepto el límite de puestos.

Además, un administrador puede:

* Ver los alumnos inscritos y los alumnos en lista de espera de una sesión.
* Dar de baja a los alumnos de un curso con una o varias sesiones canceladas.
* Marcar la asistencia para las sesiones que se cancelan.
* Marcar un curso como completo que contenga una o varias sesiones canceladas.
* Reprogramar una sesión que se canceló.
* Agregar un instructor a una sesión cancelada al reprogramarla.

Tenga en cuenta que, incluso después de la cancelación, los alumnos inscritos en la instancia de formación siguen inscritos. Sus estados de inscripción (incluida la inscripción confirmada, en lista de espera y a la espera de la aprobación del responsable) no cambian. Esto resulta útil porque el administrador puede configurar y volver a programar la sesión cancelada en el futuro.

## Autor

En la **[!UICONTROL Instancia del curso]** , un autor puede cancelar una o varias sesiones. Una vez que el autor cancela una sesión, el sistema borra todos los detalles de la sesión, excepto el límite de puestos.

Por lo tanto, un autor puede utilizar la **[!UICONTROL Cancelar sesión]** vínculos para cancelar una o varias sesiones de clase o sesiones de clase virtual disponibles en la misma instancia del curso o en instancias diferentes.
