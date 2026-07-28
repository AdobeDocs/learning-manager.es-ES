---
description: Cambios en la API de ALM
jcr-language: en_us
title: Cambios en la API de la versión de agosto de 2026 de Adobe Learning Manager
source-git-commit: 857c94b5e9a7460d63a6dacc0beeddd41f362bf9
workflow-type: tm+mt
source-wordcount: '3354'
ht-degree: 3%

---


# Cambios en la API de la versión de agosto de 2026 de Adobe Learning Manager

## API de administración de grupos de usuarios en Adobe Learning Manager

Esta versión agrega tres nuevos puntos finales de API públicas con ámbito de administración para administrar grupos de usuarios personalizados mediante programación. Puede crear, cambiar el nombre y eliminar grupos de usuarios personalizados sin usar la aplicación de administración, lo que le permite automatizar la administración de grupos como parte de su identidad o los flujos de trabajo de aprovisionamiento.

Estos puntos finales solo funcionan con grupos de usuarios personalizados. Los grupos administrados por el sistema, como el grupo Todos los usuarios y los grupos de usuarios generados automáticamente, tienen el valor readOnly: true en la respuesta de la API y no se puede modificar ni eliminar a través de estos puntos finales.

Para conocer los requisitos de autenticación de API, consulte [Autenticación de API de Adobe Learning Manager](https://experienceleague.adobe.com/es/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Terminales de API de grupos de usuarios

Los tres puntos finales requieren un token de acceso de administrador con permisos de escritura (ROLE_ADMIN).

| **Método** | **Ruta** | **Operación** | **Código de éxito** |
|---|---|---|---|
| POST | /primeapi/v2/userGroups | Crear un grupo de usuarios personalizado | 201 Creado |
| PUT | /primeapi/v2/userGroups/{id} | Actualizar el nombre o la descripción de un grupo | 200 OK |
| ELIMINAR | /primeapi/v2/userGroups/{id} | Eliminar un grupo de usuarios personalizado | 204 Sin contenido |

## **Encabezados de solicitud comunes**

Los tres puntos finales requieren los siguientes encabezados.

```
Authorization: Bearer \<access-token\>
X-acap-user: \<user-id\>
X-acap-account: \<account-id\>
X-acap-caller-role: ROLE_ADMIN
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### **Crear un grupo de usuarios**

```
POST /primeapi/v2/userGroups
```

Crea un nuevo grupo de usuarios personalizado con una lista inicial de miembros. El grupo está disponible inmediatamente para su uso en la aplicación de administración.

#### **Cuerpo de solicitud**

```
{
  "name": "Marketing Team",
  "description": "Custom user group for marketing onboarding",
  "data": [
    { "type": "user", "id": "11282373" },
    { "type": "user", "id": "11282374" }
  ]
}
```

#### **Parámetros de solicitud**

| **Parámetro** | **Obligatorio** | **Tipo** | **Descripción** |
|---------------|--------------|----------|-------------------------------------------------------------------------------------|
| name | Sí | cadena | Nombre para mostrar del grupo. No debe estar en blanco ni ser solo espacio en blanco. |
| descripción | No | cadena | Descripción opcional del propósito del grupo. |
| datos | Sí | matriz | Lista de miembros inicial. Mínimo 1 artículo, máximo 100 artículos. |
| data[].type | Sí | cadena | Debe ser &quot;usuario&quot;. No se aceptan otros tipos de recursos. |
| data[].id | Sí | cadena | Cadena de ID de usuario numérico. El usuario debe pertenecer a la cuenta y tener el estado ACTIVO. |

> **Nota:** La matriz de datos solo se usa en la creación para establecer la lista de miembros inicial. Para agregar o quitar miembros después de su creación, utilice los puntos finales de pertenencia a grupos de usuarios existentes.

#### **Se creó la respuesta 201**

```
{
  "links": {
    "self": "https://<host>/primeapi/v2/userGroups"
  },
  "data": {
    "id": "2769204",
    "type": "userGroup",
    "attributes": {
      "dateCreated": "2026-06-04T14:19:53.000Z",
      "description": "Custom user group for marketing onboarding",
      "name": "Marketing Team",
      "readOnly": false,
      "userCount": 2
    }
  }
}
```

#### **POST de reglas de validación**

| **#** | **Validación** | **Código de error** | **Desencadenador** |
|-------|-------------------------------------------------------|----------------------------------------------------------|------------------------------------------------|
| 1 | el nombre está presente y no está en blanco | USERGROUP_CREATE_NAME_REQUIRED | Nombre omitido o solo espacio en blanco |
| 2 | los datos contienen al menos 1 usuario | USERGROUP_CREATE_USERS_REQUIRED | datos ausentes o matriz vacía |
| 3 | los datos contienen 100 usuarios o menos | USERGROUP_USERS_MAX_LIMIT_EXCEEDED | Más de 100 entradas en datos[] |
| 4 | Todos los ID de usuario son cadenas numéricas | INVALID_USER_IDS | Se encontró una cadena no numérica en los datos[].id |
| 5 | Todos los usuarios existen en la cuenta y tienen el estado ACTIVO | INVALID_USER_IDS / USERGROUP_CREATE_USERS_NOT_IN_ACCOUNT | Usuario no encontrado o no activo |
| 6 | La cuenta no ha alcanzado el límite de grupos personalizados | 400 | Se ha superado el límite de nivel de cuenta para grupos personalizados |

### **Actualizar un grupo de usuarios**

```
PUT /primeapi/v2/userGroups/{id}
```

Actualiza el nombre o la descripción de un grupo de usuarios personalizado existente. Este extremo no puede agregar ni quitar miembros del grupo.

Puede omitirse cualquiera de los campos; Si se omite un campo, su valor actual no cambia. Si se pasa null para la descripción, se borra. Se rechaza pasar una cadena en blanco para el nombre.

#### **Cuerpo de solicitud**

```json
{
  "name": "Updated Group Name",
  "description": "Updated description text"
}
```

#### **Parámetros de solicitud**

| **Parámetro** | **Obligatorio** | **Tipo** | **Descripción** |
|---------------|--------------|----------|---------------------------------------------------------------------------|
| name | Sí | cadena | Nuevo nombre para mostrar. No debe estar en blanco si se proporciona. Omitir para dejar sin cambios. |
| descripción | No | cadena | Nueva descripción. Pase null para borrar. Omitir para dejar sin cambios. |

#### **Respuesta 200 correcta**

```
{
  "data": {
    "type": "userGroup",
    "id": "2767870",
    "attributes": {
      "name": "Updated Group Name",
      "description": "Updated description text",
      "readOnly": false,
      "state": "Active",
      "userCount": 3
    }
  }
}
```

#### **PUT de reglas de validación**

| **#** | **Validación** | **Código de error** | **Desencadenador** |
|-------|-------------------------------------|----------------------------------------|----------------------------------------------------------|
| 1 | los datos son nulos o están ausentes | USERGROUP_UPDATE_USERS_NOT_ALLOWED | El autor de la llamada pasó datos no nulos al intentar cambiar la pertenencia |
| 2 | El nombre, si se proporciona, no está en blanco | USERGROUP_UPDATE_NAME_BLANK | nombre enviado como cadena de solo espacio en blanco |
| 3 | El grupo existe en esta cuenta | INVALID_USER_GROUP_ID | Parámetro de ruta de acceso {id} desconocido |
| 4 | El grupo aún no se ha eliminado | DELETED_USERGROUP | El grupo se eliminó anteriormente |
| 5 | Group readOnly es false | READ_ONLY_USERGROUP | Grupo administrado por el sistema |
| 6 | El grupo es un tipo personalizado (no de sistema) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Tipo de grupo interno del sistema |

### **Eliminar un grupo de usuarios**

```
DELETE /primeapi/v2/userGroups/{id}
```

Marca el grupo de usuarios personalizado especificado como eliminado. El registro del grupo no se elimina permanentemente: su estado se establece en DELETED, lo que lo hace invisible en la aplicación de administración y no apto para su uso en nuevas configuraciones. El ID de grupo no se puede reutilizar.

#### **Ejemplo de solicitud**

```
DELETE /primeapi/v2/userGroups/2767870
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_ADMIN
```

#### **Respuesta 204 Sin contenido**

El cuerpo de la respuesta está vacío.

> **Nota:** El DELETE no es idempotente. Al enviar una segunda solicitud de DELETE al mismo ID de grupo, se devuelve un error 400 con el código DELETED_USERGROUP, no 204. Trate una respuesta 400 DELETED_USERGROUP como confirmación de que el grupo ya se ha eliminado. No se admite la eliminación en bloque; cada grupo requiere una solicitud de DELETE independiente.

#### **DELETE de reglas de validación**

| **#** | **Validación** | **Código de error** | **Desencadenador** |
|-------|-------------------------------------|----------------------------------------|---------------------------------------------------|
| 1 | El grupo existe en esta cuenta | INVALID_USER_GROUP_ID | Parámetro de ruta de acceso {id} desconocido |
| 2 | El grupo aún no se ha eliminado | DELETED_USERGROUP | Repetir DELETE en un grupo que ya tiene el estado ELIMINADO |
| 3 | Group readOnly es false | READ_ONLY_USERGROUP | Grupo administrado por el sistema |
| 4 | El grupo es un tipo personalizado (no de sistema) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Tipo de grupo interno del sistema |

## API de aprendizaje externo en Adobe Learning Manager

Esta versión añade cinco nuevos puntos finales de API con ámbito de alumno para la función de aprendizaje externo. Estos puntos finales permiten a los alumnos crear, recuperar y actualizar envíos de aprendizaje externos mediante programación, por ejemplo, desde una aplicación móvil, un sistema de recursos humanos integrado o un portal de aprendizaje personalizado.

El flujo de trabajo de aprendizaje externo a través de la API refleja el flujo de trabajo en la aplicación del alumno: un alumno envía detalles de formación y un documento de prueba opcional, su responsable directo recibe una notificación para revisar el envío y, tras la aprobación, el registro aparece en la transcripción del alumno.

Los cinco puntos finales tienen el ámbito del alumno. Un alumno solo puede acceder a sus propios envíos. La API devuelve un error si un alumno intenta acceder a los datos de otro alumno.

Para conocer los requisitos de autenticación de API, consulte [Autenticación de API de Adobe Learning Manager](https://experienceleague.adobe.com/es/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Terminales de API de aprendizaje externo

Todos los puntos finales requieren un token de acceso de alumno (ROLE_LEARNER).

| **Método** | **Ruta** | **Operación** | **Código de éxito** |
|------------|---------------------------------------|----------------------------------|------------------|
| GET | /primeapi/v2/externalLearningSettings | Obtener configuración del formulario de cuenta | 200 OK |
| GET | /primeapi/v2/externalLearnings | Enumerar los envíos del llamador | 200 OK |
| GET | /primeapi/v2/externalLearnings/{id} | Obtener un único envío | 200 OK |
| POST | /primeapi/v2/externalLearnings | Crear un nuevo envío | 201 Creado |
| PUT | /primeapi/v2/externalLearnings/{id} | Actualizar un envío pendiente | 200 OK |

### Encabezados de solicitud comunes

```
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_LEARNER
Accept: application/vnd.api+json
Content-Type: application/vnd.api+json (POST and PUT only)
```

### Ciclo de vida del estado de envío

| **Estado** | **Establecido por** | **Significado** | **¿Puede actualizar el alumno?** |
|------------|------------------|-----------------------------------------|-----------------------------|
| PENDIENTE | Sistema al crear | Esperando revisión del administrador | Sí, a través del PUT |
| APROBADO | Responsable | Aceptado; aparece en transcripciones de alumnos | No- PUT devuelve 409 |
| RECHAZADO | Responsable | Rechazado; comentario de revisión adjunto | No: crear un nuevo envío |

APROBADO y RECHAZADO son estados finales. No se puede volver a abrir una presentación rechazada; el alumno debe crear un nuevo envío.

### Obtener configuración del formulario de cuenta

```
GET /primeapi/v2/externalLearningSettings
```

Devuelve la configuración de formulario de nivel de cuenta. Llame a este punto final antes de procesar un formulario de envío. La respuesta define qué campos mostrar, cuáles son obligatorios, sus tipos de datos y los campos personalizados configurados por el administrador.

Compruebe el atributo habilitado de nivel superior antes de continuar; si es falso, la función Aprendizaje externo no está activa para esta cuenta y los puntos finales de envío devolverán errores.

#### Respuesta 200 OK

```
{
  "data": {
    "id": "8627",
    "type": "externalLearningSettings",
    "attributes": {
      "enabled": true,
      "updatedAt": "2026-06-05T06:51:20.000Z",
      "coreFields": [
        { "id": "title", "type": "TEXT", "mandatory": true, "editable": false, "order": 0 },
        { "id": "description_notes", "type": "TEXT", "mandatory": false, "editable": true, "order": 1 },
        { "id": "date", "type": "TIMESTAMP", "mandatory": false, "editable": true, "order": 2 },
        { "id": "score", "type": "NUMBER", "mandatory": true, "editable": true, "order": 3 },
        { "id": "duration", "type": "TEXT", "mandatory": false, "editable": true, "order": 4 },
        { "id": "attachments", "type": "FILE_UPLOAD", "mandatory": true, "editable": true, "order": 5 }
      ],
      "customFields": [
        {
          "id": "960369b2-...",
          "type": "NUMBER",
          "mandatory": true,
          "order": 0,
          "label": { "en_US": "Employee Code" }
        },
        {
          "id": "3c6cc6d9-...",
          "type": "DROPDOWN",
          "mandatory": true,
          "order": 1,
          "label": { "en_US": "Department" },
          "options": [
            { "option_id": "opt_1", "label": { "en_US": "IT" } },
            { "option_id": "opt_2", "label": { "en_US": "HR" } },
            { "option_id": "opt_3", "label": { "en_US": "FIN" } }
          ]
        }
      ]
    }
  }
}
```

#### Referencia de campo principal

| **Id. de campo** | **Tipo** | **Obligatorio predeterminado** | **Notas** |
|-------------------|-------------|-----------------------|----------------------------------------------------------------------------------------------------------|
| título | TEXTO | Sí | Nombre del curso. Siempre presente. El administrador no puede deshabilitarlo. |
| description_notes | TEXTO | No | Descripción o notas de texto libre. |
| anuncio | MARCA DE TIEMPO | No | Intervalo de fecha Forma del valor: { &quot;start_date&quot;: &quot;<ISO-Z>&quot;, &quot;end_date&quot;: &quot;<ISO-Z>&quot; }. Cualquiera de los valores puede ser nulo. |
| puntuación | NÚMERO | Sí | Forma del valor: { &quot;managed_score&quot;: <number>, &quot;max_score&quot;: <number> }. Ambos valores deben ser numéricos. |
| duración | TEXTO | No | Cadena de forma libre, por ejemplo &quot;40 horas&quot;. |
| archivos adjuntos | FILE_UPLOAD | Sí | Prueba de finalización. **No** se pasó dentro de los campos[]; en su lugar, use el atributo submitUrl de nivel superior. |

El administrador define los campos personalizados y los devuelve en customFields[]. Sus ID, tipos, indicadores obligatorios, etiquetas y opciones desplegables varían según la configuración de la cuenta.

### Envío de listas

```
GET /primeapi/v2/externalLearnings
```

Devuelve una lista paginada de los envíos propios del alumno autenticado, ordenados por modificadoEn descendente (el último modificado primero).

#### **Parámetros de consulta**

| **Parámetro** | **Predeterminado** | **Máximo** | **Descripción** |
|---------------|-------------|-------------|-------------------------------------------------------------------------------------------------------|
| page[offset] | 0 | 5000 | Desplazamiento de registro basado en cero. |
| page[limit] | 10 | 100 | Registros por página. Los valores por encima de 100 se fijan de forma silenciosa en 100. |
| ls_qp_status | — | — | Filtrar por estado. Omitir para todos los resultados. Valores válidos: PENDIENTE, APROBADO, RECHAZADO (sin distinción de mayúsculas y minúsculas). |

#### **Respuesta 200 correcta**

```
{
  "links": {
    "next": "/primeapi/v2/externalLearnings?page[offset]=10&page[limit]=10"
  },
  "data": [
    { "id": "1001", "type": "externalLearning", "attributes": { "status": "PENDING", ... } },
    { "id": "1002", "type": "externalLearning", "attributes": { "status": "APPROVED", ... } }
  ]
}
```

### Obtener un envío

```
GET /primeapi/v2/externalLearnings/{id}
```

Devuelve el registro completo de un único envío que pertenece al alumno autenticado.

#### **Respuesta 200 OK

```
{
  "data": {
    "id": "1001",
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "https://<cdn-url>/cert.pdf",
      "title": "Java Fundamentals Certification",
      "status": "PENDING",
      "creationSource": "LEARNER",
      "createdAt": "2026-04-14T08:30:00.000Z",
      "modifiedAt": "2026-04-16T11:45:00.000Z",
      "fields": [ "...resolved against live settings..." ]
    },
    "relationships": {
      "reviewerUser": { "data": null }
    }
  }
}
```

### Crear un envío

```
POST /primeapi/v2/externalLearnings
```

Crea un nuevo envío de aprendizaje externo en estado PENDIENTE. Se deben incluir todos los campos obligatorios definidos en la configuración de la cuenta. Después de que el POST sea un éxito, el responsable del alumno recibe una notificación en la plataforma para revisar el envío.

### **Carga de archivo**

El campo de datos adjuntos se gestiona por separado de los demás campos. No lo incluya dentro de los campos []. En su lugar:

&#x200B;1. Obtenga una URL de carga S3 firmada previamente desde el punto final de carga del archivo ALM.

&#x200B;2. Cargue el archivo en esa URL.

&#x200B;3. Pase la dirección URL resultante como el atributo submitUrl de nivel superior en la solicitud del POST.

#### **Cuerpo de solicitud**

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<pre-signed-upload-url>",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals Certification" },
        { "id": "description_notes", "type": "TEXT", "value": "Completed via online course platform." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": "2026-05-01T00:00:00.000Z", "end_date": "2026-05-15T00:00:00.000Z" } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 88, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "40 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1225" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_3" }
      ]
    }
  }
}
```

