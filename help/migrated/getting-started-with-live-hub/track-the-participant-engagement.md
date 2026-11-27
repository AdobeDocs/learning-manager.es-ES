---
title: Seguimiento de la participación de los participantes
description: Descubre cómo los instructores usan el indicador de participación de los participantes en tiempo real en Live Hub para supervisar el enfoque del navegador, la actividad del chat y la participación en las encuestas.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 5d89078fff50bbd3be1a2d01085efd568b8e0130
workflow-type: tm+mt
source-wordcount: '1408'
ht-degree: 0%
---

# Seguimiento de la participación de los participantes

La participación de los participantes en Live Hub ofrece a los instructores una vista en tiempo real de la participación de los alumnos o participantes durante una sesión en directo. Combina el enfoque del navegador, la actividad del chat y la participación en una encuesta en un solo nivel de participación, que se muestra como un indicador verde, amarillo o rojo. Utilícelo para detectar las caídas de atención y ajustar su entrega en tiempo real.

La participación de los participantes muestra el nivel medio de participación de todos los alumnos de la sala principal en un momento determinado. El nivel se actualiza en cuanto un alumno se une a la sesión.

La participación de los participantes se calcula y se muestra solo durante una sesión en directo.

>[!NOTE]
>
> Solo los instructores pueden ver la participación del participante. Los alumnos no tienen acceso a él.

## Comprensión de los cálculos de nivel de participación

La puntuación de participación de los participantes le ayuda a supervisar la atención del alumno en tiempo real durante una sesión en directo. Esta insignia de participación en la parte superior de la pantalla muestra el nivel general de participación como **Baja**, **Media** o **Alta**, lo que te permite ajustar la entrega de la sesión y fomentar la participación según sea necesario.

El indicador solo está visible para los instructores de la sala principal.

![Indicador de nivel de participación](assets/engagement-level-indicator.png)
*La interfaz de Live Hub muestra la participación del participante en la esquina superior derecha.*

## ¿Cómo se calcula la puntuación de participación?

Cada alumno o participante tiene una puntuación de participación que oscila entre 0 y 100, en función de los siguientes factores:

- **Atención a la sesión**: Cuando un alumno o participante mantiene activa la ventana de la sesión, su nivel de participación es Alto de forma predeterminada. Si cambian a otra ventana o pestaña del navegador, su nivel de participación disminuye a Bajo a menos que continúen participando en las actividades de la sesión.
- **Participación en la sesión**: Actividades como hablar, compartir una pantalla, enviar mensajes de chat, responder a encuestas o cuestionarios, dibujar en la pizarra, levantar una mano, enviar reacciones y hacer clic dentro de la sesión aumentan la puntuación de participación.

### Cómo cambian las puntuaciones de participación

La puntuación de participación del alumno cambia a lo largo de una sesión en directo en función de su atención y participación. Las siguientes condiciones afectan a la forma en que se calcula la puntuación de participación:

- **Duración de la actividad**: La mayoría de las actividades de participación aumentan temporalmente la puntuación de participación, y su contribución disminuye gradualmente en aproximadamente cinco minutos. Por ejemplo, si un alumno habla durante una sesión y, a continuación, cambia a otra ventana, su puntuación de participación se reduce gradualmente en lugar de inmediatamente
- **Uso compartido de pantalla**: La puntuación de participación permanece en 100, mientras que un alumno o un participante comparte la pantalla.
- **Actividades simultáneas**: Cuando un alumno o un participante realiza varias actividades a la vez, solo se tiene en cuenta la actividad con el valor de participación más alto. Las puntuaciones de las actividades individuales no se combinan, lo que garantiza que la puntuación de participación no exceda de 100.
- **Varios dispositivos**: Si un alumno o un participante se une a la sesión desde varios dispositivos, se considera la puntuación más alta de participación en todos ellos.

## Puntuación global de participación

La insignia de participación de los participantes muestra el nivel general de participación en función de la puntuación media de participación de todos los alumnos de la sala principal, redondeada al número entero más próximo.

Se aplicarán las siguientes condiciones al calcular la puntuación de participación global:
- **Instructores y bots de grabación**: Los instructores y los bots de grabación se excluyen del cálculo global de la puntuación de participación. Los bots de grabación no aparecen en la lista de asistentes.
- **Salas para grupos de trabajo**: Los alumnos o participantes de las salas de grupo de trabajo no se incluyen en la puntuación global de participación. Cuando los alumnos se mueven entre la sala principal y una sala de grupo de trabajo, sus puntuaciones de participación individuales se restablecen y se vuelven a calcular en uno o dos minutos.
- **Nuevos alumnos**: La puntuación de participación del participante estará disponible aproximadamente un minuto después de unirse a la sesión. Hasta que la puntuación esté disponible, el alumno o participante se excluye del cálculo de la puntuación de participación global.
- **Sala principal vacía**: Cuando no hay alumnos ni participantes presentes en la sala principal, la insignia muestra la participación del participante sin un nivel de participación.

## Identificar niveles e indicadores de participación

La insignia de participación de los participantes muestra uno de los siguientes niveles de participación en función de la puntuación global de participación. Puede utilizar estos niveles para supervisar la atención del alumno y ajustar la entrega de la sesión según sea necesario.  Esto es lo que significa cada nivel:

| **Nivel de participación** | **Puntuación** | **Descripción** |
|----|----|----|
| Alto | 61 a 100 | Los alumnos participan activamente en la sesión. |
| Medio | 31 a 60 | Los alumnos muestran una interacción ocasional con una participación moderada. |
| Baja | 0 a 30 | Los alumnos muestran una interacción mínima o nula, o un enfoque reducido durante la sesión. |

