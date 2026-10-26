# ClosingDateProcedure — Procedimiento de fecha de cierre

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ClosingDateProcedure`
- **Descripción (ES):** Procedimiento de fecha de cierre
- **Entity type:** `ClosingDateProcedure` (open type: accepts dynamic/UDF properties)
- **Key:** `ClosingDateNum` (Edm.Int32)
- **DB tables (main / lines):** [OCDP](../../Tablas%20SAP%20B1/OCDP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ClosingDateProcedure?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ClosingDateProcedure/$count` | Contar |
| Get by key | `GET /b1s/v2/ClosingDateProcedure(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ClosingDateProcedure` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ClosingDateProcedure(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ClosingDateProcedure(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ClosingDateProcedure(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ClosingDateNum` 🔑 | Edm.Int32 | No | Closing Date Number | Número de fecha de cierre |
| 2 | `ClosingDateCode` | Edm.String | Yes | Closing Date Code | Código de fecha de cierre |
| 3 | `BaselineDate` | [BoClosingDateProcedureBaseDateEnum](../Enums/BoClosingDateProcedureBaseDateEnum.md) | Yes | Baseline Date | Fecha de referencia |
| 4 | `DueMonth` | [BoClosingDateProcedureDueMonthEnum](../Enums/BoClosingDateProcedureDueMonthEnum.md) | Yes | Due Month | Mes de vencimiento |
| 5 | `ExtraMonth` | Edm.Int32 | Yes | Extra Month | Mes adicional |
| 6 | `ExtraDay` | Edm.Int32 | Yes | Extra Day | Día adicional |

## Navigation properties (1)

Use `GET /b1s/v2/ClosingDateProcedure(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
