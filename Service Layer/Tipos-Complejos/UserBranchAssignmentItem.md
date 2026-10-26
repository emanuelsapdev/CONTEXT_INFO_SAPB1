# UserBranchAssignmentItem — Asignación de sucursal al usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserBranchAssignmentItem`
- **Descripción (ES):** Asignación de sucursal al usuario
- **Description (EN):** User Branch Assignment Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 2 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |

## Used by (properties)

- [User](../Entidades/Users.md).`UserBranchAssignment`
