# OCRH - Credit Card Management

- **Tabla:** OCRH
- **Descripción:** Credit Card Management
- **Cantidad de campos:** 42
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRH.html

## Campos (42)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Seq. No. in Amount | Int | 11 | - |  |  |
| 2 | `CreditCard` | Credit Card | Int | 6 | [OCRC](OCRC.md) | 0 |  |
| 3 | `CrdCardNum` | Credit Card No. | nVarChar | 254 | - |  |  |
| 4 | `CardValid` | Credit Card Validity | Date | 8 | - |  |  |
| 5 | `VoucherNum` | Voucher Number | nVarChar | 27 | - |  |  |
| 6 | `OwnerIdNum` | ID Number | nVarChar | 15 | - |  |  |
| 7 | `OwnerPhone` | Telephone | nVarChar | 50 | - |  |  |
| 8 | `CrTypeCode` | Payment Method Code | Int | 6 | [OCRP](OCRP.md) |  |  |
| 9 | `NumOfPmnts` | Number of Payments | Int | 6 | - | 1 |  |
| 10 | `PayDate` | Payment Date | Date | 8 | - |  |  |
| 11 | `FirstSum` | First Partial Payment | Num | 19.6 | - |  |  |
| 12 | `AddPmntSum` | Each Additional Payment | Num | 19.6 | - |  |  |
| 13 | `CreditSum` | Credit Amount | Num | 19.6 | - |  |  |
| 14 | `CreditCurr` | Credit Currency | nVarChar | 3 | - |  |  |
| 15 | `CreditRate` | Credit Rate | Num | 19.6 | - |  |  |
| 16 | `ConfNum` | Confirmation Number | nVarChar | 20 | - |  |  |
| 17 | `CreditType` | Credit Transaction Type | VarChar | 1 | - | S | `U` = Telephone Transaction<br>`S` = Regular<br>`I` = Internet Transaction |
| 18 | `CreditDps` | Credit Deposit Type | VarChar | 1 | - | Y | `Y` = Manual<br>`N` = Automatic |
| 19 | `Deposited` | Paid | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `DeposDate` | Payment Date | Date | 8 | - |  |  |
| 21 | `RctAbs` | Receipt No. | Int | 11 | [ORCT](ORCT.md) |  |  |
| 22 | `DepNum` | Payment Internal ID | Int | 11 | [ODPS](ODPS.md) |  |  |
| 23 | `AcctCode` | Account for Payments | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `CreditAcct` | Credit Account | nVarChar | 15 | - |  |  |
| 25 | `CardCode` | BP/Account Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 26 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `Storno` | Cancel Transaction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `RcptLineId` | Row Number in Receipt | Int | 11 | - |  |  |
| 29 | `Recived` | Received | Num | 19.6 | - |  |  |
| 30 | `Converted` | Endorsed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `ConvertTo` | Endorsed for | nVarChar | 15 | - |  |  |
| 32 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 33 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 34 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `TransRef` | Trans. Reference | nVarChar | 20 | - |  |  |
| 36 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 37 | `ConsolNum` | Vendor Credit Code | Int | 11 | - | -1 |  |
| 38 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 39 | `CardName` | BP/Account Name | nVarChar | 200 | - |  |  |
| 40 | `EnOwnerId` | Encryption of ID Number | Text | 16 | - |  |  |
| 41 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 42 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (8)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, Instance |
| CRED_CARD | No | CreditCard |
| CRED_TYPE | No | CreditType |
| RECEIPT | No | RctAbs, RcptLineId, Storno |
| CUST_CODE | No | CardCode |
| DEP_ABS | No | DepNum |
| IS_VALID | No | VoucherNum, CreditCard, Storno |
| CRED_ACCT | No | CreditAcct |
