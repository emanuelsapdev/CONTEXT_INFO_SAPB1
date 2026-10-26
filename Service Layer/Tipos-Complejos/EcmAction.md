# EcmAction — Acción de comunicación electrónica (ECM)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EcmAction`
- **Descripción (ES):** Acción de comunicación electrónica (ECM)
- **Description (EN):** Ecm Action
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 45

## Properties (45)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActionID` | Edm.Int32 | Yes | Action ID | ID de acción |
| 2 | `Protocol` | Edm.String | Yes | Protocol | Protocolo |
| 3 | `Type` | [EcmActionTypeEnum](../Enums/EcmActionTypeEnum.md) | Yes | Type | Tipo |
| 4 | `Description` | Edm.String | Yes | Description | Descripción |
| 5 | `Status` | [EcmActionStatusEnum](../Enums/EcmActionStatusEnum.md) | Yes | Status | Estado |
| 6 | `Message` | Edm.String | Yes | Message | Mensaje |
| 7 | `Environment` | Edm.Int32 | Yes | Environment | Entorno |
| 8 | `BusinessPlace` | Edm.Int32 | Yes | Business Place | Lugar de negocios |
| 9 | `Submits` | Edm.Int32 | Yes | Submits | Envíos |
| 10 | `ObjectID` | Edm.String | Yes | Object ID | ID de objeto |
| 11 | `ReportID` | Edm.String | Yes | Report ID | ID de informe |
| 12 | `SourceType` | Edm.String | Yes | Source Type | Tipo de origen |
| 13 | `SourceObject` | Edm.Int32 | Yes | Source Object | Objeto de origen |
| 14 | `AssignedID` | Edm.String | Yes | Assigned ID | ID asignado |
| 15 | `DocumentBatch` | Edm.String | Yes | Document Batch | Lote de documentos |
| 16 | `DocumentBatchLine` | Edm.Int32 | Yes | Document Batch Line | Línea de lote de documentos |
| 17 | `PeriodType` | [EcmActionPeriodTypeEnum](../Enums/EcmActionPeriodTypeEnum.md) | Yes | Period Type | Tipo de período |
| 18 | `PeriodNumber` | Edm.Int32 | Yes | Period Number | Número de período |
| 19 | `PeriodYear` | Edm.Int32 | Yes | Period Year | Año del período |
| 20 | `PeriodDateFrom` | Edm.DateTimeOffset | Yes | Period Date From | Fecha del período desde |
| 21 | `PeriodDateTo` | Edm.DateTimeOffset | Yes | Period Date To | Fecha del período hasta |
| 22 | `IsRemoved` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Removed | Está eliminado |
| 23 | `IsCanceled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Canceled | Está cancelado |
| 24 | `GenerationType` | [EcmActionGenerationTypeEnum](../Enums/EcmActionGenerationTypeEnum.md) | Yes | Generation Type | Tipo de generación |
| 25 | `GUID` | Edm.String | Yes | GUID | GUID |
| 26 | `U_B1SYS_FCE_ID` | Edm.Int32 | Yes | [AR localization] FCE ID | [Loc. AR] ID de la FCE |
| 27 | `U_B1SYS_FCE_ApprDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Appr Date | [Loc. AR] Fecha de aceptación FCE MiPyME |
| 28 | `U_B1SYS_FCE_ApprStat` | Edm.String | Yes | [AR localization] FCE Appr Stat | [Loc. AR] Estado de aceptación FCE MiPyME |
| 29 | `U_B1SYS_FCE_TotalVal` | Edm.Double | Yes | [AR localization] FCE Total Val | [Loc. AR] Importe total de la FCE |
| 30 | `U_B1SYS_FCE_PaidVal` | Edm.Double | Yes | [AR localization] FCE Paid Val | [Loc. AR] Importe pagado de la FCE |
| 31 | `U_B1SYS_FCE_Retenton` | Edm.Double | Yes | [AR localization] FCE Retenton | [Loc. AR] Retenciones de la FCE |
| 32 | `U_B1SYS_FCE_CBU` | Edm.String | Yes | [AR localization] FCE CBU | [Loc. AR] CBU informado en la FCE |
| 33 | `U_B1SYS_FCE_Currency` | Edm.String | Yes | [AR localization] FCE Currency | [Loc. AR] Moneda de la FCE |
| 34 | `U_B1SYS_FCE_InitAmnt` | Edm.Double | Yes | [AR localization] FCE Init Amnt | [Loc. AR] Importe inicial de la FCE |
| 35 | `U_B1SYS_FCE_DcApStat` | Edm.String | Yes | [AR localization] FCE Dc Ap Stat | [Loc. AR] Estado de aceptación del documento FCE |
| 36 | `U_B1SYS_FCE_DcApDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Dc Ap Date | [Loc. AR] Fecha de aceptación del documento FCE |
| 37 | `U_B1SYS_FCE_RjRsnCod` | Edm.String | Yes | [AR localization] FCE Rj Rsn Cod | [Loc. AR] Código de motivo de rechazo de la FCE |
| 38 | `U_B1SYS_FCE_RjRsnDes` | Edm.String | Yes | [AR localization] FCE Rj Rsn Des | [Loc. AR] Descripción del motivo de rechazo de la FCE |
| 39 | `U_B1SYS_FCE_DocType` | Edm.Int32 | Yes | [AR localization] FCE Document Type | [Loc. AR] Tipo de comprobante FCE |
| 40 | `U_B1SYS_FCE_POI` | Edm.String | Yes | [AR localization] FCE POI | [Loc. AR] Punto de venta de la FCE |
| 41 | `U_B1SYS_FCE_Folio` | Edm.Int32 | Yes | [AR localization] FCE Folio | [Loc. AR] Número (folio) de la FCE |
| 42 | `U_B1SYS_FCE_DocDate` | Edm.DateTimeOffset | Yes | [AR localization] FCE Document Date | [Loc. AR] Fecha del documento FCE |
| 43 | `U_B1SYS_FCE_DocRate` | Edm.Double | Yes | [AR localization] FCE Document Rate | [Loc. AR] Tipo de cambio del documento FCE |
| 44 | `U_B1SYS_XMLAmount` | Edm.Double | Yes | [AR localization] XML Amount | [Loc. AR] Importe informado en el XML |
| 45 | `U_B1SYS_SendDateINTM` | Edm.DateTimeOffset | Yes | [AR localization] Send Date INTM | [Loc. AR] Fecha de envío al intermediario |

## Used by (service operations)

- [`ElectronicCommunicationActionsService_AddEcmAction`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_addecmaction)
- [`ElectronicCommunicationActionsService_DeleteEcmAction`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_deleteecmaction)
- [`ElectronicCommunicationActionsService_GetEcmAction`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmaction)
- [`ElectronicCommunicationActionsService_GetEcmActionByDoc`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmactionbydoc)
- [`ElectronicCommunicationActionsService_GetEcmActionLogList`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmactionloglist)
- [`ElectronicCommunicationActionsService_UpdateEcmAction`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_updateecmaction)
