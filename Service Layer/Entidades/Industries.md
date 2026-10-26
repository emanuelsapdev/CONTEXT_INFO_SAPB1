# Industries — Ramos (industrias)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Industries`
- **Descripción (ES):** Ramos (industrias)
- **Entity type:** `Industry` (open type: accepts dynamic/UDF properties)
- **Key:** `IndustryCode` (Edm.Int32)
- **DB tables (main / lines):** [OOND](../../Tablas%20SAP%20B1/OOND.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Industries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Industries/$count` | Contar |
| Get by key | `GET /b1s/v2/Industries(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Industries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Industries(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Industries(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Industries(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `IndustryDescription` | Edm.String | Yes | Industry Description | Descripción del ramo |
| 2 | `IndustryName` | Edm.String | Yes | Industry Name | Nombre del ramo |
| 3 | `IndustryCode` 🔑 | Edm.Int32 | No | Industry Code | Código de ramo |

## Navigation properties (3)

Use `GET /b1s/v2/Industries(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `ProjectManagements` | Collection([PM_ProjectDocumentData](../Entidades/ProjectManagements.md)) | [ProjectManagements](ProjectManagements.md) |  | Gestión de proyectos |
