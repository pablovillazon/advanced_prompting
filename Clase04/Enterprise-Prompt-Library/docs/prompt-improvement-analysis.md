# Prompt Improvement Analysis
## Clase 3 - Evaluación, Control y Mitigación de Riesgos en Prompts

---

# Objetivo

El propósito de este documento es analizar críticamente un prompt desarrollado durante la Clase 2, identificar sus fortalezas y debilidades a partir de los casos de prueba ejecutados, y proponer una versión refinada que mejore su robustez y confiabilidad.

Este ejercicio introduce el concepto de **Prompt Quality Engineering**, donde un prompt se considera un artefacto de ingeniería que puede evaluarse, mejorarse y versionarse mediante un proceso sistemático.

---

# Contexto

Durante la Clase 2 se desarrolló un prompt para clasificar el nivel de un candidato a partir de un Curriculum Vitae.

En la Clase 3 dicho prompt será evaluado utilizando los siguientes casos de prueba:

| Caso | Documento | Objetivo |
|------|-----------|----------|
| Caso 1 | `cv-backend-good.md` | Validar el comportamiento esperado. |
| Caso 2 | `cv-backend-incomplete.md` | Evaluar el manejo de información incompleta. |
| Caso 3 | `cv-backend-contradictory.md` | Detectar inconsistencias. |
| Caso 4 | `cv-backend-irrelevant-information.md` | Filtrar información irrelevante. |
| Caso 5 | `cv-backend-unstructured.md` | Evaluar documentos sin estructura definida. |

Los resultados obtenidos permitirán identificar oportunidades de mejora sobre el prompt original.

---

# Prompt Original

```text
Actúa como Analista Senior de Recursos Humanos.

Analiza el siguiente Curriculum Vitae.

El objetivo del análisis es:

Identificar el nivel del candidato.

Clasifica el documento utilizando únicamente las siguientes categorías:

Junior, Semi Senior, Senior

La clasificación debe basarse exclusivamente en:

Experiencia, tecnologías, liderazgo.

No inventes información.

Si la información disponible no es suficiente para determinar una categoría, indícalo explícitamente.

Presenta el resultado siguiendo el formato especificado.

Formato Esperado:

Clasificación

Categoría:

Subcategoría:

Nivel de confianza:

Justificación:

Evidencias encontradas:

Observaciones:

Utiliza el documento adjunto.
```

---

# Análisis del Prompt

## Fortalezas

El prompt presenta varios elementos propios de un buen diseño inicial.

- Define claramente el rol del modelo.
- Establece un objetivo específico.
- Restringe las categorías permitidas.
- Prohíbe inventar información.
- Solicita un formato uniforme de salida.

Para documentos correctamente estructurados, estos elementos permiten obtener resultados consistentes.

---

# Debilidades Identificadas

## 1. Asume que el documento está estructurado

El prompt no contempla documentos:

- sin encabezados;
- con formato libre;
- provenientes de OCR;
- copiados desde correo electrónico;
- con errores de formato.

Esto provoca que la calidad del resultado dependa excesivamente del formato del documento.

---

## 2. No existe una fase de interpretación

El flujo actual es:

```text
Documento
      ↓
Clasificación
```

Sin embargo, un proceso más robusto debería seguir las siguientes etapas:

```text
Documento
      ↓
Interpretación
      ↓
Extracción de información
      ↓
Validación
      ↓
Clasificación
```

Separar estas etapas mejora considerablemente la calidad del análisis.

---

## 3. No identifica información faltante

El prompt únicamente indica:

> No inventes información.

Sin embargo, también debería solicitar que el modelo:

- identifique datos ausentes;
- indique qué información sería necesaria;
- advierta cuando la evidencia sea insuficiente.

---

## 4. La justificación no es completamente trazable

El prompt solicita una justificación, pero no exige relacionar cada conclusión con evidencia específica del documento.

Una buena práctica consiste en respaldar cada decisión mediante información observable y verificable.

---

## 5. No contempla inconsistencias

No existe ninguna instrucción para manejar situaciones como:

- fechas incompatibles;
- experiencia inconsistente;
- empleos superpuestos;
- proyectos imposibles cronológicamente.

El modelo debería informar estas inconsistencias antes de clasificar.

---

## 6. No diferencia hechos de inferencias

Un modelo puede producir afirmaciones como:

> "Probablemente lideró proyectos."

Sin embargo, esa afirmación puede no estar respaldada por el documento.

El prompt debería indicar explícitamente que sólo deben utilizarse hechos observables.

---

## 7. El nivel de confianza es ambiguo

El formato solicita un nivel de confianza, pero no explica cómo determinarlo.

Una escala definida mejora la consistencia entre ejecuciones.

Por ejemplo:

| Nivel | Criterio |
|--------|----------|
| Alto | Evidencia suficiente y consistente |
| Medio | Información parcial o algunos datos faltantes |
| Bajo | Evidencia insuficiente o contradictoria |

