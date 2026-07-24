---
description: En este documento se resumen los cambios de informes de agosto de 2026 en Adobe Learning Manager. Abarca columnas nuevas y actualizadas en los informes de transcripciones de alumnos, formación, inscripción, lista de espera, asistencia, auditoría de contenido y usuarios. También explica el comportamiento adaptable del curso, la puntuación del libro de calificaciones, los registros de aprendizaje externos, los informes de crédito de IA general, el seguimiento de la certificación raíz, la estandarización de la marca de tiempo y las actualizaciones de los autores de API.
jcr-language: en_us
title: Notificación de cambios en la versión de agosto de 2026 de Adobe Learning Manager
source-git-commit: 2d60f665d2e00c95edfc96360ee65fdae013c0cd
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 2%

---


# Notificación de cambios en la versión de agosto de 2026 de Adobe Learning Manager

La versión de agosto de 2026 de Adobe Learning Manager presenta mejoras en la creación de informes en cursos adaptables, libro de calificaciones, aprendizaje externo, uso de créditos de IA general y mucho más. Este artículo resume las nuevas columnas, informes y cambios de comportamiento disponibles para los administradores en esta versión.

## Cambios habidos

Las actualizaciones de informes abarcan ocho áreas de funciones: comportamiento adaptativo del curso, lista de espera adaptable, puntuación del libro de calificaciones, aprendizaje externo, exportaciones incrementales de usuarios, uso de créditos de IA general, seguimiento de la certificación raíz y alineación de la marca de tiempo webhook. Los cambios afectan de manera más significativa a los siguientes informes:

- Transcripciones de alumnos (LT)
- Informe de cursos de formación
- Informe de inscripción
- Informe de lista de espera
- Informe de auditoría de contenido

La mayoría de las actualizaciones introducen nuevas columnas. Algunos introdujeron nuevos tipos de informes. Algunos han cambiado la forma en que se modela o se formatea la información existente.

## Informe de cambios del curso adaptable

### Informe de cursos de formación

Las tres nuevas columnas del informe de formación admiten el comportamiento de curso adaptable.

| **Columna** | **Descripción** | **Valores compatibles** |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Objeto de aprendizaje adaptativo | Identifica si un curso es adaptable | verdadero (adaptable), falso (no adaptable) |
| Grupos de usuarios de visibilidad | Muestra los grupos de usuarios que pueden ver cada módulo | Uno o varios nombres de grupos de usuarios (por ejemplo, Todos los alumnos, UG-Australia) |
| Obligatorio | Indica si un módulo es obligatorio para un grupo de usuarios | Nombres de grupos de usuarios para los que el módulo es obligatorio; blank = opcional |

Puede combinar **Grupos de usuarios de visibilidad** y **Obligatorio** para interpretar las reglas de finalización adaptables directamente en el informe. Por ejemplo, un módulo puede estar visible para **todos los alumnos**, pero solo es obligatorio para el **grupo de administradores**.

### Transcripciones de alumnos

Una nueva columna **Finalizaciones anteriores** captura los datos de finalización históricos cuando la lógica adaptable desencadena la nueva finalización.

| **Subcampo** | **Descripción** |
|-----------------------|-----------------------------------------|
| completedRefreshDate | Marca de tiempo cuando se restableció la finalización |
| completedDate | Marca de tiempo de finalización anterior |
| progressAtRefresh | Progreso del alumno antes del restablecimiento |
| gradeAtRefresh | Puntuación del alumno en el momento del restablecimiento |

La transcripción del alumno ahora admite varios ciclos de finalización. Cuando se produce un evento de nueva finalización, por ejemplo, debido a actualizaciones del curso o nuevos módulos obligatorios, la finalización anterior se mueve a la columna **Finalizaciones anteriores**. La finalización actual permanece en los campos de transcripción estándar.

### Informe de inscripción

Una nueva columna **En lista de espera** indica si un alumno está en lista de espera en algún módulo de un curso.

| **Valor** | **Significado** |
|-----------|---------------------------------------------------------|
| verdadero | El alumno se encuentra en lista de espera en uno o varios módulos. |
| falso | El alumno ha confirmado la inscripción en todos los módulos visibles |

### Informe de lista de espera

Dos nuevas columnas y un módulo de soporte mejorado de detalles de estado permiten el seguimiento de la lista de espera en el nivel de módulo.

