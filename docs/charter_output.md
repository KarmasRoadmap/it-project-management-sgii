# Project Charter

## Sistema de Gestión de Inventarios Inteligente (SGII) para Cadena de Retail Regional

---

**Materia:** Gestión de Proyectos de TI  
**Profesor:** Ing. Luis Humberto Cruz Aguilar  
**Grupo:** 8A / 8B / 8C — Ingeniería en Sistemas, 8.º Semestre  
**Fecha de elaboración:** 29 de junio de 2026  
**Referencia normativa:** PMBOK® Guide (7.ª edición) / Heagney, *Fundamentals of Project Management* (4.ª ed.)

---

## 1. Sección de Identificación (Identification Section)

| Campo | Valor |
|---|---|
| **Nombre del proyecto** | Sistema de Gestión de Inventarios Inteligente (SGII) para Cadena de Retail Regional |
| **ID del proyecto** | SGII-RETAIL-2026-001 |
| **Fecha de aprobación del Charter** | 7 de julio de 2026 |
| **Patrocinador (Sponsor)** | Lic. María Fernanda Gutiérrez — Directora de Operaciones, Comercializadora Regional del Norte S.A. de C.V. |
| **Project Manager** | Ing. Carlos Alberto Ramírez López, PMP |
| **Cliente principal** | Gerencia de Logística y Cadena de Suministro — Comercializadora Regional del Norte S.A. de C.V. |
| **Versión del documento** | 1.0 |

---

## 2. Descripción General del Proyecto (Overview of the Project)

El proyecto SGII consiste en el diseño, desarrollo e implantación de una aplicación web empresarial orientada a la gestión inteligente de inventarios para una cadena de retail regional que opera cinco sucursales distribuidas en tres estados del norte del país. Actualmente, la organización gestiona sus inventarios de forma semimanual mediante hojas de cálculo y un sistema legado con más de diez años de antigüedad, lo que provoca quiebres de stock frecuentes, sobreinventario de productos de baja rotación, diferencias de hasta un 18 % entre el inventario físico y el registrado, y una incapacidad operativa para anticipar picos de demanda estacional.

El SGII integrará un **frontend SPA desarrollado en React con TypeScript**, que ofrecerá dashboards interactivos, gestión de productos, control de entradas y salidas, transferencias entre sucursales y reportes exportables. El **backend se construirá sobre Django 5 con Django REST Framework (DRF)**, exponiendo una API RESTful que centralizará la lógica de negocio y la capa de persistencia. Como motor de base de datos se empleará **PostgreSQL 16**, aprovechando sus capacidades de concurrencia, integridad referencial y extensiones analíticas. Todo el sistema se desplegará en contenedores **Docker** orquestados mediante **Docker Compose**, garantizando portabilidad y consistencia entre los entornos de desarrollo, pruebas y producción.

El componente diferenciador del sistema es un **módulo de inteligencia artificial para predicción de demanda**, construido con modelos de series temporales (SARIMA y Prophet) y entrenado con datos históricos de ventas de al menos 24 meses. Este módulo generará pronósticos de demanda con horizonte de 30, 60 y 90 días por producto y sucursal, permitiendo optimizar los niveles de inventario de seguridad, reducir el costo de mantenimiento y minimizar pérdidas por obsolescencia.

El sistema será **multi-sucursal desde su concepción**: cada sucursal gestionará su propio inventario local con visibilidad controlada, mientras que la oficina central dispondrá de una vista consolidada con capacidades de transferencia entre almacenes y reportes agregados. El control de acceso se implementará mediante roles y permisos granulares (Administrador, Gerente de Sucursal, Operador de Almacén, Auditor).

---

## 3. Objetivo del Proyecto (Objective)

### Objetivo SMART

**Específico:** Desarrollar e implantar un sistema web de gestión de inventarios con módulo de predicción de demanda basado en machine learning para las cinco sucursales de la Comercializadora Regional del Norte, reemplazando completamente el sistema legado actual.

**Medible:** Reducir la diferencia entre inventario físico y sistémico del 18 % actual a ≤ 3 %; reducir los eventos de quiebre de stock en un 40 % durante el primer trimestre de operación; generar pronósticos de demanda con un error absoluto medio porcentual (MAPE) ≤ 15 %.

**Alcanzable:** El proyecto cuenta con un equipo de cinco profesionales (dos desarrolladores backend, un desarrollador frontend, un científico de datos, un QA), tecnologías de código abierto maduras y ampliamente documentadas, y acceso a los datos históricos de ventas de la organización.

**Relevante:** La gestión ineficiente de inventarios representa actualmente una pérdida estimada de $120,000 USD anuales para la organización, entre mermas, sobrecostos de almacenamiento y ventas perdidas por desabasto. El SGII ataca directamente esta causa raíz.

