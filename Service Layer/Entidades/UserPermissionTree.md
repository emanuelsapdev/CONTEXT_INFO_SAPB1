# UserPermissionTree — Árbol de autorizaciones de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserPermissionTree`
- **Descripción (ES):** Árbol de autorizaciones de usuario
- **Entity type:** `UserPermissionTree` (open type: accepts dynamic/UDF properties)
- **Key:** `PermissionID` (Edm.String)
- **DB tables (main / lines):** [OUPT](../../Tablas%20SAP%20B1/OUPT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 9 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserPermissionTree?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserPermissionTree/$count` | Contar |
| Get by key | `GET /b1s/v2/UserPermissionTree('value')` | Obtener por clave |
| Create | `POST /b1s/v2/UserPermissionTree` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserPermissionTree('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserPermissionTree('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserPermissionTree('value')` (only if the B1 object allows removal) | Borrar |

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 2 | `DisplayOrder` | Edm.Int32 | Yes | Display Order | Orden de visualización |
| 3 | `PermissionID` 🔑 | Edm.String | No | Permission ID | ID de permiso |
| 4 | `Options` | [BoUPTOptions](../Enums/BoUPTOptions.md) | Yes | Options | Opciones |
| 5 | `Name` | Edm.String | Yes | Name | Nombre |
| 6 | `Levels` | Edm.Int32 | Yes | Levels | Niveles |
| 7 | `IsItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Item | Es artículo |
| 8 | `ParentID` | Edm.String | Yes | Parent ID | ID del padre |
| 9 | `UserPermissionForms` | Collection([UserPermissionForm](../Tipos-Complejos/UserPermissionForm.md)) | Yes | User Permission Forms | Formularios de permisos del usuario |

## Navigation properties (1)

Use `GET /b1s/v2/UserPermissionTree('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
