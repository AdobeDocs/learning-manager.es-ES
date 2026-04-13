---
title: Equivalentes y alternativas en Adobe Learning Manager
description: Ofrece una experiencia de aprendizaje impecable y elimina la formación redundante con equivalentes y alternativos en ALM. Esta nueva capacidad permite a los administradores configurar reglas unidireccionales (alternativas) o bidireccionales (equivalentes), en las que, al completar un curso de formación, se concede automáticamente una finalización alternativa a otro
jcr-language: en-us
source-git-commit: e70a3b5a5d1080dc4b3a56aa726c717120c6bfa3
workflow-type: tm+mt
source-wordcount: '3457'
ht-degree: 0%

---


# Alternativas y equivalentes

## Introducción

En muchas organizaciones, los alumnos se encuentran con situaciones de formación en las que diferentes cursos pueden satisfacer legítimamente el mismo requisito. Por ejemplo, ¿cuándo un curso nuevo debe sustituir a uno antiguo? ¿Cuándo debería presentarse un curso más completo para uno más corto o cuándo debería ofrecerse un curso sustituto especial?

La función Cursos alternativos o Ruta de aprendizaje ofrece a ALM una forma formal de decir lo siguiente:

&quot;Si el alumno ha completado este curso de formación, asígnele el trato de que cumple los requisitos de formación relacionados.&quot;

La función funciona en todos los cursos y rutas de aprendizaje, garantiza que se cumplen los requisitos descendentes, como los requisitos previos y las reglas de cumplimiento, y lo hace sin obligar a los alumnos a pasar por contenido redundante. También mantiene la precisión de los informes al registrar lo que se completó directamente frente a lo que se satisfizo a través de una alternativa.

Básicamente, la función introduce el concepto de finalización alternativa: un estado de finalización especial creado automáticamente cuando un alumno finaliza un curso de origen configurado que cuenta para otro curso de destino.

## Relaciones alternativas

Algunas relaciones de formación son bidireccionales, lo que significa que cada curso puede satisfacer los requisitos del otro. En la práctica, se trata de un escenario en el que dos cursos de formación se consideran mutuamente sustituibles. Por el contrario, las relaciones unidireccionales permiten que una formación satisfaga los requisitos de otra, pero no viceversa. ALM modela ambos escenarios utilizando el mismo mecanismo de finalización alternativo subyacente.

* **Relación bidireccional (equivalentes):** Completar cualquiera de los cursos de formación satisface los requisitos del otro.
* **Relación unidireccional:** Completar el entrenamiento A satisface el entrenamiento B, pero completar B no satisface A. Esto es común cuando una versión más reciente o más completa debe contar para un requisito más antiguo, pero no al revés.

Por ejemplo, cuando un curso de superconjunto más completo abarca todo en un curso de subconjunto más sencillo. Completar el superconjunto debe satisfacer el requisito del subconjunto, pero no necesariamente al revés.

Un curso más nuevo y ampliado que debería tener en cuenta un requisito más antiguo.

Un curso diseñado para un público específico (por ejemplo, una variante regional o adaptada a la accesibilidad) que sigue cumpliendo los mismos requisitos que el curso principal.

Una nueva versión mejorada de un curso que la organización desea contar para un requisito anterior, pero la versión anterior no debe contar para el nuevo requisito.

En Alternativas, la relación es normalmente de una forma. Si el curso A es un curso alternativo para el curso B, completar A puede satisfacer el requisito de B, pero completar B no necesariamente satisface A.

Cuando se completa una formación de origen configurada, ALM produce automáticamente una finalización alternativa para uno o más cursos de destino.

## ¿Qué problemas resuelve esto?

Sin alternativas, los administradores y alumnos se enfrentan a varios problemas recurrentes:

