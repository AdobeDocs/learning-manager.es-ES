---
description: Importa contenido e imágenes de aprendizaje de Adobe Experience Manager Assets a Adobe Learning Manager y mantén el contenido vinculado actualizado automáticamente.
jcr-language: en_us
title: Integración con AEM Assets
exl-id: cd33c0f2-59df-4f35-a7d9-d7bff6b9ffba
source-git-commit: f6dc1e97076edf812862b80a6ed5931989c660da
workflow-type: tm+mt
source-wordcount: '3447'
ht-degree: 0%
---

# AEM integración de activos

## Información general

Adobe Learning Manager ahora se integra con Adobe Experience Manager Assets as a Cloud Service. Los equipos pueden almacenar contenido e imágenes de aprendizaje en Adobe Experience Manager Assets, importarlos a Adobe Learning Manager y administrar actualizaciones desde un único lugar. Cuando cambia un activo, el contenido vinculado de la biblioteca de contenido se puede actualizar automáticamente, por lo que los autores no necesitan volver a cargar los archivos.

Dado que su organización administra los activos en un único lugar, los autores utilizan archivos actuales aprobados por la marca en lugar de descargar y volver a cargar copias. Adobe Experience Manager Assets también mantiene el historial de versiones de cada archivo, lo que le proporciona un registro de qué versión estaba activa y cuándo.

La instalación es una tarea que se realiza una sola vez y es la parte que necesita más atención. Después de la configuración, la importación de recursos funciona como cualquier otra carga.

>[!NOTE]
>
>Esta integración está disponible para todas las cuentas de Adobe Learning Manager que tengan una licencia de Adobe Experience Manager Assets, incluidas las cuentas de Captivate Prime y Ultimate. La misma documentación se aplica a ambos.

## Quién hace qué

| Función | Lo que hacen |
|---|---|
| Administrador de integración de ALM | Conecta la cuenta y elige la configuración de integración. |
| Administrador de Adobe Admin Console | Asigna la cuenta técnica generada a los perfiles de producto de AEM Assets adecuados. |
| Administrador de ALM | Importa imágenes desde varios lugares mediante la integración. |
| Autor de ALM | Importa contenido e imágenes, y crea cursos. |

Cada función tiene una parte independiente para configurar y utilizar la integración.

## Implementaciones admitidas

| Elemento | Admitido |
|---|---|
| Adobe Experience Manager Assets as a Cloud Service, instancia de autor | Sí |
| Adobe Experience Manager Assets as a Cloud Service, publicación o entrega | No |
| Adobe Experience Manager local | No |

>[!NOTE]
>
>Adobe Learning Manager se conecta a las instancias de autor solo porque los recursos se crean y se administran allí. Publish y las instancias de entrega no forman parte de la integración actual.

## Configurar la integración

Conecte Adobe Learning Manager a Adobe Experience Manager Assets, asigne la cuenta técnica y elija la configuración de actualización.

Este flujo de trabajo es para administradores de integración. Completa cada paso para que las actualizaciones automáticas funcionen para tus autores. La configuración consta de cinco partes: conéctese a su organización de IMS, busque la cuenta técnica, asígnela en Adobe Admin Console, elija su configuración y proporcione acceso a los autores.

### Requisitos previos {#setup-prerequisites}

Debe cumplir todos estos requisitos. La falta de cualquiera de ellos es la razón más común por la que falla una conexión.

* Tiene la función de administrador de integración en Adobe Learning Manager. El flujo de trabajo de conexión sólo está disponible para esta función.
* Es el administrador de la organización de IMS de la organización de Adobe Identity Management System (IMS) que seleccione.
* Tiene acceso a al menos una organización a la que se pueden asociar instancias de AEM Assets con Learning Manager.

Si no es administrador de la organización de IMS, solicite a su administrador de TI que le conceda acceso o que ejecute la conexión con usted.

### Cómo se asigna Adobe Learning Manager a la organización de IMS

Cada cuenta de Adobe Learning Manager se conecta a una organización de IMS (también denominado perfil IMS). Tenga en cuenta lo siguiente cuando planifique su configuración:

* Una organización de IMS puede contener varios programas y entornos, y cada programa puede tener instancias de Adobe Experience Manager Assets. Puede utilizar cualquiera de esas instancias con la cuenta conectada.
* Las instancias de una organización de IMS diferente no se pueden usar con esa cuenta.
* Una organización de IMS vinculada a una cuenta de Adobe Learning Manager no se puede vincular a otra cuenta al mismo tiempo.

