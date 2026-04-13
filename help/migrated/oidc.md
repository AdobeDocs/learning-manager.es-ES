---
description: Información sobre el método de inicio de sesión de OIDC
jcr-language: en_us
title: Iniciar sesión en Adobe Learning Manager con OpenID Connect
source-git-commit: 7c430e3fbb2716455310f2130d73af10ce2e56c7
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---


# Iniciar sesión en Adobe Learning Manager con OpenID Connect (OIDC)

Descubra cómo funciona el inicio de sesión de OpenID Connect en Adobe Learning Manager para alumnos, autores y administradores. Este artículo abarca la experiencia, no la implementación.

## Información sobre el inicio de sesión de OpenID Connect

OpenID Connect (OIDC) es un método de inicio de sesión común creado a partir de estándares web. Muchas empresas utilizan un proveedor de identidades (por ejemplo, Okta, Google Workspace o Microsoft Entra ID) para empleados y socios.

Cuando su organización habilite OIDC para Adobe Learning Manager:

* El inicio de sesión se realiza mediante la página de inicio de sesión habitual de la organización, no mediante una contraseña que se aplique únicamente a Adobe Learning Manager, a menos que la organización decida lo contrario.
* Después de autenticarse, Adobe Learning Manager recibe la información que su organización permite (como los atributos de correo electrónico y perfil) y abre la experiencia adecuada para usted: alumno, autor, administrador u otras funciones admitidas por su cuenta.

OIDC es una alternativa a otras opciones de inicio de sesión que puede ofrecer su cuenta, como el inicio de sesión único basado en Adobe ID o SAML (SSO). El administrador decide qué métodos están disponibles.

## Por qué las organizaciones eligen OpenID Connect

Las organizaciones a menudo eligen OIDC porque:

* Los usuarios ven la misma experiencia de identidad corporativa o en la nube que usan para otras aplicaciones.
* Las políticas de contraseña, la autenticación multifactor y el ciclo de vida de la cuenta se administran en el proveedor de identidad, de forma coherente con otras aplicaciones empresariales.
* OIDC sigue patrones similares a otros flujos de inicio de sesión modernos desde la perspectiva del usuario y de TI, sin el mayor intercambio de documentos asociado con algunas configuraciones de solo SAML.

Tu experiencia se mantiene: ve a Learning Manager, inicia sesión donde te indique la organización y aterriza en la aplicación.

## Lo que ve al iniciar sesión

### Abrir Adobe Learning Manager

Puede utilizar:

* La URL principal de Adobe Learning Manager para su entorno
* Un dominio personalizado que haya configurado su organización, si corresponde
* Un vínculo desde un correo electrónico, una invitación o una página de registro automático
* Un marcador o un vínculo profundo a un curso, página de catálogo o recurso específico

Si su cuenta utiliza OIDC, el inicio de sesión suele redirigir el navegador al proveedor de identidades de su organización.

### Iniciar sesión con su organización

En la página de su proveedor de identidades, introduzca sus credenciales y complete los pasos adicionales que necesite su organización, como la autenticación multifactor. Este paso se produce fuera del propio formulario de inicio de sesión de Adobe Learning Manager cuando el método en uso es OIDC. Desde tu perspectiva, se siente como iniciar sesión en tu cuenta de empresa o educativa. Es posible que no veas términos técnicos como *OIDC* o *OAuth* durante este paso.

### Volver a Adobe Learning Manager

Después de iniciar sesión correctamente, el navegador vuelve a Adobe Learning Manager. El producto entonces:

* Reconoce que utiliza la información de correo electrónico y de perfil que comparte su proveedor de identidades, según la configuración de su organización
* Aplica sus permisos en Adobe Learning Manager (alumno, autor, administrador, administrador de integración, etc.)
* Abre la aplicación o el área adecuada (por ejemplo, la experiencia del alumno en comparación con la de administrador o autor), de acuerdo con la forma en que Adobe Learning Manager asigna funciones a su cuenta

Si se produce un error (por ejemplo, si su cuenta no está aprovisionada o su organización bloquea el acceso), es posible que le aparezca un error o que no pueda continuar. Póngase en contacto con su equipo interno de TI o con el administrador de Adobe Learning Manager.

## Usar otras opciones de inicio de sesión con OpenID Connect

Adobe Learning Manager puede admitir más de un método de inicio de sesión en una cuenta (varias opciones de SSO). Por ejemplo:

* Algunos usuarios inician sesión con Adobe ID
* Otros usan SAML SSO
* Otros usan OIDC

Las opciones que se le muestren dependerán de cómo esté configurada su cuenta. Al habilitar OIDC para su organización, no se eliminan por sí mismos otros métodos a menos que los administradores cambien esa configuración.

## Funciones y escenarios admitidos

Cuando su organización utiliza OIDC con Adobe Learning Manager, se admiten los siguientes comportamientos, lo que es coherente con el funcionamiento previsto de otros métodos de inicio de sesión empresarial.

### Cuadro 1. Compatibilidad con OIDC en situaciones habituales

