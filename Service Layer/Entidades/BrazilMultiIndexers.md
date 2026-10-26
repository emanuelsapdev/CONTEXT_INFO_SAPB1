# BrazilMultiIndexers — Brasil - Multi-indexadores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BrazilMultiIndexers`
- **Descripción (ES):** Brasil - Multi-indexadores
- **Entity type:** `BrazilMultiIndexer`
- **Key:** `ID` (Edm.Int32)
- **DB tables (main / lines):** [OBMI](../../Tablas%20SAP%20B1/OBMI.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BrazilMultiIndexers?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BrazilMultiIndexers/$count` | Contar |
| Get by key | `GET /b1s/v2/BrazilMultiIndexers(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BrazilMultiIndexers` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BrazilMultiIndexers(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BrazilMultiIndexers(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BrazilMultiIndexers(1)` (only if the B1 object allows removal) | Borrar |
| Action `GetIndexerTypeList` | `POST /b1s/v2/BrazilMultiIndexers(1)/GetIndexerTypeList` | Obtener lista de tipos de indexador |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` 🔑 | Edm.Int32 | No | ID | ID |
| 2 | `IndexerType` | [BrazilMultiIndexerTypes](../Enums/BrazilMultiIndexerTypes.md) | Yes | Indexer Type | Tipo de indexador |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `Description` | Edm.String | Yes | Description | Descripción |
| 5 | `FirstRefIndexerCode` | Edm.String | Yes | First Ref Indexer Code | Código del primer indexador de referencia |
| 6 | `SecondRefIndexerCode` | Edm.String | Yes | Second Ref Indexer Code | Código del segundo indexador de referencia |
| 7 | `ThirdRefIndexerCode` | Edm.String | Yes | Third Ref Indexer Code | Código del tercer indexador de referencia |

## Bound actions (1)

### GetIndexerTypeList

- **Descripción (ES):** Obtener lista de tipos de indexador
- **Request:** `POST /b1s/v2/BrazilMultiIndexers(1)/GetIndexerTypeList`
- **Returns:** Collection([BrazilMultiIndexerParams](../Tipos-Complejos/BrazilMultiIndexerParams.md))

