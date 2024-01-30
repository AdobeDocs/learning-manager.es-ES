---
jcr-language: en_us
title: Los vínculos de correo electrónico activados desde plantillas modificadas generan un error en Learning Manager
description: Los vínculos de correo electrónico activados a partir de plantillas modificadas generan un error en Adobe Learning Manager
contentowner: nluke
preview: true
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 73%

---



# Los vínculos de correo electrónico activados desde plantillas modificadas generan un error en Learning Manager

## El problema

Se produce un error después de hacer clic en un vínculo de un mensaje de correo electrónico automatizado, de bienvenida y de inscripción.

**Error**

HTTP Status 400 - Bad request

![](assets/email-404.png)

## Causa

Esto suele ocurrir cuando las plantillas de correo electrónico se personalizan incorrectamente.

**Solución**

Para evitar cualquier error relacionado con vínculos rotos que pueda aparecer debido a la personalización, siga los pasos que se indican a continuación:

1. Inicie sesión como Administrador.
1. En el panel izquierdo, haga clic en **[!UICONTROL Plantillas de correo electrónico]**.

1. Desplácese hasta la plantilla correspondiente y haga clic en ella para modificarla.

   Se abrirá la ventana **Vista previa de plantilla**.

   ![](assets/email-template.png)

   Tenga en cuenta estos puntos al editar una plantilla de correo electrónico:

   * Es recomendable que modifique una plantilla de correo electrónico en la interfaz de Learning Manager.
   * Copie y pegue la plantilla modificada en un archivo de Bloc de notas/Word para guardar una copia de los cambios realizados.
   * Evite reemplazar el texto dinámico de la plantilla que aparece resaltado en azul. Por ejemplo, &quot;**NombreOrganización**&quot;, &quot;**Alumno**&quot;, &quot;**haga clic aquí**&quot;, &quot;**CertificateName**&quot;, etc.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar los cambios aplicados a la plantilla.
1. Active el correo electrónico para verificar si los vínculos funcionan según lo previsto.
1. Revertir los ajustes al original haciendo clic en la opción **Volver al original** para la plantilla modificada.
