# Prompt Improvement Analysis
## Clase 3 - Evaluación, Control y Mitigación de Riesgos en Prompts

---

# Objetivo

En este ejercicio analizaremos un prompt desarrollado durante la Clase 2 utilizando un enfoque similar al proceso de revisión de software.

El propósito no es únicamente verificar si el prompt "funciona", sino identificar oportunidades para hacerlo **más robusto, reproducible y confiable** frente a distintos escenarios de entrada.

Al finalizar este análisis obtendremos una segunda versión del prompt que será utilizada durante el resto del laboratorio.

---

# Prompt Original

```text
Actúa como Analista Senior de Recursos Humanos.

Analiza el siguiente Curriculum Vitae.

El objetivo del análisis es:

Identificar el nivel del candidato

Clasifica el documento utilizando únicamente las siguientes categorías:

Junior, Semi Senior, Senior

La clasificación debe basarse exclusivamente en:

Experiencia, tecnologías, liderazgo

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

# Contexto de Evaluación

Durante la ejecución del laboratorio este prompt fue probado utilizando cinco documentos distintos.

| Caso | Escenario |
|------|-----------|
| Caso 1 | CV completo y correctamente estructurado |
| Caso 2 | CV con información incompleta |
| Caso 3 | CV con información contradictoria |
| Caso 4 | CV con información irrelevante |
| Caso 5 | CV no estructurado (texto continuo) |

Los cuatro primeros casos obtuvieron resultados aceptables.

El **Caso 5** permitió identificar varias debilidades importantes.

---

# Evaluación del Prompt Original

## Fortalezas

El prompt presenta varios elementos propios de un buen diseño.

- Define claramente el rol del modelo.
- Establece un objetivo específico.
- Restringe las categorías permitidas.
- Indica explícitamente que no debe inventarse información.
- Solicita un formato de salida uniforme.

Estas características permiten obtener resultados consistentes cuando el documento de entrada posee una estructura clara.

---

# Debilidades Identificadas

A continuación se presentan las principales oportunidades de mejora detectadas durante la evaluación.

---

## Debilidad 1
### Asume que el documento posee una estructura estándar

El prompt inicia con:

> Analiza el siguiente Curriculum Vitae.

Sin embargo, nunca especifica qué hacer cuando el documento:

- no posee encabezados;
- está escrito como texto continuo;
- proviene de un OCR;
- contiene errores de formato;
- mezcla diferentes secciones.

En consecuencia, la clasificación depende excesivamente del formato del documento y no únicamente de su contenido.

---

## Debilidad 2
### No existe una etapa de interpretación del documento

El flujo implícito del prompt es:

```text
Documento
      ↓
Clasificación
```

En realidad, el proceso debería incluir una etapa previa de comprensión y organización de la información.

```text
Documento
      ↓
Interpretación
      ↓
Extracción de información
      ↓
Clasificación
```

Separar ambas etapas hace que el prompt sea mucho más robusto frente a documentos reales.

---

## Debilidad 3
### No solicita identificar información faltante

El prompt únicamente indica:

> No inventes información.

Sin embargo, no solicita:

- identificar datos ausentes;
- informar qué información sería necesaria;
- advertir cuando la evidencia resulta insuficiente.

En consecuencia, el modelo puede producir una clasificación con un nivel de confianza poco justificado.

---

## Debilidad 4
### La justificación carece de trazabilidad

El prompt solicita una justificación, pero no exige que cada conclusión esté respaldada por evidencia explícita encontrada en el documento.

Por ejemplo:

```text
Categoría: Senior
```

¿Por qué?

¿Dónde aparece esa evidencia?

¿Qué experiencia o tecnologías justifican dicha conclusión?

Una buena práctica consiste en relacionar cada conclusión con información verificable del documento.

---

## Debilidad 5
### No contempla inconsistencias

El prompt tampoco establece qué hacer cuando el documento presenta contradicciones.

Ejemplos:

- años de experiencia incompatibles con la fecha de graduación;
- empleos superpuestos;
- proyectos desarrollados antes de iniciar la experiencia laboral.

Sin una instrucción explícita, el modelo puede ignorar estas inconsistencias o emitir conclusiones incorrectas.

---

## Debilidad 6
### No diferencia hechos de inferencias

Un modelo de lenguaje puede producir afirmaciones como:

> "El candidato probablemente lideró proyectos..."

Sin embargo, dicha afirmación puede no estar respaldada por el documento.

El prompt debería indicar expresamente que:

- sólo pueden utilizarse hechos observables;
- no deben realizarse inferencias no sustentadas.

---

## Debilidad 7
### El nivel de confianza es ambiguo

El formato solicita un nivel de confianza, pero no define cómo debe determinarse.

Cada modelo puede interpretar este criterio de forma diferente.

Una escala predefinida mejora la consistencia entre ejecuciones.

Por ejemplo:

| Nivel | Criterio |
|--------|----------|
| Alto | Evidencia suficiente y consistente |
| Medio | Información parcial o incompleta |
| Bajo | Evidencia insuficiente o contradictoria |

---

# Resumen del Análisis

| Aspecto evaluado | Estado |
|------------------|--------|
| Definición del rol | ✅ Correcto |
| Objetivo claro | ✅ Correcto |
| Restricción de categorías | ✅ Correcto |
| Formato de salida | ✅ Correcto |
| Manejo de documentos no estructurados | ❌ Mejorable |
| Detección de inconsistencias | ❌ Ausente |
| Identificación de información faltante | ❌ Ausente |
| Separación entre hechos e inferencias | ❌ Ausente |
| Escala objetiva de confianza | ❌ Ausente |
| Trazabilidad de la evidencia | ⚠ Parcial |

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

# Mejoras Incorporadas

| Aspecto | Versión Original | Versión Refinada |
|----------|------------------|------------------|
| Manejo de documentos no estructurados | ❌ | ✅ |
| Interpretación previa del documento | ❌ | ✅ |
| Extracción explícita de evidencias | ❌ | ✅ |
| Filtrado de información irrelevante | ❌ | ✅ |
| Identificación de información faltante | ⚠ Parcial | ✅ |
| Detección de inconsistencias | ❌ | ✅ |
| Separación entre hechos e inferencias | ❌ | ✅ |
| Escala objetiva para el nivel de confianza | ❌ | ✅ |
| Trazabilidad mediante evidencias | ⚠ Parcial | ✅ |

---

# Reflexión Final

Este ejercicio demuestra que un prompt no debe considerarse un artefacto estático.

Al igual que cualquier componente de software, un prompt puede:

- diseñarse;
- evaluarse;
- probarse;
- refinarse;
- versionarse;
- mejorarse continuamente.

La diferencia entre un **Prompt Engineer** y un **Prompt Quality Engineer** no radica únicamente en escribir buenos prompts, sino en establecer un proceso sistemático para medir su calidad, identificar sus limitaciones y evolucionarlos con base en evidencia obtenida mediante pruebas.

En este sentido, los cinco casos de prueba utilizados durante el laboratorio constituyen una **suite de pruebas para prompts**, equivalente a una batería de pruebas en Ingeniería de Software, permitiendo comparar versiones, medir mejoras y justificar objetivamente la evolución de una Enterprise Prompt Library.