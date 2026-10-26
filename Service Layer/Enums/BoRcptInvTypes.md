# BoRcptInvTypes — Tipo de documento en pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoRcptInvTypes`
- **Descripción (ES):** Tipo de documento en pagos
- **Underlying type:** Edm.Int32
- **Members:** 27

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `it_AllTransactions` | -1 | All Transactions | Todas las transacciones |
| `it_OpeningBalance` | -2 | Opening Balance | Saldo inicial |
| `it_ClosingBalance` | -3 | Closing Balance | Saldo de cierre |
| `it_Invoice` | 13 | Invoice | Factura de clientes (13) |
| `it_CredItnote` | 14 | Credentials Itnote | Nota de crédito de clientes (14) |
| `it_TaxInvoice` | 15 | Tax Invoice | Factura de impuestos (15) |
| `it_Return` | 16 | Return | Devolución (16) |
| `it_PurchaseInvoice` | 18 | Purchase Invoice | Factura de proveedores (18) |
| `it_PurchaseCreditNote` | 19 | Purchase Credit Note | Nota de crédito de proveedores (19) |
| `it_PurchaseDeliveryNote` | 20 | Purchase Delivery Note | Pedido de entrada de mercancías (20) |
| `it_PurchaseReturn` | 21 | Purchase Return | Devolución de mercancías (21) |
| `it_Receipt` | 24 | Receipt | Pago recibido (24) |
| `it_Deposit` | 25 | Deposit | Depósito (25) |
| `it_JournalEntry` | 30 | Journal Entry | Asiento contable (30) |
| `it_PaymentAdvice` | 46 | Payment Advice | Pago efectuado (46) |
| `it_ChequesForPayment` | 57 | Cheques For Payment | Cheques para pago (57) |
| `it_StockReconciliations` | 58 | Stock Reconciliations | Conciliaciones de stock (58) |
| `it_GeneralReceiptToStock` | 59 | General Receipt To Stock | Entrada de mercancías (59) |
| `it_GeneralReleaseFromStock` | 60 | General Release From Stock | Salida de mercancías (60) |
| `it_TransferBetweenWarehouses` | 67 | Transfer Between Warehouses | Transferencia entre almacenes (67) |
| `it_WorkInstructions` | 68 | Work Instructions | Instrucciones de trabajo (68) |
| `it_DeferredDeposit` | 76 | Deferred Deposit | Depósito diferido (76) |
| `it_CorrectionInvoice` | 132 | Correction Invoice | Factura de corrección (132) |
| `it_APCorrectionInvoice` | 163 | AP Correction Invoice | Factura de corrección de proveedores (163) |
| `it_ARCorrectionInvoice` | 165 | AR Correction Invoice | Factura de corrección de clientes (165) |
| `it_DownPayment` | 203 | Down Payment | Anticipo de clientes (203) |
| `it_PurchaseDownPayment` | 204 | Purchase Down Payment | Anticipo de proveedores (204) |

## Used by (1 properties)

- [PaymentInvoice](../Tipos-Complejos/PaymentInvoice.md).`InvoiceType`
