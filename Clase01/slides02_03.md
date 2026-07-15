<!-- ========================================================= -->
<!-- BLOQUE III                                                -->
<!-- Prompt Patterns                                           -->
<!-- ========================================================= -->

---

# Prompt Patterns

## Reutilizando soluciones para problemas recurrentes

En Ingeniería de Software, un **patrón de diseño** documenta una solución reutilizable para un problema que aparece con frecuencia.

El Prompt Engineering adopta la misma filosofía.

Un **Prompt Pattern** describe una estrategia que puede aplicarse repetidamente para mejorar el comportamiento de un modelo de lenguaje en determinados escenarios.

---

### ¿Por qué utilizar patrones?

- Reducen la improvisación.
- Favorecen la reutilización.
- Facilitan el mantenimiento.
- Mejoran la consistencia.
- Permiten documentar decisiones de diseño.

> **Idea clave**

Un Prompt Pattern no indica *qué* escribir; indica *cómo estructurar* una solución.

::: notes

### Objetivo docente

Relacionar Prompt Engineering con los Design Patterns de la Ingeniería de Software.

No presentar los patrones como "trucos".

Presentarlos como soluciones reutilizables.

### Imagen sugerida

Comparación:

Design Patterns (Software)

↓

Prompt Patterns (LLM)

### Referencias

White et al. (2023)

*A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.*

Gamma et al. (1994)

*Design Patterns: Elements of Reusable Object-Oriented Software.*

:::
---

# Cuatro Prompt Patterns Fundamentales

Durante esta clase utilizaremos cuatro patrones ampliamente adoptados en aplicaciones empresariales.

| Patrón | Propósito |
|---------|-----------|
| **Persona Pattern** | Define el rol desde el cual responde el modelo. |
| **Specification Pattern** | Establece reglas y restricciones explícitas. |
| **Template Pattern** | Convierte el prompt en una plantilla reutilizable. |
| **Output Schema Pattern** | Define una estructura de salida consistente. |

---

### Observación

Estos patrones pueden utilizarse de manera independiente o combinarse dentro de un mismo prompt.

> **Idea clave**

Los mejores prompts suelen combinar varios patrones simultáneamente.

::: notes

### Objetivo docente

Presentar únicamente los patrones que serán utilizados durante el laboratorio.

Los demás patrones del catálogo podrán mencionarse brevemente, pero no desarrollarse en profundidad.

### Imagen sugerida

Diagrama de capas donde cada patrón aporta un componente diferente al diseño del prompt.

### Referencias

White et al. (2023)

OpenAI Prompt Engineering Guide.

Anthropic Documentation.

:::
---

# Ejemplo: Evolución de un Prompt

## Versión 1 — Prompt improvisado

```
Clasifica el siguiente correo electrónico.
```

---

## Versión 2 — Aplicando Prompt Patterns

```
Rol:
Eres un analista senior de soporte técnico.

Objetivo:
Clasificar la solicitud según prioridad y área responsable.

Restricciones:
Utiliza únicamente las categorías definidas.

Formato:
Devuelve la respuesta en formato JSON.

Entrada:
{{mensaje}}
```

---

### Reflexión

El cambio no consiste en agregar más texto.

Consiste en organizar mejor la información.

> **Idea clave**

Los Prompt Patterns convierten instrucciones aisladas en componentes reutilizables.

::: notes

### Objetivo docente

Mostrar que los patrones mejoran la estructura del prompt.

No necesariamente incrementan su longitud.

### Demostración

Ejecutar ambas versiones utilizando el mismo correo electrónico.

Comparar:

- claridad;
- consistencia;
- facilidad de reutilización.

### Imagen sugerida

Comparación lado a lado de ambos prompts y sus respectivas respuestas.

### Referencias

White et al. (2023)

Prompt Pattern Catalog.

OpenAI Best Practices.

:::
---

# Cierre de la sesión

Durante esta clase hemos recorrido el primer nivel del Prompt Engineering profesional.

## Hemos aprendido que:

- Un prompt puede diseñarse como un activo de ingeniería.
- Todo prompt posee una arquitectura.
- Existen patrones reutilizables para resolver problemas frecuentes.
- La documentación y reutilización forman parte del ciclo de vida del prompt.

---

## A continuación

Aplicaremos estos conceptos desarrollando una biblioteca inicial de prompts para un proceso organizacional.

Esta actividad servirá como base para las siguientes clases del módulo.

> **Idea clave**

Los prompts no se improvisan; se diseñan, documentan y evolucionan.

::: notes

### Objetivo docente

Preparar la transición hacia la práctica guiada.

Explicar que el laboratorio utilizará exactamente los cuatro patrones estudiados.

### Imagen sugerida

Vista previa del repositorio:

Enterprise Prompt Library

con el archivo:

classify-ticket.md

### Referencias

White et al. (2023)

Prompt Pattern Catalog.

OpenAI Prompt Engineering Guide.

GitHub Documentation.

:::