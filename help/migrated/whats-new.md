---
title: Novedades de esta versión
description: Obtenga más información sobre las nuevas funciones y mejoras de Adobe Learning Manager
source-git-commit: 655c94f0faaa6c025e07b11d3d9bfac4f221f899
workflow-type: tm+mt
source-wordcount: '2372'
ht-degree: 0%

---

# Novedades de esta versión

## Interfaz de usuario renovada

La interfaz de usuario de Adobe Learning Manager se ha actualizado para ofrecer una experiencia más limpia y moderna. Se han renovado las páginas de aterrizaje de las funciones de administrador y autor, y se han realizado actualizaciones de los temas de la interfaz de usuario para todas las funciones. Sin embargo, no se ha realizado ningún cambio en la ubicación de los menús, botones o vínculos y podrá encontrarlos exactamente donde se encontraban antes.

Las actualizaciones de temas se aplicarán automáticamente a las cuentas que utilicen el tema predeterminado. Las actualizaciones del tema de la interfaz de usuario no afectarán a las cuentas que hayan realizado modificaciones para utilizar un tema personalizado. Estas cuentas deben volver al tema predeterminado para obtener las actualizaciones del nuevo tema.

![Imagen de IU](assets/refreshed-ui.png)

*Interfaz de usuario renovada de Adobe Learning Manager*

### Acerca de este cambio

**¿Qué cambios se han producido en esta versión?**

Hay una nueva plantilla en el encabezado que ajusta automáticamente el logotipo a un tamaño y una posición fijos, manteniendo la proporción de aspecto del logotipo. El cambio pretende mejorar el atractivo visual de la experiencia del alumno.

El nombre de la organización en el encabezado también cambia de tamaño automáticamente a 336 (mínimo) x 680 (máximo) px para los alumnos.

**¿Cuál es el tamaño recomendado del logotipo?**

La anchura máxima del logotipo es de 210 px. Los logotipos con una anchura superior a 210 px o una altura superior a 42 px cambian de tamaño a 42 x 210 px.

Si el tamaño del logotipo es inferior al recomendado, el logotipo se carga sin cambios y se alinea al centro.

**¿Cuál es el impacto?**

Los nombres de las empresas que sean más largos se recortarán y los puntos suspensivos rellenarán el espacio.

**¿Qué recomendamos?**

* Cambie el tamaño de la imagen manteniendo intacta la relación de aspecto. El tamaño máximo recomendado del logotipo es de 42 px (vertical) x 210 px (horizontal).
* Para muchas cuentas, esto se aplicaría automáticamente; no se requiere ningún cambio.

## Extensibilidad nativa

Configura experiencias personalizadas en la versión nativa de Adobe Learning Manager, lo que te permite no usar el enfoque descentralizado en casos menos complicados. También puede crear aplicaciones personalizadas y colocarlas en distintos puntos de la versión nativa de los flujos de trabajo de alumno, responsable, administrador, autor o instructor.

Un alumno puede utilizar una aplicación personalizada o una extensión creada por un administrador.

Ver [Extensibilidad nativa](/help/migrated/administrators/feature-summary/native-extensibility.md) para obtener más información.

## Herramienta de creación de pruebas

Ahora podrá crear evaluaciones en Learning Manager con la nueva herramienta de creación de pruebas en la página Biblioteca de contenido. Las evaluaciones creadas pasan a formar parte de la biblioteca de contenido y se pueden añadir a una carpeta &quot;pública&quot; para reutilizar el curso.

Ver [Crear una prueba](/help/migrated/authors/feature-summary/content-library.md) para obtener más información.

## Informar de cambios en esta versión

### Cambios en el informe de inscripción de ayudas de trabajo

En versiones anteriores de Adobe Learning Manager, el informe de inscripción de ayudas de trabajo no tenía filtros. Adobe Learning Manager descargó todos los datos de una cuenta.

En esta versión, hemos añadido un menú desplegable en el cuadro de diálogo Informe de ayudas de trabajo.

### Cambios en el informe de anuncio de notificaciones

En versiones anteriores de Adobe Learning Manager, el informe Anuncio de notificación no tenía filtros. Adobe Learning Manager descargó todas las notificaciones de la cuenta.

En esta versión, hemos añadido un filtro de fecha, mediante el cual puede descargar las notificaciones dentro de un período especificado.  Sin embargo, puede descargar el informe sólo durante los últimos seis meses.

### Cambios en los datos de revisión de cursos en el informe de inscripción

En esta versión, puede descargar la información de revisión del curso en un informe de inscripción especificando una hora. El período de descarga se limitará a seis meses para las cuentas con más de cinco millones de inscripciones. Para todas las demás cuentas, el período será de 15 meses.

