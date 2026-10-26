# CashFlowAssignment — Asignaciones de flujo de caja

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CashFlowAssignment`
- **Descripción (ES):** Asignaciones de flujo de caja
- **Description (EN):** Cash Flow Assignment
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CashFlowAssignmentsID` | Edm.Int32 | Yes | Cash Flow Assignments ID | ID de asignación de flujo de caja |
| 2 | `CashFlowLineItemID` | Edm.Int32 | Yes | Cash Flow Line Item ID | ID de partida de flujo de caja |
| 3 | `Credit` | Edm.Double | Yes | Credit | Haber/Crédito |
| 4 | `PaymentMeans` | [PaymentMeansTypeEnum](../Enums/PaymentMeansTypeEnum.md) | Yes | Payment Means | Medio de pago |
| 5 | `CheckNumber` | Edm.String | Yes | Check Number | Número de cheque |
| 6 | `AmountLC` | Edm.Double | Yes | Amount LC (local currency) | Importe (moneda local) |
| 7 | `AmountFC` | Edm.Double | Yes | Amount FC (foreign currency) | Importe (ME) |
| 8 | `JDTLineId` | Edm.Int32 | Yes | JDT Line ID | ID de línea de asiento |
| 9 | `JDTId` | Edm.Int32 | Yes | JDT ID | ID de asiento |

## Used by (properties)

- [JournalEntryLine](JournalEntryLine.md).`CashFlowAssignments`
- [Payment](../Entidades/VendorPayments.md).`CashFlowAssignments`
