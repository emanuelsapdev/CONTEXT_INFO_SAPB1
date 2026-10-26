# PWZ4 - Payment Wizard - Rows 4

- **Tabla:** PWZ4
- **Descripción:** Payment Wizard - Rows 4
- **Cantidad de campos:** 38
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ4.html

## Campos (38)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `PymNum` | Payment Number | Int | 11 | - |  |  |
| 3 | `CardCode` | Vendor's Card code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `CardName` | Vendor's Card Name | nVarChar | 200 | - |  |  |
| 5 | `PymMeth` | Payment Method | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 6 | `GLAccCode` | G/L Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `PymAmount` | Sum of payment amount | Num | 19.6 | - |  |  |
| 8 | `PymAmntFC` | Total Payment Amount (FC) | Num | 19.6 | - |  |  |
| 9 | `ObjType` | Object Type | nVarChar | 20 | - |  | `24` = Incoming Payment<br>`46` = Outgoing Payment |
| 10 | `RctId` | Document ID | Int | 11 | - |  |  |
| 11 | `DocCurr` | Document Currency | nVarChar | 3 | - |  |  |
| 12 | `BankAccou` | Acct No. | nVarChar | 50 | [OACT](OACT.md) |  |  |
| 13 | `BnkDflt` | Default Bank | nVarChar | 30 | - |  |  |
| 14 | `BankCountr` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 15 | `BankActKey` | Bank Account Internal ID | Int | 11 | [DSC1](DSC1.md) |  |  |
| 16 | `LineType` | Line Type | VarChar | 1 | - | G |  |
| 17 | `ManualNum` | Manual Entry No. | Int | 11 | - | 0 |  |
| 18 | `TBankCode` | Target Default Bank | nVarChar | 30 | - | -1 |  |
| 19 | `TDflAccoun` | Target Default Account | nVarChar | 50 | - |  |  |
| 20 | `TBankCount` | Target Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 21 | `TargetBran` | Target Bank Branch | nVarChar | 50 | - |  |  |
| 22 | `BcgPmnt` | Payment Amount (BCG) | Num | 19.6 | - |  |  |
| 23 | `BcgPmntFc` | Payment Amount FC (BCG) | Num | 19.6 | - |  |  |
| 24 | `RecipStatu` | Recipient Status | nVarChar | 2 | - |  |  |
| 25 | `BudgetId` | VAT Budget Classification Code | nVarChar | 100 | - |  |  |
| 26 | `OKATO` | OKATO | nVarChar | 11 | - |  |  |
| 27 | `PymReason` | Payment Reason | nVarChar | 2 | - |  |  |
| 28 | `PostPeriod` | Posting Period Code | nVarChar | 10 | - |  |  |
| 29 | `BaseDocTyp` | Base Document Type | nVarChar | 2 | - |  |  |
| 30 | `BaseDocDat` | Base Docoument Date | Date | 8 | - |  |  |
| 31 | `TaxPymType` | Tax Payment Type | nVarChar | 2 | - |  |  |
| 32 | `OKTMO` | OKTMO | nVarChar | 12 | - |  |  |
| 33 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 34 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 35 | `UIPCode` | UIP Code | nVarChar | 25 | - |  |  |
| 36 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 37 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 38 | `EnBankAcco` | Encryption of Acct No. | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, RctId, ObjType |
