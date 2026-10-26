# CashFlowLineItems — Partidas de flujo de caja

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CashFlowLineItems`
- **Descripción (ES):** Partidas de flujo de caja
- **Entity type:** `CashFlowLineItem`
- **Key:** `LineItemID` (Edm.Int32)
- **DB tables (main / lines):** [OCFW](../../Tablas%20SAP%20B1/OCFW.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CashFlowLineItems?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CashFlowLineItems/$count` | Contar |
| Get by key | `GET /b1s/v2/CashFlowLineItems(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CashFlowLineItems` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CashFlowLineItems(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CashFlowLineItems(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CashFlowLineItems(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineItemID` 🔑 | Edm.Int32 | No | Line Item ID | ID de partida |
| 2 | `LineItemName` | Edm.String | Yes | Line Item Name | Nombre de partida |
| 3 | `ActiveLineItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active Line Item | Partida activa |
| 4 | `ParentArticle` | Edm.Int32 | Yes | Parent Article | Artículo padre |
| 5 | `Level` | Edm.Int32 | Yes | Level | Nivel |
| 6 | `Drawer` | Edm.Int32 | Yes | Drawer | Librador |
