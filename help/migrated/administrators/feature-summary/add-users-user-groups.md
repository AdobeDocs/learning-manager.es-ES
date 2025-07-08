---
description: Aprenda a añadir usuarios internos y externos a Adobe Learning Manager siguiendo instrucciones paso a paso. Explora distintos métodos como la entrada manual, la importación en bloque y la sincronización automatizada de usuarios para simplificar la gestión de usuarios y mejorar tu plataforma de aprendizaje.
jcr-language: en_us
title: Añadir usuarios en Adobe Learning Manager
contentowner: manochan
exl-id: 7df98f2b-c422-4733-8ce4-5489506d4fdf
source-git-commit: 60c171374e4a6b15d92907ae441fc63ba6ee4743
workflow-type: tm+mt
source-wordcount: '2216'
ht-degree: 1%

---


# Añadir usuarios en Adobe Learning Manager

En Adobe Learning Manager, los usuarios son alumnos que utilizan la plataforma para el aprendizaje o la formación. Hay dos tipos de usuarios: usuarios internos y usuarios externos.

Los usuarios internos son empleados o miembros del equipo de su organización.

Los usuarios externos son alumnos externos a su empresa, como clientes, socios, proveedores o clientes, que pueden acceder a su contenido de aprendizaje.

Adobe Learning Manager (ALM) permite a los administradores integrar y administrar usuarios internos y externos mediante diversos métodos, incluidas la entrada manual, la carga de CSV, el registro automático y las integraciones de sistemas.

## Usuarios internos

Los usuarios internos de Adobe Learning Manager se refieren a los empleados o miembros del equipo de su organización. Puede añadirlos manualmente, cargarlos en bloque o importarlos mediante integraciones del sistema. Después de añadir a estos usuarios, puede organizarlos en grupos, asignar cursos y supervisar su progreso de aprendizaje.

Los usuarios de Adobe Learning Manager pueden asumir diferentes responsabilidades y administrar diversas tareas en función de las funciones que tengan asignadas. Cada función, incluidos el administrador, el autor, el instructor y el administrador de integración, ofrece un conjunto de capacidades específicas adaptadas para respaldar las responsabilidades del usuario dentro de la plataforma.

### Métodos para añadir usuarios internos

Los administradores pueden añadir usuarios internos mediante los siguientes métodos:

* **Agregar un solo usuario**: agregue manualmente un usuario cada vez.
* **Perfil de registro automático**: permite que los alumnos se registren automáticamente como alumnos en Adobe Learning Manager mediante un vínculo de registro creado por el administrador.
* **Carga en bloque mediante CSV**: carga un archivo CSV para agregar varios usuarios a la vez.

### Añadir manualmente un usuario interno

Los administradores pueden agregar manualmente un usuario proporcionando su nombre, correo electrónico, identificador único y nombre del responsable. El identificador único de Adobe Learning Manager es un identificador necesario que los administradores asignan al crear un usuario. Debe ser único para cada usuario y servir de referencia coherente en todo el sistema.

