# Casos de Prueba — [Nombre del Módulo]

## Convenciones

- **ID:** `TC-[MOD]-[NNN]` (ver [guía de uso](../docs/guia-de-uso.md)).
- **Prioridad:** Alta / Media / Baja.
- **Estado:** Draft / Passed / Failed / Blocked / Skipped.
- **Nivel:** Unit / Component / Integration-API / E2E-UI (según la [pirámide de pruebas](../docs/estrategia-de-pruebas.md)).
- **Tipo:** Functional / Regression / Smoke / Security / etc. (ver [glosario](../docs/glosario.md)).

> Un ejemplo completo y llenado está en [`ejemplos/ejemplo-login/casos-login.md`](../ejemplos/ejemplo-login/casos-login.md).

---

## Formato Ficha (recomendado)

Divide cada caso en dos partes: una **tabla superior** con los metadatos y **texto estructurado** (listas) para pasos y resultados. Es más legible y fácil de editar en Markdown que una tabla gigante.

Copia el bloque siguiente por cada caso.

### TC-[MOD]-[NNN] — [Título del caso]

| Campo | Valor |
| :--- | :--- |
| **Módulo/Feature** | |
| **Requisito asociado** | [ID de historia de usuario o requisito] |
| **Prioridad** | Alta / Media / Baja |
| **Nivel** | Unit / Component / Integration-API / E2E-UI |
| **Tipo** | Functional / Regression / Smoke / … |
| **¿Automatizable?** | Sí / No / Automatizado |
| **Precondiciones** | |
| **Datos de Prueba** | |

**Pasos:**

1. [Paso 1]
2. [Paso 2]
3. [Paso 3]

**Resultado Esperado:**

- [Resultado 1]
- [Resultado 2]

**Postcondiciones:** [Estado en que queda el sistema o limpieza necesaria]

**Ejecución:**

| Resultado Real | Estado | Defecto ID | Fecha | Ejecutado por |
| :--- | :--- | :--- | :--- | :--- |
| | Draft | N/A | | |

**Notas:**

---

## Formato Tabla (alternativa)

Útil para exportar a Excel. En Markdown, usa `<br>` para los saltos de línea dentro de las celdas.

| ID | Título | Módulo | Prioridad | Nivel | Tipo | Datos de Prueba | Pasos | Resultado Esperado | Resultado Real | Estado | Defecto ID |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-[MOD]-001 | | | | | | | 1. <br> 2. <br> 3. | | | Draft | N/A |

Si no quieres incluir los pasos, elimina la columna **Pasos**.
