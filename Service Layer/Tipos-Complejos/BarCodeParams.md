# BarCodeParams — Parámetros de códigos de barras

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BarCodeParams`
- **Descripción (ES):** Parámetros de códigos de barras
- **Description (EN):** Bar Code Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 3 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 4 | `Barcode` | Edm.String | Yes | Barcode | Código de barras |

## Used by (service operations)

- [`BarCodesService_GetList`](../Servicios/BarCodesService.md#barcodesservice_getlist)
