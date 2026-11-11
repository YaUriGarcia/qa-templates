# Reporte de Ejecución de Pruebas — [Nombre del Proyecto]

| | |
|---|---|
| **Ciclo** | [Ej. Sprint 14 / Release v1.2] |
| **Fecha de Ejecución** | [dd/mm/aaaa] |
| **Ejecutado por** | [Tu nombre / Equipo de QA] |
| **Entorno** | [QA / Staging] · **Build:** [número o versión] |
| **Plan de pruebas** | [enlace al plan] |

---

## 1. Resumen Ejecutivo
[Un párrafo breve con el estado general. Ej: se completó la ejecución de los casos críticos del módulo de pagos. Se encontraron 2 bugs de severidad alta que bloquean el pase a producción. El resto de la funcionalidad opera con normalidad.]

## 2. Alcance de la ejecución

- **Probado:** [módulos o funcionalidades cubiertas]
- **No probado:** [qué quedó fuera y por qué]

## 3. Métricas de Ejecución

| Métrica | Cantidad |
|---|---|
| Casos totales planificados | [Ej. 50] |
| Casos ejecutados | [Ej. 50] |
| **Passed** | [Ej. 45] |
| **Failed** | [Ej. 3] |
| **Blocked** | [Ej. 2] |
| **Skipped** | [Ej. 0] |
| **% de éxito** (Passed / ejecutados) | [Ej. 90%] |
| **% de cobertura de requisitos** | [Ej. 95%] |

### Defectos por severidad

| Severidad | Abiertos | Cerrados |
|---|---|---|
| Crítica | | |
| Alta | | |
| Media | | |
| Baja | | |

## 4. Detalle de la Ejecución
*(Resume por módulo o lista los casos si son pocos)*

| ID Caso | Módulo | Descripción breve | Resultado | Bug Asociado |
|---|---|---|---|---|
| TC-LGN-001 | Login | Inicio de sesión exitoso | Passed | — |
| TC-LGN-002 | Login | Contraseña incorrecta | Failed | BUG-LGN-001 |
| TC-PAG-010 | Pagos | Pago con tarjeta de crédito | Blocked | — |
| [...] | [...] | [...] | [...] | [...] |

## 5. Defectos Encontrados en este Ciclo

| ID Bug | Título | Severidad | Prioridad | Estado Actual |
|---|---|---|---|---|
| BUG-LGN-001 | Mensaje de error incorrecto al fallar login | Baja | Media | Nuevo |
| BUG-PAG-005 | El botón de pagar no responde en móviles | Crítica | Alta | En progreso |

## 6. Riesgos y Bloqueos

- **Bloqueos:** [Ej. el entorno de QA se cayó a las 3 PM e impidió probar el flujo X.]
- **Riesgos:** [Ej. no se pudo probar la integración con el banco porque el servicio estaba en mantenimiento.]

## 7. Conclusión y Recomendación

- [ ] **Apto para Release:** la calidad es aceptable y no hay bloqueadores.
- [ ] **Apto con Reservas:** se puede liberar, pero se deben monitorear los bugs reportados.
- [ ] **No Apto para Release:** existen bugs críticos o bloqueos que impiden el despliegue.

**Justificación:**
[Breve explicación de la decisión.]

Para la decisión final de liberación, usa el [checklist de release](../docs/checklist-release.md).