**Temporal:** El sistema completo (incluyendo el módulo de IA) debe estar desarrollado, probado y en producción en un plazo máximo de 12 semanas calendario, contadas a partir de la aprobación formal del Project Charter.

| Variable PCTS | Meta |
|---|---|
| **Performance** | MAPE de predicción ≤ 15 %; tiempo de carga de dashboard < 2 segundos; uptime del sistema ≥ 99.5 % |
| **Cost** | Presupuesto total de $35,000 USD (desviación máxima permitida: ±5 %) |
| **Time** | 12 semanas (desviación máxima permitida: +1 semana) |
| **Scope** | Funcionalidades definidas en la sección 4. Cualquier adición requiere control de cambios formal. |

---

## 4. Alcance del Proyecto (Scope)

### 4.1 Dentro del Alcance (In-Scope)

1. **Módulo de autenticación y control de acceso:** Registro de usuarios, inicio de sesión, recuperación de contraseña, gestión de roles y permisos (Administrador, Gerente de Sucursal, Operador de Almacén, Auditor), autenticación basada en JWT con refresh tokens.

2. **Módulo de catálogo de productos:** CRUD completo de productos, incluyendo código SKU, descripción, categoría, proveedor, unidad de medida, precio de compra, precio de venta, stock mínimo y stock máximo por sucursal. Importación masiva desde archivos CSV y Excel.

3. **Módulo de gestión de inventarios multi-sucursal:**
   - Registro de entradas (compras a proveedores, devoluciones de clientes).
   - Registro de salidas (ventas, transferencias a otras sucursales, mermas).
   - Transferencias entre sucursales con trazabilidad completa.
   - Inventario cíclico programable con conciliación de diferencias.
   - Visualización de inventario en tiempo real por sucursal y producto.
   - Alertas automáticas de stock bajo y stock excedente.

4. **Módulo de predicción de demanda (IA/ML):**
   - Entrenamiento de modelos SARIMA y Prophet con datos históricos (≥ 24 meses).
   - Selección automática del mejor modelo por producto mediante validación cruzada temporal.
   - Predicciones de demanda a 30, 60 y 90 días por producto-sucursal.
   - Cálculo de inventario de seguridad óptimo basado en nivel de servicio deseado.
   - Reprogramación automática de reentrenamiento cada 7 días.

5. **Módulo de reportes y dashboards:**
   - Dashboard ejecutivo con KPIs (rotación de inventario, días de inventario, quiebres de stock, exactitud de inventario).
   - Reporte de valuación de inventario (FIFO, costo promedio ponderado).
   - Reporte de productos de baja rotación y obsolescencia.
   - Reporte de cumplimiento de pronósticos vs. demanda real.
   - Exportación a PDF y Excel de todos los reportes.

6. **Infraestructura y DevOps:**
   - Containerización completa con Docker y Docker Compose.
   - Pipeline CI/CD básico con GitHub Actions para pruebas automáticas y despliegue.
   - Scripts de migración de datos históricos desde el sistema legado.
   - Entornos separados: desarrollo, staging (QA) y producción.
   - Backup automatizado diario de la base de datos PostgreSQL.

7. **Documentación:**
   - Manual de usuario final (operadores de sucursal y gerentes).
   - Manual de administración del sistema.
   - Documentación técnica de la API (Swagger/OpenAPI).
   - Documentación de arquitectura y despliegue.

8. **Capacitación:**
   - 3 sesiones de capacitación presencial (una en oficina central, una virtual para sucursales foráneas, una para administradores).
   - Material de capacitación en video y guías rápidas.

### 4.2 Fuera del Alcance (Out-of-Scope)

- Integración con sistemas de punto de venta (POS) de terceros (se contempla como proyecto fase 2).
- Aplicación móvil nativa (iOS/Android); el sistema será responsive web, pero no se desarrollarán apps nativas.
- Módulo de contabilidad financiera o facturación electrónica.
- Integración con sistemas ERP de la organización (SAP, Oracle Netsuite).
- Automatización de pedidos a proveedores (solo se generarán recomendaciones de compra, no órdenes de compra automáticas).
- Hardware (servidores, computadoras, lectores de código de barras); el proyecto asume que la infraestructura de hardware existe.
- Migración de datos de inventario con más de 36 meses de antigüedad.
- Soporte multi-idioma (solo español en la versión 1.0).
- Entrenamiento de modelos de deep learning (LSTM, Transformers) — se limita a modelos estadísticos clásicos y Prophet.

---

## 5. Hitos Principales (Major Milestones)

