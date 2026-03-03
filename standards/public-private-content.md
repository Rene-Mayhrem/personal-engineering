# Política de Contenido Público vs Privado

## Regla principal
Todo contenido del repositorio público debe poder compartirse sin riesgo legal, de seguridad o de confidencialidad.

## Contenido público (permitido)
- Diseños de referencia anonimizados.
- Postmortems sanitizados (sin datos de clientes).
- Runbooks genéricos.
- Lecciones aprendidas y tradeoffs técnicos.
- Arquitecturas y decisiones sin secretos ni propiedad intelectual sensible.

## Contenido privado (no publicar)
- Nombres de clientes, contratos, SLA reales.
- Topología exacta, IPs, cuentas, secretos, tokens.
- Códigos internos, datos regulatorios o financieros sensibles.
- Información salarial o de performance review personal.

## Estrategia recomendada
- Mantener `private/` para información sensible local.
- Publicar solo artefactos sanitizados y generalizados.
- Crear versión pública de cada caso con redacción neutral.

## Checklist de sanitización
- [ ] Sin nombres de empresa o cliente.
- [ ] Sin identificadores de infraestructura real.
- [ ] Sin capturas de dashboards con datos sensibles.
- [ ] Sin referencias a incidentes no públicos.
- [ ] Sin secretos en texto, código o metadata.
