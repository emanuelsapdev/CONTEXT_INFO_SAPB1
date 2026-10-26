# NCMCodesSetup — Configuración de códigos NCM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `NCMCodesSetup`
- **Descripción (ES):** Configuración de códigos NCM
- **Entity type:** `NCMCodeSetup`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [ONCM](../../Tablas%20SAP%20B1/ONCM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/NCMCodesSetup?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/NCMCodesSetup/$count` | Contar |
| Get by key | `GET /b1s/v2/NCMCodesSetup(1)` | Obtener por clave |
| Create | `POST /b1s/v2/NCMCodesSetup` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/NCMCodesSetup(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/NCMCodesSetup(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/NCMCodesSetup(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `NCMCode` | Edm.String | Yes | NCM Code | Código NCM |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `GroupCode` | Edm.String | Yes | Group Code | Código de grupo |

## Navigation properties (2)

Use `GET /b1s/v2/NCMCodesSetup(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `DNFCodeSetup` | Collection([DNFCodeSetup](../Entidades/DNFCodeSetup.md)) | [DNFCodeSetup](DNFCodeSetup.md) |  | Configuración de códigos DNF |
