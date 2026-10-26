# ExceptionalEvents — Eventos excepcionales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ExceptionalEvents`
- **Descripción (ES):** Eventos excepcionales
- **Entity type:** `ExceptionalEvent`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OEEV](../../Tablas%20SAP%20B1/OEEV.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ExceptionalEvents?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ExceptionalEvents/$count` | Contar |
| Get by key | `GET /b1s/v2/ExceptionalEvents('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ExceptionalEvents` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ExceptionalEvents('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ExceptionalEvents('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ExceptionalEvents('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
