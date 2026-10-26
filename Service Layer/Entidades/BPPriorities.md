# BPPriorities — Prioridades de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BPPriorities`
- **Descripción (ES):** Prioridades de socios de negocios
- **Entity type:** `BPPriority` (open type: accepts dynamic/UDF properties)
- **Key:** `Priority` (Edm.Int32)
- **DB tables (main / lines):** [OBPP](../../Tablas%20SAP%20B1/OBPP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BPPriorities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BPPriorities/$count` | Contar |
| Get by key | `GET /b1s/v2/BPPriorities(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BPPriorities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BPPriorities(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BPPriorities(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BPPriorities(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Priority` 🔑 | Edm.Int32 | No | Priority | Prioridad |
| 2 | `PriorityDescription` | Edm.String | Yes | Priority Description | Descripción de prioridad |

## Navigation properties (1)

Use `GET /b1s/v2/BPPriorities(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
