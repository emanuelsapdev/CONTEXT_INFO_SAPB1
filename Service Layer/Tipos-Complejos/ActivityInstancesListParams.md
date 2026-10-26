# ActivityInstancesListParams — Parámetros de lista de instancias de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityInstancesListParams`
- **Descripción (ES):** Parámetros de lista de instancias de actividad
- **Description (EN):** Activity Instances List Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 2 | `InstanceCount` | Edm.Int32 | Yes | Instance Count | Cantidad de instancias |

## Used by (service operations)

- [`ActivitiesService_GetTopNActivityInstances`](../Servicios/ActivitiesService.md#activitiesservice_gettopnactivityinstances)
