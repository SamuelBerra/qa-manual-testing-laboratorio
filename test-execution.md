# Ejecución de pruebas

## Información de la ronda

| Campo | Detalle |
| --- | --- |
| Fecha | 2026-09-10 |
| Entorno | Laboratorio de Testing · Chromium |
| Alcance | Inicio, catálogo, carrito, checkout y login |
| Estado general | Aprobado |

## Resumen

| Planificados | Ejecutados | Aprobados | Fallidos | Bloqueados |
| ---: | ---: | ---: | ---: | ---: |
| 5 | 5 | 5 | 0 | 0 |

## Detalle de ejecución

| ID | Resultado esperado | Resultado observado | Estado |
| --- | --- | --- | --- |
| TC-HOME-001 | Cargar inicio, categorías y productos destacados. | La página cargó con el texto principal, categorías y sección **Productos destacados**. | ✅ Aprobado |
| TC-PROD-001 | Abrir el detalle con información y acción de compra. | Se abrió `/products/bandas-elasticas-de-resistencia` con precio, descripción, cantidad y botón **Añadir al carrito**. | ✅ Aprobado |
| TC-CART-001 | Añadir un producto y actualizar el resumen. | El carrito mostró `Bandas Elásticas de Resistencia`, cantidad `1`, total `$350.00` e indicador `1`. | ✅ Aprobado |
| TC-CHECKOUT-001 | Exigir autenticación antes de checkout. | Al seleccionar **Ir al checkout** sin sesión, el sitio mostró `/auth/login` con **Inicia Sesión**. | ✅ Aprobado |
| TC-LOGIN-001 | Impedir el envío con campos vacíos. | Con email y contraseña vacíos, **Iniciar Sesión** permaneció deshabilitado. | ✅ Aprobado |

## Conclusión

Los cinco flujos ejecutados funcionaron según lo esperado. La validación se limitó a acciones públicas y no se realizaron registros, compras ni envíos de datos personales.
