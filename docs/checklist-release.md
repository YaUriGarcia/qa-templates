# Checklist de Release (Go / No-Go) — [Nombre del Proyecto] v[X.Y.Z]

| | |
|---|---|
| **Release** | v[X.Y.Z] |
| **Fecha prevista** | dd/mm/aaaa |
| **Responsable de QA** | |

---

## 1. Calidad del build

- [ ] Pipeline de CI/CD en verde
- [ ] Pruebas unitarias y de integración/API aprobadas
- [ ] Suite de regresión ejecutada y aprobada
- [ ] Flujos críticos E2E aprobados
- [ ] Cobertura mínima alcanzada ([x]%)

## 2. Defectos

- [ ] Sin defectos **críticos** abiertos
- [ ] Sin defectos **altos** abiertos (o aprobados explícitamente con workaround)
- [ ] Defectos conocidos documentados en las notas de la versión

## 3. Pruebas específicas

- [ ] Smoke test aprobado en Staging
- [ ] Pruebas exploratorias realizadas en funcionalidades de alto riesgo
- [ ] Pruebas de performance básicas aprobadas (si aplica)
- [ ] Análisis de seguridad (SAST/DAST/SCA) sin hallazgos críticos (si aplica)
- [ ] UAT aprobado por el negocio (si aplica)

## 4. Documentación

- [ ] Casos de prueba actualizados
- [ ] Reporte de ejecución entregado ([`reporte-ejecucion.md`](../reportes/reporte-ejecucion.md))
- [ ] Notas de la versión (release notes) listas

## 5. Despliegue y contingencia

- [ ] Plan de despliegue revisado
- [ ] Plan de **rollback** definido y probado
- [ ] Smoke test post-despliegue preparado
- [ ] Monitoreo y alertas verificados

## 6. Decisión

- [ ] **GO:** liberar.
- [ ] **GO con reservas:** liberar con riesgos aceptados y monitoreo reforzado.
- [ ] **NO-GO:** no liberar.

**Justificación:**

| Rol | Nombre | Decisión | Fecha |
|---|---|---|---|
| QA | | | |
| Dev Lead | | | |
| Product Owner | | | |
