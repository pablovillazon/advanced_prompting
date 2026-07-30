# Laboratorio Guiado
# Clase 3
## Evaluación de Prompts mediante Casos de Prueba

---

# Objetivo

Aplicar un proceso sistemático de evaluación sobre el prompt desarrollado en la Clase 2, utilizando múltiples casos de prueba para identificar fortalezas, debilidades y oportunidades de mejora.

Al finalizar el laboratorio el estudiante habrá construido el primer componente del **Prompt Evaluation Framework** dentro de su Enterprise Prompt Library.

---

# Resultados de Aprendizaje

Al concluir este laboratorio el estudiante será capaz de:

- Diseñar casos de prueba para un prompt.
- Evaluar la calidad de las respuestas generadas por un LLM.
- Detectar problemas de precisión, consistencia y completitud.
- Registrar resultados de evaluación de forma estructurada.
- Refinar un prompt a partir de la evidencia obtenida.

---

# Escenario

Una organización ha comenzado a utilizar IA Generativa para automatizar parte de sus procesos documentales.

Antes de utilizar los prompts en producción, el equipo de ingeniería debe verificar que estos producen resultados confiables.

Su trabajo consistirá en evaluar el prompt desarrollado durante la Clase 2 utilizando distintos documentos de prueba.

---

# Requisitos

Debe disponer del repositorio desarrollado en la actividad anterior.

Como mínimo deberá contener:

```text
Enterprise-Prompt-Library/

README.md

prompts/

templates/

sample-data/
```

---

# Paso 1
## Crear la carpeta de evaluación

Dentro del repositorio cree la siguiente estructura.

```text
evaluations/

README.md

test-cases.md

evaluation-report.md

improved-prompt.md
```

---

# Paso 2
## Seleccionar el Prompt

Utilice el mismo prompt desarrollado en la Clase 2.

Puede ser cualquiera de los siguientes:

- Resumen
- Clasificación
- Extracción de información

No modifique todavía el prompt.

La evaluación debe realizarse sobre la versión original.

---

# Paso 3
## Diseñar Casos de Prueba

Construya al menos cinco escenarios de evaluación.

Se recomienda utilizar una combinación similar a la siguiente.

| Caso | Descripción |
|-------|-------------|
| Caso 1 | Documento completo y correctamente estructurado |
| Caso 2 | Documento con información incompleta |
| Caso 3 | Documento con datos contradictorios |
| Caso 4 | Documento con información irrelevante |
| Caso 5 | Documento con datos mínimos |

Puede adaptar los casos según el dominio elegido.

---

# Paso 4
## Ejecutar las Pruebas

Para cada documento:

1. Abra ChatGPT (o el modelo utilizado durante el curso).

2. Pegue el prompt desarrollado.

3. Adjunte el documento correspondiente.

4. Ejecute el análisis.

5. Guarde la respuesta obtenida.

No modifique el prompt entre una prueba y otra.

---

# Paso 5
## Evaluar la Respuesta

Para cada ejecución analice los siguientes aspectos.

| Criterio | Pregunta |
|----------|----------|
| Exactitud | ¿La información es correcta? |
| Completitud | ¿Respondió todo lo solicitado? |
| Consistencia | ¿Mantiene el mismo criterio? |
| Relevancia | ¿La respuesta aporta valor? |
| Claridad | ¿El resultado es fácil de interpretar? |

Puede utilizar una escala de 1 a 5.

---

# Paso 6
## Registrar Hallazgos

Complete un registro similar al siguiente.

| Caso | Resultado | Problema identificado | Acción propuesta |
|------|-----------|----------------------|-----------------|
| Caso 1 | Correcto | Ninguno | Mantener |
| Caso 2 | Parcial | Omite experiencia laboral | Mejorar instrucciones |
| Caso 3 | Incorrecto | No detecta contradicciones | Solicitar validación explícita |

---

# Paso 7
## Refinar el Prompt

Analice los problemas encontrados.

Posteriormente genere una segunda versión del prompt incorporando mejoras.

Ejemplos.

- Mayor contexto.
- Restricciones adicionales.
- Formato de salida.
- Validaciones.
- Manejo de datos faltantes.

Guarde esta nueva versión en:

```text
evaluations/improved-prompt.md
```

---

# Producto Esperado

Al finalizar el laboratorio el repositorio deberá contener la siguiente estructura.

```text
Enterprise-Prompt-Library/

evaluations/

README.md

test-cases.md

evaluation-report.md

improved-prompt.md
```

---

# Discusión Final

Al concluir el laboratorio reflexione sobre las siguientes preguntas.

- ¿El prompt respondió correctamente en todos los casos?
- ¿Qué tipo de errores fueron más frecuentes?
- ¿Cómo podrían evitarse?
- ¿Qué cambios mejoraron la calidad de las respuestas?
- ¿Considera que el prompt está listo para utilizarse en un entorno organizacional?

---

# Evidencia

Cada estudiante deberá mostrar al docente:

- El prompt original.
- Los casos de prueba.
- Los resultados obtenidos.
- El reporte de evaluación.
- La versión mejorada del prompt.

---

# Conclusión

Este laboratorio introduce el concepto de **Prompt Quality Engineering**, donde un prompt deja de considerarse un texto estático y pasa a formar parte de un ciclo continuo de evaluación, mejora y versionamiento.

La carpeta **evaluations/** construida durante esta sesión será reutilizada en la siguiente clase para incorporar métricas, control de versiones y estrategias de optimización de prompts en entornos organizacionales.