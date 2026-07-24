---
description: Imparte un curso a varias audiencias controlando qué módulos ve cada alumno y cuáles son necesarios en función de los grupos de usuarios a los que pertenezcan.
jcr-language: en_us
title: Cursos adaptables en Adobe Learning Manager
contentowner: mmanuel
source-git-commit: ffaf107e8077b6a6270fa2f8afc76e721d393702
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 0%

---


# Cursos adaptables en Adobe Learning Manager

Los cursos adaptables de Adobe Learning Manager permiten impartir un curso a varias audiencias controlando los módulos que ve cada alumno y los que son necesarios, en función de los grupos de usuarios a los que pertenecen.

En lugar de crear cursos independientes para cada función, región o perfil de cumplimiento, un único curso adaptable presenta dinámicamente el contenido adecuado al alumno adecuado.

## ¿Qué problema resuelven los cursos adaptativos?

Las organizaciones que capacitan a grandes y diversos trabajadores se enfrentan a un desafío común: la privacidad de los datos, la ética en el lugar de trabajo y la seguridad deben llegar a los alumnos con diferentes funciones, ubicaciones u obligaciones de cumplimiento.

Eso crea duplicación: los autores mantienen varios cursos casi idénticos, los informes están fragmentados y, cuando cambia el contenido principal, cada copia debe actualizarse.

Un curso adaptable resuelve este problema permitiendo a los autores configurar reglas de visibilidad y finalización en el nivel de módulo, vinculadas a grupos de usuarios. Un curso sirve a todas las audiencias simultáneamente.

### Escenarios comunes

- Un curso de cumplimiento tiene un módulo principal para todos los empleados, además de módulos de adición específicos de la jurisdicción. Cada alumno ve solo los complementos que se aplican a su ubicación.
- Un curso de contratación de nuevos empleados muestra distintos módulos a los empleados, gestores y contratistas. Cada función ve solo lo que es relevante para ellos.
- Un curso de seguridad añade un nuevo módulo obligatorio a mediados de año. Los administradores activan una finalización de la actualización, por lo que todos los alumnos completados anteriormente deben realizar el nuevo módulo para seguir cumpliendo con las normativas.

### Ejemplo real

Una organización lanza un curso de cumplimiento obligatorio a toda su plantilla. El curso consta de siete módulos:

- Se aplican dos módulos a todos los empleados.
- Dos módulos se aplican solo a los gestores de personal.
- Dos módulos se aplican solo a colaboradores individuales con funciones técnicas.
- Un módulo sólo se aplica a los directores superiores y superiores.

## Cómo funcionan la visibilidad y la finalización del módulo

Cada módulo de contenido de un curso adaptable tiene dos configuraciones:

**Visible para:** grupos de usuarios que pueden ver el módulo. Los alumnos de estos grupos ven el módulo en el curso y pueden acceder a él, pero no cuenta para la finalización a menos que también estén en **Obligatorio para**.

**Obligatorio para:** grupos de usuarios para los que se requiere el módulo para completar el curso. Un módulo enumerado en **Obligatorio para** está visible automáticamente para esos grupos; no es necesario agregar los mismos grupos a ambas configuraciones.

Un módulo se encuentra en uno de los tres estados para cualquier alumno en cualquier momento:

| Estado | ¿Cómo se determina? | ¿Cuenta hacia la finalización? |
|---|---|---|
| Obligatorio | El alumno está en un grupo de usuarios en **Obligatorio para** | Sí, debe completarse |
| Opcional | El alumno está en un grupo bajo **Visible para** pero no **Obligatorio para** | No: visible y accesible, pero no obligatorio |
| Oculto | El alumno no está en ningún grupo bajo ninguna de las opciones | No visible para el alumno en absoluto. |

## Características de un curso adaptativo

La característica definitoria de los cursos adaptativos es que el curso evalúa el perfil del alumno de forma continua, no solo durante la inscripción.

Cuando el grupo de usuarios de un alumno cambia mientras está inscrito:

