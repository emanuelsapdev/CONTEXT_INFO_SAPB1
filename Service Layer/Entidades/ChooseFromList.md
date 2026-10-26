# ChooseFromList — Selección de lista

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ChooseFromList`
- **Descripción (ES):** Selección de lista
- **Entity type:** `ChooseFromList` (open type: accepts dynamic/UDF properties)
- **Key:** `ObjectName` (Edm.String)
- **DB tables (main / lines):** [CHFL](../../Tablas%20SAP%20B1/CHFL.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ChooseFromList?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ChooseFromList/$count` | Contar |
| Get by key | `GET /b1s/v2/ChooseFromList('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ChooseFromList` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ChooseFromList('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ChooseFromList('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ChooseFromList('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ObjectName` 🔑 | Edm.String | No | Object Name | Nombre del objeto |
| 2 | `ChooseFromList_Lines` | Collection([ChooseFromList_Line](../Tipos-Complejos/ChooseFromList_Line.md)) | Yes | Choose From List Lines | Líneas de selección de lista |
