# UserTablesMD — Metadatos de tablas de usuario (UDT)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserTablesMD`
- **Descripción (ES):** Metadatos de tablas de usuario (UDT)
- **Entity type:** `UserTablesMD` (open type: accepts dynamic/UDF properties)
- **Key:** `TableName` (Edm.String)
- **DB tables (main / lines):** [OUTB](../../Tablas%20SAP%20B1/OUTB.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserTablesMD?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserTablesMD/$count` | Contar |
| Get by key | `GET /b1s/v2/UserTablesMD('value')` | Obtener por clave |
| Create | `POST /b1s/v2/UserTablesMD` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserTablesMD('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserTablesMD('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserTablesMD('value')` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TableName` 🔑 | Edm.String | No | Table Name | Nombre de la tabla |
| 2 | `TableDescription` | Edm.String | Yes | Table Description | Descripción de la tabla |
| 3 | `TableType` | [BoUTBTableType](../Enums/BoUTBTableType.md) | Yes | Table Type | Tipo de tabla |
| 4 | `Archivable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Archivable | Archivable |
| 5 | `ArchiveDateField` | Edm.String | Yes | Archive Date Field | Campo de fecha para archivado |
| 6 | `DisplayMenu` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Menu | Mostrar menú |
| 7 | `ApplyAuthorization` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Authorization | Aplicar autorización |

## Navigation properties (2)

Use `GET /b1s/v2/UserTablesMD('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserFieldsMD` | Collection([UserFieldMD](../Entidades/UserFieldsMD.md)) | [UserFieldsMD](UserFieldsMD.md) |  | Metadatos de campos de usuario (UDF) |
| `UserObjectsMD` | Collection([UserObjectsMD](../Entidades/UserObjectsMD.md)) | [UserObjectsMD](UserObjectsMD.md) |  | Metadatos de objetos de usuario (UDO) |
