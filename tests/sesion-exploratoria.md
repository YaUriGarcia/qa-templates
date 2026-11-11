# Sesión de Pruebas Exploratorias — [Módulo / Funcionalidad]

| | |
|---|---|
| **ID de sesión** | EXP-[MOD]-[NNN] |
| **Fecha** | dd/mm/aaaa |
| **Tester** | |
| **Entorno / Build** | [QA / Staging] · [versión] |
| **Duración (timebox)** | [ej. 60 min] |

---

## 1. Charter (misión)

> Explorar **[área o funcionalidad]** con **[recursos, datos o técnica]** para descubrir **[riesgo o información buscada]**.

*Ejemplo:* Explorar el flujo de checkout con distintos métodos de pago y datos límite para descubrir errores de validación y de cálculo de totales.

## 2. Alcance y fuera de alcance

- **Dentro:**
- **Fuera:**

## 3. Heurísticas o ideas de prueba

- [ ] Valores límite y datos inválidos
- [ ] Interrumpir el flujo (refrescar, volver atrás, cerrar sesión)
- [ ] Distintos roles y permisos
- [ ] Distintos dispositivos / navegadores
- [ ] Conexión lenta o caída de red
- [ ] Concurrencia (dos usuarios sobre el mismo dato)

## 4. Notas de la sesión

| Hora | Observación | Tipo (Bug / Pregunta / Idea / Riesgo) | Referencia |
|---|---|---|---|
| | | | |

## 5. Resultados

| Métrica | Valor |
|---|---|
| Bugs encontrados | |
| Preguntas abiertas | |
| Ideas de nuevos casos | |

**Bugs reportados:** BUG-[MOD]-[NNN], …

## 6. Siguientes pasos

- [ ] Convertir hallazgos en casos de prueba formales ([`casos-prueba.md`](casos-prueba.md))
- [ ] Reportar los bugs ([`reporte-bugs.md`](../reportes/reporte-bugs.md))
- [ ] Programar una nueva sesión en [área de riesgo]
