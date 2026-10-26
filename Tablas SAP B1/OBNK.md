# OBNK - External Bank Statement Received

- **Tabla:** OBNK
- **Descripción:** External Bank Statement Received
- **Cantidad de campos:** 75
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBNK.html

## Campos (75)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | External Bank Statement No. | Int | 11 | [OBNH](OBNH.md) |  |  |
| 2 | `AcctCode` | Account Number | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 3 | `Sequence` | Sequence No. | Int | 11 | - | 0 |  |
| 4 | `AcctName` | Account Name | nVarChar | 200 | - |  |  |
| 5 | `Ref` | Reference | nVarChar | 35 | - |  |  |
| 6 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 7 | `Memo` | Details | nVarChar | 254 | - |  |  |
| 8 | `DebAmount` | Debit Amount (FC) | Num | 19.6 | - |  |  |
| 9 | `DebAmntCur` | Currency for Accounts Payable | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 10 | `CredAmnt` | Credit Amount (FC) | Num | 19.6 | - |  |  |
| 11 | `CredAmntCu` | Credit Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 12 | `balance` | Balance | Num | 19.6 | - |  |  |
| 13 | `BankMatch` | Reconciliation No. | Int | 11 | - |  |  |
| 14 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `ExternCode` | External Code | nVarChar | 30 | - |  |  |
| 17 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 18 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 19 | `StatemNo` | Statement Number | Int | 11 | - |  |  |
| 20 | `DocNum` | Invoice Document | nVarChar | 27 | - |  |  |
| 21 | `PaymCreat` | Payment Created | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `LineStatus` | Row Status | VarChar | 1 | - |  |  |
| 23 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 24 | `DocNumType` | Doc. No. Source | VarChar | 1 | - | D | `P` = Payment Reference No.<br>`I` = ISR<br>`D` = Doc Num |
| 25 | `Memo2` | Details 2 | nVarChar | 254 | - |  |  |
| 26 | `PaymentRef` | Payment Reference No. | nVarChar | 35 | - |  |  |
| 27 | `autoCreate` | Manually/Automatically Create | VarChar | 1 | - | M | `M` = Manual<br>`A` = Automatic |
| 28 | `BSLineDate` | Bank Statement Entry Date | Date | 8 | - |  |  |
| 29 | `BSValuDate` | Bank Statement Due Date | Date | 8 | - |  |  |
| 30 | `InOpCode` | Internal Bank Operation Code | Int | 11 | [OBTC](OBTC.md) |  |  |
| 31 | `Cleared` | Cleared | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `OposAct` | BP Bank Account | nVarChar | 50 | - |  |  |
| 33 | `DebAmntLC` | Debit Amount (LC) | Num | 19.6 | - |  |  |
| 34 | `CredAmntLC` | Credit Amount (LC) | Num | 19.6 | - |  |  |
| 35 | `ExchngRate` | Exchange Rate | Num | 19.6 | - |  |  |
| 36 | `BPIBAN` | IBAN of the BP Bank Account | nVarChar | 50 | - |  |  |
| 37 | `Fee` | Fee on the Line | Num | 19.6 | - |  |  |
| 38 | `PmnPstDate` | Payment Posting Date | Date | 8 | - |  |  |
| 39 | `PmnValDate` | Payment Due Date | Date | 8 | - |  |  |
| 40 | `LnDocDate` | Line Document Date | Date | 8 | - |  |  |
| 41 | `VatAmntLC` | VAT Amount (LC) | Num | 19.6 | - |  |  |
| 42 | `VatAmntFC` | VAT Amount (FC) | Num | 19.6 | - |  |  |
| 43 | `JDTID` | Journal Entry ID | Int | 11 | [OJDT](OJDT.md) |  |  |
| 44 | `PmntID` | Payment ID | Int | 11 | - |  |  |
| 45 | `ObjCrtType` | Document Type | Int | 6 | - | 24 |  |
| 46 | `PstMethod` | Posting Method | VarChar | 1 | - | C | `A` = G/L Account from/to Bank Account<br>`C` = BP from/to Bank Account<br>`J` = Interim Account from/to Bank Account<br>`E` = External Reconciliation<br>`I` = Ignore |
| 47 | `FeeAct` | G/L Account for Fee | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `FeeProfitC` | Fee Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 49 | `FeeProj` | Project Fee | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 50 | `BpBankCode` | BP Bank Code | nVarChar | 30 | - |  |  |
| 51 | `FeeProfit2` | Fee Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 52 | `FeeProfit3` | Fee Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 53 | `FeeProfit4` | Fee Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 54 | `FeeProfit5` | Fee Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 55 | `ApplWTSum` | Applied WTax Sum | Num | 19.6 | - |  |  |
| 56 | `InfoLog` | Information Log | nVarChar | 254 | - |  |  |
| 57 | `LineOrigin` | Row Origin | VarChar | 1 | - | R | `R` = Regular<br>`A` = Archive |
| 58 | `BPSwift` | BP BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 59 | `Source` | Source | VarChar | 1 | - | I | `I` = Imported<br>`A` = Imported and Amended<br>`M` = Manually Entered |
| 60 | `PayOrderNo` | Payment Order Number | Int | 11 | - |  |  |
| 61 | `TaxIDNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 62 | `PONumber` | External Payment Order Number | Int | 11 | - |  |  |
| 63 | `FormatName` | Format Name for Bank Statement | nVarChar | 254 | - |  |  |
| 64 | `FileCRC` | Bank Statement File Hash Code | nVarChar | 32 | - |  |  |
| 65 | `FolioPref` | Folio Prefix String | nVarChar | 4 | - |  |  |
| 66 | `FolioNum` | Folio Number | Int | 11 | - |  |  |
| 67 | `BPLIdPmn` | Branch for Payment ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 68 | `BPAcctName` | BP Bank Account Name | nVarChar | 250 | - |  |  |
| 69 | `EnOposAct` | Encryption of BP Bank Account | Text | 16 | - |  |  |
| 70 | `EnBPIBAN` | Encryption of BP Bank IBAN | Text | 16 | - |  |  |
| 71 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 72 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 73 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 74 | `CtrlAcct` | Control Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 75 | `eDocConfCd` | eDoc Confirmation Code | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AcctCode, Sequence |
| MATCH_ID | No | BankMatch |
