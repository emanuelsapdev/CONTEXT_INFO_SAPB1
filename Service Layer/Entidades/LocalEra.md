# LocalEra — Era local

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `LocalEra`
- **Descripción (ES):** Era local
- **Entity type:** `LocalEra` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OJPE](../../Tablas%20SAP%20B1/OJPE.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/LocalEra?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/LocalEra/$count` | Contar |
| Get by key | `GET /b1s/v2/LocalEra('value')` | Obtener por clave |
| Create | `POST /b1s/v2/LocalEra` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/LocalEra('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/LocalEra('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/LocalEra('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EraName` | Edm.String | Yes | Era Name | Nombre de la era |
| 2 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 3 | `Code` 🔑 | Edm.String | No | Code | Código |