| # | Hito | Fecha estimada | Semana | Criterio de aceptación |
|---|---|---|---|---|
| M1 | **Project Charter aprobado y kick-off realizado** | 7 de julio de 2026 | Semana 1 | Charter firmado por sponsor y PM; reunión de kick-off con todos los stakeholders registrada en minuta |
| M2 | **Requerimientos funcionales y no funcionales aprobados** | 14 de julio de 2026 | Semana 2 | Documento SRS (Software Requirements Specification) validado y firmado por el Gerente de Logística |
| M3 | **Prototipo de alta fidelidad validado** | 21 de julio de 2026 | Semana 3 | Prototipo en Figma revisado y aprobado por los gerentes de sucursal; sin observaciones bloqueantes |
| M4 | **Arquitectura del sistema y modelo de datos aprobados** | 25 de julio de 2026 | Semana 3 | Diagrama de arquitectura, DER (Diagrama Entidad-Relación), y diccionario de datos revisados por líder técnico |
| M5 | **MVP — Módulos core completados (inventario, catálogo, auth)** | 11 de agosto de 2026 | Semana 6 | CRUD de productos, entradas/salidas, transferencias y autenticación funcionales en staging; pruebas de integración pasando al 100 % |
| M6 | **Módulo de predicción de demanda completado** | 25 de agosto de 2026 | Semana 8 | Modelos entrenados; API de predicciones respondiendo con MAPE validado ≤ 15 % sobre datos de prueba |
| M7 | **Sistema integrado en staging — pruebas UAT iniciadas** | 5 de septiembre de 2026 | Semana 10 | Todos los módulos integrados; suite de pruebas E2E pasando; usuarios clave ejecutando pruebas de aceptación |
| M8 | **Despliegue a producción y cierre del proyecto** | 22 de septiembre de 2026 | Semana 12 | Sistema en producción en las 5 sucursales; migración de datos completada; capacitación impartida; acta de cierre firmada |

---

## 6. Entregables Principales (Major Deliverables)

| ID | Entregable | Tipo | Responsable | Fecha |
|---|---|---|---|---|
| D1 | Project Charter y Plan de Proyecto | Documento | Project Manager | Semana 1 |
| D2 | Documento de Especificación de Requerimientos (SRS) | Documento | Project Manager + Analista | Semana 2 |
| D3 | Prototipo de alta fidelidad (Figma) | Artefacto | Desarrollador Frontend | Semana 3 |
| D4 | Documento de Arquitectura del Sistema (SAD) | Documento | Desarrollador Backend Líder | Semana 3 |
| D5 | Código fuente del backend (Django + DRF) con API documentada | Software | Desarrolladores Backend | Semana 6–10 |
| D6 | Código fuente del frontend (React + TypeScript) | Software | Desarrollador Frontend | Semana 6–10 |
| D7 | Modelos de predicción entrenados y notebooks de entrenamiento | Software + Documento | Científico de Datos | Semana 8 |
| D8 | Suite de pruebas unitarias, de integración y E2E | Software | QA Engineer | Semana 10 |
| D9 | Scripts de migración de datos y backups | Software | Desarrollador Backend | Semana 11 |
| D10 | Manuales de usuario y documentación técnica | Documento | Todo el equipo | Semana 11 |
| D11 | Sistema desplegado en producción (5 sucursales) | Software | Project Manager + DevOps | Semana 12 |
| D12 | Material de capacitación y grabaciones de sesiones | Multimedia | Project Manager | Semana 12 |
| D13 | Acta de cierre del proyecto y lecciones aprendidas | Documento | Project Manager | Semana 12 |

---

## 7. Supuestos del Proyecto (Assumptions)

1. **Disponibilidad de datos históricos:** Se asume que la organización dispone de al menos 24 meses de datos de ventas en formato digital (exportable a CSV), con granularidad diaria y desglosada por producto y sucursal. La ausencia de estos datos invalidaría el módulo de predicción de demanda.

2. **Infraestructura de hardware existente:** Se asume que cada sucursal cuenta con al menos dos computadoras con acceso a internet de banda ancha (≥ 10 Mbps), y que la oficina central dispone de un servidor físico o instancia en la nube donde se desplegarán los contenedores Docker. El proyecto no incluye partida presupuestaria para adquisición de hardware.

3. **Colaboración del personal operativo:** Se asume que los gerentes de sucursal y operadores de almacén estarán disponibles para las sesiones de levantamiento de requerimientos (mínimo 4 horas por sucursal durante las semanas 1–2) y para las pruebas de aceptación de usuario durante la semana 10.

4. **Estabilidad de los requerimientos:** Se asume que los requerimientos funcionales, una vez aprobados en la semana 2, no sufrirán cambios sustanciales. Cambios menores se gestionarán mediante control de cambios; cambios mayores requerirán renegociación del alcance, costo y cronograma.

