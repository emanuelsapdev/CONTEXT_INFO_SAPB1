# BoBaselineDate — Fecha de referencia (vencimiento)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBaselineDate`
- **Descripción (ES):** Fecha de referencia (vencimiento)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bld_PostingDate` | 0 | Posting Date | Fecha de contabilización |
| `bld_SystemDate` | 1 | System Date | Fecha del sistema |
| `bld_TaxDate` | 2 | Tax Date | Fecha del documento |
| `bld_ClosingDate` | 3 | Closing Date | Fecha de cierre |

## Used by (1 properties)

- [PaymentTermsType](../Entidades/PaymentTermsTypes.md).`BaselineDate`
