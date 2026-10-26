# BrazilBeverageIndexers — Brasil - Indexadores de bebidas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BrazilBeverageIndexers`
- **Descripción (ES):** Brasil - Indexadores de bebidas
- **Entity type:** `BrazilBeverageIndexer`
- **Key:** `BeverageID` (Edm.Int32)
- **DB tables (main / lines):** [OBBI](../../Tablas%20SAP%20B1/OBBI.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BrazilBeverageIndexers?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BrazilBeverageIndexers/$count` | Contar |
| Get by key | `GET /b1s/v2/BrazilBeverageIndexers(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BrazilBeverageIndexers` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BrazilBeverageIndexers(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BrazilBeverageIndexers(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BrazilBeverageIndexers(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BeverageGroupCode` | Edm.String | Yes | Beverage Group Code | Código de grupo de bebida |
| 2 | `BeverageTableCode` | Edm.String | Yes | Beverage Table Code | Código de tabla de bebida |
| 3 | `BeverageCommercialBrandCode` | Edm.Int32 | Yes | Beverage Commercial Brand Code | Código de marca comercial de bebida |
| 4 | `BeverageID` 🔑 | Edm.Int32 | No | Beverage ID | ID de bebida |

## Navigation properties (2)

Use `GET /b1s/v2/BrazilBeverageIndexers(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BrazilStringIndexer` | [BrazilStringIndexer](../Entidades/BrazilStringIndexers.md) | [BrazilStringIndexers](BrazilStringIndexers.md) | BeverageGroupCode → ID | Brasil - Indexadores de cadenas |
| `BrazilNumericIndexer` | [BrazilNumericIndexer](../Entidades/BrazilNumericIndexers.md) | [BrazilNumericIndexers](BrazilNumericIndexers.md) | BeverageCommercialBrandCode → ID | Brasil - Indexadores numéricos |
