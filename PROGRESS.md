# PROGRESS

Sistema de medición para verificar crecimiento real, no solo actividad.

## Baseline (Semana 0)
Completar antes de iniciar:
- Horas semanales disponibles reales:
- Nivel percibido por dominio (1-5): Infra / Distribuidos / Reliability / Arquitectura.
- % de documentos existentes con criterio audit-ready:
- Incidentes analizados formalmente en los últimos 3 meses:
- Número actual de diseños defendibles en entrevista:

## KPIs principales

| KPI | Tipo | Meta 6 meses | Frecuencia | Fuente |
|---|---|---:|---|---|
| Horas de deep work técnico | Leading | >= 180h | semanal | tracking/weekly-review-template.md |
| Notas de clase de calidad | Leading | >= 24 | semanal | docs/classes/ |
| Diseños de arquitectura completos | Lagging | >= 6 | mensual | docs/architecture/system-designs/ |
| ADRs con decisión ejecutable | Lagging | >= 4 | mensual | docs/architecture/adrs/ |
| Postmortems completos | Lagging | >= 2 | mensual | ops/postmortems/ |
| SLOs definidos y revisados | Outcome | >= 2 servicios | mensual | ops/sli-slo/ |
| Case studies de impacto | Outcome | >= 3 | mensual | portfolio/case-studies/ |
| % acciones cerradas de postmortem | Reliability | >= 80% | mensual | ops/postmortems/ |

## Scorecard mensual

| Mes | Horas | Clases | Diseños | ADRs | Postmortems | Case Studies | % Acciones cerradas |
|---|---:|---:|---:|---:|---:|---:|---:|
| M1 |  |  |  |  |  |  |  |
| M2 |  |  |  |  |  |  |  |
| M3 |  |  |  |  |  |  |  |
| M4 |  |  |  |  |  |  |  |
| M5 |  |  |  |  |  |  |  |
| M6 |  |  |  |  |  |  |  |

## Reglas de calidad por artefacto

### Nota de clase válida
- Tiene problema técnico concreto.
- Incluye experimento o escenario operativo.
- Termina con decisiones o acciones aplicables.

### Diseño válido
- Tiene requisitos funcionales y no funcionales.
- Incluye diagrama + capacidad + failure modes.
- Declara tradeoffs y riesgos residuales.

### Postmortem válido
- Timeline con UTC, RCA claro y acciones con dueño/fecha.
- Evita culpas personales.
- Mide efectividad de acciones posteriores.

## Rutina de revisión
- Semanal (45 min): actualizar métricas leading + plan de la semana.
- Mensual (90 min): evaluar outcomes y ajustar roadmap.
- Trimestral (2h): re-priorizar dominios según brechas.
