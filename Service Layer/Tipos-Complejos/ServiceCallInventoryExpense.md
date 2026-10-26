# ServiceCallInventoryExpense — Gastos de inventario de la llamada de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceCallInventoryExpense`
- **Descripción (ES):** Gastos de inventario de la llamada de servicio
- **Description (EN):** Service Call Inventory Expense
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `PartType` | [BoSvcExpPartTypes](../Enums/BoSvcExpPartTypes.md) | Yes | Part Type | Tipo de pieza |
| 3 | `DocumentType` | [BoSvcEpxDocTypes](../Enums/BoSvcEpxDocTypes.md) | Yes | Document Type | Tipo de documento |
| 4 | `DocumentPostingDate` | Edm.DateTimeOffset | Yes | Document Posting Date | Fecha de contabilización del documento |
| 5 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 6 | `StockTransferDirection` | [BoStckTrnDir](../Enums/BoStckTrnDir.md) | Yes | Stock Transfer Direction | Dirección de la transferencia de stock |
| 7 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |

## Used by (properties)

- [ServiceCall](../Entidades/ServiceCalls.md).`ServiceCallInventoryExpenses`
