---
template:
  id: TMP-001
  name: Generic Summary Template
  version: 1.0
  category: Summarization
  language: es
  author: Enterprise Prompt Library
---

# Plantilla de Prompt para Resumen de Documentos

## Objetivo

Esta plantilla permite generar resúmenes ejecutivos de diferentes tipos de documentos organizacionales.

Está diseñada para reutilizarse en múltiples dominios, tales como:

- Recursos Humanos
- Finanzas
- Soporte Técnico
- Legal
- Marketing
- Educación
- Salud

La plantilla puede adaptarse modificando únicamente las variables definidas a continuación.

---

# Variables

| Variable | Descripción | Ejemplo |
|----------|-------------|----------|
| {{rol}} | Rol que asumirá el modelo | Analista Senior de Recursos Humanos |
| {{tipo_documento}} | Tipo de documento a analizar | Curriculum Vitae |
| {{audiencia}} | Público objetivo del resumen | Gerente de Tecnología |
| {{objetivo}} | Finalidad del resumen | Apoyar un proceso de selección |
| {{longitud}} | Tamaño esperado del resumen | 150 palabras |
| {{idioma}} | Idioma de salida | Español |
| {{criterios}} | Aspectos que deben priorizarse | Experiencia, tecnologías y liderazgo |

---

# Prompt

```text
Actúa como {{rol}}.

Analiza el {{tipo_documento}} proporcionado.

El objetivo del análisis es:

{{objetivo}}

Genera un resumen ejecutivo dirigido a:

{{audiencia}}

El resumen debe cumplir las siguientes condiciones:

- Idioma: {{idioma}}
- Longitud aproximada: {{longitud}}
- Priorizar: {{criterios}}
- Utilizar un lenguaje profesional y objetivo.
- No inventar información.
- Si algún dato no está presente en el documento, indícalo explícitamente.
- Organizar las ideas de forma clara y coherente.

Analiza únicamente el documento adjunto.
```

---

# Ejemplo de Configuración

| Variable | Valor |
|----------|-------|
| rol | Analista Senior de Recursos Humanos |
| tipo_documento | Curriculum Vitae |
| audiencia | Gerente de Tecnología |
| objetivo | Apoyar el proceso de contratación |
| longitud | 150 palabras |
| idioma | Español |
| criterios | Experiencia profesional, tecnologías, liderazgo y certificaciones |

---

# Resultado Esperado

El modelo debe producir un resumen ejecutivo que:

- sea preciso;
- sea conciso;
- mantenga únicamente información relevante;
- no incluya opiniones personales;
- no agregue información inexistente;
- esté adaptado a la audiencia indicada.

---

# Casos de Uso

Esta plantilla puede utilizarse con diferentes documentos.

| Documento | Resultado esperado |
|------------|-------------------|
| Curriculum Vitae | Resumen del perfil profesional |
| Factura | Resumen financiero |
| Contrato | Resumen ejecutivo del contrato |
| Ticket de Soporte | Resumen del incidente |
| Informe Académico | Síntesis de resultados |
| Alta Médica | Resumen clínico |

---

# Buenas Prácticas

- Definir claramente el rol del modelo.
- Especificar la audiencia objetivo.
- Indicar el propósito del resumen.
- Limitar la longitud esperada.
- Priorizar la información relevante.
- Solicitar explícitamente que no se invente información.
- Trabajar siempre sobre documentos completos.

---

# Errores Comunes

## Rol ambiguo

❌

```text
Resume este documento.
```

---

## Objetivo poco claro

❌

```text
Haz un resumen.
```

---

## Sin restricciones

❌

No indicar:

- longitud;
- audiencia;
- idioma;
- criterios de selección.

---

# Compatibilidad

Esta plantilla puede utilizarse con modelos compatibles con procesamiento de documentos, entre ellos:

- ChatGPT
- Claude
- Gemini
- Microsoft Copilot

---

# Historial de Versiones

| Versión | Descripción |
|----------|-------------|
| 1.0 | Creación inicial de la plantilla |