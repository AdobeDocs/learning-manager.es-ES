---
description: Explica cómo Experience Builder puede publicar páginas de aprendizaje y catálogos orientados al público para visitantes anónimos, incluidas las funciones clave, los widgets admitidos, los requisitos previos (Training Data Access Connector), las limitaciones y las directrices para la configuración, la escalabilidad y la migración desde la página principal antigua no conectada.
jcr-language: en_us
title: Configurar y administrar páginas sin sesión iniciada en Experience Builder
exl-id: e4685cab-08ca-4b6b-93f4-a9eecf382dc4
source-git-commit: ef6f7a9acd27b7fb4c08fe9a8b366d628d199050
workflow-type: tm+mt
source-wordcount: '6051'
ht-degree: 1%

---


# Introducción

La experiencia sin iniciar sesión en Experience Builder permite a las organizaciones mostrar su contenido de aprendizaje y páginas del portal a todos los visitantes, incluidos los que no han iniciado sesión. Esta función está diseñada para atraer, informar e interactuar con posibles alumnos, ya que ofrece una vista previa fluida y de marca de sus ofertas de formación antes de solicitarles que inicien sesión o se inscriban.

Esta función te permite crear y personalizar páginas públicas mediante la misma interfaz de arrastrar y soltar fácil de usar que se encuentra en el Experience Builder estándar. Puede mostrar catálogos de cursos, categorías, rutas y contenido estático enriquecido, incluidas imágenes, texto, HTML e iframes incrustados, para cualquiera que visite su portal. Esto facilita resaltar los programas de aprendizaje, promover nuevos cursos y proporcionar información esencial a un público más amplio.

Los visitantes pueden examinar el catálogo, ver detalles sobre los cursos e instancias y utilizar la búsqueda global para explorar las oportunidades de formación disponibles. Sin embargo, las acciones que requieren la identidad de un usuario, como inscribirse en un curso, acceder a funciones personalizadas (como Calendario, Cumplimiento, Tabla de posiciones o Aprendizaje social) o consumir formación, solicitarán al visitante que inicie sesión. Este enfoque garantiza que la información confidencial y personalizada permanezca segura, al tiempo que permite una experiencia de previsualización completa.

Los administradores pueden configurar qué páginas y widgets pueden ver los usuarios que no han iniciado sesión, lo que garantiza que solo se muestre el contenido adecuado. Las páginas se pueden configurar para que sean accesibles tanto para los usuarios que hayan iniciado sesión como para los que no, o exclusivamente para uno de estos grupos. Experience Builder ofrece un modo de vista previa, que te permite ver exactamente cómo aparecerán las páginas a los visitantes antes de que se publiquen.

Para habilitar esta función, el administrador de integración de ALM debe activar el conector de acceso a datos de formación. Este conector garantiza que los metadatos del curso sean de acceso público.

La promoción de la marca y la localización son totalmente compatibles, lo que te permite personalizar los títulos de las páginas, los favoritos y la configuración de idioma para adaptarlos a la identidad de tu organización y a las necesidades de tu audiencia. Como parte de la transición a esta experiencia mejorada, la función heredada de la página de inicio para los usuarios que no hayan iniciado sesión quedará obsoleta. Por lo tanto, todo el nuevo contenido público debe crearse utilizando Experience Builder.

## Propósito de la función

La experiencia sin iniciar sesión en Experience Builder permite a las organizaciones mostrar públicamente el contenido de aprendizaje y las páginas del portal a cualquiera, sin necesidad de que los usuarios inicien sesión. Esto ayuda a atraer, informar e interactuar con posibles alumnos al proporcionar una vista previa de la formación y los recursos disponibles antes de la inscripción o la autenticación.

## Casos prácticos del mundo real en la experiencia de inicio de sesión no registrado

- **Marketing y divulgación**: las organizaciones pueden promocionar sus programas de formación a audiencias externas, como clientes potenciales, socios o solicitantes de empleo, haciendo que los catálogos de los cursos y los detalles del programa sean de acceso público.
- **Exploración previa a la inscripción**: Los alumnos pueden examinar los cursos disponibles, consultar información general y explorar las categorías antes de decidir si se inscriben o inician sesión, lo que les ayuda a tomar decisiones fundamentadas sobre la inscripción.
- **Portales de formación corporativa**: Las empresas pueden proporcionar un portal público con información de cumplimiento o incorporación, lo que permite a los nuevos empleados o contratistas ver qué formación está disponible antes de recibir las credenciales.
- **Páginas de aterrizaje de eventos o campañas**: Las organizaciones que ejecutan campañas o eventos de aprendizaje pueden crear páginas públicas dedicadas para resaltar cursos, horarios o recursos destacados, lo que aumenta la visibilidad y la participación.
- **SEO y capacidad de detección**: al hacer públicas determinadas páginas y catálogos, las organizaciones mejoran la visibilidad de sus motores de búsqueda, lo que facilita que las personas descubran sus ofertas de aprendizaje en línea.

## Conceptos clave de la experiencia de inicio de sesión no registrado

La experiencia sin iniciar sesión de Experience Builder le permite mostrar públicamente el contenido de aprendizaje y las páginas del portal, lo que permite a los visitantes explorar sin iniciar sesión.

- **Crear páginas y menús públicos**: Configuras páginas y un solo menú al que todos pueden acceder, independientemente del estado de inicio de sesión.
- **Agregar solo widgets compatibles**: se incluyen los widgets que no necesitan contexto de usuario (categorías, cursos y rutas de aprendizaje, cuadro de contenido, HTML, iframe), mientras que el sistema oculta los widgets específicos del usuario.
- **Configurar el comportamiento de la página adaptable**: decides si aparece una página para los usuarios que han iniciado sesión o no, y el sistema adapta los widgets visibles y el contenido en función del estado de inicio de sesión.
- **Vista previa de ambas experiencias**: Utiliza las opciones de vista previa para ver el aspecto de las páginas para los usuarios que han iniciado sesión o no, con diferencias en la visibilidad y el contenido de los widgets.
- **Habilitar búsqueda global**: Los visitantes buscan cursos y contenido, pero solo obtienen las funciones de búsqueda básicas sin integración avanzada de IA.
- **Permite a los visitantes examinar el catálogo y las descripciones generales de los cursos**: Los visitantes exploran páginas de catálogos, detalles de cursos e instancias, pero deben iniciar sesión para inscribirse o acceder a funciones personalizadas.
- **Personaliza la construcción de marca y la localización**: Establece favoritos y configuraciones de idioma para que coincidan con las necesidades de construcción de marca y accesibilidad de tu organización.
- **Habilitar el conector de acceso a datos de formación**: active este conector para exportar los metadatos del curso para su visualización pública, con lo que las páginas que no estén conectadas se mantendrán actualizadas.
- **Controlar el alto tráfico con la infraestructura compartida**: el sistema administra grandes volúmenes de visitantes anónimos utilizando recursos compartidos y límites de velocidad.
- **Optimizar para SEO**: La plataforma prepara páginas públicas para la indexación de motores de búsqueda, lo que facilita la búsqueda del contenido de aprendizaje.

## Requisitos previos para la experiencia sin sesión iniciada

- Debe habilitar el conector de acceso a datos de formación en el administrador de integración para poder utilizar la experiencia de inicio de sesión no registrado.
- El conector exporta los metadatos del curso a un repositorio público, que mantiene actualizadas las páginas que no han iniciado sesión.

### Inicialización del conector TDA

El conector de Acceso a datos de formación (TDA) es un requisito previo esencial para habilitar la nueva función de generador de experiencias sin conexión en ALM. Este conector facilita la exportación de metadatos de formación, lo que permite que el portal muestre información del curso a los usuarios que no hayan iniciado sesión.

- **Activación del conector**: debe habilitar el conector TDA desde el panel de administración de integración. Este paso desbloquea la funcionalidad del generador de experiencias que no ha iniciado sesión y hace que las opciones de interfaz de usuario relevantes estén visibles en la interfaz de administración.
- **Exportación de metadatos**: una vez activada, el conector exporta los metadatos de formación esenciales (como el nombre del curso, la descripción, la información general, la clasificación, la duración y las aptitudes) de ALM a un repositorio público. Estos datos se utilizan para rellenar páginas y widgets que no han iniciado sesión.
- **Programación y sincronización**: El proceso de exportación se puede programar (por ejemplo, diariamente) para garantizar que en el portal se reflejen las últimas actualizaciones del curso. Los cambios realizados en ALM aparecerán en las páginas que no hayan iniciado sesión después del siguiente ciclo de exportación, sujetos al almacenamiento en caché y a la frecuencia de exportación.
- **Disponibilidad de la función**: Solo se puede acceder a las funciones del generador de experiencias que no haya iniciado sesión, como la creación de menús, la compatibilidad con widgets y la visibilidad del catálogo, una vez que se haya inicializado el conector de TDA. Si el conector no está habilitado, el generador de experiencias seguirá estando limitado a los escenarios de usuarios que hayan iniciado sesión.
- **Migración y soporte**: Para las cuentas que realizan la transición desde funciones heredadas de la página de inicio sin inicio de sesión, inicializar el conector de TDA es el primer paso hacia la migración. Garantiza que puedes aprovechar la flexibilidad del nuevo creador de experiencias y las capacidades mejoradas.

## Qué pueden hacer los visitantes sin iniciar sesión

En un sitio de Experience Builder que no esté conectado, los visitantes pueden examinar el catálogo de formación abriendo la página del catálogo para catálogos públicos. Pueden utilizar filtros como catálogo, producto, función, tipo, aptitudes y etiquetas, dependiendo de cómo haya configurado el sitio. Los visitantes también pueden buscar cursos de formación mediante la barra de búsqueda global en el encabezado (si está activada) y ver los resultados de búsqueda directamente en la página del catálogo.

Los visitantes pueden ver los detalles de la formación abriendo páginas de información general de cursos, rutas de aprendizaje y certificaciones. Estas páginas muestran metadatos clave, incluidos el título, la descripción, el autor, la duración, el formato, las etiquetas y las aptitudes.

Además, los visitantes pueden explorar contenidos estáticos y promocionales. Pueden leer bloques de texto y contenido enriquecido, ver banners y mosaicos de imágenes e interactuar con iframes incrustados como micrositios externos, vídeos o herramientas.

Si un visitante hace clic en Inscribir o intenta comenzar a entrenar, el sistema le pedirá que inicie sesión o que se registre. Después de iniciar sesión correctamente, se redirige al visitante a la página adecuada, ya sea la página principal, una página personalizada o la formación específica que ha seleccionado.

## Lo que no está disponible sin iniciar sesión

En un sitio de Experience Builder que no tenga iniciada sesión, los visitantes no pueden acceder a las funciones o al contenido que requieran autenticación del usuario. No pueden inscribirse en cursos de formación, iniciar o consumir cursos, ni acceder a widgets personalizados como Mi aprendizaje, Calendario, Cumplimiento, Tabla de posiciones o Aprendizaje social. Estos widgets dependen de los datos específicos del usuario y solo están disponibles después de iniciar sesión.

Los visitantes tampoco pueden realizar acciones como inscribirse en un curso o acceder a cualquier contenido que requiera realizar un seguimiento del progreso o del contexto del usuario. Al intentar inscribirse o iniciar un curso de formación, se solicita al visitante que inicie sesión o se registre antes de continuar.

## Widgets admitidos en modo sin inicio de sesión

En el modo sin conexión, solo se admiten los widgets que no requieren datos específicos del usuario. Estos incluyen:

- Widget de categorías, que muestra las categorías de formación disponibles.
- Widget de cursos y rutas, que muestra los cursos y las rutas de aprendizaje del catálogo público. 1
- Cuadro de contenido, para agregar texto estático, imágenes o contenido promocional.
- widget de HTML, para incrustar contenido de HTML personalizado.
- Widget de Iframe, para mostrar sitios, vídeos o herramientas externos en la página.
- Los widgets que requieren contexto de usuario, como Mi aprendizaje, Calendario, Cumplimiento, Tabla de posiciones y Aprendizaje social, no están disponibles en el modo sin conexión.

Los widgets que requieren contexto de usuario, como Mi aprendizaje, Calendario, Cumplimiento, Tabla de posiciones y Aprendizaje social, no están disponibles en modo sin conexión

## Páginas y menús en una experiencia sin conexión

- Solo se admite un menú sin inicio de sesión, visible para todos los visitantes sin autenticación.
- Las páginas se pueden añadir a los menús de inicio de sesión y de no inicio de sesión; si una página está en ambos, adapta sus widgets y su contenido en función del estado de inicio de sesión del usuario.
- Los menús no conectados no tienen segmentación de audiencia ni personalización. Todos ven el mismo conjunto de páginas.
- Los widgets que no se admiten en el modo de inicio de sesión no se ocultan automáticamente; el diseño de página se ajusta para rellenar los huecos.
- La administración de menús y páginas (agregar, previsualizar, eliminar) es como el modo de inicio de sesión, pero con adaptaciones para las restricciones que no han iniciado sesión.

## Comportamiento de búsqueda y catálogo

En el modo sin conexión, los usuarios pueden acceder a la página del catálogo y utilizar la búsqueda para examinar los cursos y las rutas de aprendizaje disponibles. La página del catálogo muestra todos los cursos públicos, junto con los filtros y la funcionalidad de búsqueda, con la misma configuración de cuenta que en el modo de inicio de sesión. Cuando un usuario realiza búsquedas, los resultados aparecen en la página del catálogo y los usuarios pueden ver las páginas de información general de cursos e instancias sin iniciar sesión. Sin embargo, acciones como la inscripción requieren inicio de sesión.

Si un usuario intenta inscribirse, el sistema requiere que inicie sesión primero. La búsqueda de usuarios que no hayan iniciado sesión es más sencilla que la de los usuarios que hayan iniciado sesión y no incluye funciones avanzadas como la integración con el Asistente de inteligencia artificial.

## Implementación técnica

### Configuración del conector de acceso a datos de formación

Debe habilitar el conector de acceso a datos de formación en el panel de administración de la integración para poder utilizar la función experience builder sin conexión. Este conector exporta metadatos de formación de ALM a un repositorio público, lo que permite acceder a ellos a través de las API para las páginas no conectadas. La configuración del conector es un requisito previo para activar la función y garantiza que el portal muestre información de formación actualizada.

Exportación y sincronización de metadatos\
El conector exporta campos de metadatos clave como el nombre del curso, la descripción, la clasificación, la duración y las aptitudes. Puede programar exportaciones (por ejemplo, diarias) para mantener el portal sincronizado con ALM. No se pueden incluir todos los campos de metadatos; consulte ingeniería para obtener una lista completa. Los datos exportados se utilizan para rellenar las páginas que no han iniciado sesión y los cambios en ALM aparecerán después del siguiente ciclo de exportación.

Almacenamiento en caché y frecuencia de exportación\
El sistema utiliza la frecuencia de exportación de backend y el almacenamiento en caché de frontend para administrar las actualizaciones de datos. Los cambios realizados en ALM se reflejan en su portal después de la actualización programada de la exportación y la caché. Es posible que algunas actualizaciones no aparezcan inmediatamente debido a estos mecanismos. Si necesita actualizaciones más rápidas, ajuste la programación de exportación o borre la caché según sea necesario.

Compatibilidad con la personalización de CSS/JS\
Puede aplicar CSS y JavaScript personalizados a las páginas que hayan iniciado sesión y a las que no lo hayan hecho mediante la ficha de personalización. Esto le permite mantener una marca coherente, agregar elementos de interfaz de usuario personalizados y mejorar la experiencia del usuario en todo el portal. Todas las personalizaciones se aplican de forma global, lo que garantiza una apariencia unificada.

Diferencias de URL y marca (favicon, título de página)\
Las páginas que no han iniciado sesión y las que sí lo han hecho pueden tener direcciones URL distintas para distinguir los estados de los usuarios. Puedes personalizar el favicon y el título de la página de tu portal, lo que te ayuda a reforzar tu identidad de marca. Estas funciones están disponibles en el generador de experiencias; consulte con el departamento de ingeniería para conocer el estado más reciente de la compatibilidad con usuarios no conectados.

## Rendimiento y escalabilidad

### Pila compartida frente a pila premium

La pila compartida permite a varios clientes utilizar el generador de experiencias sin conexión en infraestructuras comunes, que admite niveles de tráfico estándar. El paquete premium es una opción de pago que proporciona recursos dedicados, funciones en tiempo real y límites de licencias más altos para los clientes con necesidades avanzadas. Elija la pila en función del tráfico previsto y los requisitos empresariales.

### Límites de tráfico y limitación de velocidad

La pila compartida impone límites de tráfico para garantizar un uso justo entre los clientes. El equipo de ingeniería implementará la limitación de velocidad para evitar que un solo cliente consuma todos los recursos. Si planeas campañas de marketing o esperas un tráfico elevado, coordina con el equipo de ingeniería para comprender tus límites y evitar interrupciones en el servicio. La limitación de velocidad ayuda a mantener la estabilidad y el rendimiento del sistema para todos los usuarios.

Consideraciones de multitenencia y SEO\
La plataforma es compatible con el multiinquilino, lo que permite a varios clientes alojar sus portales en infraestructuras compartidas. Las páginas que no han iniciado sesión son compatibles con SEO, junto con sitemap.xml y robots.txt para optimizar la visibilidad del motor de búsqueda. Esto garantiza que los motores de búsqueda puedan detectar e indexar el portal de forma adecuada.

## Migración y desaprobación

### Transición desde la página principal existente sin iniciar sesión

La función heredada de página de inicio sin inicio de sesión quedará obsoleta. Las nuevas cuentas no verán esta opción y se notificará a las cuentas existentes que la utilicen que migren a la solución basada en experience builder. Debe recrear su página de inicio con el nuevo generador de experiencias para obtener una mayor flexibilidad, compatibilidad con widgets y una experiencia de usuario mejorada. El plan de transición garantiza una interrupción mínima y un apoyo continuo.

