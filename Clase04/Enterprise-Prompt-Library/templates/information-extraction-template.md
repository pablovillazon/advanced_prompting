---
template:
  id: TMP-003
  name: Generic Information Extraction Template
  version: 1.0
  category: Information Extraction
  language: es
  author: Enterprise Prompt Library
---

# Plantilla de Prompt para Extracción de Información

## Objetivo

Esta plantilla permite extraer información estructurada a partir de documentos organizacionales.

Su propósito es convertir documentos no estructurados en datos que puedan ser utilizados por otros sistemas, procesos o agentes de inteligencia artificial.

Esta plantilla constituye la base para procesos de automatización documental y puede integrarse con plataformas RPA, BPM, motores de reglas o flujos de trabajo basados en IA.

---

# Casos de Uso

Puede utilizarse para analizar:

- Curriculum Vitae
- Facturas
- Contratos
- Tickets de Soporte
- Correos Electrónicos
- Informes
- Formularios
- Órdenes de Compra
- Actas
- Reportes Técnicos

---

# Variables

| Variable | Descripción | Ejemplo |
|----------|-------------|----------|
| {{rol}} | Rol asumido por el modelo | Analista Documental |
| {{tipo_documento}} | Documento que será procesado | Factura |
| {{objetivo}} | Propósito de la extracción | Registrar la factura en el ERP |
| {{campos}} | Información que debe extraerse | Número, Fecha, Cliente, Total |
| {{formato}} | Formato esperado | JSON |
| {{idioma}} | Idioma de salida | Español |

---

# Prompt

```text
Actúa como {{rol}}.

Analiza el siguiente {{tipo_documento}}.

El objetivo del análisis es:

{{objetivo}}

Extrae únicamente la siguiente información:

{{campos}}

Utiliza exclusivamente la información presente en el documento.

No inventes datos.

Si algún campo no existe, devuelve el valor:

"No encontrado"

Entrega el resultado en formato:

{{formato}}

Analiza únicamente el documento adjunto.
```

---

# Formato Esperado

## Opción 1. JSON

```json
{
  "campo_1": "",
  "campo_2": "",
  "campo_3": ""
}
```

---

## Opción 2. Tabla Markdown

| Campo | Valor |
|-------|-------|
| Campo 1 | Valor |
| Campo 2 | Valor |

---

# Ejemplo de Configuración 1

## Extracción desde una Factura

| Variable | Valor |
|----------|-------|
| rol | Analista Financiero |
| tipo_documento | Factura |
| objetivo | Registrar la factura en el ERP |
| campos | Número de factura, Fecha, Cliente, Proveedor, Total, Moneda |
| formato | JSON |
| idioma | Español |

---

# Resultado Esperado

```json
{
  "numero_factura": "F-2026-001258",
  "fecha": "20/07/2026",
  "cliente": "Financiera Andina S.A.",
  "proveedor": "TechNova Solutions S.R.L.",
  "moneda": "BOB",
  "total": "25892.82"
}
```

---

# Ejemplo de Configuración 2

## Extracción desde un Curriculum Vitae

| Variable | Valor |
|----------|-------|
| rol | Analista de Recursos Humanos |
| tipo_documento | Curriculum Vitae |
| objetivo | Registrar el perfil en el ATS |
| campos | Nombre, Profesión, Experiencia, Tecnologías, Idiomas |
| formato | JSON |
| idioma | Español |

---

# Resultado Esperado

```json
{
  "nombre": "Alejandro Vargas Rojas",
  "profesion": "Ingeniero de Sistemas",
  "experiencia": "8 años",
  "tecnologias": [
    "C#",
    ".NET",
    "ASP.NET Core",
    "SQL Server",
    "Docker",
    "Kubernetes"
  ],
  "idiomas": [
    "Español",
    "Inglés",
    "Portugués"
  ]
}
```

---

# Ejemplo de Configuración 3

## Extracción desde un Contrato

| Variable | Valor |
|----------|-------|
| rol | Analista Legal |
| tipo_documento | Contrato |
| objetivo | Registrar metadatos del contrato |
| campos | Partes, Fecha de inicio, Duración, Valor, SLA, Obligaciones |
| formato | JSON |
| idioma | Español |

---

# Resultado Esperado

```json
{
  "cliente": "Financiera Andina S.A.",
  "proveedor": "TechNova Solutions S.R.L.",
  "fecha_inicio": "01/08/2026",
  "duracion": "12 meses",
  "valor_total": "1020000 BOB",
  "sla": "99.5%",
  "obligaciones_proveedor": [
    "Asignar líder técnico",
    "Entregar reportes",
    "Mantener confidencialidad"
  ]
}
```

---

# Buenas Prácticas

- Definir previamente los campos que deben extraerse.
- Solicitar un formato estructurado (JSON o tabla).
- Indicar explícitamente que no deben inventarse datos.
- Especificar cómo manejar campos inexistentes.
- Utilizar nombres consistentes para los atributos.
- Mantener el mismo esquema entre diferentes documentos.

---

# Errores Comunes

## Solicitar demasiada información

❌ Incorrecto

```text
Extrae toda la información del documento.
```

Es preferible solicitar únicamente los campos necesarios para el proceso.

---

## No definir el formato de salida

❌ Incorrecto

```text
Extrae la información importante.
```

No queda claro cómo debe organizarse el resultado.

---

## Mezclar extracción con interpretación

❌ Incorrecto

```text
Extrae los datos y recomienda qué hacer.
```

La extracción debe limitarse a recuperar información objetiva.

La interpretación debe realizarse mediante otro prompt especializado.

---

# Compatibilidad

Esta plantilla puede utilizarse con modelos capaces de analizar documentos completos:

- ChatGPT
- Claude
- Gemini
- Microsoft Copilot

---

# Aplicaciones Organizacionales

Esta plantilla puede integrarse con:

- Sistemas ERP.
- CRM.
- BPM.
- RPA.
- Bases de datos.
- APIs REST.
- Flujos de automatización.
- Agentes inteligentes.

La salida estructurada puede utilizarse directamente como entrada para otros procesos automatizados.

---

# Relación con la Enterprise Prompt Library

Esta plantilla constituye el puente entre los documentos del **Sample Data Pack** y los sistemas de automatización organizacional.

```text
Documento

        ↓

Prompt de Extracción

        ↓

JSON / Tabla

        ↓

ERP / CRM / RPA / API / Agente IA
```

---

# Historial de Versiones

| Versión | Descripción |
|----------|-------------|
| 1.0 | Creación inicial de la plantilla |