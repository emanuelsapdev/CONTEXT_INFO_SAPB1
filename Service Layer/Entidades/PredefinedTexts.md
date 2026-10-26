# PredefinedTexts — Textos predefinidos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PredefinedTexts`
- **Descripción (ES):** Textos predefinidos
- **Entity type:** `PredefinedText`
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OPDT](../../Tablas%20SAP%20B1/OPDT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PredefinedTexts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PredefinedTexts/$count` | Contar |
| Get by key | `GET /b1s/v2/PredefinedTexts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PredefinedTexts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PredefinedTexts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PredefinedTexts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PredefinedTexts(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 2 | `TextCode` | Edm.String | Yes | Text Code | Código de texto |
| 3 | `Text` | Edm.String | Yes | Text | Texto |
