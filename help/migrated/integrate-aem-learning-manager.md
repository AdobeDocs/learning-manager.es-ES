---
jcr-language: en_us
title: Integración de Learning Manager con AEM
description: Learning Manager es un sistema de gestión de aprendizaje con un sistema de gestión de contenido de aprendizaje integrado. Los usuarios gestionan su contenido de aprendizaje cargándolo en Learning Manager para que esta solución realice el control de versiones, la asignación a cursos, la configuración de la visibilidad para los alumnos, el seguimiento del consumo y la notificación a los administradores.
contentowner: saghosh
exl-id: 61fae7bd-1703-4ed1-9bd9-07387d67a91c
source-git-commit: 447a4e041d74cf086afada3794ac08a04e70c2ca
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 45%

---

# Integración de Learning Manager con AEM

Learning Manager es un sistema de gestión de aprendizaje con un sistema de gestión de contenido de aprendizaje integrado. Los usuarios gestionan su contenido de aprendizaje cargándolo en Learning Manager para que esta solución realice el control de versiones, la asignación a cursos, la configuración de la visibilidad para los alumnos, el seguimiento del consumo y la notificación a los administradores.

Sin embargo, hay usuarios que almacenan y administran su contenido en sistemas de administración de recursos. El contenido se reutiliza a continuación para otras funciones.

Las distintas tiras presentes en la aplicación del alumno se pueden incrustar en los sitios de AEM. Todos los alumnos que inicien sesión en el sitio de AEM verán sus datos de formación específicos en estas tiras.

## Descargar el paquete de contenido {#downloadthecontentpackage}

