---
description: Obtenga información sobre cómo Adobe Learning Manager marca a los alumnos como asistentes cuando ven una grabación de sesión de Adobe Connect, sin actualizaciones manuales
jcr-language: en_us
title: Seguimiento de la asistencia mediante las vistas de grabación de Adobe Connect
exl-id: f4cb951e-3cb1-4caf-b6b8-aec86b32f782
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%
---

# Seguimiento de la asistencia mediante las vistas de grabación de Adobe Connect

## Información general

Adobe Learning Manager puede realizar el seguimiento de la asistencia a sesiones de clase virtual de Adobe Connect mediante vistas de grabación. Cuando un alumno pierde una sesión en directo pero observa la grabación en Adobe Connect durante bastante tiempo, Learning Manager indica que el alumno ha asistido a la sesión. A continuación, el alumno completa el módulo de sesión y puede avanzar hacia la finalización del objeto de aprendizaje al que pertenece la sesión.

Antes de esta función, Learning Manager no podía registrar la asistencia de los alumnos que veían una grabación de Connect. Un alumno que se perdía una sesión en directo no podía completarla y un instructor tenía que intervenir y marcar la asistencia manualmente. Esta función elimina ese paso manual. Adobe Connect indica quién ha visto qué grabación y durante cuánto tiempo, y Learning Manager compara el tiempo de visualización con los criterios de finalización establecidos para la cuenta.

Una vez que el alumno cumple los criterios de finalización de la sesión grabada, los alumnos se marcan en la aplicación de administración.

El ID de correo electrónico del alumno debe ser el mismo en Adobe Learning Manager y Adobe Connect, ya que Adobe Learning Manager redirige al alumno a Adobe Connect con el mismo ID de correo electrónico.
La frecuencia de sincronización predeterminada y el intervalo más corto que el administrador de integración puede establecer es de una hora.


## Quién hace qué

| Función | Lo que hacen |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Administración | Abre la grabación de la sesión y la observa cuando falta la sesión en directo. |
| El instructor | Inicia la grabación durante la sesión en directo, por lo que existe una grabación y una transcripción. |
| Administrador de integración | Configura la cuenta de Adobe Connect que utiliza la sincronización de asistencia y establece la programación de sincronización o la activa o desactiva. |
| Autor o administrador de entregas | Programa las sesiones de clase virtual y, para los programas de varios días, reutiliza una sala permanente en varios días. |
| Adobe Connect | Captura el correo electrónico de cada alumno y la hora de visualización de grabación, y muestra la lista de visores de grabación mediante una API. |

Cada función tiene una parte independiente para que la asistencia basada en la grabación funcione.

## Glosario

| Término | Significado |
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| Sesión de clase virtual | Una sesión de clase virtual alojada en Adobe Connect. |
| Formación virtual con instructor | Formación impartida por un instructor mediante sesiones de clase virtual. |
| Objeto de aprendizaje | Un curso, por ejemplo, que contiene el módulo de sesión. |
| Sala permanente | Una sala de Adobe Connect que se puede reutilizar para varias sesiones, por ejemplo el día 1, el día 2 y el día 3. |
| Criterios de finalización | El porcentaje de la grabación que un alumno debe ver para que se marque como completada para el módulo. |

## Casos de uso

### Un alumno pierde una sesión en directo

Un alumno no puede unirse a la sesión de clase virtual en directo. Más adelante, el alumno abre la sesión en Learning Manager y observa la grabación. Una vez que la hora de visualización cumple los criterios de finalización, Learning Manager marca al alumno como asistido y el alumno completa el módulo sin solicitar ayuda al instructor.

### Un alumno que solo observa parcialmente

Un alumno abre la grabación pero ve menos del recurso compartido necesario. No se cumplen los criterios de finalización, por lo que Learning Manager no marca al alumno como asistido.

### Sesiones de varios días en una sala permanente

Un autor o un administrador de entregas programa las sesiones para el día 1, el día 2 y el día 3 en la misma sala de Connect permanente. Pueden ver y reutilizar el nombre de la sala sin iniciar sesión en Adobe Connect.

## Funciones principales

