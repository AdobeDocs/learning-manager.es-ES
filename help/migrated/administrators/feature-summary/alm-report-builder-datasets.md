---
jcr-language: en_us
title: Conjuntos de datos disponibles en Report Builder
description: Guía de referencia de los conjuntos de datos, campos y campos derivados disponibles en Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: b21196a3121c88bf54f33aecc0f4649eceb3ddf6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 28%

---


# Conjuntos de datos disponibles en Report Builder

El Report Builder organiza todas las columnas disponibles en conjuntos de datos, grupos con nombre de campos relacionados. En este artículo se enumeran los conjuntos de datos, se describe su contenido y se indican los conjuntos de datos que se pueden combinar en un único informe.

**Conjuntos de datos en esta versión**

**Conjunto de datos**

**Qué contiene**

**Campos de clave**

**Usuario**

Datos de perfil del alumno para alumnos activos y eliminados

Nombre, correo electrónico, ID de usuario, responsable, campos activos, estado

**Transcripción**

Registros de inscripción y finalización

Fecha de inscripción, fecha de finalización, porcentaje de progreso, estado, puntuación

**Objeto de aprendizaje**

Metadatos de curso, ruta de aprendizaje y certificación

Nombre del objeto de aprendizaje, ID del objeto de aprendizaje, tipo, catálogo, etiqueta del catálogo, estado

**Instancia de objeto de aprendizaje**

Detalles a nivel de instancia para cursos con varias instancias

Nombre de instancia, ID de instancia, límite de inscripción, fecha límite

**Catálogo**

Metadatos de catálogo y pares clave-valor de etiqueta de catálogo

Nombre del catálogo, ID del catálogo, clave de etiqueta y valor de etiqueta. **Las columnas de etiquetas de catálogo están configuradas por el cliente**. Solo aparecen si su cuenta tiene etiquetas de catálogo configuradas. Los nombres y valores de las etiquetas que verá reflejarán su propia configuración.

**Grupo de usuarios**

Pertenencia a grupos de usuarios y jerarquía

Nombre de grupo de usuarios, ID de grupo de usuarios, grupo principal, número de miembros

**Sesión de módulo**

Detalles de la sesión para clase, clase virtual y módulos de aprendizaje electrónico

Id. de sesión, nombre de sesión, nombres de instructor, hora de inicio, hora de finalización, ubicación

Lista de columnas en conjuntos de datos

Widget

* Fecha de creación
* ID
* Nombre

Etiqueta de catálogo

* Widget
* ID
* Nombre
* Valor

Campo personalizado (objeto de aprendizaje)

* Porcentaje de finalización de los objetos de aprendizaje
* Porcentaje de cumplimiento de los objetos de aprendizaje

Campo personalizado (usuario)

* Porcentaje de finalización del usuario
* Porcentaje de cumplimiento del usuario

Objeto de aprendizaje

* Nombres de los autores
* Fecha de retirada automática
* Recuento de finalización
* Fecha de creación
* Duración (minutos)
* Recuento de inscripciones
* Tipo de inscripción
* Formato
* ID
* Cambio de instancia activado
* Última fecha de finalización
* Fecha de la última publicación
* Inscripción múltiple habilitada
* Nombre
* Requisitos previos obligatorios
* Precio
* Crédito de habilidad
* Nivel de aptitud
* Nombre de la aptitud
* Valoración media en estrellas
* Número de valoraciones con estrellas
* Recuento iniciado
* Estado
* Etiquetas
* Tipo
* ID exclusivo

Instancia a objeto de aprendizaje

* Límite de finalización
* Fecha de creación
* Plazo de inscripción
* ID
* Última fecha de finalización
* ID de objeto de aprendizaje
* Nombre
* Estado
* Tipo
* Límite para darse de baja

Módulo

* Hora de finalización del acceso
* Hora de inicio del acceso
* ID de curso
* ID de instancia del curso
* Duración (minutos)
* Hora de finalización
* Recuento de inscripciones
* ID
* Nombre de los instructores
* Ubicación
* Información de ubicación
* Región de la ubicación
* URL de ubicación
* ID de módulo
* Nombre
* Límite de puestos
* Hora de inicio
* Tipo
* Límite de lista de espera

Transcripción (objeto de aprendizaje)

* Fecha de finalización
* Límite de finalización
* Origen de finalización
* Fuente de finalización: ID de usuario
* Fuente de finalización: nombre de usuario
* Fecha de inscripción
* Fuente de inscripción
* Estado de inscripción
* ID de objeto de aprendizaje
* Nombre del objeto de aprendizaje
* ID de instancia a objeto de aprendizaje
* Vencido
* ID del objeto de aprendizaje principal
* Fecha de aprobación
* Porcentaje de progreso
* ID de certificación raíz
* Fecha de inicio
* Estado
* Tiempo empleado (minutos)
* Puntuación más alta del usuario
* ID de usuario
* Puntuación más reciente del usuario

