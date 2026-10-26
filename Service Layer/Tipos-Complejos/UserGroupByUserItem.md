# UserGroupByUserItem — Grupo del usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserGroupByUserItem`
- **Descripción (ES):** Grupo del usuario
- **Description (EN):** User Group By User Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `USERId` | Edm.Int32 | Yes | USER ID | ID de usuario |
| 2 | `GroupId` | Edm.Int32 | Yes | Group ID | ID de grupo |
| 3 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 4 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |

## Used by (properties)

- [User](../Entidades/Users.md).`UserGroupByUser`
