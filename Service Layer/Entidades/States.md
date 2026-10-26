# States — Estados/Provincias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `States`
- **Descripción (ES):** Estados/Provincias
- **Entity type:** `State`
- **Key:** `Code` (Edm.String), `Country` (Edm.String)
- **DB tables (main / lines):** [OCST](../../Tablas%20SAP%20B1/OCST.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/States?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/States/$count` | Contar |
| Get by key | `GET /b1s/v2/States(Code='value',Country='value')` | Obtener por clave |
| Create | `POST /b1s/v2/States` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/States(Code='value',Country='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/States(Code='value',Country='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/States(Code='value',Country='value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Country` 🔑 | Edm.String | No | Country | País |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `GSTCode` | Edm.String | Yes | GST Code | Código GST |
| 5 | `IsUnionTerritory` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Union Territory | Es territorio de la unión (India) |

## Navigation properties (1)

Use `GET /b1s/v2/States(Code='value',Country='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
