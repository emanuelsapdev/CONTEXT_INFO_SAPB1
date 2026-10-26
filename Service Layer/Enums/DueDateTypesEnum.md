# DueDateTypesEnum — Tipo de fechas de vencimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DueDateTypesEnum`
- **Descripción (ES):** Tipo de fechas de vencimiento
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ddtAfterTimePeriod` | 0 | After Time Period | Después de un período |
| `ddtByDates` | 1 | By Dates | Por fechas |

## Used by (1 properties)

- [CreditCardPayment](../Entidades/CreditCardPayments.md).`DueDatesType`