5. **Disponibilidad del equipo de proyecto:** Se asume que los cinco miembros del equipo trabajarán a tiempo completo (40 horas/semana) durante las 12 semanas del proyecto, sin ausencias prolongadas (> 3 días) no planificadas.

6. **Licencias y herramientas:** Se asume que todas las herramientas de desarrollo (IDE, control de versiones GitHub, Figma, Docker Hub) y las bibliotecas de software (Django, React, Prophet, scikit-learn) están disponibles bajo licencias de código abierto o gratuitas, sin costo adicional de licenciamiento.

7. **Entorno normativo y legal:** Se asume que el tratamiento de datos de inventario no está sujeto a regulaciones especiales de protección de datos personales, ya que no se procesarán datos de clientes finales, solo datos transaccionales agregados de productos.

---

## 8. Restricciones del Proyecto (Constraints)

| # | Restricción | Tipo | Descripción |
|---|---|---|---|
| C1 | **Tiempo** | Cronograma | El proyecto debe completarse en exactamente 12 semanas (7 de julio al 22 de septiembre de 2026). La fecha de cierre es inamovible debido al inicio del siguiente ciclo fiscal de la organización. No se autorizará extensión superior a una semana. |
| C2 | **Presupuesto** | Costo | El presupuesto máximo es de $35,000 USD. No existe reserva de contingencia adicional; cualquier sobrecosto debe absorberse mediante reducción controlada del alcance. |
| C3 | **Stack tecnológico** | Tecnología | El stack está predefinido y no es negociable: React 18+ con TypeScript en frontend; Django 5+ con Django REST Framework en backend; PostgreSQL 16 como base de datos; Docker y Docker Compose para containerización. No se permite el uso de frameworks alternativos (Vue, Angular, FastAPI, Flask, MySQL, MongoDB). |
| C4 | **Equipo** | Recursos Humanos | El equipo es fijo: 2 desarrolladores backend (Python/Django), 1 desarrollador frontend (React/TypeScript), 1 científico de datos (Python/ML), 1 QA Engineer. No se contempla contratación de personal adicional ni reemplazo de miembros durante la ejecución del proyecto. |
| C5 | **Arquitectura de despliegue** | Infraestructura | El sistema debe desplegarse on-premise en la oficina central (no en nube pública como AWS, GCP o Azure). Esto es por política de seguridad de datos de la organización. Se proporcionará un servidor con Ubuntu Server 24.04 LTS, 16 GB RAM, 4 vCPU, 500 GB SSD. |
| C6 | **Navegadores soportados** | Tecnología | El frontend debe ser compatible con las versiones más recientes de Google Chrome, Mozilla Firefox y Microsoft Edge. No se requiere compatibilidad con Safari ni Internet Explorer. |
| C7 | **Idioma** | Comunicación | Toda la documentación, la interfaz de usuario, los mensajes del sistema y el material de capacitación deben estar en español. El código fuente (nombres de variables, comentarios) puede estar en inglés. |

---

## 9. Necesidad de Negocio u Oportunidad — Beneficios (Business Need or Opportunity)

### 9.1 Situación Actual (Problemática)

La Comercializadora Regional del Norte S.A. de C.V. opera cinco sucursales que en conjunto manejan un catálogo de aproximadamente 4,200 SKUs activos, con un valor de inventario promedio de $2.8 millones de dólares. La gestión actual de inventarios presenta las siguientes deficiencias críticas:

- **Quiebres de stock frecuentes:** En el último año fiscal se registraron 847 eventos de desabasto que resultaron en ventas perdidas estimadas en $68,000 USD.
- **Sobreinventario de baja rotación:** Aproximadamente el 22 % del valor del inventario corresponde a productos con más de 180 días sin movimiento, generando un costo de mantenimiento anual de $35,000 USD.
- **Diferencia inventario físico vs. sistémico del 18 %:** Las discrepancias generan ajustes contables trimestrales que impactan negativamente los estados financieros y la confiabilidad del sistema.
- **Falta de visibilidad multi-sucursal:** No existe un mecanismo eficiente para identificar excedentes en una sucursal que puedan transferirse a otra con déficit; esto genera compras innecesarias a proveedores externos.
- **Planeación reactiva:** Las decisiones de reabastecimiento se toman con base en la intuición del gerente de sucursal, sin soporte analítico.

### 9.2 Beneficios Esperados

