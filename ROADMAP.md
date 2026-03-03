# ROADMAP (6 meses)

Horizonte: 24 semanas.
Cadencia: 1 revisión semanal + 1 revisión mensual.
Meta: pasar de ejecución SRE a diseño/arquitectura con ownership de confiabilidad end-to-end.

## Fase 1: Infraestructura y plataformas (Semanas 1-8)

### Objetivos
- Dominar fundamentos de plataforma moderna y operación reproducible.
- Estandarizar observabilidad mínima y prácticas de operación.
- Construir bases para decisiones de arquitectura posteriores.

### Entregables obligatorios
- 8 notas de clase técnicas (`docs/classes/infrastructure/`).
- 2 runbooks operativos (`ops/runbooks/`): despliegue y rollback.
- 1 documento de SLI/SLO inicial (`ops/sli-slo/`).
- 2 ADRs sobre decisiones de plataforma (`docs/architecture/adrs/`).
- 1 diseño de arquitectura base (`docs/architecture/system-designs/`).

### Contenido núcleo
- Linux internals para operación (CPU, memoria, IO, cgroups, namespaces).
- Networking de producción (L3/L4, DNS, TLS, balanceo, retries, timeouts).
- IaC y configuración declarativa (Terraform/OpenTofu + módulos).
- Containers y orquestación (Kubernetes primitives, scheduling, limits).
- Observabilidad foundation (logs, metrics, traces, alert fatigue).

### Criterios de salida
- Puedes explicar por qué un sistema falla bajo saturación y cómo mitigarlo.
- Tienes SLOs definidos para al menos un servicio ejemplo.
- Runbooks ejecutables sin conocimiento tribal.

## Fase 2: Sistemas distribuidos (Semanas 9-16)

### Objetivos
- Diseñar sistemas distribuidos con tradeoffs explícitos.
- Mejorar decisiones de consistencia, disponibilidad y costo.
- Operacionalizar patrones de resiliencia en arquitecturas reales.

### Entregables obligatorios
- 8 notas de clase (`docs/classes/distributed-systems/`).
- 3 diseños de sistema con escenarios de fallo (`docs/architecture/system-designs/`).
- 3 ADRs sobre storage, messaging y caché.
- 2 case studies (`portfolio/case-studies/`) orientados a negocio/técnica.
- 1 revisión técnica entre pares simulada (`templates/review-template.md` aplicado).

### Contenido núcleo
- Consenso y coordinación (Raft/Paxos a nivel práctico).
- Data partitioning, replication, quorum y consistency models.
- Event-driven architecture, queues y backpressure.
- Idempotencia, exactly-once myths, retries seguros.
- Cache-aside, invalidación, stampede protection.

### Criterios de salida
- Cada diseño incluye capacidad, límites y estrategia de degradación.
- Puedes defender decisiones CAP/PACELC según caso de uso.
- Los riesgos residuales están documentados y priorizados.

## Fase 3: Reliability engineering y arquitectura senior (Semanas 17-24)

### Objetivos
- Integrar diseño + operación + mejora continua en un sistema de confiabilidad.
- Elevar la narrativa técnica para nivel Senior/Staff.
- Construir evidencia clara de impacto y madurez arquitectónica.

### Entregables obligatorios
- 8 notas de clase (`docs/classes/reliability/`).
- 2 postmortems completos de incidentes reales o simulados.
- 2 diseños de arquitectura de referencia (`portfolio/reference-architectures/`).
- 1 documento de estrategia de confiabilidad trimestral.
- 1 paquete portfolio para entrevista (casos + decisiones + métricas).

### Contenido núcleo
- Error budgets y governance de SLOs.
- Capacity planning y performance engineering.
- Chaos/game days con hipótesis y medición.
- Incident command, comunicación ejecutiva, decisiones bajo presión.
- Roadmapping técnico y priorización por riesgo.

### Criterios de salida
- Puedes liderar una revisión de arquitectura con criterios operativos.
- Demuestras evolución cuantitativa en métricas de confiabilidad.
- Tu portfolio muestra decisiones defendibles con impacto verificable.

## Plan mensual consolidado

### Mes 1
- Baseline técnico y operativo.
- 1 ADR, 1 runbook, 4 clases.

### Mes 2
- Plataforma consolidada + observabilidad.
- 1 ADR, 1 diseño base, 4 clases.

### Mes 3
- Fundamentos distribuidos aplicados.
- 1 diseño distribuido, 1 case study, 4 clases.

### Mes 4
- Tradeoffs avanzados y resiliencia.
- 2 diseños, 2 ADRs, 4 clases.

### Mes 5
- Reliability program.
- 1 postmortem, 1 arquitectura de referencia, 4 clases.

### Mes 6
- Consolidación para nivel senior.
- 1 postmortem, 1 arquitectura de referencia, paquete portfolio final.

## Riesgos y mitigación
- Riesgo: acumulación de notas sin síntesis.
  - Mitigación: regla semanal de convertir notas en conocimiento reusable.
- Riesgo: exceso de teoría sin artefactos de operación.
  - Mitigación: cada bloque teórico debe producir runbook, diseño o postmortem.
- Riesgo: falta de consistencia por carga laboral.
  - Mitigación: mínimo no negociable de 4 horas semanales + revisión mensual.

## Definición de éxito al final de 6 meses
- >= 24 notas de clase técnicas de alta calidad.
- >= 6 diseños de arquitectura con tradeoffs y riesgos.
- >= 4 ADRs útiles y trazables.
- >= 2 postmortems completos con acciones verificables.
- >= 3 case studies listos para entrevista.
