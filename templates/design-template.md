# System Design Template

## 1. Context
- Sistema/Servicio:
- Autor:
- Fecha:
- Estado: Draft | Review | Approved
- Stakeholders:

## 2. Problem and Goals
### Problema
Describe la necesidad de negocio y técnica.

### Objetivos
- Objetivo 1
- Objetivo 2

### Non-goals
- No resolver X en esta iteración.

## 3. Requirements
### Funcionales
- RF1:
- RF2:

### No funcionales
- Disponibilidad objetivo (ej. 99.95%)
- Latencia objetivo (ej. p95 < 200ms)
- RPO/RTO
- Cumplimiento y seguridad

## 4. Constraints and Assumptions
- Restricción técnica:
- Restricción organizacional:
- Supuesto crítico:

## 5. Proposed Architecture
- Diagrama: ruta al archivo en `docs/architecture/diagrams/`
- Componentes:
- Flujo de datos:
- Estrategia de despliegue:

## 6. Capacity and Scaling
- Tráfico esperado (RPS)
- Tamaño de datos
- Proyección 6-12 meses
- Estrategia de escalado

## 7. Reliability and Failure Modes
- Dependencias críticas
- Puntos de fallo
- Estrategias de resiliencia (retry, circuit breaker, fallback)
- Observabilidad mínima requerida

## 8. Security and Compliance
- Autenticación/autorización
- Gestión de secretos
- Cifrado en tránsito/en reposo
- Riesgos de seguridad relevantes

## 9. Alternatives Considered
- Alternativa A: pros/contras
- Alternativa B: pros/contras

## 10. Tradeoffs
- Disponibilidad vs consistencia
- Coste vs rendimiento
- Simplicidad vs flexibilidad

## 11. Rollout Plan
- Fase 1:
- Fase 2:
- Fase 3:

## 12. Risks and Mitigations
- Riesgo 1 + mitigación
- Riesgo 2 + mitigación

## 13. Success Metrics
- KPI 1:
- KPI 2:

## 14. Open Questions
- Pregunta pendiente 1

---

## Ejemplo real (resumen)

### Context
- Sistema/Servicio: Notification Pipeline
- Autor: A. Engineer
- Fecha: 2026-03-02
- Estado: Draft

### Problem and Goals
Plataforma actual pierde eventos bajo picos de 20k msg/min y no garantiza trazabilidad por usuario.

### Requirements (no funcional)
- Disponibilidad mensual >= 99.9%
- p95 end-to-end < 3s
- Durabilidad de eventos >= 24h en cola

### Proposed Architecture
- API Gateway -> Ingestion Service -> Kafka -> Consumer Workers -> Provider adapters
- DLQ para mensajes inválidos o reintentos agotados
- Idempotency key por `event_id`

### Capacity and Scaling
- Pico esperado: 5k RPS ingress
- Particiones Kafka iniciales: 48, escalables a 96
- Consumers autoscaling por lag (`consumer_lag > threshold`)

### Failure Modes
- Falla de provider externo: fallback a reintento exponencial + circuit breaker.
- Saturación de consumers: escala horizontal por lag y priorización por cola crítica.

### Tradeoffs
- Kafka sobre SQS para ordenar por clave y throughput alto, aceptando mayor complejidad operativa.

### Success Metrics
- Message success rate >= 99.5%
- DLQ rate < 0.5%
- Mean delivery latency p95 < 2.5s
