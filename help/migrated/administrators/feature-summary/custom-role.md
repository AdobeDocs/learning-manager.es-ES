---
jcr-language: en_us
title: Funciones personalizadas
description: La función Rutas de aprendizaje le ayuda a definir funciones personalizadas y a asignar responsabilidades específicas a un conjunto de usuarios. Esta función le permite asignar responsabilidades fuera del ámbito de la función existente de la persona.
contentowner: dvenkate
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '2224'
ht-degree: 0%

---



# Funciones personalizadas

Esta función le ayuda a definir funciones personalizadas y a asignar responsabilidades específicas a un conjunto de usuarios. Esta función le permite asignar responsabilidades fuera del ámbito de la función existente de la persona.

Puede crear una función personalizada para proporcionar capacidades de creación limitadas a un catálogo concreto. También puede crear una función dedicada a administrar informes. Esas funciones pueden asignarse a personas que se supone deben asumir esas responsabilidades específicas.

## Crear una función personalizada {#create-role}

1. Inicie sesión como administrador. Abrir **[!UICONTROL Usuarios]** > **[!UICONTROL Función personalizada]**.
1. Seleccionar **[!UICONTROL Crear función]**. La **[!UICONTROL Crear nuevo rol]** se abre la pestaña.

   ![](assets/create-new-role.png)

   *Crear una función personalizada*

1. Introduzca el nombre en el **[!UICONTROL Nombre de la función]** campo.
1. **[!UICONTROL Privilegios de cuenta]**: Estos privilegios otorgan a los propietarios de roles acceso a aspectos específicos de la configuración del sistema y que actúan en toda la cuenta. Elija los permisos de acceso. El usuario tiene control total sobre los permisos asignados.

>[!NOTE]
>
>   El ámbito no es aplicable a estos privilegios.


![](assets/account-privileges.png)

*Establecer el ámbito*

1. **Privilegios de funciones principales**: Se utiliza para conceder acceso a funciones específicas de administración de actividades de aprendizaje. Con esta opción se pueden conceder permisos para las siguientes funciones.

   * Catálogos
   * Informes
   * Etiquetas

   ![](assets/core-features.png)

   *Establecer el ámbito para catálogos, informes y etiquetas*

1. **Privilegios de funciones: objetos de aprendizaje:**  Utilice esta opción para proporcionar acceso a las funciones relacionadas con los objetos de aprendizaje. Puede proporcionar acceso a los siguientes objetos de aprendizaje.

   * Certificaciones
   * Cursos
   * Ayudas de trabajo
   * Programas de aprendizaje

   También puede otorgar un control de operación específico para los objetos de aprendizaje. El permiso puede ser uno de los siguientes:

   * Control total
   * Editar y eliminar
   * Inscripción
   * Informe

   ![](assets/learning-objects.png)

   *Conceder permisos específicos*

1. **Ámbito de los privilegios de funciones:** El ámbito de los privilegios de funciones asignados a esta función se puede restringir a un grupo de usuarios específico o a uno o varios catálogos.

   Catálogos: utilice el botón de opción para proporcionar control sobre **[!UICONTROL Todos los catálogos]** o utilice el **[!UICONTROL Definir acceso por catálogo]** para proporcionar acceso a catálogos específicos. También puede seleccionar varios catálogos.

   Grupos de usuarios: proporcione acceso a **[!UICONTROL Todos los grupos de usuarios]** o utilice el **[!UICONTROL Definir acceso por grupo de usuarios]** para proporcionar acceso a grupos de usuarios específicos. Solo se puede especificar un único grupo de usuarios.

   >[!NOTE]
   >
   >Si ha seleccionado Anuncio, Interacción, Plantillas de correo electrónico, Aptitudes y Usuarios en Privilegios de cuenta, el acceso a los grupos de usuarios se proporciona a todos los grupos de usuarios de forma predeterminada, y esta opción está desactivada.

   Si ha seleccionado Planes de aprendizaje en Privilegios de cuenta, el acceso a todos los catálogos y grupos de usuarios se proporciona de forma predeterminada y estas opciones de Ámbito están desactivadas.

   ![](assets/define-scope-of-privileges.png)

   *Definir ámbito de privilegios*

