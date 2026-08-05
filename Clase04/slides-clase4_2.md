# Clase 4 - Bloque 2
# Versionado y Gobernanza de Prompts

---

# Diapositiva 3
# ¿Por qué versionar un prompt?

## Un prompt también evoluciona

Después de ejecutar pruebas y recibir retroalimentación, es normal que un prompt cambie.

Las modificaciones pueden incluir:

- Corrección de errores.
- Mejora en las instrucciones.
- Incorporación de nuevos casos de uso.
- Cambios en el formato de salida.
- Adaptación a nuevos modelos de IA.

Si estos cambios no se registran, rápidamente aparecen problemas como:

- Múltiples versiones del mismo prompt.
- Dificultad para reproducir resultados.
- Pérdida de mejoras anteriores.
- Incertidumbre sobre cuál versión utilizar.

En un entorno organizacional, cada cambio debe quedar documentado y ser fácilmente rastreable.

### Versionado Semántico

Se recomienda utilizar un esquema similar al empleado en el desarrollo de software.

| Versión | Cuándo utilizarla |
|---------|-------------------|
| **v1.0** | Primera versión estable del prompt. |
| **v1.1** | Corrección menor o mejora del texto sin modificar el comportamiento esperado. |
| **v1.2** | Ajustes menores derivados de nuevos casos de prueba. |
| **v2.0** | Cambios importantes en la estructura, lógica o alcance del prompt. |

> **Idea clave:** Un prompt sin versión es un documento difícil de mantener y reproducir.

---

### Notas del docente

**Conceptos clave**

- Semantic Versioning.
- Prompt Versioning.
- Trazabilidad.
- Reproducibilidad.
- Control de cambios.

**Bibliografía**

- Semantic Versioning 2.0 (semver.org).
- Git Documentation.
- OpenAI Cookbook.
- Microsoft Learn – Prompt Engineering.

---

# Diapositiva 4
# Gobernanza de Prompts

## Más allá del versionado

Versionar un prompt es solo una parte del proceso.

La **gobernanza** define las reglas que permiten administrar una biblioteca de prompts de forma consistente y colaborativa.

### Buenas prácticas

- Mantener un único repositorio oficial.
- Documentar el propósito de cada prompt.
- Registrar todas las modificaciones realizadas.
- Conservar ejemplos y casos de prueba.
- Asociar cada versión con su evaluación correspondiente.
- Evitar duplicidad de prompts con funcionalidades similares.
- Establecer responsables para la revisión y aprobación de cambios.

### Artefactos mínimos de gobernanza

```text
Enterprise-Prompt-Library/

README.md
CHANGELOG.md
VERSIONING.md

prompts/
templates/
sample-data/
evaluations/
docs/
```

Cada uno de estos documentos cumple una función específica para garantizar que cualquier integrante del equipo pueda comprender, reutilizar y mantener los prompts desarrollados.

> **Idea clave:** La gobernanza convierte una colección de prompts en un activo organizacional sostenible.

---

### Notas del docente

**Mensaje para reforzar**

La mayoría de los problemas en organizaciones no provienen de prompts mal diseñados, sino de la falta de documentación, control de versiones y procesos de mantenimiento. Una buena gobernanza facilita la colaboración, reduce errores y preserva el conocimiento generado por el equipo.

**Bibliografía**

- GitHub Docs – Repository Best Practices.
- Microsoft Learn – AI Engineering.
- OpenAI Documentation – Prompt Engineering Best Practices.
- White et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT*.