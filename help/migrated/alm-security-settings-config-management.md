---
title: 'Adobe Learning Manager: configuración de seguridad y administración de la configuración'
description: Este documento describe los tipos de cuentas administrativas de Adobe Learning Manager, la configuración relacionada con la seguridad, los valores predeterminados seguros recomendados, las funciones de la API, la funcionalidad de exportación, los métodos de comparación de la configuración, las prácticas de publicación y el historial de versiones. Proporciona instrucciones detalladas sobre cómo funcionan las cuentas privilegiadas, sus implicaciones de seguridad y cómo se admite la administración de configuración en toda la plataforma.
jcr-language: en-us
exl-id: a2e34104-c417-407f-af85-9f3f4b2a9fcb
source-git-commit: 3188d7f5593aeee87978e1e46456f01e1f41d57b
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# Configuración de seguridad y administración de la configuración

Esta guía proporciona respuestas detalladas a las recomendaciones de FedRAMP (FRR-RSC-03 a FRR-RSC-08) para Adobe Learning Manager (ALM). Describe las prácticas recomendadas de seguridad, los valores predeterminados seguros recomendados y las herramientas para auditar, exportar y administrar la configuración de cuentas privilegiadas. El documento está diseñado para administradores y equipos de cumplimiento para garantizar la configuración y administración seguras de las cuentas de ALM.

También destaca las áreas en las que ALM cumple o parcialmente los estándares FedRAMP, con referencias a documentación de apoyo y recursos disponibles en Adobe Experience League.

+++¿Qué opciones de configuración relevantes para la seguridad solo pueden utilizarlas los administradores personalizados o los administradores de integración en Adobe Learning Manager y cuáles son sus implicaciones de seguridad?

Los dos tipos de cuentas privilegiadas de Adobe Learning Manager: Administrador personalizado y Administrador de integración. Cada uno tiene un conjunto definido de configuraciones relevantes para la seguridad con implicaciones documentadas.

**Administrador personalizado: qué pueden hacer**:

* Las funciones personalizadas las configura el administrador completo en Administración de ALM > Usuarios > Funciones personalizadas. Se puede conceder acceso a un administrador personalizado a una o varias de estas categorías de permisos: Privilegios de cuenta (anuncios, interacción, aptitudes, administración de usuarios), Privilegios de funciones (catálogos, informes, etiquetas) y Privilegios de objetos de aprendizaje (cursos, certificaciones, rutas de aprendizaje).
* El ámbito es la configuración más sensible a la seguridad: una función personalizada se puede restringir a grupos de usuarios específicos y/o catálogos específicos. Sin restricciones de ámbito, una función personalizada tiene acceso efectivo en toda la plataforma a las funciones que se le han otorgado, lo que le permite ocupar el espacio de un administrador completo.
* Si se concede acceso a Configuración a una función personalizada en Privilegios de cuenta, ese administrador personalizado puede modificar los métodos de inicio de sesión, la configuración de notificaciones y las configuraciones de nivel de cuenta, un privilegio de gran impacto que solo se debe conceder con una justificación empresarial explícita.

**Administrador de integración: qué pueden hacer**:

* Los administradores de integración gestionan los registros de las aplicaciones de OAuth 2.0 en Administrador de integración > Aplicaciones > Registrar. Estos seleccionan uno de los seis ámbitos de OAuth, que van desde el acceso de lectura del alumno hasta el acceso de lectura/escritura de la función de administrador. El ámbito de lectura/escritura de administrador concede a la aplicación registrada los mismos privilegios que a un administrador completo a través de la API.
* Los administradores de integración configuran FTP, SFTP, Salesforce, Workday y otros conectores que importan registros de usuarios, asignaciones de funciones y finalizaciones de cursos, y exportan los datos de la plataforma a sistemas externos.
* Los administradores de integración configuran webhooks que envían datos de eventos de ALM en tiempo real (inscripciones, finalizaciones, cambios de funciones) a direcciones URL externas. Un extremo de webhook comprometido o configurado incorrectamente es un riesgo de exfiltración de datos.
* Los administradores de integración pueden configurar integraciones de LTI. Una vez habilitado, LTI no se puede deshabilitar.

