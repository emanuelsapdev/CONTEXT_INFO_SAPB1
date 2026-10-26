# UserPermissionItem — Elemento de autorización de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserPermissionItem`
- **Descripción (ES):** Elemento de autorización de usuario
- **Description (EN):** User Permission Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.Int32 | Yes | User Code | Código de usuario |
| 2 | `PermissionID` | Edm.String | Yes | Permission ID | ID de permiso |
| 3 | `Permission` | [BoPermission](../Enums/BoPermission.md) | Yes | Permission | Permiso |
| 4 | `EffectivePermission` | [BoPermission](../Enums/BoPermission.md) | Yes | Effective Permission | Permiso efectivo |

## Used by (properties)

- [User](../Entidades/Users.md).`UserPermission`
