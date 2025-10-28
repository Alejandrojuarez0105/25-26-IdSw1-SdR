#  Primera Reunión con el Cliente – Proyecto de Planificación Automática de Exámenes

**Fecha:** 24/10/2025  
**Cliente:** David García  
**Proyecto:** Generador Automático de Horarios de Exámenes  

---

##  Propósito del Proyecto

El cliente plantea desarrollar una herramienta capaz de **automatizar la creación del calendario de exámenes finales** de la Universidad Europea del Atlántico.  

El sistema deberá asignar fechas, franjas horarias y aulas de forma inteligente, evitando solapamientos y mejorando la gestión actual del proceso. La meta principal es **reducir errores humanos y optimizar el uso de los recursos disponibles** (profesores, aulas y horarios).

---

##  Descripción General del Sistema

La aplicación tendrá como función principal **generar automáticamente el calendario de exámenes** a partir de la información de:

- **Asignaturas**, con su código y grado correspondiente.  
- **Profesores**, identificados por su nombre y código interno.  
- **Aulas**, considerando su capacidad y disponibilidad.  
- **Franjas horarias** definidas por la universidad.

El algoritmo deberá garantizar que:

- Ningún profesor o aula tenga dos exámenes asignados en la misma franja.  
- Las fechas se distribuyan correctamente dentro del período oficial de exámenes.  
- Se respeten las reglas de capacidad y los límites horarios establecidos.

---

##  Franjas Horarias Establecidas

| Franja | Hora de inicio |
|:-------|:----------------|
| 1 | 08:30 |
| 2 | 11:30 |
| 3 | 14:30 |
| 4 | 17:30 |

Estas franjas serán fijas y se aplicarán uniformemente durante todo el periodo de evaluación.

---

##  Entidades Identificadas

### **Asignatura**
- Código  
- Nombre  
- Profesor responsable  
- Grado o titulación  

### **Profesor**
- Nombre completo  
- ID o código de identificación  
- Lista de asignaturas que imparte  

### **Aula**
- Identificador o número  
- Capacidad máxima  

### **Examen**
- Fecha asignada  
- Franja horaria  
- Aula correspondiente  
- Asignatura asociada  

---

##  Funcionalidades Previstas

- **Generación automática del calendario de exámenes.**  
- **Asignación de aulas y horarios** sin conflictos entre profesores ni asignaturas.  
- **Gestión y edición de datos** de profesores, asignaturas y aulas.  
- **Visualización y exportación del calendario final**, para uso administrativo o docente.

---

##  Próximas Etapas

1. Definir los **casos de uso principales** del sistema.  
2. Diseñar el **modelo de dominio (UML)** inicial.  
3. Establecer las **reglas de negocio** y restricciones de asignación.  
4. Preparar los primeros **bocetos de interfaz o flujo de uso** para validarlos con el cliente en la siguiente reunión.

---

##  Observaciones Importantes

- El sistema deberá ser **intuitivo y fácil de manejar** por el personal administrativo.  
- En reuniones posteriores se definirán los **criterios de prioridad** (por ejemplo, qué asignaturas o grados deben programarse primero).
- El cliente insistió en la **prioridad de evitar solapamientos** entre exámenes y en **respetar la capacidad real de las aulas**.  

---

##  Conclusión

El cliente busca una solución que **automatice y optimice la planificación de exámenes**, reduciendo la carga manual y los conflictos de horarios.  
La próxima fase se centrará en definir los **casos de uso** y las **reglas de asignación** que servirán de base para la lógica del generador automático.
