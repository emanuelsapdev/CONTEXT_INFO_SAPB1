# CurrenciesDecimalsEnum — Decimales de la moneda

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `CurrenciesDecimalsEnum`
- **Descripción (ES):** Decimales de la moneda
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `cd1Digit` | 0 | Cd 1 Digit | 1 dígito |
| `cd2Digits` | 1 | Cd 2 Digits | 2 dígitos |
| `cd3Digits` | 2 | Cd 3 Digits | 3 dígitos |
| `cd4Digits` | 3 | Cd 4 Digits | 4 dígitos |
| `cd5Digits` | 4 | Cd 5 Digits | 5 dígitos |
| `cd6Digits` | 5 | Cd 6 Digits | 6 dígitos |
| `cdDefault` | 6 | Default | Predeterminado |
| `cdWithoutDecimals` | 7 | Without Decimals | Sin decimales |

## Used by (1 properties)

- [Currency](../Entidades/Currencies.md).`Decimals`
