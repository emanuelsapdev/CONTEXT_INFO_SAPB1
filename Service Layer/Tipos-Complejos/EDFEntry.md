# EDFEntry — Entrada de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFEntry`
- **Descripción (ES):** Entrada de documento electrónico
- **Description (EN):** EDF Entry
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 62

## Properties (62)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 3 | `ParentAbsEntry` | Edm.Int32 | Yes | Parent Abs Entry | Entrada absoluta del padre |
| 4 | `Type` | [ElectronicDocumentEntryTypeEnum](../Enums/ElectronicDocumentEntryTypeEnum.md) | Yes | Type | Tipo |
| 5 | `Status` | [ElectronicDocumentEntryStatusEnum](../Enums/ElectronicDocumentEntryStatusEnum.md) | Yes | Status | Estado |
| 6 | `BranchID` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 7 | `Environment` | Edm.Int32 | Yes | Environment | Entorno |
| 8 | `Description` | Edm.String | Yes | Description | Descripción |
| 9 | `Message` | Edm.String | Yes | Message | Mensaje |
| 10 | `Submits` | Edm.Int32 | Yes | Submits | Envíos |
| 11 | `ObjectID` | Edm.String | Yes | Object ID | ID de objeto |
| 12 | `ReportID` | Edm.String | Yes | Report ID | ID de informe |
| 13 | `SrcObjType` | Edm.String | Yes | Src Obj Type | Tipo de objeto de origen |
| 14 | `SrcAbsEntry` | Edm.Int32 | Yes | Src Abs Entry | Entrada absoluta de origen |
| 15 | `AssignedID` | Edm.String | Yes | Assigned ID | ID asignado |
| 16 | `DocBatchID` | Edm.String | Yes | Document Batch ID | ID de lote de documentos |
| 17 | `DocBatchIndex` | Edm.Int32 | Yes | Document Batch Index | Índice en lote de documentos |
| 18 | `GenerationType` | [ElectronicDocGenTypeEnum](../Enums/ElectronicDocGenTypeEnum.md) | Yes | Generation Type | Tipo de generación |
| 19 | `TestMode` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Test Mode | Modo de prueba |
| 20 | `PeriodType` | [ElectronicDocumentEntryPeriodTypeEnum](../Enums/ElectronicDocumentEntryPeriodTypeEnum.md) | Yes | Period Type | Tipo de período |
| 21 | `PeriodNumber` | Edm.Int32 | Yes | Period Number | Número de período |
| 22 | `PeriodYear` | Edm.Int32 | Yes | Period Year | Año del período |
| 23 | `PeriodDateFrom` | Edm.DateTimeOffset | Yes | Period Date From | Fecha del período desde |
| 24 | `PeriodDateTo` | Edm.DateTimeOffset | Yes | Period Date To | Fecha del período hasta |
| 25 | `IsRemoved` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Removed | Está eliminado |
| 26 | `IsCancelation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Cancelation | Es cancelación |
| 27 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 28 | `CreateTime` | Edm.Int32 | Yes | Create Time | Hora de creación |
| 29 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 30 | `UpdateTime` | Edm.Int32 | Yes | Update Time | Hora de actualización |
| 31 | `User` | Edm.Int32 | Yes | User | Usuario |
| 32 | `User2` | Edm.Int32 | Yes | User 2 | Usuario 2 |
| 33 | `ScheduledJobID` | Edm.Int32 | Yes | Scheduled Job ID | ID de trabajo programado |
| 34 | `GUID` | Edm.String | Yes | GUID | GUID |
| 35 | `Authority` | Edm.String | Yes | Authority | Autoridad |
| 36 | `CancellationStatus` | [ElectronicDocumentEntryCancellationStatusEnum](../Enums/ElectronicDocumentEntryCancellationStatusEnum.md) | Yes | Cancellation Status | Estado de cancelación |
| 37 | `ProcessingTarget` | Edm.String | Yes | Processing Target | Destino del procesamiento |
| 38 | `EDocType` | Edm.Int32 | Yes | E Document Type | Tipo de documento electrónico |
| 39 | `EDocNum` | Edm.String | Yes | E Document Number | Número del documento electrónico |
| 40 | `Emergency` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Emergency | Emergencia |
| 41 | `StatusReason` | Edm.String | Yes | Status Reason | Motivo del estado |
| 42 | `StatusDesc` | Edm.String | Yes | Status Description | Descripción del estado |
| 43 | `U_B1SYS_FCE_ID` | Edm.Int32 | Yes | [AR localization] FCE ID | [Loc. AR] ID de la FCE |
| 44 | `U_B1SYS_FCE_ApprDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Appr Date | [Loc. AR] Fecha de aceptación FCE MiPyME |
| 45 | `U_B1SYS_FCE_ApprStat` | Edm.String | Yes | [AR localization] FCE Appr Stat | [Loc. AR] Estado de aceptación FCE MiPyME |
| 46 | `U_B1SYS_FCE_TotalVal` | Edm.Double | Yes | [AR localization] FCE Total Val | [Loc. AR] Importe total de la FCE |
| 47 | `U_B1SYS_FCE_PaidVal` | Edm.Double | Yes | [AR localization] FCE Paid Val | [Loc. AR] Importe pagado de la FCE |
| 48 | `U_B1SYS_FCE_Retenton` | Edm.Double | Yes | [AR localization] FCE Retenton | [Loc. AR] Retenciones de la FCE |
| 49 | `U_B1SYS_FCE_CBU` | Edm.String | Yes | [AR localization] FCE CBU | [Loc. AR] CBU informado en la FCE |
| 50 | `U_B1SYS_FCE_Currency` | Edm.String | Yes | [AR localization] FCE Currency | [Loc. AR] Moneda de la FCE |
| 51 | `U_B1SYS_FCE_InitAmnt` | Edm.Double | Yes | [AR localization] FCE Init Amnt | [Loc. AR] Importe inicial de la FCE |
| 52 | `U_B1SYS_FCE_DcApStat` | Edm.String | Yes | [AR localization] FCE Dc Ap Stat | [Loc. AR] Estado de aceptación del documento FCE |
| 53 | `U_B1SYS_FCE_DcApDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Dc Ap Date | [Loc. AR] Fecha de aceptación del documento FCE |
| 54 | `U_B1SYS_FCE_RjRsnCod` | Edm.String | Yes | [AR localization] FCE Rj Rsn Cod | [Loc. AR] Código de motivo de rechazo de la FCE |
| 55 | `U_B1SYS_FCE_RjRsnDes` | Edm.String | Yes | [AR localization] FCE Rj Rsn Des | [Loc. AR] Descripción del motivo de rechazo de la FCE |
| 56 | `U_B1SYS_FCE_DocType` | Edm.Int32 | Yes | [AR localization] FCE Document Type | [Loc. AR] Tipo de comprobante FCE |
| 57 | `U_B1SYS_FCE_POI` | Edm.String | Yes | [AR localization] FCE POI | [Loc. AR] Punto de venta de la FCE |
| 58 | `U_B1SYS_FCE_Folio` | Edm.Int32 | Yes | [AR localization] FCE Folio | [Loc. AR] Número (folio) de la FCE |
| 59 | `U_B1SYS_FCE_DocDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Document Date | [Loc. AR] Fecha del documento FCE |
| 60 | `U_B1SYS_FCE_DocRate` | Edm.Double | Yes | [AR localization] FCE Document Rate | [Loc. AR] Tipo de cambio del documento FCE |
| 61 | `U_B1SYS_XMLAmount` | Edm.Double | Yes | [AR localization] XML Amount | [Loc. AR] Importe informado en el XML |
| 62 | `U_B1SYS_SendDateINTM` | Edm.DateTimeOffset | Yes | [AR localization] Send Date INTM | [Loc. AR] Fecha de envío al intermediario |

## Used by (service operations)

- [`ElectronicDocumentService_CreateEntry`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_createentry)
- [`ElectronicDocumentService_GetEntry`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getentry)
- [`ElectronicDocumentService_GetEntryList`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_getentrylist)
- [`ElectronicDocumentService_UpdateEntry`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_updateentry)
