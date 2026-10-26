# RouteStageParams — Parámetros de etapas de ruta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RouteStageParams`
- **Descripción (ES):** Parámetros de etapas de ruta
- **Description (EN):** Route Stage Parameters

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalNumber` | Edm.Int32 | Yes | Internal Number | Número interno |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 5 | `GenerationTime` | Edm.TimeOfDay | Yes | Generation Time | Hora de generación |
| 6 | `DateOfUpdate` | Edm.DateTimeOffset | Yes | Date Of Update | Fecha de actualización |

## Used by (service operations)

- [`RouteStagesService_GetList`](../Servicios/RouteStagesService.md#routestagesservice_getlist)
