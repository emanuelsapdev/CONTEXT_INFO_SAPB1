# BoDueDateEnum — Fecha de vencimiento (ejecución de pagos)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDueDateEnum`
- **Descripción (ES):** Fecha de vencimiento (ejecución de pagos)
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `boddDateOfPaymentRun` | 0 | Date Of Payment Run | Fecha de la ejecución de pagos |
| `boddDueDateOfInvoice` | 1 | Due Date Of Invoice | Vencimiento de la factura |
| `boddPaymentTerms` | 2 | Payment Terms | Condiciones de pago |

## Used by (1 properties)

- [WizardPaymentMethod](../Entidades/WizardPaymentMethods.md).`DueDateSelection`
