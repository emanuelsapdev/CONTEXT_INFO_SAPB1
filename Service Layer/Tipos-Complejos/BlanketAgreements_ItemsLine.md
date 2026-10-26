# BlanketAgreements_ItemsLine — Líneas de artículos del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BlanketAgreements_ItemsLine`
- **Descripción (ES):** Líneas de artículos del acuerdo global
- **Description (EN):** Blanket Agreements Items Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 33

## Properties (33)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AgreementNo` | Edm.Int32 | Yes | Agreement Number | Número de acuerdo |
| 2 | `AgreementRowNumber` | Edm.Int32 | Yes | Agreement Row Number | Número de línea del acuerdo |
| 3 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 4 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 5 | `ItemGroup` | Edm.Int32 | Yes | Item Group | Grupo de artículos |
| 6 | `PlannedQuantity` | Edm.Double | Yes | Planned Quantity | Cantidad planificada |
| 7 | `UnitPrice` | Edm.Double | Yes | Unit Price | Precio unitario |
| 8 | `PriceCurrency` | Edm.String | Yes | Price Currency | Moneda del precio |
| 9 | `CumulativeQuantity` | Edm.Double | Yes | Cumulative Quantity | Cantidad acumulada |
| 10 | `CumulativeAmountLC` | Edm.Double | Yes | Cumulative Amount LC (local currency) | Importe acumulado (moneda local) |
| 11 | `CumulativeAmountFC` | Edm.Double | Yes | Cumulative Amount FC (foreign currency) | Importe acumulado (ME) |
| 12 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |
| 13 | `InventoryUoM` | Edm.String | Yes | Inventory Uo M | Unidad de medida de inventario |
| 14 | `PortionOfReturns` | Edm.Double | Yes | Portion Of Returns | Proporción de devoluciones |
| 15 | `EndOfWarranty` | Edm.DateTimeOffset | Yes | End Of Warranty | Fin de la garantía |
| 16 | `PlannedAmountLC` | Edm.Double | Yes | Planned Amount LC (local currency) | Importe planificado (moneda local) |
| 17 | `PlannedAmountFC` | Edm.Double | Yes | Planned Amount FC (foreign currency) | Importe planificado (ME) |
| 18 | `LineDiscount` | Edm.Double | Yes | Line Discount | Descuento de línea |
| 19 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 20 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 21 | `UnitsOfMeasurement` | Edm.Double | Yes | Units Of Measurement | Unidades de medida |
| 22 | `UndeliveredCumulativeQuantity` | Edm.Double | Yes | Undelivered Cumulative Quantity | Cantidad acumulada no entregada |
| 23 | `UndeliveredCumulativeAmountLC` | Edm.Double | Yes | Undelivered Cumulative Amount LC (local currency) | Importe acumulado no entregado (moneda local) |
| 24 | `UndeliveredCumulativeAmountFC` | Edm.Double | Yes | Undelivered Cumulative Amount FC (foreign currency) | Importe acumulado no entregado (ME) |
| 25 | `ShippingType` | Edm.Int32 | Yes | Shipping Type | Clase de expedición |
| 26 | `Project` | Edm.String | Yes | Project | Proyecto |
| 27 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 28 | `TAXRate` | Edm.Double | Yes | TAX Rate | Tasa de impuesto |
| 29 | `PlannedVATAmountLC` | Edm.Double | Yes | Planned VAT Amount LC (local currency) | Importe de IVA planificado (moneda local) |
| 30 | `PlannedVATAmountFC` | Edm.Double | Yes | Planned VAT Amount FC (foreign currency) | Importe de IVA planificado (ME) |
| 31 | `CumulativeVATAmountLC` | Edm.Double | Yes | Cumulative VAT Amount LC (local currency) | Importe de IVA acumulado (moneda local) |
| 32 | `CumulativeVATAmountFC` | Edm.Double | Yes | Cumulative VAT Amount FC (foreign currency) | Importe de IVA acumulado (ME) |
| 33 | `BlanketAgreements_DetailsLines` | Collection([BlanketAgreements_DetailsLine](../Tipos-Complejos/BlanketAgreements_DetailsLine.md)) | Yes | Blanket Agreements Details Lines | Líneas de detalle del acuerdo global |

## Used by (properties)

- [BlanketAgreement](../Entidades/BlanketAgreements.md).`BlanketAgreements_ItemsLines`
