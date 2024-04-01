---
title: Novedades de esta versión
description: Obtenga más información sobre las nuevas funciones y mejoras de la versión de noviembre de 2023 de Adobe Learning Manager.
exl-id: d670dc47-d57f-464a-bee8-064cc16e59f9
source-git-commit: 447a4e041d74cf086afada3794ac08a04e70c2ca
workflow-type: tm+mt
source-wordcount: '2373'
ht-degree: 70%

---

# Novedades de esta versión

## Interfaz de usuario renovada

La interfaz de usuario de Adobe Learning Manager se ha actualizado para ofrecer una experiencia más limpia y moderna. Se han renovado las páginas de inicio para las funciones de administrador y autor, y se han actualizado los temas de la interfaz de usuario para todas las funciones. Sin embargo, no se ha realizado ningún cambio en la ubicación de los menús, botones o vínculos y podrá encontrarlos exactamente donde se encontraban antes.

Las actualizaciones del tema se aplicarán automáticamente a las cuentas que utilicen el tema predeterminado. Las actualizaciones del tema de la interfaz de usuario no afectarán a las cuentas que hayan realizado modificaciones para utilizar un tema personalizado. Estas cuentas deben volver al tema predeterminado para obtener las actualizaciones del nuevo tema.

![Imagen de IU](assets/refreshed-ui.png)

### Acerca de este cambio

**¿Qué cambios incluye esta versión?**

Hay una nueva plantilla en el encabezado, que ajusta automáticamente el logotipo a un tamaño y posición fijos, manteniendo su relación de aspecto. El cambio pretende mejorar el atractivo visual de la experiencia del alumno.

El tamaño del nombre de la organización del encabezado también se ha ajustado automáticamente a 336 (mínimo) x 680 (máximo) px para los alumnos.

**¿Cuál es el tamaño recomendado del logotipo?**

La anchura máxima del logotipo es de 210 px. Los logotipos con una anchura superior a 210 px o una altura superior a 42 px cambian de tamaño a 42 x 210 px.

Si el tamaño del logotipo es inferior al recomendado, este se cargará sin cambios y se alineará en el centro.

**¿Cuál es el impacto?**

Los nombres de empresas que sean más largos se recortarán y se rellenará el espacio con puntos suspensivos.

**¿Qué recomendamos?**

* Cambie el tamaño de la imagen manteniendo intacta la relación de aspecto. El tamaño máximo recomendado del logotipo es de 42 px (vertical) x 210 px (horizontal).
* En muchas cuentas, esto se aplicará automáticamente; no es necesario ningún cambio.

## Extensibilidad nativa

Configure experiencias personalizadas en la versión nativa de Adobe Learning Manager, por lo que no será necesario que utilice una interfaz sin encabezado en casos de uso menos complicados. También puede crear aplicaciones personalizadas y colocarlas en distintos puntos de la versión nativa de los flujos de trabajo del alumno, el responsable, el administrador, el autor o el instructor.

Un alumno puede utilizar una aplicación personalizada o una extensión creada por un administrador.

Consulte [Extensibilidad nativa](/help/migrated/administrators/feature-summary/native-extensibility.md) para obtener más información.

## Herramienta de creación de pruebas

Ahora podrá crear evaluaciones en Learning Manager con la nueva herramienta de creación de pruebas en la página Biblioteca de contenido. Las evaluaciones creadas pasan a formar parte de la biblioteca de contenido y se pueden añadir a una carpeta &quot;pública&quot; para reutilizar el curso.

Ver [Crear una prueba](/help/migrated/authors/feature-summary/content-library.md) para obtener más información.

## Cambios de esta versión relacionados con los informes

### Cambios en el informe de inscripción de ayudas de trabajo

En versiones anteriores de Adobe Learning Manager, el informe de inscripción de ayudas de trabajo no incluía filtros. Adobe Learning Manager ha descargado todos los datos de una cuenta.

En esta versión, hemos añadido un menú desplegable en el cuadro de diálogo Informe de ayudas de trabajo.

### Cambios en el informe de anuncio de notificaciones

En versiones anteriores de Adobe Learning Manager, el informe Anuncio de notificación no tenía filtros. Adobe Learning Manager ha descargado todas las notificaciones de la cuenta.

