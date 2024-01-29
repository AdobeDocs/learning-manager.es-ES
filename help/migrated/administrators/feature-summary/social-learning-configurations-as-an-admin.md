---
description: Como administrador, puede habilitar, deshabilitar y supervisar las actividades realizadas en Aprendizaje social. Una vez activada la función Aprendizaje social, los alumnos pueden verla y empezar a participar en Aprendizaje social.
jcr-language: en_us
title: Supervisión y moderación de Aprendizaje social como administrador
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3604'
ht-degree: 0%

---



# Supervisión y moderación de Aprendizaje social como administrador

Como administrador, puede habilitar, deshabilitar y supervisar las actividades realizadas en Aprendizaje social. Una vez activada la función Aprendizaje social, los alumnos pueden verla y empezar a participar en Aprendizaje social.

## Habilitar y configurar opciones en Aprendizaje social {#enableandconfiguresettingsinsociallearning}

Para activar y configurar la función de Aprendizaje social, haga lo siguiente:

1. Haga clic en **[!UICONTROL Aprendizaje social]** desde el panel de navegación izquierdo. Se le redirigirá a la página de actividad.
1. Habilitar **[!UICONTROL Aprendizaje social]** mediante la función **[!UICONTROL Habilitar]** en la página Actividad si la está activando por primera vez. De lo contrario, se puede activar desde la **[!UICONTROL Configuración]** página.

   Aparece un cuadro de diálogo emergente como la captura de pantalla a continuación.

   ![](assets/artboard-20-2x.png) ![](assets/enable-social-learningforthefirsttime.png)

   *Activar el aprendizaje social*

<!-- ![](assets/enable-social-learningfeatureinsettings.png) ![](assets/enable-social-learningdialog.png)-->

El administrador puede configurar opciones de Aprendizaje social. La configuración incluye tipos de gestión del contenido como **[!UICONTROL Conservación solo manual]** y **[!UICONTROL Sin gestión]**. La configuración del ámbito se puede establecer en un ámbito diferente, como el tipo de usuario (interno/externo) o cualquier otro campo activo presente en la cuenta. El administrador puede establecer la ruta URL desde la que los alumnos pueden descargar la aplicación de Adobe Learning Manager para escritorio.

## Revisión de contenido {#contentcuration}

Dado que el Aprendizaje social es un aprendizaje informal, su funcionalidad es similar a la de otras plataformas de redes sociales. A menudo, las redes sociales distraen a las personas porque consumen con frecuencia contenido irrelevante que afecta a su productividad. Este pensamiento puede ser atendido por la moderación de contenido y la curación.

**[!UICONTROL Conservación solo manual]** y **[!UICONTROL Sin gestión]** Hay dos opciones de revisión que el administrador puede seleccionar.

**[!UICONTROL Gestión manual asistida automáticamente]:** Learning Manager cuenta con un motor de revisión automática basado en inteligencia artificial que puede descubrir de forma inteligente la esencia del contenido en cualquier formato que se pueda proporcionar posteriormente a los alumnos deseados. También puede aprobar o rechazar la publicación de un contenido en función de su puntuación de confianza.

Por ejemplo, Adarsh es un alumno y encontró un blog interesante, por lo que lo publica en la plataforma de aprendizaje social de Adobe Learning Manager. A continuación, la publicación se envía al motor de gestión de contenido basado en IA, que predice las aptitudes presentes en el contenido y las compara con las aptitudes asociadas del tablero. Si alguna de las aptitudes coincide, el contenido se publica; de lo contrario, se envía para una revisión solo manual.

La puntuación de confianza mínima necesaria para publicar es del 50 %.

