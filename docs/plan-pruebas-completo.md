# Plan de Pruebas — [Nombre del Módulo]

## 1. Información General

| | |
|---|---|
| **Versión** | 1.0 |
| **Fecha** | dd/mm/aaaa |
| **Autor** | |
| **Última actualización** | dd/mm/aaaa |

### Historial de cambios

| Versión | Fecha | Autor | Cambio |
|---|---|---|---|
| 1.0 | dd/mm/aaaa | | Versión inicial |

---

## 2. Objetivo

Validar que el módulo de **[nombre del módulo]** funcione según lo especificado, contribuyendo a asegurar:

- Integridad de datos
- Correcta persistencia en base de datos
- Seguridad de accesos
- Experiencia de usuario adecuada
- Integración correcta con otros módulos

## 3. Alcance

**Incluye:**

- [Funcionalidad 1, ej. CRUD completo de la entidad]
- [Validación de campos]
- [Roles y permisos]
- [Relaciones entre entidades]
- [Paginación y búsqueda]

**No incluye:**

- Desarrollo de nuevas funcionalidades
- Cambios en la estructura de la base de datos
- [Otro]

## 4. Referencias

- Requisitos / historias de usuario: [enlace]
- Diseño o prototipos: [enlace]
- [Estrategia de pruebas](estrategia-de-pruebas.md)
- [Guía de uso y convenciones](guia-de-uso.md)

## 5. Estrategia de pruebas

El enfoque general (pirámide, niveles y CI/CD) está definido en la [estrategia de pruebas](estrategia-de-pruebas.md). Marca los tipos de prueba que aplican a este módulo (definiciones en el [glosario](glosario.md)):

| Tipo de prueba | Aplica | No aplica | Notas |
|---|:---:|:---:|---|
| Unit | | | |
| Component | | | |
| Integration | | | |
| Smoke | | | |
| Sanity | | | |
| Functional | | | |
| Regression | | | |
| E2E | | | |
| API | | | |
| UI | | | |
| Contract | | | |
| Acceptance (UAT) | | | |
| System | | | |
| Performance — load | | | |
| Performance — stress | | | |
| Performance — spike | | | |
| Scalability | | | |
| Security — SAST | | | |
| Security — DAST | | | |
| Security — SCA | | | |
| Security — pentesting | | | |
| Accessibility (a11y) | | | |
| Compatibility / cross-browser | | | |
| Usability | | | |
| Reliability / chaos | | | |
| Recovery / failover | | | |
| Mutation | | | |
| Visual regression | | | |
| Localization (i18n) | | | |
| Data migration | | | |
| Exploratory / manual | | | |
| A/B testing | | | |

## 6. Entornos

| Entorno | URL / Referencia | Propósito |
|---|---|---|
| Desarrollo | | |
| Staging / QA | | |
| Producción | | |

## 7. Datos de prueba

Describir origen de datos, anonimización, fixtures, mocks, etc. Ver [`datos-ejemplo.md`](../tests/datos-ejemplo.md).

## 8. Herramientas

| Propósito | Herramienta |
|---|---|
| Unit | |
| Integration / API | |
| E2E / UI | |
| Performance | |
| Security | |
| CI/CD | |
| Gestión de casos y defectos | |

## 9. Supuestos y dependencias

- **Supuestos:** [ej. el entorno de QA estará disponible durante todo el ciclo]
- **Dependencias:** [ej. servicio externo de pagos en modo sandbox]

## 10. Criterios de entrada

- [ ] Build desplegado en entorno de pruebas
- [ ] Casos de prueba revisados y aprobados
- [ ] Datos de prueba disponibles
- [ ] [Otro criterio]

## 11. Criterios de salida

- [ ] 100% de los casos críticos ejecutados y aprobados
- [ ] Sin defectos críticos ni altos abiertos
- [ ] Cobertura mínima de casos ejecutados: [x]%
- [ ] Reporte de ejecución entregado

## 12. Criterios de suspensión y reanudación

- **Suspender si:** el entorno no está disponible, el build es inestable o falla el smoke test.
- **Reanudar cuando:** el entorno está restablecido y el smoke test pasa.

## 13. Roles y responsabilidades

| Rol | Nombre | Responsabilidad |
|---|---|---|
| QA Lead | | |
| QA Engineer | | |
| Dev | | |
| Product Owner | | |

## 14. Cronograma

| Fase | Inicio | Fin | Responsable |
|---|---|---|---|
| | | | |

## 15. Gestión de defectos

- **Herramienta:** [Jira / GitHub Issues / otra]
- **Severidad:** Crítica / Alta / Media / Baja
- **Flujo:** Nuevo → Asignado → En progreso → Resuelto → Verificado → Cerrado (con Reabierto y Rechazado; ver [guía de uso](guia-de-uso.md))

## 16. Riesgos

| Riesgo | Impacto | Probabilidad | Mitigación |
|---|---|---|---|
| | | | |

## 17. Entregables

- Plan de pruebas
- Casos de prueba
- Matriz de trazabilidad
- Reporte de ejecución
- Reporte de defectos
- Métricas de calidad

## 18. Métricas

- Casos ejecutados / total
- % de éxito
- Defectos por severidad
- Cobertura de pruebas
- Tiempo medio de resolución de defectos
