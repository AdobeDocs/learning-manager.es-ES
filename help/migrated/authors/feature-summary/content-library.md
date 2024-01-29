---
description: Aprenda a crear contenido para alinearlo con cursos como contenido con ritmo personalizado.
jcr-language: en_us
title: Biblioteca de contenido
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '3113'
ht-degree: 0%

---



# Biblioteca de contenido

Aprenda a crear contenido para alinearlo con cursos como contenido con ritmo personalizado.

## Biblioteca de contenido {#contentlibrary}

El contenido es el elemento básico de un curso. Los autores crean una biblioteca de contenido que se puede alinear a los cursos como contenido con ritmo personalizado. Solo los autores tienen acceso a esta biblioteca de contenido.

## Tipos de contenido admitidos {#supported}

Puede cargar contenido interactivo y estático en la biblioteca.

La tabla siguiente muestra el tipo de archivo interactivo y estático que puede cargar en la biblioteca.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Contenido interactivo</b></p></td>
   <td>
    <p><b>Tipo de contenido</b></p></td>
   <td>
    <p><b>Extensiones</b></p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p></p>
    <ul>
     <li>SCORM 1.2</li>
     <li>SCORM 2004</li>
     <li>AICC</li>
     <li>TinCan</li>
    </ul>
    <p></p></td>
   <td>
    <p>cremallera</p></td>
  </tr>
  <tr>
   <td>
    <p><b>Contenido estático</b></p></td>
   <td>
    <p><b>Tipo de contenido</b></p></td>
   <td>
    <p><b>Extensiones</b></p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>Vídeo</p></td>
   <td>
    <p>mp4, wmv, 3gp, 3g2, 3gp2, asf, avi, f4v h264, mpe, mpeg, mpg, mpg2, m4v, mov, wmv</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>Audio</p></td>
   <td>
    <p>mp3, wav, aac, m4a, wma, vorbis, pcm, eac3, amr, ac3</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>PDF</p></td>
   <td>
    <p>pdf</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS PowerPoint</p></td>
   <td>
    <p>pptx, ppt</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS Word</p></td>
   <td>
    <p>docx, doc</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS Excel</p></td>
   <td>
    <p>xlsx, xls</p></td>
  </tr>
 </tbody>
</table>

## Añadir nuevo contenido en la biblioteca {#addnewcontentinthelibrary}

Como se ha mencionado en la sección anterior, puede agregar contenido interactivo y estático en la biblioteca.

## Añadir contenido estático {#addstaticcontent}

1. Haga clic en Biblioteca de contenido en el panel izquierdo después de iniciar sesión como autor y hacer clic en Agregar.

   Como alternativa, puede hacer clic en Crear contenido en la página Introducción.

1. En el campo Nombre, especifique un nombre para el contenido que desea cargar.
1. En el campo Descripción , escriba la descripción del contenido. Asegúrese de que la descripción que desea introducir es significativa. El límite de caracteres es de 400 caracteres.
1. Para agregar el contenido, haga clic en Agregar archivo de contenido y cargue el archivo de recursos. Cuando se agrega contenido para varios idiomas, no se puede combinar contenido estático e interactivo en un solo grupo. O todo el contenido de todas las configuraciones regionales debe ser estático o todo el contenido debe ser interactivo.

   Si desea reemplazar el contenido, puede reemplazar un contenido estático por otro diferente. Lo mismo se aplica al contenido interactivo.

1. En el campo Duración, puede introducir el tiempo esperado que un alumno dedicaría a este módulo. La duración es en minutos.

   El tiempo de aprendizaje empleado por el alumno se calcula en función de la duración especificada si el alumno ha marcado un curso como completado. Si el alumno consume el contenido del reproductor, el tiempo dedicado a él se añade al tiempo dedicado a aprendizaje. Si el tiempo de contenido real es menor que la duración especificada, no ocurre nada, ya que el reproductor siempre respeta el tiempo de contenido para la visualización.

1. En el campo Etiquetas de contenido , introduzca las etiquetas del contenido cargado para que se pueda detectar el contenido.

   Un autor puede utilizar estas etiquetas para buscar el contenido al añadir el contenido al curso.

