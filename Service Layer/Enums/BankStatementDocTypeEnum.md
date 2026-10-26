# BankStatementDocTypeEnum — Tipo de documento del extracto bancario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BankStatementDocTypeEnum`
- **Descripción (ES):** Tipo de documento del extracto bancario
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bsdtReceipts` | 0 | Receipts | Cobros |
| `bsdtPaymentToVendor` | 1 | Payment To Vendor | Pago a proveedor |
| `bsdtInvoices` | 2 | Invoices | Facturas de clientes |
| `bsdtPurchases` | 3 | Purchases | Facturas de proveedores |
| `bsdtDownPaymentIncoming` | 4 | Down Payment Incoming | Anticipo de clientes |
| `bsdtDownPaymentOutgoing` | 5 | Down Payment Outgoing | Anticipo de proveedores |
| `bsdtRevertInvoices` | 6 | Revert Invoices | Notas de crédito de clientes |
| `bsdtRevertPurchases` | 7 | Revert Purchases | Notas de crédito de proveedores |
| `bsdtJournalEntry` | 8 | Journal Entry | Asiento contable |

## Used by (1 properties)

- [BankStatementRow](../Tipos-Complejos/BankStatementRow.md).`DocumentType`
