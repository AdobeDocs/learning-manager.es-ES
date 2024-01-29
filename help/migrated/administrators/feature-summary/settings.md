---
description: Obtenga información sobre la configuración de la cuenta de Learning Manager que puede configurar como administrador.
jcr-language: en_us
title: Configuración
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3791'
ht-degree: 0%

---



# Configuración

Obtenga información sobre la configuración de la cuenta de Learning Manager que puede configurar como administrador.

Puede cambiar la configuración del perfil de administrador y actualizar la configuración de la cuenta. Consulte su información de perfil, añada o cambie la foto de perfil y modifíquela **[!UICONTROL Acerca de mí]** contenido. Actualice la información de su empresa, configure los métodos de inicio de sesión de los usuarios y configure la integración de conexiones a través de la configuración de la cuenta.

## Configuración de cuenta {#accountsettings}

Para actualizar la configuración de la cuenta de su organización, haga clic en **[!UICONTROL Configuración]** en el panel izquierdo.

**Información básica (información de la empresa)**

Haga clic en **[!UICONTROL Cambiar]** en la página y edite la configuración de país, zona horaria, configuración regional y año financiero.

**Configurar el administrador de contactos**

Si desea añadir o cambiar las direcciones de correo electrónico de los administradores de asistencia de su organización , puede configurar haciendo clic en **[!UICONTROL General]** en el panel izquierdo. Haga clic en **[!UICONTROL Cambiar]** adyacente a **[!UICONTROL ID de correo electrónico de asistencia]** y añada los ID de correo electrónico. El correo electrónico se envía a estos administradores cuando el alumno hace clic en él **[!UICONTROL Contactar con administrador]** al pie de la página.

Añada ID de correo electrónico adicionales con punto y coma como separador.

**Métodos de acceso** - Los administradores pueden elegir el modo en el que los usuarios internos o externos pueden acceder a la cuenta.

* **Usuarios internos:** Para los usuarios internos, puede configurar Adobe ID o el inicio de sesión único como modo de inicio de sesión.
* **Usuarios externos:** Para usuarios externos, puede establecer el ID de Adobe ID o de inicio de sesión único o de administrador de aprendizaje.

Si elige ID de Learning Manager, los usuarios externos pueden iniciar sesión en esta cuenta después de crear su nombre de usuario y contraseña de Learning Manager.

>[!NOTE]
>
>Si hay varios perfiles externos definidos, todos los perfiles pueden tener cualquier tipo de inicio de sesión. Por ejemplo, si el tipo de inicio de sesión es Adobe ID, todos los perfiles tienen que iniciar sesión solo con Adobe ID. Cada perfil no puede tener su tipo de inicio de sesión individual.

Puede acceder a la aplicación Learning Manager mediante Adobe ID o mediante el inicio de sesión único. El inicio de sesión único es un mecanismo que permite a un usuario autenticarse una vez y obtener acceso a varias aplicaciones muchas veces. Esta configuración no es obligatoria para la organización. Si su organización tiene un proveedor de SSO basado en SAML 2.0, puede utilizarlo para configurar la aplicación Learning Manager. La configuración es necesaria en el nivel de la organización y en la aplicación Learning Manager. Si decide utilizar SSO, póngase en contacto con el servicio de asistencia del Adobe para recibir las instrucciones de configuración

**Comentarios**

Haga clic en **[!UICONTROL Comentarios]** en el panel izquierdo para configurar el cuestionario y obtener comentarios de los alumnos después de completar un curso. Consulte la [contenido de ayuda de la función cursos](courses.md) sobre la creación de comentarios de L1 y L3.

**Varios intentos**

Seleccionar **[!UICONTROL Configuración]** > **[!UICONTROL General]** > **[!UICONTROL Varios intentos]**.

Si activa la casilla de verificación &quot;Varios intentos&quot;, los autores pueden definir &quot;Varios intentos&quot; para módulos o cursos de aprendizaje electrónico interactivos. Al seleccionar la segunda casilla, los administradores pueden definir &quot;Intentos infinitos&quot; de forma predeterminada para cualquier curso de aprendizaje electrónico interactivo recién creado.

![](assets/admin-config.png)

*Seleccione la casilla de verificación Varios intentos*

**Moderación del curso**

