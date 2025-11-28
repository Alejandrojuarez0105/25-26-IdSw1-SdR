# Casos de Uso - Sistema Generador de Calendarios de Exámenes

Este apartado muestra los **actores** y los **casos de uso** del sistema, junto con sus relaciones principales.

---

## Tabla de Actores y Casos de Uso

|                                                               Actor                                                               |                                                                                          Casos de Uso                                                                                           |                                                                                               Relaciones                                                                                                |                                                                      Imagen                                                                       |
| :-------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------: |
|    **[Alumno](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUAlumno.png)**    |                                                               - Ver Calendario de Exámenes<br>- Descargar Calendario de Exámenes                                                                |                                                                             Descargar Calendario **extend** Ver Calendario                                                                              |  <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUAlumno.png?raw=true" width="250">   |
|  **[Profesor](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUProfesor.png)**  |                                            - Comunicar Incidencias de Horario<br>- Ver Calendario de Exámenes<br>- Descargar Calendario de Exámenes                                             |                                                                             Descargar Calendario **extend** Ver Calendario                                                                              | <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUProfesor.png?raw=true" width="250">  |
|   **[Usuario](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUUsuario.png)**   | - Generar Calendario de Exámenes<br>- Verificar Conflictos de Exámenes con Incidencias de Profesores<br>- Consultar Calendario Generado<br>- Exportar o Publicar Calendario<br>- Exportar Datos |                                                                                                No aplica                                                                                                |  <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUUsuario.png?raw=true" width="250">  |
| **[Generador](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUGenerador.png)** |         - Procesar Solicitud de Generación<br>- Generar Fechas de Exámenes<br>- Revisar Posibles Conflictos<br>- Aplicar Correcciones Solicitadas<br>- Finalizar Asignación de Exámenes         | Procesar Generación **include** Generar Fechas<br>Generar Fechas **include** Revisar Conflictos<br>Revisar Conflictos **extend** Finalizar Asignación<br>Aplicar Correcciones **extend** Generar Fechas | <img src="https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/casos-de-uso/images/CdUGenerador.png?raw=true" width="250"> |

---

## Explicación de Relaciones

- **extend**: Significa que un caso de uso se ejecuta opcionalmente en función de otro (p. ej., Descargar Calendario se extiende de Ver Calendario).
- **include**: Significa que un caso de uso siempre se ejecuta como parte de otro (p. ej., Procesar Generación incluye Generar Fechas).

---

## Notas

- Los **actores** representan quién interactúa con el sistema, ya sea un usuario humano o un componente automatizado.
- Los **casos de uso** describen funcionalidades visibles del sistema para cada actor.
- El **Generador Automático** refleja la lógica interna que asegura la generación correcta del calendario de exámenes.
