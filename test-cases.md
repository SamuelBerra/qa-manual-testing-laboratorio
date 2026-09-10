# Casos de prueba

## Resumen

| ID | Módulo | Escenario | Prioridad | Tipo |
| --- | --- | --- | --- | --- |
| TC-HOME-001 | Inicio | Carga de la página principal | Alta | Positiva |
| TC-PROD-001 | Catálogo | Navegación al detalle de un producto | Alta | Positiva |
| TC-CART-001 | Carrito | Agregar un producto desde su detalle | Alta | Positiva |
| TC-CHECKOUT-001 | Checkout | Restricción de acceso sin sesión | Alta | Positiva |
| TC-LOGIN-001 | Login | Botón de acceso deshabilitado con campos vacíos | Media | Negativa |

---

## TC-HOME-001 — Carga de la página principal

| Campo | Detalle |
| --- | --- |
| Prioridad | Alta |
| Tipo | Positiva / funcional |
| Precondición | Ninguna. |

| # | Paso | Resultado esperado |
| --- | --- | --- |
| 1 | Abrir `https://www.laboratoriodetesting.com/`. | La página principal carga sin errores visibles. |
| 2 | Revisar el contenido principal. | Se visualizan el mensaje principal, las categorías y la sección **Productos destacados**. |

---

## TC-PROD-001 — Navegación al detalle de un producto

| Campo | Detalle |
| --- | --- |
| Prioridad | Alta |
| Tipo | Positiva / funcional |
| Precondición | Estar en la página principal. |
| Datos de prueba | Producto: `Bandas Elásticas de Resistencia`. |

| # | Paso | Resultado esperado |
| --- | --- | --- |
| 1 | Seleccionar el producto desde **Productos destacados**. | Se abre la ficha del producto. |
| 2 | Revisar la ficha. | Se muestran el nombre, precio `$350.00`, descripción, control de cantidad y botón **Añadir al carrito**. |

---

## TC-CART-001 — Agregar un producto desde su detalle

| Campo | Detalle |
| --- | --- |
| Prioridad | Alta |
| Tipo | Positiva / funcional |
| Precondición | Estar en el detalle de `Bandas Elásticas de Resistencia`. |
| Datos de prueba | Cantidad: `1`. |

| # | Paso | Resultado esperado |
| --- | --- | --- |
| 1 | Seleccionar **Añadir al carrito**. | El sistema agrega el producto al carrito. |
| 2 | Revisar el resumen del carrito. | Se muestra el producto, cantidad `1`, total `$350.00` y un indicador de carrito con `1`. |

---

## TC-CHECKOUT-001 — Restricción de acceso al checkout sin sesión

| Campo | Detalle |
| --- | --- |
| Prioridad | Alta |
| Tipo | Positiva / seguridad de acceso |
| Precondición | Tener al menos un producto en el carrito y no haber iniciado sesión. |

| # | Paso | Resultado esperado |
| --- | --- | --- |
| 1 | Seleccionar **Ir al checkout**. | El acceso al checkout requiere autenticación. |
| 2 | Revisar la página de destino. | Se redirige a `/auth/login` y se muestra el formulario **Inicia Sesión**. |

---

## TC-LOGIN-001 — Botón de acceso deshabilitado con campos vacíos

| Campo | Detalle |
| --- | --- |
| Prioridad | Media |
| Tipo | Negativa / validación |
| Precondición | Estar en `/auth/login`. |

| # | Paso | Resultado esperado |
| --- | --- | --- |
| 1 | Dejar vacíos los campos **Email** y **Contraseña**. | Los campos permanecen vacíos. |
| 2 | Revisar el botón **Iniciar Sesión**. | El botón se muestra deshabilitado y no permite el envío de un formulario vacío. |
