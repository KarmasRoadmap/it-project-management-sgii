# REPORTE DE EJECUCIÓN DEL PROYECTO
## SGII — Sistema de Gestión de Inventarios Inteligente

**Fecha del reporte:** 29 de junio de 2026 — Cierre Semana 4  
**Versión:** 2.0 (posterior a integración de cambios)  
**Project Manager:** [Nombre del PM]  
**Equipo:** 5 integrantes  
**Duración planificada:** 12 semanas  
**Presupuesto aprobado (BAC):** $35,000 USD

---

# SECCIÓN 1: IT PROJECT MANAGEMENT DOCUMENTATION

## 1.1 Job Performance Data — Datos de Rendimiento del Trabajo

### 1.1.1 Métricas de Progreso Semanal (Semanas 1–4)

| Semana | Trabajo Planeado (PV) | Trabajo Real (EV) | Horas Planeadas | Horas Reales | Costo Planeado | Costo Real (AC) | % Completado Planeado | % Completado Real |
|--------|------------------------|-------------------|-----------------|--------------|----------------|-----------------|------------------------|-------------------|
| 1      | $2,800                 | $2,650            | 160             | 168          | $2,800         | $2,920          | 8.0%                   | 7.6%              |
| 2      | $5,700                 | $5,200            | 320             | 340          | $5,700         | $5,950          | 16.3%                  | 14.9%             |
| 3      | $8,700                 | $7,100            | 480             | 520          | $8,700         | $9,100          | 24.9%                  | 20.3%             |
| 4      | $11,667                | $8,500            | 640             | 710          | $11,667        | $12,200         | 33.3%                  | 24.3%             |

> **Nota:** Las horas están calculadas sobre una base de 40 horas semanales por integrante × 5 integrantes = 200 horas/semana. Horas acumuladas a la semana 4: 800 horas planeadas.

### 1.1.2 Earned Value Analysis (EVA) — Cierre Semana 4

El Earned Value Analysis (EVA) constituye una herramienta fundamental para el control integrado de alcance, cronograma y costo en un único sistema de métricas. Como establece Heagney (2012, p. 143), "earned value analysis allows the project manager to measure project performance by comparing the amount of work planned with what was actually accomplished to determine if cost and schedule performance is what was planned."

| Indicador | Fórmula | Valor | Interpretación |
|-----------|---------|-------|----------------|
| **BAC** (Budget at Completion) | — | $35,000 | Presupuesto total aprobado del proyecto |
| **PV** (Planned Value) | — | $11,667 | Valor del trabajo que debió completarse a la fecha (33.3% del BAC) |
| **EV** (Earned Value) | — | $8,500 | Valor del trabajo efectivamente completado (24.3% del BAC) |
| **AC** (Actual Cost) | — | $12,200 | Costo real incurrido a la fecha (34.9% del BAC) |
| **CV** (Cost Variance) | EV − AC | **−$3,700** | **Desfavorable:** Se ha gastado $3,700 más de lo que se ha ganado en valor |
| **SV** (Schedule Variance) | EV − PV | **−$3,167** | **Desfavorable:** El proyecto está retrasado en $3,167 respecto al plan |
| **CPI** (Cost Performance Index) | EV ÷ AC | **0.70** | Por cada dólar gastado, solo se generan $0.70 de valor. Ineficiencia de costos del 30% |
| **SPI** (Schedule Performance Index) | EV ÷ PV | **0.73** | El proyecto avanza al 73% de la velocidad planificada |

Heagney (2012, p. 150) señala que "a CPI or SPI less than 1.0 indicates a problem that must be addressed." Ambos indicadores se encuentran por debajo de 1.0, confirmando una situación que requiere acciones correctivas inmediatas.

### 1.1.3 Proyecciones (Forecast)

| Indicador | Fórmula | Valor | Interpretación |
|-----------|---------|-------|----------------|
| **EAC** (Estimate at Completion) | BAC ÷ CPI | **$50,000** | Costo total estimado al finalizar, si se mantiene el ritmo de ineficiencia actual |
| **ETC** (Estimate to Complete) | EAC − AC | **$37,800** | Costo estimado para completar el trabajo restante |
| **VAC** (Variance at Completion) | BAC − EAC | **−$15,000** | Se proyecta exceder el presupuesto en $15,000 |
| **TCPI** (To-Complete Performance Index) | (BAC − EV) ÷ (BAC − AC) | **1.16** | Eficiencia requerida en el trabajo restante para no exceder el BAC. Requiere mejorar el CPI actual de 0.70 a 1.16 |

El TCPI de 1.16 indica que, para completar dentro del presupuesto original, el equipo debe incrementar su eficiencia en un 66% respecto al desempeño actual (de CPI 0.70 a 1.16). Heagney (2012, p. 151) advierte que valores de TCPI significativamente superiores a 1.0 pueden ser "difficult to achieve" y sugieren la necesidad de acciones correctivas o ajustes al plan.

---

## 1.2 Change Requests — Control de Cambios

De acuerdo con Heagney (2012, p. 131), "the change control process is designed to ensure that changes are properly evaluated and approved before they are implemented." A continuación se presentan las cinco solicitudes de cambio identificadas durante la revisión de la Semana 4, procesadas mediante el método de seis pasos (Heagney, 2012, pp. 132–136):

### 1.2.1 Change Log (Registro de Cambios)

| CR ID | Fecha | Solicitante | Descripción Resumida | Categoría | Estatus |
|-------|-------|-------------|----------------------|-----------|---------|
| CR-001 | 2026-06-22 | Project Manager | Ausencia de recurso clave por enfermedad (2 días) | Schedule / Resources | Aprobado |
| CR-002 | 2026-06-22 | QA Lead | 3 deliverables sin liberar de ~8 planeados | Schedule / Scope | Aprobado |
| CR-003 | 2026-06-23 | Senior Management | Adelantar entrega de software startup 1 semana | Schedule | Aprobado |
| CR-004 | 2026-06-23 | Tech Lead | Actividad crítica más larga requiere 3 días extra | Schedule | Aprobado |
| CR-005 | 2026-06-24 | Procurement | Incremento +4% costos de materiales por inflación | Budget | Aprobado |

