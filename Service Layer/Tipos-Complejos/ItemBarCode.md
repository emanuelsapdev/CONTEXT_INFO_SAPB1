# ItemBarCode — Código de barras del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemBarCode`
- **Descripción (ES):** Código de barras del artículo
- **Description (EN):** Item Bar Code
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 3 | `Barcode` | Edm.String | Yes | Barcode | Código de barras |
| 4 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemBarCodeCollection`
