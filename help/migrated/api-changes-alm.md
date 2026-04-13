---
description: Cambios en la API de ALM
jcr-language: en_us
title: Cambios en la API en la versión de abril
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '4093'
ht-degree: 0%

---


# Cambios en la API de la versión de abril de 2026

La versión de abril de 2026 de Adobe Learning Manager introduce mejoras específicas en la API pública en torno a alternativas y equivalentes, acceso al contenido con ventana de tiempo, intentos de cuestionario basados en contenido, experiencias sin inicio de sesión y gestión de ayudas de trabajo. Los cambios están diseñados para ser en gran medida compatibles con versiones anteriores, al tiempo que permiten integraciones más precisas.

## Aprendizaje adaptable para rutas de aprendizaje

Esta versión añade compatibilidad total con la API pública para rutas de aprendizaje adaptables. Las rutas de aprendizaje (LP) ahora pueden definir reglas adaptables que controlan qué secciones y objetos de subaprendizaje (subobjetos de aprendizaje) son visibles para los diferentes grupos de alumnos, y la API pública refleja este comportamiento.

Se ven afectados los siguientes puntos finales:

- GET /primeapi/v2/learningObjects?filter.loTypes=learningPath
- GET /primeapi/v2/learningObjects/{loId}

Un nuevo atributo booleano, attributes.isAdaptive, indica que un programa de aprendizaje utiliza reglas adaptables. Cuando este indicador es true, el atributo sections se interpreta de forma adaptativa.

Para las llamadas de alumnos, solo se devuelven las secciones visibles para el alumno actual. Cada sección incluye la lista de ID de objeto de aprendizaje (loIds), un indicador obligatorio y un LOCount obligatorio que se calculan según la configuración adaptable de ese alumno, así como el sectionId. La relación relations.subLOs ahora también se filtra, por lo que solo contiene los objetos de subaprendizaje que son visibles para ese alumno.

Para las llamadas de administrador, las secciones también pueden exponer una matriz adaptiveConfig. Se describen las reglas adaptables por grupo de usuarios, incluidos userGroupId y userGroupName, y si la sección es obligatoria para ese grupo. Las herramientas orientadas a los administradores pueden utilizar esta opción para visualizar y gestionar reglas adaptables.

Restablecer finalización para programas de aprendizaje

La versión introduce una API para __actualizar (restablecer) la finalización__ de los objetos de aprendizaje, incluidos los programas de aprendizaje adaptables. Esto es compatible con situaciones como el reciclaje, actualizaciones periódicas de cumplimiento o reinicios de programas.

Hay un nuevo punto final disponible:

```
POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion
```

Esta operación requiere los permisos de escritura adecuados y restablece el estado de finalización de la instancia de objeto de aprendizaje especificada en el contexto de usuario especificado. Está pensada para su uso por parte de automatizaciones del lado de los administradores o herramientas de aprendizaje con un ámbito cuidado.

Una versión en bloque de esta capacidad está planificada mediante una API de trabajos. La forma de solicitud está diseñada para dirigirse a los usuarios por correo electrónico, ID de usuario o ID de grupo de usuarios, por ejemplo:

```
{  
  "emails": ["[user1@example.com](mailto:user1@example.com)", "[user2@example.com](mailto:user2@example.com)"],  
  "userIds": ["12345", "67890"],  
  "userGroupIds": ["ug1", "ug2"]  
}  
```

Las integraciones deben utilizar esta API cuando necesiten reiniciar a los alumnos en cada programa o curso. Los clientes deben gestionar correctamente las respuestas a los errores: la API puede rechazar las solicitudes de actualización, donde no es aplicable un restablecimiento (por ejemplo, cuando no existe finalización o no se admiten los tipos de objetos de aprendizaje).

## Equivalentes y finalizaciones alternativas

Para admitir implementaciones en las que varios objetos de aprendizaje pueden cumplir el mismo requisito, la versión introduce finalizaciones de equivalentes y alternativas como API públicas.

Los puntos finales del objeto de aprendizaje ahora contienen esta información:

```
- GET /primeapi/v2/learningObjects
- GET /primeapi/v2/learningObjects/{loId}
```

Un nuevo atributo booleano attributes.isAlternateComplete indica si la finalización del alumno para un objeto de aprendizaje determinado es el resultado de un objeto de aprendizaje alternativo o equivalente en lugar del propio objeto. Cuando esto es cierto, la relación relations.alternativeCompltions enumera los objetos de aprendizaje que actuaron como alternativos. Esto permite que los informes descendentes y los paneles distingan entre finalizaciones directas y alternativas y muestren qué alternativas cumplen el requisito.

Además, una vista relacionada de objetos de aprendizaje permite descubrir alternativas potenciales que pueden satisfacer a un objeto de aprendizaje. Esto se expone a través de:

