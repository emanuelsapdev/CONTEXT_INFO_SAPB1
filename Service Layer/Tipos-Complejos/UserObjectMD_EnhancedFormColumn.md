# UserObjectMD_EnhancedFormColumn — Columnas del formulario mejorado del UDO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserObjectMD_EnhancedFormColumn`
- **Descripción (ES):** Columnas del formulario mejorado del UDO
- **Description (EN):** User Object Metadata Enhanced Form Column
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `ColumnNumber` | Edm.Int32 | Yes | Column Number | Número de columna |
| 3 | `ChildNumber` | Edm.Int32 | Yes | Child Number | Número de hijo |
| 4 | `ColumnAlias` | Edm.String | Yes | Column Alias | Alias de columna |
| 5 | `ColumnDescription` | Edm.String | Yes | Column Description | Descripción de columna |
| 6 | `ColumnIsUsed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Column Is Used | Columna en uso |
| 7 | `Editable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Editable | Editable |

## Used by (properties)

- [UserObjectsMD](../Entidades/UserObjectsMD.md).`UserObjectMD_EnhancedFormColumns`
