# ODPS - Deposit

- **Tabla:** ODPS
- **Descripción:** Deposit
- **Cantidad de campos:** 76
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODPS.html

## Campos (76)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DeposId` | Payment Internal ID | Int | 11 | - | 0 |  |
| 2 | `DeposType` | Payment Type | VarChar | 1 | - | K | `K` = Check Deposit<br>`C` = Cash Payment<br>`V` = Credit Deposit<br>`B` = Bill of Exchange |
| 3 | `DeposNum` | Payment No. | Int | 11 | - |  |  |
| 4 | `DeposDate` | Payment Date | Date | 8 | - |  |  |
| 5 | `DeposCurr` | Currency for Payments | nVarChar | 3 | - |  |  |
| 6 | `BanckAcct` | Deposit Account | nVarChar | 15 | - |  |  |
| 7 | `DeposAcct` | Bank Account Number | nVarChar | 50 | - |  |  |
| 8 | `DeposBrnch` | Branch for Payments | nVarChar | 50 | - |  |  |
| 9 | `Memo` | Details | nVarChar | 254 | - |  |  |
| 10 | `LocTotal` | Total (LC) | Num | 19.6 | - |  |  |
| 11 | `FcTotal` | Total (FC) | Num | 19.6 | - |  |  |
| 12 | `SysTotal` | Total (SC) | Num | 19.6 | - |  |  |
| 13 | `TransAbs` | Journal Entry Key | Int | 11 | [OJDT](OJDT.md) |  |  |
| 14 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 15 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 16 | `DocTime` | Pay-In Time | Int | 6 | - |  |  |
| 17 | `AllocAcct` | Cash | nVarChar | 15 | - |  |  |
| 18 | `ChkType` | Check Deposit Type | VarChar | 1 | - | C | `C` = Cash Checks<br>`S` = Postdated Checks |
| 19 | `DpsBank` | Bank Name for Payments | nVarChar | 30 | - |  |  |
| 20 | `DpostorNam` | Name of Depositor | nVarChar | 30 | - |  |  |
| 21 | `Printed` | Original/Copy | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `DocRate` | Payment Rate | Num | 19.6 | - |  |  |
| 23 | `CrdBankAct` | Voucher Account | nVarChar | 15 | - |  |  |
| 24 | `IsCard` | Business Partner or Account | VarChar | 1 | - | A | `A` = G/L Account<br>`C` = BP |
| 25 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 27 | `Splited` | Split | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 29 | `VatAct` | Tax Account | nVarChar | 15 | - |  |  |
| 30 | `ComissAct` | Commissions Account | nVarChar | 15 | - |  |  |
| 31 | `VatTotal` | Total Tax | Num | 19.6 | - |  |  |
| 32 | `Comission` | Commission | Num | 19.6 | - |  |  |
| 33 | `ComissDate` | Commission Date | Date | 8 | - |  |  |
| 34 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 35 | `Series` | Series | Int | 11 | - |  |  |
| 36 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 37 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 38 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 39 | `VatTotlSys` | Total Tax on Input (SC) | Num | 19.6 | - |  |  |
| 40 | `ComissnSys` | Total Commission (SC) | Num | 19.6 | - |  |  |
| 41 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 42 | `DepostNorm` | Deposit Norm | nVarChar | 8 | - |  |  |
| 43 | `PostType` | Transaction Type | VarChar | 1 | - | C | `C` = Collection<br>`D` = Discounted |
| 44 | `BankCountr` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 45 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `CnclDps` | Cancel Deposit | Int | 11 | - | -1 |  |
| 47 | `CommisVat` | Commission VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 48 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 49 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 50 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 51 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 52 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 53 | `ReconAfter` | Reconcile Amounts After Dpst | VarChar | 1 | - | Y |  |
| 54 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 55 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 56 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 57 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 58 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 59 | `ComisFC` | Total Commission (FC) | Num | 19.6 | - |  |  |
| 60 | `VatTotlFC` | Total Tax on Input (FC) | Num | 19.6 | - |  |  |
| 61 | `ComisCurr` | Commission Currency | nVarChar | 3 | - |  |  |
| 62 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 63 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 64 | `SysRate` | System Currency Rate | Num | 19.6 | - |  |  |
| 65 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 66 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 67 | `IncomeAct` | Withholding Income Tax Account | nVarChar | 15 | - |  |  |
| 68 | `IncomeLC` | Withholding Income Tax LC | Num | 19.6 | - |  |  |
| 69 | `IncomeFC` | Withholding Income Tax FC | Num | 19.6 | - |  |  |
| 70 | `IncomeSC` | Withholding Income Tax SC | Num | 19.6 | - |  |  |
| 71 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 72 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 73 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 74 | `EnDeposAcc` | Encryption of Bank Account No. | Text | 16 | - |  |  |
| 75 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 76 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DeposId |
| VIS_NUM | Yes | DeposNum, Series |
| SERIES | No | Series |