Transcripción (módulo)

* Fecha de finalización
* ID de curso
* ID de módulo
* Nombre de módulo
* Fecha de aprobación
* Porcentaje de progreso
* Puntuación total del módulo de prueba
* Fecha de inicio
* Estado
* Tiempo empleado (minutos)
* Correo electrónico de usuario
* Puntuación más alta del usuario
* ID de usuario
* Puntuación más reciente del usuario
* Nombre de usuario

Usuario

* Adobe ID
* Idioma del contenido
* Fecha de creación
* Fecha de eliminación
* Número de miembros del equipo directo
* Correo electrónico
* ID
* Idioma de la interfaz
* Es administrador
* Es autor
* Es función personalizada
* Es instructor
* Es administrador de integración
* Es alumno
* Es responsable
* Es usuario raíz
* Último acceso
* Correo electrónico del responsable
* ID de responsable
* Nombre del responsable
* ID exclusivo del responsable
* Nombre
* Funciones
* Origen
* Estado
* Número de miembros del equipo
* Zona horaria
* Tipo
* ID exclusivo

Grupo de usuarios

* Fecha de creación
* ID
* Número de miembros
* Nombre
* Estado

Grupo de usuarios (campo activo)

* Fecha de creación
* ID
* Número de miembros
* Nombre
* Estado

Grupo de usuarios (personalizado)

* Fecha de creación
* ID
* Número de miembros
* Nombre
* Estado

Grupo de usuarios (equipo directo)

* Fecha de creación
* ID
* Número de miembros
* Nombre
* Correo electrónico de propietario
* ID del propietario
* Nombre del propietario
* ID exclusivo del propietario
* Estado

Grupo de usuarios (integrado)

* Fecha de creación
* ID
* Número de miembros
* Nombre
* Estado

Grupo de usuarios (equipo)

* Fecha de creación
* ID
* Número de miembros
* Descripción
* Nombre
* Correo electrónico de propietario
* ID del propietario
* Nombre del propietario
* Estado del propietario
* ID exclusivo del propietario
* Estado

**Cómo se unen los conjuntos de datos**

No todos los pares de conjuntos de datos se pueden combinar en un solo informe. Los conjuntos de datos deben compartir una relación lógica en el modelo de datos de Adobe Learning Manager para poder unirse. Al agregar la primera columna, Report Builder filtra los conjuntos de datos restantes para mostrar sólo los compatibles. Si un conjunto de datos aparece atenuado, no se puede unir directamente con las columnas que ya ha seleccionado.

Esto significa que el conjunto de datos no se puede combinar con las columnas que ya ha seleccionado. Se trata de una restricción estricta en el modelo de datos. Los dos conjuntos de datos no comparten una ruta de unión compatible.

Un ejemplo común es el campo derivado **Compliance %**. Cuando se selecciona Cumplimiento %, los conjuntos de datos **Transcripción**, **Transcripción del módulo** y **Instancia de objeto de aprendizaje** están deshabilitados. El porcentaje de cumplimiento se calcula a nivel de usuario o de grupo de usuarios en relación con los objetos de aprendizaje y los catálogos. Está pensado para usarse solo con las columnas y filtros **Usuario**, **Grupo de usuarios**, **Objeto de aprendizaje** y **Catálogo**.

Para utilizar un conjunto de datos deshabilitado, anule la selección de las columnas que causan el conflicto y, a continuación, agregue el conjunto de datos que necesite.

Las relaciones de unión que se indican a continuación se extraen del modelo de datos de Report Builder. Comprenderlos le ayuda a planificar qué conjuntos de datos combinar antes de crear un informe.

**Conjuntos de datos de concentrador**

Dos conjuntos de datos actúan como centros centrales. La mayoría de los otros conjuntos de datos se conectan a través de ellos:

* **Enrollment** (conjunto de datos de inscripción), la tabla de hechos principal. Se conecta directamente al **Usuario** (el alumno que se inscribió), al **Objeto de aprendizaje** (en el que se inscribió) y, a través del objeto de aprendizaje, a **Sesión de módulo**, **Catálogo**, **Etiqueta de catálogo** y **Instancia de objeto de aprendizaje**.
* **Transcripción del módulo** (conjunto de datos moduleTranscript): la tabla de hechos de progreso de nivel de módulo. Se conecta al **Usuario** y a la **Sesión del módulo**, que a su vez se vincula al **Objeto de aprendizaje**.

