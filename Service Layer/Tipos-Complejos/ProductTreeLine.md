# ProductTreeLine — Líneas de la lista de materiales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductTreeLine`
- **Descripción (ES):** Líneas de la lista de materiales
- **Description (EN):** Product Tree Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 24

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 3 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 4 | `Price` | Edm.Double | Yes | Price | Precio |
| 5 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 6 | `IssueMethod` | [BoIssueMethod](../Enums/BoIssueMethod.md) | Yes | Issue Method | Método de emisión (manual/notificación) |
| 7 | `InventoryUOM` | Edm.String | Yes | Inventory Unit of Measure | Unidad de medida de inventario |
| 8 | `Comment` | Edm.String | Yes | Comment | Comentario |
| 9 | `ParentItem` | Edm.String | Yes | Parent Item | Artículo padre |
| 10 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 11 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 12 | `Project` | Edm.String | Yes | Project | Proyecto |
| 13 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 14 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 15 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 16 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 17 | `WipAccount` | Edm.String | Yes | Wip Account | Cuenta de producción en curso (WIP) |
| 18 | `ItemType` | [ProductionItemType](../Enums/ProductionItemType.md) | Yes | Item Type | Tipo de artículo |
| 19 | `LineText` | Edm.String | Yes | Line Text | Texto de línea |
| 20 | `AdditionalQuantity` | Edm.Double | Yes | Additional Quantity | Cantidad adicional |
| 21 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 22 | `ChildNum` | Edm.Int32 | Yes | Child Number | Número de hijo |
| 23 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 24 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |

## Used by (properties)

- [ProductTree](../Entidades/ProductTrees.md).`ProductTreeLines`