>[!NOTE]
>
>   En Learning Manager 27.6, puede crear una función personalizada con un ámbito que abarque varios catálogos, y que cada catálogo tenga asignado su propio conjunto de permisos.


Para otorgar diversos permisos a los catálogos, siga los pasos que se indican a continuación:

1. Haga clic en la opción **[!UICONTROL Definir acceso por catálogo]**.
1. Elija los catálogos y podrá ver el nivel de permiso de cada catálogo. Estos son los permisos:

   <table>
        <tbody>
        <tr>
          <td>
          <p><b>Permiso</b></p></td>
          <td>
          <p><b>Descripción</b></p></td>
        </tr>
        <tr>
          <td>
          <p>Control total</p></td>
          <td>
          <p>Otorga Control total a todos los objetos de aprendizaje. Los permisos incluyen Agregar, Editar, Eliminar, Leer, Inscribir e Informe.<br></p></td>
        </tr>
        <tr>
          <td>
          <p>Informe</p></td>
          <td>
          <p>Otorga acceso a la pestaña Informes solo del objeto de aprendizaje.</p></td>
        </tr>
        <tr>
          <td>
          <p>Inscribir</p></td>
          <td>
          <p>Otorga permiso solo para inscribirse en el objeto de aprendizaje.</p></td>
        </tr>
        <tr>
          <td>
          <p>Solo lectura</p></td>
          <td>
          <p>Otorga permiso solo para ver los objetos de aprendizaje del catálogo.</p></td>
        </tr>
        </tbody>
      </table>

1. Active o desactive los permisos según sus necesidades.
1. Para guardar los cambios, haga clic en **[!UICONTROL OK]**. A continuación, para guardar los cambios de la función personalizada, haga clic en **[!UICONTROL Guardar]**.

Por ejemplo, considere el siguiente escenario.

El permiso resultante que un usuario personalizado tendría en un objeto de aprendizaje es una intersección del permiso de objeto de aprendizaje y el permiso de catálogo.

Un usuario personalizado tiene permiso completo para cursos y acceso de solo lectura para Catálogo A, pero tiene permiso completo para Catálogo B. Los resultados son un acceso de solo lectura en los cursos de Catálogo A y Control total en los cursos de Catálogo B.

Un usuario con una función personalizada puede:

* Ver solo el contenido de los catálogos a los que tiene acceso.
* Acceda a cualquier objeto de aprendizaje en función de los permisos del catálogo del que forma parte el objeto de aprendizaje.

Como administrador, puede:

* Elija más de un catálogo para una función personalizada.
* Modifique los permisos de un catálogo en cualquier momento.
* Elimine los catálogos de un ámbito para el que ya no desee conceder permisos.
* Otorgue implícitamente el permiso Solo lectura a un catálogo cuando conceda permisos al catálogo.

La tabla siguiente ilustra cómo se conceden los permisos.

<table>
    <tbody>
     <tr>
      <td>
       <p><strong> </strong></p></td>
      <td>
       <p><strong>Permiso de nivel de catálogo</strong></p></td>
     </tr>
     <tr>
      <td>
       <p><strong>Permiso de nivel de objeto de aprendizaje</strong></p>
       <p><strong>(Ejemplo: Cursos)</strong></p></td>
      <td>
       <p>Control total</p></td>
      <td>
       <p>Inscribir</p></td>
      <td>
       <p>Informe</p></td>
      <td>
       <p>Solo lectura</p></td>
     </tr>
     <tr>
      <td>
       <p>Control total</p></td>
      <td>
       <p>Control total</p></td>
      <td>
       <p>Inscribir</p></td>
      <td>
       <p>Informe</p></td>
      <td>
       <p>Solo lectura</p></td>
     </tr>
     <tr>
      <td>
       <p>Inscribir</p></td>
      <td>
       <p>Inscribir</p></td>
      <td>
       <p>Inscribir</p></td>
      <td>
       <p>Solo lectura</p></td>
      <td>
       <p>Solo lectura</p></td>
     </tr>
     <tr>
      <td>
       <p>Editar y eliminar</p></td>
      <td>
       <p>Editar y eliminar</p></td>
      <td>
       <p>Solo lectura</p></td>
      <td>
       <p>Solo lectura</p></td>
      <td>
       <p>Solo lectura</p></td>
     </tr>
     <tr>
      <td>
       <p>Informe</p></td>
      <td>
       <p>Informe</p></td>
      <td>
       <p>Solo lectura</p></td>
      <td>
       <p>Informe</p></td>
      <td>
       <p>Solo lectura</p></td>
     </tr>
    </tbody>
   </table>
