# Casos de Uso - Sistema Generador de Calendarios de Exámenes

<div align=center>

**Generador**

|![](/casos-de-uso/images/CdUGenerador.svg)
|:-:
|[Código fuente](/casos-de-uso/modelosUML/CdUGenerador.puml)

</div>

---

<div align=center>

**Usuario**

|![](/casos-de-uso/images/CdUUsuario.svg)
|:-:
|[Código fuente](/casos-de-uso/modelosUML/CdUUsuario.puml)

</div>

---

<div align=center>

**Profesor**

|![](/casos-de-uso/images/CdUProfesor.svg)
|:-:
|[Código fuente](/casos-de-uso/modelosUML/CdUProfesor.puml)

</div>

---

<div align=center>

**Alumno**

|![](/casos-de-uso/images/CdUAlumno.svg)
|:-:
|[Código fuente](/casos-de-uso/modelosUML/CdUAlumno.puml)

</div>

---

## Tabla de Actores y Casos de Uso (explicación)

| Actor | Casos de Uso | Relaciones | Explicación |
|:-:|:-:|:-:|:-:|
| **Generador** | - Procesar Solicitud de Generación<br>- Generar Fechas de Exámenes<br>- Revisar Posibles Conflictos<br>- Aplicar Correcciones Solicitadas<br>- Finalizar Asignación de Exámenes | Procesar Generación **include** Generar Fechas<br>Generar Fechas **include** Revisar Conflictos<br>Revisar Conflictos **extend** Finalizar Asignación<br>Aplicar Correcciones **extend** Generar Fechas | Como funciona:<br>El **Generador** inicia la asignación de exámenes mediante **Procesar Solicitud de Generación**, lo que incluye automáticamente **Generar Fechas de Exámenes**.<br>Tras generar las fechas, revisa posibles conflictor con **Revisar Posibles Conflictos**, y puede aplicar correciones mediante **Aplicar Correcciones Solicitadas**, lo que opcionalmente afecta la generación de fechas.<br>Finalmente, la asignación se completa con **Finalizar Asignación de Exámenes**, que puede ejecutarse después de la revisión de conflictos. |
| **Usuario** | - Generar Calendario de Exámenes<br>- Verificar Conflictos de Exámenes con Incidencias de Profesores<br>- Consultar Calendario Generado<br>- Exportar o Publicar Calendario<br>- Importar Datos | No aplica | El usuario puede generar el calendario, revisar conflictos, consultar el resultado, exportar o publicar el calendario e importar datos. |
| **Profesor** | - Comunicar Incidencias de Horario<br>- Ver Calendario de Exámenes<br>- Descargar Calendario de Exámenes | Descargar Calendario **extend** Ver Calendario | El profesor puede ver el calendario y puede reportar incidencias. La descarga del calendario es opcional respecto a la visualización. |
| **Alumno** | - Ver Calendario de Exámenes<br>- Descargar Calendario de Exámenes | Descargar Calendario **extend** Ver Calendario | El alumno puede consultar el calendario y, opcionalmente, descargarlo. La descarga solo ocurre si antes se ve el calendario. |

---

## Explicación de Relaciones

- **extend**: Significa que un caso de uso se ejecuta opcionalmente en función de otro (p. ej., Descargar Calendario se extiende de Ver Calendario).
- **include**: Significa que un caso de uso siempre se ejecuta como parte de otro (p. ej., Procesar Generación incluye Generar Fechas).

---

## Notas

- Los **actores** representan quién interactúa con el sistema, ya sea un usuario humano o un componente automatizado.
- Los **casos de uso** describen funcionalidades visibles del sistema para cada actor.
- El **Generador** refleja la lógica interna que asegura la generación correcta del calendario de exámenes.
