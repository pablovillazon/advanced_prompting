# Evaluation Dashboard
## Panel de Control para la Evaluación de Prompts

---

# Propósito

El **Evaluation Dashboard** proporciona una vista resumida del estado de calidad de un prompt.

En lugar de revisar múltiples documentos (Scorecards, Test Cases, Reportes de Evaluación o CHANGELOG), el Dashboard concentra los indicadores más relevantes para apoyar la toma de decisiones.

Su objetivo es responder rápidamente preguntas como:

- ¿Está listo el prompt para producción?
- ¿Cuál es su versión actual?
- ¿Qué calidad tiene?
- ¿Cuándo fue evaluado por última vez?
- ¿Qué aspectos requieren mejoras?

---

# Información recomendada

Un Dashboard debería mostrar como mínimo:

- Nombre del prompt.
- Versión.
- Estado.
- Fecha de evaluación.
- Puntaje total.
- Resultados por métrica.
- Cobertura de pruebas.
- Próximas mejoras.

---

# Indicadores sugeridos

## Estado del Prompt

Puede utilizarse la siguiente clasificación:

| Estado | Significado |
|----------|------------|
| 🟢 Ready for Production | Cumple los criterios establecidos. |
| 🟡 Needs Improvement | Requiere mejoras menores. |
| 🔴 Under Review | Requiere rediseño o nuevas pruebas. |

---

## Indicadores mínimos

| Indicador | Descripción |
|-----------|-------------|
| Versión | Última versión publicada. |
| Score | Resultado de la Prompt Scorecard. |
| Exactitud | Resultado obtenido. |
| Consistencia | Nivel alcanzado. |
| Robustez | Comportamiento ante casos difíciles. |
| Casos ejecutados | Total de pruebas realizadas. |
| Cobertura | Porcentaje de casos ejecutados respecto al total planificado. |
| Última evaluación | Fecha de la evaluación más reciente. |

---

# Buenas Prácticas

- Actualizar el Dashboard después de cada nueva versión.
- Mantener coherencia con la Scorecard y el CHANGELOG.
- Registrar únicamente información verificable.
- Utilizar el Dashboard como punto de entrada para revisar el estado general del prompt.

---

# Relación con otros documentos

El Dashboard consolida información proveniente de:

- `metrics/prompt-scorecard.md`
- `metrics/quality-metrics.md`
- `evaluations/prompt-evaluation-report.md`
- `versions/CHANGELOG.md`

---

# Conclusión

El Evaluation Dashboard facilita el seguimiento de la calidad de los prompts a lo largo del tiempo y permite comunicar de forma clara el estado de un proyecto a desarrolladores, revisores y responsables del negocio. Constituye una práctica habitual en procesos de ingeniería donde las decisiones deben apoyarse en indicadores y no únicamente en observaciones individuales.