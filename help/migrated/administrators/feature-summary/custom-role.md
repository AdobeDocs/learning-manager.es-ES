---
jcr-language: en_us
title: Funciones personalizadas
description: La función Rutas de aprendizaje le ayuda a definir funciones personalizadas y a asignar responsabilidades específicas a un conjunto de usuarios. Esta función le permite asignar responsabilidades fuera del ámbito de la función existente de la persona.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '5437'
ht-degree: 25%

---

# Funciones personalizadas

Esta función le ayuda a definir funciones personalizadas y a asignar responsabilidades específicas a un conjunto de usuarios. Esta función le permite asignar responsabilidades fuera del ámbito de la función existente de la persona.

Adobe Learning Manager permite a los administradores completos delegar responsabilidades de administración de funciones personalizadas en administradores personalizados de confianza, incluida la creación, edición y asignación de funciones personalizadas, sin otorgarles credenciales de administrador completas. Esta capacidad permite a los administradores personalizados administrar otras funciones sin sobrecargar a los administradores con tareas. Esto se controla mediante el nivel de permisos **Avanzado** en la sección **Usuarios** de una definición de función personalizada. Consulte [Qué desbloquea el permiso de usuario avanzado](#advanced-user) para obtener más información.

Las organizaciones utilizan esta capacidad para delegar la administración de funciones rutinarias a los administradores personalizados designados. Por ejemplo, para permitir que un equipo dedicado cree y asigne funciones de editor o autor de forma continua, o para permitir que un equipo de operaciones limpie las cuentas de los usuarios que han abandonado la organización. Esto evita la necesidad de dar a esos equipos acceso completo de administrador, lo que conlleva privilegios más amplios de los que requieren sus responsabilidades.

Puede crear una función personalizada para proporcionar capacidades de autoría limitadas a un catálogo en particular. También puede crear una función destinada a gestionar informes. Dichas funciones después pueden asignarse a las personas que, se supone, asumirán estas responsabilidades.

>[!NOTE]
>
>La adición de una nueva función personalizada no afectará a los grupos de usuarios personalizados existentes ni a ningún grupo basado en funciones, como Todos los administradores, Todos los autores, etc.

El administrador puede crear funciones de administrador y autor personalizadas con permisos personalizados para cada función. A continuación se muestra una descripción general de los permisos asociados a cada función:

**Permisos de función de autor personalizados**

Los autores personalizados pueden realizar las siguientes tareas:

* Accede a la biblioteca de contenido para añadir, editar o eliminar contenido principal.
* Crear, editar y eliminar:
  * Cursos
  * Ayudas de trabajo
  * Certificaciones
  * Rutas de aprendizaje
  * Planes de aprendizaje

Los administradores y autores, incluidos los administradores personalizados y los autores personalizados, podrán compartir objetos de aprendizaje (LO) en catálogos compartidos externamente. Los administradores y los autores deben poder buscar catálogos compartidos externamente al crear objetos de aprendizaje (LO).

**Permisos de funciones de administrador personalizadas**

La función de administrador personalizada replica un conjunto de responsabilidades de administración, incluido el acceso a los privilegios de nivel de cuenta. A los administradores personalizados se les conceden permisos para administrar las funciones clave relacionadas con las actividades de aprendizaje, como:

* Planes de aprendizaje
* Catálogos
* Informes
* Etiquetas

Además, los administradores personalizados pueden:

* Administrar cursos y ayudas de trabajo, incluida la inscripción y eliminación de usuarios.
* Cree, edite y elimine certificaciones, rutas de aprendizaje y planes de aprendizaje.
* Accede a las funciones de informes e inscripción para todos los objetos de aprendizaje (LO).

Ahora los administradores pueden ver los permisos creados mediante CSV en Adobe Learning Manager. La opción filtrar por filtra las funciones personalizadas por administrador creadas y las importadas mediante CSV. Después de seleccionar una función personalizada, puede ver sus permisos.

![](assets/filter.png)
_Filtrar funciones personalizadas_

## Crear una función personalizada {#create-role}

1. Inicie sesión como administrador. Abra **[!UICONTROL Usuarios]** > **[!UICONTROL Función personalizada]**.
2. Seleccione **[!UICONTROL Crear rol]**. Se abre la ficha **[!UICONTROL Crear función]**.

   ![](assets/create-new-role.png)

   *Crear una función personalizada*

3. Escriba el nombre en el campo **[!UICONTROL Nombre del rol]**.
4. **[!UICONTROL Privilegios de cuenta]**: Estos privilegios otorgan a los propietarios del rol acceso a aspectos específicos de la configuración del sistema y que actúan en toda la cuenta. Elija los permisos de acceso. El usuario tiene control total sobre los permisos asignados.

   Los administradores pueden conceder permisos detallados para la sección Usuario, que tiene usuarios internos/externos, grupos de usuarios y usuarios avanzados.

   >[!NOTE]
   >
   >   El ámbito no es aplicable a estos privilegios.


   ![](assets/account-privileges.png)

   *Establecer el ámbito*

5. **Privilegios de funciones - Funciones principales**: Se utiliza para conceder acceso a funciones específicas de administración de actividades de aprendizaje. Mediante esta opción se pueden otorgar permisos a las funciones siguientes.

   Los administradores pueden proporcionar permisos detallados, como permisos de solo lectura, de creación, de edición y de eliminación para los catálogos.

   * Catálogos
   * Informes
   * Etiquetas

   ![](assets/core-features.png)

   *Establecer ámbito para catálogos, informes y etiquetas*

6. **Privilegios de funciones: objetos de aprendizaje:** Utilice esta opción para proporcionar acceso a funciones relacionadas con objetos de aprendizaje. Los administradores pueden proporcionar permisos detallados para todos los objetos de aprendizaje, incluidos cursos, rutas de aprendizaje, certificaciones y ayudas de trabajo. Pueden asignar permisos a los usuarios como crear, editar, eliminar o acceso de solo lectura.

   * Certificaciones
   * Cursos
   * Ayudas de trabajo
   * Programas de aprendizaje

   También puede otorgar un control de operación específico para los objetos de aprendizaje. El permiso puede ser uno de los siguientes:

   * Solo lectura
   * Crear
   * Editar
   * Eliminar
   * Inscripción
   * Informe

   También puede otorgar control total a los objetos de aprendizaje.

   ![](assets/learningobjects.png)

   *Conceder permisos específicos*

7. **Ámbito de los privilegios de funciones:** El ámbito de los privilegios de funciones asignados a esta función se puede restringir a un grupo de usuarios específico o a uno o varios catálogos.

   Catálogos: utilice el botón de opción para proporcionar control sobre **[!UICONTROL Todos los catálogos]**; también puede utilizar la opción **[!UICONTROL Definir acceso por catálogo]** para conceder acceso a determinados catálogos. También puede seleccionar varios catálogos.

   Grupos de usuarios: proporcione acceso a **[!UICONTROL Todos los grupos de usuarios]**; también puede utilizar la opción **[!UICONTROL Definir acceso por grupo de usuarios]** a fin de otorgar acceso a determinados grupos de usuarios. Únicamente puede especificarse un grupo de usuarios.

   >[!NOTE]
   >
   >Si ha seleccionado Anuncio, Interacción, Plantillas de correo electrónico, Aptitudes y Usuarios en Privilegios de cuenta, el acceso a los grupos de usuarios se proporciona a todos los grupos de usuarios de forma predeterminada, y esta opción está desactivada.

   Si ya ha seleccionado Planes de aprendizaje en Privilegios de cuenta, el acceso a todos los catálogos y grupos de usuarios se proporciona de forma predeterminada y estas opciones de Ámbito están deshabilitadas.

   ![](assets/define-scope-of-privileges.png)

   *Definir ámbito de privilegios*

>[!NOTE]
>
>   En Learning Manager 27.6, es posible crear una función personalizada con un ámbito que abarque varios catálogos, y que cada catálogo tenga asignado su propio conjunto de permisos.


Para conceder varios permisos a los catálogos, siga los pasos que se indican a continuación:

1. Haga clic en la opción **[!UICONTROL Definir acceso por catálogo]**.
1. Seleccione los catálogos y podrá ver el nivel de permiso de cada catálogo. Estos son los permisos:

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
          <p>Concede el control total de todos los objetos de aprendizaje. Los permisos son para añadir, editar, eliminar, leer, inscribir e informes.<br></p></td>
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
          <p>Otorga permiso solo para inscribir para el objeto de aprendizaje.</p></td>
        </tr>
        <tr>
          <td>
          <p>Solo lectura</p></td>
          <td>
          <p>Otorga permiso solo para ver los objetos de aprendizaje del catálogo.</p></td>
        </tr>
        </tbody>
      </table>

1. Active o desactive los permisos según necesite.
1. Para guardar los cambios, haga clic en **[!UICONTROL Aceptar]**. A continuación, para guardar los cambios de la función personalizada, haga clic en **[!UICONTROL Guardar]**.

Por ejemplo, podría darse el caso siguiente:

El permiso resultante que un usuario personalizado tiene sobre un objeto de aprendizaje es una combinación del permiso del objeto de aprendizaje y el permiso del catálogo.

Un usuario personalizado tiene permiso completo para cursos y de acceso de solo lectura para Catálogo A, y tiene permiso completo para Catálogo B. El resultado es el acceso de solo lectura en los cursos de Catálogo A y el control total en los cursos de Catálogo B.

Un usuario con una función personalizada puede:

* Ver contenido solo de los catálogos a los que tiene acceso.
* Tener acceso a cualquier objeto de aprendizaje conforme a los permisos del catálogo del que forma parte el objeto de aprendizaje.

  Como administrador, puede:

* Seleccionar más de un catálogo para una función personalizada.
* Modificar los permisos de un catálogo en cualquier momento.
* Eliminar los catálogos de un ámbito para el que ya no desea conceder permisos.
* Otorgar implícitamente el permiso de solo lectura para un catálogo al otorgar permisos al catálogo.

  En la tabla siguiente, se muestra cómo se otorgan permisos.

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

1. **Usuarios:** utilice esta opción para determinar los usuarios a los que se asigna esta función. Puede elegir uno o más usuarios con el cuadro de búsqueda.

   **Agregar usuarios a la carga de CSV de funciones personalizadas:** Para agregar usuarios mediante la carga de CSV, agregue una columna CustomRole al archivo .csv que el administrador usó para importar usuarios. Introduzca la función del usuario en la columna Función personalizada para los usuarios a los que desea asignar una función personalizada. Para cargar el archivo CSV, haga clic en **[!UICONTROL Agregar > Cargar un CSV]**.

   * No puede buscar grupos de usuarios
   * No puede buscar usuarios que ya tengan asignada la función de administrador.
   * La asignación de una nueva función personalizada a un usuario anula la función personalizada anterior del usuario.

   <!--![](assets/users.png)-->

   * Un administrador personalizado con permiso en Configuración podrá configurar la programación para sincronizar o sincronizar usuarios desde la fuente de datos aunque no tenga permiso para la entidad Usuarios.
   * Si un administrador personalizado tiene permiso en la entidad Usuarios, los usuarios se pueden asignar a sí mismos la función de administrador y convertirse en administradores estándar.

## <a id="advanced-user"></a>Qué desbloquea el permiso de usuario avanzado {#whatadvanceduserpermissionunlocks}

Cuando un administrador completo habilita el acceso **Avanzado** en **Usuarios** en una función personalizada, el administrador personalizado obtiene acceso a cuatro secciones adicionales: **Funciones personalizadas**, **Registros de importación**, **Campos activos** y **Limpieza de usuarios**.

Hay dos niveles de acceso disponibles:

* **Solo lectura**: el administrador personalizado puede ver información y descargar informes, pero no puede realizar cambios.
* **Control total**: el administrador personalizado puede crear, editar y eliminar funciones personalizadas, importar usuarios y purgar usuarios eliminados.

### Herencia de permisos y ámbito

Cuando un administrador personalizado crea una nueva función personalizada o modifica una existente, los permisos y el ámbito que puede asignar se limitan a lo que ellos mismos poseen. Un administrador personalizado no puede conceder a un rol permisos que excedan los suyos propios y no puede extender el ámbito de un rol más allá de su propio ámbito asignado.

Esto significa que un administrador personalizado con acceso a un catálogo específico solo puede crear funciones con ámbito para ese catálogo o un subconjunto del mismo. Del mismo modo, solo pueden asignar los permisos que poseen personalmente a las funciones que crean.

Al asignar usuarios a una función que haya creado, puede buscar y agregar cualquier usuario de la cuenta. Los permisos relacionados con el usuario en funciones personalizadas siempre se aplican al ámbito completo del grupo de usuarios y al ámbito completo del catálogo. El ámbito de catálogo o grupo de usuarios no se aplica cuando una función personalizada incluye permisos de administración de usuarios.

Si un administrador completo reduce el ámbito o quita un permiso de la función, las funciones que haya creado anteriormente no se verán afectadas de inmediato. Esas funciones seguirán funcionando con sus permisos existentes hasta que se abra un administrador completo que las guarde individualmente.

## Otorgar permisos de usuario avanzado a una función personalizada

Los administradores completos realizan este procedimiento para habilitar la administración de usuarios ampliada para una función personalizada.

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **Usuarios** en la barra de navegación izquierda y, a continuación, seleccione **Funciones personalizadas**.
3. Seleccione **Crear función personalizada** para crear una nueva función o seleccione una función existente para editarla.
4. En **Privilegios de cuenta**, busque la sección **Usuarios**.
5. En la sección **Usuarios avanzados**, seleccione **Solo lectura** o **Control total** en función del nivel de acceso requerido.
6. Agregue usuarios a la función en la sección **Usuarios**.
7. Seleccione **Guardar**.

Los usuarios asignados ahora pueden acceder a las secciones **Funciones personalizadas**, **Campos activos**, **Registros de importación** y **Limpieza de usuario** al iniciar sesión.

## Qué pueden hacer los administradores personalizados con el acceso de solo lectura

### Importar registros

Los administradores personalizados con acceso de solo lectura pueden ver todos los registros de importación de la cuenta. El botón **Agregar** no está disponible. No se pueden iniciar nuevas importaciones.

### Limpieza de usuarios

La sección **Limpieza de usuarios** está disponible en modo de solo vista. Los administradores personalizados pueden:

* Ver la lista de usuarios eliminados
* Buscar usuarios específicos
* Filtrar usuarios eliminados por mes de eliminación
* Ver otros usuarios de la cuenta

No hay acciones, como purgar, disponibles en **acceso de solo lectura**.

### Funciones personalizadas

Los administradores personalizados pueden ver todas las definiciones de funciones personalizadas de la cuenta, incluidos sus permisos asignados y las listas de usuarios. Pueden descargar el informe de funciones personalizadas. No pueden editar, crear ni eliminar ningún rol.

## Qué pueden hacer los administradores personalizados con el acceso de Control total

**Importar registros**

Los administradores personalizados con Control total pueden ver todos los registros y agregar o importar nuevos usuarios a través de CSV.

**Limpieza de usuarios**

Control total proporciona acceso a todas las acciones de limpieza del usuario:

* Ver, buscar y filtrar usuarios eliminados por mes de eliminación
* Seleccionar usuarios individuales o seleccionar todos
* Purgar usuarios eliminados del sistema
* Buscar y purgar otros usuarios

**Funciones personalizadas**

Los administradores personalizados con Control total pueden:

* Crear nuevas funciones personalizadas, con permisos iguales o inferiores a los suyos propios
* Editar funciones personalizadas existentes
* Eliminar funciones personalizadas
* Asignar usuarios a funciones personalizadas
* Quitar usuarios de funciones personalizadas
* Descargar el informe de funciones personalizadas
* Filtrar la lista de funciones por **Todas**, **Creadas a partir de la interfaz de usuario** o **Creadas a partir del archivo CSV**

>[!NOTE]
>
>Los administradores personalizados no pueden agregarse a otra función y tampoco pueden editar su propia función con permisos más altos.

>[!IMPORTANT]
>
>Las funciones creadas por un administrador personalizado pueden incluir acceso a funciones personalizadas, incluido el permiso de usuario avanzado que habilita la administración de funciones personalizadas. Esto significa que un administrador personalizado con Control total puede crear funciones que otorguen a otros usuarios las mismas funciones de funciones personalizadas que tienen. Los permisos disponibles durante la creación de la función siguen sujetos al modelo de delegación estándar. El administrador personalizado solo puede asignar los permisos que posean personalmente, a menos que la cuenta tenga habilitada la administración de funciones ampliada.

### Ejemplo: creación de funciones con ámbito como administrador personalizado

Un administrador completo concede a un administrador personalizado Control total con acceso a dos catálogos de productos. A continuación, el administrador personalizado:

1. Crea una función de editor con ámbito en el primer catálogo y le asigna autores
1. Crea una segunda función de editor con ámbito en el segundo catálogo y asigna un conjunto diferente de autores
1. Asigna a los nuevos autores, que se unen al equipo, la función adecuada sin involucrar al administrador completo

Cada función que crea el administrador personalizado hereda un subconjunto de los permisos del administrador personalizado. Los autores asignados a estas funciones pueden acceder al contenido de sus respectivos catálogos y publicarlo. No pueden administrar funciones personalizadas por sí mismos, porque la sección Funciones personalizadas no está disponible en las funciones creadas por los administradores personalizados.

## Comparación de capacidades

| Sección | Solo lectura | Control total |
|---|---|---|
| Registros de importación: ver registros | ✓ | ✓ |
| Registros de importación: añadir o importar usuarios mediante CSV | — | ✓ |
| Limpieza de usuarios: ver usuarios eliminados, buscar, filtrar | ✓ | ✓ |
| Limpieza de usuarios: purgar usuarios eliminados | — | ✓ |
| Funciones personalizadas: ver todas las funciones y definiciones | ✓ | ✓ |
| Funciones personalizadas: descargar informe de funciones personalizadas | ✓ | ✓ |
| Funciones personalizadas: crear, editar y eliminar roles | — | ✓ |
| Funciones personalizadas: asignar y quitar usuarios | — | ✓ |

## Retrocompatibilidad

Si una cuenta tiene funciones personalizadas existentes con acceso **avanzado** habilitado, dichas funciones incluyen automáticamente acceso a los registros de importación cuando se actualiza la cuenta. Si el acceso avanzado está deshabilitado actualmente en una función, no hay ningún cambio. El papel sigue comportándose como antes.

>[!NOTE]
>
>Si las opciones de acceso avanzado están habilitadas para los usuarios, revise qué funciones tienen este privilegio y confirme que dichas funciones están pensadas para conservarlo.

## Seguimiento de auditoría de cambios de funciones personalizadas

Todos los cambios en las funciones personalizadas, incluidas la creación, la edición, la eliminación y la asignación de usuarios, se registran en el informe de auditoría de funciones personalizadas. El informe de auditoría ahora muestra el nombre de la función personalizada responsable de cada cambio, en lugar de una etiqueta de administrador genérico. No se requiere ninguna configuración para habilitar este comportamiento.

Los administradores completos pueden acceder al informe de auditoría desde la sección **Informes**.

## Casos prácticos del mundo real

### Equipo de administración de roles

Una gran organización tiene un equipo dedicado que se encarga de crear y asignar funciones de autor de contenido en docenas de catálogos de productos. Anteriormente, cada nueva función requería un administrador completo para crearla. Con el acceso de Control total, el equipo de administración de funciones puede crear funciones de editor y autor con ámbito en catálogos específicos, asignar nuevos autores y administrar dichas funciones de forma independiente, sin que intervenga ningún administrador completo en las operaciones rutinarias.

### Operaciones de RR. HH. y gestión del ciclo de vida del usuario

Un equipo de operaciones de RR. HH. se encarga de limpiar las cuentas cuando los empleados abandonan la organización. Deben purgar usuarios eliminados con regularidad, pero no deben tener acceso al contenido del curso, los datos del alumno ni la configuración del sistema. La concesión del acceso de Control total avanzado, cuyo ámbito se limita únicamente a la administración de usuarios, proporciona al equipo de HR el acceso específico que necesita para la limpieza e importación de usuarios sin exponer ninguna otra función administrativa.

### Equipo de cumplimiento y auditoría

Un equipo de auditoría interna debe revisar periódicamente qué funciones personalizadas existen, qué permisos incluyen y quién desempeña cada función. Con el acceso de solo lectura, el equipo de auditoría puede ver todas las definiciones de función y descargar el informe de funciones personalizadas para su revisión, pero no puede modificar nada.

## Qué pueden hacer los administradores personalizados

Los siguientes procedimientos se aplican a los administradores personalizados con acceso de **Control total**. Inicie sesión como administrador personalizado y vaya a **Usuarios** > **Funciones personalizadas** para empezar.

### Revisar las funciones personalizadas existentes

1. Seleccione **Usuarios** > **Funciones personalizadas**.
1. Utilice el menú desplegable de filtros para reducir la lista:

   * **Todos**: cada función de la cuenta
   * **Creado desde la interfaz de usuario**: funciones creadas manualmente
   * **Creado desde CSV**: funciones importadas mediante CSV

1. Seleccione un nombre de función para abrir su definición completa, incluidos los permisos, el ámbito y los usuarios asignados.

### Crear una nueva función personalizada

1. Seleccione **Usuarios** > **Funciones personalizadas** y, a continuación, seleccione **Crear función**.
1. Introduzca un nombre para el rol.
1. En **Privilegios de cuenta**, configure los permisos. Sólo los permisos dentro de su propio ámbito están disponibles para su selección. Los permisos fuera de su ámbito aparecen deshabilitados.
1. Establezca el ámbito de catálogo y de grupo de usuarios para la función.
1. En la sección **Usuarios**, busque y agregue los usuarios que desempeñarán esta función.
1. Seleccione **Guardar**.

>[!NOTE]
>
>No puede agregarse a un rol que cree y no puede crear un rol con permisos que excedan los suyos propios. Si un permiso está deshabilitado durante la creación de la función, queda fuera del ámbito actual.

### Editar una función personalizada

1. Seleccione **Usuarios** > **Funciones personalizadas** y abra la función que desea actualizar.
1. Seleccione **Editar**.
1. Actualice el nombre, los permisos, el ámbito o las asignaciones de usuario según sea necesario.
1. Seleccione **Guardar**.

>[!NOTE]
>
>No puede editar los permisos de su propia función personalizada. Póngase en contacto con un administrador completo si necesita realizar cambios en su propia función.

### Asignar usuarios a una función personalizada

1. Abra la función personalizada de **Usuarios** > **Funciones personalizadas**.
1. En la sección **Usuarios**, busque el usuario que desea agregar.
1. Seleccione el usuario para agregarlo a la función.
1. Seleccione **Guardar**.

### Quitar usuarios de una función personalizada

1. Abra la función personalizada de **Usuarios** > **Funciones personalizadas**.
1. En la sección **Usuarios**, busque el usuario que desea quitar.
1. Seleccione la acción de eliminación junto a su nombre.
1. Seleccione **Guardar**.

### Purgar usuarios eliminados

1. Seleccione **Usuarios** en la barra de navegación izquierda.
1. Seleccione **Limpieza de usuarios**.
1. Utilice el campo de búsqueda o el filtro de mes de eliminación para localizar a los usuarios que desea eliminar.
1. Marque la casilla de verificación junto a los usuarios individuales o seleccione **Seleccionar todo** para seleccionar todos los resultados.
1. Seleccione **Acciones** > **Purgar usuario**.

## Asignar varias funciones personalizadas a un usuario

Puede asignar varias funciones personalizadas a los usuarios de las siguientes maneras:

* Uso de la IU: Puede asignar más de una función personalizada a un usuario directamente desde la interfaz de Adobe Learning Manager.
* Uso de la carga de CSV: Puede cargar un archivo CSV para asignar varias funciones personalizadas a varios usuarios a la vez.

Esto facilita la administración del acceso de los usuarios y los permisos de control en todo el sistema.

### Asignar varias funciones personalizadas mediante la interfaz de usuario

La asignación de varias funciones personalizadas a través del Admin Console en Adobe Learning Manager es una opción rápida e intuitiva, ideal para la incorporación, los ajustes de permisos o las actualizaciones más pequeñas. Las funciones se pueden asignar visualmente, sin necesidad de cargar archivos CSV, lo que reduce el riesgo de errores y proporciona visibilidad en tiempo real. Este método admite actualizaciones rápidas a medida que cambian las responsabilidades y permite el cambio de funciones y la delegación según sea necesario.

Para asignar varias funciones personalizadas a un usuario, siga estos pasos:

1. Inicie sesión como administrador y seleccione **[!UICONTROL Usuarios]**.
2. Seleccione **[!UICONTROL Funciones personalizadas]** en el panel izquierdo.
3. Cree una nueva función personalizada y agregue privilegios de cuenta, catálogos, objetos de aprendizaje o ámbitos. Consulte los [pasos mencionados aquí](#create-a-custom-role).
4. Agregar usuarios a la función personalizada.

   ![](assets/add-users-in-custom-roles.png)
   _Asignar usuarios a una función personalizada_

5. Seleccione **[!UICONTROL Guardar]**.

Seleccione varias funciones personalizadas para un usuario según sea necesario. Cada usuario puede tener hasta 50 asignaciones de funciones personalizadas. El número de funciones disponibles disminuye con cada asignación.

Después de asignar usuarios a una función personalizada adicional, puede ver cuántas asignaciones de funciones quedan disponibles para cada usuario.

>[!NOTE]
>
>Puede asignar hasta 50 funciones a cada usuario y añadir hasta 500 usuarios a cada función.

### Asignar varias funciones personalizadas mediante CSV

La carga de un archivo CSV en Adobe Learning Manager permite la asignación eficiente de funciones personalizadas en bloque. Este proceso resulta especialmente beneficioso para incorporar a un gran número de empleados, reorganizar los equipos o actualizar el acceso a la nueva formación. Las importaciones de CSV ahorran esfuerzo manual, garantizan asignaciones uniformes y reducen errores. Este método resulta especialmente útil durante fusiones, actualizaciones de todo el departamento o despliegues globales de formación. Este método ayuda a los administradores a ahorrar tiempo, estandarizar funciones y mantener la gobernanza.

Ahora puede asignar varias funciones a un usuario mediante la importación de CSV cargando dos archivos en Box:

* [role.csv](assets/role.csv)
* [user_role.csv](assets/user_role.csv)

El archivo user_role.csv incluye los campos Función personalizada e ID de usuario.

El archivo role.csv incluye los campos, Función personalizada, Origen de la creación e información detallada para catálogos, usuarios, cursos, rutas de aprendizaje, etc.

Si el archivo CSV tiene datos incorrectos o supera los límites (50 funciones por usuario y 500 usuarios por función), aparecerá un mensaje que muestra los errores.

![](assets/error-custom-role.png)
_Notificación de error para funciones personalizadas_
Los usuarios reciben notificaciones por correo electrónico cuando se asignan funciones, incluido el nombre de la función.

### Administrar funciones personalizadas

Los administradores pueden actualizar, añadir o eliminar funciones personalizadas para los usuarios de Adobe Learning Manager a medida que cambian las responsabilidades. Esto garantiza que el acceso se alinea con las funciones actuales sin que esto afecte al historial de aprendizaje o los datos de inscripción. Desde la página **[!UICONTROL Usuarios]**, el administrador puede buscar usuarios, ver sus funciones y ajustarlos mediante la opción Administrar funciones personalizadas. Esta interfaz guiada permite añadir o quitar funciones fácilmente, al tiempo que mantiene la gobernanza y la seguridad.

>[!NOTE]
>
>Los administradores personalizados no pueden administrar funciones personalizadas (agregar o quitar funciones personalizadas) ni ascender a la función de administrador.

Después de asignar funciones personalizadas a los usuarios, puede agregar o quitar funciones personalizadas de la página **[!UICONTROL Usuarios]**.

1. Busque un usuario en la página **[!UICONTROL Usuarios]**.

   ![](assets/search-user-role.png)
   _Buscar un usuario en la página Usuarios_

2. Seleccione la flecha desplegable al final de la fila donde se muestra el nombre de usuario y, a continuación, seleccione **[!UICONTROL Administrar funciones personalizadas]**.

   ![](assets/select-manage-custom-roles.png)
   _Seleccione Administrar funciones personalizadas en la página de usuario_

3. Aparece un cuadro de diálogo que muestra la lista de funciones personalizadas asignadas al usuario. Seleccione **[!UICONTROL Agregar o quitar roles]** para agregar o quitar roles personalizados asignados al usuario.

   ![](assets/add-remove-roles.png)
   _Seleccione Agregar o quitar funciones en el aviso Administrar funciones personalizadas_

4. Busque otras funciones personalizadas que se vayan a asignar al usuario. Después de buscar una, seleccione la función personalizada.

   ![](assets/add-new-custom-role.png)
   _Seleccionar la función personalizada_

5. Seleccione **[!UICONTROL Guardar]**. Aparece un cuadro de diálogo de confirmación para el cambio en la función personalizada. Seleccione **[!UICONTROL Sí]**.

   ![](assets/confirmation-prompt.png)
   _Seleccione Sí en el mensaje de confirmación_

Se asigna una tercera función personalizada al usuario.

Para eliminar las funciones personalizadas, siga estos pasos:

1. Busque un usuario en la página **[!UICONTROL Usuarios]**.
2. Seleccione el menú desplegable cerca del usuario y seleccione **[!UICONTROL Administrar funciones personalizadas]**.
3. Seleccione **[!UICONTROL Agregar o quitar roles]** para agregar o quitar roles personalizados.
4. Seleccione el **[!UICONTROL icono de eliminación]** para eliminar la función personalizada.

   ![](assets/remove-custom-roles.png)
   _Quitar funciones personalizadas_

### Cambiar funciones personalizadas

Para ver y seleccionar cualquier función personalizada que tenga asignada, use la opción **[!UICONTROL Cambiar función personalizada]**.

![](assets/switch-roles.png)
_Seleccionar funciones personalizadas_

Los usuarios reciben notificaciones por correo electrónico cuando se les asignan las funciones personalizadas. Los correos electrónicos ahora incluyen nombres de funciones para una mayor claridad.

## Descargar el informe de funciones personalizadas

Los administradores pueden descargar un informe CSV que enumere todas las funciones personalizadas y sus permisos asociados. El informe indica si cada función se ha creado manualmente o mediante carga de CSV y proporciona un resumen del acceso y los privilegios asignados a cada función.

Para descargar el informe, siga estos pasos:

1. Inicie sesión como **[!UICONTROL administrador]**.
2. Seleccione **[!UICONTROL Usuarios]** > **[!UICONTROL Funciones personalizadas]**.
3. Seleccione la opción **[!UICONTROL Descargar]** para descargar el informe CSV.

![](assets/download-report.png)
_Descargar informe de funciones personalizadas_

El informe tiene dos archivos CSV: role.csv y user_role.csv. El archivo role.csv incluye:

* Función personalizada
* ID de usuario
* Fuente de creación.

El archivo user_role.csv incluye los campos Función personalizada, Origen de la creación e información detallada para catálogos, usuarios, cursos, rutas de aprendizaje, etc.

## Seguimiento de auditoría para funciones personalizadas

Los administradores pueden descargar el informe de auditoría de funciones personalizadas para realizar un seguimiento de todos los cambios realizados en las funciones personalizadas, incluida la creación, modificación y eliminación de funciones personalizadas y su acceso a funciones asociado.

Consulte este artículo [Seguimiento de auditoría de funciones personalizadas](/help/migrated/administrators/feature-summary/reports.md#audit-trail-for-custom-roles) para obtener más información.

## Restringir el acceso a las carpetas a los autores personalizados {#folder-custom-author}

Learning Manager ya admite la posibilidad de conceder acceso a la biblioteca de contenido mediante funciones personalizadas. Todos los autores personalizados que ya tengan acceso a la biblioteca de contenido seguirán teniendo acceso a todos los archivos de contenido incluso después de configurar las carpetas de contenido. Esto es para mantener el comportamiento heredado. No es necesario que los administradores realicen cambios si desean continuar con el comportamiento actual.

En el caso de que deseen restringir el acceso a estos autores personalizados, los administradores deben editar la función personalizada existente y configurarla proporcionando acceso solo a carpetas de contenido específicas.

![](assets/folder-access-forcustomauthors.png)

*Restringir el acceso a las carpetas a los autores personalizados*

Al crear un autor personalizado, ahora puede asignarle carpetas de contenido. Elija la opción **Carpetas seleccionadas**.

Después de hacer clic en la opción, se abre un nuevo cuadro de diálogo en el que puede asignar las carpetas al autor personalizado.

![](assets/choose-folder.png)

*Seleccionar las carpetas del autor personalizado*

Elija las carpetas y haga clic en **[!UICONTROL Aceptar]**.

## Tablero de resumen de aprendizaje para administrador personalizado {#custom-admin-dashboard}

Los administradores personalizados pueden ver la misma vista que un administrador. Es posible que un administrador personalizado vea datos fuera de su ámbito. Esto solo es aplicable si el administrador personalizado tiene un ámbito completo. Para conceder el ámbito completo, al crear un administrador personalizado, habilite la opción **[!UICONTROL Control total]** en el informe de resumen de cuenta.

![](assets/create-custom-role.png)

*Crear una función personalizada*

Por lo tanto, se seleccionarán las opciones **[!UICONTROL Todos los catálogos]** y **[!UICONTROL Todos los grupos de usuarios]** y se desactivará el resto.

![](assets/scope-of-featureprivileges.png)

*Definir ámbito de privilegios*

## Permisos implícitos {#implicitpermissions}

Cuando se asigna a un usuario una función con una entidad determinada, puede haber casos en los que deba acceder también a otras entidades con el fin de realizar tareas en la entidad para la que tiene permiso. Por ejemplo, si se concede acceso a Crear en una entidad de curso a un usuario, necesita acceder a las entidades Aptitud y Etiqueta para poder asociarlas con el curso que se crea. Esta tabla proporciona información sobre estos permisos implícitos.

<table>
 <tbody>
  <tr>
   <th>Tipo de acceso</th>
   <th>Permiso de entidad otorgado por el administrador</th>
   <th>Permiso implícito de entidad</th>
   <th>Acceso implícito</th>
  </tr>
  <tr>
   <td>Gestionar</td>
   <td>Usuario</td>
   <td>Grupo</td>
   <td>CRUD</td>
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
   <td>Widget<br>
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
   <td>Marca</td>
   <td>Escribir</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Usuario</td>
   <td>Facturación</td>
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
   <td>Marca<br>
     Usuario</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Marca</td>
   <td>Configuración</td>
   <td>Leer</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Facturación<br>
     Interacción</td>
   <td>Usuario</td>
   <td>Leer</td>
  </tr>
 </tbody>
</table>

## Acceder a una función personalizada {#accessacustomrole}

Cuando un administrador asigna una función personalizada, se recibe una notificación por correo electrónico.

Nota: Si ya ha iniciado sesión en Learning Manager con una función personalizada, deberá volver a iniciar sesión en Learning Manager para acceder a la función nueva.

Para alternar entre funciones, haga clic en el icono de su perfil en la esquina superior derecha de Learning Manager; a continuación, seleccione la función.

## Planes de aprendizaje definidos por funciones configurables {#scopeconfigure}

En versiones anteriores de Learning Manager, cualquier función personalizada con permiso para crear planes de objetos de aprendizaje podía definir el ámbito del plan de aprendizaje para todos los tipos de grupos de usuarios y objetos de aprendizaje

La opción del ámbito solía estar desactivada cuando se concedía acceso al plan de aprendizaje, lo que de forma predeterminada proporcionaba al usuario acceso a todos los catálogos y grupos de usuarios.

Todos los planes de aprendizaje creados por un administrador se aplican de forma predeterminada a todos los usuarios. También se puede asignar cualquier objeto de aprendizaje a los usuarios. Por otro lado, los usuarios con funciones personalizadas tienen acceso a todos los ámbitos, por ejemplo todos los catálogos, objetos de aprendizaje o grupos de usuarios. Esto significaba que los administradores no podían crear funciones personalizadas de la forma prevista que permitieran el acceso a planes de aprendizaje a usuarios con un ámbito limitado.

En esta actualización de Learning Manager, puede crear funciones personalizadas para planes de aprendizaje que permiten definir el ámbito de usuarios y objetos de aprendizaje. En otras palabras, los Planes de aprendizaje se pueden crear con un ámbito limitado que se deriva del ámbito de la función de un administrador personalizado.

Ahora, un administrador puede definir o restringir el ámbito mientras otorga acceso a la administración del plan de aprendizaje.

Los administradores personalizados pueden crear planes de aprendizaje con un ámbito limitado, determinado por el ámbito de la función configurable del administrador personalizado. Solo pueden acceder a estos planes de aprendizaje los administradores personalizados con la misma función, además de los administradores regulares. Además, los administradores personalizados no pueden ver ningún otro plan de aprendizaje en la cuenta.

Los administradores personalizados existentes que tengan acceso a planes de aprendizaje siempre tendrán ámbito completo (por definición). Tendrán acceso a todos los planes de aprendizaje de la cuenta, al igual que un administrador normal. Las nuevas funciones personalizadas creadas con ámbito completo y los nuevos administradores personalizados añadidos a dichas funciones seguirán teniendo acceso a todos los planes de aprendizaje.

Los planes de aprendizaje creados por el administrador y los administradores personalizados de ámbito completo se crearán de la forma habitual y no estarán limitados por el ámbito.

En la sección **Ámbito de los privilegios de funciones**, conceda acceso a grupos de usuarios y a catálogo para la función personalizada.

![](assets/scope-for-featureprivileges.png)

*Conceder acceso a grupos de usuarios o a catálogos para la función personalizada*

Asigne un usuario a la función personalizada.

![](assets/assign-users-to-customrole.png)

*Asignar un usuario a una función personalizada*

El usuario ahora inicia sesión en Learning Manager como administrador personalizado y añade un plan de aprendizaje.

Cuando se añade un nuevo alumno, el administrador personalizado puede seleccionar un curso de formación únicamente en los catálogos del ámbito de la función configurable.

Este plan de aprendizaje ahora se aplica al alumno solo si el usuario también se añade al grupo dentro del grupo de usuarios del ámbito del plan de aprendizaje. Todos los demás alumnos quedan exentos de este plan de aprendizaje.

## Se añade el alumno al grupo {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

El administrador personalizado puede seleccionar cualquier grupo de usuarios que tenga usuarios dentro del grupo de usuarios del ámbito de la función.

Cuando un usuario se añade a un determinado grupo, solo los usuarios que ya forman parte del grupo de usuarios del ámbito del plan de aprendizaje y que se añadieron al grupo de usuarios especificado se asignarán al objeto de aprendizaje.

## Cambio de ámbito {#changeinscope}

Cuando el administrador cambia el ámbito de la función personalizada, el cambio también se aplica en cascada al administrador personalizado. Cuando el administrador personalizado elige un plan de aprendizaje que ya tenía el ámbito de una función personalizada anterior, se muestra un mensaje como el siguiente:

![](assets/change-scope.png)

*Mensaje después de que cambie el ámbito*

El administrador personalizado ahora debe actualizar o actualizar el ámbito anterior al nuevo ámbito.

Si se hace clic en **[!UICONTROL Actualizar ámbito]**, el ámbito se actualiza. Se muestra un mensaje de advertencia.

![](assets/refresh-scope-message.png)

*Mensaje de advertencia después de actualizar un ámbito*

Si se hace clic en **[!UICONTROL Sí]**, el ámbito se actualiza.

## Añadir informe de interacción a una función personalizada {#gamification-custom}

Un administrador puede activar los informes de interacción para un usuario personalizado.

1. En la página **[!UICONTROL Funciones personalizadas]**, escriba el nombre de la función personalizada.
1. En los **[!UICONTROL Privilegios de funciones: Sección Características principales]**, habilite la opción **[!UICONTROL Control total]** para la categoría **[!UICONTROL Informes]**.

1. En la sección **[!UICONTROL Usuarios]**, seleccione el usuario al que se asignará la función personalizada que se acaba de crear.
1. Haga clic en **[!UICONTROL Guardar]**.

Cuando un usuario inicia sesión como administrador personalizado y hace clic en **[!UICONTROL Informes]** en el panel izquierdo, aparecen las transcripciones, como se muestra a continuación:

![](assets/download-gamificationtranscripts.png)

*Descargar las transcripciones de interacciones*

Haga clic en **[!UICONTROL Transcripciones de interacciones]**, elija un usuario y genere el informe.

Si un administrador cambia los puntos de nivel, los informes muestran niveles de acuerdo con los puntos actuales.

El restablecimiento de la interacción no restablece la fecha de nivel alcanzado.

## Preguntas frecuentes

**¿Qué sucede si un administrador completo quita un permiso de mi función personalizada?**

Su función conserva sus permisos existentes hasta la próxima vez que se abra un administrador completo y guarde su definición de función. El cambio no surte efecto inmediatamente. Sus permisos actuales seguirán en vigor hasta que se modifique y guarde explícitamente su función.

**¿Puedo conceder acceso al catálogo de funciones a los catálogos a los que no puedo acceder?**

No. El ámbito de cualquier función que cree se limita a los catálogos y grupos de usuarios dentro de su propio ámbito. No puede crear una función con un acceso más amplio del que tiene, a menos que el administrador haya configurado su cuenta para permitir la administración de funciones ampliada.

**¿Cuál es la diferencia entre Solo lectura y Control total?**

**Solo lectura** te permite ver **Funciones personalizadas**, Campos activos, **Registros de importación** y **Limpieza de usuarios**. Puede examinar, buscar y descargar informes, pero no puede realizar ninguna acción. **Control total** te ofrece todas esas funciones, además de la posibilidad de crear, editar y eliminar funciones, importar usuarios mediante CSV, asignar y eliminar usuarios de funciones y purgar usuarios eliminados.

**¿Puedo dar a un rol los mismos permisos que tengo para crear?**

Sí. Puede asignar los permisos que tenga personalmente a las funciones que cree. No puede exceder su propio conjunto de permisos, pero puede crear funciones con el mismo nivel de acceso que tiene, o cualquier subconjunto del mismo.

**¿El seguimiento de auditoría muestra quién soy cuando realizo cambios?**

Sí. En el informe de auditoría se enumera la función personalizada como origen de cada cambio. Esto significa que los administradores completos pueden ver qué función personalizada ha realizado cada cambio en el sistema.

**¿Qué sucede con las funciones existentes cuando esta característica está habilitada para la cuenta?**

Las funciones personalizadas existentes con acceso **Avanzado** ya habilitado obtienen acceso automáticamente a **Registros de importación**. El resto del comportamiento existente no cambia. Los roles que no tienen el acceso avanzado habilitado no se ven afectados.

