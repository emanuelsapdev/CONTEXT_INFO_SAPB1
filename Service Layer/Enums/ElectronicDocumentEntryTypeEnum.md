# ElectronicDocumentEntryTypeEnum — Tipo de entrada del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentEntryTypeEnum`
- **Descripción (ES):** Tipo de entrada del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 50

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edetNone` | 0 | None | Ninguno |
| `edetSetup` | 1 | Setup | Configuración |
| `edetReport` | 2 | Report | Informe |
| `edetDocumentAR` | 3 | Document AR | Documento de ventas |
| `edetDocumentAP` | 4 | Document AP | Documento de compras |
| `edetDraftAR` | 5 | Draft AR | Borrador de ventas |
| `edetDraftAP` | 6 | Draft AP | Borrador de compras |
| `edetOther` | 7 | Other | Otro |
| `edetSkip` | 8 | Skip | Omitir |
| `edetContingency` | 9 | Contingency | Contingencia |
| `edetBpCheck` | 10 | Bp Check | Verificación de socio de negocios |
| `edetIncomingPayment` | 11 | Incoming Payment | Pago recibido |
| `edetOutgoingPayment` | 12 | Outgoing Payment | Pago efectuado |
| `edetInternalReconciliation` | 13 | Internal Reconciliation | Conciliación interna |
| `edetTransportationDocument` | 14 | Transportation Document | Documento de transporte |
| `edetInventoryTransfer` | 15 | Inventory Transfer | Transferencia de stock |
| `edetVATObligations` | 16 | VAT Obligations | Obligaciones de IVA |
| `edetVATDeclarations` | 17 | VAT Declarations | Declaraciones de IVA |
| `edetVATLiabilities` | 18 | VAT Liabilities | Pasivos de IVA |
| `edetVATPayments` | 19 | VAT Payments | Pagos de IVA |
| `edetDelivery` | 20 | Delivery | Entrega |
| `edetReturn` | 21 | Return | Devolución |
| `edetARInvoice` | 22 | AR Invoice | Factura de clientes |
| `edetARCreditMemo` | 23 | AR Credit Memo | Nota de crédito de clientes |
| `edetGoodsReceiptPO` | 24 | Goods Receipt PO | Pedido de entrada de mercancías |
| `edetGoodsReturn` | 25 | Goods Return | Devolución de mercancías |
| `edetAPInvoice` | 26 | AP Invoice | Factura de proveedores |
| `edetAPCreditMemo` | 27 | AP Credit Memo | Nota de crédito de proveedores |
| `edetDraftIncomingPayment` | 28 | Draft Incoming Payment | Borrador de pago recibido |
| `edetDraftOutgoingPayment` | 29 | Draft Outgoing Payment | Borrador de pago efectuado |
| `edetJournalEntry` | 30 | Journal Entry | Asiento contable |
| `edetEBooksExpense` | 31 | E Books Expense | Gasto de libros electrónicos |
| `edetGSTReturnF5` | 32 | GST Return F 5 | Declaración GST F5 |
| `edetGSTReturnF7` | 33 | GST Return F 7 | Declaración GST F7 |
| `edetGSTReturnF8` | 34 | GST Return F 8 | Declaración GST F8 |
| `edetSkatDKPeriod` | 35 | Skat DK Period | Período Skat DK |
| `edetSkatDKDraftReport` | 36 | Skat DK Draft Report | Borrador de informe Skat DK |
| `edetSkatDKReport` | 37 | Skat DK Report | Informe Skat DK |
| `edetINV` | 38 | INV | Factura (INV) |
| `edetRIN` | 39 | RIN | Nota de crédito (RIN) |
| `edetDLN` | 40 | DLN | Entrega (DLN) |
| `edetINVBasedOnDLN` | 41 | INV Based On DLN | Factura basada en entrega |
| `edetSeries` | 42 | Series | Series |
| `edetInvoices` | 43 | Invoices | Facturas |
| `edetGoodsTransfers` | 44 | Goods Transfers | Transferencias de mercancías |
| `edetGoodsIssue` | 45 | Goods Issue | Salida de mercancías |
| `edetGoodsReceipt` | 46 | Goods Receipt | Entrada de mercancías |
| `edetPickList` | 47 | Pick List | Lista de picking |
| `edetDraftGoodsIssue` | 48 | Draft Goods Issue | Borrador de salida de mercancías |
| `edetDraftGoodsReceipt` | 49 | Draft Goods Receipt | Borrador de entrada de mercancías |

## Used by (1 properties)

- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`Type`
