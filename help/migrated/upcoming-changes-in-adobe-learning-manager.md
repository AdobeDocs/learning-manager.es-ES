---
title: Novedades de la versión de abril de 2026 de Adobe Learning Manager
description: Obtenga más información sobre las nuevas funciones, mejoras y actualizaciones importantes de la versión de abril de 2026 de Adobe Learning Manager.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 47d49f4bbb81db88635b2c115768e15a3818e153
workflow-type: tm+mt
source-wordcount: '20175'
ht-degree: 0%

---

# Actualizaciones en Adobe Learning Manager

>[!IMPORTANT]
>
>Las funciones de esta versión están disponibles en versión beta. La funcionalidad y el comportamiento pueden cambiar antes de la disponibilidad general. Comparta comentarios a través de sus canales habituales de soporte de Adobe.


Este documento resume las nuevas funciones, mejoras y actualizaciones de la versión de abril de 2026 de Adobe Learning Manager. Utilícelo para planificar cambios para su organización y conocer lo que está disponible para alumnos, administradores y autores.

**Para alumnos:** El reproductor Fluidic muestra ahora el nombre del siguiente módulo y un botón para salir. El idioma del reproductor se puede establecer mediante LTI para una experiencia coherente en todas las plataformas. El contenido de Captivate incluye una tabla de contenido unificada, marcas de finalización a nivel de diapositiva y exportaciones de notas fiables. Hay disponible compatibilidad con varios idiomas para las ayudas de trabajo, las preguntas de la lista de comprobación y las pistas de texto de vídeo (VTT). El Asistente de IA ayuda a los alumnos a obtener respuestas en la experiencia de aprendizaje.

**Para administradores y autores:** El conector de Zoom admite varias sesiones VILT simultáneas. Los cursos compartidos en cuentas de igual a igual muestran el autor real en lugar de &quot;Autor externo&quot;. Los administradores pueden restringir cuándo se pueden iniciar los módulos. Las fechas de caducidad de los objetos de aprendizaje se muestran en las API del alumno. Los módulos de lista de comprobación admiten la puntuación ponderada, el texto de pregunta multilingüe y los comentarios opcionales del revisor. Los certificados personalizados ofrecen un editor de arrastrar y soltar con campos dinámicos y fondos generados por IA. Experience Builder sin conexión te permite crear páginas de aprendizaje públicas sin necesidad de iniciar sesión.

**Para instructores:** Genera códigos QR para la inscripción de instancias y la asistencia a sesiones. Agregue comentarios o sugerencias durante la evaluación de la lista de comprobación.

**Informes y análisis:** El contenido de SCORM ahora puede informar de varios intentos de prueba en los informes de nivel 2. El cálculo del tiempo dedicado al aprendizaje mejora en las transcripciones de alumnos. Se actualizan los informes de transcripciones de aprendizaje para administradores. Hay disponibles mejoras de búsqueda avanzadas.

## Navegación del reproductor Fluidic: muestra el nombre del siguiente módulo

### Información general

Esta mejora ya se incluyó en la versión de noviembre de 2025 de Adobe Learning Manager.

La acción &quot;Siguiente&quot; en el reproductor indica lo que ocurrirá al hacer clic mostrando el nombre del siguiente módulo o curso y señalando explícitamente cuando el alumno está a punto de salir del reproductor.

### Novedades...

**&quot;Next Module: {ModuleName}&quot; etiqueta en el reproductor**

El icono Siguiente del reproductor Fluidic muestra ahora el nombre del siguiente módulo del curso. Por ejemplo, Módulo siguiente: Lección 2 - Introducción.

Esto se aplica siempre que el alumno pase de un módulo al siguiente en el mismo curso.

**Borrar acción de salida en el último módulo**

Cuando el alumno se encuentra en el último módulo de un curso, aparece un nuevo botón de acción Salir , que indica que al hacer clic en él se cerrará el reproductor y se volverá al contexto del curso.

**Comportamiento interactivo para contenido móvil y de PDF**

En ventanas gráficas más pequeñas (por ejemplo, de ~320 px de ancho), la etiqueta Siguiente se puede acortar u ocultar, mostrando solo el icono, para evitar superposiciones con controles de PDF.

Para los módulos de PDF, el reproductor ajusta los controles a una línea independiente, de modo que las etiquetas de navegación y los controles del PDF no interfieran entre sí.

**Administrador actualizado > Marca > Vista previa del reproductor**

La vista previa del reproductor en Administración > Marca ahora refleja la nueva etiqueta, por ejemplo, Módulo siguiente: Lección 2. Esto permite a los administradores ver el comportamiento de navegación actualizado.

### Principales ventajas

**Navegación más clara para los alumnos**

Los alumnos ya no tienen que adivinar lo que pasará cuando seleccionen &quot;Siguiente&quot;. La etiqueta especifica claramente lo que viene después, ya sea un módulo o un curso. Esta reducción de la ambigüedad ayuda a aliviar las dudas y la confusión, especialmente en grandes audiencias del sector de la educación del cliente, donde muchos alumnos pueden no estar familiarizados con las interfaces del LMS.

**Tasas más altas de finalización de cursos**

Si se indica claramente el siguiente paso (siguiente módulo: {ModuleName}) y se agrega una acción de salida distinta para el módulo final, se reduce la probabilidad de que los alumnos abandonen el curso o pasen por alto el último paso de finalización.

**Experiencia de usuario más predecible en todos los dispositivos**

Las etiquetas actualizadas se alinean con el comportamiento Siguiente o Anterior y los iconos en el escritorio, la tableta y el móvil. Las restricciones de diseño se respetan en todos los dispositivos y flujos de PDF para que los controles puedan utilizarse y ser accesibles.

Esto es especialmente importante para las implementaciones descentralizadas en las que el reproductor Fluidic está integrado en una experiencia de aprendizaje personalizada.

### Casos de uso

**Portales educativos para clientes y socios (descentralizados o integrados en AEM)**

Cuentas que utilizan Adobe Learning Manager en una configuración totalmente descentralizada que dirigen a los alumnos desde canales de marketing externos. Estos alumnos:

* A menudo, el contenido de vídeo se consume en secuencias largas.

* Se espera una experiencia de estilo curricular donde el sistema indique claramente el próximo episodio/módulo.

En estos entornos, la etiqueta **Next Module:{ModuleName}**:

* Refuerza la naturaleza guiada del viaje.

* Minimiza la entrega entre módulos.

**Cursos de cumplimiento y certificación con módulos ordenados**

En escenarios regulados o con alto grado de cumplimiento:

* Los alumnos deben completar una secuencia estricta de módulos.

* Los autores suelen deshabilitar el índice para evitar omitirlo.

Aquí, mostrando **Siguiente módulo:{ModuleName}**:

* Confirma a los alumnos que siguen la secuencia correcta.

* Hace menos probable que malinterpreten la acción Siguiente y salgan antes de tiempo.

**Rutas de aprendizaje en las que los cursos se siguen entre sí**

Donde las rutas de aprendizaje o equivalentes encadenan varios cursos. Esto resulta útil a la hora de crear secuencias de estilo curricular para grandes audiencias.

**Consumo que da prioridad a los dispositivos móviles**

Para los alumnos que utilizan principalmente teléfonos o tabletas:

* Las etiquetas actualizadas y el comportamiento interactivo garantizan que la navegación sea comprensible sin tener que depender de pequeños iconos de cierre o controles ocultos.

* Esto es importante para la educación del cliente, los trabajadores de los pequeños encargos o los alumnos de primera línea que pueden acceder al contenido en sesiones cortas en dispositivos móviles.

## Conector de zoom: crear varias sesiones de zoom simultáneas

### Información general

La actualización del conector de Zoom mejora la forma en que Adobe Learning Manager administra el aprendizaje virtual dirigido por instructor (VILT). Antes, los usuarios solo podían crear una sesión de Zoom cada vez. Con la nueva actualización, los administradores y los autores pueden programar varias sesiones de Zoom al mismo tiempo mediante la integración estándar.

### Novedades...

#### Compatibilidad con varias sesiones de zoom simultáneas a través del conector

* El conector de zoom ahora permite crear más de una sesión VILT en la misma fecha/hora desde ALM.

* La lógica de programación ya no aplica una restricción de &quot;reunión de Zoom única a la vez&quot; en el nivel de cuenta/conector.

* Los administradores y los autores pueden configurar sesiones VILT superpuestas (por ejemplo, aulas regionales, pistas paralelas o sesiones repetidas para diferentes grupos de socios) sin soluciones alternativas.

#### Las reuniones se crean utilizando la identidad de zoom del instructor (no del superadministrador de Zoom)

Para admitir reuniones simultáneas de forma segura, el conector se ha actualizado para que:

* Las reuniones de Zoom ahora se crean utilizando la dirección de correo electrónico del instructor, en lugar del correo electrónico del superadministrador de Zoom.

* La cuenta Zoom de cada instructor puede alojar sus propias reuniones en paralelo con otros instructores, sujeto a los límites del plan Zoom existente.

**Nota**:

* Solo se admite un instructor por reunión.

* Si el correo electrónico de un instructor se actualiza posteriormente en Adobe Learning Manager, las reuniones existentes permanecen asociadas al correo electrónico original utilizado en la creación.

#### Se acabó el pegado manual de URL de zoom para sesiones simultáneas

Anteriormente, cuando una segunda o tercera sesión de Zoom tenía que ejecutarse al mismo tiempo:

* Los autores tenían que crear manualmente reuniones de Zoom fuera de ALM y, a continuación, pegar la URL de unión de Zoom en la configuración de la instancia del curso.

* Esto era propenso a errores y no se beneficiaba de las funciones del conector como el seguimiento de la asistencia.

Con el conector actualizado:

* Todas las sesiones se pueden crear directamente desde la interfaz de usuario de ALM mediante el conector de Zoom, incluso si se superponen en el tiempo.

* El ciclo de vida de la sesión (creación/cancelación) sigue gestionándose de forma centralizada mediante la integración.

### Principales ventajas

#### Mejor programación de VILT a escala

Ahora, las organizaciones pueden:

* Ejecute varias clases virtuales basadas en Zoom al mismo tiempo (por ejemplo, pistas paralelas en una conferencia virtual, cohortes regionales o sesiones de formación de socios independientes).

* Evite los cuellos de botella que antes obligaban a los administradores a serializar las sesiones o confiar en la gestión manual del zoom.

#### Menor sobrecarga de administrador y autor

La mejora elimina:

* Creación manual de reuniones de Zoom fuera de Adobe Learning Manager.

* Copie y pegue las direcciones URL de zoom en cada instancia del curso para sesiones superpuestas.

* Riesgo de vínculos mal configurados, reuniones incorrectas adjuntas o seguimiento de asistencia perdida.

Los administradores y los autores pueden administrar todas las sesiones de Zoom desde Adobe Learning Manager, utilizando flujos de trabajo conocidos.

#### Mejor alineación con las funciones de instructor y aprovisionamiento de Zoom

Al vincular reuniones a cuentas de zoom de instructores individuales:

* Cada instructor puede operar dentro de sus propios límites de licencia de Zoom.

* Las organizaciones pueden utilizar su modelo de aprovisionamiento de Zoom existente (una cuenta por instructor, por unidad de negocio, etc.) mientras se sigue integrando completamente con Adobe Learning Manager.

* Esto evita el cuello de botella de un solo punto que supone el uso de un usuario de Zoom superadministrador compartido en todas las sesiones.

### Casos de uso

#### Eventos y cumbres virtuales multipista

Los equipos de educación del cliente que organizan eventos grandes (por ejemplo, campamentos de inicio de productos, cumbres de partners o semanas de certificación) pueden:

* Configure varias sesiones basadas en zoom en la misma franja horaria (para diferentes pistas o temas).

* Administre todos ellos como módulos VILT en los cursos y rutas de aprendizaje de Adobe Learning Manager.

* Proporciona a los alumnos una experiencia unificada mientras el conector gestiona toda la creación de reuniones de Zoom subyacente.

#### Formación global para partners y clientes

Las organizaciones que capacitan a clientes y socios de todas las regiones pueden:

* Ejecute sesiones de Zoom independientes para EMEA, APAC y América en horas solapadas para que coincidan con las horas de trabajo locales.

* Evite forzar una única franja horaria global o la configuración manual del zoom para cohortes adicionales.

#### Habilitación interna

Los equipos de capacitación interna (ventas, asistencia, etc.) pueden:

* Programe sesiones de incorporación paralelas o sesiones en grupo basadas en funciones (por ejemplo, salas de zoom independientes para desarrolladores, administradores y responsables de departamento empresariales) en ALM.

* Mantenga todas las sesiones dentro del modelo VILT de ALM para fines de informes y cumplimiento, en lugar de realizar una transición parcial a reuniones de Zoom no administradas.

## Mostrar el autor original de los cursos compartidos en cuentas de igual a igual

### Información general

Cuando se comparte un curso a través del catálogo en una cuenta de igual a igual, Adobe Learning Manager etiqueta actualmente al autor como &quot;autor externo&quot; en las vistas de alumno, administrador y autor de la cuenta receptora. Esto puede crear problemas para los alumnos y los administradores, especialmente en las grandes empresas, ya que se hace difícil identificar y ponerse en contacto con el propietario del contenido adecuado cuando surgen problemas o preguntas.

La mejora garantiza que la información del autor se conserve y aparezca en los cursos compartidos en cuentas de igual a igual, en lugar de sustituirse por un marcador de posición genérico.

### Novedades...

Mostrar el nombre del autor real de los cursos compartidos en cuentas de igual a igual

Para los cursos compartidos a través de catálogos externos o de igual a igual, el nombre del autor original de la cuenta de origen ahora se muestra en la cuenta de destino en lugar de &quot;Autor externo&quot;.

Esto se aplica a:

* Aplicación del alumno (tarjeta del curso o detalles del curso).

* Vistas de administrador y de autor al previsualizar como alumno.

### Principales ventajas

#### Visibilidad directa del propietario del contenido compartido

Los alumnos y administradores de cuentas de igual a igual ahora pueden:

* Averigüe quién es el autor del curso, incluso cuando se adquiere a través de un catálogo compartido.

* Evita la etiqueta genérica y poco útil de &quot;autor externo&quot;.

#### Experiencia más coherente de varios inquilinos y cuentas de igual a igual

Para clientes que ejecuten escenarios de varios inquilinos o de empresas extendidas:

* El mismo curso se muestra con una marca de autor coherente en todas las cuentas.

* La experiencia del alumno se alinea con las expectativas de la cuenta principal (por ejemplo, ver el nombre del autor de la cuenta de origen en lugar de &quot;Autor externo&quot;).

### Casos de uso

#### Grandes empresas con cuentas de igual a igual

La empresa utiliza ALM con:

* Una cuenta principal que posee los cursos canónicos, y

* Cuentas de igual a igual que adquieren contenido mediante catálogos compartidos.

Los alumnos con cuentas de igual a igual deben saber qué equipo de la empresa ha creado un curso para enviar preguntas o sugerencias de mejora correctamente.

Con esta mejora:

* Los cursos compartidos ahora muestran el nombre correcto del autor de empresa en las cuentas de igual a igual.

* La carga de asistencia interna de la empresa se reduce porque los alumnos y los administradores locales saben con quién ponerse en contacto.

#### Uso compartido interno de varias unidades de negocio

Cuando una unidad empresarial gestiona el aprendizaje para otros:

* La unidad de negocio propietaria se puede identificar en el campo de autor en todas las cuentas de consumo.

* Los administradores de aprendizaje y desarrollo locales pueden ver rápidamente si un curso se mantiene de forma local o por otra unidad de negocio, y colaborar en consecuencia.

## Mostrar la fecha de caducidad del objeto de aprendizaje (retirada automática) en las API del alumno

### Información general

Esta mejora hace que la fecha de retirada automática de un objeto de aprendizaje (LO) esté disponible directamente a través de las API de Adobe Learning Manager orientadas al alumno. Cuando un curso, una ruta de aprendizaje o una certificación se configuran con una fecha de caducidad o de retirada automática, esa información ahora forma parte de los datos del objeto de aprendizaje devueltos por los puntos finales clave del alumno.

### Novedades...

#### Nuevo campo de caducidad/retirada automática en las API de objetos de aprendizaje

* Las API de objetos de aprendizaje (por ejemplo, los puntos finales que devuelven objetos de aprendizaje a la experiencia del alumno y a plataformas externas) ahora incluyen la fecha de caducidad del objeto de aprendizaje (la fecha de retirada automática configurada para ese objeto de aprendizaje).

* Este campo se devuelve como parte de la entidad LO en respuestas como:

   * Obtener objeto de aprendizaje (detalles de objeto de aprendizaje).

   * Los datos de objetos de aprendizaje se utilizan para rellenar el inicio del alumno, el catálogo y los resultados de búsqueda.

* El campo complementa la fecha límite de finalización existente que ya existe en el nivel de instancia; el nuevo campo es específicamente la fecha de retirada automática en el nivel de objeto de aprendizaje.

#### Disponibilidad en experiencias de alumno respaldadas por búsquedas

Dado que la fecha de caducidad se muestra como parte de la representación de objetos de aprendizaje respaldados por búsqueda, ahora está disponible en cualquier lugar que utilice ALM o una plataforma externa:

* API de búsqueda o

* catálogos basados en búsquedas y sugerencias para crear vistas de alumno.

**Ámbito y exclusiones**

La mejora solo se aplica a las API de alumno.

### Principales ventajas

#### Experiencia del alumno con detección de caducidad en LXP personalizados

Para las grandes y medianas empresas, su LXP personalizado ahora puede obtener información de caducidad de objetos de aprendizaje directamente de ALM, lo que les permite:

* Mostrar etiquetas &quot;Expirando en {date}&quot; o &quot;Expirando pronto&quot; en las tarjetas del curso y las páginas de detalles.

* Comunicarse con urgencia de forma más clara, para que los alumnos prioricen la formación que está a punto de jubilarse.

Esto es especialmente importante para el cumplimiento normativo o la formación sobre productos con plazos precisos, en la que los objetos de aprendizaje se actualizan con regularidad y las versiones anteriores se retiran.

#### Mejor orientación para los alumnos sobre los cursos de formación que deben realizar ahora

Al exponer la caducidad del objeto de aprendizaje, la experiencia del alumno puede:

* Resalta los cursos que aún son válidos frente a los que están a punto de retirarse.

* Ayude a los alumnos a evitar inscribirse en cursos de formación que ya no estarán disponibles o no serán válidos en un futuro próximo.

#### Coherencia con los datos existentes del plazo de finalización

Anteriormente, las API de alumno ya mostraban la fecha límite de finalización a nivel de instancia, pero no la fecha de retirada automática a nivel de objeto de aprendizaje. Con este cambio:

Están disponibles los siguientes aspectos de una formación:

* &quot;¿Para cuándo debo terminar esta instancia?&quot; (fecha límite de finalización).

* &quot;¿Hasta cuándo se ofrece esta formación?&quot; (fecha de retirada/caducidad automática).

### Casos de uso

#### Una empresa global con gestión estricta del ciclo de vida de los cursos

Las empresas que retiran y sustituyen regularmente los cursos (por ejemplo, actualizaciones normativas, de productos o de metodología) pueden:

* Evita la confusión del alumno sobre si un curso de formación se va a eliminar gradualmente.

* Orienta a los alumnos hacia las ofertas más actuales y de larga duración.

Ahora, sus portales personalizados y herramientas internas pueden leer la fecha de caducidad directamente desde ALM a través de las API del alumno.

#### Academias externas de clientes o socios

Para la educación de clientes y partners, las páginas y portales de marketing suelen enfatizar la formación actualizada.

