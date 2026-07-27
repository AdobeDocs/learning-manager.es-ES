---
description: La API de trabajos de informes de usuarios incrementales permite a los administradores exportar solo usuarios cuyos datos hayan cambiado en un intervalo de fechas especificado. Esto elimina la necesidad de exportaciones de usuarios completas y permite una sincronización más eficiente de los registros de usuarios nuevos o actualizados.
jcr-language: en_us
title: Informe de usuarios incrementales (API de trabajos)
source-git-commit: 40c3bcb1b23ad87a502692007f97b3df27b3a7b9
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 1%

---


# Informe de usuarios incrementales (API de trabajos)

## Información general

El Informe incremental de usuarios de Adobe Learning Manager es una nueva función de la API de trabajos que permite a los administradores y desarrolladores de integración exportar solo los usuarios cuyos datos hayan cambiado en una ventana de fecha y hora especificada. En lugar de extraer la lista de usuarios completa cada vez, puede solicitar un sector de destino que cubra solo usuarios nuevos o modificados.

Este documento abarca:

- Por qué existe la creación de informes incrementales y cuándo utilizarla
- Funcionamiento de la función, incluido el modelo de seguimiento de cambios
- La nueva API de trabajos para informes de usuarios incrementales (carga, parámetros, paginación)
- Cómo gestionar cuentas grandes (más de 5 000 000 usuarios)
- Campos con seguimiento y sin seguimiento
- Limitaciones y objetivos no deseados

## Por qué usar informes incrementales

En esta sección se explica la motivación de la función y se debe ayudarle a decidir si las exportaciones incrementales o completas se ajustan mejor a su integración.

## El problema con las exportaciones completas de usuarios

La exportación de usuarios completa actual (tipo de trabajo generateUsers) devuelve cada usuario de una cuenta con cada ejecución. En el caso de las grandes cuentas empresariales, esto crea dos problemas importantes:

| Cliente | Volumen de usuario |
|----------|-------------|
| Cliente A | 2,1 millones de usuarios |
| Cliente B | 7 millones de usuarios |
| Cliente C | Más de 1 millón de usuarios |
| D de cliente | 7,7 millones de usuarios (migración) |


* A estas escalas, la canalización de exportación se ejecuta con un uso de CPU aproximado del 90% mientras se recopilan, procesan y almacenan datos.
* Los paneles descendentes (PowerBI, Salesforce, integraciones personalizadas) vuelven a ingestar registros de usuarios sin cambios en cada ejecución, lo que hace perder ancho de banda y tiempo de procesamiento.
* No hay forma de preguntar &quot;¿qué usuarios han cambiado desde mi última exportación?&quot; utilizando la API actual.

## Cuándo usar informes incrementales

Utilice la exportación incremental cuando necesite mantener sincronizado un sistema externo con los datos de usuario de Adobe Learning Manager. Casos de uso típicos:

* Mantener actualizado un panel de la empresa (PowerBI, Tableau, SFDC) con los cambios del perfil de usuario.
* Alimentando los sistemas de gestión de identidades descendentes con cambios de roles, estados o metadatos.
* Ejecución de canalizaciones de sincronización delta nocturnas u horarias en lugar de recargas completas.
* Reducción de los costes de transferencia de datos y carga de API para cuentas con millones de usuarios.

Utilice la exportación completa (generateUsers) cuando necesite una línea de base autorizada, por ejemplo, en la primera configuración o después de un intervalo prolongado entre sincronizaciones.

| Modo de exportación | Usar cuando... |
|-------------|-----------|
| Exportación completa (generateUsers) | Bootstrap inicial; cuentas con menos de 50 000 usuarios; recuperación tras una ventana de sincronización perdida. |
| Exportación incremental (generateUserIncrementalReport) | Sincronización delta regular; grandes cuentas; canalizaciones que sólo necesitan registros modificados |

## Informe de usuario completo actual

(generateUsers) En esta sección se documenta el informe de usuario de la API de trabajos existente como referencia. Si ya está familiarizado con ella, vaya a la siguiente sección.

## Cómo funciona

El informe CSV de usuarios actuales se envía como un trabajo a través de la API Trabajos. Una canalización Snaplogic selecciona la tarea, ejecuta una consulta MySQL en la base de datos del CAPTIVATE (tablas user, usergroup, usergroup_user) y genera un archivo CSV.

## Filtros disponibles

La carga útil admite tres filtros opcionales:

* `expandMetadata`: pase true para exportar metadatos como una columna independiente.
* `fetchActiveUsers` - Pass true para exportar solo usuarios activos.
* `peerAccountId` : para generar el informe de usuario para una cuenta de igual a igual.

## Columnas CSV

El archivo CSV exportado contiene las siguientes columnas:

