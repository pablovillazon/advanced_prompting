# Sample Data Pack

> **Versión:** 1.0  
> **Proyecto:** Enterprise Prompt Library (EPL)  
> **Módulo:** Prompt Engineering Avanzado  
> **Diplomado:** Automatización de Procesos con Inteligencia Artificial Generativa y Prompt Engineering

---

# Descripción

El **Sample Data Pack** es una colección de documentos de ejemplo diseñados para apoyar el desarrollo, evaluación y validación de prompts dentro de la **Enterprise Prompt Library (EPL)**.

A diferencia de un dataset utilizado para entrenamiento de modelos de Machine Learning, este repositorio contiene **documentos sintéticos** que simulan escenarios reales de organizaciones.

Estos documentos permiten que todos los estudiantes trabajen sobre un conjunto común de información, facilitando la comparación de resultados y la evaluación objetiva de los prompts desarrollados durante el módulo.

---

# Objetivos

El Sample Data Pack tiene como propósito:

- Proporcionar documentos realistas para prácticas de Prompt Engineering.
- Evitar el uso de información confidencial o datos personales reales.
- Facilitar la evaluación objetiva de prompts.
- Servir como base para demostraciones en clase.
- Permitir la reutilización de escenarios durante diferentes actividades del diplomado.
- Apoyar la integración futura con herramientas de automatización y agentes de IA.

---

# Estructura del Repositorio

```text
sample-data/

│

├── README.md

├── hr/

├── support/

├── finance/

├── legal/

├── marketing/

├── education/

└── healthcare/
```

Cada carpeta representa un dominio de negocio diferente.

---

# Dominios Incluidos

## Recursos Humanos (`hr/`)

Documentos relacionados con procesos de selección de personal.

Ejemplos:

- Hojas de vida
- Descripciones de cargo
- Evaluaciones de desempeño
- Cartas de recomendación

Casos de uso:

- Resumen de CV
- Clasificación de candidatos
- Extracción de habilidades
- Generación de preguntas para entrevistas

---

## Soporte Técnico (`support/`)

Documentos relacionados con incidentes y atención al cliente.

Ejemplos:

- Tickets de soporte
- Reportes de incidentes
- Solicitudes de servicio

Casos de uso:

- Clasificación automática
- Priorización
- Resumen de incidentes
- Generación de respuestas

---

## Finanzas (`finance/`)

Documentos utilizados en procesos financieros.

Ejemplos:

- Facturas
- Órdenes de compra
- Comprobantes
- Cotizaciones

Casos de uso:

- Extracción de información
- Validación
- Clasificación documental

---

## Legal (`legal/`)

Documentos jurídicos y contractuales.

Ejemplos:

- Contratos
- Acuerdos
- Convenios
- Políticas

Casos de uso:

- Resumen ejecutivo
- Identificación de cláusulas
- Extracción de obligaciones

---

## Marketing (`marketing/`)

Documentos relacionados con campañas y comunicación.

Ejemplos:

- Briefs
- Planes de campaña
- Publicaciones
- Estudios de mercado

Casos de uso:

- Generación de contenido
- Resumen
- Clasificación temática

---

## Educación (`education/`)

Documentos utilizados en procesos académicos.

Ejemplos:

- Informes de estudiantes
- Sílabos
- Reportes de avance
- Evaluaciones

Casos de uso:

- Síntesis
- Retroalimentación
- Extracción de competencias

---

## Salud (`healthcare/`)

Documentos relacionados con atención médica.

Ejemplos:

- Resúmenes clínicos
- Altas médicas
- Informes de laboratorio
- Reportes de consulta

Casos de uso:

- Resumen estructurado
- Extracción de diagnósticos
- Identificación de tratamientos

> **Nota:** Todos los documentos de este repositorio son ficticios y tienen fines exclusivamente académicos.

---

# Formato de los Documentos

Los documentos se almacenan inicialmente en formato **Markdown (`.md`)**.

Posteriormente podrán exportarse a:

- PDF
- DOCX
- TXT

Esto permite demostrar el uso de los prompts con distintos formatos compatibles con modelos de IA generativa.

---

# Convenciones

Para mantener la consistencia del repositorio se utilizarán las siguientes reglas:

## Nombres de Archivos

- Utilizar minúsculas.
- Separar palabras mediante guiones.
- Evitar espacios y caracteres especiales.

Ejemplos:

```text
cv-backend-senior.md

ticket-database-latency.md

invoice-consulting-services.md
```

---

## Estructura Recomendada

Cada documento debe representar un único caso de estudio.

No combinar diferentes procesos dentro del mismo archivo.

---

## Datos Sintéticos

Todos los documentos deben ser ficticios.

No deben contener:

- nombres reales;
- números de identificación;
- direcciones;
- teléfonos;
- información financiera real;
- datos médicos reales.

---

# Cómo Utilizar este Repositorio

El flujo recomendado durante las prácticas es el siguiente:

```text
Seleccionar un documento

↓

Seleccionar un prompt

↓

Ejecutar el prompt

↓

Evaluar el resultado

↓

Refinar el prompt

↓

Documentar mejoras
```

Cada documento puede reutilizarse con distintos prompts para comparar resultados y evaluar diferentes estrategias de diseño.

---

# Relación con la Enterprise Prompt Library

Los documentos de este repositorio constituyen las **entradas** utilizadas por los prompts almacenados en la Enterprise Prompt Library.

```text
Sample Data Pack

        │

        ▼

Enterprise Prompt Library

        │

        ▼

Modelo de IA

        │

        ▼

Resultado
```

Esta separación permite mantener independientes los datos de prueba y los componentes de automatización.

---

# Próximas Versiones

La versión 1.0 incluye un documento representativo por dominio.

En futuras versiones se incorporarán:

- nuevos escenarios;
- diferentes niveles de complejidad;
- documentos multilingües;
- variantes para evaluación de prompts;
- casos límite (*edge cases*);
- documentos preparados para pruebas de agentes de IA.

---

# Historial de Versiones

| Versión | Fecha | Descripción |
|----------|--------|-------------|
| 1.0 | 2026-07-21 | Creación inicial del Sample Data Pack |