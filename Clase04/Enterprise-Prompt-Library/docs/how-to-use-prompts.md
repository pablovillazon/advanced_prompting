---
marp: false
---

# Cómo Utilizar los Prompts de la Enterprise Prompt Library

> **Versión:** 1.0  
> **Documento:** Guía de Uso  
> **Aplicable a:** Todos los prompts de la Enterprise Prompt Library (EPL)

---

# Objetivo

Este documento explica el procedimiento recomendado para utilizar los prompts almacenados en la **Enterprise Prompt Library (EPL)**.

Los prompts de esta biblioteca han sido diseñados como componentes reutilizables y documentados. Por esta razón, **no deben utilizarse copiando únicamente el texto del prompt**, sino siguiendo un proceso sistemático de preparación, ejecución y validación.

---

# Flujo General de Trabajo

```text
Seleccionar un Prompt

        ↓

Leer la documentación

        ↓

Personalizar las variables

        ↓

Abrir el modelo de IA

        ↓

Adjuntar los documentos necesarios

        ↓

Copiar el Prompt

        ↓

Ejecutar

        ↓

Validar la respuesta

        ↓

Refinar si es necesario

        ↓

Guardar el resultado
```

---

# Paso 1. Seleccionar el Prompt

Abra el repositorio y localice el prompt que corresponde al proceso que desea automatizar.

Ejemplo:

```text
Enterprise-Prompt-Library/

└── prompts/

      summarize-cv.md
```

Cada archivo representa un componente reutilizable de la biblioteca.

---

# Paso 2. Leer la Documentación

Antes de utilizar el prompt revise cuidadosamente:

- Objetivo.
- Contexto.
- Variables.
- Restricciones.
- Ejemplo de entrada.
- Ejemplo de salida.

Esto permite verificar que el prompt realmente resuelve el problema que desea automatizar.

> **Recomendación**

Nunca copie un prompt sin comprender primero su propósito.

---

# Paso 3. Identificar las Variables

La mayoría de los prompts contienen variables similares a las siguientes:

```text
{{rol}}

{{audiencia}}

{{idioma}}

{{longitud}}

{{documento}}
```

Estas variables permiten reutilizar un mismo prompt en diferentes escenarios.

---

# Paso 4. Personalizar las Variables

Reemplace cada variable por un valor específico.

Ejemplo:

| Variable | Valor |
|----------|-------|
| rol | Analista Senior de Recursos Humanos |
| audiencia | Gerente de Tecnología |
| idioma | Español |
| longitud | 150 palabras |

En este momento todavía no es necesario reemplazar la variable **{{documento}}**.

---

# Paso 5. Abrir el Modelo de IA

Puede utilizar cualquier modelo compatible con procesamiento de documentos.

Por ejemplo:

- ChatGPT
- Claude
- Gemini
- Microsoft Copilot

Se recomienda iniciar una conversación nueva para evitar que el contexto de chats anteriores influya en el resultado.

---

# Paso 6. Adjuntar el Documento

Utilice la opción **Adjuntar Archivo** del modelo de IA.

Los formatos recomendados son:

| Formato | Recomendado |
|----------|-------------|
| PDF | ✅ |
| DOCX | ✅ |
| TXT | ✅ |
| Markdown | ✅ |
| Imagen (JPG, PNG) | ✅ (cuando contiene texto legible) |

Ejemplo:

```text
CV_Juan_Perez.pdf
```

Una vez cargado el archivo, el modelo podrá analizar su contenido.

> **Importante**

No es necesario copiar manualmente el contenido del documento dentro del prompt cuando el modelo permite trabajar con archivos adjuntos.

---

# Paso 7. Copiar el Prompt

Dentro del archivo del repositorio ubique la sección:

```markdown
## Prompt
```

Copie únicamente el contenido del prompt.

Ejemplo:

```text
Actúa como un Analista Senior de Recursos Humanos.

Tu responsabilidad consiste en analizar hojas de vida para procesos de selección.

Genera un resumen ejecutivo dirigido a un Gerente de Tecnología.

Requisitos:

- máximo 150 palabras
- idioma español
- destacar experiencia relevante
- mencionar tecnologías principales
- identificar fortalezas
- no inventar información

Analiza el documento adjunto.
```

