# Caso Guiado 3
# Evolución de un Prompt mediante Patrones de Diseño

---

# Objetivo

Observar cómo un mismo prompt puede mejorar progresivamente mediante la incorporación de distintos patrones de diseño.

El escenario se basa en el proceso de **clasificación de hojas de vida** utilizado en las clases anteriores.

---

# Escenario

Una empresa tecnológica recibe cientos de hojas de vida para una vacante de **Desarrollador Backend .NET**.

El objetivo es clasificar automáticamente a los candidatos y generar un resultado que pueda integrarse con el sistema de gestión de talento.

---

# Versión 1 – Prompt Básico

```text
Clasifica la siguiente hoja de vida.
```

## Discusión

- ¿Qué información falta?
- ¿Qué tipo de respuesta esperamos?
- ¿Será consistente el resultado?

---

# Versión 2 – Persona Pattern

```text
Actúa como un Analista Senior de Recursos Humanos especializado en reclutamiento de perfiles tecnológicos.

Clasifica la siguiente hoja de vida.
```

## Mejora obtenida

- Mayor contexto.
- Respuestas más especializadas.
- Mejor alineación con el dominio.

---

# Versión 3 – Few-Shot Pattern

```text
Ejemplo 1

Perfil:
Ingeniero de Software con 6 años de experiencia en .NET.

Resultado:
Backend Senior.

---

Ejemplo 2

Perfil:
Administrador de Empresas con experiencia comercial.

Resultado:
Ejecutivo Comercial.

---

Ahora clasifica el siguiente candidato.
```

## Mejora obtenida

- Clasificaciones más consistentes.
- Reducción de ambigüedad.
- Criterios homogéneos.

---

# Versión 4 – Output Schema Pattern

```json
{
  "nombre": "",
  "perfil": "",
  "experiencia": "",
  "nivel": "",
  "fortalezas": [],
  "debilidades": [],
  "recomendacion": ""
}
```

## Mejora obtenida

- Salida estructurada.
- Integración con sistemas de RRHH.
- Procesamiento automático.

---

# Resultado Final

El prompt incorpora múltiples patrones de diseño.

```text
Persona Pattern
        +
Few-Shot Pattern
        +
Template Pattern
        +
Output Schema Pattern
```

## Reflexión

No se trata de escribir un prompt más largo.

Se trata de **resolver problemas de diseño mediante patrones adecuados**.

---

# Conclusión

El mismo proceso organizacional evolucionó desde un prompt simple hasta un componente reutilizable, consistente e integrable.

Esta evolución constituye la base para construir soluciones profesionales de automatización mediante IA Generativa.