En esta versión, hemos añadido un filtro de fecha, mediante el cual puede descargar las notificaciones dentro de un período especificado.  Sin embargo, puede descargar el informe sólo durante los últimos seis meses.

### Cambios en los datos de revisión de cursos en el informe de inscripción

En esta versión, puede descargar la información de revisión del curso en un informe de inscripción. Para ello, especifique una hora. El periodo de descarga se limitará a seis meses para las cuentas con más de cinco millones de inscripciones. Para todas las demás cuentas, el periodo será de 15 meses.

Puede descargar el informe desde **[!UICONTROL Informes]** > **[!UICONTROL Informes personalizados]** > **[!UICONTROL Informes históricos]** > **[!UICONTROL Informe de acceso al curso]**.

### Cambios en la transcripción del alumno

En versiones anteriores de Adobe Learning Manager, si un administrador personalizado presentaba un ámbito de usuario, la transcripción de aprendizaje contenía los usuarios eliminados. En esta versión, la transcripción de aprendizaje contendrá los usuarios eliminados si el administrador personalizado presenta un ámbito de usuario o tiene acceso a todos los grupos de usuarios.

### Cambios en el informe de asistencia

El informe de asistencia de la página Asistencia de Cursos de la aplicación del administrador y de la página Alumnos de la sesión de la aplicación del instructor se solía descargar de forma síncrona. En esta versión, este informe se descargará de forma asíncrona a través de una notificación.

Para obtener más información sobre los informes, consulte [Informes](/help/migrated/administrators/feature-summary/reports.md) en Adobe Learning Manager.

## Retirada de la tienda de contenido

Los cursos que hayan caducado en el catálogo de la tienda de contenido importado (formación empresarial) se eliminarán automáticamente una vez que caduquen. Los cursos se eliminarán cuando el contenido se marque para su retirada. Los alumnos ya inscritos pueden consumirlos dentro de un plazo limitado, tras el cual se eliminarán. Esto mantendrá limpio el catálogo y no mostrará a los usuarios ningún curso caducado.

## Nuevas recomendaciones basadas en habilidades

Adobe Learning Manager mejora las recomendaciones para las cuentas de clientes y socios. Esta mejora en el algoritmo de recomendación con el cambio en el algoritmo de clasificación por curso, ruta de aprendizaje y certificación proporciona una mejor experiencia al usuario a la hora de descubrir contenidos.

El algoritmo ya no permitirá recomendaciones entre iguales. El cambio no afectará a los usuarios existentes, pero seguirá existiendo la opción Adaptado al sector. En el caso de la opción Personalizado, Adobe Learning Manager ya no permitirá la selección personalizada entre iguales.

El grupo de iguales se convierte ahora en una cuenta y los alumnos verán una cadena que muestra los temas destacados del grupo. Todas las recomendaciones tienen una explicación. Por ejemplo, si ve algo sobre un tema, la tarjeta de la tira mostrará el motivo del curso.

## Mejoras del flujo de trabajo de administrador personalizado

Los administradores personalizados tendrán ahora más paridad con las funciones de administrador en cuanto al acceso a los informes. Los administradores podrán configurar el acceso a los informes con un mejor control.

En Adobe Learning Manager, solo están disponibles las transcripciones de aprendizaje y de interacciones para un administrador personalizado. En esta versión, un administrador personalizado puede acceder a todos los informes personalizados, excepto a los informes de xAPI y de correo electrónico, que siguen estando disponibles solo para el administrador. El acceso a todos los informes está sujeto al catálogo y al ámbito de usuario que tenga el administrador personalizado. Hay pocos informes que solo estén disponibles con un ámbito completo. Estos son:

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

Si selecciona Solo lectura, el administrador personalizado podrá ver todos los usuarios, pero no podrá editar sus datos ni crear un portal de registro automático para ellos.

**Planes de aprendizaje**:

Si selecciona Solo lectura, un administrador personalizado no podrá añadir ni editar un plan de aprendizaje. Puede descargar un informe del plan de aprendizaje y ver sus detalles. Sin embargo, no puede cambiar los detalles del curso.

>[!NOTE]
>
>Los planes de aprendizaje serán de solo lectura adicional, junto con un control total.

**Plantillas de correo electrónico**

