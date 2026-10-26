# OCRV - Credit Payments

- **Tabla:** OCRV
- **Descripción:** Credit Payments
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRV.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Seq. No. in Amount | Int | 11 | [OCRH](OCRH.md) |  |  |
| 2 | `PayId` | Payment No. | Int | 11 | - | 0 |  |
| 3 | `CreditCard` | Credit Card | Int | 6 | [OCRC](OCRC.md) | 0 |  |
| 4 | `CrdCardNum` | Credit Card No. | nVarChar | 254 | - |  |  |
| 5 | `CardValid` | Credit Card Validity | Date | 8 | - |  |  |
| 6 | `VoucherNum` | Voucher Number | nVarChar | 27 | - |  |  |
| 7 | `OwnerIdNum` | ID Number | nVarChar | 15 | - |  |  |
| 8 | `OwnerPhone` | Telephone | nVarChar | 50 | - |  |  |
| 9 | `PayDate` | Payment Date | Date | 8 | - |  |  |
| 10 | `PayAmount` | Payment Amount | Num | 19.6 | - |  |  |
| 11 | `CreditCurr` | Credit Currency | nVarChar | 3 | - |  |  |
| 12 | `CreditRate` | Credit Rate | Num | 19.6 | - |  |  |
| 13 | `Deposited` | Paid | VarChar | 1 | - | O | `C` = Closed<br>`O` = Open<br>`S` = Postdated |
| 14 | `DepNum2` | Postdated Deposit Key | Int | 11 | [ODPT](ODPT.md) | 0 |  |
| 15 | `DepNum` | Payment Internal ID | Int | 11 | [ODPS](ODPS.md) |  |  |
| 16 | `AcctCode` | Account for Payments | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `VouchAcct` | Voucher Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `CreditAcct` | Credit Account | nVarChar | 15 | - |  |  |
| 19 | `CardCode` | BP/Account Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 20 | `CrTypeCode` | Payment Method Code | Int | 6 | [OCRP](OCRP.md) |  |  |
| 21 | `NumOfPmnts` | Number of Payments | Int | 6 | - | 1 |  |
| 22 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `Storno` | Cancel Transaction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `Instance` | Instance | Int | 6 | [OCRH](OCRH.md) | 0 |  |
| 26 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 27 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 28 | `TransRef` | Trans. Reference | nVarChar | 20 | - |  |  |
| 29 | `CardName` | BP/Account Name | nVarChar | 200 | - |  |  |
| 30 | `EnOwnerId` | Encryption of ID Number | Text | 16 | - |  |  |
| 31 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (9)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, PayId, Instance |
| CRED_CARD | No | CreditCard |
| CUST_CODE | No | CardCode |
| DEP_ABS1 | No | DepNum |
| IS_VALID | No | VoucherNum, PayId, CreditCard, Storno |
| CRED_ACCT | No | CreditAcct |
| DEP_ABS2 | No | DepNum2 |
| DEPOSITED | No | Deposited |
| VOUCHER_ID | No | AbsId |
