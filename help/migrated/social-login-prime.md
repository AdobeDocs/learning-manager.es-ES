---
jcr-language: en_us
title: Inicio de sesión en red social en Learning Manager
description: Inicio de sesión en red social en Learning Manager
contentowner: saghosh
preview: true
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%
---


# Inicio de sesión en red social en Learning Manager

Puede utilizar sus credenciales de Facebook, LinkedIn o Twitter para iniciar sesión en Learning Manager.

## Configurar inicio de sesión social {#setupsociallogin}

1. Póngase en contacto con su responsable de éxito de clientes, si desea que configure la cuenta.

   De lo contrario, siga los pasos que se indican a continuación.

1. Busque la cuenta en la que desea configurar el inicio de sesión social.
1. Cambie el inicio de sesión a SSO.
1. Haga clic en Avanzadas. Especifique el JSON siguiente.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   Si es un JSON incorrecto, se producirá una excepción.

   Esta función de inicio de sesión social solo se utiliza para usuarios INTERNOS.

