# Prompt Evaluation Report

---

# Información General

| Campo | Valor |
|--------|-------|
| Estudiante | |
| Fecha | |
| Versión del Prompt | |
| Tipo de Prompt | ☐ Resumen ☐ Clasificación ☐ Extracción |
| Dominio | |
| Modelo utilizado | ☐ ChatGPT ☐ Claude ☐ Gemini ☐ Otro |
| Objetivo del Prompt | |

---

# Descripción del Prompt

Generar un resumen de clasificacion de una hoja de vida para facilitar la evaluación inicial de candidatos durante un proceso de selección.

La clasificacion debe ser con base en las categorias y subcategorias que la organizacion maneja.



>  `clase02/startet-kit/prompts/clasification-cv.md`

---

```text
 `clase02/startet-kit/prompts/generados/clasification-cv-senior-01.md`
```

---

# Objetivo de la Evaluación

Los objetivos de esta evaluacion son:

- Verificar que el prompt detecta información faltante.
- Evaluar la consistencia de las respuestas.
- Comprobar que no inventa información.
- Analizar si identifica contradicciones.

---

**Respuesta**

```
Verificar que el prompt detecta información faltante.
```

---

# Casos de Prueba

## Caso 1

### Documento utilizado

```
sample-data/hr/cv-backend-senior.md
```

### Objetivo

Verificar el comportamiento esperado utilizando un documento completo.

---

### Resultado obtenido

```
(Resumen)
Observaciones:

La clasificación puede realizarse con alta confianza, ya que el documento contiene evidencia explícita en los tres criterios solicitados: experiencia, tecnologías y liderazgo.
No fue necesario inferir información no presente en el CV.
El perfil está claramente orientado al desarrollo Backend sobre tecnologías Microsoft, con experiencia adicional en arquitectura, DevOps y liderazgo técnico.
```
```
Respuesta completa en:
evaluations/test-results/cv-senior-backend.md
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 5 |
| Completitud | 5 |
| Consistencia | 5 |
| Claridad | 5 |
| Relevancia | 4 |

---

### Problemas encontrados

```
Ninguno.
```

---

### Observaciones

```
En Liderazgo tecnico menciona una cualidad muy generica como es: Diseño de Soluciones.
```

---

## Caso 2

### Documento utilizado

```
clase02/starter-kit/sample-data/hr/cv-backend-incomplete.md
```

### Objetivo

Verificar el manejo de información incompleta.

---

### Resultado obtenido

```
(Resumen)
Observaciones
La información del CV es limitada respecto al nivel de profundidad técnica y el alcance de los proyectos desarrollados.
Tampoco se describen responsabilidades relacionadas con diseño de arquitectura, toma de decisiones técnicas o liderazgo, por lo que no existe evidencia suficiente para clasificar al candidato como Senior.
Sí existe evidencia suficiente para ubicarlo por encima de un perfil Junior, debido a la experiencia profesional acumulada y la progresión de cargos. Por ello, la clasificación Semi Senior se considera la más consistente con la información disponible.
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 4 |
| Completitud | 4 |
| Consistencia | 4 |
| Claridad | 4 |
| Relevancia | 4 |

---

### Problemas encontrados

```
Ninguno
```

---

### Observaciones

```
El documento de CV contiene informacion muy basica.
```

---

## Caso 3

### Documento utilizado

```
clase02/starter-kit/sample-data/hr/cv-backend-contradictory.md
```

### Objetivo

Verificar la detección de inconsistencias.

---

### Resultado obtenido

```
Observaciones
La afirmación de más de 10 años de experiencia no es consistente con la experiencia laboral documentada.
La fecha de graduación (2019) resulta difícil de conciliar con un supuesto historial profesional superior a diez años, aunque por sí sola no demuestra una inconsistencia.
La coexistencia de un cargo Junior durante un período que se superpone con cargos Senior constituye una contradicción significativa.
Debido a estas inconsistencias, no es posible determinar de forma objetiva si el candidato corresponde a las categorías Junior, Semi Senior o Senior únicamente con la información proporcionada. Se recomienda solicitar una versión corregida o validada del CV antes de realizar una clasificación.
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 |
| Completitud | 2 |
| Consistencia | 1 |
| Claridad | 2 |
| Relevancia | 4 |

---

### Problemas encontrados

```
Ninguno
```

---

### Observaciones

```
La informacion generada no corresponde con las condiciones o categorias que han sido definidas en el prompt.
```

---

## Caso 4

### Documento utilizado

```
sample-data/hr/cv-backend-irrelevant-information.md
```

### Objetivo

Evaluar la capacidad del prompt para filtrar información irrelevante.

---

### Resultado obtenido

```
**Observaciones:**