#### Formas de valor de campo

| **Tipo de campo** | **Forma de valor** | **Ejemplo** |
|----------------|---------------------------------------------------------|----------------------------------------------------------------|
| TEXTO | Cadena | &quot;Fundamentos de Java&quot; |
| NÚMERO | Objeto con puntuación_conseguida y puntuación_máxima | { &quot;managed_score&quot;: 8, &quot;max_score&quot;: 100 } |
| MARCA DE TIEMPO | Objeto con fecha_inicial y fecha_final (ISO 8601 o nulo) | { &quot;start_date&quot;: &quot;2026-05-01T00:00:00.000Z&quot;, &quot;end_date&quot;: null } |
| MENÚ DESPLEGABLE | option_id cadena de configuración de cuenta | &quot;opt_3&quot; |
| FILE_UPLOAD | No se permite dentro de los campos [] — use submitUrl | — |

#### POST de reglas de validación

| **#** | **Validación** | **Desencadenador** |
|-------|-----------------------------------------------------------------|----------------------------------------------------------|
| 1 | El aprendizaje externo está habilitado para la cuenta | Indicador de función desactivado |
| 2 | Todos los campos obligatorios están presentes en los campos [] | Campo obligatorio omitido |
| 3 | Cada forma de id. de campo, tipo y valor coincide con la configuración de la cuenta | Tipo incorrecto u objeto de valor con formato incorrecto |
| 4 | El tipo FILE_UPLOAD no está presente en los campos [] | Datos adjuntos enviados dentro de campos[] en lugar de submitUrl |
| 5 | submitUrl es una dirección URL firmada previamente S3 válida | URL de CDN y URL no S3 rechazadas en el momento de la creación |
| 6 | submitUrl presente cuando attachments.required es true | Los archivos adjuntos son obligatorios, pero falta submitUrl |

