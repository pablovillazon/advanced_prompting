# Clase 3
## Evaluación, Control y Mitigación de Riesgos en Prompts

---

# Diapositiva 1
# Prompt Engineering Avanzado

## Clase 3

### Evaluación, Control y Mitigación de Riesgos en Prompts

---

## ¿Qué aprenderemos hoy?

Pasaremos de diseñar prompts a **evaluarlos sistemáticamente**.

Aprenderemos a medir su calidad, identificar riesgos y aplicar mejoras para aumentar su confiabilidad antes de utilizarlos en procesos organizacionales.

---

### Idea clave

> **Si un prompt no puede evaluarse, tampoco puede mejorarse.**

---

### Referencias

- White et al. (2023). *Prompt Pattern Catalog.*
- OpenAI Prompt Engineering Guide.
- Anthropic Prompt Engineering Best Practices.

---

# Diapositiva 2
# ¿Por qué evaluar un Prompt?

---

Un buen resultado obtenido una sola vez **no garantiza** que un prompt sea confiable.

Un prompt utilizado en un entorno organizacional debe producir respuestas:

- Correctas
- Consistentes
- Reproducibles
- Comprensibles
- Alineadas con el objetivo del proceso

---

## Analogía

Un programa de software no se considera terminado únicamente porque "funcionó una vez".

Los prompts deben seguir el mismo principio.

---

### Idea clave

> **Prompt Engineering → Prompt Quality Engineering**

---

### Referencias

- Chip Huyen — *AI Engineering*
- Ammann & Offutt — *Introduction to Software Testing*

---

# Diapositiva 3
# Riesgos en Prompt Engineering

---

## Riesgos frecuentes

🔴 Alucinaciones

🟡 Omisión de información

🟠 Ambigüedad

🔵 Inconsistencia entre ejecuciones

🟣 Sesgos

⚫ Sobreconfianza del modelo

---

## Impacto

Un mismo prompt puede producir decisiones diferentes dependiendo del contexto, la entrada o el modelo utilizado.

---

### Idea clave

> **La IA no solo debe responder; debe responder de forma confiable.**

---

### Referencias

- OpenAI Cookbook
- Anthropic Documentation
- NIST AI Risk Management Framework

---

# Diapositiva 4
# Framework de Evaluación de Prompts

---

```text
Prompt

↓

Entrada

↓

LLM

↓

Salida

↓

Evaluación

↓

Retroalimentación

↓

Nueva versión
```

---

## Criterios de evaluación

- Exactitud
- Completitud
- Consistencia
- Relevancia
- Trazabilidad
- Reproducibilidad

---

### Idea clave

> **Todo prompt debe evolucionar mediante un proceso iterativo de evaluación y mejora.**

---

### Referencias

- White et al. (2023)
- AI Engineering (Chip Huyen)

---

# Diapositiva 5
# Del Testing de Software al Testing de Prompts

---

## Un prompt también puede probarse

Diseñamos diferentes casos de prueba para validar su comportamiento.

Ejemplos:

✅ Caso esperado

⚠ Entrada incompleta

⚠ Información contradictoria

⚠ Datos faltantes

⚠ Caso extremo

---

## Producto

Un conjunto de pruebas que permita medir el desempeño del prompt.

---

### Idea clave

> **Los casos de prueba reducen la incertidumbre y aumentan la confianza en los resultados.**

---

### Referencias

- ISO/IEC 25010 (adaptación conceptual)
- Pezzè & Young — *Software Testing and Analysis*

---

# Diapositiva 6
# Laboratorio

---

## Construiremos un Prompt Evaluation Framework

Cada estudiante evaluará el prompt desarrollado en la clase anterior utilizando múltiples documentos de prueba.

El resultado será un reporte de evaluación que incluirá:

- Casos de prueba
- Resultados obtenidos
- Problemas identificados
- Propuesta de mejora

---

## Evidencia

Nueva carpeta del repositorio:

```text
evaluations/
```

---

### Idea clave

> **No basta con escribir un prompt; es necesario demostrar que funciona correctamente.**

---

# Diapositiva 7
# Cierre

---

## Hoy aprendimos

✔ Los prompts deben evaluarse.

✔ Existen riesgos asociados al uso de IA generativa.

✔ La calidad puede medirse mediante criterios objetivos.

✔ Los casos de prueba permiten mejorar continuamente un prompt.

✔ La evaluación forma parte del ciclo de vida de una Enterprise Prompt Library.

---

## Próxima clase

### Optimización y Escalamiento de Prompts en Entornos Organizacionales

- Modularización
- Versionamiento
- Bibliotecas empresariales
- Automatización de workflows

---

### Mensaje Final

> **Los mejores prompts no son los que producen la respuesta más impresionante, sino aquellos que generan resultados confiables, repetibles y mantenibles dentro de una organización.**