Haga clic en **[!UICONTROL General]** en el panel izquierdo, y seleccione la opción Moderación de los cursos para habilitar la funcionalidad Moderación de los cursos. Para obtener más información sobre esta función, consulte [Moderación del curso](courses.md#main-pars_header_1879001177).

**Panel de debates**

Si activa la casilla de verificación Foro de debate, los alumnos y los instructores pueden publicar comentarios para los cursos mediante la ficha Debate de la página Cursos de la aplicación del alumno. Sin embargo, si la configuración del nivel del curso indica que esta función no está seleccionada, la configuración del nivel del curso tiene prioridad sobre la configuración del administrador.

**Panel del alumno**

En el panel izquierdo, haga clic en Tablero del alumno. Esta página permite elegir los widgets que desea mostrar en la página Alumnos. Seleccione los widgets que desee activar en la página Alumnos. Los widgets que no estén seleccionados no aparecerán en la página Alumnos.

**Adobe Connect**

Haga clic en **[!UICONTROL Adobe Connect]** en el panel izquierdo para configurar la cuenta de Adobe Connect para alojar sesiones de clase virtual. Para obtener más información, consulte  [Adobe Connect](adobeconnect-integration.md) ayuda de funciones.

## Configuración general {#general}

Active o desactive las siguientes opciones de configuración:

<table>
 <tbody>
  <tr>
   <th>
    <p><b>Nombre</b></p>
    </th>
   <th>
    <p><b>Descripción</b></p>
   </th>
  </tr>
  <tr>
   <td>Mostrar eficacia del curso</td>
   <td>Si se ha activado, los alumnos pueden ver la eficacia actual del curso en el icono del curso. Esta función solo está disponible para los cursos. La valoración basada en estrellas no es compatible con programas de aprendizaje ni certificados. Está disponible para cursos y programas de aprendizaje, pero no para certificaciones.</td>
  </tr>
  <tr>
   <td>Moderación del curso</td>
   <td>Si está activado, todos los cambios en los cursos deben necesitar la aprobación del administrador antes de que los alumnos puedan verlos.</td>
  </tr>
  <tr>
   <td>Panel de debates</td>
   <td>Si activa la casilla de verificación Foro de debate, los alumnos y los instructores pueden publicar comentarios para los cursos mediante la ficha Debate de la página Cursos de la aplicación del alumno. Sin embargo, si la configuración del nivel del curso indica que esta función no está seleccionada, la configuración del nivel del curso tiene prioridad sobre la configuración del administrador.</td>
  </tr>
  <tr>
   <td>Varios intentos</td>
   <td>Si se habilita, el autor puede configurar varios intentos para los módulos del curso.</td>
  </tr>
  <tr>
   <td>Opción Explorar Aptitudes</td>
   <td>Si se ha activado, los alumnos pueden explorar las aptitudes de compañeros y de liderazgo, y suscribirse a las aptitudes de su elección.</td>
  </tr>
  <tr>
   <td>Visibilidad de aptitudes/etiquetas</td>
   <td>Mostrar todas las aptitudes y etiquetas a los alumnos. Puede mostrar todas las aptitudes y etiquetas o mostrar las aptitudes y etiquetas asignadas, o bien aquellas que forman parte de los catálogos visibles para el alumno.</td>
  </tr>
  <tr>
   <td>ID exclusivos de objetos de aprendizaje</td>
   <td>Si está activado, un administrador o un autor pueden añadir un ID exclusivo para cada objeto de aprendizaje.</td>
  </tr>
  <tr>
   <td>Mostrar paneles de filtro</td>
   <td>
    <p><a id="filter-panels"></a>Controle los paneles de filtro que están disponibles en la aplicación del alumno para ajustar sus resultados de búsqueda. Las opciones son las siguientes:</p>
    <ul>
     <li>Catálogos</li>
     <li>Tipo</li>
     <li>Formato</li>
     <li>Duración</li>
     <li>Aptitudes</li>
     <li>Niveles de aptitudes</li>
     <li>Etiquetas</li>
    </ul>
    <p>Cuando el alumno inicia la aplicación del alumno, en las secciones Mi aprendizaje y Catálogo, puede ver los filtros en sus respectivos paneles.</p>
    <p><b>Nota: </b>Los filtros <b>Formato </b>y <b>Duración </b>están desactivados de forma predeterminada y no se muestran a los alumnos justo después de la publicación. El administrador debe activarlos. <br></p></td>
  </tr>
  <tr>
   <td>Mostrar listado de catálogos</td>
   <td>Si se habilita, los alumnos pueden ver una lista de todos los catálogos disponibles para ellos. Los alumnos pueden utilizar esta opción para precisar cómo se muestran los objetos de aprendizaje.</td>
  </tr>
  <tr>
   <td>Terminología del producto</td>
   <td>Learning Manager dispone de una terminología estándar que se utiliza en todo el producto. Modifique la terminología para adaptarla a las necesidades de su organización.</td>
  </tr>
  <tr>
   <td>Actualización de versión del módulo</td>
   <td>Configure la configuración predeterminada para actualizar el contenido. La configuración se puede modificar para cada contenido desde la página del curso.</td>
  </tr>
  <tr>
   <td>Registro automático de usuarios</td>
   <td>Si se habilita, los usuarios recién importados se registran automáticamente. De forma predeterminada, los usuarios deben registrarse manualmente para poder empezar a utilizar Learning Manager.</td>
  </tr>
  <tr>
   <td><a id="autodelete"></a>Eliminar automáticamente usuarios internos</td>
   <td>Si se habilita, los usuarios internos se eliminan automáticamente si no acceden al sistema durante el número de días especificado. Esta función se aplica a los usuarios que solo tienen la función <b>Alumno</b>. Para restaurar el acceso, los usuarios deben ponerse en contacto con el administrador.<br></td>
  </tr>
  <tr>
   <td>Mostrar etiquetas de catálogo</td>
   <td>Si está activada, los administradores y los autores pueden definir etiquetas de catálogo y valores, y vincularlos a objetos de aprendizaje.</td>
  </tr>
  <tr>
   <td>Los alumnos pueden ver sus puntuaciones</td>
   <td>Si se activa, los alumnos pueden ver sus puntuaciones en la transcripción del alumno.</td>
  </tr>
  <tr>
   <td>Correo electrónico de resumen</td>
   <td>
    <p>Un administrador puede activar o desactivar el envío de un correo electrónico a los alumnos. El administrador también podrá controlar la frecuencia de los mensajes de correo electrónico enviados.</p>
    <ul>
     <li>Para <b>cuentas activas</b>, los mensajes de resumen se desactivarán de forma predeterminada, lo que el administrador puede activar manualmente.</li>
     <li>Para <b>cuentas de prueba</b>, la opción de mensajes de correo electrónico de resumen permanecerá desactivada y el administrador no podrá activarla.</li>
    </ul>
    <p>Si la función está desactivada:</p>
    <ul>
     <li>La opción <b>Correo electrónico de resumen</b> se deshabilitará.</li>
     <li>Un alumno no puede ver la configuración de usuario para la suscripción al correo electrónico de resumen.</li>
    </ul>
    <p> Si la función está activada:</p>
    <ul>
     <li>El administrador puede activar y modificar la opción Correo electrónico de resumen .</li>
     <li>Desde el <b>Configuración de perfil </b>en la aplicación de alumno, un alumno (que no figure en la lista No molestar) puede optar por suscribirse o cancelar su suscripción al correo electrónico de resumen.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Activar iconos de la tarjeta de aprendizaje<br></td>
   <td>Si se ha activado, los iconos aparecerán en las tarjetas de aprendizaje de la aplicación del alumno.<br></td>
  </tr>
  <tr>
   <td>Vínculos de pie de página</td>
   <td>
    <p>Agregue vínculos o ID de correo electrónico que aparezcan como pies de página. Puede agregar hasta tres vínculos de pie de página.</p>
    <p>Para personalizar los vínculos del pie de página, siga estos pasos:</p>
    <ol>
     <li>Haga clic en <b>Añadir más</b>, introduzca el nombre y la dirección URL o el ID de correo electrónico en los campos especificados. Escriba el prefijo http:// o https:// en la dirección URL.</li>
     <li>Para aplicar el cambio en cascada en todas las configuraciones regionales, haga clic en <b>Replicar</b>. Esto garantiza que todos los idiomas obtengan el nombre y la URL.</li>
     <li>Para guardar los cambios, haga clic en <b>Guardar</b>. Aparece un mensaje emergente que confirma el cambio. Después de hacer clic en Aceptar, el pie de página se rellena con los vínculos recién agregados.</li>
    </ol>
    <p>Además, puede:</p>
    <ul>
     <li>Haga clic en <b>Restablecer</b> para restablecer los valores predeterminados en el <b>Ayuda</b> y <b>Contactar con administrador</b> campos.</li>
     <li>Personalizar el vínculo del pie de página para todos los idiomas. Haga clic en <b>Idioma</b> lista desplegable, seleccione el idioma y añada el <b>Nombre</b> y <b>URL</b> en los campos especificados. Después de guardar los cambios, los vínculos actualizados aparecen en el pie de página.<br></li>
    </ul></td>
  </tr>
  <tr>
   <td>Zona horaria del informe<br></td>
   <td>
    <p>Establezca una preferencia de nivel de cuenta para exportar la transcripción de aprendizaje en las siguientes zonas horarias:</p>
    <ul>
     <li>UTC (comportamiento predeterminado)</li>
     <li>Preferencia de zona horaria de nivel de cuenta</li>
    </ul>
    <p>La transcripción del alumno descargada mediante la API de trabajos también descarga los datos en la zona horaria seleccionada.</p>
    <p><b>Nota: </b>No se espera ningún cambio en la transcripción del alumno de forma predeterminada justo después de la publicación. Los administradores pueden configurar este ajuste desde Administración &gt; Configuración &gt; General &gt; Zona horaria del informe.</p></td>
  </tr>
 </tbody>
</table>

<table border="0" cellpadding="0" cellspacing="0" width="1709">
 <tbody>
  <tr>
   <td height="20" width="147">Nombre</td>
   <td>Descripción</td>
  </tr>
  <tr>
   <td height="20">Mostrar eficacia del curso</td>
   <td>Si se ha activado, los alumnos pueden ver la eficacia actual del curso en el icono del curso.</td>
  </tr>
  <tr>
   <td height="20">Moderación del curso</td>
   <td>Si está activado, todos los cambios en los cursos deben necesitar la aprobación del administrador antes de que los alumnos puedan verlos.</td>
  </tr>
  <tr>
   <td height="20">Panel de debates</td>
   <td>Si activa la casilla de verificación Foro de debate, los alumnos y los instructores pueden publicar comentarios para los cursos mediante la ficha Debate de la página Cursos de la aplicación del alumno. Sin embargo, si la configuración del nivel del curso indica que esta función no está seleccionada, la configuración del nivel del curso tiene prioridad sobre la configuración del administrador.</td>
  </tr>
  <tr>
   <td height="20">Varios intentos</td>
   <td>Si se habilita, el autor puede configurar varios intentos para los módulos del curso.</td>
  </tr>
  <tr>
   <td height="20">Opción Explorar Aptitudes</td>
   <td>Si se ha activado, los alumnos pueden explorar las aptitudes de compañeros y de liderazgo, y suscribirse a las aptitudes de su elección.</td>
  </tr>
  <tr>
   <td height="20">Visibilidad de aptitudes/etiquetas</td>
   <td>Mostrar todas las aptitudes y etiquetas a los alumnos. Puede mostrar todas las aptitudes y etiquetas o mostrar las aptitudes y etiquetas asignadas, o bien aquellas que forman parte de los catálogos visibles para el alumno.</td>
  </tr>
  <tr>
   <td height="20">ID exclusivos de objetos de aprendizaje</td>
   <td>Si está activado, un administrador o un autor pueden añadir un ID exclusivo para cada objeto de aprendizaje.</td>
  </tr>
  <tr>
   <td rowspan="10" height="191">Mostrar paneles de filtro</td>
   <td>Controle los paneles de filtro que están disponibles en la aplicación del alumno para ajustar sus resultados de búsqueda. Las opciones son las siguientes:</td>
  </tr>
  <tr>
   <td height="19">Catálogos</td>
  </tr>
  <tr>
   <td height="19">Tipo</td>
  </tr>
  <tr>
   <td height="19">Formato</td>
  </tr>
  <tr>
   <td height="19">Duración</td>
  </tr>
  <tr>
   <td height="19">Aptitudes</td>
  </tr>
  <tr>
   <td height="19">Niveles de aptitudes</td>
  </tr>
  <tr>
   <td height="19">Etiquetas</td>
  </tr>
  <tr>
   <td height="19">Cuando el alumno inicia la aplicación del alumno, en las secciones Mi aprendizaje y Catálogo, puede ver los filtros en sus respectivos paneles.</td>
  </tr>
  <tr>
   <td height="20">Nota: los filtros Formato y Duración están desactivados de forma predeterminada y no se muestran a los alumnos después de la publicación. El administrador debe activarlos. </td>
  </tr>
  <tr>
   <td height="20">Mostrar listado de catálogos</td>
   <td>Si se habilita, los alumnos pueden ver una lista de todos los catálogos disponibles para ellos. Los alumnos pueden utilizar esta opción para precisar cómo se muestran los objetos de aprendizaje.</td>
  </tr>
  <tr>
   <td height="20">Terminología del producto</td>
   <td>Learning Manager dispone de una terminología estándar que se utiliza en todo el producto. Modifique la terminología para adaptarla a las necesidades de su organización.</td>
  </tr>
  <tr>
   <td height="20">Actualización de versión del módulo</td>
   <td>Configure la configuración predeterminada para actualizar el contenido. La configuración se puede modificar para cada contenido desde la página del curso.</td>
  </tr>
  <tr>
   <td height="20">Registro automático de usuarios</td>
   <td>Si se habilita, los usuarios recién importados se registran automáticamente. De forma predeterminada, los usuarios deben registrarse manualmente para poder empezar a utilizar Learning Manager.</td>
  </tr>
  <tr>
   <td height="20">Eliminar automáticamente usuarios internos</td>
   <td>Si se habilita, los usuarios internos se eliminan automáticamente si no acceden al sistema durante el número de días especificado. Esta función se aplica a los usuarios que solo tienen la función Alumno. Para restaurar el acceso, los usuarios deben ponerse en contacto con el administrador.</td>
  </tr>
  <tr>
   <td height="20">Mostrar etiquetas de catálogo</td>
   <td>Si está activada, los administradores y los autores pueden definir etiquetas de catálogo y valores, y vincularlos a objetos de aprendizaje.</td>
  </tr>
  <tr>
   <td height="20">Los alumnos pueden ver sus puntuaciones</td>
   <td>Si se activa, los alumnos pueden ver sus puntuaciones en la transcripción del alumno.</td>
  </tr>
  <tr>
   <td rowspan="9" height="172">Correo electrónico de resumen</td>
   <td>Un administrador puede activar o desactivar el envío de un correo electrónico a los alumnos. El administrador también podrá controlar la frecuencia de los mensajes de correo electrónico enviados.</td>
  </tr>
  <tr>
   <td height="19">En el caso de las cuentas activas, los mensajes de resumen se desactivarán de forma predeterminada, lo que el administrador puede activar manualmente.</td>
  </tr>
  <tr>
   <td height="19">En el caso de las cuentas de prueba, la opción de mensajes de correo electrónico de resumen permanecerá desactivada y el administrador no podrá activarla.</td>
  </tr>
  <tr>
   <td height="19">Si la función está desactivada:</td>
  </tr>
  <tr>
   <td height="19">Se desactivará la opción Correo electrónico de resumen .</td>
  </tr>
  <tr>
   <td height="19">Un alumno no puede ver la configuración de usuario para la suscripción al correo electrónico de resumen.</td>
  </tr>
  <tr>
   <td height="19"> Si la función está activada:</td>
  </tr>
  <tr>
   <td height="19">El administrador puede activar y modificar la opción Correo electrónico de resumen .</td>
  </tr>
  <tr>
   <td height="20">En la Configuración de perfil de la aplicación de alumno, un alumno (que no se haya incluido en la lista No molestar) puede optar por suscribirse o cancelar su suscripción al correo electrónico de resumen.</td>
  </tr>
  <tr>
   <td height="20">Activar iconos de la tarjeta de aprendizaje</td>
   <td>Si se ha activado, los iconos aparecerán en las tarjetas de aprendizaje de la aplicación del alumno.</td>
  </tr>
  <tr>
   <td rowspan="8" height="153">Vínculos de pie de página</td>
   <td>Agregue vínculos o ID de correo electrónico que aparezcan como pies de página. Puede agregar hasta tres vínculos de pie de página.</td>
  </tr>
  <tr>
   <td height="19">Para personalizar los vínculos del pie de página, siga estos pasos:</td>
  </tr>
  <tr>
   <td height="19">1. Haga clic en Añadir más, introduzca el nombre y la URL o el ID de correo electrónico en los campos especificados. Escriba el prefijo http:// o https:// en la dirección URL.</td>
  </tr>
  <tr>
   <td height="19">2. Para aplicar el cambio en cascada en todas las configuraciones regionales, haga clic en Replicar. Esto garantiza que todos los idiomas obtengan el nombre y la URL.</td>
  </tr>
  <tr>
   <td height="19">3. Para guardar los cambios, haga clic en Guardar. Aparece un mensaje emergente que confirma el cambio. Después de hacer clic en Aceptar, el pie de página se rellena con los vínculos recién agregados.</td>
  </tr>
  <tr>
   <td height="19">Además, puede:</td>
  </tr>
  <tr>
   <td height="19">Haga clic en el icono Restablecer para restablecer los valores predeterminados de los campos Ayuda y Contactar con el administrador .</td>
  </tr>
  <tr>
   <td height="20">Personalizar el vínculo del pie de página para todos los idiomas. Haga clic en la lista desplegable Idioma, seleccione el idioma y agregue el Nombre y la URL en los campos especificados. Después de guardar los cambios, los vínculos actualizados aparecen en el pie de página.</td>
  </tr>
  <tr>
   <td rowspan="5" height="96">Zona horaria del informe</td>
   <td> Establezca una preferencia de nivel de cuenta para exportar la transcripción de aprendizaje en las siguientes zonas horarias:</td>
  </tr>
  <tr>
   <td height="19">UTC (comportamiento predeterminado)</td>
  </tr>
  <tr>
   <td height="19">Preferencia de zona horaria de nivel de cuenta</td>
  </tr>
  <tr>
   <td height="19">La transcripción del alumno descargada mediante la API de trabajos también descarga los datos en la zona horaria seleccionada.</td>
  </tr>
  <tr>
   <td height="20">Nota: no se espera ningún cambio en la transcripción del alumno de forma predeterminada justo después de la publicación. Los administradores pueden configurar este ajuste desde Administración &gt; Configuración &gt; General &gt; Zona horaria del informe.</td>
  </tr>
  <tr>
   <td height="19">Integración de Badgr</td>
   <td>Si se activa, los alumnos podrán cargar sus insignias en el sitio web de Badgr. En los contextos de formación de clientes, las organizaciones desean poder "certificar" a sus clientes y darles la oportunidad de mostrar esas credenciales en las redes sociales. Esto motiva al alumno a tomar un curso de formación y compartir sus logros con otros. </td>
  </tr>
  <tr>
   <td height="135">
    <p>Mostrar valoración</p></td>
   <td>
    <ul>
     <li>Si la opción <b>Eficacia del curso</b> Cuando se activa, los alumnos solo podrán ver el valor de la eficacia del curso.</li>
     <li>Si la opción <b>Valoración basada en estrellas</b> Si está activada, los alumnos solo podrán ver la valoración media de estrellas y el número de alumnos que han valorado el curso.<br></li>
    </ul>
    <p>Esta función solo está disponible para los cursos. La valoración basada en estrellas no es compatible con programas de aprendizaje ni certificados.<br><br><b>Nota: </b>Este cambio solo afecta a la aplicación del alumno. </p>
    <p>En el resto de aplicaciones (administrador, autor, responsable, administrador personalizado y autor personalizado), los cambios en la configuración (clasificación basada en estrellas/eficacia del curso/desactivación de mostrar clasificación) no tendrán ningún efecto. </p>
    <p>Para las nuevas cuentas, el <b>Mostrar valoraciones</b> tendrá la opción de <b>Valoración basada en estrellas</b> activado de forma predeterminada.</p>
    <p>Para las cuentas existentes, si la cuenta tenía anteriormente la opción <b>Eficacia del curso</b> activado, a continuación el <b>Mostrar valoraciones</b> se activará con la opción Eficacia del curso seleccionada. Si la opción <b>Eficacia del curso</b>s está desactivada, a continuación, el <b>Mostrar valoraciones</b> sección también se deshabilitará. Cuando el <b>Mostrar valoraciones</b> está activada, la opción <b>Valoración basada en estrellas</b> se habilitará de forma predeterminada.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p>Rutas de aprendizaje</p></td>
   <td>
    <p>Si la opción <b>Activar las funciones ampliadas de la ruta de aprendizaje</b> Si está activada, los administradores podrán incluir rutas de aprendizaje dentro de las rutas de aprendizaje y combinarlas con cursos. La opción es irreversible.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Gestión de instructores<br></p></td>
   <td>
    <p>Active este ajuste para restringir la lista de instructores que se pueden seleccionar al crear sesiones de clase o de clase virtual. Todos los usuarios que tengan el privilegio de instructor solo se pueden asignar como instructor a cualquier sesión. Esta restricción no se aplica a los flujos de trabajo de migración.<br></p></td>
  </tr>
 </tbody>
</table>

## Recomendación basada en Inteligencia artificial

Learning Manager incluye una nueva página de inicio de alumno, moderna, más orientada al contenido y personalizada según las preferencias del alumno. Las recomendaciones de aprendizaje basadas en Inteligencia artificial tienen como objetivo mejorar la participación del alumno e identificar y abordar las lagunas de aprendizaje.

El algoritmo de recomendación está diseñado para incorporar varias fuentes de entrada, incluidos los datos del sector sobre las funciones de trabajo, los cargos y las descripciones que Adobe ha obtenido de sus socios. A continuación, estos datos se utilizan para formar algoritmos de IA de Adobe, de modo que Learning Manager pueda obtener un mapa que conecte las aptitudes alineadas con el sector a los cargos o las designaciones. Esto se convierte en una entrada del algoritmo de recomendación

A continuación, Learning Manager utiliza algoritmos de modelado de temas para analizar el contenido de formación de una cuenta y asignarlo a las aptitudes.

Learning Manager utiliza los datos de actividad de los compañeros como otra señal para impulsar el algoritmo de recomendación de forma personalizada. Aquí se utilizan actividades como la inscripción, la finalización y cualquier comentario explícito proporcionado por los alumnos.

Además, Learning Manager utiliza información explícita e implícita recopilada de alumnos individuales para personalizar aún más las recomendaciones. Un alumno podrá indicar explícitamente sus áreas de interés mediante inscripciones y Learning Manager recibirá esta información implícitamente en función de cómo el alumno termine realizando los cursos de formación.

Por último, el administrador también podrá influir en el algoritmo de recomendación mediante atributos de alumno que Learning Manager debería tener en cuenta al definir grupos de compañeros, así como al destacar los cursos de formación para grupos de usuarios específicos.

## Cambio de nombre de objetos de aprendizaje {#renaminglearningobjects}

Esta función solo está disponible en inglés.

Ahora los administradores pueden cambiar el nombre de los objetos de aprendizaje en Learning Manager. A continuación se indican las terminologías cuyo nombre se puede cambiar.

Módulo\
Curso\
Programa de aprendizaje\
Certificación\
Plan de aprendizaje\
Ayuda de trabajo\
Catálogo\
Aptitud\
Insignia\
Anuncio\
Mi aprendizaje\
Tabla de posiciones\
Eficacia\
Requisito\
Trabajo Previo\
Contenido principal\
Testout\
Con Ritmo Propio\
Mezclado\
Classroom\
Clase virtual\
Actividad

Para cambiar el nombre de las terminologías, siga estos pasos.

1. Como administrador, haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL General]** > **[!UICONTROL Terminología del producto]**. Se abre la opción de terminología del producto.

   ![](assets/product-terminology.png)

   *Cambiar nombre de terminología de productos*

