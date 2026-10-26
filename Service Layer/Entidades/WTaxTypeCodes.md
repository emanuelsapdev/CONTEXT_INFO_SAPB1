# WTaxTypeCodes — Códigos de tipo de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WTaxTypeCodes`
- **Descripción (ES):** Códigos de tipo de retención
- **Entity type:** `WTaxTypeCode`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OWTT](../../Tablas%20SAP%20B1/OWTT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WTaxTypeCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WTaxTypeCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/WTaxTypeCodes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/WTaxTypeCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WTaxTypeCodes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WTaxTypeCodes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/WTaxTypeCodes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/WTaxTypeCodes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SpecificWTHAmountsService` | Collection([SpecificWTHAmounts](../Entidades/SpecificWTHAmountsService.md)) | [SpecificWTHAmountsService](SpecificWTHAmountsService.md) |  | Importes de retención específicos |
