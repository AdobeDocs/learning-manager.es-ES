---
title: Ciclo de vida de la cuenta administrativa de Adobe Learning Manager
description: Este documento proporciona orientación completa sobre la administración segura de cuentas administrativas de nivel superior en Adobe Learning Manager (ALM) para cumplir con la normativa FedRAMP y las prácticas de seguridad recomendadas.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Tipos de cuentas administrativas en Adobe Learning Manager

## Asignación de roles de ALM

En Adobe Learning Manager, la cuenta administrativa de nivel superior es la función de administrador. Esta es la función a la que se hace referencia siempre que esta guía utilice el término &quot;cuenta administrativa de nivel superior&quot; de FedRAMP. Los administradores personalizados y los administradores de integración se tratan como cuentas con privilegios (de ámbito).

La siguiente tabla asigna los niveles de cuenta de FedRAMP a las funciones específicas utilizadas en Adobe Learning Manager:

| Término de FedRAMP | Nombre de rol de ALM | Descripción |
|--------------------------------------|----------------------------|-------------|
| Cuenta administrativa de nivel superior | Administrador | Función de mayor privilegio en ALM. Control total sobre usuarios, funciones, contenido de aprendizaje, informes, integraciones y todas las configuraciones del sistema. Se asigna directamente a la definición de cuenta administrativa de nivel superior de FedRAMP. |
| Cuenta con privilegios (ámbito) | Administrador personalizado | Un subconjunto definido de permisos de administrador con ámbito para funciones específicas (por ejemplo, informes, administración de catálogos). No tiene control total a nivel de cuenta. |
| Cuenta con privilegios (integración) | Administrador de integración | Administra integraciones y acceso basado en API entre ALM y sistemas externos. Privilegios elevados con ámbito solo para administración de integración. |


Adobe Learning Manager utiliza un modelo de control de acceso basado en funciones (RBAC) para administrar el acceso administrativo. Las funciones administrativas sólo las asignan los administradores autorizados.

Consulte [Funciones personalizadas en Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) para obtener más información

## Tipos de identidad y autenticación recomendada

Adobe Admin Console admite tres tipos de identidad para las cuentas de administrador. La elección del tipo de identidad tiene implicaciones de seguridad directas:

| Tipo de identidad | Descripción | Recomendación de seguridad |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (ID personal) | Tipo predeterminado; administrado por Adobe. Cualquiera puede crear uno. | NO RECOMENDADO para administradores. La organización no tiene control sobre este tipo de cuenta. |
| Enterprise ID | Cuenta propiedad de la organización administrada por un administrador del sistema Admin Console. | Aceptable si Federated ID/SSO no está disponible. Aplicar 2FA. |
| Federated ID (SSO) | Propiedad de la organización; integrada con SAML 2.0 SSO. La organización controla la autenticación por completo. | RECOMENDADO. Se autentica a través del IdP de la organización; admite el cumplimiento de MFA a nivel de proveedor de identidad. |

Para obtener más información, consulte lo siguiente:

