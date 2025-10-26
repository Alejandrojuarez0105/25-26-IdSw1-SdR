# 🧩 Reunión con el Cliente – Proyecto de Generación Automática de Exámenes

**Fecha de la reunión:** 24/10/2025  
**Cliente:** David García


---

## 🎯 Objetivo del Proyecto

El cliente propone el desarrollo de un **sistema para la generación automática de fechas, horas y aulas** para los **exámenes finales** de la Universidad Europea del Atlántico.

El propósito principal es **automatizar la planificación de los exámenes**, evitando conflictos de horarios y mejorando la organización general del proceso.

---

## 🧠 Descripción General

El sistema deberá permitir **asignar de forma automática**:

- **Asignaturas** con sus respectivos **códigos**.  
- **Profesores responsables** de cada asignatura.  
- **Fechas y franjas horarias disponibles**.  
- **Aulas** donde se realizarán los exámenes.

Además, el sistema debe garantizar que:
- No se solapen exámenes para un mismo profesor o aula.  
- Las asignaturas tengan sus exámenes correctamente distribuidos dentro del calendario académico definido.  
- Las franjas horarias se respeten según las establecidas por la universidad.

---

## 🕐 Franjas Horarias Propuestas

El cliente especificó que los exámenes se realizan en las siguientes franjas horarias:

| Franja | Hora de inicio |
|:------:|:---------------:|
| 1 | 08:30 |
| 2 | 11:30 |
| 3 | 14:30 |
| 4 | 17:30 |

Estas franjas se aplicarán de manera uniforme a lo largo de los días del período de exámenes.

---

## 📘 Elementos Clave Identificados

Durante la reunión se identificaron los siguientes **elementos del dominio** que formarán parte del modelo inicial:

- **Asignatura**
  - Código de asignatura
  - Nombre
  - Profesor asignado
  - Grado o titulación a la que pertenece

- **Profesor**
  - Nombre y apellidos
  - Código o ID de profesor
  - Asignaturas que imparte

- **Aula**
  - Código de aula
  - Capacidad

- **Examen**
  - Fecha
  - Franja horaria
  - Aula asignada
  - Asignatura asociada

---

## 🧩 Funcionalidades a desarrollar

1. **Generación automática de calendario de exámenes**.  
2. **Asignación de aulas y franjas horarias** evitando solapamientos.  
3. **Gestión de datos de asignaturas, profesores y aulas**.  
4. **Visualización y exportación del calendario final de exámenes.**

---

## 🚧 Próximos pasos

- Definir **casos de uso principales** del sistema.  
- Elaborar el **modelo del dominio inicial** (UML).  
- Establecer **reglas de negocio** (restricciones y criterios de asignación).  
- Preparar la documentación base para la siguiente reunión con el cliente.

---

## 🗣️ Notas adicionales

- El cliente recalcó la importancia de **evitar conflictos de horarios** y **respetar las capacidades de las aulas**.  
- Se espera que el sistema sea **fácil de usar por el personal administrativo** de la universidad.  
- En futuras reuniones se concretarán los **criterios de priorización** para la asignación de aulas y fechas.

---


