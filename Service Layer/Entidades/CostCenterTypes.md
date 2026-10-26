# CostCenterTypes — Tipos de centro de costo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CostCenterTypes`
- **Descripción (ES):** Tipos de centro de costo
- **Entity type:** `CostCenterType` (open type: accepts dynamic/UDF properties)
- **Key:** `CostCenterTypeCode` (Edm.String)
- **DB tables (main / lines):** [OCCT](../../Tablas%20SAP%20B1/OCCT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CostCenterTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CostCenterTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/CostCenterTypes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CostCenterTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CostCenterTypes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CostCenterTypes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CostCenterTypes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CostCenterTypeCode` 🔑 | Edm.String | No | Cost Center Type Code | Código de tipo de centro de costo |
| 2 | `CostCenterTypeName` | Edm.String | Yes | Cost Center Type Name | Nombre del tipo de centro de costo |

## Navigation properties (1)

Use `GET /b1s/v2/CostCenterTypes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ProfitCenters` | Collection([ProfitCenter](../Entidades/ProfitCenters.md)) | [ProfitCenters](ProfitCenters.md) |  | Centros de beneficio/costo |