```
GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}
```

La respuesta devuelve objetos de aprendizaje que pueden actuar como alternativas e incluye un campo meta.count que indica el número total de dichas alternativas, independientemente del límite actual. Las integraciones pueden utilizar esto para presentar equivalentes recomendados o para generar vistas administrativas de asignaciones alternativas.

## Informes y casos prácticos de análisis

Los usuarios que generen informes o análisis deben actualizar su lógica para añadir isAlternateComplete y alternativeCompltions a sus flujos de trabajo de informes.

Las integraciones de informes que consumen datos de finalización (por ejemplo, exportación de LT, fuentes de almacén de datos personalizadas o paneles de BI) deben ampliar su lógica para leer y conservar tanto attributes.isAlternateComplete como relations.alternativeCompltions de las API de LO:

- Cuando isAlternateComplete == false:\
  Trate el registro como una __finalización directa__ del objeto de aprendizaje, como en la actualidad.
- Cuando isAlternateComplete == true:
   - Marque el registro como __finalización alternativa__ en el informe (por ejemplo, una columna &quot;Método de finalización&quot; con valores DIRECT frente a ALTERNATE).
   - Utilice relations.alternativeCompletions.data[*].id para capturar __qué objeto de aprendizaje de origen__ concedió esta finalización (por ejemplo, &quot;Curso B completado mediante un curso alternativo A&quot;).

Casos de uso típicos:

- _Informes de cumplimiento_: muestran que un curso de cumplimiento se completó mediante un equivalente aprobado y enumeran el curso de origen que cumplió el requisito.
- _Paneles de progreso del programa_: distingue a los alumnos que completaron una ruta _directamente_ de los que la completaron mediante alternativas, para obtener vistas más precisas del progreso y las correcciones.
- _Registros de auditoría_: para cualquier objeto de aprendizaje marcado como isAlternateComplete=true, los auditores pueden ver exactamente qué cursos de formación alternativos se utilizaron para conceder esa finalización.

Sin incorporar estos dos campos, los informes descendentes tratarán las finalizaciones alternativas como finalizaciones regulares y _no podrán explicar_ *por qué* un alumno muestra como completado un curso de formación que nunca realizó directamente.

## Comportamiento del alumno frente a la API del objeto de aprendizaje administrador

La estructura de ayudas de trabajo en varios idiomas es idéntica en las API de objetos de aprendizaje y de administrador. El ámbito del alumno devuelve solo las ayudas de trabajo visibles para el alumno, pero para cada ayuda de trabajo visible expone todas las configuraciones regionales configuradas a través de varias entidades de recursos (una por configuración regional) y metadatos localizados en varias configuraciones regionales. El ámbito de administración devuelve todas las ayudas de trabajo que el administrador puede administrar, con el mismo modelo de objeto de aprendizaje e ID de recurso específicos de la configuración regional. Los clientes con ámbito de alumno deben elegir el recurso cuyos atributos.locale coincidan mejor con el idioma de contenido del alumno, mientras que las herramientas de administración pueden enumerar todas las configuraciones regionales para la creación de informes y la administración.

## Lista de comprobación con capacidad de comentarios

Para admitir flujos de trabajo en los que los revisores pueden compartir comentarios estructurados sobre actividades basadas en listas de comprobación, esta versión muestra *comentarios de listas de comprobación* y controles de visibilidad de revisores a través de la API de recursos de objetos de aprendizaje.

Los metadatos relacionados con la lista de comprobación se muestran en entidades learningObjectResource (JApiLOResource, &quot;type&quot;: &quot;learningObjectResource&quot;) que representan recursos de la lista de comprobación dentro de un curso u otro objeto de aprendizaje.

La información está disponible a través de:

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

Cuando la instancia del objeto de aprendizaje contiene recursos de tipo lista de comprobación, las entradas learningObjectResource correspondientes de la matriz incluida exponen los atributos de comentario y visibilidad del revisor en atributos, y la identidad del revisor en relaciones.

### Nuevos atributos de comentario de lista de comprobación

Para los recursos de la lista de comprobación, pueden estar presentes los siguientes atributos en learningObjectResource:

- attributes.checklistComment\
  Un comentario de texto libre que deja el revisor para el alumno, por ejemplo:\
  &quot;checklistComment&quot;: &quot;Excelente rendimiento! Todos los protocolos de seguridad se siguieron correctamente&quot;.\
  Este atributo se rellena _solo si_:
   - showChecklistComment es true y
   - la configuración checklist tiene activado enable_reviewer_comments.
- attributes.showChecklistComment\
  Un indicador booleano que indica si los comentarios del revisor se deben mostrar al alumno:\
  &quot;showChecklistComment&quot;: true\
  Este atributo está presente _solo cuando_ enable_reviewer_comments está habilitado en la configuración de lista de comprobación.\
  Los clientes deben utilizar este indicador para decidir si desean mostrar checklistComment en las experiencias de los alumnos.
