# WIPMapping — Mapeo WIP

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WIPMapping`
- **Descripción (ES):** Mapeo WIP
- **Description (EN):** WIP Mapping

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `AccountFrom` | Edm.String | Yes | Account From | Cuenta desde |
| 4 | `AccountTo` | Edm.String | Yes | Account To | Cuenta hasta |

## Used by (properties)

- [PeriodCategory](PeriodCategory.md).`WIPMappingCollection`
