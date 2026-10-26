# SalesStages — Etapas de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesStages`
- **Descripción (ES):** Etapas de venta
- **Entity type:** `SalesStage` (open type: accepts dynamic/UDF properties)
- **Key:** `SequenceNo` (Edm.Int32)
- **DB tables (main / lines):** [OOST](../../Tablas%20SAP%20B1/OOST.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesStages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesStages/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesStages(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesStages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesStages(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesStages(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesStages(1)` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequenceNo` 🔑 | Edm.Int32 | No | Sequence Number | Número de secuencia |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Stageno` | Edm.Int32 | Yes | Stageno | Número de etapa |
| 4 | `ClosingPercentage` | Edm.Double | Yes | Closing Percentage | Porcentaje de cierre |
| 5 | `Cancelled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cancelled | Cancelado |
| 6 | `IsSales` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Sales | Es de ventas |
| 7 | `IsPurchasing` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Purchasing | Es de compras |

## Navigation properties (1)

Use `GET /b1s/v2/SalesStages(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