### 1.2.2 Change Request Forms Detallados

---

#### Cambio CR-001: Ausencia de Recurso Clave por Enfermedad

**Paso 1 — Registrar en Change Log:** Registrado el 2026-06-22.

**Paso 2 — Determinar si procesar:** Procede. La ausencia afecta directamente la ejecución de actividades del Critical Path. Heagney (2012, p. 132) enfatiza que "any change that affects the triple constraint must be processed through the change control system."

**Paso 3 — Someter a aprobación:**

| Campo | Detalle |
|-------|---------|
| **CR ID** | CR-001 |
| **Fecha de registro** | 2026-06-22 |
| **Solicitante** | Project Manager (detección automática) |
| **Descripción del cambio** | La persona encargada de la actividad inicial del sprint (desarrollo del módulo de autenticación — critical path) se ausentó 2 días hábiles por enfermedad certificada. La actividad, de 5 días de duración planificada, quedó detenida durante ese período. |
| **Impacto en Scope** | Ninguno. El alcance de la actividad no se modifica. |
| **Impacto en Schedule** | +2 días en el cronograma. El retraso impacta actividades subsecuentes del critical path (integración de auth con frontend, pruebas de seguridad). |
| **Impacto en Budget** | Costo de oportunidad: $600 (2 días de recurso sin producir valor). No se incurre en costo adicional directo porque es licencia por enfermedad cubierta. |
| **Recomendación** | **Aprobar.** Implementar mitigación: (a) redistribuir tareas no críticas del recurso a otro miembro del equipo durante la ausencia; (b) asignar horas extra compensatorias (no pagadas adicionalmente) al recurso en la semana siguiente para recuperar 1 de los 2 días perdidos; (c) aceptar 1 día neto de retraso en la actividad. |
| **Aprobador** | Project Sponsor |
| **Estatus** | ✅ Aprobado |

**Paso 4 — Actualizar plan:** La actividad de autenticación se extiende +1 día neto (se recuperó 1 día con horas extra). El cronograma general se desplaza +1 día.

**Paso 5 — Distribuir plan actualizado:** Comunicado al equipo en daily standup del 2026-06-23. Plan actualizado en repositorio compartido.

**Paso 6 — Monitorear:** Se hará seguimiento diario de la actividad de autenticación durante la Semana 5 para verificar la recuperación.

---

#### Cambio CR-002: 3 Deliverables sin Liberar

**Paso 1 — Registrar en Change Log:** Registrado el 2026-06-22.

**Paso 2 — Determinar si procesar:** Procede. Representa una desviación significativa del plan (3 de ~8 entregables, 37.5% de incumplimiento).

**Paso 3 — Someter a aprobación:**

| Campo | Detalle |
|-------|---------|
| **CR ID** | CR-002 |
| **Fecha de registro** | 2026-06-22 |
| **Solicitante** | QA Lead |
| **Descripción del cambio** | De un total de ~8 deliverables planeados para liberación a la Semana 4, 3 permanecen sin liberar: (1) API de autenticación — pruebas unitarias incompletas, (2) Esquema de base de datos — migraciones pendientes de validación, (3) Mockup de frontend — revisiones de UI/UX sin cerrar. Causa raíz: acumulación de trabajo no finalizado (work-in-progress excesivo) y bloqueos entre dependencias. |
| **Impacto en Scope** | No se reduce el alcance. Los 3 entregables deben completarse. |
| **Impacto en Schedule** | +4 días estimados para completar y liberar los 3 entregables (se planifica liberación escalonada en Semana 5). |
| **Impacto en Budget** | +$1,200 estimados (horas extra para QA y desarrollo en Semana 5). |
| **Recomendación** | **Aprobar con plan de remediación:** (a) Limitar WIP a máximo 2 tareas por desarrollador (principio KISS, Heagney, 2012, p. 118); (b) implementar sesiones de pair programming/testing para desbloquear dependencias; (c) establecer daily checkpoint a las 16:00 para los 3 entregables críticos; (d) reasignar temporalmente al recurso de frontend para apoyar en testing del backend. |
| **Aprobador** | Project Manager (dentro de autoridad delegada) |
| **Estatus** | ✅ Aprobado |

**Paso 4 — Actualizar plan:** Se incorporan +4 días para los 3 entregables con fechas de liberación escalonadas: API auth (día +1), DB schema (día +2), Frontend mockup (día +4). Costo adicional: $1,200.

**Paso 5 — Distribuir plan actualizado:** Planilla de seguimiento actualizada. Notificación a stakeholders vía email.

**Paso 6 — Monitorear:** Checkpoints diarios a las 16:00. Métrica: 3/3 entregables liberados al cierre de Semana 5.

---

#### Cambio CR-003: Adelantar Entrega de Software Startup 1 Semana

**Paso 1 — Registrar en Change Log:** Registrado el 2026-06-23.

**Paso 2 — Determinar si procesar:** Procede. Es una solicitud directa de Senior Management que afecta la restricción de tiempo (schedule constraint). Heagney (2012, p. 131) advierte que "changes requested by senior management must still go through the formal change control process to assess their full impact."

**Paso 3 — Someter a aprobación:**

