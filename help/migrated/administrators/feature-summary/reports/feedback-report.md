---
description: Obtenga más información sobre cómo acceder, descargar e interpretar el informe de comentarios en Adobe Learning Manager. Comprende las columnas de informes, los tipos de preguntas, las respuestas del responsable y del alumno, y cómo la información de los comentarios respalda la evaluación de la formación y la mejora continua.
jcr-language: en_us
title: Informe de comentarios en Adobe Learning Manager
source-git-commit: e0553621dd67338d2433bb1f82af43cacc2d8b8c
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 8%

---


# Informe de comentarios

## Información general

El informe Comentarios de Adobe Learning Manager recopila los comentarios del nivel 1 (comentarios del alumno) y del nivel 3 (comentarios del responsable) después de que los alumnos completen los objetos de aprendizaje. Este informe presenta una descripción general estructurada de las respuestas subjetivas y objetivas de los alumnos y sus responsables.

El informe realiza un seguimiento de los detalles del alumno, como el nombre, el correo electrónico, el nombre del formulario de comentarios, la versión y el idioma, y captura las respuestas a las preguntas definidas por el administrador. También registra la selección del alumno para cada pregunta (por ejemplo, Totalmente de acuerdo, Aceptar o Rechazar).

## Propósito y ventajas

* Proporciona información útil para mejorar la calidad del curso y la eficacia general del aprendizaje.
* Perfecciona la navegación, el ritmo y los métodos de entrega según los comentarios directos de los usuarios.

## Casos de uso

* **Identifica rápidamente problemas de contenido**: los administradores pueden detectar calificaciones bajas o comentarios negativos repetidos y actualizar los objetos de aprendizaje sin esperar tickets de asistencia ni escalaciones.
* **Mide la eficacia de la formación**: los equipos pueden comparar los comentarios de los alumnos en varios cursos o versiones para determinar qué objetos de aprendizaje funcionan bien y cuáles es posible que deban reelaborarse.
* **Realizar un seguimiento de la participación de los alumnos en los formularios de comentarios**: los administradores pueden ver cuántos alumnos responden u omiten preguntas, lo que les ayuda a perfeccionar los formularios de comentarios para mejorar la calidad de las respuestas y las tasas de finalización.

## Cómo descargar el informe de comentarios

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **[!UICONTROL Informes]** en el menú de navegación izquierdo.
   ![](assets/select-report.png)
   _La página principal del administrador muestra la opción Informes resaltada para descargar informes_

3. Selecciona **[!UICONTROL Informes personalizados]** en Informes y luego selecciona **[!UICONTROL Informes de Excel]**.
4. Seleccione **[!UICONTROL Informe de comentarios]**.
   ![](assets/select-feedback-report.png)
   La sección _Informes personalizados muestra la opción de seleccionar Informe de comentarios para acceder a los datos de comentarios del alumno y el responsable_

5. Seleccione **[!UICONTROL Todos los cursos de formación]** o **[!UICONTROL Cursos de formación seleccionados]**, y el intervalo de fechas. Si selecciona la segunda opción, puede añadir hasta un máximo de 10 cursos o rutas de aprendizaje y generar su informe de comentarios. Además, puede generar el informe durante un máximo de un año.
   ![](assets/feedback-report.png)
   _Configure el informe de comentarios seleccionando el ámbito de formación, estableciendo el intervalo de fechas y eligiendo la opción de traducción antes de la descarga_

6. Seleccione el idioma al que traducir los comentarios de L1. Las preguntas objetivas y sus respuestas se traducen al idioma seleccionado cuando se define explícitamente esa versión lingüística. En el informe sólo aparecen las preguntas subjetivas que se definen explícitamente en el idioma seleccionado.  Las respuestas a las preguntas subjetivas se formularían en el idioma de respuesta original.
7. Seleccione **[!UICONTROL Descargar]** para descargar el informe.

## ¿Qué contiene el informe Comentarios?

