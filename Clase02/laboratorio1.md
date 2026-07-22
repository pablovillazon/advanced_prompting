# Laboratorio 1
# Arquitectura de Prompts para un Proceso Organizacional

**Clase:** 2

**Duración:** 20–25 minutos

**Modalidad:** Trabajo colaborativo (equipos o individual)

---

# Objetivo

Aplicar los conceptos de modularización y arquitectura de prompts para descomponer un proceso organizacional en un conjunto de componentes reutilizables.

Al finalizar este laboratorio el estudiante será capaz de:

- Analizar un proceso organizacional.
- Identificar tareas susceptibles de automatización mediante IA Generativa.
- Descomponer un proceso en múltiples prompts especializados.
- Diseñar un flujo de interacción entre prompts.
- Documentar una arquitectura de automatización.

---

# Contexto

En la clase anterior diseñaron prompts profesionales para automatizar tareas específicas.

En esta sesión aprenderán que una organización rara vez utiliza un único prompt.

Los procesos empresariales están compuestos por múltiples actividades y cada una puede automatizarse mediante un prompt especializado.

Su tarea consiste en transformar un proceso organizacional en una **Arquitectura de Prompts**.

---

# Organización de equipos

Forme equipos de **1 o 2 integrantes**.

Cada equipo trabajará sobre un proceso diferente.

---

# Escenarios

## Equipo 1 – Recursos Humanos

Proceso de selección de personal.

Actividades actuales:

- Recepción de hojas de vida.
- Clasificación por perfil.
- Resumen del candidato.
- Generación de preguntas para entrevista.
- Elaboración de informe para el reclutador.

---

## Equipo 2 – Atención al Cliente

Proceso de gestión de tickets.

Actividades actuales:

- Recepción del ticket.
- Clasificación.
- Priorización.
- Asignación al área correspondiente.
- Respuesta inicial al cliente.

---

## Equipo 3 – Ventas

Proceso de gestión de prospectos.

Actividades actuales:

- Recepción del formulario.
- Clasificación del cliente.
- Identificación del nivel de interés.
- Generación de propuesta inicial.
- Elaboración de correo de seguimiento.

---

## Equipo 4 – Administración

Proceso de gestión documental.

Actividades actuales:

- Recepción del documento.
- Clasificación documental.
- Identificación del área responsable.
- Extracción de información relevante.
- Elaboración del resumen ejecutivo.

---

# Desarrollo

## Paso 1 – Comprender el proceso

Analicen el proceso asignado.

Respondan las siguientes preguntas.

- ¿Cuál es el objetivo del proceso?
- ¿Qué información recibe?
- ¿Qué resultado produce?
- ¿Qué actividades realiza actualmente una persona?

Tiempo sugerido: **5 minutos**.

---

## Paso 2 – Identificar las tareas automatizables

Completen la siguiente tabla.

| Actividad | ¿Puede automatizarse? | ¿Requiere un Prompt? |
|------------|----------------------|----------------------|
| | | |
| | | |
| | | |

Tiempo sugerido: **5 minutos**.

---

## Paso 3 – Diseñar la arquitectura

Transformen cada actividad automatizable en un prompt independiente.

Ejemplo.

```text
Solicitud

↓

Prompt 1
Clasificar

↓

Prompt 2
Priorizar

↓

Prompt 3
Asignar

↓

Prompt 4
Generar respuesta

↓

Resultado
```

Tiempo sugerido: **10 minutos**.

---

## Paso 4 – Documentar la arquitectura

Creen un archivo llamado:

```text
arquitectura.md
```

Utilicen la siguiente estructura.

```markdown
# Arquitectura del Proceso

## Nombre del proceso

...

## Objetivo

...

## Flujo

Proceso

↓

Prompt 1

↓

Prompt 2

↓

Prompt 3

↓

Resultado

## Prompts identificados

| Prompt | Objetivo |
|---------|----------|
| Prompt 1 | |
| Prompt 2 | |
| Prompt 3 | |
| Prompt 4 | |

## Entradas principales

-

-

## Salidas esperadas

-

-
```

---

# Producto esperado

Cada equipo deberá entregar un archivo:

```text
arquitectura.md
```

El documento deberá contener:

- Nombre del proceso.
- Objetivo.
- Diagrama del flujo de prompts.
- Lista de prompts identificados.
- Entradas del proceso.
- Salidas del proceso.

No es necesario implementar los prompts en esta etapa.

El objetivo es diseñar la arquitectura.

---

# Presentación

Cada equipo dispondrá de **3 minutos** para presentar.

La exposición deberá responder las siguientes preguntas.

1. ¿Cuál es el proceso seleccionado?

2. ¿Qué tareas decidieron automatizar?

3. ¿Cuántos prompts identificaron?

4. ¿Por qué eligieron esa arquitectura?

---

# Discusión

Después de todas las presentaciones se responderán las siguientes preguntas.

- ¿Todos los equipos diseñaron el mismo número de prompts?
- ¿Qué actividad fue más difícil de automatizar?
- ¿Qué ventajas ofrece dividir el proceso en componentes?
- ¿Qué riesgos tendría utilizar un único prompt para todo el proceso?

---

# Entregables

Cada equipo entregará:

- `arquitectura.md`

---

# Criterios de evaluación

| Criterio | Puntaje |
|----------|---------|
| Comprensión del proceso | 2 |
| Identificación de tareas automatizables | 2 |
| Diseño de la arquitectura | 3 |
| Claridad del flujo | 2 |
| Documentación | 1 |

**Total:** **10 puntos**

---

# Conclusión

Este laboratorio representa el primer paso para transformar una colección de prompts independientes en una **Arquitectura Organizacional de Automatización**.

En la siguiente actividad se refinarán estos componentes mediante plantillas reutilizables, variables y documentación estandarizada, integrándolos progresivamente en la **Enterprise Prompt Library** desarrollada durante el módulo.