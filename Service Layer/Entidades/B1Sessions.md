# B1Sessions — Sesiones de SAP Business One

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `B1Sessions`
- **Descripción (ES):** Sesiones de SAP Business One
- **Entity type:** `B1Session`
- **Key:** `SessionId` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/B1Sessions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/B1Sessions/$count` | Contar |
| Get by key | `GET /b1s/v2/B1Sessions('value')` | Obtener por clave |
| Create | `POST /b1s/v2/B1Sessions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/B1Sessions('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/B1Sessions('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/B1Sessions('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Version` | Edm.String | Yes | Version | Versión |
| 2 | `SessionTimeout` | Edm.Int32 | Yes | Session Timeout | Tiempo de expiración de la sesión |
| 3 | `SessionId` 🔑 | Edm.String | No | Session ID | ID de sesión |

## Service operations that use this type

- [`Login`](../Servicios/Global.md#login)
