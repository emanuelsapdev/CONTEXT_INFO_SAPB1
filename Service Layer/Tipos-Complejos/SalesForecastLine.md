# SalesForecastLine — Líneas de previsión de ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesForecastLine`
- **Descripción (ES):** Líneas de previsión de ventas
- **Description (EN):** Sales Forecast Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 2 | `ForecastedDay` | Edm.DateTimeOffset | Yes | Forecasted Day | Día previsto |
| 3 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 4 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |

## Used by (properties)

- [SalesForecast](../Entidades/SalesForecast.md).`SalesForecastLines`
