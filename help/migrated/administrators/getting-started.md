---
description: Este documento proporciona un enfoque recomendado para que las empresas instalen y configuren Adobe Learning Manager. El equipo de Learning Manager sugiere un enfoque por fases para poder empezar a utilizar la aplicación. No es obligatorio seguir todas las fases en una secuencia determinada.
jcr-language: en_us
title: Guía de prácticas recomendadas para configurar Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 71%

---



# Guía de prácticas recomendadas para configurar Learning Manager

Este documento proporciona un enfoque recomendado para que las empresas instalen y configuren Adobe Learning Manager. El equipo de Learning Manager sugiere un enfoque por fases para poder empezar a utilizar la aplicación. No es obligatorio seguir todas las fases en una secuencia determinada.

Estas fases pueden realizarlas tres funciones diferentes, una o más personas según la configuración de su organización. Las tres funciones son las siguientes:

1. **Administrador de TI** - El administrador de TI realiza actividades relacionadas con la activación o la integración asociadas a la aplicación Learning Manager en una organización. El administrador de TI también puede agregar uno o varios usuarios, y desempeñar una función de administrador de integración.
1. **Autor** - El autor crea el contenido de aprendizaje necesario para los requisitos de aprendizaje de la organización. El autor del contenido de formación o de aprendizaje de su organización puede comenzar a crear el contenido básico necesario para la aplicación de Learning Manager.
1. **Administrador de Learning Manager** - El administrador de la aplicación Learning Manager realiza actividades de configuración y configuración. En algunas empresas, el administrador de TI también puede desempeñar la función de administrador de la aplicación Learning Manager.

Puede revisar la infografía que se proporciona a continuación para obtener una descripción general de las fases y las tareas correspondientes.

![](assets/learning-manager-getting-started.jpg)

En esta etapa, suponemos que su empresa ya ha recibido la clave de licencia y que se ha activado la cuenta de Learning Manager. Como se menciona en la infografía, las tres pistas se explican de la siguiente manera:

## Fase 1: Configuración técnica (administrador de TI) {#phase1technicalsetupitadministrator}

En la versión 1, el administrador de TI de su organización puede cambiar a la función de administrador de integración en la aplicación Learning Manager y realizar algunas activaciones e integraciones de la siguiente manera:

### Activar o añadir campos activos (administrador de Learning Manager) {#enableaddactivefieldscaptivateprimeadministrator}

