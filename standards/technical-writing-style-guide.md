# Guía de Escritura Técnica (Senior Level)

## Objetivo
Escribir documentos que soporten decisiones de arquitectura y operación real bajo escrutinio técnico.

## Principios
- Precisión: afirmaciones respaldadas por datos o supuestos explícitos.
- Claridad: una idea principal por sección.
- Trazabilidad: enlazar decisiones con evidencia.
- Acción: terminar con decisiones, riesgos y siguientes pasos.

## Estructura recomendada
1. Contexto y problema.
2. Requisitos y restricciones.
3. Opciones evaluadas.
4. Decisión y tradeoffs.
5. Riesgos residuales y mitigaciones.
6. Métricas de éxito.

## Estilo
- Frases directas y concretas.
- Evitar adjetivos vagos: "robusto", "escalable" sin métrica.
- Usar unidades: ms, RPS, GiB, %, SLO.
- Explicitar incertidumbre: "No se midió X, se asume Y".

## Anti-patterns
- Resúmenes sin datos.
- Recomendaciones sin alternativas evaluadas.
- Diagnósticos con culpables personales.
- Conclusiones sin impacto operativo.

## Checklist antes de publicar
- [ ] ¿Un tercero puede ejecutar o refutar la decisión?
- [ ] ¿Hay tradeoffs explícitos?
- [ ] ¿Hay impacto en costo, confiabilidad y complejidad?
- [ ] ¿Hay métricas para validar éxito?
- [ ] ¿Se documentó riesgo residual?
