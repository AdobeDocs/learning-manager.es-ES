---
description: La inscripción con un solo clic permite a los alumnos hacer clic en cualquier vínculo profundo a un módulo compartido por los administradores y acceder al contenido inmediatamente sin tener que pasar por varios pasos para hacer clic en inscribir e iniciar el curso. Ahorra tiempo y mejora el acceso al curso.
jcr-language: en_us
title: Configurar la inscripción con un solo clic en Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Configurar la inscripción con un solo clic en Adobe Learning Manager

## Cómo funciona la inscripción con un solo clic

La inscripción con un solo clic se basa en dos funciones de Adobe Learning Manager (ALM) que funcionan en conjunto:
Los vínculos profundos proporcionan una dirección URL directa a un curso u objeto de aprendizaje específico dentro de ALM. Puede incrustar estos vínculos (que son direcciones URL directas a los módulos) en correos electrónicos, portales de intranet o aplicaciones de terceros. Si un alumno aún no ha iniciado sesión al hacer clic en el vínculo, ALM le solicita que se autentique y, a continuación, le lleva directamente al curso.

Por lo general, resulta útil cuando los alumnos se encuentran en medio del trabajo y utilizan Slack o equipos, o cuando necesitan un curso rápido de actualización de dos minutos antes de viajar, asistir a una reunión o una llamada de ventas. Pueden acceder al contenido inmediatamente y recibir formación.
Los servicios relacionados con la inscripción inscriben automáticamente a un alumno en un curso antes de que el vínculo profundo inicie el reproductor del curso. Esto elimina el paso de inscripción manual que, de lo contrario, interrumpiría la experiencia del alumno.

Cuando un alumno selecciona un vínculo de inscripción con un clic, ALM los inscribe a través de la API en segundo plano y los redirige al curso mediante el vínculo profundo. El reproductor del curso se abre inmediatamente.

>[!NOTE]
>
>La inscripción se produce solo en el nivel del curso, no en objetos de aprendizaje de orden superior (rutas de aprendizaje o certificaciones).

## Generar un vínculo profundo para un módulo

1. Inicie sesión en Adobe Learning Manager como administrador.
2. Seleccione **Cursos** en el panel de navegación izquierdo.
   ![](assets/one-click-enroll1.png)
3. Seleccionar un curso
4. Seleccione **Instancias**.
   ![](assets/one-click-enroll2.png)
5. Seleccione la sección **Module** en la instancia cuyos vínculos profundos de módulos desee copiar. Los detalles del módulo se muestran en la sección expandida en la parte inferior de la instancia.
   ![](assets/one-click-enroll3.png)
6. Vaya al módulo cuyo vínculo desee copiar.
   ![](assets/one-click-enroll4.png)
7. Seleccione **Copiar vínculo**. Ahora se copia el vínculo profundo. Este vínculo profundo es un vínculo para abrir el módulo concreto en un curso.

Ahora puede utilizar este vínculo profundo para enviarlo a un alumno.
