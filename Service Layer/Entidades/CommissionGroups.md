# CommissionGroups — Grupos de comisiones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CommissionGroups`
- **Descripción (ES):** Grupos de comisiones
- **Entity type:** `CommissionGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `CommissionGroupCode` (Edm.Int32)
- **DB tables (main / lines):** [OCOG](../../Tablas%20SAP%20B1/OCOG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CommissionGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CommissionGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/CommissionGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CommissionGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CommissionGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CommissionGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CommissionGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CommissionGroupCode` 🔑 | Edm.Int32 | No | Commission Group Code | Código de grupo de comisiones |
| 2 | `CommissionGroupName` | Edm.String | Yes | Commission Group Name | Nombre del grupo de comisiones |
| 3 | `CommissionPercentage` | Edm.Double | Yes | Commission Percentage | Porcentaje de comisión |

## Navigation properties (3)

Use `GET /b1s/v2/CommissionGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesPersons` | Collection([SalesPerson](../Entidades/SalesPersons.md)) | [SalesPersons](SalesPersons.md) |  | Empleados del departamento de ventas |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
