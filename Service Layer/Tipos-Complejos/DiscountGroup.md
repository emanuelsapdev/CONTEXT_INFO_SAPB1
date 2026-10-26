# DiscountGroup — Grupos de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DiscountGroup`
- **Descripción (ES):** Grupos de descuento
- **Description (EN):** Discount Group

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ObjectEntry` | Edm.String | Yes | Object Entry | Entrada del objeto |
| 2 | `DiscountPercentage` | Edm.Double | Yes | Discount Percentage | Porcentaje de descuento |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 4 | `BaseObjectType` | [DiscountGroupBaseObjectEnum](../Enums/DiscountGroupBaseObjectEnum.md) | Yes | Base Object Type | Tipo de objeto base |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`DiscountGroups`
