# LengthMeasures — Unidades de longitud

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `LengthMeasures`
- **Descripción (ES):** Unidades de longitud
- **Entity type:** `LengthMeasure` (open type: accepts dynamic/UDF properties)
- **Key:** `UnitCode` (Edm.Int32)
- **DB tables (main / lines):** [OLGT](../../Tablas%20SAP%20B1/OLGT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/LengthMeasures?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/LengthMeasures/$count` | Contar |
| Get by key | `GET /b1s/v2/LengthMeasures(1)` | Obtener por clave |
| Create | `POST /b1s/v2/LengthMeasures` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/LengthMeasures(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/LengthMeasures(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/LengthMeasures(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UnitCode` 🔑 | Edm.Int32 | No | Unit Code | Código de unidad |
| 2 | `UnitDisplay` | Edm.String | Yes | Unit Display | Visualización de unidad |
| 3 | `UnitName` | Edm.String | Yes | Unit Name | Nombre de la unidad |
| 4 | `UnitCodeforQuantityDisplay` | Edm.String | Yes | Unit Codefor Quantity Display | Código de unidad para mostrar cantidad |
| 5 | `UnitLengthinmm` | Edm.Double | Yes | Unit Lengthinmm | Longitud de la unidad en mm |
