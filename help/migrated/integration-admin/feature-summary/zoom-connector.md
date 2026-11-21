---
description: Aprenda a integrar el conector de Zoom con Adobe Learning Manager
jcr-language: en_us
title: Conector de Zoom
contentowner: mmanuel
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 3628dd3701949da127b138e0e1ffc2db8e84eab1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 2%
---

# Conector de Zoom en Adobe Learning Manager

## Introducción

El conector de Zoom en Adobe Learning Manager permite a las organizaciones ofrecer sesiones de clase virtual en directo, administrar la inscripción de alumnos y realizar un seguimiento de la asistencia y la finalización. También admite varias conexiones de Zoom en una sola cuenta, lo que permite a los administradores de integración administrar el acceso en función de las funciones o los grupos de usuarios, y a los autores seleccionar las conexiones disponibles para las sesiones del curso. Después de la sesión, los datos de asistencia y rendimiento se sincronizan de nuevo con Adobe Learning Manager para la creación de informes y el seguimiento.

## Configurar el conector de Zoom

Para configurar el conector de Zoom:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el mosaico **Zoom**.

   ![](assets/zoom-connector1.png)
   _Configurar el conector de Zoom en Adobe Learning Manager_

3. Seleccione **Conectar**. Se abre la página de configuración del conector de Zoom.
4. Escriba los siguientes detalles de la cuenta en los campos respectivos. Puede obtener estas credenciales del administrador de la cuenta de Zoom:

   * Nombre de conexión
   * ID de cuenta de Zoom
   * ID de cliente
   * Secreto de cliente
   * Dirección de correo electrónico del superadministrador
   * Roles o grupos que pueden utilizar este conector (opcional)

   ![](assets/zoom-connector2.png)
   _Escriba los detalles de configuración para configurar el conector de Zoom_

5. Seleccione **Conectar** para establecer la integración.

>[!NOTE]
>
>Al habilitar el conector, **los alumnos deben usar la misma dirección de correo electrónico** para sus cuentas de Zoom y Adobe Learning Manager para garantizar que los datos de usuario se sincronicen correctamente.

## Añadir varias conexiones de Zoom

Puede agregar varias conexiones de Zoom a Adobe Learning Manager, cada una de las cuales está vinculada a una cuenta de Zoom diferente. Por ejemplo, puede crear conexiones independientes para diferentes socios o equipos y especificar qué funciones o grupos de usuarios pueden utilizar cada conexión.

El número de conexiones que puede añadir depende de su nivel de cuenta de Adobe Learning Manager:

| **Nivel de cuenta** | **Máximo de conexiones de Zoom** |
|---|---|
| Prime | 6 |
| Ultimate | 50 |

## Crear cursos de Zoom

Una vez establecida la conexión:

1. Inicie sesión como **autor** y cree un nuevo curso de clase virtual.
2. Seleccione **Zoom** como sistema de conferencia y, a continuación, seleccione la conexión de Zoom que desee usar en la lista.
   >[!NOTE]
   >
   >La lista muestra sólo las conexiones disponibles para su rol o grupo de usuarios, y una sesión utiliza una conexión cada vez.
3. Asigne alumnos al curso a través de administradores, responsables o mediante inscripción automática.
4. Al inscribirse, los alumnos reciben un correo electrónico con los detalles del curso.
5. Los alumnos pueden iniciar sesión en su cuenta de Adobe Learning Manager para acceder al curso y unirse a la sesión de Zoom.

## Conexiones de zoom disponibles para los autores

Al crear o editar una sesión de curso, puede seleccionar las conexiones de Zoom disponibles para su función o grupo de usuarios. El administrador de integración define qué funciones o grupos de usuarios pueden acceder a cada conexión de Zoom.

Por ejemplo, supongamos que un administrador de integración configura dos conexiones de Zoom, **Asociar A Zoom** y **Asociado B Zoom**, y asigna cada conexión a un grupo de usuarios diferente:

* Si pertenece a los grupos Socio A y Socio B, puede seleccionar cualquiera de las conexiones.
* Si solo pertenece al grupo Partner A, puede seleccionar **Partner A Zoom**.
* Si no pertenece a ninguno de los grupos, estas conexiones no estarán disponibles para su selección.

