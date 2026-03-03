# Postmortem Template

## 1. Incident Summary
- Incident ID:
- Fecha:
- Duración:
- Severidad:
- Servicios impactados:
- Impacto al usuario/negocio:

## 2. Detection
- ¿Cómo se detectó?
- Tiempo hasta detección (MTTD):
- Alertas que funcionaron/fallaron:

## 3. Timeline (UTC)
- HH:MM - evento
- HH:MM - evento

## 4. Root Cause Analysis
### Causa raíz técnica

### Factores contribuyentes
- Factor 1
- Factor 2

### Por qué no se detectó antes

## 5. Mitigation and Recovery
- Acciones de mitigación aplicadas:
- Tiempo de recuperación (MTTR):
- Riesgo residual tras mitigación:

## 6. What Went Well
- Elemento positivo 1

## 7. What Went Wrong
- Brecha 1

## 8. Action Items
| ID | Acción | Dueño | Prioridad | Fecha límite | Estado |
|---|---|---|---|---|---|
| A-01 |  |  | High |  | Open |

## 9. Lessons Learned
- Lección 1

## 10. Follow-up Verification
- Fecha de verificación:
- Métricas antes/después:

---

## Ejemplo real

### Incident Summary
- Incident ID: INC-2026-03-01-API-502
- Fecha: 2026-03-01
- Duración: 47 minutos
- Severidad: SEV-2
- Servicios impactados: `checkout-api`, `payment-adapter`
- Impacto: 18% de transacciones fallidas en región us-east durante la ventana.

### Detection
- Detección por alerta `5xx_rate > 5%` sostenida por 5 min.
- MTTD: 6 min
- Alertas de saturación DB tardaron 12 min (umbral demasiado alto).

### Timeline (UTC)
- 14:02 - despliegue de nueva versión de `payment-adapter`.
- 14:07 - incremento de latencia DB y conexiones activas.
- 14:08 - comienza subida de 502 en `checkout-api`.
- 14:14 - alerta SEV-2 dispara.
- 14:19 - rollback iniciado.
- 14:49 - métricas vuelven a baseline.

### Root Cause Analysis
- Causa raíz: cambio de query sin índice adecuado en tabla de pagos, aumentando lock contention.
- Factores contribuyentes: ausencia de test de performance en CI y falta de canary por región.
- Detección tardía: alerta de DB basada en promedio de 15 min, no p95.

### Mitigation and Recovery
- Rollback de release + kill de queries bloqueantes.
- MTTR: 35 min desde reconocimiento.
- Riesgo residual: posibilidad de regresión en próximo deploy sin guardrails.

### Action Items
| ID | Acción | Dueño | Prioridad | Fecha límite | Estado |
|---|---|---|---|---|---|
| A-01 | Crear índice compuesto para query crítica | DBA | High | 2026-03-04 | Done |
| A-02 | Agregar test de carga p95 en CI | Platform | High | 2026-03-10 | Open |
| A-03 | Canary regional obligatorio en pagos | SRE | Medium | 2026-03-12 | Open |

### Lessons Learned
- `Mean latency` ocultó degradación; usar percentiles y señales de saturación.
