# EmployeeImages — Imágenes de empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmployeeImages`
- **Descripción (ES):** Imágenes de empleados
- **Entity type:** `EmployeeImage`
- **Key:** `EmployeeNo` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmployeeImages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmployeeImages/$count` | Contar |
| Get by key | `GET /b1s/v2/EmployeeImages(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EmployeeImages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmployeeImages(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmployeeImages(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmployeeImages(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeNo` 🔑 | Edm.Int32 | No | Employee Number | Número de empleado |
| 2 | `Picture` | Edm.Int32 | No | Picture | Imagen |