El instalador se envía como un paquete de contenido de AEM. [***Descargar el paquete***](https://github.com/adobe/adobe-learning-manager-reference-site).

El paquete de contenido está disponible como archivo zip y es compatible con AEM 6.4 y AEM 6.5.

## Instalar el componente de Learning Manager {#installcaptivateprimecomponent}

Instale el paquete de contenido de Learning Manager mediante el Administrador de paquetes de AEM:

>[!NOTE]
>
>Para obtener información sobre la instalación de paquetes, consulte [***Cómo trabajar con paquetes***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=es#how-to-work-with-packages).

1. Como autor de AEM, abra el Administrador de paquetes de AEM.
1. Haga clic en el botón **[!UICONTROL Cargar paquete]**.
1. Haga clic en **[!UICONTROL Examinar]** y cargue el paquete de contenido.
1. Haga clic en **[!UICONTROL Cargar]**.
1. Después de cargar el paquete, instálelo. Para ello, selecciónelo y haga clic en **[!UICONTROL Instalar]**.

   ![](assets/install-package.jpg)

   *Instalar el paquete de contenido*

## Generar el token de actualización {#generatetherefreshtoken}

El administrador de AEM necesita un token de actualización de la cuenta de Learning Manager. El administrador de integración de Learning Manager generará el token de actualización.

1. Apruebe la aplicación destacada AEM Sites.

   Haga clic en **[!UICONTROL Aplicaciones]** > **[!UICONTROL Aplicaciones destacadas]** > **[!UICONTROL Adobe Experience Manager - Sitios]**.

   ![](assets/launch-aem.jpg)

   *Aprobar la aplicación*

1. Haga clic en **[!UICONTROL Aplicaciones]** > **[!UICONTROL Aplicaciones destacadas]** y abra la aplicación AEM sitios.

   Copie el ID de aplicación y la descripción.

1. Haga clic en **[!UICONTROL Recursos del desarrollador]** > **[!UICONTROL Tokens de acceso]**.

   ![](assets/click-tokens.jpg)

   *Generar los tokens de acceso*

1. Introduzca los siguientes datos:

   * ID de cliente, que es el ID de aplicación.
   * Secreto de cliente, que está presente en la descripción.

1. Obtenga el código de OAuth. Debe utilizar la API v2 en el URI de redirección.
1. Haga clic en **[!UICONTROL Enviar]** y obtenga el token de actualización.

## Configurar el widget en AEM {#configurethewidgetinaem}

Para la configuración de widgets, el autor AEM solo necesita el token de actualización proporcionado por el administrador de integración de Learning Manager.

También puede establecer varias configuraciones de cuenta en varias páginas.

1. Haga clic en **[!UICONTROL Herramientas]** > **[!UICONTROL Cloud Service]** > **[!UICONTROL Configuración del widget de Learning Manager]**.
1. Haga clic en **[!UICONTROL Crear]**.
1. Introduzca el token de actualización aquí. Configure los demás ajustes.
1. El nombre de host debe cambiarse a &quot;learningmanagereu&quot; para las regiones de la UE.
1. Guarde y cierre la configuración.
1. Seleccione una configuración y publíquela.

## Autor de AEM {#aemauthor}

El autor de AEM debe añadir primero el componente de AEM.

A continuación, el autor de AEM podrá arrastrar y soltar el componente Adobe Learning Manager y configurarlo según corresponda.

El componente Learning Manager requiere que la configuración creada en el paso anterior se asigne a la página.  El autor puede asignar la configuración editando las propiedades de la página en **[!UICONTROL Configuración avanzada]** > **[!UICONTROL Configuración]** > **[!UICONTROL Configuración de la nube]** y proporcionar la ruta de la configuración. De este modo, el autor puede crear configuraciones para varias cuentas de Learning Manager y asignar cada una a una página de sitios diferente. Si una configuración no está asignada a la página, el componente leerá la configuración de Página principal de forma recursiva hasta que encuentre una.

## El alumno {#learner}

El alumno puede realizar los cursos desde la página.

Para poder acceder al widget de Learning Manager, el alumno debe haber iniciado sesión AEM usuario. Además, la propiedad **email** debe estar presente en el nodo &quot;/profile&quot; del nodo rep:User del alumno. Este correo electrónico debe ser exactamente igual al que aparece en la cuenta de Learning Manager.

El alumno puede realizar los cursos desde la página.

También se guarda el progreso del curso.

Se proporcionan los siguientes widgets:

1. Interacción
1. Calendario de aprendizaje
1. Widget social
1. Widget Catálogo
1. Mi aprendizaje
1. Recomendación en función del aprendizaje de los compañeros
1. Recomendaciones del administrador
1. Recomendación en función de los intereses del alumno

Si no hay recomendaciones, el widget aparecerá en blanco.

## Compatibilidad con Skyline

Skyline es la versión en la nube de AEM. Primero debe instalar Skyline desde el administrador de paquetes. Para utilizar el componente Skyline en AEM, debe haber un usuario en la cuenta de Learning Manager. En otras palabras, la dirección de correo electrónico del usuario debe existir en la cuenta.

### Implementar Skyline

Los pasos para configurar Skyline se indican en el [repositorio de GitHub](https://github.com/adobe/captivate-prime-aem-components).

## Widget Catálogo

El widget Catálogo muestra formación de un catálogo específico o un conjunto de catálogos a un usuario. En la sección Propiedades de las propiedades de la página, seleccione Catálogo entre las opciones de la lista.

<!--![](assets/catalog-widget.png)-->

El widget Catálogo contiene las siguientes opciones:

* **[!UICONTROL ID de catálogo]:** ID de catálogo separados por comas para los que se debe mostrar el curso de formación.
* **[!UICONTROL Orden]:** Tipo de orden del curso de formación. Las opciones son: nombre, fecha, fechaCreado, fechaInscrito, etc.
* **[!UICONTROL Estado del alumno]:** Devuelve todos los cursos de formación que utilizan los siguientes filtros: enrolled, started, completed y not enrolled. Los resultados de la búsqueda no se mostrarán si la opción de ordenación es dateEnrolled, dueDate o dateEnrolled.
* **[!UICONTROL Nombre de la aptitud]:** Aptitud utilizada para filtrar los cursos de formación exactos.
* **[!UICONTROL Nombre de etiqueta]:** Etiqueta utilizada para filtrar resultados exactos.

Estos son algunos componentes adicionales que puede personalizar:

**[!UICONTROL Tipos de objetos de aprendizaje]:** Filtra según el tipo del objeto de aprendizaje. Los tipos admitidos son: curso, certificación, ayuda de trabajo y programa de aprendizaje.

En AEM, el título de una tarjeta de una tira estará vacío inicialmente. En propiedades, escriba el nombre del título en widgets.html.

**Personalización**

Puede personalizar la apariencia del diseño mediante widgets.html. Puede cambiar el aspecto de las tarjetas que aparecen y personalizar el tema.

En la sección **[!UICONTROL Configuración general]**, puede elegir los colores principales y secundarios de las tarjetas y especificar las propiedades para personalizar el tema.

```
{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### Ignorar inscripción de objetos de aprendizaje de orden superior

Si la casilla de verificación **Ignorar inscripción en objeto de aprendizaje de orden superior** está activada y un usuario está inscrito directamente en un programa de aprendizaje o certificación, los cursos de esa certificación o programa de aprendizaje se mostrarán para el usuario en los widgets.

Si la casilla de verificación está desactivada, los cursos presentes en el programa de aprendizaje o la certificación en los que el usuario no se ha inscrito directamente no aparecerán.

![](assets/higher-order-lo.png)

*Seleccione la casilla Ignorar Inscripción de Objeto de Pedido Superior.

A continuación, la configuración se aplica al widget.

### Seguridad

Se añaden el ID y el secreto de cliente. Además, se oculta el token de actualización. Después de que un usuario cree toda la configuración, si el usuario vuelve a abrir la configuración para editarla o si otro usuario abre esta configuración, se enmascarará el token de actualización.
