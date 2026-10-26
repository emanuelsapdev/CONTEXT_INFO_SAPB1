# AssetClasses — Clases de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AssetClasses`
- **Descripción (ES):** Clases de activos
- **Entity type:** `AssetClass`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OACS](../../Tablas%20SAP%20B1/OACS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AssetClasses?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AssetClasses/$count` | Contar |
| Get by key | `GET /b1s/v2/AssetClasses('value')` | Obtener por clave |
| Create | `POST /b1s/v2/AssetClasses` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AssetClasses('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AssetClasses('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AssetClasses('value')` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `AssetType` | [AssetTypeEnum](../Enums/AssetTypeEnum.md) | Yes | Asset Type | Tipo de activo |
| 4 | `ValueLimitFrom` | Edm.Double | Yes | Value Limit From | Límite de valor desde |
| 5 | `ValueLimitTo` | Edm.Double | Yes | Value Limit To | Límite de valor hasta |
| 6 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 7 | `AttributeGroup` | Edm.Int32 | Yes | Attribute Group | Grupo de atributos |
| 8 | `AssetClassCollection` | Collection([AssetClassLine](../Tipos-Complejos/AssetClassLine.md)) | Yes | Asset Class Collection | Colección de clases de activo |

## Navigation properties (3)

Use `GET /b1s/v2/AssetClasses('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `AttributeGroup2` | [AttributeGroup](../Entidades/AttributeGroups.md) | [AttributeGroups](AttributeGroups.md) | AttributeGroup → Code | Grupos de atributos |
