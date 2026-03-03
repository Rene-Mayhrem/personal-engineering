# Convención de Nombres de Archivos

Objetivo: nombres predecibles, buscables y escalables.

## Reglas base
- Usar `kebab-case`.
- Solo minúsculas y ASCII.
- Evitar espacios y nombres genéricos (`notes.md`, `final.md`, `misc.md`).
- Incluir contexto técnico y, cuando aplique, fecha ISO `YYYY-MM-DD`.

## Patrones por tipo
- Clase: `YYYY-MM-DD-topic-domain-class.md`
  - Ejemplo: `2026-03-02-kubernetes-resource-governance-infra-class.md`
- Diseño: `system-name-vN.md`
  - Ejemplo: `notification-pipeline-v1.md`
- ADR: `adr-XXXX-short-title.md`
  - Ejemplo: `adr-0003-kafka-for-event-streaming.md`
- Postmortem: `incident-id-short-title.md`
  - Ejemplo: `inc-2026-03-01-api-502-checkout.md`
- Case study: `YYYY-MM-impact-topic-case-study.md`
  - Ejemplo: `2026-05-payment-reliability-case-study.md`

## Versionado de documentos
- Draft inicial: `-v1`
- Cambios mayores: incrementar `vN`
- No usar `final`, `latest`, `new`.
