# UserAccessLog — Registro de acceso de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserAccessLog`
- **Descripción (ES):** Registro de acceso de usuario
- **Description (EN):** User Access Log

- **Properties:** 16

## Properties (16)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 2 | `Action` | [UserActionTypeEnum](../Enums/UserActionTypeEnum.md) | Yes | Action | Acción |
| 3 | `ActionBy` | Edm.String | Yes | Action By | Acción realizada por |
| 4 | `ClientIP` | Edm.String | Yes | Client IP | IP del cliente |
| 5 | `ClientName` | Edm.String | Yes | Client Name | Nombre del cliente |
| 6 | `ActionDate` | Edm.DateTimeOffset | Yes | Action Date | Fecha de la acción |
| 7 | `ActionTime` | Edm.TimeOfDay | Yes | Action Time | Hora de la acción |
| 8 | `WinUsrName` | Edm.String | Yes | Win Usr Name | Nombre de usuario de Windows |
| 9 | `WinSessnID` | Edm.Int32 | Yes | Win Sessn ID | ID de sesión de Windows |
| 10 | `ProcName` | Edm.String | Yes | Proc Name | Nombre del procedimiento |
| 11 | `ProcessID` | Edm.Int32 | Yes | Process ID | ID de proceso |
| 12 | `SessionID` | Edm.Int32 | Yes | Session ID | ID de sesión |
| 13 | `ReasonID` | [UserAccessLogReasonIDTypeEnum](../Enums/UserAccessLogReasonIDTypeEnum.md) | Yes | Reason ID | ID del motivo |
| 14 | `ReasonDesc` | Edm.String | Yes | Reason Description | Descripción del motivo |
| 15 | `Source` | Edm.String | Yes | Source | Origen |
| 16 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |

## Used by (service operations)

- [`CompanyService_LogLoginAction`](../Servicios/CompanyService.md#companyservice_logloginaction)
- [`CompanyService_LogLogoffAction`](../Servicios/CompanyService.md#companyservice_loglogoffaction)
