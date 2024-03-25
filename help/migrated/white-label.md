---
jcr-language: en_us
title: Etiquetado en blanco en la aplicación móvil de Adobe Learning Manager
description: El etiquetado blanco es una práctica que consiste en cambiar la marca de una aplicación o servicio con tu propia marca y personalizarlo como si fueras el creador original. En Adobe Learning Manager, puede aplicar etiquetas blancas a la aplicación móvil para cambiar la marca de la aplicación y ponerla a disposición de los usuarios con su propia marca.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 8228a6b78362925f63575098602b33d3ee645812
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 0%

---

# Etiquetado en blanco en la aplicación móvil de Adobe Learning Manager

La aplicación móvil de Adobe Learning Manager ahora admite el etiquetado de blancos, lo que significa que ahora puede publicar la aplicación con su propia marca.

## Cómo debe empezar a prepararse para iniciar la aplicación con etiqueta blanca

Para implementar y administrar su propia aplicación con etiqueta blanca, siga estos pasos:

1. Prepare los activos (como la imagen de la pantalla de bienvenida) y el texto para poder usar ambos en la aplicación y la descripción en la tienda de aplicaciones/reproducción.

1. Asignar un recurso técnico que sea capaz de:

* Generando los archivos de certificado de notificación de inserción.
* Firmar los archivos binarios de la aplicación proporcionados por el equipo de ALM.
* Cargar y administrar el proceso de publicación. El proceso de publicación requiere la comunicación entre el administrador de aplicaciones y los equipos de la tienda de aplicaciones/play para que la aplicación cumpla con todas las directrices de publicación. Desde ALM, recibirá un binario de aplicación totalmente compatible.

## Información general

El etiquetado blanco es una práctica que consiste en cambiar la marca de una aplicación o servicio con tu propia marca y personalizarlo como si fueras el creador original. En Adobe Learning Manager, puede aplicar etiquetas blancas a la aplicación móvil para cambiar la marca de la aplicación y ponerla a disposición de los usuarios con su propia marca.

## Aspectos que se pueden personalizar

Se pueden personalizar las siguientes opciones:

### Campos

<table>

    <tbody>

    <tr>

   <td>

    <p>Id De Cuenta</p></td>

   <td>

    <p>El ID de su cuenta. Tenga en cuenta que los alumnos que pertenezcan a cualquier otra cuenta no podrán acceder a la aplicación con etiqueta blanca.</p></td>

  </tr>

  <tr>

   <td>

    <p>Id. de cuenta adicionales</p></td>

   <td>

    <p>Agregue varias cuentas (subdominios) si lo desea. Añada los subdominios separados por comas sin espacios. Por ejemplo, acc01,acc02,acc03, etc.<br> <b>Nota:</b> Debe añadir el ID de cuenta al especificar los subdominios.</br> </p></td>

  </tr>

  <tr>

  <td>

  <p>Nombre de aplicación</p></td>

  <td>

  <p>El nombre que desea usar para la aplicación.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nombre abreviado de la aplicación</p></td>

  <td>

  <p>En los casos en que el nombre de la aplicación sea largo, asigne a la aplicación un nombre corto que aparezca en el dispositivo.</p></td>

  </tr>

   <tr>

  <td>

  <p>Nombre de aplicación interna</p></td>

  <td>

  <p>Nombre con el que el sistema operativo identifica la aplicación. El formato que se suele utilizar es: com.nombre-empresa.nombre-producto.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nombre de la aplicación interna: iOS</p></td>

  <td>

  <p>Asigne a la aplicación un nombre diferente si los usuarios están en iOS. Se recomienda utilizar el mismo nombre para iOS y Android.</p></td>

  </tr>

  <tr>

  <td>

  <p>Icono de aplicación</p></td>

  <td>

  <p>El icono de la aplicación es png. Este icono se muestra en la aplicación. El formato que se debe asignar al nombre es account-id_appIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>Pantalla de bienvenida de aplicaciones</p></td>

  <td>

  <p>Para la pantalla de bienvenida de su aplicación, proporcione una imagen (png) que aparezca cuando los usuarios inicien la aplicación. El formato que se debe asignar al nombre es account-id_splashIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>ID de cliente y secreto de cliente</p></td>

  <td>

  <p>El administrador de integración de su cuenta proporciona los detalles al registrar la aplicación. El administrador de integración debe utilizar lo siguiente:<ul><li>alumno:leer,alumno:escribir como función</li><li>aplicación interna name://redirect como URL de redirección</li></ul></p></td>

  </tr>

  <tr>

  <td>

  <p>Logotipo de la cuenta</p></td>

  <td>

  <p>La dirección URL que aloja el logotipo de su organización. Proporcione un vínculo cpcontents como logotipo de la cuenta. La URL debe estar codificada en la web.</p></td>

  </tr>

  <tr>

  <td>

  <p>Id. de App Store para la aplicación (iOS)</p></td>

  <td>

  <p>El ID necesario para implementar la actualización forzada. La aplicación debe saber que el alumno debe redirigirse a la tienda de aplicaciones para actualizar la aplicación.</p></td>

  </tr>

   <tr>

  <td>

  <p>ID de Google Play Store para la aplicación (Android)</p></td>

  <td>

  <p>El ID necesario para implementar la actualización forzada.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nombre de host para enlaces profundos</p></td>

  <td>

  <p>Para alojar vínculos profundos, utilice learning Manager. Si desea utilizar otra dirección URL de nombre de host como vínculo profundo, proporcione la dirección URL del host. Por ejemplo, learningmanager.adobe.com.</p></td>

  </tr>

    </tbody>

