# ApprovalRequestDecision — Decisiones de la solicitud de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ApprovalRequestDecision`
- **Descripción (ES):** Decisiones de la solicitud de autorización
- **Description (EN):** Approval Request Decision

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ApproverUserName` | Edm.String | Yes | Approver User Name | Usuario autorizador |
| 2 | `ApproverPassword` | Edm.String | Yes | Approver Password | Contraseña del autorizador |
| 3 | `Status` | [BoApprovalRequestDecisionEnum](../Enums/BoApprovalRequestDecisionEnum.md) | Yes | Status | Estado |
| 4 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [ApprovalRequest](../Entidades/ApprovalRequests.md).`ApprovalRequestDecisions`
