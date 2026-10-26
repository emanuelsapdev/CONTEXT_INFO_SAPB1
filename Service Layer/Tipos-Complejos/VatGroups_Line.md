# VatGroups_Line — Líneas de grupos de IVA

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `VatGroups_Line`
- **Descripción (ES):** Líneas de grupos de IVA
- **Description (EN):** Vat Groups Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Effectivefrom` | Edm.DateTimeOffset | Yes | Effectivefrom | Vigente desde |
| 2 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 3 | `EqualizationTax` | Edm.Double | Yes | Equalization Tax | Impuesto de recargo de equivalencia |
| 4 | `DatevCode` | Edm.Int32 | Yes | Datev Code | Código DATEV |

## Used by (properties)

- [VatGroup](../Entidades/VatGroups.md).`VatGroups_Lines`