* La afirmación de “más de diez años de experiencia” no está respaldada por la trayectoria laboral detallada.
* Los cargos Senior se superponen con un puesto de Programador Junior entre 2023 y 2025.
* No se especifican tamaño de equipo, personal supervisado, mentorías, evaluaciones de desempeño ni responsabilidad formal sobre colaboradores.
* El liderazgo demostrado es principalmente **técnico**, no necesariamente liderazgo de personas.
* La clasificación final es **Senior**, pero se recomienda validar mediante entrevista la cronología, el alcance real de los proyectos y las funciones ejercidas en cada puesto.
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 1 |
| Completitud | 2 |
| Consistencia | 1 |
| Claridad | 3 |
| Relevancia | 3 |

---

### Problemas encontrados

```
Ninguno
```

---

### Observaciones

```
se corrio el prompt en diferentes modelos (Chatgpt y Gemini) y los resultados fueron muy diferentes.
```

---

## Caso 5

### Documento utilizado

```
sample-data/hr/cv-backend-unstructured.md
```

### Objetivo

Evaluar el comportamiento frente a documentos sin estructura.

---

### Resultado obtenido

```
Justificación:

A pesar de que el documento carece de una estructura formal, contiene información suficiente para evaluar los criterios solicitados.

Experiencia: El candidato acredita experiencia laboral continua desde febrero de 2021 hasta la actualidad, primero desarrollando sistemas web en C# y SQL Server y posteriormente desempeñándose como desarrollador Backend con ASP.NET Core.
Tecnologías: Se evidencian conocimientos y experiencia práctica en tecnologías Backend del ecosistema .NET, incluyendo ASP.NET Core, APIs REST, Entity Framework, SQL Server, Docker, Azure DevOps y participación en proyectos con microservicios y OAuth. También indica que se encuentra aprendiendo Kubernetes.
Liderazgo: No se identifican evidencias de liderazgo técnico, coordinación de equipos, mentoría, revisión de código o responsabilidades de arquitectura. El documento describe únicamente actividades de desarrollo.
```

---

### Evaluación

| Criterio | Puntuación |
|----------|:----------:|
| Exactitud | 4 |
| Completitud | 4 |
| Consistencia | 2 |
| Claridad | 1 |
| Relevancia | 2 |

---

### Problemas encontrados

```
Ninguno
```

---

### Observaciones

```
Muestra mucha informacion, a modo de justificar lo encontrado.
```

---

# Resumen de Resultados

| Caso | Exactitud | Completitud | Consistencia | Claridad | Relevancia |
|------|:---------:|:-----------:|:------------:|:--------:|:----------:|
| Caso 1 | | | | | |
| Caso 2 | | | | | |
| Caso 3 | | | | | |
| Caso 4 | | | | | |
| Caso 5 | | | | | |

---

# Hallazgos Principales

Después de ejecutar todos los casos de prueba, responda las siguientes preguntas.

## ¿Cuál fue el principal problema identificado?

```
Documentos con diferentes formatos, algunas respuestas muy extensas.
```

---

## ¿Qué caso produjo la peor respuesta?

```
El caso 5 del documento sin estructura
```

---

## ¿Qué mejoras considera necesarias?

```
Definir categoria 'No es posible' para evitar que el modelo defina una propia categoria cuando no es posible identificar.
Ajustar la justificacion para que no sea muy extensa.
```

---

# Plan de Mejora

Indique las modificaciones que realizará sobre el prompt antes de generar una nueva versión.

| Mejora propuesta | Justificación |
|------------------|---------------|
| Proponer categoria no existente| Para contar solo con 4 categorias |
| Acortar la justificacion a 3 parrafos o 150 palabras| para que no sea muy extensa la respuesta |
| | |

---

# Conclusión

Complete la siguiente reflexión.

> Después de ejecutar los cinco casos de prueba, considero que el prompt desarrollado:

☐ Está listo para utilizarse.

☐ Requiere mejoras menores.

☐ Requiere una revisión importante antes de utilizarse.

Justifique su respuesta.

```
Todos los casos han generado una respuesta, en algunos casos muy amplia, pero se tiene un resultado que puede ser procesado por un humano.
```