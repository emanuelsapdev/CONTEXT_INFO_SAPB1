# BoTaxInvoiceTypes — Tipo de factura de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTaxInvoiceTypes`
- **Descripción (ES):** Tipo de factura de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `botit_AlterationCorrectionInvoice` | 0 | Alteration Correction Invoice | Factura de corrección de modificación |
| `botit_AlterationInvoice` | 1 | Alteration Invoice | Factura de modificación |
| `botit_CorrectionInvoice` | 2 | Correction Invoice | Factura de corrección |
| `botit_Invoice` | 4 | Invoice | Factura |
| `botit_JournalEntry` | 5 | Journal Entry | Asiento contable |
| `botit_Payment` | 6 | Payment | Pago |

## Used by (2 properties)

- [PurchaseTaxInvoice](../Entidades/PurchaseTaxInvoices.md).`DocType`
- [SalesTaxInvoice](../Entidades/SalesTaxInvoices.md).`DocType`
