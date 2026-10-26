# NotaFiscalCFOP — CFOP de Nota Fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `NotaFiscalCFOP`
- **Descripción (ES):** CFOP de Nota Fiscal
- **Entity type:** `NotaFiscalCFOP` (open type: accepts dynamic/UDF properties)
- **Key:** `ID` (Edm.Int32)
- **DB tables (main / lines):** [OCFP](../../Tablas%20SAP%20B1/OCFP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/NotaFiscalCFOP?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/NotaFiscalCFOP/$count` | Contar |
| Get by key | `GET /b1s/v2/NotaFiscalCFOP(1)` | Obtener por clave |
| Create | `POST /b1s/v2/NotaFiscalCFOP` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/NotaFiscalCFOP(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/NotaFiscalCFOP(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/NotaFiscalCFOP(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` 🔑 | Edm.Int32 | No | ID | ID |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `Application` | Edm.String | Yes | Application | Aplicación |

## Navigation properties (1)

Use `GET /b1s/v2/NotaFiscalCFOP(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `NotaFiscalUsage` | Collection([NotaFiscalUsage](../Entidades/NotaFiscalUsage.md)) | [NotaFiscalUsage](NotaFiscalUsage.md) |  | Uso de Nota Fiscal |
