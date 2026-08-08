---
description: Carga los documentos, políticas o plataformas existentes para incorporar la IA al contenido de tu organización. Elija si desea restringir la generación solo a esos archivos o permitir que la IA complemente su conocimiento general.
jcr-language: en_us
title: Administrar archivos de origen
source-git-commit: 229e407621281978f94783c3e9320c237c314fc3
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# Administrar archivos de origen

**Administrar orígenes** te permite controlar qué contenido usa Content Composer para generar tu curso. Añade tus propios documentos a un curso y, a continuación, elige si restringir la IA solo a ese contenido o permitir que complemente tu material con su propio conocimiento. Si no añade ningún documento, Content Composer generará el curso utilizando los conocimientos existentes del modelo de IA.

## Generar un curso con material de origen

1. Seleccione **Administrar orígenes** o **Agregar archivos** en el panel de chat o la barra de herramientas.
   ![](../assets/5_brief_manage_sources_prompt_updated.png)

2. Arrastre un archivo al cuadro de diálogo o seleccione **+ Agregar archivos de origen** para examinar. Puede agregar varios archivos de origen.
   ![](../assets/6_manage_sources_no_files_added_updated.png)

3. Seleccione **Restringir la salida al contenido de los archivos**. Esto permite que el compositor de contenido use solo contenido de origen para generar el curso. Si esta opción está desactivada, Content Composer también utiliza la Web para crear un curso.
   ![](../assets/7_manage_sources_file_uploading_restrict_output_updated.png)

Formatos admitidos:

| **Formato** | **Tamaño máximo** |
|-------------------------|--------------|
| PDF | 100 MB |
| Markdown (.md) | 100 MB |
| PowerPoint (.ppt/.pptx) | 100 MB |
| MS Word (.doc/.docx) | 100 MB |
| Archivo de texto (.txt) | 100 MB |

Seleccione **Continuar** para generar el esquema del curso.

### Generar sin material de origen

Siga los pasos que se indican a continuación para generar el esquema del curso cuando no tenga un archivo de origen como documento de referencia.

1. Seleccione **Administrar orígenes**. Se abre el cuadro de diálogo **Administrar orígenes**.

2. Seleccione **No tengo ningún material de origen: genere el curso sin archivos de origen** para permitir que la IA genere contenido a partir de su conocimiento general. Cuando esta opción no está seleccionada y los archivos se cargan, la IA restringe el contenido generado solo a los documentos cargados.![](../assets/8_manage_sources_no_source_material_option_updated.png)

3. Seleccione **Continuar** para generar el esquema del curso.

### Actualizar un curso cuando cambia el material de origen

Los documentos de origen pueden quedar obsoletos después de que se haya generado un curso: se ha revisado una normativa, un PNT obtiene una nueva versión o se ha actualizado una presentación. Utilice este flujo de trabajo para ajustar el curso al material actual.

1. Seleccione **Administrar orígenes** en el panel de chat o en la barra de herramientas para volver a abrir el cuadro de diálogo.

2. Agregue los archivos nuevos o revisados usando **+ Agregar archivos de origen**.

3. Elimina o reemplaza cualquier archivo obsoleto para que la lista de origen refleje únicamente el material actual.

4. Seleccione Continuar para guardar la lista de fuentes actualizada.

5. Vuelva a generar las lecciones afectadas en el compositor de contenido, revise los cambios y vuelva a publicar el curso. Al volver a publicar, se envía la actualización a Adobe Learning Manager como una nueva versión de módulo. Consulte Versiones de módulo en ALM.

### Confirmar la carga del archivo

    ![](../assets/9_manage_sources_file_ingested_confirmation_updated.png)

Una vez que se adjunta un archivo, el icono de archivo en la barra de herramientas muestra un recuento de insignias. El asistente confirma la carga y ofrece un acceso directo **Generar esquema**. Selecciónelo o seleccione **Generar esquema** en la barra de herramientas superior.