1. Los cambios se pueden realizar cargando una plantilla de terminología del producto modificada descargando el archivo CSV de muestra. Para descargar el archivo CSV de muestra, haga clic en el **[!UICONTROL Descargar aquí]** opción.
1. El archivo CSV descargado contiene el nombre de los objetos de la columna A. En la columna B, elija el nombre que desea asignar al objeto respectivo. Tenga en cuenta que debe actualizar la forma singular y plural del nombre separada por (|).
1. Puede optar por modificar una o varias filas. Puede conservar las filas no modificadas o eliminarlas del archivo CSV antes de cargarlas.
1. Cargue el archivo CSV modificado y haga clic en **[!UICONTROL Guardar]**. Learning Manager actualiza los cambios para reflejar los cambios.
1. Para restablecer las terminologías predeterminadas, haga clic en **[!UICONTROL Restablecer terminología del producto]**.

   ![](assets/with-reset-option.png)

   *Restablecer la terminología del producto*

## Configuración de perfil {#profilesettings}

1. Haga clic en la flecha desplegable en la esquina superior derecha, junto a su fotografía/cuenta y elija **[!UICONTROL Configuración de perfil]**.
1. En el cuadro de diálogo emergente, puede añadir o cambiar la fotografía si pasa el ratón por encima y hace clic en **[!UICONTROL Editar]** en el área de la foto de perfil.
1. Añadir/modificar **[!UICONTROL Acerca]** contenido haciendo clic en **[!UICONTROL Editar]** junto a ella.
1. Haga clic en **[!UICONTROL Guardar].**