* Se solicita con frecuencia a los alumnos que repitan cursos que cubran contenido que ya han completado en una versión o formato diferente.
* La actualización de los programas de cumplimiento es más sencilla porque los administradores pueden reemplazar o reestructurar los cursos de formación sin obligar a los alumnos que hayan completado versiones anteriores a volver a tomar contenido alternativo o reemplazado.
* La lógica de los requisitos previos es rígida. Si un camino requiere un curso en particular como prerrequisito, no hay una manera limpia de reconocer que otro entrenamiento es lo suficientemente bueno.
* La presentación de informes y las auditorías son más difíciles. No hay ninguna señal formal que demuestre que se cumplió un requisito mediante una terminación alternativa y no hay una forma directa de rastrear la fuente del crédito.

La función de alternativas soluciona estos problemas de la siguiente manera:

* Evitar el esfuerzo duplicado para los alumnos cuando las alternativas son válidas.
* Permitir a los administradores modificar estructuras de formación (por ejemplo, intercambiar un curso dentro de una ruta) sin interrumpir las finalizaciones de los alumnos que tomaron la versión anterior.
* Permitir que los requisitos previos y las comprobaciones de cumplimiento respeten tanto las finalizaciones directas como las finalizaciones alternativas o equivalentes.
* Anotar claramente, en transcripciones e informes, si una formación se completó directamente o se cumplió a través de una relación alternativa, junto con la cual la formación sirvió como fuente.

## Funcionamiento conceptual de la función

La característica se basa en tres ideas principales: **relaciones**, **finalización alternativa** y **comportamiento descendente**.

### Relaciones entre cursos de formación

Los administradores definen las relaciones entre los cursos y las rutas de aprendizaje. Para cada relación, eligen un origen y uno o más destinos. Un solo curso puede tener hasta 30 objetivos, en función del número de cursos de formación anteriores o relacionados que deba satisfacer.

En el caso de los equivalentes, los administradores pueden hacer que la relación sea bidireccional si desean que ambos cursos de formación se satisfagan mutuamente. En el caso de los alternativos, los administradores normalmente mantienen la dirección unidireccional para reflejar que solo se permiten algunas sustituciones.

Estas relaciones se almacenan en el nivel de formación, no en el nivel de alumno. Una vez configurados y activados, pueden aplicarse   a todas las finalizaciones actuales y futuras de la formación de origen, con sujeción a la configuración de nivel de cuenta*como, por ejemplo, si se activa la finalización retroactiva.

### Finalización alternativa

Cuando un alumno finaliza un curso de origen, ALM examina todas las relaciones alternativas configuradas y, para cada curso de destino relevante, crea un registro de finalización alternativo. Este registro es distinto de una finalización normal:

* Marca el curso de formación de destino para el alumno, pero realiza un seguimiento de que se ha completado mediante alternativas en lugar de directamente.
* Registra qué entrenamiento de origen se utilizó para satisfacer el objetivo.
* Se almacena en una estructura específica para que los informes puedan distinguir entre finalizaciones directas y alternativas.

Los alumnos verán una finalización alternativa aunque no estén inscritos. El informe Transcripciones de alumnos (LT) incluye solo los registros de los cursos de formación en los que se ha inscrito el alumno.

#### Experiencia de la aplicación del alumno para finalizaciones alternativas y equivalentes

Las finalizaciones alternativas aparecen claramente en la aplicación del alumno para que los alumnos puedan comprender claramente cómo se ha satisfecho un requisito de formación, al tiempo que mantienen la coherencia con las transcripciones y los informes.

#### Comportamiento de la tarjeta LO

##### Estado de finalización alternativo

Cuando un alumno finaliza un curso de formación mediante una relación alternativa, la tarjeta de objeto de aprendizaje (LO) muestra un estado distinto que es **Completado mediante alternativo**. Esta distinción visual ayuda a los alumnos a diferenciar entre finalizaciones directas y finalizaciones concedidas mediante relaciones configuradas.

#### Indicador de método de finalización

