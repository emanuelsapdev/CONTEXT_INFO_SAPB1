# DeterminationCriterias — Criterios de determinación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DeterminationCriterias`
- **Descripción (ES):** Criterios de determinación
- **Entity type:** `DeterminationCriteria`
- **Key:** `DmcId` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DeterminationCriterias?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DeterminationCriterias/$count` | Contar |
| Get by key | `GET /b1s/v2/DeterminationCriterias(1)` | Obtener por clave |
| Create | `POST /b1s/v2/DeterminationCriterias` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DeterminationCriterias(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DeterminationCriterias(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/DeterminationCriterias(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DmcId` 🔑 | Edm.Int32 | No | Dmc ID | ID DMC |
| 2 | `DeterminationCriteriaProperty` | Edm.String | Yes | Determination Criteria Property | Propiedad del criterio de determinación |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
| 4 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
