---
jcr-language: en_us
title: Preguntas frecuentes (Report Builder)
description: Obtenga respuestas a preguntas frecuentes relativas a Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# Preguntas frecuentes (Report Builder)

**¿Cuál es la diferencia entre una plantilla y un informe?**

Las plantillas son configuraciones de informe prediseñadas que proporciona Adobe Learning Manager. Están diseñados para casos prácticos habituales, listos para su descarga inmediata y son de solo lectura. No se pueden editar. Los informes son sus propias configuraciones guardadas. Se crean creando desde cero o duplicando una plantilla y editando la copia. Los informes aparecen en la pestaña **Informes**; las plantillas aparecen en la pestaña **Plantillas**.

**¿Puedo editar una plantilla directamente?**

No. Las plantillas son de solo lectura. Para personalizar una plantilla, selecciona **Duplicar** para crear una copia editable. Los cambios se guardan como un nuevo informe en la pestaña **Informes** y no afectan a la plantilla original.

Las filas duplicadas aparecen cuando un campo de los datos tiene una relación de uno a varios con el registro principal. Las causas comunes incluyen sesiones con varios instructores (una fila por instructor por sesión) y objetos de aprendizaje con varios autores. Para resolver este problema, agregue como columna el campo que tiene varios valores, como **Nombres de instructores** o **Nombre de autor**.

**¿Por qué se muestran las fechas en UTC?**

Report Builder devuelve valores de fecha en UTC en esta versión. La zona horaria configurada de su cuenta se aplicará a los campos de fecha en una futura versión. Al analizar datos basados en fechas, tenga en cuenta el desplazamiento UTC correspondiente a la zona horaria principal de su cuenta.

**¿Cuánto tiempo tardan en aparecer los nuevos datos de inscripción o finalización?**

Report Builder extrae datos de la base de datos de Adobe Learning Manager, que tiene una latencia máxima de aproximadamente 15 minutos desde que se produce un evento en el sistema. Si acaba de registrar una inscripción o una finalización y no aparece en el informe, espere al menos 15 minutos y vuelva a descargarla.

**¿Hay un límite en las filas o columnas de un informe?**

Los informes se limitan a aproximadamente 1 millón de filas. No hay límite en el número de columnas en esta versión. Si el informe requiere más de 1 millón de filas, aplique filtros para reducir el ámbito.

**¿Hay un límite de tamaño de archivo al exportar informes del Report Builder?**

Actualmente, los archivos de informe exportados mayores de 5 GB no son compatibles con Report Builder. Si se espera que el informe supere este tamaño, plantéese aplicar filtros adicionales o reducir el número de filas para mantener la exportación por debajo de 5 GB.

**¿Puedo obtener datos del Report Builder a través de una API o automatización?**

El acceso automatizado de la API a los informes del Report Builder está previsto para una futura versión. En la versión actual, los informes se descargan manualmente a través de la interfaz de usuario del Report Builder o se reciben de forma programada a través de la función de suscripción.
