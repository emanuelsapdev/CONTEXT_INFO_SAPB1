# PostingTemplates — Plantillas de contabilización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PostingTemplates`
- **Descripción (ES):** Plantillas de contabilización
- **Entity type:** `PostingTemplates`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OTRT](../../Tablas%20SAP%20B1/OTRT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PostingTemplates?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PostingTemplates/$count` | Contar |
| Get by key | `GET /b1s/v2/PostingTemplates('value')` | Obtener por clave |
| Create | `POST /b1s/v2/PostingTemplates` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PostingTemplates('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PostingTemplates('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/PostingTemplates('value')` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `StampTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Stamp Tax | Impuesto de timbre |
| 4 | `AutomaticVAT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Automatic VAT | IVA automático |
| 5 | `ManageWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage W Tax | Gestionar retenciones |
| 6 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 7 | `PostingTemplatesLineCollection` | Collection([PostingTemplatesLine](../Tipos-Complejos/PostingTemplatesLine.md)) | Yes | Posting Templates Line Collection | Colección de líneas de plantillas de contabilización |