Si selecciona Solo lectura, un administrador personalizado podrá ver las plantillas de correo electrónico. No puede activar ni desactivar la configuración de las plantillas de correo electrónico, pero puede descargar los informes de acceso al correo electrónico.

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

Los instructores pueden personalizar su experiencia en las sesiones mediante la selección de salas específicas para ellos. En esta versión, hemos realizado las siguientes mejoras:

### Importar transcripciones

Podrá importar transcripciones de sesiones desde Connect y analizar las transcripciones. Los alumnos recibirán la transcripción después de la grabación, que podrán descargar más tarde.

### Editar vídeos

Los instructores pueden editar el vídeo y mejorar la experiencia de visualización de los alumnos. Los instructores verán un vínculo en la página Resumen de la sesión que les llevará a la página de inicio de sesión de Adobe Connect. Después de iniciar sesión, el instructor verá el vínculo de grabación. Al hacer clic en el vínculo, se les redirigirá al vídeo, que pueden recortar.

## Restringir informes de tablero a usuarios con la función de responsable

Los administradores solo pueden buscar responsables en los informes del tablero.

## Limitar el procesamiento de informes del tablero existentes

Cuando un administrador intenta trazar un informe del tablero y el informe tarda demasiado en trazarse (más de 2,5 minutos), Adobe Learning Manager muestra el siguiente mensaje:

![imagen de informe heredada](assets/error-message.png)
*Mensaje de error cuando el informe tarda demasiado*

Los informes de tal magnitud no pueden mostrarse en la interfaz de usuario, pero el administrador puede descargarlos.

## Compatibilidad de migración con etiquetas de catálogo

El flujo de trabajo de migración ahora admite etiquetas de catálogo. Los CSV de migración pueden utilizarse para importar claves y valores de etiquetas de catálogo y adjuntarlos a cursos, rutas de aprendizaje, certificaciones y ayudas de trabajo. El flujo de trabajo también puede utilizarse para eliminar valores y claves incorrectos si es necesario.

## Mejoras de la API para el filtrado complejo de cursos

El filtrado avanzado de cursos mediante etiquetas y etiquetas de catálogo (mediante una combinación de condiciones &quot;AND&quot; y &quot;OR&quot;) ahora será posible mediante las API de Learning Manager.

## Cambios en las API de esta versión

### Validación en la API del trabajo

En esta versión, si el informe de ayuda de trabajo supera los 10 millones generados mediante la API de trabajo, la respuesta mostrará el mensaje: &quot;El informe solicitado tiene demasiados datos que generar. Plantéese aplicar filtros de ayuda de trabajo&quot;.

### Notificación de una publicación eliminada

En versiones anteriores de Adobe Learning Manager, si se eliminaba cualquier curso, certificación o plan de aprendizaje y su notificación estaba presente, aún podía acceder a uno de estos componentes mediante ella.

En esta versión, nos aseguraremos de que ya no se pueda acceder a una publicación eliminada. Si especifica el id en la opción /posts/{id} API, y el ID de la publicación ya no está disponible, la API muestra el mensaje &quot;Publicación no encontrada para el recurso especificado&quot;.

### Plazo de finalización de la API de alumno

En versiones anteriores, Adobe Learning Manager obtenía el plazo de la tabla de inscripciones. En esta versión, Adobe Learning Manager calculará el plazo a partir de la tabla de instancias del curso. Si el plazo no está disponible, volverá a la tabla de inscripciones.

### Indicador de anulación

En la versión de noviembre de 2023 de Adobe Learning Manager, dejaremos de utilizar el indicador de anulación de las API. El indicador de anulación no forma parte de la especificación de las API públicas y se ha diseñado para las pruebas de back-end. El indicador ya no está disponible para las API de alumno. Sin embargo, sigue siendo válido para las API de administrador.

La razón por la que estamos dejando de utilizar el indicador para las API de alumno es que el indicador de anulación obtenía una gran cantidad de datos a través de las API de alumno.

A partir de ahora, la siguiente API de alumno dejará de funcionar debido a que presenta el indicador de anulación.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Resaltar resultados

En la próxima versión de Adobe Learning Manager, por ejemplo, en la API /search, estamos cambiando el valor predeterminado de highlightResults a false.