A continuación se indican las columnas predeterminadas del informe de nivel de cuenta:

| Columna | Descripción |
|----|----|
| Tipo de comentario | Indica si los comentarios proceden del alumno (L1) o del responsable (L3) |
| Nombre de usuario | El nombre del alumno que ha completado la formación. |
| Correo electrónico de usuario | La dirección de correo electrónico del alumno. |
| ID de la formación | Un identificador único generado por el sistema y asignado a cada objeto de aprendizaje (curso, certificación o ruta de aprendizaje). |
| Nombre de la formación | Nombre del elemento de aprendizaje para el que se envían comentarios |
| Instancia del curso de formación | Nombre de instancia de la formación (para cursos de instancias múltiples) |
| Tipo de formación | Tipo de formación (curso, certificación, itinerario de aprendizaje) |
| Tipo de formulario de comentarios | Tipo o categoría del formulario de comentarios utilizado (por ejemplo, Cursos mixtos, Cursos a ritmo personalizado y Cursos de clase) |
| Nombre del formulario de comentarios | Nombre del formulario de comentarios |
| Versión de los comentarios | Número de versión del formulario de comentarios |
| Responsable actual | El nombre del responsable del alumno. |
| Correo electrónico del responsable actual | Dirección de correo electrónico del responsable del alumno |
| Fecha de finalización | La fecha en la que el alumno ha completado el curso de formación. |
| Fecha del comentario | La fecha en la que el alumno envió los comentarios |
| Comentarios de L1 Idioma original | El idioma en el que el alumno envió originalmente los comentarios de L1 |
| Escala L3 Likert Pregunta 1 | Mide el rendimiento del alumno después del curso de formación mediante una escala de clasificación |
| Respuesta en escala Likert de L3 1 | Respuesta del responsable a esta pregunta de escala Likert |
| Pregunta de texto libre 1 de L3 | Se ha añadido una pregunta de texto libre al formulario de comentarios de L3 para los responsables. Se puede configurar como opcional u obligatoria. |
| Respuesta de texto libre de L3 1 | La respuesta del gerente a esa pregunta de texto libre |

Las siguientes columnas aparecen en el informe de nivel de cuenta en función de los cuatro tipos de preguntas añadidas al formulario de comentarios:

| Columna | Descripción |
|---|---|
| Eficacia del curso | La pregunta predefinida sobre la eficacia del curso que se muestra en el formulario |
| Respuesta de eficacia del curso | Respuesta del alumno a la pregunta sobre la eficacia del curso |
| Pregunta 1 de NPS | Primera pregunta de puntuación de Net Promoter |
| Rango 1 de NPS | Escala de clasificación utilizada (p. ej., de 0 a 10) |
| Respuesta 1 de NPS | Valoración del alumno sobre la pregunta 1 de NPS |
| Likert Pregunta 1 | Primera pregunta a escala Likert |
| Likert Answer 1 | Respuesta a la pregunta 1 de Likert |
| Pregunta de texto 1 | Primera pregunta de texto o de composición abierta en el formulario |
| Respuesta de texto 1 | Respuesta del alumno a la pregunta de texto 1 |


>[!NOTE]
>
>El informe de nivel de cuenta también incluye los campos activos configurados para los alumnos.

En el informe de nivel de objeto de aprendizaje aparecen las siguientes columnas:

| Columna | Descripción |
|---|---|
| Alumno | El nombre del alumno. |
| Correo electrónico | Dirección de correo electrónico del alumno |
| Nombre del formulario de comentarios | Nombre del formulario de comentarios |
| Versión de los comentarios | Número de versión del formulario de comentarios |
| Idioma del alumno | Idioma seleccionado por el alumno |

>[!NOTE]
>
>El informe de nivel de objeto de aprendizaje también incluye las preguntas añadidas al formulario de comentarios. Cada pregunta aparece como un encabezado de columna y las respuestas del alumno a dichas preguntas se muestran en las filas correspondientes a continuación.
