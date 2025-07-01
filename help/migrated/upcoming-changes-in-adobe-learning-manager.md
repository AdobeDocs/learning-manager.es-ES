---
title: Próximos cambios en Adobe Learning Manager
description: Descubre las nuevas funciones, mejoras y actualizaciones importantes que estarán disponibles próximamente en Adobe Learning Manager. Mantente informado de los cambios para poder planificar con antelación y aprovechar al máximo las mejoras más recientes.
source-git-commit: 97c52c188612b7ad7233a13bd90bcb174fdc60bc
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 2%

---


# Próximos cambios en Adobe Learning Manager

Nos complace compartir varias actualizaciones importantes que llegarán a Adobe Learning Manager en las próximas versiones. Estas mejoras tienen como objetivo agilizar los flujos de trabajo de los administradores, mejorar la precisión de los informes de datos y reforzar los controles basados en funciones.

Estos cambios están diseñados para reducir el esfuerzo manual, fomentar la automatización y mejorar la gobernanza en las operaciones de formación.

## Capturar finalizaciones con marca de instructor en transcripciones de alumnos (M44)

### Público

Administradores y propietarios de automatización

### Información general

En Adobe Learning Manager, al utilizar transcripciones de alumnos (LT) incrementales para los flujos de trabajo de automatización, no se capturan las finalizaciones marcadas por el instructor realizadas después de la fecha de la sesión. La marca de tiempo de finalización refleja la hora de finalización de la sesión original (no la hora en la que el instructor marcó la finalización). Como estas actualizaciones quedan fuera de la ventana de cambio de un día utilizada para la generación incremental de aprendizaje, como resultado, los datos de asistencia y finalización de los alumnos se excluyen de los informes, lo que provoca informes descendentes inexactos o incompletos y posibles brechas de cumplimiento.

### Cambios habidos

Los informes de transcripciones de alumnos (LT) incluyen finalizaciones marcadas por los instructores después de la fecha de la sesión. Esto garantiza que cualquier marca de asistencia retrasada se refleje correctamente en la exportación de transcripciones.

Los estados de asistencia como &quot;Asistencia con aprobado/suspenso&quot; aparecerán automáticamente en las exportaciones incrementales de archivos LT.

### Novedades

* Nueva columna: Marcar fecha de finalización (zona horaria UTC).
* El origen de finalización está disponible en el nivel de módulo.
* Compatible con informes LT basados en conectores o generados por API de trabajos.

![](assets/capture-instructor.png)

**Acción obligatoria**

* Si la automatización depende de las posiciones de las columnas, asegúrese de que la nueva columna tenga cuentas lógicas.
* Si utiliza nombres de columna, no es necesario realizar cambios.
* No se incluyen las finalizaciones retroadaptadas (importaciones manuales).

## Vínculos de descarga del informe Ayudas de trabajo (M44)

### Público

Administrador, administrador personalizado y propietarios de automatización

### Información general

El informe Ayudas de trabajo incluye un vínculo de descarga directa para cada ayuda de trabajo, lo que permite un acceso rápido desde el propio informe.

### Novedades

Se ha agregado una nueva columna, **[!UICONTROL Vínculo de ayuda de trabajo]**, a la tercera posición del informe. Se vincula directamente a la ayuda de trabajo si es un archivo o muestra la URL externa proporcionada por el autor.

Los usuarios con acceso (administradores/autores y funciones personalizadas) pueden descargar la ayuda de trabajo mediante este vínculo.

![](assets/download-links-for-job-aid.png)

### Acción necesaria

* Revisar flujos de trabajo automatizados mediante informes de ayudas de trabajo (mediante la API de trabajos).
* Si el script se basa en la posición de la columna, actualice los scripts según corresponda.
* No es necesario realizar ninguna acción si se utilizan nombres de columna.

## Columnas de ID de usuario interno y correo electrónico del responsable añadidas al informe de usuario (M44)

### Público

Administradores (y administradores personalizados) usando el **[!UICONTROL Informe de usuario]** (**[!UICONTROL Administrador]** > **[!UICONTROL Usuarios]** > **[!UICONTROL Interna]** > **[!UICONTROL Exportar datos de usuario]**) descargado desde la interfaz de usuario del administrador.

### Información general

Para ayudar en los flujos de trabajo de integración e identificación de usuarios, se han agregado al informe de usuario dos columnas, **[!UICONTROL Id. de usuario interno]** y **[!UICONTROL Correo electrónico del administrador]**, que se exportan a través de la interfaz de usuario.

### Novedades

El informe de usuarios incluye el ID de usuario interno de un usuario y la dirección de correo electrónico de su responsable, para asignarlos de forma exclusiva entre diferentes herramientas o puntos finales de API.

### Acción necesaria

* Si se utiliza este informe en flujos automatizados, esta columna recién añadida se debe tener en cuenta en la automatización.
* No es necesario realizar cambios si los flujos de trabajo no se ven afectados.

## Permisos de anuncios con ámbito para administradores personalizados (M44)

### Público

Administradores personalizados

### Información general

Los administradores personalizados solo pueden crear anuncios para los grupos de usuarios o catálogos dentro de su ámbito definido.

### Novedades

* Las reglas de ámbito permiten a los administradores personalizados crear anuncios solo para grupos de usuarios o catálogos específicos.
* Al definir una función personalizada, los administradores pueden asignar permisos de anuncio con ámbito en grupos de usuarios o catálogos.
* Los administradores personalizados se limitan a crear anuncios dentro de su ámbito determinado.
* El informe de anuncio de notificación para administradores personalizados mostrará a los alumnos solo dentro de su ámbito asignado.

### Acción necesaria

* El formato del informe se mantendrá sin cambios. Si los administradores personalizados lo descargan desde la interfaz de usuario, el contenido del informe estará sujeto a su ámbito.
* No es necesario realizar modificaciones si este informe no se utiliza en ningún flujo de trabajo automatizado o descendente.
