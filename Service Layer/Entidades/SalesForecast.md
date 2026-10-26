# SalesForecast — Previsiones de ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesForecast`
- **Descripción (ES):** Previsiones de ventas
- **Entity type:** `SalesForecast` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OFCT](../../Tablas%20SAP%20B1/OFCT.md), [FCT1](../../Tablas%20SAP%20B1/FCT1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesForecast?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesForecast/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesForecast(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesForecast` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesForecast(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesForecast(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesForecast(1)` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ForecastStartDate` | Edm.DateTimeOffset | Yes | Forecast Start Date | Fecha de inicio de la previsión |
| 2 | `ForecastEndDate` | Edm.DateTimeOffset | Yes | Forecast End Date | Fecha de fin de la previsión |
| 3 | `ForecastCode` | Edm.String | Yes | Forecast Code | Código de previsión |
| 4 | `ForecastName` | Edm.String | Yes | Forecast Name | Nombre de la previsión |
| 5 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 6 | `View` | [BoForecastViewType](../Enums/BoForecastViewType.md) | Yes | View | Vista |
| 7 | `SalesForecastLines` | Collection([SalesForecastLine](../Tipos-Complejos/SalesForecastLine.md)) | Yes | Sales Forecast Lines | Líneas de previsión de ventas |
