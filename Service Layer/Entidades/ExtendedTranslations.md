# ExtendedTranslations — Traducciones ampliadas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ExtendedTranslations`
- **Descripción (ES):** Traducciones ampliadas
- **Entity type:** `ExtendedTranslation`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ExtendedTranslations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ExtendedTranslations/$count` | Contar |
| Get by key | `GET /b1s/v2/ExtendedTranslations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ExtendedTranslations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ExtendedTranslations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ExtendedTranslations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ExtendedTranslations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `Category` | [TranslationCategoryEnum](../Enums/TranslationCategoryEnum.md) | Yes | Category | Categoría |
| 3 | `ID` | Edm.String | Yes | ID | ID |
| 4 | `SecondaryID` | Edm.String | Yes | Secondary ID | ID secundario |
| 5 | `SourceLanguage` | Edm.Int32 | Yes | Source Language | Idioma de origen |
| 6 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 7 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 8 | `ExtendedTranslation_ItemLines` | Collection([ExtendedTranslation_ItemLine](../Tipos-Complejos/ExtendedTranslation_ItemLine.md)) | Yes | Extended Translation Item Lines | Líneas de elementos de traducción ampliada |
