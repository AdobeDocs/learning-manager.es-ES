---
description: Obtenga información sobre cómo descargar las transcripciones de alumnos basadas en usuarios, objetos de aprendizaje o aptitudes en Learning Manager.
jcr-language: en_us
title: Transcripciones de alumnos
exl-id: 8204aa1e-0e0d-4d9e-9dc0-6260667bf4e7
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 85%

---

# Transcripciones de alumnos

Obtenga información sobre cómo descargar las transcripciones de alumnos basadas en usuarios, objetos de aprendizaje o aptitudes en Learning Manager.

Adobe Learning Manager permite a los responsables de una empresa generar transcripciones asociadas a los alumnos.

## Generar transcripciones de alumnos {#generatelearnertranscripts}

1. Para generar transcripciones de alumnos, haga clic en **[!UICONTROL Informes]** en el panel izquierdo del inicio de sesión del responsable.
1. Haga clic en la pestaña **[!UICONTROL Mis informes]** en la página.
1. Haga clic en el vínculo **[!UICONTROL Transcripciones de alumnos]**.

   ![](assets/learner-transcripts.png)

   *Crear informes para transcripciones de alumnos*

1. Aparece un cuadro de diálogo con las transcripciones de los alumnos. Elija el intervalo de fechas para el que necesita la transcripción generada.

   >[!NOTE]
   >
   >De forma predeterminada, la fecha de inicio es la fecha de registro del alumno y la fecha de finalización es siempre la fecha actual. Solo puede modificar la fecha de inicio &quot;desde&quot; cuando necesita los datos.

1. Elija los nombres de los alumnos en el campo Seleccionar alumnos y haga clic en **[!UICONTROL Generar]**.

Puede elegir un solo alumno o grupos de alumnos. Para añadir a más de un alumno, haga clic en Añadir más alumnos.

Las transcripciones se generan y se descargan en el equipo como archivos .XLS. Cada archivo .xls de Excel tiene siete hojas, cuyos detalles se mencionan a continuación:

## Descargar la transcripción del alumno en función de la zona horaria {#lt-timezone}

Al igual que un administrador, un responsable también puede elegir las columnas que se van a exportar. Además, un responsable puede descargar la transcripción del alumno en función de la zona horaria que haya seleccionado en la configuración del perfil.

Si el responsable activa esta opción, la zona horaria se selecciona de la que se ha definido en la página de configuración del perfil, como se muestra a continuación.

>[!NOTE]
>
>Para un nuevo responsable, la casilla de verificación Zona horaria está desactivada.

![](assets/image030.png)

*Descargar transcripciones de alumnos para un intervalo de tiempo*

## Contenido del archivo de transcripciones de alumnos {#learnertranscriptfilecontent}

Un archivo de transcripciones de alumnos típico se compone de seis hojas de cálculo en un solo archivo. Las hojas de transcripciones de alumnos aportan una visión general de los datos, por ejemplo la cantidad de alumnos por curso, sus aptitudes, el porcentaje de finalización por curso o alumno, así como un tablero de cumplimiento. Estos son los tableros disponibles en las transcripciones de alumnos:

**Transcripciones de alumnos**

En la hoja de cálculo de transcripción de alumno, además de los datos sobre el alumno, se proporciona información sobre el consumo del objeto de aprendizaje como la fecha de inscripción, la fecha de inicio, la nota conseguida, la puntuación de las pruebas, etcétera. Si los cursos forman parte de un programa de aprendizaje, se enumeran aparte de los detalles de consumo de cada curso.

**1- Tablero de actividades de aprendizaje**

En este tablero específico de objetos de aprendizaje, puede ver la cantidad de alumnos de cada curso, programa de aprendizaje o certificación. Puede examinar la hoja de progreso de los alumnos respecto a un determinado objeto de aprendizaje. En esta hoja, se facilitan datos como la cantidad de alumnos que han completado el curso o el programa de aprendizaje, los alumnos que lo están realizando y las fechas de vencimiento de los alumnos.

El progreso de los usuarios del curso concreto se calcula a partir de los campos de Entrada en los que se especifican los umbrales de porcentaje de progreso y la fecha de vencimiento. Por ejemplo, si especifica 7 días y un 70 % en los valores del campo Entrada, se muestra el progreso de los cursos que vencen dentro de 7 días y los cursos que tienen un progreso de más del 70 %. También puede cambiar el período de tiempo en esta hoja, donde se muestran automáticamente en el tablero los datos modificados.

**2- Tablero de actividades de aprendizaje**

En este tablero de aprendizaje, se facilitan datos de un usuario determinado. En este tablero, puede ver los cursos, los programas de aprendizaje o las certificaciones en que se ha inscrito un usuario determinado. Asimismo, la tabla ofrece datos sobre los objetos de aprendizaje completados por el usuario, los objetos de aprendizaje en curso y las próximas fechas de vencimiento para el usuario.

El progreso de los usuarios de cada curso se calcula en función de las entradas que haya especificado. Es decir, los valores de porcentaje de progreso y la fecha de vencimiento. Por ejemplo, si especifica 7 días y un 70 % en los valores del campo Entrada, se muestra el progreso del usuario en los diferentes cursos que vencen dentro de 7 días y en los cursos que tienen un progreso de más del 70 %.

**Aptitud**

En esta hoja, se proporcionan, entre otros, datos como el nombre y el nivel de la aptitud, los réditos necesarios y los obtenidos, y el porcentaje de finalización. A continuación se muestra una captura de pantalla de hoja de cálculo de aptitudes de ejemplo.

**Tablero de aptitudes**

En este panel, podrá ver si su empresa está dotada de varias aptitudes. Para una aptitud concreta, puede consultar la cantidad de usuarios de una empresa que deben tener dicha aptitud frente a la cantidad que realmente la tienen. Este tablero también especifica los usuarios que podrían necesitar una actualización de sus aptitudes. Este valor se calcula en función de lo que se indique en el campo Entrada. Por ejemplo, si indica 50 días, el tablero proporciona información sobre los usuarios que podrían necesitar una actualización de sus aptitudes transcurridos 50 días.

Este tablero de aptitudes es más específico del usuario. Puede filtrar uno o varios usuarios y ver su nivel de aptitud en forma de tablero. Con esta hoja, los responsables y los administradores realizan el seguimiento del nivel de aptitud de cada alumno en comparación con el nivel de aptitud que está previsto que adquieran. Asimismo, el tablero de aptitud indica quiénes son los alumnos que deben poner al día sus aptitudes. La lista de actualización de alumnos se basa en el número de días que se especifican en el campo Entrada.

**Tablero de cumplimiento**

Este tablero tiene dos partes, el informe de cumplimiento de usuario y el informe de cumplimiento por formación. En el informe basado en usuario, el tablero de cumplimiento es válido para efectuar el seguimiento de los alumnos que tienen fechas de vencimiento inminentes relativas a iniciativas importantes de cumplimiento. En el caso del informe basado en formación, puede filtrar por programa de aprendizaje o certificación.

En los dos informes de cumplimiento, filtre por fecha de vencimiento para ver los datos correspondientes.
