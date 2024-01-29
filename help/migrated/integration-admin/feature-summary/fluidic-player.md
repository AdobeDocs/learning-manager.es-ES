---
description: Lea este artículo para aprender a incrustar el reproductor Fluidic en una aplicación personalizada.
jcr-language: en_us
title: Reproductor Fluidic incrustable
contentowner: dvenkate
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---



# Reproductor Fluidic incrustable

Lea este artículo para aprender a incrustar el reproductor Fluidic en una aplicación personalizada.

Como empresa, ahora puede proporcionar una experiencia personalizada a los alumnos incluso fuera de Learning Manager. Con la API pública, puede obtener toda la información relacionada con los objetos de aprendizaje, las inscripciones de los alumnos y el progreso del aprendizaje, y mostrarlos en su sitio web. Y lo que es más importante, puedes incluso incrustar el reproductor Fluidic de Learning Manager en tu sitio web, para que el alumno pueda consumir el contenido directamente en tu sitio web. El reproductor Fluidic permite reproducir cualquier contenido compatible con Learning Manager. Cuando se incrusta en su propio sitio web, tiene exactamente las mismas capacidades que cuando se utiliza en Learning Manager.

**Reproducir cualquier contenido de aprendizaje online[](../../learners/feature-summary/fluidic-player.md#main-pars_text_779047019)**

El reproductor Fluidic reproduce prácticamente cualquier tipo de contenido de aprendizaje electrónico de la misma forma coherente e intuitiva, sin necesidad de plugins ni descargas. El alumno puede iniciar el contenido y, independientemente del tipo de archivo de contenido, comienza a reproducirse.

**Notas y marcadores**

Puede tomar notas y marcar cualquier contenido, independientemente de su tipo de archivo. Si desea realizar una selección determinada de un archivo o vídeo largo, puede marcar los puntos donde ha encontrado la información que es relevante para sus necesidades. Las notas y los marcadores se pueden buscar o enviar como correo electrónico. Al hacer clic en ellas, se coloca en el reproductor Fluidic exactamente en ese punto del vídeo o página del documento.

Para obtener más información sobre el reproductor Fluidic, consulte [Reproductor Fluidic](../../learners/feature-summary/fluidic-player.md).

A continuación se muestran algunos ejemplos de dónde puede utilizar el reproductor Fluidic incrustable.

* Puede utilizar el reproductor Fluidic incrustable en su sitio web**** para enumerar los cursos en los que se ha inscrito su empleado y, además, proporcionar un vínculo para iniciar un curso de formación en la misma página. Esto significaría que los alumnos pueden consumir cursos de formación en el sitio web de la intranet.

* Si se dedica a la formación, puede que tenga un sitio web en el que sus clientes adquieran cursos. Puedes integrar el reproductor incrustable en el mismo sitio web para que tus clientes puedan consumir el contenido que compren dentro de tu sitio web.

## Pasos para incrustar el reproductor Fluidic en su sitio web {#stepstoembedfluidicplayerinyourwebsite}

La creación de una aplicación personalizada para incrustar el reproductor Fluidic en su sitio web implica tres pasos básicos:

1. Cree una aplicación en la aplicación de administración de integración de Learning Manager.
1. Recupere el token de acceso.
1. Utilice el token de acceso para recuperar recursos de Learning Manager mediante una API pública.

### 1. Cree una aplicación en el administrador de integración {#1createanapplicationinintegrationadmin}

Este paso es necesario para crear un ID de aplicación/cliente y un secreto de aplicación/cliente que se utiliza para recuperar el token de actualización y el token de acceso. Para obtener más información sobre cómo crear una aplicación, consulte  [Proceso de desarrollo de aplicaciones.](developer-manual.md#main-pars_header_994876235)

1. Vaya a **[!UICONTROL IntegrationAdmin]** aplicación y abrir **[!UICONTROL Aplicaciones]**.

1. Seleccionar **[!UICONTROL Registro]** en la esquina superior derecha de la página.
1. La **[!UICONTROL Registrar una nueva aplicación]** se abre la ventana. Rellene los campos obligatorios.
1. Si la aplicación personalizada debe compartirse entre varias cuentas, seleccione **[!UICONTROL No]** en el campo de opción  **[!UICONTROL ¿Solo para esta cuenta?]**
1. Para guardar la aplicación y generar su ID y secreto de aplicación, haga clic en **[!UICONTROL Guardar]**.

### 2. Recuperando token de acceso {#2retrievingaccesstoken}

Como Learning Manager utiliza OAUTH2.0., se necesita el token de acceso para recuperar recursos mediante la API pública. El token de acceso se puede obtener mediante el token de actualización, el ID de cliente o el secreto de cliente.

**2.1 Token de actualización**

* Recuperar código de OAuth

Se requiere código OAuth para recuperar el token de actualización. Learning Manager redirige al usuario a la URL de redirección con el código OAuth al iniciar sesión mediante la URL siguiente (la extracción de código OAuth se ejemplifica en el archivo &quot;oauthredirect.html&quot; en la aplicación de ejemplo):

```
code https://learningmanager.adobe.com/oauth/o/authorize  
client_id= <application_id>  
&redirect_uri=<redirect_uri>  
&state=<dummy_data>  
&scope=learner:read,learner:write  
&response_type=CODE  
&account=<account_id>  
&email=<email_id>
```

Aquí, **[!UICONTROL id de cliente]** es el id de aplicación obtenido en el paso 1.
**[!UICONTROL redirect_url]** es la redirect_url establecida en el paso 1.
**[!UICONTROL estado]** es cualquier dato ficticio en función del cual necesitamos filtrar la URL de redirección para obtener el código OAuth. El ámbito es el ámbito del alumno establecido en el paso 1.
**[!UICONTROL response_type]**e es siempre &quot;CODE&quot;.\
**[!UICONTROL cuenta]** es un campo opcional\
**[!UICONTROL correo electrónico]** es un campo opcional\
&#42; Si se proporciona tanto el ID de cuenta como el correo electrónico, la URL anterior permitirá al usuario iniciar sesión en la misma cuenta. Este ejemplo de punto final se muestra en el archivo &quot;index.html&quot; de la aplicación de ejemplo.

* Recuperar token de actualización

Una vez recibido el código OAuth, el token de actualización se puede recuperar utilizando el código OAuth recibido, el id. de cliente y el secreto de cliente desde el punto final siguiente:

**https://learningmanager.adobe.com/oauth/token**

Como respuesta a tu solicitud de publicación, recibirás lo siguiente:

i. token_actualización\
ii. access_token\
iii. user_id\
iv. expires_in\
v. user_role\
vi. account_id

**2.2 Recuperación del token de acceso del token de actualización**

Para recuperar su token de acceso, envíe otra solicitud con su token_actualización, ID_cliente y secreto_cliente como cuerpo de la publicación a la siguiente URL:

**https://learningmanager.adobe.com/oauth/token/refresh**

Como respuesta a tu solicitud de publicación, recibirás lo siguiente:\
i. token_actualización\
ii. access_token\
iii. user_id\
iv. expires_in\
v. user_role\
vi. account_id

### 3. Recupere recursos usando la API pública {#3retrieveresourcesusingpublicapi}

Como tercer paso, debe utilizar el token de acceso para recuperar recursos de Learning Manager mediante API públicas .  Se requiere un token de acceso para realizar cualquier llamada de API pública y se debe agregar en el encabezado, como se muestra en la aplicación de ejemplo.

## Reproductor incrustable {#embeddableplayer}

Las aplicaciones de terceros pueden utilizar un reproductor incrustable para reproducir el contenido de un objeto de aprendizaje.

**Abrir un curso en el reproductor incrustable**

1. Crear una dirección URL incrustable

   Para abrir un curso con el reproductor incrustable, debe crear una dirección URL incrustable, como se muestra a continuación:

   `https://learningmanager.adobe.com/app/player?lo_id=<v2-api course id>&access_token=<access_token>`

   Aquí, lo_id debe cumplir con el formato de ID de curso de la API V2.

   Ejemplo: `https://learningmanager.adobe.com/app/player?lo_id=course:123456&access_token=45b269b75ac65d6696d53617f512450f`

   Las certificaciones, los programas de aprendizaje y las ayudas de trabajo también se pueden reproducir en el reproductor incrustable.

   Ejemplos: `https://learningmanager.adobe.com/app/player?lo_id=certification:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=learningProgram:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=jobAid:1234&access_token=c1a4847dfbf4007826a027d481b93c1e`

1. Establezca esta URL en el atributo &quot;src&quot; de iframe.

**Cierre del reproductor incrustable**

```
code window.addEventListener("message", function closePlayer(){  
   if(event.data === "status:close"){  
     //handle closing event  
   }  
});
```

## Tutorial de aplicación de ejemplo {#sampleapplicationtutorial}

El documento PDF adjunto contiene un tutorial de aplicación de ejemplo.
[Tutorial de ejemplo y origen del tutorial para incrustar el reproductor Fluidic.](assets/sample-applicationtutorial.zip) Contenidos alternativos

Si es administrador, puede configurar el material del curso para ofrecer contenido alternativo a los alumnos en el reproductor Fluidic. Por ejemplo, si tiene alumnos de distintas zonas geográficas que podrían utilizar varios idiomas, puede crear el mismo contenido en varios idiomas. El reproductor Fluidic ofrecerá al alumno el idioma para el que podría estar configurado, pero este también tiene la opción de cambiar a un idioma alternativo directamente desde el reproductor.

Controles específicos de vídeo

La tecnología de streaming utilizada por el reproductor Fluidic de Learning Manager ofrece a los alumnos una experiencia de reproducción de vídeo sin retrasos al iniciar el vídeo y sin necesidad de espacio en disco en ningún dispositivo. El reproductor Fluidic también ofrece controles inteligentes como la velocidad de reproducción (1x, 1,5X) y saltar +-10 segundos, que están diseñados para proporcionar al alumno el nivel exacto de control que necesita para adaptarse a su velocidad de aprendizaje.

Se trata de un esfuerzo que debe realizar alguien de su equipo de TI o un consultor externo que pueda crear una aplicación que luego se aloje en su sitio.

1. Modifique la URL del reproductor incrustado de Learning Manager con parámetros que apunten al objeto de aprendizaje exacto que se debe tomar.

   URL:  [https://learningmanager.adobe.com/app/player](https://cpcontents.adobe.com/public/embedplayer/index22fa615ec2baa034a22090c8cd4289fa.html)

1. Utilice cualquiera de estos parámetros para iniciar un curso:

   * course_id : ID del curso que se va a iniciar
   * learning_program_id : ID del programa de aprendizaje que se va a iniciar
   * certification_id : ID de la certificación que se va a iniciar
   * lo_id : ID del objeto de aprendizaje (curso/programa de aprendizaje/certificación/ayuda de trabajo) que se reproduce.


1. Utilice el token de acceso como parámetro obligatorio.

   * access_token : Este es el parámetro de seguridad, utilice el token de acceso de oauth de la API pública

   Puede obtener su token configurando su reproductor Fluidic incrustable en su administrador de integración. Puede obtener su token de autenticación, que se puede utilizar como su token de acceso.

   Ejemplo de URL creada; https://learningmanager.adobe.com/app/player?lo_id=&quot;+lo_id+&quot;&amp;access_token=&quot;+accToken

   Aquí, lo_id será el ID del curso, el programa de aprendizaje, la certificación y jobAid .

   Ejemplos de lo_id - course:21324, learningProgram:2143, certification:23432, jobAid:237

1. Realice llamadas a la API de Learning Manager para recuperar los parámetros mencionados anteriormente.

   Estas llamadas a la API las realizará la aplicación que el equipo o asesor de TI escribiría y alojaría en su sitio.

   Puede encontrar más información sobre el uso de la API aquí:

   API de Learning Manager V1: [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



   API de Learning Manager V2: [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)

   Los ID de los objetos difieren de la API V1 y V2. El reproductor incrustable espera ID en formato v2. Utilice la API de asignación de ID en la versión 2 para convertir los ID de la versión 1 a los ID de la versión 2.

   Después de crear la dirección URL, una forma en la que la aplicación la utilizaría para mostrarla al alumno es poniéndola dentro de un iFrame. Al hacer clic en este vínculo, se iniciaría el reproductor Fluidic con el curso concreto en contexto.

   ![](assets/salesforce-player.png)

   Para comprobar los informes de progreso y finalización, inicia sesión en Learning Manager.

   Cuando el alumno cierra el Reproductor, el reproductor Fluidic envía un mensaje de &quot;cierre&quot; al elemento principal mediante html5 postMessage. El controlador de carga debe manejar este mensaje y continuar.

Modifique la URL del reproductor incrustado de Learning Manager con parámetros que apunten al objeto de aprendizaje exacto que se debe tomar.

URL:  [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player)

Cualquiera de estos parámetros se puede utilizar para iniciar un curso:

* course_id : ID del curso que se va a iniciar
* learning_program_id : ID del programa de aprendizaje que se va a iniciar
* certification_id : ID de la certificación que se va a iniciar
* lo_id : ID del objeto de aprendizaje (curso/programa de aprendizaje/certificación/ayuda de trabajo) que se reproduce.

Parámetro obligatorio:

* access_token : Este es el parámetro de seguridad, utilice el token de acceso de oauth de la API pública

Realice llamadas a la API de Learning Manager para recuperar los parámetros mencionados anteriormente. Estas llamadas a la API las realizará la aplicación que el equipo o asesor de TI escribiría y alojaría en su sitio.

Puede encontrar más información sobre el uso de la API aquí:

API de Learning Manager V1: [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



API de Learning Manager V2:  [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)