- attributes.showReviewerNameToLearner\
  Un indicador booleano que controla si el alumno debe ver la identidad del revisor:\
  &quot;showReviewerNameToLearner&quot;: true\
  Cuando es verdadero, los clientes pueden utilizar la relación checklistReviokedBy (véase a continuación) para resolver y mostrar el nombre del revisor (por ejemplo, mediante una API de búsqueda de usuarios).

Otros contextos específicos de la lista de comprobación, como checklistEvaluationStatus, isChecklistObligatorio, resourceSubType: &quot;CHECKLIST&quot; y submitDate también están disponibles en el mismo learningObjectResource para admitir más interfaces de usuario e informes de listas de comprobación.

### Relación de identidad del revisor

Cuando los nombres de los revisores están pensados para ser visibles, learningObjectResource incluye una relación que señala al usuario del revisor:

```
"relationships": {
  "checklistReviewedBy": {
    "data": {
      "id": "user_id",
      "type": "user"
    }
  }
}
```

Esta relación se rellena _solo si_:

- showReviewerNameToLearner es true y
- checklistReviewingBy no es null (es decir, la lista de comprobación se ha revisado).

Las aplicaciones cliente deben:

1. Compruebe attributes.showReviewerNameToLearner.
2. Si está presente true y relations.checklistReviokedBy.data, llame a la API de usuario correspondiente para resolver &quot;id&quot;: &quot;user_id&quot; en un nombre para mostrar.
3. Representa el nombre del revisor junto al comentario o estado de la lista de comprobación, según corresponda.

### Acceso a recursos y comentarios de lista de comprobación

Para recuperar los recursos de la lista de comprobación y sus comentarios para un objeto de aprendizaje determinado, los clientes deben:

- Llamar

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

- En la respuesta:
   - Utilice relations.instance del objeto de aprendizaje principal para localizar las entradas de learningObjectInstance relevantes en las entradas incluidas.
   - En cada learningObjectInstance, siga relations.loResources para buscar entradas learningObjectResource.
   - Filtrar elementos learningObjectResource donde:
      - attributes.resourceSubType == &quot;CHECKLIST&quot; (para recursos de lista de comprobación), y
      - opcionalmente attributes.showChecklistComment == true para buscar listas de comprobación con comentarios visibles para el alumno.

- Para cada learningObjectResource de la lista de comprobación, utilice:
   - attributes.checklistComment (si está presente y showChecklistComment es true)
   - attributes.checklistEvaluationStatus (por ejemplo, &quot;PASSED&quot;)
   - attributes.showReviewerNameToLearner
   - relations.checklistReviokedBy (cuando esté presente) para identificar al revisor.

Este modelo permite a los clientes descentralizados o personalizados procesar una experiencia de lista de comprobación completa, que incluye el estado, los indicadores obligatorios/opcionales y los comentarios de los revisores, directamente desde las API de Captivate Prime.

### Consideraciones sobre informes y experiencia de usuario

- _Informes y análisis_
Las integraciones que controlan el rendimiento de los alumnos en listas de comprobación pueden incorporar:
   - checklistEvaluationStatus para aprobado/suspenso u otros indicadores de estado.
   - isChecklistObligatorio para diferenciar las actividades de lista de comprobación obligatorias de las opcionales.
   - Presencia o ausencia de checklistComment y showChecklistComment para auditorías de cobertura de comentarios.
- _Experiencias de los alumnos_
Las implementaciones de IU deben:
   - Respete showChecklistComment antes de mostrar comentarios.
   - Utilice showReviewerNameToLearner y checklistReviewedBy para decidir si desea mostrar el nombre del revisor o mantener el anonimato de la revisión.
   - Retrocede sin problemas cuando los comentarios están deshabilitados o no están presentes, y siguen mostrando el estado de la evaluación y la información de envío.

## Compatibilidad con varios idiomas para la ayuda de trabajo

Para admitir implementaciones en las que las ayudas de trabajo deben entregarse en varios idiomas tanto a los alumnos como a los administradores, esta versión amplía el control de las ayudas de trabajo para devolver *un recurso por configuración regional* en lugar de un único recurso en-US codificado de forma rígida.

Las ayudas de trabajo en varios idiomas siguen utilizando la jerarquía existente:

_objeto de aprendizaje_ (lo) → _recursoObjetoDeAprendizaje_ (recursoLo) → _recurso_

No se requieren cambios en el contrato de la API. Cualquier ayuda de trabajo localizada se ajusta de forma natural a esta estructura, con entidades de recursos independientes por configuración regional y metadatos localizados compartidos en los niveles learningObject/learningObjectResource.

Los datos de la ayuda de trabajo se exponen mediante:

