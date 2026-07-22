---
template:
  id: TMP-002
  name: Generic Classification Template
  version: 1.0
  category: Classification
  language: es
  author: Enterprise Prompt Library
---

# Plantilla de Prompt para Clasificación de Documentos

## Objetivo

Esta plantilla permite clasificar documentos organizacionales utilizando criterios definidos por el usuario.

Su propósito es transformar información no estructurada en información organizada que facilite la toma de decisiones o la automatización de procesos.

Puede utilizarse con documentos provenientes de diferentes dominios organizacionales.

---

# Casos de Uso

Esta plantilla puede emplearse para clasificar:

- Curriculum Vitae
- Tickets de Soporte
- Contratos
- Facturas
- Correos Electrónicos
- Solicitudes de Clientes
- Informes Técnicos
- Reportes Académicos

---

# Variables

| Variable | Descripción | Ejemplo |
|----------|-------------|----------|
| {{rol}} | Rol asumido por el modelo | Analista de Recursos Humanos |
| {{tipo_documento}} | Documento que será analizado | Curriculum Vitae |
| {{objetivo}} | Propósito de la clasificación | Identificar el nivel del candidato |
| {{categorias}} | Categorías posibles | Junior, Semi Senior, Senior |
| {{criterios}} | Aspectos que deben evaluarse | Experiencia, tecnologías, liderazgo |
| {{idioma}} | Idioma de salida | Español |

---

# Prompt

```text
Actúa como {{rol}}.

Analiza el siguiente {{tipo_documento}}.

El objetivo del análisis es:

{{objetivo}}

Clasifica el documento utilizando únicamente las siguientes categorías:

{{categorias}}

La clasificación debe basarse exclusivamente en:

{{criterios}}

No inventes información.

Si la información disponible no es suficiente para determinar una categoría, indícalo explícitamente.

Presenta el resultado siguiendo el formato especificado.
```

---

# Formato Esperado

```text
Clasificación

Categoría:

Subcategoría:

Nivel de confianza:

Justificación:

Evidencias encontradas:

Observaciones:
```

---

# Ejemplo de Configuración 1

## Clasificación de un Curriculum Vitae

| Variable | Valor |
|----------|-------|
| rol | Analista Senior de Recursos Humanos |
| tipo_documento | Curriculum Vitae |
| objetivo | Determinar el nivel del candidato |
| categorias | Junior, Semi Senior, Senior |
| criterios | Años de experiencia, liderazgo técnico, tecnologías utilizadas |
| idioma | Español |

---

# Resultado Esperado

```text
Clasificación

Categoría:
Senior

Subcategoría:
Backend .NET

Nivel de confianza:
95%

Justificación:
El candidato posee más de ocho años de experiencia, liderazgo técnico y experiencia en arquitecturas empresariales.

Evidencias encontradas:

- Más de ocho años de experiencia.
- Desarrollo con ASP.NET Core.
- Arquitecturas de microservicios.
- Azure DevOps.
- Docker.
- Kubernetes.

Observaciones:
Perfil adecuado para posiciones Senior Backend.
```

---

# Ejemplo de Configuración 2

## Clasificación de un Ticket de Soporte

| Variable | Valor |
|----------|-------|
| rol | Analista de Mesa de Ayuda |
| tipo_documento | Ticket de Soporte |
| objetivo | Determinar prioridad y área responsable |
| categorias | Crítico, Alto, Medio, Bajo |
| criterios | Impacto, urgencia, servicios afectados |
| idioma | Español |

---

# Resultado Esperado

```text
Clasificación

Categoría:
Crítico

Subcategoría:
Base de Datos

Nivel de confianza:
98%

Justificación:
Existe una degradación severa del servicio que afecta múltiples usuarios y compromete el cumplimiento del SLA.

Evidencias encontradas:

- Tiempo de respuesta superior a ocho segundos.
- Servicio bancario afectado.
- Alto impacto operacional.

Observaciones:
Escalar inmediatamente al equipo Backend y DBA.
```

---

# Buenas Prácticas

- Definir categorías mutuamente excluyentes.
- Especificar claramente los criterios de clasificación.
- Solicitar una justificación basada en evidencias.
- Incluir un nivel de confianza.
- Evitar categorías ambiguas.
- Limitar la clasificación a la información disponible en el documento.

---

# Errores Comunes

## Categorías ambiguas

❌ Incorrecto

```text
Clasifica el documento como bueno o malo.
```

---

## Criterios indefinidos

❌ Incorrecto

```text
Determina la categoría.
```

No se especifica cómo debe evaluarse el documento.

---

## Clasificación sin justificación

❌ Incorrecto

```text
Categoría:
Senior
```

Debe explicarse por qué el modelo asignó esa categoría.

---

# Compatibilidad

Esta plantilla es compatible con modelos capaces de analizar documentos completos:

- ChatGPT
- Claude
- Gemini
- Microsoft Copilot

---

# Aplicaciones Organizacionales

Esta plantilla puede integrarse en procesos como:

- Reclutamiento y selección de personal.
- Gestión de incidencias (ITSM).
- Clasificación documental.
- Gestión de contratos.
- Gestión de solicitudes de clientes.
- Automatización de mesas de ayuda.
- Priorización de casos.

---

# Historial de Versiones

| Versión | Descripción |
|----------|-------------|
| 1.0 | Creación inicial de la plantilla |