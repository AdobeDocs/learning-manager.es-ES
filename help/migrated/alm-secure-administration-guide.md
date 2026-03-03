---
title: 'Adobe Learning Manager: guía de administración segura'
description: Esta guía describe la configuración de seguridad, las funciones y las prácticas recomendadas para administrar la seguridad administrativa y el control de acceso en Adobe Learning Manager para garantizar el cumplimiento normativo y la seguridad.
jcr-language: en-us
exl-id: 67dd9334-9718-4b2a-841e-5d8bd5c42714
source-git-commit: 5682c45a4e5789a3eede53faf7cb257cd9685759
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---

# Configuración de seguridad administrativa e implicaciones de seguridad

## Funciones administrativas con impacto en la seguridad

Adobe Learning Manager utiliza un modelo de control de acceso basado en funciones (RBAC). La siguiente tabla asigna los niveles de cuenta de FedRAMP a los roles de ALM a los que se hace referencia en todo este documento:

| Término de FedRAMP | Función ALM | Relevancia de seguridad |
|-------------|---------|------------------|
| Cuenta administrativa de nivel superior | Administrador | Control total a nivel de cuenta. Acceso exclusivo a todas las opciones de configuración relevantes para la seguridad descritas en este documento. Esta es la función a la que se hace referencia en esta guía cuando se utiliza el término &quot;cuenta administrativa de nivel superior&quot;. |
| Cuenta con privilegios (ámbito) | Administrador personalizado | Acceso administrativo delegado con ámbito en funciones, grupos de usuarios o catálogos específicos. No se puede acceder a la configuración de seguridad de nivel de cuenta a menos que se conceda explícitamente. |
| Cuenta con privilegios (integración) | Administrador de integración | Administra integraciones, registros de API y configuraciones de conectores. Privilegios elevados con ámbito para la administración de integraciones. No se pueden modificar otras configuraciones de seguridad de nivel de cuenta. |

>[!NOTE]
>
>Solo los usuarios asignados explícitamente a estas funciones pueden modificar la configuración administrativa o de seguridad. A menos que se indique lo contrario, la función de administrador es la única que puede acceder a la configuración que se describe en las secciones 3 a 7.

## Configuración de inicio de sesión y autenticación

Configuración de inicio de sesión y autenticación controla el modo en que todos los usuarios, incluidos los administradores, acceden a la plataforma ALM. Estas opciones de configuración son configuradas exclusivamente por la función de administrador y tienen un impacto directo e importante en la postura de seguridad de toda la cuenta.

### Configuración del método de inicio de sesión

**Ubicación:** Administrador de ALM > Configuración > Métodos de inicio de sesión

El administrador controla el método de autenticación utilizado por todos los usuarios internos y externos. Las opciones incluyen:

- **Adobe ID:** Los usuarios se autentican mediante su cuenta de Adobe personal. Administrado por Adobe, no por la organización.
- **Inicio de sesión único (SSO) a través de SAML 2.0:** Los usuarios se autentican a través del proveedor de identidades (IdP) de la organización. La organización controla completamente la autenticación, el MFA y la política de sesiones.
- **Id. de Learning Manager:** Disponible solo para usuarios externos. Los usuarios crean un nombre de usuario y una contraseña específicos de la plataforma.
- **Varias configuraciones de SSO:** Se pueden agregar hasta 20 configuraciones de SSO para admitir diferentes grupos de usuarios, ubicaciones o divisiones organizativas

| Método Login | Implicación de seguridad | Recomendación |
|-------------|---------------------|----------------|
| **Adobe ID** | La organización no tiene control sobre la política de contraseñas, el MFA ni la recuperación de cuentas. Una cuenta de Adobe personal comprometida concede acceso a la plataforma ALM. | **NO RECOMENDADO** para usuarios administrativos o internos. Utilícelo solo cuando SSO no esté disponible. |
| **SSO (SAML 2.0 / Federated ID)** | El IdP de la organización controla completamente la autenticación. Las políticas de MFA, tiempos de espera de sesión y acceso condicional se aplican en el nivel de IdP. Revocación inmediata a la salida del usuario. | **RECOMENDADO** para todos los usuarios internos y administradores. Proporciona el nivel más alto de control organizativo. |
| **ID. del administrador de aprendizaje** | Los usuarios gestionan por sí mismos las contraseñas fuera de la infraestructura de identidad de la organización. No se puede aplicar MFA mediante ALM. La seguridad de la contraseña depende del comportamiento del usuario. | Aceptable solo para usuarios externos. No es adecuado para empleados o administradores. |

