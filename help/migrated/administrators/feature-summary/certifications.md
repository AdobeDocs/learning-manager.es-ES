---
description: Obtenga información sobre cómo crear certificaciones, inscribir alumnos y editar certificaciones publicadas.
jcr-language: en_us
title: Certificaciones
contentowner: manochan
exl-id: 406d1c33-aac3-47e1-9b32-83874976ce54
source-git-commit: 6f23c53b14d2c787e1c6ecb4eea9a3dc06f8e584
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 68%

---

# Certificaciones

Obtenga información sobre cómo crear certificaciones, inscribir alumnos y editar certificaciones publicadas.

Certifique a sus alumnos una vez o en un intervalo recurrente con esta función. Solo los administradores pueden definir las certificaciones para los alumnos.

Como administrador, puede crear un programa de certificación alojado internamente o administrado por un tercero. En caso de certificación interna, defina los cursos que un alumno debe completar para obtener la certificación. Publique el programa y después asígnelo a los alumnos.

## Crear una certificación {#createacertification}

1. Haga clic en **[!UICONTROL Certificación]** en el panel izquierdo.\
   Aparece una página con una lista de todos los borradores y el estado publicado de las certificaciones.

1. Vea las certificaciones en varios modos:

   1. Haga clic en **[!UICONTROL Draft]** para ver todas las certificaciones que están en estado de borrador. Debe completar su creación.
   1. Haga clic en **[!UICONTROL Publicado]** para ver todas las certificaciones publicadas por usted.
   1. Haga clic en **[!UICONTROL Todo]** para ver las certificaciones en todos los estados.
   1. Ordene y vea la lista de certificaciones en orden ascendente o descendente, o según la fecha en que las actualizó.

1. Haga clic en **[!UICONTROL Añadir]**.

   Aparece una nueva página de certificación.

![](assets/add-new-certification.png)

*Ver la página para añadir una certificación*

1. Añada el nombre del certificado y la descripción.

<table>
 <tbody>
  <tr>
   <th>Campo</th>
   <th>Descripción</th>
  </tr>
  <tr>
   <td>Días para completar</td>
   <td>Plazo para la certificación. Indique un valor numérico.</td>
  </tr>
  <tr>
   <td>Tipo</td>
   <td>
    <p>Tipo de certificación:</p>
    <ul>
     <li><b>Recurrente</b>: Elija esta opción si la certificación debe darse cada año, cada dos años o cada tres años.</li>
     <li><b>Perpetua</b>: Elija esta opción si la certificación debe darse una única vez.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Reasignación</td>
   <td>Elija si desea reasignar el certificado según la fecha de finalización o la fecha de inscripción.<br></td>
  </tr>
  <tr>
   <td>Validez (en meses) <br></td>
   <td>Especifique el intervalo de tiempo que la certificación seguirá siendo válida.</td>
  </tr>
  <tr>
   <td>Secuencia de los cursos<br></td>
   <td>Decida si los alumnos deben efectuar el curso en un orden secuencial o sin un orden concreto.<br></td>
  </tr>
  <tr>
   <td>Darse de baja<br></td>
   <td>Active o desactive la opción que permite a los alumnos darse de baja por su cuenta.</td>
  </tr>
  <tr>
   <td>Emisor del certificado<br></td>
   <td>
    <p>Elegir <b>Interno</b> si pertenece a su organización, o elija <b>Externo</b> para certificaciones de organizaciones externas.</p>
    <p>Si se elige <b>Certificación externa</b>, hay dos opciones más:</p>
    <ul>
     <li>Igual que fecha de aprobación<br></li>
     <li>Enviado por el alumno<br></li>
    </ul>
    <p>Los alumnos pueden especificar la fecha de finalización correcta para las certificaciones externas. En versiones anteriores, Captivate Prime establecía la fecha de finalización de forma predeterminada, según la fecha de aprobación del responsable. La fecha de finalización proporcionada por el alumno debe ser posterior a la fecha de creación del certificado<span>.</span></p></td>
  </tr>
  <tr>
   <td>Duración</td>
   <td>Si ha seleccionado Certificación externa, especifique la duración en minutos.</td>
  </tr>
  <tr>
   <td>Etiquetas</td>
   <td>Indique las etiquetas que desea asociar con el certificado. Las etiquetas son útiles para buscar el certificado.</td>
  </tr>
  <tr>
   <td>Seleccionar catálogos<br></td>
   <td>Elija el catálogo del que forma parte el certificado.</td>
  </tr>
 </tbody>
</table>

Seleccione el nivel de productos, roles y roles del **[!UICONTROL Recomendar para]** para sugerir esta ruta de aprendizaje a los usuarios que han manifestado interés en esos productos y funciones.

