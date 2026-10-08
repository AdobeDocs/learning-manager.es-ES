---
jcr-language: en_us
title: No se pueden ver los alumnos de un curso
description: En la ficha Alumnos de un curso no aparece ningún alumno inscrito en Adobe Learning Manager. Sin embargo, si genera un informe, puede ver los alumnos inscritos en el mismo.
contentowner: saghosh
exl-id: 2ea54347-fa6b-493e-b73c-d350efb2aaaf
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 58%
---
# No se pueden ver los alumnos de un curso

## Problema

No puede ver a los alumnos inscritos en un curso.

## Descripción

La ficha Alumnos de un curso no muestra ningún alumno inscrito. Sin embargo, si genera un informe, puede ver los alumnos inscritos en el mismo.

![](assets/no-learners.png)

*No se muestra ningún alumno*

## Causa

Si un alumno se inscribe a través de un objeto de aprendizaje superior (programa de aprendizaje o certificación), el alumno estará visible en la ficha Alumno del objeto de aprendizaje superior. El alumno no podrá realizar búsquedas en la ficha Alumnos del curso.

**Cómo ver a qué objeto de aprendizaje superior se inscribe el alumno?**

Puede consultar esta información en el informe Transcripciones de aprendizaje. Para generar una transcripción de alumno, siga los pasos que se indican a continuación:

1. Inicie sesión como Administrador.
1. Haga clic en **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes de Excel]** > **[!UICONTROL Transcripciones de alumnos]**.

1. Escriba el nombre del **[!UICONTROL alumno]** y especifique el intervalo de **[!UICONTROL fecha]**.
1. Expanda la sección **[!UICONTROL Opciones avanzadas]** y seleccione la opción **[!UICONTROL Activar información a nivel de módulo]**.
1. Haga clic en **[!UICONTROL Generar]**.

   En la transcripción del alumno, puede ver a qué objeto de aprendizaje superior se inscribe el alumno.