| Campo | Detalle |
|-------|---------|
| **CR ID** | CR-003 |
| **Fecha de registro** | 2026-06-23 |
| **Solicitante** | Senior Management |
| **Descripción del cambio** | La dirección solicita adelantar la entrega del software startup (MVP funcional con módulos core: autenticación, inventario básico, dashboard) de la Semana 10 a la Semana 9. Esto implica comprimir 1 semana el cronograma del milestone más importante del proyecto. |
| **Impacto en Scope** | Potencial reducción de funcionalidades no-críticas para el MVP. Propuesta: diferir módulo de reportes avanzados y notificaciones push a la fase post-MVP (Semana 10–11). |
| **Impacto en Schedule** | −7 días (compresión). La compresión del cronograma solo es viable mediante fast-tracking de actividades secuenciales y/o reducción controlada del alcance. |
| **Impacto en Budget** | +$2,800 (horas extra del equipo durante 2 semanas para absorber la compresión: 5 personas × 8h extra/semana × 2 semanas × $35/hora promedio). |
| **Recomendación** | **Aprobar con condiciones:** (a) Diferir módulo de reportes avanzados y notificaciones push a post-MVP (reduce scope MVP en ~15%); (b) aplicar fast-tracking en actividades de integración frontend-backend (solapar 3 días donde el plan original era secuencial); (c) autorizar presupuesto adicional de $2,800 para horas extra. Heagney (2012, p. 136) señala que "fast-tracking increases risk and should only be done after careful analysis." |
| **Aprobador** | Project Sponsor + Senior Management |
| **Estatus** | ✅ Aprobado con condiciones |

**Paso 4 — Actualizar plan:** El milestone de software startup se adelanta a Semana 9. Módulo de reportes y notificaciones se difieren a Semanas 10–11. Presupuesto se incrementa en $2,800. Fast-tracking aplicado en ruta de integración.

**Paso 5 — Distribuir plan actualizado:** Presentación ejecutiva a Senior Management. Plan detallado distribuido al equipo.

**Paso 6 — Monitorear:** Revisión semanal de progreso del MVP. Verificar que el fast-tracking no genere defectos de integración (métrica: ≤3 bugs críticos en pruebas de integración).

---

#### Cambio CR-004: Actividad Crítica Requiere 3 Días Extra

**Paso 1 — Registrar en Change Log:** Registrado el 2026-06-23.

**Paso 2 — Determinar si procesar:** Procede. El alargamiento de una actividad del critical path impacta directamente la fecha de finalización del proyecto. Heagney (2012, p. 89) define el critical path como "the longest path through the network, which determines the shortest time to complete the project."

**Paso 3 — Someter a aprobación:**

| Campo | Detalle |
|-------|---------|
| **CR ID** | CR-004 |
| **Fecha de registro** | 2026-06-23 |
| **Solicitante** | Tech Lead |
| **Descripción del cambio** | La actividad crítica de mayor duración en el proyecto — "Integración del motor ML de predicción de demanda con el módulo de inventario" (8 días planificados) — requiere 3 días adicionales (11 días total). Causa: complejidad subestimada en la normalización de datos históricos de ventas (3 formatos distintos de las 5 sucursales). |
| **Impacto en Scope** | Ninguno. La actividad debe completarse en su totalidad. |
| **Impacto en Schedule** | +3 días. Por ser actividad del critical path (CP), el retraso se transmite directamente a la fecha de finalización del proyecto. El proyecto pasa de 12 semanas a 12.6 semanas (aproximadamente). |
| **Impacto en Budget** | +$1,200 (3 días adicionales del Tech Lead y Data Engineer). Nota: parcialmente compensado si se utiliza buffer de contingencia del proyecto. |
| **Recomendación** | **Aprobar.** Acciones de mitigación: (a) asignar al Data Engineer a tiempo completo en esta actividad (estaba al 50%); (b) utilizar 1 día del buffer de contingencia del proyecto para absorber parte del retraso; (c) aplicar crashing controlado: +4 horas/día del Tech Lead durante 3 días (costo adicional $420). Resultado neto: +2 días en el CP en lugar de +3. |
| **Aprobador** | Project Sponsor |
| **Estatus** | ✅ Aprobado |

**Paso 4 — Actualizar plan:** La actividad de integración ML pasa de 8 a 11 días con crashing que recupera 1 día → 10 días efectivos. CP se alarga en +2 días netos. Se consume 1 día del buffer de contingencia. Costo adicional: $1,200 + $420 (crashing) = $1,620.

**Paso 5 — Distribuir plan actualizado:** Comunicado al Tech Lead y Data Engineer. Diagrama de red actualizado.

**Paso 6 — Monitorear:** Revisión diaria del avance en la actividad de integración ML. Si al día 5 de la actividad el progreso es < 50%, escalar a Project Sponsor.

---

#### Cambio CR-005: Incremento de Costos de Materiales por Inflación (+4%)

**Paso 1 — Registrar en Change Log:** Registrado el 2026-06-24.

**Paso 2 — Determinar si procesar:** Procede. Afecta el presupuesto del proyecto y es un cambio externo no controlable.

**Paso 3 — Someter a aprobación:**

| Campo | Detalle |
|-------|---------|
| **CR ID** | CR-005 |
| **Fecha de registro** | 2026-06-24 |
| **Solicitante** | Procurement / Adquisiciones |
| **Descripción del cambio** | Los costos de materiales (servicios cloud AWS, licencias de software, infraestructura de testing) han experimentado un incremento del 4% debido a inflación y ajuste de precios del proveedor cloud. El costo mensual de infraestructura pasa de $850 a $884. Impacto acumulado en las 8 semanas restantes: +$272. |
| **Impacto en Scope** | Ninguno. |
| **Impacto en Schedule** | Ninguno. |
| **Impacto en Budget** | +$272 en infraestructura cloud (8 semanas × $34 adicionales/semana). Adicionalmente, +$380 en materiales de testing y herramientas de desarrollo. Impacto total: +$652. |
| **Recomendación** | **Aprobar.** El incremento es externo y no controlable. Mitigación: (a) renegociar con el proveedor cloud un descuento por compromiso de uso (reserved instances) que podría reducir el impacto al 2%; (b) absorber el incremento del presupuesto de contingencia ($652 de $1,750 disponibles). Heagney (2012, p. 132) indica que "external changes beyond the project manager's control must still be documented and tracked." |
| **Aprobador** | Project Manager (dentro de autoridad delegada) |
| **Estatus** | ✅ Aprobado |