| Beneficio | Indicador | Meta (12 meses post-implantación) |
|---|---|---|
| Reducción de quiebres de stock | Número de eventos de desabasto por mes | Reducción ≥ 40 % |
| Mejora en exactitud de inventario | (Inventario sistémico − Inventario físico) / Inventario físico | ≤ 3 % de desviación |
| Reducción de sobreinventario | % del valor de inventario con rotación > 180 días | ≤ 10 % |
| Optimización de compras | Transferencias inter-sucursales exitosas vs. compras externas evitadas | Incremento ≥ 25 % en transferencias internas |
| Eficiencia operativa | Horas-hombre dedicadas a conteos y conciliaciones | Reducción ≥ 50 % |
| ROI estimado | (Ahorro anual − Costo del proyecto) / Costo del proyecto | ROI positivo en ≤ 8 meses |

### 9.3 Alineación Estratégica

El proyecto SGII se alinea con el objetivo estratégico 2025–2027 de la organización: *"Digitalizar los procesos core de la cadena de suministro para alcanzar eficiencia operativa clase mundial."* Asimismo, responde a la iniciativa del comité directivo de reducir costos operativos en un 12 % anual mediante tecnología.

---

## 10. Costo Preliminar del Proyecto (Preliminary Cost)

### 10.1 Desglose Presupuestario

| Partida | Descripción | Costo estimado (USD) | % del total |
|---|---|---|---|
| **Recursos Humanos** | | **$28,800** | **82.3 %** |
| Desarrollador Backend Senior (1) | 12 semanas × 40 h × $25/h | $12,000 | 34.3 % |
| Desarrollador Backend Junior (1) | 12 semanas × 40 h × $15/h | $7,200 | 20.6 % |
| Desarrollador Frontend (1) | 12 semanas × 40 h × $18/h | $8,640 | 24.7 % |
| Científico de Datos (1) | 8 semanas × 40 h × $22/h (dedicación parcial semanas 9–12) | $7,040 | 20.1 % |
| QA Engineer (1) | 6 semanas × 30 h × $16/h (dedicación intensiva semanas 6–11) | $2,880 | — |
| Project Manager (1) | Honorarios incluidos en overhead institucional | $0 | — |
| *Subtotal recursos humanos* | *Ajuste por traslape QA en partida anterior* | *$28,800* | — |
| **Infraestructura y Herramientas** | | **$1,500** | **4.3 %** |
| Registro de dominio y certificado SSL | 2 años | $300 | — |
| Repositorio privado GitHub Team | 3 meses × $55/mes | $165 | — |
| Suscripción Figma Professional | 3 meses × $15/mes | $45 | — |
| Servidor de pruebas (instancia cloud temporal semanas 8–11) | 1 mes de uso moderado | $150 | — |
| Reserva para herramientas complementarias y APIs | | $840 | — |
| **Capacitación y Despliegue** | | **$2,500** | **7.1 %** |
| Viáticos para sesiones presenciales (oficina central + 2 sucursales) | Transporte, hospedaje y alimentación (3 sesiones) | $1,200 | — |
| Impresión de manuales y material didáctico | 30 manuales a todo color | $400 | — |
| Soporte post-implantación (2 semanas) | Guardia de desarrolladores | $900 | — |
| **Reserva de Contingencia** | | **$2,200** | **6.3 %** |
| Fondo para riesgos identificados (≈ 6.3 % del presupuesto) | Ver matriz de riesgos | $2,200 | — |
| **TOTAL** | | **$35,000** | **100 %** |

### 10.2 Curva de Costo (S-Curve Proyectada)

| Semana | Costo acumulado estimado |
|---|---|
| Semana 2 | $5,200 (levantamiento de requerimientos, prototipo) |
| Semana 4 | $11,800 (desarrollo inicial, configuración) |
| Semana 6 | $18,500 (MVP, entrenamiento de modelos) |
| Semana 8 | $25,200 (módulos completos, integración) |
| Semana 10 | $30,500 (pruebas, UAT) |
| Semana 12 | $35,000 (despliegue, capacitación, cierre) |

### 10.3 Supuestos del Presupuesto

- Tarifas por hora basadas en mercado laboral mexicano para profesionales de TI de nivel intermedio-avanzado.
- No se incluyen costos de hardware porque la organización proporciona la infraestructura (ver restricción C5).
- No se incluyen licencias de software porque el stack es 100 % open source.
- Los honorarios del Project Manager son absorbidos como costo institucional (proyecto académico-universitario supervisado).

---

## 11. Riesgos del Proyecto (Project Risks)

### 11.1 Matriz de Riesgos

