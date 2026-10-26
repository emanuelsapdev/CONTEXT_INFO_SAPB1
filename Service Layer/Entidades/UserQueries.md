# UserQueries — Consultas de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserQueries`
- **Descripción (ES):** Consultas de usuario
- **Entity type:** `UserQuery` (open type: accepts dynamic/UDF properties)
- **Key:** `InternalKey` (Edm.Int32), `QueryCategory` (Edm.Int32)
- **DB tables (main / lines):** [OUQR](../../Tablas%20SAP%20B1/OUQR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserQueries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserQueries/$count` | Contar |
| Get by key | `GET /b1s/v2/UserQueries(InternalKey=1,QueryCategory=1)` | Obtener por clave |
| Create | `POST /b1s/v2/UserQueries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserQueries(InternalKey=1,QueryCategory=1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserQueries(InternalKey=1,QueryCategory=1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserQueries(InternalKey=1,QueryCategory=1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InternalKey` 🔑 | Edm.Int32 | No | Internal Key | Clave interna |
| 2 | `QueryCategory` 🔑 | Edm.Int32 | No | Query Category | Categoría de consulta |
| 3 | `QueryDescription` | Edm.String | Yes | Query Description | Descripción de la consulta |
| 4 | `Query` | Edm.String | Yes | Query | Consulta |
| 5 | `ProcedureAlias` | Edm.String | Yes | Procedure Alias | Alias del procedimiento |
| 6 | `ProcedureName` | Edm.String | Yes | Procedure Name | Nombre del procedimiento |
| 7 | `QueryType` | [UserQueryTypeEnum](../Enums/UserQueryTypeEnum.md) | Yes | Query Type | Tipo de consulta |
| 8 | `MenuCaption` | Edm.String | Yes | Menu Caption | Título del menú |
| 9 | `ParentMenuID` | Edm.Int32 | Yes | Parent Menu ID | ID del menú padre |
| 10 | `MenuPosition` | Edm.Int32 | Yes | Menu Position | Posición del menú |
| 11 | `MenuUniqueID` | Edm.String | Yes | Menu Unique ID | ID único del menú |
| 12 | `EnableMenuEntry` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Menu Entry | Habilitar entrada de menú |

## Navigation properties (1)

Use `GET /b1s/v2/UserQueries(InternalKey=1,QueryCategory=1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `QueryCategory2` | [QueryCategory](../Entidades/QueryCategories.md) | [QueryCategories](QueryCategories.md) | QueryCategory → Code | Categorías de consultas |