**Paso 4 — Actualizar plan:** Se actualiza el presupuesto de infraestructura mensual: $850 → $884. Se asignan $652 del presupuesto de contingencia ($1,750 → $1,098 restante). Si se logra el descuento del 2%, el impacto real será $326 y la contingencia restante será $1,424.

**Paso 5 — Distribuir plan actualizado:** Notificación a Procurement y Finance. Actualización del budget tracker.

**Paso 6 — Monitorear:** Revisión mensual de costos cloud. Verificar en 30 días si se obtuvo el descuento por reserved instances.

---

### 1.2.3 Resumen de Impacto de Cambios en el Plan

| Cambio | Schedule | Budget | Scope | Contingencia Consumida |
|--------|----------|--------|-------|------------------------|
| CR-001 (Ausencia) | +1 día | $0 ($600 costo de oportunidad absorbido) | Sin cambio | $0 |
| CR-002 (Deliverables pendientes) | +4 días | +$1,200 | Sin cambio | $1,200 |
| CR-003 (Adelantar startup) | −7 días (a Semana 9) | +$2,800 | −1 módulo (reportes, notificaciones → post-MVP) | $2,800 |
| CR-004 (Actividad CP +3 días) | +2 días netos | +$1,620 | Sin cambio | $1,620 |
| CR-005 (Inflación +4%) | Sin cambio | +$652 | Sin cambio | $652 |
| **Impacto Neto Acumulado** | **0 días neto** (compensado: +7 −7) | **+$6,272** | **Reducción controlada** (1 módulo diferido) | **$6,272** |

---

## 1.3 Project Plan Updated — Plan de Proyecto Actualizado

### 1.3.1 Línea Base vs. Plan Actualizado

| Elemento del Plan | Línea Base Original | Plan Actualizado (post-cambios) | Delta |
|-------------------|---------------------|----------------------------------|-------|
| Duración total | 12 semanas | 12 semanas | 0 semanas (compensado) |
| Fecha de finalización | 2026-08-17 | 2026-08-17 | Sin cambio neto |
| Budget at Completion (BAC) | $35,000 | $35,000 | $0 (los incrementos se absorben vía contingencia y reservas) |
| Presupuesto de contingencia | $1,750 | $0 (consumido) | −$1,750 |
| Costo total estimado (EAC proyectado) | $35,000 | $41,272 (BAC + sobrecostos + cambios) | +$6,272 |
| Milestone: Software Startup | Semana 10 | Semana 9 | −1 semana (adelantado) |
| Milestone: Reportes y Notificaciones | Semana 9 | Semana 10–11 | +2 semanas (diferido) |
| Alcance total | 100% funcionalidades | ~97% (módulo reportes diferido a post-MVP) | −1 módulo no-crítico |
| Critical Path — Slack total | 3 días | 1 día | −2 días (reducido por CR-004) |
| Fast-tracking aplicado | No | Sí (integración FE-BE) | — |
| Crashing aplicado | No | Sí (actividad ML, +4h/d × 3 días) | — |

### 1.3.2 Cronograma Actualizado (Hitos Principales)

| Hito | Fecha Original | Fecha Actualizada | Estatus |
|------|---------------|-------------------|---------|
| Kickoff y setup | Semana 1 | Semana 1 | ✅ Completado |
| Arquitectura y DB schema | Semana 2 | Semana 2–3 | ✅ Completado |
| Módulo de autenticación | Semana 3 | Semana 3–4 (+1d CR-001) | 🔄 En progreso |
| API de inventario core | Semana 4 | Semana 4–5 | 🔄 En progreso |
| Liberación 3 entregables pendientes | Semana 4 | Semana 5 (+4d CR-002) | 🔄 Planificado |
| Mockup frontend validado | Semana 4 | Semana 5 | 🔄 Planificado |
| Integración ML + Inventario | Semana 6–7 | Semana 6–8 (+2d CR-004) | 🔜 Próximo |
| Integración Frontend-Backend | Semana 7–8 | Semana 7–8 (fast-track) | 🔜 Próximo |
| **Software Startup (MVP)** | **Semana 10** | **Semana 9** (−7d CR-003) | 🔜 Próximo |
| Módulo reportes y notificaciones | Semana 9 | Semana 10–11 (diferido) | 🔜 Próximo |
| Pruebas integrales y UAT | Semana 11 | Semana 11 | 🔜 Próximo |
| Deployment y cierre | Semana 12 | Semana 12 | 🔜 Próximo |

### 1.3.3 Presupuesto Actualizado

| Rubro | Presupuesto Original | Ajustes | Presupuesto Actualizado |
|-------|---------------------|---------|------------------------|
| Desarrollo (horas equipo) | $24,000 | +$5,620 (CR-002, 003, 004) | $29,620 |
| Infraestructura cloud | $4,000 | +$652 (CR-005) | $4,652 |
| Licencias y herramientas | $2,500 | $0 | $2,500 |
| Testing y QA | $2,750 | $0 | $2,750 |
| Contingencia | $1,750 | −$1,750 (absorbido por cambios) | $0 |
| **Total** | **$35,000** | **+$4,522 neto** | **$39,522** |

> **Nota:** El presupuesto de contingencia de $1,750 fue consumido en su totalidad para absorber los impactos de los cambios CR-002, CR-003, CR-004 y CR-005. El sobrecosto neto de $4,522 deberá ser cubierto mediante reservas de gestión (management reserves) o aprobación de presupuesto adicional. El EAC proyectado de $41,272 refleja el estimado realista incluyendo el CPI actual.

---

