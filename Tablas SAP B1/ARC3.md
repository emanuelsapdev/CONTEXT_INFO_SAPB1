# ARC3 - Credit Vouchers History

- **Tabla:** ARC3
- **Descripción:** Credit Vouchers History
- **Cantidad de campos:** 28
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARC3.html

## Campos (28)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document No. | Int | 11 | [OVPM](OVPM.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `CreditCard` | Credit Card | Int | 6 | [OCRC](OCRC.md) | -1 |  |
| 4 | `CreditAcct` | Credit Amount | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `CrCardNum` | Credit Card No. | nVarChar | 254 | - |  |  |
| 6 | `CardValid` | Credit Card Valid Until | Date | 8 | - |  |  |
| 7 | `VoucherNum` | Credit Voucher No. | nVarChar | 20 | - |  |  |
| 8 | `OwnerIdNum` | ID Number | nVarChar | 15 | - |  |  |
| 9 | `OwnerPhone` | Telephone | nVarChar | 50 | - |  |  |
| 10 | `CrTypeCode` | Payment Method Code | Int | 6 | [OCRP](OCRP.md) | -1 |  |
| 11 | `NumOfPmnts` | No. of Payments | Int | 6 | - | 1 |  |
| 12 | `FirstDue` | 1st Payment Date | Date | 8 | - |  |  |
| 13 | `FirstSum` | First Partial Payment | Num | 19.6 | - |  |  |
| 14 | `AddPmntSum` | Each Additional Payment | Num | 19.6 | - |  |  |
| 15 | `CreditSum` | Credit Amount | Num | 19.6 | - |  |  |
| 16 | `CreditCur` | Credit Voucher Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 17 | `CreditRate` | Credit Voucher Rate | Num | 19.6 | - |  |  |
| 18 | `ConfNum` | Confirmation No. | nVarChar | 20 | - |  |  |
| 19 | `CreditType` | Credit Transaction Type | VarChar | 1 | - | S | `U` = Telephone Transaction<br>`S` = Regular<br>`I` = Internet Transaction |
| 20 | `CredPmnts` | No. of Credit Payments | Int | 6 | - | 1 |  |
| 21 | `PlCrdStat` | Pelecard Debit Status | nVarChar | 4 | - | -1 |  |
| 22 | `MagnetStr` | Magnetic Stripe Content | nVarChar | 40 | - |  |  |
| 23 | `SpiltCred` | Split Credit Voucher Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `ConsolNum` | Vendor Credit Code | Int | 11 | [OPVL](OPVL.md) | -1 |  |
| 25 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 26 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 27 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 28 | `EnOwnerId` | Encryption of ID Number | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineID, ObjType, LogInstanc |
