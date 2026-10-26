# BusinessPlaceTributaryInfo — Información tributaria del lugar de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BusinessPlaceTributaryInfo`
- **Descripción (ES):** Información tributaria del lugar de negocios
- **Description (EN):** Business Place Tributary Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 2 | `TributaryID` | Edm.Int32 | Yes | Tributary ID | ID tributario |
| 3 | `TributaryType` | Edm.Int32 | Yes | Tributary Type | Tipo tributario |
| 4 | `TTStartDate` | Edm.DateTimeOffset | Yes | TT Start Date | Fecha de inicio TT |
| 5 | `TTEndDate` | Edm.DateTimeOffset | Yes | TT End Date | Fecha de fin TT |
| 6 | `TributaryRegimeCode` | Edm.Int32 | Yes | Tributary Regime Code | Código de régimen tributario |
| 7 | `TRCStartDate` | Edm.DateTimeOffset | Yes | TRC Start Date | Fecha de inicio TRC |
| 8 | `TRCEndDate` | Edm.DateTimeOffset | Yes | TRC End Date | Fecha de fin TRC |

## Used by (properties)

- [BusinessPlace](../Entidades/BusinessPlaces.md).`BusinessPlaceTributaryInfos`
