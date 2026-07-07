---
description: Obtén más información sobre Experience Builder, una herramienta sin código/de código bajo de Adobe Learning Manager que permite a los administradores diseñar y publicar páginas de marca y fáciles de usar sin conocimientos técnicos.
jcr-language: en_us
title: Experience Builder en Adobe Learning Manager
exl-id: 8d06c2cf-816e-4ad5-85f7-bc26e9d70d51
source-git-commit: 5221f4bde68561d5253e7dfab789815e4cd55d49
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Información general

Experience Builder es una herramienta sin código/de código bajo en Adobe Learning Manager que te ayuda a crear portales de aprendizaje personalizados. Te permite diseñar portales de aprendizaje de marca y fáciles de usar sin necesidad de conocimientos técnicos o amplios conocimientos de codificación.

Con Experience Builder, los administradores pueden crear con facilidad páginas, menús y widgets para ofrecer experiencias de aprendizaje personalizadas adaptadas a su audiencia

Muchas organizaciones tienen dificultades para personalizar sus portales de aprendizaje sin ayuda técnica ni costosos integradores de sistemas. Quieren portales que se adapten a su marca, que ofrezcan contenido dirigido y que se adapten a los diferentes grupos de alumnos sin dejar de ser rápidos y fáciles de crear.

Experience Builder es una herramienta sin código/de código bajo en Adobe Learning Manager que te ayuda a crear portales de aprendizaje personalizados. Te permite diseñar portales de aprendizaje de marca y fáciles de usar sin necesidad de conocimientos técnicos o amplios conocimientos de codificación.Con Experience Builder, puedes crear nuevas páginas, menús y widgets para ofrecer experiencias de aprendizaje personalizadas a tu audiencia de forma rápida y sencilla. Con Experience Builder, puedes crear rápidamente nuevas páginas, menús y widgets para ofrecer experiencias de aprendizaje personalizadas a tu audiencia.

## El problema que resuelve Experience Builder

Experience Builder aborda los desafíos comunes a los que se enfrentan las organizaciones a la hora de personalizar sus portales de aprendizaje sin una ayuda técnica significativa ni costosos integradores de sistemas. Reduce la brecha entre dos opciones principales:

* La experiencia estándar inmediata, que ofrece una personalización limitada y puede hacer que todos los portales de aprendizaje tengan un aspecto similar.
* Una implementación descentralizada, que permite portales completamente personalizados e interactivos, pero que conlleva importantes desafíos, como un plazo de comercialización prolongado (normalmente de 3 a 6 meses), la dependencia de un equipo de desarrollo y unos costes elevados.

Experience Builder ofrece una base intermedia que permite la creación de portales de la marca y recorridos de aprendizaje únicos sin los elevados costes y gastos generales de desarrollo de un enfoque descentralizado.

## Principales ventajas de usar Experience Builder

La funcionalidad de utilizar páginas, widgets o menús ofrece varias ventajas clave:

* **Personalización sencilla**: Puedes diseñar portales que combinen con precisión tu marca con encabezados, pies de página, logotipos y diseños personalizados. La capacidad de incorporar HTML personalizado, CSS y JavaScript proporciona un control avanzado para una experiencia totalmente de marca.
* **Aprendizaje personalizado**: Una ventaja clave es la capacidad de proporcionar diferentes experiencias a distintos alumnos. Puede configurar páginas y menús para grupos de usuarios específicos (por ejemplo, equipos de ventas, diseñadores o ingenieros), asegurándose de que solo vean contenido relevante para ellos. Esto es ideal para crear campañas de microaprendizaje dirigidas a equipos o períodos de tiempo específicos.
* **No hay código/interfaz de código bajo**: Los administradores pueden crear experiencias de aprendizaje a través de una interfaz visual guiada en lugar de escribir código. Este enfoque permite a los administradores crear y administrar portales de marca sofisticados sin necesidad de conocimientos técnicos o amplios conocimientos de codificación.
* **Global and mobile-ready**: Experience Builder admite la creación de páginas multilingües para atender a diversas audiencias globales y está diseñado para ser compatible con dispositivos móviles, lo que garantiza una experiencia fluida para los alumnos en ordenadores de escritorio, teléfonos y tabletas.

