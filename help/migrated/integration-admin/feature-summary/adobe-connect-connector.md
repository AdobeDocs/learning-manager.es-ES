---
description: Aprenda a integrar el conector de Adobe Connect con Adobe Learning Manager
jcr-language: en_us
title: Conector de Adobe Connect
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 2%

---


# Conector de Adobe Connect en Adobe Learning Manager

## Introducción

Adobe Learning Manager se integra con Adobe Connect para ayudarte a impartir y gestionar la formación en clase virtual. Con esta integración, puede programar sesiones, utilizar salas de reuniones dinámicas o permanentes, capturar la asistencia, importar los resultados de las pruebas y proporcionar a los alumnos grabaciones de las sesiones.

## Configurar Adobe Connect

Para configurar Adobe Connect:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el mosaico **Adobe Connect** y seleccione **Connect**.

   ![](assets/adobe-connect-connector1.png)
   _Seleccionar Conectar para configurar el conector de Adobe Connect_

3. Escriba los siguientes datos:

   - **Nombre de conexión**
   - **URL de Adobe Connect**
   - **Correo electrónico del administrador de Connect**
4. Escriba el **ID de inicio de sesión del administrador de Connect** (obligatorio si no se utiliza el inicio de sesión por correo electrónico de Adobe Connect).

   ![](assets/adobe-connect-connector2.png)
   _Escriba los detalles necesarios para la configuración de Adobe Connect_

5. Seleccione **Habilitar autenticación de conexión**.

   >[!NOTE]
   >
   >Solo se admiten cuentas de Connect alojadas en el Adobe. (El dominio debe terminar en .adobeconnect.com)

6. Seleccione **Conectar**.

Después de autenticar el ID del correo electrónico del administrador:

- Adobe Learning Manager muestra un mensaje de confirmación de que Connect está integrado.
- La solicitud se envía al equipo de backend de Adobe Connect para su aprobación. Esto suele tardar de uno a dos días.

>[!IMPORTANT]
>
>El administrador de la cuenta de Adobe Connect debe aceptar los Términos y condiciones al iniciar sesión por primera vez. Si esto no se hace, la autenticación del inicio de sesión puede fallar.

## Añadir información sobre la sesión de la clase virtual

Si un autor no ha proporcionado los detalles de la sesión de un curso de clase virtual, el administrador puede añadirlos:

1. Inicie sesión como administrador.
2. Seleccione el curso de clase virtual.
3. Seleccione **Instancias** y, a continuación, seleccione **Detalles de la sesión**.
4. Seleccione el icono **Editar** para agregar o actualizar la información de la sesión.

>[!NOTE]
>
>La cuenta de Connect debe tener suficientes salas de reuniones y capacidad para que los usuarios simultáneos puedan ejecutar clases virtuales. Cada sesión de clase virtual de Adobe Learning Manager crea automáticamente una nueva sala de reuniones de Connect, a menos que utilice una sala permanente.

## Salas de reuniones permanentes

Adobe Connect admite salas de reuniones permanentes, que permanecen disponibles para su reutilización.

- Puede crear una sesión de clase virtual utilizando una sala permanente existente en Connect.
- También puede hacer que Adobe Learning Manager cree una sala dinámica para cada sesión.

Cuando los alumnos asisten a una sesión con Adobe Connect, entran en la sala a través de Learning Manager utilizando una autenticación segura.

Después de completar una sesión, los alumnos pueden acceder a la grabación de la sesión y a la contraseña en su aplicación de Learning Manager.

## Importar puntuaciones de pruebas de Adobe Connect

Adobe Learning Manager puede importar datos de pruebas de sesiones de Adobe Connect y combinarlos con otros flujos de trabajo de informes. Esto incluye las puntuaciones de las pruebas, las respuestas de los alumnos y los datos de finalización, como el funcionamiento de los módulos con ritmo personalizado.

### Flujo de trabajo de importación de pruebas

#### Adobe Connect (anfitrión)

- El anfitrión de Connect crea un curso y carga contenido que incluye un cuestionario interactivo.
- El anfitrión configura un curso de clase virtual y vincula el curso a la clase virtual o utiliza la opción **Compartir curso** para compartirlo durante la sesión.

#### Adobe Learning Manager (autor)

- El autor crea un curso en Adobe Learning Manager con el tipo de módulo establecido en **Clase virtual**.
- En el menú desplegable **Sistema de conferencia**, selecciona **Connect** como proveedor de clase virtual.
- Elija la **Sala de reuniones permanente** creada por el host en Connect.
- Asignar un instructor, guardar y publicar el curso.

#### Adobe Learning Manager (alumno)

- El alumno se inscribe en el curso y se une a la sesión de Connect VC.
- El host de Connect permite al alumno acceder a la sesión.

### Adobe Connect (anfitrión y alumno)

- El anfitrión comparte la prueba en la sesión.
- El alumno finaliza la prueba y sale de la sesión.

### Adobe Learning Manager (sincronización y administrador)

- Cuando finaliza la sesión, Adobe Learning Manager sincroniza automáticamente los datos de la prueba.
- El flujo de trabajo de importación de la prueba comienza una vez finalizada la duración programada.
- Para realizar un seguimiento del progreso, el administrador de integración puede comprobar el **Estado de ejecución** en el conector de Adobe Connect.
- Una vez completada la importación, el estado cambia a **Completado**.

A continuación, el administrador puede revisar los resultados importados:

- **Puntuación y asistencia:** Vea las puntuaciones finales de las pruebas y la asistencia.
- **Puntuación de prueba de L2:**
   - **Por usuario:** Muestra puntuaciones individuales en puntos y porcentajes.
   - **Por pregunta:** Muestra los resultados de la prueba en un gráfico de informe.