Puede descargar el informe desde **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes históricos]** > **[!UICONTROL Informe de acceso al curso]**.

### Cambios en la transcripción del alumno

En versiones anteriores de Adobe Learning Manager, si un administrador personalizado tenía ámbito de usuario, la transcripción de aprendizaje contenía los usuarios eliminados. En esta versión, la transcripción de aprendizaje contendrá los usuarios eliminados si el administrador personalizado tiene ámbito de usuario o acceso a todos los grupos de usuarios.

### Cambios en el informe de asistencia

El informe de asistencia de la página Asistencia de cursos de la aplicación de administración y de la página Alumnos de la sesión de la aplicación del instructor se utilizaba para descargar de forma sincrónica. En esta versión, este informe se descargará de forma asincrónica a través de una notificación.

Para obtener más información sobre los informes, consulte [Informes](/help/migrated/administrators/feature-summary/reports.md) en Adobe Learning Manager.

## Retirada de Mercado de contenido

Los cursos que hayan caducado en el catálogo de la tienda de contenido importado (formación empresarial) se eliminarán automáticamente una vez que caduquen. Los cursos se configurarán para que se retiren cuando se marque el contenido para su retirada. Los alumnos inscritos existentes pueden consumirlos en un período de tiempo limitado tras el cual se eliminarán. Esto mantendrá el catálogo limpio y no mostrará a los usuarios ningún curso caducado.

## Nuevas recomendaciones basadas en habilidades

Adobe Learning Manager mejora las recomendaciones para las cuentas habilitadas para clientes y partners. Esta mejora en el algoritmo de recomendación con el cambio en el algoritmo de clasificación para cursos, rutas de aprendizaje y certificaciones proporciona una mejor experiencia del usuario en la detección de contenido.

El algoritmo ya no permitirá recomendaciones basadas en pares. El cambio no afectará a los usuarios existentes, pero la opción Adaptado al sector seguirá existiendo. Para la opción Personalizado, Adobe Learning Manager ya no permitirá la selección personalizada basada en compañeros.

El grupo de compañeros ahora se convierte en una cuenta y los alumnos verán una cadena que muestra los temas de tendencia del grupo. Todas las recomendaciones son explicables. Por ejemplo, si está viendo algo sobre un tema, la tarjeta de la tira mostrará el motivo del curso.

## Mejoras del flujo de trabajo de administrador personalizado

Los administradores personalizados ahora tendrán más paridad con las funciones de administrador en lo que respecta al acceso a los informes. Los administradores podrán configurar el acceso de informes con un mejor control.

En Adobe Learning Manager, solo la transcripción de aprendizaje y la transcripción de interacción están disponibles para un administrador personalizado. En esta versión, un administrador personalizado puede acceder a todos los informes personalizados, excepto a los informes de xAPI y de correo electrónico, que siguen estando disponibles solo para el administrador. El acceso a todos los informes está sujeto al catálogo y al ámbito de usuario que tenga el administrador personalizado. Hay pocos informes que sólo estén disponibles con un ámbito completo. Estos son:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Informe</b></p></td>
   <td>
    <p style="text-align: left;"><b>Disponible</b></p></td>
   <td>
    <p style="text-align: left;"><b>Ámbito</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Registro de auditoría de contenido</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Catálogo completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Registro de auditoría de usuarios</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Usuario completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Acceso de inicio de sesión</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Usuario completo</p></td>
  </tr>
    </tbody>
</table>

**Nuevos controles de solo lectura**

En la página Funciones personalizadas, hemos añadido las siguientes opciones de solo lectura para permitir a los administradores proporcionar opciones más flexibles al administrador personalizado: El administrador personalizado ahora tendrá permiso adicional de solo lectura para usuarios, plantillas de correo electrónico y planes de aprendizaje.

**Usuarios**:

Si selecciona Solo lectura, el administrador personalizado podrá ver todos los usuarios, pero no podrá editar los datos de los usuarios, y crear un portal de registro automático para los usuarios.

**Planes de aprendizaje**:

Si selecciona Solo lectura, un administrador personalizado no podrá añadir ni editar un plan de aprendizaje. Pueden descargar un informe del plan de aprendizaje y ver sus detalles. Pero no pueden cambiar los detalles del curso.

>[!NOTE]
>
>Los planes de aprendizaje serán de solo lectura adicional, junto con un control total.

**Plantillas de correo electrónico**

Si selecciona Solo lectura, un administrador personalizado puede ver las plantillas de correo electrónico. No pueden habilitar ni deshabilitar la configuración de la plantilla de correo electrónico, pero pueden descargar informes de acceso a correo electrónico.

### Transcripciones de alumnos

