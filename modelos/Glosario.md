# Glosario del Proyecto: Gestión de Exámenes






*Definición de las entidades principales que componen la estructura estática del sistema.*

| Término | Definición |
| :--- | :--- |
| **Universidad** | Entidad raíz de la organización académica (ej. "Uneatlantico"). Agrupa todas las facultades y define el marco institucional. |
| **Facultad** | Unidad administrativa y docente dentro de la universidad (ej. "Politécnica Superior") encargada de gestionar los distintos Grados. |
| **Grado** | Programa de estudios oficial (ej. "Informática") que agrupa un conjunto específico de asignaturas pertenecientes a un plan de estudios. |
| **Asignatura** | Materia académica identificada por un nombre y un código único (ej. "Ingeniería de Software - IDSW1").  |
| **Examen** | Evento de evaluación asociado a una asignatura específica. Posee atributos temporales (fecha) y descriptivos (tipo), y requiere recursos físicos y humanos para su realización. |
| **Profesor** | Docente asignado a un examen. Es el responsable de impartir la asignatura y supervisar la correcta ejecución del examen presencial. |
| **Aula** | Espacio físico identificado por un código único (ej. "Aula -2.6") donde se lleva a cabo el examen. Posee una capacidad máxima. |
| **Franja Horaria** | Intervalo de tiempo predefinido (hora de inicio y fin) asignado a un examen para establecer su duración (ej. "11:30 - 13:30"). |
| **Alumno** | Estudiante matriculado en la asignatura. En el contexto de planificación, se utiliza el dato agregado de alumnos inscritos para gestionar el aforo necesario. |

---

##  Referencias Cruzadas

*Relación entre los distintos términos del glosario para entender cómo se conectan entre sí.*

* **Aula ↔ Alumno (Capacidad):**
    El término **Aula** está directamente relacionado con **Alumno**. Para asignar un aula, debemos consultar la `cantidad de alumnos` inscritos y compararla con la `capacidad` del aula.

* **Examen ↔ Profesor (Supervisión):**
    Todo **Examen** requiere obligatoriamente la referencia a un **Profesor**. No puede existir un examen planificado sin un responsable asignado para supervisarlo.

* **Examen ↔ Franja Horaria (Planificación):**
    Un **Examen** no está completo si no tiene vinculada una **Franja Horaria**. 

* **Examen ↔ Aula (Ubicación):**
    Del mismo modo, un **Examen** debe hacer referencia a un **Aula**. Si el examen cambia de fecha, es probable que también deba cambiar de aula.




