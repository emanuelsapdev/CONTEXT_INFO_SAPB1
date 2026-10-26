# EDFEntryLog — Registro de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntryLog`
- **Descripción (ES):** Registro de documento electrónico
- **Description (EN):** EDF Entry Log
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `LogNumber` | Edm.Int32 | Yes | Log Number | Número de registro |
| 3 | `LogType` | [ElectronicDocumentEntryLogTypeEnum](../Enums/ElectronicDocumentEntryLogTypeEnum.md) | Yes | Log Type | Tipo de registro |
| 4 | `LogMessage` | Edm.String | Yes | Log Message | Mensaje de registro |
| 5 | `LogData` | Edm.String | Yes | Log Data | Datos de registro |
| 6 | `LogOperationDate` | Edm.DateTimeOffset | Yes | Log Operation Date | Fecha de la operación registrada |
| 7 | `LogOperationTime` | Edm.Int32 | Yes | Log Operation Time | Hora de la operación registrada |
| 8 | `ExportFormat` | Edm.Int32 | Yes | Export Format | Formato de exportación |
| 9 | `ExportFile` | Edm.String | Yes | Export File | Archivo de exportación |
| 10 | `AuthorityProcess` | [ElectronicDocumentAuthorityProcessEnum](../Enums/ElectronicDocumentAuthorityProcessEnum.md) | Yes | Authority Process | Proceso de la autoridad |
| 11 | `IsSensitive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Sensitive | Es sensible |

## Used by (service operations)

- [`ElectronicDocumentService_GetLastLog`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getlastlog)
- [`ElectronicDocumentService_GetLogs`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getlogs)
