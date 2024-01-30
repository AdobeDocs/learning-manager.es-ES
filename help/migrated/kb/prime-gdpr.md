---
jcr-language: en_us
title: Cumplimiento del RGPD por parte de Learning Manager
description: Cumplimiento del RGPD por parte de Adobe Learning Manager
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 39%

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

De acuerdo con el RGPD, si su empresa proporciona un producto o servicio a los residentes de la UE y determina cómo y por qué recopilar, realizar un seguimiento y supervisar sus datos, se considera que usted es un [controlador de datos](https://gdpr-info.eu/art-24-gdpr/). Como cliente de Adobe Learning Manager, si realiza una de estas actividades, se considerará controlador de datos.

Las empresas que procesan datos en nombre de controladores se consideran  [procesadores de datos](https://gdpr-info.eu/art-28-gdpr/). Como proveedor de LMS alojado en la nube, Adobe Learning Manager desempeña la función de Adobe de datos. A continuación, se ofrecen más detalles sobre  [RGPD y su empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++¿Cómo te permite Learning Manager cumplir con el RGPD?

Learning Manager ha incorporado las siguientes herramientas y procesos que le ayudarán en el cumplimiento del RGPD. Para respaldar que cualquier proceso que vaya más allá del producto cumpla totalmente con la normativa, es posible que deba evaluarlo con su equipo de cumplimiento.

**Derecho al olvido: controlador de datos:** El RGPD requiere que los controladores de datos ofrezcan a sus usuarios la funcionalidad del derecho al olvido. Esto significa que cualquier usuario tiene derecho a solicitar al responsable del tratamiento que elimine de forma permanente cualquier dato personal almacenado para ese usuario. Si recibe una solicitud de este tipo y además evalúa que es una solicitud válida, esta funcionalidad se proporciona ahora en Learning Manager a través de la funcionalidad para [purgar usuarios](../administrators/feature-summary/purge-users.md). Esta función permite al administrador iniciar una eliminación permanente de cualquier dato relacionado con un individuo específico, a petición del individuo, en cuyo momento Learning Manager eliminará de forma definitiva los datos de su base de datos y automáticamente se realizará una purga de los registros de copia de seguridad (destinados a la recuperación del sistema).

**Derecho al olvido - Contactar con el procesador de datos:** El usuario final también puede ponerse en contacto con Adobe de forma independiente para eliminar su información identificable personal. En este caso, Learning Manager detectará automáticamente qué cuentas poseen la información identificable personal de ese usuario y Adobe notificará inmediatamente al administrador de esa solicitud. A continuación, el administrador puede evaluar la validez de la solicitud y realizar una llamada a la misma mediante la función Purgar usuarios.

**Derecho de acceso:** El RGPD otorga al usuario final el derecho a solicitar datos que un controlador pueda haber almacenado para ese usuario final. Para responder a esta solicitud, Learning Manager permite al administrador generar automáticamente transcripciones de alumnos que se pueden compartir con el usuario.

**Privacidad por diseño, cifrado de datos:** Procesamos los datos tanto en tránsito como en reposo utilizando los mejores estándares de cifrado para garantizar la seguridad de los datos. Los algoritmos de cifrado utilizados son SHA-256. Esto garantiza que cualquier dato que almacene esté adecuadamente protegido para que no caiga en manos equivocadas.

+++

