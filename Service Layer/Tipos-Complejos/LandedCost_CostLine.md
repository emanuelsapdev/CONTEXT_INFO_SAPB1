# LandedCost_CostLine — Líneas de costos del costo de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `LandedCost_CostLine`
- **Descripción (ES):** Líneas de costos del costo de importación
- **Description (EN):** Landed Cost Cost Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LandedCostCode` | Edm.String | Yes | Landed Cost Code | Código de costo de importación |
| 3 | `AllocationBy` | [LandedCostAllocationByEnum](../Enums/LandedCostAllocationByEnum.md) | Yes | Allocation By | Asignación por |
| 4 | `Amount` | Edm.Double | Yes | Amount | Importe |
| 5 | `AmountFC` | Edm.Double | Yes | Amount FC (foreign currency) | Importe (ME) |
| 6 | `Factor` | Edm.Double | Yes | Factor | Factor |
| 7 | `CostType` | [LCCostTypeEnum](../Enums/LCCostTypeEnum.md) | Yes | Cost Type | Tipo de costo |
| 8 | `IncludeForCustoms` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include For Customs | Incluir para aduana |
| 9 | `OpenAmount` | Edm.Double | Yes | Open Amount | Importe abierto |
| 10 | `OpenAmountFC` | Edm.Double | Yes | Open Amount FC (foreign currency) | Importe abierto (ME) |
| 11 | `Broker` | Edm.String | Yes | Broker | Agente |
| 12 | `BrokerName` | Edm.String | Yes | Broker Name | Nombre del agente |
| 13 | `CostCategory` | [LandedCostCostCategoryEnum](../Enums/LandedCostCostCategoryEnum.md) | Yes | Cost Category | Categoría de costo |

## Used by (properties)

- [LandedCost](../Entidades/LandedCosts.md).`LandedCost_CostLines`
