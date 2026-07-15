# Laboratorio 1
## Construcción Iterativa de un Prompt Profesional

**Clase:** 1

**Duración:** 20 minutos

**Modalidad:** Guiado por el docente

---

# Objetivo

Diseñar un prompt profesional aplicando una metodología iterativa basada en componentes arquitectónicos (rol, contexto, objetivo, restricciones y formato).

Al finalizar este laboratorio el estudiante será capaz de:

- Identificar las limitaciones de un prompt improvisado.
- Mejorar progresivamente un prompt mediante iteraciones.
- Comparar resultados entre diferentes versiones.
- Comprender cómo las decisiones de diseño modifican el comportamiento del modelo.

---

# Caso de estudio

La empresa **TechSolutions S.A.** recibe aproximadamente **300 solicitudes diarias** en su mesa de ayuda.

Actualmente un operador humano clasifica manualmente cada solicitud para determinar:

- categoría;
- prioridad;
- departamento responsable.

La empresa desea automatizar este proceso utilizando un modelo de lenguaje.

---

# Material proporcionado

## Solicitud recibida

**Asunto**

No puedo acceder al sistema

**Mensaje**

Buenos días.

Desde esta mañana intento ingresar al sistema ERP, pero aparece el mensaje **Error 500**.

Necesito emitir facturas hoy mismo.

Muchas gracias.

---

# Paso 1 — Prompt inicial

Sin utilizar ningún patrón de diseño, escriba el primer prompt que utilizaría para resolver el problema.

**Tiempo sugerido:** 3 minutos.

Ejemplo:

```text
Clasifica este correo electrónico.
```

---

## Reflexión

Discuta con su grupo:

- ¿Qué información falta?
- ¿Puede otra persona reutilizar este prompt?
- ¿Obtendrán todos los usuarios exactamente la misma respuesta?

---

# Paso 2 — Agregar un Rol

Ahora incorpore un rol profesional.

Ejemplo:

```text
Actúa como un analista senior de soporte técnico.
```

Ejecute nuevamente el prompt.

---

## Reflexión

¿Qué cambió respecto a la primera versión?

---

# Paso 3 — Agregar Contexto

Incorpore información relevante sobre el proceso organizacional.

Ejemplo:

```text
La empresa recibe aproximadamente 300 solicitudes de soporte diariamente.
Todas deben clasificarse antes de asignarlas al departamento correspondiente.
```

Ejecute nuevamente el prompt.

---

# Paso 4 — Definir el Objetivo

Especifique claramente qué espera obtener.

Ejemplo:

```text
Clasifica la solicitud indicando:

- categoría
- prioridad
- departamento responsable
- justificación
```

---

# Paso 5 — Incorporar Restricciones

Agregue reglas que limiten el comportamiento del modelo.

Ejemplo:

```text
No inventes información.

Utiliza únicamente las categorías definidas.

Si la información es insuficiente, indícalo explícitamente.
```

---

# Paso 6 — Definir el Formato

Solicite un formato estructurado.

Ejemplo:

```json
{
    "categoria":"",
    "prioridad":"",
    "departamento":"",
    "justificacion":""
}
```

Ejecute nuevamente el prompt.

---

# Comparación de resultados

Complete la siguiente tabla.

| Versión | ¿Qué mejoró? |
|----------|--------------|
| Prompt inicial | |
| Con rol | |
| Con contexto | |
| Con objetivo | |
| Con restricciones | |
| Con formato | |

---

# Discusión

Responda junto con su grupo:

1. ¿Qué componente produjo la mayor mejora?

2. ¿Cuál fue el más difícil de definir?

3. ¿Qué componente considera indispensable?

No existe una única respuesta correcta.

El objetivo es analizar el impacto de cada decisión de diseño.

---

# Conclusiones

Complete las siguientes afirmaciones.

**Antes del laboratorio pensaba que...**

_____________________________________________________

**Después del laboratorio considero que...**

_____________________________________________________

---

# Entregable

Cada grupo entregará:

- El prompt inicial.
- El prompt final.
- Una breve explicación de las decisiones de diseño adoptadas.
