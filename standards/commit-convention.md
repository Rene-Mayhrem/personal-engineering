# Convención de Commits

Convención basada en Conventional Commits, ajustada para ingeniería de plataformas.

## Formato
`<type>(<scope>): <summary>`

Ejemplo:
`feat(reliability): define error budget policy for checkout-api`

## Types permitidos
- `feat`: nueva capacidad o comportamiento.
- `fix`: corrección de bug o regresión.
- `docs`: documentación técnica.
- `refactor`: cambio estructural sin alterar comportamiento externo.
- `test`: pruebas o validaciones.
- `chore`: tareas de mantenimiento.
- `perf`: mejora de rendimiento.
- `build`: cambios de build/deps/pipeline.
- `ops`: cambios operativos (runbooks, alertas, SLOs, incident tooling).

## Scopes recomendados
- `infra`
- `networking`
- `k8s`
- `observability`
- `distributed`
- `reliability`
- `security`
- `portfolio`
- `docs`

## Reglas
- Summary en imperativo y máximo 72 caracteres.
- Un commit = una intención coherente.
- Referenciar ticket/incidente cuando aplique.
- Para breaking changes usar footer `BREAKING CHANGE:`.

## Ejemplos
- `feat(distributed): add outbox pattern design for order events`
- `fix(observability): reduce false positives in saturation alert`
- `ops(reliability): add runbook for kafka consumer lag spikes`
- `docs(portfolio): publish case study on payment outage`
