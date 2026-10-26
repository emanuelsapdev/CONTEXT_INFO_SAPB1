# InventoryCycles — Ciclos de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `InventoryCycles`
- **Descripción (ES):** Ciclos de inventario
- **Entity type:** `InventoryCycles` (open type: accepts dynamic/UDF properties)
- **Key:** `CycleCode` (Edm.Int32)
- **DB tables (main / lines):** [OCYC](../../Tablas%20SAP%20B1/OCYC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 22 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/InventoryCycles?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/InventoryCycles/$count` | Contar |
| Get by key | `GET /b1s/v2/InventoryCycles(1)` | Obtener por clave |
| Create | `POST /b1s/v2/InventoryCycles` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/InventoryCycles(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/InventoryCycles(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/InventoryCycles(1)` (only if the B1 object allows removal) | Borrar |

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CycleCode` 🔑 | Edm.Int32 | No | Cycle Code | Código de ciclo |
| 2 | `CycleName` | Edm.String | Yes | Cycle Name | Nombre del ciclo |
| 3 | `Frequency` | [BoFrequency](../Enums/BoFrequency.md) | Yes | Frequency | Frecuencia |
| 4 | `Day` | Edm.Int32 | Yes | Day | Día |
| 5 | `Hour` | Edm.TimeOfDay | Yes | Hour | Hora |
| 6 | `NextCountingDate` | Edm.DateTimeOffset | Yes | Next Counting Date | Siguiente fecha de recuento |
| 7 | `Interval` | Edm.Int32 | Yes | Interval | Intervalo |
| 8 | `Sunday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sunday | Domingo |
| 9 | `Monday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Monday | Lunes |
| 10 | `Tuesday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tuesday | Martes |
| 11 | `Wednesday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Wednesday | Miércoles |
| 12 | `Thursday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Thursday | Jueves |
| 13 | `Friday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Friday | Viernes |
| 14 | `Saturday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Saturday | Sábado |
| 15 | `RepeatOption` | [RepeatOptionEnum](../Enums/RepeatOptionEnum.md) | Yes | Repeat Option | Opción de repetición |
| 16 | `RecurrenceSequenceSpecifier` | [RecurrenceSequenceEnum](../Enums/RecurrenceSequenceEnum.md) | Yes | Recurrence Sequence Specifier | Especificador de secuencia de recurrencia |
| 17 | `RecurrenceDayInMonth` | Edm.Int32 | Yes | Recurrence Day In Month | Día del mes de recurrencia |
| 18 | `RecurrenceMonth` | Edm.Int32 | Yes | Recurrence Month | Mes de recurrencia |
| 19 | `RecurrenceDayOfWeek` | [RecurrenceDayOfWeekEnum](../Enums/RecurrenceDayOfWeekEnum.md) | Yes | Recurrence Day Of Week | Día de la semana de recurrencia |
| 20 | `endType` | [EndTypeEnum](../Enums/EndTypeEnum.md) | Yes | End Type | Tipo de fin |
| 21 | `MaxOccurrence` | Edm.Int32 | Yes | Max Occurrence | Ocurrencias máximas |
| 22 | `SeriesEndDate` | Edm.DateTimeOffset | Yes | Series End Date | Fecha de fin de la serie |

## Navigation properties (2)

Use `GET /b1s/v2/InventoryCycles(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ItemGroups` | Collection([ItemGroups](../Entidades/ItemGroups.md)) | [ItemGroups](ItemGroups.md) |  | Grupos de artículos |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
