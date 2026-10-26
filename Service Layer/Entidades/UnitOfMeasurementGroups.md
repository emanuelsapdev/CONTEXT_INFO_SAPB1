# UnitOfMeasurementGroups — Grupos de unidades de medida

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UnitOfMeasurementGroups`
- **Descripción (ES):** Grupos de unidades de medida
- **Entity type:** `UnitOfMeasurementGroup`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OUGP](../../Tablas%20SAP%20B1/OUGP.md), [UGP1](../../Tablas%20SAP%20B1/UGP1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UnitOfMeasurementGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UnitOfMeasurementGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/UnitOfMeasurementGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/UnitOfMeasurementGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UnitOfMeasurementGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UnitOfMeasurementGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UnitOfMeasurementGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `BaseUoM` | Edm.Int32 | Yes | Base Uo M | Unidad de medida base |
| 5 | `UoMGroupDefinitionCollection` | Collection([UoMGroupDefinition](../Tipos-Complejos/UoMGroupDefinition.md)) | Yes | Uo M Group Definition Collection | Colección de definiciones del grupo de unidades de medida |

## Navigation properties (4)

Use `GET /b1s/v2/UnitOfMeasurementGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ItemGroups` | Collection([ItemGroups](../Entidades/ItemGroups.md)) | [ItemGroups](ItemGroups.md) |  | Grupos de artículos |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | BaseUoM → AbsEntry | Unidades de medida |