# SECCIÓN 2: DOCUMENTATION OF PROGRESS

## 2.1 Justificación de Técnicas Analíticas Utilizadas

El monitoreo y control efectivo de un proyecto de TI requiere la aplicación de técnicas cuantitativas que permitan evaluar objetivamente el desempeño y anticipar desviaciones. A continuación se justifica la selección de las tres técnicas empleadas en el proyecto SGII, con fundamento en Heagney (2012).

### 2.1.1 Earned Value Analysis (EVA)

El Earned Value Analysis integra las tres restricciones del triángulo de la gestión de proyectos —alcance, cronograma y costo— en un sistema unificado de medición. Heagney (2012, p. 143) lo define como "a method of measuring project performance by comparing the amount of work planned with what was actually accomplished."

**Justificación para el proyecto SGII:**

- **Integración de métricas:** SGII involucra múltiples flujos de trabajo paralelos (backend, frontend, ML, infraestructura). El EVA permite consolidar el desempeño de todos los flujos en indicadores normalizados (CPI, SPI), facilitando una visión holística del proyecto (Heagney, 2012, p. 145).

- **Detección temprana de desviaciones:** La fórmula SV = EV − PV reveló un retraso de $3,167 en la Semana 4, mientras que CV = EV − AC evidenció un sobrecosto de $3,700. Heagney (2012, p. 149) enfatiza que "variances indicate trends early enough to take corrective action."

- **Capacidad predictiva:** El EAC y TCPI calculados permiten proyectar el costo final ($50,000 si se mantiene el CPI actual) y determinar el nivel de eficiencia requerido para cumplir el presupuesto (TCPI = 1.16). Heagney (2012, p. 150) señala que "the real value of earned value is its ability to forecast the final cost and schedule."

- **Comunicación con stakeholders:** Los indicadores EVA (CPI, SPI) son comprensibles para stakeholders no técnicos, facilitando la comunicación del estado del proyecto en términos de eficiencia (Heagney, 2012, p. 152).

### 2.1.2 Critical Path Method (CPM)

El Critical Path Method identifica la secuencia más larga de actividades dependientes que determina la duración mínima del proyecto. Heagney (2012, p. 87) establece que "the critical path is the longest path through the network and determines the shortest possible project duration."

**Justificación para el proyecto SGII:**

- **Identificación de actividades sin holgura:** En SGII, la actividad de integración del motor ML con el módulo de inventario (8 días originales) es parte del critical path. El CPM permitió identificar que cualquier retraso en esta actividad (CR-004: +3 días) se transmite directamente a la fecha de finalización. Heagney (2012, p. 89) advierte que "any delay in a critical path activity delays the entire project."

- **Evaluación de impacto de cambios:** Cuando Senior Management solicitó adelantar el software startup (CR-003), el CPM fue esencial para determinar que la compresión de 7 días requería fast-tracking y reducción de alcance. Sin CPM, esta decisión habría sido especulativa (Heagney, 2012, p. 92).

- **Gestión de buffers:** El CPM reveló que tras los cambios, el slack total del proyecto se redujo de 3 días a 1 día, indicando una disminución crítica de la holgura disponible y un mayor riesgo de retraso (Heagney, 2012, p. 95).

- **Optimización de recursos:** El CPM permitió determinar qué actividades podían recibir fast-tracking (solapamiento de actividades secuenciales) y cuáles requerían crashing (asignación de recursos adicionales), decisiones que Heagney (2012, pp. 92–94) describe como fundamentales para la compresión del cronograma.

### 2.1.3 Variance Analysis (Análisis de Varianzas)

El análisis de varianzas compara sistemáticamente el desempeño real contra la línea base planificada, identificando desviaciones y sus causas raíz. Heagney (2012, p. 117) define el control como "the process of comparing actual performance to the plan and taking corrective action when necessary."

**Justificación para el proyecto SGII:**

- **Descomposición de desviaciones:** El análisis de varianza permitió desglosar la brecha de −$3,167 (SV) en sus componentes: retrasos por enfermedad (−$600), entregables no liberados (−$1,800), y subestimación de complejidad técnica (−$767). Heagney (2012, p. 119) recomienda "analyzing the root cause of variances, not just their magnitude."

- **Umbrales de acción:** Se establecieron umbrales de varianza aceptable (CV ≥ −5%, SV ≥ −5%). Al superar ambos (−31% y −27%, respectivamente), se activaron las acciones correctivas documentadas en los CR. Heagney (2012, p. 121) señala que "variances exceeding the threshold must trigger corrective action."

- **Principio KISS:** El análisis de varianza se implementó siguiendo el principio "Keep It Simple, Stupid" recomendado por Heagney (2012, p. 118): métricas claras (CV, SV), umbrales definidos, reportes concisos, y acciones correctivas específicas.

- **Retroalimentación continua:** Las varianzas se revisan semanalmente en las reuniones de control, permitiendo ajustes iterativos al plan. Heagney (2012, p. 122) destaca que "control must be timely to be effective — variances identified too late cannot be corrected."

---

## 2.2 Outputs del Proceso de Monitoreo y Control

### 2.2.1 Informes de Desempeño (Performance Reports)

| Output | Descripción | Frecuencia | Audiencia | Contenido Clave |
|--------|-------------|------------|-----------|-----------------|
| **Weekly Status Report** | Reporte semanal de avance con métricas EVA | Semanal (viernes) | Project Team, PM | EV, PV, AC, CV, SV, CPI, SPI, % completado, riesgos activos |
| **Milestone Review Report** | Reporte de cumplimiento de hitos | Al cierre de cada milestone | PM, Sponsor, Stakeholders | Cumplimiento de entregables, desviaciones, lecciones aprendidas |
| **Earned Value Dashboard** | Tablero visual de indicadores EVA | Actualización semanal, consulta on-demand | Todo el equipo | Gráficas de tendencia CPI/SPI, curva S (PV, EV, AC), proyecciones EAC |
| **Variance Analysis Report** | Análisis detallado de varianzas que exceden umbrales | Cuando una varianza excede ±5% | PM, Tech Lead | Causa raíz, impacto en CP, acciones correctivas propuestas |

