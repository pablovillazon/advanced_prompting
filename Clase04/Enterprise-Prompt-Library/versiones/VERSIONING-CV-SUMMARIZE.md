# VERSIONING EXAMPLE
## Enterprise Prompt Library

Este documento muestra cómo evoluciona el prompt de clasificación de Currículums Vitae desarrollado durante el módulo. 'prompts/summarize-cv.md'

---

# Historial de Versiones

## v1.0
**Fecha:** 10/07/2026

### Descripción

Primera versión funcional del prompt.

### Características

- Define el rol del modelo.
- Clasifica candidatos en Junior, Semi Senior o Senior.
- Solicita una justificación.
- Incluye un formato básico de salida.

### Estado

✅ Publicado

---

## v2.0
**Fecha:** 05/08/2026

### Cambios realizados

- Nueva etapa de interpretación del documento.
- Extracción explícita de evidencias.
- Detección de inconsistencias.
- Identificación de información faltante.
- Escala objetiva del nivel de confianza.
- Separación entre hechos e inferencias.
- Ignora informacion no relevante.

### Motivo

Los casos de prueba revelaron que el prompt no manejaba correctamente documentos incompletos o sin estructura.

### Estado

✅ Versión estable
