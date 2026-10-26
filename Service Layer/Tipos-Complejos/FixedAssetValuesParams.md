# FixedAssetValuesParams — Parámetros de valores de activos fijos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FixedAssetValuesParams`
- **Descripción (ES):** Parámetros de valores de activos fijos
- **Description (EN):** Fixed Asset Values Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `FiscalYear` | Edm.String | Yes | Fiscal Year | Ejercicio fiscal |
| 3 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |

## Used by (service operations)

- [`FixedAssetItemsService_GetAssetEndBalance`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_getassetendbalance)
- [`FixedAssetItemsService_GetAssetValuesList`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_getassetvalueslist)
- [`FixedAssetItemsService_UpdateAssetEndBalance`](../Servicios/FixedAssetItemsService.md#fixedassetitemsservice_updateassetendbalance)