>[!INFO]
>
>Vea este curso de formación de ALM Academy para obtener más información sobre cómo añadir usuarios individuales en Adobe Learning Manager.<br>[![botón](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555534)</br>

Para añadir un solo usuario a Adobe Learning Manager:

1. Inicie sesión como administrador.
2. Seleccione **Usuarios** y, a continuación, elija **Interno**.
3. Selecciona **Agregar** y luego elige **Usuario único**.

   ![](assets/add-single-user.png)
   _Interfaz de administrador que muestra la opción de agregar manualmente un único usuario interno_
4. En el símbolo del sistema **Agregar usuario**, escriba el **Nombre**, **Correo electrónico** y el **Perfil** (cargo) del usuario.

   ![](assets/add-a-user-prompt.png)
   _Campos para escribir el nombre, el correo electrónico, el identificador único y el perfil de un nuevo usuario_
5. Busque el responsable del usuario y seleccione el nombre en la lista de responsables.
6. Seleccione **Agregar**.
El usuario recibe un correo electrónico de bienvenida que contiene una URL de inicio de sesión para el acceso.


### Permitir el registro automático para usuarios internos

El registro automático es un proceso de incorporación de autoservicio en el que los usuarios pueden visitar una URL de registro, introducir sus datos e inscribirse automáticamente en la plataforma. Este método minimiza el esfuerzo administrativo al permitir a los usuarios registrarse a través de la dirección URL proporcionada.

Para crear una URL de registro automático para un usuario:

1. Inicie sesión como administrador.
2. Seleccione **Usuarios** y, a continuación, elija **Interno**.
3. Seleccione **Agregar** y, a continuación, elija **Registro automático.**


   ![](assets/add-self-register-link.png)
   _Menú desplegable para seleccionar la opción de registro automático_
4. En el símbolo del sistema **Agregar perfil de registro automático**, escriba el perfil en el campo **Nombre de perfil** (cargo del usuario).
5. Seleccione el administrador del usuario buscando el administrador en el campo **Nombre del administrador**. El responsable asignado al perfil de registro automático debe ser un usuario registrado en Adobe Learning Manager.


   ![](assets/add-a-user-prompt.png)
   _Campos de entrada para establecer el nombre del perfil y asignar un administrador a un perfil de registro automático_
6. Seleccione una imagen con la opción **Agregar imagen**. Esta imagen estará visible para los alumnos en la sección de perfil.
7. Seleccione **Guardar**.

   Adobe Learning Manager crea un perfil de usuario y genera una URL de registro automático, que se puede compartir con los usuarios para completar su registro.


   ![](assets/self-register-url.png)
   _Mensaje de confirmación que indica la creación correcta de una URL de registro automático_
8. Comparta la URL con los usuarios que deseen registrarse por sí mismos.


   La URL se puede compartir con varios usuarios para su registro. Por ejemplo, puede generar una dirección URL para el perfil **Sales Associate** y compartirla con el equipo de Sales Associate para que se registren.

![](assets/self-register-screem.png)
_El vínculo de registro automático abre una página de registro_

### Ver la lista de direcciones URL de registro automático

Para ver la lista de direcciones URL de registro automático:

1. Seleccione **Usuarios** y, a continuación, elija **Interno**.
2. Seleccione **Registro automático**.

   Los administradores pueden ver la lista de direcciones URL de registro automático.

![](assets/self-registration-profile.png)
_Vista de lista que muestra las direcciones URL de registro automático disponibles para usuarios internos_

### Cargar usuarios internos en bloque

Los administradores pueden añadir varios usuarios a la vez cargando un archivo CSV con información de usuario como el nombre, la dirección de correo electrónico y el nombre del responsable. Esta función de carga en bloque ahorra tiempo y esfuerzo en comparación con la adición de usuarios individualmente.

>[!INFO]
>
>Vea este curso de formación de ALM Academy para aprender a añadir usuarios en bloque mediante un CSV. <br>[![botón](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)</br>

Para añadir varios usuarios:

1. Inicie sesión como administrador.
2. Seleccione **Usuarios** y, a continuación, elija **Interno**.
3. Selecciona **Agregar** y luego elige **Cargar un CSV**.

   ![](assets/select-upload-acsv.png)
   _Opción para cargar un archivo CSV para la importación masiva de usuarios_

4. Prepare un archivo CSV con los siguientes campos:

   * Nombre del empleado*
   * Correo electrónico del empleado*
   * Perfil/designación del empleado
   * Id./correo electrónico del responsable\
     (*) Campos obligatorios.

5. Antes de añadir el ID de correo electrónico de un responsable para cualquier empleado, asegúrese de que el responsable ya esté incluido como empleado en el archivo CSV. Por ejemplo, consulte al empleado llamado Howard Walters en la captura de pantalla siguiente.

   ![](assets/csv-image.png)
   _Imagen de archivo CSV de muestra con todos los campos_

6. Cargue el archivo CSV y asigne los campos de datos según corresponda.

   ![](assets/map-the-column.png)
   _Interfaz de asignación de CSV para alinear columnas de hoja de cálculo con campos del sistema_
7. Seleccione **Guardar** para importar los usuarios.

   Aparece un mensaje de confirmación después de que la carga se realice correctamente.

   ![](assets/csv-save-success.png)
   _La imagen muestra el estado de la carga del archivo CSV como correcta_

>[!NOTE]
>
>Mantener un archivo CSV maestro para todas las adiciones y eliminaciones. No es posible actualizar y volver a cargar un archivo CSV existente.

Al cargar un archivo CSV para añadir usuarios, es importante incluir toda la información relacionada en el orden correcto. Si asigna el ID de correo electrónico de un responsable a un empleado, los detalles del responsable deben aparecer antes en el archivo CSV. Esto garantiza que el sistema reconozca al responsable como un usuario existente antes de vincularlo a los miembros de su equipo. Por ejemplo, si Howard Walters es un responsable, incluya todos sus detalles de usuario en el CSV antes de enumerar los empleados que reportan ante él.

### Administrar registro de usuarios

Después de añadir usuarios individualmente o en bloque, debe registrarlos para activar sus cuentas. Esto permite a los usuarios acceder a Adobe Learning Manager y empezar a utilizar la plataforma.

Para registrar a los usuarios:

1. Seleccione **Usuarios** en la página principal del administrador.
2. Seleccione las casillas de verificación junto a los nombres de los usuarios que desea registrar.
3. Seleccione **Acciones** y, a continuación, elija **Registrar**.

   ![](assets/register-user.png)
   _Botón de registro para activar los usuarios seleccionados en Adobe Learning Manager_

4. Seleccione **Sí** para activar el usuario.

Se envía un correo electrónico de verificación al usuario. El usuario debe seleccionar el vínculo en el correo electrónico para activar su cuenta y comenzar a utilizar Adobe Learning Manager.

## Usuarios externos

Adobe Learning Manager le permite añadir usuarios fuera de su empresa, como clientes, socios, proveedores o clientes, para acceder al contenido de aprendizaje. Una vez agregados, puede agruparlos, asignar cursos y realizar un seguimiento de su progreso de aprendizaje.

La adición de usuarios externos en Adobe Learning Manager implica los siguientes pasos:

* Crear un perfil de registro externo
* Habilitar el perfil de registro
* Compartir el vínculo de registro con usuarios externos
* Pausar o reanudar el perfil cuando sea necesario

Adobe Learning Manager admite la inscripción de estos usuarios a través de perfiles de registro externos.

Para crear un usuario externo, siga estos pasos:

1. Inicie sesión como administrador.
2. Seleccione **Usuarios** y, a continuación, elija **Externo**.
3. Seleccione **Agregar** para crear un registro para un usuario externo.
4. En el cuadro de diálogo **Agregar perfil de registro externo**, proporcione lo siguiente:

   * **Nombre de perfil:** Escriba el nombre.
   * **Correo electrónico del administrador:** Escriba la dirección de correo electrónico del administrador.
   * **Límite de puestos:** Establezca el número máximo de inscripciones permitidas.
   * **Caducidad:** Defina la última fecha para nuevos registros. Una vez que caduque, el vínculo no funcionará para el nuevo registro de usuario.

   ![](assets/add-external-user-prompt.png)
   _Cuadro de diálogo para especificar el nombre del perfil, el correo electrónico del administrador, el límite de puestos y la caducidad_

5. Seleccione una imagen con la opción **Agregar imagen**. Esta imagen estará visible para los alumnos en la sección de perfil.
6. Seleccione la sección **Configuración avanzada** para expandirla y escriba los detalles necesarios:
   * **Requisito de inicio de sesión:** Escriba el número de días. Si los alumnos permanecen inactivos durante todo el período, se eliminarán automáticamente.
   * **Dominios permitidos:** Escriba la lista separada por comas de los dominios de correo electrónico permitidos. Solo los usuarios con direcciones de correo electrónico de dominios aprobados pueden registrarse.
   * **Se requiere verificación por correo electrónico:** Seleccione esta opción para aplicar la verificación por correo electrónico durante el registro.

   ![](assets/advanced-settings-add-external.png)
   _Panel Configuración avanzada para establecer los requisitos de inicio de sesión, los dominios permitidos y la verificación por correo electrónico_

7. Seleccione **Guardar**.

Se generará una URL de registro.

### Habilitar el perfil externo

Para activar el perfil externo:

1. Localice el perfil recién creado en la lista de perfiles externos.
2. Seleccione el botón de alternancia **Estado** para habilitarlo.

El administrador puede compartir esta dirección URL con el socio externo para que pueda registrarse e iniciar sesión en Adobe Learning Manager con ella.

![](assets/enable-the-external-user.png)
_Seleccione el conmutador para habilitar el perfil externo_

### Copiar y compartir la URL de registro del perfil externo

La URL de registro para un perfil externo se puede copiar desde la sección **Usuarios externos**.

![](assets/copy.png)
_Copiar la dirección URL de registro de un perfil externo_

### Diferencias clave entre los registros de usuarios internos y externos

Existen algunas diferencias entre los registros internos y externos:

| Usuarios internos | Usuarios externos |
|---|---|
| Puede iniciar sesión con las credenciales de Adobe ID o SSO. | Puede iniciar sesión con cualquier ID de correo electrónico. |
| La interacción está disponible. | La interacción está disponible. El administrador debe habilitar la interacción para alumnos externos en [Configuración de interacción](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/gamification). |

### Pausar perfil de registro externo

En Adobe Learning Manager, los administradores pueden administrar el registro de usuarios externos pausando sus perfiles. Esto resulta útil cuando desea pausar temporalmente a los nuevos usuarios para que no se unan mediante un perfil de registro externo específico. Al pausar un perfil, se impide que los usuarios que han recibido invitaciones pero no se han registrado aún completen el proceso de registro. Esta acción no afecta a los usuarios que ya han completado su registro.

Para pausar un perfil externo:

1. Seleccione **Acciones** en la esquina superior derecha de la página **Usuarios externos**.
2. Seleccione **Pausar** para pausar el perfil de registro externo.

Esto bloquea los nuevos registros de los usuarios que no hayan aceptado sus invitaciones. Tenga en cuenta que esta acción solo afecta a los usuarios que aún no han completado su registro.

![](assets/pause-external-user.png)
_Opción para pausar un perfil de registro externo existente desde el menú Acciones_

### Reanudar perfil de registro externo

Si un perfil externo estaba previamente en pausa, los administradores pueden reanudarlo para permitir que los nuevos usuarios completen su registro. Esto reactiva el proceso de registro para los usuarios que fueron invitados pero no completaron su registro.

Para reanudar un usuario externo:

1. Seleccione **Acciones** en la esquina superior derecha de la página.
2. Seleccione **Reanudar** para reanudar el acceso de un asociado en pausa.

![](assets/resume-an-external-user.png)
_Opción para reanudar un perfil de registro externo previamente pausado_

### Controlar el uso de asientos externos

Los administradores pueden realizar un seguimiento del número de usuarios añadidos a cada perfil externo en Aprendizaje Adobe.

Para comprobar los asientos usados:

1. Seleccione **Puestos usados** en la lista de perfiles externos.

Puede ver el número de alumnos añadidos a la organización asociada y si los alumnos están activos.

## Administrar usuarios

Los administradores pueden editar los detalles de los usuarios, eliminar usuarios, asignar funciones y eliminarlas. Esto ayuda a garantizar que cada usuario tenga el acceso y las tareas adecuados.

>[!INFO]
>
>Vea este curso de formación de ALM Academy para aprender a asignar y eliminar funciones, enviar un correo electrónico de bienvenida y eliminar y purgar usuarios.<br>[[button]](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555586)</br>

### Editar un usuario

Use la opción **Editar usuario** en Adobe Learning Manager para actualizar la información de perfil de un usuario, como el nombre, la dirección de correo electrónico, el identificador único, el perfil y el nombre del administrador. Los administradores pueden realizar estos cambios para garantizar que los datos de los usuarios sean precisos y estén actualizados.

Para editar un usuario:

1. Seleccione **Usuarios** en la página principal del administrador.
2. Seleccione el usuario que desea editar en la lista **Usuarios**.
3. Seleccione **Editar perfil**.

   ![](assets/edit-a-profile.png)
   _Opción Eliminar usuario en el menú Acciones para quitar un usuario de la plataforma_

4. Seleccione **Sí** para eliminar el usuario.

Aparece un mensaje de confirmación cuando el usuario se elimina correctamente.

## Asignar una función a un usuario

Las funciones de usuario en Adobe Learning Manager definen qué acciones puede realizar cada persona en el sistema. Cada función incluye permisos específicos basados en las responsabilidades del usuario.

Adobe Learning Manager admite las siguientes funciones de usuario:

* **Administrador**: Administra usuarios y grupos de usuarios, asigna funciones y configura preferencias en todo el sistema como orígenes de datos, dominios permitidos y opciones de visualización. Los administradores también son responsables de crear y organizar el contenido de aprendizaje, realizar el seguimiento del progreso de los alumnos, generar informes y configurar integraciones con sistemas externos.
* **Autor**: Crea y administra contenido, incluidos módulos y cursos.
* **Responsable**: supervisa las actividades de aprendizaje del equipo, designa a miembros del equipo para los cursos, aprueba solicitudes y proporciona comentarios.
* **Administrador de integración**: Administra las integraciones del sistema y las conexiones de datos entre ALM y las plataformas externas.
* **Funciones personalizadas**: los administradores pueden crear funciones personalizadas para dar a los usuarios acceso personalizado en función de sus responsabilidades. Consulte este [artículo](/help/migrated/administrators/feature-summary/custom-role.md) para obtener más información sobre las funciones personalizadas.

Para asignar funciones a usuarios:

1. Seleccione **Usuarios** en la página principal del administrador.
2. Seleccione el usuario al que desea asignar una función.
3. Seleccione **Acciones** en la esquina superior derecha.
4. Seleccione **Asignar función**.
5. Seleccione el rol requerido.

   ![](assets/assign-roles-users.png)
   _Las opciones del menú Asignar función muestran las funciones disponibles para el usuario seleccionado_

6. Seleccione **Sí** en el cuadro de diálogo de confirmación.

## Eliminar una función

Al quitar una función de usuario, se revocan los permisos otorgados por dicha función.

Para eliminar funciones de usuarios:

1. Seleccione **Usuarios** en la página principal del administrador.
2. Seleccione los usuarios cuyas funciones desee quitar.
3. Seleccione **Acciones** y, a continuación, seleccione **Quitar rol**.

   ![](assets/remove-a-role.png)
   _Opción para quitar las funciones asignadas a un usuario en el menú Acciones_

4. Seleccione **Sí** en el cuadro de diálogo de confirmación.

