# PickLists — Listas de picking

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PickLists`
- **Descripción (ES):** Listas de picking
- **Entity type:** `PickList` (open type: accepts dynamic/UDF properties)
- **Key:** `Absoluteentry` (Edm.Int32)
- **DB tables (main / lines):** [OPKL](../../Tablas%20SAP%20B1/OPKL.md), [PKL1](../../Tablas%20SAP%20B1/PKL1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PickLists?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PickLists/$count` | Contar |
| Get by key | `GET /b1s/v2/PickLists(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PickLists` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PickLists(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PickLists(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PickLists(1)` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Absoluteentry` 🔑 | Edm.Int32 | No | Absoluteentry | Entrada absoluta (ID interno) |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `OwnerCode` | Edm.Int32 | Yes | Owner Code | Código del titular |
| 4 | `OwnerName` | Edm.String | Yes | Owner Name | Nombre del titular |
| 5 | `PickDate` | Edm.DateTimeOffset | Yes | Pick Date | Fecha de picking |
| 6 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 7 | `Status` | [BoPickStatus](../Enums/BoPickStatus.md) | Yes | Status | Estado |
| 8 | `ObjectType` | Edm.String | Yes | Object Type | Tipo de objeto |
| 9 | `UseBaseUnits` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Base Units | Usar unidades base |
| 10 | `CreateQRCodeFrom` | Edm.String | Yes | Create QR Code From | Crear código QR desde |
| 11 | `PickListsLines` | Collection([PickListsLine](../Tipos-Complejos/PickListsLine.md)) | Yes | Pick Lists Lines | Líneas de la lista de picking |

## Navigation properties (1)

Use `GET /b1s/v2/PickLists(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | OwnerCode → InternalKey | Usuario |

## Service operations that use this type

- [`PickListsService_Close`](../Servicios/PickListsService.md#picklistsservice_close)
- [`PickListsService_UpdateReleasedAllocation`](../Servicios/PickListsService.md#picklistsservice_updatereleasedallocation)
