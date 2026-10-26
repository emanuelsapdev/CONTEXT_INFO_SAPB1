# WeightMeasures — Unidades de peso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WeightMeasures`
- **Descripción (ES):** Unidades de peso
- **Entity type:** `WeightMeasure` (open type: accepts dynamic/UDF properties)
- **Key:** `UnitCode` (Edm.Int32)
- **DB tables (main / lines):** [OWGT](../../Tablas%20SAP%20B1/OWGT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WeightMeasures?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WeightMeasures/$count` | Contar |
| Get by key | `GET /b1s/v2/WeightMeasures(1)` | Obtener por clave |
| Create | `POST /b1s/v2/WeightMeasures` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WeightMeasures(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WeightMeasures(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/WeightMeasures(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UnitCode` 🔑 | Edm.Int32 | No | Unit Code | Código de unidad |
| 2 | `UnitDisplay` | Edm.String | Yes | Unit Display | Visualización de unidad |
| 3 | `UnitName` | Edm.String | Yes | Unit Name | Nombre de la unidad |
| 4 | `UnitWeightinmg` | Edm.Double | Yes | Unit Weightinmg | Peso de la unidad en mg |

## Navigation properties (1)

Use `GET /b1s/v2/WeightMeasures(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
