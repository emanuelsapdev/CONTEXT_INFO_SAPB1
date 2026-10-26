# BlanketAgreements_DetailsLine — Líneas de detalle del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BlanketAgreements_DetailsLine`
- **Descripción (ES):** Líneas de detalle del acuerdo global
- **Description (EN):** Blanket Agreements Details Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AgreementNo` | Edm.Int32 | Yes | Agreement Number | Número de acuerdo |
| 2 | `AgreementRowNumber` | Edm.Int32 | Yes | Agreement Row Number | Número de línea del acuerdo |
| 3 | `AgreementEffectiveRowNumber` | Edm.Int32 | Yes | Agreement Effective Row Number | Número de línea vigente del acuerdo |
| 4 | `Frequency` | [BlanketAgreementDatePeriodsEnum](../Enums/BlanketAgreementDatePeriodsEnum.md) | Yes | Frequency | Frecuencia |
| 5 | `From` | Edm.DateTimeOffset | Yes | From | Desde |
| 6 | `To` | Edm.DateTimeOffset | Yes | To | Hasta |
| 7 | `ReleaseInformation` | Edm.String | Yes | Release Information | Información de liberación |
| 8 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 9 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 10 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |
| 11 | `ConsumeSalesForecast` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Consume Sales Forecast | Consumir previsión de ventas |
| 12 | `PlannedAmountLC` | Edm.Double | Yes | Planned Amount LC (local currency) | Importe planificado (moneda local) |
| 13 | `PlannedAmountFC` | Edm.Double | Yes | Planned Amount FC (foreign currency) | Importe planificado (ME) |

## Used by (properties)

- [BlanketAgreements_ItemsLine](BlanketAgreements_ItemsLine.md).`BlanketAgreements_DetailsLines`