La tarjeta LO incluye un indicador del método de finalización (por ejemplo, una etiqueta o un icono) para mostrar que la finalización se ha realizado a través de una alternativa. Si posteriormente se revoca una finalización alternativa debido a cambios como la finalización retroactiva o la eliminación del curso de formación de origen, ALM deshará todas las adiciones de interfaz de usuario que realizó para la finalización alternativa. El alumno seguirá sin poder orientar el objeto de aprendizaje según el comportamiento de acceso al catálogo actual.

#### Detalles de transparencia y auditoría

Los alumnos pueden abrir la tarjeta de objeto de aprendizaje para ver detalles adicionales, como los siguientes:

* El curso de origen o la ruta de aprendizaje que concedió la finalización alternativa

Esto garantiza la transparencia.

#### Filtrado y vistas

##### Filtro de método de finalización

La aplicación del alumno proporciona un filtro que permite a los alumnos distinguir entre:

* Completado
* Completado mediante alternativo (filtra los objetos de aprendizaje que solo tienen finalizaciones alternativas). Si un objeto de aprendizaje tiene finalización alternativa y directa, no se incluirá).
* Cuando seleccione **Completado** y **Completado mediante alternativo**, podrá ver todas las finalizaciones

Esto permite a los alumnos comprender rápidamente cómo se cumplieron sus requisitos de aprendizaje.

##### Vistas de transcripción y progreso

El filtro de método de finalización está disponible en las vistas de alumno. Por ejemplo:

* Secciones de seguimiento de progreso y finalización

Estas opiniones indican claramente qué cursos de formación se completaron directamente y cuáles se cumplieron a través de suplentes.

<!--## Configure equivalent courses (complete each other)

Use this workflow to define courses that are **equal in value**, where completing either course should automatically complete the other.

1. Launch ALM and navigate to courses.
2. Select a course to configure.
3. Navigate to the **Alternates** section.
4. Search for and select one or more related courses.
5. For each selected course, enable **Completes each other**.
6. Save the configuration.

**Result**

- ALMm records a **bi-directional equivalence relationship**.
- Either course can act as a completion source for the other.

## Configure alternate courses (superset → subset)

Use this workflow when one course is a **superset** of another and should satisfy completion for the simpler or subset course.

1. Launch ALM and navigate to courses.
2. Select the **superset (primary)** course.
3. Go to the **Alternates** section.
4. Select one or more **alternate (subset)** courses.
5. Leave the relationship as **alternate** (do not enable completes each other).
6. Save the configuration.

**Result**

- Completion flows **one-way** from the source course to the alternate.
- Reverse completion is not applied.

## Apply completion logic after source course completion

Automatically evaluate and apply alternate or equivalent completion once a learner completes a configured source course. ALM:

1. Detects completion of a **source course**.
2. Evaluates configured relationships:
   - Equivalent relationships
   - Alternate relationships
3. For each related course:
   - Marks the course as completed if conditions are met
4. Creates a completion record with method **Alternate**.

**Key system rules**

- Alternate completion:
  - Satisfies prerequisites
  - Allows progress in learning paths and certifications
- Alternate completion does **not** award:
  - Skills
  - Badges
  - Gamification credits

## Record completion in Learning Transcript

Ensure alternate and equivalent completions are clearly distinguishable from direct completions for audit and reporting. ALM:

1. Updates the **Learner Transcript (LT)**.
2. Sets:
   - Completion status = Completed
   - Completion method = **Alternate**
3. Sets completion date equal to the **source course completion date**.

## Enable retroactive completion (optional)

Apply alternate or equivalent completion benefits to learners who completed source courses **before** the relationships were configured.

1. Open **Account-level settings** from Administrator home > Settings > General.
2. Enable **Retroactive completion**.
3. Save the configuration.

ALM:

1. Scans historical learner completions.
2. Applies alternate or equivalent completion where applicable.
3. Updates learner transcripts automatically.

