# Counties — Condados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Counties`
- **Descripción (ES):** Condados
- **Entity type:** `County` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsId` (Edm.Int32)
- **DB tables (main / lines):** [OCNT](../../Tablas%20SAP%20B1/OCNT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Counties?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Counties/$count` | Contar |
| Get by key | `GET /b1s/v2/Counties(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Counties` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Counties(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Counties(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Counties(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` 🔑 | Edm.Int32 | No | Abs ID | ID absoluto |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Country` | Edm.String | Yes | Country | País |
| 4 | `State` | Edm.String | Yes | State | Estado/provincia |
| 5 | `Name` | Edm.String | Yes | Name | Nombre |
| 6 | `IbgeCode` | Edm.String | Yes | Ibge Code | Código IBGE (Brasil) |
| 7 | `GiaCode` | Edm.String | Yes | Gia Code | Código GIA |
| 8 | `TaxZone` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Zone | Zona fiscal |

## Navigation properties (2)

Use `GET /b1s/v2/Counties(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |
