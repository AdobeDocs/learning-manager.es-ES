---
description: Obtenga más información sobre las nuevas funciones y mejoras de Adobe Learning Manager
jcr-language: en_us
title: Resumen de las nuevas funciones
contentowner: jayakarr
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '26196'
ht-degree: 0%

---



# Resumen de las nuevas funciones

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Actualización 95: versión de noviembre de 2023 de Adobe Learning Manager

**Fecha de publicación:** 18 de noviembre de 2023

## Novedades de esta versión

Ver [Novedades de Adobe Learning Manager](/help/migrated/whats-new.md) para obtener más información.
+++

+++Actualización 94

**Fecha de publicación:** 23 de agosto de 2023

## Novedades de esta actualización

* Seleccione el icono de engranaje del reproductor para cambiar la calidad del vídeo.
* Cambia la calidad y velocidad de un vídeo en las redes sociales.
+++

+++Actualización 93: versión de julio de 2023 de Adobe Learning Manager

**Fecha de publicación:** 10 de julio de 2023

Novedades de esta versión

### Recommendations mejorado

Adobe Learning Manager ha introducido un nuevo y mejorado sistema de recomendaciones para los cursos. Esta función de recomendaciones utiliza algoritmos de IA y los intereses de los usuarios, como productos, funciones y niveles, para ofrecer recomendaciones de contenido personalizadas.

### Inscripción múltiple

En esta versión de Adobe Learning Manager, presentamos la inscripción múltiple para alumnos que permite a los alumnos inscribirse en más de una instancia de un curso en uno o varios períodos de tiempo.

### Rechazo Del Conector De Exavault

Esta versión de Adobe Learning Manager incluirá un nuevo conector, que utilizará el protocolo SFTP de la familia AWS Transfer.

Para obtener más información, consulte [Novedades de la versión de julio de 2023 de Adobe Learning Manager](/help/migrated/whats-new-2023-july.md).
+++

+++Actualización: 92

**Fecha de publicación:** 23 de junio de 2023

**Errores corregidos en esta actualización**

* Después de completar un módulo, la API de grados no se activa automáticamente, lo que hace que la marca de verificación verde no se muestre como se esperaba en la interfaz de usuario.
* Después de completar algunos módulos de una ruta de aprendizaje o una certificación, la marca de verificación verde, que indica que la finalización se ha realizado correctamente, no se muestra del modo esperado.
* Adobe Learning Manager no se inicia del modo esperado después de cargar un archivo CSV de usuarios con campos incorrectos.
* La ventana emergente de advertencia sobre cómo contactar con el administrador también muestra otras direcciones de correo electrónico.
* Todas las insignias obtenidas por un alumno no se muestran en la respuesta.
* Durante el registro del usuario, debe aceptarse un nombre de usuario con &quot; &quot;.

#### Reproductor

* Añada un menú para seleccionar la resolución de pantalla al reproducir un vídeo.
+++

+++Actualización 91

**Fecha de publicación:** 1 de junio de 2023

### Conectores

* El conector de Adobe Connect requiere API para enviar tokens de CSRF. Para obtener más información, consulte Mejorar la seguridad de las cuentas de Adobe Connect.

### Cambio de cadena

* Hemos cambiado el nombre de la cadena Clasificar este curso de formación a Clasificar este curso, Clasificar esta ruta de aprendizaje o Clasificar esta certificación en función de la formación que realice un alumno. En función del tipo de formación, el alumno verá la cadena en consecuencia.

### Errores corregidos en esta actualización

* La descripción de la aplicación móvil de Adobe Learning Manager de Play Store indica incorrectamente que un alumno puede realizar un curso sin conexión.
* Se han producido problemas al migrar contenido (module_version.csv y course_module.csv) de LinkedIn a Adobe Learning Manager.
* Si una cuenta está en estado inactivo y se creó hace más de tres años, todos los usuarios de la cuenta se eliminan según el RGPD, independientemente del estado de los usuarios.
* En la aplicación del instructor, cuando establece el límite de la lista de espera en cero en una sesión y guarda la sesión, la interfaz de usuario muestra incorrectamente &quot;No aplicable&quot; en lugar de cero.
* Al generar transcripciones de alumnos para el conector de Power BI, la columna Duración del módulo o formación (minutos) muestra valores nulos para determinados módulos de clase o clase virtual.
* Después de marcar un curso como completado para los alumnos de una instancia o varias instancias, todos los alumnos del curso se marcan como completados, no solo los alumnos de la instancia o instancias actuales.
+++

+++Actualización 90

**Fecha de publicación:** 4 de abril de 2023

### Errores Corregidos En Esta Actualización

El inicio de sesión de SAML falla si la dirección URL de inicio de sesión de SSO contiene entity_id.
+++

+++Actualización 89: versión de marzo de 2023 de Adobe Learning Manager

**Fecha de publicación:** 1 de abril de 2023

### Novedades de esta actualización

**Mejoras en la experiencia de formación a cargo del instructor (ILT)**

Se han realizado varias mejoras en la experiencia de formación dirigida por instructor (ILT). Entre las mejoras clave se incluyen: la capacidad de filtrar las sesiones de clase según la ubicación, la capacidad de cambiar instancias (VILT) sin perder el progreso, un nuevo &quot;Asistente de programación&quot; para gestionar conflictos en los instructores de reserva y las clases, la capacidad de adjuntar &quot;Aptitudes&quot; a los instructores y elegir instructores en función de las aptitudes.

**Mejoras de la lista de verificación de la observación**:

Los autores ahora pueden seleccionar &quot;Responsable&quot; y &quot;Gerente de tienda&quot; como Observador de las listas de comprobación. Los responsables pueden ver y completar las listas de comprobación en la interfaz Responsable sin tener que cambiar de función a un instructor. Se envía una notificación al responsable cuando se le asigna una lista de comprobación.

**Utilizar cualquier cámara de aplicación o smartphone para escanear códigos QR de Learning Manager**

Los alumnos ahora podrán utilizar cualquier aplicación de escaneado de código QR o la cámara de su smartphone para escanear los códigos QR generados por Learning Manager para la inscripción de cursos, la finalización y mucho más.

**Mejoras de informes**

Un nuevo informe de utilización del instructor, un informe de revisión de cursos de formación, un informe de ayudas de trabajo y otras mejoras en los informes.

**Compatibilidad con sesiones híbridas**

Adobe Learning Manager ahora admite la posibilidad de crear sesiones &quot;híbridas&quot; de formación impartida por instructores (ILT). Las sesiones de ILT virtuales se pueden crear con información de ubicación opcional para que los alumnos puedan asistir a la sesión en persona, así como si estuvieran disponibles en la ubicación.

**Mejor seguimiento del progreso para ILT virtual y de clase**

Los módulos ILT de clase y virtuales ahora ofrecen la capacidad de informar del estado de la prueba de un alumno (aprobado o suspenso) junto con el estado de asistencia. Por lo tanto, se puede considerar tanto la asistencia como el éxito de las pruebas para decidir el progreso del alumno.

**Aplicación Adobe Learning Manager para Microsofts Teams**

La nueva aplicación Adobe Learning Manager para Microsofts Teams está diseñada para fomentar el aprendizaje en el flujo de trabajo e impulsar el aprendizaje social. Los alumnos podrán acceder al contenido de aprendizaje en la plataforma Microsofts Teams sin necesidad de cambiar a un navegador. Póngase en contacto con su CSAM para obtener la versión beta de la aplicación Adobe Learning Manager en MS Teams.

### Errores corregidos en esta actualización

**Curso**

* Un autor personalizado no puede obtener una vista previa de un módulo cuando el curso se encuentra en el estado &quot;UNDER_CONSTRUCTION&quot;. La respuesta muestra el error 404.
* El título del curso en la página del curso o la adición de una aplicación de autor se desborda cuando el título del curso supera un determinado límite de caracteres.

**Autor**

* En la aplicación de autor, el título del curso (si es largo) excede los límites de la página al crear un curso.
* En ocasiones, se añade un curso, aunque no se haya seleccionado ningún autor.

**Informes de tableros**

* La información sobre herramientas se muestra correctamente cuando el idioma de la interfaz es el inglés, pero genera un error de consola cuando el idioma de la interfaz es diferente.
* Cambie el nombre &quot;Obligatorio&quot; a &quot;Obligatorio&quot; en el tablero del alumno.

**Aplicación de instructor**

* El formato de hora en la aplicación del instructor no es coherente con el resto de aplicaciones.

**Social**

* Para ciertos tipos de publicaciones, después de la publicación, el tablero social no se abre como se esperaba.

**Administrador**

* Un usuario con una función personalizada no puede descargar recursos al obtener una vista previa de un curso.

**Plantillas de correo electrónico**

* Cuando un alumno se da de baja de un programa de aprendizaje que contiene un curso de clase o clase virtual, no recibe ningún correo electrónico de cancelación.

**Ayudas de trabajo**

* No se puede ver el nombre del curso en el widget de ayuda de trabajo.

**Publicación**

* La descripción del módulo añadida en Adobe Captivate no está visible en Learning Manager cuando el módulo se publica en ALM.

**Campos activos**

* Cuando se está procesando un archivo CSV con un gran número de registros, tarda un tiempo considerable, durante el cual, si un usuario inicia sesión e introduce un valor para uno de los atributos, podría crear un nuevo grupo de usuarios que podría generar errores de CSV. Para solucionarlo, cuando la importación de CSV está en curso, el mensaje emergente del atributo Campos activos se deshabilita y se vuelve a habilitar una vez completada la carga del CSV.
* Si la columna del archivo CSV de usuarios tiene el mismo nombre que el campo activo de usuarios externos, la carga del archivo CSV falla.

**Correcciones relacionadas con la API**

* En la respuesta learningObjects, falta el atributo bookmark.
* Se crea una entrada de acceso al generar tokens de actualización de OAuth para usuarios eliminados.
* La API de objeto de aprendizaje devuelve un valor loFormat incorrecto, ya que los módulos previos al trabajo se tenían en cuenta para calcular el tipo de curso junto con el contenido principal.

**Problemas conocidos de esta actualización**

* El botón Compartir del catálogo de alumnos no funciona del modo esperado en el navegador Safari ni en la aplicación para dispositivos móviles y iPad MS Teams.
* Las notificaciones no aparecen en la pestaña Actividad una vez que la aplicación se elimina en otros equipos.
No ocurre nada al hacer clic en las notificaciones de la pestaña Actividad de la aplicación en iPhone 14.
* En la aplicación de MS Teams, las notificaciones de Learning Manager (completado, inscrito, fecha límite y vencido) no muestran el estado ni el nombre del curso en la ficha Actividad.
* Aparece un mensaje emergente con contenido XML cuando el administrador de integración no aprueba la aplicación MS Teams.
* El idioma de la interfaz de usuario en la aplicación Adobe Learning Manager en MS Teams no cambia a veces del modo esperado cuando se cambia el idioma.
* No es posible interactuar con la primera notificación cuando el foco está dentro de Iframe (fichas Inicio y Catálogo).

**Limitaciones de la aplicación móvil de Adobe Learning Manager**

* Visualización de contenido sin conexión.
* Vista de cuadrícula o lista en la página Catálogo/Mi aprendizaje.
* Varios intentos de realizar un curso.
* Plazo de inscripción en una tarjeta de curso.
* En dispositivos iOS, las notificaciones push no aparecen cuando la aplicación está en primer plano.
* Los vínculos profundos en las notificaciones push no se redirigen a la página de aterrizaje prevista.
* Al hacer clic en el botón Registrar interés se redirigirá a la web.
* Al responder o comentar en Aprendizaje social, no podrá adjuntar un archivo.
* No podrá iniciar sesión en LinkedIn Learning.
+++

+++Actualización 8

**Fecha de publicación:** 7 de marzo de 2023

### Mejoras De Rendimiento En Esta Versión

Cuando se realiza una inscripción masiva de alumnos, no se genera ningún archivo de registro para cada alumno.
Hemos optimizado el procesamiento de planes de aprendizaje para cuentas grandes. De este modo, se evitan problemas de búsqueda o retrasos.
+++

+++Actualización 87

**Fecha de publicación:** 1 de marzo de 2023

## Errores Corregidos En Esta Actualización

* Un alumno no recibe el correo electrónico de cancelación de la sesión si se elimina el módulo CR/VC del curso en el que se ha inscrito.
* Cambiar GetNotificationData de GET a POST. La implementación original produjo el error, **IllegalArgumentException: El encabezado de la solicitud es demasiado grande**, lo que produjo notificaciones fallidas.
+++

+++Actualización: 86

**Fecha de publicación:** 17 de febrero de 2023

### Error Corregido En Esta Versión

En la aplicación del alumno, la búsqueda de usuarios y grupos de usuarios falla debido a algunos problemas con la configuración regional.
+++

+++Actualización 85

**Fecha de publicación:** 13 de febrero de 2023

### Qué ha cambiado en esta actualización

Se ha agregado la compatibilidad con el código de idioma de cuatro letras al filtrar los idiomas en GET learningmanagerapi/v2/learningObjects.

### Errores Corregidos En Esta Actualización

Para algunas configuraciones regionales, la búsqueda devuelve resultados incorrectos.
Los metadatos del curso se sobrescriben cuando el curso tiene más de una variante de la misma configuración regional.
+++

+++Actualización 84

**Fecha de publicación:** 2 de febrero de 2023

### Qué ha cambiado en esta actualización

**Informe de ayuda de trabajo**

Esta actualización incluye un nuevo informe de ayudas de trabajo que enumera todas las ayudas de trabajo de la cuenta.

**Control de versiones**

Hemos añadido control de versiones para los recursos al añadir los recursos al crear un curso.

**Informe de intentos**

Puede ver un informe de todos los intentos de respuesta y las visitas de un alumno en cada curso de formación.

**API de restablecimiento de módulo**

