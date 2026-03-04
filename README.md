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
│   ├── subjects/
│   │   ├── algorithms-and-data-structures/
│   │   ├── containers-and-orchestration/
│   │   ├── system-design-studio/
│   │   └── ... (otras materias)
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

## Cómo usar las carpetas
- `docs/subjects/`: planificación curricular por materia. Aquí defines objetivos, semanas, evaluación y criterios de salida (`syllabus.md`).
- `docs/classes/`: notas de ejecución por sesión de estudio/lab. Deben incluir experimento, métricas y decisiones.
- `docs/knowledge-base/`: conocimiento estable y reusable. Solo entra contenido que ya validaste en práctica.
- `docs/architecture/adrs/`: decisiones de arquitectura con contexto, alternativa y consecuencias.
- `docs/architecture/system-designs/`: diseños completos listos para revisión técnica (NFRs, capacidad, failure modes, rollout).
- `docs/reference/`: fuentes primarias (papers, libros, links) que sustentan decisiones.
- `ops/runbooks/`: procedimientos operativos accionables (deploy, rollback, mitigación).
- `ops/postmortems/`: análisis de incidentes con timeline UTC, RCA y acciones con due date.
- `ops/sli-slo/`: definición y seguimiento de SLI/SLO/error budget por servicio.
- `portfolio/case-studies/`: evidencia de impacto técnico y de negocio para entrevistas/revisión senior.
- `portfolio/reference-architectures/`: arquitecturas reutilizables para problemas recurrentes.
- `portfolio/artifacts/`: evidencias de soporte (diagramas, tablas de capacidad, reportes).
- `tracking/`: revisiones semanales/mensuales y control de KPIs.
- `standards/`: reglas del sistema (commits, naming, escritura técnica, público vs privado).
- `templates/`: plantillas base para asegurar calidad homogénea de documentos.
- `blog/`: borradores y artículos publicados cuando conviertas artefactos en contenido público.
- `private/`: trabajo sensible o personal no publicable.

## Flujo recomendado por cada sesión
1. Abrir materia en `docs/subjects/*/syllabus.md` y elegir objetivo de la semana.
2. Ejecutar estudio/lab y registrar evidencia en `docs/classes/`.
3. Promover aprendizajes estables a `docs/knowledge-base/`.
4. Si hubo decisión o diseño, crear ADR o system design.
5. Si hubo incidente/simulación, crear postmortem y acciones.
6. Actualizar KPIs en `PROGRESS.md` y revisión en `tracking/`.

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
- Plantilla de syllabus: `templates/syllabus-template.md`

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
