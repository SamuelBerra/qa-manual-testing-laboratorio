# Portafolio QA — Pruebas manuales de Laboratorio de Testing

## Descripción

Pruebas funcionales manuales realizadas sobre [Laboratorio de Testing](https://www.laboratoriodetesting.com/), una tienda de práctica con catálogo, carrito, checkout y autenticación.

## Objetivo

Validar los flujos públicos principales de una compra: carga de la página inicial, navegación al producto, agregado al carrito, acceso al checkout y restricción de acceso para usuarios sin sesión.

## Resultados de la ronda

| Métrica | Resultado |
| --- | --- |
| Casos planificados | 5 |
| Casos ejecutados | 5 |
| Aprobados | 5 |
| Fallidos | 0 |
| Bloqueados | 0 |

## Alcance

| Incluido | Fuera de alcance |
| --- | --- |
| Página de inicio | Creación de cuentas |
| Detalle de producto | Compra final y pago |
| Carrito | Recuperación de contraseña |
| Acceso al checkout | Integraciones externas |
| Validación inicial de login | |

## Documentación

| Archivo | Contenido |
| --- | --- |
| [Casos de prueba](test-cases.md) | Escenarios, precondiciones, pasos y resultados esperados. |
| [Ejecución de pruebas](test-execution.md) | Resultado observado y estado de cada prueba. |

## Entorno

| Campo | Detalle |
| --- | --- |
| Aplicación | Laboratorio de Testing |
| URL | https://www.laboratoriodetesting.com/ |
| Fecha de ejecución | 2026-09-10 |
| Navegador | Chromium |

> La ronda no incluye una compra real ni ingreso de datos personales. El acceso al checkout se validó solamente hasta la redirección al login de un usuario no autenticado.
