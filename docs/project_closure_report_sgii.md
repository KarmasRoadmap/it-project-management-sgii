# PROJECT CLOSURE REPORT
## SGII — Sistema de Gestión de Inventarios Inteligente
### Cadena Retail · 5 Sucursales

---

| **Campo** | **Detalle** |
|-----------|-------------|
| **Nombre del Proyecto** | SGII: Sistema de Gestión de Inventarios Inteligente |
| **Cliente / Sponsor** | Cadena Retail (5 sucursales) |
| **Project Manager** | Ana García |
| **Fecha de Inicio Planificada** | 3 de marzo de 2025 (Día hábil 1) |
| **Fecha de Cierre Planificada** | Día hábil 57 (~22 de mayo de 2025) |
| **Fecha de Cierre Real (proyectada)** | Día hábil 62 (~29 de mayo de 2025) |
| **Duración Planificada** | 57 días hábiles (11.4 semanas) |
| **Duración Real (proyectada)** | 62 días hábiles (12.4 semanas) |
| **Presupuesto Aprobado** | $35,000 USD |
| **Presupuesto Real (proyectado)** | $36,400 USD (+4% por inflación en materiales/equipo) |
| **Stack Tecnológico** | React + TypeScript · Django + DRF · PostgreSQL · Docker · scikit-learn |
| **Tamaño del Equipo** | 5 personas (PM + 2 Devs + 1 Data/ML + 1 QA) |
| **Metodología** | Predictiva (Waterfall con solapamiento en Desarrollo) |

---

## 1. RESUMEN EJECUTIVO

El proyecto SGII tuvo como objetivo diseñar, desarrollar y desplegar un sistema inteligente de gestión de inventarios para una cadena retail con 5 sucursales, incorporando un módulo de machine learning para predicción de demanda y optimización de stock. El proyecto se ejecutó bajo un enfoque predictivo estructurado en 7 fases (Iniciación → Planificación → Diseño → Desarrollo → Pruebas → Despliegue → Cierre), con una duración planificada de 57 días hábiles y un presupuesto de $35,000 USD.

Durante la ejecución, el proyecto enfrentó **tres impactos significativos** identificados en la reunión de revisión de la Semana 4 (Unit 2 — Project Execution Review):

1. **Enfermedad del PM (Ana García)** durante la actividad inicial A01 (Kickoff), generando un retraso de **2 días hábiles**.
2. **Extensión de la actividad crítica más larga** (A22 — Desarrollo del Modelo ML Predictivo), que requirió **3 días adicionales** por complejidad imprevista en el feature engineering.
3. **Solicitud de adelanto de 1 semana (5 días hábiles)** por parte de la startup cliente (*management request*), comprimiendo el deadline objetivo.
4. **Incremento del 4% en costos de materiales y equipo** por inflación, impactando el presupuesto en aproximadamente **$1,400 USD**.
5. **3 deliverables pendientes de liberación** al momento del corte de la Semana 4 (Project Charter A03, Línea Base A08, y UAT Sign-off A29), requiriendo seguimiento intensivo.

A pesar de estos desafíos, el proyecto **logró su objetivo principal**: el sistema fue desplegado exitosamente en las 5 sucursales con todas las funcionalidades core operativas, aunque con un retraso neto de 5 días hábiles y un sobrecosto del 4%.

---

## 2. HITS — COSAS QUE SE HICIERON BIEN (Fortalezas)

### HIT 1: Ejecución paralela efectiva de los tracks de desarrollo
La planificación de tres tracks simultáneos —Frontend (Carlos Ruiz), Backend (María López) e IA (Pedro Martínez)— permitió maximizar la utilización de recursos y reducir la duración total del proyecto. El solapamiento de actividades en la Fase 4 (Desarrollo) generó una compresión natural de ~16 días respecto a una ejecución secuencial. La coordinación mediante dailies stand-up de 15 minutos mantuvo la sincronización entre tracks sin overhead excesivo.

### HIT 2: Gestión proactiva del riesgo de enfermedad del PM
Cuando Ana García (PM) reportó enfermedad de 2 días durante el Kickoff (A01), se activó el plan de contingencia predefinido en el Plan de Gestión de Riesgos (A06): el Dev1 (Carlos Ruiz) asumió temporalmente la facilitación de la reunión de kickoff, y la documentación fue completada por el PM a su regreso. La recuperación fue total y no se generaron desviaciones adicionales en cascada más allá del desplazamiento de 2 días en la línea base.

### HIT 3: Rigor técnico en el módulo de IA (scikit-learn)
Aunque la actividad A22 (Desarrollo del Modelo ML) se extendió 3 días, el equipo de Data/ML (Pedro Martínez) mantuvo un estándar de calidad elevado: validación cruzada con k=5 folds, prevención de data leakage con separación temporal train/test, y documentación exhaustiva del feature engineering. El modelo final alcanzó un **RMSE un 18% inferior al baseline**, superando el criterio de aceptación definido en el UAT (A29).

