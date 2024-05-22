---
jcr-language: en_us
title: Obsoletaciones de API en Adobe Learning Manager
description: A medida que evolucionan las API de Adobe Learning Manager, estas se reorganizan o actualizan periódicamente. Cuando las API evolucionan, la API antigua queda obsoleta y, finalmente, se elimina. Esta página contiene información que debe conocer al migrar de versiones de API obsoletas a versiones de API más nuevas y estables.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 32%

---

# Cambios y depreciaciones de la API en Adobe Learning Manager

## Rechazas de API en la versión de marzo de 2024 de Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

### Cambios en los límites de desplazamiento

Debido al gran número de registros recuperados por el valor de desplazamiento y a la ralentización del rendimiento general, estamos aplicando un límite de **500** registros. En la siguiente versión, tanto para el administrador como para el alumno, el **Usuarios de GET** La API devolverá un máximo de **500** registros.

Si necesita obtener más registros, utilice la **Trabajos de GET** API.

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

#### ¿Qué rutas están obsoletas?

Las siguientes rutas están en desuso:

* /learningObjects
   * Rutas obsoletas:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Nuevos trazados:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Ruta obsoleta:
      * enrollment.instances.subLoInstances.learningObject
   * Nueva ruta:
      * enrollment.instances.subLoInstances

* /enrollments
   * Ruta obsoleta:
      * loInstance.learningObject.enrollment
   * Nueva ruta:
      * loInstance.learningObject

* /learningObjects/{id}
   * Ruta obsoleta:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nueva ruta:
      * instance.subLoInstances

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Ordenar por nombre

En la siguiente versión de Adobe Learning Manager, name y -name ya no se usan en el campo de ordenación de las siguientes API:

* GET /userGroups/{userGroupId}/users
* GET/usuarios

>[!NOTE]
>
>Para todas las cuentas existentes y nuevas, la ordenación por nombre y -name quedará obsoleta.


## Rechazas de API en la versión de noviembre de 2023 de Adobe Learning Manager

### Indicador de anulación

En la versión de noviembre de 2023 de Adobe Learning Manager, hemos suspendido el indicador de anulación de las API. El indicador de anulación no forma parte de la especificación de las API públicas y se ha diseñado para las pruebas de back-end. El indicador ya no está disponible para las API de alumno. Sin embargo, sigue siendo válido para las API de administrador.

La razón por la que estamos dejando de utilizar el indicador para las API de alumno es que el indicador de anulación obtenía una gran cantidad de datos a través de las API de alumno.

A partir de ahora, la siguiente API de alumno dejará de funcionar debido a que presenta el indicador de anulación.

_/primeapi/v2/users?page[offset]=0&amp;página[límite]=10&amp;sort=id&amp;override=TRUE_

### Cambios en la API para nuevas recomendaciones basadas en aptitudes

Adobe Learning Manager mejora las recomendaciones para las cuentas de clientes y socios. Esta mejora en el algoritmo de recomendación con el cambio en el algoritmo de clasificación por curso, ruta de aprendizaje y certificación proporciona una mejor experiencia al usuario a la hora de descubrir contenidos.

El algoritmo ya no permitirá recomendaciones entre iguales. El cambio no afectará a los usuarios existentes, pero seguirá existiendo la opción Adaptado al sector. En el caso de la opción Personalizado, Adobe Learning Manager ya no permitirá la selección personalizada entre iguales.

El grupo de iguales se convierte ahora en una cuenta y los alumnos verán una cadena que muestra los temas destacados del grupo. Todas las recomendaciones tienen una explicación. Por ejemplo, si ve algo sobre un tema, la tarjeta de la tira mostrará el motivo del curso.

### Cambios En El Informe De Anuncio De Notificaciones

En versiones anteriores de Adobe Learning Manager, el informe Anuncio de notificación no tenía filtros. Adobe Learning Manager ha descargado todas las notificaciones de la cuenta.

En la versión de noviembre de 2023, hemos añadido un filtro de fecha mediante el cual puede descargar las notificaciones dentro de un período especificado.  Sin embargo, puede descargar el informe sólo durante los últimos seis meses.

### Rechazo de valores de desplazamiento altos en el extremo GET/usuarios

Para mejorar el rendimiento del sistema y administrar el uso de recursos de forma más eficaz, Adobe ha eliminado los valores de desplazamiento alto en el extremo GET/usuarios para ambos **ADMINISTRADOR** y **ALUMNO** ámbitos. Se recomienda utilizar la **API de trabajos** para recuperar los registros con un valor de desplazamiento.