| ID | Riesgo | Categoría | Probabilidad (P) | Impacto (I) | Severidad (P × I) | Estrategia | Plan de Mitigación | Plan de Contingencia | Responsable |
|---|---|---|---|---|---|---|---|---|---|
| R1 | **Datos históricos de ventas incompletos o de baja calidad** (datos faltantes, formatos inconsistentes, sin granularidad por sucursal) | Datos / Técnico | Alta (0.70) | Muy Alto (0.80) | **0.56 — Crítico** | Mitigar | Auditoría de calidad de datos en semana 1; solicitar datasets de prueba antes del kick-off. Dedicar 20 h del científico de datos a limpieza y normalización. | Si > 30 % de los datos son irrecuperables, reducir alcance del módulo de predicción a Prophet únicamente (sin SARIMA) con menor horizonte de predicción (solo 30 días). | Científico de Datos + PM |
| R2 | **Retraso en firma de aprobaciones por parte del sponsor o gerentes de sucursal** | Stakeholders / Organizacional | Media (0.50) | Alto (0.60) | **0.30 — Alto** | Mitigar | Establecer SLAs de respuesta (máx. 48 h) en el Project Charter. Agendar recordatorios automáticos. Escalar a Dirección de Operaciones si hay demora > 72 h. | Comenzar actividades no dependientes de la aprobación bloqueada (preparar infraestructura, entrenamiento preliminar de modelos con datos sintéticos). | Project Manager |
| R3 | **Rotación o salida de un miembro del equipo durante la ejecución** | Recursos Humanos | Baja (0.25) | Muy Alto (0.85) | **0.21 — Alto** | Mitigar + Aceptar | Documentación cruzada obligatoria (code reviews, pair programming rotativo). Todo el conocimiento debe estar en el repositorio, no en personas. Mantener buffer de 1 semana en el cronograma (semana 12). | Si sale un backend: el otro backend absorbe tareas críticas; QA asume tareas de testing de backend. Si sale el frontend: contratar freelancer de emergencia con presupuesto de contingencia ($2,200). | Project Manager |
| R4 | **Los modelos de predicción no alcanzan el MAPE ≤ 15 % acordado** | Técnico / Calidad | Media (0.45) | Alto (0.55) | **0.25 — Alto** | Mitigar | Prueba temprana de factibilidad en semana 3 (proof of concept con datos reales). Si el MAPE sobre datos de validación supera el 20 %, explorar features adicionales (estacionalidad, promociones, días festivos regionales). | Si en semana 7 el MAPE sigue > 15 %, el módulo se entrega con el mejor modelo disponible y se documenta como limitación conocida. El sistema igualmente aporta valor con los módulos core de inventario. | Científico de Datos |
| R5 | **Resistencia al cambio por parte del personal operativo de sucursales** | Organizacional / Adopción | Media (0.55) | Medio (0.50) | **0.28 — Medio** | Mitigar | Involucrar a gerentes y operadores desde el levantamiento de requerimientos (sentido de pertenencia). Capacitación práctica con datos reales de su sucursal. Designar un "campeón del sistema" por sucursal. | Si la adopción es baja en semana 12, extender el soporte post-implantación 2 semanas adicionales (costo: $900 de la reserva de contingencia). | Project Manager + Sponsor |
| R6 | **Problemas de rendimiento en el servidor on-premise bajo carga concurrente** | Infraestructura / Técnico | Media (0.40) | Medio (0.50) | **0.20 — Medio** | Mitigar | Pruebas de carga con Locust en staging (simular 50 usuarios concurrentes). Configurar connection pooling en PostgreSQL, caching con Redis, y Gunicorn con workers pre-fork. | Si el servidor resulta insuficiente, habilitar swap y reducir workers de Gunicorn. Documentar requerimiento de hardware real para la fase 2. | Desarrollador Backend Líder |
| R7 | **Cambio en los requerimientos por parte de la Gerencia de Logística después de la semana 2** | Alcance / Stakeholders | Media (0.40) | Medio (0.45) | **0.18 — Medio** | Mitigar + Controlar | Proceso formal de control de cambios: todo cambio post-línea base debe documentarse en un RFC (Request for Change) con análisis de impacto en costo, tiempo y alcance. Solo el sponsor puede aprobar cambios que afecten la línea base. | Si el cambio es menor y no afecta la ruta crítica, se absorbe con el buffer de la semana 12. Si es mayor, se negocia reducción de otro entregable de igual magnitud (trade-off PCTS). | Project Manager + Sponsor |

### 11.2 Resumen de Severidad

| Nivel | Cantidad de riesgos |
|---|---|
| Crítico (≥ 0.40) | 1 (R1) |
| Alto (0.20–0.39) | 4 (R2, R3, R4, R5) |
| Medio (0.10–0.19) | 2 (R6, R7) |
| Bajo (< 0.10) | 0 |

---

## 12. Aceptación del Project Charter (Project Charter Acceptance)

Los abajo firmantes, en pleno uso de sus facultades y responsabilidades, manifiestan su conformidad con el contenido del presente Project Charter —incluyendo el alcance, los objetivos, el presupuesto, el cronograma de hitos, los entregables y la matriz de riesgos— y autorizan formalmente el inicio y la ejecución del proyecto **"Sistema de Gestión de Inventarios Inteligente (SGII) para Cadena de Retail Regional"** (ID: SGII-RETAIL-2026-001), a partir del 7 de julio de 2026.

