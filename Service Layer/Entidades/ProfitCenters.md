# ProfitCenters — Centros de beneficio/costo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ProfitCenters`
- **Descripción (ES):** Centros de beneficio/costo
- **Entity type:** `ProfitCenter` (open type: accepts dynamic/UDF properties)
- **Key:** `CenterCode` (Edm.String)
- **DB tables (main / lines):** [OPRC](../../Tablas%20SAP%20B1/OPRC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 9 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ProfitCenters?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ProfitCenters/$count` | Contar |
| Get by key | `GET /b1s/v2/ProfitCenters('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ProfitCenters` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ProfitCenters('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ProfitCenters('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ProfitCenters('value')` (only if the B1 object allows removal) | Borrar |

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CenterCode` 🔑 | Edm.String | No | Center Code | Código del centro |
| 2 | `CenterName` | Edm.String | Yes | Center Name | Nombre del centro |
| 3 | `GroupCode` | Edm.String | Yes | Group Code | Código de grupo |
| 4 | `InWhichDimension` | Edm.Int32 | Yes | In Which Dimension | En qué dimensión |
| 5 | `CostCenterType` | Edm.String | Yes | Cost Center Type | Tipo de centro de costo |
| 6 | `EffectiveFrom` | Edm.DateTimeOffset | Yes | Effective From | Vigente desde |
| 7 | `EffectiveTo` | Edm.DateTimeOffset | Yes | Effective To | Vigente hasta |
| 8 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 9 | `CenterOwner` | Edm.Int32 | Yes | Center Owner | Responsable del centro |

## Navigation properties (4)

Use `GET /b1s/v2/ProfitCenters('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Dimension` | [Dimension](../Entidades/Dimensions.md) | [Dimensions](Dimensions.md) | InWhichDimension → DimensionCode | Dimensión |
| `CostCenterType2` | [CostCenterType](../Entidades/CostCenterTypes.md) | [CostCenterTypes](CostCenterTypes.md) | CostCenterType → CostCenterTypeCode | Tipos de centro de costo |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | CenterOwner → EmployeeID | Empleados |
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