Si se selecciona el permiso Usuario o Todos los grupos de usuarios y el administrador personalizado intenta descargar transcripciones de alumnos, la opción Incluir alumnos eliminados devolverá todos los alumnos eliminados del informe.

### Informes

Un administrador personalizado puede acceder a los siguientes informes según el ámbito definido:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Informe</b></p></td>
   <td>
    <p style="text-align: left;"><b>Disponible</b></p></td>
   <td>
    <p style="text-align: left;"><b>Ámbito</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Registro de auditoría de contenido</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Catálogo completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Registro de auditoría de usuarios</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Usuario completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Acceso de inicio de sesión</p></td>
   <td>
    <p>Sí</p></td>
   <td>
    <p>Usuario completo</p></td>
  </tr>
    </tbody>
</table>

<!--| Report | Available | Scope |
|--- |--- |
| Content Audit Trail | Yes | Full Catalog |
| User Audit Trail | Yes | Full User |
|Login Access | Yes | Full User |-->

## Integración de Connect mejorada

Los instructores pueden personalizar la experiencia de su sesión seleccionando salas específicas para cada instructor. En esta versión, hemos realizado las siguientes mejoras:

### Importar transcripciones

Podrá importar transcripciones de sesiones desde Connect y analizar las transcripciones. Los alumnos recibirán la transcripción después de la grabación, que podrán descargar más tarde.

### Editar vídeos

Los instructores pueden editar el vídeo y mejorar la experiencia de visualización de los alumnos. Los instructores verán un vínculo en la página Introducción a la sesión para llevarlos a la página de inicio de sesión de Adobe Connect. Después de iniciar sesión, el instructor verá el vínculo de grabación. Al hacer clic en el vínculo, se les redirigirá al vídeo, que pueden recortar.

## Restringir informes de tablero a usuarios con la función de responsable

Los administradores solo pueden buscar responsables en los informes del tablero.

## Limitar el procesamiento de informes de tableros heredados

Cuando un administrador intenta trazar un informe del tablero y el informe tarda demasiado en trazarse (más de 2,5 minutos), Adobe Learning Manager muestra el siguiente mensaje:

![imagen de informe heredada](assets/error-message.png)
*Mensaje de error cuando el informe tarda demasiado*

Los informes de esta magnitud no se pueden mostrar en la interfaz de usuario, pero el administrador puede descargarlos.

## Compatibilidad de migración para etiquetas de catálogo

El flujo de trabajo de migración ahora admite etiquetas de catálogo. Los archivos CSV de migración se pueden utilizar para importar claves de etiquetas de catálogo y valores de etiquetas de catálogo y adjuntarlos a cursos, rutas de aprendizaje, certificaciones y ayudas de trabajo. El flujo de trabajo también se puede utilizar para eliminar valores y claves incorrectos si es necesario.

## Mejoras de la API para el filtrado complejo de cursos

El filtrado avanzado de cursos mediante etiquetas y etiquetas de catálogo (mediante una combinación de condiciones &quot;AND&quot; y &quot;OR&quot;) ahora será posible mediante las API de Learning Manager.

## Cambios en la API en esta versión

### Validación en la API del trabajo

En esta versión, si el informe de ayuda de trabajo supera los 10 millones generados mediante la API de trabajo, la respuesta mostrará el mensaje: &quot;El informe solicitado tiene demasiados datos que generar. Plantéese aplicar filtros de ayuda de trabajo&quot;.

### Notificación de una publicación eliminada

En las versiones anteriores de Adobe Learning Manager, si se elimina cualquier curso, certificación o plan de aprendizaje y se muestra una notificación, podría seguir accediendo al curso, certificación o plan de aprendizaje si visita la notificación.

En esta versión, nos aseguraremos de que ya no se pueda acceder a una publicación eliminada. Si especifica el id en la opción /posts/{id} API, y el ID de la publicación ya no está disponible, la API muestra el mensaje &quot;Publicación no encontrada para el recurso especificado&quot;.

### Fecha límite de finalización de API de alumno

En versiones anteriores, Adobe Learning Manager obtenía la fecha límite de la tabla de inscripción. En esta versión, Adobe Learning Manager calculará la fecha límite en la tabla de instancias del curso. Si la fecha límite no está disponible, volverá a la tabla de inscripción.

### Anular indicador

En la versión de noviembre de 2023 de Adobe Learning Manager, se dejará de incluir el indicador de anulación en las API. El indicador override no forma parte de la especificación de la API pública y está pensado para pruebas de backend. El indicador ya no está disponible para las API de alumno. Sin embargo, el indicador sigue siendo válido para las API de administración.