### Actualizar una presentación

```
PUT /primeapi/v2/externalLearnings/{id}
```

Actualiza un envío PENDIENTE existente. Solo se pueden actualizar los envíos PENDIENTES. Al intentar enviar un PUT de un envío APROBADO o RECHAZADO, se devuelve un error 409.

**Este extremo usa semántica de reemplazo completo.** Proporcione la matriz completa de campos [] en cada solicitud de PUT, no solo los campos que está cambiando. Los campos omitidos de la matriz se borran.

#### Campos que el alumno puede actualizar

| **Campo / atributo** | **El alumno puede actualizar** | **Notas** |
|-----------------------|------------------------|----------------------------------------------------------------------------|
| fields[] | Sí | Reemplazo completo: incluya todos los campos, no solo los modificados |
| submitUrl | Sí | Las URL de CDN se aceptan en el PUT; Las direcciones URL prefirmadas de S3 solo son necesarias en el POST |
| reviewerUserId | No | Establecer por acción del administrador; de solo lectura para el alumno |
| revisadoEn | No | Establecer por acción del administrador; de solo lectura para el alumno |
| reviewerComment | No | Establecer por acción del administrador; de solo lectura para el alumno |
| el estado del objeto | No | Controlada por el responsable: PENDIENTE → APROBADO o RECHAZADO |
| creationSource | No | Always LEARNER para envíos creados mediante API |
| createdAt | No | Establecer en tiempo de creación; inmutable |

