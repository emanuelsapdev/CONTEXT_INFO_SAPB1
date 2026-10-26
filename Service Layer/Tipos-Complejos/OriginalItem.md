# OriginalItem — Artículo original

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `OriginalItem`
- **Descripción (ES):** Artículo original
- **Description (EN):** Original Item

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |
| 3 | `AlternativeItems` | Collection([AlternativeItem](../Tipos-Complejos/AlternativeItem.md)) | Yes | Alternative Items | Artículos alternativos |

## Used by (service operations)

- [`AlternativeItemsService_AddItem`](../Servicios/AlternativeItemsService.md#alternativeitemsservice_additem)
- [`AlternativeItemsService_GetItem`](../Servicios/AlternativeItemsService.md#alternativeitemsservice_getitem)
- [`AlternativeItemsService_UpdateItem`](../Servicios/AlternativeItemsService.md#alternativeitemsservice_updateitem)
