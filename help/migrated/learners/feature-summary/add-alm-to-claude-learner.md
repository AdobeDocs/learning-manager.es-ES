---
description: Añada el servidor de Adobe Learning Manager a su propia cuenta de Claude como conector personalizado, inicie sesión y pregunte sobre su aprendizaje
jcr-language: en_us
title: Añadir Adobe Learning Manager a Claude como alumno
exl-id: 31c00b29-4919-48b7-9993-ed3ac358ba5e
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---

# Añadir Adobe Learning Manager a Claude como alumno

Siga estos pasos solo si su organización aún no ha añadido el conector para usted. Si ve un conector de Adobe Learning Manager en Claude, seleccione **Connect**.

## Agregar el conector en Claude

1. En Claude, vaya a **Personalizar** \> **Conectores**.
2. Seleccione **Agregar** (**+**) y, a continuación, seleccione **Agregar conector personalizado**.
3. Escriba un **Nombre**, como Adobe Learning Manager.
4. Escriba la dirección URL del extremo de MCP en **URL del servidor MCP remoto**.
5. Seleccione **Continuar**.
6. En **Autenticación**, mantenga **Iniciar sesión ahora**.
7. En **cliente OAuth**, seleccione **Usar su propio cliente OAuth**.
8. Escriba el Id. de cliente en **Id. de cliente**.
9. Escriba la clave secreta en **Secreto de cliente**.
10. Seleccione **Agregar**.
11. Inicie sesión en Adobe Learning Manager cuando se abra la página de inicio de sesión.

Después de iniciar sesión, el conector se muestra como conectado. Haz una pregunta sobre tu aprendizaje. Para obtener ideas, vea **solicitudes de muestra para alumnos**.

>[!IMPORTANT]
>
>Claude etiqueta el campo Secreto de cliente como opcional, pero Adobe Learning Manager lo requiere. Si lo deja vacío o introduce un valor incorrecto, el inicio de sesión falla y aparece el mensaje &quot;Error de autorización&quot;.

>[!NOTE]
>
>Las solicitudes se ejecutan con sus propios permisos. Claude solo puede ver lo que se puede ver en Adobe Learning Manager.

## Usar una cuenta de Adobe Learning Manager diferente

Si su navegador ya tiene una sesión de Adobe Learning Manager activa, Claude se conecta a esa cuenta sin pedir las credenciales. Para conectarse como otro usuario, cierre sesión primero en Adobe Learning Manager o utilice una ventana privada del navegador.

## Otros clientes de IA

Para ChatGPT u otro cliente, los pasos difieren. Consulte la documentación del cliente de AI para agregar un conector personalizado y use los mismos tres valores de su administrador.

## Resolución de problemas

**El inicio de sesión muestra un mensaje de redirección no registrado.** El administrador debe agregar el dominio Claude a **Dominios de redirección** para el servidor. Pida al administrador que agregue <https://claude.ai> e inténtelo de nuevo.

**Claude dice que la autorización falló.** Compruebe la clave secreta para ver si hay espacios adicionales o un valor incorrecto. Copie de nuevo desde el administrador, quite el conector y vuelva a agregarlo.

**Se conectó como usuario incorrecto.** Desconecte el conector, cierre sesión en Adobe Learning Manager y vuelva a conectarse en una ventana privada del navegador.

**Claude te pide que inicies sesión de nuevo.** Su sesión ha caducado o se ha revocado su acceso. Seleccione **Conectar** para iniciar sesión de nuevo.
