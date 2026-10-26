# TCSAccumulationBaseEnum — Base de acumulación TCS

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TCSAccumulationBaseEnum`
- **Descripción (ES):** Base de acumulación TCS
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tcsAccumulationOnInvoice` | 0 | Accumulation On Invoice | Acumulación en la factura |
| `tcsAccumulationOnPayment` | 1 | Accumulation On Payment | Acumulación en el pago |

## Used by (1 properties)

- [FinancialYear](../Entidades/FinancialYears.md).`TCSAccumulationBase`
