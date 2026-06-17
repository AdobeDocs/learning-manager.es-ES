---
jcr-language: en_us
title: Limitaciones de Report Builder en Adobe Learning Manager
description: Entiende qué es lo que no admite Report Builder en esta versión para que puedas planificar tu enfoque de creación de informes en consecuencia.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Limitaciones de Report Builder en Adobe Learning Manager

Report Builder cubre una amplia gama de necesidades de informes personalizados, pero algunos tipos de informes, conjuntos de datos y configuraciones no se admiten en esta versión. En esta sección se enumeran las limitaciones conocidas y se sugieren soluciones alternativas cuando estén disponibles.

## Certificaciones periódicas

Algunas consultas que implican certificaciones periódicas no funcionan correctamente en Report Builder en esta versión. Si el informe implica ciclos de certificación recurrentes, como el seguimiento de la nueva inscripción o la nueva finalización en varios períodos de certificación, utilice en su lugar los informes de certificación existentes en Adobe Learning Manager.

## Conjuntos de datos y tipos de informes no compatibles

Los siguientes elementos no están disponibles en Report Builder en esta versión:

* **Datos de resultados empresariales**: Report Builder no admite integraciones de Traer tus propios datos (BYOD). No se admiten informes que combinan datos empresariales externos con datos de LMS.
* **Informes de auditoría**: Las pistas de auditoría del sistema y los registros de actividad del administrador no se pueden crear en Report Builder. Utilice los informes de auditoría existentes en la vista de administrador para estos datos.
* **Informes incrementales**: Report Builder genera informes de instantáneas completos cada vez. No se admiten los informes incrementales que devuelven sólo los registros cambiados desde la última descarga. Para los datos incrementales, utilice la API de trabajos.

## Limitaciones de informes de tendencias

### Solo una columna de fecha por informe de tendencia

Un único informe de tendencias solo puede agrupar por una columna basada en fechas. No se pueden combinar dos tendencias basadas en fechas diferentes en el mismo informe.

Por ejemplo, puede generar:

* Un informe que muestra **inscripciones por mes** (agrupadas por fecha de inscripción)
* Un informe independiente que muestra **finalizaciones por mes** (agrupadas por fecha de finalización)

No se puede crear un único informe que muestre el mes de inscripción y el mes de finalización como columnas de tendencia independientes. Para obtener ambos, cree dos informes independientes y analícelos en paralelo.

### Las tendencias reflejan los datos actuales, no las instantáneas históricas

Los informes de tendencias en Report Builder se basan en datos actuales puntuales, no en instantáneas históricas. El informe refleja el estado actual de los registros, distribuidos en los campos de fecha.

Esto significa:

* Es posible que un alumno que se inscribió en enero pero que más tarde se dio de baja no aparezca en la tendencia de inscripción de enero
* Un grupo de usuarios reorganizado no reflejará su pertenencia histórica en los últimos meses
* Es posible que los registros eliminados no aparezcan en la tendencia durante el período en el que estuvieron activos

Utiliza los informes de tendencias para el análisis direccional. Para realizar registros históricos precisos o auditorías, utilice los informes fijos existentes o las exportaciones de la API de trabajos.
