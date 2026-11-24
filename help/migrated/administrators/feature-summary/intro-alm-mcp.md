---
description: Amplía Adobe Learning Manager a Claude, ChatGPT Enterprise y agentes personalizados para que los alumnos puedan encontrar cursos, realizar un seguimiento del progreso y obtener respuestas.
jcr-language: en_us
title: Servidor de Adobe Learning Manager Model Context Protocol
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---

# Servidor de Adobe Learning Manager Model Context Protocol

El protocolo de contexto de modelo (MCP) es un estándar abierto que permite a un cliente de IA descubrir e invocar herramientas externas. El servidor Adobe Learning Manager MCP expone las herramientas de Adobe Learning Manager Learning a cualquier cliente compatible con MCP, como un agente empresarial personalizado, Claude o ChatGPT Enterprise. Los alumnos obtienen su formación y progreso del cliente que ya utilizan, mientras que el contenido y los registros de aprendizaje permanecen en Adobe Learning Manager.

## Cómo funciona

Un alumno envía una solicitud en lenguaje natural a un cliente de IA. El cliente selecciona la herramienta de alumno más relevante y llama al servidor MCP con el token de acceso de OAuth del alumno. Adobe Learning Manager ejecuta la herramienta como ese alumno y devuelve el resultado, y el cliente compone la respuesta final.

Cada llamada incluye la identidad del alumno. Por lo tanto, un alumno puede recuperar solo el contenido y los registros a los que ya tiene permiso de acceso.

El cliente de AI llama al servidor MCP, que enruta cada solicitud a la herramienta de alumno correspondiente.

## Capacidades del alumno

Los alumnos trabajan con lenguaje natural en el cliente de IA que ya utilizan. El cliente interpreta cada solicitud, llama a la herramienta de alumno de Adobe Learning Manager adecuada y devuelve una respuesta en función de los derechos de acceso de dicho alumno. Los alumnos pueden:

* Descubre los cursos, las certificaciones y las rutas de aprendizaje disponibles para ellos.
* Realiza un seguimiento de sus inscripciones, el progreso y los plazos, incluido el aprendizaje que está a punto de caducar.
* Obtén respuestas basadas en el contenido de aprendizaje.
* Genera una ruta de aprendizaje personalizada a partir de sus objetivos y guárdala.

Para obtener la lista completa, consulte la **referencia de herramientas del alumno**.

## Educación de clientes y socios

>[!IMPORTANT]
>
>Los clientes que crean sus propios agentes empresariales también pueden conectarse al servidor. Por ejemplo, una organización asociada puede ofrecer a sus propios clientes acceso al aprendizaje a través de su propio agente.

La educación de clientes y socios es un uso primordial del servidor MCP. Las organizaciones que crean sus propios agentes de IA empresarial pueden conectarlos a las herramientas de aprendizaje de Adobe Learning Manager. Sus clientes y socios aprenden dentro del asistente que ya utilizan, sin tener que cambiar a otro asistente de aprendizaje.

Por ejemplo, Acme Inc. crea su propio asistente de inteligencia artificial empresarial. Un socio de Acme Inc. visita al asistente para obtener información sobre los productos de Acme Inc. El asistente se conecta a la cuenta de Adobe Learning Manager de Acme Inc. a través del servidor MCP y devuelve respuestas relacionadas con el aprendizaje. El socio nunca abandona la experiencia de Acme Inc.

Este enfoque permite a las organizaciones:

* Ofrece formación a través de la experiencia de IA existente de un partner.
* Amplía los agentes empresariales personalizados con las herramientas de aprendizaje de Adobe Learning Manager.
* Integra la formación en sus propios flujos de trabajo.
* Integra el aprendizaje con su ecosistema de IA empresarial.

## Educación de los empleados

Los empleados que ya utilizan un cliente de IA, como Claude, pueden obtener allí su información de aprendizaje. Por ejemplo, un empleado puede comprobar el aprendizaje asignado, revisar inscripciones, buscar cursos sobre un tema o solicitar una ruta de aprendizaje, sin cambiar a Adobe Learning Manager. Para solicitudes de muestra, obtenga más información sobre [solicitudes de muestra para alumnos](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

Este enfoque permite a los empleados:

* Permanecer en las herramientas que ya utilizan.
* Llega a su aprendizaje dondequiera que trabajen.
* Utiliza cualquier cliente de IA compatible con MCP como punto de entrada a Adobe Learning Manager.
* Recupere información de aprendizaje sin cambiar el contexto.

## Un servidor para ambas audiencias

La educación de clientes y partners, y la educación de empleados utilizan las mismas herramientas de aprendizaje y el mismo servidor. Solo cambia la audiencia. Elige el enfoque que encaje con los alumnos.

| **Público** | **Ejemplo** | **Dónde trabajan los alumnos** |
|----|----|----|
| Externo | Clientes y socios | El agente de inteligencia artificial empresarial de su propia organización |
| Interno | Empleados | Un cliente de IA empresarial, como Claude o ChatGPT Enterprise |

## Configurar funciones

El programa de instalación se divide en tres funciones.

* **Administrador:** Crea una aplicación cliente MCP en Adobe Learning Manager y la administra. Más información sobre [configurar un servidor MCP](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).
* **Administrador de clientes de IA:** Agrega el servidor al cliente de IA empresarial de la organización, como Claude o ChatGPT Enterprise.
* **Alumno:** Selecciona **Connect** en el cliente de IA, autentica la conexión y proporciona los detalles de su cuenta de Adobe Learning Manager.

## Seguridad de las solicitudes de alumnos

Cada alumno autentica la conexión y proporciona los detalles de su cuenta de Adobe Learning Manager. Cada solicitud se ejecuta como ese alumno, por lo que el cliente de IA devuelve únicamente la información a la que el alumno puede acceder en Adobe Learning Manager. El servidor no concede a los alumnos acceso adicional.

## limitaciones

* El servidor MCP solo está disponible para las cuentas de nivel Adobe Learning Manager Ultimate.
* La disponibilidad de las herramientas depende de lo que admita tu cliente de IA.
* El servidor trata cada solicitud como nueva. Las conversaciones de varias vueltas solo funcionan si su cliente de inteligencia artificial conserva el contexto de la conversación.
