# BoSuppLangs — Idiomas soportados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSuppLangs`
- **Descripción (ES):** Idiomas soportados
- **Underlying type:** Edm.Int32
- **Members:** 34

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ln_Null` | 0 | Null | Ninguno |
| `ln_Hebrew` | 1 | Hebrew | Hebreo |
| `ln_Spanish_Ar` | 2 | Spanish Ar | Español (Argentina) |
| `ln_English` | 3 | English | Inglés |
| `ln_Polish` | 5 | Polish | Polaco |
| `ln_English_Sg` | 6 | English Sg | Inglés (Singapur) |
| `ln_Spanish_Pa` | 7 | Spanish Pa | Español (Panamá) |
| `ln_English_Gb` | 8 | English Gb | Inglés (Reino Unido) |
| `ln_German` | 9 | German | Alemán |
| `ln_Serbian` | 10 | Serbian | Serbio |
| `ln_Danish` | 11 | Danish | Danés |
| `ln_Norwegian` | 12 | Norwegian | Noruego |
| `ln_Italian` | 13 | Italian | Italiano |
| `ln_Hungarian` | 14 | Hungarian | Húngaro |
| `ln_Chinese` | 15 | Chinese | Chino |
| `ln_Dutch` | 16 | Dutch | Neerlandés |
| `ln_Finnish` | 17 | Finnish | Finés |
| `ln_Greek` | 18 | Greek | Griego |
| `ln_Portuguese` | 19 | Portuguese | Portugués |
| `ln_Swedish` | 20 | Swedish | Sueco |
| `ln_English_Cy` | 21 | English Cy | Inglés (Chipre) |
| `ln_French` | 22 | French | Francés |
| `ln_Spanish` | 23 | Spanish | Español |
| `ln_Russian` | 24 | Russian | Ruso |
| `ln_Spanish_La` | 25 | Spanish La | Español (Latinoamérica) |
| `ln_Czech_Cz` | 26 | Czech Cz | Checo |
| `ln_Slovak_Sk` | 27 | Slovak Sk | Eslovaco |
| `ln_Korean_Kr` | 28 | Korean Kr | Coreano |
| `ln_Portuguese_Br` | 29 | Portuguese Br | Portugués (Brasil) |
| `ln_Japanese_Jp` | 30 | Japanese Jp | Japonés |
| `ln_Turkish_Tr` | 31 | Turkish Tr | Turco |
| `ln_Arabic` | 32 | Arabic | Árabe |
| `ln_Ukrainian` | 33 | Ukrainian | Ucraniano |
| `ln_TrdtnlChinese_Hk` | 35 | Trdtnl Chinese Hk | Chino tradicional (Hong Kong) |

## Used by (3 properties)

- [CompanyInfo](../Tipos-Complejos/CompanyInfo.md).`LanguageCode`
- [User](../Entidades/Users.md).`LanguageCode`
- [UserDefaultGroup](../Entidades/UserDefaultGroups.md).`LanguageCode`
