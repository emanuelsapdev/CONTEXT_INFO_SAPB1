# FiscalPrinter — Impresora fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `FiscalPrinter`
- **Descripción (ES):** Impresora fiscal
- **Entity type:** `FiscalPrinter`
- **Key:** `EquipmentNo` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/FiscalPrinter?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/FiscalPrinter/$count` | Contar |
| Get by key | `GET /b1s/v2/FiscalPrinter('value')` | Obtener por clave |
| Create | `POST /b1s/v2/FiscalPrinter` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/FiscalPrinter('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/FiscalPrinter('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/FiscalPrinter('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EquipmentNo` 🔑 | Edm.String | No | Equipment Number | Número de equipo |
| 2 | `Model` | Edm.String | Yes | Model | Modelo |
| 3 | `ManufacturerSerialN` | Edm.String | Yes | Manufacturer Serial N | Número de serie del fabricante |
| 4 | `RegisterNo` | Edm.Int32 | Yes | Register Number | Número de registro |
| 5 | `FiscalDocumentModel` | Edm.String | Yes | Fiscal Document Model | Modelo de documento fiscal |
| 6 | `FiscalPrintersParams` | Collection([FiscalPrinterParams](../Tipos-Complejos/FiscalPrinterParams.md)) | Yes | Fiscal Printers Parameters | Parámetros de impresoras fiscales |

## Navigation properties (2)

Use `GET /b1s/v2/FiscalPrinter('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `NFModel` | [NFModel](../Entidades/NFModels.md) | [NFModels](NFModels.md) | FiscalDocumentModel → AbsEntry | Modelos de Nota Fiscal |
| `POSDailySummary` | Collection([POSDailySummary](../Entidades/POSDailySummary.md)) | [POSDailySummary](POSDailySummary.md) |  | Resumen diario de POS |
