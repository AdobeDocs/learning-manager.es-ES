---
description: Los administradores pueden ejecutar una sesión suplantada en la que pueden iniciar sesión en nombre de cualquier usuario de su cuenta con las funciones de alumno y responsable.
jcr-language: en_us
title: Suplantación del alumno y el responsable
contentowner: saghosh
exl-id: 0306f255-283f-43b9-9494-11b3dc3765da
source-git-commit: b5bbb184fc86965255b0247195a50cc65a03cd1a
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 56%

---

# Suplantación del alumno y el responsable {#impersonation-of-learner-and-manager}

En grandes organizaciones, el personal de asistencia al cliente necesita una capacidad de suplantación para depurar los problemas a los que se enfrentan los alumnos.

Con esta capacidad para suplantar a otros usuarios, los administradores pueden identificar y realizar todas las actividades realizadas por los alumnos y responsables de su organización.

>[!NOTE]
>
>Los administradores personalizados no tienen la capacidad de suplantar a usuarios; solo los administradores pueden realizar la suplantación de usuarios.

## Cómo funciona

Los administradores pueden buscar un usuario (interno o externo) y, a continuación, suplantar a un usuario. A continuación, se redirige al administrador a la página del usuario (en la aplicación del responsable si corresponde o la aplicación del alumno) y, a continuación, se cierra la sesión del administrador. A continuación, se redirige al administrador a la página Completar el perfil, si se ha configurado para el usuario que suplanta el administrador.

Esto es lo que debe tener en cuenta al hacerse pasar por un usuario:

* Todos los administradores ven esta función de forma predeterminada.
* Solo se pueden suplantar los usuarios activos de la cuenta.
* Un administrador no puede suplantarse a sí mismo.
* Un administrador solo puede suplantar durante 60 minutos.
* Un administrador personalizado con acceso de solo lectura no puede suplantar a los usuarios.

## Suplantar a un usuario

Para suplantar un usuario, siga los pasos que se indican continuación:

1. Inicie sesión en la aplicación como administrador.
1. Seleccione Perfil > Suplantar usuario.

   A la vez, solo puede suplantar a un usuario.

1. Busque un usuario (interno o externo) en el cuadro de búsqueda presente en el modo. Solo se puede suplantar a un usuario cada vez. Seleccione Continuar.

   También puede buscar con el correo electrónico del usuario, UUID, etc.

1. Aparece un mensaje para confirmar que suplantará a un usuario.

   Seleccione Continuar.

   Un mensaje de confirmación, &quot;Impersonation Mode: You are logged in as &quot;username (user email). Logout&quot; aparece en el encabezado de la página.

**Una sesión suplantada dura 60 minutos.**

Al cambiar a una función de alumno o responsable, aparece un mensaje que indica que el administrador se encuentra en un modo de suplantación del usuario.

## Inicio de sesión e informe de acceso

El inicio de sesión y el acceso de un administrador se capturan en el informe de inicio de sesión y acceso. Para cada usuario suplantado por el administrador, se crea un registro en el informe.

Las columnas que forman parte de esta función son:

* Suplantado por nombre de usuario
* Suplantado por correo electrónico del usuario

Estas columnas se añaden al final del informe.

Cada inicio de sesión se cuenta por separado en el informe.

## Actividades no admitidas

* Suplantación de componentes AEM.
* Suplantación en la aplicación móvil.
* Suplantación en la experiencia móvil envolvente.
* Suplantación de aplicaciones envolventes. Solo es aplicable a las aplicaciones de ALM.

## Preguntas más frecuentes

+++¿Puedo iniciar sesión en Adobe Learning Manager incluso cuando me están suplantando?

Sí, el inicio de sesión de un usuario es independiente de la suplantación.
+++

+++¿Se cuentan de forma exclusiva los eventos de suplantación?

Sí, cada acceso de inicio de sesión o visita del administrador mientras se realiza la suplantación se contará por separado.
+++

+++¿Cuál es el tiempo de espera de suplantación?

60 minutos. Si un usuario que está suplantando cierra la ventana del navegador y, a continuación, se desplaza a cualquier URL principal en un plazo de 60 minutos, la actividad de suplantación continuará y se deberá mostrar el mensaje del banner.
+++
