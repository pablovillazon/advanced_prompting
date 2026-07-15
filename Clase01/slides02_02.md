<!-- ========================================================= -->
<!-- BLOQUE II                                                 -->
<!-- Anatomía de un Prompt Profesional                         -->
<!-- ========================================================= -->

---

# Anatomía de un Prompt Profesional

## Todo prompt tiene una arquitectura

Cuando diseñamos software no comenzamos escribiendo código.

Primero definimos una arquitectura.

Del mismo modo, un prompt profesional no se construye agregando instrucciones al azar, sino organizando información mediante componentes claramente definidos.

---

### Componentes principales

- Rol
- Contexto
- Objetivo
- Restricciones
- Formato de salida
- Variables de entrada *(opcional)*
- Ejemplos *(cuando sean necesarios)*

> **Idea clave**

La calidad de un prompt depende más de su estructura que de su longitud.

::: notes

### Objetivo docente

Introducir el concepto de arquitectura de un prompt.

Evitar presentar los componentes como una simple lista.

Enfatizar que representan decisiones de diseño.

### Imagen sugerida

Diagrama en bloques similar a una arquitectura de software.

```
                Prompt

        +------------------+

        Rol

        Contexto

        Objetivo

        Restricciones

        Formato

        Variables

        Ejemplos
```

### Referencias

OpenAI Prompt Engineering Guide.

Anthropic Prompt Design Best Practices.

Microsoft Learn - Prompt Engineering.

:::
---

# Componente 1: Definir el Rol

El rol establece la perspectiva desde la cual el modelo debe responder.

No modifica el conocimiento del modelo, pero orienta el tipo de razonamiento y el estilo de la respuesta.

## Ejemplo

❌ Resume este documento.

✅ Actúa como un analista financiero y resume el siguiente informe para un comité ejecutivo.

---

### Buenas prácticas

- Asignar roles específicos.
- Evitar roles ambiguos.
- Utilizar roles coherentes con el proceso organizacional.

---

> **Idea clave**

El rol proporciona contexto funcional al modelo.

::: notes

### Objetivo docente

Explicar que el rol ayuda a orientar el comportamiento esperado del modelo, especialmente en tareas organizacionales.

### Demostración

Ejecutar el mismo prompt utilizando tres roles diferentes:

- abogado
- médico
- gerente financiero

Comparar los resultados.

### Imagen sugerida

Diagrama mostrando un mismo problema abordado desde distintos roles profesionales.

### Referencias

White et al. (2023)

Persona Pattern.

Anthropic Documentation.

:::
---

# Componentes 2 y 3: Contexto y Objetivo

## Contexto

Describe la situación en la que se desarrolla la tarea.

Permite reducir ambigüedades.

## Objetivo

Define exactamente qué debe realizar el modelo.

---

## Ejemplo

**Contexto**

La empresa recibe aproximadamente 300 solicitudes de soporte diariamente.

**Objetivo**

Clasificar cada solicitud según prioridad y departamento responsable.

---

### Recomendaciones

- Incluir únicamente el contexto relevante.
- Formular un objetivo único y específico.
- Evitar combinar múltiples tareas en un mismo prompt.

---

> **Idea clave**

Un buen contexto responde al "por qué".

Un buen objetivo responde al "qué".

::: notes

### Objetivo docente

Diferenciar claramente contexto y objetivo.

Muchos estudiantes los mezclan.

### Actividad rápida

Pedir a los estudiantes identificar el contexto y el objetivo en un ejemplo proyectado.

### Imagen sugerida

Diagrama simple:

Contexto

↓

Objetivo

↓

Respuesta

### Referencias

Google Prompt Design Guide.

OpenAI Documentation.

:::
---

# Componentes 4 y 5: Restricciones y Formato

## Restricciones

Definen los límites del comportamiento esperado.

Ejemplos:

- No inventar información.
- Utilizar únicamente las categorías proporcionadas.
- No emitir opiniones.

---

## Formato

Define cómo debe entregarse la respuesta.

Ejemplos:

- Tabla
- Lista
- Markdown
- JSON
- XML

---

### Ejemplo

Devuelve únicamente la siguiente estructura:

```json
{
  "categoria":"",
  "prioridad":"",
  "responsable":"",
  "justificacion":""
}
```

---

> **Idea clave**

Las restricciones controlan el comportamiento.

El formato facilita la integración con otros sistemas.

::: notes

### Objetivo docente

Relacionar el formato con procesos automatizados.

Un JSON puede ser consumido directamente por una API.

### Imagen sugerida

Comparación entre:

Texto libre

↓

JSON

↓

Sistema de automatización

### Referencias

OpenAI Structured Outputs.

Microsoft Prompt Flow.

LangChain Output Parsers.

:::
---

# Construyendo un Prompt Profesional

A continuación se presenta un ejemplo que integra todos los componentes estudiados.

```text
Rol:
Eres un analista senior de soporte técnico.

Contexto:
La empresa procesa cientos de solicitudes diariamente.

Objetivo:
Clasificar la solicitud según prioridad y área responsable.

Restricciones:
No inventes información.
Utiliza únicamente las categorías definidas.

Formato:
Devuelve la respuesta en formato JSON.

Entrada:
{{mensaje}}
```

---

## Reflexión

Observe que el prompt no es necesariamente más largo.

Es simplemente más estructurado.

> **Idea clave**

La arquitectura transforma un conjunto de instrucciones en una especificación reutilizable.

::: notes

### Objetivo docente

Cerrar el bloque mostrando que todos los componentes forman parte de un único diseño.

### Transición

En el siguiente bloque aprenderemos que existen patrones reutilizables para construir este tipo de prompts de forma sistemática.

### Imagen sugerida

El prompt mostrado como un diagrama por capas donde cada componente aparece con un color diferente.

### Referencias

White et al. (2023)

Prompt Pattern Catalog.

OpenAI Prompt Engineering Guide.

Anthropic Best Practices.

:::