# RCT1 - Incoming Payment - Checks

- **Tabla:** RCT1
- **Descripción:** Incoming Payment - Checks
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RCT1.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [ORCT](ORCT.md) |  |  |
| 2 | `LineID` | Row Number | Int | 11 | - |  |  |
| 3 | `DueDate` | Check Date | Date | 8 | - |  |  |
| 4 | `CheckNum` | Check Number | Int | 11 | - |  |  |
| 5 | `BankCode` | Account No. | nVarChar | 30 | - | -1 |  |
| 6 | `Branch` | Branch Number | nVarChar | 50 | - |  |  |
| 7 | `AcctNum` | Account Number | nVarChar | 50 | - |  |  |
| 8 | `Details` | Details | nVarChar | 254 | - |  |  |
| 9 | `Trnsfrable` | Negotiable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `CheckSum` | Check Amount | Num | 19.6 | - |  |  |
| 11 | `Currency` | Check Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 12 | `Flags` | Flags | Int | 11 | - | 0 |  |
| 13 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 24 |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `CountryCod` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 16 | `CheckAct` | Checking Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `CheckAbs` | Check ID Entry | Int | 11 | [OCHH](OCHH.md) |  |  |
| 18 | `BnkActKey` | Bank Account No. | Int | 11 | [DSC1](DSC1.md) |  |  |
| 19 | `ManualChk` | Manual Check | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 20 | `FiscalID` | Fiscal ID | nVarChar | 100 | - |  |  |
| 21 | `OrigIssdBy` | Orginally Issued By | nVarChar | 254 | - |  |  |
| 22 | `Endorse` | Endorse | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `EndorsChNo` | Endorsable Check No. | Int | 11 | [OCHH](OCHH.md) |  |  |
| 24 | `EnAcctNum` | Encryption of Account Number | Text | 16 | - |  |  |
| 25 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 26 | `ECheck` | E-Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineID |
