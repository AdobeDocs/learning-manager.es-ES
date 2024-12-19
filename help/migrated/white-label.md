---
jcr-language: en_us
title: Etiquetado en blanco en la aplicación móvil de Adobe Learning Manager
description: El etiquetado blanco es una práctica que consiste en cambiar la marca de una aplicación o servicio con tu propia marca y personalizarlo como si fueras el creador original. En Adobe Learning Manager, puede aplicar etiquetas blancas en la aplicación móvil para cambiar la marca de la aplicación y ponerla a disposición de los usuarios con su propia marca.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: eb93f8c5fd3d64366756840789b984ca986dbf0b
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 0%

---

# Etiquetado en blanco en la aplicación móvil de Adobe Learning Manager

La aplicación móvil de Adobe Learning Manager ahora admite el etiquetado blanco, lo que significa que ahora puede publicar la aplicación con su propia marca.

## Cómo debe empezar a prepararse para iniciar la aplicación con etiqueta blanca

Para implementar y administrar su propia aplicación con etiqueta blanca, siga estos pasos:

1. Prepare los activos (como la imagen de la pantalla de bienvenida) y el texto para poder usar ambos en la aplicación y la descripción en la tienda de aplicaciones/reproducción.

1. Asignar un recurso técnico que sea capaz de:

   * Generando los archivos de certificado de notificación de inserción.
   * Firmar los archivos binarios de la aplicación proporcionados por el equipo de ALM.
   * Cargar y administrar el proceso de publicación. El proceso de publicación requiere la comunicación entre el administrador de aplicaciones y los equipos de la tienda de aplicaciones/play para que la aplicación cumpla con todas las directrices de publicación. Desde ALM, recibirá un binario de aplicación totalmente compatible.

## Información general

El etiquetado blanco es una práctica que consiste en cambiar la marca de una aplicación o servicio con tu propia marca y personalizarlo como si fueras el creador original. En Adobe Learning Manager, puede aplicar etiquetas blancas en la aplicación móvil para cambiar la marca de la aplicación y ponerla a disposición de los usuarios con su propia marca.

## Aspectos que se pueden personalizar

Se pueden personalizar las siguientes opciones:

### Campos

<table>

 <tbody>

  <tr>

   <td>

    <p>Id De Cuenta</p>

   </td>

   <td>

    <p>El ID de su cuenta. Tenga en cuenta que los alumnos que pertenezcan a cualquier otra cuenta no podrán acceder a la aplicación con etiqueta blanca.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Id. de cuenta adicionales</p>

   </td>

   <td>

    <p>Agregue varias cuentas (subdominios) si lo desea. Añada los subdominios separados por comas sin espacios. Por ejemplo, acc01,acc02,acc03, etc.<br> <b>Nota:</b> Debe agregar el id. de cuenta al especificar los subdominios.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nombre de aplicación</p></td>

   <td>

    <p>El nombre que desea usar para la aplicación.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nombre abreviado de la aplicación</p>

   </td>

   <td>

    <p>En los casos en que el nombre de la aplicación sea largo, asigne a la aplicación un nombre corto que aparezca en el dispositivo.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nombre de aplicación interna</p></td>

   <td>

    <p>Nombre con el que el sistema operativo identifica la aplicación. El formato que se suele utilizar es: com.nombre-empresa.nombre-producto.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nombre de la aplicación interna: iOS</p>

   </td>

   <td>

    <p>Asigne a la aplicación un nombre diferente si los usuarios están en iOS. Se recomienda utilizar el mismo nombre para iOS y Android.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Icono de aplicación</p>

   </td>

   <td>

    <p>El icono de la aplicación es png. Este icono se muestra en la aplicación. El formato que se debe asignar al nombre es account-id_appIcon.png. Las dimensiones del icono de la aplicación son de 512 × 512 píxeles.<div>Tenga en cuenta que Apple no permite el canal de Alpha en los iconos de la aplicación. Por lo tanto, asegúrese de eliminar el canal del Alpha del recurso antes de enviarlo.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Pantalla de bienvenida de aplicaciones</p></td>

   <td>

    <p>Para la pantalla de bienvenida de su aplicación, proporcione una imagen (png) que aparezca cuando los usuarios inicien la aplicación. El formato que se debe asignar al nombre es account-id_splashIcon.png. Las dimensiones de las pantallas de bienvenida basadas en cuadrados son de 1052 × 1052 píxeles y las pantallas de bienvenida basadas en círculos son de 768 x 768 píxeles.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID de cliente y secreto de cliente</p>

   </td>

   <td>

    <p>El administrador de integración de su cuenta proporciona los detalles al registrar la aplicación. El administrador de integración debe utilizar lo siguiente:<ul><li>alumno:leer,alumno:escribir como función</li><li>aplicación interna name://redirect como URL de redirección</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Logotipo de la cuenta</p>

   </td>

   <td>

    <p>La dirección URL que aloja el logotipo de su organización. Proporcione un vínculo cpcontents como logotipo de la cuenta. La URL debe estar codificada en la web.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Id. de App Store para la aplicación (iOS)</p>

   </td>

   <td>

    <p>El ID necesario para implementar la actualización forzada. La aplicación debe saber que el alumno debe redirigirse a la tienda de aplicaciones para actualizar la aplicación.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID de Google Play Store para la aplicación (Android)</p>

   </td>

   <td>

    <p>El ID necesario para implementar la actualización forzada.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nombre de host para enlaces profundos</p>

   </td>

   <td>

    <p>Para alojar vínculos profundos, utilice learning Manager. Si desea utilizar otra dirección URL de nombre de host como vínculo profundo, proporcione la dirección URL del host. Por ejemplo, learningmanager.adobe.com.</p>

   </td>

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

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

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

