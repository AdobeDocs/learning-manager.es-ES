---
description: Cambios en la API de ALM
jcr-language: en_us
title: Cambios en la API en la versión de abril
source-git-commit: 7d3314f9293e1ad7e4ff4f6e537e19c82f7416e9
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Cambios en la API de la versión de mayo de 2026

## Mejora de la API GET/learningObjects

La API GET/learningObjects ahora incluye un nuevo atributo startDate en el recurso learningObjectInstance cuando se incluye la relación de instancias.

**Extremo**
GET /learningObjects/{id}?include=instance

**Cambiar**
Se ha agregado un nuevo campo, startDate, en:
included[].attributes.startDate

**Descripción**
startDate representa la fecha y hora de inicio programadas de una instancia de objeto de aprendizaje.

Ejemplo de **&#x200B;**
https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course:13209797?include=instance
Respuesta de muestra (truncada)

```
{
  "id": "course:13209797_16226533",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2026-05-20T04:35:46.000Z",
    "isAET": false,
    "isDefault": true,
    "isFlexible": false,
    "startDate": "2026-10-06T18:29:59.000Z",
    "state": "Active",
    "timeZoneCode": "IST"
  }
}
```

**Notas**

* El campo se devuelve solo para las instancias de objeto de aprendizaje aplicables.
* El valor se devuelve en formato de fecha y hora ISO 8601 UTC.
* Las integraciones existentes siguen siendo compatibles con versiones anteriores.