#### Cuerpo de la solicitud

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<cdn-url>/cert-v2.pdf",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals — Updated" },
        { "id": "description_notes", "type": "TEXT", "value": "Updated notes." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": null, "end_date": null } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 92, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "42 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1227" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_2" }
      ]
    }
  }
}
```

## API para ID de certificación relevante para el alumno e ID de certificación raíz en LT

Cuando se renueva una certificación periódica, Adobe Learning Manager crea una nueva versión de la certificación e inscribe automáticamente en ella a los alumnos activos. Si su integración consulta datos de certificación directamente en lugar de basarse en la experiencia del alumno de Adobe Learning Manager, puede utilizar esta API para determinar exactamente qué versión de una certificación periódica es relevante para un alumno específico en cualquier momento.

### Propósito de la API

Las certificaciones periódicas generan un nuevo ID de certificación cada vez que se renuevan. En la experiencia del alumno nativo de Adobe Learning Manager, solo se muestra la versión relevante para cada alumno. Las versiones anteriores se ocultan automáticamente una vez que un alumno se mueve a una más reciente.

Si su integración recupera datos de certificación de forma independiente, por ejemplo, para mostrar información de certificación en un portal externo, es posible que no aplique automáticamente este filtrado. Sin ella, un alumno podría ver todas las versiones históricas de una certificación recurrente, incluidas las que ya no son relevantes para él, sin indicar con qué actuar.

Esta API corrigió esa brecha. Dado el ID de certificación raíz, devuelve la versión de certificación específica que se aplica a un alumno determinado, teniendo en cuenta su historial de inscripción y cualquier repetición.

### Comprender la periodicidad de certificaciones

Cuando se configura una certificación para que se repita, cada renovación crea una nueva versión de certificación con su propio ID único. Todas las versiones se remontan a un único **ID de certificación raíz,** el ID de la certificación original cuando se creó por primera vez.

Por ejemplo, una certificación que se repite cada mes podría producir una secuencia de versiones a lo largo del tiempo, donde cada nueva versión se genera automáticamente cuando se alcanza el intervalo de periodicidad. Los alumnos que se inscriben activamente cuando se produce una repetición se inscriben automáticamente en la nueva versión.

Dado que cada versión tiene un ID distinto, la versión relevante de un alumno depende de su calendario de inscripción individual:

- Un alumno que se inscribió antes de una repetición y completó su certificación antes de que tuviera lugar la siguiente repetición habrá pasado por varias versiones a lo largo del tiempo.

- Un alumno que se inscribe a lo largo de un ciclo de periodicidad se inscribe directamente en la versión que esté en vigor en el momento de inscribirse.

### Determinar la versión de certificación correspondiente

Utilice la API de la versión de certificación para identificar qué versión de una certificación periódica es relevante para un alumno específico.

Proporcione el **ID de certificación raíz** como entrada. La API evalúa el historial de inscripción del alumno y devuelve la versión adecuada en función de las siguientes reglas:

| **Estado del alumno** | **Lo que devuelve la API** |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| El alumno aún no se ha inscrito en la certificación | La última versión disponible de la certificación |
| El alumno está inscrito actualmente | La versión específica en la que está inscrito el alumno actualmente, teniendo en cuenta las repeticiones que se hayan producido desde su inscripción original |

Esto significa que dos alumnos que consulten el mismo ID de certificación raíz al mismo tiempo pueden recibir resultados diferentes, en función del historial de inscripción individual de cada alumno.

**Nota**: Puede haber una breve ventana durante una repetición, mientras se crea la nueva versión y se migran las inscripciones, en la que la API puede devolver la versión que está a punto de ser reemplazada en lugar de la recién creada.

**Ejemplo**

Considere una certificación que se repite mensualmente, en la que se han creado cuatro versiones a lo largo del tiempo debido a las reapariciones sucesivas:

- Un alumno que se ha inscrito en la primera versión y ha progresado en cada repetición a medida que se produce, volverá a la versión en la que está activo actualmente, que refleja su propio historial de finalización y repetición, no necesariamente la última versión que existe.

- Un alumno que aún no se ha inscrito volverá a la versión creada más recientemente, ya que es la versión a la que deben unirse las nuevas inscripciones.

Esto permite que la integración dirija siempre a un alumno a la versión de certificación que sea relevante para él, en lugar de mostrar todas las versiones históricas o adivinar cuál se aplica.

### Referencia de API

**Obtener la certificación aplicable para una certificación raíz**

```
GET /primeapi/v2/learningObjects/{loId}/applicableCertification
```

Resuelve la versión de certificación que se aplica al alumno actual, dado el ID de una certificación raíz. Para los alumnos que se han inscrito, devuelve la versión en la que se han inscrito actualmente. Para los alumnos que no están inscritos, se devuelve la última versión activa.

| **Propiedad** | **Valor** |
|----------------------------------------------------------|--------------------------|
| **Ámbito** | Acceso de lectura del alumno |
| **Límite de velocidad (llamadas estándar de alumnos)** | 70 solicitudes por minuto |
| **Límite de velocidad (credenciales de API elevadas o de nivel de administrador)** | 500 solicitudes por hora |
| **Formato de respuesta** | application/vnd.api+json |

**Nota**: Esta API devuelve información de la versión de un solo alumno cada vez. No devuelve una lista de todas las versiones de una certificación.

**Parámetros de ruta**

| **Parámetro** | **Obligatorio** | **Tipo** | **Descripción** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| loId | Sí | cadena | El ID del objeto de aprendizaje, en concreto, la certificación raíz, para la que se solicita la versión aplicable. Esto está sujeto a los permisos de acceso estándar. |

**Parámetros de consulta**

| **Parámetro** | **Obligatorio** | **Tipo** | **Descripción** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| incluir | No | cadena | Una lista separada por comas de los modelos relacionados que se incluirán en la respuesta junto con la certificación resuelta, como subLO o inscripción. Utiliza la misma sintaxis de inclusión que otros puntos finales de objetos de aprendizaje de Adobe Learning Manager. |

**Ejemplo de solicitud**

```
GET /primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

