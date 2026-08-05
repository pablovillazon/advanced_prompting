# Clase 4 - Bloque 3
# Métricas y Calidad de Prompts

---

# Diapositiva 5
# ¿Cómo medir la calidad de un prompt?

## "Lo que no se puede medir, no se puede mejorar"

Hasta la clase anterior evaluamos los prompts utilizando casos de prueba y un reporte de evaluación.

En un entorno organizacional esto no es suficiente. Es necesario definir **métricas objetivas** que permitan comparar versiones, justificar mejoras y tomar decisiones basadas en evidencia.

### Una buena métrica debe ser

- Objetiva.
- Repetible.
- Fácil de interpretar.
- Independiente del evaluador.
- Útil para comparar distintas versiones del mismo prompt.

### Métricas recomendadas

| Métrica | ¿Qué evalúa? |
|----------|--------------|
| Exactitud | ¿La respuesta es correcta? |
| Completitud | ¿Responde todos los aspectos solicitados? |
| Consistencia | ¿Produce resultados similares ante entradas equivalentes? |
| Relevancia | ¿La respuesta se mantiene enfocada en el objetivo? |
| Robustez | ¿Responde adecuadamente ante entradas incompletas, ambiguas o mal estructuradas? |

Estas métricas pueden obtenerse utilizando la **Prompt Test Suite** desarrollada durante la Clase 3.

> **Idea clave:** La calidad de un prompt debe demostrarse con evidencia obtenida mediante pruebas y métricas, no únicamente con percepciones subjetivas.

---

### Notas del docente

**Conceptos clave**

- Prompt Quality.
- Quality Metrics.
- Evaluación objetiva.
- Indicadores de desempeño.
- Mejora continua.

**Bibliografía**

- White et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT*.
- OpenAI Documentation – Prompt Engineering Best Practices.
- Microsoft Learn – Evaluate Generative AI Applications.
- Google Cloud – Generative AI Evaluation Concepts.

---

# Diapositiva 6
# Prompt Scorecard

## Evaluación basada en evidencia

Una forma sencilla de comparar distintas versiones de un prompt consiste en utilizar una **Scorecard**, donde cada criterio recibe una puntuación.

### Ejemplo

| Criterio | Puntaje (1–5) |
|-----------|:-------------:|
| Exactitud | ⭐⭐⭐⭐⭐ |
| Completitud | ⭐⭐⭐⭐☆ |
| Consistencia | ⭐⭐⭐⭐⭐ |
| Relevancia | ⭐⭐⭐⭐⭐ |
| Robustez | ⭐⭐⭐☆☆ |

### Interpretación

- **22–25 puntos:** Prompt listo para producción.
- **18–21 puntos:** Requiere mejoras menores.
- **13–17 puntos:** Debe refinarse antes de reutilizarse.
- **Menos de 13 puntos:** Requiere rediseño.

### ¿Para qué sirve una Scorecard?

- Comparar versiones del mismo prompt.
- Identificar fortalezas y debilidades.
- Priorizar mejoras.
- Documentar la evolución del prompt.
- Comunicar resultados al equipo.

En organizaciones, estas métricas pueden incorporarse a procesos de revisión similares a los utilizados en el desarrollo de software.

> **Idea clave:** Una Scorecard convierte la evaluación de prompts en un proceso sistemático, reproducible y orientado a la mejora continua.

---

### Notas del docente

**Mensaje para reforzar**

Un prompt no debería aprobarse únicamente porque "parece funcionar". Al igual que el software, debe cumplir criterios de calidad medibles. La Scorecard proporciona un lenguaje común para evaluar, comparar y justificar cambios entre distintas versiones.

**Bibliografía**

- ISO/IEC 25010 – Systems and Software Quality Models (como referencia conceptual para atributos de calidad).
- Microsoft Learn – Responsible AI Evaluation.
- OpenAI Cookbook.
- LangSmith Documentation (conceptos de evaluación de aplicaciones basadas en LLMs).