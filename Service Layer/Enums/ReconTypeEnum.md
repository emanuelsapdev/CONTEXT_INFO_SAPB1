# ReconTypeEnum — Tipo de conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ReconTypeEnum`
- **Descripción (ES):** Tipo de conciliación
- **Underlying type:** Edm.Int32
- **Members:** 19

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rtManual` | 0 | Manual | Manual |
| `rtAutomatic` | 1 | Automatic | Automática |
| `rtSemiAutomatic` | 2 | Semi Automatic | Semiautomática |
| `rtPayment` | 3 | Payment | Pago |
| `rtCreditMemo` | 4 | Credit Memo | Nota de crédito |
| `rtReversal` | 5 | Reversal | Reversión |
| `rtZeroValue` | 6 | Zero Value | Valor cero |
| `rtCancellation` | 7 | Cancellation | Cancelación |
| `rtBoE` | 8 | Bo E | Letra de cambio |
| `rtDeposit` | 9 | Deposit | Depósito |
| `rtBankStatementProcess` | 10 | Bank Statement Process | Proceso de extracto bancario |
| `rtPeriodClosing` | 11 | Period Closing | Cierre de período |
| `rtCorrectionInvoice` | 12 | Correction Invoice | Factura de corrección |
| `rtInventoryOrExpenseAllocation` | 13 | Inventory Or Expense Allocation | Asignación de inventario o gastos |
| `rtWIP` | 14 | WIP | Producción en curso (WIP) |
| `rtDeferredTaxInterimAccount` | 15 | Deferred Tax Interim Account | Cuenta transitoria de impuesto diferido |
| `rtDownPaymentAllocation` | 16 | Down Payment Allocation | Asignación de anticipo |
| `rtAutoConversionDifference` | 17 | Auto Conversion Difference | Diferencia de conversión automática |
| `rtInterimDocument` | 18 | Interim Document | Documento transitorio |

## Used by (1 properties)

- [InternalReconciliation](../Entidades/InternalReconciliations.md).`ReconType`