1. **Usuarios:** Utilice esta opción para determinar a qué usuarios se les asigna esta función. Puede elegir uno o varios usuarios mediante el cuadro de búsqueda.

**Añadir usuarios a la carga de CSV de funciones personalizadas:** Para añadir usuarios mediante la carga de CSV, agregue una columna CustomRole al archivo .csv que el administrador utilizó para importar usuarios. Introduzca la función del usuario en la columna Función personalizada para los usuarios a los que desea asignar una función personalizada. Para cargar el archivo CSV, haga clic en  **[!UICONTROL Agregar > Cargar un CSV]**.

Columna CustomRoleNota:

* No puede buscar grupos de usuarios.
* No puede buscar usuarios que ya tengan asignada la función de administrador.
* La asignación de una nueva función personalizada a un usuario anula la función personalizada anterior del usuario.

<!--![](assets/users.png)-->

* Un administrador personalizado con permiso en Configuración podrá configurar la programación para sincronizar o sincronizar usuarios desde la fuente de datos aunque no tenga permiso para la entidad Usuarios.
* Si un administrador personalizado tiene permiso en la entidad Usuarios, los usuarios se pueden asignar a sí mismos la función de administrador y convertirse en administradores estándar.

## Restringir el acceso a las carpetas a los autores personalizados {#folder-custom-author}

Learning Manager ya admite la posibilidad de conceder acceso a la biblioteca de contenido mediante funciones personalizadas. Todos los autores personalizados que ya tengan acceso a la biblioteca de contenido seguirán teniendo acceso a todos los archivos de contenido incluso después de configurar las carpetas de contenido. Esto es para mantener el comportamiento heredado. Los administradores no necesitan realizar ningún cambio en caso de que deseen continuar con el comportamiento actual.

En caso de que deseen restringir el acceso a estos autores personalizados, los administradores deben editar la función personalizada existente y configurarla proporcionando acceso solo a carpetas de contenido específicas.

![](assets/folder-access-forcustomauthors.png)

*Restringir el acceso a las carpetas a los autores personalizados*

Al crear un autor personalizado, ahora puede asignarle carpetas de contenido. Elija la opción **Carpetas seleccionadas**.

Después de hacer clic en la opción, se abre un nuevo cuadro de diálogo en el que puede asignar las carpetas al autor personalizado.

![](assets/choose-folder.png)

*Seleccione las carpetas del autor personalizado*

Elija las carpetas y haga clic en **[!UICONTROL OK]**.

## Tablero de resumen de aprendizaje para administradores personalizados {#custom-admin-dashboard}

Los administradores personalizados pueden ver la misma vista que un administrador. Un administrador personalizado puede tener datos fuera de su ámbito. Esto solo es aplicable si el administrador personalizado tiene ámbito completo. Para conceder el ámbito completo, al crear un administrador personalizado, habilite la opción **[!UICONTROL Control total]** en el informe de resumen de cuenta.

![](assets/create-custom-role.png)

*Crear una función personalizada*

Como resultado, las opciones, **[!UICONTROL Todos los catálogos]** y **[!UICONTROL Todos los grupos de usuarios]** se seleccionará y el resto se desactivará.

![](assets/scope-of-featureprivileges.png)

*Definir ámbito de privilegios*

## Permisos implícitos {#implicitpermissions}

Cuando a un usuario se le asigna una función con una entidad específica, puede haber casos en los que también necesite acceso a otras entidades para poder realizar tareas en la entidad concedida. Por ejemplo, si se concede a un usuario el acceso Crear en la entidad Curso, este necesita acceder a las entidades Aptitud y Etiqueta para poder asociarlas al curso que se está creando. Esta tabla proporciona información sobre estos permisos implícitos.

