# BUG-LGN-001 — El mensaje de bienvenida muestra el correo en lugar del nombre

| Campo | Valor |
|---|---|
| **ID del Defecto** | BUG-LGN-001 |
| **Ticket** | #1 |
| **Módulo / Funcionalidad** | Login |
| **Estado** | Nuevo |
| **Severidad** | Baja |
| **Prioridad** | Media |
| **Entorno** | QA · Build: 1.2.0-rc1 |
| **Caso de Prueba Asociado** | TC-LGN-001 |
| **¿Es regresión?** | No |
| **Reportado por** | Yair Uriel García González |
| **Asignado a** | — |
| **Fecha de Reporte** | 11/11/2026 |
| **Fecha de Verificación** | — |

---

## 1. Descripción del Problema

Tras iniciar sesión con un usuario cuyo nombre contiene un espacio, el mensaje de bienvenida muestra el correo electrónico en lugar del nombre.

## 2. Pasos para Reproducir

1. Ingresar a <https://qa.tienda-demo.example/login>.
2. Ingresar el usuario `user@test.com` y la contraseña `****`.
3. Hacer clic en "Iniciar Sesión".

## 3. Resultado Actual

El Dashboard muestra "Bienvenido, <user@test.com>".

## 4. Resultado Esperado

El Dashboard debe mostrar "Bienvenido, [Nombre del Usuario]".

## 5. Evidencia Adjunta

- [x] Captura de pantalla
- [ ] Video de reproducción
- [ ] Logs del servidor / consola del navegador
- [ ] Archivo JSON / request / response de API

## 6. Notas Adicionales

- **Frecuencia del fallo:** Siempre con nombres de más de 15 caracteres o con espacios.
- **Workaround:** Ninguno.
- **Dispositivo / Navegador:** Chrome v120, Windows 11.
