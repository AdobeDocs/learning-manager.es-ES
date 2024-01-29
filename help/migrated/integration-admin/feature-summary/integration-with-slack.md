---
jcr-language: en_us
title: Integración de Learning Manager con Slack
description: Integración de Learning Manager con Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---



# Integración de Learning Manager con Slack

Nosotros tenemos **eliminado** **Slack** como conector en Learning Manager. Ya no tendrá acceso al conector de Slack.

Como usuario Slack, puede instalar la aplicación Adobe Learning Manager desde el directorio de aplicaciones de Slack en sus equipos de Slack y explorar el contenido de Learning Manager directamente desde Slack. Puede interactuar con Primebot para buscar nuevos cursos, ver recomendaciones y recibir notificaciones sobre las próximas fechas límite en Learning Manager. También puede inscribirse y saltar directamente a su aprendizaje desde Slack.

La aplicación de Learning Manager para Slack no es compatible con una instancia de Azure de Learning Manager.

## Instalación de la aplicación Adobe Learning Manager {#installingadobecaptivateprimeapp}

Como alumno, puede instalar la aplicación CP Prime en su cuenta de Slack. Para instalar la aplicación, en su cuenta de Slack, abra el directorio de la aplicación y busque Learning Manager. Descargue e instale la aplicación. Si la aplicación no está aprobada en su cuenta, póngase en contacto con el administrador de integración para obtener la aprobación. Si ya está aprobado, podrá iniciar sesión.

## Aprobar el inicio de sesión del alumno como administrador de integración {#approvinglearnersigninasanintegrationadmin}

Como administrador de integración, para aprobar el permiso de un alumno para utilizar la aplicación Captivate Prime en el Slack, siga estos pasos.

1. Seleccionar **[!UICONTROL Aplicaciones]** en el panel izquierdo y haga clic en el **[!UICONTROL Aplicaciones destacadas]** .

   ![](assets/featuredapps.jpg)

1. Haga clic en el **[!UICONTROL Slack]** se abre el mosaico > la página de integración de slack. Haga clic en **[!UICONTROL Aprobar]** en la esquina superior derecha para aprobar la aplicación.

   ![](assets/approval.png)

1. Volver a la **[!UICONTROL Aplicaciones]** página. Una vez aprobado, el Slack debe aparecer en la **[!UICONTROL Aplicaciones externas]** .
1. Los alumnos ahora pueden iniciar sesión en su cuenta de Captivate Prime mediante Slack.

## Funcionalidades de Primebot {#primebotfunctionalities}

Ahora puede empezar a interactuar con el Primebot. Las siguientes son las funcionalidades del bot.

1 - Comando

&#42;/prime&#42; se puede utilizar para consultas puntuales relacionadas con su cuenta de Adobe Learning Manager.

Los subcomandos disponibles son:

/prime find `<query>` - buscar cursos, certificaciones, etc.

/prime recomiende: mostrar recomendaciones

/prime dates: mostrar los plazos vencidos y próximos

/prime enrollments - mostrar inscripciones

/prime skills: mostrar aptitudes

/prime notifications: mostrar notificaciones

/prime catalogs: mostrar catálogos

/prime invite - [Solo para administradores] invitar a los usuarios de Slack del equipo actual a probar primebot

/prime profile- mostrar perfil

/prime logout: cerrar sesión en su cuenta de Captivate Prime en este equipo de Slack

/prime help: mostrar mensaje de ayuda

2 - Recomendar

Puedes probar una frase como `show my recommendations` para obtener una lista personalizada de cursos recomendados, certificaciones y programas de aprendizaje de su cuenta de Adobe Learning Manager.

3 - Búsqueda

Puedes probar frases como `search for machine learning` o `search for artificial intelligence`. Puede especificar el tipo de objeto de aprendizaje mediante frases como `search for machine learning certifications`, `search for artificial intelligence courses` o `search for adobe photoshop job aids`. También puede buscar dentro de un catálogo utilizando frases como `search for machine learning in Lynda catalog`.

4 - Plazos

Usar frase como `show my deadlines` para obtener una lista de los plazos vencidos y próximos de su cuenta de Adobe Learning Manager. Puedes filtrar las fechas límite vencidas o próximas con frases como `show my overdue deadlines` o `show my upcoming deadlines`.
