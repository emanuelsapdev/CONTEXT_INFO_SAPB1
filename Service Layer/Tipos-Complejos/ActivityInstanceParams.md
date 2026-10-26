# ActivityInstanceParams — Parámetros de instancia de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityInstanceParams`
- **Descripción (ES):** Parámetros de instancia de actividad
- **Description (EN):** Activity Instance Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActivityCode` | Edm.Int32 | Yes | Activity Code | Código de actividad |
| 2 | `InstanceDate` | Edm.DateTimeOffset | Yes | Instance Date | Fecha de instancia |

## Used by (service operations)

- [`ActivitiesService_DeleteSingleInstanceFromSeries`](../Servicios/ActivitiesService.md#activitiesservice_deletesingleinstancefromseries)
- [`ActivitiesService_GetSingleInstanceFromSeries`](../Servicios/ActivitiesService.md#activitiesservice_getsingleinstancefromseries)
- [`ActivitiesService_GetTopNActivityInstances`](../Servicios/ActivitiesService.md#activitiesservice_gettopnactivityinstances)
