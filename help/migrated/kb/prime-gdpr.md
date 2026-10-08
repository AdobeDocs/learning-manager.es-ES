---
jcr-language: en_us
title: Cumplimiento del RGPD por parte de Learning Manager
description: Cumplimiento de Adobe Learning Manager con el RGPD
contentowner: dvenkate
exl-id: 8ea31464-b4ce-49e8-b471-5630f0216aa4
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 63%
---
# Cumplimiento del RGPD por parte de Learning Manager

>[!IMPORTANT]
>
>El contenido de este documento no es asesoramiento jurídico y no pretende sustituir al asesoramiento jurídico. Consulte al departamento legal de su empresa para obtener asesoramiento sobre el RGPD.

Adobe Learning Manager se compromete a cumplir con el RGPD, lo que garantiza que los datos de los usuarios se gestionen de forma segura y transparente. Proporciona funciones esenciales del RGPD, como la capacidad de purgar usuarios (eliminar permanentemente todos los datos personales) y permite a los administradores generar transcripciones de alumnos para compartir información con los usuarios cuando lo soliciten.

Todos los datos de los usuarios están protegidos con un fuerte cifrado durante la transferencia y el almacenamiento, utilizando estándares como SHA-256. En el caso de algunas integraciones, los alumnos deben autenticarse, lo que garantiza que se obtenga su consentimiento antes de compartir cualquier dato. Estos controles de privacidad y seguridad ayudan a las organizaciones que utilizan Adobe Learning Manager a cumplir con el RGPD y a proteger la información de los alumnos.

+++¿Qué es el RGPD?

El RGPD es un nuevo reglamento de la Unión Europea que entrará en vigor el 25 de mayo de 2018. Proporciona un fuerte control de la privacidad de los datos y permite a los usuarios finales hacerse cargo de sus propios datos personales.

+++

+++¿Cómo o por qué le afecta como cliente de Adobe Learning Manager?

Aunque el RGPD es un reglamento de la UE, es aplicable a las entidades empresariales de todo el mundo que recopilen información personal de cualquier usuario que pueda ser residente en la UE.  Como cliente de Learning Manager, evalúe si el RGPD es aplicable a su organización.

+++

+++¿Qué papel desempeña Adobe a este respecto como proveedor de Learning Manager?

De acuerdo con el RGPD, si tu empresa ofrece un producto o servicio a los residentes de la UE y determina cómo y por qué recopilar, rastrear y supervisar sus datos, se te considera un [controlador de datos](https://gdpr-info.eu/art-24-gdpr/). Como cliente de Adobe Learning Manager, si realiza una de estas actividades, se considerará controlador de datos.

Las empresas que procesan datos en nombre de controladores se consideran [procesadores de datos](https://gdpr-info.eu/art-28-gdpr/). Como proveedor de LMS de Adobe Learning Manager alojado en la nube, Adobe desempeña el papel de procesador de datos. Aquí tienes más información sobre el [RGPD y tu empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++¿Cómo le permite Learning Manager cumplir con el RGPD?

Learning Manager ha incorporado las siguientes herramientas y procesos que le ayudarán en el cumplimiento del RGPD. Para respaldar cualquier proceso que vaya más allá del producto para que cumpla totalmente la reglamentación, es posible que todavía tenga que evaluar con su equipo de cumplimiento.

**Derecho al olvido - Cómo contactar con el controlador de datos:** el RGPD requiere que los controladores de datos admitan una funcionalidad de derecho al olvido para sus usuarios. Esto significa que cualquier usuario tiene derecho a solicitar al controlador de datos que elimine de forma permanente cualquier dato personal almacenado para ese usuario. Si recibe una solicitud de este tipo y además evalúa que es una solicitud válida, esta funcionalidad se proporciona ahora en Learning Manager a través de la funcionalidad para [purgar usuarios](../administrators/feature-summary/purge-users.md). Esta función permite al administrador iniciar una eliminación permanente de cualquier dato relacionado con un individuo específico, a petición del individuo, en cuyo momento Learning Manager eliminará de forma definitiva los datos de su base de datos y automáticamente se realizará una purga de los registros de copia de seguridad (destinados a la recuperación del sistema).

**Derecho al olvido - Contactar con el procesador de datos:** El usuario final también puede ponerse en contacto con Adobe de forma independiente para eliminar su información identificable personal. En este caso, Learning Manager detectará automáticamente qué cuentas poseen la información identificable personal de ese usuario y Adobe notificará inmediatamente al administrador de esa solicitud. A continuación, el administrador puede evaluar la validez de la solicitud y realizar una llamada a la misma mediante la función Purgar usuarios.

**Derecho de acceso:** El RGPD otorga al usuario final el derecho a solicitar datos que un controlador pueda haber almacenado para ese usuario final. Para respaldar esta solicitud, Learning Manager permite al administrador autogenerar el expediente académico del alumno, que puede compartirse con el usuario.

**Privacidad por diseño, cifrado de datos:** Procesamos datos en tránsito y en reposo utilizando los mejores estándares de cifrado de su clase para garantizar la seguridad de los datos. Los algoritmos de cifrado utilizados son SHA-256. Esto garantiza que cualquier dato que almacene esté adecuadamente protegido para que no caiga en manos equivocadas.

+++