---

# Resumen del Análisis

| Aspecto | Estado |
|----------|--------|
| Definición del rol | ✅ Correcto |
| Objetivo claro | ✅ Correcto |
| Restricción de categorías | ✅ Correcto |
| Formato de salida | ✅ Correcto |
| Manejo de documentos no estructurados | ❌ Mejorable |
| Identificación de información faltante | ❌ Ausente |
| Detección de inconsistencias | ❌ Ausente |
| Separación entre hechos e inferencias | ❌ Ausente |
| Escala objetiva de confianza | ❌ Ausente |
| Trazabilidad mediante evidencias | ⚠ Parcial |

---

# Prompt Refinado (Versión 2)

```text
Actúa como Analista Senior de Recursos Humanos especializado en evaluación técnica de perfiles de desarrollo de software.

Analiza el Curriculum Vitae adjunto con el objetivo de clasificar el nivel profesional del candidato.

La clasificación deberá utilizar exclusivamente una de las siguientes categorías:

- Junior
- Semi Senior
- Senior

No utilices categorías diferentes.

--------------------------------------------------
Proceso de análisis
--------------------------------------------------

### 1. Interpretación del documento

Analiza el documento independientemente de su formato.

El CV puede encontrarse:

- correctamente estructurado;
- parcialmente estructurado;
- sin encabezados;
- como texto continuo;
- con errores de formato;
- con información repetida.

Extrae únicamente la información que pueda identificarse de forma explícita.

No asumas que el documento posee una estructura estándar.

--------------------------------------------------

### 2. Extracción de evidencias

Identifica únicamente información relacionada con:

- experiencia profesional;
- tecnologías utilizadas;
- responsabilidades técnicas;
- liderazgo o coordinación;
- proyectos relevantes;
- formación académica.

Ignora información personal que no aporte a la clasificación (hobbies, mascotas, preferencias, frases personales, etc.).

--------------------------------------------------

### 3. Validación

Antes de clasificar:

- identifica información faltante;
- detecta posibles contradicciones cronológicas o técnicas;
- verifica si existen evidencias suficientes.

Nunca inventes información.

Nunca completes datos faltantes mediante inferencias.

Si existen contradicciones importantes, indícalo explícitamente.

--------------------------------------------------

### 4. Clasificación

Realiza la clasificación utilizando exclusivamente la evidencia encontrada.

No utilices conocimientos externos.

No supongas experiencia que no aparezca documentada.

--------------------------------------------------

### 5. Nivel de confianza

Asigna un nivel de confianza utilizando la siguiente escala.

Alto

Existe evidencia suficiente y consistente.

Medio

Existe evidencia parcial o algunos datos faltantes.

Bajo

La información es insuficiente o presenta contradicciones importantes.

--------------------------------------------------

Presenta el resultado exactamente con el siguiente formato.

# Clasificación

**Categoría:**

**Subcategoría (opcional):**

**Nivel de confianza:**

# Justificación

Explique por qué asignó dicha categoría utilizando únicamente información encontrada en el documento.

# Evidencias encontradas

Liste las evidencias relevantes en formato de viñetas.

# Información faltante

Indique qué información hubiera permitido realizar una mejor evaluación.

# Inconsistencias detectadas

Si no existen inconsistencias escriba:

"Ninguna."

# Observaciones

Incluya únicamente observaciones relevantes para el proceso de selección.

No agregue recomendaciones personales ni información que no esté respaldada por el documento.
```

---

# Comparación entre Versiones

| Aspecto | Versión 1 | Versión 2 |
|----------|:---------:|:---------:|
| Manejo de documentos no estructurados | ❌ | ✅ |
| Interpretación previa del documento | ❌ | ✅ |
| Extracción explícita de evidencias | ❌ | ✅ |
| Filtrado de información irrelevante | ❌ | ✅ |
| Identificación de información faltante | ⚠ | ✅ |
| Detección de inconsistencias | ❌ | ✅ |
| Separación entre hechos e inferencias | ❌ | ✅ |
| Escala objetiva del nivel de confianza | ❌ | ✅ |
| Trazabilidad de la evidencia | ⚠ | ✅ |

---

# Conclusiones

La evaluación realizada demuestra que un prompt no debe considerarse un elemento estático, sino un artefacto susceptible de mejora continua.

Al igual que en la Ingeniería de Software, un prompt puede diseñarse, probarse, evaluarse, refinarse y versionarse utilizando evidencia obtenida a partir de casos de prueba.

Este proceso constituye la base del **Prompt Quality Engineering**, disciplina que busca garantizar que los prompts sean robustos, reproducibles y confiables antes de ser utilizados en entornos organizacionales.

Los cinco casos de prueba utilizados durante el laboratorio conforman una **Prompt Test Suite**, equivalente a una batería de pruebas de software, permitiendo medir objetivamente la evolución de un prompt entre distintas versiones y justificando cada mejora incorporada.