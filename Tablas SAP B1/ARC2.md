# ARC2 - Incoming Payment - Invoices - History

- **Tabla:** ARC2
- **Descripción:** Incoming Payment - Invoices - History
- **Cantidad de campos:** 68
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARC2.html

## Campos (68)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [OVPM](OVPM.md) |  |  |
| 2 | `InvoiceId` | Sequence No. | Int | 11 | - |  |  |
| 3 | `DocEntry` | Invoice Key | Int | 11 | - |  |  |
| 4 | `SumApplied` | Paid (LC) | Num | 19.6 | - |  |  |
| 5 | `AppliedFC` | Paid (FC) | Num | 19.6 | - |  |  |
| 6 | `AppliedSys` | Paid (SC) | Num | 19.6 | - |  |  |
| 7 | `InvType` | Document Type | nVarChar | 20 | - | 13 | `203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Payment Advice<br>`57` = Checks for Payment<br>`76` = Postdated Deposit<br>`-2` = Opening Balance<br>`-3` = Closing Balance<br>`30` = Journal Entry<br>`-1` = All Transactions<br>`163` = A/P Correction Invoice<br>`165` = A/R Correction Invoice<br>`0` |
| 8 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 9 | `Flags` | Flags | Int | 11 | - | 0 |  |
| 10 | `IntrsStat` | Interest Letter Status | VarChar | 1 | - | U | `U` = Not Sent<br>`S` = Sent<br>`C` = Closed |
| 11 | `DocLine` | Row Key | Int | 11 | - | 0 |  |
| 12 | `vatApplied` | Tax Definition | Num | 19.6 | - |  |  |
| 13 | `vatAppldFC` | Tax Paid (FC) | Num | 19.6 | - |  |  |
| 14 | `vatAppldSy` | Tax Paid (SC) | Num | 19.6 | - |  |  |
| 15 | `selfInv` | Auto. Invoice | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 16 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 17 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 18 | `Dcount` | Discount | Num | 19.6 | - |  |  |
| 19 | `DcntSum` | Discount Amount | Num | 19.6 | - |  |  |
| 20 | `DcntSumFC` | Discount Amount (FC) | Num | 19.6 | - |  |  |
| 21 | `DcntSumSy` | Discount Amount (SC) | Num | 19.6 | - |  |  |
| 22 | `BfDcntSum` | Amount Bef. Discount | Num | 19.6 | - |  |  |
| 23 | `BfDcntSumF` | Amount Bef. Discount (FC) | Num | 19.6 | - |  |  |
| 24 | `BfDcntSumS` | Amount Bef. Discount (SC) | Num | 19.6 | - |  |  |
| 25 | `BfNetDcnt` | Net Amount Bef. Discount | Num | 19.6 | - |  |  |
| 26 | `BfNetDcntF` | Net Amount Bef. Discount (FC) | Num | 19.6 | - |  |  |
| 27 | `BfNetDcntS` | Net Amount Bef. Discount (SC) | Num | 19.6 | - |  |  |
| 28 | `PaidSum` | Amount Paid (LC) | Num | 19.6 | - |  |  |
| 29 | `ExpAppld` | Freight applied | Num | 19.6 | - |  |  |
| 30 | `ExpAppldFC` | Freight applied FC | Num | 19.6 | - |  |  |
| 31 | `ExpAppldSC` | Freight applied SC | Num | 19.6 | - |  |  |
| 32 | `Rounddiff` | Rounding Diff. | Num | 19.6 | - |  |  |
| 33 | `RounddifFc` | Rounding Diff. (FC) | Num | 19.6 | - |  |  |
| 34 | `RounddifSc` | Rounding Diff. (SC) | Num | 19.6 | - |  |  |
| 35 | `InstId` | Installment ID | Int | 6 | - | 1 |  |
| 36 | `WtAppld` | Applied WTax | Num | 19.6 | - |  |  |
| 37 | `WtAppldFC` | Applied WT (FC) | Num | 19.6 | - |  |  |
| 38 | `WtAppldSC` | Applied WTax (SC) | Num | 19.6 | - |  |  |
| 39 | `LinkDate` | Link Date | Date | 8 | - |  |  |
| 40 | `AmtDifPst` | Amount Diffs. Posting Date | Date | 8 | - |  |  |
| 41 | `PaidDpm` | Paid Down Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 42 | `DpmPosted` | Link Date | VarChar | 1 | - |  |  |
| 43 | `ExpVatSum` | VAT on Expenses Sum | Num | 19.6 | - |  |  |
| 44 | `ExpVatSumF` | VAT on Expenses Sum (FC) | Num | 19.6 | - |  |  |
| 45 | `ExpVatSumS` | VAT on Expenses Sum (SC) | Num | 19.6 | - |  |  |
| 46 | `IsRateDiff` | Is Exchange Rate | VarChar | 1 | - | N |  |
| 47 | `WtInvCatS` | Withholding Tax Invoice Categ. | Num | 19.6 | - |  |  |
| 48 | `WtInvCatSF` | Withholding Tax Invoice Categ. | Num | 19.6 | - |  |  |
| 49 | `WtInvCatSS` | Withholding Tax Invoice Categ. | Num | 19.6 | - |  |  |
| 50 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 51 | `DocTransId` | Trans. ID of Paid Document | Int | 11 | [OJDT](OJDT.md) |  |  |
| 52 | `MIEntry` | MI Entry Include this Payment | Int | 11 | - | 0 |  |
| 53 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 54 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 55 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 56 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 57 | `IsSelected` | Is Record Selected | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `WTOnHold` | Withholding Tax On Hold | Num | 19.6 | - |  |  |
| 59 | `WTOnhldPst` | Withholding Tax Posted | Num | 19.6 | - |  |  |
| 60 | `baseAbs` | Base Document Number | Int | 11 | - |  |  |
| 61 | `MIType` | MI Type Include this Payment | nVarChar | 20 | - |  | `270` = A/R Monthly Invoice<br>`140000014` = A/P Monthly Invoice |
| 62 | `DocSubType` | Document Subtype | nVarChar | 2 | - | -- |  |
| 63 | `SpltPmtVAT` | Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 65 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 66 | `WTSumFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 67 | `WTSumSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 68 | `SelOrder` | Select Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, InvoiceId, ObjType, LogInstanc |
