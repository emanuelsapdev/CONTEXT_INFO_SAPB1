# AttributeGroups — Grupos de atributos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AttributeGroups`
- **Descripción (ES):** Grupos de atributos
- **Entity type:** `AttributeGroup`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AttributeGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AttributeGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/AttributeGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AttributeGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AttributeGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AttributeGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AttributeGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 4 | `AttributeGroupCollection` | Collection([AttributeGroupLine](../Tipos-Complejos/AttributeGroupLine.md)) | Yes | Attribute Group Collection | Colección de grupos de atributos |

## Navigation properties (1)

Use `GET /b1s/v2/AttributeGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `AssetClasses` | Collection([AssetClass](../Entidades/AssetClasses.md)) | [AssetClasses](AssetClasses.md) |  | Clases de activos |
