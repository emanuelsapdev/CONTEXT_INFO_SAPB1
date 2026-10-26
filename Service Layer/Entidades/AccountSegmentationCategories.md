# AccountSegmentationCategories — Categorías de segmentación de cuentas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AccountSegmentationCategories`
- **Descripción (ES):** Categorías de segmentación de cuentas
- **Entity type:** `AccountSegmentationCategory` (open type: accepts dynamic/UDF properties)
- **Key:** `SegmentID` (Edm.Int32), `Code` (Edm.String)
- **DB tables (main / lines):** [OASC](../../Tablas%20SAP%20B1/OASC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AccountSegmentationCategories?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AccountSegmentationCategories/$count` | Contar |
| Get by key | `GET /b1s/v2/AccountSegmentationCategories(SegmentID=1,Code='value')` | Obtener por clave |
| Create | `POST /b1s/v2/AccountSegmentationCategories` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AccountSegmentationCategories(SegmentID=1,Code='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AccountSegmentationCategories(SegmentID=1,Code='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AccountSegmentationCategories(SegmentID=1,Code='value')` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SegmentID` 🔑 | Edm.Int32 | No | Segment ID | ID de segmento |
| 2 | `Code` 🔑 | Edm.String | No | Code | Código |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `ShortName` | Edm.String | Yes | Short Name | Nombre corto |

## Navigation properties (1)

Use `GET /b1s/v2/AccountSegmentationCategories(SegmentID=1,Code='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `AccountSegmentation` | [AccountSegmentation](../Entidades/AccountSegmentations.md) | [AccountSegmentations](AccountSegmentations.md) | SegmentID → Numerator | Segmentaciones de cuentas |
