# personal-systems-engineering

Repositorio para construir una trayectoria autodidacta de nivel senior en Systems Engineering, con enfoque práctico en SRE, arquitectura y operación de sistemas reales.

## Visión
Desarrollar un sistema de aprendizaje y ejecución técnica que produzca evidencia verificable de capacidad para diseñar, operar y evolucionar plataformas distribuidas confiables.

## Objetivos
- Consolidar una `Knowledge Base` técnica con criterio de producción.
- Mantener un `Engineering Notebook` de clases, experimentos y decisiones.
- Construir un `Portfolio` auditable de diseño y arquitectura.
- Medir progreso con métricas cuantitativas y revisiones periódicas.
- Demostrar crecimiento de SRE a Senior Architect con entregables reales.

## Principios de diseño
- Profesional: cada documento debe servir para operar, decidir o comunicar.
- Minimalista: estructura simple, sin carpetas vacías innecesarias.
- Escalable: fácil de extender por dominios y por año.
- Trazable: cada decisión importante debe tener contexto y evidencia.
- Operable: prioriza runbooks, postmortems, SLOs y diseños ejecutables.

## Estructura del repositorio
```text
.
├── README.md
├── ROADMAP.md
├── PROGRESS.md
├── docs/
│   ├── architecture/
│   │   ├── adrs/
│   │   ├── diagrams/
│   │   └── system-designs/
│   ├── classes/
│   │   ├── infrastructure/
│   │   ├── distributed-systems/
│   │   └── reliability/
│   ├── knowledge-base/
│   │   ├── fundamentals/
│   │   ├── cloud/
│   │   ├── networking/
│   │   ├── databases/
│   │   ├── observability/
│   │   └── security/
│   └── reference/
│       ├── papers/
│       ├── books/
│       └── links/
├── ops/
│   ├── incident-reviews/
│   ├── postmortems/
│   ├── runbooks/
│   └── sli-slo/
├── portfolio/
│   ├── artifacts/
│   ├── case-studies/
│   └── reference-architectures/
├── standards/
│   ├── commit-convention.md
│   ├── file-naming-convention.md
│   ├── public-private-content.md
│   └── technical-writing-style-guide.md
├── templates/
│   ├── class-template.md
│   ├── design-template.md
│   ├── postmortem-template.md
│   └── review-template.md
├── tracking/
│   ├── monthly-review-template.md
│   └── weekly-review-template.md
├── blog/
│   ├── assets/images/
│   ├── drafts/
│   └── published/
└── private/
    ├── career/
    ├── interview-prep/
    ├── journal/
    └── salary/
```

## Flujo de trabajo recomendado
1. Captura clase o lectura en `docs/classes/` usando `templates/class-template.md`.
2. Extrae conocimiento estable a `docs/knowledge-base/`.
3. Si hay una decisión, registra ADR en `docs/architecture/adrs/`.
4. Si hay diseño completo, crea documento en `docs/architecture/system-designs/` con `templates/design-template.md`.
5. Si hubo incidente o simulación, documenta en `ops/postmortems/`.
6. Resume impacto para CV/entrevista en `portfolio/case-studies/`.
7. Actualiza `PROGRESS.md` cada semana.

## Estándares obligatorios
- Convención de commits: `standards/commit-convention.md`
- Convención de nombres: `standards/file-naming-convention.md`
- Guía de escritura técnica: `standards/technical-writing-style-guide.md`
- Separación público/privado: `standards/public-private-content.md`

## Criterio de calidad (audit-ready)
Un documento se considera aceptable solo si:
- Explica el problema con contexto operativo.
- Declara supuestos y restricciones.
- Incluye tradeoffs explícitos.
- Define métricas de éxito y riesgo residual.
- Permite que otra persona ejecute o critique la decisión.

## Primeros pasos
1. Leer `ROADMAP.md` y ajustar disponibilidad semanal real.
2. Configurar baseline de métricas en `PROGRESS.md`.
3. Crear primera clase en `docs/classes/infrastructure/`.
4. Publicar primer diseño en `docs/architecture/system-designs/`.
