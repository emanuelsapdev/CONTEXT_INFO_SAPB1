# MaterialRevaluationSNBParams — Parámetros de revalorización por series/lotes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MaterialRevaluationSNBParams`
- **Descripción (ES):** Parámetros de revalorización por series/lotes
- **Description (EN):** Material Revaluation Serial and Batch Parameters

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SnbAbsEntry` | Edm.Int32 | Yes | Snb Abs Entry | Entrada absoluta de serie/lote |
| 2 | `NewCost` | Edm.Double | Yes | New Cost | Nuevo costo |
| 3 | `DebitCredit` | Edm.Double | Yes | Debit Credit | Debe/haber |
| 4 | `SystemNumber` | Edm.Int32 | Yes | System Number | Número del sistema |
| 5 | `LotNumber` | Edm.String | Yes | Lot Number | Número de lote |
| 6 | `ManufactureNumber` | Edm.String | Yes | Manufacture Number | Número de fabricación |
| 7 | `AdmissionDate` | Edm.DateTimeOffset | Yes | Admission Date | Fecha de admisión |
| 8 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |

## Used by (service operations)

- [`MaterialRevaluationSNBService_Add`](../Servicios/MaterialRevaluationSNBService.md#materialrevaluationsnbservice_add)
- [`MaterialRevaluationSNBService_GetList`](../Servicios/MaterialRevaluationSNBService.md#materialrevaluationsnbservice_getlist)