![](assets/recommend-for.png)

Elija los cursos que se añadirán a la certificación de **[!UICONTROL Cursos]** > **[!UICONTROL Catálogo]** .

Coloque el ratón sobre el mosaico de cada curso y haga clic en + para añadirlos a la certificación. Haga clic en **[!UICONTROL Vista previa]** para ver el curso como alumno antes de añadirlo.

1. Haga clic en **[!UICONTROL Plan de estudios]** para ver o verificar la lista de cursos que ha añadido.
1. Haga clic en **[!UICONTROL Publicar]**.

## Asignación de instancias de curso para certificaciones {#courseinstancemappingforcertifications}

Para asignar cursos e instancias de certificaciones:

1. En el panel izquierdo, haga clic en Certificaciones.
1. En la lista de certificaciones, seleccione Ver certificación de la certificación en la que desea asignar el curso y la instancia.
1. En el panel izquierdo, haga clic en Cursos. Se muestran los cursos para la certificación. Haga clic en Editar.
1. Coloque el ratón sobre el curso en el que desee definir la asignación de instancias; a continuación, seleccione Asignación de instancia del curso.
1. En la ventana que aparece, seleccione la instancia del curso que se entregará para la certificación que ha elegido.
1. Haga clic en Guardar.

Un administrador puede añadir cursos de clase y de clase virtual a un programa de aprendizaje. La sesión que el autor ha otorgado durante la creación del curso se convierte en la instancia predeterminada. Cuando el administrador añade cursos a un programa de aprendizaje, de forma predeterminada se asigna a la instancia predeterminada de todos los cursos, pero el administrador puede cambiar la asignación de la instancia. La cantidad de cursos añadidos a un programa de aprendizaje también figura en la página de instancias, como se muestra a continuación.

## Habilitar el control total del catálogo {#catalog}

Al igual que la concesión del control total del [catálogo para los aprendizajes o módulos](shared-catalog-full-control.md), puede habilitar el control total del catálogo para las certificaciones.

## Inscribir a alumnos en la certificación o darles de baja {#enrollorunenrolllearnerstothecertification}

Para obtener más información sobre los pasos necesarios para inscribirse, consulte [Inscribir alumnos](courses.md#main-pars_header_1058138132).

## Dar de baja alumnos {#unenrollmentforlearners}

Al crear certificaciones, el administrador tiene una opción para seleccionar si los alumnos pueden darse de baja de la certificación. Si el administrador selecciona la opción, el alumno puede darse de baja él mismo.

![](assets/unenrollment.png)

*Seleccionar dar de baja a alumnos*

## Marcar finalización {#markcompletion}

Los administradores pueden marcar una certificación como completa mediante la opción pertinente. Para marcar una certificación como completa, efectúe los pasos siguientes.

1. Abrir **[!UICONTROL Certificación]** > **[!UICONTROL Alumnos]**.

   Se abre la página Alumnos con la lista de alumnos inscritos.

1. Seleccione uno, varios o todos los alumnos para marcar Finalización de la certificación con la casilla de verificación que hay para cada alumno.
1. Haga clic en  **[!UICONTROL Acción]** > **[!UICONTROL Marcar finalización.]**

   Si una certificación tiene varios cursos, se marcará la finalización de todos ellos.

## Cursos obligatorios para certificaciones externas {#mandatory}

En versiones anteriores de Learning Manager, para obtener un certificado, no era obligatorio que el alumno en certificación externa completase el curso.

Ahora puede hacer que los cursos sean obligatorios habilitando la opción **[!UICONTROL Definir los cursos requeridos como obligatorios para la finalización del certificado]** en la ficha Programa durante la edición de la certificación.

## Editar una certificación publicada {#editingapublishedcertification}

Un administrador puede editar una certificación en un estado publicado. En este estado, el administrador puede editar todas las secciones de una certificación y volver a publicar.

Para editar una certificación publicada, haga clic en la tarjeta de certificación y, a continuación, en **[!UICONTROL Editar]** en la esquina superior derecha de la página.

Mientras edita las secciones de una certificación, si necesita abandonar la página, debe volver a publicar la certificación. Aparece un cuadro de diálogo de confirmación que le solicita volver a publicar la certificación.

![](assets/edit-a-certificate.png)

## Suscripción {#subscription}

Un administrador puede recopilar la puntuación de la prueba y los informes de estado del alumno. Se puede establecer la frecuencia del informe, el asunto del correo electrónico y el ID del correo electrónico de los destinatarios. Según la frecuencia establecida, el destinatario recibirá un correo electrónico con el informe adjunto.

![](assets/report-subscription.jpeg)

*Establecer la frecuencia del informe y otras propiedades*