**Referencias**:

* [Funciones personalizadas | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Administrar funciones personalizadas mediante CSV | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/configure-role-csv-files)
* [Manual para desarrolladores de aplicaciones \| Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)
* [Conectores de Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/connectors)

+++

+++¿Cuáles son los valores predeterminados seguros recomendados para las cuentas administrativas y privilegiadas de nivel superior en Adobe Learning Manager y dónde se configuran?

Adobe Learning Manager documenta los valores predeterminados seguros recomendados específicos para la función de administrador y los tipos de cuenta con privilegios.

* **Valores predeterminados de la cuenta de administrador de nivel superior (configurados en el primer aprovisionamiento)**:

* Método de inicio de sesión para usuarios internos: inicio de sesión único (SSO) mediante SAML 2.0: configurado en Administración de ALM > Configuración > Métodos de inicio de sesión. No uses Adobe ID para empleados o administradores.
* Verificación en dos pasos (2FA): obligatoria para todos los usuarios: configurada en Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración de autenticación.
* Duración máxima de la sesión: 8 horas (o según la política de la organización): configurada en Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración avanzada.
* Tiempo máximo de inactividad: 30 minutos (o según la política de la organización): la misma ubicación que antes.
* Eliminación automática de usuarios inactivos: se activa con un período de retención definido por la organización (p. ej., 90 días de inactividad): Administración de ALM > Configuración > General.
* Vencimiento del perfil de usuario externo: se establece en cada perfil externo en la creación: Administrador de ALM > Usuarios > Externo. Sin perfiles externos indefinidos.
* Restricciones de acceso a IP: restrinja los intervalos de IP aprobados cuando sea posible: Admin Console > Configuración > Configuración avanzada.

**Valores predeterminados de la función de administrador personalizado (configurados al crear cada función)**:

* Ámbito de OAuth para aplicaciones registradas: ámbito mínimo requerido. No conceda nunca acceso de lectura/escritura a la función de administrador a menos que sea estrictamente necesario.
* Ámbito de la función personalizada: restrinja a grupos de usuarios específicos y catálogos específicos. No cree funciones personalizadas con el ámbito Todos los usuarios y Todos los catálogos a menos que la función lo requiera de forma genuina.
* Acceso a la configuración en funciones personalizadas: no se concede a menos que la función específica lo requiera, dado el riesgo de escalación de privilegios.

**Valores predeterminados del administrador de integración**:

* Ámbito de API OAuth: seleccione el ámbito más restrictivo que cumpla los requisitos de la integración. No conceda lectura/escritura de administrador a aplicaciones que solo necesiten acceso de lectura del alumno.
* Credenciales de conector, credenciales de LTI y direcciones URL de webhook: tratar como secretos confidenciales; nunca compartir por correo electrónico ni confirmar en el control de código fuente.

**Referencias**:

