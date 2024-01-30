---
jcr-language: en_us
title: Límites de velocidad de API en Learning Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 51%

---



# Límites de velocidad de API en Learning Manager

## Introducción a la limitación de tipos {#introductiontoratelimiting}

Adobe Learning Manager expone una suite completa de API REST que ayuda a los clientes a crear aplicaciones que se integran con Learning Manager, o incluso experiencias de usuario y extensiones personalizadas, para los flujos de trabajo que ayudan a su empresa.

Cada vez que se llama a una API, hay recursos computacionales compartidos que se utilizan en los servidores de Learning Manager, por lo que debemos tener cuidado y precaución para garantizar que las aplicaciones funcionen correctamente y no pongan en peligro las características de rendimiento y disponibilidad de la plataforma. Esto se consigue introduciendo límites en la forma en que los clientes de la API realizan llamadas (frecuencia y velocidad).

Por ejemplo, una aplicación podría estar intentando obtener todos los usuarios de esa cuenta y realizar varias llamadas de API paginadas a una velocidad rápida. Y por error, un desarrollador podría llamar a esto en un bucle apretado que resulta en una gran carga en el servidor y hacer que las aplicaciones sean lentas e incluso poner en peligro la plataforma al consumir más recursos de los que se pretende o se requiere.

Para resolver este problema, estamos introduciendo límites de velocidad en el número de llamadas de API que puede realizar un solo usuario en una aplicación de cliente específica de una cuenta específica. Medimos esto en términos de solicitudes por minuto, abreviadas como RPM. Por ejemplo, cuando decimos que el límite para las llamadas a la API de GET es de 600 RPM, simplemente significa que un solo usuario no puede exceder un máximo de 600 llamadas en un minuto, y si el usuario excede ese límite, el usuario obtendrá una tasa limitada. El seguimiento de las solicitudes se realiza en una granularidad de milisegundos, por lo que este límite corresponde a 1 solicitud cada 100 milisegundos (ms). Hay un parámetro más, llamado Burst, que también se define junto con el límite de velocidad, que define cuántas solicitudes puede realizar un usuario que excedan la velocidad especificada (en nuestro caso, 600 RPM). Por ejemplo, si el parámetro Explosión es 10; significa que se asignarán hasta 10 ranuras en una cola y cuando una solicitud llega &quot;demasiado pronto&quot; (en nuestro caso, antes de 100 ms), se procesa inmediatamente si hay una ranura disponible en la cola. La ranura se marca como &quot;tomada&quot; y no se libera para su uso por otra solicitud hasta que haya pasado el tiempo apropiado (en nuestro caso, después de 100 ms). El tráfico del mundo real suele estar repleto de ráfagas, y ahí es donde ayuda el parámetro Ráfaga. Para la plataforma de Learning Manager, definimos límites para una versión de API específica (por ejemplo, V2), una función (alumno/administrador) y un verbo (GET/PUT/POST/DELETE/PATCH). En el ejemplo, descrito anteriormente diríamos que el límite de tasa es (600, 10).

Aunque siempre hemos tenido límites de velocidad para la API pública en Learning Manager, hasta ahora hemos sido bastante liberales al permitir un RPM muy alto. Sin embargo, con el crecimiento de tu plataforma de aprendizaje favorita, hemos visto un rápido crecimiento en el uso de nuestra API, y hemos decidido hacer que estos límites de tasas se documenten explícitamente para el beneficio de todos nuestros clientes y para una mejor gestión de la plataforma. En este contexto, hemos actualizado nuestra API para empezar a devolver una nueva respuesta de API (código de estado HTTP 429); que no ha visto hasta ahora. Esta respuesta se proporciona a los clientes de API cuando se supera el límite de velocidad. Las aplicaciones cliente ahora tendrán que controlar este código de respuesta como adecuado a la lógica de su aplicación; y este documento está destinado principalmente a ayudar a los desarrolladores con la información que necesitan para incorporar la lógica correcta en su código cuando vean dicha respuesta.