La mayoría de los informes que combinan datos de alumnos, cursos y finalizaciones se crean a través de uno de estos dos centros.

**Unir rutas por caso de uso**

**Para combinar estos conjuntos de datos**

**Ruta de unión**

**Usuario** + **Inscripción**

Inscripción → Usuario (mediante el ID del alumno)

**Inscripción** + **Objeto de aprendizaje**

Inscripción → Objeto de aprendizaje (mediante ID de objeto de aprendizaje)

**Objeto de aprendizaje** + **Catálogo**

Objeto de aprendizaje → Catálogo de objetos de aprendizaje → Catálogo

**Objeto de aprendizaje** + **Etiqueta de catálogo**

Objeto de aprendizaje → Etiquetas de catálogo de objetos de aprendizaje

**Objeto de aprendizaje** + **Instancia de objeto de aprendizaje**

Instancia de objeto de aprendizaje

**Sesión de módulo** + **Objeto de aprendizaje**

Módulo Sesión → Objeto de aprendizaje (mediante curso de sesión)

**Sesión de módulo** + **Usuario** (instructor)

Sesión de módulo → Usuario (a través del alias de instructor FK)

**Usuario** + **Grupo de usuarios**

Pertenencia a grupos de usuarios → Usuario + Grupo de usuarios

**Objeto de aprendizaje** + **Usuario** (autor)

LO Author → Usuario (vía autor alias FK)

**Usuario** + **Campos activos**

Campos activos del usuario → Usuario (mediante ID de usuario)

**Relaciones con alias**

Algunos campos del modelo de datos se unen a la entidad **Usuario** mediante una función con nombre en lugar de un ID de alumno directo. Se trata de claves externas con alias. Señalan a la misma tabla de usuario pero representan una función diferente:

* **Instructor**: La sesión del módulo se une al usuario como instructor de la sesión
* **Autor**: El autor de objeto de aprendizaje se une al usuario como autor del objeto de aprendizaje
* **Administrador**: El usuario se une a sí mismo para representar al responsable del alumno.
* **Completado por**: La inscripción y la transcripción del módulo incluyen una referencia de usuario &quot;completada por&quot; independiente.

Por este motivo, un solo informe puede mostrar tanto el nombre de un alumno como el nombre de su instructor. Ambos proceden de la entidad Usuario a través de diferentes rutas de unión.

**Tipos de conjunto de datos de grupo de usuarios**

La categoría **Grupo de usuarios** contiene varias vistas de conjunto de datos distintas, cada una de las cuales cubre un tipo diferente de grupo:

**Conjunto de datos**

**Tipo de grupo**

**Grupo de usuarios** (userGroup)

Todos los grupos de usuarios. Utilice este como conjunto de datos principal del grupo de usuarios

**Grupo de usuarios de campos activos** (active_field_user_group)

Grupos basados en valores de campo activos (por ejemplo, región, departamento)

**Grupo de usuarios del equipo** (team_user_group)

Grupos basados en la jerarquía de responsables

**Grupo de usuarios personalizado** (custom_user_group)

Grupos personalizados configurados manualmente

**Grupo de usuarios integrado** (inbuild_user_group)

Grupos definidos por el sistema

Los conjuntos de datos de grupos de usuarios basados en vistas (**Campo activo**, **Equipo**, **Personalizado**, **Integrado**) no tienen relaciones de clave externa directas en el esquema, son vistas SQL. Esto significa que tienen restricciones de unión más flojas que el conjunto de datos **Grupo de usuarios** principal. Use el conjunto de datos **Grupo de usuarios** principal al unir datos de grupos de usuarios con datos de inscripción o transcripción para obtener los resultados más confiables.

**Campos derivados**

Los campos derivados son columnas calculadas previamente por el Report Builder. Se muestran por separado de las columnas estándar en el selector de columnas.

**Campo derivado**

**Lo que calcula**

**Conjuntos de datos requeridos**

**Porcentaje de cumplimiento**

Porcentaje de alumnos requeridos que completaron cursos con etiqueta de cumplimiento

Grupo de usuarios, objeto de aprendizaje, transcripción

**% de finalización**

Finalizaciones divididas por inscripciones × 100

Transcripción u objeto de aprendizaje

**Recuento de usuarios inscritos**

Total de alumnos inscritos para un objeto de aprendizaje

Objeto de aprendizaje

**Recuento de finalización**

Finalizaciones totales de un objeto de aprendizaje

Objeto de aprendizaje

**Iniciar recuento**

Alumnos que han iniciado pero no completado

Objeto de aprendizaje

**Recuento de miembros**

Número de usuarios en un grupo de usuarios

Grupo de usuarios
