---
description: Creación y administración de informes para responsables.
jcr-language: en_us
title: Informes
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 0%

---



# Informes

Creación y administración de informes para responsables.

Adobe Learning Manager le permite crear informes variados para realizar el seguimiento, supervisar y controlar las actividades de los alumnos. Se realiza un seguimiento de las actividades de los alumnos y se capturan automáticamente en la base de datos. Los informes de responsable y administrador se generan a partir de la base de datos.

## Resumen {#overview}

El proceso de generación de informes es el mismo para el administrador y el responsable. Los responsables pueden ver los informes correspondientes a sus subordinados, mientras que el administrador puede ver todos los informes de la organización.

Los informes se agregan en un tablero. Debe existir un informe dentro de un tablero. A **Panel predeterminado** existe de forma predeterminada en la página informes. Cualquier informe que agregue se moverá a este panel predeterminado. Para agregar informes a paneles individuales, utilice la flecha desplegable y elija Agregar informe. Para obtener más información sobre la creación de paneles, consulte la sección Tableros de esta página.

## Tableros de responsable {#manager-dashboards}

Un responsable puede ver información sobre su equipo directo o indirecto en forma de resumen.

El responsable puede filtrar el informe por intervalos como trimestre, este mes, últimos tres meses completos y últimos 12 meses completos.

## Resumen del aprendizaje {#learningsummary}

![](assets/manager-learningsummary.png)

*Ver resumen de aprendizaje*

![](assets/manager-dashboard.jpg)

*Filtrar resumen de aprendizaje por fecha*

## Panel de cumplimiento {#compliancedashboard}

Consulte el cumplimiento del equipo y el miembro del equipo que roza el incumplimiento. Elija los objetos de aprendizaje y vea el estado de cada uno.

![](assets/compliance-dashboard.png)

*Ver panel de cumplimiento*

## Estado de aptitudes {#skillsstatus}

Consulte el porcentaje de alumnos de cada aptitud. Elija un máximo de cinco aptitudes de los alumnos que desee ver. La visualización se realiza en forma de gráfico de barras apiladas. Al pasar el ratón por cada barra, puede ver el desglose del estado de esa aptitud.

![](assets/manager-skills-status.png)

*Ver el estado de las aptitudes de un alumno*

## Rastreador de aptitudes {#skilstracker}

Vea una proyección de finalización de aptitudes de un equipo. Elija el porcentaje de finalización de destino y la fecha de una aptitud.

En función de los datos históricos, puede ver una representación gráfica de la proyección de finalización de aptitudes en la fecha seleccionada.

![](assets/historical-data.png)

*Ver proyección de finalización de aptitudes*

## Creación de informes {#creatingreports}

1. Haga clic en Informes en el panel izquierdo. Aparece la página Resumen del informe.\
   **Nota**
De forma predeterminada, aparecen al menos tres informes de muestra en la página Resumen de informes. Solo puede ver estos informes de muestra para hacerse una idea de cómo puede crearlos y personalizarlos.

1. En la página Resumen del informe, haga clic en Agregar. Aparece el cuadro de diálogo Creación de informes.
1. Haga clic en Guardar para terminar de crear un informe. A continuación se muestra un informe de muestra como referencia.

![](assets/add-report.png)

*Cuadro de diálogo Agregar informe*

En Tipo de informe, puede elegir un conjunto de informes predefinidos o elegir uno personalizado. Puede ver los siguientes informes como parte de un conjunto de informes predefinidos:

* Aptitudes asignadas y obtenidas
* Curso inscrito y completado
* Eficacia de los cursos
* Programas de aprendizaje inscritos y completados
* Tiempo de aprendizaje dedicado a cada curso
* Tiempo de aprendizaje dedicado por trimestre

Puede utilizar los tipos de informe mencionados anteriormente para generar informes de más de 300 variaciones.

Nombre del informe Escriba un título para el informe.

**Eje Y principal** Elija el criterio principal o el primero para el informe en las opciones desplegables. Para algunos de los criterios seleccionados, tiene la opción de elegir uno o varios estados en el cuadro desplegable Estados adyacente. Por ejemplo, para un criterio principal de estadísticas de inscripción en cursos, los estados pueden ser completado, incompleto, inscrito, etc. Los datos del rango principal se representan en forma de gráficos de barras en el informe.

**Eje Y secundario** Seleccione los criterios/rango del eje Y secundario para el informe en las opciones desplegables. Por ejemplo, en la opción de inscripción en programas de aprendizaje, elija uno o varios estados en el menú desplegable Estados adyacente. Los datos del rango secundario se representan en forma de gráficos de líneas.