</table>

>[!NOTE]
>
>Proporciona los datos a tus CSAM para que puedan añadirlos al binario de tu aplicación personalizada.


#### Actualizar asociación de sitio para controlar vínculos profundos personalizados

Si utiliza un dominio personalizado o learningmanager\*.adobe.com como host, no es necesario realizar ninguna acción. Sin embargo, si utiliza una solución personalizada o un nombre de host específico para las direcciones URL, agregue los archivos de asociación del sitio.

>[!CAUTION]
>
>Si los archivos no están presentes, los vínculos profundos no funcionarán. Asegúrese de que los archivos estén presentes.


Consulte los siguientes vínculos para obtener más información:

- [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)

- [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Generar notificaciones push

El envío de notificaciones push a las aplicaciones Android y iOS requiere dos mecanismos diferentes.

* Para iOS, genere los certificados de notificación de inserción.
* Para Android, proporcione una clave de servidor generada a partir del proyecto Firebase.

Siga las instrucciones que se indican a continuación para configurar los proyectos en Firebase:

### Notificaciones push en iOS

En el desarrollo de aplicaciones de iOS, un certificado de notificación de inserción es una credencial criptográfica emitida por Apple que permite a un servidor enviar notificaciones de inserción de forma segura a un dispositivo iOS a través del servicio de notificaciones de inserción (APN) de Apple.

El certificado garantiza una comunicación segura entre su servidor (o proveedor) y las APN de Apple al enviar notificaciones push a dispositivos iOS.

Tanto Android como iOS utilizan Firebase Cloud Messaging (FCM) como servicio para enviar notificaciones push a dispositivos.

### Cómo generar el certificado en iOS

Siga el procedimiento:

1. Genere o descargue el **Certificado de notificación de inserción** y clave privada (.p12). Para obtener más información, consulte la [Documento para desarrolladores de Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Instale el archivo p12 después de descargar el archivo. Utilice la contraseña para instalar en su **Acceso a Llaveros**.

1. Vaya a **Mis certificados** y exporte el certificado. Asegúrese de seleccionar el tipo MIME .cer.

1. Una vez que tenga disponibles el archivo p12 y el archivo cer, ejecute los siguientes comandos:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```
Si puede conectarse al servidor, el certificado que ha creado es válido. En el archivo myapnappkey.pem, copie el certificado y los valores de clave privada.

### Notificaciones push en Android

Configure un proyecto en Firebase y comparta la clave del servidor con el CSAM.

Póngase en contacto con el equipo de CSM y obtenga los archivos agregados a los servicios SNS en AWS. Los usuarios tendrán que obtener la entrada registrada en el servicio SNS para la notificación de inserción, lo que les exigirá compartir los certificados generados anteriormente para su validación.

>[!NOTE]
>
>Para Android, el usuario debe proporcionar la clave de servidor del proyecto de Firebase que crea para Android para añadir la entrada en el servicio SNS.


## Crear proyecto en Firebase

### Android

Vuelva a utilizar el mismo proyecto que ha creado en los pasos anteriores para las notificaciones push.

[Agregar el proyecto](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) en Firebase y recupere el ***google-services.json*** archivo.

### iOS

[Agregar el proyecto](https://firebase.google.com/docs/ios/setup) a Firebase y recuperar el ***GoogleService-Info.plist*** archivo.

>[!IMPORTANT]
>
>Envíe los archivos al equipo de CSAM de Adobe Learning Manager para incluirlos en la compilación del archivo binario de la aplicación.


## Generar los archivos binarios firmados

### iOS

```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist ./deviceAppBuildScripts/${ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```

>[!NOTE]
>
>Necesitará XCode 15.2 o superior para crear los archivos binarios firmados.


## Android

```
sh""" ~/Library/Android/sdk/build-tools/30.0.3/apksigner sign --ks $storeFile --ks-pass "pass:$store\_password" --ks-key-alias $key\_alias --key-pass "pass:$key\_password" --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Necesitará herramientas de creación de sdk de Android para crear los archivos binarios firmados.

**¿Qué viene después?**

Después de generar los archivos binarios, muévalos a Play Store o App Store.

## ¿Cómo puedo aplicar los cambios?

Envía los activos y archivos necesarios al equipo de CSM. A continuación, el equipo de CSM rellena el [forma](https://forms.office.com/r/bJRRaRBvSh) con los cambios necesarios y adjunta los activos necesarios. A continuación, el equipo examinará los cambios e informará a los equipos de ingeniería al respecto. A continuación, el equipo de ingeniería generará una compilación y la compartirá con el equipo de CSM.

El equipo de CSM compartirá la compilación con el cliente.

## Qué no se puede personalizar

- Pantalla Actualizar contraseña
- Pantalla Crear una cuenta
