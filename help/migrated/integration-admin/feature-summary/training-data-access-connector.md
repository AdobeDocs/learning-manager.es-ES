---
description: Aprenda a integrar el conector de acceso a datos de formación con Adobe Learning Manager
jcr-language: en_us
title: Conector de Training Data Access
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---


# Conector de Training Data Access en Adobe Learning Manager

## Introducción

El **conector Training Data Access** te permite crear una experiencia de aprendizaje descentralizada que puede ser independiente o integrarse en una interfaz personalizada creada con **Adobe Experience Manager (AEM) Sites**. Este conector le ayuda a recuperar y mostrar contenido de formación actualizado a los alumnos, con funciones de búsqueda y filtro.

>[!IMPORTANT]
>
>- Esta función solo está disponible si Adobe Learning Manager se vende como **complemento** en Adobe Experience Manager.
>- Los datos del curso recuperados a través de este conector se actualizan cada 24 horas
>- Este conector no es de autoservicio para crear una experiencia de inicio de sesión sin encabezado o basada en AEM. Póngase en contacto con el Adobe para planificar el enfoque adecuado para su caso de uso.

## Cómo funciona

Una vez habilitado el conector, Adobe Learning Manager muestra un conjunto de API públicas que proporcionan metadatos de formación, como cursos, rutas de aprendizaje y certificados. Puede utilizar estas API para crear una interfaz de usuario personalizada de marca que muestre contenido de formación y admita la funcionalidad de búsqueda y filtro.

## Configurar el conector de Acceso a datos de formación

Puedes integrar Adobe Learning Manager con tu sistema de almacenamiento de datos y búsqueda para insertar metadatos de formación en AEM Sites u otras experiencias descentralizadas.

Para configurar el conector:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el icono **Training Data Access** y seleccione **Connect**.

   ![](assets/training-data-access-connector1.png)
   _Seleccione Conectar para configurar el conector de Acceso a datos de formación_

3. Escriba un **Nombre de conexión**.
4. Seleccione el **Tipo de interfaz**:

   - **Administrador de aprendizaje nativo**: Experiencia de inicio de sesión estándar, disponible de forma predeterminada.
   - **Interfaces sin encabezado**: Opción premium que muestra las API públicas para una interfaz de usuario sin sesión iniciada y descentralizada.

   ![](assets/training-data-access-connector2.png)
   _Escriba los detalles necesarios para la configuración del conector de Training Data Access_

5. Seleccione **Conectar**. Adobe Learning Manager genera automáticamente la **URL base** y la **URL de CDN**. Utilizarás estas direcciones URL en tu sitio o aplicación personalizados para obtener datos de formación.

>[!NOTE]
>
>Los clientes del plan prémium reciben una URL de API diferente a la de los clientes estándar.

## Exportar metadatos de formación

Para exportar metadatos de formación:

1. Seleccione **Exportar metadatos de formación** en la página del conector.
2. Seleccione **Habilitar exportación de metadatos de formación con esta conexión** para comenzar a insertar los datos de formación en el sistema de búsqueda y recuperación.
3. Seleccione **Habilitar programación** y establezca la fecha, hora e intervalo de inicio.

   ![](assets/training-data-access-connector3.png)
   _Programar exportación para metadatos de formación_

4. Seleccione **Guardar**.

   - Esto carga automáticamente todas las imágenes de curso, ruta de aprendizaje y certificado en la **CDN**.
   - También exporta los metadatos asociados a su sistema de búsqueda.

### Exportaciones a petición

- **Ejecutar exportaciones a petición:** Ve a **Bajo demanda**, establece la **Fecha de inicio** y selecciona **Ejecutar** para ejecutar una exportación cuando sea necesario.
- **Comprobar estado de ejecución:** Vea el progreso y el historial de exportación en la página **Estado de ejecución**.

## Crear y publicar el sitio web en AEM

Para mostrar los datos de formación en un sitio web descentralizado o basado en AEM Sites:

1. **Instale el paquete AEM** desde el [repositorio GitHub de Adobe](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0) (requisito previo).
2. Use la **URL base**, la **URL de CDN**, el **ID de cliente**, el **Secreto de cliente** y el **Token de actualización de administrador** para crear una configuración en AEM.
3. Cree el sitio utilizando componentes AEM.
4. Publish abre el sitio para los alumnos.
5. Para obtener información completa sobre la configuración, consulte [este artículo](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/aem-sites/adobe-learning-manager-integration-aem) y [este artículo](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/aem-sites/integrate-aem-learning-manager).

### Experiencia del alumno

Una vez que el sitio esté activo:

- El sitio web muestra todos los **Cursos**, **Rutas de aprendizaje** y **Certificados** recuperados de Adobe Learning Manager mediante el sistema de búsqueda.
- Los alumnos que **no hayan iniciado sesión** pueden examinar y ver los detalles del curso.
- Cuando un alumno hace clic para inscribirse en un curso, ruta de aprendizaje o certificado, se le solicita **iniciar sesión** para completar la inscripción e iniciar la formación.

## Experiencia sin sesión iniciada

La experiencia de no inicio de sesión le permite crear una experiencia en tiempo real para los usuarios que no han iniciado sesión. Por ejemplo, una experiencia que no haya iniciado sesión sirve como página de aterrizaje para las campañas de marketing que alientan los registros.

La experiencia de inicio de sesión no registrado en Adobe Learning Manager se puede configurar mediante el conector **Training Data Access**. El conector ofrece las siguientes opciones:

- Oferta estándar
- Oferta Premium

### Oferta estándar

La oferta estándar es crear la versión nativa de Adobe Learning Manager. Los usuarios pueden crear una experiencia descentralizada, de solo demostración y sin haber iniciado sesión. La experiencia descentralizada de demostración no es escalable y no debe utilizarse en un entorno de producción.

### Oferta Premium

La oferta premium ayuda a los usuarios a crear una interfaz descentralizada, que se configura mediante el conector **Training Data Access**. Esto permite a los usuarios obtener datos en tiempo real sobre detalles del curso y la ruta de aprendizaje, como el nombre, la descripción, el autor, las aptitudes, la duración, etc. En los escenarios de aprendizaje mixto, también se obtienen límites de puestos en tiempo real, puestos ocupados, listas de espera y recuentos de listas de espera. Los clientes pueden utilizar estas API para crear capacidades de búsqueda y filtro, así como un resumen completo del curso para los alumnos que no hayan iniciado sesión.

Los clientes pueden adquirir un plan prémium para crear esta experiencia altamente ampliable sin haber iniciado sesión.

>[!NOTE]
>
>Póngase en contacto con el equipo de asistencia o el CSM para adquirir el plan premium.

Después de que un usuario adquiera un plan, el equipo de CSM activará el plan premium para él. Mediante el conector de Acceso a datos de formación, los usuarios pueden configurar una experiencia sin conexión con las funciones mencionadas anteriormente.
