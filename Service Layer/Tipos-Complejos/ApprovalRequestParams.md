# ApprovalRequestParams — Parámetros de solicitudes de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ApprovalRequestParams`
- **Descripción (ES):** Parámetros de solicitudes de autorización
- **Description (EN):** Approval Request Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 3 | `Status` | [BoApprovalRequestStatusEnum](../Enums/BoApprovalRequestStatusEnum.md) | Yes | Status | Estado |

## Used by (service operations)

- [`ApprovalRequestsService_GetAllApprovalRequestsList`](../Servicios/ApprovalRequestsService.md#approvalrequestsservice_getallapprovalrequestslist)
- [`ApprovalRequestsService_GetApprovalRequestList`](../Servicios/ApprovalRequestsService.md#approvalrequestsservice_getapprovalrequestlist)
- [`ApprovalRequestsService_GetOpenApprovalRequestList`](../Servicios/ApprovalRequestsService.md#approvalrequestsservice_getopenapprovalrequestlist)