| Función | Qué hace |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Asistencia automática | Marca a un alumno como asistido para una sesión de clase virtual basada en Connect cuando el alumno observa la grabación el tiempo suficiente para cumplir el límite de umbral prescrito. |
| Tiempo de visualización desde Connect | Utiliza el correo electrónico del alumno y la hora de visualización de grabación que captura Adobe Connect. |
| Umbral de criterios de finalización | Marca al alumno como completado para el módulo cuando el tiempo de visualización alcanza el porcentaje establecido en los criterios de finalización. |
| Sólo tiempo de visualización real | Cuenta el tiempo que un alumno vio de verdad. Al arrastrar la barra de búsqueda no se agrega tiempo de inspección. |
| Sincronización programada | Ejecuta una canalización back-end según una programación que controla el administrador de integración y que se puede activar o desactivar. |
| Visibilidad de sala persistente | Muestra el nombre de la sala de Connect en el nivel de instancia para que los autores puedan reutilizar una sala permanente en los distintos días. |

## Cómo funciona el seguimiento de asistencia

*Un alumno que abre la grabación en Learning Manager marca el módulo completado.*

### Flujo de principio a fin

1. El instructor aloja la sesión de clase virtual en directo en Adobe Connect e inicia la grabación. La grabación y la transcripción estarán disponibles después de la sesión.

1. Un alumno que no asistió a la sesión selecciona la grabación para verla. Adobe Connect realiza un seguimiento de la vista automáticamente.

1. Adobe Connect captura el correo electrónico del alumno y el tiempo que este ha dedicado a ver el contenido.

1. En la programación configurada, una canalización de SnapLogic de back-end llama a la API de Adobe Connect y extrae la lista de visores de grabación para un marco de tiempo determinado. El canal utiliza la cuenta de Adobe Connect configurada en Integration Admin.

1. Learning Manager asigna cada visor al curso y módulo coincidentes.

1. Learning Manager compara el tiempo total de visualización del alumno con los criterios de finalización.

1. Si el tiempo de visualización cumple los criterios, Learning Manager marca al alumno como completado para el módulo. En el back-end, Learning Manager lo registra rellenando el archivo CSV de cursos de usuarios.

>[!NOTE]
>
>Adobe Connect no envía datos a Learning Manager. Learning Manager lo extrae a nivel de instancia de Adobe Connect, por ejemplo, &quot;estos cinco usuarios han visto estas seis grabaciones en las últimas 24 horas&quot;. Por lo tanto, la asistencia se actualiza después de la siguiente ejecución de la canalización, no en el momento en que el alumno finaliza la visualización.

### Criterios de finalización y tiempo de visualización

El alumno debe ver al menos el porcentaje de la grabación que definen los criterios de finalización. Tenga en cuenta estas reglas:

* El porcentaje se aplica a la duración de la grabación, no a la duración de la sesión programada. Si se graba una sesión de 15 minutos durante sólo 5 minutos, el tiempo requerido se basa en los 5 minutos. Adobe Connect proporciona la duración de la grabación.

* El porcentaje se establece en el lado de Learning Manager. Es una configuración común en toda la cuenta, no una configuración para cada instancia. El mismo tipo de configuración ya se aplica a las sesiones en directo; por ejemplo, requiere una participación del 80 %.

* Adobe Connect registra el tiempo que el alumno ha estado observando. Saltar a la barra de búsqueda no cuenta y Learning Manager procesa el tiempo de inspección que pasa en Connect.

| Criterios de finalización | Longitud de grabación | Tiempo de visualización necesario | Resultado |
|-------------------------|------------------------------------|-----------------------|-------------------------------------------------------------|
| 50% | 5 minutos | 2,5 minutos | Marcado como completo una vez que se observan 2,5 minutos. |
| 50% | 5 minutos (la sesión duró 15 minutos) | 2,5 minutos | Según la grabación de 5 minutos, no la sesión de 15 minutos. |
| 0% | Cualquiera | Ninguna más allá de la apertura | Abrir la grabación es suficiente. |

### Ventana de idoneidad

Learning Manager solo aplica la asistencia basada en grabación hasta la fecha de finalización del objeto de aprendizaje. Si el objeto de aprendizaje no tiene fecha de finalización, Learning Manager utiliza la fecha de finalización del objeto de aprendizaje principal.

### Programar la sincronización

El administrador de integración controla la frecuencia de ejecución de la canalización. La programación puede ser por horas o semanalmente, entre otros intervalos, y el administrador de integración puede activarla o desactivarla. Se utiliza la misma cuenta de Adobe Connect para cada ejecución.