## Enable retroactive incompletion (irreversible)

Revoke previously applied alternate or equivalent completions when relationships are removed or corrected.

1. Open **Account-level settings**.
2. Enable **Retroactive incompletion**.
3. Modify or remove alternate/equivalent relationships.

ALM:

1. Identifies impacted alternate completions.
2. Revokes previously applied alternate or equivalent completions.
3. Updates transcript entries to **Alternate (Revoked)**.-->

### Flujo de principio a fin

**Para alumnos**

1. Vaya a **Mi aprendizaje** o **Cursos completados** en la aplicación del alumno.
2. Revise las tarjetas de aprendizaje para identificar los cursos de formación marcados como **Completados mediante Alternativa**.
3. Abra una tarjeta de objeto de aprendizaje para ver los detalles (en la página Información general ) sobre el curso de formación de origen.
4. Use el filtro para seleccionar **Directo**, **Alternativo** o **Todo**.
5. Revise la lista actualizada en función del método de finalización seleccionado.

**Para administradores y autores**

* Configure relaciones alternativas entre cursos o rutas de aprendizaje en la interfaz de administración.

## Comportamiento retroactivo de finalización e infinalización

ALM admite la finalización retroactiva y la finalización retroactiva para garantizar que las relaciones alternativas sigan siendo precisas a lo largo del tiempo, incluso cuando las relaciones se modifican o eliminan después de que los alumnos hayan completado la formación.

### Finalización retroactiva

#### Definición

Cuando se habilita la finalización retroactiva, los alumnos que completaron un curso de origen en el pasado reciben automáticamente una finalización alternativa para el curso de destino si se crea una relación alternativa más adelante. Esto garantiza que el aprendizaje histórico se respete sin que los alumnos tengan que volver a recibir formación.

#### Cómo funciona

1. Un administrador permite la finalización retroactiva en el nivel de cuenta.
2. El administrador define una relación alternativa entre una formación de origen y de destino.
3. El sistema analiza los registros de finalización históricos para la formación de origen.
4. Los alumnos que cumplen los requisitos obtienen una finalización alternativa para el curso de formación de destino.
5. Estos registros aparecen como **Completado mediante alternativo** en informes y transcripciones de alumnos.

>[!NOTE]
>
>Cuando la finalización retroactiva está activada, se aplica solo a las relaciones que se crean posteriormente. No se aplica a las relaciones que ya existían antes de que se habilitara el ajuste retroactivo.

### Incumplimiento retroactivo

#### Definición

Cuando se activa la finalización retroactiva, se revocan las finalizaciones alternativas si se elimina la relación alternativa subyacente o si se elimina el curso de formación de origen.
Esto garantiza que el sistema refleje las relaciones de formación actuales y válidas.

#### Cómo funciona

1. Un administrador habilita la infinalización retroactiva en el nivel de cuenta.
2. El administrador elimina una relación alternativa o el curso de formación de origen.
3. El sistema identifica a los alumnos que han recibido una finalización alternativa a través de la relación afectada.
4. Se revocan los registros de finalización alternativos correspondientes.
5. Los registros revocados se marcan como **Alternativos (revocados)** en transcripciones e informes para la visibilidad de la auditoría.

#### Incidencia en los requisitos previos

Las finalizaciones alternativas, incluidas las concedidas retroactivamente, se tratan como finalizaciones válidas al evaluar los requisitos previos. Si un alumno tiene **Completado mediante alternativo**, se le permite continuar con los cursos que requieren el entrenamiento de destino.

Si posteriormente se revoca una finalización alternativa mediante finalización retroactiva, el alumno puede dejar de cumplir los requisitos de los cursos que dependen de ese requisito previo. Si el alumno no ha iniciado el objeto de aprendizaje dependiente/subsiguiente, se restablecerá la elegibilidad administrada por el objeto de aprendizaje de origen. Si el alumno ya ha iniciado o completado un objeto de aprendizaje dependiente/subsiguiente, no se producirá ningún impacto.

