---
description: Registre el servidor Adobe Learning Manager MCP como conector en su cliente de IA empresarial para que los alumnos de su organización puedan conectarse y consultar su aprendizaje.
jcr-language: en_us
title: Añade Adobe Learning Manager a tu cliente de inteligencia artificial empresarial
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---

# Añade Adobe Learning Manager a tu cliente de inteligencia artificial empresarial

## Información general

Necesita privilegios de administrador en su cliente de IA. Antes de empezar, obtenga la URL del terminal de MCP, el ID del cliente y la clave secreta de su administrador de Adobe Learning Manager. Más información sobre [configurar un servidor de Protocolo de contexto de modelo](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).

## Agregar el conector

1. Inicie sesión como administrador en el cliente de inteligencia artificial de su empresa.
2. Abra la configuración del administrador para conectores.
3. Agregue un conector personalizado que utilice el Protocolo de contexto de modelo.
4. Introduzca la URL del punto final de Adobe Learning Manager MCP.
5. Introduzca el ID de cliente y la clave secreta de su administrador de Adobe Learning Manager.
6. Guarde el conector.
7. Ponga el conector a disposición de los alumnos.

>[!NOTE]
>
>Las interfaces de cliente de IA cambian con frecuencia. Si estos pasos no coinciden con su cliente, consulte la documentación de su proveedor de clientes de AI para agregar un conector remoto.

## Resolución de problemas

**Los alumnos no ven el conector.**
Confirme que el conector está activado para el espacio de trabajo o el grupo del alumno.

**La autorización falla cuando un alumno selecciona Conectar.**
Compruebe que el ID de cliente y la clave secreta coinciden con los valores de la página **Credenciales de cliente** del servidor en Adobe Learning Manager.
