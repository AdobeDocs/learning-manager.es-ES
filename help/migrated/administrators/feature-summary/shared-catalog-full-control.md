---
jcr-language: en_us
title: Permitir control total del catálogo compartido
description: Permitir control total del catálogo compartido en Adobe Learning Manager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 89%

---



# Permitir control total del catálogo compartido

## Crear catálogo {#createcatalog}

Como administrador, puede crear un catálogo de cursos, programas de aprendizaje, ayudas de trabajo y certificaciones.

Para obtener más información, consulte [Catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Compartir catálogo {#sharecatalog}

Puede compartir los catálogos con usuarios internos de una empresa o con cualquier usuario externo. Sin embargo, el uso compartido es exclusivo. Es decir, un catálogo compartido internamente no se puede compartir con grupos externos y viceversa.

Los cursos, los programas de aprendizaje, las ayudas de trabajo y las certificaciones son los objetos de aprendizaje admitidos para el catálogo compartido.

Para obtener más información, consulte [Compartir catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Permitir control total del catálogo compartido {#fullcontrol}

Puede otorgar acceso completo a su catálogo a cuentas externas. De este modo, el administrador de la cuenta puede aceptar el catálogo y, en consecuencia, añadir o eliminar aprendizajes o módulos.

Para otorgar el control total a una cuenta externa:

1. Después de añadir aprendizajes a un catálogo, debe compartir el catálogo con usuarios externos.
1. En el cuadro de diálogo Cuenta externa, añada el subdominio y el ID de correo electrónico del administrador de la empresa externa.
1. En la opción Control de catálogo, cambie el botón para permitir que los usuarios externos tengan control total del catálogo.

   ![](assets/catalog-control.png)

   *Permitir control total del catálogo compartido*

   Al permitir el control total del catálogo, el administrador de la empresa externa acepta la solicitud para permitir modificaciones en el catálogo. A continuación, el creador de la empresa externa puede editar los cursos o añadir módulos.

   Consulte las secciones siguientes para obtener más información.

## Administrador de empresa externa {#administratorofexternalorganization}

Una vez que el administrador de la empresa anterior permite el control total del catálogo, el administrador de la empresa externa acepta la solicitud, acepta el catálogo y lo visualiza.

1. Haga clic en el icono de la notificación para aceptar el catálogo.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Para aceptar la invitación del catálogo, haga clic en Aceptar.
1. En la lista de catálogos, si inicia el catálogo que se ha compartido con usted, verá un mensaje que indica que el catálogo ahora tiene control total.

   ![](assets/catalog-details.png)

   *Ver detalles del catálogo*

1. Puede modificar el nombre del catálogo y la descripción.

## Compartir catálogo para programa de aprendizaje, certificación y ayudas de trabajo {#sharecatalogforlearningprogramcertificationandjobaids}

Al igual que la concesión del control total del catálogo para los cursos, el administrador puede otorgar el control total del catálogo en los casos siguientes:

* Programas de aprendizaje
* Certificaciones
* Ayudas de trabajo

## Restablecer curso {#resetcourse}

1. En la tarjeta de catálogo que tiene un vínculo roto, haga clic en **[!UICONTROL Restablecer curso]**.

<!-- ![](assets/reset-course.png)-->

1. Verá un mensaje de alerta después de hacer clic en el botón Restablecer. La acción de restablecer el curso:

   * Elimina todo el contenido recién añadido del catálogo.
   * Actualiza el catálogo en sincronización con el catálogo compartido original.
   * Restaura la relación con el objeto de aprendizaje principal.

   La acción de restablecer el catálogo es irreversible. No puede deshacer los cambios que haya realizado en el catálogo.

1. Para aceptar los cambios, haga clic en Sí.
1. En el catálogo de cursos, puede ver el que catálogo ya no muestra el mensaje *Vínculo interrumpido*.

   Si examina los detalles del catálogo, verá que se ha restaurado su estado original.

## Volver a añadir un objeto de aprendizaje {#readdalearningobject}

Si de forma involuntaria ha eliminado un curso, un programa de aprendizaje, una certificación o ayuda de trabajo, se pueden restaurar.

Para restaurar un objeto de aprendizaje eliminado, haga clic en Volver a añadir.

Esta acción invierte la acción y restaura el objeto de aprendizaje en la vista de catálogo.

![](assets/re-add-button.png)

*Agregar de nuevo un objeto de aprendizaje*

Después de hacer clic en el botón Volver a añadir, aparece un mensaje de confirmación que indica que el objeto de aprendizaje se ha añadido correctamente al catálogo.

## Empresa externa {#externalorganization}

Una vez que el administrador de la cuenta externa ha aceptado el catálogo, el autor ya puede añadir cursos y programas de aprendizaje.

1. Como usuario, recibe una notificación de que el catálogo ya está disponible en su cuenta.
1. Para ver una lista de los cursos, haga clic en **[!UICONTROL Cursos]** en el panel de navegación izquierdo. Puede ver todos los cursos que ha creado y los que se comparten con usted.
1. Para ver los detalles del curso, haga clic en **[!UICONTROL Ver curso]** en la tarjeta del curso.

   <!--![](assets/view-course.png)-->

1. En la página de detalles del curso, puede ver información sobre el curso y los módulos compartidos. Para añadir un módulo, haga clic en Añadir módulos. Al añadir módulos a los módulos existentes, los nuevos aparecen al final de los que ya existían. Los módulos siempre se pueden reordenar.
1. Tras haber añadido los módulos, haga clic en Volver a publicar.

   Una vez que haya vuelto a publicar los módulos, en la tarjeta del catálogo aparece el mensaje *Vínculo interrumpido*.

   Como ha actualizado el catálogo original con módulos nuevos, la relación vigente con el curso adquirido ya no existe.

   El objeto de aprendizaje no estará sincronizado con la cuenta de origen, ya que el contenido del objeto de aprendizaje se ha modificado.

   <!--![](assets/link-broken.png)-->

Después de añadir y volver a publicar el módulo, si cree que ha añadido o eliminado por error un curso del catálogo anteriormente, puede restablecer el módulo y revertirlo a su estado original cuando se compartió por primera vez con control total.
