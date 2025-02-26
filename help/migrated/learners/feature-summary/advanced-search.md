---
jcr-language: en_us
title: Búsqueda basada en IA en Adobe Learning Manager
description: Más información sobre la búsqueda basada en IA en Adobe Learning Manager
exl-id: 9982a8be-b2e6-42a4-836a-7f9337588ae8
source-git-commit: e25c92f9d91768db607cb153138cd02d1fbe28aa
workflow-type: tm+mt
source-wordcount: '1173'
ht-degree: 0%

---

# Búsqueda avanzada de IA en Adobe Learning Manager

La funcionalidad de búsqueda en ALM mejora la experiencia del usuario al permitirle encontrar contenido relevante de manera eficiente y ayudarles a consumir el contenido adecuado.

Adobe Learning Manager presenta una capacidad de búsqueda basada en IA que combina la búsqueda léxica y semántica. La búsqueda es más inteligente, ya que busca términos específicos y entiende el contexto y la intención detrás de ellos. La búsqueda avanzada basada en IA entiende el significado de tu consulta y ofrece resultados relevantes.

>[!NOTE]
>
>La búsqueda basada en IA solo está disponible para los alumnos.

## ¿Por qué es importante la búsqueda?

La funcionalidad de búsqueda es importante por varias razones:

* **Experiencia de usuario**: Una función de búsqueda bien implementada mejora la satisfacción de los usuarios al permitirles encontrar rápidamente la información que necesitan.
* **Eficacia**: Ahorra tiempo al reducir el esfuerzo necesario para localizar contenido específico, especialmente en bases de datos grandes o sistemas de administración de aprendizaje.
* **Accesibilidad**: Las funciones de búsqueda efectivas hacen que la información sea más accesible, lo que garantiza que los usuarios puedan interactuar con contenido relevante para sus necesidades.
* **Personalización**: Los sistemas de búsqueda avanzada pueden adaptar los resultados en función de las preferencias del usuario, lo que mejora la relevancia de la información presentada.

## Evolución de los comportamientos de búsqueda en la web

A medida que la gente busca en línea, su forma de hacerlo está cambiando y los motores de búsqueda se están adaptando para mantenerse al día. Las siguientes son algunas de las formas clave en las que la gente busca información hoy en día:

* **Impulsado por intención**: En lugar de escribir palabras clave exactas, los usuarios ahora expresan sus necesidades con frases como Deseo o Necesito hacerlo. Los motores de búsqueda modernos entienden el propósito detrás de estas frases y dan resultados más relevantes.
* **Resultados clasificados**: los resultados de la búsqueda se organizan en función de lo que otros usuarios consideren útil. Esto significa que el contenido más útil aparece en la parte superior, lo que facilita la búsqueda de información de calidad.
* **Varios orígenes**: Cuantos más orígenes cubra un motor de búsqueda, mejores serán los resultados. Al extraer información de una variedad de fuentes de confianza, los motores de búsqueda proporcionan respuestas más completas y precisas.
* **Personalizado**: los motores de búsqueda ajustan los resultados en función de factores como la hora, la ubicación y las preferencias del usuario. Esto facilita a los usuarios encontrar información que se ajuste a sus necesidades específicas en este momento.

## Por qué es mejor la búsqueda de Adobe Learning Manager

Adobe Learning Manager ofrece una experiencia de búsqueda más inteligente y avanzada que no solo coincide con las palabras clave, sino que entiende contextualmente el significado de la consulta del usuario para encontrar los resultados más relevantes para ellos.

* **Con tecnología de IA**: Adobe Learning Manager usa técnicas avanzadas de IA para entender el significado detrás de la intención de búsqueda y no solo las palabras. Esto ayuda a mostrar resultados que coinciden realmente con lo que el usuario quiere, haciendo las búsquedas más precisas.
* **Impulsado por pares**: Adobe Learning Manager utiliza un rango de parámetros de calidad del curso para clasificar los resultados más útiles. Este algoritmo de clasificación está entrenado en 50 millones de puntos de datos que puntúan periódicamente cada contenido en el repositorio
* **Completo**: Adobe Learning Manager busca en toda la biblioteca, incluido contenido propio, títulos de cursos de terceros, descripciones, etiquetas, notas personalizadas y otros metadatos. Para contenido como Vídeo y PDF, se transcribe automáticamente y se busca dentro de su transcripción.

## Búsqueda basada en IA de Adobe Learning Manager

Adobe Learning Manager utiliza tecnología avanzada de IA para mejorar la experiencia de búsqueda y facilitar la búsqueda de contenido de aprendizaje relevante. Los principales componentes de la búsqueda avanzada se describen a continuación.

### Reconocimiento de términos clave

Adobe Learning Manager utiliza el procesamiento del lenguaje natural (NLP) para identificar las palabras clave importantes de los títulos y descripciones de los cursos. A continuación, se centra en esas palabras clave para proporcionar mejores resultados de búsqueda, lo que ayuda a impulsar los resultados con esas palabras clave sobre otros resultados. Por ejemplo, si un alumno busca **Conceptos básicos de Photoshop**, Adobe Learning Manager dará prioridad a la palabra **Photoshop** para mostrar los cursos más relevantes.