**[!UICONTROL Conservación solo manual]:** Para comprobar la autenticidad del contenido antes de que se active, el administrador puede activar la configuración de gestión solo manual. Una vez activada la configuración de revisión solo manual, va a los expertos en la materia principales (máximo 3) para la revisión. Sobre la base de la respuesta media, la publicación se aprueba o se rechaza en consecuencia. Si la respuesta es mayor que el 50 por ciento, la publicación se publica o se rechaza. Para obtener más información sobre las PYME, [haga clic aquí](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

## Conservación automática del contenido {#autocuration}

Moderar el contenido manualmente suele ser propenso a errores y requerir mucho tiempo. Además, el proceso no es escalable y no es adecuado para un gran volumen de actividades sociales. Por lo tanto, la selección de contenido se vuelve crítica automáticamente cuando se atiende a muchos usuarios que son activos socialmente.

En Learning Manager, hay una opción para seleccionar contenido automáticamente. La revisión se controla mediante un motor habilitado para IA, que asigna las aptitudes predefinidas, después de que el administrador asigne las aptitudes predefinidas con una aptitud. Para obtener más información, consulte [Asignación de dominio de aptitudes](curation-skills.md).

En la conservación automática, se permiten los siguientes tipos de contenido:

* PDF
* Archivos de audio y vídeo
* Presentations: PPT o PPTX
* Documentos: .doc, .docx

Un administrador puede activar la opción para seleccionar contenido automáticamente desde la aplicación del administrador.

1. En el panel izquierdo de la aplicación de administración, haga clic en **[!UICONTROL Aprendizaje social]**.
1. En la página, haga clic en la ficha **[!UICONTROL Configuración]**.
1. Active la opción **[!UICONTROL Gestión manual asistida automáticamente]**.

   ![](assets/auto-curation.png)

   *Seleccione la opción Gestión manual con asistencia automática*

Cuando un usuario carga un contenido en un tablero, un algoritmo basado en Inteligencia artificial extrae el texto del contenido y, a continuación, lo pasa al motor de revisión. El motor de revisión intenta encontrar las aptitudes presentes en el contenido.

Las aptitudes previstas del contenido cargado se emparejan con las del tablero en el que se cargó el contenido.  Si alguna aptitud coincide con una puntuación de confianza de más del 50 % de la aptitud del tablero, el contenido se publica en el tablero. Si la puntuación de confianza es inferior al 50 %, el contenido se envía para revisión manual.

Cada vez que se selecciona automáticamente un contenido, el usuario recibe una notificación de que el contenido está disponible en el tablero en el que se cargó anteriormente.

![](assets/only-ai-based.png)

*Diagrama de flujo de la configuración de revisión*

Se recomienda que el administrador añada expertos en la materia para aptitudes si la revisión solo manual está activada. El administrador puede añadir expertos en la materia al proporcionar puntos de expertos en la materia por adelantado a los usuarios con experiencia en una aptitud. Para obtener más información sobre cómo proporcionar puntos a las PYME,  [haga clic aquí](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

**Sin gestión:** Las publicaciones de todos los alumnos se publican automáticamente sin moderación de contenido.

<!--![](assets/artboard-6-2x.png)-->

## Preguntas frecuentes sobre la revisión automática de contenido {#faq-auto-curation}

+++ ¿Cuánto tiempo tiene un experto en la materia para seleccionar una publicación?

Un experto en la materia dispone de un mínimo de 24 horas para seleccionar una publicación. Debido a las diferencias de zona horaria, puede aumentar a 47 horas.

+++

+++¿Pasa al siguiente conjunto de tres expertos en la materia si los tres están disponibles? ¿Siempre participan tres expertos en la materia?

La solicitud de revisión pasa a la parte superior de los expertos en la materia el primer día. Si no responden, la solicitud pasa a los tres siguientes expertos en la materia al día siguiente.

Si los tres nuevos expertos en la materia no responden, la solicitud pasa a los moderadores del tablero.

Si los moderadores del tablero no responden, la solicitud se aprueba automáticamente.

+++

+++Si dos expertos en la materia realizan la revisión y uno no la realiza, ¿la solicitud pasa al cuarto experto o la solicitud obtiene el promedio de la valoración de la publicación correspondiente a la primera ronda de expertos en la materia?

Se requiere un índice de aprobación del 50 % para aprobar la publicación. Del mismo modo, se utiliza una tasa de rechazo del 50 % para rechazar la publicación. En cada aprobación realizada por un experto en la materia, se evalúa si ha alcanzado el 50 %.

Si no se alcanza el 50 % después de un día, se envía al siguiente conjunto de expertos en la materia y caducan las solicitudes de revisión anteriores sin respuesta.

Por ejemplo, el primer día, la solicitud de revisión se envía a tres expertos en la materia; uno de ellos la aprueba y dos de ellos no responden. Al día siguiente, la solicitud de revisión pasa al siguiente conjunto de tres expertos en la materia; en este nivel, hay cuatro expertos en la materia activos en total. Al menos dos expertos en la materia deben aprobarla para que se apruebe la revisión.(En el caso de que dos la aprueben y dos la rechacen, se utilizará la cantidad que primero alcance el 50 %).

+++

+++Según lo que veo, solo se asigna un &quot;moderador&quot; (y no es obligatorio) cuando alguien crea un nuevo tablero. ¿En qué casos un alumno puede asignar un &quot;moderador&quot; a un tablero si se van a asignar expertos en la materia a la aptitud a la que está asociado un tablero?

Las siguientes son las responsabilidades de un moderador del tablero social:

* Posibilidad de editar el nombre del tablero, la descripción, la configuración de visibilidad del tablero y otra configuración.
* Posibilidad de eliminar una publicación del tablero en caso de que la publicación no sea adecuada para el público.
* El moderador recibe notificaciones de &quot;Informar de una irregularidad&quot; en el tablero.
* El moderador recibe solicitudes de revisión si no hay ningún experto en la materia presente para el tablero.

+++

+++Nuestro equipo de formación añadirá/supervisará las aptitudes asociadas al nivel de aptitud, así como los expertos en la materia asignados a las aptitudes.

Los expertos en la materia se añaden o asignan en función de la aptitud, no del nivel. Esto es como se ha diseñado.

+++

+++¿Cuál es la diferencia entre un &quot;moderador&quot; de aprendizaje social y un &quot;experto en la materia&quot; de aprendizaje social?

**Moderadores:** Dueños secundarios de la junta. Los creadores los añaden mientras se crea el tablero para que puedan controlarlo en ausencia del creador. De forma predeterminada, el creador del tablero es el moderador.

**PYME:** Los expertos en la materia son expertos en habilidades específicas. El administrador puede asignar expertos en la materia a una aptitud concreta para seleccionar el contenido de dicha aptitud. Los expertos en la materia reciben las solicitudes de revisión de los tableros vinculados a sus aptitudes. Los alumnos también pueden convertirse en expertos en la materia mediante la obtención de puntos.

+++

+++Si hay dos o tres expertos en la materia asignados a una aptitud, ¿la aprobación o el rechazo de una publicación de Aprendizaje social dependen de la revisión de todos los expertos en la materia o de quién la realice primero?

Se requiere un índice de aprobación del 50 % para aprobar la publicación. Del mismo modo, se utiliza una tasa de rechazo del 50 % para rechazar la publicación. En cada aprobación realizada por un experto en la materia, se evalúa si ha alcanzado el 50 %.

Si no se alcanza el 50 % después de un día, se envía al siguiente conjunto de expertos en la materia y caducan las solicitudes de revisión anteriores sin respuesta.

+++

## Configuración del ámbito {#scopesettings}

En Aprendizaje social, un ámbito determina los tableros que se ven, lo que controla la visibilidad del contenido. Si un usuario tiene un ámbito, por ejemplo, ***Proveedor_A***, solo puede ver los tableros y publicaciones asociadas creados por otras personas que pertenezcan al mismo ámbito ***Proveedor_A***.

Esto permite a los administradores mantener una cohorte de usuarios, por ejemplo, proveedores, socios o departamentos de una organización por separado.

Permite el aprendizaje social y la tabla de posiciones tanto para usuarios internos como externos.

Hay secciones separadas para habilitar a los usuarios internos y externos.

**Activar para alumnos internos**

En esta sección, puede elegir la característica de usuario para definir el ámbito de aprendizaje social para usuarios internos. Usuarios con las mismas características **valor** compartir el mismo espacio de Aprendizaje social.

Desde el **Característica de usuario** , elija la opción que corresponda.

![](assets/choose-value-of-usercharacteristic.png)

*Seleccione las características del usuario para definir el ámbito*

De forma predeterminada, la opción **[!UICONTROL Todos los usuarios internos]** en la opción Lista desplegable de características de usuario siempre está seleccionada.

Puede definir el ámbito de los usuarios internos en función de sus campos activos.

**Activar para alumnos externos**

Para definir el ámbito de aprendizaje de los usuarios externos, utilice un perfil externo. Los alumnos con el mismo perfil externo comparten un espacio común de Aprendizaje social.

![](assets/choose-an-externalprofile.png)

*Habilitar ámbito para alumnos externos*

El ámbito de los usuarios externos se basa en sus perfiles externos.

Por ejemplo, en la lista anterior, si habilita **[!UICONTROL Acme Corp]**, todos los alumnos que pertenecen a Acme Corp pueden ver los tableros que han creado. Si desactiva la opción **Henry Cavill**, los alumnos no pueden ver ningún tablero creado por Henry Cavill.

El administrador puede definir el ámbito de visibilidad del contenido en función del campo activo que se muestre en la **[!UICONTROL Característica de usuario]** campo.

Por ejemplo, el administrador puede establecer el ámbito en **[!UICONTROL Tipo de usuario (interno/externo)]** usuarios. Al establecer el ámbito en Tipo de usuario, el contenido compartido en la plataforma de Aprendizaje social por cualquier alumno interno solo es visible para otros alumnos internos de la organización, no para los usuarios externos, y viceversa.

Después de que el administrador seleccione una característica de usuario, puede limitar la función de aprendizaje social a alumnos y grupos de alumnos seleccionando la casilla de verificación debajo del campo de características de usuario. Haga clic en el campo de valor para seleccionar el alumno o los grupos de alumnos para los que desea activar la función Aprendizaje social.

De forma predeterminada, el ámbito lo establece el **[!UICONTROL Tipo de usuario]** alumnos internos o externos.

Si el campo activo no contiene ningún valor, el **[!UICONTROL Valor]** la lista desplegable de campos no estará visible para el administrador.

<!--![](assets/scope-settings.png) ![](assets/scope-settings1-png.jpg)-->

Los usuarios también pueden publicar su contenido mediante la aplicación de Adobe Learning Manager para escritorio. Dependiendo de si es usuario de Mac o Windows, haga clic en los vínculos correspondientes para descargar la aplicación de escritorio y siga los pasos indicados para instalarla en el sistema. Si tiene dificultades en la instalación, [haga clic aquí](../../kb/troubleshooting-issues-with-adobe-learning-manager-desktop-app.md).

## Permisos de creación de tableros {#permission}

Para restringir la creación de tableros de todos los alumnos y moderarlos de forma eficaz, un administrador puede conceder permisos para crear tableros a un grupo seleccionado de usuarios.

![](assets/grant-permissiontocreateboards.png)

*Definir permisos para crear un tablero*

De forma predeterminada, la opción **[!UICONTROL Todos los alumnos]** está activado.

**[!UICONTROL Todos los alumnos]:** Si elige esta opción, todos los usuarios internos y externos pueden crear tableros.

**Un grupo de alumnos:** Si elige esta opción, sólo los usuarios que tengan permisos para crear un tablero verán el **[!UICONTROL Crear nuevo tablero]** en Aprendizaje social. Elija el grupo de usuarios al que se debe conceder permiso para crear un tablero. También puede añadir grupos de usuarios generados automáticamente y personalizados.

<!--![](assets/grant-permissiontoausergroup.png)-->

Los usuarios que comparten el mismo ámbito solo pueden ver el tablero. Para los usuarios que no tienen permiso, el **[!UICONTROL Crear nuevo tablero]** el vínculo permanece invisible.

Para que los cambios surtan efecto, espere 60 minutos.

## Usuarios especiales {#privilege}

Un administrador puede otorgar privilegios especiales a un grupo de usuarios, mediante los cuales los miembros del grupo pueden participar en todos los tableros. El grupo de usuarios especiales omite cualquier restricción establecida en la sección Configuración del ámbito.

El grupo de usuarios puede generarse automáticamente o personalizarse.

Un usuario al que se le haya concedido este privilegio tiene acceso a todos los tableros, excepto **tableros privados**.

![](assets/special-users.png)

*Otorgar privilegios especiales*

Cuando el administrador selecciona un grupo de usuarios, de forma predeterminada, todos los usuarios del grupo pueden acceder a todos los tableros, independientemente del ámbito del usuario. Cualquier usuario con estos privilegios elevados puede ver y participar en todos los tableros internos y externos.

Los usuarios especiales reciben solicitudes de revisión en todos los ámbitos si los usuarios tienen suficientes puntos expertos en la materia para esa aptitud.

Si el usuario no dispone de los puntos de experto en la materia necesarios, los privilegios de revisión se transfieren a los tres expertos en la materia principales de esa aptitud.

En el nuevo ámbito, obtiene puntos para actividades transversales.

En las secciones de tabla de clasificación social, un usuario puede ver todos los usuarios de su ámbito junto con usuarios especiales.

Si se le han concedido privilegios de usuario especiales, puede ver todos los usuarios de la cuenta en su tabla de posiciones, independientemente de los ámbitos de los usuarios.

Si los usuarios especiales se convierten en PYMES al obtener puntos suficientes, aparecen en el **[!UICONTROL Principales expertos en la materia]** en la tabla de líderes sociales.

Para que los cambios surtan efecto, espere 60 minutos.

## Personalizar el banner social {#customize-social-banner}

El administrador puede personalizar el título y el subtítulo que aparecen en la imagen de encabezado de la página principal de Aprendizaje social. Independientemente de lo que el administrador decida introducir como título y subtítulo, las mismas funciones se encuentran en la página principal de Aprendizaje social del alumno.

1. En la aplicación de administración, haga clic en **[!UICONTROL Aprendizaje social]** > **[!UICONTROL Configuración]**.
1. Haga clic en **[!UICONTROL Personalizar]**.
1. Cambie la imagen del banner. Las dimensiones de la imagen deben ser al menos **1600 x 240 px**.
1. Active la opción para ocultar o mostrar el **[!UICONTROL Más información]** en el banner.
1. Introduzca el título y el subtítulo en los campos especificados a continuación:

   ![](assets/image012.png)

   *Personalizar el banner social*

Dispone de otras opciones:

* **[!UICONTROL Idioma]:** En la lista desplegable, elija el idioma al que traducir el título y el subtítulo. También puede añadir texto personalizado para diferentes idiomas.
* **[!UICONTROL Replicar]:** Haga clic en este botón para replicar el título y el subtítulo en todos los idiomas.
* **[!UICONTROL Restablecer]:** Haga clic en este botón para volver al título y al subtítulo originales.

En la página principal de Aprendizaje social, la información proporcionada por el administrador se muestra como encabezado de página.

<!--![](assets/banner-learner.png)-->

## Tendencias {#trends}

Las tendencias de actividad social del alumno se pueden ver y seguir en la pestaña Actividad en la sección Tendencias . Estos datos se pueden ver para diferentes períodos de tiempo, como los últimos siete días, el mes pasado, los últimos tres meses y todo el tiempo.

Los últimos siete días es el valor predeterminado en el filtro de fecha.

>[!NOTE]
>
>Los últimos siete días es el valor predeterminado en el filtro de fecha.

El primer elemento visual proporciona al administrador la siguiente información para el período de tiempo seleccionado en el filtro de fecha:

1. **[!UICONTROL Nuevos mensajes]**: muestra el número de publicaciones nuevas creadas dentro del período de fecha. También se muestra el número total de publicaciones durante todo el período.
1. **[!UICONTROL Porcentaje de usuarios activos]**: muestra el porcentaje total de usuarios activos en Aprendizaje social en comparación con el número total de usuarios disponibles en la cuenta.
1. **[!UICONTROL Nuevas placas]**: muestra el número de tableros nuevos que se han creado. También se muestra el número total de tableros para todo el período.

El segundo elemento visual es un gráfico de líneas que muestra la tendencia del número de tableros o publicaciones creados en función del período de tiempo seleccionado en el filtro de fecha. Haga clic en el filtro para ver las diferentes opciones de tiempo, como los últimos siete días, el mes pasado, los últimos tres meses y todas las horas.

![](assets/trends.png)

*Gráfico de líneas que muestra la tendencia*

## Aptitudes {#skills}

Puede ver todas las aptitudes que se han utilizado en la plataforma de actividad social en esta sección. El administrador puede utilizar el campo de búsqueda para buscar una aptitud que no se haya utilizado todavía al crear un tablero y asignarle expertos en la materia. Al hacerlo, los expertos en la materia recibirían una notificación cuando se creara un tablero con esta aptitud y podrían revisar la publicación como parte del flujo de trabajo de revisión manual.

En el caso de una cuenta con Aprendizaje social deshabilitado, no se muestra ninguna aptitud. La barra de búsqueda también está disponible para estas cuentas, de modo que el administrador tenga la funcionalidad de buscar una aptitud y añadirle expertos en la materia.

El administrador puede ver la puntuación de actividad, el número de publicaciones, tableros, usuarios y nombre de expertos en la materia para cada aptitud utilizada al crear un tablero o una publicación.

<!--![](assets/modify-smes-2.png)-->

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Sl. No.</b></p></td>
   <td>
    <p><b>Nombre de columna</b></p></td>
   <td>
    <p><b>Explicación</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Nombre de aptitud</p></td>
   <td>
    <p>Muestra los nombres de las aptitudes que se utilizan en Aprendizaje social.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Puntuación de actividad</p></td>
   <td>
    <p>Muestra la suma de los puntos de actividad de todos los tableros que pertenecen a la aptitud.</p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Publicaciones</p></td>
   <td>
    <p>Muestra el número total de publicaciones creadas con una aptitud.</p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Tableros</p></td>
   <td>
    <p>Muestra el número total de tableros creados con una aptitud.</p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>Usuarios</p></td>
   <td>
    <p>Muestra el número total de alumnos que han utilizado esa aptitud.</p></td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>PYMES</p></td>
   <td>
    <p>Muestra los 3 expertos en la materia principales actuales de esa aptitud. El administrador puede añadir o modificar expertos en la materia haciendo clic en el vínculo.</p></td>
  </tr>
 </tbody>
</table>

## Dominio de aptitudes {#skilldomain}

En función de las aptitudes utilizadas principalmente por los usuarios finales de Learning Manager, Adobe Learning Manager ha categorizado una lista de 25 dominios de aptitudes que el sistema de gestión automática utiliza para seleccionar contenido. El administrador debe asignar las aptitudes empresariales configuradas a los dominios de aptitudes proporcionados por Captivate Prime. La asignación de aptitudes se puede realizar desde la página Aptitud de administrador al crear una aptitud o modificando una aptitud existente. Para obtener más información sobre cómo asignar o añadir una aptitud, [haga clic aquí](skills-levels.md#Createaskillandalevel).

+++Lista de dominios de aptitudes que utiliza el sistema de revisión de Learning Manager

1. Contabilidad
1. Analytics
1. Ética empresarial
1. Derecho mercantil
1. Proceso empresarial
1. Seguridad informática
1. Gestión de relaciones con los clientes
1. Diseño
1. Finanzas
1. Gestión de recursos humanos
1. Tecnología de la información
1. Aprendizaje
1. Gestión
1. Marketing
1. Medicina
1. Producción y fabricación
1. Gestión de calidad
1. Ventas
1. Investigación científica e ingeniería
1. Redes sociales
1. Habilidades sociales
1. Gestión estratégica
1. Gestión de la cadena de suministro
1. Comunicación técnica
1. Seguridad en el lugar de trabajo

+++

## Expertos en la materia (PYME) {#subjectmatterexpertssmes}

**Expertos en la materia** son personas que tienen un conocimiento y experiencia considerable en una habilidad. Una **PYME** desempeña un papel importante en el aprendizaje social cuando el administrador ha configurado la configuración de revisión como manual o cuando el método de revisión automática no puede seleccionar el contenido. Solo se muestran los tres principales expertos en la materia en la columna Expertos en la materia.

## Requisitos para ser PYME {#requirementstobeansme}

El estatus de pyme solo se puede obtener mediante la obtención de puntos de pyme a través de actividades en Aprendizaje social. El administrador puede otorgar puntos a una PYME en función de su experiencia en el nivel de aptitud.

## Añadir expertos en la materia a una aptitud {#addingsmestoaskill}

Para añadir expertos en la materia a una aptitud, siga estos pasos:

1. Haga clic en **[!UICONTROL Añadir expertos en la materia]** o **[!UICONTROL Modificar expertos en la materia]**.

   ![](assets/add-smes-06.png)

   *Añadir o modificar SME*

1. Haga clic en **[!UICONTROL Opciones avanzadas]** en el cuadro de diálogo emergente.

   ![](assets/advanced-optionssmes.png)

   *Cuadro de diálogo Ver opciones avanzadas*

1. Busque al usuario con experiencia en la aptitud. Una vez que se encuentre el usuario, escriba el número de puntos que desea darle en la **Agregar puntos** cuadro de entrada.

   Si el usuario ya tiene puntos, el número de puntos nuevos otorgados al usuario se añade al número actual de puntos.

   De forma predeterminada, para cada nuevo usuario que vaya a Aprendizaje social, el punto actual es 0.

   ![](assets/advanced-options.png)

   *Añadir puntos para un usuario*

1. Seleccionando el **[!UICONTROL Activar puntos mínimos de SME]** , puede establecer un límite para el número mínimo de puntos que necesita un usuario para mostrarse como experto en la materia en la lista de expertos en la materia principales. Una vez establecido el valor de umbral, los expertos en la materia con puntos inferiores o iguales al valor de punto mínimo requerido no se enumeran en las listas de expertos en la materia.

   Si el **[!UICONTROL Activar puntos mínimos de SME]** Si la casilla de verificación no está seleccionada, los tres usuarios principales con puntos más altos se consideran expertos en la materia para esa aptitud en particular.

1. Haga clic en **[!UICONTROL Guardar]** para mostrar los cambios que se han realizado.

## Sistema de puntos SME {#smepointsystem}

**Se concede a las PYME un número de puntos basado en lo siguiente:**

* Se otorgan 2 puntos a un usuario cada vez que otro usuario vota una publicación creada por él.
* Se otorgan 2 puntos a un usuario cada vez que otro usuario aprueba su comentario.
* Se otorgan 5 puntos a un alumno para responder a una pregunta.
* Se conceden 2 puntos más al alumno cada vez que se vota a favor de la respuesta proporcionada.

## Puntos de estado de pymes basados en la actividad de revisión {#smestatuspointsbasedoncurationactivity}

**Se concede a las pymes una serie de puntos también en función de las actividades de revisión para lo siguiente:**

* Cuando se envía una publicación para revisión manual porque la revisión automática no está segura de si el contenido es relevante o no, el experto en la materia gana 5 puntos al enviar la moderación.

## Descargar configuraciones {#downloadconfigurations}

<!--![](assets/download-config.png)-->

En el caso de los servidores para empresas, el administrador puede cambiar la ubicación desde la que los alumnos pueden descargar la aplicación de escritorio tanto para Windows como para Mac.

![](assets/enterprise-servers.png)

*Cambiar la ubicación de descarga*

La dirección URL de Enterprise Server debe estar alojada públicamente.

## Actividades sociales para el plan de facturación Usuarios activos mensuales {#socialactivitiesformonthlyactiveusersbillingplan}

Cada vez que un usuario crea un nuevo tablero social, publicación social o comentario social, se contaría como actividad válida para ser contada contra el **Usuario de activación mensual**(MAU) si la cuenta sigue el modelo de facturación MAU. Para obtener más información, consulte [administración de facturación](billing-management.md).

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++Cómo habilitar el aprendizaje social para alumnos externos

En **[!UICONTROL Aprendizaje social]** > **[!UICONTROL Configuración]**, en la sección Configuración del ámbito, habilite la opción **[!UICONTROL Activar para alumnos externos]**. En el menú desplegable, elija un perfil externo y defina el ámbito de aprendizaje de ese perfil.

![](assets/social-scope-external-users.png)

*Seleccione la opción Activar para alumnos externos .*
+++
