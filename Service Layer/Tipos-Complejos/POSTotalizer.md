# POSTotalizer — Totalizador POS

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `POSTotalizer`
- **Descripción (ES):** Totalizador POS
- **Description (EN):** POS Totalizer

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Number` | Edm.Int32 | Yes | Number | Número |
| 4 | `Total` | Edm.Double | Yes | Total | Total |
| 5 | `Description` | Edm.String | Yes | Description | Descripción |

## Used by (properties)

- [POSDailySummary](../Entidades/POSDailySummary.md).`POSTotalizerCollection`
