---
title: Función personalizada con permisos de anuncio con ámbito
jcr-language: en_us
description: Aprenda a crear una función personalizada en Adobe Learning Manager que permita anuncios solo para catálogos y grupos de usuarios seleccionados.
source-git-commit: 85eeebb33a67bf5528c88b26941345e00e98e0d3
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Función personalizada con permisos de anuncio con ámbito

Los administradores pueden crear funciones personalizadas con permisos de anuncio restringidos a catálogos y grupos de usuarios específicos. Esto garantiza que los anuncios sean específicos, relevantes y solo visibles para los alumnos previstos. Los anuncios con ámbito garantizan que los usuarios adecuados reciban el anuncio correspondiente sin enviar detalles a otros.

## Crear una función personalizada con un ámbito específico

El administrador puede crear una función personalizada con permisos de anuncio limitados a un catálogo y un grupo de usuarios específicos.

Para crear una función personalizada con un ámbito específico:

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **[!UICONTROL Usuarios]** en el panel de navegación izquierdo.

   ![](assets/select-uses-admin.png)
   _Asignar funciones personalizadas a usuarios para permisos y responsabilidades específicos en Adobe Learning Manager_

3. Seleccione Funciones personalizadas.
4. Seleccione Crear función personalizada.

   ![](assets/create-custom-roles.png)
   _Asignar funciones personalizadas a los usuarios para personalizar los permisos y agilizar el control administrativo de grupos de usuarios o catálogos específicos_

5. Escriba el nombre y la descripción de la función personalizada.
6. Seleccione Anuncio en Privilegios de cuenta.

   ![](assets/select-announcement.png)
   _Habilite permisos de anuncio en Privilegios de cuenta para permitir que los administradores personalizados administren comunicaciones dirigidas dentro del ámbito_

7. Seleccione Definir acceso por catálogo en Ámbito de los privilegios de funciones y seleccione el catálogo.
8. En la misma sección, elija Definir acceso por grupo de usuarios y seleccione la
grupo de usuarios.

   ![](assets/select-scope-announcement.png)
   _Establecer ámbitos de catálogo y de grupo de usuarios para garantizar que los administradores personalizados puedan administrar permisos y acceso únicamente dentro de sus ámbitos asignados_

9. Seleccione y añada el usuario al que desee asignar esta función personalizada. Los usuarios asignados pueden crear un anuncio para su ámbito.

Un administrador personalizado puede crear anuncios limitados a sus grupos de usuarios y catálogos asignados, lo que garantiza que los mensajes lleguen a la audiencia adecuada y evita notificaciones innecesarias. En el caso de los anuncios de notificaciones y correos electrónicos, los administradores pueden añadir grupos de usuarios adicionales, pero solo los usuarios dentro del ámbito definido los recibirán. Para los anuncios de recomendación y cabecera, solo puede seleccionar grupos de usuarios dentro del ámbito asignado.

## Crear anuncio para el ámbito asignado

Un administrador personalizado puede crear anuncios limitados a sus grupos de usuarios y catálogos asignados, lo que garantiza que los mensajes lleguen a la audiencia adecuada y evita notificaciones innecesarias.

Para crear un anuncio para el ámbito asignado:

1. Inicie sesión en Adobe Learning Manager como administrador personalizado.
2. Seleccione **[!UICONTROL Anuncio]** en el panel de navegación izquierdo.
3. Seleccione **[!UICONTROL Agregar]**.

   ![](/help/migrated/assets/create-add-announcement.png)
   _Página de anuncios en Adobe Learning Manager, donde los administradores pueden crear y administrar anuncios para grupos de usuarios específicos_

4. Seleccione **[!UICONTROL Tipo de anuncio]** en el menú desplegable.
a. **[!UICONTROL Como notificación]**
b. **[!UICONTROL Como cabecera]**
c. **[!UICONTROL Como recomendación]**
d. **[!UICONTROL Como correo electrónico]**
5. Seleccione **[!UICONTROL Como Cabecera]**.
6. Seleccione el idioma y cargue una imagen para la cabecera.
7. Opcionalmente, añada una dirección URL para el botón de acción.

   ![](/help/migrated/assets/announcement-screen.png)
   _Pantalla Crear anuncio que permite a los administradores establecer el tipo de anuncio, cargar archivos adjuntos y agregar botones de acción_

   El ámbito asignado está preseleccionado en la sección **[!UICONTROL Ámbito]** y los administradores personalizados no pueden modificarlo.

   >[!NOTE]
   >
   >**[!UICONTROL Para los anuncios Notification]** y **[!UICONTROL Email]**, pueden incluir grupos de usuarios y catálogos adicionales si estos se superponen con su ámbito asignado.

8. Seleccione **[!UICONTROL Guardar]**.

Solo los alumnos que se encuentren dentro del ámbito del administrador personalizado podrán ver el anuncio. Consulte este [artículo](/help/migrated/administrators/feature-summary/announcements.md) para aprender a crear varios tipos de anuncios.

## Restablecer el ámbito por administradores personalizados

Los administradores personalizados pueden restablecer el ámbito de sus anuncios publicados si un administrador ha cambiado el ámbito de los mismos. Una vez restablecido el ámbito, el ámbito actualizado se aplicará al anuncio y solo los alumnos del nuevo ámbito podrán ver el anuncio.

Para restablecer el ámbito:

1. Inicie sesión en Adobe Learning Manager como administrador personalizado.
2. Seleccione **[!UICONTROL Anuncio]** en el panel de navegación izquierdo.
3. Seleccione la pestaña **[!UICONTROL Publicado]**.
4. Seleccione cualquier anuncio y, a continuación, seleccione el icono de configuración.
5. Seleccione **[!UICONTROL Editar]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Pantalla de anuncio que muestra los anuncios publicados con las opciones de edición, publicación y otras_

6. Seleccione **Restablecer**.

   ![](/help/migrated/assets/reset-the-scope.png)
   _Anuncio que muestra una notificación de cambio de ámbito, con una opción para que los administradores personalizados restablezcan y actualicen la selección de ámbito para reflejar los nuevos permisos de acceso_

El ámbito se actualizará y solo los usuarios dentro del ámbito actualizado podrán ver el anuncio.

## Editar el anuncio mediante la IU del administrador

Los administradores pueden editar y administrar todos los anuncios creados por los administradores personalizados. Si un administrador intenta editar un anuncio creado por un administrador personalizado con un ámbito específico, aparecerá un mensaje de advertencia en el anuncio indicando el ámbito **[!UICONTROL Quitar]**. El administrador puede eliminar el ámbito para que el anuncio esté disponible para todos. En este caso, el administrador personalizado recibirá una advertencia de que se ha cambiado el ámbito del anuncio.

Para editar el anuncio a través de la IU del administrador:

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **[!UICONTROL Anuncio]** en el panel de navegación izquierdo.
3. Seleccione la pestaña **[!UICONTROL Publicado]**.
4. Seleccione cualquier anuncio y, a continuación, seleccione el icono de configuración.
5. Seleccione **[!UICONTROL Editar]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Pantalla de anuncio que muestra los anuncios publicados con las opciones de edición, publicación y otras_

6. Seleccione **[!UICONTROL Quitar]**.

   ![](/help/migrated/assets/remove-the-scope.png)
   _Pantalla de anuncio que indica que se debe quitar el ámbito para permitir a los administradores editar los anuncios creados para grupos de usuarios con ámbito_

El administrador puede editar el anuncio después de eliminar el ámbito.