Tener fechas de caducidad en la API de objetos de aprendizaje permite a los creadores de experiencias:

* Oculta o quita el énfasis al contenido que esté cerca de la retirada.

* Crea campañas de &quot;Última oportunidad para completar&quot;.

## Compatibilidad multilingüe para ayudas de trabajo

### Información general

La mejora extiende el modelo de localización de Adobe Learning Manager a las ayudas de trabajo, lo que permite a los autores adjuntar diferentes archivos de contenido por idioma a una sola ayuda de trabajo. En lugar de crear ayudas de trabajo independientes para cada idioma, los autores ahora pueden administrar todas las versiones localizadas como una ayuda de trabajo lógica.

### Novedades...

#### Carga de contenido específico del idioma para las ayudas de trabajo

Los autores pueden adjuntar diferentes archivos por idioma admitido a una sola ayuda de trabajo, como cursos y otros objetos de aprendizaje.

La experiencia de creación/edición de ayudas de trabajo ahora admite:

* Seleccionar un idioma.

* Cargar el archivo específico de idioma para ese idioma en la misma entidad de ayuda de trabajo.

#### Gestión coherente del idioma en la IU del reproductor y del alumno

El reproductor Fluidic se ha actualizado para que, cuando un alumno abra una ayuda de trabajo, se muestre la variante de contenido correspondiente al idioma del alumno (cuando esté disponible).

Los administradores y los autores pueden ver las ayudas de trabajo como objetos individuales con variantes de idioma, en lugar de elementos independientes por idioma.

### Principales ventajas

#### Ayuda de trabajo única para todos los idiomas

Los autores pueden evitar crear ayudas de trabajo independientes por idioma.

Todas las variantes de idioma de la misma ayuda de trabajo (por ejemplo, un procedimiento, SOP, PDF de lista de comprobación o guía de referencia) se pueden administrar en un solo lugar.

#### Mejor experiencia para alumnos de todo el mundo

Los alumnos ven automáticamente la ayuda de trabajo en su idioma preferido, lo que significa que hay:

* Menos confusión sobre qué versión abrir.

* Menos riesgo de acceder a copias fuera de la configuración regional o obsoletas.

Esto resulta especialmente útil en organizaciones multilingües en las que el mismo proceso o documentación del producto debe estar disponible en varios idiomas.

### Casos de uso

#### Despliegue global del contenido de referencia

Una empresa debe proporcionar ayudas de trabajo en varios idiomas a los alumnos de todo el mundo, por ejemplo:

* Hojas de referencia de productos.

* Procesar listas de comprobación.

* Libros de estrategias de soporte

En lugar de crear ayudas de trabajo independientes como &quot;Inicio rápido del producto - ES&quot;, &quot;Inicio rápido del producto - DE&quot;, &quot;Inicio rápido del producto - JP&quot;, etc., pueden crear una ayuda de trabajo, adjuntar archivos localizados para cada idioma y permitir que ALM proporcione la versión correcta a cada alumno en función de la configuración de idioma.

#### Documentación dirigida al cliente o al socio para varios mercados

Para las academias de clientes y socios, las ayudas de trabajo pueden incluir:

* Hojas de trucos de productos

* Guías de integración

* Flujos de trabajo de asistencia

Con ayudas de trabajo en varios idiomas:

* Cada socio ve la versión localizada sin tener que elegir entre las entradas específicas del idioma.

* Los equipos de marketing y capacitación pueden administrar una ayuda de trabajo por tema en todas las configuraciones regionales.

## Definir restricción en la hora de inicio del módulo

### Información general

La mejora permite a los autores y administradores de Adobe Learning Manager definir una ventana de tiempo durante la cual los alumnos pueden iniciar un módulo. Fuera de la ventana de inicio/finalización configurada, el módulo permanece visible en la estructura del curso, pero los alumnos no pueden iniciarlo.

Esta capacidad es fundamental para los usuarios que necesitan un control más estricto sobre cuándo está disponible determinado contenido o que deben dejar de iniciarse, por ejemplo, en programas cronometrados, formación basada en cohortes o ejercicios sensibles al tiempo.

### Novedades...

Los autores ahora pueden configurar, en el nivel de módulo de un curso, una fecha/hora de inicio y una fecha/hora de finalización que determine cuándo se permite a los alumnos iniciar ese módulo. En esta ventana, el módulo se comporta de la forma habitual; antes de la hora de inicio o después de la hora de finalización, el alumno ve el módulo en el esquema del curso, pero no puede iniciarlo.

La configuración aparece en la interfaz de usuario de creación del curso como controles de programación adicionales para tipos de módulos específicos, como contenido con ritmo personalizado, pruebas o actividades. Los administradores pueden utilizar estos controles para crear módulos que se abran en fases o para evitar inicios tardíos en programas en los que se debe consumir contenido dentro de un período de tiempo definido.

#### Principales ventajas

La principal ventaja es la capacidad de controlar cuándo se puede acceder a los módulos. Los equipos de formación pueden sincronizar la disponibilidad de los módulos con eventos reales, como los lanzamientos de nuevos productos, los plazos reglamentarios y los programas internos. Esto garantiza que los alumnos completen el contenido de los requisitos previos antes de poder acceder a los módulos posteriores.

Por ejemplo, la cohorte 1 puede acceder al módulo 2 solo en la semana 2, mientras que el módulo 3 permanecerá bloqueado hasta la semana 3, lo que elimina la necesidad de ocultar y mostrar manualmente el contenido o crear versiones de cursos independientes.

Esto mejora la experiencia del alumno: en lugar de módulos opuestos a los que se puede acceder técnicamente, pero que no deberían estar en ese momento (o que ya deberían estar completados), los alumnos ven una estructura de curso en la que los módulos que se les permite iniciar están claramente alineados con el programa previsto.

#### Casos de uso

* **Programa de habilitación basado en cohorte**: En este programa, cada semana se abre un nuevo módulo. El contenido de la Semana 1 está disponible inmediatamente, mientras que la Semana 2 está visible, pero no se puede iniciar hasta una fecha especificada. La semana 3 sigue el mismo proceso de control. Los alumnos pueden ver la ruta de aprendizaje completa, pero el sistema controla cuándo pueden empezar realmente cada paso.

* **Formación de productos o campañas con plazos determinados**: los equipos de marketing o de productos pueden crear un módulo de formación al que solo se debe acceder mientras una campaña está activa o cuando una versión específica de un producto aún está disponible. Esta ventana de inicio designada garantiza que los alumnos no inicien un módulo sobre una versión del producto interrumpida después de la hora de finalización especificada.

* **Entornos de evaluación o examen**: las organizaciones pueden abrir un módulo (como una prueba) para una ventana corta y bien definida (por ejemplo, &quot;puede comenzar el examen en cualquier momento entre 9:00 y 12:00 en una fecha determinada&quot;). Los alumnos no pueden comenzar el examen fuera de esa ventana, lo que permite una programación equitativa en las zonas horarias y cohortes.

## Controlar el idioma del reproductor mediante un parámetro LTI personalizado

### Información general

La mejora permite que las plataformas externas que utilizan LTI (interoperabilidad de herramientas de aprendizaje) especifiquen el idioma del contenido de Adobe Learning Manager en el momento del inicio. En lugar de depender del alumno para cambiar el idioma en el reproductor Fluidic, el consumidor de LTI puede enviar un código de idioma a través de un parámetro personalizado de LTI. Adobe Learning Manager utilizará este código para seleccionar la variante de idioma adecuada.

### Novedades...

Las plataformas externas que actúan como consumidores de LTI ahora pueden pasar un parámetro de idioma personalizado (y la configuración de reproductor relacionada) al iniciar contenido de ALM. ALM lee este parámetro y:

* Define el idioma del reproductor en consecuencia.

* Inicia la variante de idioma correspondiente del módulo cuando se configura contenido en varios idiomas.

Esto significa que un alumno que selecciona francés por primera vez en la plataforma externa verá el reproductor y el módulo ALM iniciarse directamente en francés, sin tener que ajustar nada dentro de ALM.

La mejora también se adapta a escenarios en los que la plataforma externa trata a ALM como un reproductor de contenido descentralizado. Por ejemplo, permite ocultar los elementos de exploración y la tabla de contenido enviando parámetros personalizados adicionales para ajustar determinados valores de la interfaz de usuario. Estos ajustes funcionan junto con el parámetro de idioma, lo que permite a la plataforma externa proporcionar una experiencia fluida y de marca mientras se sigue utilizando ALM para la reproducción y el seguimiento.

### Principales ventajas

* **Experiencia de idioma coherente en todos los sistemas**: Cuando un alumno selecciona un idioma en el portal externo, esa elección se refleja inmediatamente en ALM. Esto garantiza que los alumnos no tengan ninguna discrepancia entre el idioma del portal y el curso. Como resultado, no tendrán que buscar un cambio de idioma dentro del reproductor.

* **Informes específicos del idioma**: En su plataforma, la selección de idioma es coherente con ALM, lo que mejora la precisión de sus análisis y el seguimiento de los alumnos. Esta alineación también admite configuraciones en las que los controles de idioma propios de ALM se deshabilitan u ocultan intencionadamente en el reproductor Fluidic para cursos específicos. En estos casos, la plataforma externa sirve como única fuente de verdad para el lenguaje.

### Casos de uso

* Un caso de uso significativo es el de las grandes empresas que utilizan integraciones basadas en ITL. Los alumnos primero se inscriben y seleccionan un idioma en la plataforma. Luego lanzan sesiones de entrenamiento de ALM a través de LTI. Con esta mejora, cuando un alumno selecciona español, el módulo ALM se abre automáticamente en español. Esto significa que los alumnos no necesitan ajustar la configuración de idioma en ALM. Además, los informes basados en el idioma siguen siendo coherentes con lo que los alumnos ven y experimentan en ALM.

* Otra aplicación es la entrega de experiencias de curso descentralizadas en un portal de clientes o socios. En esta configuración, el portal puede incrustar contenido de ALM mediante un iframe, mientras que toda la experiencia de usuario de navegación e idioma (UX) se administra fuera de ALM. Utilizando parámetros personalizados de LTI, el portal puede garantizar que el reproductor ALM se muestre en el idioma correcto y que los elementos innecesarios de la interfaz de usuario (como la tabla de contenido y los botones de navegación) estén ocultos. Esto permite a los alumnos percibir una sola aplicación coherente en lugar de una colección inconexa de herramientas.

* Esto resulta beneficioso para las organizaciones que imparten formación a gran escala en varios idiomas mediante otro LMS o plataforma de aprendizaje. Pueden estandarizar el uso de esa plataforma para administrar perfiles de alumnos, seleccionar configuraciones regionales y presentar catálogos. Mientras tanto, ALM sirve como un motor confiable de contenido y seguimiento, respetando las preferencias de idioma e interacciones del usuario especificadas por el sistema externo durante cada lanzamiento de LTI.

## Ponderación de preguntas de lista de comprobación para evaluaciones de instructores

### Información general

La mejora introduce listas de comprobación ponderadas, lo que permite a los instructores y responsables evaluar a los alumnos mediante escalas graduadas y puntuaciones totales, en lugar de tratar cada pregunta de la lista de comprobación como igual. El objetivo es facilitar la creación de listas de comprobación mediante la aplicación de evaluaciones ponderadas de las preguntas, lo que permite reflejar la importancia relativa de las distintas acciones o aptitudes en una sola lista de comprobación.

### Novedades...

Las listas de comprobación admiten los siguientes tipos:

1. Sí/No
El comportamiento sigue siendo el mismo que en la actualidad: cada pregunta es Sí/No y los criterios para aprobar se basan en el número de respuestas afirmativas.

2. Preguntas del mismo peso

   * Las preguntas se marcan en una escala numérica (de 0 a 10 de forma predeterminada), donde:

      * Los valores máximos y mínimos de la escala se pueden personalizar en el nivel de lista de comprobación.

      * La escala ahora puede comenzar en 0 (la puntuación mínima anterior era 1).

   * Todas las preguntas comparten la misma puntuación máxima, por lo que la lista de comprobación se comporta como una escala graduada uniforme para cada pregunta.

3. Preguntas de peso diferente

   * Cada pregunta tiene su propia puntuación máxima (peso).

   * Los criterios para aprobar dependen del porcentaje de la puntuación total posible que el alumno obtenga en la lista de comprobación (por ejemplo, &quot;aprobar si el alumno alcanza ≥ 70 % de la puntuación total disponible&quot;).

Para todos los tipos de listas de comprobación:

* El **Revisor** (instructor o responsable) evalúa al alumno según el tipo de lista de comprobación configurada:

   * Seleccionando Sí/No.

   * Seleccione las puntuaciones en la escala definida.

* El informe **Checklist** se ha actualizado para incluir preguntas con diferente grosor:

   * Puntuación máxima para cada pregunta.

   * Puntuación obtenida por cada alumno para esa pregunta.

Esto permite analizar el rendimiento global y el rendimiento específico de la pregunta en función de las ponderaciones previstas.

### Principales ventajas

* **Evaluaciones más ricas y realistas**: Los instructores pueden reflejar las prioridades del mundo real dando más puntos a los comportamientos críticos y menos a los menores, mientras siguen utilizando un flujo de trabajo de lista de comprobación adecuado para tareas observadas o prácticas.

* **Aprobado/suspenso basado en la puntuación total**: las evaluaciones se pueden basar en la puntuación porcentual global, no solo en cuántas preguntas pasan un umbral, sino también en cómo se alinean más estrechamente con los esquemas típicos de competencia o gradación.

* **Mejor presentación de informes**: Los informes de lista de comprobación actualizados exponen la puntuación máxima y la puntuación obtenida por pregunta, lo que permite a los propietarios del programa y a los equipos de calidad identificar puntos débiles específicos y perfeccionar la orientación de formación o evaluación.

### Casos de uso

* **Evaluaciones de habilidades empresariales**: Los ingenieros se evalúan mediante listas de comprobación prácticas basadas en escenarios en las que determinados pasos de diagnóstico o comunicación deben tener más peso que los pasos cosméticos o de bajo riesgo. Las preguntas ponderadas y los criterios de aprobación de la puntuación total hacen que estas evaluaciones sean más creíbles y predictivas del rendimiento del mundo real.

* **Observaciones de seguridad y cumplimiento**: en el sector sanitario, de fabricación o de servicios in situ, se pueden asignar puntuaciones máximas más altas a los pasos de seguridad críticos, lo que garantiza que la falta de una acción crítica de seguridad tenga un impacto mayor en la puntuación total que la falta de un paso de procedimiento menor.

* **Orientación y calibración**: con el valor máximo y las puntuaciones obtenidas por pregunta en el informe, los responsables pueden ver exactamente dónde los alumnos obtienen un rendimiento inferior y calibran a los instructores sobre cómo puntuar de forma coherente.

## Compatibilidad con varios idiomas para preguntas de lista de comprobación

### Información general

La mejora introduce la compatibilidad con varios idiomas para las preguntas de la lista de comprobación, lo que permite a los revisores evaluar y puntuar las listas de comprobación en el idioma que prefieran. Esta función es especialmente útil en las regiones multilingües y en las implementaciones globales, ya que permite a los autores crear preguntas de lista de comprobación localizadas para cada idioma de contenido admitido, al tiempo que mantiene un único módulo de lista de comprobación y un proceso de evaluación coherente.

En Adobe Learning Manager hoy:

* Todos los módulos orientados al alumno (SCORM, PDF, HTML, etc.) se puede proporcionar en varios idiomas de contenido, lo que permite a los alumnos elegir el idioma que prefieran.

* En un módulo de lista de comprobación, los revisores (instructores/responsables) evalúan a los alumnos en función de las preguntas definidas en dicha lista de comprobación.

### Novedades...

**Creación**

* Los autores ahora pueden añadir preguntas de lista de comprobación en todos los idiomas seleccionados en el nivel del curso.

* Para cada lista de comprobación:

   * Se espera que el autor proporcione un texto de pregunta equivalente en todos los idiomas de contenido en los que exista el curso.

   * Los autores son responsables de garantizar que el significado de cada pregunta sea coherente en todos los idiomas.

**Experiencia de revisión**

* Los revisores verán las preguntas de la lista de comprobación y la interfaz de usuario de evaluación en el idioma de contenido seleccionado.

* Cuando una pregunta se evalúa en un idioma:

   * La evaluación (puntuación, Sí/No, estado) es lógicamente la misma en todos los idiomas. Es una única lista de comprobación con varias vistas de idioma, no listas de comprobación independientes por idioma.

**Informes**

El informe Lista de comprobación mostrará el texto de la pregunta en el idioma de contenido del usuario:

* Un administrador o revisor que ejecute el informe en cada idioma verá los nombres de las preguntas traducidas de ese idioma.

* Las respuestas y puntuaciones subyacentes siguen siendo las mismas; solo se traducen las etiquetas de las preguntas.

### Principales ventajas

* **Mejor experiencia de revisión**: Los revisores pueden trabajar completamente en su propio idioma, leyendo preguntas y registrando evaluaciones sin barreras lingüísticas.

* **Alineación normativa y de políticas**: En las regiones con requisitos de igualdad lingüística (por ejemplo, holandés/francés en Bélgica), las listas de verificación ahora pueden cumplir los mismos estándares que otros materiales de aprendizaje, lo que reduce el riesgo de cumplimiento.

* **Lógica de evaluación coherente**: Aunque el texto está localizado, la evaluación y la puntuación se comparten en todos los idiomas, lo que garantiza que los resultados sean comparables y se administren de forma centralizada.

### Casos de uso

* Las franquicias multinacionales que operan en varios idiomas pueden implementar un solo curso y una lista de comprobación, a la vez que ofrecen experiencias de revisor localizadas en cada territorio.

* Cualquier empresa global con instructores locales (por ejemplo, EMEA, LATAM, APAC) puede hacer que los revisores trabajen en su idioma local mientras comparten el mismo diseño de lista de comprobación global y la misma generación de informes.

## Lista de comprobación con capacidad de comentario para el revisor

### Información general

La mejora introduce una función de comentarios para las evaluaciones de la lista de comprobación, que permite a los revisores, como instructores y gestores, proporcionar comentarios cualitativos junto con las puntuaciones numéricas. Estos comentarios se pueden hacer visibles para los alumnos cuando sea necesario.

El objetivo es apoyar las evaluaciones basadas en listas de comprobación donde los comentarios de los mentores son tan cruciales como el resultado numérico. Esto incluye destacar fortalezas específicas, áreas de mejora o proporcionar contexto para la puntuación dada.

Hoy en día, los revisores pueden:

* Evalúa una lista de comprobación para cada alumno, pregunta por pregunta.

* Vea los resultados y vuelva a evaluar a los alumnos que han suspendido.

En escenarios reales, como la aviación, los instructores de campo evalúan a los agentes de planta y al personal del aeropuerto. Del mismo modo, los instructores y mentores de las pequeñas y medianas empresas (PYMES) suelen utilizar listas de comprobación para evaluar el desempeño laboral. Sin embargo, estas listas de comprobación no suelen incluir una sección estructurada para capturar comentarios narrativos relacionados con la evaluación.

### Novedades...

#### Opciones de creación

Los autores pueden configurar cada lista de comprobación para:

* Habilitar o deshabilitar la función de comentarios para los revisores.

* Decida si el nombre del revisor debe mostrarse a los alumnos junto con los comentarios.

Esto permite a las organizaciones adaptar la visibilidad de los comentarios a sus requisitos culturales y de privacidad.

#### Experiencia del revisor

Cuando los comentarios están activados:

* Los revisores (instructores o responsables) pueden añadir comentarios opcionales al evaluar una lista de comprobación.

* Pueden elegir si los comentarios son visibles para los alumnos, en función de la configuración de la lista de comprobación.

