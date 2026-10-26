# EcmActionLog — Registro de acción de comunicación electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EcmActionLog`
- **Descripción (ES):** Registro de acción de comunicación electrónica
- **Description (EN):** Ecm Action Log

- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActionID` | Edm.Int32 | Yes | Action ID | ID de acción |
| 2 | `LogID` | Edm.Int32 | Yes | Log ID | ID de registro |
| 3 | `Type` | [EcmActionLogTypeEnum](../Enums/EcmActionLogTypeEnum.md) | Yes | Type | Tipo |
| 4 | `Message` | Edm.String | Yes | Message | Mensaje |
| 5 | `Data` | Edm.String | Yes | Data | Datos |
| 6 | `LogDate` | Edm.DateTimeOffset | Yes | Log Date | Fecha de registro |
| 7 | `LogTime` | Edm.Int32 | Yes | Log Time | Hora de registro |
| 8 | `ExportFormat` | Edm.Int32 | Yes | Export Format | Formato de exportación |
| 9 | `ExportFile` | Edm.String | Yes | Export File | Archivo de exportación |
| 10 | `AuthorityProcess` | [ElectronicDocumentAuthorityProcessEnum](../Enums/ElectronicDocumentAuthorityProcessEnum.md) | Yes | Authority Process | Proceso de la autoridad |
| 11 | `IsSensitive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Sensitive | Es sensible |

## Used by (service operations)

- [`ElectronicCommunicationActionsService_AddEcmActionLog`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_addecmactionlog)
- [`ElectronicCommunicationActionsService_GetEcmActionLog`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmactionlog)
- [`ElectronicCommunicationActionsService_GetEcmActionLogList`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmactionloglist)
