# BoAlertTypeforWHStockEnum — Tipo de alerta para stock de almacén

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAlertTypeforWHStockEnum`
- **Descripción (ES):** Tipo de alerta para stock de almacén
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `atfwhs_WarningOnly` | 0 | Warning Only | Solo advertencia |
| `atfwhs_Block` | 1 | Block | Bloquear |
| `atfwhs_NoMessage` | 2 | Number Message | Sin mensaje |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`AlertTypeforWHStock`
