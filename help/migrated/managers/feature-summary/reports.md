---
description: Creación y administración de informes para responsables.
jcr-language: en_us
title: Informes
contentowner: manochan
exl-id: 5a59b56c-111b-46e4-95e5-60cc3af75c4d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 63%

---

# Informes

Creación y administración de informes para responsables.

Adobe Learning Manager le permite crear diversos informes para supervisar y controlar las actividades de los alumnos. Las actividades de los alumnos se supervisan y se capturan automáticamente en la base de datos. Los informes del responsable y el administrador se generan a partir de la base de datos.

## Información general {#overview}

El proceso de generación de informes es el mismo para el administrador y para el responsable. Los responsables pueden ver los informes correspondientes a sus subordinados, mientras que el administrador puede ver todos los informes en toda la empresa.

Los informes se añaden en un tablero. Un informe debe estar dentro de un tablero. Existe un **Panel predeterminado** de forma predeterminada en la página Informes. Cualquier informe añadido por usted se añade a este tablero predeterminado. Para agregar informes a paneles individuales, utilice la flecha desplegable y elija Agregar informe. Para obtener más información sobre cómo crear tableros, consulte la sección Tableros en esta página.

## Tableros de responsables {#manager-dashboards}

Un responsable puede ver información sobre su equipo directo o indirecto en forma de resumen.

El responsable puede filtrar el informe por intervalos como trimestre, este mes, últimos tres meses completos y últimos 12 meses completos.

## Resumen del aprendizaje {#learningsummary}

![](assets/manager-learningsummary.png)

*Ver resumen de aprendizaje*

![](assets/manager-dashboard.jpg)

*Filtrar resumen de aprendizaje por fecha*

## Tablero de cumplimiento {#compliancedashboard}

Consulte el cumplimiento del equipo y el miembro del equipo que roza el incumplimiento. Elija los objetos de aprendizaje y vea el estado de cada uno.

![](assets/compliance-dashboard.png)

*Ver panel de cumplimiento*

## Estado de aptitudes {#skillsstatus}

Consulte el porcentaje de alumnos para cada aptitud. Elija un máximo de cinco aptitudes de los alumnos que desee consultar. La visualización se realiza en forma de gráfico de barras apiladas. Al pasar el cursor sobre cada barra, puede ver el desglose del estado de esa aptitud.

![](assets/manager-skills-status.png)

*Ver el estado de las aptitudes de un alumno*

## Rastreador de aptitudes {#skilstracker}

Vea una proyección de finalización de aptitudes de un equipo. Elija el porcentaje de finalización de destino y la fecha de una aptitud.

En función de los datos históricos, puede ver una representación gráfica de la proyección de finalización de aptitudes en la fecha seleccionada.

![](assets/historical-data.png)

*Ver proyección de finalización de aptitudes*

## Cómo crear informes {#creatingreports}

1. Haga clic en Informes en el panel de la izquierda. Aparece la página Resumen de informes.\
   **Nota**
De forma predeterminada, aparecen al menos tres informes de muestra en la página Resumen de informes. Solo puede ver estos informes de muestra para hacerse una idea de cómo los crearía y los personalizaría.

1. En la página Resumen de informes, haga clic en Añadir. Aparece el cuadro de diálogo de creación de informes.
1. Haga clic en Guardar para terminar de crear un informe. A continuación, se proporciona un informe de muestra como referencia.

![](assets/add-report.png)

*Cuadro de diálogo Agregar informe*

En Tipo de informe, puede seleccionar un conjunto de informes predefinidos o un tipo personalizado. Puede ver los siguientes informes como parte del conjunto de informes predefinidos:

* Aptitudes asignadas y obtenidas
* Cursos en los que me inscribí y que finalicé
* Eficacia de los cursos
* Programas de aprendizaje en los que me inscribí y que finalicé
* Tiempo de aprendizaje dedicado a cada curso
* Tiempo de aprendizaje dedicado por trimestre

Puede utilizar los tipos de informes especificados anteriormente para generar más de 300 variaciones de informes.

Nombre del informe Escriba un título para el informe.

**Eje Y principal** Elija el criterio principal/principal para el informe entre las opciones desplegables. Para algunos de los criterios seleccionados, tiene la opción de elegir uno o varios estados en el cuadro desplegable Estados adyacente. Por ejemplo, para un criterio principal de estadísticas de inscripción en cursos, los estados pueden ser completado, incompleto, inscrito, etc. Los datos del intervalo principal se representan en forma de gráfico de barras en el informe.

