# Teams — Equipos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Teams`
- **Descripción (ES):** Equipos
- **Entity type:** `Team` (open type: accepts dynamic/UDF properties)
- **Key:** `TeamID` (Edm.Int32)
- **DB tables (main / lines):** [OHTM](../../Tablas%20SAP%20B1/OHTM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Teams?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Teams/$count` | Contar |
| Get by key | `GET /b1s/v2/Teams(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Teams` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Teams(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Teams(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Teams(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TeamID` 🔑 | Edm.Int32 | No | Team ID | ID de equipo |
| 2 | `TeamName` | Edm.String | Yes | Team Name | Nombre del equipo |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `TeamMembers` | Collection([TeamMember](../Tipos-Complejos/TeamMember.md)) | Yes | Team Members | Miembros del equipo |
