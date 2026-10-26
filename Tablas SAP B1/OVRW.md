# OVRW - VAT Reposting Wizard

- **Tabla:** OVRW
- **Descripción:** VAT Reposting Wizard
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVRW.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RunName` | Wizard Run Name | nVarChar | 100 | - |  |  |
| 3 | `RunDate` | Wizard Run Date | Date | 8 | - |  |  |
| 4 | `Status` | Status | VarChar | 1 | - | E | `E` = Executed<br>`S` = Saved<br>`D` = Draft<br>`C` = Canceled |
| 5 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 6 | `LedgerType` | Ledger Type | VarChar | 1 | - | S | `S` = Sales<br>`P` = Purchase |
| 7 | `DebitAcc` | Debit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 9 | `JESeries` | Journal Entry Series | nVarChar | 11 | - | 0 |  |
| 10 | `APTISeries` | Invoice Series | nVarChar | 11 | - | 0 |  |
| 11 | `DateType` | Date Type | VarChar | 1 | - | R | `R` = Posting Date<br>`D` = Due Date<br>`T` = Document Date |
| 12 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 13 | `DateTo` | Date To | Date | 8 | - |  |  |
| 14 | `IncCorAlt` | Include Corr. and Alter. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `BPLId` | This field is not used anymore | Int | 11 | [OBPL](OBPL.md) |  |  |
| 16 | `RunType` | Run Type | VarChar | 1 | - | M | `M` = Manual<br>`C` = Automatic - Export - Confirmation Expected<br>`E` = Automatic - Export - Confirmed/Not Confirmed<br>`S` = Separate Accounting |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
