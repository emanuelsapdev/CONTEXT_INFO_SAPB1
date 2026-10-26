# AssetClassLine — Línea de clase de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetClassLine`
- **Descripción (ES):** Línea de clase de activo
- **Description (EN):** Asset Class Line

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `DepreciationAreaID` | Edm.String | Yes | Depreciation Area ID | ID del área de amortización |
| 4 | `ActiveStatus` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active Status | Estado activo |
| 5 | `AccountDetermination` | Edm.String | Yes | Account Determination | Determinación de cuentas |
| 6 | `DepreciationTypeID` | Edm.String | Yes | Depreciation Type ID | ID de tipo de amortización |
| 7 | `UseLife` | Edm.Int32 | Yes | Use Life | Vida útil |

## Used by (properties)

- [AssetClass](../Entidades/AssetClasses.md).`AssetClassCollection`
