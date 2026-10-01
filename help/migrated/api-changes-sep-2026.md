---
description: Puntos finales de API públicos orientados al alumno para enumerar, recuperar, inscribirse y eliminar rutas de aprendizaje personalizadas en Adobe Learning Manager y puntos finales de API para comprobar si un alumno determinado puede acceder directamente a uno o varios objetos de aprendizaje a través de un catálogo asignado a ellos.
jcr-language: en_us
title: Cambios en la API en septiembre de 2026
source-git-commit: 328d899c05384ff522f7f6413d2a451139f066ee
workflow-type: tm+mt
source-wordcount: '1374'
ht-degree: 3%
---

# Cambios en la API de la versión de septiembre de 2026 de Adobe Learning Manager

## API para comprobar el acceso al catálogo de objetos de aprendizaje

Determine si el alumno actual tiene acceso directo al catálogo de uno o varios objetos de aprendizaje, independientemente de si el alumno ha alcanzado ese contenido a través de una ruta de aprendizaje o certificación.

### Propósito de la API

Cuando un alumno abre una ruta de aprendizaje o una certificación, puede examinar los cursos individuales que contiene, incluso si un curso específico no se le ha asignado directamente a través de un catálogo. Esto es compatible con la detección de contenido: los alumnos pueden explorar el contenido de una ruta de aprendizaje antes de decidir si desean continuar con ella.

Sin embargo, poder ver un curso de esta forma no debería significar automáticamente que el alumno pueda inscribirse en él. La inscripción debe depender de si el alumno tiene acceso directo al catálogo de ese curso específico, no solo acceso indirecto a través de una ruta de aprendizaje contenedora.

Esta API le permite comprobar, para un alumno determinado, si se puede acceder directamente a uno o varios objetos de aprendizaje a través de un catálogo asignado a ellos. Utilice el resultado para controlar la interfaz de usuario relacionada con la inscripción; por ejemplo, para mostrar una opción de inscripción solo cuando se confirma el acceso directo al catálogo, mientras que la propia página del curso se mantiene visible en ambos casos.

### Punto final

`GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs`

| Propiedad | Valor |
|---|---|
| **Ámbito** | Acceso de lectura del alumno |
| **Formato de respuesta** | application/vnd.api+json |

### Parámetros de consulta

| Parámetro | Obligatorio | Tipo | Descripción |
|---|---|---|---|
| ids | Sí | cadena o matriz | Uno o varios ID de objeto de aprendizaje que comprobar. Acepta un único ID o una lista separada por comas. Máximo de 10 ID por solicitud. |

### Ejemplo de solicitud

```
GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs?ids=course%3A2400159%2Ccourse%3A2400160%2Ccourse%3A2400161%2Ccourse%3A2400162
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

>[!NOTE]
>
>Los ID de objeto de aprendizaje deben estar codificados en URL. Los dos puntos de un identificador como course:2400159 se codifican como %3A y la coma que separa varios identificadores se codifica como %2C.

### Ejemplo de respuesta - 200 OK

```json
{
  "course:2400162": false,
  "course:2400161": false,
  "course:2400160": true,
  "course:2400159": true
}
```

| Valor | Significado |
|---|---|
| verdadero | El alumno que realiza la llamada tiene acceso directo al catálogo de este objeto de aprendizaje. |
| falso | El objeto de aprendizaje no está disponible directamente para el alumno que realiza la llamada mediante un catálogo. Es posible que el alumno pueda verlo si se puede acceder a él a través de una ruta de aprendizaje o una certificación a la que tenga acceso. |

### Códigos de respuesta

| Estado | Significado |
|---|---|
| 200 | La solicitud se realizó correctamente. La respuesta contiene un resultado para cada ID solicitado. |
| 400 | Error de solicitud erróneo genérico. Por ejemplo, se proporcionaron más de 10 ID o un ID no estaba bien formado. |
| 401 | A la solicitud le faltan credenciales de alumno válidas o se ha denegado el acceso debido a credenciales no válidas. |

### Ejemplo de respuesta de error

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "Either LO id is blank or not as per public api specification"
  }
}
```

### Utilice esta API en su integración

Un caso de uso común es una página del curso a la que llega un alumno que navega desde una ruta de aprendizaje. Desea que la página del curso en sí siga siendo accesible para su detección, al tiempo que muestra la acción **Inscribir** solo si el alumno tiene acceso directo al catálogo de ese curso.

1. Cuando se cargue la página del curso, llame a este punto final con el ID de objeto de aprendizaje del curso.
2. Si la respuesta devuelve true para ese ID, muestre la opción **Inscribir**.
3. Si la respuesta devuelve false, mantenga la página del curso visible, el título, la descripción y los detalles del curso, pero oculte la opción **Inscribir**.