>[!NOTE]
>
>Si su empresa tiene más de una organización de IMS, elija la que sea titular de su licencia de Adobe Experience Manager Assets y las instancias que desee que utilicen los autores.

### Conectar con la organización de IMS

1. Inicie sesión en Adobe Learning Manager como **administrador de integración**.
1. Seleccione **Adobe Experience Manager Assets** como tipo de conector.

   ![](assets/aem-assets-integrationstep1.png)

1. Seleccione **Conectar**.

   ![](assets/aem-assets-integrationstep2.png)

1. Inicie sesión con su Adobe ID cuando se le solicite y seleccione la organización de IMS que contiene sus instancias de Adobe Experience Manager Assets.

   ![](assets/aem-assets-integrationstep3.png)

   ![](assets/aem-assets-integrationstep4.png)

A continuación, Adobe Learning Manager verifica su función de administrador de la organización IMS y el acceso a la instancia. Si ambas comprobaciones se superan, vincula su cuenta a la cuenta de IMS ya creada con el ámbito de la API de autor de AEM Assets a la organización de IMS seleccionada y crea una cuenta técnica para su organización. A continuación, se abre la página de descripción general de la conexión y se muestran los detalles técnicos de la cuenta.

### Buscar la cuenta técnica

La cuenta técnica se crea específicamente para su organización. Adobe Learning Manager lo utiliza para leer o escribir con AEM Assets [Open API](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/assets/author/) en segundo plano.

1. Inicie sesión como **Administrador de integración**; abra la página de descripción general de la conexión de **Adobe Experience Manager Assets**.
1. En la sección **Credentials**, busque el **correo electrónico de cuenta técnica**.
1. Copie el correo electrónico técnico de la cuenta. La usarás para encontrar la cuenta en **Adobe Admin Console**.

### Asignar la cuenta técnica en Adobe Admin Console

Añada la cuenta técnica a un perfil de producto para cada instancia de Adobe Experience Manager Assets que desee que utilice Adobe Learning Manager. Por ejemplo, si tiene 10 instancias y solo desea que 6 de ellas funcionen con Adobe Learning Manager, asigne la cuenta a los perfiles de esas 6 instancias.

1. Inicie sesión en **Adobe Admin Console** como administrador de la misma organización de IMS.
2. Seleccione **Productos y servicios** y, a continuación, seleccione **Adobe Experience Manager as a Cloud Service**.

   ![](assets/aem-assets-integration6.png)

3. Seleccione la instancia que desea utilizar con Adobe Learning Manager.

   ![](assets/aem-assets-integration7.png)

4. Abra el perfil de productos que tenga el acceso que necesita Adobe Learning Manager. Por ejemplo, el perfil AEM Administradores.

   ![](assets/aem-assets-integration8.png)

5. Seleccione **Agregar credenciales de API**.

   ![](assets/aem-assets-integration9.png)

6. Busque la cuenta técnica. Conéctelo con el correo electrónico de la cuenta técnica que ha copiado del administrador de integración. La cuenta suele estar al final de la lista.

   ![](assets/aem-assets-integration10.png)

7. Seleccione la cuenta técnica y, a continuación, seleccione **Guardar**.
8. Repita los pasos 3 a 7 para cada instancia que desee utilizar.

Si la lista de credenciales de API del perfil está vacía, la cuenta técnica aún no está asignada. Para obtener más información sobre los perfiles de producto y las credenciales de API, consulte la documentación de Adobe Admin Console.

>[!IMPORTANT]
>
>No omita este paso. Si no asigna la cuenta técnica, los autores podrán seguir importando recursos desde Adobe Experience Manager Assets, pero las actualizaciones automáticas no funcionarán. A continuación, debe actualizar el contenido manualmente.

### Elija la configuración de integración

Después de conectarse, habilite la conexión y elija cómo gestiona Adobe Learning Manager las actualizaciones y las vistas previas.

| Configuración | Qué hace |
|---|---|
| Actualizaciones automáticas | Actualiza los elementos vinculados de la biblioteca de contenido cuando el recurso cambia en Adobe Experience Manager Assets. |
| Actualización a objetos de aprendizaje | También aplica la actualización a los objetos de aprendizaje que utilizan el elemento Biblioteca de contenido. |
| Vínculo de vista previa pública | Crea un vínculo de vista previa del contenido admitido y lo guarda en los metadatos del activo en AEM Assets. |

