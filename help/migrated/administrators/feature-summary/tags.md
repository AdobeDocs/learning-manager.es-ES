---
description: Aprenda a administrar etiquetas en Learning Manager.
jcr-language: en_us
title: Etiquetas
contentowner: dvenkate
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---



# Etiquetas

Ahora, los administradores pueden gestionar etiquetas en Learning Manager. Utiliza una base de datos de etiquetado y gestión mejoradas para ayudar a los alumnos a buscar mejor y a obtener resultados de búsqueda adecuados rápidamente. Puede administrar etiquetas redundantes, mal escritas e irrelevantes con esta función. También puede agregar, editar, eliminar, anexar o reemplazar etiquetas.

La lista de objetos de aprendizaje asociados a la etiqueta se puede ver haciendo clic en el recuento proporcionado junto a cada etiqueta. La lista muestra el número de cursos, programas de aprendizaje, certificados, ayudas de trabajo y grupos de contenido. Haga clic en cualquiera de estas opciones para ver la lista.

Puede ordenar las etiquetas según el uso o el orden alfabético mediante la **[!UICONTROL Ordenar por]** opción.

## Agregar/ eliminar/ editar etiquetas {#adddeleteedittags}

1. Como administrador, en el panel de navegación izquierdo, haga clic en **[!UICONTROL Etiquetas]**. La **[!UICONTROL Tag Management]** se abre la página.
1. Para añadir una nueva etiqueta, haga clic en **[!UICONTROL Añadir]**. El botón Añadir está disponible en la esquina superior derecha de la página. Si no hay etiquetas existentes, el **[!UICONTROL Añadir]** botón también estará disponible en el medio de la **[!UICONTROL Tag Management]** página.

   Al añadir varias etiquetas, sepárelas con (,) o (;). Un nombre de etiqueta puede contener un máximo de 50 caracteres.

1. Para eliminar una etiqueta existente, selecciónela haciendo clic en la casilla de verificación. Puede seleccionar varias etiquetas de hasta cincuenta en número para eliminarlas a la vez. Para eliminar, siga este paso:

   * Seleccione las etiquetas que desea eliminar > abra el **[!UICONTROL Acción]** menú desplegable > seleccionar **[!UICONTROL Eliminar]**.

1. Solo puede editar una etiqueta a la vez. Para editar una etiqueta, siga este paso:

   * Seleccione la etiqueta que desea editar > abra el icono **[!UICONTROL Acciones]**menú desplegable > clic **[!UICONTROL Editar]**.

   La **[!UICONTROL Editar etiqueta]** que aparece. Introduzca el nuevo nombre de etiqueta y haga clic en **[!UICONTROL Guardar]**.

   Si el nombre de la etiqueta que ha introducido ya existe, Adobe Learning Manager muestra un mensaje de advertencia. No pueden existir dos etiquetas con el mismo nombre.

## Reemplazar etiquetas {#replacetags}

1. Seleccione las etiquetas que desea reemplazar. Puede seleccionar hasta 50 etiquetas a la vez. Abra el **[!UICONTROL Acciones]** menú desplegable y seleccione **[!UICONTROL Reemplazar]**.
1. La **[!UICONTROL Reemplazar etiquetas]** que muestra las etiquetas seleccionadas.

1. En la **[!UICONTROL Nombre de las etiquetas reemplazadas]** , introduzca el nombre de la nueva etiqueta con la que desea reemplazar las etiquetas seleccionadas. Puede sustituirlas por una etiqueta existente en el menú desplegable o añadir una nueva etiqueta.

   El punto y coma o la coma no pueden formar parte del nombre de la etiqueta.  Tenga en cuenta que las etiquetas sin punto y coma y la visualización de mensajes de error al utilizar dichas etiquetas como parte de algún objeto de aprendizaje no se controlarán en los escenarios de migración.

1. Haga clic en **[!UICONTROL Reemplazar]**.

## Anexar etiquetas {#appendtags}

En el caso de la operación Anexar para etiquetas, la etiqueta nueva/existente se anexará a toda la lista de objetos de aprendizaje y grupos de contenido asociados a las etiquetas seleccionadas.

1. Seleccione las etiquetas que desee anexar. Puede seleccionar hasta 50 etiquetas a la vez. Abra el menú desplegable Acciones y seleccione **[!UICONTROL Anexar]**.
1. La  **[!UICONTROL Anexar etiquetas]** que muestra las etiquetas seleccionadas.
1. Puede añadir una etiqueta adicional a todo el aprendizaje con las etiquetas seleccionadas introduciendo el nombre de la **[!UICONTROL Nueva etiqueta]** o en la lista desplegable de las etiquetas existentes. La nueva etiqueta se añadirá a todo el aprendizaje asociado en Learning Manager.

   El punto y coma o la coma no pueden formar parte del nombre de la etiqueta. Si se utiliza, Prime mostrará un mensaje de error. Tenga en cuenta que las etiquetas sin punto y coma y la visualización de mensajes de error al utilizar dichas etiquetas como parte de algún objeto de aprendizaje no se controlarán en los escenarios de migración.

1. Haga clic en **[!UICONTROL Anexar]**.

## Configuración {#settings}

Como administrador, puede otorgar permiso al autor para crear etiquetas haciendo clic en la opción de configuración.

![](assets/unknown-1.jpeg)

*Página Configuración para crear una etiqueta*

* Cuando un usuario tiene permiso para crear etiquetas y selecciona etiquetas existentes que no son válidas en la actualidad,

  Aparece un mensaje de error que sugiere que la etiqueta seleccionada ya no es válida. Las etiquetas nuevas se crearán eliminando los caracteres no admitidos. En este caso, el autor debería poder ver sus etiquetas antiguas convirtiéndose en etiquetas nuevas antes de guardarlas.

* Si el usuario no tiene los permisos necesarios para crear etiquetas nuevas, aparecerá un mensaje de error que indica que la etiqueta seleccionada ya no es válida. Los autores pueden ponerse en contacto con los administradores para modificar etiquetas no válidas.

  Los autores no pueden crear ni guardar etiquetas no válidas. Pueden quitar las etiquetas no válidas y añadir cualquier otra etiqueta válida existente y continuar.
