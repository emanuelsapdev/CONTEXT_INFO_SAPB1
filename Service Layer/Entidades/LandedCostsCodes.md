# LandedCostsCodes — Códigos de costos de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `LandedCostsCodes`
- **Descripción (ES):** Códigos de costos de importación
- **Entity type:** `LandedCostsCode` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OALC](../../Tablas%20SAP%20B1/OALC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/LandedCostsCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/LandedCostsCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/LandedCostsCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/LandedCostsCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/LandedCostsCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/LandedCostsCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/LandedCostsCodes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `AllocationBy` | [BoAllocationByEnum](../Enums/BoAllocationByEnum.md) | Yes | Allocation By | Asignación por |
| 4 | `LandedCostsAllocationAccount` | Edm.String | Yes | Landed Costs Allocation Account | Cuenta de asignación de costos de importación |
