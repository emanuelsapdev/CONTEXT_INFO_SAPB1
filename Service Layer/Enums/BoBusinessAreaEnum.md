# BoBusinessAreaEnum — Área de negocio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBusinessAreaEnum`
- **Descripción (ES):** Área de negocio
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `baSales` | 0 | Sales | Ventas |
| `baPurchase` | 1 | Purchase | Compras |
| `baSalesAndPurchase` | 2 | Sales And Purchase | Ventas y compras |

## Used by (1 properties)

- [TaxCodeDetermination](../Entidades/TaxCodeDeterminations.md).`BusinessArea`
