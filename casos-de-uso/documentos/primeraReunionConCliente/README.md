# Sistema Generador de Calendarios de Exámenes

## Descripción General

Este documento describe los **casos de uso** y los **actores** que interactúan con el **Sistema Generador de Calendarios de Exámenes**.  
Cada actor representa un tipo de cliente o componente que participa en la generación, consulta o gestión del calendario de exámenes.

---

## Actores del Sistema

El sistema cuenta con los siguientes actores principales:

1. **Usuario (Administrativo)**
2. **Profesor**
3. **Alumno**
4. **Sistema Generador (Interno)**

---

## Usuario (Administrativo)

El **Usuario** representa al personal administrativo encargado de gestionar los datos y supervisar el proceso de generación del calendario.

**Puede realizar las siguientes acciones:**

- Iniciar sesión
- Obtener datos de la base de datos
- Actualizar información de asignaturas
- Actualizar información de profesores
- Actualizar información de aulas
- Generar calendario de exámenes
- Verificar conflictos de exámenes
- Consultar calendario generado
- Exportar o publicar calendario
- Cerrar sesión

---

## Profesor

El **Profesor** consulta la información relacionada con sus exámenes y horarios.

**Puede realizar las siguientes acciones:**

- Consultar fechas de exámenes
- Consultar aula asignada
- Verificar conflictos de horario

---

## Alumno

El **Alumno** accede a la información del calendario final de exámenes para su consulta o descarga.

**Puede realizar las siguientes acciones:**

- Ver calendario de exámenes
- Descargar calendario

---

## Sistema Generador (Interno)

El **Sistema Generador** es un componente automatizado que recopila información, asigna fechas y genera el calendario final de manera autónoma.

**Puede realizar las siguientes acciones:**

- Conectarse a la base de datos universitaria
- Recopilar datos de asignaturas, profesores, aulas y alumnos
- Asignar fechas y horarios automáticamente
- Verificar conflictos de exámenes
- Emitir advertencias de conflictos
- Generar calendario final
- Publicar calendario