## ¿Cómo se confirman los límites de tarifas aplicados? {#howtoconfirmtheenforcedratelimits}

Para cada solicitud, los encabezados de respuesta contienen la siguiente información:

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit especifica el umbral de tasa de solicitud base en términos de solicitudes por minuto.
* x-burst especifica cuántas solicitudes superiores a la tasa de solicitud base se aceptan para procesarse inmediatamente.

## ¿Cómo detectar los errores causados por los límites de tasas? {#howtocatcherrorscausedbyratelimits}

Para cada solicitud, puede comprobar si se ha topado con el límite de tarifa. Si obtiene un código de respuesta de 429, &quot;{&quot;message&quot;:&quot;429 Too many requests&quot;}&quot;, ha alcanzado el límite de velocidad.

Se recomienda incluir código en el script que detecte 429 respuestas. Si el script omite el error &quot;Demasiadas solicitudes&quot; y sigue intentando realizar solicitudes, es posible que empiece a recibir errores nulos. En ese momento, la información de error no será útil para diagnosticar el problema.

Por ejemplo, una solicitud de rizo que se tope con el límite de velocidad podría devolver la siguiente respuesta:

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

La respuesta contiene información sobre las siguientes claves:

```
status: 429 
retry-after: 10.752
```

El código de estado 429 significa &quot;demasiadas solicitudes&quot; y la solicitud actual no se procesa. El encabezado de reintento tras especifica que puede reintentar la llamada de API en 10.752 segundos. El código debe dejar de realizar solicitudes de API adicionales hasta que haya transcurrido tiempo suficiente para volver a intentarlo.

El siguiente pseudocódigo muestra una forma sencilla de detectar errores de límite de velocidad:

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

De hecho, incluso hemos creado una API ficticia de Learning Manager para que puedas probar y ponerte cómodo manejando el código de estado 429.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Esta API ficticia tiene un límite de:

```
x-rate-limit: 5r/m 
x-burst: 2
```

El límite de la API ficticia es intencionalmente bajo, por lo que se topa con los límites de velocidad muy rápidamente y, a continuación, puede centrarse más en el desarrollo del código para detectar y controlar los errores de límite de velocidad.

## Prueba de la API ficticia {#testingthedummyapi}

Hemos proporcionado un punto final para que pueda comprobar cómo funciona la limitación de velocidad. Para esto, hemos creado un punto final especial llamado GET /dummy que tiene el ámbito de lectura del alumno. Esta API se ha configurado deliberadamente para un límite de velocidad muy estricto de 5 solicitudes por minuto, con límite de ráfaga = 2.

Puede probar fácilmente esto golpeando este punto final con velocidades por debajo de 5 RPM y por encima de 5 RPM. Escriba código para controlar el código de estado HTTPS de 429 y basándose en la información de los encabezados de respuesta.