>[!CAUTION]
>
>Si el método de inicio de sesión se establece en Adobe ID para usuarios internos, la organización pierde la capacidad de aplicar la autenticación multifactor, controlar la complejidad de las contraseñas o revocar el acceso inmediatamente cuando un usuario se va. Esto aumenta considerablemente el riesgo de acceso no autorizado.

Consulte [Funciones personalizadas](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) para obtener más información.

### Multi-Factor Authentication (MFA)

**Ubicación:** Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración de autenticación

El cumplimiento de MFA para los usuarios de **Adobe ID** y **Enterprise ID** lo configura el **Administrador del sistema** en Adobe Admin Console, no dentro de la propia aplicación ALM.  Para los usuarios de **Federated ID / SSO**, el MFA se aplica en el proveedor de identidades de la organización.

- **2FA forzado:** Los usuarios no pueden deshabilitar la verificación en dos pasos. Proporciona una sólida protección contra el robo de credenciales y la suplantación de identidad.
- **2FA opcional:** Los usuarios eligen si habilitar la verificación en dos pasos. Posición de seguridad considerablemente más débil.
- **MFA no configurado:** Las contraseñas protegen el acceso por sí solas. Alto riesgo, en particular para las cuentas administrativas.

>[!IMPORTANT]
>
>Las cuentas administrativas sin AM obligatorio corren un riesgo significativamente mayor de acceso no autorizado. Una credencial de administrador comprometida sin MFA otorga un control total de la cuenta, incluida la capacidad de modificar toda la configuración de seguridad.

### Duración de la sesión y tiempo de espera inactivo

**Ubicación:** Adobe Admin Console > Configuración > Privacidad y seguridad > Configuración avanzada

El **Administrador del sistema** configura la duración máxima de la sesión activa y el tiempo de espera de la sesión inactiva para la organización. Esta configuración se aplica a todos los usuarios, incluidos los administradores.

- **Duración máxima de la sesión:** fuerza la reautenticación tras un período definido independientemente de la actividad. Limita la ventana de oportunidad si una sesión se ve comprometida.
- **Tiempo de inactividad máximo:** Finaliza las sesiones que han estado inactivas durante un período definido. Protege contra sesiones autenticadas desatendidas en dispositivos compartidos o desbloqueados.

## Configuración de asignación de roles y ámbito de privilegios

La asignación de roles y la configuración del ámbito de privilegios determinan quién tiene acceso administrativo en ALM y qué pueden hacer. Se encuentran entre las configuraciones de seguridad de mayor impacto de la plataforma. Solo el rol Administrador puede crear, asignar, modificar o revocar roles administrativos.

### Asignación de funciones administrativas

**Ubicación:** Administrador de ALM > Usuarios > Interno > Acciones > Asignar función / Quitar función

El **administrador** puede otorgar o revocar las siguientes funciones:

- **Administrador:** Acceso completo a nivel de cuenta
- **Autor:** Acceso de creación de contenido
- **Administrador personalizado:** Acceso administrativo con ámbito (consulte la sección 4.2)
- **Administrador de integración:** Acceso a la integración y a la API (consulte la sección 7)

| Configuración/Acción | Implicación de seguridad | Práctica recomendada |
|---|---|---|
| **Otorgando función de administrador** | Control total de la cuenta. Un usuario con esta función puede modificar todas las configuraciones de este documento, incluida la reconfiguración de la autenticación y la revocación del acceso de otros administradores. | Asigne solo a un número mínimo de usuarios con una necesidad empresarial verificada. Mantener una lista documentada de todos los titulares de la función de administrador. |
| **No se pudieron revocar las funciones al salir** | Los usuarios salientes conservan el acceso a las funciones administrativas. Riesgo de acceso no autorizado, exfiltración de datos o sabotaje. | Elimine las funciones inmediatamente cuando cambien las responsabilidades laborales o administrativas de un usuario. Realizar revisiones de acceso periódicas. |
| **Asignación excesiva de funciones generales** | Un amplio acceso administrativo aumenta el impacto potencial de una cuenta comprometida y reduce la responsabilidad por las acciones administrativas. | Aplica el principio del menor privilegio. Prefiera funciones con ámbito (por ejemplo, Administrador personalizado) cuando sea posible. |

