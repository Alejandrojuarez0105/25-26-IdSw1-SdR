# Generador de fechas de Exámenes — Diagrama de Contexto

## Información del artefacto

- **Proyecto**: Generador de fechas de Exámenes
- **Fase RUP**: Inception (Inicio)
- **Fecha**: 2025-12-02
- **Autor**: Alejandro Juárez

---

## Introducción

Este documento presenta el **diagrama de contexto del Generador de fechas de Exámenes**, modelado como una máquina de estados.
El diagrama describe la secuencialidad de navegación entre las funcionalidades del sistema, las precondiciones de acceso y los distintos modos de operación.

Se presentan dos variantes:

1. **Diagrama de contexto**, centrado en el flujo del sistema.
2. **Diagrama de contexto explicado**, que hace explícitos los roles permitidos en cada transición.

---

## Propósito

- Representar la perspectiva completa del sistema como un conjunto de estados bien definidos.
- Explicitar las transiciones que conectan cada funcionalidad.
- Identificar las precondiciones de navegación entre modos del sistema.
- Validar que todos los casos de uso están correctamente insertados en el flujo global.
- Ofrecer una herramienta para evaluar estados innecesarios o redundantes.
- Garantizar coherencia entre navegación, permisos y roles del sistema.

---

## Diagramas

### Diagrama de contexto (flujo del sistema)

<div align=center>

**Diagrama de contexto**

|![](/casos-de-uso/DiagramaDeContexto/images/DiagramaDeContextoGenerador.svg)
|:-:
|[Código fuente](/casos-de-uso/DiagramaDeContexto/modelosUML/DiagramaDeContextoGenerador.puml)

</div>

---

### Diagrama de contexto explicado (roles incluidos)

<div align=center>

**Diagrama de contexto explicado**

|![](/casos-de-uso/DiagramaDeContexto/images/DiagramaDeContextoExplicadoGenerador.svg)
|:-:
|[Código fuente](/casos-de-uso/DiagramaDeContexto/modelosUML/DiagramaDeContextoExplicadoGenerador.puml)

</div>

---

## Estados del sistema

| Estado                   | Descripción                         | Función principal                                 |
| ------------------------ | ----------------------------------- | ------------------------------------------------- |
| **SESION_CERRADA**       | Estado inicial del sistema          | Punto de entrada, requiere autenticación          |
| **SISTEMA_DISPONIBLE**   | Menú principal                      | Acceso a todas las funcionalidades                |
| **IMPORTAR_DATOS**       | Carga de datos iniciales            | Importación de información base                   |
| **GENERAR_CALENDARIO**   | Inicio del proceso de generación    | Configuración inicial para creación de calendario |
| **GENERANDO_EXAMENES**   | Proceso de generación activo        | Ejecución del algoritmo de asignación de fechas   |
| **CALENDARIO_GENERADO**  | Calendario disponible para revisión | Resultados iniciales listos para revisión         |
| **REVISAR_CALENDARIO**   | Ajuste y detección de conflictos    | Detección y corrección de conflictos              |
| **ASIGNACION_EXAMENES**  | Asignación final                    | Confirmación de horarios antes de publicar        |
| **PUBLICAR_CALENDARIO**  | Publicación oficial                 | Hacer el calendario accesible                     |
| **CONSULTAR_CALENDARIO** | Consulta de calendario              | Visualización de calendario publicado             |
| **DESCARGAR_CALENDARIO** | Descarga de calendario              | Obtención de copia del calendario                 |
| **EXPORTAR_CALENDARIO**  | Exportación avanzada                | Distribución del calendario                       |
| **VER_INCIDENCIAS**      | Comunicación de incidencias         | Comunicación y resolución de problemas            |

---

## Transiciones principales

### Autenticación y navegación al menú

- `iniciarSesion()`: SESION_CERRADA → SISTEMA_DISPONIBLE (proceso de autenticación exitoso)
- `cerrarSesion()`: SISTEMA_DISPONIBLE → SESION_CERRADA

### Flujo principal de generación de calendarios

#### Fase 1: Preparación de datos

