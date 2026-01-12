---
jcr-language: en_us
title: Solución de problemas de integración de Salesforce (SFDC) con Adobe Learning Manager
description: solucione problemas comunes de integración de Salesforce (SFDC) con Adobe Learning Manager (ALM), incluidos errores de exportación, problemas de permisos de campo en objetos personalizados de SFDC y notas importantes de compatibilidad con SFDC-ALM.
contentowner: saghosh
source-git-commit: cedb4acc89e7d972a4752e10c4fb6930c4633f6a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Solución de problemas de integración de Salesforce (SFDC) con Adobe Learning Manager

## Solución de problemas de exportación de SFDC (sin exportación durante más de 2-3 horas)

Si la exportación de SFDC no ha finalizado correctamente durante más de **2-3 horas**, siga los pasos que se indican a continuación para identificar y conocer el problema.

1. Vaya a la página de inicio de **Salesforce**.
2. En el cuadro de búsqueda **Búsqueda rápida**, escriba **`Bulk Data Load Jobs`** y ábralo.
3. La página muestra trabajos de carga de datos en bloque para los **últimos 7 días**.
4. Busque trabajos relacionados con **objetos de Adobe Learning Manager (ALM)**.
5. Haga clic en el trabajo específico que desea investigar.
6. Desplácese hasta la **parte inferior** de la página de detalles del trabajo para ver el **mensaje de error** y los detalles adicionales.

En muchos casos, la causa raíz es **permisos de nivel de campo insuficientes en SFDC**. El nombre del campo que falla puede tener este aspecto:

- `cp_Module_ID`
- u otros campos `cp_...` relacionados con objetos personalizados ALM.

Si estos campos aparecen en el error, vaya a la sección siguiente.

## Otorgar permisos de campo en campos de objetos personalizados de ALM en SFDC

Use la característica **Accesibilidad a campos** para corregir problemas de permisos en campos específicos (por ejemplo, `cp_Module_ID`).

### Pasos

1. Vaya a la página de inicio de **Salesforce**.
2. En el cuadro de búsqueda **Búsqueda rápida**, escriba **`Field Accessibility`** y ábralo.
3. En la lista de objetos, seleccione el **tipo/objeto de informe** correspondiente.
   - Ejemplo: `cp_LearnerTranscript_xxxx_xxxx` para el informe Transcripciones de alumnos (LT).
4. En la página siguiente, elija **&quot;Ver por campos&quot;**.
5. En el **menú desplegable de campos**, seleccione el campo que aparece en el error de exportación
   - Ejemplo: `cp_Module_ID`.
6. En la matriz de acceso, haga clic en la entrada **&quot;Oculto&quot;** para el perfil **Administrador del sistema** (y otros perfiles relevantes, si es necesario).
7. En la página siguiente:
   - Habilite **&quot;Visible&quot;** cuando sea apropiado.
   - Haga clic en **Guardar** en la parte inferior de la página.
8. Después de guardar, vuelve a la vista de accesibilidad del campo. El campo debe mostrarse ahora como **&quot;Editable&quot;** para **Administrador del sistema** (y cualquier otro perfil que haya actualizado).

## Repita el proceso para todos los campos afectados y vuelva a intentar la exportación

1. **Repita** los pasos de accesibilidad de campos de la sección 2 para **cada campo** indicó que tenía problemas de permisos en **trabajos de carga de datos en bloque**.
2. Una vez que todos los campos problemáticos tengan la visibilidad y los permisos de edición adecuados:
   - Vuelva a **Adobe Learning Manager**.
   - En la configuración del **conector SFDC**, **vuelva a intentar la exportación**.


## Notas importantes y limitaciones

Tenga en cuenta estos detalles de SFDC-ALM al diseñar o solucionar problemas de integraciones.

### No hay creación automática de objetos/campos en SFDC

- El conector **SFDC no crea nuevos objetos o campos en Salesforce**.
- Si se agrega un **nuevo campo en ALM** y desea que aparezca en SFDC:
   - **Cree manualmente el campo personalizado correspondiente** en SFDC.
   - **Asigne** el campo personalizado de SFDC al **campo ALM apropiado** en la configuración del conector.
   - Asegúrese de que el nuevo campo tenga **permisos adecuados a nivel de campo** (consulte la sección 2).

### URL de devolución de llamada para cuentas de ALM con dominios personalizados

- Si la cuenta de ALM usa un **dominio personalizado**, el equipo de ingeniería debe **agregar ese dominio personalizado** a la **lista de permitidos de URL de devolución de llamada** para la aplicación de producción OAuth del conector SFDC.
- Esto se hace mediante una **solicitud Jira** al equipo de ingeniería.
- Sin esto, el flujo de OAuth para el conector puede fallar.

### Limitación de zona horaria (solo UTC)

- Si la organización de SFDC usa una **zona horaria distinta de UTC**, **pueden perderse los datos de finalización e inscripción** durante la sincronización.
- Motivo: ALM **solo admite actualmente la zona horaria UTC** para la integración de SFDC.
- Referencia interna: PAPI-24525 se levanta para admitir zonas horarias adicionales.

### Limitación del tipo de datos de filtro (lista de selección frente a lista de comprobación)

- ALM permite importar **filtros SFDC creados con campos de lista de selección**.
- ALM **no admite** filtros basados en campos de casilla de verificación de lista de comprobación o selección múltiple.
- Motivo: ALM **solo admite tipos de datos de cadena** para filtros SFDC.
