# Laboratorio Asincrónico
# Proyecto Integrador – Fase 1
## Construcción de una Biblioteca Organizacional de Prompts

**Módulo:** Prompt Engineering Avanzado

**Clase:** 1

**Modalidad:** Individual

**Tiempo estimado:** 4 a 6 horas

---

# Introducción

En una organización, los prompts representan conocimiento reutilizable.

Al igual que el código fuente, deben diseñarse, documentarse, mantenerse y evolucionar.

Durante este módulo construiremos progresivamente una **Biblioteca Organizacional de Prompts** (*Enterprise Prompt Library*), aplicando principios de ingeniería para garantizar su reutilización, calidad y mantenibilidad.

En esta primera fase usted desarrollará la versión inicial de dicha biblioteca.

---

# Objetivo

Diseñar y documentar una colección de prompts reutilizables para automatizar tareas de un proceso organizacional utilizando una metodología estandarizada.

Al finalizar esta actividad usted será capaz de:

- Analizar un proceso organizacional.
- Identificar oportunidades de automatización mediante IA Generativa.
- Diseñar prompts reutilizables.
- Aplicar Prompt Patterns básicos.
- Documentar prompts siguiendo una plantilla profesional.
- Construir una biblioteca organizada de prompts.

---

# Escenario

La empresa ficticia **Andes Business Group** iniciará un proyecto de incorporación de Inteligencia Artificial Generativa en sus procesos administrativos.

Cada profesional del equipo ha sido asignado a un único departamento.

Su responsabilidad consiste en desarrollar la primera versión de la biblioteca oficial de prompts para dicho departamento.

---

# Departamentos disponibles

Seleccione únicamente **uno** de los siguientes departamentos.

- Recursos Humanos
- Ventas
- Administración
- Atención al Cliente
- Finanzas

Toda la actividad deberá desarrollarse exclusivamente sobre el departamento seleccionado.

---

# Actividades

Su biblioteca deberá contener **cinco prompts diferentes**, orientados a automatizar tareas reales del departamento elegido.

Los cinco prompts deben corresponder a procesos distintos.

---

## Ejemplo

### Recursos Humanos

- Clasificar hojas de vida.
- Generar preguntas para entrevistas.
- Elaborar retroalimentación de entrevistas.
- Resumir evaluaciones de desempeño.
- Redactar cartas de contratación.

---

### Ventas

- Clasificar prospectos.
- Generar propuestas comerciales.
- Resumir reuniones con clientes.
- Elaborar correos de seguimiento.
- Analizar objeciones comerciales.

---

### Administración

- Clasificar documentos.
- Resumir actas de reunión.
- Generar memorandos.
- Extraer tareas pendientes.
- Redactar informes administrativos.

---

### Atención al Cliente

- Clasificar tickets.
- Priorizar solicitudes.
- Generar respuestas iniciales.
- Resumir conversaciones.
- Detectar incidentes críticos.

---

### Finanzas

- Clasificar comprobantes.
- Resumir reportes financieros.
- Analizar gastos.
- Detectar inconsistencias.
- Elaborar reportes ejecutivos.

---

# Requisitos de cada prompt

Cada prompt deberá contener, como mínimo, los siguientes componentes.

- Rol.
- Contexto.
- Objetivo.
- Restricciones.
- Formato de salida.

Además, deberá incorporar al menos **tres Prompt Patterns** estudiados durante la clase.

---

# Documentación

Cada prompt deberá documentarse utilizando la plantilla proporcionada durante la sesión presencial.

Como mínimo deberá incluir los siguientes apartados.

- Nombre.
- Versión.
- Autor.
- Objetivo.
- Proceso organizacional.
- Prompt completo.
- Variables de entrada.
- Formato esperado.
- Restricciones.
- Ejemplo de entrada.
- Ejemplo de salida.
- Observaciones.

---

# Organización del repositorio

Organice su trabajo siguiendo la siguiente estructura.

```text
Enterprise-Prompt-Library/

│

├── README.md

│

├── prompts/

│   └── departamento/

│        prompt-01.md

│        prompt-02.md

│        prompt-03.md

│        prompt-04.md

│        prompt-05.md

│

├── templates/

│      prompt-template.md

│

└── reflexion.md
```

---

# Archivo README.md

Incluya una breve descripción de la biblioteca.

Debe responder, como mínimo, las siguientes preguntas.

- ¿Qué departamento fue seleccionado?
- ¿Cuál es el propósito de la biblioteca?
- ¿Qué procesos automatiza?
- ¿Qué beneficios aportaría a la organización?

Extensión sugerida:

300 a 500 palabras.

---

# Archivo reflexion.md

Elabore una reflexión individual respondiendo las siguientes preguntas.

## Parte I

¿Qué diferencias encontró entre escribir un prompt improvisado y diseñar un prompt profesional?

---

## Parte II

¿Qué componente resultó más difícil de definir?

¿Por qué?

---

## Parte III

¿Cuál de los Prompt Patterns utilizados considera más útil?

Justifique su respuesta.

---

## Parte IV

¿Qué mejoras realizaría después de utilizar estos prompts en un entorno real?

---

# Entregables

El estudiante deberá entregar un único archivo comprimido (.zip) con la siguiente estructura.

```text
Apellido_Nombre_PromptEngineering.zip

│

└── Enterprise-Prompt-Library/
```

No se aceptarán entregas con una estructura diferente.

---

# Criterios de evaluación

| Criterio | Puntaje |
|----------|---------|
| Organización del repositorio | 10 |
| Calidad de la documentación | 20 |
| Diseño de los prompts | 25 |
| Aplicación de Prompt Patterns | 15 |
| Reutilización y parametrización | 10 |
| Ejemplos de entrada y salida | 10 |
| Reflexión crítica | 10 |

**Total:** 100 puntos

---

# Recomendaciones

Antes de entregar su trabajo verifique que:

- Todos los prompts poseen un objetivo claramente definido.
- Los prompts pueden reutilizarse.
- Las variables de entrada están identificadas.
- El formato de salida es consistente.
- La documentación está completa.
- La estructura del repositorio coincide con la especificada.

---

# Importante

No se evaluará únicamente que el prompt funcione.

Se evaluará principalmente la calidad de su diseño, su documentación y su potencial de reutilización dentro de un entorno organizacional.

Durante las siguientes clases esta biblioteca será utilizada para incorporar técnicas de evaluación, optimización, control de versiones y gobernanza, por lo que se recomienda mantener una organización clara y una documentación completa desde esta primera versión.