#### Impacto en las rutas de aprendizaje y las certificaciones

Las finalizaciones alternativas contribuyen a la finalización de rutas de aprendizaje y certificaciones perpetuas. Los alumnos pueden avanzar o completar estos programas cuando se cumplan los cursos de formación necesarios mediante relaciones alternativas.

Si se revoca una finalización alternativa, las certificaciones o rutas de aprendizaje afectadas pueden perder el progreso hasta que se cumpla el requisito mediante una finalización válida.

### Flujo de trabajo integral

#### Activación de la finalización o infinalización retroactivas

1. Los administradores pueden acceder a la configuración de la cuenta y activar la finalización retroactiva o la finalización retroactiva.
2. Los administradores pueden crear, modificar o eliminar relaciones alternativas entre los cursos de formación.

#### Acciones del sistema

* **Para la finalización retroactiva**:
El sistema concede finalizaciones alternativas basadas en finalizaciones de fuentes históricas.
* **Por finalización retroactiva**:
El sistema revoca las finalizaciones alternativas cuando se eliminan relaciones o se eliminan cursos de formación de origen.

#### Experiencia del alumno

Los alumnos ven estados de finalización actualizados en las tarjetas de objetos de aprendizaje y en las transcripciones, como:

* **Completado a través de Alternate**

Cuando se revoca una finalización alternativa, no se muestra ninguna etiqueta en la IU del alumno. En los informes y transcripciones, los métodos de finalización aparecen como:

* Alternativas
* Alternativas (revocado)
* Directo

Las comprobaciones de requisitos previos, el progreso de la ruta de aprendizaje y el estado de certificación se actualizan dinámicamente en función del estado de finalización actual.

Los objetos de aprendizaje ordenados se desbloquean dinámicamente según una finalización alternativa.

Las aptitudes, insignias, puntos de interacción o comentarios no se otorgarán a los alumnos al finalizar de forma alternativa los objetivos.

#### Informes y auditoría

Todos los cambios retroactivos se reflejan en el informe Transcripciones de aprendizaje (LT). Una vez eliminado el origen, la transcripción del alumno puede seguir mostrando un ID de formación de origen junto a **Alternativa revocada**. Los informes distinguen claramente entre finalizaciones directas, finalizaciones alternativas y finalizaciones alternativas revocadas para respaldar el cumplimiento, apoyar las investigaciones y las auditorías.

El informe de inscripción deja el campo Origen de finalización en blanco en el caso de la finalización directa, mientras que la transcripción del alumno muestra el correo electrónico y el tipo del mismo.

Cuando se elimina un destino del origen (o se elimina el origen en sí), es posible que el informe de inscripción no muestre el mismo estado **Alternativo o Alternativo (Revocado)** que el mostrado en la transcripción del alumno.

Incluso cuando   Las **alternativas** están deshabilitadas, las entradas históricas en las filas **Auditoría de contenido** o **Inscripción** pueden seguir mostrando actividad relacionada con las alternativas.

La fecha de finalización puede preceder a la fecha de inscripción cuando se complete un objeto de aprendizaje mediante una ruta alternativa **antes** de que el alumno se inscriba realmente. Dado que se pueden producir finalizaciones alternativas independientemente del estado del alumno (**Inscrito**, **No inscrito** o **En curso**), los alumnos pueden completar el objeto de aprendizaje primero e inscribirse solo en el curso de destino más adelante.

## Consecuencias de retirar y eliminar la formación de origen en alternativas

El estado del ciclo de vida de un curso de formación de origen (retirado o eliminado) afecta directamente al modo en que se mantienen las finalizaciones alternativas para los alumnos. ALM maneja estos escenarios de manera diferente para preservar la precisión histórica mientras garantiza que las relaciones actuales sigan siendo válidas.