```
GET /primeapi/v2/learningObjects/jobAid:{jobAidId}?include=instances.loResources.resources
```

Cuando una ayuda de trabajo tiene varias variantes de idioma, la matriz incluida contiene varias entradas &quot;tipo&quot;: &quot;recurso&quot;, una para cada configuración regional (por ejemplo, en-US, fr-FR, es-ES), todas vinculadas desde un único recurso learningObjectResource.

### Estructura de ayudas de trabajo en varios idiomas

Las ayudas de trabajo en varios idiomas utilizan:

- _learningObject (tipo: learningObject)_
   - Contiene metadatos localizados con varias entradas (p. ej., en-US, fr-FR) para que los clientes puedan presentar el título o la descripción de la ayuda de trabajo en el idioma adecuado.
- _learningObjectInstance (tipo: learningObjectInstance)_
   - Hace referencia a una o varias entradas learningObjectResource mediante relations.loResources.
- _learningObjectResource (tipo: learningObjectResource)_
   - Contiene configuraciones comunes (tipo de contenido, versión, etc.) y metadatos localizados en varias configuraciones regionales.
   - Vínculos a una o varias entidades de recursos mediante relations.resources.
- _recurso (tipo: recurso)_
   - *Uno por configuración regional*, cada uno con su propio id., configuración regional, nombre y URL (location / downloadUrl).

Para una ayuda de trabajo en varios idiomas, un patrón típico es:

- learningObjectResource con metadatos localizados para en-US y fr-FR
- relations.resources.data que señala a:
   - recurso con configuración regional: &quot;en-US&quot;
   - recurso con configuración regional: &quot;fr-FR&quot;

Los clientes pueden seleccionar el recurso adecuado haciendo coincidir la configuración regional del alumno con el campo resource.attributes.locale.

### Nuevo formato de Id. de recurso para ayudas de trabajo

Para distinguir correctamente varias variantes localizadas de un recurso de ayuda de trabajo, el _formato de identificador de recurso ha cambiado_.

_Formato de id. de recurso antiguo (heredado)_

Anteriormente, los recursos de ayudas de trabajo utilizaban un formato de ID opaco, como:

jobAid:131032_-1_-1_2_resource

Este formato no codificaba la configuración regional, y las API mostraban de forma efectiva solo un recurso (normalmente en-US).

_Nuevo formato de Id. de recurso (compatible con varios idiomas)_

El nuevo formato es:

```
jobAid:<jobAidId>_<version>_<localeCode>
```

Ejemplos:

- jobAid:131032_2_en-US
- jobAid:131032_2_fr_FR
- jobAid:131032_2_es_ES

Desglose visual:

```
jobAid:131032_2_fr_FR

        │      │ │ │

        │      │ │ └──► Locale Code (fr_FR, en_US, es_ES, etc.)

        │      │ └────► Version (2)

        │      └──────► JobAid ID (131032)

        └─────────────► Resource Type Prefix ("jobAid:")
```

Esta estructura permite a los clientes:

- Identifique rápidamente a qué ayuda de trabajo y versión pertenece un recurso.
- Deduzca directamente la configuración regional del ID de recurso cuando sea necesario.

### Retrocompatibilidad: 

```/resources/{resourceId}```

El extremo de recurso heredado sigue estando disponible:

```GET /primeapi/v2/resources/{resourceId}

```

Ahora es _compatible con versiones anteriores_ con los formatos de ID nuevo y antiguo:

- _Formato de id. antiguo_ (por ejemplo, jobAid:131032_-1_-1_2_resource)
   - Sigue trabajando.
   - Devuelve el _primer recurso creado_ asociado con ese identificador heredado (normalmente el recurso original en-US).
- _Nuevo formato de id._ (por ejemplo, jobAid:131032_2_fr_FR)
   - Devuelve el _recurso específico de configuración regional exacto_ correspondiente a ese identificador.
   - Esto permite la recuperación y manipulación precisas de variantes de ayudas de trabajo localizadas.

Las integraciones que actualmente almacenan o hacen referencia a los identificadores de recursos antiguos pueden seguir funcionando sin cambios, mientras que se recomienda a las implementaciones más recientes que adopten el nuevo formato de identificador para las operaciones específicas de la configuración regional.

### Consideraciones sobre integración y experiencia de usuario

- _IU de alumno/administrador_
   - Utilice learningObject.localizedMetadata y learningObjectResource.localizedMetadata para presentar los títulos y descripciones en el idioma adecuado.
   - Utilice resource.attributes.locale para seleccionar la dirección URL correcta (location/downloadUrl) para la configuración regional del alumno.
   - Implemente el comportamiento de reserva (por ejemplo, utilice en-US) si la configuración regional exacta de un alumno no está disponible.
