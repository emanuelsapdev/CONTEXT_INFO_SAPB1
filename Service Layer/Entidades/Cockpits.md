# Cockpits — Cockpits

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Cockpits`
- **Descripción (ES):** Cockpits
- **Entity type:** `Cockpit`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OCPT](../../Tablas%20SAP%20B1/OCPT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 10 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Cockpits?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Cockpits/$count` | Contar |
| Get by key | `GET /b1s/v2/Cockpits(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Cockpits` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Cockpits(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Cockpits(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Cockpits(1)` (only if the B1 object allows removal) | Borrar |

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.Int32 | Yes | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `Description` | Edm.String | Yes | Description | Descripción |
| 5 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 6 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 7 | `Time` | Edm.TimeOfDay | Yes | Time | Hora |
| 8 | `Manufacturer` | Edm.String | Yes | Manufacturer | Fabricante |
| 9 | `Publisher` | Edm.String | Yes | Publisher | Publicador |
| 10 | `CockpitType` | [BoCockpitTypeEnum](../Enums/BoCockpitTypeEnum.md) | Yes | Cockpit Type | Tipo de cockpit |

## Navigation properties (1)

Use `GET /b1s/v2/Cockpits(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |

## Service operations that use this type

- [`CockpitsService_PublishCockpit`](../Servicios/CockpitsService.md#cockpitsservice_publishcockpit)
