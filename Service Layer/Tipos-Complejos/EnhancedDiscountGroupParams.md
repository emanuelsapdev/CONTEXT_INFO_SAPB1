# EnhancedDiscountGroupParams — Parámetros de grupos de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EnhancedDiscountGroupParams`
- **Descripción (ES):** Parámetros de grupos de descuento
- **Description (EN):** Enhanced Discount Group Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Type` | [DiscountGroupTypeEnum](../Enums/DiscountGroupTypeEnum.md) | Yes | Type | Tipo |
| 3 | `ObjectCode` | Edm.String | Yes | Object Code | Código de objeto |

## Used by (service operations)

- [`EnhancedDiscountGroupsService_GetList`](../Servicios/EnhancedDiscountGroupsService.md#enhanceddiscountgroupsservice_getlist)