## Carpeta de contenido {#content-folder}

Learning Manager admite carpetas de contenido privado. Un administrador puede configurar carpetas de contenido privado y proporcionar su acceso a determinados autores personalizados mediante funciones personalizadas. Tenga en cuenta que los autores estándar (también denominados autores completos) siguen teniendo acceso a todo el contenido de la cuenta. Por lo tanto, los autores completos tienen acceso a todas las carpetas y a todo el contenido.

Los administradores pueden configurar las carpetas de contenido. Solo una vez configuradas, las carpetas de contenido pasan a estar visibles para los autores y estos pueden incluir el contenido en una o varias carpetas.

Para añadir una carpeta de contenido, en la aplicación de administrador, haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Carpeta de contenido]**.

![](assets/manage-content-folders.png)

*Cambiar configuración de carpeta de contenido*

### Carpeta

Una carpeta es un repositorio de contenido, que es un subconjunto de toda la biblioteca de contenido disponible en una cuenta con las siguientes propiedades:

* Solo un administrador puede crear, editar o eliminar una carpeta.
* Un administrador puede controlar el acceso a las carpetas como parte de la definición de funciones solo para administradores personalizados.
* Contenido **debe estar asociado en todo momento a al menos una carpeta**. Para empezar, todo el contenido se asociará a la carpeta pública, que se puede modificar posteriormente.
* El contenido se puede asociar a varias carpetas en el momento de la creación, lo que también será posible mediante una operación de copia
* Todos los nombres de carpeta deben ser exclusivos en la cuenta; de lo contrario, se producirá un error al asignar un nombre a una carpeta.