Si vuelven a evaluar a un alumno, pueden actualizar o cambiar los comentarios para reflejar la evaluación más reciente.

#### Informes y notificaciones

* El informe Lista de comprobación obtiene una nueva columna para los comentarios del revisor, que captura el comentario proporcionado durante la evaluación.

* Los alumnos reciben notificaciones (en la plataforma y por correo electrónico) cada vez que se realiza una evaluación de la lista de comprobación. Estas notificaciones incluyen:

   * El comentario y

   * El nombre del revisor, si se configuraron para ser visibles.

Esto garantiza que los comentarios no solo se almacenen, sino que se muestren de forma activa a los alumnos.

### Principales ventajas

* **Comentarios más ricos y parecidos a los de un entrenador**: Las puntuaciones numéricas se complementan con comentarios contextuales, lo que hace que las listas de comprobación sean una herramienta más eficaz para el entrenamiento, no solo para el cumplimiento.

* **Trazabilidad y auditabilidad**: Las organizaciones obtienen un registro persistente de quién evalúa quién, cuándo y qué dicen, lo cual es importante en entornos regulados y roles de alto riesgo.

* **Mejor participación del alumno**: Los alumnos reciben instrucciones claras vinculadas a evaluaciones específicas, lo que mejora su comprensión de las expectativas y los pasos posteriores.

### Casos de uso

* Las organizaciones con entornos regulados pueden utilizar comentarios para documentar el juicio clínico o los comentarios sobre procedimientos del personal que se observa sobre el terreno.

* Las organizaciones de aviación y de asistencia en tierra pueden adjuntar notas detalladas sobre el rendimiento operativo, las prácticas de seguridad y el comportamiento de cara al cliente, lo que convierte una lista de comprobación en una herramienta de información estructurada.

* En la orientación y la evaluación de expertos en la materia, los instructores pueden captar observaciones matizadas que no encajarían en una puntuación por sí solas, por ejemplo, &quot;se ha gestionado bien la escalada, pero es necesario mejorar la gestión del tiempo&quot; o &quot;un excelente flujo de solución de problemas; no se ha realizado un paso de documentación&quot;.

## Informes de pruebas e intentos múltiples en el nivel de contenido

### Información general

>[!IMPORTANT]
>
>Tenga en cuenta que la función solo estará disponible después de habilitarla en la cuenta. Póngase en contacto con el soporte ALM.


Actualmente, ALM admite varios intentos en el nivel de LMS mediante la función Varios intentos de prueba (MQA) :

* Los autores pueden configurar intentos en el nivel del curso (aplicado a todos los módulos de prueba del curso) o en el nivel del módulo (por módulo de prueba).

* Los intentos pueden ser:

   * Un número específico (por ejemplo, 3 intentos), o

   * Intentos infinitos, controlados a nivel de LMS.

* Cuando un alumno consume un módulo a través del reproductor Fluidic y luego cierra el reproductor o completa el módulo, esa sesión se trata como un único intento de LMS.

* Cada intento de LMS se captura en el informe de prueba de L2 como una nueva fila.

Sin embargo, si el propio archivo de contenido (por ejemplo, una prueba de Articulate SCORM) implementa su propia lógica de varios intentos, el informe de prueba de L2 de ALM no distingue ni realiza un seguimiento correcto de esos intentos internos.

Esta mejora introduce el seguimiento de varios intentos en el nivel de contenido de los cuestionarios, lo que permite a Adobe Learning Manager capturar con precisión cada intento dentro del propio contenido en el informe de cuestionarios de L2. Se ha diseñado para situaciones en las que la herramienta de creación de contenido (como Articulate SCORM) gestiona los intentos de las pruebas de forma independiente. Con esta función, los intentos se reflejan correctamente en los informes de ALM sin depender de la configuración de Intento múltiple de prueba (MQA) en el nivel de LMS.

### Novedades...

#### Indicador de autor para los intentos de contenido

* Al cargar contenido en la biblioteca de contenido, los autores ahora pueden indicar que un archivo de contenido específico tiene varios intentos incrustados.

* Se trata de una configuración por contenido que indica a ALM que trate los intentos definidos dentro del contenido como la fuente de confianza.

#### Comportamiento del curso/módulo

Cuando dicho contenido se utiliza en un curso:

* El módulo derivará sus intentos del contenido, no del LMS MQA.

* Los alumnos solo verán un intento en el nivel de LMS:

   * En la vista de módulo y en la vista de información general del curso no aparece el botón &quot;Reintentar&quot; del LMS para ese módulo.

   * El control de intentos (por ejemplo, reintentos dentro de la prueba) se rige por el propio contenido.

#### Informes

El informe de prueba de L2 trata cada intento de nivel de contenido como una fila de intentos independiente:

* Cada intento de prueba interno configurado en el contenido aparece como su propia fila en el informe de prueba de L2, como en la representación actual de los intentos en el nivel de LMS.

* El formato de cada fila sigue siendo el mismo que el de las filas de varios intentos existentes en los informes de L2 (las mismas columnas, estructura y semántica).

* Esto proporciona una experiencia de creación de informes coherente:

   * Tanto si los intentos están controlados por LMS MQA o por el contenido, el informe de prueba de L2 muestra una fila por intento.

#### Principales ventajas

* Historial de intentos preciso para pruebas SCORM en las que los intentos se controlan internamente mediante herramientas como Articulate, sin forzar la configuración de MQA en el nivel de LMS.

* Experiencia de alumno más limpia: para los intentos controlados por contenido, los alumnos ven una única ranura en el nivel de LMS y no necesitan interactuar con los controles de reintento de LMS; todos los reintentos se gestionan dentro de la interfaz de usuario de la prueba que ya conocen.

* Arquitectura flexible: los usuarios pueden elegir si ALM MQA o los intentos a nivel de contenido deben impulsar el comportamiento por módulo, en función de cómo se haya creado su contenido y de cómo prefieran administrar los intentos.

* Modelo de informes coherente: los consumidores descendentes del informe de prueba de L2 pueden tratar cada fila como &quot;un intento&quot;, independientemente del lugar en el que se origine la lógica del intento.

#### Casos de uso

* Las organizaciones que utilizan Articulate SCORM pueden mantener una lógica de cuestionario autocontenida en el paquete SCORM mientras obtienen informes precisos de intentos en ALM sin configuración de LMS adicional.

* Las organizaciones que utilizan contenido SCORM proporcionado por el proveedor pueden evitar la necesidad de modificar o implementar una lógica de intentos e intentos adicional con MQA en el nivel de LMS.

## Códigos QR de instructor para la inscripción de instancias y la asistencia a sesiones

### Información general

Esta mejora añade la capacidad de los instructores de generar códigos QR por sí mismos para:

* Inscripción de instancias de cursos,

* Asistencia a la sesión, o

* Inscripción + asistencia juntos

a nivel de sesión. Se ha diseñado para situaciones en las que los alumnos entran en una clase física o híbrida y requieren una opción rápida de autoservicio para inscribirse y registrar su asistencia mediante un código QR.

### Novedades...

#### Códigos QR generados por instructor

* Los instructores pueden generar códigos QR en el nivel de sesión para:

   * Inscribir en la instancia: los alumnos pueden inscribirse en la instancia que incluya la sesión actual.

   * Marcar la asistencia a la sesión: los alumnos analizan durante o después de la sesión para registrar la asistencia a esa sesión específica.

   * Inscribir en instancia + marcar asistencia a la sesión : un QR combinado para los participantes que aún no se han inscrito y necesitan que se marque su asistencia en un solo paso.

* Los instructores pueden exportar los códigos QR que necesitan en función del escenario (inscripción, asistencia o ambas cosas).

#### Empaquetado de código QR

El PDF de código QR exportado incluye:

* Nombre del curso

* Nombre de la instancia

* Nombre de la sesión

Esto facilita a los instructores y coordinadores identificar e imprimir el código QR correcto para cada sesión.

### Principales ventajas

* **Autonomía del instructor**: los instructores ya no tienen que esperar a que los administradores creen códigos QR. Pueden generarlas directamente para cada sesión, mejorando la agilidad y reduciendo los gastos de coordinación.

* **Mejor logística en el aula**: para audiencias que entran o se encuentran en el lugar (como trabajadores de campo, personal de planta o asistentes externos), los instructores pueden administrar la inscripción y la asistencia en el lugar mediante códigos QR.

* **Menor carga de trabajo de administración**: los equipos de administración pueden centrarse en la configuración y el control en lugar de gestionar las solicitudes de generación de código QR rutinarias para cada sesión.

### Casos de uso

* Las organizaciones que ejecutan grandes volúmenes de sesiones in situ (por ejemplo, formación sobre productos para profesionales) pueden permitir a los instructores imprimir códigos QR específicos de la sesión que inscriben y marcan la asistencia con una digitalización.

* En la formación en venta, fabricación y atención sanitaria, en la que los alumnos suelen unirse a las sesiones directamente desde la planta o sin preinscripción, se puede colocar un código QR de &quot;Inscripción + Asistencia&quot; en la puerta. Esto permite a los alumnos realizar autoservicio de inscripción y asistencia a través de sus teléfonos.

* Los eventos de formación para socios o clientes permiten que el formador in situ se adapte fácilmente a los cambios en la sala, sesiones adicionales o asistentes adicionales sin necesidad de consultar al administrador para obtener nuevos códigos QR.

## Mejoras en el reproductor Captivate y ALM

### Información general

Esta mejora mejora mejora la experiencia de reproducción de contenido de Adobe Captivate en el reproductor Adobe Learning Manager (ALM), especialmente tras los cambios recientes en la arquitectura de Captivate. El objetivo es permitir que los alumnos interactúen con los módulos de Captivate de forma nativa en ALM, al tiempo que se garantiza que la navegación, el seguimiento de la finalización y la toma de notas sean claros, coherentes y fiables.

### Novedades...

#### Experiencia unificada del índice

* En el lado izquierdo del reproductor solo se muestra el índice de ALM.

* El índice del propio Captivate se oculta cuando el módulo se reproduce dentro de ALM.

* Esto elimina la duplicación, garantiza una única fuente de confianza para la navegación y libera espacio en la pantalla.

#### Comentarios de finalización visual

* El índice ALM muestra marcas de graduación verdes (o señales visuales equivalentes) que indican la finalización del nivel de diapositiva.

* A medida que los alumnos avanzan por las diapositivas del Captivate, la tabla de contenido de ALM refleja las diapositivas que se han completado, en consonancia con las expectativas del alumno para los participantes en los cursos modernos.

#### Controles de progreso contextual

* Los controles del reproductor se adaptarán en función del tipo de diapositiva:

   * Para diapositivas de vídeo:

      * Mostrar una barra de progreso de tiempo, que refleje la reproducción de vídeo.

* Para diapositivas que no sean de vídeo:

   * Mostrar controles de navegación de diapositivas (diapositiva siguiente/anterior, etc.) en lugar de una barra de tiempo no funcional.

      * Esto evita mostrar controles irrelevantes o que no funcionan en determinados tipos de diapositivas.

#### Navegación simplificada

* La barra de navegación del módulo (ALM) y la barra de navegación del curso independientes se han combinado en una única barra intuitiva.

* Esta navegación unificada:

   * Diferencia claramente entre desplazarse por el módulo Captivate y volver al nivel curso/módulo.

   * Reduce la confusión causada por varias barras con fines superpuestos.

#### Vinculación de notas fiables

* Las notas se vinculan a números de diapositiva en lugar de a marcas de tiempo.

* Este cambio:

   * Corrige errores de exportación causados por marcas de tiempo incorrectas o que faltan.

   * Garantiza que las notas se puedan exportar de forma coherente como PDF, con una asignación fiable entre las notas y el contexto de la diapositiva al que pertenecen.

### Principales ventajas

* Experiencia más limpia en un solo reproductor: los alumnos interactúan con un índice y un modelo de navegación, lo que reduce la confusión y la carga cognitiva.

* Indicaciones precisas de finalización y progreso: Las marcas de nivel de diapositiva y los controles contextuales ayudan a los alumnos a comprender dónde se encuentran y qué queda.

* Toma de notas y exportaciones más fiables: al vincular notas a diapositivas en lugar de marcas de tiempo frágiles, los usuarios recuperan un flujo de trabajo fiable de notas al PDF, incluso con contenido de Captivate basado en diapositivas.

* Flujo de trabajo de autor preservado: los autores conservan la simplicidad de la publicación directa de Captivate en ALM, mientras que los alumnos obtienen una experiencia de reproducción moderna e integrada sin cargas de creación adicionales.

### Casos de uso

* Los programas de habilitación que dependen de Captivate para simulaciones interactivas pueden implementar contenido en ALM, lo que garantiza que la navegación, el seguimiento de la finalización y las notas funcionen de forma coherente para los alumnos.

* Las organizaciones que utilizan Captivate como su principal herramienta de creación de contenido pueden mantener la publicación en un clic y evitar la confusión de las dobles TDC y los controles no funcionales para los alumnos.

* Las organizaciones que dependen de notas exportadas desde contenido de Captivate en ALM (para orientación, cumplimiento o registros) pueden acceder a lo siguiente:

   * Las notas se vinculan correctamente a las diapositivas.

   * Los PDF se generan del modo esperado.

## Cálculo del tiempo de aprendizaje dedicado mejorado en transcripciones de alumnos

### Información general

Adobe Learning Manager ha revisado la forma en que calcula el tiempo de aprendizaje en transcripciones de alumnos en su versión de abril de 2026. Anteriormente, la lógica de informes podía provocar tiempos inexactos si los alumnos dejaban el reproductor abierto sin interactuar con el contenido, lo que provocaba discrepancias. El nuevo método ahora realiza un seguimiento del tiempo activo en función de la participación del usuario, específicamente cuando la pestaña está enfocada y cuando hay actividad del usuario. Este cambio da como resultado datos más precisos.

Esta actualización mejora los informes y los paneles, lo que ayuda a los administradores a garantizar mejor el cumplimiento normativo y realizar el seguimiento del progreso de los alumnos. Después de la versión, revise las transcripciones de alumnos para ver estas mejoras.

El método de cálculo actualizado se centra en la participación real, como el enfoque de pestaña activa y las interacciones recientes de los usuarios, lo que mejora la precisión de los informes de tiempo en las siguientes áreas:

* Transcripciones de alumnos (IU)
* Métricas de Admin Dashboard
* Informes de inscripción de cursos
* API y conectores

### Qué ha cambiado

La columna **Tiempo de aprendizaje empleado** en transcripciones de alumnos ahora usa una lógica mejorada para calcular el tiempo de forma más precisa. En lugar de simplemente hacer un seguimiento de los tiempos de apertura/cierre del reproductor, el sistema ahora distingue entre períodos activos y de inactividad en función de la participación del usuario.

* **Tiempo activo**: Tiempo en el que el alumno está involucrado de forma activa (por ejemplo, en la pestaña correcta, realizando acciones como desplazarse o ver vídeo).
* **Tiempo de inactividad**: Tiempo en el que el alumno no está involucrado (por ejemplo, cambio de tabulación, sin actividad durante más de 10 minutos), lo que se excluye del total.

Esto se aplica a la mayoría de los tipos de módulos, con excepciones para los módulos SCORM, Captivate y XAPI, que conservan la lógica original.

### Cómo funciona

El nuevo cálculo varía según el tipo de módulo:

* **Módulos de vídeo y audio**: Se activa cuando se reproduce el contenido, incluso si el alumno cambia a otra ficha. El foco de tabulación no es necesario para realizar el seguimiento del tiempo de reproducción.
* **Módulos estáticos (PDF, PPT, Excel, etc.)**: activos en la pestaña y realizando actividades (movimiento del ratón, desplazamiento, clic, entrada de teclado) en los últimos 10 minutos. Si no hay actividad durante 10 minutos, se pasa a ralentí.
* **SCORM y Captivate** conservan la lógica original de apertura/cierre.
* **xAPI** ahora usa detección de tiempo activo basada en pestañas, donde el tiempo se cuenta solo cuando la pestaña está activa. Tenga en cuenta que el contenido AICC **no es compatible**.
* **HTML, LTI y otro contenido**: Puede variar; compruebe la precisión de las transcripciones de alumnos.

El tiempo de inactividad se resta, lo que garantiza que solo se notifique el tiempo de participación real.

>[!NOTE]
>
>Si el portátil pasa al modo de suspensión, es posible que no se realice un seguimiento correcto del tiempo de aprendizaje. Esto se debe a que el seguimiento de la actividad se detiene mientras el sistema está en modo de suspensión y se reanuda sólo cuando se despierta el equipo portátil.


### Tabla de resumen

| **Tipo de módulo** | **Tiempo activo (contado)** | **Tiempo de inactividad (excluido)** |
| --- | --- | --- |
| **Vídeo / Audio** | Tiempo de reproducción | No iniciado; finalizado; pausado **\>10 min** |
| **Estático (PDF/PPT/DOC)** | Actividad **y** activas con el tabulador en los últimos **10 min** | No hay actividad **\>10 min**; ficha inactiva |
| **SCORM** | Tiempo informado por tiempo de ejecución de contenido | No se puede detectar el estado inactivo |
| **Captivate** | Temporización basada en diapositivas | No se puede detectar el estado inactivo |
| **xAPI** | Pestaña activa | Pestaña inactiva |
| **HTML** | Tiempo de apertura del reproductor con la pestaña activa | Pestaña inactiva |
| **Productor/Consumidor de LTI** | Si el contenido de LTI se reproduce dentro del reproductor de ALM (es decir, ALM consume contenido de LTI alojado en otro LMS que actúa como productor), se aplica esta lógica del tiempo empleado.<br><br>Sin embargo, si el contenido se reproduce fuera del LMS (es decir, el contenido se aloja en ALM, ALM es el productor, pero la reproducción se produce en un reproductor externo), esta parte de la lógica del cálculo de tiempo no se aplica.  <br>**Nota**: El consumidor de LTI no es compatible con Adobe Learning Manager. | Pestaña inactiva |

**Nota**:

* **Revisitas y sesiones paralelas**: Cuenta como activa cuando se cumplen las condiciones anteriores.
* **Todos los dispositivos, navegadores e idiomas**: incluido; el uso móvil sin conexión se agrega después de la sincronización.

### Ventajas del nuevo cálculo

* **Informes precisos**: Elimina los tiempos de espera de los jugadores desatendidos, lo que proporciona duraciones de aprendizaje realistas.
* **Mejor cumplimiento normativo**: Admite un seguimiento preciso de la formación obligatoria (por ejemplo, los requisitos mensuales de 5 horas de una empresa).
* **Paneles mejorados**: Los gráficos de actividad de los usuarios y los informes de tiempo empleado ahora reflejan la participación real.
* **Información del alumno**: ayuda a los administradores a identificar el progreso auténtico y a dirigirse a los alumnos desinteresados.

### Impacto de informes y análisis

* **Transcripciones de alumnos:** El &quot;tiempo de aprendizaje dedicado&quot; ahora refleja la **participación real**.
* **Panel de administración:** Las métricas que incluyen el tiempo (por ejemplo, mosaicos de &quot;tiempo empleado&quot; y tendencias) mostrarán valores **más bajos pero más realistas** en escenarios donde el tiempo de inactividad infló los resultados anteriormente.
* **Informes de inscripción de cursos:** Los campos relacionados con el tiempo adoptan el **nuevo cálculo** después del inicio.
* **Nota de comparación:** Dado que los datos históricos no se vuelven a calcular, los análisis de series temporales que abarcan la fecha de lanzamiento pueden mostrar un **cambio de paso**. Considera la anotación o segmentación por fecha en las herramientas de análisis.

### API y conectores

* **No hay cambios de esquema** en los extremos o campos existentes que informan del tiempo empleado.
* La **semántica de campos** se ha actualizado para reflejar el _cálculo de tiempo activo_ para las sesiones **después del inicio de la característica.**
* Los **conectores y exportaciones** que consumen tiempo en los campos recibirán automáticamente los valores actualizados en el futuro.

### Retrocompatibilidad y migración de datos

* **Sesiones históricas:** No recalculadas.
* **Nuevas sesiones:** Usa el cálculo de tiempo activo **new**.
* **Períodos mixtos:** Para auditorías o informes longitudinales, segmenta por **antes y después del inicio** para evitar interpretaciones erróneas.

### Limitaciones conocidas

* **El contenido interactivo** (SCORM/Captivate) sigue dependiendo de la temporización proporcionada por el contenido; no está disponible la detección de inactividad en el contenido.
* **El contenido basado en Iframe** (HTML/xAPI) limita la detección de interacciones granuladas; en su lugar, se usa el foco de tabulación.

### Preguntas frecuentes

**¿Esta actualización cambia los registros históricos?**

No. El cambio solo se aplica a las sesiones posteriores al inicio de la función.

**¿Cómo compruebo los cambios?**

Consulte las transcripciones de alumnos de los módulos recientes; compare los tiempos con las duraciones previstas.

**¿Afecta esto a todas las cuentas?**

Sí, es una actualización global para todas las cuentas de Adobe Learning Manager.

**¿Los alumnos deben realizar alguna acción?**

No. El cambio es automático y transparente para los alumnos.

**¿Qué sucede si los alumnos dejan contenido abierto?**

Ahora se excluye el tiempo de inactividad, lo que impide la generación de informes excesivos.

**¿Las sesiones de vídeo/audio se pausan automáticamente cuando la pestaña está inactiva?**

No. El comportamiento de la reproducción no cambia. El tiempo se excluye cuando está en pausa > 10 minutos o cuando no se reproduce activamente.

**¿Se reflejará la actividad móvil sin conexión?**

Sí. El uso sin conexión se incluye cuando el dispositivo se sincroniza.

**¿Qué debo hacer si mis paneles ahora muestran promedios más bajos?**

Esto se espera cuando el tiempo de inactividad haya inflado los resultados anteriormente. Anota los paneles y ajusta los destinos según sea necesario.

**¿Hay requisitos previos?**

Ninguno; el cambio es automático.

## Actualización de los informes de transcripciones de aprendizaje para administradores

Estamos actualizando los informes de transcripciones de aprendizaje (LT) para que los administradores puedan realizar mejor las evaluaciones basadas en listas de comprobación y recibir comentarios de los revisores.

## ¿Qué está cambiando?

### &#x200B;1. Cambio de nombre de columna en la transcripción de Admin Learning

Columna **Comentario de envío** existente en el aprendizaje de administración
La transcripción es:

1. **Se cambió el nombre a:** `Reviewer's remarks`

### Datos mostrados en esta columna:

* **Para módulos de envío:**
La columna sigue mostrando el comentario del envío (sin cambios de comportamiento).

* **Para módulos de lista de comprobación:**
La columna ahora muestra el comentario de evaluación (los comentarios del revisor de la lista de comprobación).

Este cambio se aplica a todos los orígenes de LT de administrador:

* LT descargado de la IU del administrador
* LT obtenido mediante la API de trabajos
* LT generado mediante conectores

Después de este cambio, la misma columna incluye: - Comentarios de envío para los módulos de envío

* Comentarios de evaluación para los módulos de lista de comprobación

Bajo el nuevo nombre de encabezado **Comentarios del revisor**.

### &#x200B;2. Nueva columna en exportaciones de transcripciones de aprendizaje basadas en conectores

Para transcripciones de aprendizaje exportadas mediante conectores:

* Al final del informe se agrega una nueva columna denominada **Comentarios del revisor**.
* Esta columna contiene los comentarios del revisor, alineados con el comportamiento descrito anteriormente:
   * Comentarios de envío para los módulos de envío
   * Comentarios de evaluación para los módulos de lista de comprobación

## Incidencia en las integraciones y automatizaciones existentes

Si utiliza informes de transcripciones de aprendizaje en integraciones personalizadas, automatizaciones o herramientas de creación de informes externas, revise los siguientes escenarios:

| Escenario | Consecuencias | Acción necesaria |
|----------|--------|----------------|
| Los campos de Admin LT se identifican por nombre de columna (por ejemplo, &quot;Enviar comentario&quot;) | El encabezado de columna cambia a las observaciones del revisor. | Sí. Actualice cualquier asignación o lógica que haga referencia al envío de comentarios para utilizar los comentarios del revisor. |
| Solo puede identificar los campos de Admin LT por posición de columna (según el índice) | La posición de esta columna sigue siendo la misma en Admin LT. | Normalmente no hay acción. Si su lógica no depende del texto del encabezado, no es necesario realizar ningún cambio en el administrador LT, solo cambie el nombre de la columna si actualmente se utiliza la columna &quot;Enviar comentarios&quot;. |
| Se utiliza LT exportado por conector y se basa en un recuento de columnas fijo o en una posición específica de la última columna | Se añade una nueva columna al final del informe. | Sí. Ajuste la lógica de análisis o validación para tener en cuenta una columna adicional al final del archivo. |
| Se utiliza LT exportado por conector y se asigna por nombre de columna | Hay disponible una nueva columna Comentarios del revisor. | Opcional. No es necesario realizar ningún cambio a menos que desee utilizar los nuevos datos de comentarios del revisor/lista de comprobación. |

**Qué debes hacer**

* Revise cualquier script, trabajo de ETL, tablero o integración que consuma informes de transcripciones de aprendizaje de administración.
* Si hace referencia al nombre de columna anterior _Enviar comentario_, actualice la configuración o el código para utilizar el nuevo nombre de columna Comentarios del revisor.
* Si utiliza exportaciones LT basadas en conectores y supone un número fijo de columnas o una última columna fija, actualice la lógica para controlar una columna adicional al final de la exportación.

Si su implementación actual se basa únicamente en posiciones de columna en Admin LT y no valida ni depende del texto del encabezado de columna, no se requiere ningún cambio para el propio Admin LT. Sólo es necesario prestar atención a las exportaciones de conectores cuando se depende de un diseño fijo.


## Experiencia no registrada en Experience Builder

La experiencia sin iniciar sesión en Experience Builder permite a las organizaciones mostrar su contenido de aprendizaje y páginas del portal a todos los visitantes, incluidos los que no han iniciado sesión. Esta función está diseñada para atraer, informar e interactuar con posibles alumnos, ya que ofrece una vista previa fluida y de marca de sus ofertas de formación antes de solicitarles que inicien sesión o se inscriban.

Esta función te permite crear y personalizar páginas públicas mediante la misma interfaz de arrastrar y soltar fácil de usar que se encuentra en el Experience Builder estándar. Puede mostrar catálogos de cursos, categorías, rutas y contenido estático enriquecido, incluidas imágenes, texto, HTML e iframes incrustados, para cualquiera que visite su portal. Esto facilita resaltar los programas de aprendizaje, promover nuevos cursos y proporcionar información esencial a un público más amplio.

Los visitantes pueden examinar el catálogo, ver detalles sobre los cursos e instancias y utilizar la búsqueda global para explorar las oportunidades de formación disponibles. Sin embargo, las acciones que requieren la identidad de un usuario, como inscribirse en un curso, acceder a funciones personalizadas (como Calendario, Cumplimiento, Tabla de posiciones o Aprendizaje social) o consumir formación, solicitarán al visitante que inicie sesión. Este enfoque garantiza que la información confidencial y personalizada permanezca segura, al tiempo que permite una experiencia de previsualización completa.

Los administradores pueden configurar qué páginas y widgets pueden ver los usuarios que no han iniciado sesión, lo que garantiza que solo se muestre el contenido adecuado. Las páginas se pueden configurar para que sean accesibles tanto para los usuarios que hayan iniciado sesión como para los que no, o exclusivamente para uno de estos grupos. Experience Builder ofrece un modo de vista previa, que te permite ver exactamente cómo aparecerán las páginas a los visitantes antes de que se publiquen.

Para habilitar esta función, el administrador de integración de ALM debe activar el conector de acceso a datos de formación. Este conector garantiza que los metadatos del curso sean de acceso público.

La promoción de la marca y la localización son totalmente compatibles, lo que te permite personalizar los títulos de las páginas, los favoritos y la configuración de idioma para adaptarlos a la identidad de tu organización y a las necesidades de tu audiencia. Como parte de la transición a esta experiencia mejorada, la función heredada de la página de inicio para los usuarios que no hayan iniciado sesión quedará obsoleta. Por lo tanto, todo el nuevo contenido público debe crearse utilizando Experience Builder.

### Propósito de la función

La experiencia sin iniciar sesión en Experience Builder permite a las organizaciones mostrar públicamente el contenido de aprendizaje y las páginas del portal a cualquiera, sin necesidad de que los usuarios inicien sesión. Esto ayuda a atraer, informar e interactuar con posibles alumnos al proporcionar una vista previa de la formación y los recursos disponibles antes de la inscripción o la autenticación.

### Casos prácticos del mundo real en la experiencia de inicio de sesión no registrado

* **Marketing y divulgación**: las organizaciones pueden promocionar sus programas de formación a audiencias externas, como clientes potenciales, socios o solicitantes de empleo, haciendo que los catálogos de los cursos y los detalles del programa sean de acceso público.
* **Exploración previa a la inscripción**: Los alumnos pueden examinar los cursos disponibles, consultar información general y explorar las categorías antes de decidir si se inscriben o inician sesión, lo que les ayuda a tomar decisiones fundamentadas sobre la inscripción.
* **Portales de formación corporativa**: Las empresas pueden proporcionar un portal público con información de cumplimiento o incorporación, lo que permite a los nuevos empleados o contratistas ver qué formación está disponible antes de recibir las credenciales.
* **Páginas de aterrizaje de eventos o campañas**: Las organizaciones que ejecutan campañas o eventos de aprendizaje pueden crear páginas públicas dedicadas para resaltar cursos, horarios o recursos destacados, lo que aumenta la visibilidad y la participación.
* **SEO y capacidad de detección**: al hacer públicas determinadas páginas y catálogos, las organizaciones mejoran la visibilidad de sus motores de búsqueda y ayudan a las personas a descubrir sus ofertas de aprendizaje en línea.

### Conceptos clave de la experiencia de inicio de sesión no registrado

La experiencia sin iniciar sesión de Experience Builder le permite mostrar públicamente el contenido de aprendizaje y las páginas del portal, lo que permite a los visitantes explorar sin iniciar sesión.

* **Crear páginas y menús públicos**: Configuras páginas y un solo menú al que todos pueden acceder, independientemente del estado de inicio de sesión.
* **Agregar solo widgets compatibles**: se incluyen los widgets que no necesitan contexto de usuario (categorías, cursos y rutas de aprendizaje, cuadro de contenido, HTML, iframe), mientras que el sistema oculta los widgets específicos del usuario.
* **Configurar el comportamiento de la página adaptable**: decides si aparece una página para los usuarios que han iniciado sesión o no, y el sistema adapta los widgets visibles y el contenido en función del estado de inicio de sesión.
* **Vista previa de ambas experiencias**: Utiliza las opciones de vista previa para ver el aspecto de las páginas para los usuarios que han iniciado sesión o no, con diferencias en la visibilidad y el contenido de los widgets.
* **Habilitar búsqueda global**: Los visitantes buscan cursos y contenido, pero solo obtienen las funciones de búsqueda básicas sin integración avanzada de IA.
* **Permite a los visitantes examinar el catálogo y las descripciones generales de los cursos**: Los visitantes exploran páginas de catálogos, detalles de cursos e instancias, pero deben iniciar sesión para inscribirse o acceder a funciones personalizadas.
* **Personaliza la construcción de marca y la localización**: Establece favoritos y configuraciones de idioma para que coincidan con las necesidades de construcción de marca y accesibilidad de tu organización.
* **Habilitar el conector de acceso a datos de formación**: active este conector para exportar los metadatos del curso para su visualización pública, con lo que las páginas que no estén conectadas se mantendrán actualizadas.
* **Controlar el alto tráfico con la infraestructura compartida**: el sistema administra grandes volúmenes de visitantes anónimos utilizando recursos compartidos y límites de velocidad.
* **Optimizar para SEO**: La plataforma prepara páginas públicas para la indexación de motores de búsqueda, lo que facilita la búsqueda del contenido de aprendizaje.

### Requisitos previos para la experiencia sin sesión iniciada

* Debe habilitar el conector de acceso a datos de formación en el administrador de integración para poder utilizar la experiencia de inicio de sesión no registrado.
* El conector exporta los metadatos del curso a un repositorio público, que mantiene actualizadas las páginas que no han iniciado sesión.

#### Inicialización del conector de Training Data Access

El conector de Acceso a datos de formación (TDA) es un requisito previo esencial para habilitar la nueva función de generador de experiencias sin conexión en ALM. Este conector facilita la exportación de metadatos de formación, lo que permite que el portal muestre información del curso a los usuarios que no hayan iniciado sesión.

* **Activación del conector**: debe habilitar el conector TDA desde el panel de administración de integración. Este paso habilita la funcionalidad de generador de experiencias que no ha iniciado sesión y hace que las opciones de interfaz de usuario relevantes estén visibles en la interfaz de administración.
* **Exportación de metadatos**: una vez activada, el conector exporta los metadatos de formación esenciales (como el nombre del curso, la descripción, la información general, la clasificación, la duración y las aptitudes) de ALM a un repositorio público. Estos datos se utilizan para rellenar páginas y widgets que no han iniciado sesión.
* **Programación y sincronización**: El proceso de exportación se puede programar (por ejemplo, diariamente) para garantizar que en el portal se reflejen las últimas actualizaciones del curso. Los cambios realizados en ALM aparecerán en las páginas que no hayan iniciado sesión después del siguiente ciclo de exportación, sujetos al almacenamiento en caché y a la frecuencia de exportación.
* **Disponibilidad de la función**: Solo se puede acceder a las funciones del generador de experiencias que no haya iniciado sesión, como la creación de menús, la compatibilidad con widgets y la visibilidad del catálogo, una vez que se haya inicializado el conector de TDA. Si el conector no está habilitado, el generador de experiencias seguirá estando limitado a los escenarios de usuarios que hayan iniciado sesión.
* **Migración y soporte**: Para las cuentas que realizan la transición desde funciones heredadas de la página de inicio sin inicio de sesión, inicializar el conector de TDA es el primer paso hacia la migración. Garantiza que puedes utilizar la flexibilidad y las capacidades mejoradas del nuevo creador de experiencias.


### Qué pueden hacer los visitantes sin iniciar sesión

En un sitio de Experience Builder que no esté conectado, los visitantes pueden examinar el catálogo de formación abriendo la página del catálogo para catálogos públicos. Pueden utilizar filtros como catálogo, producto, función, tipo, aptitudes y etiquetas, dependiendo de cómo haya configurado el sitio. Los visitantes también pueden buscar cursos de formación mediante la barra de búsqueda global en el encabezado (si está activada) y ver los resultados de búsqueda directamente en la página del catálogo.

Los visitantes pueden ver los detalles de la formación abriendo páginas de información general de cursos, rutas de aprendizaje y certificaciones. Estas páginas muestran metadatos clave, incluidos el título, la descripción, el autor, la duración, el formato, las etiquetas y las aptitudes.

Además, los visitantes pueden explorar contenidos estáticos y promocionales. Pueden leer bloques de texto y contenido enriquecido, ver banners y mosaicos de imágenes e interactuar con iframes incrustados como micrositios externos, vídeos o herramientas.

Si un visitante hace clic en Inscribir o intenta comenzar a entrenar, el sistema le pedirá que inicie sesión o que se registre. Después de iniciar sesión correctamente, se redirige al visitante a la página adecuada, ya sea la página principal, una página personalizada o la formación específica que ha seleccionado.

### Lo que no está disponible sin iniciar sesión

En un sitio de Experience Builder que no tenga iniciada sesión, los visitantes no pueden acceder a las funciones o al contenido que requieran autenticación del usuario. No pueden inscribirse en cursos de formación, iniciar o consumir cursos, ni acceder a widgets personalizados como Mi aprendizaje, Calendario, Cumplimiento, Tabla de posiciones o Aprendizaje social. Estos widgets dependen de los datos específicos del usuario y solo están disponibles después de iniciar sesión.

Los visitantes tampoco pueden realizar acciones como inscribirse en un curso o acceder a cualquier contenido que requiera realizar un seguimiento del progreso o del contexto del usuario. Al intentar inscribirse o iniciar un curso de formación, se solicita al visitante que inicie sesión o se registre antes de continuar.

### Widgets admitidos en modo sin inicio de sesión

En el modo sin conexión, solo se admiten los widgets que no requieren datos específicos del usuario. Estos incluyen:

* Widget de categorías, que muestra las categorías de formación disponibles.
* Widget de cursos y rutas, que muestra los cursos y las rutas de aprendizaje del catálogo público.
* Cuadro de contenido, para agregar texto estático, imágenes o contenido promocional.
* widget de HTML, para incrustar contenido de HTML personalizado.
* Widget de Iframe, para mostrar sitios, vídeos o herramientas externos en la página.
* Los widgets que requieren contexto de usuario, como Mi aprendizaje, Calendario, Cumplimiento, Tabla de posiciones y Aprendizaje social, no están disponibles en el modo sin conexión.

### Páginas y menús en una experiencia sin conexión

* Solo se admite un menú sin inicio de sesión, visible para todos los visitantes sin autenticación.
* Las páginas se pueden añadir a los menús de inicio de sesión y de no inicio de sesión; si una página está en ambos, adapta sus widgets y su contenido en función del estado de inicio de sesión del usuario.
* Los menús no conectados no tienen segmentación de audiencia ni personalización. Todos ven el mismo conjunto de páginas.
* Los widgets que no se admiten en el modo de inicio de sesión no se ocultan automáticamente; el diseño de página se ajusta para rellenar los huecos.
* La administración de menús y páginas (agregar, previsualizar, eliminar) es como el modo de inicio de sesión, pero con adaptaciones para las restricciones que no han iniciado sesión.

### Comportamiento de búsqueda y catálogo

En el modo sin conexión, los usuarios pueden acceder a la página del catálogo y utilizar la búsqueda para examinar los cursos y las rutas de aprendizaje disponibles. La página del catálogo muestra todos los cursos públicos, junto con los filtros y la funcionalidad de búsqueda, con la misma configuración de cuenta que en el modo de inicio de sesión. Cuando un usuario realiza búsquedas, los resultados aparecen en la página del catálogo y los usuarios pueden ver las páginas de información general de cursos e instancias sin iniciar sesión. Sin embargo, acciones como la inscripción requieren inicio de sesión.

Si un usuario intenta inscribirse, el sistema requiere que inicie sesión primero. La búsqueda de usuarios que no hayan iniciado sesión es más sencilla que la de los usuarios que hayan iniciado sesión y no incluye funciones avanzadas como la integración con el Asistente de inteligencia artificial.

### Implementación técnica

#### Configuración del conector de acceso a datos de formación

Debe habilitar el conector de acceso a datos de formación en el panel de administración de la integración para poder utilizar la función experience builder sin conexión. Este conector exporta metadatos de formación de ALM a un repositorio público, lo que permite acceder a ellos a través de las API para las páginas no conectadas. La configuración del conector es un requisito previo para activar la función y garantiza que el portal muestre información de formación actualizada.

#### Exportación y sincronización de metadatos