- `importarDatos()`: SISTEMA_DISPONIBLE → IMPORTAR_DATOS
- `completarImportacion()`: IMPORTAR_DATOS → SISTEMA_DISPONIBLE

#### Fase 2: Generación inicial

- `generarCalendario()`: SISTEMA_DISPONIBLE → GENERAR_CALENDARIO
- `procesarGeneracion()`: GENERAR_CALENDARIO → GENERANDO_EXAMENES
- `generarFechasExamenes()`: GENERANDO_EXAMENES → CALENDARIO_GENERADO

#### Fase 3: Revisión y ajuste

- `revisarConflictos()`: CALENDARIO_GENERADO → REVISAR_CALENDARIO
- `aplicarCorrecciones()`: REVISAR_CALENDARIO → CALENDARIO_GENERADO
- `solicitarCorreccion()`: CALENDARIO_GENERADO → GENERANDO_EXAMENES

#### Fase 4: Finalización y publicación

- `finalizarAsignacion()`: REVISAR_CALENDARIO → ASIGNACION_EXAMENES
- `publicarCalendario()`: ASIGNACION_EXAMENES → PUBLICAR_CALENDARIO
- `completarPublicacion()`: PUBLICAR_CALENDARIO → SISTEMA_DISPONIBLE
- `completarAsignacion()`: ASIGNACION_EXAMENES → SISTEMA_DISPONIBLE

### Consulta y exportación

- `consultarCalendario()`: SISTEMA_DISPONIBLE → CONSULTAR_CALENDARIO
- `completarConsulta()`: CONSULTAR_CALENDARIO → SISTEMA_DISPONIBLE
- `descargarCalendario()`: CONSULTAR_CALENDARIO → DESCARGAR_CALENDARIO
- `volverAConsulta()`: DESCARGAR_CALENDARIO → CONSULTAR_CALENDARIO
- `exportarCalendario()`: SISTEMA_DISPONIBLE → EXPORTAR_CALENDARIO
- `completarExportacion()`: EXPORTAR_CALENDARIO → SISTEMA_DISPONIBLE

### Gestión de incidencias

- `comunicarIncidencias()`: SISTEMA_DISPONIBLE → VER_INCIDENCIAS
- `completarComunicacionIncidencias()`: VER_INCIDENCIAS → SISTEMA_DISPONIBLE

### Cancelaciones y retornos

- `cancelarGeneracion()`: GENERANDO_EXAMENES → SISTEMA_DISPONIBLE
- `cancelarRevision()`: CALENDARIO_GENERADO → SISTEMA_DISPONIBLE
- `cancelarRevisión()`: REVISAR_CALENDARIO → SISTEMA_DISPONIBLE

## Flujo natural del sistema

1. El usuario inicia sesión.
2. Carga los datos base.
3. Genera el calendario.
4. Revisa y corrige conflictos.
5. Asigna y publica el calendario.
6. Los usuarios finales lo consultan y pueden descargarlo.
7. Los profesores reportan incidencias y se reinicia el ciclo si es necesario.

## Validación del diagrama

### Completitud funcional

- ✓ Cubre todas las funcionalidades principales del sistema
- ✓ Incluye todos los actores identificados
- ✓ Representa el ciclo de vida completo del calendario

### Consistencia de navegación

- ✓ Todos los estados son alcanzables
- ✓ No hay estados huérfanos
- ✓ Existen rutas de retorno consistentes

### Claridad semántica

- ✓ Nombres de estados en participios/pasados
- ✓ Verbos en acciones específicas del usuario
- ✓ Roles explícitos en transiciones

## Consideraciones de implementación

### Precondiciones implícitas

1. **Para generar calendario**: Datos importados previamente
2. **Para revisar calendario**: Calendario generado existente
3. **Para publicar calendario**: Asignación finalizada sin conflictos

### Estados críticos

- **CALENDARIO_GENERADO**: Punto de control antes de revisiones
- **ASIGNACION_EXAMENES**: Último estado antes de publicación
- **PUBLICAR_CALENDARIO**: Estado irreversible (requiere confirmación)

### Manejo de errores

- Cancelaciones permitidas en estados de proceso activo
- Retorno al menú principal en operaciones fallidas
- Separación clara entre procesos automáticos y manuales
