# JDT1 - Journal Entry - Rows

- **Tabla:** JDT1
- **Descripción:** Journal Entry - Rows
- **Cantidad de campos:** 150
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/JDT1.html

## Campos (150)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransId` | Transaction Key | Int | 11 | [OJDT](OJDT.md) |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `Account` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `Debit` | Debit Amount | Num | 19.6 | - |  |  |
| 5 | `Credit` | Credit Amount | Num | 19.6 | - |  |  |
| 6 | `SYSCred` | System Credit Amount | Num | 19.6 | - |  |  |
| 7 | `SYSDeb` | System Debit Amount | Num | 19.6 | - |  |  |
| 8 | `FCDebit` | Debit Amount (FC) | Num | 19.6 | - |  |  |
| 9 | `FCCredit` | Credit Amount (FC) | Num | 19.6 | - |  |  |
| 10 | `FCCurrency` | Foreign Currency | nVarChar | 3 | - |  |  |
| 11 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 12 | `SourceID` | Source Key | Int | 11 | - |  |  |
| 13 | `SourceLine` | Source Row Number | Int | 6 | - |  |  |
| 14 | `ShortName` | BP/Account Code | nVarChar | 15 | - |  |  |
| 15 | `IntrnMatch` | Internal Reconciliation No. | Int | 11 | - | 0 |  |
| 16 | `ExtrMatch` | External Reconciliation No. | Int | 11 | - | 0 |  |
| 17 | `ContraAct` | Offset Account | nVarChar | 15 | - |  |  |
| 18 | `LineMemo` | Row Details | nVarChar | 254 | - |  |  |
| 19 | `Ref3Line` | Reference 3 | nVarChar | 200 | - |  |  |
| 20 | `TransType` | Original Journal | nVarChar | 20 | - | -1 | `15` = Delivery<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Vendor Payment<br>`57` = Checks for Payment<br>`76` = Postdated Deposit<br>`182` = BoE Transaction<br>`-2` = Opening Balance<br>`-3` = Closing Balance<br>`30` = Journal Entry<br>`58` = Stock Update<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfers<br>`68` = Work Instructions<br>`162` = Inventory Valuation<br>`-1` = All Transactions<br>`321` = Internal Reconciliation<br>`140000009` = Outgoing Excise Invoice<br>`10000079` = TDS Adjustment<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`140000010` = Incoming Excise Invoice<br>`202` = Production Order |
| 21 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 22 | `Ref2Date` | Posting Date 3 | Date | 8 | - |  |  |
| 23 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 24 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 25 | `CreatedBy` | Origin | Int | 11 | - |  |  |
| 26 | `BaseRef` | Base Reference | nVarChar | 11 | - |  |  |
| 27 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 28 | `TransCode` | Transaction Code | nVarChar | 4 | [OTRC](OTRC.md) |  |  |
| 29 | `ProfitCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 31 | `SystemRate` | System Price | Num | 19.6 | - |  |  |
| 32 | `MthDate` | Reconciliation Date | Date | 8 | - |  |  |
| 33 | `ToMthSum` | Reconciliation Total | Num | 19.6 | - |  |  |
| 34 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `BatchNum` | Journal Voucher No. | Int | 11 | [OBTD](OBTD.md) |  |  |
| 36 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 37 | `RelTransId` | Linked Transaction Key | Int | 11 | - | -1 |  |
| 38 | `RelLineID` | Linked Row No. | Int | 11 | - | -1 |  |
| 39 | `RelType` | Link Type | VarChar | 1 | - | N | `N` = Without Link<br>`D` = WTax Deduction - Correction |
| 40 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 41 | `VatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 42 | `BaseSum` | Base Amount | Num | 19.6 | - |  |  |
| 43 | `VatRate` | Tax % | Num | 19.6 | - |  |  |
| 44 | `Indicator` | Indicator Code | nVarChar | 2 | [OIDC](OIDC.md) |  |  |
| 45 | `AdjTran` | Adjusting Trans. (Period 13) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `RevSource` | Revaluation Source | VarChar | 1 | - | N | `F` = Foreign Currency<br>`S` = System<br>`N` = No |
| 47 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 30 |  |
| 48 | `VatDate` | Document Date | Date | 8 | - |  |  |
| 49 | `PaymentRef` | Payment Reference No. | nVarChar | 27 | - |  |  |
| 50 | `SYSBaseSum` | System Base Amount | Num | 19.6 | - |  |  |
| 51 | `MultMatch` | Multiple BP Reconciliation No. | Int | 11 | - | 0 |  |
| 52 | `VatLine` | VAT Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 53 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 54 | `SYSVatSum` | System VAT Amount | Num | 19.6 | - |  |  |
| 55 | `Closed` | Closed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `GrossValue` | Gross Value | Num | 19.6 | - |  |  |
| 57 | `CheckAbs` | Internal Check Number | Int | 11 | - |  |  |
| 58 | `LineType` | Line Type | Int | 11 | - | 0 |  |
| 59 | `DebCred` | Debit Credit Line Indicator | VarChar | 1 | - |  | `D` = Debit<br>`C` = Credit |
| 60 | `SequenceNr` | Assigned Sequence No. | Int | 11 | - | 0 |  |
| 61 | `StornoAcc` | Storno Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `BalDueDeb` | Balance Due - Debit | Num | 19.6 | - |  |  |
| 63 | `BalDueCred` | Balance Due - Credit | Num | 19.6 | - |  |  |
| 64 | `BalFcDeb` | Balance Due (FC) - Debit | Num | 19.6 | - |  |  |
| 65 | `BalFcCred` | Balance Due (FC) - Credit | Num | 19.6 | - |  |  |
| 66 | `BalScDeb` | Balance Due (SC) - Debit | Num | 19.6 | - |  |  |
| 67 | `BalScCred` | Balance Due (SC) - Credit | Num | 19.6 | - |  |  |
| 68 | `IsNet` | Use Net Amount | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 69 | `DunWizBlck` | Wizard Dunning Block | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 70 | `DunnLevel` | Dunning Level | Int | 11 | [ODUN](ODUN.md) | 0 |  |
| 71 | `DunDate` | Last Dunning Date | Date | 8 | - |  |  |
| 72 | `TaxType` | Tax Type | Int | 6 | - | 0 |  |
| 73 | `TaxPostAcc` | Tax Posting Account | VarChar | 1 | - | N | `N`<br>`R` = Sales Tax Account<br>`P` = Purchasing Tax Account |
| 74 | `StaCode` | Authority Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 75 | `StaType` | Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 76 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 77 | `ValidFrom` | Valid From | Date | 8 | - | 19000101 |  |
| 78 | `GrossValFc` | Gross Value (FC) | Num | 19.6 | - |  |  |
| 79 | `LvlUpdDate` | Dunning Level Update Date | Date | 8 | - |  |  |
| 80 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 81 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 82 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 83 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 84 | `MIEntry` | MI Entry when include this OB | Int | 11 | [OMIN](OMIN.md) | 0 |  |
| 85 | `MIVEntry` | A/P Monthly Invoice | Int | 11 | [OMIV](OMIV.md) | 0 |  |
| 86 | `ClsInTP` | Tax Payment Wizard | Int | 11 | [OTPW](OTPW.md) | 0 |  |
| 87 | `CenVatCom` | CENVAT Component | Int | 11 | - | -1 |  |
| 88 | `MatType` | Material Type | Int | 11 | - | -1 |  |
| 89 | `PstngType` | Posting Type | Int | 11 | - | 0 |  |
| 90 | `ValidFrom2` | Valid from2 | Date | 8 | - | 19000101 |  |
| 91 | `ValidFrom3` | Valid from3 | Date | 8 | - | 19000101 |  |
| 92 | `ValidFrom4` | Valid from4 | Date | 8 | - | 19000101 |  |
| 93 | `ValidFrom5` | Valid from5 | Date | 8 | - | 19000101 |  |
| 94 | `Location` | Loc. | Int | 11 | [OLCT](OLCT.md) |  |  |
| 95 | `WTaxCode` | Withholding Tax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 96 | `EquVatRate` | Equalization Tax % | Num | 19.6 | - |  |  |
| 97 | `EquVatSum` | Equalization Tax Amount | Num | 19.6 | - |  |  |
| 98 | `SYSEquSum` | System Equalization Tax Amount | Num | 19.6 | - |  |  |
| 99 | `TotalVat` | Total Tax | Num | 19.6 | - |  |  |
| 100 | `SYSTVat` | System Total Tax | Num | 19.6 | - |  |  |
| 101 | `WTLiable` | WTax-Liable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 102 | `WTLine` | WTax Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 103 | `WTApplied` | Applied WTax | Num | 19.6 | - |  |  |
| 104 | `WTAppliedS` | Applied WTax (SC) | Num | 19.6 | - |  |  |
| 105 | `WTAppliedF` | Applied WTax (FC) | Num | 19.6 | - |  |  |
| 106 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 107 | `WTSumFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 108 | `WTSumSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 109 | `PayBlock` | Payment Block | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 110 | `PayBlckRef` | Payment Block Abs Entry | Int | 11 | [OPYB](OPYB.md) |  |  |
| 111 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 112 | `InterimTyp` | Interim Account Type | Int | 11 | - | 0 |  |
| 113 | `DprId` | Down Payment Request Key | Int | 11 | - |  |  |
| 114 | `MatchRef` | Reconciliation Reference | nVarChar | 20 | - |  |  |
| 115 | `Ordered` | Payment Ordered | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 117 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 118 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 119 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 120 | `VatRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 121 | `SLEDGERF` | Subledger Flag | VarChar | 1 | - |  |  |
| 122 | `InitRef2` | Initial Reference 2 | nVarChar | 100 | - |  |  |
| 123 | `InitRef3Ln` | Initial Reference 3 | nVarChar | 27 | - |  |  |
| 124 | `ExpUUID` | Expense UUID | nVarChar | 50 | - |  |  |
| 125 | `ExpOPType` | Expense Operation Type | VarChar | 1 | - |  | `P` = Professional Services<br>`R` = Renting Assets<br>`O` = Others<br>`D` = Disposal of Goods<br>`S` = Import of Goods and Services<br>`V` = Import by Virtual Transfer<br>`G` = Global Operations |
| 126 | `ExTransId` | Exposed Transaction ID | Int | 11 | - |  |  |
| 127 | `DocArr` | Source of Posting | Int | 6 | - |  |  |
| 128 | `DocLine` | Source Line Internal ID | Int | 11 | - |  |  |
| 129 | `MYFtype` | MYF type | nVarChar | 2 | - |  | `S1` = MYF Wholesale Sales<br>`S2` = Retail Sales<br>`P1` = MYF Wholesale Purchases<br>`P3` = Other Expense Transactions |
| 130 | `DocEntry` | Source Document Entry | Int | 11 | - |  |  |
| 131 | `DocNum` | Source Document Number | Int | 11 | - |  |  |
| 132 | `DocType` | Source Document Type | nVarChar | 20 | - |  |  |
| 133 | `DocSubType` | Document Subtype | nVarChar | 2 | - |  |  |
| 134 | `RmrkTmpt` | Remark Text Template | Int | 11 | [OTTR](OTTR.md) |  |  |
| 135 | `CemCode` | Cost Element Code | nVarChar | 20 | [OCEM](OCEM.md) |  |  |
| 136 | `InClassCat` | Income Classification Category | Int | 11 | - |  |  |
| 137 | `InClassTyp` | Income Classification Type | Int | 11 | - |  |  |
| 138 | `ExClassCat` | Expense Classification Category | Int | 11 | - |  |  |
| 139 | `ExClassTyp` | Expense Classification Type | Int | 11 | - |  |  |
| 140 | `VATClassCa` | VAT Classification Category | Int | 11 | - |  |  |
| 141 | `VATClassTy` | VAT Classification Type | Int | 11 | - |  |  |
| 142 | `EVatCate` | VAT Category | Int | 11 | - |  |  |
| 143 | `EWtPercCat` | Withheld Percentage Category | Int | 11 | - |  |  |
| 144 | `EWtAmount` | Withheld Amount | Num | 19.6 | - |  |  |
| 145 | `EBVatExCau` | VAT Exemption Cause | Int | 11 | [OVEC](OVEC.md) |  |  |
| 146 | `OrgBPName` | BP name at time of creation. | nVarChar | 200 | - |  |  |
| 147 | `OrgAccName` | Account name at time of creation. | nVarChar | 200 | - |  |  |
| 148 | `AllocNum` | Allocation Number for IL | nVarChar | 50 | - |  |  |
| 149 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 150 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |

## Claves e índices (12)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TransId, Line_ID |
| SHORT_NAME | No | ShortName, IntrnMatch |
| ACCOUNT | No | Account, IntrnMatch |
| TRANS_TYPE | No | TransType |
| PROFIT_ID | No | ProfitCode |
| CURRENCY | No | FCCurrency |
| DUEDATE | No | DueDate |
| REFDATE | No | RefDate |
| INTRNMATCH | No | ShortName, Account, IntrnMatch |
| JDT1BASEL | No | TransType, CreatedBy, SourceLine |
| JDT1CHECKA | No | CheckAbs, TransType |
| PROJECT | No | Project |
