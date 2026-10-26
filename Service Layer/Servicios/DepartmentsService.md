# DepartmentsService — Servicio de departamentos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `DepartmentsService`
- **Descripción (ES):** Servicio de departamentos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`DepartmentsService_GetDepartmentList`](#departmentsservice_getdepartmentlist) | action | Collection([DepartmentParams](../Tipos-Complejos/DepartmentParams.md)) | Get Department List | Obtener lista de departamentos |

## DepartmentsService_GetDepartmentList

- **Descripción (ES):** Obtener lista de departamentos
- **Request:** `POST /b1s/v2/DepartmentsService_GetDepartmentList`
- **Parameters:** none
- **Returns:** Collection([DepartmentParams](../Tipos-Complejos/DepartmentParams.md))