**Eje X** Elija los criterios del eje X adecuados para el informe en las opciones desplegables. Si se elige el eje X como fecha, está disponible una opción para agrupar el criterio del eje X por día, mes, trimestre y año.

**Fecha** Elija la opción adecuada en el menú desplegable. Opciones: último mes, trimestre, año, trimestre hasta la fecha (últimos 90 días), año hasta la fecha (últimos 365 días) e intervalo de fechas. Si selecciona el intervalo de fechas, proporcione las fechas Desde y Hasta de la siguiente manera:

**Desde** Elija la fecha de inicio a partir de la cual desea ver el informe.

**Para** Elija la fecha de finalización del informe.

## Filtros {#filters}

Los filtros aparecen en el cuadro de diálogo Agregar informe en la parte inferior en función de los tipos de informes que haya elegido. A continuación se mencionan algunos de los filtros destacados.

**Responsable** Puede elegir cualquiera de los responsables según la jerarquía. Para algunos responsables, puede haber responsables subordinados y varios empleados que informen a cada responsable subordinado.

**Perfil** Elija la designación de su empleado. Ayudaría a ver los informes de los empleados en función de su perfil o designación. Por ejemplo, técnico informático, ingeniero, etc.

**Grupo de usuarios** Elija el grupo de usuarios en función del cual desee filtrar los informes. Learning Manager busca los grupos de usuarios definidos para su cuenta desde la función Usuarios.

**Curso** Puede filtrar su informe según cualquier curso si lo selecciona de la lista desplegable.

![](assets/sample-report-admin.png)

*Ver el gráfico de los cursos inscritos y completados*

>[!NOTE]
>
>Encima de la leyenda del gráfico, puede ver un cuadro de zoom. Puede mover el cursor sobre él, hacer clic y arrastrar el cursor sobre cualquier parte del área del cuadro de zoom que desee aumentar.

Puede ver los valores secundarios del eje Y en forma de línea a través de las barras del gráfico. Por ejemplo, en la muestra anterior, puede ver los valores de Eficacia en una línea gris a lo largo del gráfico.

## Informes de grupos de usuarios {#user-group-reporting}

Realiza un seguimiento del rendimiento de los grupos de usuarios, como departamentos, socios externos y funciones, en comparación con otros grupos de usuarios o con otros objetivos de aprendizaje.

### Grupos de usuarios {#usergroups}

Para generar informes basados en grupos de usuarios, elija **Grupo de usuarios** en el eje X desde la lista de opciones desplegables como se muestra en la captura de pantalla a continuación.

![](assets/x-axis-reporting.png)

*Generar informes de grupos de usuarios*

Otro **Seleccionar** aparece junto al eje X con una lista de grupos de usuarios disponibles para su cuenta. En este menú desplegable, puede seleccionar uno o varios grupos de usuarios.

Una vez guardado y generado este informe, si ha seleccionado varios grupos de usuarios, el informe se genera con todos los grupos de usuarios representados en un gráfico de barras adyacentes en el eje X.

Este informe de grupo de usuarios le permite comparar el rendimiento de un departamento/división/función con el otro para evaluar sus logros de aprendizaje.

### Atributos de usuario/grupos de usuarios personalizados {#customusergroupsuserattributes}

También puede crear grupos de usuarios personalizados con la función Añadir usuarios/grupos de usuarios en Learning Manager. Después de crear los grupos de usuarios, puede generar informes para esos grupos de usuarios personalizados con la ayuda de una lista de atributos, como ubicación, sucursal, etc.

En el eje X, elija la opción Atributos de usuario y seleccione el atributo desde **seleccionar** situado junto a él. Para crear un informe de grupo de usuarios personalizado basado en estos atributos, también debe elegir el grupo de usuarios adecuado en el filtro.

Los responsables pueden crear informes de grupos de usuarios solo para los miembros de su propio equipo como alumnos.

## Tipos de informes {#typesofreports}

* Estadísticas de distribución de cursos para alumnos
* Informe sobre la eficacia de los cursos
* Informe basado en habilidades del alumno
* Estadísticas de inscripción de programas de aprendizaje para alumnos
* Tiempo de aprendizaje dedicado por los alumnos
* Finalización de certificación

## Mis informes {#myreports}

Un tablero es una colección de informes. Los informes se pueden agrupar en un tablero según su elección.

**Informes de muestra**

