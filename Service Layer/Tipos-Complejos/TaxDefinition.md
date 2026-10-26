# TaxDefinition — Definición de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxDefinition`
- **Descripción (ES):** Definición de impuestos
- **Description (EN):** Tax Definition
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Effectivefrom` | Edm.DateTimeOffset | Yes | Effectivefrom | Vigente desde |
| 2 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |

## Used by (properties)

- [SalesTaxAuthority](../Entidades/SalesTaxAuthorities.md).`TaxDefinitions`