El conector exporta campos de metadatos clave como el nombre del curso, la descripción, la clasificación, la duración y las aptitudes. Puede programar exportaciones (por ejemplo, diarias) para mantener el portal sincronizado con ALM. No se pueden incluir todos los campos de metadatos; consulte ingeniería para obtener una lista completa. Los datos exportados se utilizan para rellenar las páginas que no han iniciado sesión y los cambios en ALM aparecerán después del siguiente ciclo de exportación.

#### Almacenamiento en caché y frecuencia de exportación

El sistema utiliza la frecuencia de exportación de backend y el almacenamiento en caché de frontend para administrar las actualizaciones de datos. Los cambios realizados en ALM se reflejan en su portal después de la actualización programada de la exportación y la caché. Es posible que algunas actualizaciones no aparezcan inmediatamente debido a estos mecanismos. Si necesita actualizaciones más rápidas, ajuste la programación de exportación o borre la caché según sea necesario.

#### Compatibilidad con la personalización de CSS/JS

Puede aplicar CSS y JavaScript personalizados a las páginas que hayan iniciado sesión y a las que no lo hayan hecho mediante la ficha de personalización. Esto le permite mantener una marca coherente, agregar elementos de interfaz de usuario personalizados y mejorar la experiencia del usuario en todo el portal. Todas las personalizaciones se aplican de forma global, lo que garantiza una apariencia unificada.

#### Diferencias de URL y marca (favicon, título de página)

Las páginas que no han iniciado sesión y las que sí lo han hecho pueden tener direcciones URL distintas para distinguir los estados de los usuarios. Puedes personalizar el favicon y el título de la página de tu portal, lo que te ayuda a reforzar tu identidad de marca. Estas funciones están disponibles en el generador de experiencias; consulte con el departamento de ingeniería para conocer el estado más reciente de la compatibilidad con usuarios no conectados.

### Rendimiento y escalabilidad

#### Pila compartida frente a pila premium

La pila compartida permite a varios clientes utilizar el generador de experiencias sin conexión en infraestructuras comunes, que admite niveles de tráfico estándar. El paquete premium es una opción de pago que proporciona recursos dedicados, funciones en tiempo real y límites de licencias más altos para los clientes con necesidades avanzadas. Seleccione la pila en función del tráfico previsto y los requisitos empresariales.

#### Límites de tráfico y limitación de velocidad

La pila compartida impone límites de tráfico para garantizar un uso justo entre los clientes. El equipo de ingeniería implementará la limitación de velocidad para evitar que un solo cliente consuma todos los recursos. Si planeas campañas de marketing o esperas un tráfico elevado, coordina con el equipo de ingeniería para comprender tus límites y evitar interrupciones en el servicio. La limitación de velocidad ayuda a mantener la estabilidad y el rendimiento del sistema para todos los usuarios.

#### Consideraciones de multitenencia y SEO

La plataforma es compatible con el multiinquilino, lo que permite a varios clientes alojar sus portales en infraestructuras compartidas. Las páginas que no han iniciado sesión son compatibles con SEO, junto con sitemap.xml y robots.txt para optimizar la visibilidad del motor de búsqueda. Esto garantiza que los motores de búsqueda puedan detectar e indexar el portal de forma adecuada.

### Migración y desaprobación

#### Transición desde la página principal existente sin iniciar sesión

Debe recrear su página de inicio con el nuevo generador de experiencias para obtener una mayor flexibilidad, compatibilidad con widgets y una experiencia de usuario mejorada. El plan de transición garantiza una interrupción mínima y un apoyo continuo.

#### Plan de comunicación

Los clientes que utilicen la página de inicio heredada recibirán una comunicación clara sobre los plazos de eliminación y los pasos de migración. Se ofrecerá asistencia técnica para ayudarte a mover tu página de inicio a la nueva plataforma de experience builder, lo que te garantiza las ventajas de las nuevas funciones y las actualizaciones continuas.

### Compatibilidad con localización e inicio de sesión

#### Lógica de retroceso de configuración regional

El sistema muestra las páginas en la configuración regional en la que se crearon. Si la configuración regional de un usuario no está disponible, el sistema utiliza una lógica alternativa para seleccionar la siguiente mejor configuración regional disponible. Esto garantiza que los usuarios vean siempre el contenido en un idioma compatible, lo que mejora la accesibilidad y la satisfacción de los usuarios.

#### Tipos de inicio de sesión admitidos

La experiencia de inicio de sesión no registrado admite todos los tipos de inicio de sesión disponibles en ALM, incluidos el inicio de sesión único y el inicio de sesión estándar. Los usuarios pueden examinar el contenido sin iniciar sesión y se les pedirá que inicien sesión cuando sea necesario, como inscribirse en un curso o acceder a funciones personalizadas. Esto proporciona una transición fluida de la navegación a la participación.


### API sin registro

#### API del objeto de aprendizaje de administración

Las páginas de Experience Builder que no están conectadas y los portales descentralizados suelen organizar o filtrar cursos según el producto y la función. La API de objeto de aprendizaje de administración se ha mejorado para garantizar que estas asociaciones sean accesibles de forma coherente para las integraciones de servicios de fondo y descentralizadas, así como para el conector de TDA.

**Punto final y comportamiento**

Seguirá utilizando el punto final del objeto de aprendizaje de administrador existente:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Donde:

* loId es el ID del objeto de aprendizaje (por ejemplo, course:12345).
* forcedFields[learningObject] indica a la API que incluya explícitamente productos y funciones para ese objeto de aprendizaje.

Esto se consigue asegurándose de que las asociaciones de producto y función de la orden de fabricación están presentes en la respuesta cuando se solicita a través de forcedFields. A continuación, la respuesta contiene, en atributos, los metadatos de producto y función necesarios para calcular o exponer los productos recomendados (rec\_products) y las funciones (rec\_roles) para Experience Builder y otros consumidores.

Una llamada típica de un administrador o de una integración tiene el siguiente aspecto:

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

El JSON de objeto de aprendizaje devuelto tiene la misma estructura básica que antes, pero ahora puede confiar en que los campos de producto/función están presentes cuando los solicite con forcedFields. Las integraciones que no utilizan forcedFields siguen comportándose como antes.

#### Lista de objetos de aprendizaje: compatibilidad con ayudas de trabajo en el filtro effectiveModifiedDate

**Propósito**

El conector de Training Data Access (TDA) y las implementaciones descentralizadas a menudo necesitan realizar una sincronización incremental, basada en la **fecha de modificación efectiva** de los objetos de aprendizaje. Hasta esta versión, las ayudas de trabajo (tipo LO jobAid) no se gestionaban correctamente cuando se combinaban con los filtros effectiveModifiedDate. Esta versión lo corrige para que las ayudas de trabajo se puedan sincronizar de forma incremental, como los cursos y las rutas de aprendizaje.

**Punto final y comportamiento**

El punto final de lista de objetos de aprendizaje existente se utiliza con filtros de fecha y tipo de objeto de aprendizaje:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

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
 "authorNames": ["Author"],
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
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
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

#### **API de menú: filtro de menú no conectado**

**Propósito**

Experience Builder y las interfaces de usuario descentralizadas necesitan una forma sencilla de recuperar el **menú sin inicio de sesión** , que define la navegación para los visitantes públicos. Antes de esta versión, tenía que obtener todos los menús y, a continuación, aplicar una lógica personalizada para identificar cuál representaba la navegación sin conexión. Esta versión añade un sencillo filtro del lado del servidor.

**Punto final y comportamiento**

El extremo de lista de menús existente se utiliza con un nuevo parámetro de consulta:

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

Los puntos clave:

* include=pages,subMenus.pages es opcional, pero se recomienda cuando necesite los detalles de la página y del submenú en la misma respuesta.
* isNonLoggedIn=true es nuevo en esta versión e indica al servidor que devuelva sólo los menús marcados como menús sin conexión.

Sin el parámetro isNonLoggedIn, el extremo se comporta exactamente como antes y devuelve menús según el comportamiento predeterminado existente. Con isNonLoggedIn=true, normalmente devuelve el menú único utilizado por la experiencia de inicio de sesión no registrado para su cuenta (ya que normalmente hay un menú sin inicio de sesión por cuenta).

En la práctica, un cliente ahora puede emitir:

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

y recupera la estructura de navegación no conectada en una sola llamada, con todas las páginas que deberían estar visibles para los visitantes anónimos.

Esto resulta especialmente útil cuando se está creando un sitio sin encabezado que no ha iniciado sesión y se desea reflejar la misma navegación que usa Experience Builder, o cuando se está depurando si el menú sin iniciar sesión se ha configurado correctamente.

### Permitir la lista de dominios personalizados

La pila no conectada consta de:

* Un dominio de CDN público (por ejemplo, cpcontents.adobe.com o yourdomain.example.com) que ofrece diseños, JSON de configuración y activos estáticos.
* Un extremo de Elasticsearch público (ES) que sirve datos de catálogo y de búsqueda, pero solo si la solicitud proviene de un **dominio de la lista de permitidos** para esa cuenta de ALM.

Cuando se introduce un dominio personalizado, funciona perfectamente sin ningún esfuerzo adicional después del proceso existente para añadir un dominio personalizado.

#### Requisitos previos

Antes de incluir en la lista blanca un dominio personalizado para usuarios no registrados:

1. El dominio personalizado se configura para su cuenta de ALM (por ejemplo, DNS para academy.yourcompany.com apunta a Adobe / Akamai y se aprovisionan los certificados).
2. El conector **Training Data Access (TDA)** está habilitado para la cuenta.
3. La característica **Experience Builder no conectado** está habilitada (en el Adobe).

Estas medidas garantizan que:

* Su cuenta tiene una **cuenta JSON** sin sesión iniciada (a menudo denominada accountConfig / experienceBuilderConfig), que incluye campos como cpDomain, almDomain, almCdnBaseUrl, esBaseUrl y dominios de la lista de permitidos.
* La pila sin sesión iniciada sabe dónde enviar datos y desde qué dominios debe aceptar solicitudes.

#### Cómo funcionan las listas de permitidos

La lista de permitidos se almacena en la configuración que exporta TDA y se lee la pila no conectada. Dicha configuración incluye:

* Los dominios de ALM (cpDomain, almDomain).
* La **URL base de CDN** para contenido no registrado (almCdnBaseUrl).
* La **dirección URL base de búsqueda pública** (esBaseUrl).
* La lista de dominios a los que se les permite realizar llamadas públicas sin iniciar sesión para esa cuenta.

Para que Experience Builder no conectado funcione en un dominio personalizado:

* El navegador debe cargar el HTML que no ha iniciado sesión desde ese dominio personalizado (o desde el dominio CDN que no ha iniciado sesión en ALM, según su configuración).
* Las llamadas de ese dominio a los puntos finales públicos de ES y CDN deben aceptarse. Esto solo sucede si el dominio está presente en la lista de permitidos.

Esta versión agrega un nuevo dominio de CDN sin inicio de sesión, cpcontents.adobe.com, y especifica que debe colocarse en **dominios incluidos en la lista de permitidos** en el conector de TDA. Para los usuarios nativos existentes que no han iniciado sesión, esto requiere una actualización.

#### Permitir-enumerar un dominio personalizado

**Configurar el dominio personalizado en ALM**

Trabaje con Adobe para registrar su dominio, por ejemplo, academy.yourcompany.com, como dominio personalizado para su cuenta de ALM. Actualice DNS para que apunte al Adobe Akamai según se indica y espere a que se complete SSL y el enrutamiento.

En este momento, tanto el tráfico que ha iniciado sesión como el que no lo ha hecho puede llegar a ALM a través de ese dominio, pero las llamadas de búsqueda y catálogo que no han iniciado sesión pueden seguir bloqueadas si el dominio no está incluido en la lista de permitidos.

**Habilitar TDA y Experience Builder sin sesión iniciada**

Asegúrese de que:

* El **conector de acceso a datos de formación** está habilitado.
* La característica **Experience Builder no conectado** está activada para la cuenta.

Al habilitar TDA, se crea o actualiza el JSON de la cuenta que no ha iniciado sesión. En el caso de las nuevas cuentas, el proceso también muestra de forma predeterminada el nuevo dominio de CDN sin inicio de sesión (cpcontent.adobe.com), por lo que el extremo público de ES espera llamadas de ese dominio.

En el caso de las cuentas que ya estaban utilizando la pila anterior sin inicio de sesión, los conectores existentes deben eliminarse y volver a crearse para seleccionar el nuevo dominio.

**Agregar el dominio personalizado a la lista de permitidos**

La parte crítica es indicarle a la pila de ES no iniciada que academy.yourcompany.com es un origen aprobado. Hay dos caminos comunes.

1. **Vuelva a habilitar el conector de TDA (sencillo, fácil de usar)**

Los usuarios nativos existentes que no hayan iniciado sesión deberán eliminar y volver a habilitar la conexión TDA para que el nuevo dominio aparezca automáticamente en la lista de permitidos. Haciendo esto se logran dos cosas:

1. Se regenerará el JSON de la cuenta que no ha iniciado sesión.
2. Los dominios de la lista de permitidos se actualizan para incluir el nuevo dominio de CDN no registrado y su dominio personalizado.

Se recomienda cuando tiene un número reducido de cuentas y puede tolerar que se deshabilite y se vuelva a habilitar temporalmente el conector.

1. **Compruebe que el dominio esté incluido en la lista de permitidos**

Después de la inclusión en la lista de permitidos, abra el sitio que no haya iniciado sesión en el dominio personalizado e inspeccione las llamadas de red del navegador.

Desea ver lo siguiente:

