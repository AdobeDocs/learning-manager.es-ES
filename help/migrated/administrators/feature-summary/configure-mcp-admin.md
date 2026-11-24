---
description: Cree, administre y retire servidores de Model Context Protocol en Adobe Learning Manager para que los clientes de IA puedan acceder de forma segura a la formación de sus alumnos.
jcr-language: en_us
title: Configurar un servidor de Protocolo de contexto de modelo
exl-id: 3130c36d-e63e-4cd6-b0ed-561371b9b261
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---

# Configurar un servidor de Protocolo de contexto de modelo

## Información general

Cada servidor MCP registra una aplicación cliente OAuth 2.0 que autoriza a los clientes de IA a actuar en nombre de los alumnos. Como administrador, cree el servidor, copie sus credenciales y, a continuación, déselas al administrador del cliente de AI, que completa la conexión. Puede volver a visitar un servidor en cualquier momento para editarlo, perfeccionar sus descripciones de herramientas, copiar sus credenciales o eliminarlo.

>[!NOTE]
>
>El servidor proporciona acceso de lectura solo a los usuarios con la función Alumno.

## Crear el servidor MCP

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Navega a **IA en Aprendizaje** > **Servidores MCP**.
3. Seleccione **Nuevo servidor MCP**.
4. Introduzca los detalles del servidor, incluida una descripción.

   * **Nombre del servidor:** Escriba un nombre de hasta 50 caracteres.
   * **Descripción:** Escriba una descripción breve de hasta 150 caracteres.
   * **URL:** Escriba la dirección URL de su empresa o aplicación.
   * **Dominios de redirección:** Escriba el dominio de cada cliente de IA que se conectará, como [http://\*.chatgpt.com](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.chatgpt.com) o [http://\*.claude.ai](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.claude.ai). Este campo es obligatorio.

   ![](assets/2_Administrator--Configure-MCP-image1.png)

5. Seleccione **Siguiente**.
6. En la página **Herramientas disponibles**, revise las herramientas del alumno que expone el servidor. Proporcionar descripciones detalladas, contextuales y basadas en objetivos para las herramientas de MCP.Proporcione descripciones detalladas y contextuales para cada herramienta. Una descripción precisa ayuda a los clientes compatibles con MCP a seleccionar e invocar la herramienta adecuada. Incluye el propósito de la herramienta, las tareas admitidas, las entradas esperadas y los casos de uso típicos.

   ![](assets/2_Administrator--Configure-MCP-image2.png)

   Seleccione **Ver** en cada herramienta para ver las instrucciones para determinar cuándo está seleccionada la herramienta y cómo responde.

   ![](assets/2_Administrator--Configure-MCP-image3.png)

7. Seleccione **Credenciales de cliente** en el panel de navegación izquierdo.
8. Copie la **URL del extremo de MCP**, el **ID de cliente** y la **clave secreta**. Seleccione **Copiar** junto a cada valor.

   ![](assets/2_Administrator--Configure-MCP-image4.png)

9. Seleccione **Cerrar**.

>[!NOTE]
>
>El servidor proporciona acceso de lectura solo a los usuarios con la función Alumno.

Indique la URL del terminal, el ID del cliente y la clave secreta al administrador del cliente de AI.

## Editar la descripción de una herramienta

Una descripción de la herramienta indica al cliente de AI cuándo seleccionar la herramienta y cómo responde la herramienta. También puede agregar mensajes de ejemplo. Las descripciones de herramientas bien escritas ayudan a los clientes compatibles con MCP a descubrir e invocar las herramientas adecuadas de forma más precisa. Incluye el propósito de la herramienta, las tareas admitidas, las entradas esperadas y los casos prácticos habituales.

1. En la página **Herramientas disponibles**, seleccione el menú **Acciones** de una herramienta.
2. Seleccione la configuración de la herramienta **MCP** \> **Editar**.

   ![](assets/2_Administrator--Configure-MCP-image5.png)

3. En el cuadro de diálogo **Editar herramienta**, actualice **Instrucciones/Descripción**.

   ![](assets/2_Administrator--Configure-MCP-image6.png)

4. En **Mensajes de ejemplo**, edite los mensajes. Para agregar una solicitud, seleccione **Agregar otro ejemplo**.
5. Seleccione **Guardar**.

Para devolver una herramienta a su texto original, seleccione el menú **Acciones** de la herramienta y, a continuación, seleccione **Configuración de la herramienta MCP** \> **Restablecer**.

## Edición de un servidor MCP

1. Seleccione **IA en Aprendizaje** > **Servidores MCP**.
2. Seleccione el nombre del servidor.
3. Seleccione **Editar**.
4. Actualice los campos en la página **Detalles de la aplicación** y guarde los cambios.

## Eliminar un servidor MCP

1. Seleccione **IA en Aprendizaje** > **Servidores MCP**.
2. En la fila del servidor, seleccione el menú **Acciones**.
3. Seleccione **Eliminar**.
4. En el cuadro de diálogo de confirmación, seleccione **Eliminar**.

>[!WARNING]
>
>Al eliminar un servidor, se elimina el acceso a todas sus herramientas para las aplicaciones de IA conectadas. Las sesiones activas pueden dejar de funcionar inmediatamente y no se puede deshacer la eliminación.

## Resolución de problemas

**Los cambios de herramientas no aparecen de inmediato.**
Las modificaciones de las descripciones de herramientas tardan algún tiempo en surtir efecto. Espere e inténtelo de nuevo.

**Un cliente de IA dejó de funcionar después de que se eliminara un servidor.**
Cree un nuevo servidor y proporcione las nuevas credenciales al administrador del cliente de AI.

**El cliente de inteligencia artificial usa la herramienta incorrecta.**
Revise las descripciones de las herramientas que haya cambiado. Seleccione **Restablecer** para restaurar el texto original.

## Prácticas recomendadas

* Conserve las descripciones originales de las herramientas a menos que tenga una razón específica para cambiarlas.
* Escriba descripciones de herramientas específicas e inequívocas e indicaciones de ejemplo cuando las edite.
* Almacene la clave secreta de forma segura y compártala únicamente con el administrador del cliente de inteligencia artificial.
* Cree un servidor independiente para cada aplicación de IA, de modo que pueda revocar una sin que afecte a las demás.
* Confirme que ninguna aplicación de IA depende de un servidor antes de eliminarlo.
