# DiscountGroupLine — Línea de grupo de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DiscountGroupLine`
- **Descripción (ES):** Línea de grupo de descuento
- **Description (EN):** Discount Group Line

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ObjectType` | [DiscountGroupBaseObjectEnum](../Enums/DiscountGroupBaseObjectEnum.md) | Yes | Object Type | Tipo de objeto |
| 3 | `ObjectCode` | Edm.String | Yes | Object Code | Código de objeto |
| 4 | `DiscountType` | [DiscountGroupDiscountTypeEnum](../Enums/DiscountGroupDiscountTypeEnum.md) | Yes | Discount Type | Tipo de descuento |
| 5 | `Discount` | Edm.Double | Yes | Discount | Descuento |
| 6 | `PaidQuantity` | Edm.Double | Yes | Paid Quantity | Cantidad pagada |
| 7 | `FreeQuantity` | Edm.Double | Yes | Free Quantity | Cantidad gratuita |
| 8 | `MaximumFreeQuantity` | Edm.Double | Yes | Maximum Free Quantity | Cantidad gratuita máxima |

## Used by (properties)

- [EnhancedDiscountGroup](../Entidades/EnhancedDiscountGroups.md).`DiscountGroupLineCollection`
