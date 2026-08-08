---
description: 'Obtenga información sobre cómo Content Composer gestiona las actualizaciones de cursos en Adobe Learning Manager: cómo la republicación crea una nueva versión de módulo y cómo los autores de ALM actualizan los cursos existentes para utilizar la versión más reciente.'
jcr-language: en_us
title: Control de versiones de módulos en Adobe Learning Manager
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Control de versiones de módulos en Adobe Learning Manager

El material de origen cambia con el tiempo: se revisa una política, un PNT obtiene una nueva versión y se actualiza una presentación. Compositor de contenido y ALM gestionan una actualización como un cambio de versión, no una edición in situ, por lo que los cursos publicados anteriormente siguen funcionando mientras se actualiza el módulo subyacente.

Al volver a publicar, Adobe Learning Manager carga el módulo existente como una nueva versión en la biblioteca de contenido, lo que incrementa el número de versión del módulo en uno.

1. En Content Composer, actualice los archivos de origen y vuelva a generar las lecciones afectadas (consulte Actualizar un curso cuando cambie el material de origen) y, a continuación, vuelva a publicar.

2. La publicación de la actualización no sobrescribe el módulo existente, sino que añade una nueva versión junto a él en la biblioteca de contenido de ALM.

3. Un autor de ALM debe actualizar explícitamente cada curso de ALM que utilice el módulo para señalar a la nueva versión; los cursos existentes siguen haciendo referencia a la versión con la que se crearon hasta que un autor de ALM realiza ese cambio.

4. Los alumnos que ya han completado el curso con la versión anterior mantienen su registro de finalización existente. La nueva versión se aplica a los alumnos inscritos después de actualizar el curso de ALM.

Revise las lecciones regeneradas en Compositor de contenido antes de volver a publicar. La regeneración puede ajustar el texto editado anteriormente, las imágenes o las preguntas de las pruebas en las lecciones afectadas.
