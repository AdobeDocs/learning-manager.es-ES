---
title: Subtítulos opcionales en sesiones de Live Hub
description: Aprenda cómo los subtítulos opcionales muestran el contenido hablado en tiempo real para que los instructores y los alumnos puedan seguirlo durante las sesiones de Live Hub.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 574ba5fd9ac9dc02130a39006574c9ca1ce6c1d1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 4%
---

# Explicación de los subtítulos opcionales

Los subtítulos opcionales se generan automáticamente durante una sesión de Live Hub y se actualizan continuamente mientras los asistentes hablan. Los subtítulos aparecen en un área de presentación dedicada y se muestran en el idioma seleccionado por el instructor en **Configuración de la sala**.

Tanto los instructores como los participantes pueden ver los subtítulos. Cada asistente puede mostrar u ocultar los subtítulos de forma independiente sin que esto afecte a la configuración de los subtítulos de otros asistentes.

Solo los instructores pueden cambiar el idioma de los subtítulos. Los participantes solo pueden ver los subtítulos en el idioma elegido por los instructores. Los participantes no pueden cambiar el idioma de los subtítulos.

## Cómo determina Live Hub el idioma de los subtítulos

Live Hub selecciona automáticamente el idioma de los subtítulos en función del siguiente orden de prioridad:

1. **Idioma del curso:** Live Hub usa el idioma del curso si es compatible con subtítulos. Para un curso multilingüe, si la instancia del curso actual utiliza un idioma que no admite subtítulos opcionales, Live Hub selecciona el idioma de la primera instancia del curso que admite subtítulos opcionales. Vea [Idiomas admitidos en ALM](../../migrated/languages-supported.md) para obtener más información.
1. **Idioma de la cuenta:** Si el idioma del curso no es compatible, Live Hub comprueba el idioma de la cuenta y lo utiliza si es compatible.

>[!NOTE]
>
>Si no se admite el idioma del curso ni el de la cuenta, Live Hub selecciona inglés como idioma de los subtítulos. Además, los subtítulos están desactivados de forma predeterminada y deben habilitarse manualmente.

## Idiomas admitidos para los subtítulos opcionales

Live Hub admite subtítulos opcionales en los siguientes idiomas:

* Inglés
* Francés
* Alemán
* Chino
* Español
* Italiano
* Japonés
* Portugués
* Danés
* Neerlandés
* Finés
* Turco
* Coreano
* Noruego
* Sueco
* Ruso

## Cómo funcionan los subtítulos opcionales

En una sesión de Live Hub, los subtítulos opcionales se generan automáticamente. Los subtítulos se muestran en un panel dedicado y se actualizan continuamente a medida que hablan los participantes. Tanto los instructores como los alumnos pueden ver los subtítulos.

Cada participante puede mostrar u ocultar los subtítulos como prefiera. El cambio de esta configuración no afecta a otros participantes.

![](assets/closed-captions-overview.png)
*Interfaz de Live Hub que muestra los subtítulos opcionales en la sesión*

## Funciones y permisos

La función **subtítulos opcionales** está disponible para instructores y alumnos en una sesión de Live Hub. Las acciones disponibles varían según la función de usuario.

| **Instructores** | **Alumnos** |
|---|---|
| [Mostrar subtítulos opcionales](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#display-closed-captions) | [Mostrar subtítulos opcionales](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#display-closed-captions) |
| [Cambiar el aspecto de los subtítulos opcionales](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#change-the-appearance-of-closed-captions) | [Cambiar el aspecto de los subtítulos opcionales](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#change-the-appearance-of-closed-captions) |
| [Seleccionar idioma de subtítulos](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#select-the-caption-language) | |