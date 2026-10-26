# BoORCTPaymentTypeEnum — Tipo de pago (forma de envío)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoORCTPaymentTypeEnum`
- **Descripción (ES):** Tipo de pago (forma de envío)
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bopt_None` | 0 | None | Ninguno |
| `bopt_Electronic` | 1 | Electronic | Electrónico |
| `bopt_Post` | 2 | Post | Correo |
| `bopt_Telegraph` | 3 | Telegraph | Telégrafo |
| `bopt_Express` | 4 | Express | Expreso |

## Used by (1 properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentType`
