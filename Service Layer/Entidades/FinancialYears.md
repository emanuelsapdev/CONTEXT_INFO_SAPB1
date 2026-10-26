# FinancialYears — Ejercicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `FinancialYears`
- **Descripción (ES):** Ejercicios
- **Entity type:** `FinancialYear`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OFYM](../../Tablas%20SAP%20B1/OFYM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/FinancialYears?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/FinancialYears/$count` | Contar |
| Get by key | `GET /b1s/v2/FinancialYears(1)` | Obtener por clave |
| Create | `POST /b1s/v2/FinancialYears` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/FinancialYears(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/FinancialYears(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/FinancialYears(1)` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 6 | `AssessYear` | Edm.String | Yes | Assess Year | Año fiscal de evaluación |
| 7 | `TCSAccumulationBase` | [TCSAccumulationBaseEnum](../Enums/TCSAccumulationBaseEnum.md) | Yes | TCS Accumulation Base | Base de acumulación TCS |