Un administrador ahora puede restablecer un módulo mediante la API de restablecimiento de módulos. Para obtener más información, consulte [Referencia de API de Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

**Plantilla de correo electrónico**

Para algunas plantillas de correo electrónico, ahora puede agregar un requisito previo a la plantilla.

**Otros cambios**

* Puede añadir un curso aprobado por el responsable como requisito previo.
* Mejora del rendimiento al actualizar el tablero de resumen de aprendizaje.
* Los ID de correo electrónico y los ID de cuenta se verifican antes de enviar un informe de rebote.

### ERRORES CORREGIDOS EN ESTA ACTUALIZACIÓN

* Los nombres de los autores duplicados aparecen en la página Resumen del curso .
* Un hipervínculo en la página de creación de la cuenta generó el error 404.
* La configuración regional checa no se reflejaba del modo esperado en la configuración del reproductor.
* En algunos casos, las aptitudes se muestran como no definidas para los alumnos en curso y no iniciados.
* El tiempo empleado en varios días muestra el tiempo empleado en los informes de transcripciones e inscripciones de alumnos.
* El botón Atrás no responde a los perfiles Administrador y Responsable de la ficha Curso > Puntuación de prueba L2 > Por pregunta y Asistencia y Puntuación respectivamente.
* Para algunas configuraciones regionales, en una plantilla de correo electrónico, falta contenido en el cuerpo del correo electrónico y la traducción de idioma en la plantilla no es coherente.
+++

+++Actualización 83

**Fecha de publicación:** 18 de enero de 2023

### Qué ha cambiado en esta actualización

**Nueva columna**

Una nueva columna, **unenrollmentAllowed**, se añade a course.xlsx. Descargue el archivo de este manual.

**Conector de LinkedIn Learning**

Para Vinculado en el conector de aprendizaje, hay una nueva casilla de verificación introducida El alumno puede darse de baja en la página Filtros . Para obtener más información, consulte [Conector de linkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md).

### Errores Corregidos En Esta Actualización

* Al pasar el cursor sobre los gráficos de barras, la información sobre herramientas del informe del tablero aparece como se esperaba.
* En los informes de Actividad del usuario, el informe Tiempo de aprendizaje empleado muestra datos incorrectos para los datos diarios/mensuales.
* En algunos casos, el gráfico de puntuación de la prueba muestra valores incorrectos.
* En un curso con contenido SCORM con varios intentos establecidos, cuando un alumno intenta realizar el curso, el botón Regresar está desactivado.
* En algunos casos, después de inscribir a un alumno en un curso y descargar un registro de auditoría de correo electrónico, el correo electrónico se envía, pero no aparece en el registro.
* La invitación de calendario de un instructor debe incluir el instructor de texto en la asignatura.
* El icono de la tarjeta de aprendizaje no se refleja en las tarjetas de la ruta de aprendizaje y la recomendación de cursos relacionados incluidas en la página de resumen del curso.
* En la configuración de la página de inicio del alumno, agregue una sección Guardados por mí .
* En el caso de determinadas cuentas, se solicita al usuario que inicie sesión de inicio de sesión único en una cuenta en la que se requiere el ID de Adobe.
* En las zonas horarias con horario de verano, el campo &#39;start_time&#39; se calcula en función de la diferencia horaria actual, no en función de la diferencia horaria en la fecha y hora de inicio reales. Esto causó invitaciones con tiempos incorrectos.
* Cada vez que se repite una certificación, se crea internamente una copia de los cursos subyacentes en la base de datos. Estos cursos aparecen después en la búsqueda, en contra del comportamiento esperado.
* Cuando falla la carga de un archivo CSV, no recibe ninguna notificación por correo electrónico.
* Si los nombres de los campos activos son largos, los nombres desaparecen al arrastrarlos y soltarlos. A continuación, el botón Guardar tampoco funciona del modo esperado.
* Un informe de sesión no se exporta a través de la página de asistencia y puntuación de un curso si el primer usuario del informe tiene un registro en la tabla de grado de actividad con el comentario como nulo.
* Cuando utilice la cuenta de administrador para recuperar las insignias, puede ordenar la lista como se esperaba. Sin embargo, cuando se realiza la misma acción para un alumno, los resultados no se ordenan.
* Si elige un curso de los resultados de búsqueda y luego intenta volver a los resultados de búsqueda con el botón Atrás , los resultados de la búsqueda desaparecen.
* No todos los usuarios se añaden a un grupo de usuarios como instructores en una sesión.
* Las plantillas que tienen varias plantillas de usuario en su interior, su asunto se sobrescribe con algunos valores.
+++

+++Actualización 82

**Fecha de publicación:** 15 de diciembre de 2022

* La API de objetos de interés de GET ahora incluye información de precios, si está disponible.
* Se agrega una nueva columna Completado por a los informes LT. Esto ayuda al administrador a identificar el origen de finalización de un objeto de aprendizaje.
* Hemos añadido un nuevo módulo ILT que puede registrar el estado de aprobado/suspenso del alumno junto con la asistencia. Los instructores ahora pueden marcar a un alumno como asistido con aprobado o asistido con suspenso.
* Un administrador ahora puede solicitar a los alumnos que completen y aprueben antes de consumir el siguiente módulo/curso. Esto es aplicable a requisitos previos, cursos solicitados y programas de aprendizaje.

**Correcciones de errores**

* Problemas de idioma bahasa de la experiencia móvil envolvente en la barra lateral y el pie de página.
* Correcciones de la vista envolvente relacionadas con la previsualización de módulos.
* Una búsqueda de cursos en administrador y autor devuelve resultados en una configuración regional diferente a la escrita.
* Los cambios en las plantillas de correo electrónico de bienvenida no se guardaban después de la edición.
* Los usuarios que tenían diferentes ID de correo electrónico y Adobe ID no podían iniciar sesión en la aplicación móvil.
* Los usuarios se identificaron incorrectamente al unirse a sesiones de Zoom / BJ VC.
+++

+++Actualización 81: versión de noviembre de 2022 de Adobe Learning Manager

**Fecha de publicación:** 5 de noviembre de 2022

**Nota:** Con esta versión de Adobe Learning Manager, los usuarios con cuentas inactivas ya no pueden acceder a sus cuentas mediante subdominios. Se puede acceder a las cuentas mediante el ID de cuenta o mediante la página acapindex.html e introduciendo el ID de correo electrónico.

### Novedades de esta versión

La versión de noviembre de 2022 de Adobe Learning Manager consta de lo siguiente:

* Configuración de SSO múltiple
* Compatibilidad con funciones no registradas
* Mejoras de la página Resumen de formación
* Personalización del reproductor
* Suplantación del alumno y el responsable

Para obtener más información, consulte [Novedades de la versión de noviembre de 2022 de Adobe Learning Manager](/help/migrated/whats-new-2022-november.md).

**Nota:** Con la versión de noviembre de 2022 de Adobe Learning Manager, el zoom dejará de utilizarse [Autenticación JWT para junio de 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). En consecuencia, el conector de Zoom con JWT seguirá funcionando hasta la fecha mencionada, pero recomendamos a los usuarios que creen una aplicación OAuth de servidor a servidor para reemplazar la funcionalidad en su cuenta. Cualquier conexión nueva tendrá la autenticación de Zoom OAuth de forma predeterminada.

### Errores corregidos en esta actualización

* Como alumno, al intentar acceder a un programa de aprendizaje con más de 10 cursos en dispositivos móviles, aparece un mensaje de error.
* Si un curso ha establecido un recordatorio para enviarlo n días después de no cumplir la fecha límite, el correo electrónico se envía n días después de la fecha prevista, pero el número de días que no se ha cumplido la fecha límite es n-1 en lugar de n.
* Un vídeo no se carga en el reproductor si los comentarios de L1 están activados para el curso en la aplicación del alumno y el usuario solo tiene una función de alumno.
* Un correo electrónico de recordatorio de finalización no muestra la hora en la zona horaria del usuario como se esperaba.
* Las transcripciones de alumnos que se generan mediante informes del tablero no respetan los filtros y muestran más información de la necesaria.
* No se puede seleccionar contenido en el que el idioma de la interfaz no se agregue como idioma del contenido.
* Al registrarse automáticamente en un curso por segunda vez, la dirección URL que aparecía era incorrecta.
* Cuando se elimina a un instructor de una sesión de clase virtual, no recibe ningún correo en el que se le notifique la cancelación de la sesión.
* El texto &quot;minuto&quot; en un icono de la página de formación del alumno no se traduce al indonesio bahasa, como se esperaba.
* El tablero de cumplimiento muestra datos incorrectos para los alumnos que no cumplen la normativa.
* Al añadir un informe, no es posible seleccionar cursos o catálogos en los que el idioma de la interfaz no se haya añadido al idioma del contenido.
* Hemos añadido los siguientes idiomas de contenido en esta versión:
   * Búlgaro
   * flamenco
   * Portugués (Brasil)

### Problemas conocidos de esta actualización

* En algunos casos, el gráfico de puntuación de la prueba no se muestra del modo esperado. Al cambiar el tamaño del gráfico, aparece un espacio en blanco al principio. Además, no aparecen todas las preguntas y los datos incorrectos se muestran de forma intermitente.
+++

+++Actualización 80

**Fecha de publicación:** 20 de septiembre de 2022

* Se han solucionado los problemas de inicio de sesión en la aplicación móvil de iOS.
* Se ha corregido un problema con los correos electrónicos devueltos.
* Los instructores recibían una notificación incorrecta incluso antes de que los alumnos realizaran los envíos.
* Un instructor recibe una notificación por correo electrónico aunque un alumno no haya enviado una actividad.
* Después de crear una sesión de clase virtual en MS Teams o Adobe Connect, los instructores no reciben las invitaciones de la sesión.
* Estado incorrecto en una ruta de aprendizaje.
* Mejora del rendimiento de la aplicación.
+++

+++Actualización 79

**Fecha de publicación:** 18 de agosto de 2022

* La confirmación de invitación de calendario para las sesiones ILT / VILT ahora funciona con el calendario de Google.
* Un administrador de la tienda ahora puede ver notificaciones para los usuarios debajo de ellos, incluso si se les elimina como administrador de personas.
* En algunos casos, la inscripción de cursos falla y se muestra el error 500.
* En algunos casos, no es posible modificar una instancia de curso virtual para equipos.
* Los administradores e instructores pueden añadir comentarios para los usuarios que no hayan asistido a las sesiones ILT/VILT.
* Mejoras en el rendimiento al descargar informes de gran tamaño.
* Cuando se devuelve el correo electrónico de un usuario, el administrador recibe una notificación por correo electrónico. El correo electrónico contiene un vínculo que, al hacer clic en él, descarga un archivo CSV con la lista de usuarios cuyo correo electrónico ha sido rechazado. A continuación, el administrador puede realizar las acciones necesarias.
   * El correo electrónico se activa cuando un correo electrónico rebota o cae.
   * El correo electrónico se activa una vez al día para todos los administradores que se añaden a la lista.
   * El vínculo caduca en siete días.
* Aparece un mensaje de error al intentar integrar una cuenta de Adobe Connect ya integrada con otra cuenta de Learning Manager.
+++

+++Actualización 78

**Fecha de publicación:** 4 de agosto de 2022

### Errores corregidos en esta actualización

* Si tiene un curso que contiene un módulo con una vista previa y, a continuación, utiliza una API para recuperar los recursos del curso, la respuesta no contendrá ningún dato de location, contentZipUrl ni contentStructureInfoUrl.
* Respuesta incorrecta después de enviar una solicitud XAPI desde el documento de Swagger, donde el nombre de dominio es learningmanager.
* En la sección /boards/{id}Respuesta de la API /posts, la propiedad &quot;post.attributes.myPoll&quot; aparece como un objeto vacío.
* En algunos casos, para un usuario que no haya iniciado sesión, el botón Añadir al carro está desactivado para algunos cursos o rutas de aprendizaje.
* URL de subdominio incorrecta en la página de construcción de marca.
+++

+++Actualización 7

**Fecha de lanzamiento:** 24 de mayo de 2022

**Problemas resueltos en esta actualización:**

* Los nuevos cursos no respetan la secuencia en la aplicación de Salesforce. Si modifica la secuencia, el curso no se muestra en la secuencia deseada.
* Después de modificar la configuración en la página principal de Classic y guardarla, los cambios no se guardan del modo esperado. Esto sucede intermitentemente.
* El código de HTML se muestra cuando los alumnos comprueban sus notificaciones, lo que afecta negativamente a la experiencia.
* En el tablero, el tiempo dedicado al aprendizaje se muestra incorrectamente como cero horas.

## ACTUALIZACIÓN: Adobe Learning Manager pasará a denominarse Adobe Learning Manager

Esta es una actualización sobre un cambio inminente y le ayuda a prepararse para él.

**Adobe Learning Manager pasará a denominarse como producto a Adobe Learning Manager en julio de 2022.**. Se trata de un esfuerzo estratégico que se está llevando a cabo para reflejar con mayor precisión la alineación del producto con determinadas prioridades empresariales.

El equipo del producto está tomando todas las medidas necesarias para garantizar que su uso de la plataforma no se vea afectado. Puede seguir utilizando el producto de la forma habitual. Los administradores de la plataforma pueden observar el nuevo nombre de la marca en determinadas pantallas en julio.

Como parte de este cambio, se ven afectadas las direcciones URL de acceso de Learning Manager.

Por ejemplo, si la dirección URL de acceso de su cuenta es `https://learningmanager.adobe.com/XYZ`, la nueva URL se `https://learningmanager.adobe.com/XYZ`.

Todas las direcciones URL existentes seguirán funcionando.

Para completar esta acción, póngase en contacto con el departamento de TI de su organización. Para obtener más información, póngase en contacto con nosotros en `learningmanagersupport@adobe.com`.
+++

+++Actualización 76

**Fecha de publicación:** 20 de abril de 2022

* Correcciones en terminologías de productos en algunos informes de tableros.
* Una barra doble (&quot;//&quot;) en la dirección URL de un extremo produjo errores de validación.
* Después de actualizar una página, el porcentaje completado y los últimos campos visitados mostraban información incorrecta.
* Hemos realizado algunos cambios en la forma de calcular el valor Certificado o Plan de aprendizaje.
* Un administrador personalizado podía añadir a todos los usuarios como instructores aunque solo se le permitiera añadir un usuario.
* En un PDF de insignia, se mostraba una fecha de finalización incorrecta.
+++

+++Actualización 75

**Fecha de publicación:** 29 de marzo de 2022

* En algunas cuentas, después de copiar el archivo .csv sin procesar en la ubicación de FTP, la importación de usuarios no se realiza del modo esperado y hay varias notificaciones de errores.
* En versiones anteriores de Learning Manager, para configurar un conector de Zoom, era necesario configurar primero Exavault FTP para copiar el archivo csv. En esta versión, el conector de FTP ya no se utilizará para el archivo csv y, por lo tanto, no es necesario configurar el FTP primero.
+++

+++Actualización 74: instancia de Learning Manager AWS India

**Fecha de publicación:** 15 de febrero de 2022

### Resumen

Una [instancia](https://learningmanagerapac.adobe.com/acapindex.html) de Learning Manager ahora se alojará en AWS en Bombay (ap-south-1). Para los clientes que utilicen esta instancia de India, solo se almacenará la información de identificación personal (PII) y los registros de aprendizaje del usuario en la región de India.

### Qué se admite

La instancia de Adobe Learning Manager India está a la par con otras instancias como las regiones de la UE y EE. UU. en términos de capacidades de funciones. Hay algunas características que no se admiten en la instancia de India. Estos son:

* Pago con tarjeta de crédito para la compra de asientos
* Catálogo de contenido de Creative Cloud
* Aplicación de Slack
* **&#42;** A la espera de la certificación para el cumplimiento de SOC2

### Preguntas más frecuentes

**¿En qué se diferencia esta instancia en Bombay de otros entornos solo de AWS?**

No hay diferencia. La instancia en Mumbai es la misma que [AWS US](http://learningmanager.adobe.com/) o [AWS EU](http://learningmanagereu.adobe.com/) instancias. Esta instancia se aloja en India, y todos los registros de aprendizaje y los datos de los usuarios permanecen en India. Las siguientes funciones no son compatibles en la instancia de India:

* Pago con tarjeta de crédito para la compra de asientos
* Catálogo de contenido de Creative Cloud
* Aplicación de Slack
* **&#42;** A la espera de la certificación para el cumplimiento de SOC2

**¿Este entorno será compatible con el marco común de control (CCF)?**

Sí. La nueva instancia es compatible con Common Control Framework (CCF).
+++

+++Actualización 73

Fecha de publicación: 5 de febrero de 2022

* La compatibilidad con plantillas de correo electrónico ahora está disponible para los idiomas de contenido, incluidos el húngaro y el finlandés.
+++

+++Actualización 72: versión de enero de 2022 de Learning Manager

Fecha de publicación: 15 de enero de 2022

### Novedades y cambios

* Añadir ubicaciones de clase
* Cambios de interacción
* conector de Microsofts Teams
* Cambios en la API
* Cambios web envolventes en dispositivos móviles

<!--
For more information, see What's new in the [**January 2022 release of Adobe Learning Manager**](../whats-new.md).
-->

### Errores corregidos en esta versión

**Biblioteca de contenido**

* La búsqueda de archivos de contenido en carpetas de contenido privadas no funcionaba para usuarios con privilegios de función personalizados. Esto se ha solucionado.

**Cursos**

* La eliminación de un curso o una ruta de aprendizaje no era posible si tenían una asociación histórica con un plan de aprendizaje. Esto se ha solucionado. Los usuarios ahora pueden eliminar un curso o una ruta de aprendizaje si no están asociados actualmente a un plan de aprendizaje.
* Al previsualizar un curso o una ruta de aprendizaje, si el archivo de recursos tiene un nombre largo sin espacios, el nombre de archivo no se ajusta como se esperaba y se desborda en la siguiente línea. Este problema se ha solucionado.
* En el caso de la clase virtual, anteriormente podía crear un módulo sin seleccionar ningún sistema de conferencia de clase virtual en ese momento, ya que en una nueva instancia la dirección URL de clase virtual no tenía la información necesaria. Esto se evita ahora con un mensaje de error en la fase de creación del módulo en el que se le solicita que especifique el sistema de conferencia de clase virtual antes de guardar el módulo.
* La página de la lista de espera mostraba un mensaje de banner engañoso en los usuarios registrados, que se ha eliminado ahora.
* En el caso de la desinscripción masiva de cursos, la ventana emergente para introducir los ID de correo electrónico no aparecía, lo que se ha solucionado.
* La opción de enviar correo electrónico a los alumnos desde la ficha Asistencia y puntuación en la aplicación del administrador y el instructor no excluía a los alumnos desmarcados después de realizar la operación Seleccionar todo . Por lo tanto, Learning Manager enviaba correo electrónico a todos los alumnos. Este problema se ha solucionado ahora.
* El informe de inscripción aparece como No iniciado, aunque un alumno ya haya completado el curso.

**SSO**

* En la configuración de SSO, si el ID de entidad tenía espacios iniciales o de formación, la configuración de inicio de sesión no funcionaba, ahora se gestiona como parte de la corrección.

**Anuncios**

* Como administrador, las fechas de inicio y finalización de un anuncio no se guardaban si el idioma de la interfaz y el contenido se establecía en alemán/español. Este problema se ha solucionado ahora.

**Plantilla de correo electrónico**

* Las invitaciones de sesión se extienden a lo largo de varios días en los que las invitaciones no reflejan la información correcta sobre los días que están bloqueados en algunos clientes de correo electrónico. Esto se ha solucionado.
* Falta la variable &quot;Nombre del lugar&quot; en la plantilla de correo electrónico &quot;Recordatorio de la próxima sesión&quot; para los alumnos de la configuración regional alemana. Esto se ha añadido.
* El vínculo para crear una cuenta como parte del correo electrónico de bienvenida al usuario no tenía en cuenta la configuración regional del usuario, que ahora se ha solucionado.

**Recordatorios por correo electrónico**

* Si los alumnos se inscribían en un curso de formación a través de un plan de aprendizaje, se enviaban correos electrónicos de recordatorio de finalización varias veces en función del número de ediciones realizadas en las fechas de finalización del mismo plan de aprendizaje. Este problema se ha solucionado ahora.

**Usuario**

* El mensaje que se muestra al usuario cuando su cuenta está inactiva/suspendida se ha mejorado, lo que indica que debe ponerse en contacto con el administrador para que habilite sus cuentas de nuevo.

**Actividad**

* Un instructor no podía ver los envíos de alumnos si el nombre del archivo de envío tenía un carácter especial. Esto se ha solucionado.

**Informe**

* Un administrador no ha podido descargar el informe de inscripción en el curso si contiene un alumno que se ha inscrito indirectamente en este curso a través de una ruta de aprendizaje flexible, pero que aún no ha elegido una instancia para este curso en la ruta de aprendizaje. Este problema se ha solucionado ahora.
* La reorganización de informes en el tablero de informes para las funciones de administrador y responsable no conservaba el estado del orden de los informes. Este problema se ha solucionado ahora.

**Contenido**

* El audio en el contenido de formación no se reproducía automáticamente en el modo de vista previa como alumno debido a las políticas de reproducción automática del navegador. Esto se ha solucionado ahora para los navegadores compatibles, excepto Safari.

**Interacción**

* Si un alumno externo se convertía como alumno interno en la misma cuenta, no podía acceder a la tabla de posiciones de interacción en la aplicación del alumno. Este problema se ha solucionado ahora.

**Reproductor**

* El reproductor no mostraba el mensaje de advertencia cuando el usuario intentaba saltar módulos en el curso ordenado que tenía el tipo de módulos AICC. Esto se ha solucionado.
* En determinados cursos adquiridos que tenían módulos de vídeo en la reproducción de casos de LMS sin encabezado, la reproducción no funcionaba para determinados usuarios. Este problema se ha solucionado ahora.

**Tablero de responsable**

* Un responsable no pudo exportar el informe para su equipo directo desde la página de habilidades de equipo de Manager Dashboard. Este problema se ha solucionado ahora.

**Publicar**

* En el caso europeo, el contenido de Learning Manager que se publicaba directamente en Adobe Learning Manager desde Adobe Captivate se publicaba en la configuración regional de Deutsch de forma predeterminada. Esto se ha solucionado.

**API**

* El campo de duración se añade ahora al modelo de ayuda de trabajo.
* Para las API de recomendación, a veces una solicitud de GET devuelve el error 500.
* Al migrar cursos de formación mediante Exavault y si el texto contiene caracteres no ingleses, solía actualizarse con caracteres no utilizables en el texto. Este problema se ha solucionado ahora.

**Localización**

* `NormalTextRun  BCX0 SCXW38820519 For the`Aplicaciones de administrador, autor y alumno, parte del contenido en alemán no aparece del modo esperado.

## Problemas conocidos de esta versión

* En la página Aprendizaje social, al crear una publicación, no es posible grabar un audio ni cargarlo después de pulsar el botón del micrófono. Esta es una limitación del navegador.
* En iOS, los archivos de audio H264 y WMA no son compatibles con el navegador móvil.
* Los alumnos con un signo + en su dirección de correo electrónico no tienen marcado el progreso. Esto es después de que toman un curso de clase virtual en Microsofts Teams.
* En el navegador Safari Mobile, los alumnos no podrán cargar más de 200 mb de archivo en Aprendizaje social. Se trata de una limitación del navegador.
+++

+++Actualización 71

Fecha de publicación: 17 de noviembre de 2021

### Compartir formación con responsables

Learning Manager ofrece un panel de cumplimiento a todos los administradores y responsables. A los gestores les resulta muy útil realizar un seguimiento del cumplimiento de los miembros de su equipo para una formación concreta. Al mismo tiempo, los administradores desean que todos los responsables añadan cursos de formación sobre cumplimiento a su panel y realicen un seguimiento.

En Learning Manager, el **Compartir con responsables** El flujo de trabajo permite a los administradores compartir la formación con los responsables para que puedan ser añadidos al tablero de cumplimiento de un responsable. Por lo tanto, los responsables no necesitan realizar ninguna acción y pueden empezar a realizar un seguimiento del cumplimiento de forma inmediata.

Para obtener más información, consulte  [**Compartir formación con responsables**](../administrators/feature-summary/reports.md#share_training_managers).

### Errores corregidos en esta actualización

* Si hay dos cuentas y la función Ruta de aprendizaje mejorada está desactivada, y hay un catálogo compartido de la primera cuenta a la otra, la ruta de aprendizaje de la segunda cuenta tiene secciones duplicadas en la página del curso.
* Ahora, un FTP personalizado admite sftp://, además de http:// y https://
* El conector de Exavault utiliza ahora las API V2.
* En algunos casos, la calidad de los vídeos no era óptima. El problema se ha solucionado ahora.
* Incluso después de que un alumno haya completado un curso obligatorio y lo haya aprobado el responsable, la certificación permanece en estado Aprobación pendiente .
* Si los nombres de los autores contienen caracteres acentuados, la migración del curso falla.
* Si el campo activo tiene valores en mayúsculas, el campo activo no se guarda del modo esperado.
* No se pueden filtrar las rutas de aprendizaje en función de las aptitudes.
* Cuando un administrador crea una instancia y añade una nueva sesión, un instructor no recibe el correo electrónico de invitación a la sesión. Este problema se produce en cursos de Zoom VC.
+++

+++Actualización 70

Fecha de publicación: 28 de octubre de 2021

### Errores corregidos en esta actualización

* En algunos casos, la información sobre una ruta de aprendizaje no se refleja en una transcripción del alumno.
* El texto dentro del **Marcar finalización** se actualiza para reflejar que la operación es irreversible.
* En algunos casos, la API de objetos de aprendizaje devolvió un error de metadatos.
+++

+++Actualización 69: versión de octubre de 2021 de Learning Manager

**Fecha de publicación:** 09 de octubre de 2021

### Ruta de aprendizaje

La **Versión de octubre de 2021 de Adobe Learning Manager** introduce el concepto de rutas de aprendizaje.

>[!NOTE]
>
>La **Configuración > General** tiene una nueva opción para activar las capacidades ampliadas de las rutas de aprendizaje. Si esta opción está activada, puede añadir rutas de aprendizaje en otra ruta de aprendizaje. Una vez activada, no se puede cambiar la opción.

Las rutas de aprendizaje reemplazan nuestra función existente de programas de aprendizaje. Imagine que los programas de aprendizaje obtienen mejoras eficaces sin eliminar las capacidades existentes. Además, la función se marca como una ruta de aprendizaje.

Para obtener más información, consulte [***Rutas de aprendizaje***](../administrators/feature-summary/learning-paths.md).

### Otros cambios

* Nueva aplicación de Salesforce
* Centro de contenido
* Informar de cambios
* Informe de resumen de sesión
* Cambios de índice del reproductor
* Cambios en la API
* Cambios relacionados con el conector

Para obtener más información, consulte [***Novedades de la versión de octubre de 2021 de Learning Manager***](../whats-new.md).

### Errores corregidos en esta actualización

* Las plantillas de correo electrónico como, por ejemplo, Darse de baja del curso, Darse de baja del programa de aprendizaje o Darse de baja de la certificación, no reflejan las últimas terminologías de productos definidas en el archivo .csv. Ahora, el texto predeterminado de las plantillas de correo electrónico admite terminologías personalizadas.
* El idioma de usuario en Learning Manager no se admite en el flujo de trabajo Publicar en Learning Manager. Si el idioma del usuario es diferente, la publicación en Learning Manager se realiza en inglés.
* Si añade muchos catálogos a una función personalizada, se produce un error al actualizar la función. Ahora el límite de número de catálogos se ha aumentado a 50 catálogos.
* En algunos casos, los cursos de formación que se eliminan siguen siendo visibles en un catálogo. Este problema solo se producía en la aplicación de administración y se ha solucionado ahora.
* Cuando se cambia la función de responsable de un usuario a otro, la función de responsable del usuario anterior se reflejaba en la interfaz de usuario. Esto se ha solucionado. Este problema solo se producía para usuarios externos, no internos.
* En algunos casos específicos, la importación falló para un gran conjunto de usuarios que se importaban a través del archivo CSV de usuarios. Este problema se ha solucionado ahora.
* Una transcripción de aprendizaje no muestra la fecha de finalización de un certificado externo si se añade un curso obligatorio después de crear un certificado externo y se inscribe un usuario en él. Esto se ha solucionado.
* Un certificado no muestra el nombre adaptado del alumno como se esperaba. Esto se ha solucionado.
* En el caso de las sesiones de clase virtual de Zoom, un instructor no siempre recibe la invitación para la sesión. Esto se ha solucionado. El instructor recibe ahora la comunicación necesaria.
* Un alumno no recibe invitaciones para una sesión si las plantillas de nivel de curso están activadas, pero las plantillas de nivel de cuenta están desactivadas. Esto se ha solucionado.
* Para zonas horarias específicas, los recordatorios por correo electrónico se entregaron un día después de lo esperado. Esto se ha solucionado.
* Los alumnos no reciben correos de notificación de sesión si determinadas plantillas de correo electrónico están desactivadas.
* En caso de que los autores, los administradores actualizaran una reunión de BlueJeans, la dirección URL de la reunión de BJ dejaba de poder utilizarse. Esto se ha solucionado.
* Al ejecutar la API de GET/LO en algunos casos, los cursos que forman parte de un programa de aprendizaje no se devuelven.
* Si el alumno intenta cargar contenido cuyo nombre tiene espacio en blanco, se produce un error interno del servidor.
* Los PDF de insignias generados para los alumnos tenían problemas de formato cuando se generaban en configuraciones regionales distintas al inglés. Estos problemas se han solucionado ahora.
+++

+++Actualización 68

Fecha de publicación: 28 de septiembre de 2021

### Errores corregidos en esta actualización

* En el navegador móvil, se han habilitado vínculos profundos para lo siguiente:

   * Todos los tableros
   * Tablero público y publicación
   * Tablero privado y publicación con acceso
   * Tablero privado y publicación sin acceso
   * Tablero restringido y publicación
   * Comentar en publicación
   * Responder al comentario
   * Perfil de usuario social

* En el caso de las cuentas que utilizan dominios personalizados, la aplicación del alumno no muestra el icono de favoritos.
* En AEM, el componente Learning Manager elimina la configuración de otros componentes.
* La página de ayuda AEM componente redirige a una ubicación incorrecta.
* Externalización de la obtención y el almacenamiento de mensajes de correo electrónico y tokens de usuario para que los usuarios puedan implementar su propio back-end de almacenamiento en lugar de utilizar AEM nodos de usuario.
* Al editar la descripción de texto sin formato en Cursos, Programas de aprendizaje, Certificados y Ayudas de trabajo, se muestra un mensaje de advertencia.
* Los informes del tablero de responsable no se descargan cuando un usuario tiene funciones personalizadas y de responsable.
* Un mensaje de correo electrónico de resumen muestra un valor incorrecto de la actividad de formación.
* En algunos casos, Learning Manager se comporta de forma inesperada al pasar de la Tienda de contenido a la página del alumno.
* En la aplicación de redes sociales, los filtros no funcionan del modo esperado en la vista de lista.
* El correo electrónico de bienvenida que reciben los usuarios internos también lo reciben usuarios externos.
* Añada el widget de Learning Manager en la plantilla de página en AEM.
* Si desea volver a publicar un certificado después de eliminar un curso, no puede hacerlo.
* Los alumnos no reciben mensajes de correo electrónico que contengan detalles de una sesión.
+++

+++Actualización 67: actualizaciones de Azure

Esta actualización introduce una nueva instancia de Azure.

>[!NOTE]
>
>En la instancia, no se admiten los elementos siguientes:
>
>* [Dominio personalizado](../custom-domain.md)
>* [Compra con tarjeta de crédito](../administrators/feature-summary/billing-management.md)
>* [Catálogo de contenido](../administrators/feature-summary/content-catalogs.md)

+++

+++Actualización 66: versión de agosto de 2021 de Learning Manager

La **Agosto de 2021** **versión de Adobe Learning Manager** se centra en mejorar la experiencia del alumno, los informes y los flujos de trabajo administrativos. Algunos de los aspectos destacados son:

* **Tienda de contenido:** Learning Manager ofrece ahora más de 70 000 cursos de diferentes campos, como, por ejemplo, tecnología, administración, liderazgo, etc.
* **Compatibilidad con accesibilidad mejorada:** La compatibilidad de accesibilidad con la función de alumno se refuerza mediante la navegación por teclado mejorada, la capacidad del lector de pantalla y el cumplimiento normativo de la relación de contraste.
* **Formato de texto enriquecido:** Learning Manager ahora ofrece edición de texto enriquecido para descripciones de cursos, programas, certificados y ayudas de trabajo. Esto permite a los autores especificar descripciones en texto enriquecido, incluidos hipervínculos, imágenes y otras opciones de formato de texto, en lugar de texto sin formato.
* **Clasificación por estrellas:** Ahora, un alumno puede valorar un curso con una escala de 5 puntos. Un administrador puede seleccionar entre la clasificación de eficacia existente o la clasificación de 5 estrellas.
* **Integración en Badgr:** Los alumnos ahora pueden autorizar a Learning Manager a insertar automáticamente las insignias que se han obtenido en Learning Manager en la cuenta de Badgr, desde la que se pueden compartir las insignias en redes sociales.
* **Exportar eventos de aprendizaje a Salesforce:** Learning Manager ahora ofrece la posibilidad de exportar algunos eventos específicos de Learning Manager, como la adición y la inscripción de nuevos usuarios y la finalización de cursos a un inquilino de Salesforce, y proporciona la posibilidad de vincularlos al objeto Usuario o Contacto adecuado en Salesforce.

Para obtener más información, consulte [***Novedades y cambios en la versión de agosto de 2021 de Learning Manager***](../whats-new.md).


**Fecha de publicación:** 7 de agosto de 2021

### Errores corregidos en esta actualización

**Experiencia del alumno**

* Después de añadir un alumno a dos grupos de usuarios y un plan de aprendizaje, el alumno se inscribe en una instancia diferente del mismo curso.
* En algunos casos, después de la inscripción e iniciar el curso, el curso no se reproduce como se esperaba.
* La descripción del curso muestra etiquetas de HTML, lo que se ha solucionado.
* Si comenta una publicación en un tablero social que abarca varias líneas, el comentario aparece en una sola línea. Esto se ha solucionado.

**Creación**

* En algunos casos con inscripciones automáticas, los alumnos reciben varios mensajes de correo electrónico de inscripción.

**Informes**

* Cuando la interfaz se establece en algunas configuraciones regionales distintas a la inglesa, las transcripciones de alumnos no se generan del modo esperado.
* Posibilidad de restablecer el progreso de un curso dentro de un programa de aprendizaje y una certificación.
* Si un archivo CSV contiene campos activos con el mismo nombre, pero con una distinción entre mayúsculas y minúsculas diferente, el archivo CSV genera una excepción.

**Otros**

* La opción para editar puntuaciones y comentarios debe estar desactivada cuando no se ha seleccionado ningún alumno o si la asistencia del alumno seleccionado no está marcada.
* Los valores de los campos activos se muestran en minúsculas en el cuadro de diálogo Editar usuario, aunque un usuario haya añadido previamente los valores en mayúsculas.
* Capacidad de los administradores y la administración para ver las aprobaciones pendientes de los cursos. Esto permite a la administración garantizar que los responsables realicen un seguimiento del aprendizaje y la formación de los empleados, así como permitir que los administradores de Learning Manager aprueben la inscripción en cursos según sea necesario.
* Un usuario que tenga un permiso de autor o de administrador/autor personalizado no puede editar una ayuda de trabajo creada por otro usuario.
* En la función de administrador, cuando el usuario se desplaza a Curso > Instancia y selecciona la opción &quot;Alumnos inscritos&quot; de cualquier instancia, anteriormente se solían mostrar los alumnos de &quot;Instancia predeterminada&quot;. El administrador debe cambiar la instancia manualmente desde el menú desplegable. Ahora, Learning Manager desplaza correctamente al usuario a la página de alumnos con la instancia correcta seleccionada.

**Aplicación de dispositivo**

* En dispositivos Android y iPhone, un alumno no puede iniciar módulos de cursos de forma aleatoria. Al hacerlo, se produce el error 401 no autorizado.
* Un alumno puede analizar dos códigos QR, pero al analizar el tercer código QR, se muestra un mensaje de error.
* En algunos dispositivos Android y iOS, un archivo no se abre del modo esperado para algunos cursos descargados.
* Al intentar abrir una ayuda de trabajo, aparece un mensaje de error.
* La aplicación del dispositivo se comporta de forma inesperada cuando se consume un programa de aprendizaje sin conexión.
* Cuando un alumno vuelve a estar en línea y abre la aplicación, esta se bloquea en la pantalla de bienvenida.
* A veces, cuando un usuario vuelve a estar en línea, la aplicación cambia a la vista clásica.
* A veces, cuando un curso se consume sin conexión, el progreso no se guarda.
* A veces, el nombre de un curso no se muestra del modo esperado desde el principio cuando es largo.
* En la página del catálogo, los cursos no se ordenan del modo esperado.
+++

+++Actualización 65

Fecha de publicación: julio de 2021

### Errores corregidos en esta actualización

* Problemas con inicios de sesión para usuarios.
* La plantilla de correo electrónico de inscripción en el curso del responsable no muestra la fecha límite de finalización del curso si se añade la variable a la plantilla.
* TLS 1.0 y TLS 1.1 ya no se usan.
* Problemas con la eliminación de datos del RGPD para un usuario.
+++

+++Actualización 64

Fecha de publicación: julio de 2021

### Errores corregidos en esta actualización

* La notificación de inscripción se envía a los alumnos que ya se han inscrito en un curso.
* Cuando se genera un certificado personalizado como insignia, el formato de fecha no se admite en el idioma alemán.
+++

+++Actualización 63

Fecha de publicación: junio de 2021

### Errores corregidos en esta actualización

* Puede crear un usuario con un nombre en blanco en un archivo csv.
* Si hay un carácter &#39;/&#39; en el campo activo, después de crear un trabajo para descargar user.csv, el estado del trabajo no cambia de &quot;Enviado&quot; a &quot;Completado&quot;.
* Los módulos ordenados no respetan la secuencia.
* Cuando se elimina un autor externo, el curso que ha creado el autor ya no está disponible.
* La búsqueda en un objeto de aprendizaje con más de una aptitud produce resultados inesperados.
+++

+++Actualización 62

Fecha de publicación: junio de 2021

### Errores corregidos en esta actualización

* No se puede iniciar sesión en la aplicación cuando se inicia sesión en la cuenta mediante SP-login.
* Los vídeos no se procesan desde Brightcove como se esperaba.
* La API userGroupInfo no está visible al visitar el programa de aprendizaje en cualquiera de las aplicaciones.
* No se puede buscar un programa de aprendizaje y una certificación retirados al crear un informe del tablero.
* Un autor no puede editar ni actualizar una ayuda de trabajo creada por otro autor.
* La API para el envío de archivos no funciona del modo esperado en el clúster de la UE.
+++

+++Actualización 61

Fecha de publicación: mayo de 2021

### Errores corregidos en esta actualización

* Mejora del rendimiento en llamadas de userGroupInfo.
* Después de activar los nuevos perfiles de Brightcove, Learning Manager admite contenido con módulos de vídeo y audio.
* Las transcripciones de aprendizaje no capturan los datos si se selecciona un intervalo de fechas limitado.
* Se envía una invitación de sesión a los alumnos inscritos para todas las sesiones, incluso cuando solo se añade una nueva sesión.
* Los módulos de audio no se cargan del modo esperado.
+++

+++Actualización 60

Fecha de publicación: abril de 2021

### Errores corregidos en esta actualización

**Informe**

* Después de crear un informe, si busca un curso retirado, no podrá hacerlo.
* Los errores de un informe se propagan a otros. Como resultado, esos informes dieron lugar a errores.

**Ayudas de trabajo**

* Después de descargar una ayuda de trabajo, no puede eliminarla.

**Reproductor**

* Los subtítulos de WebVTT no aparecen del modo esperado.

**Aplicación del alumno**

* En la página Resumen de certificación, la certificación externa no muestra la duración añadida por un autor.
* Añadir la opción **Todo** en el filtro Aptitud.
* Los alumnos recibían varios mensajes de correo electrónico de resumen.
* El número de filas seleccionadas no se refleja como se espera en una página.

**AEM componente**

* Los widgets no se actualizan del modo esperado después de actualizar la página.

**Localización**

* Algunas cadenas alemanas no se localizan del modo esperado.
* La traducción de cadenas se establece de forma predeterminada en inglés si un alumno no ha seleccionado la interfaz y el idioma del contenido.

**Certificación**

* El orden del módulo se puede omitir si no se cumplen los requisitos previos.

**Navegador**

* Las aplicaciones de autor, responsable o alumno no se muestran del modo esperado en IE 11.

**Interacción**

* Los puntos de interacción no se canjean del modo esperado.

**Biblioteca de contenido**

* Los cursos de la aplicación de prueba de contenido no funcionan del modo esperado.

**Reproductor**

* El reproductor solo se carga en el espacio donde está presente el widget.
* Los vídeos de un módulo de Captivate no se reproducen del modo esperado.

**Conector**

* En algunos casos, los archivos se eliminan de un conector de FTP/Box.
* Los archivos se eliminan de FTP si los archivos se actualizan con los mismos nombres.
* Un evento de BlueJeans admite la paginación si el número de eventos es superior a 100.

**Actualización 3.3 de la aplicación para dispositivos móviles: marzo de 2021**

Fecha de publicación: 26 de marzo de 2021

### Novedades y cambios {#whatsnewandchanged}

La actualización 3.3 de la aplicación móvil de Captivate Learning Manager presenta una nueva página de inicio que admite encabezados y recomendaciones de formación basadas en Inteligencia artificial. Esta página principal está disponible para todas las cuentas configuradas para la nueva opción Diseño envolvente. Las cuentas configuradas con el diseño clásico seguirán viendo la página principal clásica o heredada. No deben observar ningún cambio en la página principal.

Además, esta actualización también permite a los alumnos descargar su insignia como PDF y una imagen. La actualización también introduce una ventana emergente de comentarios, que permite a los alumnos proporcionar comentarios sobre la aplicación de forma anónima.

Para obtener más información, consulte  [aplicación de dispositivo de Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

Siga leyendo para obtener más información.

#### Nueva página de inicio

Para todas las cuentas que tienen activada la opción Diseño envolvente, hay una nueva página de inicio que admite la configuración de Diseño envolvente.

#### Valoración de votos

En esta versión, Learning Manager solicita al usuario que proporcione comentarios sobre su experiencia con la aplicación móvil.

#### Descargar insignia

Esta actualización permite a los alumnos descargar sus insignias en formato de PDF e imagen.

<!--## Previous update releases {#previousupdatereleases}-->
+++

+++Actualización 60: versión de febrero de 2021 de Learning Manager

Fecha de publicación: 20 de febrero de 2021

### Novedades y cambios {#Whatsnewandchanged-1}

* Vista de tablero en Aprendizaje social.
* Personalización del banner social.
* Filtros de catálogo en la aplicación del alumno.
* Dar de baja de formación.
* Importar usuarios desde contactos de Salesforce.
* ...y muchos más.

Para obtener más información, consulte Novedades de la [Actualización de febrero de 2021 de Learning Manager](../whats-new.md).

### Errores corregidos en esta actualización {#bug-fixes}

**Certificación**

* En algunos casos, un alumno no podía intentar realizar de nuevo un curso que formara parte de una certificación, aunque el número máximo de intentos del curso se hubiera establecido en infinito. Este problema se ha solucionado ahora.
* En algunos casos, un alumno no puede inscribirse en una certificación debido a la **Inscribir** el botón no está visible como se esperaba.

**Biblioteca de contenido**

* URL de ayuda incorrecta en el **Añadir nuevo contenido** página. Se ha actualizado la dirección URL correcta.

**Curso**

* Un informe de puntuación de prueba L2 descargado para un módulo de contenido AICC muestra una puntuación incorrecta en la columna Puntuación total del usuario / Puntuación de prueba. Este problema se ha solucionado.
* La descarga de recursos de un curso no funcionaba si era un duplicado de otro curso y si el alumno no tenía acceso al curso original que se utilizó para crear un curso duplicado.
* Las imágenes del banner no se eliminaban cuando el autor las eliminaba cuando el curso estaba en estado Borrador. Este problema se ha solucionado.

**AEM**

* Después de insertar el componente Learning Manager en AEM, la página tardaba mucho tiempo en cargarse, lo que impedía el acceso a los demás componentes. Este problema se ha solucionado.

**Administrador**

* Los cursos que se han retirado no aparecen en los resultados de búsqueda del modo esperado. Este problema se ha solucionado.
* El administrador no pudo buscar cursos retirados en **Aplicación de administración** -> **Informes personalizados** -> **Informes de Excel** -> **Informes del curso**, que ahora se ha solucionado.

* La descarga de un informe de prueba como Excel no funciona si el archivo contiene alumnos que han consumido los cursos de formación antes y después de la actualización de contenido. Este problema se ha solucionado.
* La carga de CSV falla si los campos activos contienen caracteres especiales. Esto se ha solucionado.
* En algunos casos, cuando un alumno realiza una prueba creada en Captivate, las respuestas no se capturan del modo previsto.
* Después de crear una suscripción e intentar editarla, el **Guardar** y **Cancelar** los botones no aparecen como se esperaba. Esto se ha solucionado.

**Reproductor**

* Para un tipo específico de contenido del escenario de reanudación de SCORM-2004 no funcionaba. Por lo tanto, los alumnos tenían que desplazarse hasta el punto en el que se quedaron. Esto se ha solucionado. El contenido ahora debe reanudarse desde el punto en el que lo dejó el usuario.
* Después de inscribirse en un curso, en algunos casos, el contenido no se reproduce del modo esperado. Este problema se ha solucionado.

**Darse de baja**

* Un informe de inscripción solo muestra 20 alumnos que se han dado de baja, incluso aunque haya más alumnos que se han dado de baja del curso/certificación. Este problema se ha solucionado.
* Se ha producido un problema al exportar la lista de alumnos dados de baja en el informe de inscripción en algunos casos. Esto se ha solucionado.

**Programa de aprendizaje**

* En un plan de aprendizaje flexible, si un alumno se inscribe solo en una instancia del curso, al hacer clic en el vínculo de los otros cursos cuyas instancias no se han seleccionado, se abre una página en blanco.

**Alumno**

* Algunos alumnos, cuyos nombres de usuario tienen caracteres especiales, no reciben las notificaciones por correo electrónico que esperaban.
* En la vista envolvente, en algunos casos, el widget de calendario no muestra las próximas sesiones de clase virtual del modo esperado.
* En la aplicación del alumno, el **Aptitud** El filtro no funcionó como se esperaba. Este problema se ha solucionado.

**Buscar**

* En un escenario específico, el responsable no podía buscar anteriormente un grupo de usuarios del responsable. Este problema se ha solucionado ahora para la función de responsable.

**Grupo de usuarios**

* Al exportar un informe de grupo de usuarios con más de 500 usuarios, los valores de datos y los encabezados de columna del informe no coincidían; este problema se ha solucionado.
* Cuando el administrador editaba la firma de correo electrónico en las plantillas de correo electrónico y añadía varias líneas, solo aparecían etiquetas html en la interfaz de administración. Este problema se ha solucionado ahora.
* En **Aplicación de administración > Catálogo > Buscar catálogo**, no se puede buscar.

**Usuarios**

* Se eliminaban algunos usuarios externos activos. Hemos realizado algunos cambios y el problema se ha solucionado ahora.

**Importar**

* La importación de un archivo csv falla si el encabezado csv contiene espacios en blanco finales o si el correo electrónico de un usuario contiene acentos o caracteres diacríticos.

**Envío de actividad**

* En la página de envíos de actividad de la aplicación del instructor, el valor de fecha enviado se solapaba con el nombre del archivo si era largo; se ha solucionado este problema de la interfaz de usuario.

**Instructor**

* Un instructor recibe invitaciones de sesión para todas sus sesiones, aunque solo se haya añadido una nueva sesión. Este problema se ha solucionado.

**SCORM**

* Para cierto contenido de SCORM, hay pocos problemas relacionados con el navegador, problemas de navegación del reproductor e incoherencias en el registro de la puntuación de la prueba. Estos problemas se han solucionado.

**SAML y SSO**

* Hemos actualizado el mensaje de error que aparece cuando caducan las credenciales de SSO.

**API de Learning Manager**

* La API getlearningObject devolvía datos de inscripción incorrectos debido a problemas en el almacenamiento en caché. Este problema se ha solucionado.
* Ahora, una sesión de clase virtual muestra la dirección URL de la reunión en el campo Ubicación de una invitación a la reunión.
* Si ha configurado varias integraciones de proveedores de clase virtual y alguna de ellas no funciona del modo esperado, el menú desplegable de selección de clase virtual solía mostrar una lista vacía. Esto se ha solucionado. Las integraciones de clases virtuales restantes se enumeran ahora correctamente.
* Las plantillas de clase virtual de Connect no se cargan del modo esperado cuando un instructor se une a la sesión.
* Se muestra una duración incorrecta en la interfaz de usuario después de migrar módulos con duración en el archivo csv module_version.
* En algunas cuentas, la actualización de un usuario no funciona del modo esperado. Esto se ha solucionado.

### Problemas conocidos de esta actualización {#known-issues}

* Cuando se utiliza el **Duración** En el filtro de la aplicación del alumno, es posible que el contenido y el filtro no estén sincronizados si el alumno utiliza otra configuración regional de contenido y no forma parte de la instancia predeterminada en términos de inscripción.

>[!NOTE]
>
>La formación &#39;**Duración**&#39; y &#39;**Formato** Los filtros &#39; se identifican en función del contenido de formación disponible para la instancia predeterminada y la configuración regional preferida de la cuenta.

+++

+++Actualización 59

## Actualización 59

Fecha de publicación: 18 de diciembre de 2020

### Conector de eventos de BlueJeans {#bluejeanseventconnector}

El conector de eventos de BlueJeans conecta los sistemas de Learning Manager y BlueJeans para automatizar la sincronización de datos. Con este conector, puede:

* **Configurar sesiones virtuales mediante eventos de BlueJeans:** Configure un nuevo evento en BlueJeans y configure una sesión de clase virtual en Learning Manager seleccionando el evento de BlueJeans adecuado. Los detalles de fecha y hora se seleccionan automáticamente en los eventos de BlueJeans.
* **Sincronización automatizada de finalización de usuarios:** Un proceso automatizado de sincronización de finalización de usuarios permite al administrador de Learning Manager obtener automáticamente los registros de finalización de los eventos de BlueJeans.

Este nuevo conector requiere un conjunto independiente de credenciales para configurarlo.

Para obtener más información, consulte [***Conector de eventos de BlueJeans***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Actualización 58: versión de diciembre de 2020 de Learning Manager

## Actualización 58: versión de diciembre de 2020 de Learning Manager

Fecha de publicación: 5 de diciembre de 2020

### Novedades y cambios {#Whatsnewandchanged-2}

Esta versión se centra en lo siguiente:

* Nueva experiencia de página de inicio del alumno
* Diseño interactivo para una experiencia web móvil para la función de alumno
* Recomendación basada en Inteligencia artificial para alumnos
* Correos electrónicos de resumen semanales
* Lista de comprobación
* Integración de Marketo Engage
* Dominio personalizado
* Importación de puntuaciones de pruebas de Adobe Connect
* Vínculo profundo al catálogo para alumnos
* Mejoras de aprendizaje de linkedIn
* ...y muchos más

Para obtener más información, consulte  [***Novedades de la versión de diciembre de 2020 de Adobe Learning Manager***](../whats-new.md).

### Funciones no compatibles en la experiencia móvil envolvente {#unsupportedfeaturesinmobileimmersiveexperience}

Las siguientes funciones no son compatibles:

* Aplicación social: se redirige a un alumno a la experiencia clásica si este hace clic en el widget Social de la página de inicio
* Configuración de perfil/Editar perfil
* Ver insignia/aptitudes
* Tabla de posiciones: se redirige a un alumno a la experiencia clásica si hace clic en el widget Tabla de posiciones de la página de inicio.
* Descargar ayudas de trabajo.
* Opciones de filtro en Buscar.

### Errores corregidos en esta actualización {#bug-fixes-1}

* No se puede eliminar una carpeta de contenido si la carpeta de contenido contiene contenido eliminado.
* El plan de aprendizaje permite a los administradores configurar un curso con instancias automáticas. En un curso con el módulo de envío de actividad, la información del instructor no se configuraba antes correctamente. Ahora, Learning Manager asigna automáticamente al instructor desde la instancia predeterminada a esta instancia automática.
* Una insignia personalizada con una etiqueta de catálogo con un espacio no permite que el PDF se descargue del modo esperado.
* Un informe descargado desde el tablero es diferente del correo electrónico recibido para el informe del tablero.
* Una transcripción del alumno no tiene datos actualizados para una certificación recurrente.
* Después de iniciar un curso, si deja que se agote el tiempo de espera del curso, el número de intentos no se muestra del modo esperado. A veces, también aparece una pantalla en blanco al intentar realizar un curso varias veces.
* Se produce el error 5xx después de cargar un módulo.
* Un tablero social privado no está visible para todos los alumnos.

### Problemas conocidos de esta actualización {#known-issues-1}

Después de completar un curso o una certificación, no aparece de inmediato la ventana emergente de comentarios. Este problema solo se produce cuando se realiza el curso en la interfaz de usuario envolvente. Si se realiza en la interfaz de usuario clásica, la ventana emergente de comentarios se muestra del modo esperado.

+++

+++Actualización 57

## Actualización 57

Fecha de publicación: 23 de septiembre de 2020

**Biblioteca de contenido**

* En la biblioteca de contenido, al retirar un contenido, no se elimina el contenido de la **Publicado**. Al actualizar la página, el contenido retirado ya no se muestra.
* Al crear una carpeta de contenido, el **Nombre** no se marca como obligatorio, que de hecho es un campo obligatorio.

**Solicitud del cliente**

* Para identificar todos los cursos en los que está inscrito cada alumno y si los ha completado, incluya los siguientes campos en el tablero, Informe de suscripción:

   * UUID
   * Dirección de email

**Transcripciones de alumnos**

* La generación de una transcripción del alumno en la configuración regional indonesia generaba errores.

**Buscar**

* No se puede buscar un curso específico. Esto se ha solucionado.

+++

+++Actualización 56: aplicación móvil

Fecha de publicación: 25 de agosto de 2020

### Realizar cursos desde LinkedIn Learning {#takecoursesfromlinkedinlearning}

Learning Manager ya admite cursos de LinkedIn Learning en la plataforma de aprendizaje. Ahora los alumnos pueden realizar estos cursos de LinkedIn Learning en la aplicación móvil de Learning Manager. En la aplicación del dispositivo, busque un curso e inícielo.

Para obtener más información, consulte Realizar cursos desde [***LinkedIn Learning***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin).

### Notificación de inserción para inscripciones de administradores {#pushnotificationforadminenrollments}

Cuando el administrador inscribe alumnos en cursos de formación, los alumnos reciben notificaciones sobre las inscripciones.

Las notificaciones push ahora también son compatibles con los anuncios.

### Comentarios de L1 obligatorios {#mandatoryl1feedback}

En su última versión de agosto de 2020, Learning Manager permite a los administradores configurar los comentarios de L1 para que todas las preguntas sean obligatorias. Ahora se admite lo mismo desde la perspectiva del alumno en la aplicación móvil.

### Mejoras de la interfaz de usuario {#userinterfaceenhancements}

**Vínculos de pie de página**

El administrador puede configurar varios vínculos de pie de página en la vista del administrador en la Web. Los alumnos ahora pueden acceder a estos vínculos tocando los iconos de hamburguesa y Ayuda .

De forma predeterminada, habrá dos vínculos y el administrador puede añadir otros tres (a través de la vista de administrador en la web) que aparecerán en la aplicación.

**Vista de tarjetas para objetos de aprendizaje**

De forma predeterminada, en las secciones Mi aprendizaje y Catálogo de la aplicación, los cursos de formación aparecen como tarjetas en lugar de como listas. Este es un cambio para los alumnos, ya que anteriormente la vista predeterminada era &quot;Vista de lista&quot;.

Sin embargo, los alumnos pueden alternar entre la vista de lista y la vista de tarjetas.

+++

+++Actualización 55: versión de agosto de 2020 de Learning Manager

Fecha de publicación: 23 de agosto de 2020

### Novedades y cambios {#Whatsnewandchanged-3}

Esta versión se centra en lo siguiente:

* Mejoras de informes
* Carpetas de contenido privado
* FTP personalizado
* Compatibilidad de subtítulos en vídeos
* mejoras de Power BI
* Mejoras de comentarios
* API nuevas y modificadas
* Cambios en la política de retención de datos
* ...y muchos más

Para obtener más información, consulte  [***Novedades de la versión de agosto de 2020 de Adobe Learning Manager***](../whats-new.md).

### Notas sobre esta versión {#notes}

* La generación de una transcripción de alumno (~1 GB) tarda menos de 15 minutos en completarse.
* En versiones anteriores de Learning Manager, las columnas de transcripciones de alumnos Puntuación de prueba y Puntuación de prueba más alta se utilizaban para proporcionar la puntuación y la puntuación máxima con el formato 25/100. Para mejorar la legibilidad y el análisis, la puntuación de prueba también se exporta como columnas independientes: **Puntuación_de_prueba, Puntuación_máx._de_prueba, Puntuación_más_alta_de_prueba y Puntuación_más_alta_de_prueba_máx.**. Estos permiten a los administradores realizar cálculos y análisis rápidos.

### Errores corregidos en esta actualización {#bug-fixes-2}

**Conector**

* Un alumno no puede participar al mismo tiempo en dos reuniones diferentes creadas por dos autores diferentes.
* Al hacer clic en la opción Administrar conexiones desde la tarjeta Adobe Connect, se accede a la página de conexión FTP.
* Una sincronización de FTP programada se cierra con una excepción.
* Hay problemas relacionados con la contraseña al conectarse a Exavault.

**Curso**

* Puede crear un módulo de clase virtual sin seleccionar ningún sistema de conferencia. Como efecto secundario, el proceso de creación de un curso genera el error 500.
* Un alumno no puede descargar recursos aunque esté inscrito en un curso que se ha duplicado.
* Al previsualizar un curso como alumno, un administrador o un autor no pueden descargar recursos a menos que estén inscritos en el curso.

**Aplicación de dispositivo**

* En casos de inscripción específicos, el gráfico de rosquilla en Mi aprendizaje pendiente muestra distintos valores de la aplicación del alumno en el navegador y en la aplicación para dispositivos móviles.

**Certificación**

* El filtro de informe Estado no funciona del modo esperado al intentar descargar un informe del tablero para la certificación.

**Buscar**

* En la página Catálogo de alumnos, al intentar buscar un curso por su nota, no aparecen resultados de búsqueda.

**SCORM**

* Para algunos contenidos, el reproductor SCORM muestra una pantalla en blanco.
* El contenido de Storyline se identifica como contenido de Captivate si el proyecto de Storyline publicado contiene un objeto web que señala a la salida del Captivate publicado.
* El contenido de SCORM no se puede iniciar debido a una dirección URL incorrecta.

**Función personalizada**

* En determinados casos, un administrador personalizado no puede ver la lista completa de objetos de aprendizaje.
* Un administrador personalizado no puede buscar un programa de aprendizaje o una certificación en los informes del tablero.
* Un administrador personalizado no puede buscar un responsable en un tablero.
* Las transcripciones de alumnos generadas por un administrador personalizado no contienen los datos de usuarios eliminados.
* Un autor o un administrador personalizados no pueden duplicar un programa de aprendizaje, un curso o una certificación.

**Informes**

* La columna Tipo de una transcripción de alumno muestra el valor como curso para los cursos que forman parte de una certificación, si el alumno ha anulado su inscripción a la certificación.

**Aptitudes**

* Al añadir una aptitud para un curso, se producen algunos problemas al buscar una aptitud.

**Interacción**

* Si se establecen muchos usuarios como confidenciales, al hacer clic en la ficha del alumno confidencial en Internet Explorer y Edge, el navegador se comporta de forma inesperada.
* Cuando se cambia la frecuencia de un criterio, los puntos calculados con una frecuencia anterior se añaden al cálculo actual.

**Administrador**

* No se puede marcar la asistencia de los alumnos si se cambia la instancia del curso asignada a un programa de aprendizaje.

**Plantillas de correo electrónico**

* En los programas de aprendizaje y las certificaciones, falta el botón de alternancia en la plantilla de correo electrónico.

**Biblioteca de contenido**

* El contenido de SCORM no se inicia del modo esperado debido a una dirección URL incorrecta.

**Transcripciones de alumnos**

* Al generar transcripciones de alumnos, si añade un alumno eliminado en el cuadro de entrada Seleccionar alumnos y, a continuación, activa la opción &quot;Incluir datos de alumnos eliminados&quot; en Avanzado, la página se comporta de forma inesperada.

**Buscar**

* No se puede buscar un curso mediante sus notas.

**Informes de Excel**

* Si el informe de seguimiento de auditoría de un usuario tarda más de una hora en descargarse debido a datos grandes o a un procesamiento lento, la conexión se agota y el informe nunca se descarga.
* En una transcripción de alumno, la columna Tipo se muestra como &quot;Curso&quot; en lugar de &quot;Certificación&quot; para los cursos que forman parte de la certificación, si el alumno ha anulado su inscripción a la certificación.

**Aplicación del alumno**

* Un alumno puede realizar un curso solicitado de forma desordenada accediendo a los cursos mediante un correo electrónico de cancelación de la inscripción o una notificación de cancelación de la inscripción.
* Un alumno no recibe mensajes de correo electrónico de recordatorio de sesión como se esperaba.
* Un curso no se inicia del modo esperado si falta un determinado módulo.

**Anuncios**

* Si un anuncio contiene la etiqueta <a>, el anuncio no se crea del modo esperado.

**Cuenta**

* En algunos casos, las cuentas se desactivan aunque una cuenta tenga una orden de compra válida.

**API**

* Si hace clic en Administrar conexiones desde la tarjeta Adobe Connect, se le redirigirá a la página Conexión FTP.
* En algunos casos, el administrador de Connect recibe alertas incorrectas.
* La migración de aprendizaje de linkedIn produce algunos errores.

### Problemas conocidos de esta actualización {#known-issues-2}

**Informes de tableros**

* Cuando se elimina un programa de aprendizaje de certificación, en el informe de cursos de formación activos, se muestran los cursos presentes en el programa de aprendizaje o la certificación, aunque estos no tengan ninguna inscripción.

+++

+++Actualización 54: aplicación móvil

## Actualización 54: aplicación móvil

Fecha de publicación: 16 de abril de 2020

Para obtener las últimas funciones, actualizaciones y una mejor experiencia, le recomendamos que actualice la aplicación del dispositivo a la versión más reciente. La actualización es **obligatorio**.

### Funciones nuevas y mejoradas {#newandenhancedfeatures}

Un administrador puede comunicar información importante a todos los usuarios de la aplicación. Los anuncios pueden ser de tipo vídeo o imagen o un simple mensaje de texto. Con esta versión de la aplicación del dispositivo, ahora se admiten anuncios en la aplicación del dispositivo. Aparecerá un nuevo anuncio en cuanto se inicie la aplicación, para que los alumnos no se pierdan ninguna comunicación importante enviada por los administradores. Los alumnos pueden leerlo al instante o más tarde visitando la **Anuncios** .

Cuando hay uno o varios anuncios, puede verlos en el **Anuncios** sección.

Para ver un anuncio, toque **Anuncios**. El anuncio más reciente aparece en la pantalla.

Para ver el anuncio siguiente, toque **Deslizar hacia la izquierda para el siguiente**.

### Anuncios {#announcements}

![](assets/read-later.png)

Si no desea leer el anuncio en ese momento, siempre puede optar por leerlo más tarde. Toque **Leer más tarde** en el anuncio y el anuncio vuelve al estado no leído.

### Errores corregidos en esta actualización {#bugsfixedinthisupdate}

* En iOS, un podcast deja de reproducirse cuando la pantalla está bloqueada. El problema se ha solucionado y el audio se reproducirá incluso cuando la pantalla esté bloqueada.
* Si realiza un curso en la aplicación del dispositivo, la diapositiva de resultados a veces puede aparecer en blanco. Este problema se ha solucionado en esta actualización.

+++

+++Actualización 53: versión de abril de 2020 de Learning Manager

Fecha de publicación: 4 de abril de 2020

La versión de abril de 2020 de Learning Manager se centró en lo siguiente:

* [Mejoras de rendimiento](../whats-new.md#performance)
* [Formación en aula](../whats-new.md#classroom)
* [Flujos de trabajo de responsable](../whats-new.md#manager)
* [Aprendizaje social](../whats-new.md#social)
* [Informes](../whats-new.md#reporting)
* [Experiencia del alumno](../whats-new.md#learner)
* [Cambios en el nivel de API](../whats-new.md#api)

Para obtener más información, consulte [***Novedades de la versión de abril de 2020 de Learning Manager***](../whats-new.md).

+++

+++Actualización 52: aplicación móvil

## Actualización 52: aplicación móvil

Fecha de publicación: 20 de diciembre de 2019

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-1}

#### Logotipo de marca de empresa {#companybrandinglogo}

La aplicación ahora tiene la capacidad de mostrar el nombre de la marca, el logotipo de la marca o ambos dentro de la aplicación del dispositivo, en función de la configuración establecida por el administrador.

#### Vínculos profundos {#deeplinks}

Learning Manager ahora inicia la aplicación del dispositivo en cuanto hace clic en un vínculo o URL compatible con Learning Manager. En caso de que la aplicación no esté instalada en el dispositivo, la URL se abre en el navegador.

A continuación, se muestran algunos casos de uso que se admitirán en esta actualización.

* Haga clic en una URL de formación recibida en un correo electrónico.
* URL de formación predeterminadas que aparecen en las plantillas de correo electrónico.
* URL de cuenta que aparece en las plantillas de correo electrónico.
* Go-URL de Mi aprendizaje y Catálogo.

Además, cualquier URL con dominio *learningmanager.adobe.com* se abre en la aplicación del dispositivo.

#### Cargar activos en un certificado externo como prueba de finalización {#uploadassetsinexternalcertificateasproofofcompletion}

En esta actualización, un alumno puede cargar activos como prueba de finalización de un certificado externo.

Un alumno puede abrir un certificado externo y cargar activos, como archivos PDF, de texto o de imagen.

Para obtener más información, consulte  [***Cargar activos en un certificado externo***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Problemas resueltos en esta versión {#issuesfixedinthisrelease}

* Un usuario no puede iniciar sesión en la aplicación del dispositivo si el correo electrónico contiene caracteres especiales.
* Al desplazarse, el icono del objeto de aprendizaje parpadea cuando está en una vista de lista.
* Ahora puede ver todas las notificaciones de inserción sin tocar el botón de flecha abajo y ver los mensajes de uno en uno.
* Al hacer clic en una notificación de una publicación que se ha aceptado o rechazado en la revisión, se abre una página en blanco en la aplicación. En esta actualización, se abre la página del tablero.

+++

+++Actualización 51

En esta actualización, también puede cambiar la imagen del banner de un objeto de aprendizaje.

También puede personalizar el banner en una página de Aprendizaje social.

## Actualización 51

Fecha de publicación: 17 de diciembre de 2019

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-2}

### Planes de aprendizaje definidos por funciones configurables {#learningplansscopedbyconfigurableroles}

Puede crear funciones personalizadas para planes de aprendizaje que permitan el ámbito de usuarios y objetos de aprendizaje. En otras palabras, los planes de aprendizaje se pueden crear con un ámbito limitado derivado del ámbito de la función de un administrador personalizado.

Ahora, un administrador puede definir o restringir el ámbito mientras otorga acceso a la administración del plan de aprendizaje.

Para obtener más información, consulte [***Planes de aprendizaje definidos por funciones configurables***](../administrators/feature-summary/custom-role.md#scopeconfigure).

### Restringir campos activos en informes {#restrictactivefieldsinreports}

Para Campos activos, hemos agregado dos nuevas opciones: **Comunicado** y **Exportable**.

Para los campos CSV y los campos añadidos manualmente, si un campo activo se marca como **Comunicado**, el campo activo se puede buscar en un filtro dentro de un informe de tablero.

Para obtener más información, consulte  [***Restringir campos activos en informes***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***.***

### Ver la descripción del módulo de contenido {#viewdescriptionofcontentmodule}

Como autor, puede ver la descripción de los módulos al añadir el módulo a un curso.

Al crear un módulo, agregue su descripción. Para obtener más información sobre la creación de un curso, consulte [***Crear un curso***](../authors/feature-summary/courses.md).

### Mostrar nombres de cursos y sesiones {#displaycourseandsessionnames}

Como instructor, puede ver los nombres de los cursos y las sesiones en la vista Asistencia. Puede realizar un seguimiento de las sesiones que se modifican.

### Anuncio para alumnos {#announcementforlearners}

Los alumnos ahora pueden ver un anuncio en vista completa en lugar de en vista de lista. Esto sucede cuando el alumno tiene un anuncio sin leer. Esto mejora la experiencia de visualización del anuncio de los alumnos.

Adobe Learning Manager ahora le permite personalizar su cuenta para proporcionar una experiencia mejorada a sus usuarios. A continuación se muestra una lista de elementos que se pueden personalizar. Contacto [Asistencia de Learning Manager](mailto:learningmanagersupport@adobe.com)para realizar estos cambios.

* Colores de la tarjeta de aprendizaje
* Icono de progreso
* Imagen del puntero del ratón
* Fuente

Para obtener más información, consulte [***Personalizar la cuenta***](../administrators/feature-summary/themes.md#customize).

### Cargar imágenes de banner {#uploadbannerimages}

En esta actualización, también puede cambiar la imagen del banner de un objeto de aprendizaje.

También puede personalizar el banner en una página de Aprendizaje social.

### Compatibilidad con API {#apisupport}

Esta actualización de Learning Manager incluye API para las siguientes operaciones:

**Descargar insignia de PDF**

Esta actualización incluye API de alumno para permitir la descarga del PDF de una insignia.

**Descargar transcripciones de alumnos**

Esta actualización incluye API de alumno para permitir la descarga de transcripciones de alumnos.

**Descargar informe de prueba**

Esta actualización incluye API de administración para permitir la descarga de informes de prueba.

**Interacción paginada**

La API del alumno ahora permite obtener todos los alumnos y puntos de interacción dentro del ámbito del alumno. Esto ayuda a crear una tabla de posiciones de interacción.

**API:** `GET /users`

**Solicitar:** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Respuesta:** *La respuesta incluirá a los usuarios ordenados por puntos de interacción.*

**No molestar**

Actualmente, solo los administradores pueden añadir usuarios a una lista de No molestar a través de la interfaz de usuario. Después de esta versión, un alumno podrá establecer estos permisos para sí mismo a través de la API, siempre que el administrador haya activado esta API. La activación de esta API para una cuenta requiere una configuración de back-end. Esta API permite al alumno editar los permisos siguientes relacionados con los correos electrónicos.

* Dirigir correos electrónicos a alumno
* Correos electrónicos de escalación a responsables de alumnos
* Sobre subordinados directos
* Sobre subordinados de omisión de nivel

Para obtener más información sobre las API de Learning Manager, consulte lo siguiente:

* [***Referencia de API***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***Guía para desarrolladores de API***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Problemas resueltos en esta versión {#Issuesfixedinthisrelease-1}

* Solo los usuarios que pertenecen a un grupo de usuarios específico deben recibir anuncios destinados a ellos. Otros usuarios no deben recibir los anuncios.
* El reproductor muestra una rueda de carga antes de que se muestre el contenido.
* Los metadatos del usuario en los informes provocan una excepción de puntero nulo.
* Al añadir un instructor para una instancia predeterminada de un curso de Connect VC, aparece el mensaje: *&quot;No hay ninguna sesión para este módulo&quot;*, se muestra en la página Instancia del curso de la aplicación de administración.

* Al exportar una transcripción de alumno, se produce un comportamiento inesperado durante una transferencia por FTP.
* El nombre de un autor se muestra incorrectamente en los cursos de un programa de aprendizaje.
* Los cambios en la terminología del producto de las ayudas de trabajo no se reflejan del modo esperado.
* El nombre de un módulo se trunca si es largo y se ve en modo vertical en un dispositivo móvil.
* No se puede crear una instancia para un curso de Connect anterior después de actualizar la instancia predeterminada con la implementación de Connect anterior.
* Un instructor recibe una invitación de calendario incluso antes de que se publique el curso.

+++

+++Actualización 50

## Actualización 50

Fecha de publicación: 24 de octubre de 2019

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-3}

#### Crear función personalizada con varios ámbitos del catálogo {#createcustomrolewithmultiplecatalogscopes}

Como administrador, puede restringir una función personalizada en función de catálogos y grupos de usuarios. Todos los usuarios que pertenezcan a estas funciones solo podrán ver los objetos de aprendizaje del catálogo que pertenezcan a su ámbito. Estos usuarios solo pueden realizar acciones que se hayan definido en el ámbito de sus grupos de usuarios.

Hasta ahora, en Learning Manager, el ámbito de una función personalizada podía abarcar varios catálogos para un solo grupo de usuarios con permisos completos.

En esta actualización de Learning Manager, puede crear una función personalizada con un ámbito que abarque varios catálogos, y que cada catálogo tenga asignado su propio conjunto de permisos. Para obtener más información, consulte [***Ámbito de funciones personalizadas en varios catálogos***](../administrators/feature-summary/custom-role.md#multi-scope).

### Mejoras en la búsqueda {#enhancementstosearch}

**Plan de aprendizaje**

En la página Planes de aprendizaje de administradores y autores, se ha incorporado una barra de búsqueda que permite buscar cualquier plan de aprendizaje.

![](assets/search-for-as-learningplan.png)

**Aplicaciones de administrador y autor**

En esta actualización de Learning Manager, como administrador o autor, además de ejecutar una búsqueda de escritura anticipada, puede ejecutar una búsqueda libre para buscar cualquier objeto de aprendizaje.

### Se mantiene el filtro de búsqueda {#searchfilterispreserved}

Solo se aplica a un perfil de alumno.

En la **Catálogo** y **Mi aprendizaje** , un alumno puede aplicar un filtro en el panel izquierdo, por ejemplo, **Cursos** o **Programas de aprendizaje** y, a continuación, hace clic en un elemento de curso o de catálogo.

![](assets/choose-learning-objects.png)

Cuando el alumno vuelva a la **Catálogo** o **Mi aprendizaje** páginas con el botón atrás del navegador, el filtro se mantiene. El filtro que había aplicado un alumno con anterioridad ya no se restablece.

### Controlar la visibilidad de los filtros de búsqueda {#controlvisibilityofsearchfilters}

En versiones anteriores de Learning Manager, los administradores no tenían control sobre las opciones de visibilidad de un filtro de catálogo, por lo que los alumnos no veían las aptitudes ni las etiquetas. En esta versión de Learning Manager, el administrador puede filtrar los tipos, las aptitudes y las etiquetas de un catálogo.

En la **Configuración** para la categoría Mostrar paneles de filtro, al hacer clic en **[!UICONTROL Editar]**, puede ver las siguientes opciones. Las opciones determinan los paneles de filtro que están visibles para los alumnos, de modo que los alumnos puedan ajustar los resultados de búsqueda.

Para obtener más información, consulte [***Mostrar paneles de filtro***](../administrators/feature-summary/settings.md#filter-panels).

### Descargar código QR de la aplicación del administrador {#downloadqrcodefromadministratorapp}

En actualizaciones anteriores de Learning Manager, un administrador personalizado tenía problemas al descargar un código QR. En esta actualización, un administrador personalizado con acceso a **Todos los alumnos** y permiso para **Inscripción de cursos** Puede descargar el código QR.

El código QR sigue sin estar disponible para los usuarios con funciones personalizadas en el caso de que tengan permisos para un ámbito limitado de usuarios.

### Añadir comentarios al inscribir alumnos {#addcommentswhileenrollinglearners}

Como administrador o responsable, puede añadir comentarios al inscribir alumnos en un curso. Puede mencionar información adicional sobre la cohorte de usuarios que se inscriben. Estos datos se exportan en los informes del curso.

Para obtener más información, consulte [***Añadir comentarios al inscribir alumnos***](../administrators/feature-summary/courses.md#enroll-comments).

### Compatibilidad con la sala de reuniones permanente de Adobe Connect {#supportforadobeconnectpersistentmeetingroom}

En Adobe Connect, los clientes utilizan salas de reuniones que ya han creado en Connect. Todas las salas de reuniones de Connect son permanentes y las plantillas de sala de reuniones se configuran cuidadosamente para proporcionar una experiencia unificada para cada sala de reuniones permanente.

En esta versión de Learning Manager, la integración con Adobe Connect se ha mejorado para admitir también el espacio de trabajo persistente. Esto significa que ahora puede crear una sesión de clase virtual utilizando una de las salas ya creadas en Adobe Connect.

Learning Manager ahora también permite a los alumnos entrar en la sala de conexión para su sesión virtual mediante la autenticación SSO.

Para obtener más información, consulte [***Compatibilidad con salas de reuniones permanentes en Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent).

### Advertencia antes de marcar la asistencia si la duración de la sesión es cero {#warningbeforemarkingattendanceifthesessiondurationiszero}

Un autor o un administrador pueden crear una sesión con una duración de 0. Es posible cuando:

* la fecha de inicio y/o la fecha de finalización están vacías.
* la hora de inicio y/o la hora de finalización están vacías.

En esta actualización, un **mensaje de advertencia, que indica que la duración de una sesión es cero**, se muestra al administrador, responsable o instructor.

### Advertencia si se crea un módulo de clase sin agregar datos de sesión {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Si un autor crea un curso añadiendo una clase o un módulo de clase virtual, el autor puede optar por:

* No añadir una fecha de inicio/finalización ni una hora de inicio/finalización.
* Añada una fecha, pero no una hora de inicio/finalización.
* Añada una fecha y una hora de inicio.

En todos los casos anteriores, cuando un administrador, un responsable o un instructor marcan la asistencia o la finalización, los valores de la fecha de inicio y de finalización de la sesión son iguales, lo que significa que, en una transcripción de alumno, el valor Tiempo de aprendizaje empleado se muestra como cero.

En esta actualización, un **mensaje de advertencia, que indica que los datos de la sesión están incompletos**, se muestra al autor.

### Problemas resueltos en esta versión {#Issuesfixedinthisrelease-2}

**Aplicación del alumno**

* Un alumno no puede ver un curso de un programa de aprendizaje si el curso lo ha creado un autor externo.
* Si un administrador añade una publicación a un tablero externo, la solicitud de revisión se dirige a un experto en la materia interno al que se ha asignado esa aptitud.
* Un alumno no puede ver el botón Iniciar o Continuar después de inscribirse en cursos de LinkedIn.

**Correo electrónico**

* Cuando había un gran número de usuarios en una lista No molestar con el correo electrónico, el **Configuración** página se cargaría muy lentamente. En esta actualización, la paginación se añade a una lista de No molestar con el correo electrónico.
* Un instructor recibe actualizaciones/correos electrónicos para las sesiones de las que no forma parte. En esta actualización, se ha solucionado.

**Aptitudes**

* En una transcripción de alumno, el tipo de valor de una aptitud se muestra incorrectamente como texto.

**Aplicación móvil**

* En la aplicación móvil, un alumno podía ver e inscribirse en una instancia de plan de aprendizaje, lo que no era el comportamiento previsto. En esta actualización, se ha solucionado.

**Funciones personalizadas**

* Como administrador personalizado, no puede buscar un responsable en un informe del tablero.

**Varios intentos**

* En algunos casos, algunos módulos de curso no se muestran a los alumnos.

**Inscripción externa**

* No es posible cambiar el perfil externo de un usuario si se han rellenado puestos para perfiles principales.

### Problemas conocidos de esta versión {#knownissuesinthisrelease}

* En los navegadores que se indican a continuación, al pasar el ratón sobre el panel izquierdo, el texto aparece tras un ligero retraso.

   * Edge 42.17134.1.0
   * Edge 44.17763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Un alumno puede entrar en una sala de reuniones de Connect antes y después de la sesión.

+++

+++Actualización 49

## Actualización 49

Fecha de publicación: 26 de agosto de 2019

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-4}

**Mejoras de rendimiento**

* La importación de usuarios en el sistema es más rápida en comparación con las versiones anteriores. Hay una mejora significativa al importar grandes datos de usuario.
* En el caso de los responsables y los administradores, las opciones de la lista desplegable Configuración del informe se han modificado para cargar los datos a petición.
* Se ha mejorado el rendimiento de la API. Muchas API ahora deben tener un tiempo de respuesta mejorado.
* El tiempo necesario para generar transcripciones de alumnos se ha mejorado.
* No hay retrasos en las páginas en las que se enumeran los alumnos internos y externos, especialmente cuando hay un gran número de usuarios.

**Privilegios de usuarios especiales**

Un administrador puede otorgar privilegios especiales a un grupo de usuarios, mediante los cuales los miembros del grupo pueden participar en todos los tableros. El grupo de usuarios especiales omite cualquier restricción establecida en la sección Configuración del ámbito. Para obtener más información, consulte [***Privilegios de usuarios especiales***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege).

**Cambios en la interfaz de usuario**

* En la **Agregar informe** diálogo, el **Intervalo de tiempo** y **Filtros** los selectores aparecen como secciones independientes, que de forma predeterminada están contraídas. Para obtener más información, consulte [***Crear informes***](../administrators/feature-summary/reports.md#report).

* En la **Agregar informe** , para un grupo de usuarios, puede utilizar la búsqueda de escritura anticipada para elegir uno o varios grupos de usuarios. Para obtener más información, consulte [***Informes de grupos de usuarios***](../administrators/feature-summary/reports.md#user-group-reporting).

**Cambios en los valores de las columnas de tiempo**

En las transcripciones de alumnos, en las columnas de tiempo, los minutos se redondean al minuto más próximo y el valor del segundo es 00. Para obtener más información, consulte [***Columnas de tiempo***](../administrators/feature-summary/learner-transcripts.md#datetime).

### Problemas resueltos en esta versión {#Issuesfixedinthisrelease-3}

**Panel del alumno**

* Un calendario de aprendizaje mostraba el estado **Sesión inscrita** incluso cuando un responsable aún no aprobaba la inscripción. Ahora el estado correcto **Pendiente** se muestra al alumno hasta que el responsable aprueba la inscripción.

* En un caso concreto, para una sesión, el calendario de aprendizaje mostraba el estado **Inscrito** aunque el alumno haya completado un curso.

**Tablero de responsable**

* Los responsables no podían realizar el seguimiento de los cursos de cumplimiento de su equipo si los miembros del equipo se inscribían mediante planes de aprendizaje.

**Buscar**

* En la vista de instructor no se podía buscar un alumno.

**Interfaz de usuario**

* En el caso de una cuenta a la que se han aplicado cambios de taxonomía, los cambios no se reflejaron del modo esperado en las notificaciones.

### Problemas conocidos de esta versión {#Knownissuesinthisrelease-1}

* Con la barra de búsqueda, no puede buscar usuarios eliminados en la lista Usuarios externos . Como solución alternativa, desplácese hacia abajo para ver la lista de todos los usuarios y localice manualmente al usuario requerido.
* Si un usuario especial publica en un tablero externo, la solicitud de revisión la reciben los expertos en la materia en su ámbito.

+++

+++Actualización 48

## Actualización 48

Fecha de publicación: 2 de agosto de 2019

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-5}

**Separación del alcance en Aprendizaje social para usuarios internos y externos** Un administrador puede definir ámbitos separados para alumnos internos y externos. Hay dos nuevas secciones para usuarios internos y externos. En ambas secciones, puede definir los ámbitos de los grupos de alumnos. Para los usuarios internos, puede definir los valores de la característica de usuario. Para usuarios externos, puede definir el perfil externo, dentro del cual los alumnos pueden compartir el mismo espacio social. Para obtener más información, consulte [***Configuración del ámbito***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Creación de tableros sociales con restricción social** Para restringir la creación de tableros de todos los alumnos y moderarlos de forma eficaz, un administrador puede conceder permisos para crear tableros a un grupo seleccionado de usuarios. El administrador puede restringir la creación de un tablero solo a un grupo seleccionado y no a todos los alumnos que participan en el aprendizaje social. Para obtener más información, consulte [***Permisos de creación de tableros***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Mostrar solo los campos activos vacíos a los alumnos** Un administrador puede elegir mostrar los campos activos u ocultar los campos después de que se hayan rellenado los valores. Para obtener más información, consulte [***Visualización de usuario***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Los usuarios internos se eliminan cuando transcurre un intervalo de inactividad especificado** Un administrador puede definir la duración (en días) dentro de la cual se elimina un alumno interno si este permanece inactivo durante el tiempo especificado. Para obtener más información, consulte ***[Eliminar usuarios automáticamente](../administrators/feature-summary/settings.md#autodelete)***.  **Personalizar vínculos en el pie de página** Un administrador puede agregar y personalizar vínculos en el pie de página. Los vínculos también se pueden personalizar para varias configuraciones regionales. El método existente para agregar el vínculo Contactar con el administrador en el pie de página también está disponible en la **Vínculos de pie de página** sección. Para obtener más información, consulte [***Personalizar vínculos de pie de página***](../administrators/feature-summary/settings.md#footer).

### Problemas conocidos de esta versión {#Knownissuesinthisrelease-2}

* Los vínculos de pie de página personalizado no aparecen para las funciones de administrador de integración.

+++

+++Actualización 47: aplicación móvil

## Actualización 47: aplicación móvil

Fecha de publicación: 24 de julio de 2019

Usuarios de Android:

Esta actualización también admite los cambios necesarios para cumplir con las recomendaciones revisadas de Google para implementar notificaciones automáticas. Por lo tanto, ya no recibirá **notifications** si utiliza la versión 2.7.4 o una anterior.

Para recibir notificaciones, recomendamos actualizar a la versión 2.8.

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-6}

**Aprendizaje social**

Comparta su experiencia con sus compañeros en forma de contenido generado por el usuario publicado en paneles de discusión basados en temas. Otros alumnos interesados en habilidades similares pueden seguir estos tableros para aprender e incluso contribuir al tema, algo parecido a una plataforma de redes sociales.

Comparte ideas e información significativa en un entorno informal. Indicar si una publicación le gusta, cargar contenido y comentar en ellas. Para obtener más información, consulte [***Aprendizaje social en la aplicación móvil***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Compartir medios en un tablero**

Comparte imágenes, documentos o archivos de audio o vídeos con cualquier tablero para que otros miembros del tablero puedan ver tu publicación e iniciar una interacción.  Para obtener más información, consulte [***Compartir publicación***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Enviar archivo para los módulos Clase y Actividad**

Envíe los archivos como prueba de finalización del curso al instructor. El instructor puede aprobar o rechazar el envío en función del contenido del archivo. Para obtener más información, consulte [***Enviar archivo para su aprobación***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile).

**Compatibilidad actualizada de la plataforma**

La aplicación móvil de Learning Manager ahora es compatible con dispositivos con Android 7 y versiones superiores, y con iOS 10 y versiones superiores. Para obtener más información, consulte [***Requisitos del sistema***](../system-requirements.md).

### Problemas conocidos de esta versión {#Knownissuesinthisrelease-3}

1. En Android, no se puede cargar un archivo de GIF en una publicación, un comentario o al responder a un comentario.
1. Como moderador de cualquier tablero, no puede eliminar una publicación, comentario o respuesta de un usuario. Sin embargo, puede realizar lo mismo desde la aplicación web.
1. En la aplicación, no puede marcar un tipo de pregunta.
1. Después de activar Aprendizaje social en la aplicación, vuelva a iniciar la aplicación para ver la pestaña **Aprendizaje social**. Si no ve Aprendizaje social, cierre la aplicación y reiníciela. La ficha Aprendizaje social sería visible.

+++

+++Actualización 46

### Funciones nuevas y mejoradas {#Newandenhancedfeatures-7}

## Actualización 46

Fecha de publicación: 20 de junio de 2019

**Revisión automática de contenido**

El aprendizaje social permite seleccionar el contenido publicado por los alumnos de dos formas: **Sin gestión** y **Conservación manual**. En esta versión, Adobe Learning Manager mejora el aprendizaje social al proporcionar funciones de corrección automática habilitadas para la IA. Una vez publicado el contenido, este se analiza para identificar si pertenece a la aptitud para la que se ha publicado. Según la puntuación de confianza, el contenido se publica en directo o se envía para su revisión manual. Para obtener más información, consulte *[** Revisión con asistencia automática **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Asignar aptitud con dominios de aptitudes**

Asigne las aptitudes de su cuenta a los dominios de aptitudes presentes en el LMS de Learning Manager. Esto ayuda a vincular las aptitudes de su cuenta con los dominios de aptitudes que admite Learning Manager para la revisión asistida automáticamente. Para obtener más información, consulte [***Asignar aptitud con dominios***](../administrators/feature-summary/curation-skills.md).

**Especificaciones de CSV y ejemplos de CSV**

Especificaciones de CSV actualizadas que puede utilizar para asignar los datos de migración de LMS existentes. Utilice las especificaciones csv y los archivos zip csv de muestra más recientes para comprender el formato de datos que se debe introducir. Para obtener más información, consulte  [***Manual de migración***.](../integration-admin/feature-summary/migration-manual.md)

### Problemas resueltos en esta versión {#Issuesfixedinthisrelease-4}

**API de Learning Manager**

* Cuando se añade un perfil externo mediante el método POST de la API *externalProfile*, no se muestra el correo de bienvenida.

**Tablero de responsable**

* Cuando un responsable seleccionó la opción **Este trimestre**, no se mostraron los detalles de inscripción, progresión y finalización de un objeto de aprendizaje. En esta versión, estos detalles ahora se muestran del modo esperado.

**Estudiantes en lista de espera**

* En versiones anteriores de Learning Manager, cuando un responsable inscribía alumnos y un instructor deseaba comprobar si había alumnos en lista de espera, se mostraba un mensaje de error. En esta versión, un instructor puede examinar la lista de alumnos en lista de espera sin encontrar ningún mensaje de error.

**Introducción a la certificación**

* Después de que un autor creara un curso y una certificación con una descripción y contenido de información general, cuando un alumno accedía a la página del curso, el contenido de la información general no se mostraba del modo esperado. Sin embargo, el contenido estaba visible en las páginas de vista previa de los alumnos en las aplicaciones de administrador y autor. En esta versión, el contenido de la descripción general se muestra del modo esperado en la aplicación del alumno.

**Catálogo**

* Para cada catálogo, un alumno puede ver todos los objetos de aprendizaje. En versiones anteriores, si algún catálogo no contenía un objeto de aprendizaje, el catálogo seguía apareciendo al principio de otros catálogos. En esta versión, todos los catálogos que no tienen objetos de aprendizaje aparecen en la parte inferior de los catálogos.

+++

+++Actualización 45

Fecha de publicación: 30 de mayo de 2019

**Funciones nuevas y mejoradas**

* Se ha consolidado la búsqueda de alumnos inscritos en la sección de alumnos del objeto de aprendizaje en todas las instancias. Busque usuarios inscritos en la sección Alumno del objeto de aprendizaje mediante la búsqueda de escritura anticipada. Para obtener más información, consulte [***Buscar usuarios inscritos***](../administrators/feature-summary/courses.md#searchforusers).
* Capacidades de edición completas de objetos de aprendizaje adquiridos mediante el catálogo compartido. Para obtener más información, consulte [***Control de catálogo compartido***](../administrators/feature-summary/shared-catalog-full-control.md). Para activar la función, póngase en contacto con el servicio de asistencia de Learning Manager.
* Ahora, los instructores pueden identificar fácilmente las sesiones y los módulos con revisiones pendientes. Para obtener más información, consulte [***Revisiones pendientes***](../instructors/feature-summary/learners.md#pending).

* Las aptitudes ahora admiten la concesión de valores de crédito en formato decimal. Esto permite a los autores asignar un valor de crédito de nivel decimal a un determinado curso. Para obtener más información, consulte [***Compatibilidad con decimales***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatiza la creación de funciones personalizadas. Para obtener más información, consulte [***Configurar funciones mediante archivos csv***](../integration-admin/feature-summary/configure-role-csv-files.md).
* Los envíos necesarios para las certificaciones externas y los módulos de actividad ahora son opcionales. Esto permite a los responsables y a los instructores realizar evaluaciones sin envío. Para obtener más información, consulte [***Presentación facultativa***](../managers/feature-summary/learning-objects.md#optional).
* Descargar transcripciones de alumnos de usuarios eliminados. Para obtener más información, consulte [***Transcripciones de alumnos***](../administrators/feature-summary/learner-transcripts.md).
* Compatibilidad con los siguientes idiomas:

   * Coreano
   * Turco
   * Neerlandés
   * Polaco

**Problemas conocidos**

* La compatibilidad de decimales en los créditos de aptitudes solo se admite para el inglés.
* Para los idiomas coreano, japonés y ruso, el valor del meridiano de tiempo de sesión no se muestra del modo esperado.

**Problemas resueltos en esta versión**

* Las puntuaciones de las pruebas no se guardan para un programa de aprendizaje o una certificación en las pestañas Asistencia y Puntuación.
* Un administrador o un responsable no pueden marcar como completa una certificación externa.
* En el cuadro de diálogo Transcripciones de alumnos, un administrador no puede seleccionar un intervalo de fechas personalizado si el idioma es portugués o español.
* Un administrador no puede crear un perfil externo si el idioma del perfil es el francés.
* Los campos activos no están visibles en el cuadro de diálogo Editar usuario si la configuración regional está en cualquier otro idioma que no sea inglés.

+++

+++Actualización 44: aplicación móvil

Fecha de publicación: 26 de abril de 2019

* **Cambios en la interfaz de usuario:** En la aplicación, el  ![](assets/hamburger.jpg) y el  ![](assets/search-magnifying-glass-icon.png) ahora aparecen en la parte superior.

![](assets/1.png)

* **Escanea el código QR para inscribirte:** Se han mejorado las capacidades del código QR. Además de admitir la marca de asistencia mediante código QR, ahora también es posible inscribirse en un curso y completarlo mediante código QR.

  Para inscribirse en un curso y completarlo, puede escanear el código QR que le haya proporcionado el administrador. Para obtener más información sobre el análisis de códigos QR en la versión web de Learning Manager, consulte  [***Escanear código QR***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompleteenrollcompleteacourse).

* **Varios intentos en el curso:** La aplicación Learning Manager permite al alumno realizar cursos con varios intentos activados. Para obtener más información sobre la configuración de varios intentos, consulte  [***Varios intentos***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#Multiintentos).

+++

+++Actualización 43

## Actualización 43

Fecha de publicación: 28 de enero de 2019

* El tiempo de aprendizaje empleado por un alumno en un módulo se puede contar varias veces al marcar la asistencia más de una vez. Este problema se ha solucionado.
* Al marcar la asistencia de un objeto de aprendizaje en una sesión de varios días, se puede mostrar una fecha de inicio de sesión incorrecta para un alumno en una transcripción de aprendizaje. Este problema se ha solucionado.
* Es posible que los usuarios no puedan ver un curso cuando este se añade a un programa de aprendizaje o certificación completado. Este problema se ha solucionado.
* La inscripción de usuarios puede ocurrir incorrectamente cuando se mueven fuera de un grupo de usuarios. Este problema se ha solucionado.
* Es posible que el alumno y el instructor no reciban un correo electrónico cuando se cambian los detalles de la sesión en la aplicación del instructor. Este problema se ha solucionado.
* Es posible que la URL de Adobe Connect no funcione correctamente cuando se proporciona &quot;/&quot; al final de la URL. Este problema se ha solucionado.
* Puede aparecer un mensaje de error al seleccionar al menos un módulo obligatorio para un curso ya publicado. Este problema se ha solucionado.
* Cuando un alumno ha completado un curso y el autor lo marca como obligatorio, es posible que la finalización del curso no se marque como completada. Este problema se ha solucionado.
* El valor comprobado de un módulo seleccionado para un curso duplicado puede no aparecer al instante. Solo se muestra como un curso duplicado cuando se actualiza la página. Este problema se ha solucionado.
* Todos los módulos se mostrarán como no marcados en el modo de edición después de publicar un curso. Es necesario actualizar la página para ver los cambios. Este problema se ha solucionado.
* La selección de un módulo obligatorio puede haber estado disponible para un curso solicitado cuando no debería haberlo estado. Este problema se ha solucionado.
* Un módulo obligatorio sigue apareciendo en la casilla de verificación desplegable incluso después de quitarlo mientras se edita el curso. Este problema se ha solucionado.
* Los módulos de trabajo previo y Prueba podrían estar marcados como obligatorios de forma predeterminada. Este problema se ha solucionado.
* Al hacer clic en el vínculo de comentarios de L3 en su correo electrónico, es posible que el modo de comentarios no se abra. Este problema se ha solucionado.
* Falta la certificación en la lista desplegable de informes del tablero, aunque está visible en la aplicación del administrador y en la lista de API de datos. Este problema se ha solucionado.
* El administrador no pudo retirar algunos objetos de aprendizaje por falta de permisos, aunque los catálogos compartidos son independientes de las cuentas de Learning Manager. Este problema se ha solucionado.

+++

+++Actualización 42

Actualización 42

Fecha de publicación: 11 de enero de 2019.

* La inserción de notificaciones de usuarios puede fallar aleatoriamente, lo que provoca que los correos electrónicos asociados no se envíen. Este problema se ha solucionado.
* `If a Learner is enrolled in Learning Program 1 and a Course in Learning Program 2, when the Learning Transcript is downloaded for a user group or more than one individual, the Learning Transcript may have missing data. This issue is fixed.`

+++

+++Actualización 41

Actualización 41: Fecha de publicación: 1 de diciembre de 2018.

* Los administradores pueden controlar el permiso otorgado a los alumnos para ver las puntuaciones de las pruebas en las transcripciones de los alumnos. Esto se puede activar o desactivar desde la página Configuración .
* La inserción de notificaciones de usuarios puede fallar aleatoriamente, lo que provoca que los correos electrónicos asociados no se envíen. Este problema se ha solucionado.
* Es posible que los datos de tiempo dedicado al aprendizaje no aparezcan en los informes de transcripciones de alumnos y paneles. Este problema se ha solucionado.
* Es posible que la información sobre actividades como la inscripción o la finalización no esté presente en la transcripción del alumno descargada por un responsable. Esto se ha solucionado.
* Los módulos que forman parte de un curso que aún está en curso pueden aparecer como completados en la transcripción del alumno. Este problema se ha solucionado.
* Es posible que la transcripción del alumno no muestre los datos descargados según el intervalo de fechas seleccionado. Este problema se ha solucionado.
* Es posible que los catálogos no aparezcan para los usuarios que solo tengan asignada la función de autor. Este problema se ha solucionado.
* Cuando un administrador de funciones personalizadas descarga la transcripción del alumno, el informe descargado no tendrá información sobre los objetos de aprendizaje que solo formaban parte de los catálogos predeterminados. Este problema se ha solucionado.
* Puede producirse una discrepancia en el número total de usuarios y la lista de usuarios de la página Grupo de usuarios. Esto se ha solucionado.
* Es posible que la ventana emergente Programa de aprendizaje no aparezca aunque esté activada y que se redirija a los usuarios a la página del objeto de aprendizaje. Este problema se ha solucionado.
* Cuando se borra la lista de espera y los alumnos se inscriben en un curso, el administrador puede recibir una notificación por correo electrónico con su nombre en lugar de mencionar el nombre del alumno. Este problema se ha solucionado.
* Es posible que el apellido no aparezca en la interfaz de usuario de un usuario agregado mediante la API de usuario de POST. Este problema se ha solucionado.

+++

+++Actualización 40

Actualización 40

Fecha de publicación: septiembre de 2018.

Mejora del rendimiento

* Los usuarios pueden experimentar problemas de tiempo de espera al descargar grandes conjuntos de transcripciones de alumnos. Este problema se ha solucionado.
* Los usuarios pueden experimentar retrasos al descargar un gran conjunto de informes de inscripción en los que se registra la puntuación de la prueba del alumno. Este problema se ha solucionado.
* La descarga de un gran conjunto de informes de puntuación de prueba puede tardar más de lo habitual. Esto se ha solucionado.
* Cuando el alumno finaliza un programa de aprendizaje, es posible que el formulario de comentarios de L1 no aparezca automáticamente aunque el administrador haya activado la ventana emergente automática. Este problema se ha solucionado.
* En los informes descargados de seguimiento de auditoría de usuarios y seguimiento de auditoría de contenido, es posible que las columnas modificadas por nombre de usuario y modificadas por correo electrónico de usuario no estén registradas. El informe muestra el sistema en estos casos. Esto se ha actualizado para que se marque como Desconocido.

+++

+++Actualización 39

Fecha de publicación: 19 de mayo de 2018.

* Esta versión de Adobe Learning Manager incluye nuevas funciones y mejoras. Le permite crear funciones personalizadas, añadir etiquetas de catálogo, purgar usuarios, gestionar etiquetas, cambiar el nombre de los objetos de aprendizaje, integrar Slack, nuevas integraciones de conectores, compatibilidad con xAPI y mucho más. Para obtener más información sobre las nuevas funciones y mejoras, consulte  [Resumen de la nueva función](../whats-new.md#main-pars_text).

* Learning Manager cumple con el RGPD. Para obtener más información, consulte [Cumplimiento del RGPD por parte de Learning Manager](/help/migrated/kb/prime-gdpr.md).

## Problema conocido {#knownissue}

* El hipervínculo al número de cursos y certificaciones dentro del modo de etiquetas incluye cursos paralelos y certificaciones recurrentes. Al hacer clic en el hipervínculo, es posible que estos cursos y certificaciones no aparezcan en la lista, lo que provoca una discrepancia en los números.

+++

+++Actualización 38

* Los alumnos con el estado Pendiente o En espera de aceptación se marcaban como completados. Este problema se ha solucionado.
* Cuando un instructor busca y selecciona a todos los alumnos, el número de alumnos seleccionados y el recuento mostrado presentan disparidades. Este problema se ha solucionado.
* Al buscar y seleccionar cualquier alumno y marcar la asistencia, Learning Manager puede marcar la asistencia de todos los alumnos. Esto se ha solucionado.
* Learning Manager mostraría la hora en los mensajes de correo electrónico en formato de 24 horas. Esto se ha solucionado. Ahora la hora se muestra en formato de 12 horas.
* Cuando un responsable nominaba a un alumno para un curso mediante el botón nominar disponible en la página de notificaciones, el modo nominar no se cargaba. Esto se ha solucionado.
* En los informes de Excel exportados, la fecha límite, que debería ser la fecha de inscripción + días para completar el valor establecido en la instancia automática de los objetos de aprendizaje, se mostraba de forma incorrecta. Este problema se ha solucionado.

* Los resultados de la búsqueda de usuarios se muestran vacíos cuando no hay usuarios presentes en el grupo en el que se realiza la búsqueda. Esto se ha solucionado.
* Los responsables no se pueden eliminar aunque no haya informes directos. Este problema se ha solucionado. Ahora se pueden eliminar responsables.
* Es posible que la funcionalidad de progreso de Restablecer módulo deje de funcionar. Esto se ha solucionado.
* La certificación eliminada podría aparecer en el widget para los alumnos. Este problema se ha solucionado.
* Se ha resuelto el problema con el cálculo de la eficacia del curso.

* Se ha solucionado el problema de integración de la nueva cuenta de conexión.
* La ventana emergente automática Comentarios de L1 podría no aparecer si está activada en instancias no predeterminadas. Se ha solucionado el problema.
* Es posible que el instructor no pueda marcar la asistencia de todos los usuarios de una sola vez para las sesiones que forman parte del programa de aprendizaje/certificación. Esto se ha solucionado.

+++

+++Actualización 37

Fecha de publicación: 25 de marzo de 2018

La versión de marzo de 2018 de Adobe Learning Manager incluye increíbles nuevas funciones y mejoras. Le ofrece la generación de informes de seguimiento de auditoría de usuarios e informes de inicio de sesión/acceso, proporciona a los alumnos la capacidad de elegir instancias de cursos, mejoras en clases y clases virtuales, y mucho más. Esta versión también incluye correcciones de errores y mejoras de rendimiento.

Para leer todas las novedades de esta versión, consulte  [Novedades de Adobe Learning Manager](../whats-new.md).

### Problema conocido {#KnownIssue-1}

**Problema:** El acceso a algunos objetos de aprendizaje específicos mediante Internet Explorer v11.1478.10586.0 puede hacer que Learning Manager se bloquee.

**Solución alternativa:** Actualice el navegador Internet Explorer 11 a la versión más reciente poniéndose en contacto con el equipo de TI de su organización.

+++

+++Actualización 36

Fecha de publicación: 22 de enero de 2018.

### Problemas solucionados {#issuesfixed}

* Cualquier cambio en la configuración de la plantilla de correo electrónico puede provocar la desaparición del banner de correo electrónico. Este problema se ha solucionado.
* Es posible que los alumnos no puedan añadir o iniciar ayudas de trabajo privadas. Esto se ha solucionado.
* Es posible que los grupos de usuarios personalizados presentes en una cuenta no aparezcan en el campo grupo de usuarios en el modo de agregar o editar informe. Este problema se ha solucionado.
* Si el nombre de una imagen de insignia contiene espacio, es posible que el alumno no vea el contenido en la página de inicio.
* Cuando se elimina de un curso a un usuario inscrito, es posible que el informe del curso y el informe de prueba no se generen para ese curso en particular. Este problema se ha solucionado.
* Si el administrador cambia el número de puestos nominados para un responsable, es posible que el recuento aparezca incorrecto en la solicitud de nominación al abrirse desde diferentes lugares. Este problema se ha solucionado.
* Al convertir un usuario externo en un usuario interno, es posible que el usuario no se añada al grupo Todos los alumnos internos . Este problema se ha solucionado.
* Si busca un alumno individual, lo selecciona y realiza la acción de darse de baja, podría darse el caso de que se diera de baja a todos los alumnos de ese grupo en lugar de solo al seleccionado. Este problema se ha solucionado.
* Como administrador, es posible que no pueda utilizar la casilla de verificación para seleccionar un alumno en las certificaciones. Este problema se ha solucionado.
* La creación y actualización de grupos de usuarios con más de 600 usuarios individuales puede dar lugar a un error. Este problema se ha solucionado. Ahora puede crear grupos de usuarios con más de 600 usuarios individuales.
* Si elimina un grupo de usuarios personalizado que forma parte de otro grupo de usuarios personalizado, la regla de intersección puede pasar el número de usuario al grupo superior. Este problema se ha solucionado.
* Cuando el catálogo predeterminado está deshabilitado, se crea un nuevo catálogo y el responsable tiene acceso a este catálogo recién creado, es posible que no pueda buscar ningún curso en ese catálogo. Este problema se ha solucionado.
* Es posible que los usuarios de aplicaciones móviles no reciban los comentarios de L1 como notificaciones push. Esto se ha solucionado.

+++

+++Actualización 35

Fecha de publicación: 7 de enero de 2018.

Esta versión de Learning Manager ofrece optimizaciones de rendimiento destinadas a mejorar la escalabilidad, el rendimiento y la seguridad.

### Mejoras {#enhancements}

* Disfrute de búsquedas elásticas al buscar cursos y usuarios en todas las aplicaciones. Esto incluye la búsqueda de cursos, usuarios y grupos de usuarios.
* Soporte para el uso del conector de Box a fin de integrar Learning Manager con sistemas externos para automatizar la sincronización de datos. Para obtener más información, consulte [Conector de Box](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946).
* Especificaciones de CSV actualizadas que puede utilizar para asignar los datos de migración de LMS existentes. Utilice las especificaciones csv y los archivos zip csv de muestra más recientes para comprender el formato de datos que se debe introducir. Para obtener más información, consulte [Manual de migración.](../integration-admin/feature-summary/migration-manual.md)

+++

+++Actualización 34

### Problemas solucionados {#IssuesFixed-1}

* Los anuncios pueden fallar cuando el número de usuarios es alto. Este problema se ha solucionado.
* El acceso a la cuenta de Learning Manager mediante la URL del subdominio en la UE podría redirigir a los usuarios a otra página. Este problema se ha solucionado.
* Cuando se solicita un programa de aprendizaje, el alumno debe poder consumirlo solo en el orden especificado. Los alumnos podían realizar cursos que no aparecían en la lista en primer lugar mediante los hipervínculos del curso. Este problema se ha solucionado. Los alumnos ya no pueden iniciar un curso hasta que termine el curso anterior.

* Es posible que el mensaje de error de versión del navegador no compatible no aparezca en las versiones no compatibles de Internet Explorer (IE 7, IE 8, IE 9 e IE 10) y Safari (versión 7, 8 y 9). Este problema se ha solucionado.



+++

+++Actualización 3

Fecha de publicación: 5 de octubre de 2017.

### Problemas solucionados {#IssuesFixed-2}

* Es posible que los cambios realizados en un curso compartido no se propaguen a la cuenta compartida si el autor de la cuenta de origen guarda automáticamente el curso. Este problema se ha solucionado.
* En ocasiones, para proyectos específicos de Learning Manager, el contenido se bloqueaba en el reproductor Fluidic. Este problema se ha solucionado.

* La lista de calendarios en el widget Calendario de aprendizaje del tablero del alumno podría aparecer en un orden aleatorio. Este problema se ha solucionado. El anuncio aparecerá ahora de forma ordenada.
* Al marcar la asistencia con la opción seleccionar todo, los alumnos se marcan como asistidos en todos los objetos de aprendizaje de la misma sesión. Este problema se ha solucionado.
* En algunas pantallas de alta resolución, el correo electrónico recibido de Learning Manager presentaba problemas de alineación y truncamiento de la imagen y el texto del banner. Esto se ha solucionado.
* Algunos correos electrónicos de Learning Manager, como los correos electrónicos sin datos de notificación, no se activaban para los usuarios. Ejemplo: correo electrónico recibido al crear y habilitar el perfil externo y correo electrónico recibido al configurar la cuenta de conexión. Este problema se ha solucionado.
* Cuando se crea un programa de aprendizaje, se establece un recordatorio, se inscriben usuarios y, a continuación, se cambia la fecha límite de la instancia, es posible que la fecha límite modificada no se refleje en los recordatorios. Esto se ha solucionado. Los recordatorios ahora contendrán el plazo modificado.
* En determinados casos, para el contenido creado con Adobe Presenter, el tiempo total y el tiempo transcurrido en el reproductor Fluidic no estaban sincronizados con el contenido. Este problema se ha solucionado.
* En determinados casos, después de añadir un programa de aprendizaje a un catálogo, la opción para añadir aún podría estar activada. Este problema se ha solucionado.
* Al abrir Learning Manager en el navegador de un dispositivo, se muestra una opción para utilizar Learning Manager en la aplicación del dispositivo. Hacer clic en Sí debería iniciar Play Store (Android) si la aplicación no está instalada, o iniciar la aplicación si está instalada (en Android y iOS). Este flujo de trabajo tenía problemas y se han solucionado.

+++

+++Actualización 32

Fecha de publicación: 17 de agosto de 2017

### Problemas solucionados {#IssuesFixed-3}

**Curso con varias versiones de módulos que vuelven a la versión anterior al eliminarse.**

Cuando un curso tiene varias entradas de versión de módulo para módulos específicos, al eliminar el módulo, se revertiría a la versión anterior y no se eliminaría por completo. Este problema se ha solucionado.

**Los cambios en un curso compartido no se propagaban si se guardaban automáticamente al desplazarse por las fichas.**

Es posible que los cambios en un curso compartido no se propaguen a la cuenta de inquilino si el autor de la cuenta principal guarda automáticamente el curso al pasar a la siguiente pestaña. Este problema se ha solucionado.

**Los usuarios no podían cambiar el plazo de instancias de un curso que solo es de actividad.**

Los usuarios no podían cambiar la fecha límite de una instancia en los cursos de actividad, ya que se revertiría a la fecha límite anterior. Este problema se ha solucionado.

**Incapacidad para utilizar un ID exclusivo una vez eliminado de un objeto de aprendizaje.**

Cuando asigne un ID exclusivo a un curso y lo elimine, no podrá volver a utilizar el ID. Este problema se ha solucionado.

**Un programa de aprendizaje que ya se ha inscrito como parte de un evento de plan de aprendizaje podría volver a aparecer como parte de otro evento en la aplicación del alumno.**

Si un programa de aprendizaje ya se ha inscrito como parte de un evento de plan de aprendizaje, puede volver a aparecer como parte de otro evento en la aplicación del alumno. Este problema se ha solucionado.

**El alumno recibe correos electrónicos de recordatorio con la fecha límite o la hora de la sesión especificadas incorrectamente.**

Los alumnos suelen recibir correos electrónicos con recordatorios de fechas límite o de horas de sesión incorrectos debido a las correcciones de la zona horaria. Este problema se ha solucionado.

**La línea de tiempo de la tabla de posiciones de interacción muestra alumnos externos si se convierte de alumno externo a interno.**

La línea de tiempo de la tabla de posiciones de interacción de un alumno interno puede mostrar a un alumno externo cuando se convierte de externo a interno. Este problema se ha solucionado.

**El campo UUID de un alumno se muestra en formato editable al crear un único usuario y un usuario de CSV en una cuenta con UUID activado.**

El campo UUID se mostraba al alumno al completar su perfil aunque el administrador hubiera proporcionado el UUID para usuarios individuales y CSV. Este problema se ha solucionado.

**En determinados casos, el tiempo de aprendizaje empleado no se captura en los informes.**

Los datos del tiempo de aprendizaje empleado no se mostraban en los informes de un alumno.

* Si el sistema para los módulos de conexión marca automáticamente su asistencia.
* Cuando se analiza un código QR para módulos CR y VC mediante la aplicación de dispositivo de Learning Manager.

**Esta versión de Learning Manager también incluye mejoras y correcciones de errores relacionados con el reproductor de dispositivos.**

* Problemas relacionados con la finalización de los módulos de actividad. Esto se ha solucionado.
* Cuando el alumno reproduce un vídeo en modo vertical, es posible que los botones +10 y -10 no funcionen. Esto se ha solucionado
* Se ha mejorado la experiencia de reproducción de determinados proyectos de muestra al reproducirse en un dispositivo Android (móvil y tableta) que antes parpadeaban.
* Al añadir una nueva nota, el panel de notas debe cerrarse y la reproducción debe reanudarse en el reproductor. Esto podría no suceder en ciertos casos. Esto se ha solucionado.
* Al abrir las notas añadidas a un módulo, es posible que no se muestre el botón Cerrar. Este problema se ha solucionado.
* Cuando el alumno abre el panel Notas mediante el marcador Nota, puede que tenga que hacer clic dos veces en el icono Notas para cerrar el panel.
* Al hacer clic en la tabla de contenido, es posible que no se contraiga automáticamente y que necesite cierre manual para ver el contenido. Este problema se ha solucionado.
* Es posible que un curso que tiene un módulo con varios idiomas no muestre todos los idiomas disponibles, ya que la barra de desplazamiento podría no escalarse en consecuencia. Esto se ha solucionado.
* Al abrir un módulo de curso de actividad de terceros en un reproductor en modo horizontal, es posible que la orientación del texto no se ajuste, lo que dificulta el desplazamiento. Esto se ha solucionado.
* Se ha aumentado el área de toque para el botón de cierre del reproductor en el modo en línea y fuera de línea.
* El índice no se cierra automáticamente cuando se cambia la orientación del dispositivo. Esto se ha solucionado.
* Se han solucionado algunos problemas menores relacionados con la interfaz de usuario, como la alineación del botón de reproducción, el botón de opción y otros ajustes en el modo horizontal y vertical.

* Se ha solucionado el problema de que la barra de búsqueda se mostrara incluso cuando la opción de mostrar control de reproducción no estaba marcada en el contenido.
* El botón de cierre del reproductor no estaba visible para determinados proyectos cuando se cambia la orientación del dispositivo. Esto se ha solucionado.
* Se ha solucionado el problema por el que la sección del índice del módulo se truncaba en modo horizontal en el reproductor del dispositivo. En algunos casos, el índice no era visible para el contenido en el reproductor del dispositivo. Esto también se ha corregido.

**Esta versión de Learning Manager también incluye las mejoras y correcciones que se indican a continuación para la aplicación de dispositivos**.

* Es posible que las notificaciones push relacionadas con los plazos de finalización no se entreguen en ciertos dispositivos. Este problema se ha solucionado.
* Ahora también se admite el ciclo de vida de objetos de aprendizaje en aplicaciones de dispositivos. Los alumnos ahora pueden acceder al contenido más reciente de los objetos de aprendizaje si el autor los ha editado.

* Se han solucionado los problemas de orientación de la aplicación (incluido el modo vertical y la orientación predeterminada) de Learning Manager.
* Es posible que no haya una opción para actualizar el contenido cuando el usuario pasa del modo sin conexión al modo en línea.
* La ordenación de módulos ahora es compatible con cursos en aplicaciones de dispositivos en modo en línea.

* Si un usuario no ha descargado ninguna ayuda de trabajo, al hacer clic en la ficha Mis ayudas de trabajo en el modo sin conexión, la aplicación se podría bloquear en IOS y mostrar un mensaje que indica un error al cargar los datos en Android. Esto se ha solucionado.
* La aplicación Learning Manager se cierra o genera un error si se accede al curso inmediatamente después de apagar Internet, aunque se trate de un curso descargado. Este problema se ha solucionado ahora.
* En ocasiones, al escanear el código QR, se muestra una imagen capturada del escaneo anterior del código QR. Esto se ha corregido.
* Al intentar eliminar una ayuda de trabajo que ya se ha añadido de la ficha Ayudas de trabajo en determinadas ocasiones, aparece un mensaje de error. Este problema se ha solucionado.

+++

+++Actualización 31

Fecha de publicación: 16 de julio de 2017

### Mejoras {#Enhancements-1}

**Interacción**

Esta versión mejora el ámbito de la interacción. Los usuarios externos ahora pueden participar en la interacción. Como administrador, puede definir el ámbito de la interacción cambiando la configuración del ámbito. Puede habilitar la interacción de forma selectiva entre usuarios, grupos o ubicaciones de perfil similares.

**Mejoras de usuarios externos**

Con esta mejora, puede establecer un intervalo de tiempo tras el cual los usuarios se eliminan automáticamente después del período de inactividad. La mejora también permite al administrador volver a añadir un usuario como alumno externo tanto para alumnos eliminados automáticamente como para alumnos eliminados manualmente.

**Ayuda de trabajo, anuncios e informe de darse de baja**

Las ayudas de trabajo son contenido de formación al que puede acceder un alumno sin tener que inscribirse en ningún objeto de aprendizaje específico, como un curso o un programa de aprendizaje. Con esta mejora, los administradores pueden extraer y descargar el informe de ayudas de trabajo. Como administrador, también puede generar un informe de todos los anuncios que ha enviado. Los administradores y responsables también pueden extraer un informe de los alumnos que se han dado de baja.

**Conectores de Learning Manager**

Ahora puede exportar aptitudes de usuarios a una ubicación de FTP para integrarlas con cualquier sistema de terceros mediante la opción Exportación de datos. Puede especificar el nombre de conexión de la integración y elegir si desea importar usuarios internos o exportar aptitudes de usuario configurándolas o obteniéndolas a petición.

**Copiar instancias de curso**

Ahora puede copiar la URL de instancia haciendo clic en la flecha desplegable en la esquina superior derecha de una instancia.

### Problemas solucionados {#IssuesFixed-4}

**Los usuarios no reciben la invitación de calendario al inscribirse en el programa de aprendizaje**

A veces, los usuarios no recibían la invitación de archivo de invitación de calendario (.ics) al inscribirse en programas de aprendizaje, certificados con clases y sesiones de Connect. Este problema se ha solucionado. Los usuarios ahora obtendrán archivos .ics como archivos adjuntos que mencionan los detalles de la sesión junto con el correo electrónico de inscripción.

**La descripción de la actividad, aunque se proporcione en varios idiomas, seguirá apareciendo en inglés**

Un usuario cuya preferencia de idioma de contenido esté establecida en un idioma que no sea inglés podría ver la descripción del módulo de actividad en inglés. Este problema se ha solucionado.

+++

+++Actualización 30

Fecha de publicación: 30 de junio de 2017

### Mejoras {#Enhancements-2}

**Se admiten varios objetos de aprendizaje en el plan de aprendizaje**

Como administrador o autor, ahora puede asignar varios objetos de aprendizaje a un plan de aprendizaje. Si alguna de las instancias del objeto de aprendizaje se retira o caduca, todo el plan de aprendizaje se desactiva automáticamente. Con esta mejora, también puede buscar **[!UICONTROL Aprendizaje completado]** y **[!UICONTROL Asignar aprendizaje]** campos con ID exclusivos de objetos de aprendizaje.

**Accesibilidad**

Con esta actualización, la experiencia del alumno de Learning Manager ahora admite la sección 508, Estándar de accesibilidad. Learning Manager también es compatible con la última versión de **[!UICONTROL MANDÍBULAS]**. Esta función solo se admite en la aplicación del alumno. Utilice Internet Explorer 11, Windows Chrome o macOS Safari para acceder a esta función.

### Problemas solucionados {#IssuesFixed-5}

**Información incorrecta en determinadas zonas horarias**

Los recordatorios de plazos indicaban el número de días que faltaban incorrectamente para los alumnos en determinadas zonas horarias. Este problema se ha solucionado.

**Problemas del programa de aprendizaje en el caso de instancias de programa caducadas**

El inicio de módulos del programa de aprendizaje tenía problemas si la instancia del programa había caducado. Esto provocaba que la expansión del módulo no funcionara y que los alumnos no pudieran iniciar el reproductor y visitar el contenido. Este problema se ha solucionado.

**Problemas de traducción en la aplicación del alumno**

Los usuarios de Learning Manager experimentaron ciertos problemas de traducción en la aplicación del alumno. Estos problemas se han solucionado.

**Problemas relacionados con la suscripción a una aptitud**

En algunos casos, los alumnos no podían suscribirse a una nueva aptitud. Este problema se ha solucionado.

+++

+++Actualización 29

Fecha de publicación: 9 de abril de 2017

### Nuevas funciones {#newfeatures}

Para obtener una lista de las nuevas funciones y mejoras de la versión de abril de Learning Manager, consulte [¿Qué hay de nuevo?](../whats-new.md)

**Aplicación de alumno basada en widget**

Utilice los widgets de la página de inicio para administrar los cursos, las aptitudes y los logros. Utilice la barra de búsqueda para realizar una búsqueda en todo el LMS que abarque todos los objetos de aprendizaje, catálogos, aptitudes, notas y debates

Para obtener información detallada sobre la nueva página de inicio, consulte  [Página de inicio del alumno en Learning Manager](../learners/feature-summary/getting-started-learner.md).

**Configuración de administrador para el tablero del alumno**

Como administrador, puede controlar la página de inicio del alumno activando y desactivando distintos widgets.

**Aplicación móvil de Learning Manager para alumnos**

La nueva aplicación móvil de Learning Manager permite a los alumnos utilizar la aplicación para inscribirse y realizar cursos. La aplicación también se puede utilizar para administrar paneles.

Para obtener más información sobre el uso de Learning Manager en móviles, consulte  [Aplicación de alumno de Learning Manager para móviles](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Marcado de la asistencia mediante código QR**

Utilice el escáner de códigos QR para marcar su asistencia a las sesiones de clase con sus dispositivos móviles.

**Función de instructor**

Learning Manager presenta ahora instructores para módulos. Los instructores pueden gestionar las sesiones de los módulos, incluidos el tiempo, el lugar y el límite de puestos de los módulos que se les asignan.

Para ver información detallada sobre los instructores, consulte  [Instructores de Learning Manager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Cuenta de igual a igual**

Si es administrador, puede crear cuentas de igual a igual con las que compartir las licencias adquiridas.

Para obtener información sobre cómo crear y administrar cuentas de igual a igual, consulte  [Cuentas de igual a igual](../administrators/feature-summary/peer-account.md#main-pars_text).

**Ofertas de equivalencia de cursos**

Uso **[!UICONTROL Añadir nuevo idioma]** al añadir un módulo o un curso para que esté disponible en varios idiomas y formatos.

**Transcripciones de alumnos**

Learning Manager ofrece a los responsables y administradores la posibilidad de descargar datos de transcripción para realizar un seguimiento del historial de aprendizaje de cada usuario y de los equipos.

**Integración con otros proveedores de contenido**

Learning Manager ha introducido tres nuevos conectores en esta versión, para que los alumnos puedan acceder a los cursos y consumirlos de los siguientes proveedores de contenido: Lynda.com, getAbstract y Harvard ManageMentor.

Para obtener información sobre cómo configurar y utilizar estos conectores, consulte  [Conectores](../integration-admin/feature-summary/connectors.md#main-pars_header).

**ID exclusivo de objetos de aprendizaje**

Al crear objetos de aprendizaje, ahora los autores y los administradores pueden especificar ID exclusivos para los cursos, los programas de aprendizaje o las certificaciones. Si desea habilitar el ID exclusivo al crear un objeto de aprendizaje, haga clic en Configuración > General. Seleccione la casilla de verificación Activar situada junto a la opción ID exclusivos de objetos de aprendizaje.

**Foro de debate para alumnos**

Utilice el foro de debate de los cursos para interactuar con compañeros e instructores. Los alumnos pueden ver todas las publicaciones de los cursos. Sin embargo, también puede eliminar sólo las publicaciones que haya introducido. Para obtener más información sobre el foro de debate, consulte  [Ver y participar en debates](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Mejoras {#Enhancements-3}

**X de Y cursos**

Los criterios de finalización de los objetos de aprendizaje, como cursos, certificaciones y planes de aprendizaje, se pueden establecer de forma que los alumnos solo tengan que completar X de Y módulos o cursos. Los autores también pueden establecer criterios de finalización para las certificaciones y los planes de aprendizaje.

Para obtener más información sobre esta función, consulte  [Criterios de finalización del curso](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Moderación del curso**

Los administradores ahora reciben notificaciones cada vez que un autor edita o actualiza módulos y vuelve a publicar un curso.

**Configuración de administrador para restablecer módulos**

Ahora, los administradores pueden configurar la opción Restablecer módulo para permitir que los alumnos restablezcan un curso no aprobado o incompleto.

**Catálogo de informes**

Al crear informes en Learning Manager, ahora puede generar informes y gráficos para catálogos.

**Mejoras del plan de aprendizaje**

Los administradores ahora pueden crear planes de aprendizaje de los tipos En fecha. Con el plan de aprendizaje por fecha, un administrador puede especificar el nombre del evento, elegir la fecha del evento y seleccionar el grupo de usuarios al que pertenece el evento.

**Mensajes de inscripción específicos del curso**

Ahora los administradores pueden configurar y enviar por correo electrónico a los alumnos mensajes de inscripción específicos de los cursos.

**Anuncios fijos**

Como administrador, ahora puede habilitar la función Anuncios fijos.

**Compatibilidad con URL en los anuncios**

Puede agregar direcciones URL como anuncios agregando la dirección URL en HTML.

**Añadir nuevos tipos de entrega (cursos)**

Adobe Learning Manager ahora permite añadir tipos de entrega para los cursos.

**Mejoras de la función Autor**

Anteriormente, los autores solo podían crear módulos y cursos. Ahora, los autores también pueden crear certificaciones y programas de aprendizaje para los alumnos.

**Función de autor para usuarios externos**

Como administrador, ahora puede asignar funciones de autor a usuarios externos.

**Varios autores**

Learning Manager ahora permite a varios autores editar simultáneamente el mismo grupo de contenido.

**Mejoras de Adobe Connect**

Ahora puede configurar una sola URL de Adobe Connect con varias cuentas de Learning Manager.

**Compatibilidad con nuevos idiomas**

A partir de esta versión, se ofrece compatibilidad con japonés, portugués brasileño e italiano.



+++

+++Actualización 28

Fecha de publicación: 30 de enero de 2017

### Problemas solucionados {#IssuesFixed-6}

#### Configuración de cuenta {#accountsettings}

Como administrador, al hacer clic en Perfil externo y elegir Acciones > Cambiar perfil, no se mostraban todos los perfiles. Este problema se ha solucionado ahora.

#### Ciclo de vida del curso {#courselifecycle}

* Al iniciar un curso creado con la herramienta de aprendizaje electrónico de la biblioteca de Biz, la acción &quot;Reanudar&quot; no funcionaba. Este problema se ha solucionado.
* Algunos usuarios no podían iniciar un curso en iPad utilizando el vínculo del curso en Anuncios. Esto se ha solucionado.
* Al hacer clic en el botón Continuar del programa del alumno, no podía acceder a los cursos en orden. Esto se ha solucionado.
* La etiqueta Resumen del curso de los cursos del programa del alumno no estaba colocada correctamente. Este problema se ha solucionado ahora.

#### Aplicación del alumno {#learnerapp}

* En su dispositivo, si abría una imagen de anuncio en modo de pantalla completa, no podía volver a la aplicación. Esto se ha solucionado ahora.
* El contenido de Tincan que se cargó desde Captivate no se reproducía en modo en línea en los sistemas operativos Android y iOS. Este problema se ha solucionado.

#### Informes del curso {#coursereports}

Se generan informes de transcripciones de alumnos incorrectos en Learning Manager cuando el curso tiene varias versiones de módulos. Esto se ha solucionado.

#### Capa de API {#apilayer}

Se produce un error cada vez que intenta obtener la información de la versión del módulo mediante AP/courses/{coursesid}. Esto se ha solucionado.

+++

+++Actualización 27

Fecha de publicación: 23 de diciembre de 2016.

### Nuevas funciones {#Newfeatures-1}

Adobe permite a las empresas migrar los datos de formación y el contenido de formación de su organización desde sus sistemas de gestión de aprendizaje (LMS) existentes a la aplicación LMS de Learning Manager.

Learning Manager proporciona las herramientas y plantillas necesarias para que el administrador de integración de su organización pueda configurar y realizar las tareas de migración.

Para obtener más información sobre la función de migración, consulte  [Ayuda del manual de migración](../integration-admin/feature-summary/migration-manual.md)

### Mejoras {#Enhancements-4}

**Registro de usuarios**

Como administrador, ahora puede añadir nombres de dominio específicos mientras añade usuarios externos. Cuando los alumnos se registran en la cuenta, solo pueden introducir direcciones de correo electrónico de esos nombres de dominio.

También puede enviar vínculos de verificación por correo electrónico al correo electrónico de los usuarios cuando estos se registran en la cuenta. Para obtener más información sobre esta mejora, consulte  [Añadir usuarios/grupos de usuarios](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Reproductor Fluidic**

El reproductor Fluidic ahora le permite modificar la velocidad de reproducción. Puede elegir entre cinco variantes de velocidad disponibles. El reproductor Fluidic también le permite controlar los ajustes de volumen al realizar un curso.

Como alumno, también puede saltar hacia delante o hacia atrás 10 segundos con los nuevos iconos a cada lado del botón de reproducción en el reproductor Fluidic. Para obtener más información sobre estas mejoras, consulte  [Reproductor Fluidic](../learners/feature-summary/fluidic-player.md).

Las mejoras del reproductor Fluidic solo se aplican a vídeos.

+++

+++Actualización 26

Fecha de publicación: 6 de diciembre de 2016.

### Mejora {#enhancement}

Como parte de esta actualización, Learning Manager proporciona un punto final [PATCH/usuarios/{id}](<https://learningmanager.adobe.com/docs/Learning> ¡Manager/api/v1/#!/user/patch_users_id) para actualizar usuarios en una aplicación. Puede acceder a este punto final de la API con la función de administrador. Con****este punto final, puede actualizar la siguiente información de los usuarios de Learning Manager:

* Nombre
* Correo electrónico
* Perfil
* Función
* Responsable

### Problema resuelto {#issuefixed}

**Reproductor Fluidic**

Al realizar un curso desarrollado en Captivate con  `code cpQuizInfoStudentName` , el nombre del alumno no aparecía correctamente. Este problema se ha solucionado.

+++

+++Actualización 25

Fecha de publicación: 17 de noviembre de 2016.

### Mejoras {#Enhancements-5}

**Catálogos compartidos**

La función Catálogo compartido permite a los administradores de todas las cuentas compartir o adquirir catálogos con objetos de aprendizaje. Como extensión de esta función de catálogo compartido, se admite la propagación de actualizaciones a objetos de aprendizaje como insignias, aptitudes, módulos, cursos, programas de aprendizaje, certificaciones y ayudas de trabajo.

Para obtener más información sobre esta función, consulte  [Ayuda de catálogos compartidos](../administrators/feature-summary/catalogs.md#propagation)

**Comentarios de L1 y L3**

* El cuadro de diálogo Comentarios de L1 aparece en cuanto un alumno completa el consumo del curso. Además, el alumno recibe una notificación sobre la finalización de los comentarios de L1.
* Se ha incluido una opción para añadir preguntas descriptivas en la función de comentarios de L1 y L3. Los administradores pueden añadir estas preguntas descriptivas a los alumnos. Esta disposición se añade al conjunto predeterminado de preguntas que proporciona Learning Manager. Puede añadir dos preguntas descriptivas para los comentarios de L1 y una pregunta descriptiva para los comentarios de L3.\
  Para obtener más información sobre esta función, consulte [Comentarios de L1 y L3 preguntas descriptivas Ayuda](../administrators/feature-summary/courses.md#descriptive)

**Exportar usuarios**

* En función de la solicitud de algunos usuarios de empresa grandes, se proporciona una nueva opción para descargar la lista de todos los usuarios de la cuenta de Learning Manager. En el inicio de sesión del administrador, haga clic en **[!UICONTROL Usuarios]** en el panel izquierdo y haga clic en **[!UICONTROL Exportar datos de usuario]** para descargar la lista de usuarios como una hoja de excel.

### Problemas resueltos {#Issuesfixed-1}

**Inscripciones de cursos**

* En algunos casos, cuando un administrador intentaba ver las inscripciones de los cursos mediante la ficha Alumnos, algunos de los nombres de los alumnos inscritos no aparecían. Este problema se ha solucionado.

**Añadir cursos**

* Al añadir una aptitud al curso, si un autor añade una aptitud que tiene un espacio en blanco al final del nombre, solía producirse un error y el curso no se guardaba. Este problema se ha solucionado.

**Realizar cursos**

* En un curso solicitado, algunos alumnos no podían pasar de un módulo a otro mientras consumían un curso, ya que los módulos no se marcaban como completados. Este problema se ha solucionado.
* En un curso solicitado, los alumnos no podían navegar por los módulos del índice en los modos normal y de revisión. Este problema se ha solucionado.

**Reproductor Fluidic**

* En algunos casos, cuando un usuario carga contenido de un módulo con fotogramas o diapositivas ocultos, la Tabla de contenido del panel izquierdo solía mostrar los fotogramas o diapositivas ocultos. Este problema se ha solucionado.

**Informes**

* El tiempo necesario para cargar informes es mayor en la última actualización de Learning Manager. Este problema se ha solucionado.

+++

+++Actualización 24

Fecha de publicación: 12 de octubre de 2016.

### Mejoras {#Enhancements-6}

**Informes del curso**

* Para las cuentas de Learning Manager habilitadas para el identificador único universal (UUID), el UUID aparece en el informe de inscripción de cursos, las transcripciones de alumnos y los informes de puntuación de las pruebas.

### Problemas resueltos {#Issuesfixed-2}

**Ayudas de trabajo**

* En algunos casos, cuando un alumno intentaba navegar desde Aprendizaje>Ayudas de trabajo a Aprendizaje>Cursos, los cursos no se cargaban del modo esperado en la ficha Aprendizaje>Cursos. Este problema se ha solucionado.

**Añadir usuarios**

* En algunos casos, cuando se añade un solo usuario a la aplicación Learning Manager, el usuario no recibe ninguna notificación por correo electrónico. Este problema se ha solucionado.
* Los administradores no podían descargar el archivo CSV si fallaba el proceso de carga del CSV. Este problema se ha solucionado, los administradores pueden descargar el archivo CSV más reciente aunque falle el proceso de carga del archivo CSV.
* Si se importa un archivo CSV después de modificar la información del usuario registrado automáticamente con mayúsculas y minúsculas, los detalles del usuario registrado automáticamente no se mostraban en la interfaz de usuario del administrador. Este problema se ha solucionado.

**Informes del curso**

* En algunos casos, las puntuaciones de las pruebas no aparecían en los cursos aunque sí aparecían en las transcripciones de los alumnos. Este problema se ha solucionado.

**Informes de inscripción**

* En algunos casos, los informes de Excel de inscripción del alumno no se descargaban para los objetos de aprendizaje. Este problema solía producirse cuando se utilizaban caracteres especiales o no ASCII en el nombre de los objetos de aprendizaje. Este problema se ha solucionado.

**Inicio de sesión de usuario**

* Al configurar una contraseña durante el registro o el restablecimiento, el mensaje de error no aparece aunque la contraseña introducida no cumpla la política de contraseñas. Este problema se ha solucionado.

**Eficacia del curso**

* En la función de alumno, la eficacia de los cursos se mostraba como uno de los **Ordenar por** opciones de filtro incluso cuando un administrador ha desactivado la eficacia del curso para los alumnos. Este problema se ha solucionado.

**Certificaciones**

* Cuando un administrador eliminaba alumnos de una certificación periódica, solía producirse un error y la aplicación de Learning Manager se bloqueaba. Este problema se ha solucionado.

**Informes**

* Cuando un administrador intenta generar un informe de certificación con **Hasta la fecha** como opción, los usuarios inactivos no se mostraban en el informe. Este problema se ha solucionado.
* Cuando un administrador hacía clic en el vínculo Informes del curso de la ficha Informes > Mis informes, solía aparecer un cuadro de diálogo emergente sin ningún botón Cerrar. Este problema se ha solucionado.

**Reproductor Fluidic**

* Al previsualizar cursos como administrador o como autor, cuando un usuario elige el modo Pantalla completa en el reproductor Fluidic, la pantalla aparece en blanco. Este problema se ha solucionado.

**Compatibilidad con varios idiomas**

* Solían aparecer caracteres de signo de interrogación en lugar de caracteres chinos en respuesta a las llamadas de API de los usuarios. Este problema se ha solucionado.

**Capa de API**

* Solía producirse un error cada vez que un usuario intentaba obtener el ID de catálogo predeterminado mediante la API get/catalog/catalog Id. Un ID de catálogo predeterminado puede ser similar a &#39;970_default&#39;. Este problema se ha solucionado.

**Interfaz de usuario**

* Se han solucionado algunos errores tipográficos menores en la interfaz de usuario de la función de alumno de Learning Manager.

+++

+++Actualización 23

Fecha de publicación: 19 de septiembre de 2016.

### Problemas resueltos {#Issuesfixed-3}

**Transcripciones de alumnos**

* En algunos casos, si había más de veinte alumnos inactivos/eliminados en una cuenta, los alumnos inactivos mayores de veinte no se mostraban en la lista desplegable de búsqueda del cuadro de diálogo de transcripciones de alumnos. Este problema se ha solucionado.
* Si una cuenta de usuario externa ha caducado, sus alumnos no se muestran en la transcripción del alumno generada. Este problema se ha solucionado.

**Catálogos**

* Algunos de los clientes tenían problemas con la visualización de grupos de usuarios en un catálogo. Aunque haya más de veinte grupos de usuarios en un catálogo, solo se muestran 20 grupos de usuarios. Hemos solucionado este problema mostrando 200 grupos de usuarios en una página.

+++

+++Actualización 22

Fecha de publicación: 13 de septiembre de 2016.

En esta versión de actualización, hemos solucionado algunos de los problemas de backend de ingeniería de productos para mejorar la experiencia del cliente.

### Problemas resueltos {#Issuesfixed-4}

* Se ha producido un problema con la exportación de datos de módulos en transcripciones de alumnos que provocaba una exportación de datos incorrecta. Este problema se ha solucionado.
* Si un usuario utiliza una extensión de ID de correo electrónico con más de cuatro caracteres, no se admitía. Por ejemplo, si un ID de correo electrónico es <abcd@company.world> no se admitió, ya que el mundo de la extensión tenía más de cuatro caracteres. Lo hemos solucionado para admitir la extensión con más de cuatro caracteres.

+++

+++Actualización 21

Fecha de publicación: 1 de septiembre de 2016.

### Mejoras {#Enhancements-7}

**Eficacia del curso**

Ahora, los administradores pueden personalizar la función de eficacia del curso o del programa de aprendizaje para ocultar la puntuación de eficacia en la vista de los alumnos.

**Añadir usuarios externos**

Learning Manager ha aumentado el límite máximo de autorregistros externos a 5 dígitos.

**Informes**

Todos los informes descargados y las listas de alumnos de todos los objetos de aprendizaje muestran ahora los usuarios eliminados con una demarcación clara para los usuarios eliminados.

### Problemas resueltos {#Issuesfixed-5}

**Ciclo de vida del curso**

En algunos casos, cuando un autor editaba un curso compartido para actualizar la información de un módulo modificado, solía aparecer un mensaje de advertencia que indicaba que el usuario no podía editar porque se estaban procesando cambios anteriores. Este problema se ha solucionado.

**Compatibilidad con varios idiomas**

En algunas de las funciones de la interfaz de usuario de Learning Manager, los mensajes no se traducían y se mostraban al usuario en las frases de la configuración regional adecuadas. Este problema se ha solucionado.

**Añadir usuarios**

* Cuando se vuelve a añadir a un usuario eliminado como usuario único, el usuario no se añadía al grupo de usuarios &quot;todos los usuarios&quot; de forma predeterminada. Este problema se ha solucionado.
* Solía aparecer un número limitado de perfiles en los cuadros de diálogo de cambio de perfil de inscripción externa y de inscripción automática. La paginación ya está implementada.

**Ayudas de trabajo**

Cada vez que un alumno accedía a la ficha Ayudas de trabajo de la cuenta de alumno, solía aparecer el mensaje de error: &quot;Esta ayuda de trabajo ya no existe en la lista&quot; antes de cargar el contenido. Este problema se ha solucionado.

**Catálogos**

Durante la creación del catálogo, al añadir cursos como contenido al catálogo, el filtro Ordenar por no funcionaba del modo esperado. Este problema se ha solucionado.

**Configuración**

En la configuración de la cuenta, cuando un administrador utilizaba un subdominio que ya estaba siendo utilizado por otra cuenta, el administrador no recibía ningún mensaje de error. Este problema se ha solucionado.

**Capa de API**

* Cuando se utiliza include manager al buscar usuarios, se obtiene una jerarquía completa de responsables en lugar del responsable inmediato del usuario. Este problema se ha solucionado.
* Cuando un usuario con permiso de autorización de ámbito de alumno intentaba añadir usuarios, solía aparecer un mensaje de error genérico. Este problema se ha solucionado y ahora el alumno recibe un mensaje de acceso no autorizado.
* Cuando un usuario intentaba eliminar un último usuario existente en un grupo de usuarios, solía aparecer un mensaje de error 204 para el usuario. Este problema se soluciona ahora mostrando un mensaje de error relevante al usuario que indica que el grupo debe tener al menos un usuario.
* El espacio, si existe al principio del nombre, se recortó al mostrar el nombre de usuario en la API de GET/usuarios. Esto se ha solucionado ahora.
* Los borradores de cursos también se devolvían como respuesta cuando el administrador intentaba obtener todos los cursos. Se supone que estos borradores de cursos son privados del autor. Este problema se ha solucionado, los borradores de cursos no vuelven ahora.

**Integración con Adobe Connect**

* En algunos casos de sesiones de clase virtual basadas en Adobe Connect, la asistencia no se marcaba automáticamente después de la sesión. Este problema solía ocurrir solo cuando el instructor utilizaba un ID de inicio de sesión para iniciar sesión en lugar del ID de correo electrónico. Ahora se ha solucionado.
* En algunos casos, el nombre del instructor solía aparecer varias veces en la lista desplegable Instructor durante la creación del módulo de clase virtual basado en Adobe Connect. Este problema se ha solucionado.

+++

+++Actualización 20

Fecha de publicación: 22 de agosto de 2016.

### Mejoras {#Enhancements-8}

**Capa de API**

Como parte de esta actualización, hemos añadido las siguientes API nuevas para satisfacer algunos de los requisitos de nuestros clientes:

1. Usuarios de POST
1. Usuarios de DELETE
1. GET userGroups
1. grupos de usuarios de GET /{id}
1. grupos de usuarios de DELETE /{id}/Usuarios
1. grupos de usuarios de POST /{id}/Usuarios
1. GET /users/userId/userGroups

También hemos mejorado el modelo de usuario existente con las siguientes adiciones:

1. El modelo de responsable se agrega como relación con el modelo de usuario
1. userGroupId se agrega como un nuevo parámetro a GetUsers

**Transcripciones de alumnos**

Cuando un usuario generaba transcripciones de alumnos para un alumno, el cuadro de diálogo emergente solía aparecer durante muy poco tiempo y desaparecía sin solicitar una acción del usuario. Hemos mejorado la experiencia del usuario al proporcionar una ventana emergente que hace una pausa y solicita al usuario que haga clic en Aceptar.

**Integración con Adobe Connect**

El ID de inicio de sesión se proporciona como un nuevo campo opcional en la configuración de la integración de Adobe Connect para los usuarios que no utilizan su ID de correo electrónico para iniciar sesión.

### Problemas resueltos {#Issuesfixed-6}

**Informes del curso**

* Cuando un módulo de un curso consistía en preguntas de tipo abierto o solo preguntas de encuesta, solía aparecer un informe de puntuación de prueba en blanco cuando se exportaba. Este problema se ha solucionado.
* En algunos casos, el informe de puntuación de prueba no se descargaba cuando un usuario utilizaba el vínculo Exportar puntuación de prueba. Este problema se ha solucionado.

**Crear cursos**

La página Configuración del curso de la función de autor no aparecía cuando el administrador retiraba una aptitud asociada a ese curso. Este problema se ha solucionado.

**Encriptador inteligente**

El campo de búsqueda no admitía caracteres especiales como entrada y, como resultado, los resultados de la búsqueda no se mostraban. Este problema se ha solucionado.

+++

+++Actualización 19

Fecha de publicación: 11 de agosto de 2016.

### Mejoras {#Enhancements-9}

**Encriptador inteligente**

El rendimiento del motor de búsqueda se ha mejorado para proporcionar resultados de búsqueda más precisos a los usuarios.

**Integración con Adobe Connect**

El proceso de verificación/autenticación de la solicitud de integración se ha mejorado en la aplicación Learning Manager.

### Problemas resueltos {#Issuesfixed-7}

**Añadir usuarios**

* Cuando había un gran número de usuarios de Learning Manager, se producía un retraso al cargar la página de usuarios y grupos de usuarios. Este problema se ha solucionado.
* Una vez que el administrador completaba la carga del archivo CSV con nuevos usuarios, la lista de usuarios de la página no se actualizaba con los nuevos usuarios hasta que se actualizaba la página. Este problema se ha solucionado.
* En ocasiones, después de importar usuarios mediante CSV, el valor de ID de usuario de la página solía sustituirse por el ID de correo electrónico. Este problema se ha solucionado.

**Crear grupos de usuarios**

En algunos casos, el recuento de usuarios no se mostraba en la página de grupos de usuarios predeterminados de Learning Manager. Este problema se ha solucionado.

**Transcripciones de alumnos**

Los valores de atributo de los campos activos se mostraban incorrectamente en las transcripciones de alumnos para las certificaciones. Este problema se ha solucionado.

**Uso compartido de varias cuentas**

En un escenario en el que un administrador de cuentas compartiera un catálogo de cursos con el receptor y actualizara la prueba o el módulo de trabajo previo más adelante, el contenido del módulo de trabajo previo o de prueba se solía reproducir en el módulo de contenido del receptor. Este problema se ha solucionado.

**Temas y marca**

Cuando un administrador cambiaba un tema a la aplicación mediante el widget de vista previa en vivo y cambiaba su función, el widget de vista previa en vivo no funcionaba del modo esperado en una nueva función. Este problema se ha solucionado.

**Compatibilidad con varios idiomas**

Cuando un administrador cambiaba la configuración regional de la aplicación a chino simplificado o español, parte del contenido del menú en el panel izquierdo, las instrucciones en línea y los mensajes emergentes no se mostraban en palabras u oraciones significativas. Este problema se ha solucionado.

**Reproductor Fluidic**

* Cuando un autor crea un curso con contenido AICC o Tin Can e intenta obtener una vista previa del contenido, este no se reproduce. Este problema se ha solucionado.
* La vista previa del módulo no funcionaba al crear un curso o al editarlo un autor. Este problema se ha solucionado.

**Catálogos**

Cuando un alumno intentaba acceder a la URL de los catálogos/programas de aprendizaje directamente en el navegador, se solía redirigir a los cursos. Este problema se ha solucionado.

**Integración de Salesforce**

* Después de establecer una conexión de Salesforce o FTP, en la página Asignar atributos, las flechas desplegables de los campos no se mostraban en los navegadores IE, Edge y Safari. Además, algunos de los mensajes emergentes no se mostraban en los flujos de trabajo. Este problema se ha solucionado.
* En algunos casos, cuando un administrador intentaba sincronizar los datos importados con .csv en el conector de FTP, la sincronización solía fallar con entradas replicadas. Este problema se ha solucionado.

**Capa de API**

* Cuando un administrador autoriza al alumno externo utilizando la autenticación de OAuth, a veces los alumnos externos no pueden iniciar sesión en la aplicación. Este problema se ha solucionado.
* En ocasiones, cuando se producía una llamada de API para las ayudas de trabajo del alumno, solía aparecer un error de acceso no autorizado. Este problema se ha solucionado.

**Configuración**

En la página de orígenes de datos, cuando se establece y se guarda una hora de programación automática, a veces vuelve al estado anterior. Este problema se ha solucionado.

**Informes de grupos de usuarios**

Los valores del grupo de usuarios en el filtro no se rellenaban cuando el tipo de informe se elige como Personalizado. Este problema se ha solucionado.

**Integración con Adobe Connect**

Solía aparecer un título de encabezado inapropiado para la integración de Adobe Connect después de completar la conexión correctamente. Se corrige el texto del encabezado de página.

**Informes**

A veces, incluso si se seleccionaba la opción &#39;Mostrar datos de valores actuales&#39;, los datos más recientes no se mostraban en los informes. Este problema se ha solucionado.

+++

+++Actualización 18

Fecha de publicación: 31 de julio de 2016.

## Nuevas funciones y mejoras {#newfeaturesandenhancements}

Para obtener una lista de las nuevas funciones y mejoras de la versión de julio de Learning Manager, consulte [Novedades de la aplicación](../whats-new.md).

A continuación se indican algunas de las funciones de mejora para su referencia.

**Transcripciones de alumnos**

Learning Manager proporciona una función para generar transcripciones para los alumnos de Learning Manager de su organización. Para obtener más información, consulte  [Contenido de ayuda de la función Transcripciones de alumnos](../administrators/feature-summary/learner-transcripts.md).

**Exportar insignia como PDF**

Learning Manager le permite exportar las insignias como archivos de PDF. Para obtener más información, consulte  [Contenido de la función Insignias](../administrators/feature-summary/badges.md).

**Puntuación de prueba para módulos**

Puede añadir una puntuación de prueba para los módulos Clase, Clase virtual y Actividad.

**Añadir usuarios**

* Puede mover alumnos de un grupo de registro automático a otro grupo.
* Puede mover usuarios de un grupo externo a otro.
* Puede hacer que un usuario de un grupo externo sea responsable del mismo grupo externo.
* Después de añadir un grupo de usuarios externos a Learning Manager, también puede pausar el proceso de registro de usuarios externos. En cualquier momento, siempre puede revocar el bloqueo (pausa) eligiendo una opción de Reanudar .
* Ahora puede editar el nombre y el ID de correo electrónico de los alumnos.

**Inscripción automática**

Los alumnos también pueden darse de baja de objetos de aprendizaje como cursos, programas de aprendizaje o certificaciones. Sin embargo, el alumno no puede darse de baja de un objeto de aprendizaje después de completarlo.

**Consumir objetos de aprendizaje**

Ahora, los administradores pueden marcar una actividad de aprendizaje de los alumnos como completada.

**Informes**

* Puede suscribirse a informes de cursos, programas de aprendizaje o certificados. También puede suscribirse a informes de cursos individuales para obtener datos como la puntuación de la prueba y el estado del alumno. Las suscripciones se enviarán a su ID de correo electrónico registrado en la cuenta de Learning Manager. También puede cambiar este ID de correo electrónico.
* Al exportar el informe de inscripción de certificación, aparece una nueva columna denominada **Fecha de vencimiento** también se exporta. Los datos de esta columna permiten a los administradores conocer a los alumnos que incumplieron los plazos de consumo de objetos de aprendizaje.

**Plantillas de correo electrónico**

Ahora, puede editar el encabezado de las plantillas de correo electrónico.

+++

+++Actualización 17

Fecha de publicación: 15 de junio de 2016.

### Problemas resueltos {#Issuesfixed-8}

**Añadir usuarios**

Cuando había un gran número de usuarios de Learning Manager, se producía un retraso al cargar la página de usuarios y grupos de usuarios. Este problema se ha solucionado.

**Crear grupos de usuarios**

En algunos casos, el recuento de usuarios no se mostraba en la página de grupos de usuarios predeterminados de Learning Manager. Este problema se ha solucionado.

+++

+++Actualización 16

Fecha de publicación: 10 de junio de 2016.

## Problema resuelto {#Issuefixed-1}

Algunos clientes tuvieron problemas al utilizar la función de inicio de sesión único en Learning Manager. Este problema se ha solucionado haciendo referencia al entityId de Learning Manager a una URL (<https://learningmanager.adobe.com>) en lugar de una palabra clave. Learning Manager cumple la especificación SAML 2.0.

+++

+++Actualización 15

Fecha de publicación: 25 de mayo de 2016

### Mejoras {#Enhancements-10}

**Certificaciones/programas de aprendizaje**

* En la lista de inscripción de alumnos para certificaciones y programas de aprendizaje, se muestra el nombre completo (nombres y apellidos) de los alumnos. Anteriormente, solía aparecer solo el nombre de los alumnos.
* Las aptitudes con créditos de nivel superior se consideran de la lista de cursos de certificaciones/programas de aprendizaje y se muestran en las tarjetas como aptitudes de certificación/programa de aprendizaje. Si hay varios cursos con el mismo valor de créditos, se seleccionan por orden alfabético. Anteriormente, los nombres de aptitudes para los programas de certificación/aprendizaje se consideraban aleatoriamente en una lista de cursos respectivos.

**Importar CSV**

Para la función de carga automática de CSV mediante FTP, los administradores reciben notificaciones por correo electrónico si se produce un error en la carga del CSV.

**Añadir socios externos**

Cuando los alumnos externos visitan la página de registro utilizando una URL de perfil externo, el nombre del perfil externo se muestra en la página de registro para una mejor identificación.

### Problemas resueltos {#Issuesfixed-9}

**Previsualización y publicación de cursos**

* En la función de autor, al previsualizar un curso cargado desde Captivate como contenido de SCORM+SWF con `code $$cpQuizInfoStudentName$$` variable, se muestra un valor nulo para la variable. Este problema se ha solucionado.
* Cuando se publicaba y se veía un curso de Presenter con un título que contenía apóstrofo (&#39;) en Learning Manager, solían aparecer signos de interrogación (???) en el índice. Este problema se ha solucionado.

**Certificaciones**

* Si una certificación está asociada a un catálogo y cuando se repite, aparece en todos los catálogos asociados. Anteriormente, había algunos casos en los que los usuarios no podían ver las certificaciones recurrentes en sus catálogos.
* Al crear certificaciones, si un administrador introduce el **días para completar** que sea mayor o igual que el período de validez de la certificación, aparece un mensaje de advertencia. Anteriormente, el mensaje de advertencia no se mostraba a los administradores.
* La certificación **validez** se muestra a los usuarios en términos de meses. Anteriormente, el valor base aparecía en términos de años.

**Definir programas de aprendizaje**

La fecha límite no aparece para las instancias predeterminadas del programa de aprendizaje. Anteriormente solía aparecer un plazo predefinido que podía no ser relevante para los usuarios.

**Crear cursos utilizando módulos**

* Cuando un autor actualizaba un módulo de un curso mixto, la página de asistencia no aparecía en la función de administrador. Este problema se ha solucionado.
* Cuando el nombre de una instancia de curso contiene dos puntos (:), la acción de exportación para la lista de alumnos produce un error. Este problema se ha solucionado.

+++

+++Actualización 14

Fecha de publicación: 4 de mayo de 2016

### Mejoras {#Enhancements-11}

**Catálogos**

Cuando un alumno accede al catálogo, el enfoque predeterminado cambia entre las pestañas en función de la disponibilidad de los objetos de aprendizaje, en el siguiente orden: 1. Cursos 2. Programas 3. Certificaciones y 4. Ayudas de trabajo. Por ejemplo, si los cursos no están disponibles en la ficha Cursos de ese alumno, el enfoque cambia al siguiente objeto de aprendizaje, que es Programas si hay programas de aprendizaje.

**Configuración de cuenta**

Se proporciona una opción de comentarios en el cuadro de diálogo de confirmación de la desactivación de la cuenta cuando un administrador decide desactivar una cuenta.

### Problemas resueltos {#Issuesfixed-10}

**Exportar informes**

* La exportación de la lista de alumnos solía fallar cuando un gran conjunto de usuarios se inscribía en un programa de aprendizaje. Este problema se ha solucionado.
* Cuando un curso tiene dos instancias con el mismo nombre y el nombre de la instancia es largo, no se crearon dos hojas de cálculo en el archivo de Excel exportado. Este problema se ha solucionado.

**Inscripción masiva**

Cuando se inscribía un gran número de alumnos en objetos de aprendizaje como programas de aprendizaje, cursos, certificaciones, ayudas de trabajo y planes de aprendizaje, la inscripción solía fallar. Este problema se ha solucionado.

+++

+++Actualización 13

Fecha de publicación: 20 de abril de 2016

### Problemas resueltos {#Issuesfixed-11}

**Crear cursos utilizando módulos**

Cuando se cargaba contenido de un módulo con un nombre de archivo largo, se producían problemas con el aspecto de los botones. Además, las opciones de carga y eliminación del módulo no funcionaron del modo esperado. Este problema se ha solucionado.

**Importar CSV**

De acuerdo con la solicitud de los clientes estadounidenses, la hora de carga automática de CSV por FTP se ha cambiado de GMT medianoche a PST medianoche.

**Exportar informes**

La exportación de datos de inscripción solía fallar si uno de los alumnos inscritos se eliminaba después de consumir el curso. Este problema se ha solucionado.

**Plantillas de correo electrónico**

* La palabra **socios,** que se utilizó para representar a grupos externos,**** es **** eliminado del cuerpo y del título de las plantillas de correo electrónico. Los grupos externos no se denominan necesariamente asociados.\
  **Nota:** Esta plantilla actualizada no aparecerá si la plantilla predeterminada ya se ha modificado. Para ver la plantilla actualizada, haga clic en **Volver al original** en **Vista previa de plantilla** diálogo.

* No se puede hacer clic en la dirección URL en el correo electrónico que reciben los administradores cuando **Perfil creado (registro automático)** y **Perfil creado (externo/socios)** se editan las plantillas de correo electrónico. Este problema se ha solucionado.

+++

+++Actualización 12

Fecha de publicación: 7 de abril de 2016

### Mejoras {#Enhancements-12}

**Ayudas de trabajo**

Cree ayudas de trabajo mediante una dirección URL. Puede mencionar solo un nombre de URL en el flujo de trabajo de creación de ayudas de trabajo y crear ayudas de trabajo si desea utilizar cualquier contenido en línea existente como ayuda de trabajo.

**Añadir alumnos**

Se permite la edición de datos de un solo usuario, como el nombre, el correo electrónico, el perfil y el nombre del responsable. Todos los grupos de usuarios correspondientes se actualizan con los datos de usuario más recientes.

**Exportar informes**

Las columnas Nombre del responsable, Nombre del objeto de aprendizaje y Valor no único definido por el usuario del CSV se añaden a la lista de alumnos exportada para objetos de aprendizaje. Anteriormente, solían aparecer solo los datos básicos de los alumnos, como el nombre, la fecha, el correo electrónico y el estado.

**Añadir socios externos**

La aplicación Learning Manager no permite a los alumnos externos iniciar sesión en la aplicación una vez que ha caducado su cuenta. Los socios externos pueden ver el estado de su cuenta en la aplicación.

**Certificaciones**

Puede renovar las certificaciones en términos de meses mencionando el valor en **Validez** campo. Anteriormente, la renovación de la certificación solo se permitía en términos de años.

### Problemas resueltos {#Issuesfixed-12}

**Anuncios**

En el inicio de sesión del administrador, la paginación no funcionaba en la página Anuncios. Este problema se ha solucionado.

**Planes y programas de aprendizaje**

* Cuando un alumno intentaba omitir un módulo de curso solicitado en un programa de aprendizaje, no se mostraba ningún mensaje de error. Este problema se ha solucionado ahora. Un mensaje de error **No se pueden omitir módulos** aparece.
* Los cursos no se añadían a los programas de aprendizaje cuando se utilizaba la paginación en la lista de cursos. Este problema se ha solucionado.
* **Retirado** aparecía dos veces en Programas de aprendizaje > instancias. Este problema se ha solucionado.

**Ayudas de trabajo**

* Cuando un alumno elimina ayudas de trabajo del **Aprendizaje** ficha, **Nombre** la ordenación no funcionaba del modo esperado hasta que se actualizó la página. Este problema se ha solucionado.

* Si una ayuda de trabajo forma parte de varios cursos, los cursos no se mostraban en la lista de ayudas de trabajo. Este problema se ha solucionado.
* Si un alumno acerca o aleja el explorador, la paginación de la lista de ayudas de trabajo no funcionaba del modo esperado. Este problema se ha solucionado.

**Toma de cursos**

* Si un alumno acerca o aleja el explorador, la paginación de los cursos no funcionaba del modo esperado. Este problema se ha solucionado.

**Creación de aptitudes**

En el inicio de sesión de los alumnos, consulte la información del nombre de la aptitud en **Mapa de aptitudes **era** **no muestra el nombre completo****. Este problema se ha solucionado.

**Añadir socios externos**

* Se ha incluido un mensaje de texto en la página de registro de usuarios externos como **Los usuarios deben registrarse y crear primero una contraseña de nombre de usuario para los inicios de sesión posteriores**.

**Notificaciones de usuarios**

* Cuando un alumno externo hace clic en **Abrir Notas** en la notificación de correo electrónico Regresar al curso, se abre el reproductor, pero el panel de notas no funcionaba. Este problema se ha solucionado.
* Cuando un alumno externo intenta abrir los módulos previos al trabajo o de prueba mediante **Abrir Notas** en la notificación de correo electrónico Regresar al curso, el contenido de las notas no estaba visible. Este problema se ha solucionado.

**Crear cursos utilizando módulos**

Cuando un administrador intentaba inscribir alumnos en un curso mixto que contenía un módulo de clase caducado, no se abría el cuadro de diálogo de inscripción. Este problema se ha solucionado.

**Exportar informes**

Si el texto de una pregunta contiene más de 255 caracteres y está habilitado para el formato SCORM 1.2, los informes de prueba de dichas preguntas no funcionaban. Este problema se ha solucionado.

+++

+++Actualización 11

Fecha de publicación: 15 de marzo de 2016

### Problemas resueltos {#Issuesfixed-13}

**Crear cursos con módulos**

* En el inicio de sesión del administrador, al intentar crear una nueva instancia para cursos de **Retirado**, solía producirse un error. Este problema se ha solucionado.
* En el inicio de sesión del administrador con contenido localizado, al inscribir alumnos en la instancia del curso, se distorsionaban las acciones y los diseños de pantalla de inscripción. Este problema se ha solucionado.
* Cuando un autor estaba creando módulos de clase o clase virtual, el mes predeterminado del calendario de fechas solía aparecer como Ene de 2015. Este problema se ha solucionado de forma predeterminada para reflejar la fecha actual.
* Cuando el nombre de una instancia de curso se componía de una barra diagonal o una barra diagonal inversa, la acción de exportación de la lista de alumnos solía fallar. Este problema se ha solucionado.

**Anuncios**

Cuando un alumno coloca el ratón sobre un anuncio de vídeo, el cursor no cambia a un dedo señalador, como se esperaba. Este problema se ha solucionado.

**Notificaciones de usuarios**

Cuando un alumno externo hace clic en **Abrir Notas** en la notificación de correo electrónico Regresar al curso, no funcionaba. Este problema se ha solucionado ahora. Este vínculo abre el Reproductor con notas, incluso cuando el usuario no ha iniciado sesión en Learning Manager.

**Compatibilidad con los idiomas alemán y francés**

Las URL de ayuda en la función de carga de CSV se dirigían al contenido de ayuda en inglés. Este problema se ha solucionado.

**Previsualización y publicación de cursos**

Al iniciar sesión como autor, al obtener una vista previa del contenido de la API TinCan (SWF/HTML) de Presenter 10 y 11, el contenido no funcionaba. Este problema se ha solucionado.

**Correos electrónicos personalizables**

Los nombres de título de las plantillas de correo electrónico no eran apropiados. El contenido se actualiza en estos títulos de plantilla para que sean legibles.

**Ayudas de trabajo**

En el navegador Internet Explorer 11, el nombre y el icono de la ayuda de trabajo aparecían distorsionados en la vista previa del autor y el administrador. Este problema se ha solucionado.

+++

+++Actualización 10

Fecha de publicación: 28 de febrero de 2016.

## Nuevas funciones {#Newfeatures-2}

### Ayudas de trabajo

Las ayudas de trabajo son un repositorio de contenido de formación al que pueden acceder los alumnos sin ningún criterio de inscripción o finalización. Los alumnos pueden consultar estas ayudas de trabajo para obtener ayuda para realizar cualquier actividad o tarea en una organización. El administrador puede realizar un seguimiento del número de descargas por ayuda de trabajo.

Para obtener más información sobre esta función, consulte  [Ayuda de ayudas de trabajo](../learners/feature-summary/job-aids.md).

### Anuncios

Un anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador puede crear y difundir a un conjunto definido de usuarios. Utiliza los anuncios para motivar a los alumnos a realizar cursos de formación y, de este modo, crear una cultura de aprendizaje.

Para obtener más información sobre esta función, consulte  [Ayuda de anuncios](../learners/feature-summary/announcements.md).

### Compatibilidad con API Tin Can

Adobe Learning Manager admite la especificación Tin Can API (también conocida como Experience API o xAPI). Puede cargar y realizar el seguimiento de contenido compatible con la API Tin Can de forma similar al seguimiento de contenido SCORM y AICC.

Para obtener más información, póngase en contacto con el equipo de soporte técnico de Adobe.

### Secuencia del curso

Puede crear una ruta de aprendizaje asignando automáticamente un curso de seguimiento o cualquier actividad de aprendizaje.

Se han actualizado los eventos de los planes de aprendizaje. Se han añadido varios eventos nuevos. Consulte la  [Planes de aprendizaje](../learners/feature-summary/learning-programs.md) para obtener más información.

### Recordatorio de notas

Si toma notas mientras está realizando un curso, Learning Manager le recordará que, pasados 15 días, debe enviar una notificación para revisar las notas.

### Interacción a nivel de grupo

Los administradores pueden definir el ámbito de la interacción cambiando la configuración del ámbito. Puede habilitar la interacción de forma selectiva entre usuarios, grupos o ubicaciones de perfil similares. Consulte la  [Interacción](../learners/feature-summary/gamification.md) para obtener más información.

### Compatibilidad con los idiomas alemán y francés

La aplicación Learning Manager está disponible en francés y alemán. Puede personalizar el idioma para los comentarios, las instancias de cursos y la comunicación.

### Mejoras {#Enhancements-13}

Hay importantes mejoras en las funciones existentes de Learning Manager. Algunas de las mejoras predominantes son las siguientes:

### Importar CSV

Si elimina usuarios, no puede volver a agregar a los mismos usuarios a la aplicación con la adición de un solo usuario. Sin embargo, puede volver a añadir al usuario eliminado mediante el proceso de carga de CSV. Hay cambios significativos en la restricción de campos obligatorios en la función de carga de CSV. Consulte la  [Preguntas frecuentes sobre CSV](../administrators/add-users-in-bulk.md) para obtener más información.

### Vista de lista de cursos

De forma predeterminada, puede ver los cursos como tarjetas. En esta versión se ha introducido una vista de lista. Puede hacer clic en el icono de la barra triple situado junto al campo de búsqueda para cambiar la vista.

### Eliminar cursos

Ahora puede eliminar cursos en las fases de borrador y retirado. Consulte la  [Cursos](../administrators/feature-summary/courses.md) para obtener más información. Si se elimina un objeto de aprendizaje, también se eliminan todos sus datos de informes. Si se elimina un curso y formaba parte de cualquier otro objeto de aprendizaje, el usuario recibe el mensaje correspondiente.

**Planes y programas de aprendizaje**

Puede aplicar el orden en que los alumnos pueden realizar los cursos dentro de los programas de aprendizaje. Puede eliminar programas de aprendizaje en las fases de borrador y retirado. Si se elimina un objeto de aprendizaje, también se eliminan todos sus datos de informes.

**Certificaciones**

Puede eliminar certificaciones en fases de borrador y retiradas. Si se elimina un objeto de aprendizaje, también se eliminan todos sus datos de informes.

**Valoración de eficacia del curso**

En el inicio de sesión del administrador, puede exportar datos de comentarios de L1 y L3 de cualquier curso.

**Crear cursos con módulos**

Puede hacer que los alumnos completen los requisitos previos antes de realizar los cursos.

**Notificaciones de usuarios**

Los alumnos reciben notificaciones cada vez que se inscriben automáticamente en un programa de aprendizaje.

**Módulos de clase (ILT)**

Puede crear cursos de clase para una fecha pasada. Esta función permite a los administradores de la empresa proporcionar información sobre cursos de clase antiguos también en Learning Manager y generar informes.

**Exportar informes**

Se ha mejorado el informe de los alumnos. Puede ver en el informe el nombre, el correo electrónico, el estado del objeto de aprendizaje, los criterios de inscripción, la fecha de inscripción, la fecha de finalización y la fecha de inicio.

**Añadir socios externos**

Después de inscribir alumnos externos en la cuenta de Learning Manager, también puede reducir el número de alumnos, si es necesario. Sin embargo, no puede reducir el tamaño de los alumnos más allá del número de puestos utilizados. Como solución alternativa, puede eliminar primero a los alumnos registrados y luego volver a inscribirse con el número de puestos necesario.

### Problemas resueltos {#Issuesfixed-14}

**Asistencia de alumnos**

La hoja de asistencia de la vista del administrador muestra el nombre completo del empleado, si está disponible. Anteriormente, solía aparecer solo el nombre del alumno.

**Planes y programas de aprendizaje**

Todos los cursos de los programas de aprendizaje se muestran en el orden previsto. Anteriormente, había problemas en el orden de los cursos en un programa de aprendizaje. Este problema se ha solucionado.

**Añadir alumnos**

Si un usuario registrado automáticamente intenta registrarse de nuevo mediante el proceso de registro automático, aparecerá el mensaje correspondiente. El formato y el contenido del mensaje son fijos.

**Informes**

Si desea que el contenido identifique el tiempo empleado por el usuario en consumir contenido, puede identificarlo mediante una variable, `code cmi.core.session_time`. La variable no se estableció anteriormente. Este problema se ha solucionado.

**Crear cursos con módulos**

Siempre que otro módulo reemplaza un módulo de curso existente, se genera una nueva versión del mismo. Si se exportaba la prueba de este nuevo módulo, solía producirse una excepción y no se generaba el informe de prueba. Este problema se ha solucionado ahora.

**Plantillas de correo electrónico**

Se han corregido los errores tipográficos en las plantillas de correo electrónico.

+++

+++Actualización 9

Fecha de publicación: 9 de febrero de 2016.

## Comportamiento Cerrar sesión actualizado {#signoutbehaviorupdated}

Cuando los usuarios hagan clic **[!UICONTROL Cerrar sesión]** en Learning Manager, ahora cierran la sesión de la aplicación Learning Manager y también la de sus ID de Adobe.

+++

+++Actualización 8

Fecha de publicación: 20 de enero de 2016.

### Mejoras {#Enhancements-14}

**Correos electrónicos personalizables**

* Los usuarios pueden modificar la sección de pie de página de las plantillas de correo electrónico. Puede personalizar el pie de página de una plantilla de correo electrónico con el texto que desee. El pie de página personalizado se aplica automáticamente a todos los tipos de plantillas de correo electrónico.

**Toma de cursos**

* Los objetos de recursos en el modo de vista previa de un curso se muestran uno tras otro en una nueva línea. Anteriormente, había casos en los que los recursos de un curso solían aparecer uno junto al otro en una sola línea.

**Vínculo directo a objetos de aprendizaje**

* Puede acceder a los objetos de aprendizaje (excepto a la certificación) mediante una dirección URL directa. La **[!UICONTROL Copiar URL]** se muestra en los mosaicos de objetos de aprendizaje. Los usuarios pueden hacer clic en **[!UICONTROL Copiar URL]** y pegue el vínculo en otra página del navegador para acceder directamente al objeto de aprendizaje.

**Crear cursos utilizando módulos**

* Al crear un curso, los autores pueden organizar los requisitos previos de los cursos en cualquier orden. Anteriormente, esta opción no estaba disponible en Learning Manager.

* Los autores pueden añadir o eliminar requisitos previos de cursos en Cursos publicados. Anteriormente, esta función solo estaba disponible para los borradores de cursos.

**Registro de usuarios**

* Los usuarios pueden iniciar sesión en Learning Manager sin ninguna verificación de URL adicional si su Adobe ID coincide con el ID de correo electrónico de Learning Manager. Al añadir usuarios a la cuenta, el administrador de una organización proporciona el ID de correo electrónico de Learning Manager.

**Crear catálogo**

* En la función de administrador, al crear catálogos mediante **Añadir objetos de aprendizaje** , los cursos retirados no aparecen en la lista de cursos.

**Otras correcciones**

* En la función de administrador, el nombre completo de los alumnos se muestra en **Alumnos** . Anteriormente, solía aparecer solo el nombre del alumno.

+++

+++Actualización 7

Fecha de publicación: 13 de enero de 2016.

### Problemas resueltos {#Issuesfixed-15}

**Toma de cursos**

* Al acceder al contenido del curso, la barra de reproducción de contenido siempre aparece en la pantalla. Anteriormente había un problema con la barra de reproducción de contenido, ya que solía desaparecer de la pantalla intermitentemente.
* Al acceder al contenido del curso, si el contenido tiene un cuadro de diálogo emergente que aparece preguntando a los usuarios si realmente desean salir o permanecer en la página, al pulsar Permanecer en dicho cuadro de diálogo, el usuario vuelve al contenido. En algunos casos, al hacer clic en el botón de permanecer , se solía retirar al usuario del contenido del curso.

**Otras correcciones**

* Se han resuelto algunos problemas relacionados con la reproducción de contenido.

+++

+++Actualización 6

Fecha de publicación: 22 de diciembre de 2015

### Mejoras {#Enhancements-15}

**Panel personal**

* Al acceder a cursos, catálogos y programas de aprendizaje con las funciones de administrador y de autor, el orden de las fichas se ha modificado a **Publicado - Borrador - Todo - Retirado**. La selección predeterminada es **Publicado.**

### Problemas resueltos {#Issuesfixed-16}

**Toma de cursos**

* En la función de alumno mientras está realizando un curso, si el reproductor se cierra con el botón de retroceso del navegador o con la tecla Retroceso del teclado, el tiempo de aprendizaje dedicado al curso se captura en los informes. En algunos casos, se producía el problema de que esta duración no se registraba en los informes.

**Registro de usuarios**

* Si un usuario registra una cuenta de Learning Manager mediante el registro automático habilitado para SSO, el nombre de usuario en la lista de usuarios aparece correctamente según los registros. Hubo algunos casos en los que el nombre de usuario solía aparecer incorrectamente.

**Crear cursos utilizando módulos**

* Cuando un autor duplica un curso, los archivos de recursos del curso duplicado se pueden eliminar o actualizar. En algunos casos, los usuarios tenían problemas para actualizar o quitar recursos de cursos duplicados.

**Creación de catálogos personalizados para grupos de usuarios**

* Al utilizar **Añadir objetos de aprendizaje** en la función de administrador, puede filtrar cursos, elegir un curso y añadir mediante **Añadir** situado en la parte inferior del cuadro de diálogo. En algunos casos, **Añadir** no aparecía para algunos usuarios.

+++

+++Actualización 5

Fecha de publicación: 11 de diciembre de 2015

### Problemas resueltos {#Issuesfixed-17}

**Inicio de sesión de usuario**

* Cuando un usuario intentaba iniciar sesión en la aplicación de Learning Manager sin utilizar el vínculo de activación, el mensaje de error aparecía en un formato incorrecto. Este problema se ha solucionado.

**Aplicación para tabletas**

* Después de instalar Learning Manager en tabletas Android o iPhone, no aparecen los mensajes de compatibilidad del navegador. Anteriormente, solía aparecer un mensaje de compatibilidad del navegador para los usuarios. Este problema se ha solucionado.

+++

+++Actualización 4

Fecha de publicación: 9 de diciembre de 2015

### Mejoras {#Enhancements-16}

**Añadir usuarios**

* En la función de administrador, cuando el administrador registra usuarios o completa la adición de un solo usuario, aparece un mensaje que indica que el flujo de trabajo se ha completado correctamente, junto con los siguientes pasos a seguir.
* Cuando un usuario intenta iniciar sesión en la aplicación de Learning Manager directamente sin utilizar el vínculo de activación del usuario, aparece un mensaje de error que solicita a los usuarios que utilicen el vínculo de activación.

**Navegadores compatibles**

* Si algún usuario accede a la aplicación Learning Manager en navegadores no compatibles, el usuario recibe una alerta con la lista de navegadores de la lista blanca.

### Problemas resueltos {#Issuesfixed-18}

**Informes**

* En la función de administrador o de responsable, al crear un informe con el eje secundario con el tiempo de aprendizaje dedicado, aplicar el filtro de responsable y guardar el informe, el usuario no podía descargar dichos informes. Puede descargar todos los tipos de informes.

**Añadir usuarios**

* Se mostraron algunos errores tipográficos en el mensaje de alerta al habilitar alumnos externos en la función de administrador. El problema se ha solucionado.
* En la función de administrador, aparece el mensaje de error correspondiente cuando el campo Responsable no se ha seleccionado correctamente durante la adición de un solo usuario.

**Registro de usuarios**

* El correo electrónico de bienvenida recibido por los nuevos usuarios destaca la importancia de vincular Adobe ID con el ID de Learning Manager para que el inicio de sesión se realice correctamente.

**Correos electrónicos personalizables**

* Al añadir varios alumnos a los cursos de clase que tienen sesiones como archivos adjuntos, algunos alumnos no recibían notificaciones por correo electrónico. Este problema se ha solucionado.
* Los mensajes de correo electrónico dirigidos a los alumnos sobre las inscripciones a objetos de aprendizaje y otros eventos contienen el nombre de objeto de aprendizaje específico en el asunto del correo electrónico.

**Otras correcciones**

* Se han solucionado los problemas relacionados con los vínculos URL en las plantillas de correo electrónico.
* Asistencia prestada para

   * Publicar en Learning Manager
   * Compatibilidad de carga de contenido más rápida para la versión CP 8 (se requiere el parche CP803)

+++

+++Actualización 3

Fecha de publicación: 26 de octubre de 2015.

### Mejoras {#Enhancements-17}

**Añadir usuarios**

* El vínculo Ayuda en línea se proporciona en el cuadro de diálogo Añadir usuarios > Carga de CSV para una mejor comprensión de los usuarios al cargar el archivo CSV.

**Reproductor Fluidic**

* Al cargar contenido de cursos de Captivate con más de 500 MB, el contenido no se reproducía en el reproductor Fluidic. Esta restricción se ha eliminado. Actualmente, el límite de tamaño se ha cambiado a 2 GB.

**Factura**

* En la función de administrador, cuando un usuario introduce una serie de alumnos y hace clic en ellos **Realizar pedido,** aparece un cuadro de diálogo con detalles sobre los cargos de suscripción mensuales y anuales por usuario.

### Problemas resueltos {#Issuesfixed-19}

**Crear cursos utilizando módulos**

* Al crear cursos con módulos de actividad, los autores pueden elegir direcciones URL externas válidas aunque contengan rutas de carpeta en la dirección URL. Anteriormente, no se admitían las direcciones URL con rutas de carpeta. Este problema se ha solucionado.
* Si el contenido del curso es un proyecto que se carga con un archivo zip en Learning Manager y si ese archivo zip contiene rutas de carpeta, como Zip>carpeta>contenido, este tipo de contenido no se admitía. Este problema se ha solucionado.

**Aplicación para tabletas**

* Cuando un usuario intentaba descargar los archivos de recursos de un curso en la aplicación de Android de Learning Manager, los archivos de recursos no se podían descargar. Este problema se ha solucionado.
* Al consumir un curso con el reproductor Fluidic, cuando un usuario graba una nota e intenta descargarla del curso más adelante, no se puede descargar. Este problema se ha solucionado.

+++

+++Actualización 2

Fecha de publicación: 28 de septiembre de 2015

### Mejoras {#Enhancements-18}

**Crear cursos utilizando módulos**

* La aplicación Learning Manager admite la carga de contenido SCORM aunque la versión no se mencione en el archivo manifest.xml. De forma predeterminada, la versión se considera 1.2.
* Al cargar contenido de cursos de Captivate con más de 500 MB, el contenido no se reproducía en el reproductor Fluidic. Como parte de la Actualización 2, el límite de tamaño se ha cambiado a 800 MB.

**Factura**

* En la función de administrador, al comprar una suscripción con tarjeta de crédito, el usuario puede elegir el primer pedido a partir de 10 alumnos. Los alumnos mínimos necesarios para el primer pedido se han reducido de 100 a 10.

**Registro de usuarios**

* Se ha proporcionado un vínculo URL para crear Adobe ID en el correo electrónico de bienvenida recibido por los alumnos después de su registro.

**Añadir usuarios**

* En la función de administrador, la adición de usuarios mediante la opción de carga de CSV directamente desde la cuenta de Exavault no funcionaba para algunos clientes. Este problema se ha solucionado.

### Problemas resueltos {#Issuesfixed-20}

**Planes y programas de aprendizaje**

* Los alumnos se pueden inscribir automáticamente en el mismo programa de aprendizaje como parte de varios planes de aprendizaje. Anteriormente, había algunas excepciones a este flujo de trabajo. Este problema se ha solucionado.

**Ver tabla de clasificación e insignias**

* En la función de alumno, después de realizar un curso que contiene una insignia, la imagen de la insignia no aparecía en el mapa de insignias del tablero del alumno ni en el archivo descargado. Este problema se ha solucionado.

**Aplicación para tabletas**

* Aparece una ventana emergente para indicar la disponibilidad de la aplicación del alumno cuando la URL de la aplicación se abre en un navegador en un dispositivo Android.

**Otras correcciones**

* Se ha resuelto un problema con la creación de cuentas de usuario debido a la compatibilidad con el almacenamiento de red de Akamai.
* Se ha resuelto un problema relacionado con la carga de contenido de SCORM 1.2 que contenía un archivo zip con varias carpetas.

+++
