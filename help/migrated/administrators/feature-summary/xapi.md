---
jcr-language: en_us
title: xAPI en Learning Manager
description: Experience API (xAPI) es una especificación de software de aprendizaje electrónico que permite que el contenido de aprendizaje y los sistemas de aprendizaje se comuniquen entre sí de forma que se registren y se realice un seguimiento de todos los tipos de experiencias de aprendizaje. Las experiencias de aprendizaje se registran en un almacén de registros de aprendizaje (LRS). Los LRS pueden existir dentro de los sistemas tradicionales de gestión del aprendizaje (LMS) o por su cuenta.
contentowner: dvenkate
preview: true
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 0%

---



# xAPI en Learning Manager

## ¿Qué es xAPI? {#whatisxapi}

Experience API (xAPI) es una especificación de software de aprendizaje electrónico que permite que el contenido de aprendizaje y los sistemas de aprendizaje se comuniquen entre sí de forma que se registren y se realice un seguimiento de todos los tipos de experiencias de aprendizaje. Las experiencias de aprendizaje se registran en un almacén de registros de aprendizaje (LRS). Los LRS pueden existir dentro de los sistemas tradicionales de gestión del aprendizaje (LMS) o por su cuenta.

Para obtener más información sobre xAPI, consulte [Especificaciones de xAPIc](https://github.com/adlnet/xAPI-Spec).

## ¿Cómo admite xAPI Learning Manager? {#howdoeslearningmanagersupportxapi}

Learning Manager tiene un almacén de registros de aprendizaje incorporado. Este LRS tiene la capacidad completa de aceptar declaraciones xAPI de contenido alojado en Learning Manager. Incluso acepta declaraciones de xAPI que generan terceros. Estas declaraciones de xAPI se almacenan en Learning Manager y, a continuación, se pueden exportar fuera de Learning Manager para visualizarlas en cualquier sistema de almacenamiento de datos de terceros.

## ¿Cuándo se utiliza xAPI? {#whendoyouusexapi}

Cada vez es más necesario capturar las experiencias de aprendizaje del usuario final, que se extienden a varios sistemas.  También es necesario realizar un seguimiento de la participación exacta del alumno en el contenido de la formación. Va más allá de Inicio, En curso y Finalización (los únicos atributos capturados por SCORM).

## Uso de xAPI en Learning Manager {#usingxapiinprime}

### Configurar la aplicación {#setupyourapplication}

1. Inicie sesión como administrador de integración. Seleccionar **[!UICONTROL Aplicaciones > Registrar]**.

   ![](assets/appregistration.png)

   *Página de inicio para registrar una aplicación*

1. Registre una nueva aplicación.

   ![](assets/appregistration.png)

   *Registrar una nueva aplicación*

1. Defina el ámbito de la aplicación.

   * Si **[!UICONTROL Acceso de lectura y escritura xAPI de la función de administrador]** Cuando está activada, el administrador puede publicar y obtener declaraciones y documentos de xAPI.
   * Si **[!UICONTROL Acceso de lectura y escritura de xAPI de la función Alumno]** Cuando está activada, el administrador puede publicar y obtener declaraciones y documentos de xAPI.

1. Guardar cambios. Obtendrás tu ID y secreto de desarrollador.

**Puntos finales**:

Haga clic en el vínculo siguiente para ver el documento de intercambio de xAPI:

[Documento xAPI Swagger](https://learningmanagereu.adobe.com/docs/primeapi/xapi/)

>[!NOTE]
>
>La versión de xAPI admitida en Learning Manager es 1.0.3.


## Autenticación de API {#apiauthentication}

xAPI de Learning Manager utiliza el marco de OAuth 2.0 para autenticar y autorizar las aplicaciones cliente. Una vez registrada la aplicación, puede obtener el ID y el secreto de cliente. La URL de obtención se utiliza en el navegador, ya que autentica a los usuarios de Learning Manager mediante sus cuentas preconfiguradas, como SSO o Adobe ID.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<admin:xapi or learner:xapi>&response_type=CODE.
```

## Seguimiento de declaraciones de xAPI como objeto de aprendizaje del administrador {#trackingxapistatementsasprimelo}

Como autor, ahora puede elegir el módulo xAPI al crear cursos para supervisar la experiencia del usuario fuera de Learning Manager. Por ejemplo, puede utilizar esta función para evaluar las actividades de los usuarios en una plataforma de terceros utilizada para el consumo de cursos.

1. Al crear un **[!UICONTROL Módulo de actividad]**, en el símbolo **[!UICONTROL Tipo]**, utilice el menú emergente para seleccionar  **[!UICONTROL Módulo basado en xAPI.]**

   ![](assets/xapimodulecreation.png)

   *Seleccione la opción Módulo basado en xAPI*

1. Se le solicita que proporcione un IRI. Si no se proporciona, Learning Manager genera uno automáticamente.

   El IRI de una actividad es único en una cuenta. Es decir, dos módulos de Learning Manager no pueden tener el mismo IRI. Se genera un nuevo IRI en los siguientes casos:

   * Cuando se comparte un curso con el módulo xAPI entre cuentas.
   * Cuando se repite una certificación con el módulo xAPI



   Cualquier instrucción xAPI con el IRI mencionado se rastrea en el módulo anterior y se refleja en los informes de Learning Manager.

1. Para copiar el IRI generado automáticamente, vuelva a visitar la página Módulo de actividad.
1. Publique el módulo.

**Aspectos a tener en cuenta:**

* Actualmente, Learning Manager solo admite mbox como identificador. No se admiten otros identificadores, como mboz_sha1, openid , account.

* El stateId y el profileId son un UUID cuando se utilizan con Learning Manager.
* La solicitud de PUT no sobrescribe el documento para los agentes/perfil, actividad/perfil y actividad/estado de xAPI
* El grupo no identificado no es compatible con Actor.
* El parámetro &quot;related_activities&quot; no se admite en la instrucción GET.
* Los parámetros &#39;format=ids&#39; y &#39;format=canonical&#39; no se admiten en las instrucciones de GET.
* La anulación de la sentencia xAPI no deshace ninguna acción que se haya producido en Learning Manager cuando se publicó la sentencia.

## Generar informes {#generatereports}

Los informes de xAPI se pueden generar como informes de Excel. Como administrador, abra **[!UICONTROL Informes > Informes de Excel > Informe de actividad de xAPI]**.

El informe descargado obtiene toda la información publicada por el alumno y el administrador para cualquier instrucción.

Los mismos informes se pueden generar y programar mediante conectores de FTP y Box para cualquier integración de terceros. Siga estos pasos:

Iniciar sesión como **Administrador de integración > Abrir conector de FTP/Box > Seleccionar informe de actividad de xAPI** en el panel izquierdo. Elija programar/ generar un informe.

![](assets/xapischedule.png)

*Programar o generar un informe*

* Cuando solo se envía una puntuación RAW en una instrucción xAPI sin puntuación máxima, la puntuación de prueba no se muestra en LT.

* Para obtener la puntuación porcentual en Learning Manager, las puntuaciones escaladas se envían a través de xAPI.

## Ejemplo de informe {#samplereport}

[Ejemplo de informe de xAPI.](assets/xapireport8842560559890766717csv.zip)
