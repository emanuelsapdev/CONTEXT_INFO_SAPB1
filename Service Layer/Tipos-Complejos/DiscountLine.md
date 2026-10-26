# DiscountLine — Líneas de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DiscountLine`
- **Descripción (ES):** Líneas de descuento
- **Description (EN):** Discount Line

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DiscountCode` | Edm.String | Yes | Discount Code | Código de descuento |
| 2 | `LineId` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `NumOfDays` | Edm.Int32 | Yes | Number Of Days | Cantidad de días |
| 4 | `Discount` | Edm.Double | Yes | Discount | Descuento |
| 5 | `Day` | Edm.Int32 | Yes | Day | Día |
| 6 | `Month` | Edm.Int32 | Yes | Month | Mes |

## Used by (properties)

- [CashDiscount](../Entidades/CashDiscounts.md).`DiscountLines`
