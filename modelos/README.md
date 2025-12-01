# Modelo del dominio

## Diagramas

<div align=center>
	
|![](/modelos/images/DiagramaDeClasesGeneradorExamenes.svg)
|:-:
|[Código fuente](/modelos/modelosUML/DiagramaDeClasesGeneradorExamenes.puml)

</div>

### Diagrama de objetos

<div align=center>

|![](/modelos/images/DiagramaDeObjetosGeneradorExamenes.svg) | ![](/modelos/images/SegundoDiagramaDeObjetosGeneradorExamenes.svg) |
|:-:|:-:|
| [Código fuente](/modelos/modelosUML/DiagramaDeObjetosGeneradorExamenes.puml) | [Código fuente](/modelos/modelosUML/SegundoDiagramaDeObjetosGeneradorExamenes.puml) |

</div>

### Diagramas de estados

<div align=center>

|![](/modelos/images/DiagramaDeEstadosDeUnExamen.svg) | ![](/modelos/images/DiagramaDeEstadosGeneradorExamenes.svg) |
|:-:|:-:|
| [Código fuente](/modelos/modelosUML/DiagramaDeEstadosDeUnExamen.puml) | [Código fuente](/modelos/modelosUML/SegundoDiagramaDeObjetosGeneradorExamenes.puml) |

</div>

---

### Idea principal

El cliente desea un **generador automático de fechas de exámenes** que elabore el calendario completo siguiendo las reglas y restricciones establecidas por la universidad.

Cada examen debe contener:

- Nombre de la asignatura
- Grado al que pertenece
- Código de la asignatura
- Tipo (parcial o final)
- Profesor asignado
- Número de estudiantes
- Fecha del examen
- Hora (8:30, 11:30, 14:30 o 17:30)
- Aula asignada

El sistema deberá conectarse a la **base de datos universitaria**, desde donde obtendrá y actualizará toda la información relevante.

---

## ¿Por qué?

Actualmente, la universidad realiza la programación de exámenes **manualmente mediante hojas de Excel**, lo cual presenta varios problemas:

- Consumo elevado de tiempo.
- Riesgo de errores humanos.
- Dificultad para detectar conflictos de horarios o disponibilidad de aulas.

El cliente busca una **solución automatizada** que optimice este proceso y elimine el trabajo manual.

---

## ¿Qué?

El proyecto consiste en implementar un sistema capaz de:

- Obtener datos de asignaturas, profesores, aulas y estudiantes desde la base de datos.
- Generar automáticamente fechas, aulas y horarios disponibles.
- Permitir generar el calendario completo con un solo clic.

---

## ¿Para qué?

El objetivo es **automatizar la planificación de exámenes**, logrando:

- Ahorro significativo de tiempo.
- Menos errores en la programación.
- Información organizada y coherente para la universidad.

Aunque el sistema está dirigido a personal administrativo, **los estudiantes son beneficiarios indirectos** al recibir un calendario más fiable y mejor estructurado.

---

## ¿Cómo?

El sistema se conectará a la base de datos de la universidad y funcionará de manera completamente automática:

- Recopilará la información necesaria (asignaturas, profesores, estudiantes, aulas).
- Generará fechas y horarios siguiendo las reglas establecidas.
- Verificará conflictos entre exámenes.
- Permitirá exportar o publicar el calendario final.

En términos simples: **el usuario solo deberá presionar un botón para generar el calendario completo**.

---
