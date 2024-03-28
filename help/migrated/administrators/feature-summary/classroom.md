---
jcr-language: en_us
title: Añadir ubicaciones de clases
description: Los administradores pueden crear ahora una biblioteca de ubicaciones de clases. Para cada ubicación de clase, los administradores pueden establecer los metadatos que incluyen el nombre de la ubicación, el límite de puestos e información adicional como, por ejemplo, la dirección URL de la ubicación. Los autores y los administradores pueden utilizar estas ubicaciones de clases preconfiguradas para establecer eventos de formación dirigidos por un instructor (módulos de clase).
contentowner: saghosh
exl-id: 51a1e38f-d4e2-4c19-bbf7-6696505c0dfd
source-git-commit: b882c22da029cdc4c8bcc4ab1b6d861f06f83f0f
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 77%

---

# Clase

## Información general

Los administradores pueden crear ahora una biblioteca de ubicaciones de clases. Para cada ubicación de clase, los administradores pueden establecer los metadatos que incluyen el nombre de la ubicación, el límite de puestos e información adicional como, por ejemplo, la dirección URL de la ubicación. Los autores y los administradores pueden utilizar estas ubicaciones de clases preconfiguradas para establecer eventos de formación dirigidos por un instructor (módulos de clase).

Puede utilizar los siguientes dos métodos para añadir una ubicación de clase.

## Añadir una clase mediante la interfaz de usuario

Puede agregar una ubicación de clase mediante la interfaz de usuario:

1. En la aplicación de administración (la IU para las funciones de administrador), haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]**.

1. Haga clic en **[!UICONTROL Añadir]** > **[!UICONTROL Nueva ubicación]**.

1. En el cuadro de diálogo **[!UICONTROL Ubicación de clase]**, introduzca la siguiente información:

   * Escriba el **[!UICONTROL Nombre de ubicación]**. Utilice un nombre exclusivo. De lo contrario, Learning Manager mostrará un mensaje de error.
   * Introduzca la descripción de la ubicación en el campo **[!UICONTROL Información de ubicación]**. Este campo es opcional.
   * Introduzca la **[!UICONTROL URL de ubicación]**. El alumno puede ver esta información en los detalles de la clase. La dirección URL también puede ser una URL de ubicación de mapa, si es necesario. Se trata de un campo opcional.
   * Escriba y seleccione la **[!UICONTROL Región de ubicación]**. Este campo es opcional.
   * Introduzca el número de puestos disponibles en el campo **[!UICONTROL Límite de puestos]**. Esto indica el número de puestos disponibles para la clase. Este valor se puede modificar al crear el evento real de formación dirigido por un instructor.

   ![](assets/add-classroom-location.png)

   *Añadir una ubicación de clase*

Después de añadir la ubicación, el **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]** muestra una lista de las salas de reuniones:

![](assets/list-meeting-rooms.png)

*Ver todas las salas de reuniones*

La lista presenta los siguientes campos:

**[!UICONTROL Nombre de ubicación]** - Nombre de la ubicación de la clase.

**[!UICONTROL Sesiones futuras]** - Número de eventos que se producirán en la ubicación correspondiente. Haga clic en el número para ver los detalles en un cuadro de diálogo.

![](assets/sessions-list.png)

*Ver sesiones futuras*

En el cuadro de diálogo, se muestran los detalles de cada sesión, incluidos el nombre y el horario de la sesión, además del nombre del curso de formación que incluye la sesión. La hora mostrada se ajusta a la zona horaria del sistema del alumno.

La **[!UICONTROL Sesiones futuras]** visualizaciones de campo **cero** cuando la clase no se utiliza para ninguna sesión o cuando la clase está asociada a sesiones anteriores.

**[!UICONTROL Límite de asientos]** - Muestra la capacidad del asiento de la clase.

**URL de ubicación** - URL que proporcionó al crear la ubicación de clase.

**Información de ubicación** - La información de clase que proporcionó al crear la clase.

## Añadir clase mediante CSV

También puede añadir una o varias ubicaciones de clases mediante la importación de un archivo CSV que contenga la información de clase.

En **[!UICONTROL Aplicación de administración]** > **[!UICONTROL Configuración]** > **[!UICONTROL Ubicaciones de clase]** > **[!UICONTROL Añadir]**, haga clic en el **[!UICONTROL Ubicaciones de importación masiva]** botón. Desplácese a la ubicación que contiene el archivo CSV y selecciónelo.

El archivo CSV utiliza estos campos para almacenar información sobre una o varias ubicaciones de clases:

* name
* info
* url
* seatLimit

Puede personalizar los encabezados.

El archivo CSV debe contener obligatoriamente todas las columnas en el mismo orden especificado aquí.

Una vez que el sistema importe el archivo CSV, las ubicaciones se añadirán a la biblioteca.

## Buscar clases

Un autor o un administrador pueden iniciar la escritura del nombre de la ubicación para que empiecen a aparecer los resultados correspondientes. A continuación, el autor o el administrador pueden seleccionar una ubicación en los resultados mostrados. Si no se muestra ninguna ubicación en los resultados de escritura anticipada, el usuario puede añadir el nombre de la nueva ubicación de clase. Tenga en cuenta que este nombre de ubicación establecido durante el flujo de trabajo de creación de sesiones no se ha añadido a la biblioteca de ubicaciones creada por el administrador.

