---
jcr-language: en_us
title: Imposible registrarse como usuario externo
description: Los alumnos externos no pueden registrarse en un perfil en Adobe Learning Manager.
contentowner: nluke
exl-id: b1a9ecb6-75a8-44f7-b169-f77d7a4f6c2c
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 50%

---

# Imposible registrarse como usuario externo

## Problema

Los alumnos externos no pueden registrarse en un perfil.

## Error

El ID de correo electrónico ya está registrado. Utilice un correo electrónico diferente.

![](assets/cp-register-profile.png)

*Mensaje de error de un correo electrónico ya registrado*

## Descripción

Hay situaciones en las que un usuario no puede registrarse en un perfil externo. El usuario recibe el error mostrado anteriormente al registrarse.

## Causa

Este problema se produce en uno de los casos siguientes:

* El usuario ya está registrado en otro perfil externo.
* El usuario ya es un alumno interno.
* El usuario presenta el estado Eliminado.

## Solución:

**Escenario 1:** El usuario ya está registrado en otro perfil externo.

1. Inicie sesión como Administrador.
1. En **Administrar**, haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Externos]**.
1. Abra el perfil del que el usuario ya forma parte. Para ello, haga clic en Puestos usados.

   ![](assets/cp-seats-used.png)

   *Abrir perfil del usuario*

1. Seleccione el usuario, haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Cambiar perfil]**.

   ![](assets/cp-change-profile.png)

   *Cambiar el perfil del usuario*

   Se abrirá una ventana para seleccionar un nuevo perfil, como se muestra a continuación.

   ![](assets/cp-select-profiles.png)

   *Seleccionar perfil de usuario*

1. Una vez seleccionado, haga clic en **[!UICONTROL Cambiar]**.

**Situación 2:** El usuario está presente como alumno interno.

1. Inicie sesión como Administrador.
1. En **Administrar**, haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Internos]**.
1. Haga clic para abrir un perfil de alumno y haga clic en el icono Editar.

   ![](assets/cp-internal-learner.png)

   *Abrir un perfil de alumno interno*

1. Cambie la dirección de correo electrónico del alumno o agregue *_old* a la dirección de correo electrónico existente. Esto liberará la dirección de correo electrónico.

   Por ejemplo, si la dirección de correo electrónico del alumno es *<abc@adobe.com>,* cámbiela a *<abc_old@adobe.com>*

1. Haga clic en **Guardar** para conservar los cambios realizados.

**Situación 3**: el usuario presenta el estado Eliminado.

1. Inicie sesión como Administrador.
1. En **Administrar**, haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Limpieza de usuarios]**.
1. Seleccione el alumno y haga clic en el icono Editar.

   ![](assets/cp-deleted-learner.png)

   *Modificar la dirección de correo electrónico del usuario*

1. Cambie la dirección de correo electrónico del alumno o agregue *_old* a la dirección de correo electrónico existente. Esto liberará la dirección de correo electrónico.

   Por ejemplo, si la dirección de correo electrónico del alumno es **<abc@adobe.com>**, cámbiela a **<abc_old@adobe.com>**.
