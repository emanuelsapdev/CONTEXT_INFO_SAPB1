# SupportUserLoginRecord — Registro de inicio de sesión de usuario de soporte

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SupportUserLoginRecord`
- **Descripción (ES):** Registro de inicio de sesión de usuario de soporte
- **Description (EN):** Support User Login Record

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` | Edm.Int32 | Yes | ID | ID |
| 2 | `RealName` | Edm.String | Yes | Real Name | Nombre real |
| 3 | `LogReason` | [SupportUserLoginRecordLogReasonTypeEnum](../Enums/SupportUserLoginRecordLogReasonTypeEnum.md) | Yes | Log Reason | Motivo del registro |
| 4 | `LogDetail` | Edm.String | Yes | Log Detail | Detalle de registro |

## Used by (service operations)

- [`CompanyService_LogLoginAction`](../Servicios/CompanyService.md#companyservice_logloginaction)
- [`CompanyService_LogLogoffAction`](../Servicios/CompanyService.md#companyservice_loglogoffaction)
