# Territories — Territorios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Territories`
- **Descripción (ES):** Territorios
- **Entity type:** `Territory` (open type: accepts dynamic/UDF properties)
- **Key:** `TerritoryID` (Edm.Int32)
- **DB tables (main / lines):** [OTER](../../Tablas%20SAP%20B1/OTER.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Territories?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Territories/$count` | Contar |
| Get by key | `GET /b1s/v2/Territories(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Territories` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Territories(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Territories(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Territories(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TerritoryID` 🔑 | Edm.Int32 | No | Territory ID | ID de territorio |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `LocationIndex` | Edm.Int32 | Yes | Location Index | Índice de ubicación |
| 4 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 5 | `Parent` | Edm.Int32 | Yes | Parent | Padre |

## Navigation properties (4)

Use `GET /b1s/v2/Territories(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `ProjectManagements` | Collection([PM_ProjectDocumentData](../Entidades/ProjectManagements.md)) | [ProjectManagements](ProjectManagements.md) |  | Gestión de proyectos |
