# ProductionOrdersStage — Etapas de la orden de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductionOrdersStage`
- **Descripción (ES):** Etapas de la orden de fabricación
- **Description (EN):** Production Orders Stage
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `SequenceNumber` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 4 | `StageEntry` | Edm.Int32 | Yes | Stage Entry | Entrada de la etapa |
| 5 | `Name` | Edm.String | Yes | Name | Nombre |
| 6 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 7 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 8 | `RequiredDays` | Edm.Double | Yes | Required Days | Días requeridos |
| 9 | `WaitingDays` | Edm.Double | Yes | Waiting Days | Días de espera |
| 10 | `CalculationProportion` | Edm.Double | Yes | Calculation Proportion | Proporción de cálculo |

## Used by (properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`ProductionOrdersStages`
