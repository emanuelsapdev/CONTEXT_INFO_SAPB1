# AHE7 - Savings Payments

- **Tabla:** AHE7
- **Descripción:** Savings Payments
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHE7.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Row | Int | 6 | - |  |  |
| 3 | `ConName` | Contract Name | nVarChar | 50 | - |  |  |
| 4 | `PmntNotes` | Payment Details | nVarChar | 50 | - |  |  |
| 5 | `AN` | Employee | Num | 19.6 | - |  |  |
| 6 | `AG` | Employer | Num | 19.6 | - |  |  |
| 7 | `BankName` | Bank Name | nVarChar | 50 | - |  |  |
| 8 | `BankCode` | Bank Code | nVarChar | 20 | - |  |  |
| 9 | `BankAcct` | Bank Account | nVarChar | 20 | - |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `ANCurrency` | Employee Currency | nVarChar | 3 | - |  |  |
| 12 | `AGCurrency` | Employer Currency | nVarChar | 3 | - |  |  |
| 13 | `Sequence` | Frequency | VarChar | 1 | - | M | `B`<br>`M` = Monthly<br>`Q` = Quarterly<br>`S` = Semi-annually<br>`Y` = Yearly |
| 14 | `EnBnkAcct` | Encryption of Bank Account | Text | 16 | - |  |  |
| 15 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line, LogInstanc |
