# OCRY - Countries/Regions

- **Tabla:** OCRY
- **Descripción:** Countries/Regions
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRY.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 3 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `AddrFormat` | Address Format | Int | 6 | [OADF](OADF.md) |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `IsEC` | EU | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `ReportCode` | Code for Reports | nVarChar | 3 | - |  |  |
| 7 | `TaxIdDigts` | No. of Digits for Tax ID | Int | 6 | - |  |  |
| 8 | `BnkCodDgts` | No. of Digits for Bank Code | Int | 11 | - |  |  |
| 9 | `BnkBchDgts` | No. of Digits for Branch | Int | 11 | - |  |  |
| 10 | `BnkActDgts` | No. of Digits for Account No. | Int | 11 | - |  |  |
| 11 | `BnkCtKDgts` | No. of Digits for Control No. | Int | 11 | - |  |  |
| 12 | `ValDomAcct` | Domestic Bank Acct. Validation | nVarChar | 3 | - | XX | `XX`<br>`BE` = Belgium<br>`ES` = Spain<br>`FR` = France<br>`IT` = Italy<br>`NL` = Netherlands<br>`PT` = Portugal |
| 13 | `ValIban` | IBAN Validation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `IsBlackLst` | On Black List | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `UICCode` | UIC Country Code | nVarChar | 3 | - |  |  |
| 16 | `CntCodNum` | Country/Region Code Number | nVarChar | 4 | - |  |  |
| 17 | `Siscomex` | SISCOMEX Country/Region Code | nVarChar | 3 | - |  |  |
| 18 | `IsIntraS` | Intrastat Trans. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `EAEU` | EAEU | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `ISO2Code` | ISO Alpha-2 Code | nVarChar | 2 | - |  |  |
| 21 | `ISO3Code` | ISO Alpha-3 Code | nVarChar | 3 | - |  |  |
| 22 | `ISONumeric` | ISO Numeric | nVarChar | 3 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
