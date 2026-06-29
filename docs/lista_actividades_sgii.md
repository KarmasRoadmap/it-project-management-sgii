# LISTA DE ACTIVIDADES — SGII: Sistema de Gestión de Inventarios Inteligente
## Project Activity List & Network Diagram
### Duración total planificada: 57 días hábiles (~11.4 semanas) | Duración real (con impactos): 62 días hábiles

---

## 1. TABLA DE ACTIVIDADES

| ID    | Actividad                                          | Predecesor(es)  | Duración Plan (d) | Duración Real (d) | Responsable (Nombre y Rol)                | Ruta Crítica |
|-------|----------------------------------------------------|-----------------|--------------------|--------------------|-------------------------------------------|:---:|
| **FASE 1: INICIACIÓN**                             |                    |                    |                    |                    |     |
| A01   | Kickoff del Proyecto                               | —               | 2                  | 4 ⚠                | Ana García (Project Manager)              | ★   |
| A02   | Análisis de Stakeholders                           | A01             | 2                  | 2                  | Ana García (Project Manager)              | ★   |
| A03   | Desarrollo del Project Charter                     | A02             | 2                  | 2                  | Ana García (Project Manager)              | ★   |
| **FASE 2: PLANIFICACIÓN**                          |                    |                    |                    |                    |     |
| A04   | Relevamiento de Requerimientos                     | A03             | 3                  | 3                  | Ana García (PM) + Todo el equipo          | ★   |
| A05   | Creación de EDT / WBS                              | A04             | 2                  | 2                  | Ana García (Project Manager)              |     |
| A06   | Plan de Gestión de Riesgos                         | A04             | 2                  | 2                  | Ana García (Project Manager)              | ★   |
| A07   | Plan de Comunicaciones                             | A05, A06        | 1                  | 1                  | Ana García (Project Manager)              | ★   |
| A08   | Cronograma y Línea Base                            | A07             | 2                  | 2                  | Ana García (Project Manager)              | ★   |
| **FASE 3: DISEÑO**                                 |                    |                    |                    |                    |     |
| A09   | Arquitectura del Sistema                           | A08             | 3                  | 3                  | Carlos Ruiz (Desarrollador Frontend)      | ★   |
| A10   | Diseño de Base de Datos (PostgreSQL)               | A09             | 2                  | 2                  | María López (Desarrolladora Backend)      |     |
| A11   | Diseño UI/UX (Wireframes y Prototipos)              | A09             | 4                  | 4                  | Carlos Ruiz (Desarrollador Frontend)      |     |
| A12   | Diseño de Arquitectura ML (scikit-learn)           | A09             | 3                  | 3                  | Pedro Martínez (Data Scientist / ML)      | ★   |
| **FASE 4: DESARROLLO — FRONTEND**                  |                    |                    |                    |                    |     |
| A13   | Setup Frontend (React + TypeScript)                | A11             | 2                  | 2                  | Carlos Ruiz (Desarrollador Frontend)      |     |
| A14   | Desarrollo de Componentes UI                       | A13             | 6                  | 6                  | Carlos Ruiz (Desarrollador Frontend)      |     |
| A15   | Vistas de Dashboard y Reportes                     | A14             | 5                  | 5                  | Carlos Ruiz (Desarrollador Frontend)      |     |
| A16   | Integración Frontend-Backend (consumo de API)      | A15             | 3                  | 3                  | Carlos Ruiz (Desarrollador Frontend)      |     |
| **FASE 4: DESARROLLO — BACKEND**                   |                    |                    |                    |                    |     |
| A17   | Setup Backend (Django + Django REST Framework)     | A10             | 2                  | 2                  | María López (Desarrolladora Backend)      |     |
| A18   | Desarrollo de API REST (endpoints CRUD)            | A17             | 6                  | 6                  | María López (Desarrolladora Backend)      |     |
| A19   | Módulo de Autenticación, Autorización y Seguridad  | A18             | 3                  | 3                  | María López (Desarrolladora Backend)      |     |
| A20   | Lógica de Negocio Core (Gestión de Inventarios)    | A19             | 5                  | 5                  | María López (Desarrolladora Backend)      |     |
| **FASE 4: DESARROLLO — IA (RUTA CRÍTICA)**         |                    |                    |                    |                    |     |
| A21   | Adquisición y Limpieza de Datos Históricos         | A12             | 3                  | 3                  | Pedro Martínez (Data Scientist / ML)      | ★   |
| A22   | **Desarrollo del Modelo ML Predictivo (CRÍTICA)**  | A21             | **15**             | **18** ⚠           | Pedro Martínez (Data Scientist / ML)      | ★   |
| A23   | Evaluación y Optimización del Modelo               | A22             | 2                  | 2                  | Pedro Martínez (Data Scientist / ML)      | ★   |
| A24   | Integración del Modelo ML con API (inferencia)     | A23             | 3                  | 3                  | Pedro Martínez (Data Scientist / ML)      | ★   |
| **FASE 5: PRUEBAS**                                |                    |                    |                    |                    |     |
| A25   | Pruebas Unitarias (Frontend)                       | A16             | 2                  | 2                  | Laura Fernández (QA Engineer)             |     |
| A26   | Pruebas Unitarias (Backend)                        | A20             | 2                  | 2                  | Laura Fernández (QA Engineer)             |     |
| A27   | Pruebas de Integración (end-to-end)                | A24, A25, A26   | 4                  | 4                  | Laura Fernández (QA Engineer)             | ★   |
| A28   | Pruebas de Rendimiento y Carga                     | A27             | 2                  | 2                  | Laura Fernández (QA Engineer)             | ★   |
| A29   | Pruebas de Aceptación de Usuario (UAT)             | A28             | 2                  | 2                  | Laura Fernández (QA) + Ana García (PM)    | ★   |
| **FASE 6: DESPLIEGUE**                             |                    |                    |                    |                    |     |
| A30   | Preparación de Entorno de Producción (Docker)      | A29             | 2                  | 2                  | María López (Desarrolladora Backend)      | ★   |
| A31   | Migración de Datos (legado → nuevo sistema)        | A30             | 1                  | 1                  | María López (Dev2) + Pedro Martínez (ML)  | ★   |
| A32   | Go-Live / Puesta en Marcha (5 sucursales)          | A31             | 1                  | 1                  | María López (Desarrolladora Backend)      | ★   |
| A33   | Capacitación a Usuarios Finales                    | A29             | 2                  | 2                  | Ana García (Project Manager)              |     |
| **FASE 7: CIERRE**                                 |                    |                    |                    |                    |     |
| A34   | Revisión de Desempeño del Proyecto                 | A32, A33        | 1                  | 1                  | Ana García (Project Manager)              | ★   |
| A35   | Informe de Cierre y Lecciones Aprendidas           | A34             | 1                  | 1                  | Ana García (Project Manager)              | ★   |