| **Columna** | **Descripción** |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Módulo** | El nombre del módulo (sesión de clase o de clase virtual) en el que está en lista de espera el alumno. Aparece después de la columna Estado de instancia. |
| **Id. de módulo** | Identificador del módulo en el que está en lista de espera el alumno. Aparece después de la columna Módulo. |
| **Incrustado** | El nombre de la ruta de aprendizaje y el ID de cualquier ruta de aprendizaje que contenga este curso. Está en blanco si el curso no forma parte de una ruta de aprendizaje. |

El informe de la lista de espera ha cambiado de un modelo de nivel de curso a un modelo de nivel de sesión de módulo. Ahora se puede inscribir a un alumno en algunos módulos y ponerlo en lista de espera en otros. El informe también admite el seguimiento de listas de espera en las rutas de aprendizaje de Flex, donde los límites de puestos se aplican en el nivel de módulo.

### Informe de inscripción de LP

El informe de inscripción de ruta de aprendizaje también recibe una nueva columna **Comentarios**. Cuando un alumno se encuentra en una lista de espera en cualquier clase o sesión de clase virtual de los cursos que componen la ruta de aprendizaje, la columna Comentarios muestra **Lista de espera**. Cuando se confirman todas las sesiones, la columna está en blanco.

### Informe de asistencia

La columna **Estado del alumno** ahora distingue entre alumnos confirmados y en lista de espera.

| **Valor** | **Significado** |
|------------|----------------------------------------|
| Confirmado | El alumno tiene una licencia asignada |
| En la lista de espera | El alumno está pendiente de asignación de puestos |

## Informes de cambios del libro de calificaciones

### Transcripciones de alumnos

Una nueva columna **Weight** representa la contribución de cada módulo puntuable a la puntuación general del curso.

| **Valor** | **Descripción** |
|----------------------------------------------|------------------------------------------------------|
| Porcentaje numérico (por ejemplo, 20, 30, 50) | Contribución del módulo a la puntuación del curso |
| En blanco | El módulo no es puntuable (por ejemplo, PDF o vídeos) |

### Informe de auditoría de contenido

Dos nuevos eventos capturan los cambios de configuración del libro de calificaciones.

| **Evento** | **Se activa cuando** | **Datos capturados** |
|-----------------------|-----------------------------------------------------------------|----------------------------------------------------------|
| Libro de calificaciones actualizado | El libro de calificaciones está habilitado, deshabilitado o modificado en el nivel del curso | Cambio en el estado del libro de calificaciones; gradación de actualizaciones de configuración |
| Peso del módulo actualizado | El peso asignado a un módulo se modifica | identificador del módulo; valor de ponderación actualizado |

La transcripción del alumno refleja la ponderación más reciente. El informe de auditoría de contenido realiza un seguimiento de los cambios históricos. Juntos, te ofrecen una visión completa de la lógica de puntuación actual y de cómo ha evolucionado.

## Cambios en informes de aprendizaje externo

### Transcripciones de alumnos

Se han añadido tres nuevas columnas para admitir registros de aprendizaje externos.

| **Columna** | **Descripción** |
|------------------------|-----------------------------------------------------------------------------------------------------|
| Nombre del aprendizaje externo | El nombre de la actividad de aprendizaje externa enviada por el alumno. |
| Campos personalizados | Una columna por campo personalizado configurado para aprendizaje externo (texto, numérico, casilla de verificación o menú desplegable) |
| Comentario de finalización | Comentarios del responsable introducidos durante la aprobación o rechazo |

**Nota:** En la transcripción del alumno (vista de autoservicio del alumno), la ubicación de las columnas difiere de la transcripción del alumno administrador:

- **Nombre de aprendizaje externo** se agrega inmediatamente después de la columna **Módulo** existente.

- **Comentario de finalización** se agrega inmediatamente después de la columna **Comentarios del revisor** existente.

- Las columnas de campos personalizados (uno por cada campo personalizado configurado) se agregan al final de la transcripción.

En la transcripción del alumno administrador, todas las columnas nuevas, incluidos el nombre del aprendizaje externo y el comentario de finalización, se agregan al final, seguidos de las columnas de campos personalizados.

### Columna Tipo en la transcripción del alumno

