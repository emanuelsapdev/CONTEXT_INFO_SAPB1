# RetornoCodes — Códigos de retorno

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `RetornoCodes`
- **Descripción (ES):** Códigos de retorno
- **Entity type:** `RetornoCode`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/RetornoCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/RetornoCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/RetornoCodes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/RetornoCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/RetornoCodes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/RetornoCodes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/RetornoCodes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `OccurenceCode` | Edm.Int32 | Yes | Occurence Code | Código de ocurrencia |
| 3 | `MovementCode` | Edm.Int32 | Yes | Movement Code | Código de movimiento |
| 4 | `BoeStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | Boe Status | Estado de letra de cambio |
| 5 | `Description` | Edm.String | Yes | Description | Descripción |
| 6 | `Color` | Edm.Int32 | Yes | Color | Color |
| 7 | `FileFormat` | Edm.String | Yes | File Format | Formato de archivo |
| 8 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