1. Genere o descargue el **certificado de notificación push** y la clave privada (.p12). Para obtener más información, consulte el [documento para desarrolladores de Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Instale el archivo p12 después de descargar el archivo. Usa la contraseña para instalar en tu **acceso a Llaveros**.

1. Vaya a **Mis certificados** y exporte el certificado. Asegúrese de seleccionar el tipo MIME .cer.

1. Una vez que tenga disponibles el archivo p12 y el archivo cer, ejecute los siguientes comandos:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Si puede conectarse al servidor, el certificado que ha creado es válido. En el archivo myapnappkey.pem, copie el certificado y los valores de clave privada.

### Notificaciones push en Android

Para Android, el usuario debe proporcionar el archivo services.json del proyecto Firebase para añadir la entrada en el servicio SNS.

Cree un proyecto en Firebase y comparta el archivo services.json con el equipo de CSM. Este archivo es necesario para la entrada basada en token en el SNS. Tenga en cuenta que la clave del servidor ya no se utiliza. Consulte [Crear proyecto en Firebase](#create-project-in-firebase).

Para descargar el archivo services.json, siga estos pasos:

1. Inicie sesión en la consola de **Firebase**.
1. Ve a **Configuración del proyecto** y selecciona **Mensajería en la nube**.
1. Busque la **API de mensajería de Firebase Cloud** y seleccione **Administrar cuentas de servicio**.
1. En la página **Cuentas de servicio**, seleccione **Cuentas de servicio** en el panel izquierdo.
1. Busque la entrada del proyecto y seleccione **Administrar detalles** en Acciones.

   >[!NOTE]
   >
   >   El formato de la entrada de proyecto será &lt;-accountname->@appspot.gserviceaccount.com.

1. Vaya a la pestaña **Claves** y seleccione **Agregar clave**.
1. Si no hay ninguna clave, seleccione **Crear nueva clave** y seleccione **JSON** como tipo de clave. Esto generará y descargará el archivo JSON.
1. Si ya hay una clave, seleccione **Cargar clave existente**, pegue la clave y cárguela. Esto generará y descargará el archivo JSON.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Póngase en contacto con el equipo de CSM y comparta el archivo JSON para añadir la entrada a los servicios SNS en AWS. Los usuarios tendrán que obtener la entrada registrada en el servicio SNS para la notificación de inserción, lo que les exigirá compartir los certificados generados anteriormente para su validación.

## Crear proyecto en Firebase {#create-project-in-firebase}

### Android

Vuelva a utilizar el mismo proyecto que ha creado en los pasos anteriores para las notificaciones push.

[Agregue el proyecto](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) en Firebase y recupere el archivo ***google-services.json***.

### iOS

[Agregue el proyecto](https://firebase.google.com/docs/ios/setup) a Firebase y recupere el archivo ***GoogleService-Info.plist***.

>[!IMPORTANT]
>
>Envíe los archivos al equipo de CSAM de Adobe Learning Manager para incluirlos en la compilación del archivo binario de la aplicación.


## Generar los archivos binarios firmados

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

La carpeta `<root>` contiene el archivo **Runner.xcarchive.zip**. Ejecute los siguientes comandos para generar el binario firmado:

1. Ejecute el siguiente comando para descomprimir el archivo:

   ```
   unzip Runner.xcarchive.zip
   ```

2. Vaya al directorio de la aplicación:

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Copie el archivo de aprovisionamiento móvil:

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Ejecute el siguiente comando para actualizar la información de firma en la biblioteca del framework:

   ```
   codesign -f -s "Distribution Certificate Name" Frameworks/*
   ```

5. Vuelva a la carpeta `<root>` (donde se encuentra Runner.xcarchive.zip):

   ```
   cd <root>
   ```

6. Exporte el archivo usando xcodebuild:

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

7. Localice el archivo .ipa en la carpeta ipa_path.
8. Cargue el archivo .ipa en el sitio web `Diawi`.
9. Una vez cargado por completo, selecciona el botón **[!UICONTROL Enviar]**.
10. Una vez completado el proceso, recibirá un código QR y un vínculo.
11. Abra el código QR o el vínculo directamente en Safari.

Si el dispositivo está incluido en el perfil de aprovisionamiento, la instalación debe continuar en el dispositivo.

>[!NOTE]
>
>Necesitará XCode 15.2 o superior para crear los archivos binarios firmados.


### Android

**Para el archivo APK**

>[!IMPORTANT]
>
>Antes de ejecutar el comando `apksigner`, ejecute los siguientes comandos para exportar la contraseña del almacén de claves y la contraseña del alias de claves como variables de entorno:
>
>```
>export KS_PASS=your_keystore_password
>export KEY_PASS=your_key_password
>```

```
sh""" <path>/apksigner sign --ks $storeFile. --ks-pass env:KS_PASS --ks-key-alias $key_alias --key-pass env:KEY_PASS --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>La ruta de la herramienta `apksigner` suele ser similar a la siguiente: ~/Library/Android/sdk/build-tools/30.0.3/apksigner.

**Para el archivo aab**

>[!NOTE]
>
>Necesitará herramientas de creación de sdk de Android para crear los archivos binarios firmados.

Play Store requiere archivos binarios de Android en formato aab para su publicación. Por lo tanto, proporcionaremos el archivo .aab sin firmar.

>[!NOTE]
>
>Al crear un archivo de almacén de claves, debe generar una contraseña de almacén de claves, un alias de clave de firma y una contraseña de alias de clave de firma.

Siga los pasos que se indican a continuación para firmar el archivo .aab:

Ejecute el siguiente comando:

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>**[!UICONTROL jarsigner]** se incluye con Java. Asegúrese de que utiliza Java 21.

Cuando se le solicite, introduzca las siguientes contraseñas:

* Contraseña de almacén de claves
* contraseña para el alias de clave de firma

Puede utilizar el apk proporcionado. Sin embargo, si necesita generar un apk a partir de un archivo aab, siga estos pasos:

>[!NOTE]
>
>Deberá instalar **[!UICONTROL bundletool]** para generar APK.


Ejecute el siguiente comando para crear el archivo APK:

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Para descomprimir el archivo, ejecute el siguiente comando:

```
unzip my_app.apks -d output_dir
```

El archivo APK se obtendrá de la carpeta **[!UICONTROL output_dir]**.

**Lo que está por llegar**

Después de generar los archivos binarios, muévalos a Play Store o App Store.

### Envío de las aplicaciones a la tienda para su revisión

Después de obtener los archivos binarios finales, puede cargarlos en las tiendas de aplicaciones respectivas (iOS o Android) para su revisión. Siga estos pasos para cargar los archivos binarios en las tiendas de aplicaciones.

**iOS**

1. Inicie sesión en la aplicación Transporter con sus credenciales de App Store.
2. Seleccione el botón **+** en la parte superior izquierda y cargue el certificado de producción (archivo .ipa).
3. Si el archivo .ipa es correcto, se le pedirá que cargue la aplicación en App Store.
4. Una vez entregada la aplicación, inicie sesión en App Store. Dentro de unas horas, el binario aparecerá en la sección TestFlight. Puede habilitarla para la prueba de corrección final en TestFlight antes de la revisión de la aplicación y usar este IPA como binario al enviar la aplicación para una nueva versión.

**Android**

1. Abra la consola de Google Play Store.
2. Ve a **[!UICONTROL Panel]** > **[!UICONTROL Ver versiones de aplicaciones]** > **[!UICONTROL Panel de lanzamiento]** y, a continuación, selecciona **[!UICONTROL Crear nueva versión]**.
3. Cargue el archivo .aab generado como el paquete de la aplicación y escriba los detalles de la versión, como el número de versión y la información nueva.
4. Guarde los cambios y envíe la aplicación para su revisión.
5. Asegúrese de establecer la distribución de la aplicación en 100 % (Google la establece en 20 % de forma predeterminada).

#### Vínculos útiles para la publicación de aplicaciones

**Android**

[Crear y configurar la aplicación](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en)
[Preparar la aplicación para su revisión](https://support.google.com/googleplay/android-developer/answer/9859455?sjid=2454409340679630327-AP)

**iOS**

[Enviar para revisión](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review)

## ¿Cómo puedo aplicar los cambios?

Envía los activos y archivos necesarios al equipo de CSM. A continuación, el equipo de CSM rellena el [formulario](https://forms.office.com/r/bJRRaRBvSh) con los cambios necesarios y adjunta los activos necesarios. A continuación, el equipo examinará los cambios e informará a los equipos de ingeniería al respecto. A continuación, el equipo de ingeniería generará una compilación y la compartirá con el equipo de CSM.

El equipo de CSM compartirá la compilación con el cliente.

## Qué no se puede personalizar

* Pantalla Actualizar contraseña
* Pantalla Crear una cuenta