Observe que las variables ya fueron reemplazadas por valores concretos.

---

# Paso 8. Ejecutar el Prompt

La conversación en el modelo de IA debería tener una estructura similar a la siguiente.

```text
📎 CV_Juan_Perez.pdf

Actúa como un Analista Senior de Recursos Humanos.

Tu responsabilidad consiste en analizar hojas de vida para procesos de selección.

Genera un resumen ejecutivo dirigido a un Gerente de Tecnología.

Requisitos:

- máximo 150 palabras
- idioma español
- destacar experiencia relevante
- mencionar tecnologías principales
- identificar fortalezas
- no inventar información

Analiza el documento adjunto.
```

Espere a que el modelo genere la respuesta.

---

# Paso 9. Validar el Resultado

No asuma que la primera respuesta siempre es correcta.

Verifique que cumpla con los criterios definidos por el prompt.

Lista de verificación:

- ¿La información proviene únicamente del documento?
- ¿No existen datos inventados?
- ¿Se respetó la longitud solicitada?
- ¿El lenguaje es profesional?
- ¿La estructura coincide con la especificación?
- ¿La información relevante fue incluida?

Si alguna respuesta es negativa, continúe con el siguiente paso.

---

# Paso 10. Refinar el Prompt

Cuando el resultado no sea satisfactorio, modifique el prompt antes de volver a ejecutarlo.

Ejemplo.

### Prompt inicial

```text
Resume el siguiente documento.
```

### Prompt refinado

```text
Resume únicamente la experiencia profesional relacionada con desarrollo Backend utilizando tecnologías Microsoft.

Ignora información personal que no sea relevante para la evaluación técnica.
```

Generalmente pequeñas mejoras producen resultados significativamente mejores.

---

# Paso 11. Guardar el Resultado

El resultado generado puede utilizarse como:

- informe para un responsable del proceso;
- entrada para otro prompt;
- registro documental;
- información para un sistema de automatización;
- evidencia dentro del proyecto.

---

# Buenas Prácticas

- Lea siempre la documentación antes de utilizar un prompt.
- Mantenga una única responsabilidad por prompt.
- Utilice nombres descriptivos para los archivos.
- Documente cualquier modificación importante.
- Reutilice plantillas en lugar de duplicar prompts.
- Valide siempre la salida antes de utilizarla en un proceso organizacional.
- Versione los cambios cuando el comportamiento del prompt cambie significativamente.

---

# Errores Comunes

## Copiar únicamente el Prompt

❌ Incorrecto

No comprender el contexto ni las restricciones.

---

## No reemplazar las variables

❌ Incorrecto

```text
{{rol}}

{{audiencia}}

{{documento}}
```

Las variables deben sustituirse por valores reales.

---

## Omitir la validación

❌ Incorrecto

Aceptar la primera respuesta sin verificar su calidad.

---

## Modificar múltiples aspectos al mismo tiempo

❌ Incorrecto

Si cambia varias instrucciones simultáneamente será difícil identificar qué produjo la mejora.

---

# Flujo Recomendado para la Clase

Durante las actividades del módulo se recomienda seguir siempre el siguiente procedimiento.

```text
Seleccionar Prompt

↓

Leer documentación

↓

Personalizar variables

↓

Adjuntar documento

↓

Ejecutar

↓

Evaluar

↓

Refinar

↓

Guardar resultado

↓

Documentar cambios
```

Este flujo será utilizado durante todas las prácticas del módulo y servirá como base para integrar la Enterprise Prompt Library con herramientas de automatización en las siguientes clases.

---

# Próximos Pasos

En las siguientes clases aprenderá a:

- evaluar sistemáticamente la calidad de un prompt;
- diseñar casos de prueba;
- medir el desempeño mediante métricas;
- controlar versiones;
- optimizar bibliotecas de prompts para entornos organizacionales.

De esta manera, la **Enterprise Prompt Library** evolucionará desde una colección de prompts documentados hasta una biblioteca preparada para integrarse en procesos empresariales automatizados.