- Los módulos que ya no se ven en su nuevo grupo de usuarios desaparecen inmediatamente.
- Si un módulo recién visible es obligatorio para su nuevo grupo de usuarios, se añade al requisito de finalización.
- Si un módulo obligatorio ya no es obligatorio, se elimina de su requisito de finalización.
- Los módulos completados anteriormente permanecen completados. Un cambio de perfil no restablece el trabajo ya realizado.

### Dar de baja automáticamente

Si un cambio de grupo de usuarios elimina todos los módulos obligatorios de un alumno, este se dará de baja automáticamente del curso.

### Finalización automática

Si un cambio de grupo de usuarios elimina todos los módulos obligatorios incompletos restantes de un alumno en curso, el curso se completa automáticamente para ese alumno.

Si un cambio de perfil da como resultado nuevos módulos obligatorios que el alumno no ha completado, un administrador puede activar una finalización de actualización para revertir la finalización existente y solicitar al alumno que complete los nuevos módulos.

## Qué se adapta y qué sigue siendo lo mismo

Las reglas adaptables se aplican solo a **módulos de contenido**. Lo siguiente se aplica a todos los alumnos inscritos, independientemente del grupo de usuarios:

- **Módulos previos al trabajo:** Se muestran a todos los alumnos antes de que comience el contenido principal.
- **Módulos de prueba:** Disponibles para todos los alumnos; completar una prueba finaliza el curso independientemente del estado del módulo de contenido.
- **Recursos y ayudas de trabajo:** visibles para todos los alumnos inscritos en todo momento.

## Disponibilidad de funciones

La función de curso adaptable se controla mediante un indicador de nivel de cuenta de dos niveles. Póngase en contacto con el equipo de la cuenta de Adobe para habilitar esta función para su cuenta.

Una vez habilitado el indicador de cuenta:

- Hay disponible un conmutador **Reglas de finalización y visibilidad** al crear o editar un curso.
- Al activar el conmutador se activa el panel de configuración adaptable.

**Precaución:** Habilitar la marca de característica adaptable es **irreversible**. Una vez habilitado en el nivel de cuenta, no se puede deshabilitar.

## Uso compartido de catálogos

Los cursos adaptables se pueden añadir a los catálogos de su cuenta. Cuando un catálogo se comparte externamente en una cuenta de igual a igual, los cursos adaptables se excluyen automáticamente del contenido compartido.

>[!NOTE]
>
>Cuando se comparte externamente una ruta de aprendizaje o una certificación que contiene un curso adaptable, la cuenta receptora ve la ruta de aprendizaje o la certificación en su catálogo, pero el curso adaptable que contiene no aparece. El objeto de aprendizaje no se excluye por completo; solo se elimina el componente curso adaptable de la versión compartida. Los autores de la cuenta de destino deben tener en cuenta que el objeto de aprendizaje compartido puede tener menos módulos que la versión de origen.

## Configuraciones admitidas

| Configuración | ¿Admitido? |
|---|---|
| Curso adaptable en una ruta de aprendizaje habitual | Sí (véase la nota siguiente) |
| Curso adaptable en una ruta de aprendizaje flexible | Sí |
| Curso adaptable en una ruta de aprendizaje adaptable | No |
| Curso adaptable en una certificación | Sí (no recomendado para certificaciones periódicas) |
| Varias inscripciones | No |
| Cambio de instancia | Sí |
| Uso compartido de catálogos (cuenta cruzada) | No |
| Reglas de visibilidad en los módulos previos al trabajo o de prueba | No |
| Reglas de visibilidad en los módulos de contenido principales | Sí |

>[!NOTE]
>
>Cuando se incluye un curso adaptable en una ruta de aprendizaje **ordenada**, los alumnos que no tienen módulos visibles en el curso adaptable, debido a que su grupo de usuarios no coincide con las reglas de visibilidad de ningún módulo, no pueden completar ese curso. En una ruta de aprendizaje ordenada, esto impide que se pueda acceder a todos los elementos posteriores. Para evitar esto, asegúrese de que todos los alumnos inscritos en la ruta de aprendizaje pertenezcan al menos a un grupo de usuarios que tenga visibilidad de al menos un módulo en cualquier curso adaptable de la ruta.