**Eje Y secundario** Elija el criterio/rango del eje Y secundario para el informe entre las opciones desplegables. Por ejemplo, en la opción de inscripción en programas de aprendizaje, elija uno o varios estados en el menú desplegable Estados adyacente. Los datos del intervalo secundario se representan en forma de gráfico de líneas.

**Eje X** Elija los criterios apropiados del eje X para el informe entre las opciones desplegables. Si se selecciona la fecha como el eje X, está disponible la opción de agrupar los criterios del eje X por día, mes, trimestre y año.

**Fecha** Elija la opción adecuada en el menú desplegable. Opciones: último mes, trimestre, año, trimestre hasta la fecha (últimos 90 días), año hasta la fecha (últimos 365 días) e intervalo de fecha. Si selecciona el intervalo de fechas, proporcione las fechas &quot;desde&quot; y &quot;hasta&quot; como se indica a continuación:

**Desde** Elija la fecha de inicio a partir de la cual desea ver el informe.

**Para** Elija la fecha de finalización del informe.

## Filtros {#filters}

Los filtros aparecen en el cuadro de diálogo Añadir informe en la parte inferior en función de los tipos de informes que ha seleccionado. Algunos de los filtros prominentes se mencionan a continuación.

**Responsable** Puede elegir cualquiera de los responsables según la jerarquía. Algunos responsables pueden tener responsables subordinados y varios empleados que informen a cada responsable subordinado.

**Perfil** Seleccione la designación de su empleado. Ayudaría en la visualización de informes de empleados según su perfil/designación. Por ejemplo, técnico informático, ingeniero, etc.

**Grupo de usuarios** Seleccione el grupo de usuarios teniendo en cuenta para cuál desea filtrar informes. Learning Manager busca los grupos de usuarios definidos para su cuenta según la función Usuarios.

**Curso** Puedes filtrar tu informe según cualquier curso seleccionándolos en el menú desplegable.

![](assets/sample-report-admin.png)

*Ver gráfico de cursos inscritos y completados*

>[!NOTE]
>
>Sobre la leyenda del gráfico, puede ver un cuadro para aumentar el tamaño. Puede mover el cursor sobre él, hacer clic y arrastrar el cursor sobre cualquier parte del área del cuadro que desee aumentar.

Puede ver los valores secundarios del eje Y en forma de línea a través de las barras del gráfico. Por ejemplo, en la muestra especificada anteriormente, puede ver los valores de Eficacia en una línea gris a través del gráfico.

## Informes de grupos de usuarios {#user-group-reporting}

Controle la manera en que los grupos de usuarios, como los departamentos, los socios externos y las funciones, se desempeñan en comparación con otros grupos de usuarios u otros objetivos del aprendizaje.

### Grupos de usuarios {#usergroups}

Para generar informes basados en grupos de usuarios, elija **Grupo de usuarios** en el eje X entre las opciones de la lista desplegable, como se muestra en la captura de pantalla a continuación.

![](assets/x-axis-reporting.png)

*Generar informes de grupos de usuarios*

Aparece otra lista de **selección** desplegable junto al eje X con una lista de los grupos de usuarios disponibles para su cuenta. En este menú desplegable, puede seleccionar uno o varios grupos de usuarios.

Una vez que guarda y genera este informe, si ha seleccionado varios grupos de usuarios, el informe se genera con todos los grupos de usuarios representados en el gráfico de barras uno al lado del otro en el eje X.

Este informe del grupo de usuarios le permite comparar el rendimiento de un departamento/división/función con otro para evaluar sus logros de aprendizaje.

### Atributos personalizados de los usuarios/grupos de usuarios {#customusergroupsuserattributes}

También puede crear grupos de usuarios personalizados con la función Añadir usuarios/grupos de usuarios en Learning Manager. Después de crear los grupos de usuarios, puede generar informes para los grupos de usuarios personalizados con la ayuda de una lista de atributos, como, por ejemplo, ubicación, sucursal, etc.

En el eje X, elija la opción Atributos de usuario y seleccione el atributo en el menú desplegable **seleccionar** situado junto a él. Para crear un informe de grupo de usuarios personalizado basado en estos atributos, también debe elegir el grupo de usuarios adecuado en el filtro.

Los responsables pueden crear informes de grupos de usuarios solo para sus propios miembros del equipo como alumnos.

## Tipos de informes {#typesofreports}

* Estadísticas de entrega del curso para alumnos
* Informe sobre la eficacia de los cursos
* Informe basado en las aptitudes del alumno
* Estadísticas de inscripción en el programa de aprendizaje para alumnos
* Tiempo de aprendizaje dedicado por los alumnos
* Finalización de la certificación