> **Leyenda:** ★ = Pertenece a la ruta crítica | ⚠ = Impacto del escenario (desviación real vs. plan)

---

## 2. DIAGRAMA DE RED (ACTIVIDAD-NODO / AoN)

```
                          ┌──────────────────────────────────────────────────────────────┐
                          │                    RUTA CRÍTICA (★)                           │
                          │  57 días plan | 62 días real                                  │
                          └──────────────────────────────────────────────────────────────┘

FASE 1: INICIACIÓN (7 d plan / 9 d real)
  ┌──────┐     ┌──────┐     ┌──────┐
  │ A01  │────▶│ A02  │────▶│ A03  │
  │  2/4 │     │  2/2 │     │  2/2 │
  └──────┘     └──────┘     └──────┘
      ★            ★            ★

FASE 2: PLANIFICACIÓN (10 d plan / 10 d real)
  ┌──────┐     ┌──────┐     ┌──────┐     ┌──────┐
  │ A04  │──┬─▶│ A05  │──┬─▶│ A07  │────▶│ A08  │
  │  3/3 │  │  │  2/2 │  │  │  1/1 │     │  2/2 │
  └──────┘  │  └──────┘  │  └──────┘     └──────┘
      ★     │            │                   ★
            │  ┌──────┐  │
            └─▶│ A06  │──┘
               │  2/2 │
               └──────┘
                  ★

FASE 3: DISEÑO (7 d plan / 7 d real)
                      ┌──────────────────────────────┐
                      │         ┌──────┐              │
                      │         │ A10  │────▶ (BE)    │
                      │         │  2/2 │              │
                      │         └──────┘              │
  ┌──────┐     ┌──────┤                              │
  │ A08  │────▶│ A09  │   ┌──────┐                   │
  │  2/2 │     │  3/3 │──▶│ A11  │────▶ (FE)         │
  └──────┘     └──────┤   │  4/4 │                   │
      ★            ★  │   └──────┘                   │
                      │   ┌──────┐                   │
                      └──▶│ A12  │────▶ (IA)         │
                          │  3/3 │                   │
                          └──────┘                   │
                             ★                       │
                          └──────────────────────────┘

FASE 4: DESARROLLO (3 tracks paralelos ──────────────────────────────)

  Track FRONTEND (16 d):
    ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
    │ A13  │───▶│ A14  │───▶│ A15  │───▶│ A16  │──────────────┐
    │  2/2 │    │  6/6 │    │  5/5 │    │  3/3 │              │
    └──────┘    └──────┘    └──────┘    └──────┘              │
                                                              │
  Track BACKEND (16 d):                                       │
    ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐             │
    │ A17  │───▶│ A18  │───▶│ A19  │───▶│ A20  │────────┐    │
    │  2/2 │    │  6/6 │    │  3/3 │    │  5/5 │        │    │
    └──────┘    └──────┘    └──────┘    └──────┘        │    │
                                                        │    │
  Track IA — RUTA CRÍTICA (23 d plan / 26 d real):      │    │
    ┌──────┐    ┌──────────────┐    ┌──────┐    ┌──────┐│    │
    │ A21  │───▶│     A22      │───▶│ A23  │───▶│ A24  ││    │
    │  3/3 │    │ 15/18 ⚠ CRIT │    │  2/2 │    │  3/3 ││    │
    └──────┘    └──────────────┘    └──────┘    └──────┘│    │
       ★              ★                  ★           ★ │    │
                                                       │    │
FASE 5: PRUEBAS (10 d)                                  │    │
                              ┌──────┐                  │    │
                       ┌─────▶│ A25  │──────────────┐   │    │
                       │      │  2/2 │              │   │    │
                       │      └──────┘              │   │    │
                       │      ┌──────┐              │   │    │
                       │      │ A26  │──────────┐   │   │    │
                       │      │  2/2 │          │   │   │    │
                       │      └──────┘          │   │   │    │
                       │                        │   │   │    │
    ┌──────┐     ┌──────┤      ┌──────┐         │   │   │    │
    │ A24  │────▶│      │─────▶│      │         │   │   │    │
    │  3/3 │     │      │      │      │         │   │   │    │
    └──────┘     │ A27  │      │      │         │   │   │    │
        ★        │  4/4 │◀─────┴──────┴─────────┘   │   │    │
                 │      │                            │   │    │
                 └──────┘                            │   │    │
                    ★                                │   │    │
                     │                               │   │    │
                     ▼                               │   │    │
                 ┌──────┐    ┌──────┐    ┌──────┐    │   │    │
                 │ A28  │───▶│ A29  │───▶│ A30  │    │   │    │
                 │  2/2 │    │  2/2 │    │  2/2 │    │   │    │
                 └──────┘    └──────┘    └──────┘    │   │    │
                    ★            ★           ★        │   │    │
                                          ┌──────┐   │   │    │
                                          │ A33  │◀──┘   │    │
                                          │  2/2 │        │    │
                                          └──────┘        │    │
                                              │           │    │
FASE 6: DESPLIEGUE (4 d)                       │           │    │
    ┌──────┐    ┌──────┐    ┌──────┐           │           │    │
    │ A30  │───▶│ A31  │───▶│ A32  │◀──────────┘           │    │
    │  2/2 │    │  1/1 │    │  1/1 │                       │    │
    └──────┘    └──────┘    └──────┘                       │    │
       ★           ★           ★                           │    │
                   │                                       │    │
                   ▼                                       │    │
FASE 7: CIERRE (2 d)                                      │    │
    ┌──────┐    ┌──────┐                                   │    │
    │ A34  │───▶│ A35  │◀──────────────────────────────────┘    │
    │  1/1 │    │  1/1 │
    └──────┘    └──────┘
       ★           ★


Notación: Cada nodo muestra "Axx / Duración_plan / Duración_real"
         ★ = Actividad en ruta crítica
```

