# UserPermissionForm — Formularios de permisos del usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserPermissionForm`
- **Descripción (ES):** Formularios de permisos del usuario
- **Description (EN):** User Permission Form
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormType` | Edm.String | Yes | Form Type | Tipo de formulario |
| 2 | `DisplayOrder` | Edm.Int32 | Yes | Display Order | Orden de visualización |
| 3 | `PermissionID` | Edm.String | Yes | Permission ID | ID de permiso |

## Used by (properties)

- [UserPermissionTree](../Entidades/UserPermissionTree.md).`UserPermissionForms`
