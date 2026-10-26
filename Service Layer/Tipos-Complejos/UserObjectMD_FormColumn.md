# UserObjectMD_FormColumn — Columnas del formulario del UDO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserObjectMD_FormColumn`
- **Descripción (ES):** Columnas del formulario del UDO
- **Description (EN):** User Object Metadata Form Column
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormColumnAlias` | Edm.String | Yes | Form Column Alias | Alias de columna del formulario |
| 2 | `FormColumnDescription` | Edm.String | Yes | Form Column Description | Descripción de columna del formulario |
| 3 | `FormColumnNumber` | Edm.Int32 | Yes | Form Column Number | Número de columna del formulario |
| 4 | `SonNumber` | Edm.Int32 | Yes | Son Number | Número de hijo |
| 5 | `Code` | Edm.String | Yes | Code | Código |
| 6 | `Editable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Editable | Editable |

## Used by (properties)

- [UserObjectsMD](../Entidades/UserObjectsMD.md).`UserObjectMD_FormColumns`
