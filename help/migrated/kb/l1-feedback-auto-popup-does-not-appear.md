---
jcr-language: en_us
title: La ventana emergente automática de comentarios de L1 no aparece
description: Cómo resolver el error "La ventana emergente automática de comentarios de L1 no aparece"
contentowner: saghosh
exl-id: 47edcd7f-e332-4a75-a025-fd07737d0b70
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 76%

---

# La ventana emergente automática de comentarios de L1 no aparece

## Problema

La ventana emergente automática de comentarios de L1 no aparece para un alumno después de completar el curso.

## Causa

Es posible que a veces un alumno no reciba los comentarios de L1 después de completar un curso específico o que reciba un mensaje como el que se muestra a continuación:

![](assets/l1-feedback.png)

*No se pueden recibir comentarios de L1*

Esto puede deberse a varios motivos:

1. Los comentarios no se han configurado para que aparezcan tras la finalización del curso.
1. Los recordatorios están desactivados.
1. Se ha programado la aparición de un recordatorio después de un determinado periodo.

## Resolución

1. Asegúrese de que la opción &quot;Mostrar cuestionario inmediatamente después de la finalización del curso&quot; esté habilitada en **Curso** > **Instancias** > **Comentarios de L1**.
   <!--![](assets/l1-feedback.png)-->
1. Como administrador, vaya a **Configuración > Comentarios**. Compruebe cuándo está programado el recordatorio. En el caso de que esté programado para **Tras finalizar el curso**, cambie la opción a **Al finalizar el curso**.
1. Habilite las siguientes plantillas de correo electrónico: **Plantillas de correo electrónico > Recordatorios y actualizaciones > Solicitar comentarios del alumno sobre el curso**. Si la opción está desactivada, actívela y pruébela.
1. Si los pasos anteriores no funcionan, elimine el recordatorio presente en **Administración > Configuración > Comentarios**. Cree uno para &quot;Al finalizar el curso&quot; y defina la periodicidad según sea necesario.