```
curl -X GET --header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://<host>/primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs'
```

**Nota**: El valor loId debe estar codificado en URL. Los dos puntos de un Id. de certificación, como certificación:167658, se codifican como %3A.

**Ejemplo de respuesta 200 Aceptar**

La respuesta utiliza la misma estructura que una respuesta de objeto de aprendizaje estándar, lo que devuelve la certificación resuelta.

**Importante:** El campo de id. en la respuesta es el id. de la certificación **resolvió**, la versión específica aplicable a este alumno. Normalmente será diferente del ID de certificación raíz que pasó como loId, ya que el propósito de esta API es convertir un ID de raíz en la versión actual correcta.

```
{
  "data": {
    "id": "string",
    "type": "string",
    "attributes": {
      "authorNames": [
        "string"
      ],
      "bannerUrl": "string",
      "catalogs": [
        ...
      ]
    }
  }
}
```

**Códigos de respuesta**

| **Estado** | **Significado** |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 200 | La certificación aplicable se resolvió correctamente y se devuelve como respuesta. |
| 400 | El loId proporcionado no es una certificación o no es una certificación raíz. Pase el ID de la certificación original, no una versión de periodicidad, como loId. |
| 401 / 403 | A la solicitud le faltan credenciales de alumno válidas o las credenciales no tienen el acceso necesario. |
| 404 | No se pudo resolver ninguna certificación activa para esta certificación raíz. Por ejemplo, porque todas las versiones de la cadena se han retirado o eliminado, o porque la certificación no tiene ninguna referencia de certificación raíz registrada. También se puede producir un error 404 si una versión se resuelve correctamente, pero el alumno que realiza la llamada no tiene acceso al catálogo. |
| 500 | Error inesperado del servidor al resolver la certificación. Vuelva a intentar la solicitud; si el error persiste, póngase en contacto con el soporte técnico. |