* Solicitudes a almCdnBaseUrl (por ejemplo, <https://cpcontent.adobe.com/>...) con 200/304.
* Solicitudes a esBaseUrl (API de búsqueda pública, por ejemplo <https://primeapps.adobe.com/almsearch/api/v1/>...) se completó correctamente, devolviendo JSON con datos de búsqueda / catálogo.

Si estas llamadas devuelven errores 4xx o explícitos que sugieren &quot;dominio no confiable&quot; o &quot;origen no permitido&quot;, la lista de permitidos está incompleta o mal configurada y el Soporte debe ajustarla.

El LLD sin inicio de sesión también indica que la configuración de la cuenta puede contener un valor de dominio esperado. En tiempo de ejecución, el sitio comprueba que el dominio de la dirección URL coincide con lo establecido en la configuración; si no lo hace, se puede redirigir al usuario a una página de error. Esto protege contra el acceso a la configuración de un cliente a través del dominio de otro cliente.

### Uso de recomendaciones en Experience Builder sin iniciar sesión

Experience Builder, que no está conectado, te permite crear páginas de aprendizaje públicas en las que los visitantes pueden examinar tu catálogo y ver el contenido resaltado antes de iniciar sesión. Aunque estos visitantes sean anónimos, puede seguir presentando cursos de formación recomendados mediante metadatos y widgets.

En la aplicación del alumno que ha iniciado sesión, las recomendaciones se pueden personalizar: pueden depender del perfil del alumno, su historial, sus aptitudes y su progreso. En la experiencia de **sin sesión iniciada**, todavía no hay identidad de alumno, por lo que la plataforma no puede personalizar por usuario.

Por lo tanto, Recommendations en modo sin sesión iniciada:

* **Seleccionado o basado en reglas**: basado en catálogo, producto, función, etiquetas, etiquetas y otros metadatos.
* **Orientado a segmentos**: &quot;recomendado para desarrolladores&quot;, &quot;recomendado para socios&quot;, &quot;ofrecido para principiantes&quot;.
* **Centrado en el marketing**: se utiliza para atraer y guiar a los visitantes a inscribirse una vez que inician sesión.

### Metadatos y API compatibles con las recomendaciones

Entre bastidores, las páginas sin sesión iniciada utilizan:

* El **conector TDA** para exportar metadatos de objetos de aprendizaje (cursos, rutas, certificaciones, ayudas de trabajo) a un índice de búsqueda pública.
* La **pila de búsquedas públicas** para responder a consultas de widgets que no han iniciado sesión (catálogo, búsqueda, cursos y rutas, categorías).
* La **API de objetos de aprendizaje de administración** muestra metadatos de productos y funciones que se pueden usar para reglas de recomendación.

En esta versión, la API del objeto de aprendizaje de administración se ha ampliado para que las asociaciones de productos y funciones estén disponibles de forma fiable:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Esto permite que los widgets y las integraciones descentralizadas creen recomendaciones basadas en reglas mediante productos, funciones, etiquetas de catálogo, etiquetas y otros campos de forma coherente.

### Diseño de secciones de recomendaciones con widgets de Experience Builder

Puede crear secciones de recomendación en páginas que no han iniciado sesión combinando **widgets de Experience Builder** con filtros de metadatos.

#### **Widget de cursos y rutas**

Utilice el widget **Cursos y trazados** cuando desee mostrar una fila o cuadrícula de elementos recomendados. En su configuración puede elegir:

* De qué catálogos extraer.
* Etiquetas de catálogo, productos, funciones o etiquetas que se van a utilizar como filtros.
* Si se muestran cursos, rutas, certificaciones, ayudas de trabajo o una combinación.
* Ordenación y número máximo de elementos.

Por ejemplo, puede crear:

* &quot;Recomendado para desarrolladores&quot;: filtre por un producto o función que utilice para el contenido del desarrollador.
* &quot;Empezar aquí&quot;: filtre por una etiqueta como &quot;Inicio&quot; o &quot;Incorporación&quot;.
* &quot;Destacados este trimestre&quot;: filtre por una etiqueta con límite de tiempo como featured-q3-2026.

El widget no está aprendiendo del comportamiento; muestra lo que coincide con las reglas de metadatos que defina. Desde el punto de vista del visitante, sin embargo, parece una tira de recomendaciones.

#### Widget **Categorías**

Usa el widget **Categorías** para ayudar a los visitantes a navegar por conjuntos de contenido &quot;recomendado&quot;, incluso si no conocen los nombres de tus productos.

Puede configurar mosaicos que representen cada uno un segmento, por ejemplo:

* &quot;Para administradores&quot;
* &quot;Para equipos de ventas&quot;
* &quot;Para socios&quot;
* &quot;Por línea de productos&quot;

Cada mosaico puede vincularse a:

* Una página de catálogo filtrada (por ejemplo, el catálogo filtrado por determinados productos o etiquetas).
* Una página dedicada sin conexión que utiliza cursos y rutas preconfiguradas para ese segmento.

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

### Cómo se pueden usar las ayudas de trabajo en el nuevo Experience Builder sin registro

En la **interfaz de usuario**, las ayudas de trabajo participan en experiencias sin sesión iniciada principalmente a través de widgets que pueden mostrar objetos de aprendizaje:

1. **Widget de rutas y cursos**
Este widget puede mostrar varios tipos de objetos de aprendizaje, incluidas las ayudas de trabajo. En las páginas que no han iniciado sesión, puede configurarlo para:
   1. Incluir o excluir ayudas de trabajo de forma explícita.
   2. Filtre las ayudas de trabajo por catálogo, producto, función, etiquetas, etiquetas y otros metadatos.
   3. Preséntelas junto a cursos y trazados o como una tira separada de &quot;Recursos&quot;.

Por ejemplo, en una página de aterrizaje pública, puede configurar una tira titulada &quot;Recursos útiles&quot; que muestre solo las ayudas de trabajo, y otra tira titulada &quot;Cursos recomendados&quot; que muestre los cursos y las rutas.

1. **Página de catálogo y búsqueda**
Las superficies **catalog** y **search** que no estén registradas utilizan el índice de búsqueda pública (alimentado por el conector Training Data Access). Ese índice ahora admite ayudas de trabajo correctamente, por lo que:
   1. Los resultados de búsqueda que no estén registrados pueden incluir ayudas de trabajo.
   2. Filtros de catálogos no registrados (por tipo, producto, etiquetas, etc.) Puede incluir ayudas de trabajo siempre que la configuración de su cuenta y los widgets estén configurados para mostrarlas.
2. **Páginas de información general de objetos de aprendizaje**
Cuando un visitante hace clic en una ayuda de trabajo desde cualquier widget o desde el catálogo, va a una **página de descripción general de objeto de aprendizaje** para esa ayuda de trabajo en modo sin inicio de sesión. A partir de ahí, pueden leer su descripción y metadatos. Normalmente, la descarga o el consumo reales aún requieren inicio de sesión, pero la presencia y la capacidad de detección de la propia ayuda de trabajo dependen de la experiencia de no inicio de sesión.

### Cómo se exponen las ayudas de trabajo mediante API que no han iniciado sesión

En el **lado de la API**, las ayudas de trabajo son compatibles con:

1. **Conector de acceso a datos de formación y búsqueda pública**
TDA exporta metadatos de ayuda de trabajo junto con otros tipos de objetos de aprendizaje al índice de búsqueda pública que atiende consultas de catálogo y búsqueda no registradas. En esto confían Experience Builder y las interfaces de usuario descentralizadas.
2. La lista de **objetos de aprendizaje con effectiveModifiedDate**
En esta versión, se ha corregido el extremo del listado de objetos de aprendizaje para que las ayudas de trabajo funcionen correctamente con el filtro effectiveModifiedDate. Ahora puede llamar a:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Antes de este cambio, la combinación de effectiveModifiedDate con loTypes=jobAid no devolvía de forma fiable las ayudas de trabajo. Eso significa:

1. Tus trabajos de ETL o TDA pueden **sincronizar las ayudas de trabajo de forma incremental** para experiencias que no hayan iniciado sesión, del mismo modo que para cursos y rutas.
2. Cualquier implementación descentralizada que cree un directorio de ayuda de trabajo público puede consultar los cambios en función de effectiveModifiedDate y loType=jobAid.

**Nota**:

En el estado sin sesión iniciada:

* Las ayudas de trabajo son principalmente **detectables**: los visitantes pueden ver que existen, leer descripciones y entender cómo admiten temas o cursos.
* El **consumo** real (descargar o abrir el contenido de la ayuda de trabajo) normalmente requiere inicio de sesión, especialmente si las ayudas de trabajo se consideran parte del contenido interno o con licencia.

### Cambios en la descripción breve en la búsqueda de objetos de aprendizaje (sin iniciar sesión)

En la pila no conectada, la búsqueda y la lista de objetos de aprendizaje (LO) funcionan mediante el conector de Acceso a datos de formación (TDA) y un índice de Elasticsearch público. Históricamente, esta pila utilizaba un único campo de descripción/información general para cada objeto de aprendizaje. Los clientes que creaban portales descentralizados no conectados querían mostrar la misma breve descripción en los mosaicos de objetos de aprendizaje que mostraba la interfaz de usuario del alumno que había iniciado sesión, en lugar de solo la larga descripción general.

El cambio introduce la compatibilidad con el objeto de aprendizaje **breve descripción** en las API de búsqueda y listado no registradas:

* Para **cursos**, la semántica de la interfaz de usuario existente es:
* Las tarjetas de inicio de sesión muestran una breve descripción (campo de 140 caracteres), si existe; de lo contrario, vuelven a la descripción detallada.
* Para **rutas de aprendizaje**, la interfaz de usuario que ha iniciado sesión utiliza el campo Beneficios como descripción breve, si se ha definido, y vuelve a la descripción general en caso contrario.
* Para **certificaciones**, se utiliza una descripción breve, con una descripción general de la certificación más larga como reserva.
* Para **ayudas de trabajo**, se usa el campo de descripción principal.

### Otros cambios

#### Restricción de que no pueda haber dos cuentas que compartan el mismo dominio personalizado

En las arquitecturas sin inicio de sesión y sin inicio de sesión de Adobe Learning Manager, un **dominio personalizado** (por ejemplo, academy.example.com) se trata como una clave única global que debe asignarse exactamente a una cuenta de ALM, por lo que la plataforma aplica una restricción estricta de que **no hay dos cuentas que puedan compartir el mismo dominio personalizado**. Esto es necesario para la seguridad, el enrutamiento y el SEO: la capa de enrutamiento y la pila de elementos no registrados utilizan el dominio para buscar la configuración correcta de la cuenta (incluidos sus elementos JSON de cuenta no registrada, los menús de Experience Builder, la marca y los puntos finales de TDA/búsqueda),

Permitir el mismo dominio personalizado en dos cuentas haría imposible garantizar qué datos de cuenta se devuelven, podría causar fugas entre inquilinos y también dañaría artefactos generados como sitemap.xml y robots.txt que se producen por cuenta pero que los motores de búsqueda descubren por host. Operacionalmente, esto significa que cuando asigne o mueva un dominio personalizado primero debe asegurarse de que no esté asociado a ninguna otra cuenta (o anular su registro allí), y las herramientas internas de Adobe rechazarán los intentos de vincular el mismo dominio a varias cuentas.

#### Almacenamiento en caché de los recursos en el explorador en la experiencia sin iniciar sesión

En la experiencia sin inicio de sesión de Adobe Learning Manager, el almacenamiento en caché de los recursos del explorador es una parte fundamental de la estrategia de rendimiento y escala, porque las páginas públicas deben controlar un tráfico de marketing grande y a veces intenso con baja latencia y una carga de origen mínima. Los recursos estáticos y semiestáticos, como el shell del HTML sin conexión (por ejemplo, index.html/guest.html), el JSON de configuración de nivel de cuenta (account.json o config.json), el JSON de diseño de página de Experience Builder (menús, diseños de widget, configuración de tarjeta), CSS, JS, imágenes y favicons, se proporcionan desde una CDN de Akamai (cpcontents.adobe.com / cpcontent.adobe.com) con encabezados de caché que fomentan la reutilización tanto del lado de la CDN como del navegador, de modo que, después de cargar la primera página, el navegador pueda procesar las páginas posteriores sin conexión en gran medida desde su caché, revalidándose solo cuando sea necesario mediante ETag o Last-Last-Last-ag campo.

## Ayudas de trabajo multilingües

### Introducción

Las ayudas de trabajo multilingües en Adobe Learning Manager (ALM) permiten a los autores y administradores proporcionar documentos de apoyo, guías o recursos en varios idiomas dentro de una única entrada de ayuda de trabajo. Los alumnos de diferentes regiones pueden acceder a los materiales relevantes en su idioma preferido, lo que mejora la comprensión, el cumplimiento normativo y la experiencia del usuario.

### Comportamiento anterior

Anteriormente, las ayudas de trabajo de ALM admitían un solo archivo de contenido por ayuda de trabajo, incluso cuando se podía localizar el nombre y la descripción. Para proporcionar el mismo recurso en varios idiomas, los autores tenían que crear ayudas de trabajo independientes para cada idioma. Esto dio lugar a duplicaciones, confusión y aumento de los gastos administrativos. No hay una forma unificada de gestionar los recursos multilingües, lo que dificulta garantizar la coherencia y hacer un seguimiento del uso.

### Casos de uso

* **Capacitación de la fuerza laboral global**: entrega manuales de seguridad, guías de procesos o documentos de referencia en varios idiomas a una fuerza laboral diversa.
* **Cumplimiento normativo**: asegúrese de que todos los empleados reciban la misma documentación de cumplimiento en su idioma nativo.
* **Contratación coherente**: proporciona listas de comprobación o preguntas frecuentes de incorporación en los idiomas locales para los nuevos empleados en todo el mundo.
* **Duplicación reducida**: administra todas las versiones de idioma de una ayuda de trabajo en una sola entrada, lo que simplifica las actualizaciones y la creación de informes.

### Funciones principales

* **Compatibilidad con varios idiomas**: adjunta un archivo o una dirección URL únicos para cada idioma admitido en una sola ayuda de trabajo.
* **Nombre y descripción traducidos**: escriba el nombre y la descripción de la ayuda de trabajo en cada idioma.
* **Administración unificada**: edita, actualiza e informa sobre todas las versiones de idiomas desde un único lugar.
* **Compatibilidad con versiones anteriores**: Las ayudas de trabajo existentes en un solo idioma se replican automáticamente en todos los idiomas agregados hasta que se cargan nuevos archivos.

### Crear una ayuda de trabajo multilingüe

1. Vaya a la función de autor y seleccione **Ayudas de trabajo**.
2. Seleccione **Crear ayuda de trabajo**.
3. Introduzca el nombre y la descripción de la ayuda de trabajo en el idioma predeterminado.
4. Agregue el archivo de contenido principal o la dirección URL del idioma predeterminado.
5. Guarde la ayuda de trabajo.

### Añadir idiomas adicionales

1. En el editor de la ayuda de trabajo, seleccione **Agregar idioma**.
2. Seleccione el idioma o los idiomas deseados de la lista.
3. Para cada idioma agregado:
   * Introduzca el nombre y la descripción traducidos.
   * Cargue el archivo de contenido correspondiente o proporcione una dirección URL específica del idioma.
4. Repita el proceso para todos los idiomas necesarios.

### Editar y administrar idiomas

1. Para actualizar un archivo o una descripción de un idioma específico, seleccione la ficha Idioma y realice los cambios necesarios.
2. Si se agrega un idioma después de publicar la ayuda de trabajo, el archivo original se asigna automáticamente al nuevo idioma hasta que se cargue un archivo único.
3. Elimine o reemplace archivos en cualquier idioma que necesite.

### Publish y experiencia del alumno

1. Después de agregar todos los idiomas y archivos, publique la ayuda de trabajo.
2. Los alumnos ven la ayuda de trabajo en el idioma de contenido seleccionado, con el archivo o la URL adecuados.
3. Si el idioma de un alumno no está disponible, se muestra el archivo de idioma predeterminado.

### Informes

1. Descargue informes de ayudas de trabajo para ver los detalles de todos los archivos e idiomas asociados a cada ayuda de trabajo.
2. Los informes incluyen el idioma, el nombre de archivo y los datos de uso para el seguimiento.

### Prácticas recomendadas

* Proporcionar traducciones precisas para nombres, descripciones y archivos de contenido.
* Revisa y actualiza los archivos con regularidad para garantizar la coherencia entre los distintos idiomas.
* Utilice convenciones de nomenclatura claras para distinguir los archivos de los diferentes idiomas.
* Pruebe la experiencia del alumno cambiando los idiomas de contenido para verificar que la entrega de los archivos es correcta.

### Resolución de problemas

* **Falta un archivo para un idioma**: Se muestra el archivo predeterminado. Asegúrese de que todos los idiomas tengan cargado el archivo correcto.
* **Ayudas de trabajo heredadas**: agregue nuevos archivos de idioma para reemplazar los originales replicados automáticamente.
* **Se muestra un idioma incorrecto**: Compruebe la configuración de idioma del contenido del alumno y la configuración de idioma de la ayuda de trabajo.

Las ayudas de trabajo multilingües te permiten distribuir recursos de apoyo a una audiencia global en una única entrada, reducir la duplicación y garantizar que todos los alumnos reciban la información adecuada en su idioma preferido. Esta función mejora la accesibilidad, el cumplimiento normativo y la eficacia administrativa en Adobe Learning Manager.

## Obtén respuestas con AI Assistant para alumnos

AI Assistant para alumnos es un asistente conversacional basado en IA dentro de Adobe Learning Manager diseñado para guiarte a la información que necesitas más rápido. Al formular preguntas en lenguaje natural, puedes obtener explicaciones contextuales, mostrar cursos relevantes y recuperar información del contenido de aprendizaje, sin tener que navegar manualmente por los catálogos.

### Capacidades

* **Respuesta inteligente a preguntas:** Maneja conversaciones de una o varias vueltas, lo que te permite hacer preguntas de manera natural. Las respuestas proceden de cursos, rutas de aprendizaje, certificaciones y ayudas de trabajo.
* **Respuestas basadas en contenido con citas:** Extrae la información directamente de los materiales de aprendizaje e incluye citas que apuntan al curso, módulo o recurso original.
* **Amplia compatibilidad de contenido:** Admite una amplia variedad de formatos, incluidos documentos, presentaciones, vídeos, archivos de audio, contenido de HTML y módulos del Modelo de referencia de objetos de contenido compartido (SCORM).
* **Experiencia de usuario perfecta:** Disponible como panel lateral en todas las páginas del alumno, con el historial de chat basado en sesión para garantizar la continuidad.
* **Controles de administrador sólidos:** Los administradores pueden habilitar o deshabilitar el asistente, limitar el acceso de los grupos de usuarios y elegir qué catálogos internos se utilizan como origen para las respuestas generadas por IA.

### Ventajas

* **Acceso más rápido al conocimiento:** Recibe respuestas instantáneas a sus preguntas, lo que elimina la necesidad de navegar por varios cursos o documentos.
* **Mayor interacción:** Las interacciones de conversación hacen que la experiencia de aprendizaje sea más natural, intuitiva y accesible.
* **Mejor comprensión:** Puedes hacer preguntas de seguimiento para aclarar conceptos y explorar los temas con más detalle.
* **Soporte de aprendizaje ampliable:** Las respuestas automatizadas e impulsadas por IA minimizan la dependencia de los expertos en la materia y los equipos de soporte.

Más información sobre [Asistente de inteligencia artificial para alumnos](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Compatibilidad con pistas de vídeo y texto multilingües (VTT)

La compatibilidad con las pistas de vídeo y texto (VTT) multilingües en Adobe Learning Manager permite a los autores proporcionar subtítulos y pies de ilustración para contenido de vídeo y audio en varios idiomas. Esta función agiliza la localización, al hacer que la formación sea accesible para una audiencia global y al garantizar el cumplimiento de los estándares de accesibilidad. Los autores pueden generar, traducir, revisar y editar automáticamente archivos VTT directamente en la plataforma.

### Casos prácticos

* **Formación global:** Distribuye contenido de vídeo con subtítulos en varios idiomas para que llegue a los alumnos de todo el mundo.
* **Cumplimiento de accesibilidad:** Proporcione pies de ilustración para los usuarios con discapacidad auditiva en el idioma que prefieran.
* **Localización más rápida:** Reduce el esfuerzo manual y acelera la distribución de contenido generando y traduciendo archivos VTT automáticamente.
* **Experiencia coherente:** Asegúrese de que todos los alumnos reciban la misma información, independientemente del idioma.

### Funciones principales

* **Generación automática de VTT:** Carga un archivo de vídeo o audio y genera automáticamente subtítulos VTT en el idioma original.
* **Traducción en varios idiomas:** Traduzca los subtítulos a cualquiera de los 39 idiomas no ingleses admitidos.
* **Revisión y edición en la aplicación:** Revise, edite y descargue archivos VTT antes de publicarlos.
* **Notificaciones:** Recibe notificaciones en la aplicación cuando se complete la generación y traducción de VTT.
* **Publicación fluida:** Publish finalizó los subtítulos para que los alumnos accedieran en el idioma elegido.

### Cargar contenido y generar VTT

1. Ve a la biblioteca de contenido y selecciona **Agregar contenido**.
2. Carga tu archivo MP3 o MP4.
3. En el cuadro de diálogo de carga, seleccione la opción para **Generar traducción**.
4. Seleccione el idioma del contenido original (el predeterminado es el idioma del archivo).
5. Seleccione otros idiomas de destino para la traducción (se admiten hasta 39).
6. Seleccione **Guardar**. El sistema comienza a generar y traducir archivos VTT.

### Supervisar el progreso

1. Después de guardar, la nueva entrada de contenido aparece en la biblioteca de contenido.
2. Un indicador de progreso muestra el estado de la generación y traducción de VTT.
3. Recibirá una notificación en la aplicación cuando se complete el proceso.

### Revisar y editar archivos VTT

1. En la biblioteca de contenido, abra el contenido en modo **Editar**.
2. Para cada idioma, seleccione el vínculo **Revisar** situado junto al archivo VTT.
3. Aparecerá una ventana emergente con los subtítulos de ese idioma.
4. Edite los subtítulos directamente en el elemento emergente o descargue el archivo VTT para editarlo sin conexión.
5. Después de realizar cambios, vuelva a cargar o pegar los subtítulos revisados en la ventana emergente.
6. Guarde sus ediciones.

### Subtítulos de Publish

1. Cuando esté satisfecho con todas las leyendas de idioma, publique el contenido.
2. Los alumnos ven las opciones de subtítulos en todos los idiomas publicados al ver el vídeo.

### Información adicional

* **Idiomas admitidos:** Los 39 idiomas distintos del inglés admitidos por Adobe Learning Manager.
* **Notificaciones:** Se notifica a los autores cuando se completa la generación y traducción de VTT.
* **Flexibilidad de edición:** Los subtítulos se pueden editar en la aplicación o sin conexión y volver a cargarse.
* **Escalabilidad:** Diseñado para satisfacer las necesidades de accesibilidad y localización de empresas.
* **No es necesario cargar VTT manualmente:** El sistema puede generar archivos VTT desde cero utilizando el vídeo/audio cargado.

### Prácticas recomendadas

* Revise siempre los subtítulos generados automáticamente para comprobar su precisión antes de publicar.
* Proporcionar traducciones para todos los grupos de alumnos principales con el fin de maximizar la accesibilidad.
* Utilice el sistema de notificaciones para estar al día del estado del procesamiento.
* Actualice regularmente los subtítulos si cambia el contenido del vídeo.

### Resolución de problemas

* Si falla la generación de VTT, asegúrese de que el archivo esté en un formato compatible (MP3/MP4).
* En el caso de los idiomas que faltan, verifique que sean compatibles y que estén seleccionados durante la carga.
* Si los subtítulos no están sincronizados, utilice el editor de la aplicación para ajustar la temporización.

La compatibilidad con VTT multilingüe permite ofrecer experiencias de aprendizaje de vídeo localizadas y accesibles de manera eficaz. Al utilizar la generación automática, la traducción y la edición en la aplicación, puede garantizar que el contenido llegue a todos los alumnos y les sea compatible, independientemente del idioma.

## Diseñar certificados personalizados

Los certificados personalizados en Adobe Learning Manager (ALM) permiten a los administradores y autores diseñar, administrar y emitir certificados personalizados para los alumnos. La función incluye un editor con función de arrastrar y soltar, campos dinámicos, asistencia multilingüe y fondos generados por IA para que las organizaciones puedan crear certificados de marca sin conocimientos técnicos.

### Comportamiento anterior

Anteriormente, la creación de certificados en ALM estaba limitada por la rigidez de las plantillas, la falta de personalización y las barreras técnicas (como la edición de HTML). Los clientes solicitaron formas más sencillas de diseñar certificados, añadir campos dinámicos (como el nombre del alumno o el instructor) y admitir varios idiomas, todo ello manteniendo la coherencia de marca y el atractivo visual.

### Casos de uso

* **Reconocimiento de marca**: emite certificados con logotipos corporativos, colores y fuentes para el cumplimiento, la formación o el logro.
* **Personalización dinámica**: Rellena automáticamente los nombres de los alumnos, los nombres de los instructores y otros campos activos.
* **Entrega multilingüe**: proporciona certificados en varios idiomas para alumnos de todo el mundo.
* **Diseño flexible**: Crea certificados verticales u horizontales, usa fondos generados por IA y disfruta de una vista previa antes de la publicación.

### Acceso a certificados personalizados

1. Vaya a la sección **Logros** en la página principal del administrador (anteriormente denominada **Insignias**).
2. Seleccione **Certificados** para ver, crear o administrar plantillas de certificados.

### Crear un certificado

1. Seleccione **Crear certificado**.
2. Seleccione la orientación vertical u horizontal.
3. Seleccione una plantilla existente o comience desde un lienzo en blanco.
4. Introduzca un nombre de certificado y un idioma predeterminado.
5. Utilice el editor de arrastrar y soltar para agregar:
   * Campos de texto (con opciones de fuente, color y posición)
   * Imágenes (logotipos, iconos, etc.)
   * Campos dinámicos (nombre del alumno, nombre del instructor, etc.)
   * Fondos de certificado (color sólido, imagen cargada o imagen generada por IA)
6. Para fondos generados por IA: introduzca un mensaje (por ejemplo, &quot;estudiantes en una clase&quot;) para generar fondos utilizando IA.

### Añadir campos dinámicos

Los campos dinámicos de los certificados personalizados de Adobe Learning Manager son marcadores de posición que se rellenan automáticamente con información relevante, como el nombre del alumno, el nombre del instructor u otros datos específicos de la cuenta, cuando se genera el certificado, lo que permite certificados personalizados y según el contexto sin edición manual.

1. Inserta variables dinámicas como el nombre del alumno, el nombre del instructor u otros campos activos.
2. Los campos se rellenan automáticamente cuando se emite el certificado.

### Asistencia multilingüe

1. Agregue nuevos idiomas (por ejemplo, francés o alemán) al certificado.
2. Introduzca el texto traducido para cada idioma.
3. Administre traducciones y certificados de vista previa en cada idioma.

### Previsualización y publicación

1. Utilice la función de vista previa para ver cómo los alumnos pueden ver el certificado.
2. Descargue o imprima la vista previa para su revisión.
3. Guarda como borrador para continuar editándolo más tarde o publícalo cuando estés listo.

### Aplicar certificados

1. Los administradores pueden establecer certificados predeterminados para la cuenta.
2. Los autores pueden adjuntar certificados a instancias específicas de objetos de aprendizaje (cursos, rutas, etc.).
3. Seleccione diferentes certificados en el nivel de instancia según sea necesario.

### Administrar certificados

1. Ver certificados publicados y borradores en la biblioteca.
2. Edite, actualice o elimine plantillas según sea necesario.
3. Los certificados se pueden reutilizar en varias instancias.

Los certificados personalizados en ALM proporcionan una forma flexible de diseñar y emitir certificados personalizados, de marca y multilingües. La función simplifica la gestión de certificados, mejora el reconocimiento de alumnos y satisface las necesidades globales de cumplimiento normativo y marca.

## Ayudas de trabajo multilingües

Las ayudas de trabajo multilingües en Adobe Learning Manager (ALM) permiten a los autores y administradores proporcionar documentos de apoyo, guías o recursos en varios idiomas dentro de una única entrada de ayuda de trabajo. Los alumnos de diferentes regiones pueden acceder a los materiales relevantes en su idioma preferido, lo que mejora la accesibilidad, el cumplimiento normativo y la experiencia del usuario.

### Comportamiento anterior

Anteriormente, ALM solo permitía un archivo de contenido por ayuda de trabajo, aunque el nombre y la descripción se pudieran localizar. Para proporcionar el mismo recurso en varios idiomas, los autores tenían que crear ayudas de trabajo independientes para cada idioma. Esto dio lugar a duplicaciones, confusión y un mayor esfuerzo administrativo. No hay una forma unificada de gestionar los recursos multilingües, lo que dificulta garantizar la coherencia y hacer un seguimiento del uso.

### Casos de uso

* **Capacitación de la fuerza laboral global**: entrega manuales de seguridad, guías de procesos o documentos de referencia en varios idiomas a una fuerza laboral diversa.
* **Cumplimiento normativo**: asegúrese de que todos los empleados reciban la misma documentación de cumplimiento en su idioma nativo.
* **Contratación coherente**: proporciona listas de comprobación o preguntas frecuentes de incorporación en los idiomas locales para los nuevos empleados en todo el mundo.
* **Duplicación reducida**: administra todas las versiones de idioma de una ayuda de trabajo en una sola entrada, lo que simplifica las actualizaciones y la creación de informes.

### Crear una ayuda de trabajo multilingüe

1. Vaya a la función de autor y seleccione **Ayudas de trabajo**.
2. Seleccione **Crear ayuda de trabajo**.
3. Introduzca el nombre y la descripción de la ayuda de trabajo en el idioma predeterminado.
4. Cargue el archivo de contenido principal o proporcione una dirección URL para el idioma predeterminado.
5. Guarde la ayuda de trabajo.

### Añadir idiomas adicionales

1. En el editor de la ayuda de trabajo, seleccione **Agregar idioma**.
2. Seleccione el idioma o los idiomas deseados de la lista.
3. Para cada idioma agregado:
   * Introduzca el nombre y la descripción traducidos.
   * Cargue el archivo de contenido correspondiente o proporcione una dirección URL específica del idioma.
4. Repita el proceso para todos los idiomas necesarios.

### Editar y administrar idiomas

1. Para actualizar un archivo o una descripción de un idioma específico, seleccione la ficha Idioma y realice los cambios necesarios.
2. Si se agrega un idioma después de publicar la ayuda de trabajo, el archivo original se asigna automáticamente al nuevo idioma hasta que se cargue un archivo único.
3. Elimine o reemplace archivos en cualquier idioma que necesite.

### Publish y experiencia del alumno

1. Después de agregar todos los idiomas y archivos, publique la ayuda de trabajo.
2. Los alumnos ven la ayuda de trabajo en el idioma de contenido seleccionado, con el archivo o la URL adecuados.
3. Si el idioma de un alumno no está disponible, se muestra el archivo de idioma predeterminado.

### Informes

1. Descargue informes de ayudas de trabajo para ver los detalles de todos los archivos e idiomas asociados a cada ayuda de trabajo.
2. Los informes incluyen el idioma, el nombre de archivo y los datos de uso para el seguimiento.

Las ayudas de trabajo multilingües en ALM le permiten distribuir recursos de apoyo a una audiencia global en una sola entrada, reducir la duplicación y garantizar que todos los alumnos reciban la información correcta en su idioma preferido. Esta función mejora la accesibilidad, el cumplimiento normativo y la eficacia administrativa en Adobe Learning Manager.

## Mejoras en la reproducción de cursos generados por Captivate

La actualización mejora significativamente la experiencia de reproducción de contenido de Adobe Captivate en ALM al introducir una interfaz unificada y optimizada.

El reproductor de ALM ahora muestra una única tabla de contenido consolidada, que oculta la tabla de contenido del Captivate, y proporciona indicadores claros de finalización de nivel de diapositiva, incluidas marcas de graduación verdes para el seguimiento del progreso visual.

El sistema simplifica la navegación combinando los controles del módulo y del curso en una barra intuitiva, lo que reduce la confusión del alumno.

Los controles de progreso según el contexto mejoran la facilidad de uso al mostrar las barras de progreso de vídeo solo en las diapositivas de vídeo y los controles de navegación de diapositivas solo en las diapositivas que no sean de vídeo.

Además, el sistema ahora vincula notas a números de diapositivas en lugar de marcas de tiempo, lo que garantiza exportaciones fiables de PDF y resuelve incoherencias de formato anteriores.

## Mejoras de lista de comprobación

### Compatibilidad con varios idiomas para la lista de comprobación

Esta función permite crear y administrar módulos de lista de comprobación en varios idiomas. Cada pregunta, instrucción y criterio de evaluación de la lista de comprobación puede traducirse para que los revisores y los alumnos interactúen con la lista de comprobación en el idioma que prefieran. El sistema muestra la lista de comprobación en el idioma de contenido seleccionado por el usuario, lo que mejora la accesibilidad y el cumplimiento normativo para los equipos globales.

1. Añada o edite un módulo de lista de comprobación en el curso.
2. Seleccione todos los idiomas que desee admitir en las opciones de idioma.
3. Para cada idioma, introduzca traducciones para cada pregunta de lista de comprobación, instrucción y criterio de evaluación.
4. Guarde los cambios. La lista de comprobación se muestra en el idioma de contenido seleccionado por el revisor o el alumno.
5. Si más adelante agrega un nuevo idioma, proporcione traducciones para todas las preguntas y criterios antes de la publicación.
6. Al descargar informes de lista de comprobación, seleccione el idioma que prefiera para ver el informe en ese idioma.

### Ponderación de preguntas de lista de comprobación para evaluaciones de instructores

Esta función le permite asignar puntuaciones máximas diferentes (ponderación) a cada pregunta de la lista de comprobación. Puede reflejar la diversa importancia o dificultad de cada pregunta, lo que permite realizar evaluaciones más precisas y significativas. El sistema calcula la puntuación total en función de los datos introducidos y determina si el alumno supera o no los criterios establecidos.

1. Al agregar un módulo de lista de comprobación, seleccione **Puntuación personalizada**.
2. Para cada pregunta de la lista de comprobación, establezca una puntuación máxima única que refleje su importancia.
3. Defina la puntuación de aprobado global para la lista de comprobación.
4. Guarde y publique la lista de comprobación.
5. Como instructor o revisor, evalúe a cada alumno asignando una puntuación para cada pregunta (hasta el máximo que haya establecido).
6. El sistema calcula la puntuación total y determina el estado de aprobado/suspenso.
7. Descargue informes de lista de comprobación para ver las puntuaciones alcanzadas y máximas para cada pregunta y la puntuación total.

### Lista de comprobación con capacidad de comentario para el revisor

Esta función permite a los revisores añadir comentarios u opiniones durante la evaluación de la lista de comprobación. Puede proporcionar comentarios personalizados y procesables para cada alumno. También puede optar por mostrar su nombre con sus comentarios para mayor transparencia. Todos los comentarios se guardan en la transcripción del alumno y se incluyen en los informes de la lista de comprobación.

1. Al configurar la lista de comprobación, habilite **Comentarios del revisor**.
2. Opcionalmente, habilite **Mostrar nombre del revisor al alumno** si desea que su nombre aparezca con los comentarios.
3. Durante la evaluación, introduzca comentarios o valoraciones para el alumno en el campo de comentarios proporcionados.
4. Seleccione si los comentarios deben estar visibles para el alumno.
5. Envíe su evaluación. Si se activa, el alumno ve sus comentarios y su nombre junto a los resultados.
6. Todos los comentarios se guardan en la transcripción del alumno y se incluyen en los informes de la lista de comprobación para su futura referencia.

## Mejoras de búsqueda avanzadas

Esta versión incluye una mejora en la búsqueda de contenido al mostrar los cursos con coincidencias de contenido con una consulta de mayor rango. Además, las ayudas de trabajo ahora se incluyen en la clasificación de búsqueda avanzada.

## Equivalentes y suplentes

### Información general

En muchas organizaciones, los alumnos se encuentran con situaciones de formación en las que diferentes cursos pueden cumplir legítimamente los mismos requisitos; por ejemplo, cuando un nuevo curso reemplaza a uno antiguo, cuando un curso más completo puede sustituir a uno más corto o cuando es necesario ofrecer un curso sustituto especial.

La función Cursos alternativos o Ruta de aprendizaje ofrece a ALM una forma formal de decir lo siguiente:

&quot;Si el alumno ha completado este curso de formación, asígnele el trato de que cumple los requisitos de formación relacionados.&quot;

La función funciona en todos los cursos y rutas de aprendizaje, garantiza que se cumplen los requisitos descendentes, como los requisitos previos y las reglas de cumplimiento, y lo hace sin obligar a los alumnos a pasar por contenido redundante. También mantiene la precisión de los informes al registrar lo que se completó directamente frente a lo que se satisfizo a través de una alternativa.

Básicamente, la función introduce el concepto de finalización alternativa: un estado de finalización especial creado automáticamente cuando un alumno finaliza un curso de origen configurado que cuenta para otro curso de destino.

### Equivalencia frente a alternativas

Algunas relaciones de formación son bidireccionales, lo que significa que cada curso puede satisfacer los requisitos del otro. En la práctica, se trata de un escenario en el que dos cursos de formación se consideran mutuamente sustituibles. Por el contrario, las relaciones unidireccionales permiten que una formación satisfaga los requisitos de otra, pero no viceversa. ALM modela ambos escenarios usando el mismo mecanismo alternativo*de finalización subyacente.

* **Relación bidireccional:** Al completar cualquiera de los dos cursos de formación se cumple el requisito del otro.
* **Relación unidireccional:** Completar el entrenamiento A satisface el entrenamiento B, pero completar B no satisface A. Esto es común cuando una versión más reciente o más completa debe contar para un requisito más antiguo, pero no al revés.

Las alternativas se suelen usar en escenarios **unidireccionales**, por ejemplo, cuando un curso de superconjunto más completo abarca todo en un curso de subconjunto más sencillo. Completar el superconjunto debe satisfacer el requisito del subconjunto, pero no necesariamente al revés.

* Un curso más nuevo y ampliado que debería tener en cuenta un requisito más antiguo.
* Curso diseñado para un público específico (por ejemplo, una variante regional o adaptada a la accesibilidad) que sigue cumpliendo los mismos requisitos que el curso principal.
* Una nueva versión mejorada de un curso que la organización desea contar para un requisito anterior, pero la versión anterior no debe contar para el nuevo requisito.

En Alternativas, la relación suele ser **one*way**. Si el Curso A es una alternativa para el Curso B, completar A puede satisfacer el requisito de B, pero completar B no necesariamente satisface A.

Tanto la equivalencia como la alternativa comparten el mismo mecanismo subyacente en ALM: cuando se completa una formación de origen configurada, ALM produce automáticamente una finalización alternativa para uno o más cursos de formación de destino.

### ¿Qué problemas resuelve esto?

Sin alternativas y equivalencias, los administradores y alumnos se enfrentan a varios problemas recurrentes:

* Se solicita con frecuencia a los alumnos que repitan cursos que cubran contenido que ya han completado en una versión o formato diferente.
* La actualización de los programas de cumplimiento es más sencilla porque los administradores pueden reemplazar o reestructurar los cursos de formación sin obligar a los alumnos que hayan completado versiones anteriores a recuperar contenido equivalente o reemplazado.
* La lógica de los requisitos previos es rígida. Si un camino requiere un curso en particular como prerrequisito, no hay una manera limpia de reconocer que otro entrenamiento es lo suficientemente bueno.
* La presentación de informes y las auditorías son más difíciles. No hay ninguna señal formal que demuestre que se cumplió un requisito mediante una terminación alternativa y no hay una forma directa de rastrear la fuente del crédito.

La función Alternativas y equivalencias soluciona estos problemas de la siguiente manera:

* Evitar el esfuerzo duplicado para los alumnos cuando las alternativas son válidas.
* Permitir a los administradores modificar estructuras de formación (por ejemplo, intercambiar un curso dentro de una ruta) sin interrumpir las finalizaciones de los alumnos que tomaron la versión anterior.
* Permitir que los requisitos previos y las comprobaciones de cumplimiento respeten tanto las finalizaciones directas como las finalizaciones alternativas o equivalentes.
* Anotar claramente, en transcripciones e informes, si una formación se completó directamente o se cumplió a través de una relación alternativa, junto con la cual la formación sirvió como fuente.

### Funcionamiento conceptual de la función

La característica se basa en tres ideas principales: **relaciones**, **finalización alternativa** y **comportamiento descendente**.

#### Relaciones entre cursos de formación

Los administradores definen las relaciones entre los cursos y las rutas de aprendizaje. Para cada relación, eligen un **origen** y uno o más **destinos**. Un solo curso puede tener hasta 30 objetivos, en función del número de cursos de formación anteriores o relacionados que deba satisfacer.

En Equivalencia, los administradores pueden establecer la relación **bidireccional** si desean que ambos cursos de formación se satisfagan mutuamente. En el caso de Alternativas, los administradores normalmente mantienen la dirección unidireccional para reflejar que solo se permiten algunas sustituciones.

Estas relaciones se almacenan en el nivel de formación, no en el nivel de alumno. Una vez configurados y activados, se aplican a todas las finalizaciones actuales y futuras del curso de formación de origen, sujetos a los ajustes de nivel de cuenta*como, por ejemplo, si la finalización retroactiva está activada.

### Finalización alternativa

Cuando un alumno finaliza un curso de formación de origen, ALM examina todas las relaciones alternativas o equivalentes configuradas y, para cada curso de formación de destino relevante, crea un **registro de finalización alternativo**. Este registro es distinto de una finalización normal:

* Marca el curso de formación de destino para el alumno, pero realiza un seguimiento de que se ha completado mediante una alternativa o equivalencia en lugar de directamente.
* Registra qué entrenamiento de origen se utilizó para satisfacer el objetivo.
* Se almacena en una estructura específica para que los informes puedan distinguir entre finalizaciones directas y alternativas.

Los alumnos verán una finalización alternativa aunque no estén inscritos. El informe Transcripciones de alumnos (LT) incluye solo los registros de los cursos de formación en los que se ha inscrito el alumno.

### Experiencia de la aplicación del alumno para finalizaciones alternativas y equivalentes

Las finalizaciones alternativas y equivalentes aparecen claramente en la aplicación del alumno para que los alumnos puedan comprender claramente cómo se ha satisfecho un requisito de formación, al tiempo que mantienen la coherencia con las transcripciones y los informes.

#### Comportamiento de la tarjeta LO

#### Estado de finalización alternativo

Cuando un alumno finaliza una formación mediante una relación alternativa o equivalente, la tarjeta de objeto de aprendizaje (LO) muestra un estado distinto como **Completado mediante alternativo**.\
Esta distinción visual ayuda a los alumnos a diferenciar entre finalizaciones directas y finalizaciones concedidas mediante relaciones configuradas.

#### Indicador de método de finalización

La tarjeta de objeto de aprendizaje incluye un indicador del método de finalización (por ejemplo, una etiqueta o un icono) para mostrar que la finalización se ha realizado mediante un **Alternativo**.\
Si posteriormente se revoca una finalización alternativa debido a cambios como la finalización retroactiva o la eliminación del curso de formación de origen, la tarjeta de aprendizaje se actualiza para reflejar **Alternativa (revocada)**.

#### Detalles de transparencia y auditoría

Los alumnos pueden abrir la tarjeta de objeto de aprendizaje para ver detalles adicionales, como los siguientes:

* El curso de origen o la ruta de aprendizaje que concedió la finalización alternativa
* La fecha de finalización asociada al curso de formación de origen.

Esto garantiza la transparencia y respalda las auditorías y las revisiones del cumplimiento normativo.

#### Filtrado y vistas

#### Filtro de método de finalización

La aplicación del alumno proporciona un filtro que permite a los alumnos distinguir entre:

* **Finalizaciones directas**
* **Finalizaciones alternativas**
* **Todas** finalizaciones

Esto permite a los alumnos comprender rápidamente cómo se cumplieron sus requisitos de aprendizaje.

#### Vistas de transcripción y progreso

El filtro del método de finalización está disponible en vistas de learner*facing, como:

* Transcripciones de aprendizaje
* Secciones de seguimiento de progreso y finalización

Estas opiniones indican claramente qué cursos de formación se completaron directamente y cuáles se cumplieron mediante alternativas o equivalencia.

#### Alineación de informes

La lógica de filtrado de la aplicación del alumno se alinea con la columna **Método de finalización** utilizada en los informes.\
Esto garantiza la coherencia entre lo que ven los alumnos en la interfaz de usuario y lo que ven los administradores en las exportaciones y los informes de cumplimiento.

#### Fin *a* flujo final

#### Para alumnos

1. Vaya a **Mi aprendizaje** o **Cursos completados** en la aplicación del alumno.
2. Revise las tarjetas de aprendizaje para identificar los cursos de formación marcados como **Completados mediante Alternativa**.
3. Abra una tarjeta de objeto de aprendizaje para ver los detalles sobre la formación de origen y la fecha de finalización.
4. Use el menú de filtros en las vistas de transcripción o de lista de cursos para seleccionar **Directo**, **Alternativo** o **Todo**.
5. Revise la lista actualizada en función del método de finalización seleccionado.

#### Para administradores y autores

1. Configure relaciones equivalentes o alternativas entre cursos o rutas de aprendizaje en la interfaz de administración.
2. Compruebe que las finalizaciones alternativas se reflejan correctamente en las tarjetas de aprendizaje y en los filtros que se muestran al alumno*.
3. Utilice las vistas e informes del alumno para confirmar la coherencia entre la interfaz de usuario y los datos exportados.
4. Si se retira o elimina un curso de formación de origen, valide la actualización correspondiente de las tarjetas de objetos de aprendizaje afectadas (por ejemplo, mostrando **Alternativo (revocado)** cuando corresponda).

## Comportamiento retroactivo de finalización e infinalización

ALM admite la finalización retroactiva y la finalización retroactiva para garantizar que las relaciones alternativas y equivalentes sigan siendo precisas a lo largo del tiempo, incluso cuando las relaciones se crean, modifican o eliminan después de que los alumnos hayan completado la formación.

### Finalización retroactiva

#### Definición

Cuando se habilita la finalización retroactiva, los alumnos que completaron un curso de origen en el pasado reciben automáticamente una finalización alternativa para el curso de destino si se crea una relación equivalente o alternativa más adelante.\
Esto garantiza que el aprendizaje histórico se respete sin que los alumnos tengan que volver a recibir formación.

#### Cómo funciona

1. Un administrador permite la finalización retroactiva en el nivel de cuenta.
2. El administrador define una relación equivalente o alternativa entre un curso de formación de origen y de destino.
3. El sistema analiza los registros de finalización históricos para la formación de origen.
4. Los alumnos que cumplen los requisitos obtienen una finalización alternativa para el curso de formación de destino.
5. Estos registros aparecen como **Completado mediante alternativo** en informes y transcripciones de alumnos.

### Incumplimiento retroactivo

#### Definición

Cuando se activa la finalización retroactiva, las finalizaciones alternativas se revocan si se elimina la relación equivalente o alternativa subyacente o si se elimina la formación de origen.\
Esto garantiza que el sistema refleje las relaciones de formación actuales y válidas.

#### Cómo funciona

1. Un administrador habilita la infinalización retroactiva en el nivel de cuenta.
2. El administrador elimina una relación alternativa o equivalente, o elimina el aprendizaje de origen.
3. El sistema identifica a los alumnos que han recibido una finalización alternativa a través de la relación afectada.
4. Se revocan los registros de finalización alternativos correspondientes.
5. Los registros revocados se marcan como **Alternativos (revocados)** en transcripciones e informes para la visibilidad de la auditoría.

### Incidencia en los requisitos previos

Las finalizaciones alternativas, incluidas las concedidas retroactivamente, se tratan como finalizaciones válidas al evaluar los requisitos previos.\
Si un alumno tiene **Completado mediante alternativo**, se le permite continuar con los cursos que requieren el entrenamiento de destino.

Si posteriormente se revoca una finalización alternativa mediante finalización retroactiva, el alumno puede dejar de cumplir los requisitos de los cursos que dependían de ese requisito previo.

### Impacto en las rutas de aprendizaje y las certificaciones

Las finalizaciones alternativas contribuyen al progreso y a la finalización de las rutas de aprendizaje y las certificaciones.\
Los alumnos pueden avanzar o completar estos programas cuando se cumplan los cursos de formación necesarios mediante relaciones alternativas o equivalentes.

Si se revoca una finalización alternativa, las certificaciones o rutas de aprendizaje afectadas pueden perder el progreso o el estado de finalización hasta que se cumpla el requisito mediante una finalización válida.

### Finalizar *a* flujo de trabajo

#### Activación de la finalización o infinalización retroactivas

1. Los administradores pueden acceder a la configuración de la cuenta y activar la finalización retroactiva o la finalización retroactiva.
2. Los administradores pueden crear, modificar o eliminar relaciones equivalentes o alternativas entre los cursos de formación.

#### Acciones del sistema

* **Para la finalización retroactiva:**\
  El sistema concede finalizaciones alternativas basadas en finalizaciones de fuentes históricas.
* **Por infinalización retroactiva:**\
  El sistema revoca las finalizaciones alternativas cuando se eliminan relaciones o se eliminan cursos de formación de origen.

#### Experiencia del alumno

Los alumnos ven estados de finalización actualizados en las tarjetas de objetos de aprendizaje y en las transcripciones, como:

* **Completado a través de Alternate**
* **Alternativa (revocada)**

Las comprobaciones de requisitos previos, el progreso de la ruta de aprendizaje y el estado de certificación se actualizan dinámicamente en función del estado de finalización actual.

#### Informes y auditoría

Todos los cambios retroactivos se reflejan en el informe Transcripciones de aprendizaje (LT).\
Los informes distinguen claramente entre finalizaciones directas, finalizaciones alternativas y finalizaciones alternativas revocadas para respaldar el cumplimiento, apoyar las investigaciones y las auditorías.

### Comportamiento retroactivo de finalización e infinalización

ALM admite la finalización retroactiva y la finalización retroactiva para garantizar que las relaciones alternativas y equivalentes sigan siendo precisas a lo largo del tiempo, incluso cuando las relaciones se crean, modifican o eliminan después de que los alumnos hayan completado la formación.

#### Finalización retroactiva

#### Definición

Cuando se habilita la finalización retroactiva, los alumnos que completaron un curso de origen en el pasado reciben automáticamente una finalización alternativa para el curso de destino si se crea una relación equivalente o alternativa más adelante.\
Esto garantiza que el aprendizaje histórico se respete sin que los alumnos tengan que volver a recibir formación.

#### Cómo funciona

1. Un administrador permite la finalización retroactiva en el nivel de cuenta.
2. El administrador define una relación equivalente o alternativa entre un curso de formación de origen y de destino.
3. El sistema analiza los registros de finalización históricos para la formación de origen.
4. Los alumnos que cumplen los requisitos obtienen una finalización alternativa para el curso de formación de destino.
5. Estos registros aparecen como **Completado mediante alternativo** en informes y transcripciones de alumnos.

#### Incumplimiento retroactivo

#### Definición

Cuando se activa la finalización retroactiva, las finalizaciones alternativas se revocan si se elimina la relación equivalente o alternativa subyacente o si se elimina la formación de origen.\
Esto garantiza que el sistema refleje las relaciones de formación actuales y válidas.

#### Cómo funciona

1. Un administrador habilita la infinalización retroactiva en el nivel de cuenta.
2. El administrador elimina una relación alternativa o equivalente, o elimina el aprendizaje de origen.
3. El sistema identifica a los alumnos que han recibido una finalización alternativa a través de la relación afectada.
4. Se revocan los registros de finalización alternativos correspondientes.
5. Los registros revocados se marcan como **Alternativos (revocados)** en transcripciones e informes para la visibilidad de la auditoría.

#### Incidencia en los requisitos previos

Las finalizaciones alternativas, incluidas las concedidas retroactivamente, se tratan como finalizaciones válidas al evaluar los requisitos previos.\
Si un alumno tiene **Completado mediante alternativo**, se le permite continuar con los cursos que requieren el entrenamiento de destino.

Si posteriormente se revoca una finalización alternativa mediante finalización retroactiva, el alumno puede dejar de cumplir los requisitos de los cursos que dependían de ese requisito previo.

#### Impacto en las rutas de aprendizaje y las certificaciones

Las finalizaciones alternativas contribuyen al progreso y a la finalización de las rutas de aprendizaje y las certificaciones.\
Los alumnos pueden avanzar o completar estos programas cuando se cumplan los cursos de formación necesarios mediante relaciones alternativas o equivalentes.

Si se revoca una finalización alternativa, las certificaciones o rutas de aprendizaje afectadas pueden perder el progreso o el estado de finalización hasta que se cumpla el requisito mediante una finalización válida.

#### Finalizar *a* flujo de trabajo

#### Activación de la finalización o infinalización retroactivas

1. Los administradores pueden acceder a la configuración de la cuenta y activar la finalización retroactiva o la finalización retroactiva.
2. Los administradores pueden crear, modificar o eliminar relaciones equivalentes o alternativas entre los cursos de formación.

#### Acciones del sistema

* **Para la finalización retroactiva:**\
  El sistema concede finalizaciones alternativas basadas en finalizaciones de fuentes históricas.
* **Por infinalización retroactiva:**\
  El sistema revoca las finalizaciones alternativas cuando se eliminan relaciones o se eliminan cursos de formación de origen.

#### Experiencia del alumno

Los alumnos ven estados de finalización actualizados en las tarjetas de objetos de aprendizaje y en las transcripciones, como:

* **Completado a través de Alternate**
* **Alternativa (revocada)**

Las comprobaciones de requisitos previos, el progreso de la ruta de aprendizaje y el estado de certificación se actualizan dinámicamente en función del estado de finalización actual.

#### Informes y auditoría

Todos los cambios retroactivos se reflejan en el informe Transcripciones de aprendizaje (LT).\
Los informes distinguen claramente entre finalizaciones directas, finalizaciones alternativas y finalizaciones alternativas revocadas para respaldar el cumplimiento, apoyar las investigaciones y las auditorías.

### Webhooks para equivalentes y alternativas

ALM proporciona eventos webhook dedicados para finalizaciones equivalentes y alternativas para admitir la automatización, integraciones y sincronización con sistemas externos.

Estos acontecimientos permiten a los consumidores externos distinguir de manera fiable entre las finalizaciones directas y las realizadas mediante relaciones alternativas o equivalentes.

#### Información general

Cuando un alumno finaliza un curso mediante una relación alternativa o equivalente, ALM activa un evento webhook que es independiente del webhook de finalización del curso estándar.\
Esto garantiza que las integraciones puedan responder de forma diferente a las finalizaciones alternativas cuando sea necesario.

Los eventos Webhook también se activan cuando se produce la finalización retroactiva o la infinalización retroactiva, lo que abarca las actualizaciones históricas, así como los cambios en las relaciones.

#### Comportamiento del evento Webhook

* Un evento webhook distinto se activa cuando un alumno recibe el estado **Completado mediante alternativo** de un curso de destino.
* El evento se genera cuando el alumno finaliza un curso de origen configurado que satisface el destino mediante una relación equivalente o alternativa.
* Este webhook no se activa para las finalizaciones directas del curso.
* Cuando se activa la finalización retroactiva o la finalización retroactiva, se emiten eventos webhook para cada curso de alumno y destino afectado.

#### Detalles de carga útil Webhook

La carga útil de webhook de finalización alternativa incluye los siguientes atributos clave:

* **Id. del alumno**\
  Identifica el alumno que recibió la finalización alternativa.

* **Curso de origen**\
  El curso o la ruta de aprendizaje que el alumno ha completado directamente.

* **Curso de destino**\
  El curso marcado como completado mediante la relación alternativa o equivalente.

* **Método de finalización**\
  Indica que el método de finalización es **alternativo**.

* **Fecha de finalización**\
  Se deriva de la fecha de finalización del curso de origen.

* **Tipo de relación**\
  Especifica si la relación es **equivalente** o **alternativa**.

Para escenarios de finalización retroactiva, los eventos webhook indican que se ha revocado una finalización alternativa existente.

#### Consideraciones de integración

Los sistemas externos pueden utilizar estos eventos webhook para:

* Actualizar registros de alumnos
* Sincronizar estado de finalización
* Notificaciones de activadores o flujos de trabajo descendentes
* Mantener registros de auditoría para fines de cumplimiento

Los consumidores de webhook deben diferenciar explícitamente entre las finalizaciones **direct** y **alternative**.\
Las finalizaciones alternativas no otorgan habilidades, insignias ni recompensas por interacción lúdica y deben gestionarse en consecuencia en sistemas descendentes.

### Consecuencias de retirar y suprimir la formación inicial en equivalentes y suplentes

El estado del ciclo de vida de un curso de formación de origen (retirado o eliminado) afecta directamente al modo en que se mantienen las finalizaciones alternativas y equivalentes para los alumnos. ALM maneja estos escenarios de manera diferente para preservar la precisión histórica mientras garantiza que las relaciones actuales sigan siendo válidas.

#### Retirada de formación de origen

##### Definición

Al retirar un curso, este no está disponible para nuevas inscripciones y, al mismo tiempo, lo mantiene en el sistema con fines de referencia histórica, informes y auditoría.

##### Consecuencias

* Las finalizaciones alternativas existentes concedidas a través del curso de origen retirado siguen siendo válidas.
* Los alumnos que hayan completado anteriormente el curso de origen seguirán realizando una finalización alternativa para el curso de destino.
* No se generan nuevas finalizaciones alternativas a partir del curso retirado, ya que los nuevos alumnos no pueden completarlo.
* Las transcripciones de alumnos y los informes siguen mostrando **Completado mediante alternativo** para los alumnos afectados.

#### Eliminación de formación de origen

#### Definición

Al eliminar un curso, se elimina por completo del sistema, incluidos sus registros de finalización y las relaciones configuradas.

#### Consecuencias

* Si se activa la finalización retroactiva, se revocan todas las finalizaciones alternativas concedidas a través del curso de origen eliminado.
* Las transcripciones de alumnos y los informes se actualizan para mostrar **Alternativa (revocada)** para la visibilidad de la auditoría y el cumplimiento normativo.
* Los alumnos pueden perder el progreso o el estado de finalización en rutas de aprendizaje, certificaciones o requisitos previos que dependían de la finalización alternativa revocada.
* No se pueden conceder más finalizaciones alternativas del curso eliminado.

#### Flujo de trabajo

1. Un administrador retira o elimina el curso de origen mediante la interfaz de administración.
2. El sistema evalúa todas las finalizaciones alternativas y equivalentes derivadas del curso de origen.
3. El estado de finalización se actualiza en función del estado del curso:
   * **Retirado:** Las finalizaciones alternativas existentes no cambian.
   * **Eliminado:** Las finalizaciones alternativas se revocan si está habilitada la infinalización retroactiva.
4. Las transcripciones de alumnos y los informes reflejan el estado actualizado para cumplir los requisitos de cumplimiento y auditoría.

### Sin encadenamiento de relaciones

ALM no admite el encadenamiento de relaciones alternativas o equivalentes. Las finalizaciones alternativas se conceden solo para relaciones configuradas directamente y no se aplican en cascada en varios niveles de cursos.

#### Concepto: no encadenar relaciones

#### Definición

El encadenamiento se refiere a permitir que relaciones alternativas o equivalentes se propaguen a través de varios cursos.\
Por ejemplo, si el curso A es una alternativa para el curso B y el curso B es una alternativa para el curso C, el encadenamiento implicaría que la finalización del curso A otorga la finalización del curso C.

#### Política

No se admite el encadenamiento.\
Las relaciones alternativas y equivalentes solo se evalúan en un solo nivel. Completar un curso de origen concede la finalización alternativa solo a su curso o cursos de destino inmediato, no a ningún destino descendente.

#### Flujo de trabajo

#### Configuración de relaciones

Un administrador define relaciones alternativas o equivalentes entre cursos, como:

* Curso A → Curso B
* Curso B → Curso C

#### Evento de finalización

Un alumno completa directamente el curso A.

#### Acción del sistema

* El sistema concede una finalización alternativa para el curso B, si se ha definido la relación A → B.
* El sistema no concede una finalización alternativa para el curso C, incluso si existe una relación entre B y C.

#### Requisito de finalización directa

Para recibir una finalización alternativa del curso C, el alumno debe:

* Completar directamente el curso B, o
* Complete un curso configurado explícitamente como alternativa directa o equivalente para el curso C.

### Implicaciones

#### Sin beneficios indirectos

Los alumnos no pueden recibir créditos de finalización para cursos que se encuentran más abajo en una cadena de relación a menos que se complete cada curso (o su alternativa directa).\
Esto garantiza que los requisitos de aprendizaje se cumplan de forma explícita y predecible.

#### Auditoría e informes simplificados

Los informes y las transcripciones de alumnos muestran finalizaciones alternativas solo para relaciones directas.\
Esto evita pistas de auditoría complejas y de varios saltos y garantiza la claridad al revisar cómo se concedió una finalización.

### Uso compartido de catálogos con cuentas de igual a igual: relaciones no compartidas

El uso compartido de catálogos permite compartir objetos de aprendizaje entre cuentas de igual a igual, pero las relaciones alternativas y equivalentes se administran independientemente dentro de cada cuenta y no se comparten.

#### Concepto: uso compartido de catálogos y relaciones

#### Uso compartido de catálogos

Las cuentas pueden compartir catálogos con cuentas de igual a igual para proporcionar acceso a cursos, rutas de aprendizaje y otros objetos de aprendizaje en las cuentas.

#### Relaciones no compartidas

Las relaciones alternativas, equivalentes y de finalización alternativa configuradas en la cuenta de origen no se comparten ni replican cuando se comparte un catálogo.\
Cada cuenta mantiene y evalúa sus propias relaciones de forma independiente.

### Flujo de trabajo

#### Uso compartido de catálogos

Un administrador de **Cuenta A** comparte un catálogo que contiene objetos de aprendizaje con **Cuenta B**.

#### Configuración de relaciones

La cuenta A puede tener relaciones alternativas o equivalentes definidas entre los objetos de aprendizaje del catálogo compartido.

#### Acceso a cuentas de igual a igual

La cuenta B recibe acceso a los objetos de aprendizaje compartidos, pero no hereda ninguna relación alternativa o equivalente configurada en la cuenta A.

#### Gestión independiente

Si la cuenta B requiere un comportamiento alternativo o equivalente similar, un administrador de la cuenta B debe configurar manualmente las relaciones dentro de esa cuenta.

#### Implicaciones

#### Sin propagación automática de relaciones

Las relaciones alternativas y equivalentes no están disponibles automáticamente en las cuentas de igual a igual mediante el uso compartido de catálogos.

#### Se requiere configuración manual

Cada cuenta de igual a igual es responsable de definir y administrar sus propias relaciones para los objetos de aprendizaje compartidos.

#### Consideraciones de coherencia

El comportamiento de finalización, la satisfacción de los requisitos previos y la generación de informes pueden diferir entre cuentas a menos que las relaciones se alineen intencionadamente mediante la configuración manual.


### Comportamiento descendente

Una vez que existe una finalización alternativa para un curso de formación de destino, ALM la utiliza en las comprobaciones descendentes:

* Si el curso de formación de destino es un **requisito previo** para otros cursos de formación, el alumno cumple los requisitos para recibir esos cursos de formación como si hubiera completado el curso de formación de destino.
* Si el destino es un **curso obligatorio en una ruta de aprendizaje**, la lógica de finalización de la ruta puede tratar al alumno como que ha completado esa parte y proceder a marcar la ruta como completada cuando se cumplan otras condiciones.
* El cumplimiento normativo y otros paneles, como el panel de éxito de grupo, que dependen de si se cumple un requisito de formación pueden incluir alumnos que solo tienen finalizaciones alternativas.

El sistema distingue entre finalización real y finalización alternativa de modo que:

* Si más tarde el alumno realiza directamente el curso de formación de destino y lo completa, esta finalización directa puede anular la necesidad de la finalización alternativa.
* Si se elimina o se cambia la relación entre el origen y el destino, ALM puede eliminar o ajustar las finalizaciones alternativas sin tocar las finalizaciones originales, siempre que se habiliten las finalizaciones retroactivas para la cuenta.

Las finalizaciones alternativas están diseñadas para no interferir con la actividad real del alumno en el curso de formación de destino. Actúan como una superposición que se puede revisar si cambian las relaciones.