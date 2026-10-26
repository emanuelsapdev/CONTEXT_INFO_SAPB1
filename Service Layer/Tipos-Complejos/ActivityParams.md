# ActivityParams — Parámetros de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityParams`
- **Descripción (ES):** Parámetros de actividades
- **Description (EN):** Activity Parameters

- **Properties:** 24

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActivityCode` | Edm.Int32 | Yes | Activity Code | Código de actividad |
| 2 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 3 | `Notes` | Edm.String | Yes | Notes | Notas |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `Closed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Closed | Cerrado |
| 6 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 7 | `DocNum` | Edm.String | Yes | Document Number | Número de documento |
| 8 | `DocEntry` | Edm.String | Yes | Document Entry | DocEntry (clave interna del documento) |
| 9 | `Priority` | [BoMsgPriorities](../Enums/BoMsgPriorities.md) | Yes | Priority | Prioridad |
| 10 | `Details` | Edm.String | Yes | Details | Detalles |
| 11 | `Activity` | [BoActivities](../Enums/BoActivities.md) | Yes | Activity | Actividad |
| 12 | `StartTime` | Edm.TimeOfDay | Yes | Start Time | Hora de inicio |
| 13 | `EndTime` | Edm.TimeOfDay | Yes | End Time | Hora de fin |
| 14 | `HandledBy` | Edm.Int32 | Yes | Handled By | Gestionado por |
| 15 | `City` | Edm.String | Yes | City | Ciudad |
| 16 | `Street` | Edm.String | Yes | Street | Calle |
| 17 | `Room` | Edm.String | Yes | Room | Sala/oficina |
| 18 | `InactiveFlag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive Flag | Indicador de inactivo |
| 19 | `State` | Edm.String | Yes | State | Estado/provincia |
| 20 | `Country` | Edm.String | Yes | Country | País |
| 21 | `TentativeFlag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tentative Flag | Indicador de provisorio |
| 22 | `EndDueDate` | Edm.DateTimeOffset | Yes | End Due Date | Fecha de vencimiento final |
| 23 | `SalesOpportunityId` | Edm.Int32 | Yes | Sales Opportunity ID | ID de oportunidad de venta |
| 24 | `SalesOpportunityLine` | Edm.Int32 | Yes | Sales Opportunity Line | Línea de oportunidad de venta |

## Used by (service operations)

- [`ActivitiesService_GetActivityList`](../Servicios/ActivitiesService.md#activitiesservice_getactivitylist)
- [`ActivitiesService_GetListByAttendUser`](../Servicios/ActivitiesService.md#activitiesservice_getlistbyattenduser)
- [`ActivitiesService_UpdateSingleInstanceInSeries`](../Servicios/ActivitiesService.md#activitiesservice_updatesingleinstanceinseries)
