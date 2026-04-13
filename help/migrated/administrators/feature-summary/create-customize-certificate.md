---
title: Crear y personalizar un certificado
description: Los certificados personalizados en Adobe Learning Manager (ALM) permiten a los administradores y autores diseñar, administrar y emitir certificados personalizados para los alumnos.
jcr-language: en-us
source-git-commit: c012fdc19d3695add97661e290db19a90771748f
workflow-type: tm+mt
source-wordcount: '2630'
ht-degree: 0%

---


# Certificados personalizados en Adobe Learning Manager

## Introducción

Los certificados personalizados en Adobe Learning Manager cambian la forma en que los administradores diseñan, administran y entregan los certificados de finalización.

Los administradores pueden:

- Diseñe certificados en un editor visual al estilo de Canvas en lugar de escribir código.
- Adjunte certificados a cursos, rutas de aprendizaje y certificaciones con valores predeterminados flexibles.
- Usa fondos generativos impulsados por Adobes Firefly sin perder de vista las necesidades de marca y cumplimiento normativo.
- Migrar desde plantillas de HTML existentes y mantener la compatibilidad con registros históricos de alumnos.

El proceso de certificación sigue el modelo de logros y la insignia existente en Learning Manager, de modo que el comportamiento del alumno se mantiene familiar, mientras que los administradores y los equipos de asistencia dedican menos tiempo a las operaciones con certificados.

**Nota:** Las características de certificado que utilizan IA generativa están sujetas a cuota. El límite es de 10 000 solicitudes por usuario.

## Capacidades clave de la certificación personalizada

### Diseñador de certificados (editor de estilo de lienzo)

Un diseñador de certificados de arrastrar y soltar proporciona un lienzo de lo que ves es lo que obtienes (WYSIWYG) en el que los administradores pueden crear y administrar diseños sin conocimientos de HTML ni de CSS.

**Edición visual**

- Arrastra, coloca, cambia el tamaño, voltea y rota texto e imágenes.
- Alinear elementos (arriba, abajo, izquierda, derecha); enviar al fondo o traer al frente.
- Duplica o clona elementos para agilizar el trabajo de maquetación.

**Elementos compatibles**

- Campos de texto con controles de fuente, color, tamaño y alineación.
- Marcadores de posición dinámicos (por ejemplo, nombre del alumno, nombre del curso o certificación, fecha, campos de cuenta y campos de usuario activos donde solo se permiten atributos de un solo valor).
- Imágenes, incluidos logotipos e insignias, con preferencia de cambio de tamaño manual en lugar de ajuste automático para un diseño predecible.

**Fondo y diseño**

- Orientación vertical u horizontal (fijo después de la creación).
- Fondos como colores sólidos o imágenes con transparencia ajustable.
- Galería de imágenes con imágenes predefinidas y fondos compartidos.
- Controles de zoom (50 %-150 %) y alineación de cuadrícula o ajuste.

**Localización**

- Compatibilidad con varias configuraciones regionales, donde cada configuración regional tiene su propio archivo de diseño.
- Al añadir una configuración regional, su diseño se copia de la configuración regional predeterminada y, a continuación, se puede personalizar.
- Menú desplegable Idioma con vista previa por configuración regional en tiempo de diseño.

**Borrador y publicación del ciclo de vida**

- Guarde los diseños como borradores; los borradores no se pueden utilizar para la emisión.
- Después de la publicación, la estructura de diseño se bloquea; es posible que algunas ediciones requieran duplicar el diseño en su lugar.
- Vista previa en tiempo real del PDF para comprobar el diseño antes de la publicación.

### Catálogo y listado de plantillas

La página de lista **Diseño de certificado** ayuda a los administradores a administrar las plantillas de certificado a escala:

- Catálogo basado en mosaico con las fichas **Publicado** y **Borrador**.
- Buscar por título de certificado; filtrar por **Orientación**.
- Acciones en cada diseño:
   - Duplicar (para variantes).
   - Establecer como predeterminado en el nivel de **Cuenta**, **Curso**, **Ruta de aprendizaje** o **Certificación**.
   - Retirar o desactivar plantillas que ya no se utilizan.
- Compatibilidad con plantillas de proveedores de terceros que se pueden incorporar y reutilizar.

### Configuración y herencia flexibles

Los administradores pueden configurar certificados en varios niveles:

**Valores predeterminados de nivel de cuenta**

