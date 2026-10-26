# HolidayDate — Fechas festivas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `HolidayDate`
- **Descripción (ES):** Fechas festivas
- **Description (EN):** Holiday Date

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `HolidayCode` | Edm.String | Yes | Holiday Code | Código de festivo |
| 2 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 3 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 4 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [Holiday](../Entidades/Holidays.md).`HolidayDates`
