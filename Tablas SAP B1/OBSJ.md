# OBSJ - Backend scheduling job

- **Tabla:** OBSJ
- **Descripción:** Backend scheduling job
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBSJ.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Job ID | Int | 11 | - |  |  |
| 2 | `Type` | Job Type | nVarChar | 100 | - |  |  |
| 3 | `Desc` | Description | nVarChar | 100 | - |  |  |
| 4 | `Status` | Status | VarChar | 1 | - | S | `S` = Scheduled<br>`R` = Running<br>`E` = Error<br>`F` = Finished<br>`P` = Pending<br>`C` = Creating<br>`K` = Cancel |
| 5 | `Schedule` | Schedule Type | VarChar | 1 | - | O | `O` = Once |
| 6 | `NextDate` | Next Running Date | Date | 8 | - |  |  |
| 7 | `NextTime` | Next Running Time | Int | 6 | - |  |  |
| 8 | `BFParams` | Begin Function Parameters | Text | 16 | - |  |  |
| 9 | `EFParams` | End Function Parameters | Text | 16 | - |  |  |
| 10 | `BFRetry` | Begin Function Retry Times | Int | 11 | - | 0 |  |
| 11 | `EFRetry` | End Function Retry Times | Int | 11 | - | 0 |  |
| 12 | `RunAs` | Callback Run as User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `Message` | Status Message | nVarChar | 200 | - |  |  |
| 14 | `RunType` | Run Type | VarChar | 1 | - | M | `M` = Manual<br>`A` = Automatic |
| 15 | `RunAt` | Execution For | VarChar | 1 | - |  | `S` = Scheduled Task<br>`A` = Ad-Hoc Task |
| 16 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 17 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 18 | `NavParam` | Navigation Target Parameters | nVarChar | 200 | - |  |  |
| 19 | `JobType` | Job Type | Int | 11 | - |  | `157` = Payment Wizard<br>`1730000000` = EDF Wizard<br>`234003336` = DATEV Export<br>`540000035` = Purchase Quotation Generation Wizard<br>`233` = Document Generation Wizard<br>`-20000` = Test Wizard |
| 20 | `RefEntry` | Reference Entry | Int | 11 | - |  |  |
| 21 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 22 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 23 | `EndDate` | End Date | Date | 8 | - |  |  |
| 24 | `EndTime` | End Time | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
