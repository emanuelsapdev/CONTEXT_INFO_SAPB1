# InventoryPostingPriceSourceEnum — Origen del precio de la contabilización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `InventoryPostingPriceSourceEnum`
- **Descripción (ES):** Origen del precio de la contabilización de inventario
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ippsByPriceList` | 0 | By Price List | Por lista de precios |
| `ippsLastEvaluatedPrice` | 1 | Last Evaluated Price | Último precio evaluado |
| `ippsItemCost` | 2 | Item Cost | Costo del artículo |

## Used by (1 properties)

- [InventoryPosting](../Entidades/InventoryPostings.md).`PriceSource`
