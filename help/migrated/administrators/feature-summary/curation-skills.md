---
jcr-language: en_us
title: Asignar aptitud con dominios de aptitudes
description: Para que el motor de revisión habilitado para inteligencia artificial revise automáticamente una publicación de un usuario en relación con un determinado dominio, la empresa del usuario debe tener asignadas aptitudes personalizadas con los dominios de aptitudes admitidos que existen en el sistema de gestión de aprendizaje Learning Manager.
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 95%

---



# Asignar aptitud con dominios de aptitudes

Para que el motor de revisión habilitado para inteligencia artificial revise automáticamente una publicación de un usuario en relación con un determinado dominio, la empresa del usuario debe tener asignadas aptitudes personalizadas con los dominios de aptitudes admitidos que existen en el sistema de gestión de aprendizaje Learning Manager.

Al crear una aptitud, un administrador puede asignarla con los dominios de aptitudes más pertinentes que admita Learning Manager. Esto se tendrá en cuenta en el proceso de revisión automática. El sistema de gestión de aprendizaje Learning Manager presenta las aptitudes siguientes:

* Gestión de la cadena de suministro
* Contabilidad
* Investigación científica e ingeniería
* Seguridad informática
* Gestión estratégica
* Redes sociales
* Medicina
* Finanzas
* Seguridad laboral
* Aptitudes sociales
* Derecho empresarial
* Gestión
* Gestión de recursos humanos
* Comunicación técnica
* Ética de negocios
* Administración de la relación con los clientes
* Tecnologías de la información
* Producción y fabricación
* Marketing
* Gestión de la calidad
* Proceso empresarial
* Aprendizaje
* Diseño
* Análisis
* Ventas

Para añadir un dominio de aptitud, siga los pasos que se indican a continuación:

1. En el panel izquierdo de la aplicación de administrador, haga clic en **[!UICONTROL Aptitudes]**.
1. Para añadir una aptitud, haga clic en **[!UICONTROL Añadir]** en la parte superior derecha de la página.
1. En el cuadro de diálogo **[!UICONTROL Añadir aptitud]**, agregue una aptitud y una descripción de esta.
1. En la sección **[!UICONTROL Dominio de la aptitud]**, añada los dominios de la aptitud. Al indicar un dominio, se añaden los dominios. Estos dominios se completan a partir de la lista mencionada anteriormente.

   ![](assets/skill-domain-mapping.png)

   *Añada los dominios de aptitudes en la sección Dominio de aptitudes*

1. Para guardar los cambios, haga clic en **[!UICONTROL Guardar]**.

Cuando un usuario publica contenido en un tablero, dicho contenido se revisa y se aprueba o se rechaza, según la puntuación de confianza respecto a la aptitud asignada al tablero.

<!--![](assets/content-uploaded.png)-->

Si el contenido que se carga tiene una puntuación de confianza de más del 50 % de la aptitud del tablero, el contenido se publica en el tablero. Si el contenido cumple con los criterios, se obtiene una notificación que indica que el contenido se ha revisado correctamente y que está disponible en el tablero.

![](assets/curation-notification.png)

*Ver notificaciones según la puntuación de confianza*

