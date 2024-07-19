---
jcr-language: en_us
title: Asignación predeterminada de funciones de instructor a grupos de usuarios en Learning Manager
description: Asignación predeterminada de funciones de instructor a grupos de usuarios en Learning Manager
contentowner: nluke
preview: true
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 48%

---



# Asignación predeterminada de funciones de instructor a grupos de usuarios en Learning Manager

## El problema

A todos los usuarios asignados a una sesión se les asigna la función de instructor.

## Descripción

Hay situaciones en las que una sesión puede requerir varios instructores o que un administrador/autor asigne un grupo de usuarios a una sesión. Esto provoca que a todos los usuarios del grupo de usuarios se les asigne la función de instructor.

## Causa

Como las funciones no se pueden bifurcar durante la asignación masiva de usuarios de un grupo, la función de instructor se asigna a todos los usuarios.

## Solución

Cree grupos de usuarios personalizados para filtrar las funciones de usuario asignadas a una sesión. Para eliminar las funciones de instructor asignadas a un grupo de usuarios, siga estos pasos:

1. Inicie sesión como Administrador. En el panel izquierdo, haz clic en **[!UICONTROL Plantillas de correo electrónico]**.
1. Para evitar activadores de correo electrónico para los cambios que se van a realizar, haga clic en **[!UICONTROL Deshabilitar todo]**.

   ![](assets/instructor-disable-all.png)

1. Vaya a **Usuarios** > **Grupo de usuarios**. Haga clic en **[!UICONTROL Añadir]**.

   ![](assets/instructor-usergroups.png)

1. Cree un grupo de usuarios personalizado en la ventana Añadir grupo de usuarios de la siguiente manera:

   * Escriba un nombre para el grupo personalizado en el campo **[!UICONTROL Nombre]**.
   * En el campo **[!UICONTROL Incluir alumnos]**, agregue el grupo de usuarios para el que desea filtrar los instructores.
   * En el campo **[!UICONTROL Excluir alumnos]**, agregue los usuarios para los que desee conservar la función de instructor.

   ![](assets/instructor-add-ug.png)

   Los pasos anteriores crean una lista de usuarios que se van a añadir al conjunto de inclusión y eliminan usuarios específicos (instructores) mencionados en el conjunto de exclusión.

1. Haga clic en **[!UICONTROL Guardar]** los cambios realizados.
1. Busque el grupo de usuarios personalizado creado yendo a **[!UICONTROL Usuarios]** > **[!UICONTROL Interna]**.

   ![](assets/instructor-custom-ug.png)

1. Haga clic en la casilla de verificación para seleccionar todos los usuarios del grupo.

   ![](assets/instructor-bulk-ug.png)

1. Haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Quitar rol]** > **[!UICONTROL Quitar instructor]**.

Asegúrese de que todos los activadores de correo electrónico que se deshabilitaron en el paso 2 se vuelvan a activar una vez completados.
