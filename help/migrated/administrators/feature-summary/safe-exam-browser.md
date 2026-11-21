---
title: Explorador de exámenes seguro
description: Habilita la integración del navegador de exámenes seguro en el nivel de cuenta en Adobe Learning Manager para que los autores puedan requerir un entorno de navegador seguro para los cuestionarios nativos.
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%
---

# Explorador de exámenes seguro

El Explorador de exámenes seguro proporciona un entorno seguro para que los alumnos realicen pruebas nativas de Adobe Learning Manager, restringiendo el acceso a otros navegadores y aplicaciones durante una evaluación.

Los administradores pueden habilitar la integración del Explorador de exámenes seguros en el nivel de cuenta y cargar un archivo de configuración (.seb) para definir las restricciones de las pruebas. Una vez habilitada la integración, los autores pueden configurar pruebas individuales para requerir el uso del Explorador de exámenes seguro.

En este artículo se explica cómo habilitar la integración Explorador de exámenes seguro para su cuenta.

## Habilitar integración de Explorador de examen seguro

Habilite la integración del Explorador de exámenes seguros para que la opción esté disponible para los autores cuando configuren pruebas. Antes de comenzar, asegúrese de que tiene el archivo Explorador de exámenes seguros para su cuenta.

Para habilitar la integración del Explorador de exámenes seguro:

1. Inicie sesión en ALM como **Administrador**.
1. Seleccione **Configuración** > **General**.
1. Vaya a la **integración del Explorador de examen seguro**.
1. Seleccione **Editar**.

   Esto expande la **integración del Explorador de examen seguro**.

1. Seleccione **Habilitar**.
1. Seleccione **Examinar** y cargue el archivo del Explorador de examen seguro del sistema. Consulte la configuración de [Configurar el archivo del explorador de exámenes seguros](#configure-the-seb-file-for-macos) para obtener más información.

   ![Configuración de integración del Explorador de examen seguro en Configuración general](assets/safe-exam-browser-integration-settings.png "Configuración de integración del Explorador de examen seguro en Configuración general")

1. Seleccione **Guardar**.

   El Explorador de examen seguro ahora está disponible para que los autores lo habiliten al configurar pruebas compatibles.

### Configurar el archivo .seb para macOS {#configure-the-seb-file-for-macos}

Cree un archivo .seb con la herramienta de configuración SEB para definir las restricciones de las pruebas, la configuración de seguridad y las aplicaciones permitidas. Antes de utilizar el Explorador de exámenes seguros (SEB), asegúrese de que el archivo .seb cumpla los siguientes requisitos:

1. Establezca el parámetro browserWindowWebView en 3 (Integer) para habilitar SEB.
1. Establezca startURL en la dirección URL que corresponda al entorno de destino.
1. Asegúrese de que el archivo .seb incluya la información necesaria de quitURL.
