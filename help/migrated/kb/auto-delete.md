---
jcr-language: en_us
title: El usuario se elimina automáticamente en Learning Manager
description: Un usuario se elimina de Learning Manager; sin embargo, el administrador nunca ha realizado dicha acción.
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---



# El usuario se elimina automáticamente en Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problema

Un usuario se elimina de Learning Manager; sin embargo, el administrador nunca ha realizado dicha acción.

## Causa

En Adobe Learning Manager, hay una opción que le permite eliminar un usuario si este no ha iniciado sesión en el sistema durante un período de tiempo determinado.

## ¿Cómo cambiar o aplicar la configuración?

### Para alumnos internos

1. Inicie sesión como **Administrador**.
1. Debajo **Configurar**, haga clic en **Configuración** > **General**.
1. En la página Configuración general, busque la opción **Eliminar automáticamente usuarios internos**.
1. Haga clic en **[!UICONTROL Editar]** para introducir el número de días en el campo, para eliminar automáticamente un alumno si no ha accedido al sistema.

   ![](assets/cp-autodelete-internal.png)

   *Editar el número de días*

>[!NOTE]
>
>   Deje el campo en blanco si no desea eliminar usuarios automáticamente.


1. Haga clic en **[!UICONTROL Guardar]** para conservar la configuración realizada.

### Para alumnos externos:

1. Inicie sesión como **Administrador**.
1. Debajo **Gestionar**, haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Externo]**.
1. Haga clic en el nombre de un usuario externo al que se debe aplicar la configuración.

   Esto abre el **Editar perfil de registro externo** ventana.

1. Haga clic en **[!UICONTROL Configuración avanzada]** en la esquina inferior izquierda.

   ![](assets/cp-autodelete-external.png)

   *Seleccione la opción Configuración avanzada*

1. En la **Requisito de inicio de sesión** , indique el número de días que se eliminará automáticamente un alumno si no ha accedido al sistema.
1. Haga clic en **[!UICONTROL Guardar]** para conservar la configuración realizada.
