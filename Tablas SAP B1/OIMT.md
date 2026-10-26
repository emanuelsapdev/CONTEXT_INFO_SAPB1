# OIMT - Templates for Inventory JE

- **Tabla:** OIMT
- **Descripción:** Templates for Inventory JE
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIMT.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ValuatType` | Document Valuation Type | VarChar | 1 | - | N | `A`<br>`F`<br>`S`<br>`N` = unDefined |
| 2 | `TransType` | Transaction type | Int | 11 | - | -1 |  |
| 3 | `BaseType` | Base Transaction Type | Int | 6 | - | -1 |  |
| 4 | `TemplateId` | Template ID | Int | 6 | - | -1 |  |
| 5 | `LocalizId` | Localization Identifier | nVarChar | 2 | - | XX | `XX` = All Localizations |
| 6 | `Action` | Action Type | Int | 6 | - | 0 |  |
| 7 | `JEPosting` | Posting Status | VarChar | 1 | - | N | `N` = None<br>`C` = Complete<br>`P` = Partial |
| 8 | `LineActTyp` | Line Account Type | Int | 6 | - | 2 | `2` = LINE_ACCT_TYPE |
| 9 | `TmpType` | Template Type | Int | 6 | - | 0 |  |
| 10 | `Total` | Total Type | VarChar | 1 | - | M | `M` = Total from Message<br>`C` = Total from Calculator<br>`F` = Total from Formula |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TemplateId |
| SECONDARY | Yes | TransType, BaseType, ValuatType, LocalizId, Action, TmpType |
