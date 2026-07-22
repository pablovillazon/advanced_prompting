<!-- ========================================================= -->
<!-- CLASE 2                                                   -->
<!-- BLOQUE III                                                -->
<!-- Patrones de Diseño para Prompt Engineering                -->
<!-- ========================================================= -->

---

# Patrones de Diseño en Prompt Engineering

## Del Prompt Funcional al Prompt Robusto

Hasta este momento hemos aprendido a:

- Diseñar prompts profesionales.
- Modularizar procesos.
- Construir plantillas reutilizables.

La siguiente pregunta es:

> **¿Cómo mejoramos sistemáticamente un prompt para hacerlo más preciso, consistente e integrable?**

Los **Prompt Patterns** representan soluciones reutilizables a problemas frecuentes de diseño.

> **Idea clave**

Un patrón no es una receta; es una solución probada para un problema recurrente.

::: notes

### Objetivo docente

Introducir el concepto de patrón de diseño, estableciendo la analogía con la Ingeniería de Software.

Explicar que no aprenderemos una lista de patrones, sino a identificar qué problema resuelve cada uno.

### Referencias

- White, J. et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.*
- Gamma, E., et al. *Design Patterns: Elements of Reusable Object-Oriented Software.*

### Imagen sugerida

Dos columnas:

Problema → Patrón

:::

---

# Problema 1: El modelo necesita contexto

Cuando el modelo desconoce el contexto o la función que debe desempeñar, las respuestas suelen ser genéricas o inconsistentes.

## Solución: Persona Pattern

Asignar explícitamente un rol o identidad especializada.

### Ejemplo

```text
Actúa como un Analista Senior de Recursos Humanos con experiencia en selección de personal para empresas tecnológicas.
```

## Beneficios

- Respuestas más especializadas.
- Mayor coherencia con el dominio.
- Mejor alineación con el objetivo del proceso.

> **Idea clave**

El rol proporciona contexto y orienta el razonamiento del modelo.

::: notes

### Objetivo docente

Explicar que el rol no "convierte" al modelo en un experto, sino que orienta el tipo de respuesta esperada.

### Imagen sugerida

Comparación entre una respuesta genérica y otra producida tras asignar un rol.

### Referencias

- OpenAI. *Prompt Engineering Guide.*
- Anthropic. *Prompt Engineering Best Practices.*

:::

---

# Problema 2: Las respuestas son inconsistentes

Ante solicitudes similares, el modelo puede responder con formatos o criterios diferentes.

## Solución: Few-Shot Pattern

Proporcionar ejemplos representativos antes de la tarea principal.

### Ejemplo

```text
Ejemplo 1

CV: Ingeniero de Software con 5 años en .NET

Clasificación: Backend Senior

---

Ejemplo 2

CV: Licenciado en Administración con experiencia en ventas

Clasificación: Ejecutivo Comercial

---

Ahora clasifica el siguiente perfil.
```

## Beneficios

- Mayor consistencia.
- Menor ambigüedad.
- Mejor desempeño en tareas de clasificación.

> **Idea clave**

Los ejemplos enseñan al modelo el comportamiento esperado sin necesidad de modificar el modelo.

::: notes

### Objetivo docente

Mostrar que el modelo aprende del contexto proporcionado en el prompt.

### Referencias

- Brown, T. et al. (2020). *Language Models are Few-Shot Learners.*
- White et al. (2023).

:::

---

# Problema 3: Necesitamos integrar la IA con otros sistemas

Las respuestas en lenguaje natural son difíciles de consumir por aplicaciones, APIs o flujos automatizados.

## Solución: Output Schema Pattern

Definir explícitamente la estructura de salida.

### Ejemplo

```json
{
  "nombre": "",
  "perfil": "",
  "experiencia": "",
  "nivel": "",
  "recomendacion": ""
}
```

## Beneficios

- Facilita la integración con sistemas externos.
- Reduce errores de interpretación.
- Permite automatizar el procesamiento posterior.

> **Idea clave**

Un esquema de salida convierte la respuesta del modelo en un componente interoperable.

::: notes

### Objetivo docente

Relacionar este patrón con APIs, RPA y flujos de automatización.

### Referencias

- OpenAI Structured Outputs.
- Microsoft Prompt Flow Documentation.
- LangChain Output Parsers.

:::

---

# Combinando Patrones

Los patrones no se utilizan de forma aislada.

Una solución robusta suele combinar varios de ellos.

```text
Persona Pattern
        │
        ▼
Few-Shot Pattern
        │
        ▼
Template Pattern
        │
        ▼
Output Schema Pattern
```

## Reflexión

Cada patrón resuelve un problema distinto.

La calidad del prompt depende de seleccionar el patrón adecuado para cada situación.

> **Idea clave**

Diseñar prompts consiste en tomar decisiones de arquitectura, no únicamente en escribir instrucciones.

::: notes

### Objetivo docente

Cerrar el bloque reforzando la idea de que los patrones son herramientas de diseño.

Preparar la transición al Caso Guiado 3.

### Referencias

- White et al. (2023).
- Chip Huyen. *AI Engineering.*

:::