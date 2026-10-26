# OccurrenceCodes — Códigos de ocurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `OccurrenceCodes`
- **Descripción (ES):** Códigos de ocurrencia
- **Entity type:** `OccurenceCode`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OOCC](../../Tablas%20SAP%20B1/OOCC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/OccurrenceCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/OccurrenceCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/OccurrenceCodes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/OccurrenceCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/OccurrenceCodes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/OccurrenceCodes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/OccurrenceCodes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `Note` | Edm.String | Yes | Note | Nota |
| 5 | `RequestedBoeStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | Requested Boe Status | Estado solicitado de la letra de cambio |
| 6 | `IsMovement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Movement | Es movimiento |