Además de los campos activos proporcionados por los usuarios durante el registro, el administrador puede agregar más campos activos. El administrador también puede habilitar y deshabilitar los campos de usuario. Los valores de estos campos activos se generan a partir de los metadatos de varias fuentes de datos asociadas a cuentas de usuario. Consulte la [Ayuda de campos activos](feature-summary/add-users-user-groups.md#active-fields) para obtener más información.

### Inicio de sesión único {#singlesignonsso}

Puede acceder a la aplicación Learning Manager mediante Adobe ID o el inicio de sesión único. El inicio de sesión único es un mecanismo que permite a un usuario autenticarse una vez y obtener acceso a varias aplicaciones muchas veces. Esta configuración no es obligatoria para la empresa. Si su empresa tiene un proveedor de inicio de sesión único basado en SAML 2.0, puede usarlo para configurar la aplicación Learning Manager. La configuración es necesaria en su empresa y en la aplicación Learning Manager. Si elige usar inicio de sesión único, póngase en contacto con la asistencia de Adobe para recibir instrucciones sobre configuración. Consulte la [Ayuda de configuración](feature-summary/settings.md) para obtener más información.

### Importación en bloque de usuarios {#bulkimportofusers}

Cuando tiene un gran volumen de usuarios en su empresa, puede importar todos los usuarios en bloque a la aplicación Learning Manager mediante un archivo .csv. Antes de realizar esta tarea, le recomendamos que exporte la lista de usuarios de la aplicación de RR. HH. de su organización en formato .CSV. Incluso si no importa en bloque los usuarios en esta etapa, puede familiarizarse con el formato CSV. Para comenzar con el proceso de importación en Learning Manager, cargue el archivo .CSV y asigne los campos de datos de la aplicación a las columnas CSV de su organización. Consulte la [Ayuda de importación masiva](add-users-in-bulk.md) para obtener más información.

### Integración del conector de FTP {#ftpconnectorintegration}

Si debe afrontar la adición o eliminación continuas de empleados en su empresa, puede optar por automatizar la importación en bloque de usuarios mediante un conector FTP. Primero debe establecer una conexión; después, puede cargar un archivo .csv y asignar los atributos de CSV con los campos correspondientes de Learning Manager. Puede programar el proceso de importación automática y sincronizarlo cuando sea necesario. Consulte la [Ayuda del conector FTP](../integration-admin/feature-summary/connectors.md#ftpconnector) para obtener más información.

### Integración de conectores de Salesforce {#salesforceconnectorintegration}

Si tiene una cuenta de Salesforce en su empresa, puede automatizar el proceso de importación de todos los usuarios a la aplicación Learning Manager. Si desea utilizar esta función, utilice el conector de Salesforce para integrar Learning Manager con la cuenta de Salesforce y automatizar la sincronización de datos. Utilice la función de programación automática para realizar la importación automática de usuarios con regularidad. La sincronización también se puede efectuar a diario. Consulte [Ayuda del conector de Salesforce](../integration-admin/feature-summary/connectors.md#sfconnector) para obtener más información.

### Integración de Adobe Connect {#adobeconnectintegration}

Si utiliza Adobe Connect en su empresa, puede integrarlo con la aplicación Adobe Learning Manager para proporcionar una experiencia de usuario perfecta a los alumnos. La integración permite a sus alumnos acceder a clases virtuales dentro de la aplicación Learning Manager con un solo clic, sin tener que volver a iniciar sesión en Adobe Connect. Con esta función, los alumnos también pueden consumir las sesiones de clase virtual grabadas en la aplicación Learning Manager. Para integrarlos, primero debe integrar los ajustes. Utilice **Configuración > Adobe Connect > Configurar ahora** para proporcionar e integrar la URL y las credenciales de Adobe Connect. Consulte [Ayuda de integración de Adobe Connect](feature-summary/adobeconnect-integration.md) para obtener más información.

### Registro de la aplicación Salesforce {#salesforceappregistration}

Los alumnos empresariales pueden tener una experiencia fluida de acceder a la aplicación Learning Manager directamente desde sus cuentas de Salesforce. Los alumnos pueden acceder a su contenido de aprendizaje asignado, por ejemplo cursos, programas de aprendizaje y ayudas de trabajo de la aplicación Salesforce. Los usuarios también pueden acceder a notificaciones y anuncios desde la aplicación Learning Manager dentro de Salesforce. Para utilizar esta función, debe registrar la aplicación destacada de Salesforce en la aplicación Learning Manager. Consulte [Ayuda de la aplicación Salesforce](../integration-admin/feature-summary/sfdc-app.md) para obtener información sobre la instalación e instrucciones de uso.

## Fase 2: Configuración del sitio (administrador de Learning Manager) {#phase2siteconfigurationcaptivateprimeadministrator}

El administrador de la aplicación Learning Manager de su empresa debe instalar o configurar algunas funciones antes de comenzar a implementarlas para sus alumnos.

### Marca {#branding}

Es posible que una organización desee mostrar el logotipo de la empresa en la aplicación Learning Manager, tener su propio dominio en la URL, mostrar el nombre de la organización y mostrar esquemas de colores que coincidan con la marca de una organización. Learning Manager permite a las empresas usar todas estas funciones. Si desea personalizar la configuración y usar su propia marca, haga clic en la sección Marca en el panel izquierdo. Haga clic en Editar junto a todas estas opciones y personalice según sus requisitos. Consulte la [Ayuda de marcas y temas](feature-summary/themes.md) para obtener más información.

### Añadir usuarios o grupos de usuarios {#addusersusergroups}

Como los alumnos son los usuarios principales de su contenido de aprendizaje, agregar usuarios al sistema de administración de aprendizaje es el paso principal. Añada usuarios a la aplicación Learning Manager y asígneles funciones. Puede añadir usuarios de las siguientes maneras:

#### Añadir usuarios (internos) {#addusersinternal}

* **Como un solo usuario**: añadir usuarios individuales a la aplicación Learning Manager le permite probar algunos de los usuarios antes de incorporarlos de forma masiva. Además, esta opción es útil cuando desea agregar más usuarios individuales según sea necesario, después de la importación en bloque de usuarios.
* **Registro automático** - Esta opción permite a los administradores permitir que sus empleados se registren en Learning Manager.
* **Importación en bloque** (carga de CSV): con esta opción, puede importar usuarios en bloque a la aplicación Learning Manager. Como requisito previo, debe tener lista la lista de usuarios en formato CSV antes de utilizar esta función.

#### Añadir usuarios (perfiles externos) {#addusersexternalprofiles}

* Mediante inscripción externa: con esta opción, puede inscribir a miembros externos del departamento o a empleados externos de su empresa en la aplicación.

#### Añadir grupos de usuarios {#addusergroups}

La aplicación Learning Manager genera grupos de usuarios predeterminados basados en atributos similares. Además de los grupos predeterminados, puede generar grupos de usuarios personalizados a partir de parámetros como designación, ubicación para poder utilizar esos grupos en la interacción e informes, entre otros. Consulte[ Ayuda para añadir usuarios](feature-summary/add-users-user-groups.md) para obtener más información.

### Asignar funciones {#assignroles}

Después de añadir usuarios a Learning Manager, el administrador puede empezar a asignar funciones de autor, administrador o administrador de integración a los usuarios según los requisitos de la empresa. Para asignar funciones a los usuarios, en el inicio de sesión del administrador, puede hacer clic en **[!UICONTROL Usuarios]**  en el panel izquierdo, seleccione la casilla de verificación junto a cada nombre de usuario y haga clic en **[!UICONTROL Acciones]** para elegir la función que desea asignar. Adobe Learning Manager asigna las funciones de responsable a los usuarios en función de las funciones o privilegios que indique su organización en el archivo CSV. También puede cambiar las funciones de los usuarios como responsables mediante el flujo de trabajo Editar usuarios. Consulte[ Ayuda para añadir usuarios](feature-summary/add-users-user-groups.md) para obtener más información.

### Plantillas de notificación {#notificationtemplates}

Las notificaciones pueden ser útiles para los usuarios en un sistema de gestión de aprendizaje para conocer su estado o para estar informados sobre los eventos y las actividades. Al crear cursos, configurar las funciones o durante el consumo de cursos, los usuarios pasan por varios eventos que activan las notificaciones a los alumnos, sus responsables, administradores o autores. Learning Manager proporciona varias plantillas de notificación por correo electrónico en la aplicación. Como administrador, puede personalizarlas según los requisitos de su empresa. Para crear notificaciones por correo electrónico, elija **Plantillas de correo electrónico** en el panel izquierdo y haga clic en el nombre de la plantilla. Consulte [Ayuda de plantillas de correo electrónico](feature-summary/email-templates.md) para obtener más información.

**Desactivar notificaciones por correo electrónico (recomendado)**

De forma predeterminada, en la aplicación Learning Manager las notificaciones están habilitadas. Puede desactivar las notificaciones en esta fase si no desea notificar a sus empleados de la empresa.

### Insignias {#badges}

Las insignias son logros que el empleado puede ganar por la realización de un curso. Los profesionales de todo el mundo utilizan estas insignias como representación de aptitudes o logros de aprendizaje. Puede crear una colección de insignias para asignarlas a los alumnos una vez que se completa el contenido de aprendizaje. Para comenzar a crear insignias, haga clic en la función **[!UICONTROL Insignias]** en el panel izquierdo. Consulte la  [Ayuda de insignias](feature-summary/badges.md) para obtener más información.

### Comentarios {#feedback}

Los comentarios son uno de los factores importantes de un sistema de gestión de aprendizaje (LMS) para medir el progreso del aprendizaje de los alumnos y garantizar la calidad del contenido de aprendizaje. Learning Manager brinda dos tipos de opciones de comentarios a los usuarios.

* Los comentarios de L1 los proporcionan los alumnos tras completar el curso.
* Los comentarios de L3 son los comentarios que los responsables proporcionan a los alumnos en función del impacto del curso en el comportamiento de los alumnos y en las actividades diarias.

Esta función es de uso opcional para las empresas. Los administradores pueden personalizar las plantillas de comentarios según los requisitos de su empresa. Para usar esta función, el administrador debe habilitar las opciones de comentarios L1 y L3 en el nivel de instancia del curso. Para configurar los comentarios, elija cualquier curso, haga clic en Valores predeterminados de la instancia en el panel izquierdo y habilite la opción de comentarios. Consulte [Ayuda de comentarios](feature-summary/courses.md) para obtener más información.

### Interacción {#gamification}

Mantener a los alumnos interesados mientras consumen el contenido es uno de los desafíos que afrontan las empresas. La interacción aumenta la tasa de finalización de cursos mediante la participación y la motivación de los alumnos para alcanzar sus objetivos con técnicas de interacción. Los alumnos pueden competir con sus colegas para ganar puntos por distintas actividades de aprendizaje y para alcanzar niveles de bronce, plata, oro y platino. Los administradores pueden habilitar y deshabilitar cada tarea de interacción, y modificar la asignación de puntos a las tareas. Learning Manager proporciona la función de interacción con algunas opciones predeterminadas. Puede comenzar a utilizar la función con la configuración predeterminada durante un tiempo y después personalizarla. Si lo desea, puede cambiar o no la configuración de esta opción. Si tiene un experto en su empresa, le recomendamos que configure los las opciones antes de usarlo. Consulte [Ayuda de interacción](feature-summary/gamification.md) para obtener más información.

### Crear objetos de aprendizaje {#createlearningobjects}

Es la etapa lógica en la que convergen las tres pistas (pista1, pista2 y pista3) para asumir la próxima línea de acción.

En este punto, una vez creados los módulos y los cursos, puede comenzar a crear objetos de aprendizaje de nivel superior como certificaciones, programas de aprendizaje o ayudas de trabajo para avanzar. Antes de empezar a crear objetos de aprendizaje, asegúrese de haber añadido agregado algunos usuarios a la aplicación Learning Manager, y de haber creado varios módulos y cursos.

#### Crear certificaciones {#createcertifications}

La certificación es una prueba de la finalización de un contenido de aprendizaje o una prueba de logro para los alumnos una vez o en un intervalo recurrente. La inscripción de los alumnos a contenido de aprendizaje se puede aumentar proporcionando certificación a los alumnos tras finalizar el curso. Como administrador, puede crear un programa de certificación alojado internamente o administrado por un tercero. En la certificación interna, defina los cursos que un alumno debe completar para obtener la certificación. Antes de crear la certificación, asegúrese de tener algunos varios cursos disponibles en la cuenta. Consulte la  [Ayuda de certificación](feature-summary/certifications.md) para obtener más información sobre cómo crear certificaciones.

#### Crear ayudas de trabajo {#createjobaids}

Las ayudas de trabajo son un repositorio de contenido de formación al que pueden acceder los alumnos sin ningún criterio de inscripción o finalización. Los alumnos pueden consultar estas ayudas de trabajo mientras están en el trabajo a fin de obtener asistencia para efectuar cualquier actividad o tarea de una empresa. Aunque no es obligatorio utilizar ayudas de trabajo como parte de la creación del curso, el equipo de Learning Manager recomienda crear ayudas de trabajo como práctica recomendada para su empresa. Consulte la  [Ayuda de ayudas de trabajo](../authors/feature-summary/job-aids.md) para obtener información sobre cómo crear ayudas de trabajo.

#### Crear programas de aprendizaje {#createlearningprograms}

Los programas de aprendizaje son un conjunto de cursos diseñados exclusivamente que cumplen objetivos específicos del alumno. Antes de crear programas de aprendizaje, asegúrese de haber creado algunos cursos o de que haya cursos disponibles en su cuenta.  Aunque es opcional que una organización utilice esta función, el equipo de Learning Manager recomienda utilizarla para inculcar un aprendizaje centrado en los empleados. Para comenzar a usar los programas de aprendizaje, haga clic en Programas de aprendizaje en el panel izquierdo, elija un conjunto de cursos del catálogo y publíquelos. Consulte la [Ayuda de programas de aprendizaje](feature-summary/learning-programs.md) para obtener instrucciones específicas.

### Crear catálogos {#createcatalogs}

Puede usar catálogos en una empresa para crear un contenido específico o para clasificar contenido para un conjunto definido de alumnos. En Learning Manager, un catálogo es una colección de objetos de aprendizaje como cursos, certificaciones o programas de aprendizaje. Puede elegir los objetos de aprendizaje que desee al crear catálogos. Asegúrese de haber creado ya un conjunto de cursos, certificaciones o programas de aprendizaje antes de crear los catálogos. Puede crear catálogos personalizados con un conjunto de objetos de aprendizaje si desea asignarlos a cualquier grupo de usuarios internos o externos. Consulte la  [Ayuda de catálogos](feature-summary/catalogs.md) para obtener más información sobre los catálogos.

### Activar notificaciones por correo electrónico/acceso de usuario {#turnonemailnotificationsuseraccess}

En esta fase, puede activar las notificaciones por correo electrónico a los usuarios de sus aplicaciones y también habilitar el acceso de los usuarios.

## Fase 3: Creación de cursos (autor) {#phase3authoringcoursesauthor}

Los desarrolladores de contenido o los autores de su organización pueden empezar a crear el contenido de aprendizaje. Es obligatorio crear módulos y cursos, ya que constituyen la base de todo el contenido de aprendizaje en la aplicación Learning Manager.

### Crear módulos {#createmodules}

Los módulos son los componentes básicos de la aplicación Learning Manager. Para organizar el contenido de aprendizaje, empiece a crear módulos como autor. Learning Manager le permite elegir cualquiera de los cuatro tipos de módulos del curso, por ejemplo aula, con ritmo personalizado, actividad y módulos de clase virtual. Consulte la  [Ayuda de módulos](../authors/how-to-choose-modules.md) para obtener más información sobre qué tipo de módulo de curso se adapta mejor a las necesidades de su organización.

### Crear cursos {#createcourses}

Los administradores pueden asumir una función de autor en la aplicación Learning Manager y crear cursos. En la aplicación Learning Manager, un curso es una unidad básica con un conjunto de módulos que se pueden asignar al alumno. Los alumnos consumen cursos. Puede comenzar a crear cursos eligiendo los módulos que creó anteriormente, asociar las aptitudes que desea que los alumnos obtengan del curso, asociar niveles, créditos e insignias a un curso, seleccionar ayudas de trabajo, requisitos previos y recursos basados en su elección y publicar el curso. También puede crear varias instancias de un curso a fin de poder asignarlas a varios alumnos en diferentes zonas horarias, horarios, etcétera. Consulte la  [Ayuda de cursos](../authors/feature-summary/courses.md)para obtener más información sobre cómo crear un curso.

### Crear objetos de aprendizaje {#Createlearningobjects-1}

Es la etapa lógica en la que convergen las tres pistas (pista1, pista2 y pista3) para asumir la próxima línea de acción.

En este punto, una vez creados los módulos y los cursos, puede comenzar a crear objetos de aprendizaje de nivel superior como certificaciones, programas de aprendizaje o ayudas de trabajo para avanzar. Antes de empezar a crear objetos de aprendizaje, asegúrese de haber añadido agregado algunos usuarios a la aplicación Learning Manager, y de haber creado varios módulos y cursos.

#### Crear certificaciones {#Createcertifications-1}

La certificación es una prueba de la finalización de un contenido de aprendizaje o una prueba de logro para los alumnos una vez o en un intervalo recurrente. La inscripción de los alumnos a contenido de aprendizaje se puede aumentar proporcionando certificación a los alumnos tras finalizar el curso. Como administrador, puede crear un programa de certificación alojado internamente o administrado por un tercero. En la certificación interna, defina los cursos que un alumno debe completar para obtener la certificación. Antes de crear la certificación, asegúrese de tener algunos varios cursos disponibles en la cuenta. Consulte la  [Ayuda de certificación](feature-summary/certifications.md) para obtener más información sobre cómo crear certificaciones.

#### Crear ayudas de trabajo {#CreateJobaids-1}

Las ayudas de trabajo son un repositorio de contenido de formación al que pueden acceder los alumnos sin ningún criterio de inscripción o finalización. Los alumnos pueden consultar estas ayudas de trabajo mientras están en el trabajo a fin de obtener asistencia para efectuar cualquier actividad o tarea de una empresa. Aunque no es obligatorio utilizar ayudas de trabajo como parte de la creación del curso, el equipo de Learning Manager recomienda crear ayudas de trabajo como práctica recomendada para su empresa. Consulte la  [Ayuda de ayudas de trabajo](../authors/feature-summary/job-aids.md) para obtener información sobre cómo crear ayudas de trabajo.

#### Crear programas de aprendizaje {#Createlearningprograms-1}

Los programas de aprendizaje son un conjunto de cursos diseñados exclusivamente que cumplen objetivos específicos del alumno. Antes de crear programas de aprendizaje, asegúrese de haber creado algunos cursos o de que haya cursos disponibles en su cuenta.  Aunque es opcional que una organización utilice esta función, el equipo de Learning Manager recomienda utilizarla para inculcar un aprendizaje centrado en los empleados. Para comenzar a usar los programas de aprendizaje, haga clic en Programas de aprendizaje en el panel izquierdo, elija un conjunto de cursos del catálogo y publíquelos. Consulte la [Ayuda de programas de aprendizaje](feature-summary/learning-programs.md) para obtener instrucciones específicas.

## Fase 4: Administración de su LMS (administrador de Learning Manager) {#phase4managingyourlmscaptivateprimeadministrator}

### Anuncios {#announcements}

Los anuncios son útiles para que la empresa divulgue cualquier información importante a todos los alumnos de una cuenta de forma simultánea. En la aplicación Learning Manager, anuncio es un mensaje multimedia (texto, imagen o vídeo) que un administrador crea y difunde entre un determinado conjunto de usuarios y objetos de aprendizaje. Puede enviar anuncios al instante o programarlos para que se activen automáticamente en una fecha específica. Si desea utilizar esta función en la aplicación Learning Manager, elija Anuncios en el panel izquierdo y haga clic en Añadir para crear anuncios. Consulte la [Ayuda de anuncios](feature-summary/announcements.md) para obtener más información.

### Inscripción de usuarios {#userenrollment}

La inscripción de usuarios es un paso importante para una aplicación de sistema de gestión de aprendizaje (LMS). En esta etapa, puede comenzar a inscribir a los alumnos en diversos objetos de aprendizaje de la aplicación Learning Manager. Puede inscribir a los alumnos de forma manual o automática mediante planes de aprendizaje.

#### Inscripción manual {#manualenrollment}

* **Inscripción automática -** Si activa esta opción al crear un objeto de aprendizaje, los alumnos pueden inscribirse en los objetos de aprendizaje.
* **Aprobación del responsable** - Si elige esta opción en el tipo de inscripción al crear un curso, los responsables deben aprobar la inscripción de los alumnos.
* **Nominación de responsable** - Si elige este tipo de inscripción durante la creación del curso, los responsables deben nominar dichos cursos.
* **Inscripción de administrador** - En este caso, el administrador puede inscribir a algunos de los alumnos en función de los requisitos de la organización.

Consulte la [Ayuda de inscripción de usuarios](feature-summary/courses.md)para obtener más información.

Inscriba a los alumnos manualmente a objetos de aprendizaje de estas cuatro formas:

### Inscripción automatizada {#automatedenrollment}

Automatice la inscripción de alumnos en objetos de aprendizaje mediante planes de aprendizaje.

#### Planes de aprendizaje (según activadores) {#learningplansbasedontriggers}

Puede utilizar planes de aprendizaje para asignar automáticamente cursos, programas de aprendizaje o certificaciones a los alumnos si tienen lugar ciertos eventos. Por ejemplo,

* Se añade un usuario nuevo
* El usuario cambia de grupo de usuarios
* El alumno finaliza un objeto de aprendizaje
* El usuario completa una aptitud

Consulte la [Ayuda de planes de aprendizaje](feature-summary/learning-plans.md)  para obtener más información.

### Crear informes {#createreports}

En esta etapa, puede comenzar a crear y administrar varios tipos de informes.

Adobe Learning Manager le permite crear diversos informes para supervisar y controlar las actividades de los alumnos. Puede utilizar los siguientes tres tipos de funciones de generación de informes para generar informes:

* **Panel Informes** - Crear informes de resumen para obtener información procesable sobre el consumo de contenido de aprendizaje de los alumnos en función de diversas categorías, como grupos de usuarios, eficacia, tiempo de los alumnos en los cursos, etc.
* **Transcripciones de alumnos** - Crear informes centrados en el alumno con un historial completo de los alumnos desde el día del registro hasta la fecha.
* **Informes del curso** - Crear estadísticas de consumo de cursos de alumnos a partir de cursos individuales. También puede crear informes de prueba en el nivel del curso.

Consulte la  [Ayuda de informes](feature-summary/reports.md) para obtener más información sobre el proceso de generación de informes.

Para obtener más información sobre el uso de las funciones de la aplicación Learning Manager, consulte [Ayuda de Learning Manager](../topics.md) en función de cada función.
