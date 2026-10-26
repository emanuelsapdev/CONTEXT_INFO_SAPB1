# FixedAssetValues — Valores del activo fijo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FixedAssetValues`
- **Descripción (ES):** Valores del activo fijo
- **Description (EN):** Fixed Asset Values

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionType` | [AssetTransactionTypeEnum](../Enums/AssetTransactionTypeEnum.md) | Yes | Transaction Type | Tipo de transacción |
| 2 | `AcquisitionCost` | Edm.Double | Yes | Acquisition Cost | Costo de adquisición |
| 3 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 4 | `DepreciationValue` | Edm.Double | Yes | Depreciation Value | Valor de amortización |
| 5 | `NetBookValue` | Edm.Double | Yes | Net Book Value | Valor neto contable |
| 6 | `OrdinaryDepreciationValue` | Edm.Double | Yes | Ordinary Depreciation Value | Valor de amortización ordinaria |
| 7 | `UnplanedDepreciationValue` | Edm.Double | Yes | Unplaned Depreciation Value | Valor de amortización no planificada |
| 8 | `SpecialDepreciationValue` | Edm.Double | Yes | Special Depreciation Value | Valor de amortización especial |
| 9 | `WriteUp` | Edm.Double | Yes | Write Up | Revalorización (write-up) |
| 10 | `Appreciation` | Edm.Double | Yes | Appreciation | Revalorización |

## Used by (service operations)

- [`FixedAssetItemsService_GetAssetValuesList`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_getassetvalueslist)