>[!NOTE]
>
>Sólo puede utilizar una conexión de zoom para una sesión. Si dispone de varias conexiones, seleccione la conexión que desea utilizar para la sesión.

## Administrar conexiones de Zoom

La página **Administrar conexiones** muestra las conexiones de Zoom configuradas para su cuenta. La columna **Visible para** indica las funciones o los grupos de usuarios que pueden usar cada conexión. Desde esta página, puede editar, activar o desactivar y eliminar las conexiones de Zoom existentes.

![Conexión de zoom Configurar página con Habilitar configuración de conexión, credenciales y roles o grupos](assets/zoom-connection-configure-page.png "Conexión de zoom Configurar página con Habilitar configuración de conexión, credenciales y roles o grupos")

### Editar una conexión de zoom

Para editar una conexión de zoom existente:

1. Seleccione la conexión en la página **Administrar conexiones** que desee editar.
1. En la ficha Configurar, realice una de las siguientes acciones:

   1. Para actualizar las credenciales de la cuenta de Zoom, seleccione **Editar** junto a **Credenciales** y actualice los detalles necesarios.
   1. Para cambiar quién puede usar la conexión, actualice **Roles o grupos** que pueden usar este conector.

1. Seleccione **Guardar**.

### Habilitar o deshabilitar una conexión de zoom

Las nuevas conexiones de Zoom están activadas de forma predeterminada. Puede deshabilitar una conexión para evitar que los autores la utilicen sin eliminar la conexión.

Para deshabilitar una conexión:

1. En la página **Administrar conexiones**, seleccione la conexión que desea deshabilitar.
1. Active **Habilitar conexión**.
1. Seleccione **Guardar**.

   La conexión deshabilitada ya no está disponible para los usuarios de las funciones o grupos asociados.

Para volver a habilitar la conexión, selecciona **Habilitar conexión** y, a continuación, selecciona **Guardar**.

### Eliminar una conexión de zoom

Para eliminar una conexión de zoom:

1. En la página **Administrar conexiones**, vaya a la conexión que desea eliminar.
1. Seleccione el icono **Delete** junto a la conexión.
1. Seleccione **Eliminar**.

## Seguimiento de asistencia y finalización

Una vez finalizada la sesión virtual:

* Adobe Learning Manager recibe automáticamente el estado de finalización de Zoom.
* Los administradores pueden ver informes de asistencia y puntuación en Adobe Learning Manager para realizar un seguimiento de la participación y el rendimiento de los alumnos.

## Crear una aplicación de OAuth de servidor a servidor de Zoom

Para utilizar el conector de Zoom con Adobe Learning Manager, debe crear una aplicación OAuth de servidor a servidor de Zoom y configurar los ámbitos necesarios.

### Ámbitos de OAuth requeridos

Al crear la aplicación en Zoom, asegúrese de que están seleccionados los siguientes ámbitos:

| Lo que quieres | Buscar esta palabra clave | A continuación, elija |
|---|---|---|
| Ver todas las reuniones de usuarios | reunión | `meeting:read:meeting:admin, meeting:read:list_meetings:admin` |
| Ver o administrar todas las reuniones de usuarios | reunión | `meeting:update:meeting:admin, meeting:delete:meeting:admin, meeting:write:meeting:admin` |
| Ver datos del informe | informe | `report:read:meeting:admin, report:read:user:admin` (elija el que coincida con su extremo). |
| Ver toda la información del usuario | interfaz | `user:read:user:admin, user:read:list_users:admin` |
| Administrar usuarios | interfaz | `user:update:user:admin, user:write:user:admin` |
| Agregar un registrante de la reunión | solicitante de registro | `meeting:write:registrant:admin` |
| Enumerar todos los inscritos de la reunión | solicitante de registro | `meeting:read:list_registrants:admin` |
| Reuniones de subcuentas | reunión + buscar :master | `meeting:write:meeting:master` |
| Informe de los participantes de la reunión | participante | `report:read:list_meeting_participants:admin` |