### HIT 4: Entorno de despliegue con Docker — cero incidencias en Go-Live
La estandarización del entorno mediante contenedores Docker desde la Fase 3 (Arquitectura, A09) eliminó los clásicos problemas de "funciona en mi máquina". El Go-Live (A32) en las 5 sucursales se completó sin rollbacks ni incidencias críticas, validando la decisión de arquitectura tomada tempranamente. La migración de datos (A31) desde el sistema legado se ejecutó con un 99.7% de integridad verificada.

### HIT 5: Documentación de lecciones aprendidas en tiempo real
El PM mantuvo un registro continuo de lecciones aprendidas durante todo el ciclo de vida (no solo al cierre), capturando 23 lecciones en un repositorio compartido (Confluence). Esta práctica permitió que el Informe de Cierre (A35) se generara en 1 día, cuando el estimado original era de 2 días.

---

## 3. FAILURES — COSAS QUE SALIERON MAL (Debilidades)

### FAILURE 1: Retraso en el Kickoff por dependencia de persona única (Single Point of Failure)
**Evento del escenario:** Ana García (PM) se enfermó 2 días durante la actividad A01 (Kickoff del Proyecto).

**Análisis:** La actividad inicial del proyecto dependía exclusivamente del PM, sin un backup designado formalmente. Aunque el equipo respondió bien (ver HIT 2), el retraso de 2 días desplazó toda la ruta crítica, ya que A01 es la actividad raíz del diagrama de red. Este _single point of failure_ no había sido identificado en el Plan de Gestión de Riesgos (A06) con la severidad adecuada.

**Impacto:** +2 días en la duración total del proyecto.

**Causa raíz:** Ausencia de una matriz RACI que identificara responsabilidades de respaldo para actividades críticas del PM.

### FAILURE 2: Subestimación de la complejidad del módulo de ML (actividad crítica)
**Evento del escenario:** La actividad crítica más larga (A22 — Desarrollo del Modelo ML) requirió 3 días adicionales (15 → 18 días).

**Análisis:** Durante la planificación, la estimación de 15 días para A22 se basó en un benchmark optimista de proyectos similares, sin considerar adecuadamente la heterogeneidad de los datos históricos de las 5 sucursales (diferentes formatos, frecuencias de actualización y niveles de granularidad). El _feature engineering_ para normalizar series temporales de 5 fuentes dispares consumió 3 días más de lo estimado.

**Impacto:** +3 días adicionales en la ruta crítica. Efecto acumulado con Failure 1: +5 días totales.

**Causa raíz:** Estimación _bottom-up_ sin buffer de contingencia suficiente para actividades de I+D con alta incertidumbre técnica.

### FAILURE 3: 3 deliverables pendientes de liberación sin mecanismo de escalación
**Evento del escenario:** Al momento de la reunión de revisión de la Semana 4, 3 deliverables no habían sido formalmente liberados:
- **D1:** Project Charter (A03) — completado pero pendiente de firma del sponsor.
- **D2:** Línea Base del Cronograma (A08) — requería actualización post-retraso de A01.
- **D3:** UAT Sign-off (A29) — planificado, aún no ejecutado (en curso).

**Análisis:** No existía un proceso formal de _deliverable acceptance_ con SLAs definidos para la revisión y aprobación por parte del sponsor. El Project Charter (A03) estuvo 4 días hábiles esperando firma, bloqueando el inicio formal de la Fase 2 (Planificación). La falta de un mecanismo de escalación impidió resolver el bloqueo oportunamente.

**Impacto:** Riesgo de _scope creep_ por falta de baseline formal aprobada. Posible _rework_ si el sponsor solicitaba cambios tardíos al Charter.

**Causa raíz:** Proceso de gobernanza sin _acceptance criteria_ formales ni SLAs de revisión para deliverables clave.

### FAILURE 4: Incremento de costos por inflación no contemplado en reserva de contingencia
**Evento del escenario:** Los costos de materiales y equipo subieron un 4% por inflación.

**Análisis:** El presupuesto de $35,000 USD fue establecido con precios de cotización inicial, sin indexación por inflación ni cláusula de ajuste en el contrato con proveedores. La reserva de contingencia (10% = $3,500) fue consumida parcialmente por este incremento ($1,400), dejando menor margen para otros riesgos materializados. El equipo de adquisiciones no monitoreó indicadores macroeconómicos durante la ejecución.

**Impacto:** Sobrecosto de $1,400 USD (4% del presupuesto total). Reserva de contingencia reducida a $2,100 USD para riesgos remanentes.

**Causa raíz:** Presupuesto estático sin cláusulas de ajuste inflacionario. Ausencia de monitoreo de _cost performance index_ (CPI) en los reportes semanales.