- Establezca un diseño de certificado predeterminado para todos los objetos de aprendizaje nuevos.
- El valor predeterminado actúa como punto de partida; los objetos de aprendizaje existentes no se cambian automáticamente cuando cambia el valor predeterminado de la cuenta.

**Modificaciones en el nivel de instancia**

- Configuración de nivel de instancia para cursos, certificaciones y rutas de aprendizaje, que incluye:
   - Construcción de marca por cohorte (por ejemplo, para diferentes regiones o cuentas de socios).
   - Diferentes diseños de certificados para ciclos de certificación recurrentes.

**Resolución y reserva de certificados**

Cuando un alumno termina la formación, Learning Manager elige un diseño en este orden:

- Configuración de instancias de objetos de aprendizaje
- Configuración de objetos de aprendizaje
- Plantilla predeterminada de objeto de aprendizaje
- Plantilla predeterminada de cuenta

### fondos generativos impulsados por Adobe Firefly

Para ayudar a los clientes a producir certificados coherentes y fieles a la marca a escala, el diseñador se integra con el Adobe Firefly:

- Los administradores generan fondos a partir de solicitudes de palabras clave y una combinación de colores (por ejemplo, &quot;minimalista, atención sanitaria, paleta verde azulado&quot;).
- Una biblioteca de palabras clave seleccionada admite sectores comunes (envío, atención sanitaria, etc.) para usuarios que no son diseñadores.
- Las imágenes generadas se añaden a la galería de fondo y se pueden reutilizar en las plantillas.
- El crédito y la asignación de niveles para el uso del Firefly en Learning Manager se definen en la política del producto.

### Migración de certificados de HTML heredados

Las plantillas de HTML o certificado ZIP existentes se conservan, pero no se pueden editar en el nuevo diseñador:

- Las plantillas heredadas se migran con indicadores como `isLegacy` / `is_active`.
- Aparecen como entradas no editables (sin vista previa WYSIWYG) y siguen siendo válidas para su uso histórico.
- Cuando las insignias se asocian a plantillas heredadas, la migración mantiene los certificados descargables; donde no se puede conservar la configuración, se aplican los valores predeterminados globales.

### Generación y precocción de PDF

Para mejorar el rendimiento en tiempo de ejecución y la experiencia del alumno:

- Los certificados se precubren en el momento de la finalización (cuando se completa el objeto de aprendizaje) y, a continuación, se almacenan en caché para que los alumnos puedan descargarlos rápidamente.
- Los flujos de alumnos existentes para descargar certificados a través de **Insignias** y **Logros** siguen siendo los mismos.

## El reto

En la actualidad, la administración de certificados en Learning Manager depende de un modelo con gran cantidad de código y de soporte:

**Alta dependencia del CSM y los equipos de soporte**: los administradores proporcionan archivos ZIP o de HTML que los CSM o los ingenieros cargan a través de herramientas internas. Cada cambio (marca, logotipos, texto normativo, firmas) requiere un ticket interno y un ciclo de implementación.

**Agilidad limitada para equipos empresariales**: los equipos de marketing, cumplimiento o RR. HH. suelen necesitar actualizaciones de certificados frecuentes y localizadas (idiomas, campañas, reglas específicas de cada país). El flujo de trabajo actual ralentiza esas actualizaciones y retrasa los programas de cumplimiento.

**Configuración fragmentada y herencia no clara**: Las plantillas de HTML heredadas se pueden establecer en el nivel de cuenta, objeto de aprendizaje predeterminado y objeto de aprendizaje con reglas de reserva complejas. Sin una configuración personalizada de varios niveles clara, puede resultar difícil ver qué plantilla se aplica a dónde.

**Restricciones de vinculación de insignias** Los certificados están estrechamente vinculados a **insignias**:

- Un certificado debe estar asociado a una insignia; no hay una emisión de solo certificado.
Ese acoplamiento puede complicar los cambios de diseño cuando los administradores desean certificados sin elementos de interacción.

**Creación no visual e incoherencia de marca**: los certificados basados en HTML son flexibles, pero necesitan aptitudes de interfaz de usuario que muchos administradores no tienen. Algunos clientes confían en certificados predeterminados genéricos, lo que debilita la coherencia de la marca.

**Brecha competitiva**: Algunos sistemas de administración de aprendizaje incluyen diseñadores de certificados personalizados nativos (por ejemplo, Docebo). El diseño de certificados de autoservicio en esta área ha sido un hueco conocido para Adobe Learning Manager.

El resultado es un cambio lento, un coste de asistencia elevado y una experiencia de creación que no cumple las expectativas del administrador para los certificados y las credenciales.

