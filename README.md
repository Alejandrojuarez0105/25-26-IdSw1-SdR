# Avances para el cliente (David García)

En este README se incluye todo lo que se ha entendido que desea el cliente.

---

## Modelos

De momento hemos creado el **modelo del dominio**, con el cual creemos haber entendido la estructura general sobre la que se trabajará.

| Diagrama                                                                                                                                                                                        | Uso                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| [Diagrama de clases](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/primeraReunionConCliente/BocetoDiagramaClasesGeneradorExamenes.png)             | Dar una idea principal de lo superficial del proyecto.                                                   |
| [Diagrama de objetos](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/veneroFrancisco/modelos/images/primeraReunionConCliente/BocetoDiagramaObjetosGeneradorExamenes.png)           | Usar los atributos de las entidades definidas en el diagrama de clases.                                  |
| [Diagrama de estados (usuario)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/modelos/images/primeraReunionConCliente/BocetoDiagramaEstadosGeneradorExamenes.png) | Representa lo que hace el programa desde la vista del usuario, con algunas posibilidades de interacción. |
| [Diagrama de estados (sistema)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/grizoniManuela/images/modelosUML/diagramaDeEstadosPrimeraReunion.svg)                               | Muestra lo que realiza el sistema de manera más completa.                                                |

---

## Casos de uso

Los **casos de uso** representan a los actores (usuarios) y las acciones que pueden realizar en el sistema.  
A continuación, se detalla la distribución correspondiente:

| Actor                                                                                                                                                                                 | Qué puede hacer en el sistema                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Alumno](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/primeraReunionConCliente/BocetoCdUAlumno.png)                                | Puede:<br> \* Consulta de exámenes, dentro de esta puede:<br> - Descargar calendario.<br> - Ver calendario de exámenes.                                                                                                                                                                                                                                                                                                                           |
| [Profesor](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/primeraReunionConCliente/BocetoCdUProfesor.png)                            | Puede:<br> \* Consulta de exámenes, dentro de esta puede:<br> - Verificar conflictos de horario.<br> - Consultar aula asignada. <br> - Consultar fechas de exámenes.                                                                                                                                                                                                                                                                              |
| [Sistema](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/primeraReunionConCliente/BocetoCdUSistema.png)                              | Puede:<br> _ Conectarse a la base de datos universitaria.<br> _ Recopilar datos de asignaturas, profesores, aulas y alumnos.<br> _ Asignar fechas y horarios automáticamente.<br> _ Verificar conflictos de exámenes.<br> _ Generar calendario final.<br> _ Emitir advertencias de conflictos.<br> \* Publicar calendario.                                                                                                                        |
| [Usuario administrativo](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/primeraReunionConCliente/BocetoCdUUsuarioAdministrativo.png) | Puede:<br> _ Iniciar sesión.<br> _ Generar calendario de exámenes.<br> _ Verificar conflictos de exámenes.<br> _ Consultar calendario generado.<br> _ Exportar o publicar calendario.<br> _ Cerrar sesión.<br> \* Gestión de datos universitarios, dentro de esta puede:<br> - Actualizar información de aulas.<br> - Actualizar información de profesores.<br> - Actualizar información de asignaturas.<br> - Obtener datos de la base de datos. |

---