* [Configuración | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Autenticación de usuarios y contraseñas seguras | Adobe Admin Console](https://helpx.adobe.com/enterprise/using/authentication-settings.html)
* [Funciones personalizadas | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)

+++

+++¿Ofrece Adobe Learning Manager una forma de que los administradores comparen la configuración actual de la cuenta con los valores predeterminados seguros recomendados?

Adobe Learning Manager no dispone de un panel de comparación dedicado que muestre automáticamente la configuración actual junto con los valores predeterminados seguros recomendados.

**Informe de funciones personalizadas: asignaciones de funciones con privilegios actuales**:

* En ALM, vaya a Administración > Usuarios > Funciones personalizadas y haga clic en Descargar (arriba a la derecha) para exportar un archivo CSV de todas las funciones personalizadas, sus conjuntos de permisos y sus asignaciones de ámbito.
* Compare esta exportación con los valores predeterminados recomendados en FRR-RSC-02 Sección 8, comprobando específicamente si cualquier función personalizada tiene acceso a Configuración, ámbito Todos los usuarios o ámbito Todos los catálogos sin justificación documentada.

**API ALM REST: recuperación de configuración de programación**:

* El extremo de GET/cuenta devuelve datos de configuración de nivel de cuenta en formato JSON, accesibles mediante el ámbito OAuth de la función de administrador. Los clientes pueden llamar a este punto final mediante programación y diferenciar la respuesta de una línea de base derivada de los valores predeterminados recomendados en FRR-RSC-02, sección 8.
* El extremo GET/usuarios (con include=role filter) devuelve las asignaciones de funciones actuales para todos los usuarios, lo que permite detectar automáticamente las asignaciones de funciones inesperadas.

>[!NOTE]
>
>Adobe Learning Manager no ofrece una interfaz de usuario de comparación en paralelo nativa. Los clientes que necesiten comprobar el cumplimiento de la configuración de forma automatizada deben integrar la API REST de ALM con sus herramientas existentes.

**Referencia**

* [Manual del desarrollador de aplicaciones | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++¿Pueden los administradores exportar las configuraciones y los ajustes actuales relevantes para la seguridad desde Adobe Learning Manager en un formato legible por el equipo?

Adobe Learning Manager admite la exportación de datos de configuración relevantes para la seguridad a través de varios mecanismos. Ninguna exportación produce una instantánea completa de todas las configuraciones de seguridad a la vez, pero las siguientes exportaciones cubren de forma conjunta todo el ámbito de los datos relevantes para la seguridad.

**API ALM REST: exportación JSON de asignaciones de roles actuales y configuración de cuenta**:

* GET/cuenta: devuelve la configuración de nivel de cuenta en JSON, incluidos los datos de configuración de inicio de sesión activo y los metadatos de cuenta.
* GET /users?include=role: devuelve todos los usuarios con sus funciones actualmente asignadas en JSON.
* GET /userGroups: devuelve todos los grupos de usuarios y su pertenencia, relevantes para auditar el ámbito de función personalizada.
* Todas las respuestas de la API son JSON (vnd.api+json). La autenticación utiliza OAuth 2.0 con el ámbito de lectura y escritura de la función de administrador.

**Exportación de CSV de funciones personalizadas: definiciones de funciones con privilegios actuales**:

* Administración de ALM > Usuarios > Funciones personalizadas > Descargar exporta un archivo CSV de todas las definiciones de funciones personalizadas, sus categorías de permisos y las asignaciones de ámbito.
* Esta exportación se puede utilizar como una instantánea legible por el equipo de la configuración actual de la cuenta con privilegios.
**

**API de trabajos: datos de usuario y rol en bloque**:

* La API de trabajos de ALM admite la generación a petición de informes de usuarios (incluidas las asignaciones de funciones) en formato CSV. Estas pueden programarse y consumirse mediante cumplimiento externo o herramientas SIEM.

**Referencia**

* [Manual del desarrollador de aplicaciones | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++¿Ofrece Adobe Learning Manager una API a través de la cual se pueda ver y ajustar mediante programación la configuración relevante para la seguridad?

Adobe Learning Manager proporciona una versión 2 de API REST completa que permite ver y ajustar mediante programación la configuración relevante para la seguridad mediante la autenticación OAuth 2.0. A continuación se indican las funciones de API específicas relacionadas con la configuración de seguridad:

**Autenticación y ámbito**:

* El administrador de integración registra las aplicaciones en Administración de integración > Aplicaciones > Registrar. El ID de cliente y el secreto de OAuth 2.0 se emiten por aplicación.
* Hay seis ámbitos disponibles. Para la administración de la configuración de seguridad, se requiere acceso de lectura y escritura de la función de administrador. Esto concede a la aplicación el mismo acceso que a un administrador completo a través de la API.
* Los tokens de acceso se obtienen a través del código de autorización de OAuth estándar o del flujo de credenciales de cliente. URL base: https://learningmanager.adobe.com/primeapi/v2/

**Administración de usuarios y funciones mediante API**:

* GET/usuarios: recuperar todos los usuarios y sus funciones actuales
* POST/usuarios: aprovisionar nuevos usuarios mediante programación
* PATCH /users/{id}: actualizar atributos de usuario incluidas asignaciones de funciones
* DELETE /users/{id}: deshabilitar una cuenta de usuario
* POST /users/{id}/purge: purgue permanentemente un usuario y todos los registros asociados

Recuperación de configuración de cuenta:

* GET/cuenta: devuelve la configuración de nivel de cuenta, incluidos los datos de configuración de cuenta en formato JSON, incluidos campos como complianceLabelDefaultID, showComplianceLabel y custom_injections.

+++

+++¿Publica Adobe Learning Manager su guía de configuración segura en un formato legible por el equipo, como OSCAL, JSON o YAML?

Adobe Learning Manager no publica actualmente su Guía de configuración segura en un formato legible por el equipo. Las instrucciones de [FRR-RSC-01](/help/migrated/alm-administrative-lifecycle.md) y [FRR-RSC-02](/help/migrated/alm-secure-administration-guide.md) se publican como documentación legible para el usuario en Adobe Experience League en formatos de documento de HTML y descargables.

No hay ningún archivo de definición de componente OSCAL, línea base YAML o archivo de política JSON disponible públicamente que codifique los valores predeterminados seguros recomendados para Adobe Learning Manager.

Los clientes que necesiten una comparación automatizada de la configuración actual con las líneas de base recomendadas deben utilizar la [API ALM REST](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) para recuperar los datos de configuración actuales en formato JSON.

+++

+++¿La Guía de configuración segura de Adobe Learning Manager está disponible públicamente sin necesidad de iniciar sesión ni de acceder a ella de forma especial?

**Lo que está disponible públicamente**:

* [FRR-RSC-01: Guía de administración segura](/help/migrated/alm-administrative-lifecycle.md): orientación completa del ciclo de vida de las cuentas administrativas de nivel superior.
* [FRR-RSC-02: Implicaciones y configuración de seguridad administrativa](/help/migrated/alm-secure-administration-guide.md): toda la configuración relevante para la seguridad, sus implicaciones y los valores predeterminados recomendados.
* FRR-RSC-03-10 (este documento) — Preguntas y respuestas a las ocho recomendaciones de FedRAMP SHOULD.

+++

+++¿Proporciona Adobe Learning Manager un historial de versiones y versiones que permite a las agencias realizar un seguimiento de los cambios en la configuración relevante para la seguridad y de los valores predeterminados recomendados a lo largo del tiempo?

Adobe Learning Manager mantiene un historial de versiones detallado y disponible públicamente para cada actualización del producto. En cada versión se documentan los cambios relevantes para la seguridad en la configuración administrativa, las capacidades de autenticación, los puntos finales de la API y las funciones de administración de funciones.

**Notas de la versión de ALM: historial de cambios acumulativo y numerado**:

* Adobe publica notas de la versión numeradas de cada actualización de Adobe Learning Manager (p. ej., actualización 100, actualización 99). Estos se publican en Experience League y documentan todas las nuevas funciones, los cambios en la configuración existente, las adiciones y eliminaciones de la API, los cambios en los conectores y las funciones obsoletas.
* Cada nota de la versión incluye una sección dedicada a los cambios de la API, donde se enumeran los nuevos puntos finales, los campos de respuesta modificados y las depreciaciones, directamente relacionados con las funciones de configuración relevantes para la seguridad.

**Páginas nuevas: resúmenes de funciones anteriores a la versión**:

* Cada versión principal tiene una página dedicada a las novedades en la que se documentan las nuevas funciones relevantes para la seguridad con contexto. Por ejemplo, las notas de la versión incluyen cambios en el control de permisos de funciones personalizadas, la adición de visibilidad de permisos creados mediante CSV para funciones personalizadas y cambios de limitación de velocidad de API.

**Lista de API en desuso: registro autorizado de funciones de API eliminadas** s:

* Adobe mantiene una página dedicada a las depreciaciones de la API en la que se enumeran todos los puntos finales de la API ALM obsoletos y eliminados con la versión de lanzamiento en la que se produce cada obsolescencia.

**Referencias**:

* [Notas de la versión de Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/release-notes)
* [Novedades de Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/whats-new-july-2024)
* [Obsoletaciones de API en Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/api-deprecations-list)

+++
