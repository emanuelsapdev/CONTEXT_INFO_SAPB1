# TSRExceptionalEvents — Eventos excepcionales TSR

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TSRExceptionalEvents`
- **Descripción (ES):** Eventos excepcionales TSR
- **Entity type:** `TSRExceptionalEvent`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TSRExceptionalEvents?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TSRExceptionalEvents/$count` | Contar |
| Get by key | `GET /b1s/v2/TSRExceptionalEvents('value')` | Obtener por clave |
| Create | `POST /b1s/v2/TSRExceptionalEvents` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TSRExceptionalEvents('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TSRExceptionalEvents('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/TSRExceptionalEvents('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
