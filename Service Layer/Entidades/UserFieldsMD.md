# UserFieldsMD — Metadatos de campos de usuario (UDF)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserFieldsMD`
- **Descripción (ES):** Metadatos de campos de usuario (UDF)
- **Entity type:** `UserFieldMD`
- **Key:** `TableName` (Edm.String), `FieldID` (Edm.Int32)
- **DB tables (main / lines):** [CUFD](../../Tablas%20SAP%20B1/CUFD.md), [UFD1](../../Tablas%20SAP%20B1/UFD1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 14 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserFieldsMD?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserFieldsMD/$count` | Contar |
| Get by key | `GET /b1s/v2/UserFieldsMD(TableName='value',FieldID=1)` | Obtener por clave |
| Create | `POST /b1s/v2/UserFieldsMD` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserFieldsMD(TableName='value',FieldID=1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserFieldsMD(TableName='value',FieldID=1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserFieldsMD(TableName='value',FieldID=1)` (only if the B1 object allows removal) | Borrar |

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` | Edm.String | Yes | Name | Nombre |
| 2 | `Type` | [BoFieldTypes](../Enums/BoFieldTypes.md) | Yes | Type | Tipo |
| 3 | `Size` | Edm.Int32 | Yes | Size | Tamaño |
| 4 | `Description` | Edm.String | Yes | Description | Descripción |
| 5 | `SubType` | [BoFldSubTypes](../Enums/BoFldSubTypes.md) | Yes | Sub Type | Subtipo |
| 6 | `LinkedTable` | Edm.String | Yes | Linked Table | Tabla vinculada |
| 7 | `DefaultValue` | Edm.String | Yes | Default Value | Valor predeterminado |
| 8 | `TableName` 🔑 | Edm.String | No | Table Name | Nombre de la tabla |
| 9 | `FieldID` 🔑 | Edm.Int32 | No | Field ID | ID del campo |
| 10 | `EditSize` | Edm.Int32 | Yes | Edit Size | Tamaño de edición |
| 11 | `Mandatory` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Mandatory | Obligatorio |
| 12 | `LinkedUDO` | Edm.String | Yes | Linked UDO | UDO vinculado |
| 13 | `LinkedSystemObject` | [UDFLinkedSystemObjectTypesEnum](../Enums/UDFLinkedSystemObjectTypesEnum.md) | Yes | Linked System Object | Objeto del sistema vinculado |
| 14 | `ValidValuesMD` | Collection([ValidValueMD](../Tipos-Complejos/ValidValueMD.md)) | Yes | Valid Values Metadata | Valores válidos (metadatos) |

## Navigation properties (1)

Use `GET /b1s/v2/UserFieldsMD(TableName='value',FieldID=1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserTablesMD` | [UserTablesMD](../Entidades/UserTablesMD.md) | [UserTablesMD](UserTablesMD.md) | LinkedTable → TableName | Metadatos de tablas de usuario (UDT) |
