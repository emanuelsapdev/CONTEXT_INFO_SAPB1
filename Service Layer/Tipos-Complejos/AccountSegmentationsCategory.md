# AccountSegmentationsCategory — Categoría de segmentación de cuentas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AccountSegmentationsCategory`
- **Descripción (ES):** Categoría de segmentación de cuentas
- **Description (EN):** Account Segmentations Category
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SegmentID` | Edm.Int32 | Yes | Segment ID | ID de segmento |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `ShortName` | Edm.String | Yes | Short Name | Nombre corto |

## Used by (properties)

- [AccountSegmentation](../Entidades/AccountSegmentations.md).`AccountSegmentationsCategories`
