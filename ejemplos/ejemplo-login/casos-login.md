# Casos de Prueba — Login

### TC-LGN-001 — Inicio de sesión exitoso

| Campo | Valor |
| :--- | :--- |
| **Módulo/Feature** | Autenticación / Login |
| **Requisito asociado** | REQ-001 |
| **Prioridad** | Alta |
| **Nivel** | E2E-UI |
| **Tipo** | Functional / Smoke |
| **¿Automatizable?** | Sí |
| **Precondiciones** | Usuario registrado; sesión cerrada. |
| **Datos de Prueba** | Usuario: `user@test.com` / Contraseña: `User123!` |

**Pasos:**
1. Ingresar a la pantalla de Login.
2. Escribir el usuario y la contraseña de prueba.
3. Hacer clic en "Iniciar Sesión".

**Resultado Esperado:**
- El sistema valida las credenciales.
- Se redirige al Dashboard principal.
- Se muestra el mensaje "Bienvenido, [Nombre del Usuario]".

**Postcondiciones:** Cerrar sesión al terminar.

| Resultado Real | Estado | Defecto ID | Fecha | Ejecutado por |
| :--- | :--- | :--- | :--- | :--- |
| Redirigió al Dashboard, pero el mensaje mostró el correo en lugar del nombre. | Failed | BUG-LGN-001 | 11/11/2026 | Yair |

**Notas:** El error solo ocurre cuando el nombre tiene más de 15 caracteres o contiene un espacio.

---

### TC-LGN-002 — Contraseña incorrecta

| Campo | Valor |
| :--- | :--- |
| **Módulo/Feature** | Autenticación / Login |
| **Requisito asociado** | REQ-002 |
| **Prioridad** | Alta |
| **Nivel** | E2E-UI |
| **Tipo** | Functional |
| **¿Automatizable?** | Sí |
| **Precondiciones** | Usuario registrado; sesión cerrada. |
| **Datos de Prueba** | Usuario: `user@test.com` / Contraseña: `incorrecta` |

**Pasos:**
1. Ingresar a la pantalla de Login.
2. Escribir el usuario y una contraseña incorrecta.
3. Hacer clic en "Iniciar Sesión".

**Resultado Esperado:**
- El sistema no permite el acceso.
- Se muestra el mensaje "Usuario o contraseña incorrectos".

**Postcondiciones:** Ninguna.

| Resultado Real | Estado | Defecto ID | Fecha | Ejecutado por |
| :--- | :--- | :--- | :--- | :--- |
| Mostró el mensaje esperado y no permitió el acceso. | Passed | N/A | 11/11/2026 | Yair |

**Notas:** Probado en Chrome y Safari.

---

### TC-LGN-003 — Bloqueo tras 3 intentos fallidos

| Campo | Valor |
| :--- | :--- |
| **Módulo/Feature** | Autenticación / Login |
| **Requisito asociado** | REQ-003 |
| **Prioridad** | Media |
| **Nivel** | Integration-API |
| **Tipo** | Functional / Security |
| **¿Automatizable?** | Sí |
| **Precondiciones** | Usuario `user@test.com` sin bloqueos previos; `MAX_LOGIN_ATTEMPTS = 3`. |
| **Datos de Prueba** | Contraseña incorrecta enviada 3 veces. |

**Pasos:**
1. Enviar 3 veces la petición de login con contraseña incorrecta.
2. Enviar una cuarta petición con la contraseña correcta.

**Resultado Esperado:**
- La cuenta queda bloqueada tras el tercer intento.
- La cuarta petición es rechazada aunque la contraseña sea correcta.

**Postcondiciones:** Restablecer el usuario de prueba.

| Resultado Real | Estado | Defecto ID | Fecha | Ejecutado por |
| :--- | :--- | :--- | :--- | :--- |
| No se pudo ejecutar: el entorno QA estuvo caído. | Blocked | N/A | 11/11/2026 | Yair |

**Notas:** Reejecutar cuando el entorno esté disponible.
