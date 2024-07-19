---
jcr-language: en_us
title: Integración de Learning Manager con Slack
description: Integración de Learning Manager con Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 44%

---



# Integración de Learning Manager con Slack

**Se ha quitado** **Slack** como conector en Learning Manager. Ya no tendrá acceso al conector de Slack.

Como usuario de Slack, puede instalar la aplicación Adobe Learning Manager del Directorio de aplicaciones de Slack en sus equipos de Slack y explorar el contenido de Learning Manager directamente desde Slack. Puede interactuar con Primebot para buscar nuevos cursos, ver recomendaciones y recibir notificaciones sobre las próximas fechas límite en Learning Manager. También puede inscribirse e ir directamente a su aprendizaje desde Slack.

La aplicación de Learning Manager para Slack no es compatible con una instancia de Azure de Learning Manager.

## Instalación de la aplicación Adobe Learning Manager {#installingadobecaptivateprimeapp}

Como alumno, puede instalar la aplicación CP Prime en su cuenta de Slack. Para instalar la aplicación, en su cuenta Slack abra el Directorio de aplicaciones y busque Learning Manager. Descargue e instale la aplicación. Si la aplicación no está aprobada en su cuenta, póngase en contacto con el administrador de integración para obtener la aprobación. Si ya está aprobada, podrá iniciar sesión.

## Aprobar el inicio de sesión de alumnos como administrador de integración {#approvinglearnersigninasanintegrationadmin}

Como administrador de integración, para aprobar el permiso de un alumno para utilizar la aplicación Captivate Prime en el Slack, siga estos pasos.

1. Seleccione **[!UICONTROL Aplicaciones]** en el panel izquierdo y haga clic en la ficha **[!UICONTROL Aplicaciones destacadas]**.

   ![](assets/featuredapps.jpg)

1. Haga clic en el mosaico **[!UICONTROL Slack]** > se abre la página web de integración con Slack. Haga clic en **[!UICONTROL Aprobar]** en la esquina superior derecha para aprobar la aplicación.

   ![](assets/approval.png)

1. Vuelva a la página **[!UICONTROL Aplicaciones]**. Una vez aprobado, el Slack debe aparecer en la pestaña **[!UICONTROL Aplicaciones externas]**.
1. Los alumnos podrán iniciar sesión en su cuenta de Prime con Slack.

## Funcionalidades de Primebot {#primebotfunctionalities}

Ahora puede empezar a interactuar con el Primebot. A continuación, se especifican las funcionalidades del bot.

1 - Comando

&#42;/prime&#42; se puede usar para consultas puntuales relacionadas con tu cuenta de Adobe Learning Manager.

Los subcomandos disponibles son:

/prime find `<query>`: buscar cursos, certificaciones, etc.

/prime recommend: ver recomendaciones

/prime deadlines: ver los plazos vencidos y próximos

/prime enrollments: ver inscripciones

/prime skills: ver aptitudes

/prime notifications: ver notificaciones

/prime catalogs: ver catálogos

/prime invite: [Solo administrador] invita a los usuarios Slack del equipo actual a probar primebot

/prime profile: ver perfil

/prime logout: cerrar la sesión de la cuenta de Prime en este equipo de Slack

/prime help: ver un mensaje de ayuda

2 - Recomendar

Puedes probar una frase como `show my recommendations` para obtener una lista personalizada de cursos recomendados, certificaciones y programas de aprendizaje de tu cuenta de Adobe Learning Manager.

3 - Búsqueda

Puedes probar frases como `search for machine learning` o `search for artificial intelligence`. Puede especificar el tipo de objeto de aprendizaje mediante frases como `search for machine learning certifications`, `search for artificial intelligence courses` o `search for adobe photoshop job aids`. También puede buscar dentro de un catálogo usando frases como `search for machine learning in Lynda catalog`.

4 - Plazos

Usa frases como `show my deadlines` para obtener una lista de las fechas límite vencidas y futuras de tu cuenta de Adobe Learning Manager. Puedes filtrar las fechas límite vencidas o próximas con frases como `show my overdue deadlines` o `show my upcoming deadlines`.
