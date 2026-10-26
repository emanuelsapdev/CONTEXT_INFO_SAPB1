# ProjectManagementConfigurationService — Servicio de configuración de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ProjectManagementConfigurationService`
- **Descripción (ES):** Servicio de configuración de gestión de proyectos
- **Operations:** 24

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ProjectManagementConfigurationService_AddActivities`](#projectmanagementconfigurationservice_addactivities) | action | — | Add Activities | Agregar actividades |
| [`ProjectManagementConfigurationService_AddAreas`](#projectmanagementconfigurationservice_addareas) | action | — | Add Areas | Agregar áreas |
| [`ProjectManagementConfigurationService_AddPriorities`](#projectmanagementconfigurationservice_addpriorities) | action | — | Add Priorities | Agregar prioridades |
| [`ProjectManagementConfigurationService_AddStageTypes`](#projectmanagementconfigurationservice_addstagetypes) | action | — | Add Stage Types | Agregar tipos de etapa |
| [`ProjectManagementConfigurationService_AddSubprojectTypes`](#projectmanagementconfigurationservice_addsubprojecttypes) | action | — | Add Subproject Types | Agregar tipos de subproyecto |
| [`ProjectManagementConfigurationService_AddTasks`](#projectmanagementconfigurationservice_addtasks) | action | — | Add Tasks | Agregar tareas |
| [`ProjectManagementConfigurationService_DeleteActivities`](#projectmanagementconfigurationservice_deleteactivities) | action | — | Delete Activities | Eliminar actividades |
| [`ProjectManagementConfigurationService_DeleteAreas`](#projectmanagementconfigurationservice_deleteareas) | action | — | Delete Areas | Eliminar áreas |
| [`ProjectManagementConfigurationService_DeletePriorities`](#projectmanagementconfigurationservice_deletepriorities) | action | — | Delete Priorities | Eliminar prioridades |
| [`ProjectManagementConfigurationService_DeleteStageTypes`](#projectmanagementconfigurationservice_deletestagetypes) | action | — | Delete Stage Types | Eliminar tipos de etapa |
| [`ProjectManagementConfigurationService_DeleteSubprojectTypes`](#projectmanagementconfigurationservice_deletesubprojecttypes) | action | — | Delete Subproject Types | Eliminar tipos de subproyecto |
| [`ProjectManagementConfigurationService_DeleteTasks`](#projectmanagementconfigurationservice_deletetasks) | action | — | Delete Tasks | Eliminar tareas |
| [`ProjectManagementConfigurationService_GetActivities`](#projectmanagementconfigurationservice_getactivities) | action | Collection([PMC_ActivityData](../Tipos-Complejos/PMC_ActivityData.md)) | Get Activities | Obtener actividades |
| [`ProjectManagementConfigurationService_GetAreas`](#projectmanagementconfigurationservice_getareas) | action | Collection([PMC_AreaData](../Tipos-Complejos/PMC_AreaData.md)) | Get Areas | Obtener áreas |
| [`ProjectManagementConfigurationService_GetPriorities`](#projectmanagementconfigurationservice_getpriorities) | action | Collection([PMC_PriorityData](../Tipos-Complejos/PMC_PriorityData.md)) | Get Priorities | Obtener prioridades |
| [`ProjectManagementConfigurationService_GetStageTypes`](#projectmanagementconfigurationservice_getstagetypes) | action | Collection([PMC_StageTypeData](../Tipos-Complejos/PMC_StageTypeData.md)) | Get Stage Types | Obtener tipos de etapa |
| [`ProjectManagementConfigurationService_GetSubprojectTypes`](#projectmanagementconfigurationservice_getsubprojecttypes) | action | Collection([PMC_SubprojectTypeData](../Tipos-Complejos/PMC_SubprojectTypeData.md)) | Get Subproject Types | Obtener tipos de subproyecto |
| [`ProjectManagementConfigurationService_GetTasks`](#projectmanagementconfigurationservice_gettasks) | action | Collection([PMC_TaskData](../Tipos-Complejos/PMC_TaskData.md)) | Get Tasks | Obtener tareas |
| [`ProjectManagementConfigurationService_UpdateActivities`](#projectmanagementconfigurationservice_updateactivities) | action | — | Update Activities | Actualizar actividades |
| [`ProjectManagementConfigurationService_UpdateAreas`](#projectmanagementconfigurationservice_updateareas) | action | — | Update Areas | Actualizar áreas |
| [`ProjectManagementConfigurationService_UpdatePriorities`](#projectmanagementconfigurationservice_updatepriorities) | action | — | Update Priorities | Actualizar prioridades |
| [`ProjectManagementConfigurationService_UpdateStageTypes`](#projectmanagementconfigurationservice_updatestagetypes) | action | — | Update Stage Types | Actualizar tipos de etapa |
| [`ProjectManagementConfigurationService_UpdateSubprojectTypes`](#projectmanagementconfigurationservice_updatesubprojecttypes) | action | — | Update Subproject Types | Actualizar tipos de subproyecto |
| [`ProjectManagementConfigurationService_UpdateTasks`](#projectmanagementconfigurationservice_updatetasks) | action | — | Update Tasks | Actualizar tareas |

## ProjectManagementConfigurationService_AddActivities

- **Descripción (ES):** Agregar actividades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddActivities`
- **Parameters:** `PMC_ActivityCollection` (Collection([PMC_ActivityData](../Tipos-Complejos/PMC_ActivityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_ActivityCollection": [ {
    "ActivityID": 0,
    "ActivityType": "string",
    "LaborItem": "string",
    ...
  } ]
}
```

## ProjectManagementConfigurationService_AddAreas

- **Descripción (ES):** Agregar áreas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddAreas`
- **Parameters:** `PMC_AreaCollection` (Collection([PMC_AreaData](../Tipos-Complejos/PMC_AreaData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_AreaCollection": [ {
    "AreaID": 0,
    "AreaName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_AddPriorities

- **Descripción (ES):** Agregar prioridades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddPriorities`
- **Parameters:** `PMC_PriorityCollection` (Collection([PMC_PriorityData](../Tipos-Complejos/PMC_PriorityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_PriorityCollection": [ {
    "PriorityID": 0,
    "PriorityName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_AddStageTypes

- **Descripción (ES):** Agregar tipos de etapa
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddStageTypes`
- **Parameters:** `PMC_StageTypeCollection` (Collection([PMC_StageTypeData](../Tipos-Complejos/PMC_StageTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_StageTypeCollection": [ {
    "StageID": 0,
    "StageName": "string",
    "StageDescription": "string"
  } ]
}
```

## ProjectManagementConfigurationService_AddSubprojectTypes

- **Descripción (ES):** Agregar tipos de subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddSubprojectTypes`
- **Parameters:** `PMC_SubprojectTypesCollection` (Collection([PMC_SubprojectTypeData](../Tipos-Complejos/PMC_SubprojectTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_SubprojectTypesCollection": [ {
    "SubprojectTypeID": 0,
    "SubprojectTypeName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_AddTasks

- **Descripción (ES):** Agregar tareas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_AddTasks`
- **Parameters:** `PMC_TaskCollection` (Collection([PMC_TaskData](../Tipos-Complejos/PMC_TaskData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_TaskCollection": [ {
    "TaskID": 0,
    "TaskName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_DeleteActivities

- **Descripción (ES):** Eliminar actividades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeleteActivities`
- **Parameters:** `PMC_ActivityCollection` (Collection([PMC_ActivityData](../Tipos-Complejos/PMC_ActivityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_ActivityCollection": [ {
    "ActivityID": 0,
    "ActivityType": "string",
    "LaborItem": "string",
    ...
  } ]
}
```

## ProjectManagementConfigurationService_DeleteAreas

- **Descripción (ES):** Eliminar áreas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeleteAreas`
- **Parameters:** `PMC_AreaCollection` (Collection([PMC_AreaData](../Tipos-Complejos/PMC_AreaData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_AreaCollection": [ {
    "AreaID": 0,
    "AreaName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_DeletePriorities

- **Descripción (ES):** Eliminar prioridades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeletePriorities`
- **Parameters:** `PMC_PriorityCollection` (Collection([PMC_PriorityData](../Tipos-Complejos/PMC_PriorityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_PriorityCollection": [ {
    "PriorityID": 0,
    "PriorityName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_DeleteStageTypes

- **Descripción (ES):** Eliminar tipos de etapa
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeleteStageTypes`
- **Parameters:** `PMC_StageTypeCollection` (Collection([PMC_StageTypeData](../Tipos-Complejos/PMC_StageTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_StageTypeCollection": [ {
    "StageID": 0,
    "StageName": "string",
    "StageDescription": "string"
  } ]
}
```

## ProjectManagementConfigurationService_DeleteSubprojectTypes

- **Descripción (ES):** Eliminar tipos de subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeleteSubprojectTypes`
- **Parameters:** `PMC_SubprojectTypesCollection` (Collection([PMC_SubprojectTypeData](../Tipos-Complejos/PMC_SubprojectTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_SubprojectTypesCollection": [ {
    "SubprojectTypeID": 0,
    "SubprojectTypeName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_DeleteTasks

- **Descripción (ES):** Eliminar tareas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_DeleteTasks`
- **Parameters:** `PMC_TaskCollection` (Collection([PMC_TaskData](../Tipos-Complejos/PMC_TaskData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_TaskCollection": [ {
    "TaskID": 0,
    "TaskName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_GetActivities

- **Descripción (ES):** Obtener actividades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetActivities`
- **Parameters:** none
- **Returns:** Collection([PMC_ActivityData](../Tipos-Complejos/PMC_ActivityData.md))

## ProjectManagementConfigurationService_GetAreas

- **Descripción (ES):** Obtener áreas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetAreas`
- **Parameters:** none
- **Returns:** Collection([PMC_AreaData](../Tipos-Complejos/PMC_AreaData.md))

## ProjectManagementConfigurationService_GetPriorities

- **Descripción (ES):** Obtener prioridades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetPriorities`
- **Parameters:** none
- **Returns:** Collection([PMC_PriorityData](../Tipos-Complejos/PMC_PriorityData.md))

## ProjectManagementConfigurationService_GetStageTypes

- **Descripción (ES):** Obtener tipos de etapa
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetStageTypes`
- **Parameters:** none
- **Returns:** Collection([PMC_StageTypeData](../Tipos-Complejos/PMC_StageTypeData.md))

## ProjectManagementConfigurationService_GetSubprojectTypes

- **Descripción (ES):** Obtener tipos de subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetSubprojectTypes`
- **Parameters:** none
- **Returns:** Collection([PMC_SubprojectTypeData](../Tipos-Complejos/PMC_SubprojectTypeData.md))

## ProjectManagementConfigurationService_GetTasks

- **Descripción (ES):** Obtener tareas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_GetTasks`
- **Parameters:** none
- **Returns:** Collection([PMC_TaskData](../Tipos-Complejos/PMC_TaskData.md))

## ProjectManagementConfigurationService_UpdateActivities

- **Descripción (ES):** Actualizar actividades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdateActivities`
- **Parameters:** `PMC_ActivityCollection` (Collection([PMC_ActivityData](../Tipos-Complejos/PMC_ActivityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_ActivityCollection": [ {
    "ActivityID": 0,
    "ActivityType": "string",
    "LaborItem": "string",
    ...
  } ]
}
```

## ProjectManagementConfigurationService_UpdateAreas

- **Descripción (ES):** Actualizar áreas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdateAreas`
- **Parameters:** `PMC_AreaCollection` (Collection([PMC_AreaData](../Tipos-Complejos/PMC_AreaData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_AreaCollection": [ {
    "AreaID": 0,
    "AreaName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_UpdatePriorities

- **Descripción (ES):** Actualizar prioridades
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdatePriorities`
- **Parameters:** `PMC_PriorityCollection` (Collection([PMC_PriorityData](../Tipos-Complejos/PMC_PriorityData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_PriorityCollection": [ {
    "PriorityID": 0,
    "PriorityName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_UpdateStageTypes

- **Descripción (ES):** Actualizar tipos de etapa
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdateStageTypes`
- **Parameters:** `PMC_StageTypeCollection` (Collection([PMC_StageTypeData](../Tipos-Complejos/PMC_StageTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_StageTypeCollection": [ {
    "StageID": 0,
    "StageName": "string",
    "StageDescription": "string"
  } ]
}
```

## ProjectManagementConfigurationService_UpdateSubprojectTypes

- **Descripción (ES):** Actualizar tipos de subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdateSubprojectTypes`
- **Parameters:** `PMC_SubprojectTypesCollection` (Collection([PMC_SubprojectTypeData](../Tipos-Complejos/PMC_SubprojectTypeData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_SubprojectTypesCollection": [ {
    "SubprojectTypeID": 0,
    "SubprojectTypeName": "string"
  } ]
}
```

## ProjectManagementConfigurationService_UpdateTasks

- **Descripción (ES):** Actualizar tareas
- **Request:** `POST /b1s/v2/ProjectManagementConfigurationService_UpdateTasks`
- **Parameters:** `PMC_TaskCollection` (Collection([PMC_TaskData](../Tipos-Complejos/PMC_TaskData.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PMC_TaskCollection": [ {
    "TaskID": 0,
    "TaskName": "string"
  } ]
}
```