Las carpetas solo controlan la visibilidad del contenido y no crean copias del mismo. Por lo tanto, al modificar el contenido, los cambios se reflejarán en todas las carpetas asociadas.

### Carpeta pública

Una carpeta pública siempre está presente en una cuenta y, al principio, todo el contenido formará parte de esta carpeta. Más adelante, los autores pueden mover el contenido de esta carpeta a otras. Una carpeta pública tiene las siguientes propiedades:

* De forma predeterminada, todos los tipos de autores podrán acceder a todo el contenido asociado a esta carpeta.
* El contenido que forme parte de una carpeta pública no puede formar parte de ninguna otra carpeta. Lo contrario también es cierto.

Esta carpeta no puede formar parte de la definición de función configurable. Por consiguiente, no tener una carpeta pública en la definición de función configurable no restringe el acceso a una carpeta pública.

### Carpeta privada

* Cualquier carpeta creada por un administrador es una carpeta privada.

### Operaciones de carpeta

**Añadir una carpeta**

Para añadir una carpeta, haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha de la ventana.

**Eliminar una carpeta**

También puede eliminar una carpeta. Seleccione la carpeta que desea eliminar, haga clic en el menú Acciones y, a continuación, en **[!UICONTROL Eliminar carpeta]**.

>[!NOTE]
>
>Las carpetas se pueden eliminar cuando todo su contenido asociado también está asociado a otras carpetas. Si hay contenido vinculado solo a la carpeta que se va a eliminar, mueva primero el contenido a otra carpeta y, a continuación, elimine la carpeta.