<table>
 <tbody>
  <tr>
   <th>Tipo de acceso</th>
   <th>Permiso de entidad concedido por el administrador</th>
   <th>Permiso de entidad implícito</th>
   <th>Acceso implícito</th>
  </tr>
  <tr>
   <td>Gestionar</td>
   <td>Usuario</td>
   <td>Grupo</td>
   <td>Crudo</td>
  </tr>
  <tr>
   <td>Inscribir</td>
   <td>Todos los objetos de aprendizaje (curso, ayuda de trabajo, programa de aprendizaje, certificación)</td>
   <td>Usuario<br>
     Plan de aprendizaje</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>
    <p>Grupo de contenido<br>
      Ayuda de trabajo<br></p></td>
   <td>Etiqueta</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>Curso</td>
   <td>Grupo de contenido<br>
     Etiqueta<br>
     Aptitud<br>
     Insignia<br>
     Ayuda de trabajo</td>
   <td>Leer en todos</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>Programa de aprendizaje<br>
     Certificación<br></td>
   <td>Curso<br>
     Etiqueta<br>
     Aptitud<br>
     Insignia</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>Plan de aprendizaje</td>
   <td>Catálogo<br>
     Grupo<br>
     Aptitud<br>
     Todos los objetos de aprendizaje (curso, ayuda de trabajo, programa de aprendizaje, certificación)</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>Anuncio</td>
   <td>Usuario<br>
     Grupo<br>
     Todos los objetos de aprendizaje (curso, ayuda de trabajo, programa de aprendizaje, certificación)</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>Crear</td>
   <td>Interacción</td>
   <td>Branding</td>
   <td>Escribir</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Usuario</td>
   <td>Factura</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Catálogo</td>
   <td>Grupo<br>
     Todos los objetos de aprendizaje (curso, ayuda de trabajo, programa de aprendizaje, certificación)</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Configuración</td>
   <td>Branding<br>
     Usuario</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Branding</td>
   <td>Configuración</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Factura<br>
     Interacción</td>
   <td>Usuario</td>
   <td>Leer</td>
  </tr>
 </tbody>
</table>

## Acceder a una función personalizada {#accessacustomrole}

Cuando un administrador asigna una función personalizada, recibe una notificación por correo electrónico.

Nota: Si ya ha iniciado sesión en Learning Manager con una función personalizada, deberá volver a iniciar sesión en Learning Manager para acceder a la nueva función.

Para cambiar de una función a otra, haga clic en el icono de perfil en la esquina superior derecha de Learning Manager y seleccione la función.

## Planes de aprendizaje definidos por funciones configurables {#scopeconfigure}

En versiones anteriores de Learning Manager, cualquier función personalizada con permiso para crear planes de aprendizaje podía definir el ámbito del plan de aprendizaje para todos los tipos de grupos de usuarios y objetos de aprendizaje.

La configuración del ámbito solía estar desactivada cuando se concedía acceso al plan de aprendizaje, lo que de forma predeterminada proporcionaba al usuario acceso a todos los catálogos y grupos de usuarios.

Todos los planes de aprendizaje creados por un administrador, de forma predeterminada, se aplican a todos los usuarios. A los usuarios también se les puede asignar cualquier objeto de aprendizaje. Por otro lado, los usuarios con funciones personalizadas tienen acceso a todos los ámbitos, por ejemplo, todos los catálogos, objetos de aprendizaje o grupos de usuarios. Esto significaba que los administradores no podían crear funciones personalizadas de la forma prevista que permitieran el acceso a planes de aprendizaje a usuarios con un ámbito limitado.

En esta actualización de Learning Manager, puede crear funciones personalizadas para planes de aprendizaje que permitan el ámbito de usuarios y objetos de aprendizaje. En otras palabras, los planes de aprendizaje se pueden crear con un ámbito limitado derivado del ámbito de la función de un administrador personalizado.

Ahora, un administrador puede definir o restringir el ámbito mientras otorga acceso a la administración del plan de aprendizaje.

Los administradores personalizados pueden crear planes de aprendizaje con un ámbito limitado, determinado por el ámbito de la función configurable del administrador personalizado. Solo pueden acceder a estos planes de aprendizaje los administradores personalizados con la misma función, además de los administradores regulares. Además, los administradores personalizados no pueden ver ningún otro plan de aprendizaje de la cuenta.

