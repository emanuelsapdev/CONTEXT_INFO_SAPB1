# BinLocationFields — Campos de ubicaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BinLocationFields`
- **Descripción (ES):** Campos de ubicaciones
- **Entity type:** `BinLocationField`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OBFC](../../Tablas%20SAP%20B1/OBFC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BinLocationFields?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BinLocationFields/$count` | Contar |
| Get by key | `GET /b1s/v2/BinLocationFields(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BinLocationFields` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BinLocationFields(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BinLocationFields(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BinLocationFields(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `FieldType` | [BinLocationFieldTypeEnum](../Enums/BinLocationFieldTypeEnum.md) | Yes | Field Type | Tipo de campo |
| 3 | `FieldNumber` | Edm.Int32 | Yes | Field Number | Número del campo |
| 4 | `Name` | Edm.String | Yes | Name | Nombre |
| 5 | `Activated` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Activated | Activado |
| 6 | `DefaultFieldName` | Edm.String | Yes | Default Field Name | Nombre de campo predeterminado |

## Navigation properties (2)

Use `GET /b1s/v2/BinLocationFields(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `WarehouseSublevelCodes` | Collection([WarehouseSublevelCode](../Entidades/WarehouseSublevelCodes.md)) | [WarehouseSublevelCodes](WarehouseSublevelCodes.md) |  | Códigos de subnivel de almacén |
| `BinLocationAttributes` | Collection([BinLocationAttribute](../Entidades/BinLocationAttributes.md)) | [BinLocationAttributes](BinLocationAttributes.md) |  | Atributos de ubicaciones |
