# OHSV - Hasavsevet Journal Entry

- **Tabla:** OHSV
- **Descripción:** Hasavsevet Journal Entry
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHSV.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RecordKey` | Record Number | nVarChar | 7 | - |  |  |
| 2 | `Ref1` | Reference 1 | nVarChar | 5 | - |  |  |
| 3 | `Ref2` | Reference 2 | nVarChar | 5 | - |  |  |
| 4 | `RefDate` | Posting Date | nVarChar | 6 | - |  |  |
| 5 | `DueDate` | Due Date | nVarChar | 6 | - |  |  |
| 6 | `CurrCode` | Currency Code | nVarChar | 3 | - |  |  |
| 7 | `Memo` | Details | nVarChar | 22 | - |  |  |
| 8 | `DebAcct1` | Debit Account 1 | nVarChar | 8 | - |  |  |
| 9 | `CredAcct1` | Credit Account 1 | nVarChar | 8 | - |  |  |
| 10 | `DebAmnt1` | Debit | nVarChar | 12 | - |  |  |
| 11 | `credAmnt1` | Credit | nVarChar | 12 | - |  |  |
| 12 | `FDebAmnt1` | Debit Amount 1 in FC | nVarChar | 12 | - |  |  |
| 13 | `FCredAmnt1` | Credit in FC | nVarChar | 12 | - |  |  |
| 14 | `Filler` | Filler | nVarChar | 60 | - |  |  |
| 15 | `EndField` | Ending Field | nVarChar | 2 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RecordKey |
