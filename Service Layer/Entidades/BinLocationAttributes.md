# BinLocationAttributes — Atributos de ubicaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BinLocationAttributes`
- **Descripción (ES):** Atributos de ubicaciones
- **Entity type:** `BinLocationAttribute`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OBAT](../../Tablas%20SAP%20B1/OBAT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BinLocationAttributes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BinLocationAttributes/$count` | Contar |
| Get by key | `GET /b1s/v2/BinLocationAttributes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BinLocationAttributes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BinLocationAttributes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BinLocationAttributes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BinLocationAttributes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Attribute` | Edm.Int32 | Yes | Attribute | Atributo |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |

## Navigation properties (1)

Use `GET /b1s/v2/BinLocationAttributes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BinLocationField` | [BinLocationField](../Entidades/BinLocationFields.md) | [BinLocationFields](BinLocationFields.md) | Attribute → AbsEntry | Campos de ubicaciones |
