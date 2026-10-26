# DeductionTaxGroups — Grupos de deducción de retenciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DeductionTaxGroups`
- **Descripción (ES):** Grupos de deducción de retenciones
- **Entity type:** `DeductionTaxGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `GroupKey` (Edm.Int32)
- **DB tables (main / lines):** [ODDG](../../Tablas%20SAP%20B1/ODDG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DeductionTaxGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DeductionTaxGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/DeductionTaxGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/DeductionTaxGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DeductionTaxGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DeductionTaxGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/DeductionTaxGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `GroupKey` 🔑 | Edm.Int32 | No | Group Key | Clave de grupo |
| 2 | `GroupCode` | [BoDeductionTaxGroupCodeEnum](../Enums/BoDeductionTaxGroupCodeEnum.md) | Yes | Group Code | Código de grupo |
| 3 | `GroupName` | Edm.String | Yes | Group Name | Nombre del grupo |
| 4 | `MaxRedin` | Edm.Double | Yes | Max Redin | Redondeo máximo |
| 5 | `GroupExtendedCode` | Edm.String | Yes | Group Extended Code | Código ampliado del grupo |

## Navigation properties (2)

Use `GET /b1s/v2/DeductionTaxGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DeductionTaxSubGroup` | [DeductionTaxSubGroup](../Entidades/DeductionTaxSubGroups.md) | [DeductionTaxSubGroups](DeductionTaxSubGroups.md) | GroupCode → GroupCode | Subgrupos de deducción de retenciones |