Plan de comunicación\
Los clientes que utilicen la página de inicio heredada recibirán una comunicación clara sobre los plazos de eliminación y los pasos de migración. Se ofrecerá asistencia técnica para ayudarte a mover tu página de inicio a la nueva plataforma de experience builder, lo que te garantiza las ventajas de las nuevas funciones y las actualizaciones continuas.

### Compatibilidad con localización e inicio de sesión

Lógica de retroceso de configuración regional\
El sistema muestra las páginas en la configuración regional en la que se crearon. Si la configuración regional de un usuario no está disponible, el sistema utiliza una lógica alternativa para seleccionar la siguiente mejor configuración regional disponible. Esto garantiza que los usuarios vean siempre el contenido en un idioma compatible, lo que mejora la accesibilidad y la satisfacción de los usuarios.

Tipos de inicio de sesión admitidos\
La experiencia de inicio de sesión no registrado admite todos los tipos de inicio de sesión disponibles en ALM, incluidos el inicio de sesión único y el inicio de sesión estándar. Los usuarios pueden examinar el contenido sin iniciar sesión y se les pedirá que inicien sesión cuando sea necesario, como inscribirse en un curso o acceder a funciones personalizadas. Esto proporciona una transición fluida de la navegación a la participación.

## API sin registro

### API del objeto de aprendizaje de administración

Las páginas de Experience Builder que no están conectadas y los portales descentralizados suelen organizar o filtrar cursos según el producto y la función. La API de objeto de aprendizaje de administración se ha mejorado para garantizar que estas asociaciones sean accesibles de forma coherente para las integraciones de servicios de fondo y descentralizadas, así como para el conector de TDA.

**Punto final y comportamiento**

Seguirá utilizando el punto final del objeto de aprendizaje de administrador existente:

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles


Donde:

- loId es el ID del objeto de aprendizaje (por ejemplo, course:12345).
- forcedFields[learningObject] indica a la API que incluya explícitamente productos y funciones para ese objeto de aprendizaje.

Esto se consigue asegurándose de que las asociaciones de producto y función de la orden de fabricación están presentes en la respuesta cuando se solicita a través de forcedFields. A continuación, la respuesta contiene, en atributos, los metadatos de producto y función necesarios para calcular o exponer los productos recomendados (rec_products) y las funciones (rec_roles) para Experience Builder y otros consumidores.

Una llamada típica de un administrador o de una integración tiene el siguiente aspecto:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/learningObjects/course:12345?forcedFields[learningObject]=products,roles&quot; \
  -H &quot;Autorización: portador {admin_token}&quot; \
  -H &quot;Aceptar: application/vnd.api+json&quot;

El JSON de objeto de aprendizaje devuelto tiene la misma estructura básica que antes, pero ahora puede confiar en que los campos de producto/función están presentes cuando los solicite con forcedFields. Las integraciones que no utilizan forcedFields siguen comportándose como antes.

### Lista de objetos de aprendizaje: compatibilidad con ayudas de trabajo en el filtro effectiveModifiedDate

**Propósito**

El conector de Training Data Access (TDA) y las implementaciones descentralizadas a menudo necesitan realizar una sincronización incremental, basada en la **fecha de modificación efectiva** de los objetos de aprendizaje. Hasta esta versión, las ayudas de trabajo (tipo LO jobAid) no se gestionaban correctamente cuando se combinaban con los filtros effectiveModifiedDate. Esta versión lo corrige para que las ayudas de trabajo se puedan sincronizar de forma incremental, al igual que los cursos y las rutas de aprendizaje.

**Punto final y comportamiento**

El punto final de lista de objetos de aprendizaje existente se utiliza con filtros de fecha y tipo de objeto de aprendizaje:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Anteriormente, cuando filter.loTypes=jobAid se combinaba con un intervalo effectiveModifiedDate, el filtro excluía las ayudas de trabajo y la llamada se comportaba como si las ayudas de trabajo no se admitieran.

A partir de esta actualización, la llamada devuelve únicamente los objetos de aprendizaje de ayudas de trabajo cuya fecha efectiva de modificación se encuentre dentro de la ventana especificada.

```
{  
  "links": {  
    "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"  
  },  
  "data": [  
    {  
      "id": "jobAid:144968",  
      "type": "learningObject",  
      "attributes": {  
        "authorNames": ["Sid"],  
        "dateCreated": "2026-01-20T08:48:55.000Z",  
        "datePublished": "2026-01-20T08:48:55.000Z",  
        "dateUpdated": "2026-01-20T08:48:55.000Z",  
        "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",  
        "loType": "jobAid",  
        "loFormat": "Content",  
        "loResourceType": "Content",  
        "localizedMetadata": [  
          {  
            "description": "Link jobAid new",  
            "locale": "en-US",  
            "name": "Link jobAid new"  
          },  
          {  
            "description": "Link jobAid new fre",  
            "locale": "fr-FR",  
            "name": "Link jobAid new fre"  
          }  
        ],  
        "relationships": {  
          "authors": {  
            "data": [  
              { "id": "13385176", "type": "user" }  
            ]  
          },  
          "instances": {  
            "data": [  
              { "id": "jobAid:144891_-1", "type": "learningObjectInstance" }  
            ]  
          }  
        }  
      }  
    }  
  ]  
}
```

Esto significa que ahora puede implementar de forma segura las sincronizaciones incrementales de ayudas de trabajo basadas en effectiveModifiedDate, del mismo modo que ya lo hace para otros tipos.

Si se omite filter.loTypes=jobAid, el comportamiento de otros tipos de objetos de aprendizaje no cambia; el cambio solo afecta a la combinación de JobAid con ese filtro.

### **API de menú: Filtro de menú sin inicio de sesión**

**Propósito**

Experience Builder y las interfaces de usuario descentralizadas necesitan una forma sencilla de recuperar el **menú sin inicio de sesión** , que define la navegación para los visitantes públicos. Antes de esta versión, tenía que obtener todos los menús y, a continuación, aplicar una lógica personalizada para identificar cuál representaba la navegación sin conexión. Esta versión añade un sencillo filtro del lado del servidor.

**Punto final y comportamiento**

