<div align=right>

[![](https://img.shields.io/badge/-Inicio-FFF?style=flat&logo=github&logoColor=black)](#-sistema-de-generación-automática-de-exámenes)
[![](https://img.shields.io/badge/-Primera_Reunión-FFF?style=flat&logo=googlemeet&logoColor=black)](/documents/primeraReunion/primeraReunion.md)
[![](https://img.shields.io/badge/-Modelo_del_Dominio-FFF?style=flat&logo=diagramsdotnet&logoColor=black)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/interaccionesClienteYCatedratico/images/DiagramaDeClasesDespuesDeCorreciones.png)
[![](https://img.shields.io/badge/-Casos_de_Uso-FFF?style=flat&logo=readthedocs&logoColor=black)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/tree/juarezAlejandro/casos-de-uso/images/primeraReunionConCliente)
[![](https://img.shields.io/badge/-Diagrama_de_Clases-FFF?style=flat&logo=uml&logoColor=black)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/veneroFrancisco/modelos/images/primeraReunionConCliente/DiagramaClasesGeneradorExamenes.png)
[![](https://img.shields.io/badge/-Documentación-FFF?style=flat&logo=bookstack&logoColor=black)](/documents)
[![](https://img.shields.io/badge/-Issues-FFF?style=flat&logo=github&logoColor=black)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/issues)
[![](https://img.shields.io/badge/-Glosario-FFF?style=flat&logo=github&logoColor=black)](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/veneroFrancisco/modelos/Glosario.md)

</div>

# 📚 Sistema de Generación Automática de Exámenes
### Universidad Europea del Atlántico (UNEATLANTICO)

![Estado](https://img.shields.io/badge/Estado-En%20Desarrollo-yellow)
![Curso](https://img.shields.io/badge/Curso-2025--2026-green)
![Grupo](https://img.shields.io/badge/Grupo-5-orange)

---

## 📋 Descripción del Proyecto

El **Sistema de Generación Automática de Exámenes** es una solución desarrollada para la Universidad Europea del Atlántico que automatiza la planificación y asignación de fechas, horarios y aulas para los exámenes finales. El sistema elimina conflictos de horarios y optimiza el uso de los recursos disponibles.

Este proyecto forma parte de la asignatura **Ingeniería del Software I** y constituye un caso real de desarrollo de software con aplicación práctica en la gestión académica universitaria.
[Ver Contenidos](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR/blob/juarezAlejandro/README.md)
---

## 👥 Equipo de Desarrollo

### 👤 Cliente
- **David García** - Cliente y representante de la Universidad Europea del Atlántico

### 👨‍💻 Integrantes del Equipo

| Nombre | Rol | GitHub |
|--------|-----|--------|
| **Alejandro Juárez** | Coordinador del Proyecto | [@Alejandrojuarez0105](https://github.com/Alejandrojuarez0105) |
| **Rubén Tresgallo** | Desarrollador | [@rubentresgallob](https://github.com/rubentresgallob) |
| **Francisco Venero** | Desarrollador | [@franvenero](https://github.com/franvenero) |
| **Manuela Grizoni** | Desarrolladora | [@ManuelaGrzoni](https://github.com/ManuelaGrzoni) |
| **Vivian Chao** | Desarrolladora | [@VivianChaoPeraza](https://github.com/VivianChaoPeraza) |

---

## 🎯 Objetivo del Proyecto

Desarrollar un sistema automatizado que:

-  Genere calendarios de exámenes de forma automática
-  Asigne recursos óptimamente (aulas, horarios, profesores)
-  Evite conflictos de horarios entre profesores y aulas
-  Reduzca el tiempo de planificación manual
-  Garantice transparencia en la asignación de exámenes
-  Facilite la gestión académica de la universidad

---

## ⚙️ Funcionalidades Principales

### Asignación Automática

El sistema asigna automáticamente los siguientes elementos:

| Elemento | Descripción |
|----------|-------------|
|  **Asignaturas** | Código y nombre de cada asignatura |
|  **Profesores** | Asignación de profesores responsables |
|  **Fechas** | Programación de fechas de exámenes |
|  **Franjas Horarias** | Asignación en horarios específicos |
|  **Aulas** | Selección de aulas según capacidad |

### Gestión de Conflictos

- **Sin solapamientos**: Garantiza que un profesor no tenga dos exámenes simultáneos
- **Optimización de aulas**: Asigna aulas según capacidad requerida
- **Distribución equitativa**: Balance en la carga de exámenes por día
- **Validación automática**: Verificación de restricciones en tiempo real

### Franjas Horarias Disponibles

```
┌─────────────────┬──────────────┐
│ Franja Horaria  │    Horario   │
├─────────────────┼──────────────┤
│ Mañana I        │   08:30 h    │
│ Mañana II       │   11:30 h    │
│ Tarde I         │   14:30 h    │
│ Tarde II        │   17:30 h    │
└─────────────────┴──────────────┘
```

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Tecnologías |
|-----------|-------------|
|  **Control de Versiones** | GitHub |
|  **Gestión de Tareas** | GitHub Issues, GitHub Projects |
|  **Documentación** | Markdown, Diagramas UML |


---

## 📁 Estructura del Repositorio

```
25-26-IdSw1-SdR/
├── documents/           # Documentación del proyecto
│   └── primeraReunion/  # Actas de reuniones
├── images/              # Imágenes y recursos gráficos
│   └── modelosUML/      # Diagramas UML
├── modelosUML/          # Modelos del dominio
└── README.md            # Este archivo
```

---

## 📞 Contacto

| Rol | Nombre | Enlace |
|-----|--------|--------|
| 👤 **Cliente** | David García | - |
| 👨‍💻 **Coordinador** | Alejandro Juárez | [@Alejandrojuarez0105](https://github.com/Alejandrojuarez0105) |
| 🔗 **Repositorio** | 25-26-IdSw1-SdR | [Ver en GitHub](https://github.com/Alejandrojuarez0105/25-26-IdSw1-SdR) |

**Asignatura**: Ingeniería del Software I  
**Universidad**: Universidad Europea del Atlántico (UNEATLANTICO)

---

<div align="center">

Desarrollado por el Equipo 5 - UNEATLANTICO 2025-2026

</div>
