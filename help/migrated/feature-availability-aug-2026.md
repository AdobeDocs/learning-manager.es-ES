---
description: Conozca las superficies de aplicaciones compatibles con las nuevas funciones de Adobe Learning Manager para la versión de agosto de 2026, incluidas las API, los dispositivos móviles y el widget de AEM
jcr-language: en_us
title: Disponibilidad de las funciones de la versión de agosto de 2026 de Adobe Learning Manager
exl-id: e134937c-630d-4285-9181-2eca114717f6
source-git-commit: bb95f74b775d279e94fad319380d451446256636
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---


# Disponibilidad de las funciones de la versión de agosto de 2026 de Adobe Learning Manager

## Propósito

Los clientes empresariales que crean o amplían la plataforma a través de su propia interfaz de usuario (una implementación &quot;descentralizada&quot;) preguntan con regularidad si una función nueva o modificada se puede utilizar realmente fuera de la interfaz de usuario web estándar, a través de la API del alumno, la API de administración, el widget de AEM u otra superficie de integración.

Este documento proporciona una respuesta rápida y narrativa para cada función incluida en esta versión. Para cada función, este documento identifica las superficies de aplicación compatibles, la disponibilidad de la integración, la compatibilidad de la migración y cualquier comportamiento de notificación aplicable.

## Disponibilidad función por función

### Generador de correo electrónico basado en componentes

Esta será una habilitación por fases para diferentes cuentas que se registren después del lanzamiento de la función, para migrar esas cuentas del editor de correo electrónico existente al nuevo editor. Una vez activado, el cliente no puede utilizar el antiguo editor de correo electrónico. (Para habilitar las funciones, póngase en contacto con CSM/Asistencia técnica).

* **Disponible en:** Aplicación de administrador. Los administradores y los autores pueden configurar diseños y plantillas de correo electrónico aquí.
* **No aplicable:** IU orientada al alumno, API descentralizada y widget de AEM, ya que los alumnos solo reciben los correos electrónicos resultantes a través de su propio cliente de correo electrónico.
* **Notificaciones:**
  * Las notificaciones por correo electrónico se siguen distribuyendo a los alumnos en los clientes de correo electrónico compatibles.
  * Esta función no introduce ningún nuevo comportamiento de notificación en la plataforma.

### Aprendizaje externo

* **Disponible en:** web nativa, API (de alumno) descentralizada, web móvil nativa y la aplicación de administrador.
* **Aún no está disponible en:** aplicación móvil nativa.
* **API de trabajos:** No aplicable.
* **Migración:** Aún no compatible.
* **Notificaciones:**
  * Los alumnos y responsables pueden recibir notificaciones en la plataforma cuando se envían solicitudes de aprobación de aprendizaje externas y cuando se aprueban o rechazan solicitudes.
  * Actualmente no hay notificaciones por correo electrónico disponibles para este flujo de trabajo.

### Informe de usuarios incremental

* **Disponible solo en:** Job API. Proporciona una exportación incremental (delta) de datos de usuario para informes.
* **No aplicable:** IU, otras superficies de API y herramientas de migración.

### Generador de informes

* **Disponible en:** Aplicación de administrador.
* **Aún no está disponible en:** Job API. Está prevista una exportación basada en API de trabajos para una versión futura.
* **Migración:** No aplicable.
* **Notificaciones:**
  * Los usuarios reciben notificaciones en la plataforma cuando las descargas de informes están listas o cuando falla la generación de informes.
  * Las notificaciones por correo electrónico no son aplicables.

### Carpetas de contenido jerárquico

* **Disponible en:** Aplicación de administrador y aplicación de autor.
* **Migración:** admitida.
* **API de trabajos:** No aplicable. No hay ninguna superficie de API dedicada actualmente.

>[!NOTE]
>
>Los privilegios de funciones personalizadas solo se aplican en el nivel de carpeta raíz/principal, no a todas las carpetas de la jerarquía.

### Agente de información

* **Disponible en:** Aplicación de administrador. Actualmente solo está limitado a administradores completos (no a funciones personalizadas).
* **API de administración:** No disponible.
* **API de trabajos / migración:** No aplicable.

### Agente de rutas de aprendizaje

* **Disponible en:** web nativa y la API (de alumno) descentralizada.
* **Aún no está disponible en:** Native Mobile Web, Native Mobile App y AEM Widget.
* **API de trabajos / migración:** No aplicable.

### Asistente de IA (alumno)

* **Disponible en:** web nativa, API (de alumno) descentralizada y web móvil nativa.
* **Aún no está disponible en:** Aplicación móvil nativa y widget de AEM.
* **API de trabajos / migración:** No aplicable.

>[!NOTE]
>
>Esta función debe habilitarse explícitamente para que los alumnos puedan verla.

### Centro en vivo

* **Disponible en:** web nativa, API (de alumno) descentralizada, web móvil nativa y la aplicación de administrador.
* **API de trabajos:** No aplicable.
* **Migración:** No compatible actualmente.

### Administradores personalizados: Leer/Administrar otras funciones personalizadas

* **Disponible en:** Aplicación de administrador. Permite a los administradores personalizados ver y administrar otras funciones de administrador personalizadas.
* **API de trabajos / migración:** No aplicable. Aún no hay ninguna API dedicada para esto.

### Gradebook

* **Disponible en:** web nativa, API (de alumno) descentralizada, web móvil nativa, aplicación móvil nativa y la aplicación de administrador.
* **Aún no está disponible en:** AEM Widget.
* **Migración:** No compatible actualmente.
* **Notificaciones:**
  * No hay notificaciones por correo electrónico.
  * Falta de notificaciones en la plataforma

### Canales

* **Disponible en:** Native Web y la aplicación de administrador. Actualmente en beta.
* **Aún no disponible en:** API descentralizada (de alumno), web móvil, aplicación móvil, widget de AEM y API de administración.
* **API de trabajos / migración:** No aplicable.