El extremo de lista de menús existente se utiliza con un nuevo parámetro de consulta:

GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true


Los puntos clave:

- include=pages,subMenus.pages es opcional, pero se recomienda cuando necesite los detalles de la página y del submenú en la misma respuesta.
- isNonLoggedIn=true es nuevo en esta versión e indica al servidor que devuelva sólo los menús marcados como menús sin conexión.

Sin el parámetro isNonLoggedIn, el extremo se comporta exactamente como antes y devuelve menús según el comportamiento predeterminado existente. Con isNonLoggedIn=true, normalmente devuelve el menú único utilizado por la experiencia de inicio de sesión no registrado para su cuenta (ya que normalmente solo hay un menú sin inicio de sesión por cuenta).

En la práctica, un cliente ahora puede emitir:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true&quot; \
  -H &quot;Autorización: portador {admin_token}&quot; \
  -H &quot;Aceptar: application/vnd.api+json&quot;


y recupera la estructura de navegación no conectada en una sola llamada, con todas las páginas que deberían estar visibles para los visitantes anónimos.

Esto resulta especialmente útil cuando se está creando un sitio sin encabezado que no ha iniciado sesión y se desea reflejar la misma navegación que usa Experience Builder, o cuando se está depurando si el menú sin iniciar sesión se ha configurado correctamente.

## Permitir la lista de dominios personalizados

La pila no conectada consta de:

- Un dominio de CDN público (por ejemplo, cpcontents.adobe.com o yourdomain.example.com) que ofrece diseños, JSON de configuración y activos estáticos.
- Un extremo de Elasticsearch público (ES) que sirve datos de catálogo y de búsqueda, pero solo si la solicitud proviene de un **dominio de la lista de permitidos** para esa cuenta de ALM.

Cuando se introduce un dominio personalizado, funciona perfectamente sin ningún esfuerzo adicional después del proceso existente para añadir un dominio personalizado.

### Requisitos previos

Antes de incluir en la lista blanca un dominio personalizado para usuarios no registrados:

1. El dominio personalizado se configura para su cuenta de ALM (por ejemplo, DNS para academy.yourcompany.com apunta a Adobe / Akamai y se aprovisionan los certificados).
2. El conector **Training Data Access (TDA)** está habilitado para la cuenta.
3. La característica **Experience Builder no conectado** está habilitada (en el Adobe).

Estas medidas garantizan que:

- Su cuenta tiene una **cuenta JSON** sin sesión iniciada (a menudo denominada accountConfig / experienceBuilderConfig), que incluye campos como cpDomain, almDomain, almCdnBaseUrl, esBaseUrl y dominios de la lista de permitidos.
- La pila sin sesión iniciada sabe dónde enviar datos y desde qué dominios debe aceptar solicitudes.

### Cómo funcionan las listas de permitidos

La lista de permitidos se almacena en la configuración que exporta TDA y se lee la pila no conectada. Dicha configuración incluye:

- Los dominios de ALM (cpDomain, almDomain).
- La **URL base de CDN** para contenido no registrado (almCdnBaseUrl).
- La **dirección URL base de búsqueda pública** (esBaseUrl).
- La lista de dominios a los que se les permite realizar llamadas públicas sin iniciar sesión para esa cuenta.

Para que Experience Builder no conectado funcione en un dominio personalizado:

- El navegador debe cargar el HTML que no ha iniciado sesión desde ese dominio personalizado (o desde el dominio CDN que no ha iniciado sesión en ALM, según su configuración).
- Las llamadas de ese dominio a los puntos finales públicos de ES y CDN deben aceptarse. Esto solo sucede si el dominio está presente en la lista de permitidos.

Esta versión agrega un nuevo dominio de CDN sin inicio de sesión, cpcontents.adobe.com, y especifica que debe colocarse en **dominios incluidos en la lista de permitidos** en el conector de TDA. Para los usuarios nativos existentes que no han iniciado sesión, esto requiere una actualización.

### Permitir-enumerar un dominio personalizado

**Configurar el dominio personalizado en ALM**

Trabaje con Adobe para registrar su dominio, por ejemplo, academy.yourcompany.com, como dominio personalizado para su cuenta de ALM. Actualice DNS para que apunte al Adobe Akamai según se indica y espere a que se complete SSL y el enrutamiento.

En este momento, tanto el tráfico que ha iniciado sesión como el que no lo ha hecho puede llegar a ALM a través de ese dominio, pero las llamadas de búsqueda y catálogo que no han iniciado sesión pueden seguir bloqueadas si el dominio no está incluido en la lista de permitidos.

**Habilitar TDA y Experience Builder sin sesión iniciada**

Asegúrese de que:

- El **conector de acceso a datos de formación** está habilitado.
- La característica **Experience Builder no conectado** está activada para la cuenta.

Al habilitar TDA, se crea o actualiza el JSON de la cuenta que no ha iniciado sesión. En el caso de las nuevas cuentas, el proceso también muestra de forma predeterminada el nuevo dominio de CDN sin inicio de sesión (cpcontent.adobe.com), por lo que el extremo público de ES espera llamadas de ese dominio.

En el caso de las cuentas que ya utilizaban la pila anterior sin inicio de sesión, la especificación M45 indica que los conectores existentes deben eliminarse y volver a crearse para seleccionar el nuevo dominio.

**Agregar el dominio personalizado a la lista de permitidos**

La parte crítica es indicarle a la pila de ES no iniciada que academy.yourcompany.com es un origen aprobado. Hay dos caminos comunes.

1. **Vuelva a habilitar el conector de TDA (sencillo, fácil de usar)**

El wiki de Experience Builder M45 explica que los usuarios nativos no conectados existentes deberán eliminar y volver a habilitar la conexión TDA para que el nuevo dominio aparezca automáticamente en la lista de permitidos. Haciendo esto se logran dos cosas:
1. Se regenerará el JSON de la cuenta que no ha iniciado sesión.
2. Los dominios de la lista de permitidos se actualizan para incluir el nuevo dominio de CDN no registrado y su dominio personalizado.

Se recomienda cuando tiene un número reducido de cuentas y puede tolerar que se deshabilite y se vuelva a habilitar temporalmente el conector.

