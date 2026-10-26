# DynamicSystemStrings — Cadenas dinámicas del sistema

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DynamicSystemStrings`
- **Descripción (ES):** Cadenas dinámicas del sistema
- **Entity type:** `DynamicSystemString` (open type: accepts dynamic/UDF properties)
- **Key:** `FormID` (Edm.String), `ItemID` (Edm.String), `ColumnID` (Edm.String)
- **DB tables (main / lines):** [SDIS](../../Tablas%20SAP%20B1/SDIS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DynamicSystemStrings?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DynamicSystemStrings/$count` | Contar |
| Get by key | `GET /b1s/v2/DynamicSystemStrings(FormID='value',ItemID='value',ColumnID='value')` | Obtener por clave |
| Create | `POST /b1s/v2/DynamicSystemStrings` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DynamicSystemStrings(FormID='value',ItemID='value',ColumnID='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DynamicSystemStrings(FormID='value',ItemID='value',ColumnID='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DynamicSystemStrings(FormID='value',ItemID='value',ColumnID='value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormID` 🔑 | Edm.String | No | Form ID | ID de formulario |
| 2 | `ItemID` 🔑 | Edm.String | No | Item ID | ID de artículo |
| 3 | `ColumnID` 🔑 | Edm.String | No | Column ID | ID de columna |
| 4 | `ItemString` | Edm.String | Yes | Item String | Cadena del artículo |
| 5 | `IsBold` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Bold | Negrita |
| 6 | `IsItalics` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Italics | Cursiva |
