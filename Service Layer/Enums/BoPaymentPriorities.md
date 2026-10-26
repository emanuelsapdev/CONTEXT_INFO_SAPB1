# BoPaymentPriorities — Prioridad de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoPaymentPriorities`
- **Descripción (ES):** Prioridad de pago
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bopp_Priority_1` | 0 | Priority 1 | Prioridad 1 |
| `bopp_Priority_2` | 1 | Priority 2 | Prioridad 2 |
| `bopp_Priority_3` | 2 | Priority 3 | Prioridad 3 |
| `bopp_Priority_4` | 3 | Priority 4 | Prioridad 4 |
| `bopp_Priority_5` | 4 | Priority 5 | Prioridad 5 |
| `bopp_Priority_6` | 5 | Priority 6 | Prioridad 6 |

## Used by (1 properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentPriority`
