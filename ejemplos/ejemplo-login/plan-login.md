# Plan de Pruebas — Login (Tienda Demo)

| | |
|---|---|
| **Versión** | 1.0 |
| **Fecha** | 10/11/2026 |
| **Autor** | Yair Uriel García González |

---

## 1. Objetivo

Validar que el inicio de sesión funcione con credenciales válidas e inválidas y que el bloqueo por intentos fallidos proteja las cuentas.

## 2. Alcance

**Incluye:**
- Inicio de sesión con credenciales válidas e inválidas
- Mensajes de error y bloqueo tras 3 intentos fallidos
- Mensaje de bienvenida y redirección al Dashboard

**No incluye:**
- Registro de usuarios
- Recuperación de contraseña

## 3. Tipos de prueba

- [x] **Functional** — manual
- [x] **Smoke** — Postman (endpoint `/login` responde 200)
- [x] **API** — Postman
- [x] **UI** — manual (Chrome y Safari)
- [ ] **Performance**
- [x] **Security** — pruebas manuales de bloqueo de cuenta

## 4. Entornos

| Entorno | URL | Propósito |
|---|---|---|
| Staging / QA | https://qa.tienda-demo.example | Ejecución de pruebas |

## 5. Datos y herramientas

- **Datos de prueba:** usuarios de [`datos-ejemplo.md`](../../tests/datos-ejemplo.md)
- **CI/CD:** GitHub Actions
- **Gestión de casos/defectos:** GitHub Issues

## 6. Criterios de entrada

- [x] Build desplegado en QA
- [x] Casos de prueba listos
- [x] Datos disponibles

## 7. Criterios de salida

- [ ] Casos críticos ejecutados y aprobados
- [ ] Defectos críticos/altos cerrados
- [ ] Cobertura mínima: 100% de casos de prioridad Alta

## 8. Riesgos

| Riesgo | Mitigación |
|---|---|
| Entorno QA inestable | Ejecutar smoke antes de cada ciclo |
| Cuenta bloqueada por pruebas previas | Restablecer usuarios de prueba antes de cada ciclo |

## 9. Entregables

- Casos de prueba
- Reporte de ejecución
- Reporte de defectos
