# Casos Guiados
# Clase 2 – Arquitecturas de Prompts para Automatización de Procesos

---

# Objetivo

Los siguientes casos guiados tienen como propósito mostrar, paso a paso, cómo transformar un problema organizacional en una solución basada en una arquitectura de prompts reutilizable.

Cada caso será desarrollado por el docente durante la sesión presencial y servirá como base para los laboratorios y el proyecto asincrónico.

---

# Caso Guiado 1
## De un Prompt Específico a una Plantilla Reutilizable

### Objetivo del caso

Comprender por qué un prompt diseñado para un único escenario debe transformarse en una plantilla reutilizable cuando comienza a utilizarse dentro de una organización.

---

## Escenario

La empresa **Andes Business Group** ha comenzado un proceso de digitalización del área de Recursos Humanos.

Actualmente los analistas utilizan IA para resumir hojas de vida antes de las entrevistas.

Inicialmente se diseñó el siguiente prompt.

```text
Actúa como un analista de Recursos Humanos.

Resume la siguiente hoja de vida en un máximo de 150 palabras.

CV:

<documento>
```

Después de varias semanas aparecen nuevas necesidades.

Ahora también desean resumir:

- perfiles de LinkedIn;
- cartas de presentación;
- evaluaciones de desempeño;
- informes de capacitación.

El equipo comienza a copiar y modificar el mismo prompt para cada nuevo caso.

---

# Problema

Cada nueva tarea genera una nueva versión del mismo prompt.

Esto provoca:

- duplicación de instrucciones;
- mayor esfuerzo de mantenimiento;
- inconsistencias entre versiones;
- dificultad para reutilizar el conocimiento.

---

# Procedimiento

## Paso 1

Identificar qué partes del prompt permanecen constantes.

Ejemplo:

- El rol.
- La tarea de resumir.
- La estructura del resultado.

---

## Paso 2

Identificar qué elementos cambian entre un escenario y otro.

Ejemplo:

- tipo de documento;
- audiencia;
- longitud del resumen;
- idioma;
- formato de salida.

---

## Paso 3

Convertir esos elementos en variables.

```text
{{rol}}

{{documento}}

{{audiencia}}

{{idioma}}

{{longitud}}

{{formato}}
```

---

## Paso 4

Construir una plantilla reutilizable.

```text
Actúa como {{rol}}.

Resume el siguiente documento.

Audiencia:
{{audiencia}}

Idioma:
{{idioma}}

Longitud máxima:
{{longitud}}

Formato:
{{formato}}

Documento:

{{documento}}
```

---

# Producto esperado

Una única plantilla reutilizable capaz de utilizarse en diferentes procesos sin modificar la lógica principal.

Ejemplo de utilización.

| Documento | Audiencia | Longitud |
|------------|-----------|-----------|
| Hoja de vida | Gerente | 150 palabras |
| Perfil LinkedIn | Reclutador | 120 palabras |
| Carta de presentación | Comité | 200 palabras |
| Evaluación de desempeño | Director | 300 palabras |

---

# Discusión

Responder en conjunto.

- ¿Qué información se convirtió en variable?
- ¿Qué ventajas ofrece la parametrización?
- ¿Qué ocurriría si mañana cambia el formato de salida?

---

# Concepto clave

Una plantilla separa la lógica del prompt de los datos específicos del proceso.

Esta separación facilita la reutilización y el mantenimiento.

---

# Caso Guiado 2
## Diseñando una Arquitectura de Prompts

### Objetivo del caso

Comprender que la automatización de procesos requiere múltiples prompts especializados en lugar de un único prompt monolítico.

---

## Escenario

El área de Atención al Cliente recibe cientos de solicitudes diariamente.

Actualmente un operador realiza manualmente las siguientes actividades.

1. Leer el ticket.
2. Clasificar la solicitud.
3. Asignar prioridad.
4. Identificar el departamento responsable.
5. Redactar una respuesta inicial.

La empresa desea automatizar este proceso mediante IA Generativa.

---

# Problema

Un único prompt que intente realizar todas las tareas resulta difícil de mantener y reutilizar.

---

# Procedimiento

## Paso 1

Identificar las actividades del proceso.

```text
Recepción del ticket

↓

Clasificación

↓

Priorización

↓

Asignación

↓

Respuesta inicial
```

---

## Paso 2

Transformar cada actividad en un prompt especializado.

```text
Prompt 1

Clasificar Ticket
```

↓

```text
Prompt 2

Asignar Prioridad
```

↓

```text
Prompt 3

Determinar Área Responsable
```

↓

```text
Prompt 4

Generar Respuesta Inicial
```

---

## Paso 3

Organizar los prompts dentro de una arquitectura.

```text
Cliente

↓

Prompt 1

↓

Prompt 2

↓

Prompt 3

↓

Prompt 4

↓

Resultado
```

---

# Producto esperado

Cada equipo deberá construir una arquitectura similar para el proceso asignado durante el laboratorio.

La arquitectura deberá identificar:

- las actividades del proceso;
- los prompts necesarios;
- el flujo de información;
- las entradas y salidas principales.

---

# Organización del repositorio

```text
Enterprise-Prompt-Library/

├── prompts/

│   └── support/

│       classify-ticket.md

│       prioritize-ticket.md

│       assign-area.md

│       generate-response.md

│

├── templates/

├── ejemplos/

└── README.md
```

---

# Discusión

Responder en grupo.

- ¿Podría un mismo prompt utilizarse en diferentes procesos?
- ¿Qué ventajas ofrece dividir el proceso en componentes?
- ¿Qué componente sería más sencillo modificar en el futuro?

---

# Concepto clave

Una arquitectura basada en prompts está formada por múltiples componentes especializados que colaboran para automatizar un proceso organizacional.

Los prompts dejan de ser instrucciones aisladas y se convierten en activos reutilizables dentro de una biblioteca organizacional.

---

# Relación con los Laboratorios

## Laboratorio 1

Cada equipo transformará un prompt específico en una plantilla reutilizable.

---

## Laboratorio 2

Cada equipo diseñará la arquitectura de prompts para un proceso organizacional diferente.

---

## Laboratorio Asincrónico

Cada estudiante ampliará su **Enterprise Prompt Library** incorporando:

- plantillas reutilizables;
- variables documentadas;
- arquitectura del proceso;
- documentación técnica;
- ejemplos de uso.

---

# Bibliografía recomendada

## Ingeniería de Software

- Martin, R. C. *Clean Architecture.*
- Hunt, A., & Thomas, D. *The Pragmatic Programmer.*
- Fowler, M. *Refactoring.*

---

## Prompt Engineering

- White, J., et al. (2023). *A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT.*
- OpenAI. *Prompt Engineering Guide.*
- Anthropic. *Prompt Engineering Best Practices.*

---

## Automatización y Arquitectura

- Chip Huyen. *AI Engineering.*
- LangChain Documentation – Prompt Templates.
- Microsoft Prompt Flow Documentation.
- Dumas, M., et al. *Fundamentals of Business Process Management.*