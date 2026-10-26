# AlternateCatNum — Números de catálogo de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AlternateCatNum`
- **Descripción (ES):** Números de catálogo de socios de negocios
- **Entity type:** `AlternateCatNum` (open type: accepts dynamic/UDF properties)
- **Key:** `ItemCode` (Edm.String), `CardCode` (Edm.String), `Substitute` (Edm.String)
- **DB tables (main / lines):** [OSCN](../../Tablas%20SAP%20B1/OSCN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AlternateCatNum?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AlternateCatNum/$count` | Contar |
| Get by key | `GET /b1s/v2/AlternateCatNum(ItemCode='value',CardCode='value',Substitute='value')` | Obtener por clave |
| Create | `POST /b1s/v2/AlternateCatNum` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AlternateCatNum(ItemCode='value',CardCode='value',Substitute='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AlternateCatNum(ItemCode='value',CardCode='value',Substitute='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AlternateCatNum(ItemCode='value',CardCode='value',Substitute='value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` 🔑 | Edm.String | No | Item Code | Código de artículo |
| 2 | `CardCode` 🔑 | Edm.String | No | Card Code | Código del socio de negocios |
| 3 | `Substitute` 🔑 | Edm.String | No | Substitute | Sustituto |
| 4 | `DisplayBPCatalogNumber` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Business Partner Catalog Number | Mostrar número de catálogo del socio de negocios |
| 5 | `IsDefault` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Default | Es predeterminado |
| 6 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (2)

Use `GET /b1s/v2/AlternateCatNum(ItemCode='value',CardCode='value',Substitute='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