La firma de este documento constituye la autorización para que el Project Manager, Ing. Carlos Alberto Ramírez López, disponga de los recursos humanos, tecnológicos y financieros aquí descritos, y ejerza la autoridad necesaria para la conducción del proyecto dentro de los límites establecidos en las variables PCTS (Performance, Cost, Time, Scope).

---

**Patrocinador del Proyecto (Sponsor)**

| | |
|---|---|
| Nombre: | Lic. María Fernanda Gutiérrez |
| Cargo: | Directora de Operaciones |
| Organización: | Comercializadora Regional del Norte S.A. de C.V. |
| Firma: | ______________________________ |
| Fecha: | ____ / ____ / 2026 |

---

**Project Manager**

| | |
|---|---|
| Nombre: | Ing. Carlos Alberto Ramírez López, PMP |
| Cargo: | Project Manager — Proyecto SGII |
| Firma: | ______________________________ |
| Fecha: | ____ / ____ / 2026 |

---

**Cliente Principal (Representante del Negocio)**

| | |
|---|---|
| Nombre: | Lic. José Antonio Mendoza Solís |
| Cargo: | Gerente de Logística y Cadena de Suministro |
| Organización: | Comercializadora Regional del Norte S.A. de C.V. |
| Firma: | ______________________________ |
| Fecha: | ____ / ____ / 2026 |

---

**Vo. Bo. Académico**

| | |
|---|---|
| Nombre: | Ing. Luis Humberto Cruz Aguilar |
| Cargo: | Profesor Titular — Gestión de Proyectos de TI |
| Institución: | [Nombre de la Universidad] — Facultad de Ingeniería en Sistemas, 8.º Semestre, Grupo 8A / 8B / 8C |
| Firma: | ______________________________ |
| Fecha: | ____ / ____ / 2026 |

---

## 13. Stakeholders del Proyecto (Project Stakeholders)

| # | Stakeholder | Rol en el proyecto | Nivel de influencia | Nivel de interés | Expectativas principales | Estrategia de gestión |
|---|---|---|---|---|---|---|
| 1 | **Lic. María Fernanda Gutiérrez** — Directora de Operaciones | Sponsor / Patrocinadora | **Alto** | **Alto** | ROI positivo en ≤ 8 meses; reducción demostrable de mermas; sistema operando sin incidentes críticos en las 5 sucursales. | Gestionar de cerca (informes semanales de avance, dashboard de KPIs, reunión quincenal de estatus). |
| 2 | **Lic. José Antonio Mendoza Solís** — Gerente de Logística y Cadena de Suministro | Cliente principal / Dueño del producto | **Alto** | **Alto** | Sistema que resuelva los problemas reales del día a día; transición sin disrupciones; funcionalidad de transferencias entre sucursales priorizada. | Gestionar de cerca (participación en sprint reviews, validación de prototipos, pruebas UAT). |
| 3 | **Gerentes de sucursal (5)** — Uno por sucursal | Usuarios clave / Validadores | **Medio** | **Alto** | Interfaz intuitiva y rápida; mínima curva de aprendizaje; que el sistema realmente reduzca su carga de trabajo manual. | Mantener informados + involucrar activamente (sesiones de requisitos, pruebas UAT, capacitación presencial). |
| 4 | **Operadores de almacén (≈15)** — Aprox. 3 por sucursal | Usuarios finales operativos | **Bajo** | **Alto** | Sistema rápido y sin errores; que no requiera doble captura; que el proceso de entrada/salida sea simple. | Mantener informados (inclusión en prueba piloto, encuestas de satisfacción post-capacitación, canal de soporte directo). |
| 5 | **Ing. Carlos Alberto Ramírez López** — Project Manager | Director del proyecto | **Alto** | **Alto** | Cumplir con las restricciones PCTS; entregar el proyecto con la calidad acordada; gestionar riesgos efectivamente. | Responsable directo de la ejecución. |
| 6 | **Equipo de desarrollo (5 personas)** — Backend (2), Frontend (1), Data Science (1), QA (1) | Ejecutores técnicos | **Medio** | **Alto** | Requerimientos claros y estables; ambiente de trabajo colaborativo; herramientas adecuadas; ausencia de interrupciones constantes. | Gestionar de cerca (daily stand-ups, retrospectivas semanales, soporte para eliminación de impedimentos). |
| 7 | **Ing. Luis Humberto Cruz Aguilar** — Profesor Titular | Supervisor académico | **Medio** | **Medio** | Que el proyecto cumpla con los estándares de PMBOK y Heagney; que la documentación sea rigurosa y completa; que los alumnos demuestren dominio de la gestión de proyectos. | Mantener informado (entregables documentales del Charter, plan de proyecto y reportes de avance académico). |
| 8 | **Departamento de TI (Infraestructura)** — 2 ingenieros de soporte | Proveedores de infraestructura | **Medio** | **Bajo** | Que el sistema se despliegue sin conflictos con otros servicios del servidor; documentación clara de requisitos de infraestructura. | Mantener informados (especificación técnica detallada, coordinación para ventana de despliegue, documentación de operaciones). |
| 9 | **Proveedores de datos históricos** — Analista de datos de la organización | Facilitadores de datos | **Bajo** | **Bajo** | Solicitudes claras y acotadas; tiempo razonable para extracción de datos; confidencialidad de la información comercial. | Mantener informados (solicitud formal de datos en semana 1 con formato y alcance especificado). |
| 10 | **Auditoría Interna** — Equipo de control interno | Cumplimiento normativo | **Bajo** | **Medio** | Trazabilidad completa de todas las transacciones de inventario; registros de auditoría inmutables; reportes que satisfagan los requerimientos del auditor externo. | Mantener informados (inclusión de requisitos de auditoría en el SRS, validación del módulo de reportes). |