Para que te resulte más fácil, echa un vistazo a este ejemplo de código JavaScript que ilustra esto. Haga clic en [violín](https://jsfiddle.net/ACAPJS/9yv8zcmL/) y ver el código en acción.

Esta aplicación requiere que proporcione un token de aplicación de la función de alumno para su cuenta. Consulte la [Manual de desarrolladores de aplicaciones](https://captivateLearning Manager.adobe.com/docs/Learning Manager/api/v2/) para obtener información sobre los tokens de API y puede utilizar Token Helper en la sección de recursos para desarrolladores de la aplicación de administración de integración de Learning Manager para generar los tokens.

Esta aplicación está realizando 10 llamadas a la API ficticia en un bucle, de una sola vez. Dado que el límite de velocidad es (5, 2) para la API ficticia, el límite de velocidad se infringirá después de que las primeras llamadas 5+2 recibidas por Learning Manager se realicen correctamente y se obtenga una respuesta de éxito para ellas.

Sin embargo, tenga en cuenta cómo esta aplicación busca el código de estado 429 como respuesta y cómo lo gestiona. Cuando esta aplicación obtiene dicha respuesta, imprime los detalles en la respuesta de la API, espera la cantidad de tiempo sugerida y vuelve a intentar los intentos fallidos.

## Prácticas recomendadas para controlar la limitación de velocidad {#bestpracticestohandleratelimiting}

Muchas veces, los datos de una cuenta no cambian con tanta frecuencia. Por ejemplo, es posible que los cursos de una cuenta no cambien con tanta frecuencia. En lugar de intentar obtener todos los datos cada vez, compruebe si puede obtener los datos específicos cuando los necesite y considere la posibilidad de utilizar un mecanismo de caché. De esta manera, cuando su aplicación realmente necesite realizar muchas llamadas, tendrá suficiente cuota dentro de los límites de la tarifa para realizar esas llamadas importantes.

Algunos datos pueden cambiar con más frecuencia, y puede ser necesario obtenerlos con más frecuencia. Incluso si es así, pregúntese si su aplicación puede permitirse el lujo de tener datos ligeramente obsoletos (algo que puede estar en su caché, que obtuvo hace N minutos), porque puede no tener relación con el flujo de trabajo del usuario. Incluso si necesita obtener datos nuevos de los servidores, puede volver a ser prudente al obtener sólo los datos específicos que necesita, en lugar de obtenerlos todos.

También habrá ocasiones, en las que no tienes opción de obtener muchos datos porque la API puede no ser lo suficientemente flexible como para darte exactamente lo que quieres con solo una llamada. Compruebe si la API proporciona filtros y criterios de ordenación que se puedan utilizar para minimizar el número de llamadas; y siga considerando la posibilidad de almacenar en caché porque muchos usuarios de su cuenta pueden necesitar los mismos datos.

Cuando obtiene demasiados datos en el contexto de una aplicación interactiva con una interfaz gráfica de usuario, es probable que la aplicación intente hacer demasiado y podría abrumar al usuario con mucha información/funcionalidad que afectaría a la experiencia del usuario de la aplicación.

Cuando se está creando una aplicación no interactiva (tal vez algo así como un trabajo diario), es posible que se necesite obtener una gran cantidad de datos en bloque. En estos casos, considere la posibilidad de utilizar la API de trabajos, que está diseñada principalmente para devolver datos en bloque en formato CSV. Tenga en cuenta que la API de trabajos tendrá una restricción de cuota que podrá invocar N veces al día.

Dado que Learning Manager ha implementado las especificaciones de JSONAPI, hay API en las que también puede descargar algunos datos. Esto te ayudará a ahorrar en hacer llamadas API adicionales, pero tendrás que compensar esto con obtener datos con demasiada ansiedad. Dado que los datos descargados pueden ser a veces muy grandes, en las llamadas paginadas de API el tamaño máximo de página se limita a 10; pero para las llamadas de API sin Includes puede especificar un tamaño de página mayor (hasta 100)

Con el tiempo, si realiza muchas solicitudes de API en poco tiempo, se encontrará con el límite de velocidad de API para las solicitudes. Cuando alcance el límite, Learning Manager dejará de procesar más solicitudes hasta que haya transcurrido un determinado período de tiempo.

Los límites de las tasas se describen en la última sección de este artículo. Se recomienda que se familiarice con los límites.

## Límites de velocidad para puntos finales de la API V2 {#ratelimitsforv2apiendpoints}

La siguiente tabla proporciona los límites de los distintos puntos finales de la versión 2. En la actualidad, los límites de tarifas no se imponen a los clientes, pero estos límites se aplicarán a partir del DD/MM/AAAA. Por lo tanto, es importante que los clientes revisen el código de sus aplicaciones existentes para ver cómo pueden ajustar su código para tener en cuenta estos límites de velocidad y gestionar las respuestas de la API con el código de estado HTTP 429.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Operación</b></p></td> 
   <td><p><b>API de administración</b></p></td> 
   <td><p><b>API de alumno</b></p></td> 
  </tr> 
  <tr> 
   <td><p>ELIMINAR</p></td> 
   <td><p>(25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>

