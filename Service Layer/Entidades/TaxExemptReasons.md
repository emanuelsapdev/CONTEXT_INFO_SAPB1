# TaxExemptReasons — Motivos de exención de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TaxExemptReasons`
- **Descripción (ES):** Motivos de exención de impuestos
- **Entity type:** `TaxExemptReason`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [TXRE](../../Tablas%20SAP%20B1/TXRE.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TaxExemptReasons?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TaxExemptReasons/$count` | Contar |
| Get by key | `GET /b1s/v2/TaxExemptReasons('value')` | Obtener por clave |
| Create | `POST /b1s/v2/TaxExemptReasons` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TaxExemptReasons('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TaxExemptReasons('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/TaxExemptReasons('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/TaxExemptReasons('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `VatGroups` | Collection([VatGroup](../Entidades/VatGroups.md)) | [VatGroups](VatGroups.md) |  | Grupos de impuestos (IVA) |
