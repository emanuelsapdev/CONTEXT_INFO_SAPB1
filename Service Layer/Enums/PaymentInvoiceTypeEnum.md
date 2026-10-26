# PaymentInvoiceTypeEnum — Tipo de factura del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PaymentInvoiceTypeEnum`
- **Descripción (ES):** Tipo de factura del pago
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `itARInvoice` | 0 | AR Invoice | Factura de clientes |
| `itARDownPaymentInvoice` | 1 | AR Down Payment Invoice | Factura de anticipo de clientes |

## Used by (2 properties)

- [PaymentAmountParams](../Tipos-Complejos/PaymentAmountParams.md).`DocType`
- [PaymentInvoiceEntry](../Tipos-Complejos/PaymentInvoiceEntry.md).`DocType`
