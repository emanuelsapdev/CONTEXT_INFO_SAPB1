# Holidays — Días festivos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Holidays`
- **Descripción (ES):** Días festivos
- **Entity type:** `Holiday`
- **Key:** `HolidayCode` (Edm.String)
- **DB tables (main / lines):** [OHLD](../../Tablas%20SAP%20B1/OHLD.md), [HLD1](../../Tablas%20SAP%20B1/HLD1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Holidays?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Holidays/$count` | Contar |
| Get by key | `GET /b1s/v2/Holidays('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Holidays` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Holidays('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Holidays('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Holidays('value')` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `HolidayCode` 🔑 | Edm.String | No | Holiday Code | Código de festivo |
| 2 | `WeekendFrom` | [BoWeekEnum](../Enums/BoWeekEnum.md) | Yes | Weekend From | Fin de semana desde |
| 3 | `WeekendTO` | [BoWeekEnum](../Enums/BoWeekEnum.md) | Yes | Weekend TO | Fin de semana hasta |
| 4 | `ValidForOneYearOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid For One Year Only | Válido solo por un año |
| 5 | `SetWeekendsAsWorkDays` | Edm.String | Yes | Set Weekends As Work Days | Considerar fines de semana como días laborables |
| 6 | `WeekNoRule` | [BoWeekNoRuleEnum](../Enums/BoWeekNoRuleEnum.md) | Yes | Week Number Rule | Regla de número de semana |
| 7 | `HolidayDates` | Collection([HolidayDate](../Tipos-Complejos/HolidayDate.md)) | Yes | Holiday Dates | Fechas festivas |
