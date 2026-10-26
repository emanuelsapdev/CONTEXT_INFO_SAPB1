# OPWB - PWZ - Bank Account

- **Tabla:** OPWB
- **Descripción:** PWZ - Bank Account
- **Cantidad de campos:** 46
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPWB.html

## Campos (46)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |
| 4 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 5 | `Account` | Account No. | nVarChar | 50 | - |  |  |
| 6 | `Branch` | Branch | nVarChar | 50 | - |  |  |
| 7 | `Street` | Street | nVarChar | 100 | - |  |  |
| 8 | `Block` | Block | nVarChar | 100 | - |  |  |
| 9 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 10 | `City` | City | nVarChar | 100 | - |  |  |
| 11 | `County` | County | nVarChar | 100 | - |  |  |
| 12 | `State` | State | nVarChar | 3 | - |  |  |
| 13 | `ControlKey` | Ctrl Internal ID | nVarChar | 2 | - |  |  |
| 14 | `UsrNumber1` | User No. 1 | nVarChar | 25 | - |  |  |
| 15 | `UsrNumber2` | User No. 2 | nVarChar | 25 | - |  |  |
| 16 | `UsrNumber3` | User No. 3 | nVarChar | 25 | - |  |  |
| 17 | `UsrNumber4` | User No. 4 | nVarChar | 25 | - |  |  |
| 18 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 19 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 20 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 21 | `AliasName` | Alias Name | nVarChar | 50 | - |  |  |
| 22 | `AcctType` | Account Type | VarChar | 1 | - |  |  |
| 23 | `BankKey` | Bank Internal ID | Int | 11 | [ODSC](ODSC.md) |  |  |
| 24 | `BIK` | BIK | nVarChar | 15 | - |  |  |
| 25 | `AcctName` | Bank Account Name | nVarChar | 250 | - |  |  |
| 26 | `CorresAcct` | Correspondent Account | nVarChar | 30 | - |  |  |
| 27 | `Phone` | Phone | nVarChar | 50 | - |  |  |
| 28 | `Fax` | Fax | nVarChar | 50 | - |  |  |
| 29 | `ISRType` | ISR Type | Int | 6 | - | 2 | `1` = ISR<br>`2` = BISR<br>`3` = ISR+<br>`4` = BISR+ |
| 30 | `ISRBillerI` | ISR Biller ID | nVarChar | 9 | - |  |  |
| 31 | `CustIdNum` | Customer ID Number | nVarChar | 6 | - | 0 |  |
| 32 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 33 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 34 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 35 | `ABARoutNum` | ABA Routing Number | nVarChar | 25 | - |  |  |
| 36 | `MandateID` | Mandate ID | nVarChar | 35 | - |  |  |
| 37 | `SignDate` | Date of Signature | Date | 8 | - |  |  |
| 38 | `PWZAbsEntr` | PWZ ABS Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 39 | `BranchChk` | Branch Check Digit | nVarChar | 5 | - |  |  |
| 40 | `MandatDate` | Date Of Mandate Expiration | Date | 8 | - |  |  |
| 41 | `SeqType` | SEPA Seq. Type | nVarChar | 4 | - |  | `OOFF` = OOFF<br>`FRST` = FRST<br>`RCUR` = RCUR<br>`FNAL` = FNAL |
| 42 | `ActType` | Account Type | VarChar | 1 | - |  | `C` = Checking Account<br>`S` = Savings Account |
| 43 | `IsPrenot` | Is Prenotification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `EnAccount` | Encryption of Account | Text | 16 | - |  |  |
| 45 | `EnIBAN` | Encryption of IBAN | Text | 16 | - |  |  |
| 46 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| COUNTRY | Yes | Country, BankCode, Account, PWZAbsEntr |
