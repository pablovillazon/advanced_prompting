# Summarize Candidate CV

> **Versión:** 1.0  
> **Estado:** Activo  
> **Proceso:** Reclutamiento y Selección de Personal  
> **Responsable:** Equipo de Recursos Humanos  
> **Patrones utilizados:** Persona Pattern, Template Pattern, Output Schema Pattern

---

# Objetivo

Generar un resumen ejecutivo de una hoja de vida para facilitar la evaluación inicial de candidatos durante un proceso de selección.

El resumen debe destacar únicamente la información relevante para la toma de decisiones, evitando agregar contenido que no exista en el documento original.

---

# Contexto de Uso

Este prompt forma parte del proceso de reclutamiento.

Se ejecuta **después de recibir la hoja de vida** y **antes de la evaluación por parte del reclutador**.

```text
Recepción CV

↓

Resumen Ejecutivo

↓

Clasificación

↓

Evaluación

↓

Entrevista
```

---

# Entradas

| Variable | Obligatoria | Descripción |
|------------|-------------|-------------|
| rol | Sí | Perfil profesional que asumirá el modelo |
| audiencia | Sí | Persona que leerá el resumen |
| documento | Sí | Hoja de vida completa |
| idioma | No | Idioma del resultado |
| longitud | No | Máximo de palabras |

---

# Variables Recomendadas

| Variable | Valor sugerido |
|------------|---------------|
| rol | Analista Senior de Recursos Humanos |
| audiencia | Gerente de Tecnología |
| idioma | Español |
| longitud | 150 palabras |

---

# Prompt

```text
Actúa como {{rol}}.

Tu responsabilidad consiste en analizar hojas de vida para procesos de selección de personal.

Genera un resumen ejecutivo dirigido a:

{{audiencia}}

Requisitos:

- máximo {{longitud}}
- idioma {{idioma}}
- destacar experiencia relevante
- mencionar tecnologías principales
- identificar fortalezas
- no inventar información

Hoja de vida en el documento adjunto.

{{documento}}
```

---

# Restricciones

El modelo debe:

- utilizar únicamente información presente en el documento;
- mantener un tono profesional;
- conservar nombres propios;
- evitar opiniones personales;
- no realizar recomendaciones de contratación.

---

# Formato Esperado

```markdown
## Resumen Ejecutivo

### Perfil General

...

### Experiencia Relevante

...

### Competencias Técnicas

...

### Formación Académica

...

### Observaciones

...
```

---

# Ejemplo de Entrada

```text
Ingeniero de Sistemas con ocho años de experiencia en desarrollo Backend utilizando .NET, SQL Server y Azure.

Participó en proyectos financieros y de telecomunicaciones.

Cuenta con certificaciones Microsoft Azure Fundamentals y Scrum Master.
```

---

# Ejemplo de Salida

```markdown
## Resumen Ejecutivo

### Perfil General

Ingeniero de Sistemas con ocho años de experiencia en desarrollo Backend.

### Experiencia Relevante

Participación en proyectos financieros y de telecomunicaciones utilizando tecnologías Microsoft.

### Competencias Técnicas

.NET

SQL Server

Azure

Scrum

### Formación

Ingeniería de Sistemas

Certificación Azure Fundamentals

Scrum Master

### Observaciones

Perfil con experiencia sólida en tecnologías Backend Microsoft.
```

---

# Patrones Aplicados

| Patrón | Propósito |
|----------|-----------|
| Persona Pattern | Definir el rol del analista |
| Template Pattern | Reutilizar el prompt |
| Output Schema Pattern | Estructurar el resultado |

---

# Calidad Esperada

El resultado debe cumplir los siguientes criterios.

- La información corresponde exactamente al documento.
- No existen datos inventados.
- El resumen mantiene un lenguaje profesional.
- Se respetan las restricciones de longitud.
- El formato es consistente.

---

# Integración

Este prompt puede integrarse con:

- Microsoft Power Automate
- n8n
- Zapier
- LangChain
- Prompt Flow
- APIs de OpenAI

---

# Dependencias

Este prompt utiliza la plantilla:

```text
templates/summary-template.md
```

Puede formar parte del proceso:

```text
processes/recruitment.md
```

---

# Historial de Cambios

| Versión | Fecha | Descripción |
|----------|--------|-------------|
| 1.0 | 2026-07-21 | Versión inicial |