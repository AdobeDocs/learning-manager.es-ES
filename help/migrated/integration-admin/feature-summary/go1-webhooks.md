---
description: Descubre cómo los webhooks de finalización de Go1 ayudan a Adobe Learning Manager a recopilar las finalizaciones de los cursos, incluso cuando los alumnos cierran el navegador antes de tiempo
jcr-language: en_us
title: Seguimiento de finalización de Go1 con webhooks
exl-id: 25c9c401-905f-4408-89ac-ac630a45a0c7
source-git-commit: aaea92d190b8ab22ce9f08c309faf5caa0b58a69
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%
---

# Seguimiento de finalización de Go1 con webhooks

## Información general

Adobe Learning Manager ahora admite el seguimiento de finalización basado en webhook para el contenido de Go1. Esta mejora mejora la fiabilidad de la sincronización de finalización de cursos entre Go1 y Learning Manager. Los eventos de finalización se capturan incluso cuando los alumnos salen del reproductor del curso justo después de finalizar un curso.

Go1 utiliza webhooks para enviar notificaciones de finalización de cursos a Learning Manager cada vez que un alumno finaliza un curso de Go1. Learning Manager recibe y procesa estos eventos de finalización independientemente de la sesión del explorador del alumno.

Go1 también reintenta la entrega de webhook hasta que Learning Manager acuse recibo del evento de finalización. Esto ayuda a evitar registros de aprendizaje perdidos o incompletos.

## Problema que resuelve esta mejora

Anteriormente, el seguimiento de la finalización se basaba en la comunicación entre el reproductor Go1 y el administrador de aprendizaje, mientras que la sesión del navegador del alumno permanecía activa. Si un alumno cerraba la ventana del navegador o se alejaba antes de que se procesara por completo el estado de finalización, se podía perder el registro de finalización.

Como resultado:

* Es posible que las finalizaciones de los cursos no aparezcan en las transcripciones de alumnos.
* Los administradores podían encontrar discrepancias entre las finalizaciones reales y las registradas.
* Los eventos de finalización perdidos no se pudieron recuperar automáticamente.

## Flujo de trabajo de eventos

1. Un alumno inicia y completa un curso de Go1.
1. Go1 registra la finalización.
1. Go1 envía un webhook de finalización a Learning Manager.
1. Learning Manager valida y acepta el evento de finalización.
1. Learning Manager actualiza el estado de finalización del alumno.
1. Si Learning Manager no reconoce el evento, Go1 reintenta la entrega automáticamente.

## Preguntas frecuentes

**Este cambio requiere configuración de administrador**

No, este cambio no requiere ninguna configuración de administrador.

**Se ven afectados los cursos Go1 existentes**

No, los cursos Go1 existentes no se ven afectados. La mejora mejora mejora la sincronización de finalización del contenido de Go1.

**Qué sucede si un alumno cierra el explorador antes de tiempo**

Go1 envía el webhook de finalización independientemente de la sesión del explorador del alumno. Aunque el alumno salga del reproductor del curso, Go1 sigue reintentando la entrega hasta que Learning Manager reconoce el evento de finalización.
