# ActivitiesService — Servicio de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ActivitiesService`
- **Descripción (ES):** Servicio de actividades
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ActivitiesService_DeleteSingleInstanceFromSeries`](#activitiesservice_deletesingleinstancefromseries) | action | — | Delete Single Instance From Series | Eliminar una instancia de la serie |
| [`ActivitiesService_GetActivityList`](#activitiesservice_getactivitylist) | action | Collection([ActivityParams](../Tipos-Complejos/ActivityParams.md)) | Get Activity List | Obtener lista de actividades |
| [`ActivitiesService_GetListByAttendUser`](#activitiesservice_getlistbyattenduser) | action | Collection([ActivityParams](../Tipos-Complejos/ActivityParams.md)) | Get List By Attend User | Obtener lista por usuario asistente |
| [`ActivitiesService_GetSingleInstanceFromSeries`](#activitiesservice_getsingleinstancefromseries) | action | [Activity](../Entidades/Activities.md) | Get Single Instance From Series | Obtener una instancia de la serie |
| [`ActivitiesService_GetTopNActivityInstances`](#activitiesservice_gettopnactivityinstances) | action | Collection([ActivityInstanceParams](../Tipos-Complejos/ActivityInstanceParams.md)) | Get Top N Activity Instances | Obtener las N instancias de actividad principales |
| [`ActivitiesService_InitData`](#activitiesservice_initdata) | action | [Activity](../Entidades/Activities.md) | Init Data | Inicializar datos |
| [`ActivitiesService_UpdateSingleInstanceInSeries`](#activitiesservice_updatesingleinstanceinseries) | action | [ActivityParams](../Tipos-Complejos/ActivityParams.md) | Update Single Instance In Series | Actualizar una instancia de la serie |

## ActivitiesService_DeleteSingleInstanceFromSeries

- **Descripción (ES):** Eliminar una instancia de la serie
- **Request:** `POST /b1s/v2/ActivitiesService_DeleteSingleInstanceFromSeries`
- **Parameters:** `ActivityInstanceParams` ([ActivityInstanceParams](../Tipos-Complejos/ActivityInstanceParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ActivityInstanceParams": {
    "ActivityCode": 0,
    "InstanceDate": "2026-01-31"
  }
}
```

## ActivitiesService_GetActivityList

- **Descripción (ES):** Obtener lista de actividades
- **Request:** `POST /b1s/v2/ActivitiesService_GetActivityList`
- **Parameters:** none
- **Returns:** Collection([ActivityParams](../Tipos-Complejos/ActivityParams.md))

## ActivitiesService_GetListByAttendUser

- **Descripción (ES):** Obtener lista por usuario asistente
- **Request:** `POST /b1s/v2/ActivitiesService_GetListByAttendUser`
- **Parameters:** `Activity` ([Activity](../Entidades/Activities.md))
- **Returns:** Collection([ActivityParams](../Tipos-Complejos/ActivityParams.md))

```json
{
  "Activity": {
    "ActivityCode": 0,
    "CardCode": "string",
    "Notes": "string",
    "ActivityDate": "2026-01-31",
    ...
  }
}
```

## ActivitiesService_GetSingleInstanceFromSeries

- **Descripción (ES):** Obtener una instancia de la serie
- **Request:** `POST /b1s/v2/ActivitiesService_GetSingleInstanceFromSeries`
- **Parameters:** `ActivityInstanceParams` ([ActivityInstanceParams](../Tipos-Complejos/ActivityInstanceParams.md))
- **Returns:** [Activity](../Entidades/Activities.md)

```json
{
  "ActivityInstanceParams": {
    "ActivityCode": 0,
    "InstanceDate": "2026-01-31"
  }
}
```

## ActivitiesService_GetTopNActivityInstances

- **Descripción (ES):** Obtener las N instancias de actividad principales
- **Request:** `POST /b1s/v2/ActivitiesService_GetTopNActivityInstances`
- **Parameters:** `ActivityInstancesListParams` ([ActivityInstancesListParams](../Tipos-Complejos/ActivityInstancesListParams.md))
- **Returns:** Collection([ActivityInstanceParams](../Tipos-Complejos/ActivityInstanceParams.md))

```json
{
  "ActivityInstancesListParams": {
    "StartDate": "2026-01-31",
    "InstanceCount": 0
  }
}
```

## ActivitiesService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/ActivitiesService_InitData`
- **Parameters:** none
- **Returns:** [Activity](../Entidades/Activities.md)

## ActivitiesService_UpdateSingleInstanceInSeries

- **Descripción (ES):** Actualizar una instancia de la serie
- **Request:** `POST /b1s/v2/ActivitiesService_UpdateSingleInstanceInSeries`
- **Parameters:** `Activity` ([Activity](../Entidades/Activities.md))
- **Returns:** [ActivityParams](../Tipos-Complejos/ActivityParams.md)

```json
{
  "Activity": {
    "ActivityCode": 0,
    "CardCode": "string",
    "Notes": "string",
    "ActivityDate": "2026-01-31",
    ...
  }
}
```

