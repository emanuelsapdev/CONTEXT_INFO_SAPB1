# ProjectManagementService — Servicio de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ProjectManagementService`
- **Descripción (ES):** Servicio de gestión de proyectos
- **Operations:** 5

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ProjectManagementService_AddSubproject`](#projectmanagementservice_addsubproject) | action | [PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md) | Add Subproject | Agregar subproyecto |
| [`ProjectManagementService_DeleteSubproject`](#projectmanagementservice_deletesubproject) | action | — | Delete Subproject | Eliminar subproyecto |
| [`ProjectManagementService_GetSubproject`](#projectmanagementservice_getsubproject) | action | [PM_SubprojectDocumentData](../Tipos-Complejos/PM_SubprojectDocumentData.md) | Get Subproject | Obtener subproyecto |
| [`ProjectManagementService_GetSubprojectsList`](#projectmanagementservice_getsubprojectslist) | action | Collection([PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md)) | Get Subprojects List | Obtener lista de subproyectos |
| [`ProjectManagementService_UpdateSubproject`](#projectmanagementservice_updatesubproject) | action | — | Update Subproject | Actualizar subproyecto |

## ProjectManagementService_AddSubproject

- **Descripción (ES):** Agregar subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementService_AddSubproject`
- **Parameters:** `PM_SubprojectDocumentData` ([PM_SubprojectDocumentData](../Tipos-Complejos/PM_SubprojectDocumentData.md))
- **Returns:** [PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md)

```json
{
  "PM_SubprojectDocumentData": {
    "AbsEntry": 0,
    "Owner": 0,
    "SubprojectName": "string",
    "StartDate": "2026-01-31",
    ...
  }
}
```

## ProjectManagementService_DeleteSubproject

- **Descripción (ES):** Eliminar subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementService_DeleteSubproject`
- **Parameters:** `PM_SubprojectDocumentParams` ([PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PM_SubprojectDocumentParams": {
    "AbsEntry": 0
  }
}
```

## ProjectManagementService_GetSubproject

- **Descripción (ES):** Obtener subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementService_GetSubproject`
- **Parameters:** `PM_SubprojectDocumentParams` ([PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md))
- **Returns:** [PM_SubprojectDocumentData](../Tipos-Complejos/PM_SubprojectDocumentData.md)

```json
{
  "PM_SubprojectDocumentParams": {
    "AbsEntry": 0
  }
}
```

## ProjectManagementService_GetSubprojectsList

- **Descripción (ES):** Obtener lista de subproyectos
- **Request:** `POST /b1s/v2/ProjectManagementService_GetSubprojectsList`
- **Parameters:** `PM_SubprojectParams` ([PM_SubprojectParams](../Tipos-Complejos/PM_SubprojectParams.md))
- **Returns:** Collection([PM_SubprojectDocumentParams](../Tipos-Complejos/PM_SubprojectDocumentParams.md))

```json
{
  "PM_SubprojectParams": {
    "AbsEntry": 0,
    ...
  }
}
```

## ProjectManagementService_UpdateSubproject

- **Descripción (ES):** Actualizar subproyecto
- **Request:** `POST /b1s/v2/ProjectManagementService_UpdateSubproject`
- **Parameters:** `PM_SubprojectDocumentData` ([PM_SubprojectDocumentData](../Tipos-Complejos/PM_SubprojectDocumentData.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PM_SubprojectDocumentData": {
    "AbsEntry": 0,
    "Owner": 0,
    "SubprojectName": "string",
    "StartDate": "2026-01-31",
    ...
  }
}
```

