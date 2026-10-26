# BOEPortfolios — Carteras de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BOEPortfolios`
- **Descripción (ES):** Carteras de letras de cambio
- **Entity type:** `BOEPortfolio`
- **Key:** `PortfolioEntry` (Edm.Int32)
- **DB tables (main / lines):** [OPTF](../../Tablas%20SAP%20B1/OPTF.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BOEPortfolios?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BOEPortfolios/$count` | Contar |
| Get by key | `GET /b1s/v2/BOEPortfolios(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BOEPortfolios` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BOEPortfolios(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BOEPortfolios(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BOEPortfolios(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PortfolioEntry` 🔑 | Edm.Int32 | No | Portfolio Entry | Entrada de la cartera |
| 2 | `PortfolioID` | Edm.String | Yes | Portfolio ID | ID de cartera |
| 3 | `PortfolioCode` | Edm.String | Yes | Portfolio Code | Código de cartera |
| 4 | `PortfolioNum` | Edm.String | Yes | Portfolio Number | Número de cartera |
| 5 | `PortfolioDescription` | Edm.String | Yes | Portfolio Description | Descripción de la cartera |
