# ApprovalRequestLine — Líneas de la solicitud de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ApprovalRequestLine`
- **Descripción (ES):** Líneas de la solicitud de autorización
- **Description (EN):** Approval Request Line

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StageCode` | Edm.Int32 | Yes | Stage Code | Código de etapa |
| 2 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `Status` | [BoApprovalRequestDecisionEnum](../Enums/BoApprovalRequestDecisionEnum.md) | Yes | Status | Estado |
| 4 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 5 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 6 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 7 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 8 | `CreationTime` | Edm.TimeOfDay | Yes | Creation Time | Hora de creación |

## Used by (properties)

- [ApprovalRequest](../Entidades/ApprovalRequests.md).`ApprovalRequestLines`