### Configuración de funciones administrativas personalizadas

**Ubicación:** Administrador de ALM > Usuarios > Funciones personalizadas > Crear función

Aplique el principio de **mínimo privilegio**. Utilice las funciones de **administrador personalizado** para delegar funciones específicas (consulte la sección 4.2).

El **administrador** puede crear funciones personalizadas que otorguen un subconjunto definido de permisos administrativos. Las funciones personalizadas se pueden definir como ámbito para grupos de usuarios, catálogos o conjuntos de funciones específicos, lo que limita el alcance del acceso administrativo delegado.

**Las categorías de permisos disponibles incluyen:**

- **Privilegios de cuenta:** Acceso a configuraciones de todo el sistema como anuncios, interacción, habilidades y administración de usuarios.
- **Privilegios de funciones (principales):** Acceso a catálogos, informes y etiquetas.
- **Privilegios de funciones (objetos de aprendizaje):** Acceso a cursos, certificaciones, rutas de aprendizaje y ayudas de trabajo.
- **Ámbito:** Restrinja el rol a grupos de usuarios o catálogos específicos.

| Decisión de configuración | Implicación de seguridad | Práctica recomendada |
|---|---|---|
| **Creando una función personalizada demasiado amplia** | Una función personalizada con privilegios excesivos proporciona pocos beneficios de seguridad sobre la función de administrador completa y aumenta el radio de explosión de una cuenta comprometida. | Amplíe las funciones personalizadas al conjunto mínimo de permisos necesarios para la función específica. Prefiera las funciones con ámbito de catálogo y con ámbito de grupo de usuarios. |
| **Concesión de acceso de configuración a un administrador personalizado** | Los administradores personalizados con acceso a Configuración pueden modificar los métodos de inicio de sesión, la configuración de notificaciones y otras configuraciones de nivel de cuenta. | Conceda acceso a las funciones personalizadas a Configuración solo cuando sea explícitamente necesario. Audite regularmente qué funciones personalizadas tienen este privilegio. |
| **No auditar asignaciones de funciones personalizadas** | Los roles personalizados no documentados o no revisados pueden acumularse con el tiempo, lo que provoca un desplazamiento de privilegios. | Descargue periódicamente el informe de funciones personalizadas (**Usuarios > Funciones personalizadas > Descargar**) y revise todas las asignaciones de funciones personalizadas activas. |

## Configuración de aprovisionamiento de usuarios y administración de acceso

Configuración de aprovisionamiento de usuarios controla cómo se agregan los usuarios a la plataforma, cuánto tiempo permanecen activos y cuándo se eliminan sus datos. Estas opciones de configuración son configuradas exclusivamente por la función de administrador y tienen implicaciones de seguridad directas para la exposición de datos y el control de acceso.

| Configuración | Ubicación | Implicación de seguridad | Valor predeterminado recomendado |
|---|---|---|---|
| **Eliminación automática de usuario inactivo** | Administración de ALM > Configuración > General | Sin eliminación automática, las cuentas inactivas se acumulan. Las cuentas inactivas son un objetivo común para el acceso no autorizado porque pueden no estar supervisadas. | Activar. Establezca un período de retención alineado con la política de la organización (por ejemplo, 90 días de inactividad). |
| **Vencimiento del perfil de usuario externo** | Administrador de ALM > Usuarios > Externo > Añadir perfil | Los perfiles de usuario externos sin fecha de caducidad permanecen accesibles indefinidamente. Los partners o contratistas que ya no necesitan acceso mantienen un punto de entrada activo. | Establezca una fecha de caducidad para cada perfil de usuario externo en el momento de la creación. |
| **Controles de vínculo de registro automático** | Administrador de ALM > Usuarios > Interno > Añadir > Registro automático | Un vínculo de registro automático permite a cualquier usuario con la URL crear una cuenta de alumno. Si no se administra, esto puede dar lugar a que usuarios no autorizados o inesperados obtengan acceso a la plataforma. | Genere vínculos de registro automático solo cuando sea necesario. Deshabilite o revoque los vínculos no utilizados de inmediato. |
| **Pausa/reanudación de perfil externo** | Administrador de ALM > Usuarios > Externo > Acciones > Pausa | Pausar un perfil externo impide que los nuevos usuarios se registren, pero no afecta a los que ya están registrados. Si no se pausan los perfiles externos inactivos, es posible que se permitan registros no deseados. | Pausar perfiles externos cuando ya no sea necesario registrarse. Eliminar perfiles que estén permanentemente inactivos. |
| **Eliminación y purga de usuarios** | Administrador de ALM > Usuarios > Interno > Acciones > Eliminar/Limpieza de usuarios > Depurar | Los usuarios eliminados se desactivan, pero se conservan sus datos. La depuración elimina permanentemente todos los datos de usuario. Si no se purgan los usuarios que han abandonado, es posible que se conserven los registros de aprendizaje confidenciales y la información identificable personalmente más allá del período de retención necesario. | Purgar registros de usuarios de acuerdo con las políticas de privacidad y retención de datos de la organización. La purga es irreversible. |