>[!NOTE]
>
> - La puntuación de participación indica la atención del participante durante una sesión. No mide los resultados del aprendizaje ni el rendimiento.
> 
> - Las puntuaciones de participación se calculan cada minuto. Los cambios pueden tardar hasta dos minutos en aparecer en la insignia de participación.

## Preguntas más frecuentes

+++ ¿La puntuación de participación detecta si un participante está viendo activamente la sesión?

No. La puntuación de participación se calcula en función de si la ventana de la sesión está activa y de las actividades del participante, como hablar, enviar mensajes de chat y responder a las encuestas. No utiliza el vídeo de la cámara, el seguimiento de los ojos ni el estado de silencio del micrófono para medir el compromiso.

+++

+++ ¿Qué sucede cuando un participante se aleja de la ventana de la sesión?

Cuando un participante cambia a otra ficha, ventana o aplicación del explorador, la ventana de sesión deja de considerarse activa. Incluso si la ventana de la sesión permanece visible, se considera inactiva cuando otra ventana está seleccionada.

+++

+++ ¿Contribuyen todas las actividades de participación por igual a la puntuación de participación?

Hablar, compartir la pantalla, enviar mensajes de chat, responder a encuestas o cuestionarios, dibujar en la pizarra, levantar una mano y enviar reacciones contribuyen por igual a la puntuación de participación. Hacer clic dentro de la sesión contribuye un poco menos.

+++

+++ ¿Cómo cambia la puntuación de participación después de una actividad de participación?

La contribución de la mayoría de las actividades de participación disminuye gradualmente en aproximadamente cinco minutos. Por ejemplo, si un participante cambia a otra ventana y luego habla, su puntuación de participación aumenta a 100 en la siguiente actualización. En los minutos siguientes, la puntuación disminuye gradualmente a 80, 60, 40 y 20, donde se mantiene hasta que el participante vuelve a la ventana de la sesión o vuelve a participar.

Un participante que mantiene activa la ventana de sesión mantiene un alto nivel de participación.

+++

+++ ¿Los participantes en las salas de grupo de trabajo están incluidos en la puntuación global de participación?

No. En el cálculo de la puntuación global de participación solo se incluyen los participantes de la sala principal. La insignia de participación no se muestra cuando un instructor está en una sala de grupo de trabajo.

+++

+++ ¿Por qué disminuye la puntuación global de participación después de que finalicen las salas de grupo de trabajo?

Cuando los participantes se mueven de las salas de grupo de trabajo a la sala principal, sus puntuaciones de participación individuales se restablecen y se vuelven a calcular en uno o dos minutos. Esto puede reducir temporalmente la puntuación global de participación.

+++

+++ ¿Cómo se calcula la puntuación de participación cuando un participante se une desde varios dispositivos?

Si un participante se une a la sesión desde varios dispositivos, se considera la puntuación de participación más alta en todos ellos. Una sesión inactiva en un dispositivo no reduce la puntuación de participación registrada en otro dispositivo activo.

+++

+++ ¿Por qué la insignia de participación tarda hasta dos minutos en actualizarse?

La puntuación de participación de cada participante se calcula una vez cada minuto. La puntuación general de participación se actualiza una vez cada minuto, por lo que los cambios pueden tardar hasta dos minutos en aparecer en la insignia de participación.

+++

+++ ¿Qué pueden hacer los instructores cuando la insignia de participación muestra Baja?

Un nivel de participación bajo indica que la mayoría de los participantes han abandonado la ventana de la sesión y no participan activamente. Los instructores pueden utilizar encuestas, cuestionarios, mensajes de chat o preguntas de debate para fomentar la participación y llamar la atención de los participantes de vuelta a la sesión.

+++

+++ ¿Pueden los instructores utilizar puntuaciones de participación para realizar un seguimiento de la asistencia o evaluar a los alumnos?

Las puntuaciones de participación proporcionan una indicación general de la atención y actividad de los participantes durante una sesión. Un participante puede mantener un alto nivel de participación manteniendo activa la ventana de la sesión, incluso sin participar activamente ni demostrar el aprendizaje. Por lo tanto, las puntuaciones de participación pueden no ser adecuadas para evaluar el rendimiento del alumno o realizar un seguimiento de la asistencia.

+++

+++ ¿Pueden ver los participantes sus puntuaciones de participación?

No. La insignia de participación solo está visible para los instructores.

+++

+++ ¿Pueden los instructores ver las puntuaciones de participación de los participantes individuales?

No. La insignia de participación muestra solo la puntuación de participación global de la sala principal. Las puntuaciones de los participantes individuales no están disponibles.

+++

+++ ¿Pueden los instructores deshabilitar el seguimiento de participación?

No. El seguimiento de la participación siempre está habilitado y no se puede deshabilitar.

+++

+++ ¿Las puntuaciones de participación están disponibles en los informes o en el historial de la sesión?

No. La insignia de participación solo muestra la puntuación global de participación actual. Las puntuaciones de participación no se guardan ni se incluyen en los informes ni en el historial de la sesión.

+++

+++ ¿Pueden ver los coinstructores la insignia de participación?

Sí. Los instructores adjuntos también pueden ver la insignia de participación durante una sesión.

+++

+++ ¿Cómo se calculan las puntuaciones de interacción en dispositivos móviles?

Los participantes pueden acceder a las sesiones de Live Hub a través de navegadores móviles. Las puntuaciones de participación se calculan utilizando los mismos criterios que los navegadores de escritorio.

+++
