# CycleCountDeterminations — Determinación de recuento cíclico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CycleCountDeterminations`
- **Descripción (ES):** Determinación de recuento cíclico
- **Entity type:** `CycleCountDetermination`
- **Key:** `WarehouseCode` (Edm.String)
- **DB tables (main / lines):** [OCCS](../../Tablas%20SAP%20B1/OCCS.md), [CCS1](../../Tablas%20SAP%20B1/CCS1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CycleCountDeterminations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CycleCountDeterminations/$count` | Contar |
| Get by key | `GET /b1s/v2/CycleCountDeterminations('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CycleCountDeterminations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CycleCountDeterminations('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CycleCountDeterminations('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CycleCountDeterminations('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WarehouseCode` 🔑 | Edm.String | No | Warehouse Code | Código de almacén |
| 2 | `CycleBy` | [CycleCountDeterminationCycleByEnum](../Enums/CycleCountDeterminationCycleByEnum.md) | Yes | Cycle By | Ciclo por |
| 3 | `CycleCountDeterminationSetupCollection` | Collection([CycleCountDeterminationSetup](../Tipos-Complejos/CycleCountDeterminationSetup.md)) | Yes | Cycle Count Determination Setup Collection | Colección de configuración de recuento cíclico |
