# InventoryOpeningBalanceCCDNumber — Números de declaración aduanera del saldo inicial

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryOpeningBalanceCCDNumber`
- **Descripción (ES):** Números de declaración aduanera del saldo inicial
- **Description (EN):** Inventory Opening Balance CCD Number

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 2 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 3 | `CCDNumber` | Edm.String | Yes | CCD Number | Número de declaración aduanera de carga |
| 4 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 5 | `CountryOfOrigin` | Edm.String | Yes | Country Of Origin | País de origen |
| 6 | `SubLineNumber` | Edm.Int32 | Yes | Sub Line Number | Número de sublínea |
| 7 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 8 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 9 | `ChildNumber` | Edm.Int32 | Yes | Child Number | Número de hijo |

## Used by (properties)

- [InventoryOpeningBalanceLine](InventoryOpeningBalanceLine.md).`InventoryOpeningBalanceCCDNumbers`
