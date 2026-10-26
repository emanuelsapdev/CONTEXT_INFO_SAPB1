# OCHH - Check Register

- **Tabla:** OCHH
- **Descripción:** Check Register
- **Cantidad de campos:** 39
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCHH.html

## Campos (39)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CheckKey` | Check Key | Int | 11 | - |  |  |
| 2 | `CheckNum` | Check Number | Int | 11 | - |  |  |
| 3 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |
| 4 | `Branch` | Branch Number | nVarChar | 50 | - |  |  |
| 5 | `CashCheck` | Check Register Account | nVarChar | 15 | - |  |  |
| 6 | `CheckDate` | Check Date | Date | 8 | - |  |  |
| 7 | `Details` | Details | nVarChar | 20 | - |  |  |
| 8 | `CardCode` | BP/Account Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 9 | `RcptDate` | Receipt Date | Date | 8 | - |  |  |
| 10 | `RcptNum` | Receipt Number | Int | 11 | [ORCT](ORCT.md) |  |  |
| 11 | `CheckSum` | Check Amount | Num | 19.6 | - |  |  |
| 12 | `Trnsfrable` | Negotiable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Deposited` | Deposited | VarChar | 1 | - | N | `C` = As Cash<br>`N` = No<br>`S` = As Postdated |
| 14 | `Converted` | Endorsed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `Vendor` | Endorsed for | nVarChar | 15 | - |  |  |
| 16 | `TransNum` | Payment Transaction | Int | 11 | - |  |  |
| 17 | `DepNum2` | Postdated Deposit Key | Int | 11 | [ODPT](ODPT.md) | 0 |  |
| 18 | `DpstAbs` | Payment Internal ID | Int | 11 | [ODPS](ODPS.md) |  |  |
| 19 | `BankAcct` | Deposit Account | nVarChar | 15 | - |  |  |
| 20 | `AcctNum` | Account Number | nVarChar | 50 | - |  |  |
| 21 | `Currency` | Check Currency | nVarChar | 3 | - |  |  |
| 22 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `RcptLineId` | Row Number in Receipt | Int | 11 | - |  |  |
| 24 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 26 | `UserID` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `BankCountr` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 28 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 29 | `CanceJEAbs` | Cancellation Journal Entry | Int | 11 | [OJDT](OJDT.md) |  |  |
| 30 | `TempJEAbs` | Temp. Journal Entry | Int | 11 | - |  |  |
| 31 | `CardName` | BP/Account Name | nVarChar | 200 | - |  |  |
| 32 | `FiscalID` | Fiscal ID | nVarChar | 100 | - |  |  |
| 33 | `OrigIssdBy` | Orginally Issued By | nVarChar | 254 | - |  |  |
| 34 | `RejeByBank` | Rejected by Bank | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `EnAcctNum` | Encryption of Account Number | Text | 16 | - |  |  |
| 36 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 37 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 38 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 39 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CheckKey |
| RECEIPT | No | RcptNum, RcptLineId |
| DEP_ABS1 | No | DpstAbs |
| CHECK_NUM | No | CheckNum |
| DEP_ABS2 | No | DepNum2 |
