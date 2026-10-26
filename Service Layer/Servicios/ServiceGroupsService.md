# ServiceGroupsService — Servicio de grupos de servicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ServiceGroupsService`
- **Descripción (ES):** Servicio de grupos de servicios
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ServiceGroupsService_GetServiceGroupList`](#servicegroupsservice_getservicegrouplist) | action | Collection([ServiceGroupParams](../Tipos-Complejos/ServiceGroupParams.md)) | Get Service Group List | Obtener lista de grupos de servicios |

## ServiceGroupsService_GetServiceGroupList

- **Descripción (ES):** Obtener lista de grupos de servicios
- **Request:** `POST /b1s/v2/ServiceGroupsService_GetServiceGroupList`
- **Parameters:** none
- **Returns:** Collection([ServiceGroupParams](../Tipos-Complejos/ServiceGroupParams.md))

