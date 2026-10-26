# DepreciationTypePools — Grupos de tipos de amortización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DepreciationTypePools`
- **Descripción (ES):** Grupos de tipos de amortización
- **Entity type:** `DepreciationTypePool`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [ODPP](../../Tablas%20SAP%20B1/ODPP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DepreciationTypePools?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DepreciationTypePools/$count` | Contar |
| Get by key | `GET /b1s/v2/DepreciationTypePools('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DepreciationTypePools` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DepreciationTypePools('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DepreciationTypePools('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DepreciationTypePools('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/DepreciationTypePools('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `DepreciationTypes` | Collection([DepreciationType](../Entidades/DepreciationTypes.md)) | [DepreciationTypes](DepreciationTypes.md) |  | Tipos de amortización |
