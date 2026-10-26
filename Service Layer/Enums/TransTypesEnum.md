# TransTypesEnum — Tipos de transacción

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TransTypesEnum`
- **Descripción (ES):** Tipos de transacción
- **Underlying type:** Edm.Int32
- **Members:** 36

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ttAllTransactions` | 0 | All Transactions | Todas las transacciones |
| `ttOpeningBalance` | 1 | Opening Balance | Saldo inicial |
| `ttClosingBalance` | 2 | Closing Balance | Saldo de cierre |
| `ttARInvoice` | 3 | AR Invoice | Factura de clientes |
| `ttARCredItnote` | 4 | AR Credentials Itnote | Nota de crédito de clientes |
| `ttDelivery` | 5 | Delivery | Entrega |
| `ttReturn` | 6 | Return | Devolución |
| `ttAPInvoice` | 7 | AP Invoice | Factura de proveedores |
| `ttAPCreditNote` | 8 | AP Credit Note | Nota de crédito de proveedores |
| `ttPurchaseDeliveryNote` | 9 | Purchase Delivery Note | Pedido de entrada de mercancías |
| `ttPurchaseReturn` | 10 | Purchase Return | Devolución de mercancías |
| `ttReceipt` | 11 | Receipt | Pago recibido |
| `ttDeposit` | 12 | Deposit | Depósito |
| `ttJournalEntry` | 13 | Journal Entry | Asiento contable |
| `ttVendorPayment` | 14 | Vendor Payment | Pago efectuado |
| `ttChequesForPayment` | 15 | Cheques For Payment | Cheques para pago |
| `ttStockList` | 16 | Stock List | Lista de stock |
| `ttGeneralReceiptToStock` | 17 | General Receipt To Stock | Entrada de mercancías |
| `ttGeneralReleaseFromStock` | 18 | General Release From Stock | Salida de mercancías |
| `ttTransferBetweenWarehouses` | 19 | Transfer Between Warehouses | Transferencia entre almacenes |
| `ttWorkInstructions` | 20 | Work Instructions | Instrucciones de trabajo |
| `ttLandedCosts` | 21 | Landed Costs | Costos de importación |
| `ttDeferredDeposit` | 22 | Deferred Deposit | Depósito diferido |
| `ttCorrectionInvoice` | 23 | Correction Invoice | Factura de corrección |
| `ttInventoryValuation` | 24 | Inventory Valuation | Valoración de inventario |
| `ttAPCorrectionInvoice` | 25 | AP Correction Invoice | Factura de corrección de proveedores |
| `ttAPCorrectionInvoiceReversal` | 26 | AP Correction Invoice Reversal | Anulación de factura de corrección de proveedores |
| `ttARCorrectionInvoice` | 27 | AR Correction Invoice | Factura de corrección de clientes |
| `ttARCorrectionInvoiceReversal` | 28 | AR Correction Invoice Reversal | Anulación de factura de corrección de clientes |
| `ttBoETransaction` | 29 | Bo E Transaction | Transacción de letras de cambio |
| `ttProductionOrder` | 30 | Production Order | Orden de fabricación |
| `ttDownPayment` | 31 | Down Payment | Anticipo de clientes |
| `ttPurchaseDownPayment` | 32 | Purchase Down Payment | Anticipo de proveedores |
| `ttInternalReconciliation` | 33 | Internal Reconciliation | Conciliación interna |
| `ttInventoryPosting` | 34 | Inventory Posting | Contabilización de inventario |
| `ttInventoryOpeningBalance` | 35 | Inventory Opening Balance | Saldo inicial de inventario |

## Used by (2 properties)

- [JournalEntry](../Entidades/JournalEntries.md).`OriginalJournal`
- [Layer](../Tipos-Complejos/Layer.md).`DocType`
