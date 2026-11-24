---
description: Consulte lo que los alumnos pueden hacer con el servidor de Adobe Learning Manager Model Context Protocol y las herramientas que admiten cada función.
jcr-language: en_us
title: Herramientas del alumno para el servidor de Protocolo de contexto de modelo
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---

# Herramientas del alumno para el servidor de Protocolo de contexto de modelo

## Información general

Cada capacidad se ejecuta como alumno que ha iniciado sesión después de que el alumno se conecte. Una solicitud devuelve solo lo que el alumno puede acceder en Adobe Learning Manager. Obtén más información sobre [cómo conectar tu cliente de inteligencia artificial](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md).

## Capacidades del alumno

| **Capacidad** | **Qué pueden hacer los alumnos** | **Ejemplo de solicitud** |
|----|----|----|
| Buscar contenido de aprendizaje | Buscar cursos, certificaciones y rutas de aprendizaje | ¿Qué cursos de liderazgo hay disponibles? |
| Ver inscripciones | Comprobar las inscripciones y el aprendizaje debido | ¿Cuáles de mis cursos están a punto de caducar? |
| Haz preguntas de aprendizaje | Obtén respuestas del contenido de aprendizaje | ¿Qué significa la gestión de riesgos de la cadena de suministro en FedRAMP? |
| Generación de rutas de aprendizaje | Crear rutas de aprendizaje personalizadas | Ayúdame a encontrar cursos para mejorar las habilidades en la administración de proyectos. |
| Guardado de rutas de aprendizaje | Guardar rutas de aprendizaje generadas | Guarda esta ruta de aprendizaje. |

## Herramientas de MCP compatibles

El servidor Adobe Learning Manager MCP expone las siguientes herramientas de aprendizaje.

| **Nombre de herramienta** | **Descripción** |
|----|----|
| search_learning_items | Busque en el catálogo cursos, rutas de aprendizaje, certificaciones, ayudas de trabajo, insignias, aptitudes, catálogos y etiquetas. Filtra por estado del alumno, aptitud, etiqueta, catálogo, formato de entrega, precio e idioma. Para preguntas de materia, use answer_learning_content_question. Ejemplo: &quot;Cursos de Python para principiantes&quot;. |
| list_my_learning_enrollments | Enumere los cursos inscritos, en curso y completados del alumno, las rutas de aprendizaje, las certificaciones y las ayudas de trabajo, con el estado, el progreso y la fecha límite. Filtrar por tipo de objeto de aprendizaje o estado de finalización. Los resultados muestran las inscripciones más recientes en primer lugar. Ejemplo: &quot;¿Qué hay que hacer pronto?&quot; |
| get_learning_object | Obtén todos los detalles de un curso, una ruta de aprendizaje, una certificación o una ayuda de trabajo por ID, opcionalmente con instancias, habilidades y objetos de subaprendizaje. Obtenga el ID de search_learning_items o list_my_learning_enrollments. |
| get_my_learning_profile | Obtenga el perfil del alumno, incluidos los detalles de la cuenta y del responsable. Para las inscripciones y el progreso, utilice list_my_learning_enrollments. |
| answer_learning_content_question | Responda preguntas sobre el contenido de aprendizaje, basado en el material de aprendizaje y citado en los objetos de aprendizaje de origen. Resume un objeto de aprendizaje o compara dos en paralelo para la cobertura, la profundidad, los requisitos previos y la audiencia. Para buscar o enumerar contenido, utilice search_learning_items o list_my_learning_enrollments. Ejemplo: &quot;Explique TCP frente a UDP como se describe en mi curso de redes&quot;. |
| personalized_learning_path | Recomienda cursos que coincidan con los objetivos, temas y necesidades de un alumno. Guarde una ruta aprobada en la cuenta del alumno. Enumere las rutas guardadas u obtenga los detalles y los cursos de una ruta por ID. |

>[!IMPORTANT]
>
>Los nombres de las herramientas se muestran como referencia y pueden variar dependiendo de la implementación del cliente.