---

## 3. RESUMEN DE LA RUTA CRÍTICA

### Secuencia crítica (planificada):

```
A01 → A02 → A03 → A04 → A06 → A07 → A08 → A09 → A12 → A21 → A22 → A23 → A24 → A27 → A28 → A29 → A30 → A31 → A32 → A34 → A35
```

| Métrica | Plan | Real (con impactos) | Δ |
|---------|------|----------------------|---|
| Duración total | **57 días hábiles** | **62 días hábiles** | **+5 días** |
| Holgura total (slack) ruta crítica | 0 días | 0 días | — |
| Actividades críticas | 21 de 35 | 21 de 35 | — |
| % actividades en ruta crítica | 60% | 60% | — |

### Análisis de impactos del escenario:

| Evento | Actividad afectada | Impacto en duración | Efecto en ruta crítica |
|--------|-------------------|---------------------|------------------------|
| Persona enferma (PM) | A01 – Kickoff | **+2 días** (2→4) | Desplaza toda la ruta crítica +2 días |
| Actividad crítica extendida | A22 – Modelo ML | **+3 días** (15→18) | Extiende la ruta crítica +3 días acumulados |
| Startup adelanta 1 semana | Deadline | **−5 días** (meta: 52 días) | Requiere compresión del cronograma |
| Costos materiales +4% | Presupuesto | Incremento ~$1,400 USD | Impacto financiero, no temporal |

