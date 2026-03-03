# Class Note Template

## Metadata
- Date:
- Domain: (Infrastructure | Distributed Systems | Reliability)
- Source: (curso, paper, libro, incidente)
- Time invested (h):
- Difficulty (1-5):

## Problem Statement
Describe el problema técnico real que esta clase ayuda a resolver.

## Core Concepts
- Concepto 1:
- Concepto 2:
- Concepto 3:

## Practical Scenario
Contexto de producción donde aplicarías estos conceptos.

## Experiment / Validation
- Hipótesis:
- Setup:
- Métrica observada:
- Resultado:

## Key Tradeoffs
- Opción A vs Opción B
- Coste operativo vs simplicidad
- Rendimiento vs confiabilidad

## Decisions / Takeaways
- Decisión 1:
- Decisión 2:

## Follow-up Actions
- [ ] Acción concreta con fecha
- [ ] Documento a crear/actualizar

---

## Ejemplo real

### Metadata
- Date: 2026-03-02
- Domain: Infrastructure
- Source: Kubernetes scheduling deep dive
- Time invested (h): 2.5
- Difficulty (1-5): 4

### Problem Statement
Un servicio de API presenta latencia p95 alta en horas pico; se sospecha contención de CPU por límites mal definidos en pods.

### Core Concepts
- `requests` define scheduling guarantee.
- `limits` impone throttling de CPU por cgroup.
- El throttling sostenido impacta p95 y timeouts en cascada.

### Practical Scenario
Cluster multi-tenant con workloads batch y online compartiendo nodos.

### Experiment / Validation
- Hipótesis: reducir `cpu limit` agresivo y elevar `request` mejora estabilidad de latencia.
- Setup: canary 10% de tráfico por 2 horas.
- Métrica observada: `container_cpu_cfs_throttled_periods_total`, p95 latency, error rate.
- Resultado: throttling -38%, p95 -22%, sin aumento de costo > 5%.

### Key Tradeoffs
- Aumentar `requests` mejora QoS, pero reduce densidad por nodo.
- Quitar `limits` evita throttling, pero aumenta riesgo de noisy neighbors.

### Decisions / Takeaways
- Mantener `limits` menos agresivos y ajustar HPA por saturación real.
- Introducir alerta por throttling > 15% sostenido.

### Follow-up Actions
- [ ] Crear ADR de política de recursos en Kubernetes (2026-03-06)
- [ ] Actualizar runbook de tuning de performance (2026-03-08)
