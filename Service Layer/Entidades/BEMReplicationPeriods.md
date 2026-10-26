# BEMReplicationPeriods — Períodos de replicación BEM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BEMReplicationPeriods`
- **Descripción (ES):** Períodos de replicación BEM
- **Entity type:** `BEMReplicationPeriod`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 9 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BEMReplicationPeriods?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BEMReplicationPeriods/$count` | Contar |
| Get by key | `GET /b1s/v2/BEMReplicationPeriods(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BEMReplicationPeriods` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BEMReplicationPeriods(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BEMReplicationPeriods(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BEMReplicationPeriods(1)` (only if the B1 object allows removal) | Borrar |

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ScopeKey` | Edm.String | Yes | Scope Key | Clave de alcance |
| 3 | `ScopeName` | Edm.String | Yes | Scope Name | Nombre del alcance |
| 4 | `Periodic` | [BEMPeriodicTypeEnum](../Enums/BEMPeriodicTypeEnum.md) | Yes | Periodic | Periódico |
| 5 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 6 | `Status` | [BEMReplicationStatusEnum](../Enums/BEMReplicationStatusEnum.md) | Yes | Status | Estado |
| 7 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 8 | `LastRepId` | Edm.String | Yes | Last Rep ID | ID del último informe |
| 9 | `RepMessage` | Edm.String | Yes | Rep Message | Mensaje del informe |
