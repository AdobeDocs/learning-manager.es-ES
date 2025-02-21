---
jcr-language: en_us
title: Importar aptitudes desde orígenes externos
description: Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, mediante los conectores correspondientes.  Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en Learning Manager y estarán disponibles para los autores durante el flujo de trabajo de creación del curso.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: d96b25245daadaa0f5a330bcf8a7ab5bba995876
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Importar aptitudes desde orígenes externos

Importe aptitudes de proveedores de contenido, como LinkedIn y Go1, mediante los conectores correspondientes. Esta mejora forma parte del objetivo de integrar Learning Manager con Skills Cloud y Talent Management Systems externos. Las aptitudes importadas se añadirán a las aptitudes definidas por el administrador en Learning Manager y estarán disponibles para los autores durante el flujo de trabajo de creación del curso. También se han realizado mejoras en la funcionalidad de búsqueda de aptitudes en toda la plataforma para proporcionar una mejor experiencia de búsqueda cuando la cuenta tiene un gran número de aptitudes.

## Configurar importación de aptitudes

Siga los pasos del procedimiento para habilitar la importación de aptitudes en la cuenta.

1. En la aplicación de administración, seleccione **Configuración** en el panel izquierdo.
1. Seleccione **General**.
1. En la sección **Importación de aptitudes**, seleccione **Habilitar**. Si está activado, puede elegir un origen externo para importar aptitudes. Una vez activada, para todas las importaciones posteriores de recursos de aprendizaje, las aptitudes se importarán en el repositorio de aptitudes para los elementos recién importados. Las aptitudes de los recursos de aprendizaje existentes se pueden importar al repositorio de aptitudes una vez y, para ejecutar esta ejecución inicial, póngase en contacto con su CSM.
1. Seleccione un proveedor de contenido en el menú desplegable.

Como administrador, solo puede importar aptitudes desde una fuente.

### Nivel de aptitud predeterminado

El nivel de aptitud predeterminado es uno y el crédito es 10 después de migrar las aptitudes.

No puede editar el nombre de la aptitud, la descripción y añadir niveles a aptitudes externas. Sin embargo, puede añadir dominios, insignias y editar créditos.

### Aptitudes y créditos del curso predeterminado

Después de importar aptitudes, se añaden a los recursos de aprendizaje importados del origen que se seleccionó como origen de aptitudes. Por ejemplo, si el origen de la aptitud es LinkedIn Learning, todos los recursos de aprendizaje importados de LinkedIn Learning tendrán las aptitudes que proporciona. Cuando se importa a recursos de aprendizaje, cada recurso de aprendizaje proporciona un valor predeterminado de 10 créditos.

#### Informes

La columna **Origen** con valores: Interno, LinkedIn Learning, Go1, que indica el origen de la importación de aptitudes.

Las aptitudes añadidas recientemente estarán en la parte superior.

En la página de configuración del curso, la columna **Asignado por** que contiene valores, Interno y Proveedor de contenido.


## Flujo de trabajo del administrador de integración

El administrador de integración carga los archivos CSV (aptitud, nivel de aptitud y curso) y, a continuación, migra los cursos a la cuenta. Por ejemplo, después de que el administrador seleccione LinkedIn Learning, el administrador de integración puede programar una actividad en la que las aptitudes y los niveles se importen a Adobe Learning Manager.

## Exportar las aptitudes

Como administrador,

1. Seleccione **Aptitudes** en el panel izquierdo.
1. Seleccione el origen de cualquier aptitud. Puede ver los cursos, las ayudas de trabajo, los alumnos inscritos y los instructores del curso.

### Editar una aptitud

Seleccione una aptitud. En el elemento emergente **Editar una aptitud**, no puedes editar el nombre y la descripción de la aptitud. Sin embargo, puede añadir dominios de aptitudes y una insignia para la aptitud.
