---
description: Obtenga información sobre cómo el informe de seguimiento de auditoría del administrador realiza un seguimiento de los cambios de configuración, mostrando quién los ha realizado, cuándo y los valores anteriores y posteriores.
jcr-language: en_us
title: Informe de seguimiento de auditoría de administrador
exl-id: 71b2ee42-ef1c-47fb-95ad-c339562e227d
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%
---

# Informe de seguimiento de auditoría de administrador {#adminaudittrailreport}

Genere un informe de los cambios de configuración realizados en los ajustes Básico, Avanzado e Integración de la cuenta, incluidos el usuario que ha realizado cada cambio, el momento y el valor anterior y posterior.

## Qué captura el informe

El informe de seguimiento de auditoría del administrador proporciona un registro histórico de los cambios de configuración para que pueda determinar:

- Quién hizo el cambio
- Cuando se realizó el cambio
- Cuál era el escenario antes del cambio
- Cuál es el ajuste después del cambio

El informe abarca los cambios realizados en:

- Configuración de **Conceptos básicos**
- Configuración **avanzada**
- Configuración de **integraciones**

El informe es solo aditivo: los nuevos registros de cambios se añaden con el tiempo y las entradas grabadas anteriormente nunca se eliminan. Esto le permite revisar el historial completo de una configuración en varios cambios, no solo su valor actual.

El informe está disponible para cualquier usuario con privilegios de Informe y acceso completo a grupos de usuarios. Esto incluye administradores completos y administradores personalizados a los que se haya concedido acceso al informe.

>[!NOTE]
>
>Los registros están disponibles a partir de la actualización 112 de septiembre de 2026. Los cambios realizados antes de esta actualización no se incluyen en el informe. Consulte [notas de la versión](/help/migrated/release-note/release-notes.md) Actualización 12.

## Por qué este informe es importante para el cumplimiento

Las organizaciones que operan en los sectores regulados a menudo necesitan demostrar que los cambios de configuración de los sistemas que gestionan registros electrónicos son objeto de seguimiento, atribuibles y conservados. El informe de seguimiento de auditoría del administrador admite estos requisitos al identificar los valores de persona, configuración, tiempo y antes y después de cada cambio.

>[!NOTE]
>
>Este informe respalda las actividades de cumplimiento de su organización. No certifica por sí mismo el cumplimiento de ningún reglamento o norma específicos.

## Generar un informe de seguimiento de auditoría de administrador

1. Inicie sesión en Adobe Learning Manager como administrador.
2. En la barra de navegación izquierda, seleccione **Administrar** > **Informes** > **Informes personalizados**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report1.png)

3. Desplácese hacia abajo y seleccione **Seguimiento de auditoría del administrador**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report2.png)

4. **Seleccionar intervalo**: elija el período del que desea informar: **Última semana**, **Último mes** o **Elegir fechas**. Si selecciona **Elegir fechas**, escriba una fecha **Desde** y una fecha **Hasta**.
5. **Seleccionar tipo de configuración**: elige **Seleccionar todo**, **Aspectos básicos**, **Integraciones** o **Avanzado**.

   Para ver la lista completa de configuraciones de las que se realiza un seguimiento en este informe en Básico, Integraciones y Avanzado, seleccione **Descargar lista de configuraciones**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report6.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report3.png)

6. Seleccione **Generar**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report4.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report5.png)

Un archivo `.csv` que contiene los cambios se descarga en la carpeta Descargas del explorador. La generación de informes puede tardar unos minutos: puede seguir utilizando Adobe Learning Manager mientras se procesa. Si cierra la ventana del navegador antes de que el informe esté listo, la descarga comenzará la próxima vez que inicie sesión.

## Usos comunes de este informe

- **Investigar un cambio de configuración inesperado**: confirma qué ha cambiado, cuándo y quién lo ha hecho, en lugar de confiar en las suposiciones.
- **Revisar los cambios realizados por varios administradores**: genera una vista consolidada de todas las actividades de configuración que están en el ámbito del informe durante un período determinado, en lugar de ponerse en contacto con cada administrador individualmente.
- **Confirmar un cambio de configuración aprobado**: verifique que el administrador esperado haya realizado el cambio dentro del período de tiempo esperado y que el nuevo valor coincida con el aprobado.
- **Comparar el historial de una configuración con varios cambios**: usa la columna **Revisión** para ver cuántas veces ha cambiado una configuración específica y revisa cada valor grabado en secuencia, incluso si un cambio posterior restauró uno anterior.
- **Admitir una revisión del cumplimiento**: genera el informe para el período que se examina como parte de tus registros administrativos y de cumplimiento.
- **Revisar la configuración después de un cambio de directiva**: confirme que las actualizaciones de configuración previstas se aplicaron de manera coherente e identifique los cambios que se produjeron inesperadamente.
- **Mantener un registro administrativo histórico**: descarga y conserva informes según las prácticas de administración de registros de tu organización.