Al añadir una clase, la plataforma de aprendizaje indica también si esta ya se ha reservado para el periodo indicado. Incluso ofrece sugerencias de horarios alternativos. Por lo tanto, esto permite al autor ajustar la hora de la reunión si decide utilizar la misma ubicación de clase.

![](assets/classroom-search.png)

*Buscar clases*

## Limitar a una lista predeterminada de instructores

Actualmente, los usuarios pueden añadir a cualquier usuario registrado como instructor al crear una sesión de clase o de clase virtual. Esta función permanece invariable en esta versión.

Sin embargo, los administradores cuentan ahora con una opción adicional para controlar de forma más eficaz quién se asigna como instructor en la plataforma de aprendizaje. Esto impide la adición accidental de un nuevo instructor al crear una sesión.

## Administrador

Un administrador puede seleccionar la **[!UICONTROL Gestión de instructores]** opción (disponible en **[!UICONTROL Aplicación de administración]** > **[!UICONTROL Configuración]** > **[!UICONTROL General]**) para garantizar que solo los usuarios que sean instructores predeterminados puedan añadirse como instructores para una sesión.

Para configurar un instructor, los administradores pueden seleccionar **[!UICONTROL ADMINISTRAR]** > **[!UICONTROL Usuarios]** para abrir la página Administración de usuarios, seleccione un usuario y, a continuación, asigne la función de instructor al usuario (mediante **[!UICONTROL Acciones]** > **[!UICONTROL Asignar función]**).

## Autor

Si el administrador selecciona la opción **[!UICONTROL Administración de instructores]**, un autor solo puede buscar y añadir usuarios con la función de instructor a las sesiones de clase y de clase virtual, las listas de verificación y los módulos de envío de archivos.

Además, el autor puede realizar lo siguiente:

* Añadir y eliminar instructores de las sesiones existentes.
* Añadir instructores a las sesiones existentes que ya tienen uno o varios instructores.

Por lo tanto, después de que un administrador active la opción **[!UICONTROL Administración de instructores]**, solo se pueden añadir como instructores los usuarios con esta función.

>[!NOTE]
>
>Esto no es aplicable al migrar sesiones mediante el archivo CSV de sesiones. En ese caso, se puede añadir como instructor un usuario que no tenga esta función.

## Cancelar sesión existente

Un autor o un administrador pueden cancelar una sesión y reprogramarla, si es necesario.

Cuando un usuario cancela una sesión, el sistema envía un mensaje de correo electrónico de cancelación de la reunión a todos los instructores y los alumnos inscritos. Este mensaje incluye información actualizada de la sesión.

Hay una plantilla denominada **[!UICONTROL Cancelación de la sesión]** que ayuda a cancelar una sesión.

En la página **[!UICONTROL Instancia de curso]**, cada una de las sesiones mostradas en una instancia del curso incluye una opción para su cancelación.

![](assets/cancel-session.png)

*Cancelar una sesión existente*

Al hacer clic en el vínculo **[!UICONTROL Cancelar sesión]**, aparece un mensaje de advertencia.

En el cuadro de diálogo de este mensaje, si hace clic en **[!UICONTROL Continuar]**, el sistema cancela la sesión.

Después de cancelar la sesión, el sistema también borra los siguientes detalles:

* Fecha de inicio de la sesión
* Fecha de finalización de la sesión
* Hora de inicio de la sesión
* Hora de finalización de la sesión
* Instructores añadidos a la sesión
* URL de clase virtual
* Ubicación/lugar añadido a la sesión
* Límite de lista de espera añadido por el instructor

## Administrador

En la página **[!UICONTROL Instancia de curso]**, un administrador puede cancelar una o varias sesiones. Después de que el administrador cancele una sesión, el sistema borra todos los detalles de la sesión, excepto el límite de puestos.

Además, el administrador puede realizar lo siguiente:

* Consultar los alumnos de una sesión que se han inscrito o están en lista de espera.
* Dar de baja a alumnos de un curso con una o varias sesiones canceladas.
* Marcar la asistencia a las sesiones canceladas.
* Marcar como completado un curso que contenga una o varias sesiones canceladas.
* Reprogramar una sesión cancelada.
* Añadir un instructor a una sesión cancelada al reprogramarla.

Tenga en cuenta que, incluso después de la cancelación, los alumnos inscritos en la instancia del curso de formación permanecerán inscritos. Sus estados de inscripción (incluida la inscripción confirmada, en lista de espera y a la espera de la aprobación del responsable) no cambian. Esto es útil porque el administrador puede configurar y reprogramar la sesión cancelada en el futuro.

## Autor

En la página **[!UICONTROL Instancia de curso]**, un autor puede cancelar una o varias sesiones. Cuando el autor cancela una sesión, el sistema borra todos los detalles de la sesión, excepto el límite de puestos.

Por lo tanto, un autor puede utilizar la **[!UICONTROL Cancelar sesión]** vínculos para cancelar una o varias sesiones de clase o sesiones de clase virtual disponibles en la misma instancia del curso o en instancias diferentes.
