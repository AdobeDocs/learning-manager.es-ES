---
jcr-language: en_us
title: Report Builder - Preguntas frecuentes
description: Obtenga respuestas a preguntas frecuentes relativas a Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---


# Report Builder - Preguntas frecuentes


**¿Cuál es la diferencia entre una plantilla y un informe?**

Las plantillas son configuraciones de informe prediseñadas que proporciona Adobe Learning Manager. Están diseñados para casos prácticos habituales, listos para su descarga inmediata y son de solo lectura. No se pueden editar. Los informes son sus propias configuraciones guardadas. Se crean creando desde cero o duplicando una plantilla y editando la copia. Los informes aparecen en la pestaña **Informes**; las plantillas aparecen en la pestaña **Plantillas**.

**¿Puedo editar una plantilla directamente?**

No. Las plantillas son de solo lectura. Para personalizar una plantilla, selecciona **Duplicar** para crear una copia editable. Los cambios se guardan como un nuevo informe en la pestaña **Informes** y no afectan a la plantilla original.

Las filas duplicadas aparecen cuando un campo de los datos tiene una relación de uno a varios con el registro principal. Las causas comunes incluyen sesiones con varios instructores (una fila por instructor por sesión) y objetos de aprendizaje con varios autores. Para resolver este problema, agregue como columna el campo que tiene varios valores, como **Nombres de instructores** o **Nombre de autor**.

**¿Por qué cambia el orden de las filas entre dos descargas del mismo informe?**

La generación de informes utiliza un sistema de consultas distribuidas. Sin una ordenación explícita, el orden de las filas depende del nodo de consulta que devuelva primero los resultados, que pueden diferir entre las ejecuciones. Aplique al menos una ordenación al informe para garantizar que el resultado sea coherente en todas las descargas.

**¿Por qué se muestran las fechas en UTC?**

Report Builder devuelve valores de fecha en UTC en esta versión. La zona horaria configurada de su cuenta se aplicará a los campos de fecha en una futura versión. Al analizar datos basados en fechas, tenga en cuenta el desplazamiento UTC correspondiente a la zona horaria principal de su cuenta.

**¿Cuánto tiempo tardan en aparecer los nuevos datos de inscripción o finalización?**

Report Builder extrae datos de la base de datos de Adobe Learning Manager, que tiene una latencia máxima de aproximadamente 15 minutos desde que se produce un evento en el sistema. Si acaba de registrar una inscripción o una finalización y no aparece en el informe, espere al menos 15 minutos y vuelva a descargarla.

**¿Hay un límite en las filas o columnas de un informe?**

Los informes se limitan a aproximadamente 1 millón de filas. No hay límite en el número de columnas en esta versión. Si el informe requiere más de 1 millón de filas, aplique filtros para reducir el ámbito.

**¿Puedo obtener datos del Report Builder a través de una API o automatización?**

El acceso automatizado de la API a los informes del Report Builder está previsto para una futura versión. En la versión actual, los informes se descargan manualmente a través de la interfaz de usuario del Report Builder o se reciben de forma programada a través de la función de suscripción.
