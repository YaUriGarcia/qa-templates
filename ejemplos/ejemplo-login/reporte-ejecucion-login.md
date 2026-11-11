# Reporte de Ejecución de Pruebas — Login (Tienda Demo)

| | |
|---|---|
| **Ciclo** | Release v1.2.0-rc1 |
| **Fecha de Ejecución** | 11/11/2026 |
| **Ejecutado por** | Yair Uriel García González |
| **Entorno** | QA · **Build:** 1.2.0-rc1 |
| **Plan de pruebas** | [plan-login.md](plan-login.md) |

---

## 1. Resumen Ejecutivo
Se ejecutaron los casos del módulo de Login. Se encontró un defecto de severidad baja en el mensaje de bienvenida y un caso quedó bloqueado por una caída del entorno QA. No hay bloqueadores para el release.

## 2. Alcance de la ejecución
- **Probado:** inicio de sesión exitoso y con contraseña incorrecta.
- **No probado:** bloqueo por intentos fallidos (entorno caído).

## 3. Métricas de Ejecución

| Métrica | Cantidad |
|---|---|
| Casos totales planificados | 3 |
| Casos ejecutados | 2 |
| **Passed** | 1 |
| **Failed** | 1 |
| **Blocked** | 1 |
| **Skipped** | 0 |
| **% de éxito** | 50% |

### Defectos por severidad

| Severidad | Abiertos | Cerrados |
|---|---|---|
| Crítica | 0 | 0 |
| Alta | 0 | 0 |
| Media | 0 | 0 |
| Baja | 1 | 0 |

## 4. Detalle de la Ejecución

| ID Caso | Módulo | Descripción breve | Resultado | Bug Asociado |
|---|---|---|---|---|
| TC-LGN-001 | Login | Inicio de sesión exitoso | Failed | BUG-LGN-001 |
| TC-LGN-002 | Login | Contraseña incorrecta | Passed | — |
| TC-LGN-003 | Login | Bloqueo tras 3 intentos fallidos | Blocked | — |

## 5. Defectos Encontrados en este Ciclo

| ID Bug | Título | Severidad | Prioridad | Estado Actual |
|---|---|---|---|---|
| BUG-LGN-001 | El mensaje de bienvenida muestra el correo en lugar del nombre | Baja | Media | Nuevo |

## 6. Riesgos y Bloqueos
- **Bloqueos:** el entorno QA estuvo caído y no permitió ejecutar TC-LGN-003.
- **Riesgos:** la protección de bloqueo de cuenta quedó sin validar.

## 7. Conclusión y Recomendación

- [ ] **Apto para Release**
- [x] **Apto con Reservas**
- [ ] **No Apto para Release**

**Justificación:** el único defecto es cosmético, pero se debe reejecutar TC-LGN-003 antes de liberar para validar el bloqueo de cuenta.