- _API y almacenamiento_
   - Para nuevas integraciones, almacene los _identificadores de recursos de nuevo formato_ (```jobAid:<jobAidId>_<version>_<localeCode>```) para habilitar la recuperación específica de la configuración regional sin ambigüedades.
   - Los identificadores heredados aún se pueden usar con /resources/{resourceId}, pero no distinguirán entre configuraciones regionales.

## Restricciones de espacio de tiempo para módulos de inicio

Algunas experiencias de aprendizaje deben estar disponibles solo dentro de un intervalo de tiempo definido. La versión muestra información de intervalos de tiempo sobre los recursos de objetos de aprendizaje e introduce un punto final de validación que comprueba si un alumno puede iniciar un recurso en el tiempo actual.

Los metadatos de franja horaria están disponibles a través del punto final:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

En el nivel de recurso del objeto de aprendizaje, ahora puede haber un objeto timeSlot presente en los atributos, con valores startTime y endTime en UTC. Esto especifica la ventana durante la cual se puede iniciar el recurso.

Antes de iniciar un módulo, las integraciones pueden llamar a un nuevo punto final de validación:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

Este punto final, diseñado para escenarios de lectura del alumno, devuelve si el alumno puede iniciar el recurso en ese momento, teniendo en cuenta el intervalo de tiempo configurado, el tipo de entrega y otras reglas de back-end.

Los reproductores personalizados y las aplicaciones cliente deben utilizar canStart para exigir el acceso basado en el tiempo y utilizar los metadatos timeSlot para mostrar mensajes claros sobre cuándo el contenido está disponible o caduca. Las respuestas negativas de canStart se deben controlar explícitamente para informar a los alumnos de por qué el contenido no se puede iniciar todavía o ya.

## Cuestionarios de varios intentos basados en el contenido

Algunos paquetes de contenido implementan su propio seguimiento de intentos en lugar de depender únicamente de Adobe Learning Manager. La versión introduce un indicador que indica cuándo los intentos los controla el propio contenido.

Mediante:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Los recursos de objetos de aprendizaje ahora pueden exponer un atributo booleano hasContentDrivenAttemptTracking. Cuando esto es cierto, el cuestionario o módulo gestiona los intentos internamente (por ejemplo, a través de la lógica SCORM o xAPI), y es posible que los contadores de intentos estándar de la plataforma no reflejen completamente la experiencia del alumno.

Las integraciones que muestren recuentos de intentos o controlen el comportamiento de reintentos deben comprobar este indicador. Cuando está activada, no deben inferir los límites de intentos únicamente a partir de los metadatos de la plataforma y deben estar preparados para basarse en informes del lado del contenido (por ejemplo, a través de declaraciones xAPI) o reglas específicas de la empresa.

## Cambio de comportamiento en el formato de ID de recurso de ayuda de trabajo

Esta versión introduce un __cambio de comportamiento__ importante en el formato de los identificadores de recursos de la ayuda de trabajo. Si bien no hay ningún punto final nuevo involucrado, esto tiene un impacto directo en los sistemas que almacenan o analizan estos ID.

Anteriormente, los identificadores de recursos de ayuda de trabajo utilizaban un formato como:

```jobAid:<jobAidId>_-1_-1_2_resource```

En la versión de abril de 2026, se ha sustituido por un formato simplificado y más explícito:

```jobAid:<jobAidId>_<version>_<localeCode>```

Por ejemplo:

jobAid:131032_2_fr_FR

Los componentes son:

- ```<jobAidId>```: el identificador numérico de la ayuda de trabajo (por ejemplo, 131032),
- ```<version>```: el número de versión de la ayuda de trabajo (por ejemplo, 2),
- ```<localeCode>```: el código local (por ejemplo, en_US, fr_FR, es_ES).

Cualquier integración que indexe recursos o persista en ID de recursos de ayuda de trabajo debe actualizar su lógica de análisis y almacenamiento para reconocer el nuevo formato. Dado que los identificadores en sí cambian, se recomienda encarecidamente que vuelva a generar los índices locales definidos por los identificadores de recursos de ayuda de trabajo después de actualizar a la versión de abril de 2026.

## Definir imágenes de banners de cursos mediante la migración

Ahora puede definir o actualizar las imágenes de los banners del curso en Adobe Learning Manager como parte del flujo de trabajo de migración estándar. Esto le ayuda a iniciar o limpiar catálogos grandes mientras mantiene las páginas del curso visualmente coherentes, sin necesidad de editarlas manualmente

### Dónde se definen las imágenes del banner

Las imágenes de banner se configuran en el archivo de migración _course.csv_, que ya se utiliza para proporcionar metadatos del curso, como:

- id
- courseName
- courseCreationDate
- state
- autor
- thumbnailUrl

