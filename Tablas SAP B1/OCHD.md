# OCHD - Checks for Payment Drafts

- **Tabla:** OCHD
- **Descripción:** Checks for Payment Drafts
- **Cantidad de campos:** 62
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCHD.html

## Campos (62)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CheckKey` | Check Key | Int | 11 | - |  |  |
| 2 | `CheckNum` | Check Number | Int | 11 | - |  |  |
| 3 | `BankNum` | Bank No. | nVarChar | 30 | - |  |  |
| 4 | `Branch` | Branch | nVarChar | 50 | - |  |  |
| 5 | `BankName` | Bank Name | nVarChar | 250 | - |  |  |
| 6 | `CheckDate` | Cashing Date | Date | 8 | - |  |  |
| 7 | `DpstAcct` | Bank Account Number | nVarChar | 50 | - |  |  |
| 8 | `DpstBranch` | Branch for Payments | Int | 6 | - |  |  |
| 9 | `AcctNum` | Account No. | nVarChar | 50 | - |  |  |
| 10 | `Details` | Details | nVarChar | 254 | - |  |  |
| 11 | `TransRef` | Transaction Reference | nVarChar | 11 | - |  |  |
| 12 | `PmntDate` | Payment Date | Date | 8 | - |  |  |
| 13 | `PmntNum` | Payment No. | Int | 11 | [OVPM](OVPM.md) |  |  |
| 14 | `CheckSum` | Check Amount | Num | 19.6 | - |  |  |
| 15 | `Trnsfrable` | Freely Negotiable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `VendorCode` | Vendor Code | nVarChar | 15 | - |  |  |
| 17 | `Currency` | Check Currency | nVarChar | 3 | - |  |  |
| 18 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `CardOrAcct` | Business Partner or Account | VarChar | 1 | - | C | `C` = Card<br>`A` = Account |
| 20 | `Printed` | Printed | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 21 | `VendorName` | Vendor Name | nVarChar | 200 | - |  |  |
| 22 | `TotalWords` | Total in Words | nVarChar | 254 | - |  |  |
| 23 | `Signature` | Signature | nVarChar | 30 | - |  |  |
| 24 | `CheckAcct` | Credited Account Code | nVarChar | 15 | - |  |  |
| 25 | `TransNum` | Transaction Number | Int | 11 | [OJDT](OJDT.md) | 0 |  |
| 26 | `LinesSum` | Row Totals | Num | 19.6 | - |  |  |
| 27 | `Deduction` | WTax Deduction - Amt | Num | 19.6 | - |  |  |
| 28 | `DdctPrcnt` | Withholding Tax Deduction % | Num | 19.6 | - |  |  |
| 29 | `Address` | Address | nVarChar | 254 | - |  |  |
| 30 | `CreateJdt` | Create Journal Entry | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 31 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 32 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 33 | `VatTotal` | Total Tax | Num | 19.6 | - |  |  |
| 34 | `VatCalcult` | Calculate Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 36 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 37 | `SumRfndCln` | Deduction Refund Amount | Num | 19.6 | - |  |  |
| 38 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 39 | `PrintedBy` | Printed By | Int | 6 | - |  |  |
| 40 | `Transfered` | Transferred to next year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 42 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 43 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 123 |  |
| 44 | `CountryCod` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 45 | `AddrName` | Address Name | nVarChar | 50 | - |  |  |
| 46 | `PrnConfrm` | Confirm Printing | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 47 | `BnkActKey` | Bank Account Internal ID | Int | 11 | [DSC1](DSC1.md) |  |  |
| 48 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 49 | `ManualChk` | Manual Check | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 50 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 51 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 52 | `VATRegNum` | Branch Reg. No. | nVarChar | 32 | - |  |  |
| 53 | `Endorse` | Endorse | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 54 | `EndorsChNo` | Endorsable Check No. | Int | 11 | [OCHH](OCHH.md) |  |  |
| 55 | `UserSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 56 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 57 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 58 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 59 | `ECheck` | E-Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 60 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 61 | `EnAcctNum` | Encryption of Account Number | Text | 16 | - |  |  |
| 62 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CheckKey |
| VPM_NUM | No | PmntNum |
| TRANS_NUM | No | TransNum |
