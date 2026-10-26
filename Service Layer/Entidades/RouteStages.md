# RouteStages — Etapas de ruta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `RouteStages`
- **Descripción (ES):** Etapas de ruta
- **Entity type:** `RouteStage`
- **Key:** `InternalNumber` (Edm.Int32)
- **DB tables (main / lines):** [ORST](../../Tablas%20SAP%20B1/ORST.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/RouteStages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/RouteStages/$count` | Contar |
| Get by key | `GET /b1s/v2/RouteStages(1)` | Obtener por clave |
| Create | `POST /b1s/v2/RouteStages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/RouteStages(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/RouteStages(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/RouteStages(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalNumber` 🔑 | Edm.Int32 | No | Internal Number | Número interno |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 5 | `GenerationTime` | Edm.TimeOfDay | Yes | Generation Time | Hora de generación |
| 6 | `DateOfUpdate` | Edm.DateTimeOffset | Yes | Date Of Update | Fecha de actualización |