### Retirar formación de origen

#### Definición

Al retirar un curso, este no está disponible para nuevas inscripciones y, al mismo tiempo, lo mantiene en el sistema con fines de referencia histórica, informes y auditoría.

#### Consecuencias

* Las finalizaciones alternativas existentes concedidas a través del curso de origen retirado siguen siendo válidas.
* Los alumnos que hayan completado anteriormente el curso de origen seguirán realizando una finalización alternativa para el curso de destino.
* No se generan nuevas finalizaciones alternativas a partir del curso retirado, ya que los nuevos alumnos no pueden completarlo.
* Las transcripciones de alumnos y los informes siguen mostrando **Completado mediante alternativo** para los alumnos afectados.

### Eliminar formación de origen

#### Definición

Al eliminar un curso, se elimina por completo del sistema, incluidos sus registros de finalización y las relaciones configuradas.

#### Consecuencias

* Si se elimina un curso de formación de origen, el estado puede cambiar a **Alternativo (revocado)**. La retirada de un objeto de aprendizaje no activa este estado.
* Si se activa la finalización retroactiva, se revocan todas las finalizaciones alternativas concedidas a través del curso de origen eliminado.
* Las transcripciones de alumnos y los informes se actualizan para mostrar **Alternativa (revocada)** para la visibilidad de la auditoría y el cumplimiento normativo.
* La finalización de las rutas de aprendizaje y la disponibilidad de los certificados no se ven afectadas.
* No se pueden conceder más finalizaciones alternativas del curso eliminado.

#### Flujo de trabajo

1. Un administrador retira o elimina el curso de origen mediante la interfaz de administración.
2. El sistema evalúa todas las finalizaciones alternativas derivadas del curso de origen.
3. El estado de finalización se actualiza en función del estado del curso:
   * **Retirado:** Las finalizaciones alternativas existentes no cambian.
   * **Eliminado:** Las finalizaciones alternativas se revocan si está habilitada la infinalización retroactiva.
4. Las transcripciones de alumnos y los informes reflejan el estado actualizado para cumplir los requisitos de cumplimiento y auditoría.

## Sin encadenamiento de relaciones

ALM no admite el encadenamiento de relaciones alternativas. Las finalizaciones alternativas se conceden solo para relaciones configuradas directamente y no se aplican en cascada en varios niveles de cursos.

### Concepto: no encadenar relaciones

#### Definición

El encadenamiento se refiere a permitir que las relaciones alternativas se propaguen a través de varios cursos. Por ejemplo, si el curso A es una alternativa para el curso B y el curso B es una alternativa para el curso C, el encadenamiento implicaría que la finalización del curso A otorga la finalización del curso C.

#### Política

No se admite el encadenamiento. Las relaciones alternativas y equivalentes solo se evalúan en un solo nivel. Completar un curso de origen concede la finalización alternativa solo a su curso o cursos de destino inmediato, no a ningún destino descendente.

### Flujo de trabajo

#### Configuración de relaciones

Un administrador define relaciones alternativas entre cursos, como:

* Curso A → Curso B
* Curso B → Curso C

#### Evento de finalización

Un alumno completa directamente el curso A.

#### Acción del sistema

* El sistema concede una finalización alternativa para el curso B, si se ha definido la relación A → B.
* El sistema no concede una finalización alternativa para el curso C, incluso si existe una relación entre B y C.

#### Requisito de finalización directa

Para recibir una finalización alternativa del curso C, el alumno debe:

* Completar directamente el curso B, o
* Complete un curso configurado explícitamente como alternativa directa o equivalente para el curso C.

## Implicaciones

### Sin beneficios indirectos

Los alumnos no pueden recibir créditos de finalización para cursos que se encuentran más abajo en una cadena de relación a menos que se complete cada curso (o su alternativa directa). Esto garantiza que los requisitos de aprendizaje se cumplan de forma explícita y predecible.