## Cómo abordan estos desafíos las certificaciones personalizadas

### Flujos de trabajo de autoservicio y fáciles de usar por el administrador

Estos son los flujos de trabajo:

- El diseñador de certificados y la lista reemplazan los scripts de carga y el aprovisionamiento interno del HTML con una experiencia orientada al administrador:
- Los administradores crean, publican y retiran diseños de certificados en Learning Manager sin código ni participación de CSM.
- Las actualizaciones de diseño (por ejemplo, la construcción de marca estacional o específica del socio) tardan minutos en la interfaz de usuario en lugar de tickets y ciclos de ingeniería.
- Los valores predeterminados de nivel de cuenta y de nivel de objeto de aprendizaje reducen la configuración repetitiva por objeto.

### Reducción de los gastos de asistencia y del riesgo operativo

Consolidando la administración de certificados en **Logros** con una experiencia de usuario clara:

- Las cargas de trabajo para las solicitudes de &quot;cargar o cambiar mi certificado&quot; se eliminan para los equipos de CSM e ingeniería.
- El producto aplica restricciones seguras (por ejemplo, orientación bloqueada, plantillas heredadas no editables) para reducir el riesgo de implementaciones existentes.
- Las plantillas heredadas migradas mantienen los certificados históricos disponibles sin esfuerzo adicional de asistencia técnica.

### Gobernanza, coherencia y control de la marca

Los valores predeterminados, Firefly y galerías ayudan a los clientes a:

- Envía plantillas de la marca una vez en el nivel de cuenta y sustituye solo cuando sea necesario.
- Usa fondos de Firefly dentro de las protecciones empresariales en lugar de recursos externos ad hoc.
- Regule los certificados mediante los estados de publicación y retirada, con borradores previsualizables antes del despliegue.

### Alineación con los flujos de insignia y certificado existentes

El diseño mantiene la ruta actual del alumno: los certificados se descargan desde **Insignias** y **Logros**, lo que limita el reciclaje.

### Rendimiento y escalabilidad

Certificados predefinidos y rendimiento objetivo de procesamiento controlado por JSON:

- Los certificados se generan al finalizar y se almacenan, por lo que la descarga es en realidad una recuperación estática.
- Los diseños basados en JSON mantienen la ligereza para el editor y el procesamiento en tiempo de ejecución a escala.

## Casos prácticos del mundo real

### Educación de clientes y partners: credenciales de marca a escala

**Escenario:** Una empresa de software administra academias de clientes y socios con cientos de programas en regiones y marcas.

- Utiliza plantillas predeterminadas a nivel de cuenta con fondos generados por el Firefly alineados con cada línea de productos.
- Añade diseños específicos de la configuración regional para títulos de certificación localizados, descargos de responsabilidad normativos y firmas.
- En el caso de los partners prémium, puede duplicar plantillas básicas y añadir marcas compartidas de partners (logotipo y texto legal) en el nivel de instancia.
- Los PDF predefinidos permiten a los partners descargar certificados justo después de completar las certificaciones de partners con una carga mínima en Learning Manager.

Este modelo se adapta a los ecosistemas de franquicias o de varias marcas en los que los certificados refuerzan el valor de la marca y del socio (por ejemplo, redes de socios de gran tamaño como RealPage).

### Formación normativa y de cumplimiento normativo: entornos multinacionales de gran cambio

**Escenario:** Una empresa regulada debe actualizar el texto del certificado de cumplimiento a menudo por país e idioma.

- La **edición dirigida por el administrador** permite a los equipos legales o de cumplimiento cambiar la redacción y los campos dinámicos sin tickets de ingeniería.
- Los diseños específicos de la configuración regional admiten **renuncias de responsabilidad específicas de cada país o región** y firmas en una red troncal de diseño compartido.
- La **lógica de reserva** garantiza que, si falta una plantilla de instancia de objeto de aprendizaje específica, el sistema seguirá utilizando valores predeterminados seguros y evitará errores de emisión.

Esto se aplica a la atención sanitaria, las finanzas, la administración pública y otros sectores en los que el texto del certificado cambia con frecuencia y se audita.

### Certificaciones periódicas con contenido de catálogo compartido o de igual a igual

**Escenario:** Una cuenta maestra de Learning Manager comparte contenido con varias **cuentas de igual a igual** (por ejemplo, muchas cuentas de cliente), cada una con certificaciones recurrentes y sus propios certificados.