### Versiones {#versioning}

La biblioteca de contenido también mantiene las versiones de los contenidos cargados. Si realiza algún cambio en el contenido, por ejemplo, una presentación de PowerPoint, y vuelve a cargar el PPT en la biblioteca, el número de versión se incrementa en uno. Esto le ayuda a realizar un seguimiento de los cambios en el contenido.

## Añadir contenido interactivo {#addinteractivecontent}

1. Haga clic en Biblioteca de contenido en el panel izquierdo después de iniciar sesión como autor y hacer clic en Agregar.

   Como alternativa, puede hacer clic en Crear contenido en la página Introducción.

1. En el campo Nombre, especifique un nombre para el contenido que desea cargar.
1. En el campo Descripción , escriba la descripción del contenido. Asegúrese de que la descripción que desea introducir es significativa. El límite de caracteres es de 245 caracteres.
1. Para agregar el contenido, haga clic en Agregar archivo de contenido y cargue el archivo de recursos. Cuando se agrega contenido para varios idiomas, no se puede combinar contenido estático e interactivo en un solo grupo. O todo el contenido de todas las configuraciones regionales debe ser estático o todo el contenido debe ser interactivo.

* [Tipos de archivo compatibles](content-library.md#supported)*

  El contenido interactivo puede ser un proyecto publicado por SCORM, AICC o un Captivate. El archivo debe ser un archivo zip.

  También puede añadir contenido de HTML generado a partir de Captivate, Presenter o Presenter Video Express.

[Tipos de archivo compatibles](content-library.md#supported)

1. Learning Manager admite subtítulos para contenido de vídeo cargado en Learning Manager. Ahora, los autores pueden cargar el archivo que contiene los subtítulos, junto con el archivo de vídeo.

   A continuación, los alumnos pueden ver los subtítulos durante la reproducción del módulo de vídeo.

   El formato admitido es  [Pistas de texto de vídeo web (WebVTT)](https://www.w3.org/TR/webvtt1/).

   La compatibilidad con los subtítulos está disponible para el contenido de vídeo cargado en la biblioteca de contenido de Learning Manager.

   Como autor, cuando cargue contenido de vídeo o audio, también puede cargar el archivo .vtt que contiene los subtítulos.

   A continuación, los subtítulos aparecen en el reproductor Fluidic. Los subtítulos también son compatibles con [Estándares WCAG2.0](https://www.w3.org/TR/WCAG20/).

   Al añadir contenido de vídeo a la biblioteca, también puede añadir el archivo vtt, que **debe** ser un archivo válido.

   ![](assets/webvtt.png)

   *Agregar un archivo webvtt*

   El archivo VTT cargado corresponde a la versión existente del contenido. Por lo tanto, el archivo WebVTT cargado no se vincula a la versión anterior del contenido.

   En caso de que esté creando el contenido en diferentes idiomas, puede cargar un archivo WebVTT diferente para cada idioma. Los alumnos podrán ver los subtítulos correspondientes al idioma seleccionado durante la reproducción.

   >[!NOTE]
   >
   >   Un archivo VTT admite un idioma. Para admitir varios idiomas, cargue varios archivos de vídeo para cada idioma del contenido y, a continuación, cargue el archivo VTT correspondiente para cada archivo de vídeo.

   Como autor, cada vez que cambie el contenido, el vídeo o el audio, Learning Manager le solicitará un nuevo archivo vtt.

   Después de añadir este contenido a un curso y previsualizarlo como alumno, puede ver los subtítulos en el vídeo.

   En el reproductor, active el botón CC del reproductor Fluidic para mostrar u ocultar los subtítulos.

   La misma vista está presente en el **aplicación del alumno** así como en **Vista previa como alumno**.

   Cuando usted **agregar, actualizar o eliminar** en el archivo vtt, recibirá una notificación.
La compatibilidad con WebVTT no está disponible para:

   1. Anuncios de vídeo.
   1. Vídeo reproducido en el contenido de aprendizaje electrónico. Esto se controla mediante el contenido.
   1. Vídeo cargado en Aprendizaje social.
   1. Vídeo creado en la aplicación de escritorio de Learning Manager.
   1. Contenido de vídeo creado mediante el proceso de migración.
   1. Reproducción de vídeo en la aplicación móvil en modo sin conexión.

1. En el campo Duración, puede introducir el tiempo esperado que un alumno dedicaría a este módulo. La duración es en minutos.
1. En el campo Etiquetas de contenido , introduzca las etiquetas del contenido cargado para que se pueda detectar el contenido.

### Compatibilidad con catálogos compartidos

Si una cuenta de vendedor comparte un catálogo que contiene los cursos y estos contienen los módulos, el audio o el vídeo con los subtítulos, los cursos deben tener el mismo comportamiento en la cuenta del comprador.

La propagación de módulos debe funcionar correctamente de la cuenta de vendedor a la del comprador. Esto puede incluir: editar/eliminar/añadir el archivo vtt en el módulo.

Una vez que haya cargado el contenido, puede ver una notificación haciendo clic en el icono de campana en la esquina superior derecha de la página. Cada vez que modifique un contenido y lo vuelva a cargar, recibirá una notificación. Si realiza los cambios, solo usted recibirá la notificación, no otros autores.

## Crear una prueba

Cree evaluaciones en Adobe Learning Manager con la nueva herramienta de creación de pruebas en la página Biblioteca de contenido. Las evaluaciones creadas pasan a formar parte de la biblioteca de contenido y se pueden añadir a una carpeta &quot;pública&quot; para reutilizar el curso.

1. Seleccione Biblioteca de contenido en el panel izquierdo.
1. En la esquina superior derecha de la pantalla, seleccione **Agregar > Prueba**.
1. En la página Crear prueba, escriba el nombre y la descripción de la prueba.
1. En la sección Contenido de la prueba, seleccione **Añadir pregunta de prueba**.
1. En el cuadro de diálogo Pregunta de prueba, seleccione el tipo de pregunta. Hay tres tipos de preguntas:
   * Pregunta de opción múltiple
   * True o false
   * Rellene el espacio en blanco
1. Introduzca la pregunta y seleccione la respuesta correcta.
1. Establezca los puntos para la prueba.
1. Si desea que la pregunta se responda correctamente para aprobar la prueba, seleccione la casilla de verificación **Obligatoriamente responder correctamente para aprobar la prueba**.
1. Seleccionar **Guardar y cerrar**.
1. Introduzca los puntos para aprobar la prueba en el **Criterios de aprobación** campo.
1. Si desea que un alumno vea una respuesta correcta, active el botón deslizante **Mostrar respuestas correctas** a los alumnos después de la prueba.
1. Si desea que las preguntas y las respuestas aparezcan de forma aleatoria, active los botones deslizantes:
   * Aleatorizar orden de preguntas
   * Aleatorizar orden de opción de respuesta
1. Especifique una carpeta para añadir la prueba y hacer que la prueba esté disponible para todos los autores.
1. En la **Duración** , especifique el tiempo que el alumno debe dedicar a la prueba.
1. Especifique una etiqueta de la lista de etiquetas ya creadas.
1. Añade un logotipo y un fondo a la prueba.
1. En la esquina superior derecha de la página, seleccione **Publicar**.

La prueba se añade a la biblioteca de contenido. Como cualquier contenido de la biblioteca de contenido, puede retirar una prueba y, a continuación, eliminarla.


## Añadir a carpeta {#add-folder}

Después de que un administrador cree las carpetas de contenido, usted, como autor, puede cargar contenido en una carpeta de contenido, de modo que el contenido solo esté visible para usted o para un grupo seleccionado de autores de la cuenta. También puede hacer público el contenido y hacerlo visible para todos los autores de la cuenta.

**Uso de ejemplo**

Por ejemplo, las agencias desean mantener un control total del contenido y alguien que pasa por alto el contenido debe tener acceso a todo el contenido. Al mismo tiempo, los creadores de contenido de las agencias deben tener acceso solo a su propio contenido y, en algunos casos, al contenido de otra persona.

La biblioteca de contenido con contenido existente (es decir, contenido cargado antes de configurar las carpetas de contenido) se define como **Carpeta pública**. Esta carpeta no se puede retirar ni eliminar. El contenido que forma parte de la carpeta pública está accesible para todos los tipos de autores. Una vez configuradas las carpetas de contenido, los autores estándar y personalizados deben seleccionar la carpeta en la que se debe colocar el contenido al cargar contenido nuevo.

>[!NOTE]
>
>Las carpetas públicas y privadas se excluyen mutuamente. Esto significa que el contenido **no** se asociarán a la carpeta pública y a la carpeta privada al mismo tiempo. Se puede asociar a una carpeta pública, **o** se puede asociar a una o varias carpetas privadas en cualquier momento.

Al añadir contenido, puede elegir la carpeta en la que se incluirá este.

![](assets/add-to-content-folder.png)

*Añadir contenido a una carpeta*

Si elige **Público**, el contenido estará visible para todos los autores. Todo el contenido que existiera en la cuenta y que no forme parte de ninguna carpeta se incluirá en la carpeta pública de forma predeterminada.

Tenga en cuenta que las carpetas de contenido son simplemente compartimentos virtuales para vincular el contenido. En el caso de que un contenido se coloque en dos carpetas, significa que el archivo de contenido siempre es un único archivo pero está vinculado a varias carpetas. Por lo tanto, en caso de que el contenido lo actualice el autor-personalizado-1 que tiene acceso a la carpeta-personalizada-1, el mismo contenido actualizado también se reflejará en la carpeta-personalizada-2 a la que tiene acceso el autor-personalizado-2.

En la biblioteca de contenido, hay dos opciones para administrar las carpetas de contenido:

**Todas las carpetas**

Es una lista que muestra todas las carpetas creadas en la cuenta.

![](assets/list-of-all-folders.png)

*Ver todas las carpetas*

**Todos los autores**

Es una lista que muestra los autores que han creado contenido y lo han cargado en la biblioteca.

![](assets/list-of-all-authors.png)

*Ver todos los autores*

Esto está disponible **solo** cuando un administrador crea una carpeta nueva.

## Mover contenido a una carpeta {#movecontenttofolder}

Para mover el contenido de una carpeta pública a cualquier carpeta privada:

1. Seleccionar **Público** de la carpeta **Todas las carpetas** lista desplegable.

   ![](assets/list-of-public-folders.png)

   *Ver todo el contenido cargado*

1. Elija el contenido que desea mover a una carpeta. A continuación, haga clic **[!UICONTROL Acciones]** > **[!UICONTROL Organizar contenido]** > **[!UICONTROL Mover contenido a la carpeta]**.

   ![](assets/move-content-to-folder.png)

   *Mover el contenido seleccionado a la carpeta*

1. Elija la carpeta a la que desea mover el contenido. Haga clic en **[!UICONTROL Mover]**.

## Copiar contenido en la carpeta {#copycontenttofolder}

Copiar una carpeta significa que estaría agregando una etiqueta a la carpeta. La operación de copia no creará copias de contenido, sino que solo agregará una asociación con las carpetas especificadas.

![](assets/copy-content-to-folder.png)

*Copiar una carpeta*

## Desvincular carpeta {#unlinkfolder}

Desvincular significa quitar el contenido de la carpeta seleccionada.

El contenido se puede desvincular de una carpeta especificada **SOLO** si también está asociado a otras carpetas. Si el contenido que se va a desvincular solo está asociado a una carpeta, es recomendable utilizar la operación MOVER.

>[!NOTE]
>
>El menú Organizar, en Acciones, está desactivado inicialmente. Para utilizarlo, primero debe seleccionar una carpeta en la lista desplegable de carpetas.

![](assets/unlink-a-folder.png)

*Desvincular una carpeta*

## Añadir contenido para diferentes idiomas {#addcontentfordifferentlanguages}

1. Para añadir el contenido para diferentes idiomas, haga clic en el **Añadir nuevo idioma** y elija los idiomas correspondientes. Con este enfoque, puede añadir compatibilidad multilingüe para su contenido.

   ![](assets/add-new-languagetab.png)

   *Añadir nuevo idioma a un contenido*

1. Repita el proceso de carga de contenido para los nuevos idiomas.
1. Si desea quitar un idioma, haga clic en la ficha Agregar nuevo idioma y desactive la selección.

   Una vez que haya realizado los cambios, haga clic en Guardar. En la biblioteca, el nuevo contenido ahora está disponible para su consumo.

## Definir criterios de finalización {#setcompletioncriteria}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Contenido estático</b></p></td>
   <td>
    <p><b>Contenido interactivo</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Solo puede definir el <b>Finalización</b> Criterios para el contenido de las siguientes opciones:</p>
    <ul>
     <li>Al iniciar contenido</li>
     <li>Basado en el porcentaje mínimo requerido</li>
    </ul></td>
   <td>
    <p>Puede definir ambos <b>Finalización</b> y <b>Correcto</b> criterios para el contenido de las siguientes opciones:</p>
    <ul>
     <li>Al iniciar contenido</li>
     <li>Basado en el porcentaje mínimo requerido</li>
     <li>Prueba superada o intentos de opciones</li>
    </ul>
    <p><b>NOTA:</b> Solo se puede editar el contenido del HTML de Captivate, Presenter Video Express o Presenter.</p></td>
  </tr>
 </tbody>
</table>

Después de agregar el contenido, puede modificar los criterios de finalización del contenido.

En Learning Manager, se otorgan insignias y aptitudes en función de los criterios de éxito y finalización. Si el alumno ha completado un curso, pero no lo ha superado con éxito, no recibe la insignia ni la aptitud correspondientes al objeto de aprendizaje.

Por ejemplo, si ha utilizado Adobe Captivate para crear el curso y establecer los parámetros de aprendizaje en el cuadro de diálogo Preferencias, la misma configuración se migra a Learning Manager en las opciones de Criterios de finalización.

En la sección Criterios de finalización, puede definir las opciones que se indican a continuación:

**Al Iniciar Contenido:** Si activa esta opción, definirá los criterios de finalización del contenido cuando un alumno lo abra.

**Según el porcentaje mínimo requerido:** Establezca un valor como porcentaje mínimo del consumo del alumno. Por ejemplo, si establece el porcentaje en 50, el alumno puede consumir el 50 % del contenido y seguir cumpliendo los criterios de finalización.

**Prueba:** Elija uno de los siguientes criterios:

* **Prueba superada:** El estado se comunica como Completado solo si un alumno supera la prueba.
* **Prueba intentada:** El estado se indica como Completado si los alumnos intentan realizar la prueba, independientemente de si la aprueban o la suspenden.
* **Prueba superada o límite alcanzado:** El estado se comunica como Completado si los alumnos aprueban la prueba o han realizado todos los intentos. Por ejemplo, si el número de intentos definido en el curso es dos, y:

   * Si los alumnos realizan el primer intento y aprueban, el estado se notifica como Completado y Aprobado.
   * Si los alumnos realizan el primer intento y fallan, el estado se notifica como Incompleto y Fallido , ya que el límite de intentos sigue sin alcanzarse.
   * Si los alumnos vuelven a realizar la prueba y suspenden, el estado se indica como Completado y Suspendido.
   * Si los alumnos vuelven a intentar la prueba y la aprueban, el estado se indica como Completado y Aprobado.

## Definir criterios de éxito {#setsuccesscriteria}

Del mismo modo, puede definir los criterios de éxito del curso. Un criterio de éxito indica que el rendimiento de un alumno es Aprobado o Suspendido. Si ha creado un curso en Captivate, puede establecer los criterios de éxito del curso en el cuadro de diálogo Preferencias, como se muestra a continuación:

Por ejemplo, ha cargado un módulo que contiene una prueba. Ahora, ha establecido los criterios de finalización de ese módulo en Al iniciar el contenido y los criterios de éxito en Prueba superada.

Si el alumno ha iniciado el curso y ha suspendido la prueba, el curso se marcará como Completado; sin embargo, los criterios de éxito solo se cumplirán cuando el alumno apruebe la prueba.

## Opciones de filtro de contenido {#contentfilteroptions}

### Ordenar por fecha {#sortaccordingtodate}

Organice el contenido según cuándo se modificó por última vez. Puede ordenar el contenido en orden ascendente o descendente.

![](assets/according-to-date.png)

*Ordenar contenido por fecha*

### Ordenar según el uso {#sortaccordingtousage}

Organice el contenido según si se está utilizando en algún curso. En el menú desplegable Tipo, elija En uso o No utilizado.

![](assets/according-to-usage.png)

*Ordenar contenido por uso*

## Buscar contenido {#searchforcontent}

En la biblioteca de contenido, puede buscar contenido eligiendo el nombre del contenido o las etiquetas asociadas al mismo.

En la barra de búsqueda, introduzca el nombre de un curso o una etiqueta y podrá ver las recomendaciones.

<!--![](assets/search-bar.png)-->

## Retirar contenido {#retirecontent}

Una vez que publique un contenido, no podrá eliminarlo. Primero debe retirar el contenido. Al marcar un contenido como Retirado, el contenido ya no está visible para los alumnos. El contenido también se mueve a la sección Retirado . También puede mover el contenido al estado publicado más adelante.

Para retirar contenido, siga estos pasos:

* En Biblioteca de contenido, seleccione el contenido que desea retirar.
* Seleccione Acción > Retirar.

El contenido que se utiliza en cualquier objeto de aprendizaje no se ve afectado. Los alumnos pueden seguir accediendo al contenido.

## Volver a publicar contenido retirado {#republishretiredcontent}

Una vez que retire un contenido, puede volver a publicarlo y hacer que aparezca en la lista Publicados. Por ejemplo, si ha retirado la versión 1 de un contenido y desea reemplazarla por la versión 2, puede mover la versión 1.pptx, por ejemplo, a la lista Publicados, y actualizar el archivo con la versión 2.pptx. El nuevo archivo estará disponible para su consumo en varios cursos.

Para volver a publicar el contenido retirado:

1. Vaya a la **Retirado** y seleccione el contenido que desea volver a publicar.
1. Seleccionar **Acción** > **Volver a publicar**.

El contenido aparecerá ahora en la lista Publicados.

## Eliminar contenido {#deletecontent}

Una vez que haya retirado un contenido, puede eliminarlo.

* Vaya a la pestaña Retirado y seleccione el contenido que desee eliminar.
* Seleccione Acción > Eliminar.

Tenga en cuenta que los cursos existentes que utilizan el contenido, que se eliminan de la biblioteca de contenido, seguirán utilizando el contenido.

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++ ¿Cómo cargar contenido SCORM en Adobe Learning Manager?

Cree un curso de aprendizaje electrónico compatible con SCORM en cualquier herramienta, como Adobe Captivate, y publique el contenido como un archivo zip. A continuación, en Learning Manager, cargue el archivo zip en el catálogo y establezca los criterios de finalización y éxito.
+++

+++¿Cómo cargo una nueva versión del mismo contenido en el Administrador de aprendizaje?

En Learning Manager, la biblioteca de contenido también mantiene las versiones del contenido cargado. Si realiza algún cambio en el contenido, por ejemplo, una presentación de PowerPoint, y vuelve a cargar la presentación en la biblioteca, el número de versión se incrementa en uno. Esto le ayuda a realizar un seguimiento de los cambios en el contenido. Se puede aplicar una nueva versión del contenido a todos los objetos de aprendizaje simultáneamente, o aplicar actualizaciones individuales para cada curso.
+++

+++Cómo editar los detalles de un curso en otro idioma?
Después de agregar uno o varios idiomas, como se describe en una sección anterior, haga clic en cada ficha de idioma y, a continuación, agregue o edite la información del curso.

&lt;!--![](assets/edit-course-language.png)--->
+++