### Auditoría e informes simplificados

Los informes y las transcripciones de alumnos muestran finalizaciones alternativas solo para relaciones directas. Esto evita pistas de auditoría complejas y de varios saltos y garantiza la claridad al revisar cómo se concedió una finalización.

## Uso compartido de catálogos con cuentas de igual a igual: relaciones no compartidas

El uso compartido de catálogos permite que los objetos de aprendizaje se compartan entre cuentas de igual a igual, pero las relaciones alternativas y equivalentes se administran independientemente dentro de cada cuenta y no se comparten.

### Concepto: uso compartido de catálogos y relaciones

#### Uso compartido de catálogos

Las cuentas pueden compartir catálogos con cuentas de igual a igual para proporcionar acceso a cursos, rutas de aprendizaje y otros objetos de aprendizaje en las cuentas.

#### Relaciones no compartidas

Las relaciones alternativas, equivalentes y de finalización alternativa configuradas en la cuenta de origen no se comparten ni replican cuando se comparte un catálogo. Cada cuenta mantiene y evalúa sus propias relaciones de forma independiente.

### Flujo de trabajo

#### Uso compartido de catálogos

Un administrador de **Cuenta A** comparte un catálogo que contiene objetos de aprendizaje con **Cuenta B**.

#### Configuración de relaciones

La cuenta A puede tener relaciones alternativas definidas entre los objetos de aprendizaje del catálogo compartido.

#### Acceso a cuentas de igual a igual

La cuenta B recibe acceso a los objetos de aprendizaje compartidos, pero no hereda ninguna relación alternativa configurada en la cuenta A.

#### Gestión independiente

Si la cuenta B requiere un comportamiento alternativo similar, un administrador de la cuenta B debe configurar manualmente las relaciones dentro de esa cuenta.

#### Implicaciones

##### Sin propagación automática de relaciones

Las relaciones alternativas no están disponibles automáticamente en las cuentas de igual a igual mediante el uso compartido de catálogos.

##### Se requiere configuración manual

Cada cuenta de igual a igual es responsable de definir y administrar sus propias relaciones para los objetos de aprendizaje compartidos.

##### Consideraciones de coherencia

El comportamiento de finalización, la satisfacción de los requisitos previos y la generación de informes pueden diferir entre cuentas a menos que las relaciones se alineen intencionadamente mediante la configuración manual.

## Comportamiento descendente

Una vez que existe una finalización alternativa para un curso de formación de destino, ALM la utiliza en las comprobaciones descendentes:

* Si el curso de formación de destino es un **requisito previo** para otros cursos de formación, el alumno cumple los requisitos para recibir esos cursos de formación como si hubiera completado el curso de formación de destino.
* Si el destino es un **curso obligatorio en una ruta de aprendizaje**, la lógica de finalización de la ruta puede tratar al alumno como que ha completado esa parte y proceder a marcar la ruta como completada cuando se cumplan otras condiciones.
* El cumplimiento normativo y otros paneles, como el panel de éxito de grupo, que dependen de si se cumple un requisito de formación pueden incluir alumnos que solo tienen finalizaciones alternativas.

El sistema distingue entre finalización real y finalización alternativa de modo que:

* Si más tarde el alumno realiza directamente el curso de formación de destino y lo completa, esta finalización directa puede anular la necesidad de la finalización alternativa.
* Si se elimina o se cambia la relación entre el origen y el destino, ALM puede eliminar las finalizaciones alternativas sin tocar las finalizaciones genuinas, siempre que se habiliten las finalizaciones retroactivas para la cuenta.

Las finalizaciones alternativas están diseñadas para no interferir con la actividad real del alumno en el curso de formación de destino. Actúan como una superposición que se puede revisar si cambian las relaciones.

## Correos electrónicos y notificaciones