## Casos prácticos habituales

Experience Builder se puede utilizar para varios escenarios de aprendizaje en los que participen empleados internos y usuarios externos.

* **Portales de formación basados en funciones**: Las organizaciones con necesidades de formación específicas del departamento, como una empresa financiera con equipos de ventas y éxito del cliente independientes, pueden crear páginas de aprendizaje dedicadas para cada grupo para garantizar que el contenido sea muy relevante.
* **Páginas de aprendizaje específicas para eventos**: Puedes crear páginas temporales especializadas para eventos corporativos como un Tech Summit o un Kick Off de ventas. Estas páginas pueden incluir información de la sesión, listas de oradores y un widget de calendario de eventos, y solo se pueden dirigir al equipo relevante durante un periodo específico antes de volver a la experiencia estándar del portal.
* **Academias de clientes**: Experience Builder permite a las agencias crear academias orientadas al cliente que reflejen su identidad de marca, lo que les permite conseguir una experiencia personalizada sin el tiempo y el coste asociados a una creación descentralizada.

## Flujos de trabajo de portal externos autenticados

Las academias orientadas al cliente creadas con Experience Builder se gestionan por completo en Adobe Learning Manager. Estos portales utilizan la autenticación, los permisos y el marco de seguridad integrados de Adobe Learning Manager.

Cada alumno externo debe iniciar sesión en Adobe Learning Manager y ser abonado de al menos un grupo de usuarios. Actualmente, Experience Builder no es compatible con portales no autenticados ni públicos. Todas las experiencias personalizadas requieren que los alumnos inicien sesión en Adobe Learning Manager.

Los administradores pueden usar la opción **[!UICONTROL Menú]** de Experience Builder para asignar páginas personalizadas como páginas de destino para grupos de usuarios específicos. Cuando los alumnos de ese grupo inician sesión, Adobe Learning Manager los dirige automáticamente a la página de inicio asignada, lo que crea una experiencia personalizada y de marca para esa audiencia, como la formación del cliente, la capacitación de socios o la incorporación.

### Requisitos y limitaciones

* Autenticación obligatoria: El contenido personalizado, las páginas personalizadas y los menús solo están disponibles para los usuarios autenticados en Adobe Learning Manager.
* Asignación de grupo de usuarios: Los alumnos deben agregarse a los grupos de usuarios correctos para acceder a sus páginas de aterrizaje y menús designados.
* Páginas de destino basadas en grupos: La configuración de la página de aterrizaje se aplica a todos los miembros de un grupo de usuarios, lo que garantiza experiencias uniformes para audiencias similares.
* Ámbito de personalización: Experience Builder admite una amplia personalización de la interfaz de usuario y el diseño mediante widgets, HTML e iFrames. Sin embargo, las integraciones avanzadas como el comercio electrónico, el SSO federado o las conexiones de datos externos pueden requerir una implementación híbrida o descentralizada.

### Flujo de trabajo de configuración de portal externo

* Definir grupos de usuarios: Cree o identifique grupos en ALM que representen a sus audiencias externas (por ejemplo, clientes, socios o distribuidores). Vea [Grupos de usuarios en Adobe Learning Manager](/help/migrated/administrators/feature-summary/user-group.md) para obtener más información sobre los grupos de usuarios.
* Asignar alumnos a grupos: Añada cada alumno externo al grupo de usuarios correspondiente para que se le dirija a la experiencia de portal correcta después de iniciar sesión.
* Páginas del portal de diseño: Utilice Experience Builder para crear páginas de marca con widgets, HTML y componentes de iFrame de Adobe Learning Manager. Vea [Crear una página personalizada en Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/create-a-page.md) para obtener más información.
* Configurar menús y páginas de destino: En el Creador de menús, asigne a cada grupo de usuarios un menú único y designe su página de portal personalizada como página de destino. Vea [Crear un menú](/help/migrated/administrators/feature-summary/experience-builder/create-a-menu.md) para obtener más información.
* Prueba y Publish: Verifique la navegación, la visibilidad del contenido y el enrutamiento de página para cada grupo de usuarios antes de publicar el portal.
