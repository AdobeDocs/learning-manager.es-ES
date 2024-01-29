---
jcr-language: en_us
title: Cumplimiento del RGPD por parte de Learning Manager
description: Cumplimiento del RGPD por parte de Adobe Learning Manager
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---



# Cumplimiento del RGPD por parte de Learning Manager

>[!IMPORTANT]
>
>El contenido de este documento no es asesoramiento jurídico y no pretende sustituir al asesoramiento jurídico. Consulte al departamento legal de su empresa para obtener asesoramiento sobre el RGPD.

+++¿Qué es el RGPD?

El RGPD es un nuevo reglamento de la Unión Europea que entró en vigor el 25 de mayo de 2018. Proporciona un fuerte control de la privacidad de los datos y permite a los usuarios finales hacerse cargo de sus propios datos personales.

+++

++ ¿Cómo o por qué se aplica a usted como cliente de Adobe Learning Manager?

Aunque el RGPD es un reglamento de la UE, es aplicable a las entidades empresariales de todo el mundo que recopilen información personal de cualquier usuario que pueda ser residente en la UE.  Como cliente de Learning Manager, evalúa si el RGPD es aplicable a tu organización.

+++

+++¿Qué función desempeña el Adobe en esto como proveedor de Learning Manager?

De acuerdo con el RGPD, si su empresa proporciona un producto o servicio a los residentes de la UE y determina cómo y por qué recopilar, realizar un seguimiento y supervisar sus datos, se considera que usted es un [controlador de datos](https://gdpr-info.eu/art-24-gdpr/). Como cliente de Adobe Learning Manager, si realiza una de estas actividades, se le considerará responsable del tratamiento de datos.

Las empresas que procesan datos en nombre de controladores se consideran  [procesadores de datos](https://gdpr-info.eu/art-28-gdpr/). Como proveedor de LMS alojado en la nube, Adobe Learning Manager desempeña la función de Adobe de datos. A continuación, se ofrecen más detalles sobre  [RGPD y su empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++¿Cómo te permite Learning Manager cumplir con el RGPD?

Learning Manager cuenta con las siguientes herramientas y procesos que te ayudarán a cumplir con el RGPD. Para respaldar que cualquier proceso que vaya más allá del producto cumpla totalmente con la normativa, es posible que deba evaluarlo con su equipo de cumplimiento.

**Derecho al olvido: controlador de datos:** El RGPD requiere que los controladores de datos ofrezcan a sus usuarios la funcionalidad del derecho al olvido. Esto significa que cualquier usuario tiene derecho a solicitar al responsable del tratamiento que elimine de forma permanente cualquier dato personal almacenado para ese usuario. Si se recibe una solicitud de este tipo y se evalúa que es una solicitud válida, ahora se proporciona esta funcionalidad en Learning Manager a través de su [Purgar usuarios](../administrators/feature-summary/purge-users.md) funcionalidad. Esta función permite al administrador iniciar una eliminación permanente de cualquier dato relacionado con un individuo específico, tras la solicitud de los individuos, en cuyo momento, Learning Manager eliminará los datos de su base de datos de forma instantánea y, a continuación, depurará automáticamente los registros de copia de seguridad (destinados a la recuperación del sistema).

**Derecho al olvido: procesador de datos:** El usuario final también puede contactar con el Adobe de forma independiente para eliminar su PII. En este caso, Learning Manager detectará automáticamente qué cuentas son propietarias de la PII de ese usuario y el Adobe notificará inmediatamente al administrador de dicha solicitud. A continuación, el administrador puede evaluar la validez de la solicitud y realizar una llamada a la misma mediante la función Purgar usuarios.

**Derecho de acceso:** El RGPD otorga al usuario final el derecho a solicitar datos que un controlador pueda haber almacenado para ese usuario final. Para responder a esta solicitud, Learning Manager permite al administrador generar automáticamente transcripciones de alumnos que se pueden compartir con el usuario.

**Privacidad por diseño, cifrado de datos:** Procesamos los datos tanto en tránsito como en reposo utilizando los mejores estándares de cifrado para garantizar la seguridad de los datos. Los algoritmos de cifrado utilizados son SHA-256. Esto garantiza que todos los datos que almacene estén adecuadamente protegidos para que no caigan en las manos equivocadas.

+++