En cuanto un alumno termine un curso, este recibirá una notificación en la aplicación y un correo electrónico en el que se indica el estado del curso y cómo se ha completado, si se ha completado mediante un curso alternativo.

>[!NOTE]
>
>La finalización alternativa puede seguir activando notificaciones para los objetos de aprendizaje de destino en los catálogos en los que el alumno no puede ver. Es posible que las notificaciones de finalización/infinalización alternativas no aparezcan de la misma manera en la aplicación envolvente para dispositivos móviles que en cualquier otra parte.

## Añadir un curso alternativo

Como administrador, puede añadir cursos y rutas alternativos para que los alumnos tengan varias opciones para completar sus cursos y rutas.

1. Vaya a la sección **Aprendizaje** > **Cursos**. Aparecerá una lista de los cursos disponibles.
   ![](assets/ALM-courses-main.png)
   *Lista de cursos*
2. Vaya al curso para el que desee añadir un curso alternativo.
   ![](assets/ALM-course-single.png)
   *Agregar un curso alternativo a un curso*
3. Vaya a la sección **Administrar** > **Rutas/Cursos alternativos**.
   ![](assets/ALM-alt-train-paths.png)
   *Rutas/cursos de formación alternativos*
4. Seleccione **Agregar cursos/rutas**. Aparecerá una lista de los cursos disponibles.
   ![](assets/ALM-alt-courses-list.png)
   *Lista de cursos disponibles*
5. Seleccione los cursos que desea marcar como **Alternativos** seleccionando la casilla de verificación de cada curso en la parte superior izquierda del icono.
   ![](assets/ALM-alt-courses-added.png)
   *Agregar curso alternativo*
6. Seleccione **Agregar**.

   >[!NOTE]
   >
   >En este punto, puede eliminar los cursos alternativos si lo desea. Para eliminar los cursos alternativos, seleccione **Eliminar curso alternativo** junto a cada curso a la derecha.

7. Seleccione **Guardar**. Los cursos alternativos se han guardado.

El progreso no se ve afectado por la finalización alternativa. Cuando se completa un curso o una ruta de aprendizaje mediante una finalización alternativa, el alumno puede seguir accediendo a él y consumirlo directamente para reforzar el aprendizaje y obtener beneficios descendentes (por ejemplo, puntos de interacción). En estos casos, el estado de progreso refleja el progreso real del alumno desde el consumo directo, independientemente del estado de finalización alternativo. También recibirá una notificación en la aplicación y una notificación por correo electrónico sobre la finalización a través de una alternativa.

Hay varias ventajas de esta finalización, que se enumeran a continuación:

* Esto se considera finalización como parte del proceso de aprendizaje en el que está presente.
* Esto también abre cualquier otro curso o ruta vinculados.

## Configuración para usuarios avanzados

Los siguientes ajustes permiten a los usuarios avanzados utilizar finalizaciones e infinalizaciones retroactivas.

1. Vaya a la sección **Configurar** > **Configuración** > sección **Conceptos básicos** > **General** > **Ruta/curso alternativo**.
2. Seleccione **Activar finalizaciones retroactivas** y **Activar finalizaciones retroactivas** o solo una de las dos según sus necesidades.
   ![](assets/ALM-alt-train-paths-settings-powerusers.png)
   *Activar finalización retroactiva o infinalización*

## Informes de transcripciones de alumnos

La forma en que un alumno completa un curso o una ruta se captura en el informe de transcripciones de alumnos. Se capturan los siguientes escenarios:

1. Cuando un alumno finaliza un curso directamente sin optar por un curso alternativo, se refleja en el informe de transcripciones de alumnos
2. Cuando un alumno completa un curso alternativo, se refleja en el informe de transcripciones de alumnos
3. Cuando se revocan todas las finalizaciones alternativas debido a una infinalización retroactiva y a la eliminación de relaciones, esto se refleja en el informe de transcripciones de alumnos.