## Ubicaciones de clase

Los administradores pueden utilizar esta configuración para crear y configurar una biblioteca de ubicaciones de clase. Los autores pueden seleccionar una ubicación preconfigurada para configurar su evento de clase. Seleccione una ubicación de la biblioteca para rellenar automáticamente la información de ubicación, la URL y el límite de asientos.

Como administrador, puede hacer lo siguiente:

### Importar CSV de ubicaciones

Añada ubicaciones en su cuenta importando un archivo CSV de ubicaciones. El archivo CSV debe contener la columna Ciudad.

### Agregar una ubicación

Añada lo siguiente:

1. Nombre de ubicación: introduzca el nombre de la clase.
2. Información de Ubicación: Introduzca la información sobre la ubicación.
3. Región Ubicación: El valor introducido aparece como filtro Ubicaciones de Formación para los alumnos.
4. URL de ubicación: introduzca la dirección URL de la ubicación.
5. Límite de asientos: introduzca la capacidad de asientos de la sala.

![ubicación de clase](assets/location-alm.gif)

*Añadir ubicaciones de clase*

También puede añadir la ubicación con la ayuda de un archivo CSV. El archivo CSV debe contener los campos:

* name
* información
* url
* límite de asientos
* región

<!--![Add classroom locations](assets/add-classroom-csv.png)-->

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++¿Cómo se crean diferentes carpetas para la biblioteca de contenido?

Haga clic en **[!UICONTROL Configuración]** > **[!UICONTROL Carpeta de contenido]**. Para añadir una carpeta, haga clic en **[!UICONTROL Añadir]** en la esquina superior derecha y en el cuadro de diálogo, introduzca el nombre y la descripción de la carpeta.

Los administradores pueden configurar las carpetas de contenido. Solo una vez configuradas, las carpetas de contenido pasan a estar visibles para los autores y estos pueden incluir el contenido en una o varias carpetas.

Para obtener más información, consulte la sección sobre [Carpeta de contenido](settings.md#content-folder).
+++

+++¿Cómo se añade el ejercicio financiero para la cuenta?

En **[!UICONTROL Configuración]** > **[!UICONTROL Información básica]**, haga clic en **[!UICONTROL Cambiar]**. Desde el **[!UICONTROL El ejercicio financiero comienza a partir de]** , seleccione el mes en cuestión.
+++
