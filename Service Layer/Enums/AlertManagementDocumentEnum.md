# AlertManagementDocumentEnum — Documento de la gestión de alertas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AlertManagementDocumentEnum`
- **Descripción (ES):** Documento de la gestión de alertas
- **Underlying type:** Edm.Int32
- **Members:** 17

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `atd_NOB` | 0 | NOB | Ninguno |
| `atd_Invoices` | 1 | Invoices | Facturas de clientes |
| `atd_RevertInvoice` | 2 | Revert Invoice | Notas de crédito de clientes |
| `atd_DeliveryNotes` | 3 | Delivery Notes | Entregas |
| `atd_Returns` | 4 | Returns | Devoluciones |
| `atd_Orders` | 5 | Orders | Pedidos de cliente |
| `atd_PurchaseInvoices` | 6 | Purchase Invoices | Facturas de proveedores |
| `atd_PurchaseDeliveryNotes` | 7 | Purchase Delivery Notes | Pedidos de entrada de mercancías |
| `atd_PurchaseOrders` | 8 | Purchase Orders | Pedidos de compra |
| `atd_Quotations` | 9 | Quotations | Ofertas de ventas |
| `atd_IncomingPayments` | 10 | Incoming Payments | Pagos recibidos |
| `atd_JournalEntries` | 11 | Journal Entries | Asientos contables |
| `atd_OutgoingPayments` | 12 | Outgoing Payments | Pagos efectuados |
| `atd_ChecksForPayment` | 13 | Checks For Payment | Cheques para pago |
| `atd_CorrectionInvoice` | 14 | Correction Invoice | Factura de corrección |
| `atd_DownPaymentIncoming` | 15 | Down Payment Incoming | Anticipo de clientes |
| `atd_DownPaymentOutgoing` | 16 | Down Payment Outgoing | Anticipo de proveedores |

## Used by (1 properties)

- [AlertManagementDocument](../Tipos-Complejos/AlertManagementDocument.md).`Document`