### 2.2.2 Solicitudes de Cambio Aprobadas

| Output | Descripción |
|--------|-------------|
| **Change Log** | Registro maestro de las 5 solicitudes de cambio (CR-001 a CR-005), con trazabilidad completa: fecha, solicitante, descripción, impacto, recomendación, aprobador, estatus. |
| **Change Request Forms** | Formularios detallados para cada CR, procesados mediante el método de 6 pasos de Heagney (2012, pp. 132–136): registrar, evaluar, aprobar, actualizar, distribuir, monitorear. |
| **Register of Approved Changes** | Registro consolidado de cambios aprobados con su impacto acumulado en el plan del proyecto: +0 días netos en cronograma, +$6,272 en costo, reducción controlada de alcance. |

### 2.2.3 Actualizaciones al Plan del Proyecto

| Output | Descripción |
|--------|-------------|
| **Project Schedule v2.0** | Cronograma actualizado con fechas ajustadas de todos los hitos, fast-tracking documentado, crashing aplicado, buffers actualizados. |
| **Budget Baseline v2.0** | Presupuesto actualizado: contingencia consumida ($1,750 → $0), costos adicionales documentados ($6,272), EAC proyectado ($41,272). |
| **Scope Statement v2.0** | Declaración de alcance actualizada reflejando la decisión de diferir el módulo de reportes y notificaciones a post-MVP. |
| **Risk Register Updated** | Registro de riesgos actualizado: nuevo riesgo "Fast-tracking puede generar defectos de integración" (probabilidad: media, impacto: alto), riesgo "CPI < 1.0 puede disparar EAC > $45K" (probabilidad: alta). |
| **Network Diagram v2.0** | Diagrama de red actualizado reflejando el nuevo critical path con +2 días, ruta de fast-tracking FE-BE, y slack reducido (3d → 1d). |

### 2.2.4 Lecciones Aprendidas Preliminares

