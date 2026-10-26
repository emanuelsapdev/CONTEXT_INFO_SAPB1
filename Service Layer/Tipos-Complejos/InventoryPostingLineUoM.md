# InventoryPostingLineUoM — Unidades de medida de líneas de la contabilización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryPostingLineUoM`
- **Descripción (ES):** Unidades de medida de líneas de la contabilización
- **Description (EN):** Inventory Posting Line Uo M
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ChildNumber` | Edm.Int32 | Yes | Child Number | Número de hijo |
| 4 | `UoMCountedQuantity` | Edm.Double | Yes | Uo M Counted Quantity | Cantidad contada en unidad de medida |
| 5 | `ItemsPerUnit` | Edm.Double | Yes | Items Per Unit | Artículos por unidad |
| 6 | `CountedQuantity` | Edm.Double | Yes | Counted Quantity | Cantidad contada |
| 7 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 8 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |

## Used by (properties)

- [InventoryPostingLine](InventoryPostingLine.md).`InventoryPostingLineUoMs`
