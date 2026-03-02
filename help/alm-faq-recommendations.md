---
title: Ciclo de vida de la cuenta administrativa de Adobe Learning Manager
description: Este documento proporciona un resumen completo de las funciones de cumplimiento, configuración y administración de cuentas de seguridad de Adobe Learning Manager (ALM) alineadas con las recomendaciones de FedRAMP.
jcr-language: en-us
source-git-commit: 06051e44c0a6bc8ae60e44272ba088f2f6ff281f
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%

---


# Recomendaciones de seguridad de Adobe Learning Manager

## ¿Qué opciones de configuración relevantes para la seguridad solo pueden utilizarlas los administradores personalizados o los administradores de integración en Adobe Learning Manager y cuáles son sus implicaciones de seguridad?

Los dos tipos de cuentas privilegiadas de Adobe Learning Manager (Custom Administrator y Integration Administrator) tienen cada uno un conjunto definido de configuraciones relevantes para la seguridad con implicaciones documentadas.

### Administrador personalizado: funciones que pueden desempeñar:

* Las funciones personalizadas las configura el administrador completo en Administración de ALM > Usuarios > Funciones personalizadas. Se puede conceder acceso a un administrador personalizado a una o varias de estas categorías de permisos: Privilegios de cuenta (anuncios, interacción, aptitudes, administración de usuarios), Privilegios de funciones (catálogos, informes, etiquetas) y Privilegios de objetos de aprendizaje (cursos, certificaciones, rutas de aprendizaje).
* El ámbito es la configuración más sensible a la seguridad: una función personalizada se puede restringir a grupos de usuarios específicos y/o catálogos específicos. Sin restricciones de ámbito, una función personalizada tiene acceso efectivo en toda la plataforma a las funciones que se le han otorgado, lo que le permite ocupar el espacio de un administrador completo.
* Si se concede acceso a Configuración a una función personalizada en Privilegios de cuenta, ese administrador personalizado puede modificar los métodos de inicio de sesión, la configuración de notificaciones y las configuraciones de nivel de cuenta, un privilegio de gran impacto que solo se debe conceder con una justificación empresarial explícita.
* Un administrador personalizado con acceso a Configuración que también tenga acceso a la entidad Usuarios puede asignarse a sí mismo la función de administrador completa, con lo que pasará a tener un control administrativo total.

### Administrador de integración: funciones que pueden desempeñar:

* Los administradores de integración gestionan los registros de las aplicaciones de OAuth 2.0 en Administrador de integración > Aplicaciones > Registrar. Estos seleccionan uno de los seis ámbitos de OAuth, que van desde el acceso de lectura del alumno hasta el acceso de lectura/escritura de la función de administrador. El ámbito de lectura/escritura de administrador concede a la aplicación registrada los mismos privilegios que a un administrador completo a través de la API.
* Los administradores de integración configuran FTP, SFTP, Salesforce, Workday y otros conectores que importan registros de usuarios, asignaciones de funciones y finalizaciones de cursos, y exportan datos de la plataforma a sistemas externos.
* Ámbito de OAuth para aplicaciones registradas: ámbito mínimo requerido. No conceda nunca acceso de lectura/escritura a la función de administrador a menos que sea estrictamente necesario.
* Los administradores de integración configuran webhooks que envían datos de eventos de ALM en tiempo real (inscripciones, finalizaciones, cambios de funciones) a direcciones URL externas. Un extremo de webhook comprometido o configurado incorrectamente es un riesgo de exfiltración de datos.
* Los administradores de integración pueden configurar integraciones de LTI. Una vez habilitado, LTI no se puede deshabilitar. Las credenciales LTI expuestas permiten el acceso no autorizado al contenido del curso desde plataformas LMS externas.


## ¿Cuáles son los valores predeterminados seguros recomendados para las cuentas administrativas y privilegiadas de nivel superior en Adobe Learning Manager y dónde se configuran?

