# Glosario de Pruebas

## Niveles (por alcance)

- **Unit:** prueba de una unidad aislada de código (función, método, clase).
- **Component:** prueba de un módulo o componente completo de forma aislada, con dependencias externas simuladas.
- **Integration:** verifica la interacción entre módulos, servicios o bases de datos.
- **System:** prueba del sistema completo integrado contra los requisitos.
- **Acceptance (UAT):** validación por parte del usuario o del negocio.

## Tipos (por característica evaluada)

- **Functional:** valida que una funcionalidad cumple lo especificado.
- **Regression:** confirma que los cambios nuevos no rompen lo existente.
- **Smoke:** verificación rápida de que lo esencial funciona tras un despliegue.
- **Sanity:** comprobación acotada de una corrección o cambio específico.
- **E2E:** flujo completo de extremo a extremo desde la perspectiva del usuario. Es una forma de ejecutar pruebas de sistema o aceptación, no un nivel ISTQB.
- **API:** pruebas a nivel de endpoints (REST/GraphQL).
- **UI:** pruebas sobre la interfaz de usuario.
- **Contract:** verifica el contrato entre consumidor y proveedor de un servicio.
- **Performance (load/stress/spike):** comportamiento bajo carga normal, límite y picos.
- **Scalability:** comportamiento al escalar recursos.
- **Security (SAST/DAST/SCA/pentesting):** análisis estático, dinámico, de dependencias y pruebas de intrusión.
- **Accessibility (a11y):** cumplimiento de pautas de accesibilidad (WCAG).
- **Compatibility:** funcionamiento en distintos navegadores, dispositivos y sistemas operativos.
- **Usability:** facilidad de uso desde la perspectiva del usuario.
- **Reliability / chaos:** resiliencia ante fallos e inyección de errores.
- **Recovery / failover:** recuperación ante desastres y conmutación.
- **Mutation:** evalúa la calidad de las propias pruebas.
- **Visual regression:** detección de cambios visuales no intencionados.
- **Localization (i18n):** validación de idiomas, formatos y regionalización.
- **Data migration:** validación de migraciones de datos.
- **Exploratory / manual:** pruebas no scriptadas guiadas por la experiencia.
- **A/B testing:** comparación de variantes para medir impacto.

## Otros términos

- **Severidad:** impacto técnico de un defecto.
- **Prioridad:** urgencia de negocio para corregirlo.
- **Fixture:** conjunto de datos o archivos predefinidos para ejecutar pruebas.
- **Seeding:** carga de datos de prueba en la base antes de una ejecución.
- **Definition of Done (DoD):** criterios que debe cumplir un desarrollo para considerarse terminado.
