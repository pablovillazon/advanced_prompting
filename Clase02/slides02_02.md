<!-- ========================================================= -->
<!-- CLASE 2                                                   -->
<!-- BLOQUE II                                                 -->
<!-- Modularización y Parametrización                          -->
<!-- ========================================================= -->

---

# ¿Por qué modularizar un Prompt?

Cuando un prompt comienza a utilizarse en distintos procesos organizacionales, aparece un problema:

> **La duplicación de instrucciones.**

Cada modificación obliga a editar múltiples versiones del mismo prompt.

## Ejemplo

Departamento de RRHH:

```
Resume esta hoja de vida.
```

Departamento Comercial:

```
Resume este perfil de cliente.
```

Departamento Jurídico:

```
Resume este contrato.
```

Aunque cambian los documentos, la estructura del prompt es prácticamente la misma.

> **Idea clave**

La duplicación incrementa el costo de mantenimiento y dificulta la evolución de una biblioteca de prompts.

::: notes

### Objetivo docente

Introducir el problema de la duplicación.

Relacionarlo con el principio **DRY (Don't Repeat Yourself)** utilizado en Ingeniería de Software.

### Pregunta para discusión

¿Cuántas versiones distintas del mismo prompt existirían en una organización con 30 departamentos?

### Imagen sugerida

Tres documentos distintos conectados a tres prompts casi idénticos.

### Referencias

- Hunt, A. & Thomas, D. *The Pragmatic Programmer.*
- Robert C. Martin. *Clean Architecture.*
- White et al. (2023). *Prompt Pattern Catalog.*

:::

---

# De la Duplicación a la Reutilización

En Ingeniería de Software resolvemos la duplicación mediante funciones y componentes reutilizables.

En Prompt Engineering aplicamos el mismo principio mediante **Prompt Templates**.

## Comparación

| Prompt fijo | Prompt reutilizable |
|-------------|---------------------|
| Diseñado para un único caso | Diseñado para múltiples escenarios |
| Difícil de modificar | Fácil de mantener |
| Requiere copiar y pegar | Se reutiliza mediante parámetros |

> **Idea clave**

Un Prompt Template separa la lógica del contenido específico.

::: notes

### Objetivo docente

Presentar el concepto de plantilla como una solución de ingeniería y no como una característica de una herramienta.

### Imagen sugerida

Diagrama:

```
Plantilla

      │

      ▼

Documento A

Documento B

Documento C
```

### Referencias

- LangChain Documentation – Prompt Templates.
- DSPy Documentation (Programación declarativa de prompts).

:::

---

# Parametrización mediante Variables

Una plantilla se adapta a diferentes escenarios reemplazando valores específicos por variables.

## Ejemplo

```text
Actúa como {{rol}}.

Resume el siguiente documento.

Audiencia:
{{audiencia}}

Formato:
{{formato}}

Longitud máxima:
{{longitud}}

Documento:
{{documento}}
```

## Variables comunes

- `{{rol}}`
- `{{documento}}`
- `{{audiencia}}`
- `{{idioma}}`
- `{{formato}}`
- `{{longitud}}`

> **Idea clave**

Las variables permiten reutilizar la misma plantilla en distintos procesos sin modificar su estructura.

::: notes

### Objetivo docente

Explicar que las variables representan puntos de configuración y no cambios en la lógica del prompt.

### Demostración

Sustituir únicamente la variable `{{audiencia}}` y comparar cómo cambia la respuesta del modelo.

### Imagen sugerida

Una plantilla central alimentada por diferentes conjuntos de parámetros.

### Referencias

- LangChain Prompt Templates.
- Microsoft Prompt Flow Documentation.
- OpenAI Prompt Engineering Guide.

:::

---

# Diseñando una Plantilla Reutilizable

Una buena plantilla debe definir claramente:

- El propósito del prompt.
- Las variables requeridas.
- Las variables opcionales.
- El formato esperado de la respuesta.
- Las restricciones aplicables.

## Ejemplo de estructura

```text
Nombre:
Resumen Ejecutivo

Variables requeridas:
- documento
- audiencia

Variables opcionales:
- idioma
- longitud
- formato

Salida:
Markdown
```

> **Idea clave**

Una plantilla reutilizable debe documentarse igual que cualquier otro componente de software.

::: notes

### Objetivo docente

Introducir la importancia de documentar las plantillas.

Relacionar esta práctica con APIs, funciones o componentes reutilizables.

### Imagen sugerida

Plantilla documentada dentro del repositorio:

```text
templates/

summary-template.md
```

### Referencias

- GitHub Documentation.
- White et al. (2023).
- LangChain Documentation.

:::

---

# Hacia una Biblioteca de Plantillas

Cuando varias plantillas se organizan de manera estructurada, obtenemos una **Biblioteca de Prompts**.

```text
Enterprise-Prompt-Library/

├── prompts/
├── templates/
├── variables/
├── ejemplos/
└── README.md
```

Cada plantilla puede reutilizarse en distintos procesos organizacionales.

> **Idea clave**

La reutilización comienza cuando los prompts dejan de pertenecer a una persona y pasan a formar parte del conocimiento compartido de la organización.

::: notes

### Objetivo docente

Preparar la transición hacia el siguiente bloque.

Mostrar que las plantillas constituyen el punto de partida para construir arquitecturas de automatización.

### Pregunta para reflexión

¿Qué ventajas tendría compartir una biblioteca de prompts entre diferentes equipos de una organización?

### Imagen sugerida

Repositorio GitHub mostrando carpetas de plantillas y prompts reutilizables.

### Referencias

- White et al. (2023).
- GitHub Documentation.
- Chip Huyen. *AI Engineering.*

:::