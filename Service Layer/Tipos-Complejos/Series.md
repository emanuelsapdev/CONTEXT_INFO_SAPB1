# Series — Serie de numeración

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Series`
- **Descripción (ES):** Serie de numeración
- **Description (EN):** Series
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 26

## Properties (26)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Document` | Edm.String | Yes | Document | Documento |
| 2 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 3 | `InitialNumber` | Edm.Int32 | Yes | Initial Number | Número inicial |
| 4 | `LastNumber` | Edm.Int32 | Yes | Last Number | Último número |
| 5 | `NextNumber` | Edm.Int32 | Yes | Next Number | Siguiente número |
| 6 | `Prefix` | Edm.String | Yes | Prefix | Prefijo |
| 7 | `Suffix` | Edm.String | Yes | Suffix | Sufijo |
| 8 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 9 | `GroupCode` | [BoSeriesGroupEnum](../Enums/BoSeriesGroupEnum.md) | Yes | Group Code | Código de grupo |
| 10 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 11 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 12 | `Name` | Edm.String | Yes | Name | Nombre |
| 13 | `SeriesProperty` | Edm.Int32 | Yes | Series Property | Propiedad de la serie |
| 14 | `IsDigitalSeries` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Digital Series | Es serie digital |
| 15 | `DigitNumber` | Edm.Int32 | Yes | Digit Number | Número de dígitos |
| 16 | `SeriesType` | [BoSeriesTypeEnum](../Enums/BoSeriesTypeEnum.md) | Yes | Series Type | Tipo de serie |
| 17 | `IsManual` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Manual | Es manual |
| 18 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 19 | `ATDocumentType` | Edm.String | Yes | AT Document Type | Tipo de documento AT |
| 20 | `IsElectronicCommEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Electronic Comm Enabled | Comunicación electrónica habilitada |
| 21 | `CostAccountOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cost Account Only | Solo cuenta de costos |
| 22 | `InvoiceType` | Edm.Int32 | Yes | Invoice Type | Tipo de factura |
| 23 | `InvoiceTypeOfNegativeInvoice` | Edm.Int32 | Yes | Invoice Type Of Negative Invoice | Tipo de factura negativa |
| 24 | `PortugalSeriesAction` | Edm.String | Yes | Portugal Series Action | Acción de serie (Portugal) |
| 25 | `PortugalSeriesStatus` | Edm.String | Yes | Portugal Series Status | Estado de serie (Portugal) |
| 26 | `PortugalSeriesPhase` | Edm.String | Yes | Portugal Series Phase | Fase de serie (Portugal) |

## Used by (service operations)

- [`SeriesService_AddSeries`](../Servicios/SeriesService.md#seriesservice_addseries)
- [`SeriesService_GetDefaultSeries`](../Servicios/SeriesService.md#seriesservice_getdefaultseries)
- [`SeriesService_GetDocumentSeries`](../Servicios/SeriesService.md#seriesservice_getdocumentseries)
- [`SeriesService_GetSeries`](../Servicios/SeriesService.md#seriesservice_getseries)
- [`SeriesService_UpdateSeries`](../Servicios/SeriesService.md#seriesservice_updateseries)