>[!IMPORTANT]
>
>La purga es permanente e irreversible. Se eliminan todos los registros de aprendizaje, los datos de inscripción y la información del usuario. Si se hace referencia a un usuario purgado en configuraciones de conector, esos conectores se deshabilitarán. Confirme la selección cuidadosamente antes de ejecutar una purga.

## Configuración de informes y acceso a datos

La configuración de informes y acceso a datos determina qué usuarios pueden ver, generar y exportar los datos de la plataforma. La configuración incorrecta de estas opciones puede provocar la exposición de información confidencial personal, organizativa o relacionada con el cumplimiento.

| Configuración | Ubicación | Implicación de seguridad | Valor predeterminado recomendado |
|---|---|---|---|
| **Concesión de acceso de informe a funciones personalizadas** | Administrador de ALM > Usuarios > Funciones personalizadas > Privilegios de funciones > Informes | Los informes pueden contener información de identificación personal (PII), datos de finalización del curso, puntuaciones de evaluación y progreso del alumno. El acceso a las funciones de elaboración de informes debe limitarse a los usuarios con una necesidad empresarial verificada. | Conceder acceso al informe sólo a funciones con una necesidad específica y documentada. Utilice el acceso de sólo lectura cuando no sea necesario el acceso de escritura. |
| **Control total frente al ámbito de informe de solo lectura** | Administrador de ALM > Usuarios > Funciones personalizadas > Informe de resumen de cuenta | El informe de resumen de Control total de la cuenta concede a los administradores una visibilidad personalizada en todos los grupos de usuarios y catálogos, independientemente del ámbito de su función. Esto puede exponer datos fuera del ámbito previsto de una función de administrador de ámbito. | Otorgue el control total del informe de resumen de cuenta solo a aquellas funciones que requieran de forma genuina la visibilidad de los informes en toda la organización. |
| **Acceso a informes de correo electrónico y xAPI** | Administrador de ALM > Usuarios > Funciones personalizadas | Los informes de xAPI y los informes de correo electrónico solo están disponibles para la función de administrador completa. Estos informes pueden contener datos detallados de comportamiento y comunicación. El acceso está restringido por diseño. | No intente delegar el acceso a informes de correo electrónico o xAPI mediante funciones personalizadas. Estos son solo para administradores por diseño. |
| **Datos de usuario exportados** | Administrador de ALM > Usuarios > Interno > Exportar datos de usuario | La función Exportar datos de usuario genera un archivo descargable que contiene todos los registros de usuario internos. Estos datos deben tratarse de acuerdo con las políticas de seguridad y privacidad de la organización. | Limitar la capacidad de exportación al personal autorizado. Tratar los datos exportados como confidenciales. No almacenarla ni transmitirla fuera de sistemas aprobados. |

## Configuración de integración y acceso a API

La integración y la configuración de acceso a la API controlan la forma en que los sistemas externos se conectan a Adobe Learning Manager. Esta configuración amplía el acceso más allá de la interfaz de usuario de ALM y, si se configura incorrectamente, puede exponer los datos y la funcionalidad de la plataforma a sistemas no autorizados.  La configuración de integración se administra mediante la función de administrador de integración. La función de administrador completa conserva la capacidad de revisar, aprobar y revocar aplicaciones registradas.

