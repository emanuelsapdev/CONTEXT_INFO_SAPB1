# EDFEntryAddLogInputParams — Parámetros para agregar registro a documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntryAddLogInputParams`
- **Descripción (ES):** Parámetros para agregar registro a documento electrónico
- **Description (EN):** EDF Entry Add Log Input Parameters

- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `GUID` | Edm.String | Yes | GUID | GUID |
| 3 | `LogType` | [ElectronicDocumentEntryLogTypeEnum](../Enums/ElectronicDocumentEntryLogTypeEnum.md) | Yes | Log Type | Tipo de registro |
| 4 | `LogMessage` | Edm.String | Yes | Log Message | Mensaje de registro |
| 5 | `LogData` | Edm.String | Yes | Log Data | Datos de registro |
| 6 | `ExportFormat` | Edm.Int32 | Yes | Export Format | Formato de exportación |
| 7 | `LogDataContentType` | [ElectronicDocumentBlobContentTypeEnum](../Enums/ElectronicDocumentBlobContentTypeEnum.md) | Yes | Log Data Content Type | Tipo de contenido de los datos de registro |
| 8 | `ZipLogData` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Zip Log Data | Comprimir datos de registro |
| 9 | `ExportFile` | Edm.String | Yes | Export File | Archivo de exportación |
| 10 | `AuthorityProcess` | [ElectronicDocumentAuthorityProcessEnum](../Enums/ElectronicDocumentAuthorityProcessEnum.md) | Yes | Authority Process | Proceso de la autoridad |
| 11 | `IsSensitive` | [BoYesNoNoneEnum](../Enums/BoYesNoNoneEnum.md) | Yes | Is Sensitive | Es sensible |

## Used by (service operations)

- [`ElectronicDocumentService_AddLog`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_addlog)