Además, cambiaremos el valor predeterminado de snippetTypes a courseName. Al hacerlo, solo se resaltarán los nombres de los cursos en la búsqueda si highlightResults es True.

### Nuevo tipo de recurso para la prueba

La `instances.loResources.resources` punto final devolverá `ResourceContentType` con Quiz.

## Aviso de retirada

El 30 de noviembre de 2023, LinkedIn Learning dejará de utilizar el método HTTP GET para obtener un token de OAuth. Después de la degradación, solo podrá generar un token de OAuth mediante el método del POST HTTP.
Adobe Learning Manager dejará de ofrecer BlueJeans en febrero de 2024. Todas las cuentas nuevas posteriores a febrero de 2024 no incluirán el conector de BlueJeans.

## Notas de la versión

Para obtener información sobre las versiones actuales y anteriores de la aplicación web y para dispositivos de Learning Manager, consulte la [Notas de la versión](release-note/release-notes.md).

## Errores solucionados en esta versión

* La miniatura de un curso que sea un requisito previo para una ruta de aprendizaje u otro curso no se mostrará cuando un alumno abra la página de vista previa de la ruta de aprendizaje o del curso.
* Si no se seleccionan las opciones Calendario, Interacción y Aprendizaje social, la configuración del tablero del alumno no conservará la siguiente configuración. Las opciones como Recomendado en las áreas de interés y Examinar por catálogo no aparecen como seleccionadas, sino que se muestran en la vista previa.
* Incluso después de que un alumno complete un curso de clases virtuales, recibirá un mensaje de recordatorio para que lo complete.
* En el caso de las cuentas de igual a igual, no se podrán descargar los informes del tablero.
* Al eliminar y añadir un módulo de la lista de comprobación de un curso, se produce un error interno.
* En el caso de las plantillas de invitación de sesión, el ID de correo electrónico del remitente presenta el texto captivatePrime en lugar de AdobeLearningManager.
* Cuando se utiliza la Eficacia del curso como eje Y secundario, la descarga del informe falla con una excepción de puntero nulo.
* Si a un alumno se le asigna una función de administrador personalizado, este se desplazará de forma predeterminada al perfil de administrador personalizado. Sin embargo, cuando se establece una URL de redirección del alumno en la cuenta, se redirige al administrador personalizado a un destino diferente, no al perfil de la función de administrador personalizado.
* El ámbito de interacción no funciona como se esperaba si disabled_sub_groups se establece en un número elevado.
* En algunos casos, los usuarios eliminados activan una migración.
* Un alumno no puede reproducir cursos de LinkedIn en la aplicación MS Teams.
* La API de inscripción no devuelve las inscripciones en un plan de aprendizaje flexible o incrustado como se esperaba.
* En la aplicación para dispositivos móviles, los nombres de un curso, una certificación o un plan de aprendizaje aparecen en minúsculas.
* En versiones anteriores de Adobe Learning Manager, si se eliminaba cualquier curso, certificación o plan de aprendizaje y su notificación estaba presente, aún podía acceder a uno de estos componentes mediante ella. En esta versión, nos aseguraremos de que ya no se pueda acceder a una publicación eliminada. Si especifica el id en la opción /posts/{id} API, y el ID de la publicación ya no está disponible, la API muestra el mensaje &quot;Publicación no encontrada para el recurso especificado&quot;.
* En la API de alumno, el campo de plazo de finalización no se muestra en la respuesta de la API de inscripción.
* En la API para obtener inscripciones de los alumnos, los detalles de inscripción aparecen incluso después de especificar un ID de instancia incorrecto.

## Problemas conocidos de esta versión

* Falla una nueva inscripción o la actualización de una inscripción cuando un plan de formación flexible se encuentra dentro de otro.
* La URL de transcripción no muestra las grabaciones de sesiones de Adobe Connect.
* Un alumno puede realizar una prueba sin conexión en la aplicación móvil, aunque no la supere.

## Requisitos del sistema

[Requisitos del sistema de Learning Manager](system-requirements.md)

## Versiones anteriores de Adobe Learning Manager

* [Versión de julio de 2023](whats-new-2023-july.md)
* [Versión de abril de 2023](whats-new-2023-april.md)
* [Versión de noviembre de 2022](whats-new-2022-november.md)
