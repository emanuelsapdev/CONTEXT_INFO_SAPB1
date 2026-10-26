# RecurringTransactionTemplates — Plantillas de transacciones recurrentes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `RecurringTransactionTemplates`
- **Descripción (ES):** Plantillas de transacciones recurrentes
- **Entity type:** `RecurringTransactionTemplate`
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [ORCP](../../Tablas%20SAP%20B1/ORCP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/RecurringTransactionTemplates?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/RecurringTransactionTemplates/$count` | Contar |
| Get by key | `GET /b1s/v2/RecurringTransactionTemplates(1)` | Obtener por clave |
| Create | `POST /b1s/v2/RecurringTransactionTemplates` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/RecurringTransactionTemplates(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/RecurringTransactionTemplates(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/RecurringTransactionTemplates(1)` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `TemplateCode` | Edm.String | Yes | Template Code | Código de plantilla |
| 3 | `TemplateDescription` | Edm.String | Yes | Template Description | Descripción de la plantilla |
| 4 | `DocumentObjectType` | [DocumentObjectTypeEnum](../Enums/DocumentObjectTypeEnum.md) | Yes | Document Object Type | Tipo de objeto del documento |
| 5 | `DraftEntry` | Edm.Int32 | Yes | Draft Entry | Entrada del borrador |
| 6 | `Frequency` | [RecurringTransactionTemplateFrequencyEnum](../Enums/RecurringTransactionTemplateFrequencyEnum.md) | Yes | Frequency | Frecuencia |
| 7 | `Remind` | [RecurringTransactionTemplateRemindEnum](../Enums/RecurringTransactionTemplateRemindEnum.md) | Yes | Remind | Recordar |
| 8 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 9 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 10 | `PriceUpdate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Price Update | Actualización de precios |
| 11 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |

## Navigation properties (1)

Use `GET /b1s/v2/RecurringTransactionTemplates(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