### Valores predeterminados de la cuenta de administrador de nivel superior (configurados en el primer aprovisionamiento):

* Método de inicio de sesión para usuarios internos: inicio de sesión único (SSO) mediante SAML 2.0: configurado en Administración de ALM > Configuración > Métodos de inicio de sesión. No uses Adobe ID para empleados o administradores.
* Verificación en dos pasos (2FA): obligatoria para todos los usuarios: configurada en Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración de autenticación.
* Duración máxima de la sesión: 8 horas (o según la política de la organización): configurada en Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración avanzada.
* Tiempo máximo de inactividad: 30 minutos (o según la política de la organización): la misma ubicación que antes.
* Eliminación automática de usuarios inactivos: se activa con un período de retención definido por la organización (p. ej., 90 días de inactividad): Administración de ALM > Configuración > General.
* Vencimiento del perfil de usuario externo: se establece en cada perfil externo en la creación: Administrador de ALM > Usuarios > Externo. Sin perfiles externos indefinidos.
* Restricciones de acceso a IP: restrinja los intervalos de IP aprobados cuando sea posible: Admin Console > Configuración > Configuración avanzada.

### Valores predeterminados de la función de administrador personalizado (configurados al crear cada función):

* Ámbito de OAuth para aplicaciones registradas: ámbito mínimo requerido. No conceda nunca acceso de lectura/escritura a la función de administrador a menos que sea estrictamente necesario.
* Ámbito de la función personalizada: restrinja a grupos de usuarios específicos y catálogos específicos. No cree funciones personalizadas con el ámbito Todos los usuarios y Todos los catálogos a menos que la función lo requiera de forma genuina.
* Acceso a la configuración en funciones personalizadas: no se concede a menos que la función específica lo requiera, dado el riesgo de escalación de privilegios.

### Valores predeterminados del administrador de integración:

* Ámbito de API OAuth: seleccione el ámbito más restrictivo que cumpla los requisitos de la integración. No conceda lectura/escritura de administrador a aplicaciones que solo necesiten acceso de lectura del alumno.
* Credenciales de conector, credenciales de LTI y direcciones URL de webhook: tratar como secretos confidenciales; nunca compartir por correo electrónico ni confirmar en el control de código fuente.

## ¿Ofrece Adobe Learning Manager una forma de que los administradores comparen la configuración actual de la cuenta con los valores predeterminados seguros recomendados?

Adobe Learning Manager no dispone de un panel de comparación dedicado que muestre automáticamente la configuración actual junto con los valores predeterminados seguros recomendados. Sin embargo, tres capacidades de plataforma permiten a los administradores auditar y comparar las configuraciones actuales de forma manual o mediante programación.

### Informe de funciones personalizadas: asignaciones de funciones con privilegios actuales:

En ALM, vaya a Administración > Usuarios > Funciones personalizadas y haga clic en Descargar (arriba a la derecha) para exportar un archivo CSV de todas las funciones personalizadas, sus conjuntos de permisos y sus asignaciones de ámbito.

### API ALM REST: recuperación de configuración programática:

* El extremo de GET/cuenta devuelve datos de configuración de nivel de cuenta en formato JSON, accesibles mediante el ámbito OAuth de la función de administrador. Los clientes pueden llamar a este extremo mediante programación.
* El extremo GET/usuarios (con include=role filter) devuelve las asignaciones de funciones actuales para todos los usuarios, lo que permite detectar automáticamente las asignaciones de funciones inesperadas. Utilice la API de trabajos para las exportaciones de usuarios en bloque.

## ¿Pueden los administradores exportar las configuraciones y los ajustes actuales relevantes para la seguridad desde Adobe Learning Manager en un formato legible por el equipo?

Adobe Learning Manager admite la exportación de datos de configuración relevantes para la seguridad a través de varios mecanismos. Ninguna exportación produce una instantánea completa de todas las configuraciones de seguridad a la vez, pero las siguientes exportaciones cubren de forma conjunta todo el ámbito de los datos relevantes para la seguridad.

