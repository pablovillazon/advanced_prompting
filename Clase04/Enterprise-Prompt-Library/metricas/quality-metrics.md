# Quality Metrics
## Métricas para la Evaluación de Prompts

---

# Propósito

Las métricas de calidad permiten evaluar objetivamente el desempeño de un prompt y medir su evolución a lo largo del tiempo.

Su uso evita evaluaciones basadas únicamente en percepciones subjetivas y facilita la comparación entre distintas versiones del mismo prompt.

Las métricas presentadas en este documento complementan la **Prompt Scorecard** y pueden utilizarse como indicadores de calidad dentro de una Enterprise Prompt Library.

---

# ¿Por qué utilizar métricas?

Una organización necesita responder preguntas como:

- ¿La nueva versión del prompt realmente mejoró?
- ¿Qué aspecto fue optimizado?
- ¿El prompt es suficientemente robusto para producción?
- ¿Las mejoras son medibles?

Las métricas permiten responder estas preguntas mediante evidencia objetiva.

---

# Métrica 1: Exactitud (Accuracy)

## ¿Qué mide?

Evalúa si el prompt produce la respuesta correcta de acuerdo con el objetivo definido.

### Ejemplo

Objetivo:

Clasificar correctamente un Curriculum Vitae.

Resultado esperado:

Senior.

Resultado obtenido:

Senior.

**Evaluación:** Exactitud alta.

---

# Métrica 2: Completitud (Completeness)

## ¿Qué mide?

Determina si la respuesta incluye todos los elementos solicitados.

Por ejemplo:

- clasificación;
- justificación;
- evidencias;
- observaciones;
- nivel de confianza.

Una respuesta correcta pero incompleta reduce la calidad del prompt.

---

# Métrica 3: Consistencia (Consistency)

## ¿Qué mide?

Verifica que el prompt produzca resultados similares cuando recibe entradas equivalentes.

Un prompt consistente genera respuestas estables y predecibles.

### Ejemplo

Cinco ejecuciones del mismo documento producen la misma clasificación.

**Resultado esperado:** Alta consistencia.

---

# Métrica 4: Relevancia (Relevance)

## ¿Qué mide?

Evalúa si el modelo permanece enfocado en el objetivo solicitado.

Una respuesta pierde relevancia cuando:

- agrega información innecesaria;
- responde preguntas no formuladas;
- introduce recomendaciones no solicitadas.

Mientras más enfocada sea la respuesta, mayor será la relevancia.

---

# Métrica 5: Robustez (Robustness)

## ¿Qué mide?

Evalúa la capacidad del prompt para manejar situaciones no ideales.

Ejemplos:

- documentos incompletos;
- documentos con errores;
- texto proveniente de OCR;
- formatos poco estructurados;
- información contradictoria.

La robustez es especialmente importante en aplicaciones reales donde la calidad de los datos de entrada no siempre está garantizada.

---

# Resumen de Métricas

| Métrica | Pregunta clave |
|----------|----------------|
| Exactitud | ¿La respuesta es correcta? |
| Completitud | ¿Respondió todo lo solicitado? |
| Consistencia | ¿Produce resultados estables? |
| Relevancia | ¿Se mantiene enfocada en el objetivo? |
| Robustez | ¿Tolera entradas difíciles? |

---

# Recomendaciones

- Definir las métricas antes de iniciar las pruebas.
- Utilizar los mismos criterios en todas las versiones.
- Comparar resultados entre versiones del prompt.
- Registrar las métricas en la Prompt Scorecard.
- Utilizar los indicadores para justificar mejoras.

---

# Relación con otros documentos

Estas métricas alimentan los siguientes artefactos:

- `metrics/prompt-scorecard.md`
- `metrics/evaluation-dashboard.md`
- `versions/CHANGELOG.md`

---

# Conclusión

Las métricas de calidad permiten transformar la evaluación de prompts en un proceso sistemático y basado en evidencia. Al medir aspectos como exactitud, completitud, consistencia, relevancia y robustez, es posible demostrar objetivamente la evolución de un prompt y respaldar las decisiones de mejora continua dentro de una Enterprise Prompt Library.