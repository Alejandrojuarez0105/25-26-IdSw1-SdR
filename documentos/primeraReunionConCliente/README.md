## Idea principal

El cliente desea un **generador de exámenes** que programe automáticamente las fechas de los exámenes dentro del calendario establecido por la universidad.  
Cada examen debe incluir información detallada:

- Grado (ej. Psicología, Ingeniería Informática)
- Año (1.º, 2.º, 3.º, 4.º)
- Código de la asignatura (ej. ABC123)
- Tipo (obligatoria u optativa)
- Nombre de la asignatura (ej. Ingeniería de Software I)
- Profesor (ej. Manuel Masias)
- Número de alumnos (ej. 40 personas)
- Fecha del examen (ej. 13 de enero)
- Hora (8:30, 11:30, 14:30 o 17:30)
- Aula (ej. Aula 1.1)

El sistema debe conectarse a la **base de datos de la universidad** para obtener y registrar la información necesaria.

---

## ¿Por qué?

Actualmente, la programación de exámenes se realiza **manualmente mediante Excel**, lo cual consume tiempo, es propenso a errores y dificulta la detección de conflictos de horarios o disponibilidad de aulas.  
El cliente busca una **solución automatizada** que elimine el trabajo manual y optimice la organización de los exámenes.

---

## ¿Qué?

El proyecto consiste en desarrollar un **sistema automático de generación de calendarios de exámenes** que:

- Obtenga los datos de asignaturas, profesores, alumnos y aulas desde la base de datos de la universidad.
- Genere automáticamente las fechas y horarios disponibles.
- Verifique conflictos (por ejemplo, si un alumno tiene dos exámenes a la misma hora).
- Permita al usuario generar todo el calendario con un solo clic.

---

## ¿Para qué?

El objetivo principal es **automatizar completamente la planificación de exámenes**, reduciendo el esfuerzo manual y los errores humanos.  
Esto permitirá al cliente:

- Ahorrar tiempo en la organización.
- Asegurar la coherencia de horarios y disponibilidad.
- Publicar los calendarios directamente para los alumnos.

Aunque los alumnos no interactúan con el sistema, **son beneficiarios indirectos** al acceder a un calendario más confiable y organizado.

---

## ¿Cómo?

El sistema se conectará a la **base de datos universitaria**, desde la cual recopilará la información necesaria.  
El proceso será completamente **automático**: el usuario solo deberá presionar un botón para generar el calendario completo.  
Entre sus funcionalidades principales se incluyen:

- Generación automática de fechas y horarios.
- Recopilación de datos de las asignaturas, profesores y alumnos.
- Verificación de posibles conflictos de exámenes.
- Emisión de advertencias (“warnings”) si un alumno tiene dos exámenes en el mismo horario.
- Exportación o publicación del calendario final.
