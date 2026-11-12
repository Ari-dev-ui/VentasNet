# Registro de cambios

## Solicitudes y matriz de impacto

| Criterio | INC-001 | CR-002 |
|---|---|---|
| Origen | Error detectado en el cálculo de ventas. | Solicitud del área comercial. |
| Descripción | El total solo considera el precio de una unidad. | Aplicar 10 % de descuento desde un subtotal de S/ 200. |
| Justificación | El total debe incluir todas las unidades compradas. | La promoción debe aplicarse a las compras que alcancen el monto indicado. |
| Requisito | RF-001: calcular el total según precio y cantidad. | RF-002: aplicar el descuento desde S/ 200. |
| Archivos afectados | `src/ventas.py` y `pruebas/casos_prueba.md`. | `src/ventas.py`, `docs/requisitos.md` y `pruebas/casos_prueba.md`. |
| Riesgo | Cobrar menos al vender varias unidades. | Aplicar mal el descuento en el límite de S/ 200. |
| Criterio de aceptación | S/ 50 × 3 unidades = S/ 150. | S/ 150 queda en S/ 150, S/ 200 baja a S/ 180 y S/ 300 baja a S/ 270. |
| Prioridad | Alta, porque afecta el importe de la venta. | Media, porque agrega una regla comercial. |
| Decisión | Aprobada en la simulación académica. | Aprobada en la simulación académica. |
| Responsable | Robles Bernardo Aribert Hans. | Robles Bernardo Aribert Hans. |

## Seguimiento

- **INC-001:** Implementada y verificada mediante CP-001. El programa calculó S/ 150 para 3 unidades de S/ 50.

- **CR-002:** Implementada y verificada mediante CP-002, CP-003 y CP-004. El descuento del 10 % se aplicó desde S/ 200. La compra de S/ 150 mantuvo su total.

## Tabla de trazabilidad

| ID de cambio | Rama | Commit | Pruebas | Versión de entrega |
|---|---|---|---|---|
| INC-001 | `fix/INC-001-total` | `302e6eb` | CP-001 | `v1.1.0` |
| CR-002 | `feature/CR-002-descuento` | `da37d63` | CP-002, CP-003 y CP-004 | `v1.1.0` |