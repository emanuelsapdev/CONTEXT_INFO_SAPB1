# PWZ2 - Payment Wizard - Rows 2

- **Tabla:** PWZ2
- **Descripción:** Payment Wizard - Rows 2
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ2.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `PymCode` | Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 3 | `BnkAccount` | Bank Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `MaxIncom` | Max. Incoming Amount | Num | 19.6 | - |  |  |
| 5 | `MaxOutgo` | Max. Outgoing Amount | Num | 19.6 | - |  |  |
| 6 | `Balance` | G/L Balance | Num | 19.6 | - |  |  |
| 7 | `ExpectBal` | Expected G/L Balance | Num | 19.6 | - |  |  |
| 8 | `Checked` | Checked | VarChar | 1 | - |  |  |
| 9 | `PymDisc` | Payment Description | nVarChar | 100 | - |  |  |
| 10 | `PymType` | Payment Type | VarChar | 1 | - |  |  |
| 11 | `IntBalance` | G/L Interim Balance | Num | 19.6 | - |  |  |
| 12 | `ExpIntBal` | Expected G/L Interim Balance | Num | 19.6 | - |  |  |
| 13 | `InterimAct` | Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 14 | `BnkCountry` | Bank Country/Region | nVarChar | 3 | - |  |  |
| 15 | `BnkCode` | Bank Code | nVarChar | 30 | - |  |  |
| 16 | `BnkAccNo` | Bank Account Number | nVarChar | 50 | - |  |  |
| 17 | `FatherLn` | Parent Line | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `NegativPym` | Negative Payment Method Code | nVarChar | 15 | - |  |  |
| 19 | `NegPymBnk` | Negative Payment Bank Code | nVarChar | 30 | - |  |  |
| 20 | `NegCountry` | Negative Payment Bank Country | nVarChar | 3 | - |  |  |
| 21 | `NegPymAcct` | Negative Payment Bank Account | nVarChar | 50 | - |  |  |
| 22 | `PaymenMean` | Payment Means | VarChar | 1 | - |  |  |
| 23 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 24 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 25 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 26 | `EnBnkAccNo` | Encryption of Bank Account No. | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, PymCode |
