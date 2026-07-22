---
marp: false
---

<!-- ========================================================= -->
<!-- CLASE 2                                                   -->
<!-- BLOQUE I                                                  -->
<!-- De los Prompts Aislados a la Automatización               -->
<!-- ========================================================= -->

---

# Arquitecturas de Prompts para Automatización de Procesos

## Clase 2

### De los Prompts Aislados a la Automatización Basada en Prompts

> **Pregunta guía**
>
> ¿Cómo pasamos de diseñar un buen prompt a automatizar un proceso organizacional completo?

::: notes

### Objetivo docente

Presentar el propósito de la segunda sesión.

Recordar que en la Clase 1 aprendimos a diseñar prompts profesionales.

Hoy aprenderemos a diseñar soluciones compuestas por múltiples prompts.

### Referencias

- White et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.*
- Chip Huyen. *AI Engineering.*

### Imagen sugerida

Un flujo organizacional donde varias tareas humanas son asistidas por distintos modelos de IA.

:::

---

# ¿Por qué un solo prompt no es suficiente?

En una conversación cotidiana, un único prompt puede resolver una tarea.

En una organización, un proceso completo suele requerir múltiples decisiones y múltiples interacciones con la IA.

## Ejemplo

**Proceso de atención de un ticket**

- Clasificar la solicitud.
- Determinar la prioridad.
- Asignar el área responsable.
- Generar una respuesta inicial.
- Registrar el resultado.

> **Idea clave**

Un proceso organizacional rara vez puede automatizarse mediante un único prompt.

::: notes

### Objetivo docente

Mostrar que los procesos organizacionales son secuencias de actividades y no tareas aisladas.

Relacionar este concepto con BPMN y análisis de procesos vistos en módulos anteriores.

### Pregunta para discusión

¿En qué procesos de su organización creen que un único prompt sería insuficiente?

### Imagen sugerida

Diagrama de flujo simple con cinco actividades consecutivas.

### Referencias

- Dumas et al. *Fundamentals of Business Process Management.*
- OMG. *BPMN 2.0 Specification.*

:::

---

# Del Proceso al Conjunto de Prompts

Cada actividad del proceso puede transformarse en un componente especializado.

```text
Recepción del ticket
        │
        ▼
Prompt 1
Clasificar
        │
        ▼
Prompt 2
Priorizar
        │
        ▼
Prompt 3
Asignar
        │
        ▼
Prompt 4
Generar respuesta
```

## Beneficios

- Cada prompt tiene una única responsabilidad.
- Los componentes pueden reutilizarse en distintos procesos.
- Es posible reemplazar o mejorar un prompt sin modificar toda la arquitectura.
- La solución resulta más fácil de mantener y evolucionar.

> **Idea clave**

Es preferible diseñar varios prompts especializados que un único prompt excesivamente complejo.

::: notes

### Objetivo docente

Introducir el concepto de **modularización**.

Relacionarlo con principios de Ingeniería de Software como:

- Responsabilidad Única (Single Responsibility Principle)
- Modularidad
- Reutilización

Enfatizar que la IA también debe diseñarse mediante componentes desacoplados.

### Demostración sugerida

Mostrar dos soluciones para el mismo problema:

**Opción A**

Un único prompt de gran tamaño que intenta:

- clasificar;
- priorizar;
- responder;
- generar un resumen;
- asignar responsables.

**Opción B**

Cuatro prompts independientes, cada uno especializado en una única tarea.

Preguntar al grupo:

> ¿Cuál sería más fácil de mantener dentro de una organización?

### Imagen sugerida

Comparación entre:

**Arquitectura monolítica**

```
+-------------------------------------+
|            Prompt gigante           |
| Clasifica                          |
| Prioriza                           |
| Resume                             |
| Responde                           |
| Asigna                             |
+-------------------------------------+
```

vs.

**Arquitectura modular**

```
+-----------+
| Clasificar|
+-----------+
      │
      ▼
+-----------+
| Priorizar |
+-----------+
      │
      ▼
+-----------+
| Asignar   |
+-----------+
      │
      ▼
+-----------+
| Responder |
+-----------+
```

### Referencias

- Robert C. Martin. *Clean Architecture.*
- Martin Fowler. *Refactoring: Improving the Design of Existing Code.*
- OpenAI. *Prompt Engineering Guide.*

:::

---

# Arquitectura de Automatización Basada en Prompts

Una arquitectura de prompts define:

- Qué tareas automatiza cada prompt.
- Cómo fluye la información entre ellos.
- Qué entradas y salidas utiliza cada componente.
- Cómo se integran dentro de un proceso organizacional.

## Analogía

| Ingeniería de Software | Prompt Engineering |
|-------------------------|--------------------|
| Función | Prompt especializado |
| Módulo | Biblioteca de prompts |
| Pipeline | Flujo de prompts |
| Sistema | Arquitectura de automatización |

> **Idea clave**

Los prompts dejan de ser instrucciones aisladas y pasan a formar parte de una arquitectura de automatización.

::: notes

### Objetivo docente

Presentar el concepto de **Arquitectura de Prompts**.

El estudiante debe comprender que la automatización no consiste únicamente en utilizar un modelo de IA, sino en diseñar un conjunto de componentes coordinados.

Relacionar esta arquitectura con conceptos ya conocidos por los estudiantes:

- BPMN
- Microservicios
- Pipelines CI/CD
- Arquitectura por componentes

### Pregunta para discusión

¿Podría reutilizarse el prompt de clasificación de tickets en otro proceso?

¿Por qué?

### Imagen sugerida

Diagrama por bloques:

```text
               Entrada

                  │

                  ▼

      +---------------------+
      | Prompt Clasificador |
      +---------------------+

                  │

                  ▼

      +---------------------+
      | Prompt Priorizador  |
      +---------------------+

                  │

                  ▼

      +---------------------+
      | Prompt Asignador    |
      +---------------------+

                  │

                  ▼

      +---------------------+
      | Prompt Respuesta    |
      +---------------------+

                  │

                  ▼

              Resultado
```

### Referencias

- Chip Huyen. *AI Engineering.*
- LangChain Documentation (Chains y LCEL).
- Microsoft Prompt Flow Documentation.

:::

---

# Transición al siguiente bloque

Hasta este momento hemos aprendido que:

- Un proceso organizacional está compuesto por múltiples actividades.
- Cada actividad puede convertirse en un prompt especializado.
- Un conjunto de prompts constituye una arquitectura de automatización.

La siguiente pregunta es:

> **¿Cómo diseñamos esos prompts para que puedan reutilizarse en distintos procesos sin volver a escribirlos desde cero?**

En el siguiente bloque estudiaremos la **modularización**, la **parametrización** y el diseño de **Prompt Templates**, que permitirán construir bibliotecas de prompts reutilizables.

::: notes

### Objetivo docente

Cerrar el bloque mostrando la evolución del razonamiento.

Clase 1

```
Prompt Profesional
```

↓

Clase 2

```
Arquitectura de Prompts
```

↓

Bloque siguiente

```
Prompt Templates
```

Esta secuencia prepara el terreno para introducir plantillas, variables y reutilización.

### Imagen sugerida

Vista previa del repositorio:

```text
Enterprise-Prompt-Library/

├── procesos/
├── prompts/
├── templates/
├── variables/
├── ejemplos/
└── README.md
```

### Referencias

- White et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.*
- LangChain Documentation.
- Microsoft Prompt Flow Documentation.

:::