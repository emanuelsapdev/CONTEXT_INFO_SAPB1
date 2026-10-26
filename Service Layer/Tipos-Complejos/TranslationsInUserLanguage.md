# TranslationsInUserLanguage — Traducciones en idiomas de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TranslationsInUserLanguage`
- **Descripción (ES):** Traducciones en idiomas de usuario
- **Description (EN):** Translations In User Language
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `KeyFromHeaderTable` | Edm.Int32 | Yes | Key From Header Table | Clave de la tabla de cabecera |
| 2 | `LanguageCodeOfUserLanguage` | Edm.Int32 | Yes | Language Code Of User Language | Código del idioma de usuario |
| 3 | `Translationscontent` | Edm.String | Yes | Translationscontent | Contenido de traducciones |

## Used by (properties)

- [MultiLanguageTranslation](../Entidades/MultiLanguageTranslations.md).`TranslationsInUserLanguages`
