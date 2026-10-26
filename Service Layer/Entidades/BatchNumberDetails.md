# BatchNumberDetails — Detalles de números de lote

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BatchNumberDetails`
- **Descripción (ES):** Detalles de números de lote
- **Entity type:** `BatchNumberDetail` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OBTN](../../Tablas%20SAP%20B1/OBTN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BatchNumberDetails?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BatchNumberDetails/$count` | Contar |
| Get by key | `GET /b1s/v2/BatchNumberDetails(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BatchNumberDetails` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BatchNumberDetails(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BatchNumberDetails(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BatchNumberDetails(1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 3 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 4 | `Status` | [BatchDetailServiceStatusEnum](../Enums/BatchDetailServiceStatusEnum.md) | Yes | Status | Estado |
| 5 | `Batch` | Edm.String | Yes | Batch | Lote |
| 6 | `BatchAttribute1` | Edm.String | Yes | Batch Attribute 1 | Atributo de lote 1 |
| 7 | `BatchAttribute2` | Edm.String | Yes | Batch Attribute 2 | Atributo de lote 2 |
| 8 | `AdmissionDate` | Edm.DateTimeOffset | Yes | Admission Date | Fecha de admisión |
| 9 | `ManufacturingDate` | Edm.DateTimeOffset | Yes | Manufacturing Date | Fecha de fabricación |
| 10 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |
| 11 | `Details` | Edm.String | Yes | Details | Detalles |
| 12 | `SystemNumber` | Edm.Int32 | Yes | System Number | Número del sistema |

## Navigation properties (1)

Use `GET /b1s/v2/BatchNumberDetails(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