**Ejemplo de respuesta de error**

```
{
  "meta": {
    "error": "string",
    "detail": "string"
  }
}
```

**Nota:** Esta API resuelve la versión de un alumno por llamada. No devuelve una lista de todas las versiones que existen para una certificación raíz.

**Aspectos importantes**

- **Certificaciones no periódicas:** Si el loId que pasa es una certificación que no está configurada para repetirse, la API devuelve esa propia certificación.

- **Versiones intermedias omitidas:** Si la inscripción activa de un alumno se ha movido directamente de una versión anterior a una posterior sin una inscripción activa entre, la API se sigue resolviendo correctamente en la versión actual real del alumno. La presencia de versiones intermedias con las que el alumno no interactuó de forma activa no afecta a la resolución.

- **Certificaciones eliminadas frente a retiradas:** Una versión de certificación que se ha eliminado se excluye por completo de la resolución. Una certificación retirada puede considerarse todavía en función de su estado; si confía en que una versión específica aún pueda resolverse, confirme su estado actual en lugar de suponer que la retirada por sí sola la elimina de la consideración.

- **La resolución es determinista:** Si los datos de inscripción de un alumno están en un estado incoherente (por ejemplo, más de una inscripción está marcada como actual), la API se resuelve en la versión creada más recientemente en lugar de devolver un resultado impredecible o un error.

