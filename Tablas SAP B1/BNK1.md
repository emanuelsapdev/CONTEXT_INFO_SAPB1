# BNK1 - Bank Statement - Documents List

- **Tabla:** BNK1
- **Descripción:** Bank Statement - Documents List
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BNK1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | Bank Statement ID | Int | 11 | - |  |  |
| 2 | `BSLine` | Bank Statement Line ID | Int | 11 | - |  |  |
| 3 | `ListLineID` | List Line ID | Int | 6 | - |  |  |
| 4 | `DocID` | Document Identifier | nVarChar | 35 | - |  |  |
| 5 | `AmntLC` | Amount (LC) | Num | 19.6 | - |  |  |
| 6 | `AmnFC` | Amount (FC) | Num | 19.6 | - |  |  |
| 7 | `IsDebit` | Debit [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdNumber, BSLine, ListLineID |
