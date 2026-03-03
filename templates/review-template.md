# Technical Review Template

## Review Metadata
- Documento revisado:
- Revisor:
- Fecha:
- Tipo: Architecture | Incident | Runbook | ADR

## 1. Scope and Intent
- ¿Qué decisión o artefacto se está evaluando?
- ¿Qué está fuera de alcance?

## 2. Strengths
- Fortaleza 1
- Fortaleza 2

## 3. Findings (ordered by severity)
| Severity | Finding | Evidence | Recommendation |
|---|---|---|---|
| High |  |  |  |

## 4. Risk Assessment
- Riesgo técnico principal:
- Riesgo operativo principal:
- Riesgo de negocio principal:

## 5. Decision
- [ ] Approved
- [ ] Approved with conditions
- [ ] Needs revision

## 6. Conditions / Required Changes
- Cambio requerido 1
- Cambio requerido 2

## 7. Follow-up Plan
- Due date de cambios:
- Re-review date:

---

## Ejemplo real

### Review Metadata
- Documento revisado: `notification-pipeline-v1.md`
- Revisor: Principal Engineer (simulado)
- Fecha: 2026-03-02
- Tipo: Architecture

### Findings
| Severity | Finding | Evidence | Recommendation |
|---|---|---|---|
| High | No hay estrategia clara para idempotencia en reintentos | Se menciona retry exponencial sin control de duplicados | Definir `idempotency_key` por evento y TTL en storage de dedupe |
| Medium | Capacity plan no considera campañas estacionales | Solo incluye promedio mensual | Modelar picos x3 y validar límites de particiones |
| Medium | Falta plan de rollback de esquema de eventos | Rollout describe solo forward migration | Definir versionado de schema + compatibility contract |

### Decision
- [x] Approved with conditions

### Conditions / Required Changes
- Agregar sección formal de failure injection y límites de backpressure.
- Adjuntar dashboard mínimo de operación para primer release.
