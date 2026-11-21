---
description: Añada el servidor Adobe Learning Manager MCP a su cliente de inteligencia artificial empresarial, como Claude o ChatGPT Enterprise, para que los alumnos puedan conectarse a él
jcr-language: en_us
title: Añade Adobe Learning Manager a tu cliente de inteligencia artificial empresarial
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---

# Añade Adobe Learning Manager a tu cliente de inteligencia artificial empresarial

Necesita privilegios de administrador en su cliente de IA. Obtenga primero la URL del terminal MCP, el ID del cliente y la clave secreta de su administrador de Adobe Learning Manager. Vea **Configurar un servidor de Protocolo de contexto de modelo** para obtener más detalles.

## Agregar el conector

1. Inicie sesión como administrador en el cliente de inteligencia artificial de su empresa.
2. Abra la configuración de administrador de los conectores.
3. Agregue un conector personalizado que utilice el Protocolo de contexto de modelo.
4. Introduzca la URL del punto final de Adobe Learning Manager MCP.
5. Introduzca el ID de cliente y la clave secreta de su administrador de Adobe Learning Manager.
6. Guarde el conector.
7. Ponga el conector a disposición de los alumnos.

>[!NOTE]
>
>Las interfaces de cliente de IA cambian con frecuencia. Si estos pasos no coinciden con su cliente, consulte la documentación del proveedor de su cliente de AI para agregar un conector remoto.

## Resolución de problemas

**Los alumnos no ven el conector.** Confirme que el conector está activado para el espacio de trabajo o el grupo del alumno.

**La autorización falla cuando un alumno selecciona Connect.** Compruebe que el ID de cliente y la clave secreta coinciden con los valores de la página **Credenciales de cliente** del servidor en Adobe Learning Manager.
