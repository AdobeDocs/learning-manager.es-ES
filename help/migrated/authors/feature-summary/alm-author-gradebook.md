---
description: Configura la puntuación ponderada para los alumnos en el libro de calificaciones, de forma que la finalización del curso se pueda vincular a la consecución de un umbral mínimo de puntuación.
jcr-language: en_us
title: Libro de calificaciones para autores
source-git-commit: 0f7f42d18c81d18b6f6592a90f9322f0cd9dcce4
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---


# Libro de calificaciones para autores

## Configurar el libro de calificaciones de un curso

Configure la puntuación ponderada para un curso en Adobe Learning Manager de forma que cada alumno reciba una puntuación agregada calculada a partir del rendimiento de su módulo y que la finalización del curso se pueda vincular a la consecución de un umbral de puntuación mínimo.

El libro de calificaciones se configura en el nivel del curso al crear un curso nuevo. No se puede añadir a un curso publicado existente.

>[!NOTE]
>
>Para que los alumnos vean el Libro de calificaciones en un curso, un administrador debe habilitar primero la **visibilidad del Libro de calificaciones** en el nivel de cuenta.

### Habilitar libro de calificaciones para un curso

* Inicie sesión en Adobe Learning Manager como autor.
* En la barra de navegación izquierda, selecciona **Cursos** y, a continuación, selecciona **Agregar** para crear un curso nuevo.
* Introduzca el nombre del curso, la descripción y otros detalles necesarios.
* En la sección **Módulos**, busque el conmutador **Gradebook**.

  ![](assets/image_0003.png)

* Seleccione el conmutador **Gradebook** para habilitarlo. Debajo aparecen dos opciones. Ambos están activados de forma predeterminada:
  * **Mostrar libro de calificaciones a los alumnos:** alumnos ven una pestaña **Libro de calificaciones** en el reproductor del curso que muestra sus puntuaciones del módulo, el desglose del peso y el resultado agregado. Desactive esta opción para calcular las notas internamente sin exponerlas a los alumnos.
  * **Incluir módulos que no contribuyan a la calificación final:** módulos no puntuables (PDF, vídeo, audio y similares) aparecen en el libro de calificaciones. Los módulos no puntuables no contribuyen a la puntuación final del alumno.

### Añadir módulos y asignar grosor

Después de activar el libro de calificaciones, agregue sus módulos de contenido y asigne un porcentaje de ponderación a cada módulo puntuable. Los porcentajes de grosor deben sumar exactamente 100 para poder guardar la configuración.

* Seleccione **Agregar módulos**.
* En el selector de módulos, seleccione los módulos que desee agregar y seleccione **Agregar**. Los módulos aparecen en la sección **Contenido**. Los módulos puntuables, SCORM, contenido de Captivate, AICC, xAPI, cuestionarios nativos, módulos de actividad, sesiones de clase y sesiones de clase virtual muestran un campo de entrada **Weightage**. Los módulos no puntuables muestran un guión en la columna de grosor.
* Escriba un valor de porcentaje en el campo **Grosor** para cada módulo puntuable. Un indicador de **grosor total** se actualiza a medida que escribe y debe alcanzar exactamente el **100%** para poder guardar.

  ![](assets/image_0004.png)

* Para módulos con varios tipos de entrega: el grosor solo se puede asignar si **todos los** tipos de entrega del módulo admiten puntuación. Si un tipo de entrega no admite la puntuación, no se puede ponderar todo el módulo.

>[!NOTE]
>
>La escala de puntuación no tiene por qué coincidir en todos los tipos de entrega. Una sesión de clase con una puntuación de 100 y un módulo SCORM con una puntuación de 10 pueden coexistir en el mismo libro de calificaciones. La fórmula normaliza cada contribución automáticamente.

### Definir la puntuación de aprobado mínima

* En el editor del curso, busque la sección **Criterios para aprobar**.
* En el campo **Puntuación mínima agregada en los módulos**, escriba un porcentaje entre 0 y 100.
* Un valor de **0** significa que el curso se completa únicamente en función de la finalización del módulo requerido, sin umbral de puntuación total.
* Cualquier valor por encima de 0 significa que el alumno debe completar los módulos necesarios Y alcanzar o superar esta puntuación total.
* En el campo **Módulos obligatorios**, escriba el número requerido o selecciónelo en el menú desplegable.

  ![](assets/image_0005.png)

* Seleccione **Guardar**.

Los alumnos pueden ver la puntuación mínima de aprobado en la pestaña **Libro de calificaciones** para que sepan cuál es el umbral antes de empezar.

### Configurar los ajustes de puntuación para módulos con varios intentos {#configurescoresettingsmultipleattempts}

Cuando un módulo permite varios intentos, elija la puntuación de intentos que se utilizará en el cálculo del Libro de calificaciones.

* En el editor del curso, busque un módulo que tenga varios intentos habilitados.

  ![](assets/image_0006.png)

* Localice la configuración de **Puntuación que se va a usar** junto a ese módulo.
* Seleccione **Más reciente** o **Más alto**:
  * **Último:** siempre se usa la puntuación de intento más reciente. Una puntuación más baja en un intento posterior reemplaza a una puntuación más alta anterior.
  * **Máxima:** Se conserva la mejor puntuación de cualquier intento. Una puntuación más baja en un intento posterior no reduce la puntuación almacenada.

    ![](assets/image_0007.png)

* Seleccione **Guardar**.

### Curso de Publish

Después de configurar todos los ajustes del Libro de calificaciones, publique el curso mediante el flujo de trabajo estándar. Seleccione **Guardar** y, a continuación, seleccione **Publish** para que el curso esté disponible para los alumnos.

### Prácticas recomendadas

* Asigne un grosor que refleje la importancia relativa de cada módulo. Otorgue porcentajes más altos a los módulos más críticos para el objetivo de aprendizaje.
* Habilita **Mostrar libro de calificaciones a los alumnos** a menos que haya una razón específica para ocultar las calificaciones. Los alumnos que pueden ver su peso y su nota de rendimiento están mejor posicionados para priorizar su esfuerzo.
* Establezca la puntuación de aprobado mínima antes de que los alumnos se inscriban. Cambiarlo después de las inscripciones activas puede afectar a las finalizaciones en curso.
* Utilice **Máximo** para la configuración de varios intentos cuando los módulos sean evaluaciones que los alumnos deben reintentar. Utilice **Último** cuando desee capturar el nivel de conocimiento actual en lugar de obtener el mejor rendimiento.
* Compruebe que el indicador **Peso total** muestra exactamente el 100 % antes de guardar.