## Mis informes {#myreports}

Un tablero es una colección de informes. Los informes se pueden agrupar en un tablero según su elección.

**Informes de muestra** 

Haga clic en esta ficha para ver algunos informes indicativos basados en puntos de datos de ejemplo. Explore estos informes para tener una idea de los distintos tipos de informes repletos de funciones que puede generar con los datos de su cuenta.

**Mis informes**

Haga clic en esta ficha del tablero para ver todos los tableros creados. En la lista desplegable del tablero de visualización, puede seleccionar el tablero por defecto o cualquiera de los tableros creados.

**Añadir tablero** 

1. Haga clic en Añadir tablero en la parte derecha de la página para comenzar a crear sus propios tableros.

   ![](assets/add-dashboard.png)

   *Crea tu propio tablero*

1. Proporcione un nombre y una descripción para el tablero y haga clic en **[!UICONTROL Guardar]**.

Puede ver el tablero creado recientemente en la lista Mis tableros.

Para añadir informes a su tablero, haga clic en el menú desplegable situado en la esquina superior derecha de la ventana de su tablero y haga clic en Añadir informe. El informe que crea de este modo se asocia con su tablero.

>[!NOTE]
>
>Los informes que cree haciendo clic en Agregar en la esquina superior derecha de la página Informes se agregan al panel predeterminado.

**Informes compartidos** 

Los informes compartidos son una colección de informes que otros usuarios dentro de la empresa han compartido con usted. Si tiene los permisos, puede descargar o duplicar los informes compartidos. Póngase en contacto con el administrador de su empresa con el fin de obtener privilegios de acceso para descargar/duplicar los informes compartidos.

**Informes de suscripción**

Para suscribirse a sus informes favoritos, proporcione su Id. de correo electrónico aquí. Los informes a los que se suscribe se le envían por correo electrónico.

Haz clic en el icono **Editar** situado en la esquina derecha del nombre de tu informe en la lista de informes para modificar tu suscripción en cualquier momento.

## Visualización de informes {#viewingreports}

En la página Resumen de informes, puede ver todos los informes. Puede minimizar cada informe si hace clic en el icono menos (-) situado en la esquina superior derecha de cada informe. Haga clic en el icono + para ver su informe nuevamente.

**Vista rápida con fechas diferentes** 

Los valores de fecha que utiliza para ver el informe son temporales. Esta vista del informe no se descarga cuando selecciona la opción Descargar. Esta vista solo es temporal.

Puede cambiar el intervalo/valor de fecha para cualquier informe y obtener una vista rápida de una fecha diferente sin tener que modificar y guardar el informe. Haga clic en el icono Editar (como se muestra con una flecha en la captura de pantalla a continuación) junto al intervalo de fecha, por ejemplo, trimestre hasta la fecha, último año, etc. Seleccione el nuevo valor en el menú desplegable y haga clic en la marca de verificación para confirmar el cambio. Para cancelar el cambio, haga clic en la marca X.

**Vista rápida con responsables diferentes**

Si varios responsables le informan a usted, podrá ver los informes rápidamente para cada responsable. Elija el nombre del responsable en la lista desplegable para mostrar un informe único para cada responsable.
**Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes** Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para ver opciones desplegables como Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Editar** Al modificar los datos, para volver a los valores iniciales, haga clic en Restablecer. Haga clic en Guardar después de modificar los valores.

**Mover al panel** Puede mover el informe actual a otro panel, que se elige de la lista de paneles.

**Crear una copia** Puede copiar el informe en el mismo panel o en otro distinto, que se elija en la lista de paneles.

**Eliminar** Haga clic en Eliminar para quitar el informe. Aparece un mensaje de advertencia/confirmación antes de que se elimine el informe.

**Cambiar tamaño** Puedes cambiar el tamaño de tus informes en tamaños 1×1 (mediano) y 2×2 (grande).

## Suscripciones por correo electrónico {#emailsubscriptions}

Puede recibir sus informes favoritos por correo electrónico mediante una suscripción.

En la página Informes, haga clic en Suscripción por correo electrónico junto al botón Añadir que se ve en la esquina superior derecha de la página. Aparece la página de suscripción a informes.

Empiece a escribir el nombre del informe en el campo Informes para seleccionar el nombre del informe en la lista desplegable. Elija la frecuencia del correo electrónico como diaria, semanal, mensual según su elección, añada el asunto del correo electrónico y haga clic en Añadir para suscribirse.

Haga clic en Editar para modificar la suscripción. Haga clic en Eliminar para eliminar la suscripción.
