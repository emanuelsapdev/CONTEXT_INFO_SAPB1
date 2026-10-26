# KPIs — Indicadores clave de rendimiento (KPI)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `KPIs`
- **Descripción (ES):** Indicadores clave de rendimiento (KPI)
- **Entity type:** `KPI`
- **Key:** `KPICode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/KPIs?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/KPIs/$count` | Contar |
| Get by key | `GET /b1s/v2/KPIs('value')` | Obtener por clave |
| Create | `POST /b1s/v2/KPIs` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/KPIs('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/KPIs('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/KPIs('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `KPICode` 🔑 | Edm.String | No | KPI Code | Código de KPI |
| 2 | `KPIName` | Edm.String | Yes | KPI Name | Nombre del KPI |
| 3 | `KPIType` | [KPITypeEnum](../Enums/KPITypeEnum.md) | Yes | KPI Type | Tipo de KPI |
| 4 | `NumberOfColumns` | Edm.Int32 | Yes | Number Of Columns | Cantidad de columnas |
| 5 | `KPI_ItemLines` | Collection([KPI_ItemLine](../Tipos-Complejos/KPI_ItemLine.md)) | Yes | KPI Item Lines | Líneas de elementos del KPI |
