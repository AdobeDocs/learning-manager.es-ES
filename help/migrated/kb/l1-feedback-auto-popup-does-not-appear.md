---
jcr-language: en_us
title: La ventana emergente automática de comentarios de L1 no aparece
description: Cómo resolver el error "La ventana emergente automática de comentarios de L1 no aparece"
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---



# La ventana emergente automática de comentarios de L1 no aparece

## Problema

La ventana emergente automática de comentarios de L1 no aparece para un alumno después de completar el curso.

## Causa

En ocasiones, puede suceder que un alumno no reciba los comentarios de L1 después de completar un curso concreto o que reciba un mensaje como el que se muestra a continuación:

![](assets/l1-feedback.png)

*No se pueden recibir comentarios de L1*

Esto puede deberse a las siguientes razones:

1. Los comentarios no se configuran para que aparezcan después de finalizar el curso.
1. Los recordatorios están desactivados.
1. Se ha programado la aparición de un recordatorio después de un determinado período de tiempo.

## Resolución

1. Asegúrese de que la opción &quot;Mostrar cuestionario inmediatamente después de la finalización del curso&quot; esté activada en **Curso** > **Instancias** > **Comentarios de L1**.
   <!--![](assets/l1-feedback.png)-->
1. Como administrador, vaya a **Configuración > Comentarios**. Compruebe cuándo está programado el recordatorio. En caso de que esté programado para **Después del curso** completado, cambie la opción a **En curso** finalización.
1. Habilite las siguientes plantillas de correo electrónico: **Plantillas de correo electrónico > Recordatorios y actualizaciones > Solicitar comentarios del alumno sobre el curso**. Si la opción está desactivada, actívela y pruébela.
1. Si los pasos anteriores no funcionan, elimine el recordatorio presente en **Administrador > Configuración > Comentarios**. Cree uno para &quot;Al finalizar el curso&quot; y defina la periodicidad según sea necesario.
