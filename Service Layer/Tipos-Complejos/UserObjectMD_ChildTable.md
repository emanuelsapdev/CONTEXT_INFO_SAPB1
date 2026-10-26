# UserObjectMD_ChildTable — Tablas hijas del UDO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserObjectMD_ChildTable`
- **Descripción (ES):** Tablas hijas del UDO
- **Description (EN):** User Object Metadata Child Table
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SonNumber` | Edm.Int32 | Yes | Son Number | Número de hijo |
| 2 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 3 | `LogTableName` | Edm.String | Yes | Log Table Name | Nombre de la tabla de registro |
| 4 | `Code` | Edm.String | Yes | Code | Código |
| 5 | `ObjectName` | Edm.String | Yes | Object Name | Nombre del objeto |

## Used by (properties)

- [UserObjectsMD](../Entidades/UserObjectsMD.md).`UserObjectMD_ChildTables`