1. **Compruebe que el dominio esté incluido en la lista de permitidos**

Después de la inclusión en la lista de permitidos, abra el sitio que no haya iniciado sesión en el dominio personalizado e inspeccione las llamadas de red del navegador.

Desea ver lo siguiente:

- Solicitudes a almCdnBaseUrl (por ejemplo, [https://cpcontent.adobe.com/](https://cpcontent.adobe.com/)...) con 200/304.
- Solicitudes a esBaseUrl (API de búsqueda pública, por ejemplo [https://primeapps.adobe.com/almsearch/api/v1/](https://primeapps.adobe.com/almsearch/api/v1/)...) se completó correctamente, devolviendo JSON con datos de búsqueda / catálogo.

Si estas llamadas devuelven errores 4xx o explícitos que sugieren &quot;dominio no confiable&quot; o &quot;origen no permitido&quot;, la lista de permitidos está incompleta o mal configurada y el Soporte debe ajustarla.

El LLD sin inicio de sesión también indica que la configuración de la cuenta puede contener un valor de dominio esperado. En tiempo de ejecución, el sitio comprueba que el dominio de la dirección URL coincide con lo establecido en la configuración; si no lo hace, se puede redirigir al usuario a una página de error. Esto protege contra el acceso a la configuración de un cliente a través del dominio de otro cliente.

## Uso de recomendaciones en Experience Builder sin iniciar sesión

Experience Builder, que no está conectado, te permite crear páginas de aprendizaje públicas en las que los visitantes pueden examinar tu catálogo y ver el contenido resaltado antes de iniciar sesión. Aunque estos visitantes sean anónimos, puede seguir presentando cursos de formación recomendados mediante metadatos y widgets.

En la aplicación del alumno que ha iniciado sesión, las recomendaciones se pueden personalizar: pueden depender del perfil del alumno, su historial, sus aptitudes y su progreso. En la experiencia de **sin sesión iniciada**, todavía no hay identidad de alumno, por lo que la plataforma no puede personalizar por usuario.

Por lo tanto, Recommendations en modo sin sesión iniciada:

- **Seleccionado o basado en reglas**: basado en catálogo, producto, función, etiquetas, etiquetas y otros metadatos.
- **Orientado a segmentos**: &quot;recomendado para desarrolladores&quot;, &quot;recomendado para socios&quot;, &quot;ofrecido para principiantes&quot;.
- **Centrado en el marketing**: se utiliza para atraer y guiar a los visitantes a inscribirse una vez que inician sesión.

### Metadatos y API compatibles con las recomendaciones

Entre bastidores, las páginas sin sesión iniciada utilizan:

- El **conector TDA** para exportar metadatos de objetos de aprendizaje (cursos, rutas, certificaciones, ayudas de trabajo) a un índice de búsqueda pública.
- La **pila de búsquedas públicas** para responder a consultas de widgets que no han iniciado sesión (catálogo, búsqueda, cursos y rutas, categorías).
- La **API de objetos de aprendizaje de administración** muestra metadatos de productos y funciones que se pueden usar para reglas de recomendación.

En esta versión, la API del objeto de aprendizaje de administración se ha ampliado para que las asociaciones de productos y funciones estén disponibles de forma fiable:

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles

Esto permite que los widgets y las integraciones descentralizadas creen recomendaciones basadas en reglas mediante productos, funciones, etiquetas de catálogo, etiquetas y otros campos de forma coherente.

### Diseño de secciones de recomendaciones con widgets de Experience Builder

Puede crear secciones de recomendación en páginas que no han iniciado sesión combinando **widgets de Experience Builder** con filtros de metadatos.

#### **Widget de cursos y rutas**

Utilice el widget **Cursos y trazados** cuando desee mostrar una fila o cuadrícula de elementos recomendados. En su configuración puede elegir:

- De qué catálogos extraer.
- Etiquetas de catálogo, productos, funciones o etiquetas que se van a utilizar como filtros.
- Si se muestran cursos, rutas, certificaciones, ayudas de trabajo o una combinación.
- Ordenación y número máximo de elementos.

Por ejemplo, puede crear:

- &quot;Recomendado para desarrolladores&quot;: filtre por un producto o función que utilice para el contenido del desarrollador.
- &quot;Empezar aquí&quot;: filtre por una etiqueta como &quot;Inicio&quot; o &quot;Incorporación&quot;.
- &quot;Destacados este trimestre&quot;: filtre por una etiqueta con límite de tiempo como featured-q3-2026.

El widget no está aprendiendo del comportamiento; muestra lo que coincide con las reglas de metadatos que defina. Desde el punto de vista del visitante, sin embargo, parece una tira de recomendaciones.

#### Widget **Categorías**

Usa el widget **Categorías** para ayudar a los visitantes a navegar por conjuntos de contenido &quot;recomendado&quot;, incluso si no conocen los nombres de tus productos.

Puede configurar mosaicos que representen cada uno un segmento, por ejemplo:

- &quot;Para administradores&quot;
- &quot;Para equipos de ventas&quot;
- &quot;Para socios&quot;
- &quot;Por línea de productos&quot;

Cada mosaico puede vincularse a:

- Una página de catálogo filtrada (por ejemplo, el catálogo filtrado por determinados productos o etiquetas).
- Una página dedicada sin conexión que utiliza cursos y rutas preconfiguradas para ese segmento.

Esto te ofrece una experiencia de &quot;rutas recomendadas por segmento&quot; sin personalización.

### Creación de recomendaciones basadas en segmentos

Dado que los visitantes que no han iniciado sesión aún no tienen un perfil de ALM, resulta útil diseñar recomendaciones **por segmento** y permitir que los visitantes se autoseleccionen.

1. Utiliza una **página de inicio sin sesión** que explique brevemente para quién es tu academia y muestre un pequeño número de puntos de entrada de segmentos (por ejemplo, &quot;Desarrolladores&quot;, &quot;Responsables de marketing&quot;, &quot;Partners&quot;, &quot;Nuevos empleados&quot;). Esto se puede hacer con un widget Categorías o un simple cuadro Contenido o sección HTML con botones.
2. Para cada segmento, crea una **página dedicada sin inicio de sesión** en Experience Builder. En esa página utilice uno o más widgets Cursos y rutas configurados con filtros que representan lo que se &quot;recomienda&quot; para ese grupo. Por ejemplo, para &quot;Desarrolladores&quot; puede filtrar por:
   1. Catálogo = &quot;Formación pública&quot;
   2. Producto = &quot;Adobe Experience Manager&quot;
   3. Tags = &quot;Fundamentos del desarrollador&quot;
3. Utilice esas páginas de segmentos como el destino de sus campañas de marketing y como el objetivo de los mosaicos en la página de inicio no iniciada.

Los visitantes perciben que están viendo recomendaciones adaptadas a su situación, a pesar de que la lógica se define en tiempo de diseño a través de metadatos.

### Transición de recomendaciones sin sesión iniciada a recomendaciones personalizadas

Las recomendaciones que no han iniciado sesión se refieren principalmente a **detectabilidad** y **conversión**. Una vez que los visitantes decidan inscribirse o empezar a formarse, iniciarán sesión y se convertirán en alumnos completos con un perfil e historial.

El flujo habitual es:

1. Un visitante descubre el contenido a través de las secciones de recomendaciones que no han iniciado sesión (recomendaciones de inicio, páginas de destino de segmentos, filas destacadas).
2. Hacen clic en una descripción general del curso o ruta y eligen inscribirse o comenzar.
3. ALM les solicita que se registren o inicien sesión.
4. Después de iniciar sesión, la experiencia de alumno con sesión iniciada estándar toma el control, que incluye:
   1. &quot;Mi aprendizaje&quot;
   2. Catálogo iniciado sesión con progreso personal
   3. Cualquier sistema de recomendaciones interno que utilice para los alumnos existentes.

En otras palabras, las recomendaciones de inicio de sesión les ayudan a decidir qué hacer a continuación y seguir adelante.

## Cómo se pueden usar las ayudas de trabajo en el nuevo Experience Builder sin registro

En la **interfaz de usuario**, las ayudas de trabajo participan en experiencias sin sesión iniciada principalmente a través de widgets que pueden mostrar objetos de aprendizaje:

1. **Widget de rutas y cursos**\
   Este widget puede mostrar varios tipos de objetos de aprendizaje, incluidas las ayudas de trabajo. En las páginas que no han iniciado sesión, puede configurarlo para:
   1. Incluir o excluir ayudas de trabajo de forma explícita.
   2. Filtre las ayudas de trabajo por catálogo, producto, función, etiquetas, etiquetas y otros metadatos.
   3. Preséntelas junto a cursos y trazados o como una tira separada de &quot;Recursos&quot;.

Por ejemplo, en una página de aterrizaje pública, puede configurar una tira titulada &quot;Recursos útiles&quot; que muestre solo las ayudas de trabajo, y otra tira titulada &quot;Cursos recomendados&quot; que muestre los cursos y las rutas.

1. **Página de catálogo y búsqueda**\
   Las superficies **catalog** y **search** que no estén registradas utilizan el índice de búsqueda pública (alimentado por el conector Training Data Access). Ese índice ahora admite ayudas de trabajo correctamente, por lo que:
   1. Los resultados de búsqueda que no estén registrados pueden incluir ayudas de trabajo.
   2. Filtros de catálogos no registrados (por tipo, producto, etiquetas, etc.) Puede incluir ayudas de trabajo siempre que la configuración de su cuenta y los widgets estén configurados para mostrarlas.
2. **Páginas de información general de objetos de aprendizaje**\
   Cuando un visitante hace clic en una ayuda de trabajo desde cualquier widget o desde el catálogo, va a una **página de información general de objeto de aprendizaje** para esa ayuda de trabajo en modo sin inicio de sesión. A partir de ahí, pueden leer su descripción y metadatos. Normalmente, la descarga o el consumo reales aún requieren inicio de sesión, pero la presencia y la capacidad de detección de la propia ayuda de trabajo dependen de la experiencia de no inicio de sesión.

### Cómo se exponen las ayudas de trabajo mediante API que no han iniciado sesión

En el **lado de la API**, las ayudas de trabajo son compatibles con:

1. **Conector de acceso a datos de formación y búsqueda pública**\
   TDA exporta metadatos de ayuda de trabajo junto con otros tipos de objetos de aprendizaje al índice de búsqueda pública que atiende consultas de catálogo y búsqueda no registradas. En esto confían Experience Builder y las interfaces de usuario descentralizadas.
2. La lista de **objetos de aprendizaje con effectiveModifiedDate**\
   En esta versión, se ha corregido el extremo del listado de objetos de aprendizaje para que las ayudas de trabajo funcionen correctamente con el filtro effectiveModifiedDate. Ahora puede llamar a:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Antes de este cambio, la combinación de effectiveModifiedDate con loTypes=jobAid no devolvía de forma fiable las ayudas de trabajo. Ahora sí, como se documenta en el wiki *Cambios en la API pública M45*. Eso significa:

1. Tus trabajos de ETL o TDA pueden **sincronizar las ayudas de trabajo de forma incremental** para experiencias que no hayan iniciado sesión, del mismo modo que para cursos y rutas.
2. Cualquier implementación descentralizada que cree un directorio de ayuda de trabajo público puede consultar los cambios en función de effectiveModifiedDate y loType=jobAid.

La respuesta de ejemplo en el documento M45 muestra un learningObject con loType: &quot;jobAid&quot; y loFormat: &quot;Content&quot; que se devuelve al utilizar este patrón.

1. **API de objeto de aprendizaje de administrador**\
   Si bien no es específico de los objetos de aprendizaje que no han iniciado sesión, M45 también actualiza la API del objeto de aprendizaje de administración para exponer de forma coherente los metadatos de producto y función para todos los tipos de objetos de aprendizaje mediante:

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles


En el caso de las ayudas de trabajo, esto significa que puedes gestionar su producto, función, etiquetas y etiquetas de forma centralizada y utilizar esos metadatos en experiencias públicas no registradas, por ejemplo en las secciones &quot;Recursos para responsables de marketing&quot; o en páginas de inicio específicas del producto.

**Nota**:

En el estado sin sesión iniciada:

- Las ayudas de trabajo son principalmente **detectables**: los visitantes pueden ver que existen, leer descripciones y entender cómo admiten temas o cursos.
- El **consumo** real (descargar o abrir el contenido de la ayuda de trabajo) normalmente requiere inicio de sesión, especialmente si las ayudas de trabajo se consideran parte del contenido interno o con licencia.

## Cambios en la &quot;breve descripción&quot; en la búsqueda de objetos de aprendizaje (sin iniciar sesión)

En la pila no conectada, la búsqueda y la lista de objetos de aprendizaje (LO) funcionan mediante el conector de Acceso a datos de formación (TDA) y un índice de Elasticsearch público. Históricamente, esta pila utilizaba un único campo de descripción/información general para cada objeto de aprendizaje. Los clientes que creaban portales descentralizados no conectados querían mostrar la misma breve descripción en los mosaicos de objetos de aprendizaje que mostraba la interfaz de usuario del alumno que había iniciado sesión, en lugar de solo la larga descripción general.

El cambio introduce la compatibilidad con el objeto de aprendizaje **breve descripción** en las API de búsqueda y listado no registradas:

- Para **cursos**, la semántica de la interfaz de usuario existente es:
   - Las tarjetas de inicio de sesión muestran &quot;Breve descripción&quot; (campo de 140 caracteres) si están presentes; de lo contrario, se remontan a la larga &quot;Descripción detallada&quot;.
- Para **rutas de aprendizaje**, la interfaz de usuario que ha iniciado sesión utiliza el campo &quot;Beneficios&quot; como breve descripción, si se ha definido, y se remite a la descripción general en caso contrario.
- Para **certificaciones**, se utiliza una breve &quot;Descripción&quot;, con una &quot;Descripción general de la certificación&quot; más larga como reserva.
- Para **ayudas de trabajo**, se usa el campo de descripción principal.

## Otros cambios

### Restricción de que no pueda haber dos cuentas que compartan el mismo dominio personalizado

En las arquitecturas sin inicio de sesión y sin inicio de sesión de Adobe Learning Manager, un **dominio personalizado** (por ejemplo, academy.example.com) se trata como una clave única global que debe asignarse exactamente a una cuenta de ALM, por lo que la plataforma aplica una restricción estricta de que **no hay dos cuentas que puedan compartir el mismo dominio personalizado**. Esto es necesario para la seguridad, el enrutamiento y el SEO: la capa de enrutamiento y la pila de elementos no registrados utilizan el dominio para buscar la configuración correcta de la cuenta (incluidos sus elementos JSON de cuenta no registrada, los menús de Experience Builder, la marca y los puntos finales de TDA/búsqueda),

Permitir el mismo dominio personalizado en dos cuentas haría imposible garantizar qué datos de cuenta se devuelven, podría causar fugas entre inquilinos y también dañaría artefactos generados como sitemap.xml y robots.txt que se producen por cuenta pero que los motores de búsqueda descubren por host. Operacionalmente, esto significa que cuando asigne o mueva un dominio personalizado primero debe asegurarse de que no esté asociado a ninguna otra cuenta (o anular su registro allí), y las herramientas internas de Adobe rechazarán los intentos de vincular el mismo dominio a varias cuentas.

### Almacenamiento en caché de los recursos en el explorador en la experiencia sin iniciar sesión

En la experiencia sin inicio de sesión de Adobe Learning Manager, el almacenamiento en caché de los recursos del explorador es una parte fundamental de la estrategia de rendimiento y escala, porque las páginas públicas deben controlar un tráfico de marketing grande y a veces intenso con baja latencia y una carga de origen mínima. Los recursos estáticos y semiestáticos, como el shell del HTML sin conexión (por ejemplo, index.html/guest.html), el JSON de configuración de nivel de cuenta (account.json o config.json), el JSON de diseño de página de Experience Builder (menús, diseños de widget, configuración de tarjeta), CSS, JS, imágenes y favicons, se proporcionan desde una CDN de Akamai (cpcontents.adobe.com / cpcontent.adobe.com) con encabezados de caché que fomentan la reutilización tanto del lado de la CDN como del navegador, de modo que, después de cargar la primera página, el navegador pueda procesar las páginas posteriores sin conexión en gran medida desde su caché, revalidándose solo cuando sea necesario mediante ETag o Last-Last-Last-ag campo.

## Iniciar las opciones de la página de inicio

En la página principal de Adobe Learning Manager, seleccione **Marca**. A continuación, en el panel izquierdo, seleccione No registrado en la página de inicio.

![opciones de la página principal](/help/migrated/administrators/feature-summary/assets/non-logged-in-homepage.png)

*Seleccione la opción No registrado en la página de inicio*

## Añadir un banner

Añada un banner para incluir un anuncio de marketing o uno de los temas más popular del día. Seleccione **Agregar banner**.

![banner](/help/migrated/administrators/feature-summary/assets/add-banner-image.png)

*Agregar un banner*

Busque la ubicación de la imagen que se utilizará como banner. A continuación, proporcione un vínculo como botón de acción en la imagen del banner.

## Añadir categorías

Este componente se puede utilizar para filtrar catálogos por etiquetas, aptitudes y catálogos. Esta sección contiene un encabezado y una descripción para cada categoría. Al hacer clic, se redirige al usuario a la página del catálogo con los filtros aplicados.

Seleccione **[!UICONTROL Agregar categoría]**. A continuación, introduzca los detalles de la categoría.

![agregar categoría](/help/migrated/administrators/feature-summary/assets//add-category.png)

*Agregar las categorías*

Guarde la categoría. La categoría se añade a la sección.

## Añadir un catálogo

Añada un catálogo para los usuarios que no hayan iniciado sesión, de modo que puedan examinar toda la formación en la plataforma.

![agregar catálogo](/help/migrated/administrators/feature-summary/assets//add-catalog.png)

*Agregar un catálogo*

Estarán presentes todos los cursos de formación exportados.
