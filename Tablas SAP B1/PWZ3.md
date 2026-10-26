# PWZ3 - Payment Wizard - Rows 3

- **Tabla:** PWZ3
- **Descripción:** Payment Wizard - Rows 3
- **Cantidad de campos:** 161
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ3.html

## Campos (161)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `PymNum` | Payment Number | Int | 11 | [OCRN](OCRN.md) |  |  |
| 3 | `CardCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `CardName` | Vendor Name | nVarChar | 200 | - |  |  |
| 5 | `PymMeth` | Payment Method | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 6 | `GLAccCode` | G/L Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `GLAccName` | G/L Account Name | nVarChar | 200 | - |  |  |
| 8 | `PymAmount` | Total Payment | Num | 19.6 | - |  |  |
| 9 | `PymAmntFC` | Total Payment (FC) | Num | 19.6 | - |  |  |
| 10 | `PymAmnSyst` | Total Payment (SC) | Num | 19.6 | - |  |  |
| 11 | `InvKey` | Invoice Key | Int | 11 | - |  |  |
| 12 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 13 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 14 | `ValDate` | Due Date | Date | 8 | - |  |  |
| 15 | `TotalLoc` | Total (LC) | Num | 19.6 | - |  |  |
| 16 | `TotalFC` | Total (FC) | Num | 19.6 | - |  |  |
| 17 | `TotalSys` | Total (SC) | Num | 19.6 | - |  |  |
| 18 | `DueBal` | Balance Due | Num | 19.6 | - |  |  |
| 19 | `DueBalFC` | Balance Due (FC) | Num | 19.6 | - |  |  |
| 20 | `DueBalSys` | Balance Due (SC) | Num | 19.6 | - |  |  |
| 21 | `DiscPrcnt` | Discount % | Num | 19.6 | - |  |  |
| 22 | `DiscSum` | Total Discount | Num | 19.6 | - |  |  |
| 23 | `DiscSumFC` | Total Discount (FC) | Num | 19.6 | - |  |  |
| 24 | `DiscSumSy` | Total Discount (SC) | Num | 19.6 | - |  |  |
| 25 | `PayAmount` | Payment Amount | Num | 19.6 | - |  |  |
| 26 | `PayAmntFC` | Payment Amount (FC) | Num | 19.6 | - |  |  |
| 27 | `PayAmntSys` | Payment Amount (SC) | Num | 19.6 | - |  |  |
| 28 | `InvPayAmnt` | Total Invoice for Payment | Num | 19.6 | - |  |  |
| 29 | `InvPayAmFC` | Total Invoice for Payment (FC) | Num | 19.6 | - |  |  |
| 30 | `InvPayAmSy` | Total Invoice for Payment (SC) | Num | 19.6 | - |  |  |
| 31 | `CardType` | BP Type | VarChar | 1 | - | C | `C` = Customer<br>`S` = Vendor<br>`L` = Lead |
| 32 | `Country` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 33 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 13 |  |
| 34 | `PymBnkTrns` | Payment Means | VarChar | 1 | - | C | `C` = Check<br>`T` = Bank Transfer<br>`B` = Bill Of Exchange |
| 35 | `ActFrmtCod` | Account Format Code | nVarChar | 210 | - |  |  |
| 36 | `Checked` | Checked | VarChar | 1 | - |  |  |
| 37 | `FatherLine` | Father Line | VarChar | 1 | - | N |  |
| 38 | `InvCurr` | Document Currency | nVarChar | 3 | - |  |  |
| 39 | `LineRate` | Row Rate | Num | 19.6 | - |  |  |
| 40 | `BfDcntSum` | Amount Before Discount | Num | 19.6 | - |  |  |
| 41 | `BfNetDcnt` | Net Amount Before Discount | Num | 19.6 | - |  |  |
| 42 | `vatApplied` | VAT Applied | Num | 19.6 | - |  |  |
| 43 | `IsTax` | Is Tax | VarChar | 1 | - | Y |  |
| 44 | `IsFreight` | Is Freight | VarChar | 1 | - | Y |  |
| 45 | `IsOrigMeth` | Original Payment Method | VarChar | 1 | - | N |  |
| 46 | `FreightSum` | Freight Sum | Num | 19.6 | - |  |  |
| 47 | `IsrRef` | ISR Ref. No. | nVarChar | 27 | - |  |  |
| 48 | `RoundSum` | Rounding Amount | Num | 19.6 | - |  |  |
| 49 | `Agent` | Agent Code | nVarChar | 32 | [OAGP](OAGP.md) |  |  |
| 50 | `InstId` | Installment ID | Int | 6 | - | 1 |  |
| 51 | `WtSum` | Withholding Tax Amount | Num | 19.6 | - |  |  |
| 52 | `BoeNum` | Bill of Exchange No. | Int | 11 | - |  |  |
| 53 | `NumAtCard` | BP Reference No. | nVarChar | 200 | - |  |  |
| 54 | `DeductPer` | Deduction Percent | Num | 19.6 | - |  |  |
| 55 | `DpmPosted` | Down Payment Posted | VarChar | 1 | - |  |  |
| 56 | `Status` | Inv Status | VarChar | 1 | - |  |  |
| 57 | `NumOfCheck` | Number of Checks | Int | 11 | - | 1 |  |
| 58 | `SumFrstChk` | Sum of First Check | Num | 19.6 | - |  |  |
| 59 | `SumNxtChk` | Sum of Next Check | Num | 19.6 | - |  |  |
| 60 | `PayToCode` | Pay To | nVarChar | 50 | - |  |  |
| 61 | `PayToCntr` | Pay to Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 62 | `PayToBank` | Pay to Bank Code | nVarChar | 30 | - |  |  |
| 63 | `PayToAct` | Pay to Bank Account No. | nVarChar | 50 | - |  |  |
| 64 | `PymCurr` | Payment Currency | nVarChar | 3 | - |  |  |
| 65 | `TaxOnExpSu` | Tax on Freight Amount | Num | 19.6 | - |  |  |
| 66 | `TransId` | Transaction Internal ID | Int | 11 | [OJDT](OJDT.md) |  |  |
| 67 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 68 | `Line_ID` | JE Row Number | Int | 11 | - | 0 |  |
| 69 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 70 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 71 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 72 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 73 | `PymDate` | Payment Date | Date | 8 | - |  |  |
| 74 | `BcgSum` | Bank Charges Amount | Num | 19.6 | - |  |  |
| 75 | `BcgSumFC` | Bank Charges Amount (FC) | Num | 19.6 | - |  |  |
| 76 | `BcgSumSy` | Bank Charges Amount (SC) | Num | 19.6 | - |  |  |
| 77 | `BcgTaxSum` | Bank Charge Tax Amount | Num | 19.6 | - |  |  |
| 78 | `BcgTaxSumF` | Bank Charge Tax Amount (FC) | Num | 19.6 | - |  |  |
| 79 | `BcgTaxSumS` | Bank Charge Tax Amount (SC) | Num | 19.6 | - |  |  |
| 80 | `PrjCode` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 81 | `BcgVatGrp` | Bank Charge Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 82 | `LinePrjCod` | Line Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 83 | `BcgPmnt` | Payment Amount (BCG) | Num | 19.6 | - |  |  |
| 84 | `BcgPmntFc` | Payment Amount FC (BCG) | Num | 19.6 | - |  |  |
| 85 | `BcgPmntSc` | Payment Amount SC (BCG) | Num | 19.6 | - |  |  |
| 86 | `PayOrderNo` | Payment Order Number | Int | 11 | [OIPO](OIPO.md) |  |  |
| 87 | `LineType` | Line Type | VarChar | 1 | - | G | `G` = General<br>`O` = Pay on Account<br>`T` = Pay to Account |
| 88 | `ManualNum` | Manual Entry No. | Int | 11 | - | 0 |  |
| 89 | `Ref1` | Reference 1 | nVarChar | 254 | - |  |  |
| 90 | `Ref2` | Reference 2 | nVarChar | 254 | - |  |  |
| 91 | `Ref3` | Reference 3 | nVarChar | 254 | - |  |  |
| 92 | `OrdrStatus` | Payment Order Status | VarChar | 1 | - |  |  |
| 93 | `BnkCode` | Bank Code | nVarChar | 30 | - |  |  |
| 94 | `BnkAccNo` | Bank Account Number | nVarChar | 50 | - |  |  |
| 95 | `Branch` | Branch | nVarChar | 50 | - |  |  |
| 96 | `BnkCountr` | Manual Line Bank Country/Region | nVarChar | 3 | - |  |  |
| 97 | `TBankCode` | Target Default Bank | nVarChar | 30 | - | -1 |  |
| 98 | `TDflAccoun` | Target Default Account | nVarChar | 50 | - |  |  |
| 99 | `TBankCount` | Target Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 100 | `TargetBran` | Target Bank Branch | nVarChar | 50 | - |  |  |
| 101 | `DscDueDate` | Discount Due Date | Date | 8 | - |  |  |
| 102 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 103 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 104 | `BoeCurrSta` | BoE Current Status | VarChar | 1 | - |  |  |
| 105 | `BoeKey` | Bill of Exchange Key | Int | 11 | [OBOE](OBOE.md) |  |  |
| 106 | `BoeDate` | BoE Date | Date | 8 | - |  |  |
| 107 | `BoeDueDate` | Bill of Exchange Due Date | Date | 8 | - |  |  |
| 108 | `Instruct1` | BoE Instruction 1 | nVarChar | 2 | - |  |  |
| 109 | `Instruct2` | BoE Instruction 2 | nVarChar | 2 | - |  |  |
| 110 | `BoeCancIns` | BoE Cancel Instruction | nVarChar | 2 | - |  |  |
| 111 | `BoeOccCode` | BoE Occurrence Code | nVarChar | 2 | - |  |  |
| 112 | `BoePtfID` | BoE Internal Portfolio ID | nVarChar | 3 | - |  |  |
| 113 | `BoeOurNum` | Our Number in Next BoE | Int | 11 | - |  |  |
| 114 | `BoeIntrAm` | BoE Interest Amount | Num | 19.6 | - |  |  |
| 115 | `BoeDiscD` | BoE Discount Date | Date | 8 | - |  |  |
| 116 | `BoeDisAmnt` | BoE Discount Amount | Num | 19.6 | - |  |  |
| 117 | `BoeFineD` | BoE Fine Date | Date | 8 | - |  |  |
| 118 | `BoeFineAmt` | BoE Fine Amount | Num | 19.6 | - |  |  |
| 119 | `BoeIntrstD` | BoE Interest Date | Date | 8 | - |  |  |
| 120 | `BoeIOFAmt` | BoE IOF Amount | Num | 19.6 | - |  |  |
| 121 | `BoeMovCode` | BoE Movement Code | nVarChar | 10 | - |  |  |
| 122 | `BarcodeRep` | Barcode Representation | nVarChar | 100 | - |  |  |
| 123 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 124 | `PONumber` | External Payment Order Number | Int | 11 | - |  |  |
| 125 | `POSeries` | External Payment Order Series | Int | 11 | - |  |  |
| 126 | `PaPriority` | Payment Priority | VarChar | 1 | - | 5 | `1`<br>`2`<br>`3`<br>`4`<br>`5`<br>`6` |
| 127 | `PaymType` | Payment Type | VarChar | 1 | - | N | `N`<br>`E` = Electronic<br>`P` = Mail<br>`T` = Telegraph<br>`X` = Express |
| 128 | `OriPymMeth` | Original Payment Method Code | nVarChar | 15 | - |  |  |
| 129 | `PymMethTyp` | Payment Method Type | VarChar | 1 | - |  | `I` = Incoming<br>`O` = Outgoing |
| 130 | `SinglePym` | Single Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 131 | `MandateID` | Mandate ID | nVarChar | 35 | - |  |  |
| 132 | `SeqType` | Sequence Type | nVarChar | 4 | - |  | `OOFF` = OOFF<br>`FRST` = FRST<br>`RCUR` = RCUR<br>`FNAL` = FNAL |
| 133 | `BaseDocDat` | Base Document Date | Date | 8 | - |  |  |
| 134 | `OKATO` | OKATO | nVarChar | 11 | - |  |  |
| 135 | `PostPeriod` | Posting Period Code | nVarChar | 10 | - |  |  |
| 136 | `RecipStatu` | Recipient Status | nVarChar | 2 | - |  |  |
| 137 | `BudgetId` | VAT Budget Classification Code | nVarChar | 100 | - |  |  |
| 138 | `PymReason` | Payment Reason | nVarChar | 2 | - |  |  |
| 139 | `BaseDocTyp` | Base Document Type | nVarChar | 2 | - |  |  |
| 140 | `TaxPymType` | Tax Payment Type | nVarChar | 2 | - |  |  |
| 141 | `OKTMO` | OKTMO | nVarChar | 12 | - |  |  |
| 142 | `PymIsUpdat` | Payment method is updated | nVarChar | 30 | - |  |  |
| 143 | `OriPymCode` | Original Payment Method Code | nVarChar | 15 | - |  |  |
| 144 | `OriPymType` | Original Payment Method Type | VarChar | 1 | - |  |  |
| 145 | `ReasonCode` | Reason Code | Int | 11 | - |  |  |
| 146 | `OriActCode` | Original Account Code | nVarChar | 15 | - |  |  |
| 147 | `OriActName` | Original Account Name | nVarChar | 200 | - |  |  |
| 148 | `ReasonLine` | Reason Line | Int | 11 | - |  |  |
| 149 | `OriFormat` | Original Format Code | nVarChar | 210 | - |  |  |
| 150 | `WtIsPym` | Withholding Tax is Payment Type | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 151 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 152 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 153 | `UIPCode` | UIP Code | nVarChar | 25 | - |  |  |
| 154 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 155 | `ExeByServ` | Executed by Server | VarChar | 1 | - |  |  |
| 156 | `SpltPmtVAT` | Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 157 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 158 | `EnPayToAct` | Encryption of Pay to Bank Acct | Text | 16 | - |  |  |
| 159 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 160 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 161 | `SelOrder` | Select Order | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, PymNum |
| DOCUMENT | No | InvKey, ObjType, InstId |
