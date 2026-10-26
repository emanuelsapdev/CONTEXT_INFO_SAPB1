# VatGroupsTaxRegionEnum — Región fiscal del grupo de IVA (Portugal)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `VatGroupsTaxRegionEnum`
- **Descripción (ES):** Región fiscal del grupo de IVA (Portugal)
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `vgtrPT` | 0 | PT | Portugal continental |
| `vgtrPT_AC` | 1 | Vgtr PT AC | Azores |
| `vgtrPT_MA` | 2 | Vgtr PT MA | Madeira |

## Used by (1 properties)

- [VatGroup](../Entidades/VatGroups.md).`TaxRegion`
