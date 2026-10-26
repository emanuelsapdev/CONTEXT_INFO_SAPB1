# OELS - Elster Run

- **Tabla:** OELS
- **Descripción:** Elster Run
- **Cantidad de campos:** 30
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OELS.html

## Campos (30)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | - |  |  |
| 2 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 3 | `DateType` | Date Type | VarChar | 1 | - |  | `P` = Posting Date<br>`D` = Document Date<br>`V` = VAT Date<br>`C` = System Date |
| 4 | `FromDate` | Date From | Date | 8 | - |  |  |
| 5 | `ToDate` | Date To | Date | 8 | - |  |  |
| 6 | `CreditMemo` | Credit Memos | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 7 | `Status` | Status | VarChar | 1 | - |  |  |
| 8 | `CompnyName` | Company Name | nVarChar | 200 | - |  |  |
| 9 | `CountyCode` | County Code | nVarChar | 100 | - |  |  |
| 10 | `TaxOffice` | Tax Office | nVarChar | 100 | - |  |  |
| 11 | `TaxNum` | Tax Number | nVarChar | 32 | - |  |  |
| 12 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 13 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 14 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `RevAutoDeb` | Revoke Automatic Debit | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 18 | `AmenReturn` | Amended Return | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 19 | `CreOffPref` | Credit Offer Prefer | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 20 | `Documents` | Documents | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 21 | `TestRun` | Test Run | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 22 | `Street` | Street | nVarChar | 100 | - |  |  |
| 23 | `City` | City | nVarChar | 100 | - |  |  |
| 24 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 25 | `Block` | Block | nVarChar | 100 | - |  |  |
| 26 | `Descript` | Description | nVarChar | 100 | - |  |  |
| 27 | `NoteType` | Supplementary Note Type | VarChar | 1 | - |  |  |
| 28 | `Note` | Supplementary Note | nVarChar | 100 | - |  |  |
| 29 | `SpecialAdP` | Special Advance Payment | Num | 19.6 | - |  |  |
| 30 | `InputData` | Input Data | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId |
