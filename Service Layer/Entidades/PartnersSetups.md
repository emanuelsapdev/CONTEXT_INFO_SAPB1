# PartnersSetups — Configuración de socios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PartnersSetups`
- **Descripción (ES):** Configuración de socios
- **Entity type:** `PartnersSetup`
- **Key:** `PartnerID` (Edm.Int32)
- **DB tables (main / lines):** [OPRT](../../Tablas%20SAP%20B1/OPRT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PartnersSetups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PartnersSetups/$count` | Contar |
| Get by key | `GET /b1s/v2/PartnersSetups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PartnersSetups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PartnersSetups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PartnersSetups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PartnersSetups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PartnerID` 🔑 | Edm.Int32 | No | Partner ID | ID del socio |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `DefaultRelationship` | Edm.Int32 | Yes | Default Relationship | Relación predeterminada |
| 4 | `RelatedBP` | Edm.String | Yes | Related Business Partner | Socio de negocios relacionado |
| 5 | `Details` | Edm.String | Yes | Details | Detalles |

## Navigation properties (2)

Use `GET /b1s/v2/PartnersSetups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Relationship` | [Relationship](../Entidades/Relationships.md) | [Relationships](Relationships.md) | DefaultRelationship → RelationshipCode | Relaciones |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | RelatedBP → CardCode | Socio de negocios |