```
internalUserID, userEmail, customerDefinedUniqueUserId, name, managerEmail,

userType, state, excludedFromGamification, pointsEarned, profile, roles,

dateCreated, lastLoginDate, dateDeleted, uiLocale, contentLocale,

timeZoneCode, userSource, group, AF_location, AF_login, AF_externalaf,

lastSocialActivityDate
```

## Solicitar carga

Tipo de trabajo: generarUsuarios. Solo función de administrador.

```
{

  "data": {

    "type": "job",

    "attributes": {

      "description": "<description of your choice>",

      "jobType": "generateUsers",

      "payload": {

        "expandMetadata": "<true to export metadata as separate column>",

        "fetchActiveUsers": "<true to export ACTIVE users only>",

        "peerAccountId": "<peerAccountId for peer account report>"

      }

    }

  }

}
```

## limitaciones

* Sin filtrado basado en fechas: cada ejecución exporta a todos los usuarios.
* No factible para grandes cuentas: agotamiento de recursos de canalización por encima de ~1 millón de usuarios.
* Sin capacidad incremental o delta.

## Informe de usuarios incrementales (generateUserIncrementalReport)

En esta sección se documenta la nueva función de informe de usuarios incremental introducida en M46. Este es el tema principal de este documento.

## ¿Qué es una exportación incremental?

Una exportación incremental devuelve sólo los usuarios cuyos datos de seguimiento hayan cambiado en una ventana de fecha y hora de inicio y finalización especificada. El back-end almacena una marca de tiempo modificada por última vez para los campos de seguimiento de cada usuario. Cuando se solicita un informe para una ventana determinada, sólo se incluyen los usuarios cuyo cambio más reciente se incluye en esa ventana.

## Cómo funciona el modelo de control de cambios

Adobe Learning Manager mantiene una marca de tiempo modificada por última vez que se actualiza cada vez que cambia un campo sobre el que se realiza un seguimiento para un usuario.

Cuando se solicita un informe incremental con un valor de start_date_time y end_date_time, el sistema devuelve usuarios cuya última marca de tiempo modificada se encuentra dentro de [start_date_time, end_date_time]. Si un usuario se ha modificado tanto dentro como después de la ventana (es decir, se ha cambiado de nuevo después de end_date_time), ese usuario no se incluye en el informe, ya que su marca de hora de la última modificación ahora está más allá de la ventana.

>[!NOTE]
>
>Esto significa que una exportación incremental captura los usuarios cuyo cambio más reciente se encuentra en la ventana especificada, no todos los usuarios que se vieron afectados en cualquier momento durante la ventana.

## Campos con seguimiento de cambios

Un usuario se incluye en un informe incremental si cambia alguno de los siguientes campos:

| Campo | Notas |
|---|---|
| userEmail | Dirección de correo electrónico del usuario |
| name | Nombre del usuario |
| managerId | La tabla de usuarios almacena managerId. Si el managerId cambia, el campo se marca como cambiado. Si solo cambia el correo electrónico del responsable (mismo managerId), este campo NO se considera cambiado. |
| tipo | Clasificación de usuarios internos o externos |
| state | Activo o eliminado |
| perfil | Asignación de perfil de usuario |
| funciones | Adiciones o eliminaciones de roles |
| uiLocale | Configuración regional de la interfaz de usuario |
| contentLocale | Configuración regional del contenido |
| timeZoneCode | Zona horaria del usuario |
| Campos activos (AF_*) | Todos los campos activos configurados, p. ej. AF_location, AF_login |
| metadatos | Todos los campos de metadatos configurados |

## Campos NO controlados por cambios

Los siguientes campos aparecen en la salida de CSV, pero no activan la inclusión en una exportación incremental cuando cambian:

* excludeFromGamification
* pointsEarned
* lastLoginDate
* dateDeleted
* dateCreated
* userSource
* lastSocialActivityDate

## Formato de salida

El informe de CSV incremental tiene las mismas columnas y el mismo formato que el informe de CSV de usuario completo. Todas las columnas aparecen en el mismo orden, incluidas todas las columnas de campos y metadatos activas, independientemente de los campos que hayan cambiado para los usuarios exportados.

>[!NOTE]
>
>Si se añade un nuevo campo activo o se elimina uno existente, todos los usuarios afectados por ese cambio aparecerán en la próxima exportación incremental. Las nuevas columnas de los nuevos campos activos se anexan al final del informe para que las integraciones existentes incrustadas en la posición de columna no se rompan.

## Nueva API de trabajos para el informe de usuarios incremental

El informe de usuarios incrementales utiliza la API de trabajos para generar un archivo CSV que contenga usuarios cuyos datos de seguimiento hayan cambiado en la ventana de fecha y hora especificada. Para conjuntos de resultados grandes, utilice el mismo modelo de paginación que se describe más adelante en este documento: envíe la misma ventana de fecha en cada solicitud y pase el último userId recibido en la respuesta anterior como fromUserId para recuperar el siguiente fragmento.

## Tipo de trabajo