Los administradores personalizados existentes que tengan acceso a planes de aprendizaje siempre tendrán ámbito completo (por definición). Tendrán acceso a todos los planes de aprendizaje de la cuenta, al igual que los administradores regulares. Las nuevas funciones personalizadas creadas con ámbito completo y los nuevos administradores personalizados añadidos a dichas funciones seguirán teniendo acceso a todos los planes de aprendizaje.

Los planes de aprendizaje creados por los administradores y los administradores personalizados de ámbito completo se crearán de la forma habitual y no estarán limitados por el ámbito.

En la sección **Ámbito de los privilegios de funciones**, conceda acceso a grupos de usuarios o a catálogos para la función personalizada.

![](assets/scope-for-featureprivileges.png)

*Conceder acceso a grupos de usuarios o a catálogos para la función personalizada*

Asigne un usuario a la función personalizada.

![](assets/assign-users-to-customrole.png)

*Asignar un usuario a una función personalizada*

El usuario ahora inicia sesión en Learning Manager como administrador personalizado y añade un plan de aprendizaje.

Cuando se añade un nuevo alumno, el administrador personalizado puede seleccionar un curso de formación únicamente en los catálogos del ámbito de la función configurable.

Este plan de aprendizaje ahora se aplica al alumno solo si el usuario también se añade al grupo dentro del grupo de usuarios del ámbito del plan de aprendizaje. Todos los demás alumnos quedan exentos de este plan de aprendizaje.

## Se añade el alumno al grupo. {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

El administrador personalizado puede seleccionar cualquier grupo de usuarios que tenga usuarios dentro del grupo de usuarios del ámbito de la función.

Cuando se añade un usuario al grupo especificado, solo se asignará el objeto de aprendizaje a los usuarios que ya formen parte del grupo de usuarios del ámbito del plan de aprendizaje y que se hayan añadido al grupo de usuarios especificado.

## Cambio de ámbito {#changeinscope}

Cuando el administrador cambia el ámbito de la función personalizada, el cambio también se aplica en cascada al administrador personalizado. Cuando el administrador personalizado elige un plan de aprendizaje que ya tenía el ámbito de una función personalizada anterior, se muestra un mensaje como el siguiente:

![](assets/change-scope.png)

*Mensaje tras los cambios de ámbito*

El administrador personalizado ahora debe actualizar o actualizar el ámbito anterior al nuevo ámbito.

Clic **[!UICONTROL Actualizar ámbito]** actualiza el ámbito. Se muestra un mensaje de advertencia.

![](assets/refresh-scope-message.png)

*Mensaje de advertencia después de actualizar un ámbito*

Clic **[!UICONTROL Sí]** actualiza el ámbito.

## Agregar informe de interacción a una función personalizada {#gamification-custom}

Un administrador puede activar los informes de interacción para un usuario personalizado.

1. En la **[!UICONTROL Funciones personalizadas]** , escriba el nombre de la función personalizada.
1. En la **[!UICONTROL Privilegios de funciones: funciones principales]** , habilite la opción **[!UICONTROL Control total]** para la categoría **[!UICONTROL Informes]**.

1. En la sección **[!UICONTROL Usuarios]**, seleccione el usuario al que se asignará la función personalizada recién creada.
1. Haga clic en **[!UICONTROL Guardar]**.

Cuando un usuario inicia sesión como administrador personalizado y hace clic en **[!UICONTROL Informes]** en el panel izquierdo, aparecen las transcripciones, como se muestra a continuación:

![](assets/download-gamificationtranscripts.png)

*Descargar las transcripciones de interacciones*

Haga clic en **[!UICONTROL Transcripciones de interacciones]**, elija un usuario y genere el informe.

Si un administrador cambia los puntos de nivel, los informes muestran niveles según los puntos actuales.

El restablecimiento de la interacción no restablece la fecha de nivel alcanzado.

## Preguntas más frecuentes {#frequentlyaskedquestions}

+++Cómo crear una función personalizada

Una función personalizada es como un subconjunto de una función de autor o administrador. Permitir uno o varios privilegios, definir el ámbito y asignar la función a un usuario.

Haga clic en **[!UICONTROL Usuarios]** > **[!UICONTROL Funciones personalizadas]**. En la página Funciones personalizadas, haga clic en **[!UICONTROL Crear función]**. Introduzca el nombre de la función personalizada y defina sus privilegios. Para obtener más información, consulte [Crear una función personalizada](custom-role.md#create-role).
+++