* [Tipos de identidad](https://helpx.adobe.com/enterprise/using/admin-console.html)
* [Autenticación de usuario y contraseñas seguras](https://helpx.adobe.com/enterprise/using/authentication-settings.html)

## Asignación de funciones y control de acceso

Un administrador existente controla el acceso a las cuentas administrativas en Adobe Learning Manager mediante la [asignación de funciones](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) explícita. Entre las características clave del acceso administrativo seguro se incluyen:

* Las funciones administrativas sólo las asignan los administradores autorizados.
* El acceso se basa en funciones y tiene un ámbito de acuerdo con los permisos asignados.
* Las organizaciones son responsables de limitar el acceso administrativo a los usuarios con necesidades comerciales legítimas.

El Adobe recomienda a los clientes que revisen periódicamente el acceso administrativo para garantizar la observancia del principio de privilegios mínimos.

## Autenticación obligatoria de múltiples factores (MFA)

Adobe recomienda encarecidamente que los administradores apliquen la verificación en dos pasos (2FA) en toda la organización. El AMF se aplica a los usuarios de Enterprise ID y Adobe ID. Los usuarios Federated ID deben hacer que se aplique MFA en el proveedor de identidades de su organización.

Para aplicar 2FA en Adobe Admin Console:

1. Inicie sesión en la Adobe Admin Console.
2. Vaya a Configuración > Privacidad y seguridad > Configuración de autenticación.
3. Active la verificación en dos pasos y seleccione la opción Exigir para evitar que los usuarios la deshabiliten.
4. Si lo desea, puede configurar restricciones de acceso basadas en IP y opciones avanzadas de sesión (duración máxima de la sesión / tiempo máximo de inactividad).

>[!IMPORTANT]
>
>Adobe recomienda aplicar 2FA y no dejarlo como opcional para los usuarios. La aplicación del 2FA puede tardar hasta 24 horas. Para usuarios Federated ID, aplique el MFA en su proveedor de identidades.

Consulte [Autenticación de usuario segura para obtener más información](https://helpx.adobe.com/enterprise/using/authentication-settings.html) para obtener más información.


## Iniciar sesión como administrador

Los [administradores](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-admin) de ALM inician sesión directamente en la plataforma de ALM mediante credenciales organizativas administradas a través del Admin Console.

### Asignar una función de administrador

En la plataforma ALM, los administradores configuran el acceso administrativo mediante la creación y administración de funciones, la asignación de permisos a los usuarios y la definición del ámbito de permisos en función de las responsabilidades operativas.

Para asignar la función de administrador en ALM:

1. Inicie sesión en Adobe Learning Manager como administrador existente.
2. Vaya a Usuarios > Internos.
3. Busque o seleccione el usuario de destino.
4. Seleccione Acciones > Asignar función > Convertir en administrador.

Las funciones administrativas personalizadas permiten a los clientes delegar tareas administrativas a la vez que mantienen un control centralizado de los privilegios de nivel de cuenta. Los administradores personalizados pueden tener un ámbito específico para grupos de usuarios o catálogos específicos.

Consulte [Agregar usuarios y grupos de usuarios](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) para obtener más información.

## Configurar métodos de inicio de sesión y SSO

Los administradores de ALM controlan los métodos de inicio de sesión disponibles para todos los usuarios a través de Configuración > Métodos de inicio de sesión, una configuración esencial relacionada con la seguridad:

* **Usuarios internos**: Defina el modo de inicio de sesión en Adobe ID o Inicio de sesión único (SSO). Se recomienda encarecidamente SSO a través de SAML 2.0.
* **Usuarios externos**: Defina el modo de inicio de sesión en Adobe ID, SSO o ID de Learning Manager. Alinee el método seleccionado con la directiva de seguridad de su organización.

Adobe recomienda utilizar Federated ID/SAML 2.0 SSO como método de inicio de sesión para todos los usuarios internos. Esto garantiza que la autenticación esté totalmente controlada por el proveedor de identidades de su organización, lo que permite la aplicación centralizada de MFA y la revocación inmediata de la cuenta al salir del usuario.

Consulte [Configuración](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/settings) para obtener más información.

## Valores predeterminados seguros recomendados en el aprovisionamiento

Cuando se aprovisiona por primera vez una cuenta de ALM, Adobe recomienda comprobar la siguiente configuración predeterminada antes de conceder a cualquier usuario administrativo acceso operativo:

| Configuración | Valor predeterminado seguro recomendado | Dónde configurar |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Método de inicio de sesión: usuarios internos | Inicio de sesión único (SSO)/Federated ID | ALM > Configuración > Métodos de inicio de sesión |
| Verificación en dos pasos (2FA) | Aplicado (no es opcional para ningún usuario) | Admin Console > Configuración > Privacidad y seguridad |
| Duración máxima de la sesión | 8 horas o por política de la organización | Admin Console > Configuración > Configuración avanzada |
| Tiempo máximo de inactividad | 30 minutos o por política de la organización | Admin Console > Configuración > Configuración avanzada |
| Ámbito de la función de administrador | Privilegio mínimo; use funciones de administrador personalizadas cuando sea posible | ALM > Usuarios > Funciones personalizadas |
| Expiración de usuario externo | Establecer una fecha de caducidad en cada perfil de usuario externo | ALM > Usuarios > Externo |

### Lista de comprobación de configuración inicial para nuevos administradores

Al aprovisionar una nueva cuenta de administrador de nivel superior, complete lo siguiente antes de conceder acceso operativo:

* Confirme que el tipo de identidad es Enterprise ID o Federated ID, no Adobe ID personal.
* Aplicar 2FA en el nivel de Admin Console (Configuración > Configuración de autenticación).
* Configure SSO/Federated ID si aún no lo ha hecho.
* Establezca la duración máxima de la sesión y el tiempo máximo de inactividad en Admin Console > Configuración > Configuración avanzada.
* Limitar el ámbito de la función de administrador: asigne solo los permisos necesarios para las responsabilidades del usuario.
* Compruebe que la cuenta de administrador esté vinculada a una dirección de correo electrónico de la organización controlada por el equipo de TI.
* Documentar la cuenta en el registro de acceso privilegiado de su organización.

## Funcionamiento de las cuentas administrativas

### Tareas administrativas cotidianas

Las cuentas administrativas se utilizan para realizar tareas operativas diarias, entre las que se incluyen:

* **Administración del ciclo de vida del usuario**: creación de usuarios, actualización de perfiles y modificación de funciones.
* **Administración de contenido de aprendizaje**: administración de cursos, programas de aprendizaje, certificaciones y catálogos.
* **Informes y análisis**: Generando y revisando informes sobre el progreso del alumno y el uso de la plataforma.
* **Integraciones y configuración del sistema**: administración de conectores, acceso basado en API y configuración de nivel de sistema.

Se espera que los administradores sigan el control de acceso interno de su organización y cambien las políticas de administración al realizar acciones administrativas.

Consulte [Preguntas más frecuentes para administradores de Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Jerarquía de funciones y delegación

Adobe Admin Console utiliza una estructura de administración jerárquica. Los administradores del sistema pueden delegar responsabilidades en funciones con privilegios más bajos para reducir la superficie de ataque de la cuenta de administrador de nivel superior:

* Administrador de productos: administra el acceso a productos de Adobe específicos (p. ej., Adobe Learning Manager).
* Administrador de perfiles de productos: administra el abono de usuarios en perfiles de productos específicos.
* Administrador de grupo de usuarios: administra el abono de grupo de usuarios.
* Administrador personalizado de ALM: administrador con ámbito en ALM con permisos configurables por catálogo y grupo de usuarios.

### Prácticas de gobernanza en curso

Las organizaciones que gestionan cuentas de administración de ALM de forma continua deben seguir las siguientes prácticas:

* **Revisión periódica de acceso**: audite periódicamente la lista de administradores del sistema en Admin Console (Usuarios > Administradores) y administradores de ALM (Usuarios > Internos) para asegurarse de que solo el personal autorizado actual tenga estas funciones.
* **Supervisión del registro de auditoría**: El registro de auditoría del Admin Console registra todos los cambios realizados por los administradores. Los administradores del sistema tienen visibilidad completa. Revise el registro con regularidad para ver si hay cambios no autorizados.
* **Acceso mínimo permanente**: evita usar cuentas de administrador de nivel superior para tareas rutinarias. Reserve el acceso completo de administrador para las tareas que lo requieran específicamente.
* **Seguridad de sesión**: Configura la duración máxima de la sesión y el tiempo máximo de inactividad en Admin Console > Configuración > Configuración avanzada para limitar la exposición de las sesiones desatendidas.

Consulte [Introducción a Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) para obtener más información.

### Administrar cuentas de usuario bajo control del administrador

Los administradores de ALM administran las cuentas de usuario internas y externas. Las operaciones relevantes para la seguridad incluyen:

* Eliminación automática de usuarios: en Configuración, los administradores pueden configurar usuarios internos inactivos para que se eliminen automáticamente pasados un número especificado de días, lo que reduce el riesgo de cuentas inactivas.
* Caducidad de usuario externo: los administradores establecen una fecha de caducidad al crear perfiles de usuario externos. Las cuentas caducadas se mueven automáticamente a un estado inactivo.
* Eliminación de usuarios: los administradores pueden eliminar usuarios manualmente mediante Usuarios > Internos > Acciones > Eliminar usuario.
* Purga de usuarios: después de la eliminación, los administradores pueden purgar de forma permanente los registros de usuarios para cumplir con las políticas de retención de datos y evitar el acceso no autorizado a datos de usuarios obsoletos.

Para obtener más información, consulte lo siguiente:

* [Añadir usuarios y grupos de usuarios](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Purgar usuarios](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users)

## Desmantelamiento de cuentas administrativas

El acceso administrativo debe eliminarse cuando ya no sea necesario. Las cuentas administrativas de desmantelamiento pueden incluir:

* Revocación de funciones administrativas de los usuarios.
* Reducir privilegios cuando ya no sea necesario el acceso administrativo completo.
* Eliminación de usuarios del sistema cuando sea necesario.

La revisión periódica y la eliminación del acceso administrativo innecesario ayudan a mantener el acceso menos privilegiado.

### Quitar derechos de administrador del sistema (Admin Console)

Cuando un administrador del sistema abandona la organización o cambia de función, los privilegios se deben revocar rápidamente:

1. Inicie sesión en Adobe Admin Console como administrador del sistema.
2. Vaya a Usuarios > Administradores.
3. Seleccione el administrador que desea quitar.
4. Haga clic en el icono Más opciones (...) > Editar administrador y, a continuación, elimine la función de administrador del sistema O seleccione Eliminar usuario para eliminar por completo al usuario de la organización.
5. Si el administrador tuviera otras funciones (administrador de productos, administrador de asistencia técnica, etc.), revoque también dichas funciones.

>[!IMPORTANT]
>
>Si el administrador saliente es el propietario del contrato de la organización, la función Propietario del contrato debe transferirse a otra persona para que pueda eliminarse. Póngase en contacto con el servicio de asistencia del Adobe si es necesario.

Para obtener más información, consulte lo siguiente:

* [Crear, actualizar o eliminar cuentas de usuario en el Admin Console](https://helpx.adobe.com/enterprise/using/manage-users-individually.html)
* [Cómo abandonar la cuenta propiedad de la organización](https://helpx.adobe.com/enterprise/using/leave-organization.html)

### Quitar la función de administrador de ALM

Para revocar el acceso de administrador de ALM sin eliminar la cuenta del usuario (por ejemplo, cuando la persona sigue siendo un alumno):

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Vaya a Usuarios > Internos.
3. Busque y seleccione el usuario.
4. Seleccione Acciones > Eliminar rol > Eliminar administrador.

El usuario vuelve a la función Alumno. Se conservan el historial de aprendizaje y las inscripciones a los cursos.

Consulte [Agregar usuarios y grupos de usuarios](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) para obtener más información.

### Eliminar y purgar usuarios

Cuando un usuario abandona la organización por completo y su cuenta se debe eliminar de la plataforma:

* Elimine al usuario: Usuarios > Interno > seleccione usuario > Acciones > Eliminar usuario. Esto deshabilita la cuenta y elimina el acceso activo.
* Purgar al usuario: Después de la eliminación, vaya a Usuarios > Limpieza de usuarios, seleccione el mes de eliminación, seleccione el usuario y elija Acciones > Purgar usuario. La depuración elimina permanentemente todos los registros de usuario.

Consulte [Purgar usuarios](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users) para obtener más información.


## Seguridad y responsabilidad compartida

Adobe Learning Manager funciona bajo un modelo de responsabilidad compartida:

* El Adobe es responsable de asegurar la plataforma y la infraestructura de ALM subyacentes.
* Los clientes son responsables de administrar el acceso administrativo, las asignaciones de funciones y las actividades del ciclo de vida de los usuarios dentro de su cuenta de ALM.

Hay disponible información adicional sobre los procedimientos de seguridad de Adobe Learning Manager en [Información general sobre seguridad de Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Mantenimiento de documentos

Este documento se puede actualizar periódicamente para reflejar los cambios en la funcionalidad de Adobe Learning Manager o las prácticas recomendadas de administración. La versión y la fecha de la última actualización se mantienen en los metadatos del documento y en el paquete de autorización FedRAMP. Los clientes deben consultar la versión disponible públicamente en Adobe Experience League para asegurarse de que están utilizando las directrices más recientes.

## Cobertura de capacidad de seguridad mejorada

### SCG-ENH-CMP

Adobe mantiene procesos documentados de gestión del inventario, la propiedad y el ciclo de vida de los componentes para garantizar una configuración y un cumplimiento controlados en todos los componentes del sistema.

### SCG-ENH-API

Adobe aplica controles de seguridad de API estandarizados, incluida la autenticación, la autorización y la supervisión, respaldados por la gobernanza documentada y las salvaguardias de la plataforma.

### SCG-ENH-MRG

Adobe aplica procesos formales de cambio y combinación de administración, incluidos controles de revisión y aprobación, para mantener la integridad del sistema y reducir el riesgo de implementación.

### SCG-ENH-VRH

El Adobe sigue un proceso definido de gestión y corrección de la vulnerabilidad que abarca la identificación, la priorización, el seguimiento y la resolución oportuna.