La actualización de un objeto de aprendizaje es un ajuste secundario de las actualizaciones automáticas. Solo se puede habilitar si las actualizaciones automáticas están habilitadas primero. Si desactiva las actualizaciones automáticas, los autores actualizan el contenido manualmente en la biblioteca de contenido.

>[!IMPORTANT]
>
>Los cambios realizados en estos ajustes, incluida su desactivación, pueden tardar hasta una hora en aplicarse. Lo mismo se aplica después de habilitar la conexión. El retraso no significa que algo esté mal. Espere hasta una hora antes de realizar la prueba.

### Dar acceso a los autores a Adobe Experience Manager Assets {#give-authors-access}

La configuración de la integración no concede a los autores acceso a sus recursos. Cada autor o administrador de Adobe Learning Manager que importe recursos también debe tener acceso a la instancia de autor de Adobe Experience Manager Assets correspondiente.

* Añada autores como usuarios de la instancia de autor de Adobe Experience Manager Assets, en la misma organización de IMS.
* Proporcióneles al menos el acceso que necesitan para examinar y seleccionar activos. El administrador de Adobe Experience Manager decidirá qué funciones y perfiles de producto utilizar.

>[!NOTE]
>
>Conceder este acceso es su responsabilidad como administrador de Adobe Experience Manager. Adobe Learning Manager no prescribe una función específica. Para obtener ayuda sobre usuarios y perfiles, consulte la documentación de Adobe Experience Manager Assets.

### Comprobar la configuración

1. Espere a que transcurra el retraso de configuración descrito anteriormente.
1. Inicie sesión como autor con acceso a la instancia.
1. En la **Biblioteca de contenido**, seleccione **Examinar** y confirme que **AEM Assets** aparece junto a **Dispositivo**.
1. Importe un activo y confirme que importa.
1. Si el activo se reemplaza, es una versión nueva o se vuelve a procesar, se actualiza en unos minutos en la mayoría de los casos o, en casos excepcionales, puede tardar hasta una hora. Si tarda más de una hora, puede volver a procesar el recurso en AEM Assets.

## Importar contenido de Adobe Experience Manager Assets

Importa contenido de aprendizaje e imágenes de Adobe Experience Manager Assets, y crea cursos sobre contenido que se mantenga actualizado.

Este flujo de trabajo es para autores. El administrador de integración debe configurar primero la integración.

### Requisitos previos {#import-prerequisites}

* El administrador de integración ha conectado la cuenta y ha habilitado la conexión.
* Tiene acceso a la instancia de autor de Adobe Experience Manager Assets que contiene sus recursos, en la organización de IMS conectada. El administrador de Adobe Experience Manager concede este acceso. Consulte [Dar acceso a los autores a Adobe Experience Manager Assets](#give-authors-access).

Una vez activada la integración, cualquier opción de carga en Adobe Learning Manager que la admita muestra dos orígenes: Dispositivo y AEM Assets. Esto incluye la biblioteca de contenido y las opciones de carga de imágenes del curso. El dispositivo sigue estando disponible, por lo que puede seguir cargando archivos desde el equipo.

### Desde donde se puede importar

La opción AEM Assets aparece en las ubicaciones de carga compatibles con ella. La carga desde el dispositivo permanece. Puede importar:

* Contenido del módulo de la biblioteca de contenido.
* Imágenes, como imágenes de portada de cursos e imágenes de banners.
* Ayudas de trabajo

Solo aparecen los tipos de archivo admitidos en esa ubicación de carga. Por ejemplo, la opción de imagen de portada solo muestra imágenes. Los tipos admitidos son imágenes (JPEG, PNG, SVG), vídeo (MP4) y documentos (PDF, paquetes SCORM, PowerPoint y Word). Las extensiones de archivo y los límites de tamaño son los mismos que para otras cargas en esa ubicación.

### El contenido y las imágenes se gestionan de forma diferente

| Elemento | Cómo se maneja. |
|---|---|
| Contenido de la biblioteca de contenido | Se copia y se vincula al activo de origen para que pueda actualizarse automáticamente. |
| Imágenes, como imágenes de portadas y banners | Se copian cuando se seleccionan. No están vinculados y no se actualizan automáticamente. |

### Importar contenido a la biblioteca de contenido

1. Abra la **biblioteca de contenido** y agregue contenido.
1. Seleccione **Examinar**.
1. Seleccione **AEM Assets**.
1. Si se le solicita, inicie sesión con su Adobe ID.
1. En la ventana **Adobe Experience Manager Assets**, busque el recurso. Si tiene acceso a más de un repositorio (AEM instancia habilitada con AEM Assets), cambie entre ellos según sea necesario.
1. Seleccione el activo y, a continuación, complete la carga y guarde.
1. Cree el curso con el grupo de contenido.

Tenga en cuenta lo siguiente:

* Los recursos se seleccionan de uno en uno. La importación en bloque y la importación de carpetas no están disponibles y no se puede migrar una biblioteca de contenido existente a Adobe Experience Manager Assets.
* El selector de recursos le permite abrir un recurso en Adobe Experience Manager Assets.
* Adobe Learning Manager no distribuye contenido directamente desde Adobe Experience Manager Assets. Copia cada activo importado y mantiene una copia local.
* El contenido importado se procesa como cualquier otro contenido de Adobe Learning Manager, incluida la transcripción para el Asistente del alumno.

### Añadir ayudas de trabajo

Seleccione archivos de ayudas de trabajo, como PDF y documentos de referencia, en AEM Assets del mismo modo que importa el contenido de la biblioteca de contenido.

### Autores sin acceso

Si un autor no tiene acceso a Adobe Experience Manager Assets para la organización IMS conectada, verá un mensaje sobre su acceso limitado cuando seleccione AEM Assets.

## Mantén el contenido actualizado

Mantenga los elementos de la biblioteca de contenido vinculados actualizados a medida que cambian los recursos en Adobe Experience Manager Assets.

### Cómo funcionan las actualizaciones automáticas

Cuando se activan las actualizaciones automáticas desde la sección Integration Administrator y se asigna la cuenta técnica, Adobe Learning Manager mantiene la biblioteca de contenido sincronizada con Adobe Experience Manager Assets.

1. En **Adobe Experience Manager Assets**, cargue una nueva versión del recurso o restaure una versión anterior.
1. Adobe Experience Manager Assets finaliza el procesamiento del recurso. Si se sustituye el activo, en la mayoría de los casos se actualiza en unos minutos o, en algunos casos excepcionales, puede tardar hasta una hora. Si tarda más de una hora, puede volver a procesar el recurso en AEM Assets.
1. Adobe Learning Manager actualiza los **elementos de biblioteca de contenido** vinculados e incrementa el número de versión.
1. Si **Actualizar a objetos de aprendizaje** está activado, los objetos de aprendizaje que utilizan esos elementos también se actualizan. Tanto los alumnos inscritos actualmente como los futuros recibirán la última versión.
1. Los alumnos obtienen la versión más reciente la próxima vez que inician el contenido. Un alumno que ya tenga abierto el contenido debe cerrarlo y volver a abrirlo.

La actualización no es instantánea. Espere un momento y actualice la biblioteca de contenido para ver el cambio.

### Actualizar contenido manualmente

Si las actualizaciones automáticas están desactivadas o la cuenta técnica no está asignada en Adobe Admin Console, actualice el contenido manualmente:

1. Abra el elemento en la **biblioteca de contenido**.
1. Seleccione el archivo actualizado de **AEM Assets**.
1. Seleccione **Guardar**.

### Cómo se aplican las actualizaciones en las configuraciones regionales

Si varias configuraciones regionales de un elemento de biblioteca de contenido multilingüe utilizan el mismo recurso, al actualizar dicho recurso se actualizan todas esas configuraciones regionales. Las configuraciones regionales que utilizan un recurso diferente no se ven afectadas.

### Cuántos grupos de contenido puede tener un activo

Un solo activo se puede vincular a hasta 10 grupos de contenido.

>[!NOTE]
>
>Planifica tus grupos de contenido teniendo esto en cuenta. Si necesita más de 10 grupos de contenido del mismo origen, use una copia del activo para los grupos adicionales.

## Vista previa de contenido de Adobe Experience Manager Assets

Utilice vínculos de vista previa para revisar contenido de SCORM y HTML sin iniciarlo como alumno.

Si la opción Vínculo de vista previa pública está activada, Adobe Learning Manager crea un vínculo de vista previa para el contenido admitido que se importa a la biblioteca de contenido y lo guarda en los metadatos del recurso en Adobe Experience Manager Assets.

El vínculo de vista previa se crea para estos tipos de contenido:

* SCORM 1.2
* SCORM 2004
* HTML

Para buscar y utilizar el vínculo:

1. En Adobe Experience Manager Assets, abra las propiedades del recurso.
1. En los metadatos, busque el vínculo de vista previa.

   <!-- TODO: The source document says "path to be mentioned here". Add the exact metadata location (confirm with Kranthi). -->

1. Copie el vínculo y péguelo en un navegador para previsualizar el activo.

Cualquier persona que abra los metadatos del activo puede ver y utilizar este vínculo.

>[!NOTE]
>
>El uso de un vínculo de vista previa no cuenta para el uso de la licencia de ALM. Si desactiva el vínculo de vista previa pública, se eliminarán los archivos de vista previa que Adobe Learning Manager creó en Adobe Experience Manager Assets.

## Cuando cambian los activos, el acceso o las conexiones

Entiende cómo la eliminación de un activo, la pérdida de acceso o la desconexión afectan a tu contenido.

### ¿Qué sucede cuando se elimina un activo? {#delete-asset}

Los cursos que ya utilizan el contenido siguen funcionando incluso si elimina el activo de origen. El modo en que la eliminación afecta a la biblioteca de contenido depende de las configuraciones regionales del grupo de contenido.

| Escenario | ¿Qué sucede? |
|---|---|
| Una configuración regional de un grupo de contenido multilingüe utiliza el recurso | Esa configuración regional se elimina. Las otras configuraciones regionales se quedan. |
| El activo es el único que hay detrás de un grupo de contenido | El grupo de contenido se retira. |

Cuando se retira un grupo de contenido:

* Los cursos existentes siguen reproduciendo el contenido copiado.
* No se puede utilizar el grupo de contenido para crear nuevas asociaciones de cursos.
* No puede editar el grupo de contenido.

### ¿Qué sucede si un autor pierde el acceso?

El contenido que el autor ha importado anteriormente sigue funcionando. Sin embargo, el autor no puede importar nuevos recursos desde esa instancia, crear grupos de contenido ni editar grupos de contenido existentes que lo utilicen.

### ¿Qué sucede si te desconectas?

El contenido y las imágenes importados permanecen en Adobe Learning Manager porque son copias. Los vínculos a los recursos de origen están rotos, por lo que el contenido vinculado ya no se actualiza. Los objetos de aprendizaje y los grupos de contenido siguen funcionando.

## Resolución de problemas

**No puedo conectar o no puedo ver el conector**

Asegúrese de que tiene la función de administrador de integración en Adobe Learning Manager.

**La conexión falla aunque sea administrador de la organización de IMS**

Asegúrese de que también tiene acceso a al menos una instancia de Adobe Experience Manager Assets en la organización de IMS seleccionada. Esto puede suceder cuando el equipo de soporte de TI administra la organización, pero no está asignado a los productos de Adobe Experience Manager Assets. Pida al administrador de Adobe Experience Manager que le añada a una instancia y, a continuación, vuelva a conectarse.

**Mi instancia de Adobe Experience Manager Assets no aparece**

Asegúrese de que la instancia pertenece a la organización de IMS vinculada a su cuenta de Adobe Learning Manager y de que es una instancia de autor de Adobe Experience Manager Assets as a Cloud Service.

**No veo AEM Assets como una opción de carga**

Pida al administrador de integración que confirme que la conexión está habilitada y espere hasta una hora después de habilitarla.

**Un autor no puede ver los recursos o no puede importar**

Pida al administrador de Adobe Experience Manager que conceda al autor acceso a la instancia de autor de Adobe Experience Manager Assets en la organización IMS conectada.

**El contenido no se actualizó o el curso muestra contenido antiguo**

1. Confirme que las actualizaciones automáticas estén activadas en la configuración del administrador de integración y dedique tiempo para que el cambio surta efecto.
2. Cerciórese de que la cuenta técnica esté asignada al perfil de producto de la instancia en Adobe Admin Console.
3. Reinicie el contenido. Si sigue mostrando contenido antiguo, actualícelo manualmente.

**Se ha retirado un grupo de contenido**

El recurso de origen se eliminó en Adobe Experience Manager Assets. Consulte [Qué sucede cuando se elimina un activo](#delete-asset).

**El vínculo de vista previa no aparece en los metadatos del recurso**

Confirme que el vínculo de Vista previa pública está activado, que el contenido es SCORM 1.2, SCORM 2004 o HTML y que ha esperado hasta una hora después de activar la opción.

## Integración con AEM Assets: Preguntas frecuentes

**Q. ¿Ofrece ALM contenido de aprendizaje directamente de AEM Assets?**

**A.** No. Copiamos el contenido de AEM Assets a ALM y guardamos una copia local en ALM.

**Q. ¿Qué sucede cuando se actualiza un recurso en AEM Assets?**

**A.** Si la opción Actualización automática está habilitada en ALM, el contenido correspondiente asociado con AEM Assets se actualiza, al igual que la versión.

**Q. ¿Pueden los administradores controlar si AEM actualizaciones pueden llegar automáticamente a los cursos?**

**A.** Sí. Durante la integración, el administrador de integración debe seleccionar Actualización automática y decidir si la actualización también se aplica automáticamente a los objetos de aprendizaje. Según la configuración de la cuenta, la actualización de los objetos de aprendizaje funcionará.

**Q. ¿Pueden los autores seguir cargando archivos desde su equipo?**

**A.** Sí

**Q. ¿Pueden los clientes migrar su biblioteca de contenido de ALM existente a AEM Assets?**

**A.** No. Actualmente no existe ninguna disposición al respecto.

**Q. ¿Se puede importar una carpeta completa de AEM Assets en la biblioteca de contenido?**

**A.** No. Actualmente no existe ninguna disposición al respecto.

**Q. ¿Admite la integración la importación masiva de activos?**

**A.** No, no hay tal provisión a partir de hoy.

**Q. ¿Qué contenido de ALM se puede seleccionar en AEM Assets?**

**A.** Admitimos las mismas extensiones de archivo que admitimos hoy en cada ubicación de carga. Los filtros se aplican cuando el Asesor de contenido de AEM se abre en ese punto de contacto de carga.

**Q. ¿Se comportan de la misma manera los activos de contenido y los activos de imagen?**

**A.** La función de actualización automática solo se aplica a Recursos de contenido, no a ningún otro recurso de ALM.

**Q. ¿Se puede reemplazar una imagen originaria de AEM Assets por un archivo local?**

**A.** Sí

**Q. ¿Qué AEM Assets puede ver un autor de ALM?**

**A.** Un autor de ALM puede ver todas las carpetas y archivos a los que tiene acceso, según sus permisos de usuario en AEM Assets.

**Q. ¿Qué sucede si se elimina el acceso AEM de un autor?**

**A.** El autor no podrá editar ni crear grupos de contenido desde AEM Assets porque ya no tendrá acceso a las instancias de recursos de ese perfil de IMS a través del Asesor de contenido de AEM.

**Q. ¿Qué sucede si la integración de AEM Assets está deshabilitada o desconectada?**

**A.** Los objetos de aprendizaje y los grupos de contenido siguen funcionando, pero la función de actualización automática de esos activos se detendrá y no continuará.

**Q. ¿Es compatible la integración AEM local?**

**A.** No. Solo admite instancias en la nube.

**Q. ¿Puede una cuenta de ALM conectarse a varias cuentas de AEM Assets?**

**A.** La cuenta de ALM se asigna al perfil de IMS y todas las instancias de AEM Assets de ese perfil de IMS se pueden conectar y utilizar. Una vez que el perfil IMS se vincula a una cuenta ALM, ese perfil IMS no se puede vincular a otra cuenta ALM.

**Q. ¿El contenido importado de AEM Assets puede ser utilizado por el Asistente del alumno?**

**A.** Si el contenido importado de AEM Assets se usa para crear un curso, el Asistente del alumno puede hacer referencia a él en conversaciones relevantes.

**Q. ¿Pueden los autores obtener una vista previa de un recurso AEM antes de seleccionarlo?**

**A.** No. La función de previsualización no está disponible antes de seleccionar el recurso, aunque AEM Assets admite la previsualización para algunos formatos de archivo.

**Q. ¿Genera ALM un vínculo de vista previa pública?**

**A.** Sí, solo para archivos SCORM 1.2, SCORM 2004 y HTML. Esto solo es posible cuando el administrador de integración activa la función de previsualización pública.

**Vínculos relacionados:**

* [Administrar contenido en la biblioteca de contenido](/help/migrated/authors/feature-summary/content-library.md)
* [Documentación de Adobe Admin Console](https://experienceleague.adobe.com/es/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
* [Documentación de Adobe Experience Manager Assets](https://experienceleague.adobe.com/es/docs/experience-manager-learn/assets/overview)
