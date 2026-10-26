# BusinessPartnerGroups — Grupos de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BusinessPartnerGroups`
- **Descripción (ES):** Grupos de socios de negocios
- **Entity type:** `BusinessPartnerGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OCRG](../../Tablas%20SAP%20B1/OCRG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BusinessPartnerGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BusinessPartnerGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/BusinessPartnerGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BusinessPartnerGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BusinessPartnerGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BusinessPartnerGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BusinessPartnerGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Type` | [BoBusinessPartnerGroupTypes](../Enums/BoBusinessPartnerGroupTypes.md) | Yes | Type | Tipo |

## Navigation properties (2)

Use `GET /b1s/v2/BusinessPartnerGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
