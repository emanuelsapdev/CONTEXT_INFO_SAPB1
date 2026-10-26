# ODTV - DATEV Export

- **Tabla:** ODTV
- **Descripción:** DATEV Export
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODTV.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | - |  |  |
| 2 | `Status` | Datev Run Status | VarChar | 1 | - | 1 | `1` = In Preparation<br>`2` = Scheduled<br>`3` = Running<br>`4` = Finished<br>`5` = Failed |
| 3 | `Descrp` | Description | nVarChar | 30 | - |  |  |
| 4 | `ExportPath` | Export Path | nVarChar | 254 | - |  |  |
| 5 | `Updater` | Updater | nVarChar | 25 | - |  |  |
| 6 | `GLAccounts` | Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Suppliers` | Suppliers | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Customers` | Customers | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `Journals` | Journals | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `AllJETypes` | All Journal Entries | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `Manual` | Manual Journal Entries | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `Purchase` | Purchase Invoices/Credit Notes | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Sales` | Sales Invoices/Credit Notes | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `DateType` | Date Type | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 16 | `EndDate` | End Date | Date | 8 | - |  |  |
| 17 | `StartFisc` | Start of the Fiscal Year | Date | 8 | - |  |  |
| 18 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 19 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 20 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 21 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 22 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 23 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 24 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 25 | `RunType` | DATEV Run Type | VarChar | 1 | - | F | `F` = Full Run<br>`D` = Delta Run |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId |
