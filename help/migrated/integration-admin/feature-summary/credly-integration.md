---
jcr-language: en_us
title: Con Credibilidad
description: Obtenga más información sobre la integración de Credly con ALM para administrar y compartir insignias externas de la plataforma en varios canales de medios sociales
contentowner: chandrum
exl-id: 168f7ff8-51f5-4962-bf76-af909fc5565b
source-git-commit: f3a0ec693e1a2e75cdad24f91f22a0290d62740d
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Con Credibilidad

[Credly](https://info.credly.com/) es una plataforma de credenciales digitales que permite a los alumnos y organizaciones obtener, compartir y verificar logros profesionales, como insignias o certificaciones. Los alumnos pueden administrar y compartir insignias a través de su perfil de Credly en redes sociales y otros lugares.

## Requisito previo

Configure una cuenta de Creative para su organización. Añada alumnos a Credly con sus ID de correo electrónico en Adobe Learning Manager. Esto permitirá a los alumnos ver las insignias en Credly y Adobe Learning Manager.

## Añadir Credly Connector a Adobe Learning Manager

Siga estos pasos para añadir Credly Connector a Adobe Learning Manager:

1. Inicie sesión como **[!UICONTROL administrador de integración]**.
2. Selecciona **[!UICONTROL Credly]** > **Connect** para agregar el conector **[!UICONTROL Credly]** a Adobe Learning Manager.

   ![](assets/connector-credly.png)
   _Agregar conector de Creative_

3. Escriba **[!UICONTROL Nombre de conexión]**.
4. Escriba **[!UICONTROL ID de organización]** y **[!UICONTROL token de autorización]**.

   >[!NOTE]
   >
   >Cada distintivo de Credly viene con un ID de organización y un token de autorización. Copie estos valores de Credly.

5. Escriba **[!UICONTROL Hostname]** y seleccione **[!UICONTROL Connect]**.

## Migrar insignias desde Credly

El archivo badge.csv de Adobe Learning Manager le permite migrar insignias desde el LMS o sistemas externos existentes. El archivo badge.csv se ha actualizado con dos nuevas columnas:

* externalBadgeId
* externalBadgeProvider

El ID de insignia externo hace referencia al ID de plantilla de insignia en la plataforma Credly y el proveedor de insignias externo es Credly. Agregue estos valores en badge.csv y siga los pasos indicados en el [Manual de migración](https://experienceleague.adobe.com/es/docs/learning-manager/using/integration/migration-manual#migrationprocedure) para migrar el csv.

## Crear una aptitud: administrador

Una vez importada la insignia en Adobe Learning Manager, el administrador puede crearla como aptitud. Para saber cómo crear una aptitud, consulte [Crear y modificar aptitudes](https://experienceleague.adobe.com/es/docs/learning-manager/using/admin/skills-levels).

### Asigne la aptitud/insignia al objeto de aprendizaje: autor

El autor/administrador puede asignar estas insignias de ALM importadas con cuidado a un curso, una ruta de aprendizaje o una certificación (no solo aptitudes). Al consumir estos objetos de aprendizaje, se consigue la insignia y se puede ver en Credly y la aplicación de ALM.

Los alumnos pueden iniciar sesión en Credly y ver las insignias en la plataforma Credly. Desde Credly, pueden compartir las insignias en plataformas externas como LinkedIn y otras redes sociales.
