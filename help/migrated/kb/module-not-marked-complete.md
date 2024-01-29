---
jcr-language: en_us
title: El módulo se marca como incompleto al finalizar el curso en Adobe Learning Manager
description: Incluso después de que un alumno complete un curso en Adobe Learning Manager, el módulo se marca como incompleto.
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---



# El módulo se marca como incompleto al finalizar el curso en Adobe Learning Manager

## Problema

Incluso después de que un alumno complete un curso en Adobe Learning Manager, el módulo se marca como incompleto.

## Causa

SCORM 2004 define los criterios de éxito y finalización y envía las sentencias para ambos por separado.

Por ejemplo, permite que haya un conjunto de contenido con un **Criterios de finalización** de vistas de diapositivas al 100 % y **Criterios de éxito** establecer como &quot;Prueba superada&quot;.

Un alumno finaliza el curso, pero suspende el cuestionario. En este caso, el progreso es del 100 %, pero el módulo se marca como incompleto porque el alumno no cumple los requisitos **Criterios de éxito**.

## Solución

El problema está relacionado con los informes **Preferencias** para el proyecto. El autor debe comprobar los criterios establecidos para la finalización y el éxito del curso.

Si se requiere algún cambio, el autor puede hacerlo mediante una herramienta de creación de contenido, como Adobe Captivate Classic. A continuación, el autor puede actualizar el módulo en consecuencia.

![](assets/scorm.png)

*Ver Preferencias De Informes De Captivate Classic*