## API de trabajos para el informe de seguimiento de auditoría de administración {#apiaudittrailreport}

### Propósito de la API

El informe de seguimiento de auditoría del administrador enumera los cambios de configuración realizados en un
Cuenta de Adobe Learning Manager. Por ejemplo, cambios en Conceptos básicos, Integraciones o
Configuración avanzada de la cuenta para un intervalo de fechas determinado. Para generar el informe de seguimiento de auditoría es necesario consultar y agregar registros de cambios de configuración en el intervalo de fechas solicitado y en los tipos de configuración. Según el tamaño del intervalo y el volumen de cambios, esto puede superar los límites de tiempo de una solicitud HTTP síncrona, lo que supone un riesgo de tiempo de espera de cliente o puerta de enlace.

Para evitar esto, el informe se genera de forma asincrónica a través de la API de trabajos genérica:

1. **Crear un trabajo.** El administrador envía una solicitud en la que se especifica el tipo de informe, el intervalo de fechas y los tipos de configuración. La API devuelve un ID de trabajo inmediatamente, sin esperar a que se compile el informe.

2. **Realizar una encuesta en el trabajo.** El administrador recupera periódicamente el trabajo mediante su ID para comprobar su estado. Cuando se completa el trabajo, la respuesta contiene el resultado o una referencia a él.

### URL base y convenciones

| Elemento | Valor |
|---|---|
| Ruta base | `/primeapi/v2` |
| Tipo de contenido | `application/vnd.api+json;charset=UTF-8` (JSON:API) |
| Autenticación | Token de OAuth del portador, con ámbito para un administrador de cuentas |
| Contexto de cuenta | Encabezado `x-acap-account` que identifica la cuenta del administrador de llamada |
| Sondeo | No se exige ningún intervalo fijo; sondear el extremo Obtener estado del trabajo hasta que `status` deje de ser `QUEUED` o `IN_PROGRESS` |

### ID

El trabajo `id` devuelto cuando se crea un trabajo es una cadena opaca (por ejemplo,
`4593`). Devolver siempre el valor exacto de `id` que recibió del archivo creado
respuesta al sondear por estado. Nunca lo construya ni lo analice.

### Ámbitos de autenticación

Cada extremo requiere un token de OAuth que incluya el siguiente ámbito, y el
el usuario que realiza la llamada debe tener la función de administrador de la cuenta:

- `admin:write` crea un trabajo de informe (`ROLE_ADMIN` requerido)
- `admin:read` leyó el estado y el resultado de un trabajo (`ROLE_ADMIN` requerido)

Las solicitudes realizadas por un llamador que no tiene `ROLE_ADMIN` en la cuenta son
rechazada; consulte [Control de errores](/help/migrated/api-changes-sep-2026.md#error-handling)

### Terminales

#### Crear un trabajo de informe de seguimiento de auditoría

`POST /primeapi/v2/jobs`

Crea un trabajo asincrónico que genera un informe de seguimiento de auditoría de cambio de configuración
para el intervalo de fechas y los tipos de configuración especificados. La respuesta regresa inmediatamente
con un recurso de trabajo en el estado `QUEUED`; el propio informe se elabora en el
fondo.

Ámbito: `admin:write`

| Parámetro | En | Obligatorio | Descripción |
|---|---|---|---|
| `jobType` | carrocería | Sí | Debe ser `generateConfigChangeAuditReport` para este informe |
| `payload.fromDate` | carrocería | Sí | Inicio de la ventana de informes, ISO-8601 con desplazamiento, por ejemplo `2026-09-15T00:00:00.000+05:30` |
| `payload.toDate` | carrocería | Sí | Fin de la ventana de informes, ISO-8601 con desplazamiento, por ejemplo `2026-09-23T23:59:59.000+05:30` |
| `payload.settingTypes` | carrocería | Sí | Conjunto de una o varias categorías de configuración que se van a incluir; los valores admitidos son `Basics`, `Integrations` y `Advanced` |

Cuerpo de solicitud de muestra

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "payload": {
        "fromDate": "2026-09-15T00:00:00.000+05:30",
        "toDate": "2026-09-23T23:59:59.000+05:30",
        "settingTypes": ["Basics", "Integrations", "Advanced"]
      }
    }
  }
}
```

Respuesta: `202 Created`. El cuerpo de respuesta es el recurso de trabajo en su
Estado `QUEUED`.

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "QUEUED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

>[!NOTE]
>
>Una ventana de `fromDate`/`toDate` que abarca un intervalo de fechas muy grande, o que
>solicita todos los tipos de configuración para una cuenta con un largo historial de cambios, puede
>el proceso tarda más tiempo. Sondear el punto final Obtener estado del trabajo en lugar de
>suponiendo que el informe esté listo después de un retraso fijo.

#### Obtener el estado de un trabajo de informe de seguimiento de auditoría

`GET /primeapi/v2/jobs/{id}`

Devuelve el estado actual de un trabajo creado anteriormente. Mientras que el trabajo es
aún en ejecución, `attributes.status` es `QUEUED` o `IN_PROGRESS` y
`attributes.result` está ausente. Una vez que finalice el trabajo, `attributes.status` se
`COMPLETED`, con la ubicación del informe en `attributes.result`, o
`FAILED`, con detalles de error en `attributes.error`.

Ámbito: `admin:read`

| Parámetro | En | Obligatorio | Descripción |
|---|---|---|---|
| `id` | path | Sí | Id. de trabajo devuelto cuando se creó el trabajo |

Ejemplo de respuesta mientras el trabajo aún se está ejecutando

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "IN_PROGRESS",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

Muestra de respuesta una vez completado el trabajo

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "COMPLETED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30",
      "dateCompleted": "2026-09-23T18:12:41.000+05:30",
      "result": {
        "downloadUrl": "https://learningmanager.adobe.com/primeapi/v2/jobs/4593/download",
        "expiresAt": "2026-09-24T18:12:41.000+05:30"
      }
    }
  }
}
```