## Referencia de columna de informe

El archivo `.csv` descargado incluye las siguientes columnas.

| Columna | Descripción |
|---|---|
| **Id. de evento** | Un identificador único para este registro de cambios específico. |
| **Marca de tiempo (UTC)** | La fecha y hora en que se realizó el cambio, en Hora universal coordinada. |
| **Correo electrónico** | La dirección de correo electrónico del administrador que realizó el cambio. |
| **UUID** | Un identificador único para el administrador que realizó el cambio. Solo se rellena si UUID está activado en el nivel de cuenta. |
| **Nombre de administrador** | El nombre para mostrar del administrador que realizó el cambio. |
| **Tipo de evento** | La categoría de evento registrada, por ejemplo `Modify`, `Create` o `Delete`. |
| **Tipo de acción** | Tipo de acción realizada en la configuración; por ejemplo, `CREATE_SETTING`, `UPDATE_SETTING` o `DELETE_SETTING`. |
| **Tipo de objeto** | Objeto de configuración o de configuración que se cambió. |
| **Id. de objeto** | El identificador único del objeto de configuración o configuración específico que se ha cambiado. |
| **Valor anterior** | El valor de la configuración antes del cambio. (Para una configuración eliminada, muestra el valor que existía antes de la eliminación). |
| **Nuevo valor** | El valor de la configuración después del cambio. (Para una configuración eliminada, esta opción está en blanco). |
| **Revisión** | El número de veces que se ha cambiado este identificador de objeto específico cuando se registra el evento. El primer cambio registrado para un objeto comienza en 1. |

>[!TIP]
>
>Para buscar todas las configuraciones eliminadas durante un periodo, filtre el archivo descargado donde **Tipo de acción** es `DELETE_SETTING`.

## Acceder a este informe mediante programación

Puede recuperar el informe de seguimiento de auditoría de administrador mediante programación mediante la API de trabajos, en lugar de generarlo manualmente desde la aplicación de administración. Esto resulta útil si desea programar exportaciones regulares o alimentar el informe en un sistema de supervisión o alerta descendente. Consulte [Informe de seguimiento de auditoría de administración de la API de trabajos](/help/migrated/api-changes-sep-2026.md#job-api-for-admin-audit-trail-report).

## limitaciones

- **Localización**: El contenido del informe no está localizado. El informe se genera en el idioma predeterminado de la cuenta, independientemente de la configuración regional de la cuenta.
- **Motivo del cambio**: En el informe no se indica por qué se ha realizado un cambio. Conserve por separado cualquier solicitud de cambio, aprobación o justificación empresarial relacionada.

## Prácticas recomendadas

- Seleccione un intervalo de fechas que abarque el cambio sospechoso o planeado.
- Seleccione **Seleccionar todo** cuando no se conozca el área de configuración afectada.
- Compare las columnas **Valor anterior** y **Valor nuevo** de cada entrada.
- Utilice las columnas **Nombre de administrador** y **Marca de tiempo** para correlacionar un cambio con el trabajo aprobado o los registros internos.
- Mantenga la solicitud de cambio, aprobación o justificación empresarial relacionadas por separado cuando su organización requiera una explicación documentada de un cambio.

## Resolución de problemas

**No veo ningún registro antes de una fecha determinada**
Los registros solo están disponibles a partir de la actualización 112 (septiembre de 2026). Los cambios realizados antes de esa actualización no se incluyen en el informe. Consulte [notas de la versión](/help/migrated/release-note/release-notes.md)

**La columna UUID está vacía para algunos o todos los registros**
La columna UUID se rellena solo si UUID está activado en el nivel de cuenta. Si no está habilitada, esta columna no estará presente.

**Tengo una función de administrador personalizada, pero no puedo encontrar este informe**
Confirme que se le han concedido privilegios de informe y acceso completo a grupos de usuarios a su función personalizada. Póngase en contacto con el propietario de la cuenta o con un administrador completo para solicitar este acceso, si es necesario.
