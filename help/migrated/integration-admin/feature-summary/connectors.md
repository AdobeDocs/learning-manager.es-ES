---
description: Información general sobre cada conector compatible con ALM
jcr-language: en_us
title: Descripción general de los conectores compatibles con ALM
contentowner: mmanuel
source-git-commit: bd80ca31ff633e21ec81e717772e43989f0d9aae
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 6%

---


# Conectores de Adobe Learning Manager

## Introducción

Adobe Learning Manager (ALM) proporciona un conjunto completo de conectores que permiten una integración perfecta con aplicaciones de terceros y sistemas empresariales. Estos conectores sirven de puente entre el sistema de gestión de aprendizaje y las plataformas externas, lo que facilita la sincronización automatizada de datos, la gestión de usuarios, la importación de contenido y las exportaciones de registros de aprendizaje.

Este documento sirve como guía de referencia completa para comprender y seleccionar los conectores apropiados para el ecosistema de aprendizaje de su organización. Tanto si buscas integrarte con sistemas de RR. HH., plataformas de comercio electrónico, herramientas de reuniones virtuales o soluciones de inteligencia empresarial.

Para obtener una lista completa de los conectores compatibles con Adobe Learning Manager, consulte los artículos de conectores anidados justo debajo de este artículo en la Tabla de contenido de la izquierda.

>[!NOTE]
>
>Esta función está parcialmente disponible en entornos autorizados por FedRAMP. Consulte [Disponibilidad de funciones en entornos FedRAMP](/help/migrated/feature-availability-in-fedramp-authorized-environment.md) para obtener más información.

