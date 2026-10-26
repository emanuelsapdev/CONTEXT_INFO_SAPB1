# BrazilStringIndexers — Brasil - Indexadores de cadenas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BrazilStringIndexers`
- **Descripción (ES):** Brasil - Indexadores de cadenas
- **Entity type:** `BrazilStringIndexer`
- **Key:** `ID` (Edm.Int32)
- **DB tables (main / lines):** [OBSI](../../Tablas%20SAP%20B1/OBSI.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 4 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BrazilStringIndexers?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BrazilStringIndexers/$count` | Contar |
| Get by key | `GET /b1s/v2/BrazilStringIndexers(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BrazilStringIndexers` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BrazilStringIndexers(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BrazilStringIndexers(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BrazilStringIndexers(1)` (only if the B1 object allows removal) | Borrar |
| Action `GetIndexerTypeList` | `POST /b1s/v2/BrazilStringIndexers(1)/GetIndexerTypeList` | Obtener lista de tipos de indexador |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `IndexerType` | [BrazilStringIndexerTypes](../Enums/BrazilStringIndexerTypes.md) | Yes | Indexer Type | Tipo de indexador |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `ID` 🔑 | Edm.Int32 | No | ID | ID |

## Navigation properties (4)

Use `GET /b1s/v2/BrazilStringIndexers(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BrazilBeverageIndexers` | Collection([BrazilBeverageIndexer](../Entidades/BrazilBeverageIndexers.md)) | [BrazilBeverageIndexers](BrazilBeverageIndexers.md) |  | Brasil - Indexadores de bebidas |
| `WithholdingTaxCodes` | Collection([WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md)) | [WithholdingTaxCodes](WithholdingTaxCodes.md) |  | Códigos de retención de impuestos |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |

## Bound actions (1)

### GetIndexerTypeList

- **Descripción (ES):** Obtener lista de tipos de indexador
- **Request:** `POST /b1s/v2/BrazilStringIndexers(1)/GetIndexerTypeList`
- **Returns:** Collection([BrazilStringIndexerParams](../Tipos-Complejos/BrazilStringIndexerParams.md))

