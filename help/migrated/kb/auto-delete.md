---
jcr-language: en_us
title: El usuario se elimina automáticamente en Learning Manager
description: Se elimina un usuario de Learning Manager. Sin embargo, el administrador no ha realizado nunca esta acción.
contentowner: nluke
exl-id: 9e293da3-bcbf-4798-b391-aef53ef8d946
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 61%

---

# El usuario se elimina automáticamente en Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problema

Se elimina un usuario de Learning Manager. Sin embargo, el administrador no ha realizado nunca esta acción.

## Causa

En Adobe Learning Manager, hay una opción que permite eliminar un usuario si este no ha iniciado sesión en el sistema durante un periodo específico.

## ¿Cómo cambiar o aplicar la configuración?

### Para alumnos internos

1. Inicie sesión como **administrador**.
1. En **Configurar**, haga clic en **Configuración** > **General**.
1. En la página Configuración general, busque la opción **Eliminar automáticamente usuarios internos**.
1. Haga clic en **[!UICONTROL Editar]** para introducir el número de días en el campo; este valor determina el periodo tras el que se eliminará un alumno si no ha accedido al sistema.

   ![](assets/cp-autodelete-internal.png)

   *Modificar el número de días*

>[!NOTE]
>
>   Deje el campo en blanco si no desea eliminar usuarios automáticamente.


1. Haga clic en **[!UICONTROL Guardar]** para conservar la configuración realizada.

### Para alumnos externos:

1. Inicie sesión como **administrador**.
1. En **Administrar**, haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Externos]**.
1. Haga clic en el nombre de un usuario externo al que se debe aplicar la configuración.

   Se abrirá la ventana **Editar perfil de registro externo**.

1. Haga clic en **[!UICONTROL Configuración avanzada]** en la esquina inferior izquierda.

   ![](assets/cp-autodelete-external.png)

   *Seleccione la opción Configuración avanzada*

1. En el campo **Requisito de inicio de sesión**, indica el número de días que un alumno debe eliminar automáticamente si no ha accedido al sistema.
1. Haga clic en **[!UICONTROL Guardar]** para conservar la configuración realizada.