### FAILURE 5: Solicitud de adelanto del deadline sin análisis de factibilidad (management request)
**Evento del escenario:** La startup solicitó adelantar el cronograma en 1 semana (5 días hábiles).

**Análisis:** La solicitud de adelanto (_management request_) fue recibida sin un análisis formal de impacto (_what-if analysis_). Con la duración real proyectada en 62 días hábiles y un target adelantado de 52 días, la brecha es de **10 días hábiles**, lo cual requeriría una compresión agresiva mediante fast-tracking o crashing. Ninguna de estas técnicas fue evaluada formalmente antes de comprometer el nuevo deadline con el sponsor, generando una expectativa no realista.

**Impacto:** Brecha de 10 días entre la duración real proyectada (62 d) y el deadline solicitado (52 d). Riesgo de pérdida de credibilidad con el sponsor si no se gestiona adecuadamente la expectativa.

**Causa raíz:** Falta de un _change control board_ (CCB) formal que evalúe solicitudes de cambio al cronograma antes de ser aceptadas.

---

## 4. IMPROVEMENTS — QUÉ HACER MEJOR LA PRÓXIMA VEZ (Lecciones Aprendidas)

### IMPROVEMENT 1: Implementar una matriz RACI con respaldos designados para actividades críticas
**Lección:** Ninguna actividad en la ruta crítica debe depender de una sola persona sin un backup formalmente designado y capacitado.

**Acción correctiva para futuros proyectos:**
- Incluir en el Plan de Gestión de Recursos una columna "Backup" para cada rol crítico (PM, Tech Lead, Data Scientist).
- Realizar _knowledge transfer sessions_ de 2 horas al inicio del proyecto entre el responsable primario y el backup.
- Establecer un protocolo de escalación: si una actividad crítica se retrasa >1 día por indisponibilidad del responsable, el backup asume inmediatamente.

### IMPROVEMENT 2: Adoptar estimación en 3 puntos (PERT) para actividades de I+D con alta incertidumbre
**Lección:** Las actividades de machine learning, data science y cualquier tarea con componente de investigación requieren estimaciones probabilísticas, no determinísticas.

**Acción correctiva para futuros proyectos:**
- Aplicar PERT (_Program Evaluation and Review Technique_) con estimaciones optimista (O), más probable (M) y pesimista (P) para actividades de I+D.
- Fórmula: `Duración esperada = (O + 4M + P) / 6`
- Incorporar un buffer de contingencia explícito del 20-25% sobre la duración esperada para actividades en la ruta crítica con varianza alta.
- Ejemplo para A22: O=12d, M=15d, P=22d → Duración esperada = (12 + 60 + 22)/6 = 15.7d con buffer de 3.1d (20%) = ~19d.

### IMPROVEMENT 3: Establecer un proceso formal de aceptación de deliverables con SLAs y escalación
**Lección:** Los deliverables completados pero no firmados son tan riesgosos como los no completados.

**Acción correctiva para futuros proyectos:**
- Definir en el Project Charter un SLA de revisión para el sponsor: 48 horas hábiles para deliverables ≤ 10 páginas, 72 horas para documentos extensos.
- Incluir cláusula de _deemed acceptance_: si el sponsor no responde dentro del SLA, el deliverable se considera aceptado provisionalmente (_conditional acceptance_).
- Implementar un _deliverable tracker_ visible en el dashboard del proyecto con semaforización: Verde (aprobado), Amarillo (en revisión, dentro de SLA), Rojo (vencido, requiere escalación).
- Designar un _deliverable owner_ responsable del seguimiento (puede ser el PM o un Project Coordinator).

### IMPROVEMENT 4: Incorporar cláusulas de ajuste inflacionario y monitoreo de CPI semanal
**Lección:** En proyectos de más de 8 semanas, la inflación puede erosionar significativamente las reservas de contingencia.

**Acción correctiva para futuros proyectos:**
- Incluir en los contratos con proveedores cláusulas de ajuste por inflación (basadas en IPC oficial o índice sectorial).
- Asignar una **reserva de gestión** (3-5% del presupuesto) separada de la reserva de contingencia, específicamente para riesgos macroeconómicos.
- Implementar monitoreo semanal del CPI (_Cost Performance Index_) mediante EVM (_Earned Value Management_):
  - CPI = EV / AC
  - Alerta temprana cuando CPI < 0.95 (sobrecosto > 5%).
- Incluir en el reporte semanal de estatus una sección de _Cost Variance_ con proyección a fin de proyecto (EAC = BAC / CPI).

### IMPROVEMENT 5: Formalizar un Change Control Board (CCB) para evaluar solicitudes de cambio al cronograma
**Lección:** Las solicitudes de cambio al cronograma (_management requests_) deben pasar por un proceso formal de evaluación de impacto antes de ser aceptadas o comunicadas al sponsor.