| Configuración | Ubicación | Implicación de seguridad | Valor predeterminado recomendado |
|---|---|---|---|
| **Registro de aplicaciones de API** | Administrador de integración > Aplicaciones > Registrar | Al registrar una aplicación se crean credenciales de OAuth 2.0 (ID de cliente y secreto) que se pueden utilizar para obtener acceso a datos y funciones de ALM mediante programación. Los ámbitos de OAuth demasiado amplios (por ejemplo, lectura y escritura de la función de administrador) conceden acceso completo a la API administrativa. | Otorgue los ámbitos mínimos requeridos de OAuth. Revisar y revocar periódicamente los registros de aplicaciones no utilizadas o heredadas. Tratar las credenciales de cliente como secretos confidenciales. |
| **Ámbito de aplicación de OAuth** | Administrador de integración > Aplicaciones > Registrar > Ámbitos | Los ámbitos de OAuth disponibles van desde el acceso de lectura del alumno hasta el acceso de lectura/escritura del administrador. La lectura y escritura de la función de administrador permite a una aplicación modificar cualquier dato que un administrador pueda modificar, incluidas las funciones de usuario y la configuración de seguridad. | Utilice el ámbito de OAuth más restrictivo que satisfaga los requisitos de la integración. No conceda nunca acceso de lectura/escritura a la función de administrador a menos que sea estrictamente necesario. |
| **Configuración del conector (FTP, Salesforce, HRIS, etc.)** | Administrador de integración > Conectores | Los conectores permiten la importación y exportación automatizadas de datos de usuario, aptitudes y finalizaciones de cursos. Los conectores mal configurados pueden importar datos de usuario incorrectos, asignar funciones no deseadas o exportar datos confidenciales a destinos no autorizados. | Revise periódicamente todas las configuraciones del conector activo. Asegúrese de que las fuentes de datos y los destinos estén autorizados. Deshabilite los conectores que ya no se usen. |
| **Configuración de webhook** | Administrador de integración > Webhooks | Los webhooks envían datos de eventos de ALM en tiempo real (inscripciones, finalizaciones, cambios de usuario) a una dirección URL externa especificada. Un extremo webhook configurado incorrectamente o comprometido puede provocar la exfiltración de datos o la exposición de eventos de alumno confidenciales. | Registre solo las URL de webhook verificadas y aprobadas por la organización. Revise las configuraciones activas de webhook con regularidad. Elimine inmediatamente los webhooks inactivos o no reconocidos. |
| **Configuración de integración de LTI** | Administrador de integración > Integraciones de LTI | La integración de LTI permite a ALM actuar como proveedor o consumidor de LTI, lo que permite que las plataformas de LMS externas accedan a los cursos de ALM. Una vez habilitado, LTI no se puede deshabilitar. Las credenciales LTI expuestas pueden permitir el acceso no autorizado al contenido del curso. | Active LTI solo cuando exista un requisito de integración verificado. Tratar las credenciales de LTI como confidenciales. Comparte credenciales solo con administradores de LMS autorizados. |

## Responsabilidades de configuración administrativa y responsabilidad compartida

Los clientes pueden configurar las opciones administrativas de Adobe Learning Manager, que forman parte de los controles de seguridad gestionados por el cliente según el modelo de responsabilidad compartida de Adobe.

| Responsabilidades de Adobe | Responsabilidades del cliente |
|---|---|
| Funcionamiento seguro de la plataforma ALM y de la infraestructura subyacente. | Configuración de todas las funciones y permisos administrativos. |
| Aplicación del modelo de control de acceso basado en funciones (RBAC). | Selección y aplicación de métodos de inicio de sesión y MFA adecuados. |

Encontrará información adicional sobre los procedimientos de seguridad de Adobe Learning Manager en:

**Referencia:** [Información general sobre seguridad de Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Mantenimiento de documentos

Este documento se puede actualizar periódicamente para reflejar los cambios en la funcionalidad o las directrices de seguridad de Adobe Learning Manager. La versión y la fecha de la última actualización se mantienen en los metadatos del documento y en el paquete de autorización FedRAMP. Los clientes deben consultar la versión disponible públicamente en Adobe Experience League para asegurarse de que están utilizando las directrices más recientes.