- Las cuentas de igual a igual pueden **agregar cursos adquiridos a certificaciones recurrentes** y configurar **plantillas de certificados locales** en el nivel de instancia.
- Las actualizaciones del curso desde la cuenta maestra se transfieren a las repeticiones según lo previsto, mientras que los diseños de certificados pueden permanecer **por cliente**.

### Programas internos de capacitación y liderazgo

**Escenario:** Los programas internos (por ejemplo, aceleradores de gerentes o academias de productos) desean **certificados visualmente distintos** que los administradores puedan actualizar sin el trabajo del HTML.

- Los propietarios del programa pueden diseñar **plantillas de marca del programa** (por ejemplo, academias internas o elementos visuales de estilo MAP) sin conocimientos de HTML.
- Las modificaciones en el nivel de instancia permiten que diferentes cohortes o regiones utilicen variantes (por ejemplo, marcas regionales o específicas de cohorte).
- Los fondos de Firefly admiten **elementos visuales específicos de eventos o cohortes** con menos dependencia de los equipos de diseño.

### Transición desde certificados de HTML heredados

**Escenario:** Los clientes existentes usan certificados personalizados de HTML5 administrados mediante CSM.

- Las plantillas HTML o ZIP heredadas se migran y se marcan como heredadas, lo que conserva el uso y las descargas anteriores.
- Los administradores pueden pasar con el tiempo a las plantillas basadas en diseñadores, empezando por los programas de alta prioridad.
- Si la migración no puede conservar una asignación (por ejemplo, las insignias desactivadas a mitad de camino), el sistema vuelve a la plantilla predeterminada global para que los alumnos no estén bloqueados.

## Crear un certificado personalizado

**Requisito previo**

Para utilizar imágenes de Firefly, la instancia de Adobe Learning Manager debe estar integrada con Firefly.

1. Inicie sesión en Adobe Learning Manager como **administrador**.
2. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate1.png)
   *Desplazarse a logros en el panel de navegación izquierdo*

3. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate2.png)
   *La página Certificado*

4. En el área superior derecha de la página, seleccione **Nuevo certificado**. Se abre el cuadro de diálogo **Crear un nuevo certificado**.
5. Seleccione **Horizontal** o **Vertical**, según el aspecto que desee que tenga el certificado. Después de seleccionar una orientación, verá una plantilla en blanco y plantillas listas para usar para esa orientación.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate3.png)
   *Opción Horizontal o Vertical*

6. Seleccione la plantilla en blanco o una plantilla existente.
7. Escriba un nombre de certificado.
8. En el menú desplegable, seleccione un idioma predeterminado.
9. Seleccione **Crear**. Si eligió la plantilla en blanco, aparecerá un lienzo en blanco debajo del nombre del certificado.
10. Agregue elementos: **Texto**, **Imagen**, **Valor dinámico** y **Fondo de certificado**.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate4.png)
   *Agregar elementos al certificado*

11. Para **Texto**, agregue contenido bajo **Texto con formato previo** o **Plantillas de texto**, o agregue texto personalizado. El texto aparece en el lienzo. Cuando se selecciona texto, las opciones de formato aparecen sobre el lienzo. Para eliminar contenido que no quieras, selecciona el icono **Delete** en la esquina superior derecha del lienzo.
12. Para agregar imágenes, seleccione **Imagen** junto a **Agregar elementos**. Cargue imágenes de su equipo o seleccione imágenes de las listas de categorías.
13. Seleccione **Valor dinámico** para agregar detalles básicos, etiquetas de catálogo y campos activos.
14. Seleccione **Fondo de certificado** para aplicar colores o imágenes. Para crear imágenes con Adobe Firefly, seleccione **Generar imagen**.
15. En el campo de solicitud, describe lo que quieres (hasta 100 caracteres) y selecciona **Generar**. Aparecen cuatro opciones de imagen en función del mensaje.
16. Seleccione la imagen que desee. Se aplica como fondo del certificado.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate5.png)
   *Agregar imagen al certificado*

17. Seleccione **Vista previa** para revisar el certificado antes de publicarlo. Esto le ayuda a comprender cómo se ve el certificado.
   ![Crear un certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate6.png)
   *Obtener una vista previa del certificado*

18. En la vista previa, puede guardar en Google Drive, descargar, imprimir o utilizar otras opciones como las propiedades de anotación o documento.
19. Seleccione **Guardar como borrador** para continuar más tarde, o seleccione **Publish** para publicar el certificado. Después de la publicación, los alumnos pueden descargar el certificado cuando cumplan el hito configurado.

