# DeductionTaxSubGroups — Subgrupos de deducción de retenciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DeductionTaxSubGroups`
- **Descripción (ES):** Subgrupos de deducción de retenciones
- **Entity type:** `DeductionTaxSubGroup`
- **Key:** `GroupCode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DeductionTaxSubGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DeductionTaxSubGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/DeductionTaxSubGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DeductionTaxSubGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DeductionTaxSubGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DeductionTaxSubGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DeductionTaxSubGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `GroupCode` 🔑 | Edm.String | No | Group Code | Código de grupo |
| 2 | `GroupName` | Edm.String | Yes | Group Name | Nombre del grupo |

## Navigation properties (1)

Use `GET /b1s/v2/DeductionTaxSubGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `DeductionTaxGroups` | Collection([DeductionTaxGroup](../Entidades/DeductionTaxGroups.md)) | [DeductionTaxGroups](DeductionTaxGroups.md) |  | Grupos de deducción de retenciones |
