---
description: Permite a los alumnos descubrir cursos, realizar un seguimiento del progreso y obtener respuestas del contenido de Adobe Learning Manager en Claude, ChatGPT Enterprise y agentes personalizados.
jcr-language: en_us
title: Servidor de Adobe Learning Manager Model Context Protocol
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: f6dc1e97076edf812862b80a6ed5931989c660da
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%
---

# Servidor de Adobe Learning Manager Model Context Protocol

## Información general

El protocolo de contexto de modelo (MCP) es una forma estándar de que un cliente de IA se conecte a las herramientas. El servidor MCP de Adobe Learning Manager lleva el aprendizaje al lugar en el que ya trabajan los alumnos. Expone las herramientas de aprendizaje de Adobe Learning Manager a cualquier cliente de IA compatible con MCP, como un agente empresarial personalizado, Claude o ChatGPT. Los alumnos pueden acceder a sus cursos de formación y a su progreso desde el mismo cliente, mientras que el contenido permanece en Adobe Learning Manager.

## Capacidades del alumno

Los alumnos trabajan con lenguaje natural en el cliente de IA que ya utilizan. El cliente interpreta cada solicitud, llama a la herramienta de alumno de Adobe Learning Manager adecuada y devuelve una respuesta en función de los derechos de acceso de dicho alumno. Los alumnos pueden:

* Descubre los cursos, las certificaciones y las rutas de aprendizaje disponibles para ellos.
* Realiza un seguimiento de sus inscripciones, el progreso y los plazos, incluido el aprendizaje que está a punto de caducar.
* Obtén respuestas basadas en el contenido de aprendizaje.
* Genera una ruta de aprendizaje personalizada a partir de sus objetivos y guárdala.
Para obtener la lista completa, consulte la **referencia de herramientas del alumno**.

El cliente de AI llama al servidor MCP, que enruta cada solicitud a la herramienta de alumno correspondiente.

Para obtener la lista completa, consulte la **referencia de herramientas del alumno**.

## Educación de clientes y socios

La educación de clientes y socios es un uso primordial del servidor MCP. Las organizaciones que crean sus propios agentes de IA empresarial pueden conectarlos a las herramientas de aprendizaje de Adobe Learning Manager. Sus clientes y socios aprenden dentro del asistente que ya utilizan, sin tener que cambiar a otro asistente de aprendizaje.

Por ejemplo, Acme Inc. crea su propio asistente de inteligencia artificial empresarial. Un socio de Acme Inc. visita el entorno de Tech Corp para obtener información sobre los productos de Tech Corp. El asistente de Acme se conecta a su cuenta de Adobe Learning Manager a través del servidor MCP y devuelve respuestas relacionadas con el aprendizaje, por lo que el socio nunca abandona la experiencia de Acme.

Este enfoque permite a las organizaciones:

* Ofrece formación a través de la experiencia de IA existente de un partner.
* Deja que los agentes empresariales personalizados utilicen las herramientas de aprendizaje de Adobe Learning Manager.
* Incorpora el aprendizaje en sus propios flujos de trabajo.
* Integra el aprendizaje con su ecosistema de IA empresarial.

## Educación de los empleados

Los empleados que ya utilizan un cliente de IA, como Claude, pueden obtener allí su información de aprendizaje. Por ejemplo, un empleado puede comprobar el aprendizaje asignado, revisar inscripciones, buscar cursos sobre un tema o solicitar una ruta de aprendizaje, sin cambiar a Adobe Learning Manager. Para ver solicitudes de muestra, consulte [solicitudes de muestra para alumnos](https://word-edit.officeapps.live.com/docs/sample-prompts-adobe-learning-manager-learners).

Este enfoque permite a los empleados:

* No te salgas de las herramientas que ya utilizan.
* Llega a su aprendizaje dondequiera que trabajen.
* Utilice cualquier cliente de AI que admita MCP como punto de entrada a Adobe Learning Manager.
* Obtenga información de aprendizaje sin cambiar el contexto.

## Un servidor para ambas audiencias

La educación de clientes y partners, y la educación de empleados utilizan las mismas herramientas de aprendizaje y el mismo servidor. Solo cambia la audiencia. Elige el enfoque que encaje con los alumnos.

| **Público** | **Ejemplo** | **Dónde trabajan los alumnos** |
|----|----|----|
| Externo | Clientes y socios | El agente de inteligencia artificial empresarial de su propia organización |
| Interno | Empleados | Un cliente de IA empresarial, como Claude o ChatGPT Enterprise |

## Configurar funciones

La configuración se divide en tres funciones.

* **Administrador:** Crea una aplicación cliente MCP en Adobe Learning Manager y la administra. Consulte [configurar un servidor MCP](https://word-edit.officeapps.live.com/docs/configure-model-context-protocol-server-adobe-learning-manager).
* **Administrador de clientes de IA:** Agrega el servidor al cliente de IA empresarial de la organización, como Claude o ChatGPT Enterprise.
* **Alumno:** Selecciona **Connect** en el cliente de IA, autentica la conexión y proporciona los detalles de su cuenta de Adobe Learning Manager.

## Seguridad de las solicitudes de alumnos

Cada alumno autentica la conexión y proporciona los detalles de su cuenta de Adobe Learning Manager. La solicitud se ejecuta como ese alumno, por lo que el cliente de IA devuelve únicamente la información a la que el alumno puede acceder en Adobe Learning Manager. El servidor no concede a los alumnos acceso adicional.

## Limitaciones de MCP en esta actualización

* La disponibilidad de las herramientas depende de lo que admita tu cliente de IA.
* Cada solicitud se trata como nueva. Las conversaciones de varias vueltas solo funcionan si tu cliente de inteligencia artificial mantiene el contexto de la conversación.
