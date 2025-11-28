# Modelo del dominio

En este apartado se encuentran los elementos que conforman el **modelo del dominio** del proyecto. Incluye:

- Diagrama de clases del generador de fechas de exámenes para la gestión académica universitaria.
- Diagrama de objetos del generador.
- Diagrama de objetos extenso (para verificación de relaciones y consistencia).
- Diagrama de estados de un examen.
- Diagrama de estados del generador de exámenes.

## Tabla de diagramas

|      [Diagrama de clases](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeClasesGeneradorExamenes.png)       |      [Diagrama de objetos](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeObjetosGeneradorExamenes.png)      | [Diagrama de objetos - extenso](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/SegundoDiagramaDeObjetosGeneradorExamenes.png) | [Diagrama de estados de un examen](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeEstadosDeUnExamen.png) | [Diagrama de estados del generador](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeEstadosGeneradorExamenes.png) |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeClasesGeneradorExamenes.png?raw=true" width="250"> | <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeObjetosGeneradorExamenes.png?raw=true" width="250"> | <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/SegundoDiagramaDeObjetosGeneradorExamenes.png?raw=true" width="250"> |  <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeEstadosDeUnExamen.png?raw=true" width="250">   |   <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/DiagramaDeEstadosGeneradorExamenes.png?raw=true" width="250">   |

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
