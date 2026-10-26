# IndiaSacCode — India - Códigos SAC

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `IndiaSacCode`
- **Descripción (ES):** India - Códigos SAC
- **Entity type:** `IndiaSacCode`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OSAC](../../Tablas%20SAP%20B1/OSAC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/IndiaSacCode?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/IndiaSacCode/$count` | Contar |
| Get by key | `GET /b1s/v2/IndiaSacCode(1)` | Obtener por clave |
| Create | `POST /b1s/v2/IndiaSacCode` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/IndiaSacCode(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/IndiaSacCode(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/IndiaSacCode(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ServiceCode` | Edm.String | Yes | Service Code | Código de servicio |
| 3 | `ServiceName` | Edm.String | Yes | Service Name | Nombre del servicio |

## Navigation properties (1)

Use `GET /b1s/v2/IndiaSacCode(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
