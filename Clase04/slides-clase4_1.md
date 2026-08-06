---
marp: false
---

# Clase 4 - Bloque 1
# PromptOps: Del Prompt Engineering a la Gestión Organizacional

---

# Diapositiva 1
# PromptOps: cuando los prompts dejan de ser individuales

## ¿Qué ocurre cuando una organización utiliza cientos de prompts?

Hasta este momento hemos aprendido a:

- Diseñar prompts.
- Documentarlos.
- Evaluarlos.
- Refinarlos mediante casos de prueba.

Sin embargo, en una organización los prompts dejan de ser documentos personales y pasan a convertirse en **activos reutilizables** que soportan procesos de negocio.

Esto plantea nuevos desafíos:

- ¿Dónde se almacenan?
- ¿Quién puede modificarlos?
- ¿Cómo se controlan los cambios?
- ¿Cómo se reutilizan?
- ¿Cómo se garantiza su calidad?

Surge entonces el concepto de **PromptOps**, una disciplina orientada a gestionar el ciclo de vida de los prompts de manera similar a como DevOps gestiona el ciclo de vida del software.

> **Idea clave:** Un buen prompt no solo debe producir buenas respuestas; también debe poder mantenerse, evolucionar y reutilizarse en un entorno colaborativo.

---

### Notas del docente

**Conceptos clave**

- PromptOps.
- Prompt Lifecycle.
- Enterprise Prompt Library.
- Gestión del conocimiento.
- Activos digitales.

**Bibliografía**

- White, J., Fu, Q., Hays, S., et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT*. arXiv.
- Microsoft Learn. *Prompt Engineering Techniques*.
- Anthropic Documentation. *Prompt Engineering Overview*.
- OpenAI Documentation. *Prompt Engineering Best Practices*.

---

# Diapositiva 2
# Del Prompt Engineering al PromptOps

## Evolución del trabajo realizado durante el módulo

Durante las cuatro clases hemos seguido un proceso incremental que refleja el ciclo de vida de un prompt.

```text
Diseño
    ↓
Documentación
    ↓
Evaluación
    ↓
Refinamiento
    ↓
Versionado
    ↓
Gobernanza
    ↓
Reutilización
```

Cada etapa incorpora nuevas prácticas que aumentan la calidad y sostenibilidad del activo.

| Etapa | Producto generado |
|--------|-------------------|
| Diseño | Prompt inicial |
| Documentación | README, plantillas y ejemplos |
| Evaluación | Casos de prueba y reporte de evaluación |
| Refinamiento | Prompt mejorado |
| Versionado | Historial de cambios |
| Gobernanza | Reglas para mantenimiento y reutilización |

Una organización madura no gestiona únicamente prompts, sino **bibliotecas completas de prompts** con procesos de revisión, documentación y mejora continua.

> **Idea clave:** PromptOps transforma un conjunto de prompts en un sistema organizado, mantenible y escalable.

---

### Notas del docente

**Mensaje para reforzar**

Muchos equipos comienzan almacenando prompts en documentos o conversaciones aisladas. Con el tiempo aparecen duplicados, versiones inconsistentes y pérdida de conocimiento. PromptOps propone tratar los prompts como cualquier otro artefacto de ingeniería: documentado, versionado, probado y gobernado.

**Bibliografía**

- White et al. (2023). *Prompt Pattern Catalog*.
- OpenAI Cookbook.
- LangChain Documentation (Prompt Management).
- GitHub Engineering Blog (buenas prácticas de colaboración y versionado).