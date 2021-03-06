# Postwork Sesi贸n 04: Inscripci贸n de estudiantes

## 馃帺 Objetivo 

- Aplicar los conocimientos de la programaci贸n as铆ncrona mediante un proyecto real.
- Practicar el uso del EventLoop, a trav茅s de su uso para implementar un sistema de registro de alumnos.

## 馃幆 Requisitos 

- IntelliJ IDEA Community Edition
- JDK (o OpenJDK)
- Postwork de la sesi贸n anterior

## 馃殌 Desarrollo

**Realizar en equipo**

El director de la escuela solicit贸 que implementen un sistema de inscripci贸n de alumnos que notifique al maestro cuando un alumno se haya inscrito a un curso y adem谩s le muestre la cantidad de alumnos que tiene su curso sin bloquear la plataforma para que m谩s estudiantes puedan inscribirse al mismo tiempo.

Es por esto que han considerado que la implementaci贸n m谩s f谩cil ser谩 mediante el uso de un **EventLoop** que reciba la informaci贸n del alumno y el curso al que se quiere inscribir, notificando en un **worker** al maestro de la inscripci贸n.

Su tarea consiste en implementar el EventLoop necesario para esta plataforma, as铆 como el worker que notifique al maestro.

El diagrama 1 muestra c贸mo ser铆a el flujo del EventLoop

![diagrama1](img/diagrama1.png)

<br/>

Completen y dividan equitativamente las siguientes instrucciones para completar tu cuarto postwork:

1. Utilicen el proyecto del postwork 3.

2. Generen un nuevo package con el nombre de **async** 

3. Generen el modelo **SolicitudEstudiante** el cual tendr谩:

    - Constructor para recibir Estudiante y Curso.

    - M茅todos get y set tanto para Estudiante como para Curso.

4. Desarrollen la interfaz **NotificadorInscripcion**, la cual notificar谩 al maestro cada que se reciba una solicitud.

5. Generen la clase **ReceptorSolicitudes** 鈥淒ebe implementar de Runnable鈥? la cual se encargar谩 de:

    - Procesar y esperar las solicitudes dentro del **run()**.

    - Iniciar y detener la ejecuci贸n. 鈥淐ada uno en su m茅todo correspondiente鈥?.

    - Agregar nuevas solicitudes a la lista.

    - Retornar si se encuentra en ejecuci贸n. 鈥淎 trav茅s de un m茅todo鈥?.

6. Desarrollen la clase InscripcionAlumnos 鈥淐ontendr谩 el main鈥? la cual se encargar谩 de generar:

    - Cursos (Por lo menos cuatro).

    - Estudiantes (Por lo menos veinte).

7. En **InscripcionAlumnos** deber谩n agregar las solicitudes, con sus respectivos estudiantes y cursos. adem谩s notificar con un **event Loop** cuando:

    - Un alumno se inscribe a un curso.

    - En un worker al maestro de que se realiz贸 dicha inscripci贸n.
<br/>
<br/>

[Regresar ](../Readme.md)(Sesi贸n 04)

[Siguiente ](../../Sesion-05/Readme.md)(Sesi贸n 05)
