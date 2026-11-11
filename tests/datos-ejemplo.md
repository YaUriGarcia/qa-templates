# Datos de Prueba — [Nombre del Proyecto / Módulo]

Este documento centraliza los datos, usuarios y configuraciones necesarias para ejecutar los casos de prueba.

> **Regla de seguridad:** nunca incluyas contraseñas reales de producción en este archivo. Los valores de abajo son ejemplos de entornos de prueba. Si el proyecto lo permite, usa variables de entorno o el gestor de secretos del equipo.

---

## 1. Usuarios de Prueba (Roles y Credenciales)

| Rol / Perfil | Usuario / Email | Contraseña | Entorno | Notas |
| :--- | :--- | :--- | :--- | :--- |
| Administrador | `admin@test.com` | `Admin123!` | QA / Staging | Acceso total al sistema. |
| Usuario Estándar | `user@test.com` | `User123!` | QA / Staging | Solo lectura y creación. |
| Usuario Bloqueado | `blocked@test.com` | `Block123!` | QA / Staging | Útil para probar mensajes de error de login. |
| Invitado | `guest@test.com` | `Guest123!` | QA / Staging | Acceso limitado. |

---

## 2. Datos Maestros y Catálogos

*(IDs de productos, clientes o configuraciones que deban existir en el entorno de pruebas).*

| Entidad | ID / Código | Descripción | Estado esperado |
| :--- | :--- | :--- | :--- |
| Producto Físico | `PROD-001` | Artículo con stock disponible. | Activo |
| Producto Digital | `PROD-002` | Licencia de software. | Activo |
| Cliente VIP | `CLI-999` | Cliente con descuentos especiales. | Activo |
| Cliente Moroso | `CLI-000` | Cliente bloqueado por falta de pago. | Inactivo |

---

## 3. Tarjetas de Crédito de Prueba (solo si aplica)

*(Si el sistema procesa pagos, usa las tarjetas de prueba de la pasarela, como Stripe o PayPal. **Verifica siempre los números vigentes en la documentación de tu pasarela**, ya que cada una define sus propios casos).*

| Escenario | Número | CVV | Fecha Exp. | Comportamiento esperado |
| :--- | :--- | :--- | :--- | :--- |
| Visa (éxito) | `4242 4242 4242 4242` | Cualquiera de 3 dígitos | Cualquier fecha futura | Pago aprobado. |
| Mastercard (éxito) | `5555 5555 5555 4444` | Cualquiera de 3 dígitos | Cualquier fecha futura | Pago aprobado. |
| Tarjeta rechazada | `4000 0000 0000 0002` | Cualquiera de 3 dígitos | Cualquier fecha futura | Pago rechazado. |
| Fondos insuficientes | `4000 0000 0000 9995` | Cualquiera de 3 dígitos | Cualquier fecha futura | Pago rechazado por fondos. |

---

## 4. Configuraciones o Feature Flags

*(Banderas de configuración o variables que alteren el comportamiento de la app).*

| Variable / Configuración | Valor para QA | Impacto en la prueba |
| :--- | :--- | :--- |
| `ENABLE_NEW_CHECKOUT` | `true` | Activa el nuevo flujo de pago. |
| `MAX_LOGIN_ATTEMPTS` | `3` | Bloquea la cuenta después de 3 intentos fallidos. |

---

## 5. Archivos de Prueba (Fixtures)

*(Si necesitas subir archivos para probar, especifica dónde están guardados).*

- **Imágenes:** carpeta `/fixtures/images/` (formatos JPG, PNG < 5 MB).
- **Documentos:** carpeta `/fixtures/docs/` (PDFs de prueba).
- **CSV / JSON:** carpeta `/fixtures/bulk/` (archivos de carga masiva).

---

## 6. Limpieza y restauración de datos

| Dato creado durante las pruebas | Cómo se limpia | Responsable |
| :--- | :--- | :--- |
| Usuarios creados en pruebas de registro | Script de limpieza / rollback | |
| Pedidos de prueba | Eliminar por prefijo `TEST-` | |
| Restauración de la base de QA | Snapshot anonimizado cada [frecuencia] | |
