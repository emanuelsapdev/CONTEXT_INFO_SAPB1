# ProductionOrderLine — Líneas de la orden de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductionOrderLine`
- **Descripción (ES):** Líneas de la orden de fabricación
- **Description (EN):** Production Order Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 32

## Properties (32)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentAbsoluteEntry` | Edm.Int32 | Yes | Document Absolute Entry | Entrada absoluta del documento |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 4 | `BaseQuantity` | Edm.Double | Yes | Base Quantity | Cantidad base |
| 5 | `PlannedQuantity` | Edm.Double | Yes | Planned Quantity | Cantidad planificada |
| 6 | `IssuedQuantity` | Edm.Double | Yes | Issued Quantity | Cantidad emitida (consumida) |
| 7 | `ProductionOrderIssueType` | [BoIssueMethod](../Enums/BoIssueMethod.md) | Yes | Production Order Issue Type | Tipo de emisión de la orden de fabricación |
| 8 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 9 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 10 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 11 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 12 | `Project` | Edm.String | Yes | Project | Proyecto |
| 13 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 14 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 15 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 16 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 17 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 18 | `UoMCode` | Edm.Int32 | Yes | Uo M Code | Código de unidad de medida |
| 19 | `WipAccount` | Edm.String | Yes | Wip Account | Cuenta de producción en curso (WIP) |
| 20 | `ItemType` | [ProductionItemType](../Enums/ProductionItemType.md) | Yes | Item Type | Tipo de artículo |
| 21 | `LineText` | Edm.String | Yes | Line Text | Texto de línea |
| 22 | `AdditionalQuantity` | Edm.Double | Yes | Additional Quantity | Cantidad adicional |
| 23 | `ResourceAllocation` | [ResourceAllocationEnum](../Enums/ResourceAllocationEnum.md) | Yes | Resource Allocation | Asignación de recursos |
| 24 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 25 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 26 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 27 | `RequiredDays` | Edm.Double | Yes | Required Days | Días requeridos |
| 28 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |
| 29 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 30 | `PlasticPackageExemptionReason` | Edm.String | Yes | Plastic Package Exemption Reason | Motivo de exención de envases plásticos |
| 31 | `SerialNumbers` | Collection([SerialNumber](../Tipos-Complejos/SerialNumber.md)) | Yes | Serial Numbers | Números de serie |
| 32 | `BatchNumbers` | Collection([BatchNumber](../Tipos-Complejos/BatchNumber.md)) | Yes | Batch Numbers | Números de lote |

## Used by (properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`ProductionOrderLines`
