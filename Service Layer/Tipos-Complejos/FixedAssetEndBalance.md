# FixedAssetEndBalance — Saldo final del activo fijo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FixedAssetEndBalance`
- **Descripción (ES):** Saldo final del activo fijo
- **Description (EN):** Fixed Asset End Balance

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `HistoricalAPC` | Edm.Double | Yes | Historical APC | Costo de adquisición histórico |
| 2 | `AcquisitionCost` | Edm.Double | Yes | Acquisition Cost | Costo de adquisición |
| 3 | `NetBookValue` | Edm.Double | Yes | Net Book Value | Valor neto contable |
| 4 | `HistoricalNBV` | Edm.Double | Yes | Historical NBV | Valor neto contable histórico |
| 5 | `OrdinaryDepreciationValue` | Edm.Double | Yes | Ordinary Depreciation Value | Valor de amortización ordinaria |
| 6 | `UnplanedDepreciationValue` | Edm.Double | Yes | Unplaned Depreciation Value | Valor de amortización no planificada |
| 7 | `SpecialDepreciationValue` | Edm.Double | Yes | Special Depreciation Value | Valor de amortización especial |
| 8 | `WriteUp` | Edm.Double | Yes | Write Up | Revalorización (write-up) |
| 9 | `SalvageValue` | Edm.Double | Yes | Salvage Value | Valor residual |
| 10 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |

## Used by (service operations)

- [`FixedAssetItemsService_GetAssetEndBalance`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_getassetendbalance)
- [`FixedAssetItemsService_UpdateAssetEndBalance`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_updateassetendbalance)
