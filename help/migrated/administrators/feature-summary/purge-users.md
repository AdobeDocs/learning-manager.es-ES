---
description: Obtenga más información sobre la purga de datos de usuarios en Learning Manager.
jcr-language: en_us
title: Purgar usuarios
contentowner: dvenkate
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---



# Purgar usuarios

Obtenga más información sobre la purga de datos de usuarios en Learning Manager.

## Resumen {#overview}

Utilice la función Purgar usuario para eliminar la información personal identificable y los registros de aprendizaje del usuario de Learning Manager. Tenga en cuenta que Eliminar y Purgar usuario son dos funciones diferentes. Aunque se puede restaurar un usuario eliminado, no se pueden restaurar todos los datos de usuario y registros de aprendizaje asociados con un usuario purgado.

La acción Purgar usuario puede tener los siguientes resultados:

* Si se purga un usuario, los vínculos de los registros de importación no funcionan para evitar la descarga de archivos CSV antiguos y la recuperación de los datos del usuario en el sistema.
* Si se purga un autor, su nombre se sustituye por el nombre del administrador que purgó ese usuario.
* Si se purgan instructores, se eliminan de las sesiones. El administrador debe reemplazar o añadir instructores para estas sesiones.
* La depuración de un usuario en Learning Manager no elimina al usuario en ninguna aplicación externa (sistemas de terceros u otras aplicaciones escritas por usted). Póngase en contacto con propietarios de aplicaciones externas para eliminar a los usuarios de dichas aplicaciones.
* Si en los valores de configuración de un conector se hace referencia a un usuario purgado, el conector está deshabilitado. El administrador debe volver a configurar el conector para reanudarlo.

Para purgar usuarios, siga estos pasos:

1. Como administrador, seleccione **[!UICONTROL Usuarios]** en el panel izquierdo. La **[!UICONTROL Usuarios internos]** se abre la página.
1. Elimine los usuarios que desee purgar. Para eliminar, seleccione uno o más usuarios usando la casilla de verificación. Abra el **[!UICONTROL Acción]** y seleccione la opción **[!UICONTROL Eliminar usuario.]**
1. En el panel izquierdo, seleccione **[!UICONTROL Limpieza de usuarios]**. La **[!UICONTROL Limpieza de usuarios]** con la lista de usuarios eliminados. Utilice los botones de opción para seleccionar el usuario que desea purgar. Solo puede purgar un usuario a la vez.

   ![](assets/purge-1.png)

   *Seleccione un usuario para purgar*

1. Abra el **[!UICONTROL Acciones]** menú desplegable y seleccione **[!UICONTROL Purgar usuario]**.

   ![](assets/purge-2.png)

   *Seleccione la opción Purgar usuario.*

1. Aparece un cuadro de diálogo que solicita confirmación. Una vez purgados, todos los datos de usuario y registros de aprendizaje asociados con el usuario seleccionado se eliminan de forma permanente. Una vez purgada, la acción no se puede deshacer. Para confirmar, haga clic en **[!UICONTROL Depurar]**.

   ![](assets/purge-3.png)

   *Mensaje de confirmación después de purgar un usuario*

1. Una vez que confirme y haga clic en Purgar, se acepta la solicitud de purga. Recibirá una notificación una vez finalizada la acción. También se proporciona un ID de solicitud de purga. Puede proporcionar este ID al CSM para realizar un seguimiento de la solicitud.

## Purga masiva de usuarios

Puede seleccionar los primeros 50 usuarios y purgar los usuarios de una sola vez. Esto permite a los administradores seleccionar 50 usuarios a la vez y purgarlos todos a la vez. Esto ayuda a los administradores cuando desean purgar usuarios en bloque. Siempre es recomendable comprobar los usuarios seleccionados para la purga. Esto es importante para garantizar que solo se purgue el conjunto correcto de usuarios.

![](assets/bulk-purge-users.png)

*Purgar usuarios de forma masiva*

+++Leer acerca de los resultados de la acción Purgar usuario

<table>
 <tbody>
  <tr>
   <th><strong>Purgar con la interfaz de usuario empresarial de Learning Manager</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Eliminar el usuario seleccionado de la cuenta empresarial solicitante.<br></td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine todos los usuarios de todas las cuentas de prueba cuyo correo electrónico o adobe_id coincida con el correo electrónico de los usuarios seleccionados.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine todos los usuarios de todas las cuentas de prueba cuyo correo electrónico o adobe_id coincida con el correo electrónico de los usuarios seleccionados y él o ella sea el creador de la cuenta de prueba.</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Eliminar el correo electrónico del usuario de todos los demás campos de la cuenta empresarial solicitante y de todas las cuentas de prueba.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Notificar al iniciador de la confirmación de eliminación.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td><strong>Purgar con una interfaz de usuario no empresarial de Learning Manager</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Eliminar el usuario seleccionado de la cuenta de prueba solicitante.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine todos los usuarios de todas las cuentas de prueba cuyo correo electrónico o adobe_id coincida con el correo electrónico de los usuarios seleccionados.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine todos los usuarios de todas las cuentas de prueba cuyo correo electrónico o adobe_id coincida con el correo electrónico de los usuarios seleccionados y él o ella sea el creador de la cuenta de prueba.</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Eliminar el correo electrónico del usuario de todos los demás campos de todas las cuentas de prueba.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Notificar al iniciador de la confirmación de eliminación.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td><strong>Purgar otros usuarios empresariales (individuos que no son usuarios internos o externos de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Eliminar el usuario seleccionado de todos los demás campos de la cuenta empresarial solicitante y de todas las cuentas de prueba.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Eliminación de usuarios de cuentas.</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Notificar al iniciador de la confirmación de eliminación. </td>
   <td>Sí</td>
  </tr>
  <tr>
   <td><strong>Depurar</strong> <strong>otros usuarios no empresariales (individuos que no son usuarios internos o externos de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Eliminar el usuario seleccionado de todos los demás campos de Todas las cuentas de prueba.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Eliminación de usuarios de cuentas.</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Notificar al iniciador de la confirmación de eliminación.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td><strong>Purgar con IMS empresarial de Adobe</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Notifique la solicitud al administrador de la empresa.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Compruebe los campos de correo electrónico para enviar notificaciones.</td>
   <td>No</td>
  </tr>
  <tr>
   <td><strong>Purgar con IMS no empresarial de Adobe</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Elimine de todas las cuentas de prueba a todos los usuarios que tengan el Adobe ID o el correo electrónico proporcionado.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine todos los usuarios de una cuenta de prueba si el correo electrónico/AdobeId proporcionado era el creador de la cuenta.</td>
   <td>Sí</td>
  </tr>
  <tr>
   <td>Elimine el ID de correo electrónico seleccionado de todos los demás campos de todas las cuentas de prueba.</td>
   <td>Sí</td>
  </tr>
 </tbody>
</table>

+++

Learning Manager ahora cumple con el RGPD. Para obtener más información sobre el cumplimiento del RGPD, consulte  [Cumplimiento del RGPD por parte de Learning Manager](../../kb/prime-gdpr.md).

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++¿Cuántos días tarda en completarse una solicitud de purga?

Una solicitud para purgar usuarios tarda un máximo de 30 días en completarse.
+++

+++¿Se puede realizar una purga masiva en Learning Manager?

Sí, puede realizar una purga masiva. Sin embargo, solo puede realizar una purga masiva de 50 usuarios.
+++
