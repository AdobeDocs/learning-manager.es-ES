---
jcr-language: en_us
title: Configurar el almacenamiento del Creative Cloud para Adobe Learning Manager Content Composer
description: Obtenga información sobre cómo configurar el almacenamiento de Creative Cloud para Adobe Learning Manager Content Composer. En esta guía se explica por qué se requiere almacenamiento de Creative Cloud, cómo los administradores pueden asignar la oferta de abono gratuito en Adobe Admin Console y cómo solucionar problemas de acceso relacionados con el almacenamiento.
contentowner: saghosh
source-git-commit: 15e1f5c383442fb93706acdf68eb889c16511859
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---


# Configurar el almacenamiento del Creative Cloud para Adobe Learning Manager Content Composer

>[!IMPORTANT]
>
>A quién va dirigido este documento: Administradores que necesitan habilitar el almacenamiento de Creative Cloud para los usuarios de Adobe Learning Manager para que puedan acceder a Content Composer y utilizarlo. Resulta especialmente útil para los administradores a la hora de solucionar problemas de errores de acceso o inicio de sesión relacionados con el almacenamiento y para la asignación de la oferta de abono gratuito a través de Adobe Admin Console.


Adobe Learning Manager (ALM) Content Composer requiere que los usuarios tengan un almacenamiento de Creative Cloud asociado a su cuenta de Adobe. Los usuarios que no tengan almacenamiento de Creative Cloud pueden no poder acceder a Content Composer y pueden encontrarse errores de inicio de sesión o relacionados con el acceso.

Para ayudar a las organizaciones a aprovisionar almacenamiento para los usuarios afectados, Adobe proporciona una oferta de abono gratuito que los administradores pueden asignar a través de Adobe Admin Console. Esta oferta incluye almacenamiento de Creative Cloud y se puede utilizar cuando un usuario aún no tiene un plan que proporcione derechos de almacenamiento.

## Antes de comenzar

Asegúrese de que:

* Tiene acceso de administrador de Adobe Admin Console.
* Se identifica el usuario que requiere acceso a Content Composer.
* Ha comprobado si el usuario ya tiene un plan que incluye almacenamiento de Creative Cloud.

## Por qué los usuarios necesitan un almacenamiento Creative Cloud

Content Composer utiliza el almacenamiento de Creative Cloud para almacenar cursos. Los usuarios que no tengan almacenamiento asignado a su perfil de Adobe pueden recibir un error al intentar utilizar el Compositor de contenido.

![Error de almacenamiento de Content Composer](../assets/coco-storage1.png)

Muchos clientes de Adobe ya disponen de un almacenamiento Creative Cloud a través de los productos de Adobe existentes y no se ven afectados. Sin embargo, es posible que algunos clientes de Adobe Learning Manager no tengan el almacenamiento aprovisionado de forma predeterminada y necesiten un administrador para activarlo.

## Habilitar el almacenamiento gratuito de Creative Cloud para usuarios

Si un usuario no tiene almacenamiento de Creative Cloud, asigne la oferta de abono gratuito de Adobe Admin Console.

1. Inicie sesión en [Adobe Admin Console](https://adminconsole.adobe.com/) con una cuenta con privilegios de administrador. Solo los administradores pueden asignar productos y ofertas a los usuarios.
2. En el Admin Console, seleccione Productos > Pruebas y ofertas especiales.

   ![Pruebas y ofertas especiales en Admin Console](../assets/coco-storage2.png)

3. Encuentra la oferta de abono gratuito que está disponible en las versiones de prueba y las ofertas especiales. Esta es la oferta que se describe como el método recomendado para habilitar el almacenamiento de Creative Cloud para los usuarios que aún no tienen derechos de almacenamiento.

   ![Oferta de suscripción gratuita](../assets/coco-storage3.png)

4. Asigne la oferta de abono gratuito a los usuarios correspondientes. La asignación solo la puede completar un administrador con los permisos de Admin Console adecuados.
5. Después de la asignación, compruebe que el usuario tenga almacenamiento de Creative Cloud disponible y solicite al usuario que inicie sesión de nuevo en Content Composer.

## Almacenamiento proporcionado mediante el abono gratuito

Los usuarios con la oferta de abono gratuito reciben aproximadamente 2 GB de almacenamiento de Creative Cloud, lo que les permite utilizar Content Composer.

## Resolución de problemas

**El usuario recibe un error al obtener acceso al editor de contenido**

Compruebe si el usuario tiene almacenamiento de Creative Cloud disponible en su perfil de Adobe.

**El usuario no puede ver la oferta de abono gratuito**

Confirme que:

* Ha iniciado sesión como administrador.
* Está viendo el área Productos de Adobe Admin Console.
* La organización cumple los requisitos para acceder a la oferta.

## Preguntas frecuentes

**¿Recibe cada usuario de Adobe Learning Manager automáticamente almacenamiento de Creative Cloud?**

No. Es posible que algunos usuarios de ALM no tengan almacenamiento aprovisionado de forma predeterminada y que necesiten derechos adicionales a través de la oferta de abono gratuito.

**¿Pueden los usuarios habilitar el almacenamiento ellos mismos?**

No. El derecho de almacenamiento debe asignarlo un administrador de Adobe a través del Admin Console.

**¿Se requiere almacenamiento de Creative Cloud para Content Composer?**

Sí. El modo de composición de contenido depende de los usuarios que tengan almacenamiento de Creative Cloud asociado a su cuenta de Adobe.

**¿Qué deben hacer los administradores si un usuario encuentra un error relacionado con el almacenamiento?**

Compruebe que el usuario tenga derechos de almacenamiento de Creative Cloud. Si no es así, asigne la oferta de abono gratuito a través de Adobe Admin Console y haga que el usuario lo intente de nuevo.

**¿Qué deben hacer los administradores si todavía tienen problemas de acceso o derechos?**

Si el administrador de Adobe Admin Console tiene un problema al asignar el almacenamiento del Creative Cloud o al depurar problemas relacionados con el acceso, es posible que el problema requiera compatibilidad con el nivel de cuenta Enterprise. En tales casos, póngase en contacto con el servicio de asistencia para empresas de Adobe a través de las opciones de asistencia disponibles en Admin Console.

Para obtener más información, vea las [opciones de soporte técnico de Adobe Enterprise](https://helpx.adobe.com/es/business/enterprise/get-help/support-options/support-for-enterprise.html)
