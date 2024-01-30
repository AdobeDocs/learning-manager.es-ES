---
jcr-language: en_us
title: Manual de desarrolladores de aplicaciones
description: La API V1 de Learning Manager ha dejado de utilizarse. Las API V1 dejarán de funcionar a partir del 28 de febrero de 2021. Es recomendable utilizar las API V2 para interactuar con Learning Manager.
contentowner: jayakarr
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '3279'
ht-degree: 64%

---



# Manual de desarrolladores de aplicaciones

La API V1 de Learning Manager ha dejado de utilizarse. Las API V1 dejarán de funcionar a partir del 28 de febrero de 2021. Es recomendable utilizar las API V2 para interactuar con Learning Manager.

## Información general {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) es una solución de gestión del aprendizaje automatizada basada en la nube y centrada en el alumno. Los clientes pueden acceder a los recursos de Learning Manager mediante programación a través de la API de Learning Manager a fin de integrarla con otras aplicaciones empresariales. Asimismo, los socios de Adobe pueden utilizar la API para mejorar la propuesta de valor de Learning Manager ampliando sus funciones o mediante su integración en otros servicios o aplicaciones.

### Escenario de uso {#usagescenario}

Mediante la API de Learning Manager, los desarrolladores pueden crear aplicaciones independientes que amplían las funciones de Learning Manager o que integran esta solución en flujos de trabajo de aplicaciones empresariales. Puede desarrollar una aplicación web, un cliente de escritorio o una aplicación para dispositivos móviles con la tecnología que desee. Como desarrollador, puede acceder a los datos de la aplicación desde Learning Manager. La implementación de la aplicación que desarrolle es externa a la plataforma Learning Manager y tendrá control total sobre el ciclo de vida del desarrollo de software a medida que evolucione la aplicación. Por lo general, las aplicaciones las desarrolla una organización del cliente para su uso con la cuenta de Learning Manager. Estas aplicaciones son privadas en esa organización de cliente específica. Además, los socios de Adobe pueden crear aplicaciones genéricas con la API de Learning Manager, que pueden utilizar un gran conjunto de clientes de Learning Manager.

## API de Learning Manager {#apidescription}

La API de Learning Manager se basa en los principios de REST y presenta elementos clave del modelo de objetos de Learning Manager a los desarrolladores de aplicaciones mediante HTTP. Antes de conocer los detalles de los puntos finales de la API y los métodos HTTP, los desarrolladores pueden familiarizarse con los diferentes objetos de Learning Manager, sus atributos y sus interrelaciones. Una vez que se conozcan los modelos, resultará útil tener nociones básicas sobre la estructura de las solicitudes y respuestas de la API y de algunos lenguajes de programación conocidos que se admiten de modo genérico en ella.

