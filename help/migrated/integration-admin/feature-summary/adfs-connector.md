---
description: Aprenda a integrar el conector de ADFS con Adobe Learning Manager
jcr-language: en_us
title: Conector ADFS
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 3%

---


# Conector de ADFS en Adobe Learning Manager

## Introducción

El conector de ADFS en Adobe Learning Manager le permite integrarse con Microsoft Azure Active Directory mediante los Servicios de federación de Active Directory (ADFS). Esta integración permite la sincronización automática de los datos de usuario de Azure AD en Learning Manager. Con funciones como la asignación de atributos, el filtrado de usuarios y las importaciones programadas, el conector ayuda a optimizar la administración de usuarios y garantiza que los datos del alumno sean precisos y estén actualizados. Resulta especialmente útil para las organizaciones que confían en ADFS para la gestión centralizada de identidades y accesos.

## Requisitos previos

Antes de configurar el conector de ADFS en Adobe Learning Manager, complete los siguientes pasos en el Portal de Azure:

- Registrar una aplicación
- Generar un secreto de cliente
- Definir permisos de API

### Registrar una aplicación en Azure

Para registrar una aplicación en Azure:

1. Inicie sesión en [Azure Portal](https://portal.azure.com/).
2. Vaya a **Azure Active Directory**.
3. Seleccione **Agregar** y luego **Registro de la aplicación**.
4. Escriba un nombre para la aplicación y seleccione **Registrar**.

### Generar un secreto de cliente

Para crear un secreto de cliente:

1. En la aplicación recién registrada, vaya a **Certificados y secretos**.
2. Seleccione **Nuevo secreto de cliente**.
3. Agregue una descripción y establezca la caducidad en **24 meses**.
4. Guarde el **valor secreto de cliente** en una ubicación segura.

### Definir permisos de API

Para agregar permisos de API:

1. Seleccione **Permisos de API** y, a continuación, seleccione **Agregar un permiso**.
2. Seleccione **Microsoft Graph** y, a continuación, seleccione **Permisos de la aplicación**.
3. Busque y seleccione los permisos siguientes:

   - **Directory.Read.All**: Leer los datos del directorio
   - **User.Read.All**: leer los perfiles completos de todos los usuarios
4. Seleccione **Agregar permisos**.
5. Otorgue **consentimiento del administrador** para los permisos.

## Configurar el conector de ADFS en Learning Manager

Puede configurar el conector de ADFS en Adobe Learning Manager para importar datos de usuario desde ADFS, exportar aptitudes de usuario a ADFS y programar sincronizaciones automatizadas para mantener ambos sistemas actualizados.

Para configurar el conector de ADFS:

1. Inicie sesión en Adobe Learning Manager como administrador de integración.
2. Pase el ratón sobre el icono del conector **ADFS**.
3. Seleccione **Conectar**.

   ![](assets/adfs-connector1.png)
   _Seleccionar Conectar para configurar el conector de ADFS_

### Introducir detalles de conexión

En la página de configuración de ADFS:

1. Escriba los siguientes datos:

   - Nombre de conexión
   - ID de cliente
   - Secreto de cliente

   ![](assets/adfs-connector2.png)
   _Escriba los detalles de configuración para conectar ADFS_

2. Seleccione **Conectar**.
3. Adobe Learning Manager buscará y rellenará automáticamente el **id. de inquilino** y el **dominio principal** desde el portal de Azure.

## Importación de usuarios desde ADFS

### Asignación de atributos

- Los administradores de integración pueden asignar atributos de ADFS a los atributos agrupables correspondientes en Adobe Learning Manager.
- Esta asignación es una configuración de una sola vez y se reutiliza para todas las importaciones de usuarios posteriores.
- Puede modificar la asignación de atributos en cualquier momento si es necesario.

### Importación automatizada de usuarios

- Adobe Learning Manager extrae automáticamente los datos de usuario de ADFS a intervalos programados.
- Esto ayuda a mantener sincronizados los registros de los usuarios en todos los sistemas.

### Filtrar usuarios

- Los administradores pueden aplicar filtros para limitar los usuarios importados.
- Por ejemplo, importe sólo usuarios de determinados responsables o departamentos.
