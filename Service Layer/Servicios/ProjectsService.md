# ProjectsService — Servicio de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ProjectsService`
- **Descripción (ES):** Servicio de proyectos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ProjectsService_GetProjectList`](#projectsservice_getprojectlist) | action | Collection([ProjectParams](../Tipos-Complejos/ProjectParams.md)) | Get Project List | Obtener lista de proyectos |

## ProjectsService_GetProjectList

- **Descripción (ES):** Obtener lista de proyectos
- **Request:** `POST /b1s/v2/ProjectsService_GetProjectList`
- **Parameters:** none
- **Returns:** Collection([ProjectParams](../Tipos-Complejos/ProjectParams.md))

