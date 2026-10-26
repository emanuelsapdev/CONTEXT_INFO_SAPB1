# WTDFreight — [Loc. AR] Gasto adicional de la definición de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WTDFreight`
- **Descripción (ES):** [Loc. AR] Gasto adicional de la definición de retención
- **Description (EN):** WTD Freight
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FreightCode` | Edm.Int32 | Yes | Freight Code | Código de gasto adicional |
| 2 | `WTaxCode` | Edm.String | Yes | W Tax Code | Código de retención |
| 3 | `EffectiveDateFrom` | Edm.DateTimeOffset | Yes | Effective Date From | Fecha de vigencia desde |
| 4 | `EffectiveDateTo` | Edm.DateTimeOffset | Yes | Effective Date To | Fecha de vigencia hasta |

## Used by (properties)

- [WTDCode](../Entidades/WitholdingTaxDefinition.md).`WTDFreightCollection`
