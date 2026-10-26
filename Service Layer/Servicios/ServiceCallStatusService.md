# ServiceCallStatusService — Servicio de estados de llamadas de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ServiceCallStatusService`
- **Descripción (ES):** Servicio de estados de llamadas de servicio
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ServiceCallStatusService_GetServiceCallStatusList`](#servicecallstatusservice_getservicecallstatuslist) | action | Collection([ServiceCallStatusParams](../Tipos-Complejos/ServiceCallStatusParams.md)) | Get Service Call Status List | Obtener lista de estados de llamadas de servicio |

## ServiceCallStatusService_GetServiceCallStatusList

- **Descripción (ES):** Obtener lista de estados de llamadas de servicio
- **Request:** `POST /b1s/v2/ServiceCallStatusService_GetServiceCallStatusList`
- **Parameters:** none
- **Returns:** Collection([ServiceCallStatusParams](../Tipos-Complejos/ServiceCallStatusParams.md))

