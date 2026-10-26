# EDFEntryListInputParams — Parámetros de lista de documentos electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntryListInputParams`
- **Descripción (ES):** Parámetros de lista de documentos electrónicos
- **Description (EN):** EDF Entry List Input Parameters

- **Properties:** 14

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 2 | `StoreEntryTypeSet` | Edm.String | Yes | Store Entry Type Set | Tipo de entrada de almacén establecido |
| 3 | `StoreEntryStatusSet` | Edm.String | Yes | Store Entry Status Set | Estado de entrada de almacén establecido |
| 4 | `MaxLines` | Edm.Int32 | Yes | Max Lines | Líneas máximas |
| 5 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 6 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 7 | `FromTime` | Edm.Int32 | Yes | From Time | Hora desde |
| 8 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 9 | `ToTime` | Edm.Int32 | Yes | To Time | Hora hasta |
| 10 | `FromEntryID` | Edm.Int32 | Yes | From Entry ID | ID de entrada desde |
| 11 | `Ascending` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ascending | Ascendente |
| 12 | `CancellationStatusSet` | Edm.String | Yes | Cancellation Status Set | Estado de cancelación establecido |
| 13 | `ProcessingTarget` | [ElectronicDocProcessingTargetEnum](../Enums/ElectronicDocProcessingTargetEnum.md) | Yes | Processing Target | Destino del procesamiento |
| 14 | `ProcessingTargetStr` | Edm.String | Yes | Processing Target Str | Destino del procesamiento (texto) |

## Used by (service operations)

- [`ElectronicDocumentService_GetEntryList`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getentrylist)
