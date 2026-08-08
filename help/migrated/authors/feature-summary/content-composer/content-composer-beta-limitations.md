---
description: Revise las limitaciones actuales de la versión beta de Content Composer, incluidas las limitaciones en la edición de esquemas, los tipos de evaluación, la personalización de temas y la colaboración, con las soluciones alternativas disponibles y el estado de la hoja de ruta para cada una.
jcr-language: en_us
title: Limitaciones de la versión beta de Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---


# Limitaciones de la versión beta de Adobe Learning Manager Content Composer

Una lista completa de las restricciones beta actuales de Content Composer, con descripciones y soluciones alternativas cuando estén disponibles.

## Limitaciones actuales

En la siguiente tabla se muestran todas las restricciones conocidas de la versión beta actual.

| **Limitación** | **Descripción** | **Solución alternativa** |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **La edición de esquema es solo conversacional** | No puede seleccionar una lección o un tema del lienzo para cambiarle el nombre, reordenarlo o eliminarlo. Todos los cambios de contorno deben realizarse a través del panel de chat del asistente. | Pregúntale al asistente: &quot;Cambiar el nombre de la Lección 2 a &#39;Higiene de la contraseña&#39;&quot; o &quot;Mover el tema 1.3 a la Lección 2.&quot; |
| **Se ha corregido la jerarquía del esquema** | La estructura del curso se ha fijado como Lecciones > Temas. No puede crear subtemas, niveles de jerarquía adicionales ni estructuras personalizadas. | Utilice los componentes disponibles para agregar profundidad dentro de un tema. |
| **El esquema no se puede modificar directamente después de generar el curso** | Una vez que se genera un curso, los nombres de los temas y de las lecciones siguen formando parte de la estructura del esquema. Debe volver a las conversaciones de nivel de esquema para cambiarlas. No puede cambiarles el nombre seleccionando un encabezado en el Editor de cursos. | Pregunte al ayudante en el Editor del curso: &quot;Cambie el nombre de la Lección 3 a &#39;Respuesta ante incidentes&#39;.&quot; |
| **Tipos de evaluación: Sólo MCQ y True/False** | La versión beta actual solo admite preguntas de opción múltiple (**MCQ**) y preguntas de tipo Verdadero/Falso. No hay disponibles otros tipos de evaluación. | - |
| **Los bancos de preguntas no están disponibles** | No puede importar ni administrar un banco de preguntas prediseñadas. | Genera preguntas adicionales de forma conversacional: Añade dos preguntas más al cuestionario para la lección 1&quot;. |
| **Las comprobaciones de conocimientos no se califican** | Las comprobaciones de conocimientos incorporadas en las lecciones no se califican. Solo se califican y registran las evaluaciones de las pruebas al final de la lección. | Utilice cuestionarios (no comprobaciones de conocimientos) para cualquier evaluación que deba generar un registro de finalización o puntuación. |
| **Las acciones de conversación se limitan a las capacidades admitidas** | El asistente puede comentar e intercambiar ideas libremente, pero las modificaciones del curso real se limitan a las funciones que admite el producto. Es posible que las solicitudes para generar estructuras de contenido o formatos no compatibles no se realicen correctamente. | Si una solicitud no funciona, pida al ayudante que le explique lo que puede hacer. |
| **Generación restringida a documentos** | Cuando está habilitada la opción **Restringir la salida al contenido en los archivos**, Content Composer genera contenido solo a partir de los documentos de origen cargados. No introduce información más allá de esas fuentes. | Desactive el botón de alternancia para permitir que la IA se complemente con conocimientos generales. |
| **Las funciones de colaboración están evolucionando** | Compartir para revisión y comentar, y Compartir para alumnos están en desarrollo activo. Los detalles de la implementación pueden cambiar antes de la disponibilidad general. | Use **Copiar vínculo** para compartir un vínculo de vista previa para una revisión informal. Para la coedición, coordine los giros con los colaboradores. No se admite la coedición simultánea. |
| **El asistente interno del producto no es un sistema de ayuda del producto** | El asistente de conversación está diseñado para tareas de edición de cursos, como generar y modificar contenido. Las respuestas a las preguntas sobre el uso del producto pueden no ser fiables porque este comportamiento aún no se ha diseñado de forma explícita. | Para preguntas de procedimiento, utilice la documentación de ayuda existente en lugar de preguntar al asistente del producto. |
