# MultiLanguageTranslations — Traducciones multilingües

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `MultiLanguageTranslations`
- **Descripción (ES):** Traducciones multilingües
- **Entity type:** `MultiLanguageTranslation` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OMLT](../../Tablas%20SAP%20B1/OMLT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/MultiLanguageTranslations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/MultiLanguageTranslations/$count` | Contar |
| Get by key | `GET /b1s/v2/MultiLanguageTranslations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/MultiLanguageTranslations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/MultiLanguageTranslations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/MultiLanguageTranslations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/MultiLanguageTranslations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 2 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 3 | `FieldAlias` | Edm.String | Yes | Field Alias | Alias del campo |
| 4 | `PrimaryKeyofobject` | Edm.String | Yes | Primary Keyofobject | Clave primaria del objeto |
| 5 | `TranslationsInUserLanguages` | Collection([TranslationsInUserLanguage](../Tipos-Complejos/TranslationsInUserLanguage.md)) | Yes | Translations In User Languages | Traducciones en idiomas de usuario |
