# ExtendedTranslation_ResultLine — Líneas de resultados de traducción ampliada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExtendedTranslation_ResultLine`
- **Descripción (ES):** Líneas de resultados de traducción ampliada
- **Description (EN):** Extended Translation Result Line

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `SubLineNumber` | Edm.Int32 | Yes | Sub Line Number | Número de sublínea |
| 4 | `LanguageCode` | Edm.Int32 | Yes | Language Code | Código de idioma |
| 5 | `TranslatedText` | Edm.String | Yes | Translated Text | Texto traducido |

## Used by (properties)

- [ExtendedTranslation_ItemLine](ExtendedTranslation_ItemLine.md).`ExtendedTranslation_ResultLines`
