# BarCodes — Códigos de barras

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BarCodes`
- **Descripción (ES):** Códigos de barras
- **Entity type:** `BarCode`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OBCD](../../Tablas%20SAP%20B1/OBCD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BarCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BarCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/BarCodes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BarCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BarCodes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BarCodes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BarCodes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 3 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 4 | `Barcode` | Edm.String | Yes | Barcode | Código de barras |
| 5 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |

## Navigation properties (2)

Use `GET /b1s/v2/BarCodes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemNo → ItemCode | Artículos |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | UoMEntry → AbsEntry | Unidades de medida |
