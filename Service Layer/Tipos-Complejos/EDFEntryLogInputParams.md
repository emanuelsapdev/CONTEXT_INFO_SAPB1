# EDFEntryLogInputParams — Parámetros de entrada de registro de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntryLogInputParams`
- **Descripción (ES):** Parámetros de entrada de registro de documento electrónico
- **Description (EN):** EDF Entry Log Input Parameters

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `GUID` | Edm.String | Yes | GUID | GUID |
| 3 | `LogType` | [ElectronicDocumentEntryLogTypeEnum](../Enums/ElectronicDocumentEntryLogTypeEnum.md) | Yes | Log Type | Tipo de registro |
| 4 | `FileName` | Edm.String | Yes | File Name | Nombre del archivo |
| 5 | `LogDataContentType` | [ElectronicDocumentBlobContentTypeEnum](../Enums/ElectronicDocumentBlobContentTypeEnum.md) | Yes | Log Data Content Type | Tipo de contenido de los datos de registro |
| 6 | `UnzipLogData` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Unzip Log Data | Descomprimir datos de registro |
| 7 | `KeepLogDataPrefix` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Keep Log Data Prefix | Prefijo de conservación de datos de registro |

## Used by (service operations)

- [`ElectronicDocumentService_ExportEntryLog`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_exportentrylog)
- [`ElectronicDocumentService_GetLastLog`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getlastlog)
- [`ElectronicDocumentService_GetLogs`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getlogs)
