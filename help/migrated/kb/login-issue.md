---
jcr-language: en_us
title: Problemas de inicio de sesión en Learning Manager
description: Problemas de inicio de sesión en Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---



# Problemas de inicio de sesión en Learning Manager

## Problema

No se puede iniciar sesión en Adobe Learning Manager.

## Error

Al intentar iniciar sesión en Adobe Learning Manager, aparece el mensaje de error siguiente:

![](assets/cp-error.png)

*Mensaje de error de una sesión caducada*

## Razón

Cuando un usuario inicia sesión mediante SSO, crea una cookie de sesión que se almacena en el navegador. También permite al usuario iniciar sesión en otras aplicaciones. La mayoría de los SSO están configurados para cerrar sesión después de 24 horas. El usuario debe autenticarse de nuevo para una nueva sesión.

En determinados casos, un usuario no puede acceder al sistema debido a cookies de SSO obsoletas. Estas cookies se reenvían a Adobe Learning Manager para su autenticación. La sesión no finaliza si un usuario no cierra el navegador durante mucho tiempo o no ha cerrado la sesión.

Adobe Learning Manager rechaza estas cookies obsoletas, lo que genera un error.

## Resolución

Si Adobe Learning Manager rechaza una cookie obsoleta, pruebe las opciones que se indican a continuación:

1. Borre las cookies y la memoria caché del navegador. Para obtener más información, consulte este artículo [documento](unable-log-in-learning-manager.md).

   Como alternativa, el administrador de IDP puede definir un cierre de sesión forzado después de un tiempo determinado. Este paso autentica de nuevo al usuario para iniciar una nueva sesión.

Hay otras razones por las que se produce este error, pero la anterior es una situación común.

## Vínculos de referencia:

[Microsoft: sesión de acceso condicional en la vida](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