### Registro de auditoría del Admin Console: exportación mediante CSV de todos los cambios de autenticación y función:

* En Adobe Admin Console, vaya a **Detalles > Registros > Registro de auditoría**, aplique los filtros necesarios y haga clic en **Exportar CSV**
* El archivo CSV exportado registra todas las acciones administrativas, incluidos los cambios en la aplicación de 2FA, los cambios en el límite de sesiones, las asignaciones y eliminaciones de funciones de administrador, las eliminaciones de usuarios y los cambios en los derechos de los productos, todo ello con marcas de hora e identidad de actores.
* Los datos se conservan durante 90 días. Los usuarios de Global Admin Console pueden exportar registros en todas las organizaciones.

### API ALM REST: exportación JSON de asignaciones de funciones y configuración de cuentas actuales:

* `GET /account`: devuelve la configuración de nivel de cuenta en JSON, incluidos los datos de configuración de inicio de sesión activo y los metadatos de cuenta.
* `GET /users?include=role`: devuelve todos los usuarios con sus funciones actualmente asignadas en JSON.
* `GET /userGroups`: devuelve todos los grupos de usuarios y su pertenencia, relevantes para la auditoría del ámbito de función personalizada.
* Todas las respuestas de API son JSON (`vnd.api+json`). La autenticación utiliza OAuth 2.0 con el ámbito de lectura y escritura de la función de administrador.

### Exportación de CSV de funciones personalizadas: definiciones de funciones con privilegios actuales:

* Administración de ALM > Usuarios > Funciones personalizadas > Descargar exporta un archivo CSV de todas las definiciones de funciones personalizadas, sus categorías de permisos y las asignaciones de ámbito.
* Esta exportación se puede utilizar como una instantánea legible por el equipo de la configuración actual de la cuenta con privilegios.

### API de trabajos: datos de usuarios y funciones en bloque:

* La API de trabajos de ALM admite la generación a petición de informes de usuarios (incluidas las asignaciones de funciones) en formato CSV. Estas pueden programarse y consumirse mediante cumplimiento externo o herramientas SIEM.

Consulte el [Manual del desarrollador de aplicaciones de Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) para obtener más información.

## ¿Ofrece Adobe Learning Manager una API a través de la cual se pueda ver y ajustar mediante programación la configuración relevante para la seguridad?

Adobe Learning Manager proporciona una versión 2 de API REST completa que permite ver y ajustar mediante programación la configuración relevante para la seguridad mediante la autenticación OAuth 2.0. A continuación se indican las funciones de API específicas relacionadas con la configuración de seguridad:

### Autenticación y ámbito

* El administrador de integración registra las aplicaciones en **Administrador de integración > Aplicaciones > Registrar**. El ID de cliente y el secreto de OAuth 2.0 se emiten por aplicación.
* Hay seis ámbitos disponibles. Para la administración de la configuración de seguridad, se requiere **acceso de lectura y escritura de la función de administrador**. Esto concede a la aplicación el mismo acceso que a un administrador completo a través de la API.
* Los tokens de acceso se obtienen a través del código de autorización de OAuth estándar o del flujo de credenciales de cliente.\
  **URL base:**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Administración de usuarios y funciones mediante API

* `GET /users`: recuperar todos los usuarios y sus funciones actuales
* `POST /users`: aprovisionar nuevos usuarios mediante programación
* `PATCH /users/{id}`: actualizar los atributos de usuario, incluidas las asignaciones de funciones
* `DELETE /users/{id}`: deshabilitar una cuenta de usuario
* `POST /users/{id}/purge`: purgar permanentemente un usuario y todos los registros asociados

### Recuperación de configuración de cuenta