**Acción correctiva para futuros proyectos:**
- Establecer un CCB con al menos 3 miembros: PM, Sponsor (o representante), y un Tech Lead.
- Toda solicitud de cambio al cronograma debe ser evaluada con un _Integrated Change Control Form_ que contenga:
  - Análisis de impacto en ruta crítica (_what-if scenario analysis_).
  - Opciones de compresión (fast-tracking, crashing) con costo asociado.
  - Recomendación del PM (Aceptar / Rechazar / Aceptar con condiciones).
- El CCB sesiona semanalmente (o bajo demanda para cambios urgentes).
- Ningún cambio se comunica al equipo hasta que el CCB lo apruebe formalmente.

---

## 5. GOALS — EVALUACIÓN DE OBJETIVOS

| # | Objetivo | ¿Se logró? | Evidencia / Comentario |
|---|----------|:----------:|------------------------|
| **G1** | Desarrollar e implementar un sistema de gestión de inventarios funcional para 5 sucursales | ✅ **SÍ** | Sistema desplegado en producción en las 5 sucursales (A32 Go-Live exitoso sin rollbacks). Funcionalidades core operativas: CRUD de inventario, dashboard de stock, alertas de reposición. |
| **G2** | Incorporar un módulo de ML para predicción de demanda con RMSE ≤ baseline | ✅ **SÍ** | Modelo ML integrado y operativo (A24). RMSE un 18% inferior al baseline. Validación cruzada y pruebas de inferencia superadas en UAT (A29). |
| **G3** | Completar el proyecto en ≤ 57 días hábiles (línea base planificada) | ❌ **NO** | Duración real proyectada: 62 días hábiles (+5 días, +8.8% de desviación). Causas: enfermedad del PM en Kickoff (+2d) y subestimación del desarrollo ML (+3d). |
| **G4** | No exceder el presupuesto de $35,000 USD | ❌ **NO** | Presupuesto real proyectado: $36,400 USD (+$1,400, +4%). Causa: inflación en costos de materiales y equipo no contemplada en la línea base. |
| **G5** | Cumplir con los criterios de aceptación del UAT (A29) | ✅ **SÍ** | UAT completado con 94% de criterios superados en primera iteración. Los ítems pendientes (3 criterios menores de usabilidad) fueron cerrados en una iteración correctiva de 1 día sin impacto en el Go-Live. |
| **G6** | Capacitar a los usuarios finales de las 5 sucursales (A33) | ✅ **SÍ** | 42 usuarios capacitados (100% del target). Material de capacitación (manuales, videos) entregado y alojado en repositorio interno. Encuesta de satisfacción post-capacitación: 4.3/5. |

### Veredicto final: **PROYECTO EXITOSO CON DESVIACIONES CONTROLADAS**

El proyecto SGII se considera **exitoso** dado que:
- El **objetivo de negocio principal** (sistema funcional de gestión de inventarios con IA en 5 sucursales) fue alcanzado.
- Las desviaciones en cronograma (+8.8%) y costo (+4%) están dentro de umbrales aceptables para un proyecto de desarrollo de software con componente de I+D (benchmark industrial: ±10-15%).
- Las lecciones aprendidas documentadas (Sección 4) proporcionan un _playbook_ accionable para reducir estas desviaciones en futuros proyectos.

---

## 6. CIERRE FORMAL

| **Aspecto** | **Estado** |
|-------------|-----------|
| Aceptación formal del sponsor (UAT Sign-off) | ✅ Firmado — 29/05/2025 |
| Transferencia a operaciones (Go-Live A32) | ✅ Completado — 29/05/2025 |
| Documentación técnica entregada | ✅ Repositorio Confluence + GitHub Wiki |
| Capacitación a usuarios (A33) | ✅ Completado — 42/42 usuarios |
| Lecciones aprendidas registradas (A35) | ✅ 23 lecciones documentadas |
| Cierre de contratos con proveedores | ✅ 3/3 proveedores cerrados |
| Liberación del equipo | ✅ Equipo reasignado a nuevos proyectos |
| Archivo del proyecto | ✅ Documentación archivada en PMIS corporativo |

---

**Firma del Project Manager:**

_________________________________  
**Ana García**  
Project Manager — SGII  
Fecha: 30 de mayo de 2025

---

**Firma del Sponsor:**

_________________________________  
**[Nombre del Sponsor]**  
Sponsor — Cadena Retail  
Fecha: ___ / ___ / _______

---

*Documento generado según estándares PMI-PMBOK® — Project Closure Process (4.7 Close Project or Phase)*  
*Basado en Heagney, Chapters 6 (WBS), 7 (Scheduling, CPM, Gantt), y escenario Unit 2 — Project Execution Review (Week 4)*
