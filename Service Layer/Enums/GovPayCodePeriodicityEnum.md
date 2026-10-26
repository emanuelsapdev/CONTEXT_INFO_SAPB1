# GovPayCodePeriodicityEnum — Periodicidad del código de pago gubernamental

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `GovPayCodePeriodicityEnum`
- **Descripción (ES):** Periodicidad del código de pago gubernamental
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gpcpMonth` | 0 | Month | Mensual |
| `gpcpQuarter` | 1 | Quarter | Trimestral |
| `gpcpHalfMonth` | 2 | Half Month | Quincenal |
| `gpcpTenDays` | 3 | Ten Days | Cada diez días |

## Used by (1 properties)

- [GovPayCode](../Entidades/GovPayCodes.md).`Prdcity`
