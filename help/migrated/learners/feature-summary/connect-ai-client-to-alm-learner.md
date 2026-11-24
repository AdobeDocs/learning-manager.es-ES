---
description: Autoriza a tu cliente de inteligencia artificial a acceder a Adobe Learning Manager una vez, para que puedas preguntar sobre tus cursos, inscripciones y rutas de aprendizaje en lenguaje natural.
jcr-language: en_us
title: Conecta tu cliente de IA a Adobe Learning Manager
exl-id: dfb3d08d-405d-468c-9126-71a345815d5c
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%
---

# Conecta tu cliente de IA a Adobe Learning Manager

## Información general

El administrador de integración debe configurar primero el conector. Si no aparece ningún conector de Adobe Learning Manager, póngase en contacto con el administrador. **El conector solo está disponible para las cuentas de nivel Adobe Learning Manager Ultimate**. Los administradores pueden ver [Agregar Adobe Learning Manager al cliente de inteligencia artificial empresarial](/help/migrated/administrators/feature-summary/add-alm-to-ai-client.md).

1. Abra el cliente de IA de su organización, como Claude o ChatGPT Enterprise.
2. Busque el conector de Adobe Learning Manager en la lista de conectores.
3. Seleccione **Conectar**.
4. Autentique la conexión y proporcione los detalles de su cuenta de Adobe Learning Manager cuando se le solicite.
5. Haz una pregunta sobre tu aprendizaje. Para obtener ideas, obtenga más información sobre [solicitudes de muestra para alumnos](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

>[!NOTE]
>
>Se autentica una vez. Las solicitudes se ejecutan con sus propios permisos, de modo que solo ve a lo que puede acceder en Adobe Learning Manager.

## Resolución de problemas

**No se encuentra el conector**
Pida al administrador que habilite el conector.

**El cliente de inteligencia artificial no recuerda tu pregunta anterior**
El servidor trata cada solicitud como nueva. Que una conversación continúe depende de tu cliente de IA. Replantea los detalles relevantes en tu próxima pregunta.

**El cliente de AI no llama al conector de Adobe Learning Manager**
Asigne un nombre a lo que desee en la pregunta, como las inscripciones o un tema del curso.
