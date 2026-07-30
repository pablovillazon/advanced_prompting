---
marp: false
theme: default
paginate: true
headingDivider: 2
footer: "Diplomado en Automatización de Procesos con IA Generativa - Módulo 4"
---

# Prompt Engineering Avanzado

## Clase 1
### Del Prompting al Prompt Engineering

**Diplomado en Automatización de Procesos con Inteligencia Artificial Generativa y Prompt Engineering**

**Módulo 4**

**Duración:** 2 horas

---

**Idea clave**

Durante esta sesión aprenderemos que el Prompt Engineering no consiste únicamente en escribir instrucciones para un modelo de IA. Analizaremos cómo diseñar prompts utilizando principios de ingeniería, con énfasis en la reutilización, la calidad y la mantenibilidad.

::: notes

### Objetivo docente

Presentar el propósito general del módulo y explicar cómo este se diferencia de los contenidos desarrollados en los módulos anteriores.

### Mensaje principal

En los módulos anteriores aprendimos a utilizar la IA.

En este módulo aprenderemos a diseñar soluciones basadas en IA.

### Imagen sugerida

Ilustración que represente un ecosistema compuesto por:

- Usuarios
- Modelos LLM
- Procesos organizacionales
- Automatización
- Bases de datos

### Referencias

OpenAI. Prompt Engineering Guide.

Anthropic. Prompt Engineering Overview.

Google Cloud. Prompt Design Guide.

:::
---

# Objetivos de la sesión

Al finalizar esta clase el estudiante será capaz de:

- Comprender por qué el Prompt Engineering constituye una disciplina de ingeniería.
- Diferenciar un prompt improvisado de un prompt diseñado.
- Reconocer los principios fundamentales que caracterizan un prompt profesional.
- Identificar la estructura general de un prompt reutilizable.
- Aplicar estos conceptos durante el laboratorio práctico.

---

> **Idea clave**

El objetivo no es escribir prompts más largos, sino diseñar prompts mejores.

::: notes

### Objetivo docente

Presentar claramente las competencias que se desarrollarán durante la sesión.

### Pregunta para iniciar la discusión

¿Cuántos de ustedes reutilizan exactamente el mismo prompt en distintas ocasiones?

Normalmente la mayoría responderá que no.

A partir de esta respuesta introducir el concepto de reutilización.

### Imagen sugerida

Diagrama simple:

Problema

↓

Diseño

↓

Prompt

↓

Resultado

↓

Evaluación

↓

Reutilización

### Referencias

White et al. (2023).

Prompt Pattern Catalog.

:::

---

# ¿Por qué hablar de Prompt Engineering?

La mayoría de los usuarios interactúa con modelos de IA escribiendo instrucciones de manera espontánea:

- "Resume este documento."
- "Escribe un correo."
- "Analiza este contrato."

Este enfoque funciona para tareas individuales, pero presenta limitaciones cuando los modelos de IA forman parte de procesos organizacionales.

## Principales problemas

- Resultados inconsistentes.
- Falta de estandarización.
- Dificultad para reutilizar el conocimiento.
- Ausencia de documentación.
- Dependencia de la experiencia individual.

---

> **Idea clave**

Los prompts improvisados pueden resolver tareas; los prompts diseñados permiten construir procesos.

::: notes

### Objetivo docente

Mostrar que la necesidad del Prompt Engineering surge cuando la IA deja de ser una herramienta personal y pasa a formar parte de procesos organizacionales.

### Actividad sugerida

Solicitar a dos estudiantes que escriban un prompt para resumir un documento.

Comparar ambos prompts.

Discutir por qué son diferentes.

### Imagen sugerida

Dos capturas de ChatGPT mostrando prompts distintos para la misma tarea.

### Referencias

Chip Huyen.

AI Engineering.

Microsoft Learn.

Prompt Engineering.

OpenAI Prompt Engineering Guide.

:::

---

# Del Prompt al Activo de Ingeniería

En Ingeniería de Software no desarrollamos sistemas escribiendo código de manera improvisada.

Aplicamos principios como:

- Arquitectura
- Modularidad
- Documentación
- Versionado
- Pruebas
- Mantenimiento

De forma análoga, un prompt utilizado en un entorno organizacional debe diseñarse siguiendo estos mismos principios.

| Ingeniería de Software | Prompt Engineering |
|-------------------------|--------------------|
| Código | Prompt |
| Función | Plantilla |
| Librería | Biblioteca de Prompts |
| Git | Versionado |
| Testing | Evaluación |
| Refactoring | Optimización |

---

> **Idea clave**

Un prompt puede administrarse como cualquier otro activo de software.

::: notes

### Objetivo docente

Establecer la analogía con la Ingeniería de Software, que servirá como hilo conductor del módulo.

### Aclaración importante

No estamos afirmando que un prompt sea software.

Estamos proponiendo que su gestión puede beneficiarse de las mismas prácticas de ingeniería.

### Imagen sugerida

Comparación entre un repositorio Git y una biblioteca de prompts.

### Referencias

Robert C. Martin.

Clean Architecture.

White et al. (2023).

Prompt Pattern Catalog.

GitHub Documentation.

:::

---

# El nuevo paradigma

## Prompt Engineering como disciplina de ingeniería

Un prompt profesional debe ser:

- Comprensible.
- Reutilizable.
- Parametrizable.
- Documentado.
- Evaluado.
- Versionado.
- Mantenible.

Estos principios serán desarrollados progresivamente durante este módulo.

## Ruta de aprendizaje

**Clase 1**

Diseño de prompts

↓

**Clase 2**

Bibliotecas y reutilización

↓

**Clase 3**

Evaluación y mitigación de riesgos

↓

**Clase 4**

Optimización, gobernanza y PromptOps

---

> **Idea clave**

A partir de este momento comenzaremos a tratar los prompts como activos organizacionales y no como instrucciones aisladas.

::: notes

### Objetivo docente

Cerrar el bloque dejando claro el cambio de paradigma.

### Transición

En el siguiente bloque responderemos una pregunta fundamental:

**¿Cómo está construido un prompt profesional?**

### Imagen sugerida

Diagrama de ciclo de vida de un prompt con las cuatro clases del módulo.

### Referencias

White et al. (2023).

OpenAI Prompt Engineering Guide.

Anthropic Prompt Engineering Best Practices.

:::