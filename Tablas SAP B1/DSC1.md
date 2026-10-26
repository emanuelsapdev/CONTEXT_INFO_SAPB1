# DSC1 - House Bank Accounts

- **Tabla:** DSC1
- **Descripción:** House Bank Accounts
- **Cantidad de campos:** 83
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DSC1.html

## Campos (83)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |
| 2 | `Account` | Acct No. | nVarChar | 50 | - |  |  |
| 3 | `Branch` | Branch | nVarChar | 50 | - |  |  |
| 4 | `NextCheck` | Next Check No. | Int | 11 | - |  |  |
| 5 | `GLAccount` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `Free` | Free | VarChar | 1 | - |  |  |
| 7 | `Street` | Street | nVarChar | 100 | - |  |  |
| 8 | `Block` | Block | nVarChar | 100 | - |  |  |
| 9 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 10 | `City` | City | nVarChar | 100 | - |  |  |
| 11 | `County` | County | nVarChar | 100 | - |  |  |
| 12 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 13 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 14 | `BISR` | BISR | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `ControlKey` | Control Key | nVarChar | 2 | - |  |  |
| 16 | `UsrNumber1` | User No. 1 | nVarChar | 25 | - |  |  |
| 17 | `UsrNumber2` | User No. 2 | nVarChar | 25 | - |  |  |
| 18 | `UsrNumber3` | User No. 3 | nVarChar | 25 | - |  |  |
| 19 | `UsrNumber4` | User No. 4 | nVarChar | 25 | - |  |  |
| 20 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 21 | `DscountBOE` | Debt of Discounted BoE | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 22 | `TolrnceDay` | Tolerance Days | Int | 11 | - |  |  |
| 23 | `MinAmntBOE` | Min. Amount of Bill of Exchange | Num | 19.6 | - |  |  |
| 24 | `MaxAmntBOE` | Max. Amount of Bill of Exchange | Num | 19.6 | - |  |  |
| 25 | `DscntLimit` | Discount Limit | Num | 19.6 | - |  |  |
| 26 | `DaysInAdva` | Days in Advance | Int | 11 | - |  |  |
| 27 | `BankCollec` | Bank on Collection | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 28 | `BankDiscou` | Bank on Discounted | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `BranchName` | Branch Name | nVarChar | 50 | - |  |  |
| 30 | `AliasName` | Alias Name | nVarChar | 50 | - |  |  |
| 31 | `CompanyCod` | Company Code | nVarChar | 10 | - |  |  |
| 32 | `AcctType` | Account Type | VarChar | 1 | - |  |  |
| 33 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 34 | `BIK` | BIK | nVarChar | 15 | - |  |  |
| 35 | `AcctName` | Bank Account Name | nVarChar | 250 | - |  |  |
| 36 | `CorresAcct` | Correspondent Account | nVarChar | 30 | - |  |  |
| 37 | `Phone` | Telephone No. | nVarChar | 50 | - |  |  |
| 38 | `Fax` | Fax | nVarChar | 50 | - |  |  |
| 39 | `GLIntriAct` | G/L Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `ChkPaper` | Paper Type | VarChar | 1 | - | D | `B` = Blank Paper<br>`S` = Overflow Prenumbered Check Stock<br>`P` = Overflow Blank Paper<br>`D` = Default |
| 41 | `MaxChkLine` | Maximum Lines | Int | 6 | - |  |  |
| 42 | `TmpltName` | Template Name | nVarChar | 8 | - |  |  |
| 43 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 44 | `BankKey` | Bank Internal ID | Int | 11 | [ODSC](ODSC.md) |  |  |
| 45 | `LockChk` | Lock Checks Printing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `OurNum` | Our Number in Next Boleto | Int | 11 | - |  |  |
| 47 | `AgreeNum` | Agreement Number | nVarChar | 10 | - |  |  |
| 48 | `AccountChk` | Account Check Digit | VarChar | 1 | - |  |  |
| 49 | `ISRType` | ISR Type | Int | 6 | - | 2 | `1` = ISR<br>`2` = BISR<br>`3` = ISR+<br>`4` = BISR+ |
| 50 | `ISRBillerI` | ISR Biller ID | nVarChar | 9 | - |  |  |
| 51 | `CustIdNum` | Customer ID Number | nVarChar | 10 | - | 0 |  |
| 52 | `InSeri` | Incoming Payment Series | Int | 11 | [NNM1](NNM1.md) | -1 |  |
| 53 | `OutSeri` | Outgoing Payment Series | Int | 11 | [NNM1](NNM1.md) | -1 |  |
| 54 | `JDTSeri` | Journal Entry Series | Int | 11 | [NNM1](NNM1.md) | -1 |  |
| 55 | `FilePlug` | Import File Name | nVarChar | 50 | - |  |  |
| 56 | `ImpStmt` | Imported Bank Statement | VarChar | 1 | - | N | `Y` = Create New - From File<br>`N` = Create New - Manually |
| 57 | `PreNumber` | Prenumbered Check | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 58 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 59 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 60 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 61 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 62 | `UsrLogSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 63 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 64 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 65 | `FineAcct` | Fine Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 66 | `IntrstAcct` | Interest Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 67 | `DscntAcct` | Discount Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 68 | `SvcFeeAcct` | Service Fee Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 69 | `BranchChk` | Branch Check Digit | nVarChar | 5 | - |  |  |
| 70 | `RetFile` | Retorno File Format | nVarChar | 50 | - |  |  |
| 71 | `IOFTaxAcct` | IOF Tax Account | nVarChar | 15 | - |  |  |
| 72 | `OthExpAcct` | Other Expenses Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 73 | `OthIncAcct` | Other Incomes Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 74 | `CollCode` | Collection Code | nVarChar | 50 | - |  |  |
| 75 | `FileSeqNNo` | File Sequence Next Number | Int | 11 | - |  |  |
| 76 | `RefCoLevel` | Reference control level | VarChar | 1 | - | H | `S` = Soft Control<br>`H` = Hard Control<br>`V` = Hard Control with variable length<br>`F` = Hard Control with fixed length |
| 77 | `RefFixLen1` | Reference fixed length 1 | Int | 6 | - |  |  |
| 78 | `RefFixLen2` | Reference fixed length 2 | Int | 6 | - |  |  |
| 79 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 80 | `NoValidBal` | No Validation for Starting/Ending Balance | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `ECheck` | E-Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 82 | `EnAccount` | Encryption of Acct No. | Text | 16 | - |  |  |
| 83 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | Country, BankCode, Account |
