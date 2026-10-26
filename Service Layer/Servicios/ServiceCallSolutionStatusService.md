# ServiceCallSolutionStatusService — Servicio de estados de soluciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ServiceCallSolutionStatusService`
- **Descripción (ES):** Servicio de estados de soluciones
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ServiceCallSolutionStatusService_GetServiceCallSolutionStatusList`](#servicecallsolutionstatusservice_getservicecallsolutionstatuslist) | action | Collection([ServiceCallSolutionStatusParams](../Tipos-Complejos/ServiceCallSolutionStatusParams.md)) | Get Service Call Solution Status List | Obtener lista de estados de soluciones |

## ServiceCallSolutionStatusService_GetServiceCallSolutionStatusList

- **Descripción (ES):** Obtener lista de estados de soluciones
- **Request:** `POST /b1s/v2/ServiceCallSolutionStatusService_GetServiceCallSolutionStatusList`
- **Parameters:** none
- **Returns:** Collection([ServiceCallSolutionStatusParams](../Tipos-Complejos/ServiceCallSolutionStatusParams.md))

