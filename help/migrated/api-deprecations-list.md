---
jcr-language: en_us
title: Rechazas de API en Adobe Learning Manager
description: A medida que evolucionan las API de Adobe Learning Manager, estas se reorganizan o actualizan periódicamente. Cuando las API evolucionan, la API antigua queda obsoleta y, finalmente, se elimina. Esta página contiene información que debe conocer al migrar de versiones de API obsoletas a versiones de API más nuevas y estables.
contentowner: saghosh
source-git-commit: 83fdd06aed823a50458d50c8ac240d56af873a6d
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---


# Rechazas de API en Adobe Learning Manager

## Rechazas de API en la versión de marzo de 2024 de Adobe Learning Manager

### Cambios en los límites de tasas

Con la próxima versión de Adobe Learning Manager, estamos reestructurando los límites de tasas de API para las nuevas cuentas. Para las cuentas existentes, solo se limitarán las API de administración. Después de los 90 días (unos 3 meses), reestructuraremos los límites de tasas para todas las API, pero las cuentas existentes se incluirán en la lista blanca de acuerdo con el uso actual. Las cuentas existentes deben volver a consultar su uso de la API de alumno.

En el caso de las cuentas nuevas, si desean aumentar los límites de las tasas, deben ponerse en contacto con el equipo de éxito del cliente de ALM.

#### ¿Qué API tendrán límite de velocidad?

En el caso de las nuevas cuentas, todas las API de administrador, alumno y búsqueda tendrán límites de velocidad y se aplicará el desglose.

La velocidad de ráfaga o el límite de ráfaga de la API se refiere al número máximo de solicitudes que se pueden realizar a una API en un breve intervalo de tiempo limitado.

En la tabla siguiente se enumeran los límites de velocidad y fragmentación para las API.

<table>
    <tr>
        <th>API</th>
        <th>Número de solicitudes-RPM</th>
        <th>Número de solicitudes-Ráfaga</th>
    </tr>
    <tr>
        <td>Administrador</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Alumno</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Buscar</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>

### Cambios en los límites de desplazamiento

Debido al gran número de registros recuperados por el valor de desplazamiento y a la ralentización del rendimiento general, estamos aplicando un límite de **500** registros. En la siguiente versión, tanto para el administrador como para el alumno, el **Usuarios de GET** La API devolverá un máximo de **500** registros.

Si necesita obtener más registros, utilice la **Trabajos de GET** API.

El cambio en los límites de compensación se aplica a todos los clientes nuevos. Para los clientes existentes, se aplica la regla de los 90 días.

### Excluir rutas

En la actualidad, las API de Learning Manager siguen una estructura de datos de gráficos, que le permite obtener datos a través del modelo de API mediante includes. Aunque se puede recorrer una API de hasta siete niveles, obtener los datos mediante una sola llamada de API resulta computacionalmente caro.

Recomendamos que todos los clientes nuevos y existentes realicen llamadas pequeñas varias veces en lugar de una llamada grande. Este enfoque evitará que se carguen datos no deseados en la llamada.

Queremos hacer cumplir estas restricciones en las nuevas cuentas y mantener una lista blanca de las cuentas existentes.

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

### Cambios de recuento de resumen de instancia

Actualmente, en el punto final del resumen de objetos de aprendizaje, obtiene el número de todas las instancias posibles. Por ejemplo, para un curso, puede ver el número de inscripciones y listas de espera en la respuesta de **GET /learningObjects/{loId}/instance/{loInstanceId}/summary**. A continuación, puede ver los argumentos completedCount e enrollmentCount en la respuesta. Si el curso es un curso virtual o de clase, también puede ver su límite de puestos y su límite de lista de espera.

El proceso de recuperar los recuentos de finalización e inscripción es computacionalmente costoso, por lo tanto, el cálculo se realiza sobre la base de una solicitud. Si los datos no están presentes en la caché, se vuelven a cargar, lo que requiere muchos recursos informáticos. Si hay muchos usuarios inscribiéndose en un curso, los recuentos serán grandes y afectarán de forma efectiva al rendimiento de la CPU.

En la siguiente versión de Adobe Learning Manager, en el extremo de resumen de la instancia de objeto de aprendizaje, se almacenan en caché los valores de completedCount, enrollmentCount, seatLimit y waitlistCount. La información almacenada en caché se mantiene hasta que se producen cambios en las inscripciones o cancelaciones de inscripciones. Para recuentos superiores a 1000 inscripciones, asumiremos los recuentos estimados e invalidaremos los resultados para todas las cuentas existentes y nuevas.

>[!NOTE]
>
>En el caso de recuentos como completedCount, enrollmentCount, seatLimit y waitlistCount superiores a 1000, es aconsejable interpretarlos como estimaciones en lugar de cifras precisas, ya que se recuperarán de la caché.

### Ordenar por nombre

En la siguiente versión de Adobe Learning Manager, name y -name dejan de utilizarse en el campo de ordenación de las siguientes API:

* GET /userGroups/{userGroupId}/users
* GET/usuarios

>[!NOTE]
>
>Para todas las cuentas existentes y nuevas, la ordenación por nombre y -name quedará obsoleta.


## Desutilizaciones de API en la versión de noviembre de 2023 de Adobe Learning Manager

### Anular indicador

En la versión de noviembre de 2023 de Adobe Learning Manager, se ha interrumpido el indicador de anulación de las API. El indicador override no forma parte de la especificación de la API pública y está pensado para pruebas de backend. El indicador ya no está disponible para las API de alumno. Sin embargo, el indicador sigue siendo válido para las API de administración.

La razón por la que estamos dejando de utilizar el indicador para las API de alumno es que el indicador de anulación obtenía una gran cantidad de datos a través de las API de alumno.

En adelante, la siguiente API de alumno dejará de funcionar porque tiene el indicador de anulación.

<code>https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&amp;página[límite]=10&amp;sort=id&amp;override=TRUE</code>

### Cambios en la API para nuevas recomendaciones basadas en aptitudes

Adobe Learning Manager mejora las recomendaciones para las cuentas habilitadas para clientes y partners. Esta mejora en el algoritmo de recomendación con el cambio en el algoritmo de clasificación para cursos, rutas de aprendizaje y certificaciones proporciona una mejor experiencia del usuario en la detección de contenido.

El algoritmo ya no permitirá recomendaciones basadas en pares. El cambio no afectará a los usuarios existentes, pero la opción Adaptado al sector seguirá existiendo. Para la opción Personalizado, Adobe Learning Manager ya no permitirá la selección personalizada basada en compañeros.

El grupo de compañeros ahora se convierte en una cuenta y los alumnos verán una cadena que muestra los temas de tendencia del grupo. Todas las recomendaciones son explicables. Por ejemplo, si está viendo algo sobre un tema, la tarjeta de la tira mostrará el motivo del curso.

### Cambios En El Informe De Anuncio De Notificaciones

En versiones anteriores de Adobe Learning Manager, el informe Anuncio de notificación no tenía filtros. Adobe Learning Manager descargó todas las notificaciones de la cuenta.

En la versión de noviembre de 2023, hemos añadido un filtro de fecha mediante el cual puede descargar las notificaciones dentro de un período especificado.  Sin embargo, puede descargar el informe sólo durante los últimos seis meses.