Las entradas de aprendizaje externas aparecen ahora junto a los objetos de aprendizaje existentes (cursos, rutas de aprendizaje, certificaciones) en la licencia de administración. La columna **Type** incluye una nueva clasificación de aprendizaje externa para facilitar el filtrado.

Los datos de aprendizaje externos fluyen tanto en la transcripción del alumno como en el LT del administrador. Los campos principales, como la fecha de finalización, el estado y la puntuación, se asignan a columnas existentes. Los campos personalizados se agregan como columnas adicionales.

## Cambios incrementales en el informe de usuario

Un nuevo modelo de exportación incremental permite exportar únicamente los usuarios cuyos datos hayan cambiado en un intervalo de tiempo especificado, en lugar de generar exportaciones de datos completas cada vez.

| **Modo de exportación** | **Comportamiento** |
|--------------------|-----------------------------------------------------------------|
| Exportación completa | Devuelve todos los usuarios de la cuenta |
| Exportación incremental | Devuelve sólo los usuarios con cambios dentro del intervalo de fechas especificado |

Para utilizar la exportación incremental, filtre por **desde la fecha** y **hasta la fecha** para definir la ventana de cambio. Los informes de usuario ahora se generan mediante una canalización de plataforma de datos y el resultado se devuelve en fragmentos para admitir cuentas de gran tamaño.

## Generación de informes de crédito de IA

Un nuevo tablero de créditos y dos informes proporcionan a los administradores visibilidad sobre el consumo de créditos de la IA general.

### Crear panel

El tablero muestra las siguientes métricas en el nivel de cuenta.

| **Métrica** | **Descripción** |
|-------------------|---------------------------------------------------|
| Créditos adquiridos | Total de créditos aprovisionados para la cuenta |
| Créditos usados | Créditos consumidos en funciones basadas en IA |
| Créditos restantes | Créditos disponibles después del consumo |
| Uso por función | Consumo de crédito dividido por función de IA individual |

### Nuevos informes

| **Informe** | **Descripción** |
|----------------------|---------------------------------------------------------------------------------------------|
| Informe de uso mensual | Resume el consumo de crédito por mes, función y créditos consumidos |
| Informe de seguimiento de auditoría | Proporciona detalles a nivel de usuario: identificador de usuario, nombre de función, créditos consumidos y marca de tiempo |

## Otros cambios de comportamiento

### Certificación raíz: ID de formación raíz

Se agrega una nueva columna **ID raíz de formación** al final de la **transcripción del alumno administrador** y de la **transcripción del alumno** (vista de autoservicio del alumno). Captura el identificador único que vincula todas las repeticiones de una certificación a una única entidad raíz. Esto permite asociar todas las instancias recurrentes de una certificación con un único ID raíz para el seguimiento y filtrado.

### Estandarización de marca de tiempo de webhook y transcripciones de alumnos

Las marcas de tiempo de Webhook ahora se alinean con el formato de transcripciones de alumnos. Cada campo de fecha y hora dentro del **objeto de datos** de una carga útil webhook ahora tiene su valor de segundos establecido en 0, lo que proporciona una granularidad de nivel de minuto coherente con los informes de transcripciones de alumnos. Esto elimina la necesidad de normalizar los formatos de marca de tiempo al comparar los datos de webhook con los datos de transcripciones de alumnos.

### Información del autor en la respuesta de la API para cursos compartidos

Cuando se comparte un curso de una cuenta de Adobe Learning Manager a otra mediante el uso compartido de catálogos, la respuesta de objeto de aprendizaje (LO) de la API ahora devuelve solo los detalles del autor original de la cuenta de origen. Anteriormente, el administrador de la cuenta de aceptación aparecía como el autor del curso en la respuesta de la API para su cuenta.

Este cambio afecta solo a las cuentas de igual a igual (de recepción). Cuando consulta el extremo de detalle de objeto de aprendizaje de un curso compartido en una cuenta receptora, el campo authorNames refleja ahora el autor original de la cuenta de origen, no el administrador de la cuenta receptora.

No hay ningún cambio en el aspecto de los detalles del autor al consultar el objeto de aprendizaje en la cuenta de origen.

**Nota:** Si su integración se basa en el campo authorNames de la respuesta de la API de objeto de aprendizaje para cursos compartidos, compruebe que los datos actualizados del autor no interrumpen ninguna lógica descendente que suponga que el nombre del administrador de la cuenta receptora aparecería en este campo.
