---
description: Descubre cómo Compositor de contenido y Adobe Learning Manager dividen las responsabilidades de creación y entrega, cómo un curso terminado pasa de Compositor de contenido a la biblioteca de contenido de ALM y cómo funcionan el seguimiento y la creación de informes de los alumnos tras la publicación.
jcr-language: en_us
title: Cómo trabajan juntos Compositor de contenido y Adobe Learning Manager
source-git-commit: 5a0f12b1ed0e5ae1bde7afbd539d70078d99f05d
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---


# Cómo trabajan juntos Adobe Learning Manager Content Composer y Adobe Learning Manager

El compositor de contenido gestiona la creación. Adobe Learning Manager se encarga de la entrega, la inscripción, el seguimiento y la creación de informes. Los dos productos se conectan a través de un paso de publicación. Una vez que publique desde Content Composer, el curso se convierte en un módulo de la biblioteca de contenido de ALM, donde se puede agrupar en un curso y asignarlo a los alumnos.

## Qué controla el Compositor de contenido

- Estructura de la lección y del tema

- Contenido del curso: texto, imágenes, vídeos, componentes y comprobaciones de conocimientos

- Cuestionarios de fin de lección, incluidos tipos de preguntas y opciones de respuesta

- Tema visual

- Criterios de finalización y criterios de éxito

- Versión de SCORM utilizada para la creación de informes

## Qué controla Adobe Learning Manager

- Inscripción y acceso de alumnos

- Metadatos del módulo: duración, etiquetas, ID exclusivos, caducidad

- Montaje del curso: combinación de módulos de compositor de contenido con otro contenido de aprendizaje

- Seguimiento, informes y transcripciones de alumnos

- Versiones del curso

- Notificaciones y recordatorios

## Desde la creación del curso hasta la finalización del alumno

1. **Cree el curso en el compositor de contenido**: cree su curso en Compositor de contenido, incluidas lecciones, temas, temas, cuestionarios y configuraciones de finalización. Antes de publicar, configure los ajustes del curso (criterios de finalización, criterios de éxito y puntuación de la prueba).
Para obtener más información, consulte [Configurar opciones del curso](#settings).

2. **Publish a Adobe Learning Manager:** una vez completada la creación, conecta Content Composer a tu cuenta de ALM mediante la configuración de **Exportar** y publica el curso. Content Composer envía el curso a la biblioteca de contenido de ALM como un módulo compatible con SCORM.
   ![Curso publicado al que se ha aplicado un encabezado, logotipo y tema de fuente personalizados](../assets/49_published_course_custom_branding_header_updated.png)

3. **Configurar el módulo en ALM:** Una vez publicado, el curso aparece como un módulo en la biblioteca de contenido de ALM. Un autor de ALM configura los metadatos del módulo, incluida la duración, las etiquetas, los ID exclusivos y la configuración de caducidad, y añade el módulo a un curso de ALM junto con otro contenido de aprendizaje.
   ![Campos de metadatos de módulo y criterios de finalización](../assets/50_alm_add_content_composer_module_metadata_updated.png)

>[!NOTE]
>
>Si establece criterios de finalización y éxito en Adobe Learning Manager (ALM), dichos ajustes tienen prioridad sobre los definidos en Composición de contenido.

4.**Curso de ALM de Publish:** Un autor de ALM ensambla el módulo en un curso de ALM, agrega imágenes y configuraciones del curso, y lo publica. Solo después de este paso se pueden inscribir los alumnos.

Para obtener más información, consulte [Adobe Learning Manager](https://experienceleague.adobe.com/es/docs/learning-manager/using/get-started/getting-started-author).
![&#x200B; La biblioteca de contenido en Adobe Learning Manager, que muestra los módulos publicados y de procesamiento](../assets/51_alm_content_library_list_view_updated.png)

Para obtener más información, consulte [Creación de cursos como autor en ALM](https://experienceleague.adobe.com/es/docs/learning-manager/using/authors/courses).

5.**Los alumnos completan el curso:** alumnos acceden al curso a través de Adobe Learning Manager, inician el módulo Compositor de contenido, completan lecciones y cuestionarios, y reciben puntuaciones según los criterios de finalización y éxito configurados en el paso 1.

Para obtener más información, consulte [Acceder a un curso como alumno](https://experienceleague.adobe.com/es/docs/learning-manager/using/get-started/getting-started-learner).

6.ALM registra el progreso del alumno: el estado de finalización, las puntuaciones de las pruebas y los datos del alumno se registran en ALM y están disponibles mediante transcripciones de alumnos e informes administrativos.

7.**Actualice el curso con control de versiones**: al actualizar contenido en Content Composer y volver a publicar, ALM crea una nueva versión del módulo. Los autores de ALM pueden actualizar los cursos existentes para utilizar la versión más reciente.