Con esta mejora, la especificación course.csv incluye una _columna opcional_ adicional para la imagen del banner del curso. El nombre exacto del encabezado se define en la especificación CSV que se descarga de la cuenta de Learning Manager (por ejemplo, puede aparecer como bannerUrl o bannerImageUrl).

La columna del titular:

- Señala al archivo de imagen que desea usar como _banner del curso_.
- Funciona igual que thumbnailUrl, con imágenes disponibles en el repositorio de contenido configurado (Box/FTP).

### Preparación de imágenes de banner para la migración

1. Cargar imágenes de banner: coloque los archivos de imagen de banner en la misma ubicación de Box o FTP que use para otros activos de migración, siguiendo la estructura de directorios existente.
2. Comprobar formato de archivo:
Utilice uno de los formatos de imagen admitidos (por ejemplo, png, jpg, jpeg, gif), tal y como se describe en los requisitos del sistema:
   1. [*Requisitos del sistema*](/help/migrated/system-requirements.md)
3. Actualizar course.csv: En la nueva columna del banner, haga referencia a la ruta de acceso relativa o al identificador de la imagen del banner. Un ejemplo conceptual:

```
id,courseName,courseCreationDate,state,author,thumbnailUrl,bannerUrl  
12345,DEMO1,2018-05-05T08:56:21.000Z,Published,Sudheer,pic1.png,banners/banner1.png  
45678,DEMO2,2018-05-05T08:56:21.000Z,Published,Sudheer,pic2.png,banners/banner2.png  
```

### Aplicar banners durante una ejecución de migración

Una vez actualizado course.csv, el flujo es el mismo que para cualquier otra migración:

1. _Cargar CSV_
Cargue el archivo course.csv actualizado (y cualquier otro archivo relevante) en la carpeta Box/FTP configurada para la migración. Los nombres de archivo deben coincidir exactamente con los nombres especificados en csv_specifications.zip (distinguen entre mayúsculas y minúsculas).
2. _Iniciar una ejecución de sprint_
En Adobe Learning Manager, como administrador de integración, inicie una _ejecución de sprint_ de migración que incluya course.csv.\
   El motor de migración lee la columna del banner y aplica la imagen del banner a cada curso.
3. _Revisar resultados y registros de errores_
Después del sprint:
   1. Comprueba los banners en las aplicaciones _Author_ y _Learner_.
   2. Si se produce un error en algunas filas (por ejemplo, debido a una ruta de archivo no válida o a un formato no compatible), descargue el archivo CSV de error de la ejecución de la migración y corrija los datos.

### Cursos nuevos frente a cursos existentes

El campo de titular funciona en ambos casos:

- _Cursos nuevos creados mediante la migración_
Cuando se crea un curso por primera vez a partir de course.csv y se rellena la columna del banner, ese banner se configura inmediatamente.
- _Cursos existentes (actualización/correcciones)_
Si vuelve a ejecutar la migración con el mismo ID del curso y un nuevo valor de banner:
   - Learning Manager localiza el curso existente.
   - La imagen del banner se _actualizó_ a la nueva imagen especificada en el CSV.

Los nombres de columna y las rutas de acceso reales deben coincidir con la _especificación CSV descargada_ y el diseño del repositorio de contenido.

## Quitar columna de orden en LearningProgramCourse

Adobe Learning Manager ahora admite un modelo simplificado para _ordenar cursos dentro de rutas de aprendizaje (programas de aprendizaje)_ durante la migración. Como parte de este cambio, la columna _order se elimina_ del archivo de migración learning_program_course.csv.

Anteriormente, el archivo learning_program_course.csv incluía una columna (a menudo denominada order o similar) que se utilizaba para:

- Establezca explícitamente la _posición_ de cada curso dentro de un programa de aprendizaje, en función del valor numérico de esa columna.
- Requerir que los administradores o scripts mantengan esta secuencia numérica manualmente, especialmente al insertar o reordenar cursos.

Ahora, Adobe Learning Manager ya no utiliza la columna de orden en learning_program_course.csv para determinar el orden del curso. En su lugar, el archivo CSV de migración se centra en _qué cursos pertenecen a cada programa de aprendizaje_, en lugar de en cómo se ordenan numéricamente.

## Incidencia en los archivos CSV de migración

### learning_program_course.csv

Debe tratar la columna de orden heredada como eliminada u omitida:

- No confíe en el orden para controlar la secuencia de cursos en un programa de aprendizaje durante la migración.
- Si todavía tiene una columna de pedido de plantillas más antiguas:
   - Learning Manager lo omitirá para realizar pedidos.
   - Puede eliminarla de forma segura del CSV a lo largo del tiempo para simplificar los archivos de migración.
- La asignación básica requerida sigue siendo la siguiente:
   - ↔ ID del programa de aprendizaje : ID del curso (y otras columnas aún documentadas como id, learningProgramId, courseId y fechas).