>[!NOTE]
>
>Con la versión de noviembre de 2022 de Adobe Learning Manager, Zoom ha dejado de usar la autenticación [JWT para junio de 2023](https://developers.zoom.us/docs/internal-apps/s2s-oauth/). Por lo tanto, el conector de Zoom con JWT seguirá funcionando hasta la fecha indicada, pero recomendamos a los usuarios que creen una aplicación OAuth de servidor a servidor para reemplazar esta función en la cuenta. Todas las conexiones nuevas tendrán la autenticación de OAuth de Zoom de forma predeterminada.

## Categorías de conectores

Los conectores de Adobe Learning Manager se pueden organizar en varias categorías funcionales en función de su finalidad principal y de sus capacidades de integración:

| Categoría | Propósito | Conectores de ejemplo |
|---------|--------|-------------------|
| Transferencia de datos | Intercambio de datos basado en archivos y operaciones en bloque | FTP, FTP personalizado, Box |
| Clase virtual | Integración de reuniones y formación en directo | Microsofts Teams, Zoom, Adobe Connect |
| Sistemas empresariales | Integración de RR. HH. y sistemas empresariales | Workday, Salesforce, ADFS |
| Plataformas de contenido | Integración de contenido de aprendizaje externo | LinkedIn Learning, Harvard ManageMentor, getAbstract |
| Analytics &amp; BI | Creación de informes y visualización de datos | Power BI, Acceso a datos de formación |
| Autenticación | Seguridad y gestión de identidades | ADFS (funciones de SSO) |
| Comercio electrónico y marketing | Integración de marketing y ventas | Adobe Commerce, Marketo Engage |

## Conectores de transferencia de datos y administración de archivos

Estos conectores facilitan el intercambio automatizado de datos a través de protocolos de transferencia de archivos, lo que permite operaciones en bloque y comunicación entre sistemas.

### Conector FTP de Adobe Learning Manager

El conector de FTP permite a las organizaciones automatizar la sincronización de datos entre Adobe Learning Manager y sistemas externos mediante el protocolo de transferencia de archivos, de uso generalizado. Este conector admite variantes seguras, incluidos SFTP (SSH File Transfer Protocol, Protocolo de transferencia de archivos SSH) y FTPS (FTP Secure, Protocolo de transferencia de archivos SSH) para mejorar la seguridad.

#### Capacidades clave:

- Cargar y descargar archivos entre Adobe Learning Manager y servidores remotos.
- Intercambio automatizado de datos para la información del usuario y los registros de formación.
- Compatibilidad con protocolos de transferencia de archivos seguros (SFTP, FTPS).
- Procesamiento por lotes de grandes conjuntos de datos.

Para obtener más información, consulte [Conector de FTP](/help/migrated/integration-admin/feature-summary/ftp-connector.md).

### Conector de FTP personalizado

El conector de FTP personalizado proporciona funciones de transferencia de archivos más sofisticadas, admite formatos de datos estructurados e intercambios de instrucciones xAPI. Este conector se ha diseñado para las organizaciones que requieren un control más granular sobre sus procesos de intercambio de datos.

#### Capacidades clave:

- Importa y exporta datos de usuarios mediante archivos CSV estructurados.
- Gestiona registros de aprendizaje e instrucciones de xAPI.
- Procesamiento automatizado de archivos desde las carpetas FTP designadas.
- Funciones de seguridad mejoradas para la transferencia de datos confidenciales.

Para obtener más información, consulte [Conector de FTP personalizado](/help/migrated/integration-admin/feature-summary/custom-ftp-connector.md).

### Conector de Box

El conector de Box aprovecha la plataforma de almacenamiento en la nube de Box para facilitar la sincronización perfecta de datos entre sistemas externos y Adobe Learning Manager. Este conector es especialmente útil para las organizaciones que ya utilizan Box para la administración de archivos.

#### Capacidades clave:

- Almacenamiento de archivos y sincronización en la nube
- Procesamiento automatizado de datos CSV.
- Integración con los flujos de trabajo de Box existentes
- Actualizaciones de datos en tiempo real desde las carpetas designadas.

Para obtener más información, consulte [Conector de Box](/help/migrated/integration-admin/feature-summary/box-connector.md).

## Conectores de clase virtual y reunión

Estos conectores integran Adobe Learning Manager con las plataformas de videoconferencia y reuniones virtuales más populares, lo que permite una distribución perfecta de sesiones de formación en directo.

### Conector de Microsoft Teams

El conector de Microsofts Teams transforma Adobe Learning Manager en una solución completa de clase virtual al integrarse directamente con las funciones de reunión de equipos. Este conector es esencial para las organizaciones que utilizan el ecosistema de Microsoft 365.

#### Capacidades clave:

- Programa sesiones de clase virtual directamente desde Adobe Learning Manager.
- Creación y gestión automáticas de reuniones de equipos.
- Acceso perfecto de los alumnos sin vínculos de reunión independientes.

Para obtener más información, consulte [Conector de MS Teams](/help/migrated/integration-admin/feature-summary/install-microsoft-teams-connector.md).

### Conector de Zoom

El conector de Zoom permite a las organizaciones aprovechar las sólidas funciones de videoconferencia de Zoom directamente en su entorno de Adobe Learning Manager, lo que proporciona una experiencia perfecta tanto para instructores como para alumnos.

#### Capacidades clave:

- Programación directa de reuniones de Zoom desde Adobe Learning Manager.
- Generación y distribución automatizadas de vínculos de reunión.
- Supervisión de la asistencia en tiempo real.
- Integración de gestión y reproducción de grabaciones.
- Compatibilidad con salas de grupo de trabajo para sesiones interactivas.

Para obtener más información, consulte [Conector de Zoom](/help/migrated/integration-admin/feature-summary/zoom-connector.md).

### Conector de Adobe Connect

El conector de Adobe Connect ofrece una profunda integración con la plataforma de clase virtual de Adobe, que ofrece funciones avanzadas para experiencias de aprendizaje online interactivas.

#### Capacidades clave:

- Funciones interactivas avanzadas (encuestas, cuestionarios, sesiones en grupo).
- Herramientas de presentación y uso compartido de pantalla de alta calidad.
- Grabación y reproducción completas de sesiones.
- Experiencia de clase virtual optimizada para dispositivos móviles

Para obtener más información, consulte [Conector de Adobe Connect](/help/migrated/integration-admin/feature-summary/adobe-connect-connector.md).

## Conectores de integración de sistemas empresariales

Estos conectores permiten a Adobe Learning Manager integrarse con los principales sistemas empresariales, lo que facilita la gestión automatizada de usuarios y la sincronización de datos organizativos.

### Conector de Workday

El conector de Workday crea un puente perfecto entre su sistema de RR. HH. y la plataforma de gestión de aprendizaje, lo que garantiza que los registros de los empleados, las estructuras organizativas y las asignaciones de funciones permanezcan sincronizados en ambos sistemas.

#### Capacidades clave:

- Aprovisionamiento automatizado de usuarios desde Workday.
- Sincronización de datos de empleados en tiempo real.
- Asignación de jerarquía organizativa.
- Automatización de la asignación de aprendizaje basada en funciones

Para obtener más información, consulte [Conector de Workday](/help/migrated/integration-admin/feature-summary/workday-connector.md).

### Conector de Salesforce

El conector de Salesforce permite a las organizaciones integrar su sistema de gestión de relaciones con los clientes con iniciativas de aprendizaje, lo que crea oportunidades para la formación en ventas, la educación del cliente y el seguimiento del rendimiento.

#### Capacidades clave:

- Importación automatizada de usuarios desde Salesforce.
- Asignación de campos de datos personalizados.
- Exportación de registros de aprendizaje a Salesforce.
- Correlación del rendimiento de ventas con la finalización de la formación.
- Gestión de programas de formación de clientes.

Para obtener más información, consulte [Conector de Salesforce](/help/migrated/integration-admin/feature-summary/salesforce-connector.md).

### Conector ADFS (Servicios de federación de Active Directory)

El conector de ADFS permite a las organizaciones implementar autenticación y autorización de nivel empresarial, lo que permite a los usuarios obtener acceso a Adobe Learning Manager mediante sus credenciales de Active Directory existentes.

#### Capacidades clave:

- Implementación del inicio de sesión único (SSO)
- Cumplimiento normativo de seguridad empresarial
- Autenticación de usuario perfecta
- Importación automatizada de usuarios
- Capacidad de programar
- Capacidad de filtrar

Para obtener más información, consulte [Conector de ADFS](/help/migrated/integration-admin/feature-summary/adfs-connector.md).

## Conectores de contenido y plataforma de aprendizaje

Estos conectores amplían el catálogo de aprendizaje mediante la integración de bibliotecas de contenido externas y plataformas de aprendizaje especializadas.

### Conector de LinkedIn Learning

LinkedIn Learning Connector proporciona acceso a la extensa biblioteca de cursos de desarrollo profesional de LinkedIn, lo que permite a las organizaciones complementar su formación interna con contenido externo líder del sector.

#### Capacidades clave:

- Acceso al catálogo completo de cursos de LinkedIn Learning.
- Descubrimiento e importación automatizados de cursos.
- Seguimiento del progreso del alumno en Adobe Learning Manager.

Para obtener más información, consulte [Conector de LinkedIn](/help/migrated/integration-admin/feature-summary/linkedin-learning-connector.md).

### Conector de Harvard ManageMentor

El conector de Harvard ManageMentor incorpora contenido de formación en liderazgo y gestión de primera categoría directamente en su entorno de Adobe Learning Manager, lo que proporciona acceso a los reconocidos recursos educativos de Harvard Business School.

#### Capacidades clave:

- Acceso premium al contenido de Harvard Business School.
- Módulos de gestión y desarrollo de liderazgo.
- Organización e importación de contenido perfectas.

Para obtener más información, consulte el [conector de Harvard ManageMentor](/help/migrated/integration-admin/feature-summary/harvard-managementor-connector.md).

### Conector de getAbstract

El conector de getAbstract proporciona acceso a resúmenes concisos de libros de negocios e información profesional, lo que permite a las organizaciones ofrecer aprendizaje continuo a través de formatos de contenido digeribles.

#### Capacidades clave:

- Acceso a los resúmenes e información de los libros de negocios.
- Seguimiento e informes de datos de uso.
- Creación automatizada de registros de finalización.

Para obtener más información, consulte [conector getAbstract](/help/migrated/integration-admin/feature-summary/getabstract-connector.md).

## Conectores de inteligencia empresarial y análisis

Estos conectores permiten funciones avanzadas de creación de informes, visualización de datos e inteligencia empresarial mediante la integración de datos de aprendizaje con plataformas de análisis externas.

### Conector de Power BI

El conector de Power BI transforma tus datos de aprendizaje en información empresarial procesable al sincronizar automáticamente las métricas de aprendizaje con la potente plataforma de inteligencia empresarial de Microsoft.

#### Capacidades clave:

- Sincronización de datos de aprendizaje en tiempo real
- Creación y administración de paneles personalizados.
- Visualización e informes avanzados de datos.
- Integración de transcripciones de alumnos e informes de aptitudes.

Para obtener más información, consulte [Conector de Power BI](/help/migrated/integration-admin/feature-summary/power-bi-connector.md).

### Conector de Training Data Access

El conector Training Data Access permite a las organizaciones crear interfaces de aprendizaje personalizadas y experiencias de aprendizaje descentralizadas, proporcionando acceso a través de API a los datos de formación y a la información del curso.

**Capacidades clave:**

- Acceso mediante API pública a los datos de cursos y rutas de aprendizaje.
- Compatibilidad con el desarrollo de interfaces de usuario personalizadas.
- Creación de experiencias de aprendizaje descentralizadas
- Funciones avanzadas de búsqueda y filtrado.

Para obtener más información, consulte [Conector de acceso a datos de formación](/help/migrated/integration-admin/feature-summary/training-data-access-connector.md).

## Conectores de comercio electrónico y marketing

Estos conectores permiten la monetización del contenido de aprendizaje y la integración con plataformas de automatización de marketing.

### Conector de Adobe Commerce

El conector de Adobe Commerce transforma Adobe Learning Manager en una plataforma completa de aprendizaje y comercio que permite a las organizaciones vender cursos, certificaciones y programas de formación a través de una experiencia de comercio electrónico totalmente integrada.

**Capacidades clave:**

- Integración perfecta de plataformas de comercio electrónico.
- Catálogo de cursos y gestión de precios.
- Procesamiento e inscripción de pagos automatizados

Para obtener más información, consulte [Conector de Adobe Commerce](/help/migrated/integration-admin/feature-summary/adobe-commerce-connector.md).

### Conector de Marketo Engage

El conector de Marketo Engage crea potentes sinergias entre las actividades de aprendizaje y las campañas de marketing, lo que permite a las organizaciones aprovechar la participación educativa para la maduración de clientes potenciales y el desarrollo de clientes.

#### Capacidades clave:

- Creación y actualizaciones automatizadas de oportunidades
- Seguimiento de la actividad de aprendizaje para información de marketing
- Activadores de eventos de inscripción y finalización de cursos.

Para obtener más información, consulte [Conector del Marketo Engage](/help/migrated/integration-admin/feature-summary/marketo-engage-connector.md).