### Esquema de recursos

#### Atributos de trabajo

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | cadena | Id. de trabajo opaco |
| `jobType` | cadena | `generateConfigChangeAuditReport` para este informe |
| `status` | cadena | `QUEUED`, `IN_PROGRESS`, `COMPLETED` o `FAILED` |
| `dateCreated` | cadena (ISO-8601) | Cuando se creó el trabajo |
| `dateCompleted` | cadena (ISO-8601) | Cuando el trabajo haya terminado; presente una vez `status` es `COMPLETED` o `FAILED` |
| `payload` | objeto | Parámetros de solicitud con los que se creó el trabajo (incrustados, consulte a continuación) |
| `result` | objeto | Dónde descargar el informe terminado; presente solo cuando `status` es `COMPLETED` (incrustado, consulte a continuación) |
| `error` | objeto | Detalles del fallo; presente sólo cuando `status` es `FAILED` |

#### Carga útil (incrustada, dentro de la solicitud de creación)

| Campo | Descripción |
|---|---|
| `fromDate` | Inicio de la ventana de informes |
| `toDate` | Fin de la ventana de informes |
| `settingTypes` | Definición de categorías incluidas en el informe: `Basics`, `Integrations`, `Advanced` |

#### Resultado (incrustado, dentro de un trabajo completado)

| Campo | Descripción |
|---|---|
| `downloadUrl` | URL firmada desde la que se puede descargar el informe generado |
| `expiresAt` | Cuando `downloadUrl` deja de ser válido; solicitar una nueva comprobación de estado para obtener un nuevo vínculo después de este tiempo |

### Gestión de errores {#audit-trail-report-error-handling}

Los siguientes códigos se aplican a estos puntos finales:

| Estado HTTP | Código de error | Cuando ocurre |
|---|---|---|
| 400 | `BAD_REQUEST` | `toDate` es anterior a `fromDate`, `settingTypes` está vacío o contiene un valor no admitido, o una fecha no es válida ISO-8601 - crear solo extremo |
| 401 | `UNAUTHORIZED_ACCESS` | Falta el token, no es válido o ha caducado |
| 403 | `FORBIDDEN` | El llamador no tiene `ROLE_ADMIN` en la cuenta |
| 400 | `OBJECT_DOESNT_EXIST` | Obtener por id: el trabajo no existe o el id está mal formado; ambos casos se contraen en la misma respuesta |

Ejemplo de respuesta de error

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "toDate must be on or after fromDate"
  }
}
```

### Utilice esta API en su integración

Un caso de uso común es una acción de &quot;Descargar seguimiento de auditoría&quot; orientada al administrador en el
la pantalla de configuración de cuenta.

1. Cuando el administrador elige un intervalo de fechas y uno o varios tipos de configuración y
confirma, llame al punto final create-job con esos valores.
2. Almacene el trabajo devuelto `id` y sondee el extremo de obtener estado del trabajo en un
intervalo razonable (por ejemplo, cada pocos segundos).
3. Mientras `status` sea `QUEUED` o `IN_PROGRESS`, siga mostrando un estado de progreso
en la IU.
4. Cuando `status` se convierta en `COMPLETED`, use `result.downloadUrl` para permitir que el
administrador descargue el informe antes de que `expiresAt` pase.
5. Cuando `status` se convierta en `FAILED`, muestra `error` al administrador y déjalo
vuelva a intentarlo.
