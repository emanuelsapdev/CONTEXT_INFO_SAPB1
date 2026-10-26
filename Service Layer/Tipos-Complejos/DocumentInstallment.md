# DocumentInstallment — Cuotas del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentInstallment`
- **Descripción (ES):** Cuotas del documento
- **Description (EN):** Document Installment
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 2 | `Percentage` | Edm.Double | Yes | Percentage | Porcentaje |
| 3 | `Total` | Edm.Double | Yes | Total | Total |
| 4 | `LastDunningDate` | Edm.DateTimeOffset | Yes | Last Dunning Date | Fecha de la última reclamación |
| 5 | `DunningLevel` | Edm.Int32 | Yes | Dunning Level | Nivel de reclamación |
| 6 | `TotalFC` | Edm.Double | Yes | Total FC (foreign currency) | Total (ME) |
| 7 | `InstallmentId` | Edm.Int32 | Yes | Installment ID | ID de cuota |
| 8 | `PaymentOrdered` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Ordered | Pago ordenado |
| 9 | `PaidToDate` | Edm.Double | Yes | Paid To Date | Pagado hasta la fecha |
| 10 | `PaidToDateFC` | Edm.Double | Yes | Paid To Date FC (foreign currency) | Pagado hasta la fecha (ME) |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentInstallments`