Haga clic en esta ficha para ver algunos informes indicativos basados en puntos de datos de ejemplo. Explore estos informes para hacerse una idea de los diferentes tipos de informes con muchas funciones que puede generar con los datos de su cuenta.

**Mis informes**

Haga clic en esta ficha del tablero para ver todos los tableros creados. En la lista desplegable del tablero de visualización, puede seleccionar el tablero por defecto o cualquiera de los tableros creados.

**Agregar panel**

1. Haga clic en Añadir panel en el lado derecho de la página para empezar a crear sus propios tableros.

   ![](assets/add-dashboard.png)

   *Crear su propio tablero*

1. Proporcione el nombre y la descripción del tablero y haga clic en **[!UICONTROL Guardar]**.

Puede ver el tablero creado recientemente en la lista Mis tableros.

Para añadir informes a su tablero, haga clic en el menú desplegable situado en la esquina superior derecha de la ventana de su tablero y haga clic en Añadir informe. El informe que cree de esta manera se asociará a su panel.

>[!NOTE]
>
>Los informes que cree haciendo clic en Agregar en la esquina superior derecha de la página Informes se agregan al panel predeterminado.

**Informes compartidos**

Los informes compartidos son un conjunto de informes que han compartido con usted otros usuarios de su organización. Si tiene los permisos, puede descargar o duplicar los informes compartidos. Póngase en contacto con el administrador de su organización para obtener derechos de acceso de descarga o duplicado para los informes compartidos.

**Informes suscritos**

Puede suscribirse a sus informes favoritos proporcionando su ID de correo electrónico aquí. Los informes a los que se suscribe se le envían por correo electrónico.

Haga clic en **Editar** situado en la esquina derecha del nombre del informe en la lista de informes para modificar la suscripción en cualquier momento.

## Visualización de informes {#viewingreports}

En la página Resumen de informes, puede ver todos los informes. Puede minimizar cada informe haciendo clic en el icono menos (-) en la esquina superior derecha de cada informe. Haga clic en el icono + para ver el informe de nuevo.

**Vista rápida con fechas diferentes**

Los valores de fecha que se utilizan para ver el informe son temporales. Esta vista del informe no se descarga al elegir la opción de descarga. Esta es sólo una vista temporal.

Puede cambiar el intervalo/valor de fecha de cualquier informe y ver rápidamente para una fecha diferente sin modificar ni guardar el informe. Haga clic en el icono de edición (como se muestra con una flecha en la captura de pantalla siguiente) junto al intervalo de fechas, como SAT, último año, etc. Elija el nuevo valor en el menú desplegable y haga clic en la marca de verificación para confirmar el cambio. Puede cancelar el cambio haciendo clic en la marca X.

**Vista rápida con diferentes responsables**

Si varios responsables le informan, puede ver rápidamente los informes de cada responsable. Elija el nombre del responsable en la lista desplegable para mostrar un informe único para cada responsable.
**Editar/Mover al tablero/Crear una copia/Eliminar/Cambiar el tamaño de informes** Haga clic en la flecha desplegable en la esquina superior derecha de cada informe para ver opciones desplegables como Editar/Mover al panel/Crear una copia/Eliminar/Cambiar el tamaño.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Editar** Al modificar datos, para volver a los valores iniciales, haga clic en Restablecer. Haga clic en Guardar después de modificar los valores.

**Mover al panel** Puede mover el informe actual a otro tablero, que se selecciona de la lista de tableros.

**Crear una copia** Puede copiar el informe en el mismo tablero o en otro, que se selecciona de la lista de tableros.

**Eliminar** Haga clic en Eliminar para eliminar el informe. Aparece un mensaje de advertencia/confirmación antes de eliminar el informe.

**Redimensionar** Puede cambiar el tamaño de los informes en tamaños 1×1 (medio) y 2×2 (grande).

## Suscripciones de correo electrónico {#emailsubscriptions}

Puede obtener sus informes favoritos por correo electrónico mediante su suscripción.

En la página Informes, haga clic en Suscripción por correo electrónico junto al botón Añadir en la esquina superior derecha de la página. Aparece la página de suscripción Informes.

Empiece a escribir el nombre del informe en el campo Informes para seleccionar el nombre del informe en la lista desplegable. Elija la frecuencia del correo electrónico como diaria, semanal, mensual según su elección, añada el asunto del correo electrónico y haga clic en Añadir para suscribirse.

Haga clic en Editar para modificar la suscripción. Haga clic en Eliminar para eliminar la suscripción.
