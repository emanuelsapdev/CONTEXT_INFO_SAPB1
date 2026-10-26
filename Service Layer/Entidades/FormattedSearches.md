# FormattedSearches — Búsquedas formateadas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `FormattedSearches`
- **Descripción (ES):** Búsquedas formateadas
- **Entity type:** `FormattedSearch` (open type: accepts dynamic/UDF properties)
- **Key:** `Index` (Edm.Int32)
- **DB tables (main / lines):** [CSHS](../../Tablas%20SAP%20B1/CSHS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 13 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/FormattedSearches?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/FormattedSearches/$count` | Contar |
| Get by key | `GET /b1s/v2/FormattedSearches(1)` | Obtener por clave |
| Create | `POST /b1s/v2/FormattedSearches` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/FormattedSearches(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/FormattedSearches(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/FormattedSearches(1)` (only if the B1 object allows removal) | Borrar |

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormID` | Edm.String | Yes | Form ID | ID de formulario |
| 2 | `ItemID` | Edm.String | Yes | Item ID | ID de artículo |
| 3 | `ColumnID` | Edm.String | Yes | Column ID | ID de columna |
| 4 | `Action` | [BoFormattedSearchActionEnum](../Enums/BoFormattedSearchActionEnum.md) | Yes | Action | Acción |
| 5 | `QueryID` | Edm.Int32 | Yes | Query ID | ID de consulta |
| 6 | `Index` 🔑 | Edm.Int32 | No | Index | Índice |
| 7 | `Refresh` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Refresh | Actualizar |
| 8 | `FieldID` | Edm.String | Yes | Field ID | ID del campo |
| 9 | `ForceRefresh` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Force Refresh | Forzar actualización |
| 10 | `ByField` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | By Field | Por campo |
| 11 | `ByFieldEx` | [FormattedSearchByFieldEnum](../Enums/FormattedSearchByFieldEnum.md) | Yes | By Field Ex | Por campo (ampliado) |
| 12 | `UserValidValues` | Collection([UserValidValue](../Tipos-Complejos/UserValidValue.md)) | Yes | User Valid Values | Valores válidos del usuario |
| 13 | `FieldIDs` | Collection([FieldID](../Tipos-Complejos/FieldID.md)) | Yes | Field I Ds | IDs de campos |