### 13.1 Matriz Poder-Interés (Resumen Visual)

```
                          INTERÉS
                  Bajo              Alto
          ┌─────────────────┬─────────────────┐
          │                  │                  │
   Alto   │   —              │  1. Sponsor      │
          │                  │  2. Cliente      │
          │                  │  5. PM           │
P         │                  │                  │
O         ├─────────────────┼─────────────────┤
D         │                  │                  │
E         │  8. Infra        │  3. Gerentes     │
R  Medio  │  7. Profesor     │  6. Equipo Dev   │
          │                  │                  │
          ├─────────────────┼─────────────────┤
          │                  │                  │
          │  9. Proveedores  │  4. Operadores   │
   Bajo   │  10. Auditoría   │                  │
          │                  │                  │
          └─────────────────┴─────────────────┘
```

**Leyenda:**
- Cuadrante superior derecho (Alto poder − Alto interés): Gestionar de cerca.
- Cuadrante inferior derecho (Bajo poder − Alto interés): Mantener informados e involucrar.
- Cuadrante superior izquierdo (Alto poder − Bajo interés): Mantener satisfechos.
- Cuadrante inferior izquierdo (Bajo poder − Bajo interés): Monitorear.

---

## Anexo A: Glosario de Siglas y Acrónimos

| Sigla | Significado |
|---|---|
| CI/CD | Continuous Integration / Continuous Deployment |
| CRUD | Create, Read, Update, Delete |
| DER | Diagrama Entidad-Relación |
| DRF | Django REST Framework |
| E2E | End-to-End (pruebas punta a punta) |
| JWT | JSON Web Token |
| KPI | Key Performance Indicator (Indicador Clave de Desempeño) |
| MAPE | Mean Absolute Percentage Error |
| MVP | Minimum Viable Product (Producto Mínimo Viable) |
| PCTS | Performance, Cost, Time, Scope |
| PMBOK | Project Management Body of Knowledge |
| PMP | Project Management Professional |
| QA | Quality Assurance (Aseguramiento de Calidad) |
| ROI | Return On Investment (Retorno sobre la Inversión) |
| SARIMA | Seasonal AutoRegressive Integrated Moving Average |
| SGII | Sistema de Gestión de Inventarios Inteligente |
| SKU | Stock Keeping Unit (Unidad de Mantenimiento de Stock) |
| SLA | Service Level Agreement (Acuerdo de Nivel de Servicio) |
| SPA | Single Page Application |
| SRS | Software Requirements Specification |
| UAT | User Acceptance Testing (Pruebas de Aceptación de Usuario) |

---

## Anexo B: Referencias Bibliográficas

1. Heagney, J. (2016). *Fundamentals of Project Management* (4.ª ed.). AMACOM — American Management Association.
2. Project Management Institute. (2021). *A Guide to the Project Management Body of Knowledge (PMBOK® Guide)* (7.ª ed.). Project Management Institute.
3. Kerzner, H. (2017). *Project Management: A Systems Approach to Planning, Scheduling, and Controlling* (12.ª ed.). John Wiley & Sons.

---

**Fin del Documento — Project Charter SGII-RETAIL-2026-001, Versión 1.0**

*Documento elaborado conforme a los lineamientos de la materia Gestión de Proyectos de TI, 8.º Semestre de Ingeniería en Sistemas, bajo la supervisión del Ing. Luis Humberto Cruz Aguilar.*