Para obtener más información sobre los distintos métodos y puntos finales de la API, consulte la  [Documentación de API de Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## Autenticación de API {#apiauthentication}

Al escribir una aplicación que realiza llamadas de API a Learning Manager, debe registrarla mediante la aplicación del administrador de integración.

Las API de Learning Manager utilizan el marco de OAuth 2.0 para autenticar y autorizar las aplicaciones cliente.

**Procedimiento**

**1. Configurar la aplicación**

Puede configurar la aplicación con el ID y el secreto de cliente para utilizar los puntos finales adecuados. Una vez registrada la aplicación, puede obtener el ID y el secreto de cliente. Se debe utilizar &quot;Get URL&quot; en el navegador, ya que autentica a los usuarios de Learning Manager mediante sus cuentas preconfiguradas, como SSO, Adobe ID, etc.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Una vez completada correctamente la autenticación, el navegador redirige al URI de redirección indicado en la URL anterior. Se añade el parámetro **code** junto al URI de redirección.

**2. Obtener token de actualización del código**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Cuerpo de la solicitud POST:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  code: 
  <code from step 1></code>
 </enter>
</enter>
```

**3.** **Obtener un token de acceso a partir del token de actualización**

URL para obtener el token de acceso:

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type: application/x-www-form-urlencoded

Cuerpo de la solicitud POST:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  refresh_token: 
  <refresh token>
   
  </refresh>
 </enter>
</enter>
```

**URL para verificar los detalles del token de acceso**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Limitación de uso**

Un token de acceso es válido durante siete días. Después de un día, debe generar un nuevo token de acceso mediante el token de actualización. Si genera un nuevo token de acceso a partir del token de actualización mientras un token de acceso existente sigue siendo válido, se devuelve el token existente.

A continuación, se describen algunos de los términos más utilizados en la API de Learning Manager como referencia.

**Includes**

Los desarrolladores pueden acceder a un único modelo de objetos de API y también a varios modelos asociados a ese modelo. Para acceder a los modelos relacionados posteriores, debe conocer la relación de cada modelo con otros modelos. **Incluye** permite a los desarrolladores acceder a los modelos dependientes. Puede utilizar un separador de comas para acceder a varios modelos. Para ver ejemplos de uso y obtener más información sobre **incluye**, consulte la sección de modelo de API de ejemplo de esta página.

**Solicitud de API**

Las solicitudes de API se pueden realizar mediante una solicitud HTTP. En función del punto final y el método, el desarrollador puede elegir entre diversos verbos de HTTP, como GET, PUT, POST, DELETE, PATCH, etc. En algunas solicitudes, se pueden transferir parámetros de consulta. Al realizar una solicitud de un modelo de datos específico, el usuario también puede solicitar modelos relacionados, tal y como se describe en las especificaciones de la API JSON. La estructura de una solicitud API típica se describe en el [uso del modelo de ejemplo](#main-pars_header_1415780624).

**Respuesta de API**

Si un cliente realiza una solicitud de API, se obtiene un documento JSON según la especificación de API JSON. La respuesta también contiene el código de estado HTTP, que el desarrollador puede comprobar para realizar los pasos siguientes adecuados en la lógica de la aplicación. La estructura de una respuesta de API típica se describe en  [uso del modelo de muestra](#main-pars_header_1415780624).

**Errores**

Cuando falla una solicitud de API, se obtiene una respuesta de error. El código de estado HTTP devuelto en la respuesta indica la naturaleza del error. Los códigos de error se representan con números para cada modelo en la referencia de API. 200, 204, 400 y 404 son algunos de los errores comunes representados en las API que indican problemas de acceso HTTP.

**Fields**

Los atributos del objeto de API y sus relaciones se denominan de forma conjunta &quot;Fields&quot;. Consulte la [API JSON para obtener más información.](http://jsonapi.org/format/#document-resource-object-fields) Puede utilizar &quot;Fields&quot; como parámetro al realizar llamadas de API para obtener uno o más atributos específicos del modelo. Si no se utiliza el parámetro &quot;Fields&quot;, la llamada de API obtiene todos los atributos disponibles del modelo. Por ejemplo, en la siguiente llamada de API, los campos[habilidad]=name obtiene únicamente el atributo name del modelo de aptitud.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Paginación**

A veces, una solicitud de API proporciona una larga lista de objetos en la respuesta. En esos casos, el atributo de paginación permite al desarrollador obtener los resultados secuencialmente en varias páginas, en las que cada página contiene un intervalo de registros. Por ejemplo, el atributo de paginación en Learning Manager permite establecer el número máximo de registros que se mostrarán en una página. Además, puede definir el valor del intervalo de registros que se mostrarán en la página.

**Ordenación**

Se permite la ordenación en los modelos de API. En función del modelo, elija el tipo de ordenación que se aplicará a los resultados. La ordenación se puede aplicar en orden ascendente o descendente. Por ejemplo, si especifica `code sort=name`, luego es una ordenación ascendente por nombre. Si especifica `code sort=-name`, es una ordenación descendente por nombre. Consulte la [Especificación de API JSON para obtener más información](http://jsonapi.org/format/#fetching-sorting).

## Ilustración de uso de API {#samplemodel}

Supongamos que un desarrollador desea obtener el nombre de la aptitud, la cantidad máxima de puntos asignada al nivel de aptitud y los puntos obtenidos por el alumno para esa aptitud.

Un modelo &quot;userSkill&quot; de las API de Learning Manager consta de los atributos predeterminados: id, type, dateAchived, dateCreated y pointsEarned. Por lo tanto, cuando un desarrollador utiliza el método GET para adquirir información del modelo &quot;userSkill&quot;, los datos actuales relativos a los atributos predeterminados se muestran en la salida de respuesta.

Sin embargo, en este caso, el desarrollador desea obtener el nombre de la aptitud y los puntos de nivel de aptitud del usuario. La API de Learning Manager permite acceder a esta información relacionada mediante campos de relación y parámetros &quot;include&quot;. Los modelos asociados de &quot;userSkill&quot; se obtienen en la etiqueta de relaciones. Puede obtener información de cada uno de los modelos asociados llamándolos junto con el modelo &quot;userSkill&quot;. Para obtener esta información, utilice **`code include`** parámetro con valores separados por puntos para cada uno de los modelos asociados. Puede utilizar la coma como separador para solicitar otro modelo, como user include=skillLevel.skill,course

**Llamada de API**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Por ejemplo, &quot;userId&quot; puede ser 746783 y &quot;userSkills id&quot; puede ser 746783_4426_1.

**Respuesta de llamada de API**

```
\{ 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1?include=skillLevel.skill&fields[userSkill]=pointsEarned&fields[skillLevel]=maxCredits&fields[skill]=name"}, 
 "data": { 
 "id": "746783_4426_1", 
 "type": "userSkill", 
 "attributes": {"pointsEarned": 5}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1"} 
 }, 
 "included": [ 
 { 
 "id": "4426", 
 "type": "skill", 
 "attributes": {"name": "Java"}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/skills/4426"} 
 }, 
 { 
 "id": "4426_1", 
 "type": "skillLevel", 
 "attributes": {"maxCredits": 10} 
 } 
 ] 
} 
```

## Modelos de Learning Manager {#models}

La API de Learning Manager permite que los desarrolladores accedan a los objetos de Learning Manager como recursos RESTful. Cada punto final de la API representa un recurso, por lo general, una instancia de objeto como una insignia o una colección de esos objetos. Así, los desarrolladores utilizan verbos de HTTP como PUT, GET, POST y DELETE para efectuar operaciones CRUD en esos objetos (colecciones).

API +++V1

El siguiente diagrama representa los distintos elementos del Modelo de objetos de Learning Manager de la API V1.

![](assets/er-diag-primemodels.png)

En la siguiente tabla se describen varios elementos del modelo de objetos de Learning Manager V1:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>N.º de serie</strong></p></td>
   <td>
    <p><strong>Objeto de Learning Manager</strong></p></td>
   <td>
    <p><strong>Descripción</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>interfaz</p></td>
   <td>
    <p>El usuario es el modelo clave en Learning Manager. Por lo general, los usuarios son los alumnos internos o externos de una organización que consumen objetos de aprendizaje. Sin embargo, pueden desempeñar otras funciones, como la de autor o responsable, junto con la función de alumno. El ID de usuario, el tipo y la dirección de correo electrónico son algunos de los atributos integrados. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>curso</p></td>
   <td>
    <p>El curso es uno de los objetos de aprendizaje admitidos en Learning Manager y consta de uno o varios módulos. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>módulo</p></td>
   <td>
    <p>El módulo es un componente básico para crear objetos de aprendizaje en Learning Manager. Los módulos pueden ser de cuatro tipos diferentes, como clase, clase virtual, actividad y ritmo personalizado. Utilice este modelo de módulo para obtener información sobre todos los módulos de una cuenta. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certificación</p></td>
   <td>
    <p>La certificación se concede a los alumnos al finalizar con éxito los cursos. Se deben incluir cursos en la aplicación antes de utilizar las certificaciones. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>programa de aprendizaje</p></td>
   <td>
    <p>Los programas de aprendizaje son cursos diseñados de forma exclusiva que cumplen los requisitos de aprendizaje específicos de los usuarios. Por lo general, los programas de aprendizaje se utilizan para impulsar objetivos de aprendizaje que abarcan varios cursos individuales. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>insignia</p></td>
   <td>
    <p>La insignia es una muestra de los logros que obtienen los alumnos cuando alcanzan hitos específicos mientras avanzan en un curso. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>skill</p></td>
   <td>
    <p>El modelo de aptitudes consta de niveles y créditos. Los alumnos pueden adquirir aptitudes una vez completado el curso correspondiente. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Este modelo proporciona información sobre la inscripción de un usuario en una única certificación.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Este modelo proporciona información sobre la inscripción de un usuario en un único curso. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Un curso puede tener una o varias instancias asociadas. Puede obtener la instancia del curso </p></td>
  </tr>
  <tr>
   <td>
    <p>11.  </p></td>
   <td>
    <p>courseSkill</p></td>
   <td>
    <p>Un modelo courseSkill especifica el progreso de una única aptitud que se consigue al completar un curso.</p></td>
  </tr>
  <tr>
   <td>
    <p>12.  </p></td>
   <td>
    <p>courseModule</p></td>
   <td>Un modelo courseModule especifica cómo se incluye un módulo en un curso. Por ejemplo, si el módulo se utiliza para pruebas preliminares o para contenido.</td>
  </tr>
  <tr>
   <td>
    <p>13.  </p></td>
   <td>learningProgramInstance</td>
   <td>
    <p>Un programa de aprendizaje puede constar de diversas instancias que imbuyen propiedades similares de un programa de aprendizaje o instancias personalizadas. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>ayuda de trabajo</p></td>
   <td>
    <p>La ayuda de trabajo es un contenido de aprendizaje al que pueden acceder los alumnos sin ningún criterio de inscripción o finalización. Puede obtener la fecha de actualización, el estado y la información de identificación, junto con sus modelos relacionados, como la versión de la ayuda de trabajo, los autores y el nivel de aptitud. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>La ayuda de trabajo puede tener una o varias versiones asociadas según el número de revisiones en el contenido y el número de cargas. Este modelo proporciona información de una única versión de ayuda de trabajo. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>El programa de aprendizaje consta de una o varias instancias. Los alumnos pueden inscribirse en una instancia de programa de aprendizaje por sí mismos o asignados por el administrador. Este modelo proporciona información de la inscripción de un usuario en una única instancia de programa de aprendizaje. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Un módulo puede tener una o varias versiones en función de las cargas de contenido modificado. Utilice este modelo para obtener información específica sobre cualquier versión del módulo. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Un nivel de aptitud consta de uno o varios cursos que se van a consumir para adquirir un nivel, junto con sus créditos asociados. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge relaciona una única insignia con un único usuario. Contiene información como, por ejemplo, cuándo se logró, assertionUrl, etc. </p></td>
  </tr>
  <tr>
   <td>
    <p>20.  </p></td>
   <td>
    <p>userSkill</p></td>
   <td>
    <p>Indica el porcentaje de una única aptitud que ha alcanzado un solo usuario.</p></td>
  </tr>
 </tbody>
</table>

+++

API +++V2

A continuación, se muestran los distintos elementos del diagrama de clases de Learning Manager de la API V2.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Objeto de Learning Manager</b></th>
   <th><b>Descripción</b></th>
  </tr>
  <tr>
   <td>account</td>
   <td>Engloba los detalles de un cliente de Learning Manager.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>La insignia es una muestra de los logros que obtienen los alumnos cuando alcanzan hitos específicos mientras avanzan en un curso. <br></td>
  </tr>
  <tr>
   <td><code>
     catalog
    </code></td>
   <td>El catálogo es una colección de objetos de aprendizaje.</td>
  </tr>
  <tr>
   <td><code>
     user
    </code></td>
   <td>El usuario es el modelo clave en Learning Manager. Por lo general, los usuarios son los alumnos internos o externos de una organización que consumen objetos de aprendizaje. Sin embargo, pueden desempeñar otras funciones, como la de autor o responsable, junto con la función de alumno. El ID de usuario, el tipo y la dirección de correo electrónico son algunos de los atributos integrados. </td>
  </tr>
  <tr>
   <td>resource</td>
   <td>Se utiliza para modelar cada recurso de contenido que un módulo busca englobar. Todos los recursos encapsulados en <code>
     an
    </code> <code>
     loResource
    </code> son equivalentes en términos del objetivo de aprendizaje, pero difieren entre sí en términos de tipo de entrega o configuración regional del contenido.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Este modelo contiene información de notificación relativa a un alumno.<br></td>
  </tr>
  <tr>
   <td>userSkill</td>
   <td>Indica el porcentaje de una única aptitud que ha alcanzado un solo usuario.<br></td>
  </tr>
  <tr>
   <td>userBadge</td>
   <td>UserBadge relaciona una única insignia <code>
     with
    </code> un único usuario. Contiene detalles como cuándo se logró, <code>
     assertionUrl
    </code> y así. <br></td>
  </tr>
  <tr>
   <td>skill</td>
   <td>El modelo de aptitudes consta de niveles y créditos. Los alumnos pueden adquirir aptitudes una vez completado el curso correspondiente. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Un nivel de aptitud consta de uno o varios cursos que se van a consumir para adquirir un nivel, junto con sus créditos asociados. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Un objeto de aprendizaje es una abstracción de varios tipos de objetos en los que los usuarios pueden inscribirse y con los que pueden aprender. Actualmente, Learning Manager dispone de cuatro tipos de objetos de aprendizaje: curso, certificación y programa de aprendizaje <code>
     and
    </code> Ayuda de trabajo.<br></td>
  </tr>
  <tr>
   <td>learningObjectInstance<br></td>
   <td>Una instancia específica de un objeto de aprendizaje.<br></td>
  </tr>
  <tr>
   <td>learningObjectResource</td>
   <td>Esto es equivalente al concepto de <code>
     module
    </code>. Un curso se compone de uno <code>
     of
    </code> más módulos. En Learning Manager, un módulo se puede entregar de diversas formas equivalentes. Por lo tanto, <code>
     loResource
    </code> básicamente engloba todos esos recursos equivalentes.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Engloba el resultado del usuario que consume un recurso específico en el contexto de un objeto de aprendizaje en el que está inscrito. Tiene información como la duración que ha pasado <code>
     user
    </code> en el recurso, el porcentaje de progreso realizado por el usuario, el estado de aprobado/suspenso y la puntuación obtenida por el usuario en cualquier prueba asociada.<br></td>
  </tr>
  <tr>
   <td>calendar<br></td>
   <td>Un objeto de calendario es una lista de <code>
     upcoming classroom
    </code> o cursos de clase virtual en los que puede inscribirse el usuario.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>Los comentarios de L1 engloban las respuestas proporcionadas por un alumno para las preguntas de comentarios asociadas a los objetos de aprendizaje. Por lo general, esta información se recopila una vez que el usuario ha completado un objeto de aprendizaje si se ha configurado la recopilación de esa información de los alumnos.<br></td>
  </tr>
  <tr>
   <td>enrollment<br></td>
   <td>Esta abstracción engloba los detalles relativos a la transacción que representan la asignación de un usuario específico a una determinada instancia de objeto de aprendizaje.<br></td>
  </tr>
 </tbody>
</table>

+++

Lista de atributos de objeto y relaciones.

+++cuenta

**Atributos**
dateCreated\
gamificationEnabled\
id\
configuración regional\
loginUrl\
logoUrl\
name\
subdominio\
themeData\
timeZoneCode

**Relaciones**
contentLocales(localizationMetadata)\
gamificationLevels(gamificationLevel)\
timeZones(timeZone)\
uiLocales(localizationMetadata)

+++

+++insignia

**Atributos**
id\
imageUrl\
name\
estado

+++

+++catálogo

**Atributos**
dateCreated\
dateUpdated\
descripción\
id\
isDefault\
isInternallySearchable\
isListable\
name\
estado

+++

+++datos

**Atributos**
id\
nombres

+++

+++interacción

**Atributos**
color\
name\
puntos

+++

+++learningObject

**Atributos**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectivenessIndex\
enrollmentType\
id\
imageUrl\
isExternal\
isSubLoOrderEnforced\
loType\
estado\
etiquetas

**Relaciones**
authors(user)\
enrollment(learningObjectInstanceEnrollment)\
instancias(learningObjectInstance)\
prerrequisitos(learningObject)\
skills(learningObjectSkill)\
subLOs(learningObject)\
AdditionalLOs(learningObject)\
suplementarioResources(recurso)

+++

+++learningObjectInstance

**Atributos**
completedDeadline\
dateCreated\
enrollmentCount\
id\
isDefault\
seatLimit\
estado\
validez

**Relaciones**
badge(badge)\
l1FeedbackInfo(feedbackInfo)\
learningObject(learningObject)\
loResources(learningObjectResource)\
localizedMetadata(localizationMetadata)\
subLoInstances(learningObjectInstance)

+++

+++learningObjectInstanceEnrollment

**Atributos**
dateCompleted\
dateEnrolled\
dateStarted\
hasPassed\
id\
progressPercent\
puntuación\
estado

**Relaciones**
learner(user)\
learnerBadge(userBadge)\
learningObject(learningObject)\
loInstance(learningObjectInstance)\
loResourceGrades(learningObjectResourceGrade)

+++

+++learningObjectResource

**Atributos**
externalReporting\
id\
loResourceType\
resourceType\
versión

**Relaciones**
learningObject(learningObject)\
loInstance(learningObjectInstance)\
localizedMetadata(localizationMetadata)\
resources(resource)

+++

+++learningObjectResourceGrade

**Atributos**
dateCompleted\
dateStarted\
dateSuccess\
duración\
hasPassed\
id\
progressPercent\
puntuación

**Relaciones**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Atributos**
créditos\
id\
**Relaciones**
learningObject(learningObject)\
skillLevel(skillLevel)

+++

+++recomendación

**Atributos**
id\
razonar

**Relaciones**
learningObject(learningObject)

+++

+++recurso

**Atributos**
authorDesiredDuration\
completedDeadline\
contentStructureInfoUrl\
contentType\
contentZipSize\
contentZipUrl\
dateCreated\
dateStart\
deseadoDuración\
downloadUrl\
extraData\
hasQuiz\
hasToc\
id\
instructorNames\
isDefault\
configuración regional\
ubicación\
name\
onlyQuiz\
reportingInfo\
reportingType\
seatLimit

+++

+++aptitud

**Atributos**
descripción\
id\
name\
estado

**Relaciones**
levels(skillLevel)

+++

+++nivelDeAptitud

**Atributos**
id\
nivelar\
maxCredits\
name\
**Relaciones**
badge(badge)\
skill(skill)

+++

+++usuario

**Atributos**
avatarUrl\
biografía\
contentLocale\
correo electrónico\
campos\
id\
name\
pointsEarned\
perfil\
ROLE\
estado\
timeZoneCode\
uiLocale

**Relaciones**
account(account)\
manager(user)

+++

+++userBadge

**Atributos**
assertionUrl\
dateAchived\
id\
modelType

**Relaciones**
badge(badge)\
learner(user)\
model(learningObject)

+++

+++calendarioDeUsuario

**Atributos**
curso\
courseType\
dateStart\
inscrito\
id\
mes\
cuartear

**Relaciones**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Atributos**
actionTaken\
canal\
dateCreated\
id\
mensaje\
modelIds\
modelNames\
modelTypes\
leer\
ROLE

+++

+++userSkill

**Atributos**
dateAchived\
dateCreated\
id\
pointsEarned

**Relaciones**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
usuario(usuario)

+++

## Proceso de desarrollo de aplicaciones {#registration}

## Requisitos previos {#prerequisites}

Como desarrollador, debe crear una cuenta de prueba en Learning Manager para poder tener acceso completo a todas las funciones de esa cuenta. Asimismo, para poder escribir una aplicación, el desarrollador debe crear varios usuarios y cursos, y lograr que la cuenta tenga un estado razonable para que la aplicación que se desarrolla tenga acceso a datos de ejemplo.

## Crear el ID y el secreto de cliente {#createclientidandsecret}

1. En **Administrador de integración** inicio de sesión, haga clic en **[!UICONTROL Aplicaciones]** en el panel izquierdo.

   ![](assets/application-development-menu.png)

   *Seleccionar aplicaciones en el administrador de integración*

1. Haga clic en **[!UICONTROL Registro]** en la esquina superior derecha de la página para registrar los detalles de la aplicación. Aparece la página de registro.

   ![](assets/register-application.png)

   *Registrar la aplicación*

   Es obligatorio rellenar todos los campos de esta página.

   **Nombre de la aplicación**: introduzca el nombre de la aplicación. No es obligatorio utilizar el mismo nombre de aplicación, puede ser cualquier nombre válido.

   **URL**: si conoce la dirección URL exacta en la que se aloja la aplicación, puede especificarla. Si no lo sabe, puede indicar la URL de su empresa. El nombre de URL válido es obligatorio en este campo.

   **Dominios de redirección**: introduzca el nombre de dominio de la aplicación a la que desea que se redirija la aplicación de Learning Manager después de la autenticación de OAuth. Puede mencionar varias direcciones URL aquí, pero debe utilizar direcciones URL válidas como `http://google.com`, `http://yahoo.com` y así.

   **Descripción:** Introduzca una breve descripción de la aplicación.

   **Ámbitos:** Elija una de las cuatro opciones disponibles para definir el ámbito de la aplicación. En función de su elección, los puntos finales de la API de Learning Manager están accesibles para la aplicación. Por ejemplo, Si elige **Acceso de lectura de la función Alumno**, todos los puntos finales de la API de alumno de Learning Manager son de solo lectura accesibles para la aplicación.

   **¿Solo para esta cuenta?**\
   **Sí** - si elige Sí, la aplicación no estará visible para otros administradores de cuentas.\
   **No** - Si elige No, otros administradores de cuentas también pueden acceder a esta aplicación, pero deben utilizar el ID de aplicación para acceder a ella. El ID de aplicación se genera y se muestra en el modo de edición de la aplicación de Learning Manager.

   Si elige **Acceso de lectura y escritura de la función de administrador** como ámbito al registrar la aplicación y elija **Acceso de lectura de la función de administrador** al crear las API, puede seguir teniendo acceso de escritura para la aplicación, ya que el ámbito de registro de la aplicación sustituye al flujo de trabajo de autorización.

1. Haga clic en **[!UICONTROL Registrar]** en la esquina superior derecha después de completar la información de la página de registro.

## Desarrollo y prueba de aplicaciones {#applicationdevelopmentandtesting}

Los desarrolladores pueden utilizar la API de Learning Manager para crear cualquier aplicación. Estos deben asegurarse de que sus cuentas incluyan algunos usuarios y cursos válidos. Pueden crear algunos usuarios y cursos ficticios y simular actividad en la cuenta de prueba para que puedan probar la funcionalidad de la aplicación.

## Implementación de aplicaciones {#applicationdeployment}

Es recomendable que el administrador de Learning Manager o un administrador de integración de la cuenta de producción asuman la responsabilidad de facilitar la aplicación a los usuarios de su organización. Una vez que la aplicación se haya probado y se considere lista para la producción, informe al administrador de la cuenta de producción. Lo ideal es que los administradores generen un nuevo ID y secreto de cliente para la aplicación en la cuenta de producción y realicen los pasos necesarios para incorporarlos en la aplicación de forma segura. El procedimiento real de implementación de aplicaciones varía de una empresa a otra y el administrador de Learning Manager de su organización debe obtener asistencia del departamento de TI/SI de su organización para completar la implementación.

## Aprobación de aplicaciones externas {#externalapplicationapproval}

Puede agregar aplicaciones externas haciendo clic en **Aprobar** en la esquina superior derecha del **Aplicaciones** página. Indique el ID de la aplicación externa y haga clic en **Guardar**.

![](assets/add-external-application.png)

*Agregar y aprobar una aplicación externa*

## Preguntas más frecuentes

+++¿Learning Manager tiene una integración de comercio electrónico?

Adobe Learning Manager no incluye una integración de comercio electrónico. Sin embargo, proporcionamos API para que pueda crear su propio LMS sin encabezado e implementar funciones de comercio electrónico.
+++
