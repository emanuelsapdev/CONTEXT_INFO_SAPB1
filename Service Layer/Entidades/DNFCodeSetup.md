# DNFCodeSetup — Configuración de códigos DNF

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DNFCodeSetup`
- **Descripción (ES):** Configuración de códigos DNF
- **Entity type:** `DNFCodeSetup`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODNF](../../Tablas%20SAP%20B1/ODNF.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DNFCodeSetup?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DNFCodeSetup/$count` | Contar |
| Get by key | `GET /b1s/v2/DNFCodeSetup(1)` | Obtener por clave |
| Create | `POST /b1s/v2/DNFCodeSetup` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DNFCodeSetup(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DNFCodeSetup(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/DNFCodeSetup(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `NCMCode` | Edm.Int32 | Yes | NCM Code | Código NCM |
| 3 | `DNFCode` | Edm.String | Yes | DNF Code | Código DNF |
| 4 | `UoM` | Edm.String | Yes | Uo M | Unidad de medida |
| 5 | `Factor` | Edm.Double | Yes | Factor | Factor |

## Navigation properties (2)

Use `GET /b1s/v2/DNFCodeSetup(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `NCMCodeSetup` | [NCMCodeSetup](../Entidades/NCMCodesSetup.md) | [NCMCodesSetup](NCMCodesSetup.md) | NCMCode → AbsEntry | Configuración de códigos NCM |