Consulta siempre las [_especificaciones de CSV_](https://experienceleague.adobe.com/es/docs/learning-manager/using/integration/migration-manual) más recientes de tu cuenta de Learning Manager (mediante csv_specifications.zip) para confirmar el conjunto de encabezados y los requisitos actuales.

## timeZoneCode en instancias del curso

A partir de esta versión, el modelo Instancia del curso (learningObjectInstance) muestra un nuevo atributo:

timeZoneCode: un campo de cadena que vincula explícitamente una instancia de curso a una de las zonas horarias configuradas de la cuenta.

Esto permite a los clientes:

- Resuelva la zona horaria de una instancia de curso de forma coherente e impulsada por la API.
- Interprete y muestre correctamente todas las fechas/horas a nivel de instancia para esa instancia, independientemente de la zona horaria del propio usuario.

### Donde aparece timeZoneCode

El campo se añade en los atributos del modelo learningObjectInstance
solo para instancias de curso.

Ejemplo:

```
{
  "id": "course:1262748_1359228",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2019-08-06T13:50:39.000Z",
    "isAET": false,
    "isDefault": true,
    "timeZoneCode": "356",
    "isFlexible": false,
    "state": "Active",
    "localizedMetadata": [
      {
        "locale": "en-US",
        "name": "Default instance"
      }
    ]
  }
}
```

### Cómo resolver timeZoneCode

El valor numérico de timeZoneCode es una clave de búsqueda en el catálogo de zonas horarias de la cuenta, que se muestra mediante la API de la cuenta:

```http
GET /primeapi/v2/account
Authorization: Bearer <access_token>
```

Dentro de la respuesta, las zonas horarias se enumeran en:

```
"data": {
  "attributes": {
    "timeZones": [
      {
        "name": "Etc/GMT+12",
        "timeZoneCode": "356",
        "utcOffset": -720,
        "utcOffsetCode": "UTC-12:00(Etc/GMT+12)",
        "zoneId": "Etc/GMT+12"
      },
      "..."
    ]
  }
}
```

### Flujo de cliente recomendado:

1. Llame a GET/cuenta una vez y almacene en caché attributes.timeZones para el inquilino.
2. Para cada instancia de curso:
   - Lea attributes.timeZoneCode.
   - Busque la entrada correspondiente en timeZones donde coincide timeZoneCode.
   - Utilice zoneId, utcOffset y utcOffsetCode de esa entrada para la lógica de visualización y programación.

## API públicas asíncronas para la suscripción de grupos de usuarios

### Introducción

Adobe Learning Manager expone dos _API asincrónicas de administración_ para administrar la pertenencia a grupos de usuarios (UG):

- POST /async/userGroups/{userGroupId}/users: agregar usuarios a un UG de forma asincrónica
- DELETE /async/userGroups/{userGroupId}/users: quitar usuarios de un UG de forma asincrónica

En lugar de actualizar la suscripción en la misma solicitud, estas API aceptan el lote y devuelven un _ID de evento_. El resultado real se entrega más tarde a través de webhooks.

Utilícelos cuando:

- Está administrando grupos grandes o actualizaciones frecuentes por lotes.
- La latencia es menos importante que la fiabilidad y el rendimiento.
- Está creando integraciones (HR, CRM, LXP) en lugar de clics de interfaz de usuario.

Para las acciones de administración pequeñas e interactivas, puede seguir utilizando las API sincrónicas de `/userGroups/{id}/users`.

### Autenticación y URL base

Estas API forman parte de la superficie estándar __v2 Admin API__.

- [URL base (prod)](https://learningmanager.adobe.com/docs/primeapi/v2/)
- Autenticación: token de acceso de OAuth 2.0 con ámbito `admin:write`
- Encabezados necesarios:
   - Autorización: portador &lt;token_acceso>
   - Tipo de contenido: aplicación/json
   - Aceptar: aplicación/json

Para conocer el comportamiento y los ámbitos generales de la API de administración, consulte:

- [Manual del desarrollador](/help/migrated/integration-admin/feature-summary/developer-manual.md)
- [Guía de referencia de API](https://learningmanager.adobe.com/docs/primeapi/v2/)

### Formato de solicitud

Tanto __add__ como __remove__ usan exactamente la misma forma de cuerpo.

#### Cuerpo

```
{
  "metadata": {
    "event_id": "my-optional-correlation-id",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

#### datos (obligatorio)

datos es la lista de identificadores de recursos de usuario para este lote.

- `type` debe ser &quot;usuario&quot;.
- `id` es el _ID de usuario numérico_ en ALM (no correo electrónico, no UUID).

#### Restricciones

- `data` debe estar presente y no vacío.
- Se requiere al menos un usuario.
- El tamaño máximo de carga útil es de 20 usuarios por solicitud.
- Todos los ID deben ser numéricos y deben hacer referencia a usuarios válidos.

Si se produce un error en cualquiera de estas condiciones, la API devolverá un error y no se pondrá nada en cola.

#### metadatos (opcional)

`metadata` es cualquier dato de correlación adicional que desee reproducir en el webhook.

Uso típico:

- `event_id`: identificador de correlación generado.
- `sourceSystem`: nombre de su sistema ascendente.
- `batchId`: identificadores de lote o trabajo.

El servicio devuelve este objeto sin cambios en la respuesta Webhook, de modo que puede hacer coincidir la devolución de llamada con su trabajo interno.

Restricciones:

- Opcional; puede omitirse por completo.
- La longitud combinada de todas las claves y valores no debe superar los 1000 caracteres.

### Formato de respuesta

Ambos puntos finales responden de forma sincrónica con un ID de evento:

```
{ "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" }
```

Comportamiento:

- Si se pasa `metadata.event_id`, se usa ese valor.
- De lo contrario, el servicio genera un UUID.

Siempre debes:

- Almacene este `event_id` como identificador principal del lote.
- Espere recibir el mismo valor en la devolución de llamada de Webhook.

Vea [Webhooks para agregar y quitar miembros de grupos de usuarios](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-adding-and-removing-user-group-membership) para obtener más información.

## Preguntas frecuentes

_¿Cómo cambia la versión de abril de 2026 la API learningObjects para programas de aprendizaje adaptables?_

Esta versión añade un indicador isAdaptive en los programas de aprendizaje y proporciona a las secciones y subobjetos información sobre el alumno. En los programas adaptativos, los alumnos solo ven las secciones y los objetos de subaprendizaje que son visibles para ellos en función de las reglas adaptativas, mientras que los administradores pueden ver la configuración adaptativa subyacente de un grupo de usuarios.

_¿Tengo que actualizar mi integración si se supone que siempre se devuelven todas las secciones y subobjetos de aprendizaje?_

Sí. Para los programas de aprendizaje adaptables, la API ahora devuelve solo las secciones y los subobjetos de aprendizaje que son visibles para el alumno actual. El código de cliente debe tratar la respuesta como la vista autorizada y posiblemente filtrada, en lugar de suponer una lista completa.

_¿Cómo puedo restablecer mediante programación la finalización de un alumno para un curso o programa de aprendizaje?_

Utilice el nuevo punto final:

```POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion```
Esto restablece la finalización de la instancia de destino cuando los permisos y el estado lo permiten.

_¿Cómo puedo saber si un alumno ha completado algo a través de un objeto de aprendizaje alternativo o equivalente?_

Compruebe el atributo isAlternateComplete en el objeto de aprendizaje. Si es verdadero, la relación alternativeCompltions muestra los objetos de aprendizaje que actuaron como alternativas para la finalización de ese alumno.

_¿Cómo puedo encontrar todas las alternativas que puedan satisfacer un objeto de aprendizaje en particular?_

Utilice el siguiente punto final:

```GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}```

y utilice la matriz de datos (para las alternativas) y meta.count (para el número total de alternativas).

_¿Cómo sé si un alumno puede iniciar un módulo en este momento?_

En primer lugar, busque el timeSlot del recurso de:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```
y luego use:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

_¿Qué significa ContentDrivenAttemptTracking en un recurso?_

Indica que el seguimiento de intentos está controlado por el propio contenido (por ejemplo, a través de la lógica SCORM/xAPI) en lugar de solo por los contadores de la plataforma. Cuando sea cierto, no confíes únicamente en los recuentos o límites de intentos de plataforma para tu experiencia de usuario e informes.

_¿Cómo puedo obtener menús apropiados para usuarios que no han iniciado sesión (experiencias públicas)?_

Uso:

```GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true```

Esto devuelve estructuras de menú y página filtradas para usuarios anónimos, adecuadas para Experience Builder u otros sitios sin encabezado.

_¿Qué ha cambiado en el filtrado de ayudas de trabajo con effectiveModifiedDate?_

Las solicitudes que combinan filter.effectiveModifiedDate con filter.loTypes=jobAid ahora devuelven correctamente solo las ayudas de trabajo dentro de la ventana de fecha especificada.

_¿Qué ha cambiado en el formato de ID de recurso de ayuda de trabajo y cómo debo gestionarlo?_

El formato de ID ha cambiado de valores como:

```jobAid:<jobAidId>_-1_-1_2_resource```

para:

```jobAid:<jobAidId>_<version>_<localeCode>```

por ejemplo jobAid:131032_2_fr_FR. Cualquier sistema que almacene o analice identificadores de recursos de ayuda de trabajo debe actualizarse y debe planear la reconstrucción de los índices locales marcados por estos identificadores después de actualizar a la versión de abril de 2026.