Después de guardar un certificado en **Publicado** o **Borrador**, puedes editarlo, clonarlo, cambiarle el nombre o eliminarlo.

## Editar un certificado personalizado

1. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
2. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
3. Seleccione la pestaña **Publicado** o **Borrador** para el certificado que desee.
4. Abra el menú de acciones (**...**) del certificado y seleccione **Editar**.
   ![Editar certificado desde el menú de acciones](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0001.png)
   *Opción Editar en el menú desplegable*

5. Realiza tus cambios.
6. Seleccione **Publish** o **Guardar como borrador**.

## Clonar un certificado personalizado

Utilice **Clone** cuando desee una copia de un certificado para un nuevo nombre o un caso de uso similar. Después de clonar, cambie el nombre del certificado para que tenga un nombre distinto; de lo contrario, el nombre puede coincidir con el origen aunque haya cambiado el diseño.

>[!NOTE]
>
>No se puede establecer un nombre nuevo mientras se guarda inmediatamente después de la clonación. Cambie el nombre del certificado después de guardarlo como borrador o después de publicarlo.

1. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
2. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
3. Seleccione la pestaña **Publicado** o **Borrador** para el certificado que desee.
4. Abra el menú de acciones (**...**) del certificado y seleccione **Clonar**.
   ![Clonar certificado desde el menú de acciones](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0002.png)
   *Opción Clonar en el menú desplegable*

5. Realiza tus cambios.

6. Seleccione **Publish** o **Guardar como borrador**.

7. Cambie el nombre del certificado clonado siguiendo los pasos de [Cambiar el nombre de un certificado personalizado](#rename-a-custom-certificate).

## Cambiar el nombre de un certificado personalizado

Puede cambiar el nombre de un certificado sin clonarlo.

1. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
2. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
3. Seleccione la pestaña **Publicado** o **Borrador** para el certificado que desee.

4. Abra el menú de acciones (**...**) del certificado y seleccione **Cambiar nombre**.
   ![Cambiar el nombre del certificado desde el menú de acciones](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0003.png)
   *Cambiar nombre de opción en el menú desplegable*

5. En el cuadro de diálogo **Cambiar nombre de certificado**, escriba el nuevo nombre.
   Cuadro de diálogo ![Cambiar nombre de certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0004.png)
   *Escriba un nuevo nombre*

6. Seleccione **Guardar**. Learning Manager muestra un mensaje de confirmación.

## Eliminar un certificado personalizado

La eliminación de un certificado no se puede deshacer. Proceda sólo si está seguro.

**Nota:** No se puede eliminar un certificado adjunto a un objeto de aprendizaje o una instancia.

1. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
2. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
3. Seleccione la pestaña **Publicado** o **Borrador** para el certificado que desee.
4. Abra el menú de acciones (**...**) del certificado y seleccione **Eliminar**. Adobe Learning Manager muestra un mensaje de confirmación.
   ![Eliminar certificado del menú de acciones](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0005.png)
   Opción *Eliminar en el menú desplegable*
   ![Confirmación de eliminación de certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0006.png)
   *Mensaje de confirmación*

5. Seleccione **Sí**. Si el certificado no está asociado a un objeto de aprendizaje o una instancia, Learning Manager completa la eliminación y puede mostrar otra confirmación.

## Establecer un certificado personalizado como certificado predeterminado

Puede establecer un certificado como predeterminado para:

- Cursos de formación
- Rutas de aprendizaje
- Certificaciones
- Todo

![Opciones de certificado predeterminadas](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0007.png)
*Establecer como certificado predeterminado*

1. En la sección **Configurar**, seleccione **Logros**. Se abre la página **Insignias**.
2. En el panel de navegación izquierdo, seleccione **Certificados**. Se abre la página **Certificados**.
3. Seleccione la pestaña **Publicado** o **Borrador** para el certificado que desee.
4. Abra el menú de acciones (**...**) del certificado, seleccione **Establecer como predeterminado** y, a continuación, seleccione una de las cuatro opciones. Learning Manager muestra un mensaje de confirmación.
5. Seleccione **Sí**. Learning Manager muestra otra confirmación. El certificado muestra una etiqueta **Predeterminado para** con la categoría seleccionada (por ejemplo, **Predeterminado para los cursos de formación**).
   ![Predeterminado para etiqueta de categoría en certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0008.png)
   *Después de convertirse en el certificado predeterminado*
