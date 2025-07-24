---
jcr-language: en_us
title: Compatibilidad con dominios personalizados
description: Los dominios personalizados no se admiten en una instancia de Azure de Learning Manager.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: 411c171c314a3aa9ad9cc10d46c2f0d447e2c0a3
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 65%

---

# Compatibilidad con dominios personalizados

Los dominios personalizados no se admiten en una instancia de Azure de Learning Manager.

## Información general {#overview}

La compatibilidad con dominios personalizados permite a los clientes obtener un control completo del nombre de dominio que pueden utilizar en su cuenta de Learning Manager. Un cliente debe adquirir el dominio personalizado por separado y trabajar con el equipo de Adobe para configurarlo como su URL de inicio de sesión para su plataforma de aprendizaje.

Esto permite al cliente usar una marca blanca para el inicio de sesión y la experiencia de acceso, por lo que los usuarios no verán ninguna presencia de Adobe o Adobe Learning Manager.

Por ejemplo, le gustaría personalizar su dominio para que sus usuarios obtengan la misma experiencia que si estuvieran en el dominio de Adobe. Si ABC Inc desea entrenar a sus clientes, le gustaría que aterrizaran en un dominio llamado `abc.com/mylearning`, en lugar de `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>Como requisito previo, debe registrar el dominio y, a continuación, Adobe le guiará a través de la personalización de la URL.


La función de dominio personalizado está disponible por un coste adicional. Póngase en contacto con su responsable de éxito de clientes para obtener más información.

* Para la función de alumno, el dominio comenzará por `https://cdn.<customer_custom_domain>/`. Por ejemplo, `https://cdn.elearningstage1.cpdomaintest.in/`
* Para todas las demás funciones, el dominio comenzará por `https://<customer_custom_domain>/`. Por ejemplo, `https://elearningstage1.cpdomaintest.in/`
* La dirección URL de inicio de sesión real será `https://<customer_custom_domain>/acapindex` o `https://<customer_custom_domain>/login`. Reemplace `<customer_custom_domain>` por el dominio real de su organización.

`<customer_custom_domain>` es la parte personalizable.

## Cómo configurar un dominio personalizado en una cuenta {#howtosetupacustomdomainonanaccount}

Como requisito previo, un cliente debe poseer un nombre de dominio y adquirir el dominio de un proveedor.

Por ejemplo, supongamos que un cliente posee un dominio ficticio, **acme.com**. El cliente desea que el contenido de Learning Manager se proporcione desde **learning.acme.com**.

Siga los pasos que se indican a continuación para configurar un dominio personalizado.

1. El cliente debe **añadir tres registros CNAME** en el dominio:

   * **learning.acme.com:** punto final público de ALB de Learning Manager compartido por el Adobe
   * **lrs.learning.acme.com:** punto final público de ALB señalado por learning.acme.com
   * **cdn.learning.acme.com:** punto final de CDN compartido por el Adobe

1. El cliente debe proporcionar certificados SSL para estos dominios:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe cargará estos certificados SSL en AWS ALB para proporcionar solicitudes a los dominios.
1. Adobe añadirá learning.acme.com a su certificado SAN.
1. Adobe generará los metadatos de SP para el cliente, ya que los metadatos contendrán las URL del dominio personalizado.

   * Si el cliente desea tener un inicio de sesión de redes sociales, Adobe debe incluir los patrones de URL de redirección de los sitios de redes sociales en la lista de direcciones URL permitidas.
   * Si el cliente ha habilitado el inicio de sesión único, el cliente debe trabajar con su IDP para incluir sus dominios en las URL de redirección. El cliente debe compartir el XML de metadatos de IDP con Adobe. Adobe debe actualizar la configuración de inicio de sesión único de la cuenta del cliente.

1. Adobe modificará las reglas S3 CORS para incluir el dominio del cliente.