**Nota**: Un equivalente con ámbito de administrador de esta API no está disponible actualmente y se está evaluando para una futura versión.

### Utilice esta API en su integración

Un caso de uso común es una página o portal externo que enumera las certificaciones a las que puede acceder un alumno. En lugar de vincularse directamente a un ID de certificación específico, que puede quedar obsoleto después de una repetición. Cree un vínculo con el ID de certificación raíz y resuelva la versión correcta en el momento en que el alumno la seleccione.

&#x200B;1. Almacene o haga referencia a certificaciones en su integración usando el **ID de certificación raíz,** el ID de la certificación tal y como se creó por primera vez, antes de cualquier repetición.

&#x200B;2. Cuando un alumno seleccione una certificación para verla o para trabajar con ella, llame a GET /primeapi/v2/learningObjects/{loId}/applied, pasando el ID de certificación raíz a loId.

&#x200B;3. Utilice la versión de certificación devuelta en la respuesta para dirigir al alumno al destino correcto, ya sea una acción de inscripción o una vista de su progreso actual.

Esto garantiza que los alumnos siempre confíen en la versión de la certificación que coincida con su inscripción y progreso reales, incluso cuando la certificación se repite a lo largo del tiempo y genera nuevas versiones.

## Informes: ID raíz de formación en la transcripción del alumno