### Cálculo del retraso neto:

```
Retraso = (+2 A01) + (+3 A22) = +5 días hábiles
Duración planificada: 57 días
Duración real proyectada: 62 días
Deadline adelantado (management): 57 − 5 = 52 días → Brecha: 62 − 52 = 10 días de desfase
```

> **Nota:** El desfase de 10 días entre la duración real (62 d) y el deadline adelantado (52 d) requeriría aplicar técnicas de **fast-tracking** (solapar actividades secuenciales de la ruta crítica) o **crashing** (asignar recursos adicionales a A22 para reducir su duración).

---

## 4. CAMINOS PARALELOS Y HOLGURAS

| Camino | Secuencia | Duración (plan) | Holgura Total |
|--------|-----------|-----------------|---------------|
| **Crítico (IA)** | A01→A02→A03→A04→A06→A07→A08→A09→A12→A21→A22→A23→A24→A27→A28→A29→A30→A31→A32→A34→A35 | **57 d** | **0 d** |
| Frontend | A09→A11→A13→A14→A15→A16→A25→(A27...) | 26 d hasta A25 | 8 d de holgura |
| Backend | A09→A10→A17→A18→A19→A20→A26→(A27...) | 25 d hasta A26 | 9 d de holgura |

---

## 5. EQUIPO DEL PROYECTO

| Sigla | Nombre | Rol | Responsabilidades clave |
|-------|--------|-----|------------------------|
| PM | **Ana García** | Project Manager | Kickoff, charter, planificación, gestión de stakeholders, cierre |
| Dev1 | **Carlos Ruiz** | Desarrollador Frontend | Arquitectura, UI/UX, React+TS, integración FE-BE |
| Dev2 | **María López** | Desarrolladora Backend | DB, Django+DRF, API REST, auth, lógica de inventario |
| Data/ML | **Pedro Martínez** | Data Scientist / ML Engineer | Arquitectura ML, datos, modelo predictivo, integración IA |
| QA | **Laura Fernández** | QA Engineer | Pruebas unitarias, integración, rendimiento, UAT |

---

*Documento generado según estándares PMI-PMBOK® — Heagney, Chapters 6 (WBS) y 7 (Scheduling, CPM, Gantt)*
