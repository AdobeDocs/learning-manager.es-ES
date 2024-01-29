---
title: Experiencia de inicio de sesión no registrado para alumnos
description: El portal nativo de Adobe Learning Manager admitirá una forma no registrada de acceder al sitio de formación. Con este modo activado, los alumnos pueden descubrir y acceder al sitio de formación y consultar los distintos cursos y contenidos disponibles. La experiencia de no conexión permite a los alumnos examinar cursos sin haber iniciado sesión en un portal.
source-git-commit: aef2dfe9d6f49dcccaf1f71b57ffa25a3075efe8
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Experiencia de inicio de sesión no registrado para alumnos

El portal nativo de Adobe Learning Manager admitirá una forma no registrada de acceder al sitio de formación. Con este modo activado, los alumnos pueden descubrir y acceder al sitio de formación y consultar los distintos cursos y contenidos disponibles.

La experiencia de no conexión permite a los alumnos examinar cursos sin haber iniciado sesión en un portal.

Para habilitar la página de inicio que no ha iniciado sesión, el administrador de integración debe habilitar y configurar la [Conector de datos de formación](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access).

A continuación, el curso de formación se puede exportar desde el conector.

>[!NOTE]
>
>Asegúrese de que la opción Native Learning Manager esté seleccionada.

El administrador puede modificar y configurar la página de inicio, que está destinada a los usuarios que no han iniciado sesión.

## Iniciar las opciones de la página de inicio

En la página principal de Adobe Learning Manager, seleccione **Branding**. A continuación, en el panel izquierdo, seleccione No registrado en la página de inicio.

![opciones de homepage](assets/non-logged-in-homepage.png)

*Seleccione la opción No registrado en la página de inicio*

## Añadir un banner

Añade un banner para cualquier anuncio de marketing o función del tema del momento. Seleccionar **Añadir banner**.

![banner](assets/add-banner-image.png)

*Añadir un banner*

Vaya a la ubicación de la imagen que se utilizará como banner. A continuación, proporcione un vínculo como botón de acción en la imagen del banner.

## Añadir categorías

Este componente se puede utilizar para filtrar catálogos por etiquetas, aptitudes y catálogos. Esta sección contiene un encabezado y una descripción para cada categoría. Al hacer clic, se redirige al usuario a la página del catálogo con los filtros aplicados.

Seleccionar **[!UICONTROL Añadir categoría]**. A continuación, introduzca los detalles de la categoría.

![agregar categoría](assets/add-category.png)

*Agregar las categorías*

Guarde la categoría. La categoría se agrega a la sección.

## Añadir un catálogo

Añada un catálogo para los usuarios que no hayan iniciado sesión, de modo que puedan examinar toda la formación en la plataforma.

![añadir catálogo](assets/add-catalog.png)

*Añadir un catálogo*

Estarán presentes todos los cursos de formación exportados.

## Funciones no compatibles

* Las ayudas de trabajo no se exportarán. Sin embargo, los alumnos pueden verlos después de iniciar sesión.
* Ordenar por en el componente de catálogo.
* Configuración de vista predeterminada utilizada en la aplicación de administración (Configuración > General > Vista de lista).
* Valoración basada en estrellas/eficacia.
* Ajuste del icono de tarjeta.
* Configuración de etiquetas y aptitudes relevantes.
* Vista de la aplicación del alumno que se muestra en el catálogo.
* Páginas de información general de formación: al hacer clic en la tarjeta se redirige a Registrarse, tras lo cual se redirige al usuario a la página de información general de formación/página de instancias.
* Todos los catálogos activados estarán presentes. Cualquier alumno que no tenga acceso a un catálogo no podrá ver el catálogo ni la formación en él después de iniciar sesión.
