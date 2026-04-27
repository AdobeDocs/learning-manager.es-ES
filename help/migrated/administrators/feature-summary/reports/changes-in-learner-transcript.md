---
description: Información sobre transcripciones de alumnos
jcr-language: en_us
title: Cambios en las transcripciones de alumnos
exl-id: 295c4e1f-c3c7-4f97-83c3-1234f3d47546
source-git-commit: 4a4c42968caf6c0c8265014d99a2211da4c1cbb9
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Cambios en las transcripciones de alumnos en la versión de abril

## Columna Método de finalización

La columna **Método de finalización** indica cómo se completó cada registro de la transcripción del alumno del administrador.

**Valores:**

1. **Directo** (para finalizaciones directas)
2. **Alternativa** (para las finalizaciones logradas mediante relaciones alternativas)
3. **Alternativa revocada** (cuando se revocan todas las finalizaciones alternativas debido a infinalización retroactiva y eliminación de relaciones)

>[!NOTE]
>
>Esta columna no está visible en el LT del alumno; solo está disponible en el LT de administrador para realizar informes y realizar un seguimiento.

**Impacto**: permite a los administradores tener pistas de auditoría claras, seguimiento del cumplimiento y transparencia sobre cómo se completó un curso.

## Seguimiento alternativo de finalización en transcripciones de alumnos

Las finalizaciones alternativas permiten que los alumnos reciban el crédito de finalización de un curso de destino o una ruta de aprendizaje cuando hayan completado un curso de origen o una ruta de acceso equivalente, en función de las relaciones establecidas.

En la transcripción del alumno (LT), las finalizaciones alternativas afectan a tres columnas existentes: **Estado**, **Fecha de finalización** y **Origen de finalización**.

- **Estado**: el estado puede ser **Completado** incluso si el alumno no ha completado directamente el curso o la ruta de acceso de destino debido a una finalización alternativa. Otros estados (**No iniciado**, **En curso**, **Dado de baja**) no se ven afectados.
- **Fecha de finalización**: para una finalización alternativa, la fecha se hereda del curso o ruta de acceso de origen. Si más tarde el alumno completa el objetivo directamente, la fecha se actualiza para reflejar la finalización directa.
- **Origen de finalización**: captura los identificadores de formación de los cursos o rutas de acceso de origen que proporcionaron la finalización alternativa. Varios orígenes activos se muestran como ID separados por comas. Si se revocan los orígenes, solo se conservan los activos. Cuando existen varios orígenes, se utiliza la fecha de finalización más temprana.

**Impacto**: las finalizaciones alternativas reducen la reconciliación manual, automatizan el seguimiento del progreso en las certificaciones y rutas de aprendizaje, y cumplen los requisitos de cumplimiento.

>[!NOTE]
>
>Las transcripciones de alumnos no muestran la columna **Método de finalización**. Esta columna solo está disponible en la transcripción del alumno del administrador.

## Lógica de fecha de finalización para alternativas

La columna **Fecha de finalización** de la transcripción del alumno se utiliza para finalizaciones directas y alternativas.

- Para finalizaciones alternativas, la fecha refleja cuándo el alumno ha completado el curso o la ruta de origen.
- Si más tarde el alumno completa el objetivo directamente, la fecha de finalización se actualiza a la fecha de finalización directa.
- No se introduce ninguna columna nueva para fechas de finalización alternativas.
- Si varios orígenes proporcionan una finalización alternativa, se utiliza la primera fecha de finalización activa.
- Si se revoca un origen (con la opción retroactiva incompleta activada), la fecha se actualiza al siguiente origen activo más antiguo o se borra si no quedan orígenes activos.

**Impacto**: Garantiza un seguimiento histórico preciso y una generación de informes coherente, incluso cuando las relaciones alternativas cambian con el tiempo.

## Finalizaciones alternativas revocadas

Las finalizaciones alternativas revocadas se producen cuando se eliminan todas las relaciones de origen para un curso de destino o una ruta de aprendizaje, siempre que se active la finalización retroactiva.

### Condiciones del activador

- La finalización retroactiva debe estar activada en el nivel de cuenta.
- La revocación solo se produce cuando se quitan **todas** las relaciones de origen activas.
- Si queda al menos un origen, la finalización alternativa persiste y la columna de origen de finalización se actualiza en consecuencia.

### Impacto en las transcripciones de alumnos

- **Estado**: si se revocan todas las finalizaciones alternativas y no hay finalización directa, el estado se actualiza (por ejemplo, de **Completado** a **No iniciado** o **En curso**).
- **Fecha de finalización**: Se borra si no quedan orígenes activos y no hay finalización directa.
- **Origen de finalización**: se ha actualizado para quitar los orígenes revocados; se borra si se revocan todos los orígenes.

Si el alumno tiene una finalización directa, revocar orígenes alternativos no afecta al estado de finalización ni a la fecha de finalización.

>[!NOTE]
>
>Si varios orígenes proporcionan una finalización alternativa y solo algunos están revocados, la transcripción refleja los orígenes activos restantes y su fecha de finalización más temprana. Si se revocan todos los orígenes y no hay finalización directa, el alumno pierde el estado de finalización del destino.

## Información mejorada para comentarios del revisor de la lista de comprobación

Los comentarios de los revisores de los módulos de lista de comprobación ahora se incluyen en el informe de transcripciones de alumnos en una columna con el nombre cambiado denominada **Comentarios de los revisores.**

| Área | Nombre de columna anterior | Nuevo nombre de columna | Notas |
|------|-----------------|-----------------|-------|
| Transcripciones de alumnos (administrador) | Enviar comentario | Comentarios del revisor | Se aplica a todos los orígenes de Admin LT: IU, API de trabajos, conectores. |

Este cambio se aplica de manera uniforme a todos los orígenes de LT de administrador (exportaciones de interfaz de usuario, informes de API de trabajos y conectores, cuando corresponda). Los comentarios del revisor aparecerán como una columna dedicada al final (para los conectores que no expusieron previamente el comentario de envío), lo que garantiza que las integraciones posteriores puedan distinguir los comentarios del revisor de otros comentarios.

**Impacto:** Permite a los alumnos y administradores ver comentarios consolidados, lo que mejora la transparencia y respalda la evaluación del rendimiento.

>[!NOTE]
>
>Para las transcripciones de alumnos de los alumnos, la columna etiquetada anteriormente como **Comentario de envío** ahora se llama **Comentarios del revisor** y se rellena con el comentario del revisor de la lista de comprobación cuando está habilitada.

## Cálculo del tiempo de aprendizaje mejorado

El informe Transcripciones de alumnos ahora utiliza lógica perfeccionada para distinguir entre el tiempo de aprendizaje activo y el tiempo de inactividad según la actividad del usuario y el enfoque de la pestaña del navegador.

**Impacto**: Proporciona una medición más precisa de la participación del alumno, que respalda los informes de cumplimiento y los análisis.
