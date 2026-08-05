# VERSIONING.md
## Política de Versionado de Prompts

---

# Propósito

Este documento define la estrategia de versionado utilizada para los prompts almacenados en la Enterprise Prompt Library.

El objetivo es mantener un historial claro de la evolución de cada prompt, facilitar la colaboración entre los miembros del equipo y garantizar la trazabilidad de los cambios realizados.

---

# ¿Por qué versionar un prompt?

Los prompts evolucionan continuamente como resultado de:

- nuevas necesidades del negocio;
- incorporación de nuevos casos de prueba;
- retroalimentación de usuarios;
- mejoras en la calidad de las respuestas;
- cambios en los modelos de Inteligencia Artificial.

Versionar un prompt permite:

- identificar la versión utilizada en cada proceso;
- reproducir resultados;
- comparar mejoras entre versiones;
- recuperar versiones anteriores cuando sea necesario;
- documentar la evolución del conocimiento.

> Un prompt debe gestionarse con el mismo nivel de disciplina que cualquier otro artefacto de ingeniería.

---

# Esquema de Versionado

La Enterprise Prompt Library utiliza un esquema de **Versionado Semántico (Semantic Versioning)** simplificado.

Formato:

```text
MAJOR.MINOR
```

Ejemplos:

```text
v1.0
v1.1
v1.2
v2.0
v2.1
```

---

# Cuándo incrementar la versión

## Versión Mayor (MAJOR)

Incrementar el número mayor cuando existan cambios significativos que modifiquen el comportamiento esperado del prompt.

Ejemplos:

- cambio completo de la estructura;
- incorporación de nuevas etapas de análisis;
- modificación del objetivo principal;
- cambio del formato de salida;
- rediseño del proceso de razonamiento.

Ejemplo

```text
v1.0  →  v2.0
```

---

## Versión Menor (MINOR)

Incrementar el número menor cuando se realicen mejoras que mantengan el comportamiento general del prompt.

Ejemplos:

- mejorar instrucciones;
- aclarar restricciones;
- corregir errores de redacción;
- añadir ejemplos;
- mejorar el formato de salida.

Ejemplo

```text
v1.0

↓

v1.1
```

---

# Ejemplo de Evolución

## Versión 1.0

Prompt inicial desarrollado durante la Clase 2.

Características:

- clasificación básica;
- formato de salida uniforme;
- sin validación de inconsistencias.

---

## Versión 1.1

Cambios realizados:

- mejora de instrucciones;
- mayor claridad en la justificación;
- restricciones adicionales para evitar alucinaciones.

---

## Versión 2.0

Cambios importantes:

- interpretación previa del documento;
- extracción explícita de evidencias;
- identificación de información faltante;
- detección de inconsistencias;
- escala objetiva del nivel de confianza.

Esta versión representa un cambio significativo respecto a la lógica del prompt original.

---

# Buenas Prácticas

Antes de publicar una nueva versión verifique que:

- el prompt haya sido probado;
- existan casos de prueba documentados;
- el CHANGELOG esté actualizado;
- la Scorecard haya sido completada;
- el README refleje los cambios realizados.

Nunca publique una nueva versión sin documentación.

---

# Relación con otros documentos

Cada nueva versión del prompt debe actualizar los siguientes archivos:

| Documento | Acción requerida |
|-----------|------------------|
| CHANGELOG.md | Registrar los cambios realizados. |
| README.md | Actualizar la documentación si corresponde. |
| Prompt Scorecard | Evaluar nuevamente la calidad del prompt. |
| Prompt Evaluation Report | Registrar los nuevos resultados obtenidos. |

---

# Flujo recomendado

```text
Modificar Prompt
        │
        ▼
Ejecutar Casos de Prueba
        │
        ▼
Evaluar Resultados
        │
        ▼
Actualizar Scorecard
        │
        ▼
Incrementar Versión
        │
        ▼
Actualizar CHANGELOG
        │
        ▼
Publicar Nueva Versión
```

---

# Ejemplo de Historial

| Versión | Fecha | Descripción |
|----------|--------|-------------|
| v1.0 | 2026-07-10 | Primera versión del prompt. |
| v1.1 | 2026-07-18 | Mejoras de redacción y restricciones. |
| v2.0 | 2026-08-01 | Incorporación de validación, evidencias y manejo de inconsistencias. |

---

# Recomendaciones

- Mantenga un único repositorio oficial.
- Versione únicamente cambios relevantes.
- Evite crear múltiples copias del mismo prompt.
- Documente siempre el motivo de cada cambio.
- Utilice el mismo esquema de versionado para todos los prompts del repositorio.

---

# Conclusión

El versionado permite administrar la evolución de los prompts de forma controlada, reproducible y colaborativa. Al igual que el software, un prompt mejora con el tiempo gracias a la evaluación continua, la retroalimentación y la incorporación de nuevas funcionalidades. Mantener una política de versionado facilita la gobernanza de la Enterprise Prompt Library y asegura que cualquier miembro del equipo pueda comprender el historial y utilizar la versión adecuada para cada contexto.