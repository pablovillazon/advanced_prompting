# Prompt Scorecard
## Evaluación de Calidad de Prompts

---

# Propósito

La **Prompt Scorecard** es un instrumento utilizado para evaluar objetivamente la calidad de un prompt.

Su objetivo es proporcionar un conjunto de criterios medibles que permitan:

- comparar distintas versiones del mismo prompt;
- identificar oportunidades de mejora;
- justificar cambios realizados;
- apoyar decisiones antes de utilizar un prompt en producción.

La Scorecard complementa el reporte de evaluación (`Prompt Evaluation Report`) y forma parte del proceso de **Prompt Quality Engineering**.

---

# ¿Cuándo utilizar la Scorecard?

Se recomienda completar una Scorecard cuando:

- se desarrolla una nueva versión del prompt;
- se realizan mejoras importantes;
- finaliza una ronda de casos de prueba;
- se desea comparar dos versiones del mismo prompt;
- un prompt será utilizado en un entorno organizacional.

---

# Criterios de Evaluación

## 1. Exactitud

Evalúa si la respuesta generada cumple correctamente el objetivo solicitado.

Preguntas guía:

- ¿La clasificación fue correcta?
- ¿La respuesta contiene errores?
- ¿Se respetó el contexto?

---

## 2. Completitud

Evalúa si el modelo respondió todos los elementos solicitados.

Preguntas guía:

- ¿Respondió todas las secciones?
- ¿Faltó información importante?
- ¿La salida quedó incompleta?

---

## 3. Consistencia

Evalúa la estabilidad del prompt.

Preguntas guía:

- ¿Entradas similares producen resultados similares?
- ¿El comportamiento es repetible?

---

## 4. Relevancia

Evalúa si la respuesta permanece enfocada en el objetivo.

Preguntas guía:

- ¿Existe información innecesaria?
- ¿El modelo divaga?
- ¿La respuesta responde exactamente lo solicitado?

---

## 5. Robustez

Evalúa el comportamiento frente a entradas difíciles.

Por ejemplo:

- documentos incompletos;
- documentos desordenados;
- información contradictoria;
- texto copiado desde OCR.

---

# Escala de Evaluación

| Puntaje | Interpretación |
|----------|----------------|
| **5** | Excelente |
| **4** | Muy bueno |
| **3** | Aceptable |
| **2** | Requiere mejoras importantes |
| **1** | Deficiente |

---

# Interpretación del Puntaje Total

| Puntaje | Estado |
|----------|---------|
| 22–25 | Listo para producción |
| 18–21 | Requiere ajustes menores |
| 13–17 | Debe refinarse |
| Menor a 13 | Requiere rediseño |

---

# Buenas Prácticas

- Evaluar siempre después de ejecutar los casos de prueba.
- Justificar cada puntuación con evidencia.
- Comparar la Scorecard entre versiones.
- Conservar el historial de evaluaciones.

---

# Relación con otros documentos

La Scorecard debe utilizarse junto con:

- `evaluations/prompt-evaluation-report.md`
- `versions/CHANGELOG.md`
- `versions/VERSIONING.md`

De esta forma es posible justificar objetivamente la evolución del prompt.

---

# Conclusión

La Prompt Scorecard convierte la evaluación de un prompt en un proceso sistemático y reproducible. Al asignar criterios medibles y documentar los resultados, facilita la mejora continua y proporciona evidencia para decidir cuándo un prompt está preparado para ser reutilizado o desplegado en un entorno organizacional.