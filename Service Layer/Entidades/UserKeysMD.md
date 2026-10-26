# UserKeysMD — Metadatos de claves de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserKeysMD`
- **Descripción (ES):** Metadatos de claves de usuario
- **Entity type:** `UserKeysMD` (open type: accepts dynamic/UDF properties)
- **Key:** `TableName` (Edm.String), `KeyIndex` (Edm.Int32)
- **DB tables (main / lines):** [OUKD](../../Tablas%20SAP%20B1/OUKD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserKeysMD?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserKeysMD/$count` | Contar |
| Get by key | `GET /b1s/v2/UserKeysMD(TableName='value',KeyIndex=1)` | Obtener por clave |
| Create | `POST /b1s/v2/UserKeysMD` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserKeysMD(TableName='value',KeyIndex=1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserKeysMD(TableName='value',KeyIndex=1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserKeysMD(TableName='value',KeyIndex=1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TableName` 🔑 | Edm.String | No | Table Name | Nombre de la tabla |
| 2 | `KeyIndex` 🔑 | Edm.Int32 | No | Key Index | Índice de clave |
| 3 | `KeyName` | Edm.String | Yes | Key Name | Nombre de clave |
| 4 | `Unique` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Unique | Único |
| 5 | `UserKeysMD_Elements` | Collection([UserKeysMD_Element](../Tipos-Complejos/UserKeysMD_Element.md)) | Yes | User Keys Metadata Elements | Elementos de la clave de usuario |