Tipo de trabajo: generateUserIncrementalReport

## Solicitar carga

```
{

    "data": {

        "type": "job",

        "attributes": {

            "description": "description of your choice",

            "jobType": "generateUserIncrementalReport",

            "payload":{

                 "fullExport": <Pass true to export all users. If fullExport is true, fromDate and toDate are ignored>,

                 "expandMetadata": <Pass true to export metadata as separate columns>,

                 "fromDate": <Start of the change window in ISO format, for example 2020-01-01T18:30:00.000Z>,

                 "toDate": <End of the change window in ISO format, for example 2020-01-31T18:30:00.000Z>,

                 "fromUserId": <For paginated requests, pass the last userId received in the previous response>

            }

        }

   }

}
```

## Parámetros de carga

| Parámetro | Tipo | Descripción |
|---|---|---|
| fromDate | Cadena (ISO 8601) | Obligatorio para la exportación incremental. Inicio de la ventana de cambio. Utilice el formato ISO 8601. |
| toDate | Cadena (ISO 8601) | Obligatorio para la exportación incremental. Fin de la ventana de cambio. Utilice el formato ISO 8601. |
| fromUserId | Cadena | Opcional. Para las solicitudes paginadas, pase el último ID de usuario recibido en la respuesta anterior como fromUserId. Omitir este parámetro para la primera solicitud. |
| expandMetadata | Booleano | Opcional. Si es true, exporta los metadatos como columnas independientes. |

Para la exportación incremental, pase `fromDate` y `toDate` para definir la ventana de cambio. Si el conjunto de resultados es mayor que un fragmento, continúe la paginación enviando los mismos `fromDate` y `toDate` y pasando los últimos `userId` de la respuesta anterior como `fromUserId`. Si fullExport es true, la ventana de fecha se omite y la API genera una exportación de usuario completa.

## Gestión de cuentas grandes (más de 500 000 usuarios)

Los informes de usuario se generan mediante una canalización de plataforma de datos y el resultado se devuelve en fragmentos para admitir cuentas grandes. Si una exportación incremental abarca más de 500.000 usuarios, el informe se pagina.

## Modelo de paginación

Para recuperar todas las páginas de una exportación incremental grande, pase los mismos valores startDateTime y endDateTime en cada solicitud y, además, pase el userId del último usuario recibido en el fragmento anterior como fromUserId. La API devolverá el siguiente conjunto de hasta 500 000 usuarios con un ID de usuario superior al transferido desde el ID de usuario.

## Flujo de trabajo de paginación

Paso 1: Envíe la primera solicitud sin fromUserId.

```
// First request – no fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z"

  }

}
```

Paso 2: Reciba el primer fragmento (hasta 500.000 usuarios). Anote el último userId de la respuesta.

Paso 3: Envíe la siguiente solicitud, pasando la misma ventana de fecha y el último userId de la respuesta anterior como fromUserId.

```
// Subsequent request – pass last userId from previous response as fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z",

    "fromUserId": "<last userId from previous response>"

  }

}
```

Paso 4: Repita el proceso hasta que una respuesta devuelva menos de 500.000 registros, lo que indica que ha llegado a la última página.

| Solicitud | Parámetro fromUserId |
|---|---|
| Primera página | Omitir de userId |
| Segunda página | Pase el último userId de la primera página como fromUserId |
| Tercera página | Pase el último userId de la segunda página como fromUserId |
| ... (continuar) | ... |
| Última página | La respuesta contiene menos de 500.000 registros |

>[!NOTE]
>
>Asegúrese de que `startDateTime` y `endDateTime` sigan siendo idénticos en todas las solicitudes paginadas para una sola ejecución de exportación. Si se cambia la ventana de fecha en mitad de la paginación, se producirán resultados incoherentes.

## limitaciones

El ámbito del informe de usuario incremental es intencionado. Las siguientes funciones están fuera del ámbito:

* No es un informe de auditoría de usuarios: no enumera los campos específicos que han cambiado.
* Sin comparación de valores antiguos/nuevos: el informe muestra solo los valores de campo actuales.
* Sin marcas de tiempo por cambio: no aparece la hora de las modificaciones de campo individuales.
* Sin indicación del número de cambios: un usuario modificado una vez y un usuario modificado diez veces aparecen de forma idéntica en la exportación.
* El formato del informe existente no cambia: la estructura de columnas del archivo CSV es la misma que la del informe completo del usuario.

## Integración de conectores

El informe de usuarios incremental está diseñado para usarse en conectores de Adobe Learning Manager (PowerBI, Salesforce y otros) como reemplazo desplegable para el informe de usuarios completo en canalizaciones de sincronización regulares. Esto permite que los conectores que utilizan actualmente generateUsers migren al modelo incremental sin cambios en el esquema de datos descendente.

Los conectores pueden utilizar el informe incremental para la sincronización delta y volver al informe completo para el inicio o la recuperación.