![](assets/search-2.png)
_Priorizar la palabra clave_

En la captura de pantalla anterior, un alumno busca cursos utilizando el término **introducción a Photoshop**. La búsqueda prioriza la palabra **Photoshop** para encontrar los cursos más relevantes en torno a **Photoshop**. Para que la palabra clave comience, entiende la intención y busca palabras similares para mostrar las mejores coincidencias. De este modo, el alumno ve los cursos centrados en Photoshop y adecuados para principiantes.

### Expandir la consulta

Adobe Learning Manager expande la consulta del usuario a un significado más contextual para ayudar a encontrar mejores resultados. De esta manera, el algoritmo de búsqueda obtiene más contexto junto con la consulta del usuario. Incluso si los alumnos utilizan términos generales, pueden encontrar resultados útiles. Por ejemplo, si un alumno busca **Customer Service Foundation**, intenta buscar la palabra clave de la consulta y expandir el resto de la consulta a frases similares.

![](assets/search-1.png)
_Expandiendo la consulta_

### Búsqueda de metadatos del curso

La búsqueda de metadatos de Adobe Learning Manager abarca los metadatos de cursos nativos e importados (por ejemplo, de LinkedIn Learning o Go1). Esta función busca en los títulos, descripciones, etiquetas, notas personalizadas y otros metadatos del curso. Esto ayuda a que los resultados sean mejores y más precisos utilizando una gran cantidad de metadatos diferentes para encontrar resultados.
Nota: Los datos de los clientes, incluidos el contenido y las transcripciones, no se comparten con ningún servicio externo de búsqueda impulsada por IA. Todo el contenido se almacena dentro del sistema de almacenamiento actual.

### Búsqueda semántica

Adobe Learning Manager ahora incorpora la búsqueda semántica junto con la búsqueda léxica tradicional, lo que mejora la precisión de los resultados de búsqueda. Al generar incrustaciones vectoriales a partir de los títulos y descripciones de los cursos, se crea una base de datos vectorial completa. Cuando un alumno envía una consulta, el sistema vectoriza la consulta y realiza una coincidencia de similitud para identificar los resultados más relevantes. Por ejemplo, si un alumno busca un tutorial de Photoshop para principiantes, el sistema entiende la solicitud y encuentra cursos que son especialmente útiles para los principiantes con Photoshop .

![](assets/semantic-search.png)
_Búsqueda semántica_

>[!NOTE]
>
>Actualmente, la búsqueda semántica solo admite contenido en inglés.

### Búsqueda en contenido

La funcionalidad de búsqueda de Adobe Learning Manager se ha mejorado para buscar contenido real. Transcribe automáticamente vídeos, archivos de audio, PDF, documentos, ppt y xls, incorporando esas transcripciones en los resultados de búsqueda. Además, utiliza las grabaciones de reuniones de Adobe Connect para proporcionar resultados más completos y relevantes. Esta mejora garantiza que se incluyan cursos con contenido enriquecido, como vídeos y notas de reuniones, lo que mejora significativamente la precisión y la eficacia de la búsqueda. La coincidencia en el contenido ayuda a mejorar la clasificación de los resultados de búsqueda al dar un impulso a los resultados encontrados a través de la coincidencia de frase tradicional y la coincidencia semántica.

>[!NOTE]
>
>El contenido recién añadido, como vídeos o PDF, estará disponible para la búsqueda en el contenido tras un período de procesamiento de 24 horas.

### Búsqueda y reclasificación basadas en IA

La búsqueda de Adobe Learning Manager es líder en el sector y utiliza una combinación única de tecnologías avanzadas para proporcionar resultados de máxima calidad. Combina los métodos de búsqueda tradicionales (como la coincidencia de frase), la búsqueda semántica sofisticada y la búsqueda en el contenido para producir resultados completos. Estos resultados se clasifican según factores clave de calidad de los cursos, como las inscripciones, las fechas de publicación, las clasificaciones, la popularidad y mucho más, lo que garantiza que se alcancen los niveles de calidad más altos de todos los índices, guiados por nuestro sistema de clasificación de calidad de los cursos.

En general, la búsqueda de ALM basada en IA se ha diseñado para ser exhaustiva, precisa y fácil de usar, lo que ayuda a los alumnos a encontrar rápidamente exactamente lo que necesitan para respaldar su recorrido de aprendizaje.


>[!NOTE]
>
>1. Los clientes que utilizan una implementación descentralizada deben seguir la documentación de la API para habilitar la búsqueda avanzada
>2. La búsqueda avanzada no está disponible actualmente para la aplicación Salesforce.
>3. Los datos de los clientes, incluidos el contenido y las transcripciones, no se comparten con ningún servicio externo de búsqueda impulsada por IA. Todo el contenido permanece almacenado de forma segura dentro del sistema de almacenamiento existente.
