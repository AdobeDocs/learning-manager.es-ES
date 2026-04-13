---
description: Más información sobre la configuración de la configuración avanzada en Adobe Learning Manager
jcr-language: en_us
title: Configuración avanzada en Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 34%

---


# Configuración avanzada en Adobe Learning Manager

## Etiquetas de catálogo

Las etiquetas de catálogo de Adobe Learning Manager se utilizan para etiquetar objetos de aprendizaje (cursos, certificaciones, rutas de aprendizaje, etc.) con campos y valores específicos. Estas etiquetas ayudan a usted y a los autores a categorizar y organizar el contenido de manera eficaz, lo que permite un mejor filtrado, seguimiento y generación de informes.

Consulte [Etiquetas de catálogo en Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md) para obtener más información.


>[!NOTE]
>
>* Etiquetas obligatorias: puede elegir que las etiquetas de catálogo sean obligatorias para los autores durante la creación del curso.
>* Flujo de trabajo de autor: los autores deben añadir etiquetas de cumplimiento al crear o editar cursos para garantizar una categorización adecuada.

## Carpeta de contenido

Las carpetas de contenido le permiten organizar y administrar el contenido creando carpetas privadas o públicas. Esta funcionalidad garantiza que el contenido solo sea accesible para autores o grupos específicos, lo que proporciona un mayor control sobre la visibilidad y la administración del contenido.

**Puntos clave:**

Una carpeta es un repositorio de contenido, que es un subconjunto de toda la biblioteca de contenido disponible en una cuenta con las siguientes propiedades:

* Solo usted (administrador) puede crear, editar o eliminar una carpeta.
* Puede controlar el acceso a las carpetas como parte de la definición de funciones sólo para administradores personalizados.
* El contenido debe estar asociado en todo momento a al menos una carpeta. Para empezar, todo el contenido se asociará a la carpeta pública, que se puede modificar posteriormente.
* El contenido se puede asociar a varias carpetas durante su creación, lo que también será posible mediante una operación de copia.
* Todos los nombres de carpeta deben ser exclusivos en la cuenta; de lo contrario, se producirá un error al asignar un nombre a una carpeta.

Las carpetas solo controlan la visibilidad del contenido, pero no crean copias de este. Por lo tanto, al modificar el contenido, los cambios se reflejarán en todas las carpetas asociadas.

**Carpeta pública**

Siempre habrá una carpeta pública en la cuenta y todo el contenido formará inicialmente parte de esta. Más adelante, los autores pueden mover el contenido de esta carpeta a otras. Una carpeta pública presenta las siguientes propiedades:

* De forma predeterminada, todos los tipos de autores podrán acceder a todo el contenido asociado a esta carpeta.
* El contenido que forma parte de una carpeta pública no puede incluirse en ninguna otra carpeta. Lo contrario también es cierto.

Esta carpeta no puede formar parte de la definición de función configurable. Por lo tanto, no tener una carpeta pública en la definición de función configurable no restringe el acceso a una carpeta pública.

**Carpeta privada**

Cualquier carpeta creada por usted es una carpeta privada.

**Agregar una carpeta de contenido**

Para añadir una carpeta de contenido, siga estos pasos:

1. Seleccione **[!UICONTROL Configuración]** > **[!UICONTROL Carpeta de contenido]**.
2. Seleccione **[!UICONTROL Agregar]** para crear una nueva carpeta.
3. Escriba el nombre y la descripción de la carpeta que desea crear.

   ![texto alt](assets/advanced-settings-picture1.png)

4. Seleccione **[!UICONTROL Guardar]** para crear la carpeta.

**Operaciones de carpeta**

* **[!UICONTROL Agregar una carpeta]**: Para agregar una carpeta, selecciónela y, a continuación, seleccione **[!UICONTROL Agregar]** en la esquina superior derecha de la pantalla.
* **[!UICONTROL Eliminar una carpeta]**: para eliminar una carpeta, selecciónela, seleccione el menú **[!UICONTROL Acciones]** y, a continuación, seleccione **[!UICONTROL Eliminar carpeta]**.

## Ubicaciones de clases

Cree y administre una biblioteca de ubicaciones de clase físicas o virtuales. Los autores y los administradores pueden utilizar estas ubicaciones para configurar eventos de formación con instructor (ILT). La función garantiza que los detalles de la clase, como los límites de plazas y la información de ubicación, estén preconfigurados y sean de fácil acceso.

Consulte [Agregar ubicaciones de clase en Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md) para obtener más información.

## Informes

Esta sección le permite configurar los paneles Cumplimiento y Éxito de grupo.

![texto alt](assets/advanced-settings-picture2.png)

Para obtener más información, consulte lo siguiente:

* [Tablero de cumplimiento](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Panel de éxito de grupo](/help/migrated/administrators/feature-summary/group-success-dashboard.md)