| Área | Lo que significa para ti |
| --- | --- |
| Usuarios internos y externos | Los empleados y los usuarios externos invitados (por ejemplo, socios) pueden utilizar OIDC donde el administrador lo habilita, incluidos los flujos que comienzan desde los vínculos de registro automático cuando la cuenta está configurada para ello. |
| Acceso por primera vez | Si la política lo permite, el primer inicio de sesión correcto de OIDC puede crear o vincular su usuario en Adobe Learning Manager según las reglas de su organización, al igual que otras opciones de SSO. |
| Perfil y atributos | La información, como el correo electrónico y otros atributos, se puede actualizar desde su proveedor de identidades con el tiempo, de modo que su perfil de Adobe Learning Manager se mantenga alineado con el directorio de su organización, dentro de lo que configure su administrador. |
| Vínculos profundos | Se admiten vínculos que señalan a una página o recurso específicos de Learning Manager (no solo la página de inicio). Puede acceder al contenido deseado después de iniciar sesión, cuando lo permita la configuración de su organización. |
| Ruta de retorno | Después de la autenticación, puede volver al lugar al que intentaba llegar (por ejemplo, la misma dirección URL del curso o catálogo desde el que empezó), en lugar de aterrizar siempre en una página principal genérica. |
| Dominio personalizado | Si su empresa utiliza un nombre de host personalizado para Adobe Learning Manager, el inicio de sesión de OIDC también se admite en ese contexto. |
| Dispositivo móvil | Es posible iniciar sesión en teléfonos y tabletas a través de navegadores o experiencias compatibles. |
| De Publish a Adobe Learning Manager (Prime) | Los flujos de trabajo que implican la publicación de contenido en Learning Manager desde herramientas conectadas siguen siendo compatibles cuando su cuenta utiliza OIDC, de forma coherente con la configuración de su integración. |
| Inicio de sesión basado en identificador | Cuando su cuenta se basa en identificadores estables (más allá del correo electrónico únicamente) para cuentas coincidentes, esos flujos son compatibles con OIDC según la configuración de su administrador. |

Si un flujo de trabajo específico no funciona, la causa puede ser la configuración del proveedor de identidades, el aprovisionamiento de cuentas o la asignación de funciones de Adobe Learning Manager. El administrador puede verificarlo.

## Cómo funcionan las funciones después de iniciar sesión

Adobe Learning Manager determina lo que puede hacer a partir de las funciones y los permisos de su cuenta, no a partir del propio protocolo OIDC. OIDC solo determina quién es usted para satisfacción de su proveedor de identidades y qué comparte su organización con Adobe Learning Manager.

* Los alumnos suelen ver cursos de formación, catálogos y planes de aprendizaje.
* Los autores pueden crear o seleccionar contenido.
* Los administradores gestionan los usuarios, la configuración y la creación de informes.

Si te alojas en una zona equivocada o no tienes el acceso que esperas, pídele a tu administrador de Adobe Learning Manager que compruebe tu perfil y tu abono de grupo.

## Solución de problemas comunes

### Cuadro 2. Solución de problemas de inicio de sesión OIDC

| Problema | Qué probar |
| --- | --- |
| Redirigir bucle o página en blanco | Borre las cookies de la dirección URL de Learning Manager y del proveedor de identidades, pruebe con otro navegador o acceda a una ventana privada. Si persiste, póngase en contacto con el equipo de TI. Los proxys corporativos o las directivas de sesión de proveedores de identidad a veces interfieren. |
| &quot;Acceso denegado&quot; o similar después de iniciar sesión como proveedor de identidad | Su proveedor de identidades le ha aceptado, pero es posible que Adobe Learning Manager no tenga un usuario coincidente o que su cuenta carezca de una licencia o función. Póngase en contacto con el administrador de Adobe Learning Manager. |
| Idioma o detalles de perfil incorrectos | La asignación de atributos la controla su organización. Pregunte al administrador si los atributos del directorio deben controlar la configuración regional o los campos de perfil. |
| El vínculo profundo abrió la página principal en lugar del recurso | El comportamiento de la ruta de retorno y del vínculo profundo puede depender de cómo se compartió el vínculo y de su sesión. Vuelva a intentar el vínculo después de iniciar sesión por completo o pregunte al administrador si el formato del vínculo es compatible con usuarios externos. |

## Lo que los administradores deben saber

Si configura Adobe Learning Manager para su organización, OIDC se configura con el registro de la aplicación de su proveedor de identidades: identificadores de cliente, puntos finales para la autorización, tokens, información de usuario y la URL de redirección que utiliza Adobe Learning Manager para completar el inicio de sesión. Esos valores provienen de la documentación de su proveedor de identidades. La configuración debe coincidir entre su proveedor de identidad y el administrador de aprendizaje, para que los usuarios vean una redirección y una devolución fluidas.

Los usuarios finales no necesitan administrar esos valores. Solo necesitan la URL correcta de Learning Manager (o dominio personalizado) y, cuando corresponda, los vínculos de invitación o registro automático de su equipo.

## Resumen

* OIDC permite a los usuarios iniciar sesión en Adobe Learning Manager a través del proveedor de identidades estándar de su organización, con un flujo familiar de redirección y devolución.
* Después de iniciar sesión, Adobe Learning Manager utiliza el correo electrónico y los atributos compartidos para identificar al usuario y aplicar funciones (alumno, autor, administrador, etc.).
* Se admite el registro automático, varias opciones de SSO, actualizaciones de atributos, aprovisionamiento de usuarios por primera vez, vínculos profundos, ruta de retorno, dominios personalizados, móvil, de Publish a Adobe Learning Manager y coincidencia basada en identificadores, según la configuración de su cuenta.
* Otros métodos de inicio de sesión (como Adobe ID o SAML) siguen estando disponibles cuando los administradores los mantienen activados.
