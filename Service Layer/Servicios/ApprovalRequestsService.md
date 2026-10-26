# ApprovalRequestsService — Servicio de solicitudes de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ApprovalRequestsService`
- **Descripción (ES):** Servicio de solicitudes de autorización
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ApprovalRequestsService_GetAllApprovalRequestsList`](#approvalrequestsservice_getallapprovalrequestslist) | action | Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md)) | Get All Approval Requests List | Obtener todas las solicitudes de autorización |
| [`ApprovalRequestsService_GetApprovalRequestList`](#approvalrequestsservice_getapprovalrequestlist) | action | Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md)) | Get Approval Request List | Obtener lista de solicitudes de autorización |
| [`ApprovalRequestsService_GetOpenApprovalRequestList`](#approvalrequestsservice_getopenapprovalrequestlist) | action | Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md)) | Get Open Approval Request List | Obtener lista de solicitudes de autorización abiertas |

## ApprovalRequestsService_GetAllApprovalRequestsList

- **Descripción (ES):** Obtener todas las solicitudes de autorización
- **Request:** `POST /b1s/v2/ApprovalRequestsService_GetAllApprovalRequestsList`
- **Parameters:** none
- **Returns:** Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md))

## ApprovalRequestsService_GetApprovalRequestList

- **Descripción (ES):** Obtener lista de solicitudes de autorización
- **Request:** `POST /b1s/v2/ApprovalRequestsService_GetApprovalRequestList`
- **Parameters:** none
- **Returns:** Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md))

## ApprovalRequestsService_GetOpenApprovalRequestList

- **Descripción (ES):** Obtener lista de solicitudes de autorización abiertas
- **Request:** `POST /b1s/v2/ApprovalRequestsService_GetOpenApprovalRequestList`
- **Parameters:** none
- **Returns:** Collection([ApprovalRequestParams](../Tipos-Complejos/ApprovalRequestParams.md))

