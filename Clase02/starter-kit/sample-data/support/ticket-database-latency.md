---
document:
  id: SUP-001
  title: Database Latency Incident
  category: Technical Support
  type: Support Ticket
  language: es
  difficulty: intermediate
  priority: High
  version: 1.0
  author: Enterprise Prompt Library Sample Data Pack
---

# Ticket de Soporte Técnico

## Información General

**Número de Ticket:** INC-2026-000184

**Fecha de creación:** 21/07/2026

**Cliente:** Financiera Andina S.A.

**Área afectada:** Plataforma de Banca Digital

**Sistema:** API de Consultas de Cuentas

**Reportado por:** María Fernández

**Cargo:** Jefe de Operaciones

**Canal:** Portal de Soporte

---

# Asunto

Lentitud severa en consultas de saldo y movimientos bancarios.

---

# Descripción del Problema

Desde aproximadamente las **08:20 AM** los usuarios reportan tiempos de respuesta excesivamente altos al consultar el saldo de sus cuentas mediante la aplicación web y la aplicación móvil.

El tiempo promedio de respuesta pasó de aproximadamente **350 ms** a valores cercanos a **8 segundos**, generando múltiples reintentos por parte de los usuarios y un incremento significativo en llamadas al centro de atención.

El problema afecta principalmente al servicio:

```
GET /api/v2/accounts/{id}/balance
```

y ocasionalmente al servicio:

```
GET /api/v2/accounts/{id}/transactions
```

No se reportan errores HTTP 500.

Las solicitudes finalmente responden correctamente, pero con una latencia muy elevada.

---

# Impacto en el Negocio

- Clientes no pueden consultar su saldo oportunamente.
- Incremento de llamadas al Call Center.
- Riesgo reputacional.
- Posible incumplimiento de SLA.

---

# Observaciones del Cliente

El incidente comenzó después del despliegue realizado durante la madrugada.

No se identifican cambios funcionales importantes.

El comportamiento empeora durante las horas de mayor concurrencia.

---

# Información Técnica Disponible

## Infraestructura

- Kubernetes
- Azure Kubernetes Service (AKS)

## Base de Datos

Microsoft SQL Server 2022

---

## Monitoreo

CPU promedio:

38%

Memoria:

61%

Conexiones activas:

145

Tiempo promedio de consultas SQL:

7.6 segundos

---

## Logs

Se observan múltiples advertencias relacionadas con consultas lentas.

Ejemplo:

```text
Warning

Query execution exceeded threshold.

Duration:

7824 ms

Stored Procedure:

sp_GetAccountBalance

Database:

CoreBanking
```

No existen errores de conectividad.

No existen reinicios de servicios.

---

# Acciones Realizadas

- Reinicio de Pods.
- Verificación del estado del clúster.
- Revisión de utilización de CPU.
- Validación del almacenamiento.
- Revisión de conexiones activas.
- Monitoreo de consultas SQL.

Ninguna acción resolvió el problema.

---

# Información Adicional

Durante la madrugada se desplegó la versión **4.8.2** del servicio de consultas.

No se modificó la infraestructura.

No existen incidentes similares abiertos.

---

# Resultado Esperado

El servicio debería responder en menos de **500 milisegundos** para el 95 % de las solicitudes.

Actualmente el tiempo promedio supera los **8 segundos**.

---

# Estado Actual

**Abierto**

Pendiente de análisis por el equipo Backend y el equipo de Base de Datos.

---

# Archivos Adjuntos

- dashboard-performance.pdf
- sql-monitoring-report.pdf
- deployment-log.txt

---

# Notas

Este documento es completamente ficticio y fue creado con fines exclusivamente académicos para el desarrollo de actividades de Prompt Engineering dentro de la Enterprise Prompt Library.