# UoMGroupDefinition — Definición del grupo de unidades de medida

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UoMGroupDefinition`
- **Descripción (ES):** Definición del grupo de unidades de medida
- **Description (EN):** Uo M Group Definition

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AlternateUoM` | Edm.Int32 | Yes | Alternate Uo M | Unidad de medida alternativa |
| 2 | `AlternateQuantity` | Edm.Double | Yes | Alternate Quantity | Cantidad alternativa |
| 3 | `BaseQuantity` | Edm.Double | Yes | Base Quantity | Cantidad base |
| 4 | `WeightFactor` | Edm.Int32 | Yes | Weight Factor | Factor de peso |
| 5 | `UdfFactor` | Edm.Int32 | Yes | Udf Factor | Factor de UDF |
| 6 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 7 | `BaseUdfFtr` | Edm.Int32 | Yes | Base Udf Ftr | Factor base de UDF |
| 8 | `BaseWgtFtr` | Edm.Int32 | Yes | Base Wgt Ftr | Factor de peso base |

## Used by (properties)

- [UnitOfMeasurementGroup](../Entidades/UnitOfMeasurementGroups.md).`UoMGroupDefinitionCollection`