La razón por la que estamos dejando de utilizar el indicador para las API de alumno es que el indicador de anulación obtenía una gran cantidad de datos a través de las API de alumno.

En adelante, la siguiente API de alumno dejará de funcionar porque tiene el indicador de anulación.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Resaltar resultados

En la próxima versión de Adobe Learning Manager, por ejemplo, en la API /search, estamos cambiando el valor predeterminado de highlightResults a false.

Además, cambiaremos el valor predeterminado de snippetTypes a courseName. Al hacerlo, solo se resaltarán los nombres de los cursos en la búsqueda si highlightResults es True.

### Nuevo tipo de recurso para la prueba

La `instances.loResources.resources` punto final devolverá `ResourceContentType` con Quiz.

## Aviso de desaprobación

El 30 de noviembre de 2023, LinkedIn Learning dejará de utilizar el método de GET HTTP para obtener un token de OAuth. Después de la degradación, solo podrá generar un token de OAuth mediante el método del POST HTTP.
Adobe Learning Manager dejará de ofrecer BlueJeans en febrero de 2024. Todas las cuentas nuevas posteriores a febrero de 2024 no incluirán el conector de BlueJeans.

## Notas de la versión

Para obtener información sobre las versiones actuales y anteriores de la aplicación web y para dispositivos de Learning Manager, consulte la [Notas de la versión](release-note/release-notes.md).

## Errores corregidos en esta versión

* Una miniatura de un curso, que es un requisito previo para una ruta de aprendizaje u otro curso, no se muestra cuando un alumno abre la página de vista previa de la ruta de aprendizaje o el curso.
* Si no se seleccionan las opciones Calendario, Interacción y Aprendizaje social, la configuración del tablero del alumno no conserva la siguiente configuración. Las opciones como Recomendado en las áreas de interés y Examinar por catálogo no aparecen como seleccionadas, sino que se muestran en la vista previa.
* Incluso después de que un alumno complete un curso de clase virtual, recibirá un correo electrónico de recordatorio para completar el curso.
* En el caso de las cuentas de igual a igual, no es posible descargar informes del tablero.
* Si se elimina y se añade un módulo de lista de comprobación en un curso, se produce un error interno.
* En el caso de las plantillas de invitación de sesión, el ID de correo electrónico del remitente tiene el texto captivatePrime en lugar de AdobeLearningManager.
* Cuando se utiliza la eficacia del curso como eje Y secundario, la descarga del informe falla con una excepción de puntero nulo.
* Si a un alumno se le asigna una función de administrador personalizado, se desplaza al perfil de administrador personalizado de forma predeterminada. Sin embargo, cuando se establece una URL de redirección del alumno en la cuenta, el administrador personalizado se lleva a otro destino, no al perfil de la función de administrador personalizado.
* El ámbito de interacción no funciona del modo esperado si disabled_sub_groups se establece en un número grande.
* En algunos casos, los usuarios eliminados activan una migración.
* Un alumno no puede reproducir cursos de LinkedIn en la aplicación MS Teams.
* La API de inscripción no devuelve las inscripciones en un plan de aprendizaje de Flex o un plan de aprendizaje incrustado como se esperaba.
* En la aplicación móvil, los nombres de un curso, una certificación o un plan de aprendizaje aparecen en minúsculas.
* En las versiones anteriores de Adobe Learning Manager, si se elimina cualquier curso, certificación o plan de aprendizaje y se muestra una notificación, podría seguir accediendo al curso, certificación o plan de aprendizaje si visita la notificación. En esta versión, nos aseguraremos de que ya no se pueda acceder a una publicación eliminada. Si especifica el id en la opción /posts/{id} API, y el ID de la publicación ya no está disponible, la API muestra el mensaje &quot;Publicación no encontrada para el recurso especificado&quot;.
* En la API del alumno, el campo de fecha límite de finalización no se muestra en la respuesta de la API de inscripción.
* En la API Obtener inscripción para alumnos, los detalles de inscripción aparecen incluso después de especificar un ID de instancia incorrecto.

## Problemas conocidos de esta versión

* Una nueva inscripción o la actualización de una inscripción fallan cuando un plan de aprendizaje de Flex está dentro de otro plan de aprendizaje de Flex.
* La URL de transcripción no muestra las grabaciones de sesiones en sesiones de Adobe Connect.
* Un alumno puede realizar una prueba sin conexión en la aplicación móvil aunque no la supere.

## Requisitos del sistema

[Requisitos del sistema de Learning Manager](system-requirements.md)

## Versiones anteriores de Adobe Learning Manager

<!--* [November 2023 release](whats-new-november-2023.md)-->
* [Versión de julio de 2023](whats-new-2023-july.md)
* [Versión de abril de 2023](whats-new-2023-april.md)
