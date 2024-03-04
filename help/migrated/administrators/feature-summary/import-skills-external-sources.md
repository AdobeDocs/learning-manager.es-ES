---
jcr-language: en_us
title: Importar aptitudes desde orígenes externos
description: Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, mediante los conectores correspondientes.  Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en Learning Manager y estarán disponibles para los autores durante el flujo de trabajo de creación del curso.
contentowner: saghosh
source-git-commit: fc77dad8f39d6d29c8ec74eb5ba137bf12ab7f8c
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Importar aptitudes desde orígenes externos

Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, mediante los conectores correspondientes. Esta mejora forma parte del objetivo de integrar Learning Manager con Skills Cloud y Talent Management Systems externos. Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en Learning Manager y estarán disponibles para los autores durante el flujo de trabajo de creación del curso. También se han realizado mejoras en la funcionalidad de búsqueda de aptitudes en toda la plataforma para proporcionar una mejor experiencia de búsqueda cuando la cuenta tiene un gran número de aptitudes.

## Configurar importación de aptitudes

Siga los pasos del procedimiento para habilitar la importación de aptitudes en la cuenta.

1. En la aplicación de administración, seleccione **Configuración** en el panel izquierdo.
1. Seleccionar **General**.
1. En la **Importación de aptitudes** , seleccione **Habilitar**. Si está activado, puede elegir un origen externo para importar **Aptitudes**. Las aptitudes de los recursos de aprendizaje existentes se importarán al repositorio de aptitudes una vez durante la ejecución inicial. Para todas las importaciones posteriores de recursos de aprendizaje, las aptitudes se importarán en el repositorio de aptitudes solo para los elementos recién importados.
1. Seleccione un proveedor de contenido en el menú desplegable.

## Flujo de trabajo del administrador de integración

El administrador de integración carga los archivos CSV (aptitud, nivel de aptitud y curso) y, a continuación, migra los cursos a la cuenta. Por ejemplo, una vez que el administrador selecciona LinkedIn Learning, puede programar una actividad en la que se importen las aptitudes y los niveles a Adobe Learning Manager.

## Exportar las aptitudes

Como administrador,

1. Seleccionar **Aptitudes** en el panel izquierdo.
1. Seleccione el origen de cualquier aptitud. Puede ver los cursos, las ayudas de trabajo, los alumnos inscritos y los instructores del curso.

### Editar una aptitud

Seleccione una aptitud. En la **Editar una aptitud** , no se puede editar el nombre y la descripción de la aptitud. Sin embargo, puede añadir dominios de aptitudes y una insignia para la aptitud.