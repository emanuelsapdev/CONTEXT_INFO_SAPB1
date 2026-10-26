# BranchesService — Servicio de sucursales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BranchesService`
- **Descripción (ES):** Servicio de sucursales
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BranchesService_GetBranchList`](#branchesservice_getbranchlist) | action | Collection([BranchParams](../Tipos-Complejos/BranchParams.md)) | Get Branch List | Obtener lista de sucursales |

## BranchesService_GetBranchList

- **Descripción (ES):** Obtener lista de sucursales
- **Request:** `POST /b1s/v2/BranchesService_GetBranchList`
- **Parameters:** none
- **Returns:** Collection([BranchParams](../Tipos-Complejos/BranchParams.md))

