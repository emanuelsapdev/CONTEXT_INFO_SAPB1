# TaxReportFilterDocumentType — Tipo de documento del filtro de informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxReportFilterDocumentType`
- **Descripción (ES):** Tipo de documento del filtro de informe de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `trfdt_ARInvoices` | 0 | AR Invoices | Facturas de clientes |
| `trfdt_ARCreditMemos` | 1 | AR Credit Memos | Notas de crédito de clientes |
| `trfdt_APInvoices` | 2 | AP Invoices | Facturas de proveedores |
| `trfdt_APCreditMemos` | 3 | AP Credit Memos | Notas de crédito de proveedores |
| `trfdt_IncomingPayments` | 4 | Incoming Payments | Pagos recibidos |
| `trfdt_JournalEntries` | 5 | Journal Entries | Asientos contables |
| `trfdt_OutgoingPayments` | 6 | Outgoing Payments | Pagos efectuados |
| `trfdt_ChecksforPayment` | 7 | Checksfor Payment | Cheques para pago |
| `trfdt_InventoryTransfers` | 8 | Inventory Transfers | Transferencias de stock |
| `trfdt_ARDownPayment` | 9 | AR Down Payment | Anticipos de clientes |
| `trfdt_APDownPayment` | 10 | AP Down Payment | Anticipos de proveedores |

## Used by (2 properties)

- [TaxReportDocument](../Tipos-Complejos/TaxReportDocument.md).`DocumentType`
- [TaxReportSeries](../Tipos-Complejos/TaxReportSeries.md).`DocumentType`