La columna **ID raíz de formación** está disponible de forma predeterminada en la transcripción del alumno para todas las cuentas.

| **Tipo de fila** | **Valor de ID de formación raíz** |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| Certificación configurada para repetirse | El ID de certificación raíz al que se remonta esta versión |
| Certificación no configurada para repetirse | El mismo valor que el ID de formación de esa fila. |
| Un curso incrustado en una certificación | El ID de certificación raíz de la certificación principal, no el ID propio del curso |
| Un curso o una ruta de aprendizaje que no forme parte de ninguna certificación | El mismo valor que el ID de formación o el ID de curso incrustado de esa fila. |

**Nota**: En el caso de cuentas muy grandes con un gran volumen de certificaciones, los valores de ID de formación raíz de la transcripción del alumno se resuelven en lotes. Esto no cambia la precisión de los datos, pero las transcripciones muy grandes pueden tardar más en generarse.

Esta columna permite agrupar e informar sobre el historial completo de un alumno en todas las versiones de una certificación periódica, en lugar de tratar cada periodicidad como un registro independiente no relacionado. Cada repetición sigue apareciendo como su propia fila en la transcripción del alumno. La columna ID de formación raíz simplemente identifica qué filas pertenecen a la misma certificación subyacente.

**Nota:** Utilice la columna ID. de formación raíz cuando necesite realizar un seguimiento del historial de participación completo de un alumno en una certificación periódica.

