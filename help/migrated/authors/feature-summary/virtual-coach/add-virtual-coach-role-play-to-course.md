---
description: Aprende a publicar un juego de roles de entrenador virtual como ayuda de trabajo y, después, añádelo a un curso como parte de un recorrido de aprendizaje estructurado
jcr-language: en_us
title: Añadir un juego de roles de entrenador virtual a un curso
exl-id: c33ec5e4-0e96-4452-ada7-d48f9c71a123
source-git-commit: 8bde6827835a7f8cd8cc28f3d2c4014527e4a96c
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%
---

# Añadir un juego de roles de entrenador virtual a un curso

Publish ofrece un juego de roles de instructor virtual como ayuda de trabajo y, a continuación, añádelo a un curso para que los alumnos puedan acceder a él como parte de un recorrido de aprendizaje estructurado.

Los juegos de rol de instructor virtual no se añaden directamente a los cursos. En su lugar, primero publique el juego de roles como una ayuda de trabajo y, a continuación, añada dicha ayuda de trabajo a un curso como un módulo. Este proceso de dos pasos le permite reutilizar el mismo juego de roles en varios cursos sin duplicarlo. Bajo el capó, se añade un juego de roles publicado a su biblioteca de contenido como un módulo LTI, que es cómo se puede implementar como una ayuda de trabajo independiente o un módulo de curso. Antes de empezar, [crea y publica un juego de roles de Entrenador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md) si aún no lo has hecho.

## Agregar el juego de roles como ayuda de trabajo

1. En el panel de navegación izquierdo de la página principal del autor, seleccione **Ayudas de trabajo**.
2. Seleccione **Crear** > **Entrenador virtual** en la esquina superior derecha.
3. Introduzca un nombre y una descripción para la ayuda de trabajo.
4. Selecciona el juego de roles de **Entrenador virtual** que deseas usar en el campo **Buscar y seleccionar Entrenador virtual**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach8.png)
   *Busque y seleccione el juego de roles publicado que desea convertir en una ayuda de trabajo.*

5. Definir visibilidad:
   - Deje la configuración predeterminada de **Compartido** para permitir que otros autores asignen esta ayuda de trabajo a sus cursos.
   - Selecciona **Privado** para restringir el acceso a tus propios cursos.
6. Opcionalmente, introduzca el tiempo de finalización esperado en minutos en el campo **Duración**.
7. En el campo **Etiquetas**, escriba palabras clave para que la ayuda de trabajo sea detectable en la búsqueda y en el catálogo.
8. De forma opcional, asigne aptitudes y niveles de aptitudes. Solo se pueden utilizar las aptitudes que ya existen en su cuenta de Adobe Learning Manager; las aptitudes no se pueden crear desde esta pantalla, por lo que su asignación no es obligatoria.
9. Seleccione **Guardar**. La ayuda de trabajo se publica y está disponible para agregarse a un curso.

## Añadir el juego de roles a un curso

Una vez publicada la ayuda de trabajo, agréguela a cualquier curso como módulo. Los alumnos perciben el juego de roles como parte de la secuencia del curso, junto con otro contenido, como vídeos, documentos o cuestionarios.

1. En el panel de navegación izquierdo de la página principal del autor, seleccione **Cursos**.
2. Abra el curso al que desee agregar el juego de roles o seleccione **Crear** para iniciar un nuevo curso. Si estás abriendo un curso existente, debes seleccionar **Editar** después de que se abra.
3. Añada el nombre y la descripción del curso.
4. Vaya a la sección **Módulos** del editor del curso.
5. Hay tres secciones en las que puede añadir módulos. Cuando quieras seleccionar un entrenador virtual, ve a la primera sección llamada **Content**, selecciona **Add Module** y luego selecciona **Virtual Coach**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach18.png)

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach9.png)
   *Elija Virtual Coach como tipo de módulo para agregar el juego de funciones publicado a un curso.*

6. Busque el juego de roles de Entrenador virtual que ha creado y selecciónelo.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach10.png)
   *Busque la ayuda de trabajo por nombre o etiqueta y, a continuación, seleccione su casilla de verificación para agregarla al curso.*

7. Seleccione **Agregar**.
8. Configure los criterios de finalización y éxito del módulo según el diseño del curso.
9. Seleccione **Volver a publicar** si actualizó un curso existente. Si actualizaste un curso existente, solo verás el botón **Volver a publicar**. Seleccione **Guardar** si ha creado el curso de nuevo. Solo verás el botón **Guardar** si has creado el curso de nuevo. Al hacer clic en el botón **Guardar**, el curso se guardará en la pestaña **Borrador** de la página Catálogo de cursos. Para publicar el mismo curso, ve al mismo curso en la página **Catálogo de cursos**, selecciona los puntos suspensivos y selecciona **Curso de Publish**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach19.png)

>[!NOTE]
>
>Cualquier cambio que realice en la ayuda de trabajo, incluidos los cambios en el contenido del juego de funciones, se reflejará automáticamente en todos los cursos a los que se haya agregado. Si el juego de roles forma parte de una evaluación formal, vuelva a publicar la ayuda de trabajo después de realizar cambios para que los alumnos vean la versión más reciente.

## Empaqueta Virtual Coach como parte de un recorrido de aprendizaje

Virtual Coach está diseñado para funcionar mejor como la &quot;última milla&quot; de formación, el punto en el que los alumnos demuestran que pueden aplicar lo que acaban de aprender, en lugar de una actividad independiente. Empaquete el juego de roles dentro de un curso o un recorrido de aprendizaje junto con el contenido relacionado, y distribuya el vínculo del curso por correo electrónico u otras comunicaciones de administración de cambios para que los alumnos sepan exactamente cuándo y por qué completarlo.

Este enfoque de empaquetado se aplica bien a varios despliegues comunes:

- **Incorporación y actualización de nuevos empleados**, donde el juego de roles sigue el contenido de incorporación y confirma que un nuevo empleado está listo para su primera conversación en vivo.
- **Certificación y refuerzo de ventas**, donde el juego de roles es el punto de control de certificación al final de un curso de capacitación de ventas.
- **Preparación para el lanzamiento de productos**, donde el juego de roles sigue a la formación sobre el lanzamiento y confirma que los representantes pueden posicionar el nuevo producto antes de que salga al mercado; por ejemplo, el escenario de preparación para el lanzamiento de productos descrito en [Qué es Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md), donde un representante debe adaptar su discurso en un comité de compra multipersona.
- **Liderazgo y entrenamiento de gerentes**, donde el juego de roles sigue un curso de habilidades de administración y precede una conversación de rendimiento real.
- **Programas de preparación para partners**, en los que el juego de roles confirma que un partner externo puede representar el producto correctamente antes de que se certifique.
- **Capacitación en administración de cambios y comunicación**, donde el juego de roles refuerza un nuevo proceso o mensaje de reorganización después de que los empleados completen el contenido relacionado.

Una vez que los alumnos puedan encontrar e iniciar el juego de roles, consulta [Practica un juego de roles con Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/practice-role-play-with-virtual-coach.md) para ver lo que experimentarán.