### ¿Qué cambia?

* Cuando un usuario añade la sala permanente creada para el día 1, Learning Manager le concede acceso a esa sala. Después, pueden añadir la misma sala a las sesiones de otros días.
* Learning Manager muestra el nombre de la sala de Connect en el nivel de instancia, en los detalles de la sesión junto a la **URL de clase virtual**.
* En la instancia predeterminada, Learning Manager muestra la configuración de la sala durante la creación del curso.

### Limitaciones y consideraciones

* La asistencia no es en tiempo real, porque Learning Manager extrae los datos según una programación.
* La función solo cubre las sesiones de clase virtual basadas en Connect.
* Debe existir una grabación, por lo que el instructor debe iniciarla durante la sesión en directo.
* La correspondencia de los alumnos se realiza a través de la dirección de correo electrónico que captura Adobe Connect.
* Al arrastrar la barra de búsqueda no se agrega tiempo de inspección.
* La asistencia basada en grabaciones se detiene en la fecha de finalización del objeto de aprendizaje o del objeto de aprendizaje principal.

### Puntos que recordar

* El tiempo de observación debe ser mayor o igual que el porcentaje prescrito (por ejemplo, el 50% de 5 minutos es de 2,5 minutos). El tiempo de visualización no se acumula si el alumno observa repetidamente la sesión, pero sigue siendo inferior al tiempo de visualización prescrito. Sin embargo, el tiempo de visualización se suma incluso si el alumno ve la sesión en diferentes puntos de tiempo por partes y cumple los criterios de umbral. Por ejemplo, si un alumno observa un minuto de la sesión el día 1 y, a continuación, observa otros 1,5 minutos de la sesión al día siguiente desde el punto en el que se fue, el tiempo de visualización se suma. Esto sucede en el lado de Adobe Connect.

* Los criterios de finalización se pueden configurar en el nivel del curso y en el nivel de cuenta. El efecto es el mismo que la participación de la sesión en directo.

* La frecuencia de sincronización predeterminada y el intervalo más corto que el administrador de integración puede establecer es de una hora.

* El ID de correo electrónico del alumno debe ser el mismo en Adobe Learning Manager y Adobe Connect, ya que Adobe Learning Manager redirige al alumno a Adobe Connect con el mismo ID de correo electrónico.

### Preguntas frecuentes

**Q. ¿Tiene que asistir el alumno a la sesión en directo?**
**A.** No. Un alumno que no asista a la sesión en directo puede seguir viéndola durante bastante tiempo para marcarla como asistido.

**Q. ¿Qué cantidad de la grabación debe ver el alumno?**
**A.** Porcentaje en los criterios de finalización, aplicado a la duración de la grabación. Por ejemplo, al 50 %, una grabación de 5 minutos necesita al menos 2,5 minutos de tiempo de visualización.

**Q. ¿Saltar hacia delante en la grabación cuenta?**
**A.** No. Adobe Connect registra el tiempo que el alumno ha visto realmente, por lo que arrastrar la barra de búsqueda no cuenta.

**Q. ¿Se marca la asistencia en cuanto el alumno termina de ver?**
**A.** No. Learning Manager extrae los datos del visor de Adobe Connect según una programación, por lo que la asistencia se actualiza cuando se ejecuta la siguiente canalización.

**Q. ¿Adobe Connect envía los datos a Learning Manager?**
**A.** No. Learning Manager lo extrae. Es un mecanismo de extracción a nivel de instancia de Adobe Connect, no un empujón.

**Q. ¿Cómo sabe Learning Manager qué alumno vio?**
**A.** Adobe Connect captura el correo electrónico del alumno y la hora de visualización de grabación. Learning Manager asigna esto al curso y al módulo.

**Q. ¿Quién controla la frecuencia con la que se ejecuta la sincronización?**
**A.** El administrador de integración establece la programación y puede activarla o desactivarla.

**Q. ¿Se establece el porcentaje de finalización para cada instancia?**
**A.** No. Es una configuración común en toda la cuenta.

**Q. ¿Pueden las sesiones de varios días compartir una sala de Connect?**
**A.** Sí. Los autores pueden reutilizar la sala permanente creada para el día 1 en las sesiones de otros días, y el nombre de la sala aparece en el nivel de instancia en Learning Manager.