| # | Lección Aprendida | Categoría | Impacto | Recomendación para Futuros Proyectos |
|---|-------------------|-----------|---------|--------------------------------------|
| 1 | La subestimación de la complejidad en la normalización de datos (3 formatos distintos de sucursales) causó un retraso de 3 días en el CP | Estimación | Alto | Incluir en la fase de discovery un análisis detallado de formatos de datos legacy antes de estimar actividades de integración |
| 2 | La acumulación de WIP (work-in-progress) —3 entregables sin liberar simultáneamente— indica que no se aplicó el principio KISS de Heagney (2012, p. 118) | Proceso | Medio | Establecer límite de WIP = 2 tareas por desarrollador desde el inicio del proyecto |
| 3 | La ausencia de 2 días de un recurso del CP generó un retraso en cascada, evidenciando que no existía un plan de respaldo para actividades críticas | Recursos | Alto | Identificar actividades del CP y designar un backup con conocimiento del contexto para cada una |
| 4 | La solicitud de adelantar el MVP (CR-003) fue viable gracias a que se había identificado el módulo de reportes como funcionalidad no-crítica para el startup | Scope Management | Medio | Definir explícitamente prioridades MoSCoW (Must, Should, Could, Won't) desde la planificación inicial |
| 5 | El presupuesto de contingencia ($1,750, 5% del BAC) resultó insuficiente para absorber todos los cambios — se requirió recurrir a reservas de gestión | Presupuesto | Alto | Establecer contingencia mínima del 10% del BAC para proyectos con componentes de ML e integración de datos, por su inherente incertidumbre técnica |
| 6 | El fast-tracking aplicado (CR-003) incrementó el riesgo de defectos de integración — se debió establecer un plan de mitigación proactivo en lugar de reactivo | Riesgo | Medio | Todo fast-tracking debe ir acompañado de un mini risk assessment documentado antes de su implementación |

---

# SECCIÓN 3: ANÁLISIS DEL ESCENARIO

## 3.1 Análisis de los Cinco Eventos del Escenario

A continuación se analiza cada uno de los cinco eventos detectados durante la revisión de la Semana 4, su impacto en el triángulo PCTS (Performance, Cost, Time, Scope), y las acciones correctivas implementadas.

---

### Evento 1: Ausencia de Recurso Clave por Enfermedad (2 Días)

**Descripción del evento:** La persona encargada de la actividad inicial del sprint (desarrollo del módulo de autenticación, actividad del Critical Path) se ausentó 2 días hábiles por enfermedad. La actividad quedó completamente detenida durante ese lapso.

**Impacto en el triángulo PCTS:**

| Dimensión | Impacto | Detalle |
|-----------|---------|---------|
| **Time** | 🔴 Alto | +2 días en una actividad del CP. Cada día de retraso en el CP se transmite directamente a la fecha de finalización (Heagney, 2012, p. 89). |
| **Cost** | 🟡 Medio | $600 en costo de oportunidad (recurso pagado sin producir valor). Sin costo incremental directo por ser licencia cubierta. |
| **Scope** | 🟢 Bajo | Sin impacto directo en alcance. La actividad debe completarse en su totalidad. |
| **Performance** | 🟡 Medio | Degradación temporal del desempeño del equipo por redistribución de carga de trabajo. |

**Acciones correctivas implementadas:**

1. Redistribución inmediata de tareas no-críticas del recurso ausente a otro miembro del equipo.
2. Asignación de horas extra compensatorias (no pagadas adicionalmente) en la semana siguiente para recuperar 1 de los 2 días perdidos.
3. Aceptación de 1 día neto de retraso, documentado como cambio aprobado CR-001.

**Resultado esperado:** Recuperación de 1 día. Impacto neto: +1 día en el cronograma. Lección: se requiere un plan de respaldo (backup) para todas las actividades del CP.

---

### Evento 2: Tres Deliverables sin Liberar

**Descripción del evento:** De aproximadamente 8 entregables planeados para liberación a la Semana 4, 3 permanecen sin liberar: API de autenticación (pruebas unitarias incompletas), esquema de base de datos (migraciones sin validar), y mockup de frontend (revisiones UI/UX sin cerrar). Esto representa un 37.5% de incumplimiento en entregables.

**Impacto en el triángulo PCTS:**

| Dimensión | Impacto | Detalle |
|-----------|---------|---------|
| **Time** | 🔴 Alto | +4 días estimados para completar y liberar los 3 entregables de forma escalonada. |
| **Cost** | 🔴 Alto | +$1,200 estimados en horas extra para QA y desarrollo durante la Semana 5. |
| **Scope** | 🟢 Bajo | El alcance no se reduce; los 3 entregables son necesarios para el MVP. |
| **Performance** | 🔴 Alto | La acumulación de WIP excesivo indica una falla en el sistema de control. Heagney (2012, p. 118) señala que "simplicity is the key to effective control" (principio KISS). |

**Acciones correctivas implementadas:**

1. Limitar el WIP a máximo 2 tareas activas por desarrollador, aplicando el principio KISS de Heagney (2012, p. 118).
2. Implementar sesiones de pair programming/testing para desbloquear dependencias cruzadas entre backend y frontend.
3. Establecer daily checkpoint a las 16:00 horas específicamente para los 3 entregables críticos.
4. Reasignar temporalmente al desarrollador frontend para apoyar en testing del backend (la validación UI/UX puede esperar 1 día adicional).

**Resultado esperado:** Los 3 entregables se liberan de forma escalonada durante la Semana 5 (API auth: día +1; DB schema: día +2; Frontend mockup: día +4). Se absorbe el costo vía presupuesto de contingencia ($1,200 de $1,750 disponibles).

---

### Evento 3: Management Solicita Adelantar Software Startup 1 Semana

**Descripción del evento:** Senior Management solicita adelantar la entrega del software startup funcional (MVP con módulos core: autenticación, inventario básico, dashboard) de la Semana 10 a la Semana 9. Esto implica comprimir 1 semana el cronograma del milestone más relevante del proyecto.

**Impacto en el triángulo PCTS:**

| Dimensión | Impacto | Detalle |
|-----------|---------|---------|
| **Time** | 🔴 Alto | Compresión de −7 días. Solo viable mediante fast-tracking o reducción de scope. Heagney (2012, p. 92) advierte que "fast-tracking increases risk." |
| **Cost** | 🔴 Alto | +$2,800 en horas extra para absorber la compresión (5 personas × 8h/semana × 2 semanas × $35/h). |
| **Scope** | 🟡 Medio | Reducción controlada: se difiere el módulo de reportes avanzados y notificaciones push a post-MVP (Semanas 10–11). Reducción de ~15% del alcance del MVP. |
| **Performance** | 🟡 Medio | Riesgo de fatiga del equipo por horas extra sostenidas durante 2 semanas. Riesgo de defectos por fast-tracking en integración. |

**Acciones correctivas implementadas:**

1. Diferir el módulo de reportes avanzados y notificaciones push a la fase post-MVP (Semana 10–11), reduciendo el alcance del startup en ~15%.
2. Aplicar fast-tracking en las actividades de integración frontend-backend: solapar 3 días de integración donde el plan original era completamente secuencial.
3. Autorizar presupuesto adicional de $2,800 para horas extra del equipo durante 2 semanas.
4. Establecer métrica de control de calidad: máximo 3 bugs críticos en pruebas de integración como resultado del fast-tracking.

**Resultado esperado:** Software startup liberado en Semana 9 con funcionalidades core (auth, inventario básico, dashboard). Reportes y notificaciones en Semana 10–11. Riesgo controlado de defectos de integración.

---

### Evento 4: Actividad Crítica Más Larga Requiere 3 Días Extra

**Descripción del evento:** La actividad de mayor duración en el Critical Path —"Integración del motor ML de predicción de demanda con el módulo de inventario"— requiere 3 días adicionales (de 8 a 11 días planificados). Causa raíz: complejidad subestimada en la normalización de datos históricos de ventas provenientes de 5 sucursales con 3 formatos de datos distintos.

**Impacto en el triángulo PCTS:**

| Dimensión | Impacto | Detalle |
|-----------|---------|---------|
| **Time** | 🔴🔴 Crítico | +3 días en el CP. Por definición, cualquier retraso en el CP se transmite íntegramente a la fecha de finalización (Heagney, 2012, p. 89). De no mitigarse, el proyecto pasaría de 12 a 12.6 semanas. |
| **Cost** | 🔴 Alto | +$1,620 ($1,200 por extensión directa + $420 por crashing: 4h/día extra × 3 días del Tech Lead). |
| **Scope** | 🟢 Bajo | Sin impacto. La actividad es esencial para el MVP y no puede reducirse. |
| **Performance** | 🟡 Medio | El crashing incrementa la carga del Tech Lead, con riesgo de fatiga y error. |

**Acciones correctivas implementadas:**

1. Reasignar al Data Engineer a tiempo completo en esta actividad (previamente estaba al 50%), duplicando la capacidad de procesamiento de datos.
2. Aplicar crashing controlado: +4 horas diarias del Tech Lead durante 3 días, recuperando 1 día del retraso.
3. Consumir 1 día del buffer de contingencia del proyecto (3 días disponibles → 2 días restantes).

**Resultado esperado:** Duración efectiva de la actividad: 10 días (en lugar de 11). Impacto neto en el CP: +2 días. El buffer de contingencia del proyecto se reduce de 3 a 2 días. Esta reducción del slack es crítica porque, combinada con CR-003, deja al proyecto con solo 1 día de holgura total.

---

### Evento 5: Incremento de Costos de Materiales por Inflación (+4%)

**Descripción del evento:** Los costos de materiales —principalmente servicios cloud (AWS) e infraestructura de testing— experimentan un incremento del 4% debido a inflación y ajuste de precios del proveedor. El costo mensual de infraestructura cloud pasa de $850 a $884.

**Impacto en el triángulo PCTS:**

| Dimensión | Impacto | Detalle |
|-----------|---------|---------|
| **Time** | 🟢 Nulo | Sin impacto en el cronograma. |
| **Cost** | 🟡 Medio | +$652 totales: $272 en infraestructura cloud (8 semanas restantes × $34/semana) + $380 en materiales de testing y herramientas. |
| **Scope** | 🟢 Nulo | Sin impacto en el alcance. |
| **Performance** | 🟢 Nulo | Sin impacto en el desempeño técnico. |

**Acciones correctivas implementadas:**

1. Absorber el incremento del presupuesto de contingencia: $652 de los $550 restantes después de CR-002 (contingencia disponible: $550 → $0 tras este cambio; se requiere acceder a reservas de gestión para el faltante de $102).
2. Negociar con el proveedor cloud un descuento por compromiso de uso (reserved instances) que podría reducir el impacto inflacionario del 4% al 2% (ahorro potencial: $136).
3. Actualizar el budget tracker con la nueva línea base de costos de infraestructura: $884/mes.

**Resultado esperado:** Si la negociación con el proveedor cloud es exitosa, el impacto neto se reduce de $652 a $326, preservando $326 en contingencia. De lo contrario, se consumen los $102 restantes de contingencia y se requiere aprobación de reservas de gestión por $102. Heagney (2012, p. 132) enfatiza que los cambios externos deben documentarse aunque estén fuera del control del PM.

---

## 3.2 Análisis Consolidado del Escenario

### 3.2.1 Balance Neto del Triángulo PCTS

| Dimensión | Estado Original (Semana 4) | Después de 5 Cambios | Tendencia |
|-----------|---------------------------|---------------------|-----------|
| **Performance (CPI)** | 0.70 | Proyectado a mejorar a ~0.85 con acciones correctivas | ⚠️ Mejorando pero aún < 1.0 |
| **Cost (vs. BAC)** | +$3,700 (CV) | +$6,272 (cambios acumulados) | 🔴 Desfavorable |
| **Time (vs. Baseline)** | −$3,167 (SV) | 0 días netos (compensado) | 🟢 Neutro (compensado) |
| **Scope** | 100% planeado | ~97% (1 módulo diferido) | 🟡 Ligeramente reducido |

### 3.2.2 Interacciones entre Cambios

Los cinco cambios no ocurrieron de forma aislada; sus efectos se combinaron de las siguientes maneras:

1. **CR-001 + CR-002 (Efecto compuesto en Schedule):** La ausencia del recurso (CR-001, +1 día) y los entregables sin liberar (CR-002, +4 días) suman +5 días de retraso. Sin embargo, CR-003 (−7 días por fast-tracking y reducción de scope) compensa parcialmente este retraso, resultando en un cronograma neto cercano al original.

2. **CR-003 + CR-004 (Conflicto de intereses):** CR-003 exige adelantar 7 días el startup, mientras CR-004 añade 2 días netos al CP. Esto genera una presión contradictoria sobre el cronograma que solo pudo resolverse mediante una combinación de fast-tracking (CR-003), crashing (CR-004), y reducción de scope (CR-003).

3. **CR-002 + CR-004 + CR-005 (Presión acumulada en presupuesto):** Los costos adicionales de CR-002 ($1,200), CR-004 ($1,620), y CR-005 ($652) suman $3,472, que junto con CR-003 ($2,800) totalizan $6,272. La contingencia de $1,750 fue insuficiente, requiriendo acceso a reservas de gestión por $4,522.

### 3.2.3 Lecciones Estratégicas del Escenario

1. **Subestimación sistemática:** Los eventos 1, 2 y 4 comparten una causa raíz común: subestimación de complejidad y falta de buffers adecuados. Heagney (2012, p. 55) recomienda "padding estimates appropriately, especially for activities with high uncertainty."

2. **Principio de control oportuno:** Los 5 eventos se detectaron gracias a la revisión de la Semana 4. Si el sistema de control hubiera sido menos frecuente (por ejemplo, quincenal), los retrasos se habrían acumulado sin posibilidad de corrección. Heagney (2012, p. 122) enfatiza que "control must be timely."

3. **Triple constraint como sistema:** El escenario demuestra que las tres restricciones (scope, schedule, budget) no operan de forma independiente. La decisión de reducir scope (CR-003) permitió absorber presiones de schedule (CR-001, CR-002) y budget (CR-005), validando el modelo del triángulo de restricciones de Heagney (2012, p. 17).

4. **Insuficiencia de la contingencia:** Una contingencia del 5% ($1,750 sobre $35,000) resultó insuficiente para un proyecto con componentes de ML e integración de datos. Proyectos futuros de complejidad similar deberían considerar contingencia ≥ 10%.

---

## Referencias

Heagney, J. (2012). *Fundamentals of Project Management* (4th ed.). AMACOM.

- Capítulo 9: Control and Evaluation (pp. 115–128) — Sistema de control, principio KISS, status reviews, process reviews.
- Capítulo 10: Change Control (pp. 129–140) — Proceso de 6 pasos, triple constraint triangle, fuentes de cambio, change log.
- Capítulo 11: Earned Value Analysis (pp. 141–158) — EV, PV, AC, CV, SV, CPI, SPI, BCWS, BCWP, ACWP, EAC, TCPI.

---

*Documento generado el 29 de junio de 2026. Versión 2.0. Aprobado por Project Manager.*
