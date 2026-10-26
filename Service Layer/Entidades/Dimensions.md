# Dimensions — Dimensiones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Dimensions`
- **Descripción (ES):** Dimensiones
- **Entity type:** `Dimension` (open type: accepts dynamic/UDF properties)
- **Key:** `DimensionCode` (Edm.Int32)
- **DB tables (main / lines):** [ODIM](../../Tablas%20SAP%20B1/ODIM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Dimensions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Dimensions/$count` | Contar |
| Get by key | `GET /b1s/v2/Dimensions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Dimensions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Dimensions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Dimensions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Dimensions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DimensionCode` 🔑 | Edm.Int32 | No | Dimension Code | Código de dimensión |
| 2 | `DimensionName` | Edm.String | Yes | Dimension Name | Nombre de la dimensión |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
| 4 | `DimensionDescription` | Edm.String | Yes | Dimension Description | Descripción de la dimensión |

## Navigation properties (2)

Use `GET /b1s/v2/Dimensions(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `DistributionRules` | Collection([DistributionRule](../Entidades/DistributionRules.md)) | [DistributionRules](DistributionRules.md) |  | Normas de reparto |
| `ProfitCenters` | Collection([ProfitCenter](../Entidades/ProfitCenters.md)) | [ProfitCenters](ProfitCenters.md) |  | Centros de beneficio/costo |