* `GET /account`: devuelve la configuración de nivel de cuenta, incluidos los datos de configuración de cuenta en formato JSON, incluidos campos como:
   * `complianceLabelDefaultID`
   * `showComplianceLabel`
   * `custom_injections`

### API de administración de usuarios de Adobe (nivel de Admin Console)

* La API de administración de usuarios de Adobe (UMAPI) proporciona acceso mediante programación a las operaciones del Admin Console:
   * Aprovisionamiento de usuarios
   * Asignación de derechos de producto
   * Asignación de funciones de administrador del sistema en el nivel de organización
* UMAPI es independiente de la API ALM REST y funciona en el nivel de organización de Adobe. Utilícelo para automatizar las asignaciones de funciones de Admin Console y el aprovisionamiento de usuarios.

## ¿Publica Adobe Learning Manager su guía de configuración segura (los valores predeterminados recomendados) en un formato legible por el equipo, como OSCAL, JSON o YAML?

Adobe Learning Manager no publica actualmente su Guía de configuración segura en un formato legible por el equipo.

## ¿La Guía de configuración segura de Adobe Learning Manager está disponible públicamente sin necesidad de iniciar sesión ni de acceder a ella de forma especial?

Sí. La Guía de configuración segura de Adobe Learning Manager está disponible públicamente en Adobe Experience League. No se requiere ninguna cuenta, inicio de sesión ni licencia para acceder a ella.

Lo que está disponible públicamente:

* FRR-RSC-01: Guía de administración segura: guía completa del ciclo de vida de las cuentas administrativas de nivel superior.
* FRR-RSC-02: Implicaciones y configuración de seguridad administrativa: todas las configuraciones relevantes para la seguridad, sus implicaciones y los valores predeterminados recomendados.

## ¿Proporciona Adobe Learning Manager un historial de versiones y versiones que permite a las agencias realizar un seguimiento de los cambios en la configuración relevante para la seguridad y de los valores predeterminados recomendados a lo largo del tiempo?

Adobe Learning Manager mantiene un historial de versiones detallado y disponible públicamente para cada actualización del producto. En cada versión se documentan los cambios relevantes para la seguridad en la configuración administrativa, las capacidades de autenticación, los puntos finales de la API y las funciones de administración de funciones.

### Notas de la versión de ALM: Numerado, Historial de cambios acumulativos

* Adobe publica notas de la versión numeradas para cada actualización de Adobe Learning Manager (p. ej., *Actualización 100*, *Actualización 99*).
* Estos se publican en **Experience League** y el documento:
   * Funciones nuevas
   * Cambios en la configuración existente
   * Adiciones y eliminaciones de API
   * Cambios en los conectores
   * Capacidades en desuso
* Cada nota de la versión incluye una sección dedicada para **cambios en la API**, que incluye:
   * Nuevos puntos finales
   * Campos de respuesta modificados
   * Rechazos
   * Estos son directamente relevantes para las capacidades de configuración relevantes para la seguridad.

### Páginas &quot;Novedades&quot;: resúmenes de funciones por lanzamiento

* Cada versión principal tiene una página **&quot;Novedades&quot;** dedicada que documenta las nuevas funciones relevantes para la seguridad con contexto.
* Algunos ejemplos de actualizaciones documentadas relacionadas con la seguridad son:
   * Cambios en el control de permisos de funciones personalizadas
   * Adición de visibilidad de permisos creados mediante CSV para funciones personalizadas
   * Cambios de limitación de velocidad de API

### Lista de API en desuso: registro autorizado de capacidades de API eliminadas

* Adobe mantiene una página dedicada de **depreciaciones de API** que muestra todos los puntos finales de API ALM obsoletos y eliminados, incluida la versión de lanzamiento en la que se produjo cada obsolescencia.
* Algunos ejemplos de depreciaciones relevantes para la seguridad son:
   * Cambios en el comportamiento de ordenación e invalidación del extremo `GET /users`
   * Requisitos de filtro de notificación y fecha de informe