Además, no incruste una ruta de aprendizaje que contenga un curso adaptable dentro de una ruta de aprendizaje de orden superior (anidada). En esta configuración, si un alumno no tiene módulos visibles u obligatorios en el curso adaptable, el reproductor incrustado puede dejar de responder, lo que impide la navegación por el contenido restante. Este comportamiento se abordará en una futura versión.

>[!NOTE]
>
>Cuando un alumno se inscribe automáticamente en un curso adaptable dentro de una ruta de aprendizaje **regular**, debido a que un cambio de grupo de usuarios quitó todos sus módulos visibles, la ruta de aprendizaje principal permanece en estado inscrito. La ruta de aprendizaje no es automática\-darse de baja. El alumno verá la ruta de aprendizaje como inscrito en su transcripción, aunque ya no se pueda acceder al curso adaptable contenido en ella. Si tu caso de uso requiere que la ruta de aprendizaje principal también se dé de baja cuando lo haga el curso adaptable, considera la posibilidad de usar una **ruta de aprendizaje adaptable** en lugar de una ruta de aprendizaje normal para que contenga el curso adaptable.

## Habilitar cursos adaptables para su cuenta

Active el aprendizaje adaptable para que los autores puedan crear cursos que muestren diferentes módulos a diferentes alumnos en función de la pertenencia a grupos de usuarios.

## Antes de habilitar

- **Permanente:** Una vez habilitado, el aprendizaje adaptable no se puede desactivar para la cuenta.
- **Afecta a ambos cursos y rutas de aprendizaje simultáneamente:** El mismo indicador que habilita los cursos adaptables también habilita las rutas de aprendizaje adaptables.
- **Los cursos existentes no se modifican:** Solo los cursos recién creados se pueden adaptar. Ningún curso normal existente se convierte automáticamente.
- **Los autores ven la opción inmediatamente:** Tan pronto como guarde, el tipo de curso adaptable aparece en el flujo de trabajo de creación.
- **Aprovisionamiento en dos niveles:** Si su cuenta se ha aprovisionado para el aprendizaje adaptable, verá la opción habilitada y bloqueada. No se puede cambiar desde la interfaz de usuario. Si no se ha aprovisionado la cuenta, la configuración no está visible en absoluto. Póngase en contacto con el Adobe para solicitar aprovisionamiento.

## Habilitar cursos adaptables

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **Configuración** en el panel de navegación izquierdo.
3. Seleccione **General**.
4. Vaya a la sección **Reglas de visibilidad y finalización**. Si se ha activado el aprendizaje adaptable para su organización, la opción aparecerá como bloqueada, como se muestra a continuación:

![](assets/image_0001.png)

El aprendizaje adaptable ahora está activo para su cuenta. Los autores pueden crear inmediatamente cursos adaptables y rutas de aprendizaje adaptables.

## ¿Qué cambia después de activar?

Después de habilitar el aprendizaje adaptable:

- Los autores ven la opción **Reglas de finalización y visibilidad del contenido** al crear un curso, además del tipo de curso normal existente.
- Cada módulo de contenido de un curso adaptable se puede configurar con reglas **opcionales** y **obligatorias** para grupos de usuarios.
- Los alumnos inscritos en un curso adaptable solo ven los módulos que sus grupos de usuarios hacen visibles.
- Todos los cursos regulares existentes permanecen sin cambios.

## Resolución de problemas

- **La sección Reglas de visibilidad y finalización no está visible en Configuración:** La característica debe estar aprovisionada en el back-end antes de que aparezca el conmutador. Póngase en contacto con el representante de su cuenta de Adobe o con el Soporte técnico de Adobe para solicitar acceso.
- **El conmutador ya está habilitado y aparece bloqueado:** El aprendizaje adaptable estaba habilitado cuando se aprovisionó su cuenta. No es necesario hacer nada. Los autores ya pueden crear cursos adaptables.
