# BoPayTermDueTypes — Inicio del vencimiento de condiciones de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoPayTermDueTypes`
- **Descripción (ES):** Inicio del vencimiento de condiciones de pago
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pdt_MonthEnd` | 0 | Month End | Fin de mes |
| `pdt_HalfMonth` | 1 | Half Month | Mitad de mes |
| `pdt_MonthStart` | 2 | Month Start | Inicio de mes |
| `pdt_None` | 3 | None | Ninguno |

## Used by (4 properties)

- [Document](../Entidades/PurchaseQuotations.md).`EndAt`
- [Document](../Entidades/PurchaseQuotations.md).`StartFrom`
- [PaymentTermsType](../Entidades/PaymentTermsTypes.md).`EndAt`
- [PaymentTermsType](../Entidades/PaymentTermsTypes.md).`StartFrom`
