# OINV - A/R Invoice

- **Tabla:** OINV
- **Descripción:** A/R Invoice
- **Cantidad de campos:** 482
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OINV.html

## Campos (482)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | VarChar | 1 | - | I | `I` = Item<br>`S` = Service |
| 4 | `CANCELED` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`C` = Cancellation |
| 5 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original<br>`A` = Amended |
| 7 | `DocStatus` | Document Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 8 | `InvntSttus` | Warehouse Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 9 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 13 | `13` = A/R Invoice |
| 11 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 12 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 13 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 14 | `CardName` | Customer/Vendor Name | nVarChar | 200 | - |  |  |
| 15 | `Address` | Bill To | nVarChar | 254 | - |  |  |
| 16 | `NumAtCard` | BP Reference No. | nVarChar | 200 | - |  |  |
| 17 | `VatPercent` | Tax Rate | Num | 19.6 | - |  |  |
| 18 | `VatSum` | Total Tax | Num | 19.6 | - |  |  |
| 19 | `VatSumFC` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 20 | `DiscPrcnt` | Discount % for Document | Num | 19.6 | - |  |  |
| 21 | `DiscSum` | Total Discount | Num | 19.6 | - |  |  |
| 22 | `DiscSumFC` | Total Discount (FC) | Num | 19.6 | - |  |  |
| 23 | `DocCur` | Document Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 24 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 25 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 26 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 27 | `PaidToDate` | Paid to Date | Num | 19.6 | - |  |  |
| 28 | `PaidFC` | Paid (FC) | Num | 19.6 | - |  |  |
| 29 | `GrosProfit` | Gross Profit | Num | 19.6 | - |  |  |
| 30 | `GrosProfFC` | Gross Profit (FC) | Num | 19.6 | - |  |  |
| 31 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 32 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 33 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 34 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 35 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 36 | `ReceiptNum` | Receipt Number | Int | 11 | - |  |  |
| 37 | `GroupNum` | Payment Terms Code | Int | 6 | [OCTG](OCTG.md) |  |  |
| 38 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 39 | `SlpCode` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 40 | `TrnspCode` | Shipping Type | Int | 6 | [OSHP](OSHP.md) | -1 |  |
| 41 | `PartSupply` | Partial Delivery | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 42 | `Confirmed` | Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 43 | `GrossBase` | Price List for Gross Profit | Int | 6 | - | 0 |  |
| 44 | `ImportEnt` | Order Number | Int | 11 | - |  |  |
| 45 | `CreateTran` | Create Journal Entry | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `SummryType` | Summary Method | VarChar | 1 | - | N | `N` = No Summary<br>`I` = By Items<br>`D` = By Documents |
| 47 | `UpdInvnt` | Whse Update | VarChar | 1 | - | N | `N` = No<br>`O` = Orders from Vendors<br>`C` = Customer Orders<br>`G` = Consignment<br>`I` = Stock |
| 48 | `UpdCardBal` | Update Balances | VarChar | 1 | - | N | `N` = No<br>`O` = Orders<br>`D` = Delivery Notes<br>`B` = Bookkeeping |
| 49 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 50 | `Flags` | Flags | Int | 11 | - | 0 |  |
| 51 | `InvntDirec` | Warehouse Direction | VarChar | 1 | - | X | `X` = Release<br>`E` = Receipt |
| 52 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 53 | `ShowSCN` | Display BP Catalog Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `FatherCard` | BP Consolidation | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 55 | `SysRate` | System Price | Num | 19.6 | - |  |  |
| 56 | `CurSource` | Base Currency | VarChar | 1 | - | C | `L` = Local Currency<br>`S` = System Currency<br>`C` = BP Currency |
| 57 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 58 | `DiscSumSy` | Total Discount (SC) | Num | 19.6 | - |  |  |
| 59 | `DocTotalSy` | Document Total (SC) | Num | 19.6 | - |  |  |
| 60 | `PaidSys` | Paid (SC) | Num | 19.6 | - |  |  |
| 61 | `FatherType` | Parent Summary Type | VarChar | 1 | - | P | `P` = Payment Consolidation<br>`D` = Delivery Consolidation |
| 62 | `GrosProfSy` | Gross Profit (SC) | Num | 19.6 | - |  |  |
| 63 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 64 | `IsICT` | A/R Invoice + Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 65 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 66 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 67 | `VolUnit` | Volume UoM | Int | 6 | - |  |  |
| 68 | `Weight` | Weight | Num | 19.6 | - |  |  |
| 69 | `WeightUnit` | Weight UoM | Int | 6 | - |  |  |
| 70 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 71 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 72 | `Filler` | Filter | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 73 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 74 | `StampNum` | Stamp No. | nVarChar | 16 | - |  |  |
| 75 | `isCrin` | Correction Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 77 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 78 | `selfInv` | Autom. Invoice | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 79 | `VatPaid` | Tax Paid to Date | Num | 19.6 | - |  |  |
| 80 | `VatPaidFC` | Tax Paid (FC) | Num | 19.6 | - |  |  |
| 81 | `VatPaidSys` | Tax Paid (SC) | Num | 19.6 | - |  |  |
| 82 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 83 | `WddStatus` | Authorization Status | VarChar | 1 | - | - | `-` = Without<br>`W` = Pending<br>`Y` = Approved<br>`N` = Rejected<br>`P` = Generated<br>`A` = Generated by Authorizer<br>`C` = Canceled |
| 84 | `draftKey` | Document Draft Internal ID | Int | 11 | [ODRF](ODRF.md) | -1 |  |
| 85 | `TotalExpns` | Total Freight Charges | Num | 19.6 | - |  |  |
| 86 | `TotalExpFC` | Total Freight Charges (FC) | Num | 19.6 | - |  |  |
| 87 | `TotalExpSC` | Total Freight Charges (SC) | Num | 19.6 | - |  |  |
| 88 | `DunnLevel` | Dunning Level | Int | 11 | [ODUN](ODUN.md) |  |  |
| 89 | `Address2` | Ship To | nVarChar | 254 | - |  |  |
| 90 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 91 | `Exported` | Exported | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 92 | `StationID` | Workstation ID | Int | 11 | [CSTN](CSTN.md) |  |  |
| 93 | `Indicator` | Indicator | nVarChar | 2 | [OIDC](OIDC.md) |  |  |
| 94 | `NetProc` | Net Procedure | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `AqcsTax` | Acquisition Tax | Num | 19.6 | - |  |  |
| 96 | `AqcsTaxFC` | Acquisition Tax (FC) | Num | 19.6 | - |  |  |
| 97 | `AqcsTaxSC` | Acquisition Tax (SC) | Num | 19.6 | - |  |  |
| 98 | `CashDiscPr` | Cash Discount Percentage | Num | 19.6 | - |  |  |
| 99 | `CashDiscnt` | Cash Discount | Num | 19.6 | - |  |  |
| 100 | `CashDiscFC` | Cash Discount (FC) | Num | 19.6 | - |  |  |
| 101 | `CashDiscSC` | Cash Discount (SC) | Num | 19.6 | - |  |  |
| 102 | `ShipToCode` | Ship-to Code | nVarChar | 50 | - |  |  |
| 103 | `LicTradNum` | Licensed Dealer No. | nVarChar | 32 | - |  |  |
| 104 | `PaymentRef` | Payment Reference No. | nVarChar | 27 | - |  |  |
| 105 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 106 | `WTSumFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 107 | `WTSumSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 108 | `RoundDif` | Rounding Diff. Amount | Num | 19.6 | - |  |  |
| 109 | `RoundDifFC` | Rounding Diff. Amount (FC) | Num | 19.6 | - |  |  |
| 110 | `RoundDifSy` | Rounding Diff. Amount (SC) | Num | 19.6 | - |  |  |
| 111 | `CheckDigit` | Control Digit | VarChar | 1 | - |  |  |
| 112 | `Form1099` | 1099 Form | Int | 11 | [OTNN](OTNN.md) |  |  |
| 113 | `Box1099` | 1099 Box | nVarChar | 20 | - |  |  |
| 114 | `submitted` | Submitted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 115 | `PoPrss` | PO Process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `Rounding` | Rounding | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `RevisionPo` | Split Purchase Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 118 | `Segment` | Segment | Int | 6 | - | 0 |  |
| 119 | `ReqDate` | Required Date | Date | 8 | - |  |  |
| 120 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 121 | `PickStatus` | Pick Status | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `Pick` | Pick | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `BlockDunn` | Block Dunning | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `PeyMethod` | Payment Method | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 125 | `PayBlock` | Payment Block | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 126 | `PayBlckRef` | Payment Block Abs Entry | Int | 11 | [OPYB](OPYB.md) |  |  |
| 127 | `MaxDscn` | Maximum Discount | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 128 | `Reserve` | Reserve | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 129 | `Max1099` | Max. 1099 Amount | Num | 19.6 | - |  |  |
| 130 | `CntrlBnk` | Central Bank Indicator | nVarChar | 15 | [OCBI](OCBI.md) |  |  |
| 131 | `PickRmrk` | Pick Remarks | nVarChar | 254 | - |  |  |
| 132 | `ISRCodLine` | ISR Coding Line | nVarChar | 53 | - |  |  |
| 133 | `ExpAppl` | Exp applied | Num | 19.6 | - |  |  |
| 134 | `ExpApplFC` | Exp applied FC | Num | 19.6 | - |  |  |
| 135 | `ExpApplSC` | Exp applied DC | Num | 19.6 | - |  |  |
| 136 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 137 | `DeferrTax` | Deferred Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 138 | `LetterNum` | Tax Exemption Letter No. | nVarChar | 50 | - |  |  |
| 139 | `FromDate` | Exemption Validity Date From | Date | 8 | - |  |  |
| 140 | `ToDate` | Exemption Validity Date To | Date | 8 | - |  |  |
| 141 | `WTApplied` | Applied WTax | Num | 19.6 | - |  |  |
| 142 | `WTAppliedF` | Applied WTax (FC) | Num | 19.6 | - |  |  |
| 143 | `BoeReserev` | Bill of Exchange Reserved | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 144 | `AgentCode` | Agent Code | nVarChar | 32 | [OAGP](OAGP.md) |  |  |
| 145 | `WTAppliedS` | Applied WTax (SC) | Num | 19.6 | - |  |  |
| 146 | `EquVatSum` | Total Equalization Tax | Num | 19.6 | - |  |  |
| 147 | `EquVatSumF` | Total Equalization Tax (FC) | Num | 19.6 | - |  |  |
| 148 | `EquVatSumS` | Total Equalization Tax (SC) | Num | 19.6 | - |  |  |
| 149 | `Installmnt` | No. of Installments | Int | 6 | - | 1 |  |
| 150 | `VATFirst` | Apply Tax on 1st Installment | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 151 | `NnSbAmnt` | WTax Non-Subject Amount | Num | 19.6 | - |  |  |
| 152 | `NnSbAmntSC` | WTax Non-Subject Amount (SC) | Num | 19.6 | - |  |  |
| 153 | `NbSbAmntFC` | WTax Non-Subject Amount (FC) | Num | 19.6 | - |  |  |
| 154 | `ExepAmnt` | Withholding Tax Exempt Amount | Num | 19.6 | - |  |  |
| 155 | `ExepAmntSC` | WTax Exempt Amount (SC) | Num | 19.6 | - |  |  |
| 156 | `ExepAmntFC` | WTax Exempt Amount (FC) | Num | 19.6 | - |  |  |
| 157 | `VatDate` | Document Date | Date | 8 | - |  |  |
| 158 | `CorrExt` | External Corrected Document No. | nVarChar | 25 | - |  |  |
| 159 | `CorrInv` | Internal Corrected Document No. | Int | 11 | - |  |  |
| 160 | `NCorrInv` | Next Correcting Document | Int | 11 | - |  |  |
| 161 | `CEECFlag` | Block Creation of Tgt Corr Doc | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 162 | `BaseAmnt` | Base Amount | Num | 19.6 | - |  |  |
| 163 | `BaseAmntSC` | Base Amount (SC) | Num | 19.6 | - |  |  |
| 164 | `BaseAmntFC` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 165 | `CtlAccount` | Control Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 166 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 167 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 168 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 169 | `TxInvRptNo` | Tax Invoice Rpt Number | nVarChar | 10 | [OVRT](OVRT.md) |  |  |
| 170 | `TxInvRptDt` | Tax Invoice Rpt Date | Date | 8 | - |  |  |
| 171 | `KVVATCode` | VAT Code for Tax Invoice Rpt | Text | 16 | - |  |  |
| 172 | `WTDetails` | Withholding Tax Details | nVarChar | 100 | - |  |  |
| 173 | `SumAbsId` | Summary VAT Abstract ID | Int | 11 | [OSRT](OSRT.md) | -1 |  |
| 174 | `SumRptDate` | Summary VAT Report Date | Date | 8 | - |  |  |
| 175 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' |  |
| 176 | `ManualNum` | Manual Number | nVarChar | 20 | - |  |  |
| 177 | `UseShpdGd` | Use Shipped Goods Account | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 178 | `BaseVtAt` | BPL ID Assigned to Invoice | Num | 19.6 | - |  |  |
| 179 | `BaseVtAtSC` | BPL Name | Num | 19.6 | - |  |  |
| 180 | `BaseVtAtFC` | Tax Reg. Number | Num | 19.6 | - |  |  |
| 181 | `NnSbVAt` | Tax Invoice Rpt Number | Num | 19.6 | - |  |  |
| 182 | `NnSbVAtSC` | Tax Invoice Rpt Date | Num | 19.6 | - |  |  |
| 183 | `NbSbVAtFC` | WTax Non-Subject VAT Amt (FC) | Num | 19.6 | - |  |  |
| 184 | `ExptVAt` | WTax Exempt VAT Amount | Num | 19.6 | - |  |  |
| 185 | `ExptVAtSC` | WTax Exempt VAT Amount (SC) | Num | 19.6 | - |  |  |
| 186 | `ExptVAtFC` | WTax Exempt VAT Amount (FC) | Num | 19.6 | - |  |  |
| 187 | `LYPmtAt` | Last Year's Payments | Num | 19.6 | - |  |  |
| 188 | `LYPmtAtSC` | Last Years Payments (SC) | Num | 19.6 | - |  |  |
| 189 | `LYPmtAtFC` | Summary Tax Report Date | Num | 19.6 | - |  |  |
| 190 | `ExpAnSum` | Period Indicator | Num | 19.6 | - |  |  |
| 191 | `ExpAnSys` | Manual Number | Num | 19.6 | - |  |  |
| 192 | `ExpAnFrgn` | Use Shipped Goods Account | Num | 19.6 | - |  |  |
| 193 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- | `--` = A/R Invoice<br>`DN` = A/R Debit Memo<br>`IE` = A/R Invoice Exempt<br>`IB` = A/R Bill<br>`EB` = A/R Exempt Bill<br>`IX` = A/R Export Invoice<br>`IR` = A/R Invoice & Receipt<br>`RI` = A/R Reserve Invoice<br>`GA` = GST Tax Invoice<br>`GD` = GST Debit Memo |
| 194 | `DpmStatus` | Summary VAT Abstract ID | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 195 | `DpmAmnt` | Down Payment Amount LC | Num | 19.6 | - |  |  |
| 196 | `DpmAmntSC` | Down Payment Amount SC | Num | 19.6 | - |  |  |
| 197 | `DpmAmntFC` | Down Payment Amount FC | Num | 19.6 | - |  |  |
| 198 | `DpmDrawn` | Drawn to Down Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 199 | `DpmPrcnt` | Down Payment Percent | Num | 19.6 | - |  |  |
| 200 | `PaidSum` | Total Paid Sum | Num | 19.6 | - |  |  |
| 201 | `PaidSumFc` | Total Paid Sum (FC) | Num | 19.6 | - |  |  |
| 202 | `PaidSumSc` | Total Paid Sum (SC) | Num | 19.6 | - |  |  |
| 203 | `FolioPref` | Folio Prefix String | nVarChar | 4 | - |  |  |
| 204 | `FolioNum` | Folio Number | Int | 11 | - |  |  |
| 205 | `DpmAppl` | Down Payment Applied LC | Num | 19.6 | - |  |  |
| 206 | `DpmApplFc` | Down Payment Applied FC | Num | 19.6 | - |  |  |
| 207 | `DpmApplSc` | Down Payment Applied SC | Num | 19.6 | - |  |  |
| 208 | `LPgFolioN` | Folio No. for Last Page in Doc. | Int | 11 | - |  |  |
| 209 | `Header` | Header | Text | 16 | - |  |  |
| 210 | `Footer` | Footer | Text | 16 | - |  |  |
| 211 | `Posted` | Down Payment Was Posted | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 212 | `OwnerCode` | Document Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 213 | `BPChCode` | BP Channel Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 214 | `BPChCntc` | BP Channel Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 215 | `PayToCode` | Pay To | nVarChar | 50 | - |  |  |
| 216 | `IsPaytoBnk` | Is Pay to Bank | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 217 | `BnkCntry` | Pay to Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 218 | `BankCode` | Pay to Bank Code | nVarChar | 30 | - |  |  |
| 219 | `BnkAccount` | Pay to Bank Account No. | nVarChar | 50 | - |  |  |
| 220 | `BnkBranch` | Pay to Bank Branch | nVarChar | 50 | - |  |  |
| 221 | `isIns` | Reserve Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 222 | `TrackNo` | Tracking Number | nVarChar | 30 | - |  |  |
| 223 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 224 | `LangCode` | Language Code | Int | 11 | [OLNG](OLNG.md) |  |  |
| 225 | `BPNameOW` | BP Name Overwritten | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 226 | `BillToOW` | Bill-To Overwritten | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 227 | `ShipToOW` | Ship-to Overwritten | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 228 | `RetInvoice` | Credit Memo | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 229 | `ClsDate` | Document Closing Date | Date | 8 | - |  |  |
| 230 | `MInvNum` | Monthly Invoice No. | Int | 11 | - |  |  |
| 231 | `MInvDate` | Monthly Invoice Date | Date | 8 | - |  |  |
| 232 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 233 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 234 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 235 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 236 | `Model` | Nota Fiscal Model | nVarChar | 6 | [ONFM](ONFM.md) | 0 |  |
| 237 | `TaxOnExp` | Tax on Freight Sum | Num | 19.6 | - |  |  |
| 238 | `TaxOnExpFc` | Tax on Freight Sum (FC) | Num | 19.6 | - |  |  |
| 239 | `TaxOnExpSc` | Tax on Freight Sum (SC) | Num | 19.6 | - |  |  |
| 240 | `TaxOnExAp` | Tax on Freight Applied | Num | 19.6 | - |  |  |
| 241 | `TaxOnExApF` | Tax on Freight Applied (FC) | Num | 19.6 | - |  |  |
| 242 | `TaxOnExApS` | Tax on Freight Applied (SC) | Num | 19.6 | - |  |  |
| 243 | `LastPmnTyp` | Last Payment Type | VarChar | 1 | - |  | `R` = Receipt<br>`V` = Vendor Payment |
| 244 | `LndCstNum` | Landed Cost Number | Int | 11 | - |  |  |
| 245 | `UseCorrVat` | Use Correction VAT Group | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 246 | `BlkCredMmo` | Block Creation of Target Credit Memo | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 247 | `OpenForLaC` | Open For Landed Costs | VarChar | 1 | - | Y | `N` = Closed for Landed Costs<br>`Y` = Open for Landed Costs |
| 248 | `Excised` | Excised | VarChar | 1 | - | O | `C` = Close<br>`O` = Open |
| 249 | `ExcRefDate` | Excise Ref. Date | Date | 8 | - |  |  |
| 250 | `ExcRmvTime` | Excise Removal Time | nVarChar | 8 | - |  |  |
| 251 | `SrvGpPrcnt` | Gross Profit Prcnt of Service | Num | 19.6 | - |  |  |
| 252 | `DepositNum` | Deposit Number | Int | 11 | - |  |  |
| 253 | `CertNum` | Certificate Number | nVarChar | 31 | - |  |  |
| 254 | `DutyStatus` | Duty Status | VarChar | 1 | - | Y | `Y` = With Payment of Duty<br>`N` = Without Payment of Duty |
| 255 | `AutoCrtFlw` | Auto Create Follow-up Document | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 256 | `FlwRefDate` | Follow-up Document Ref. Date | Date | 8 | - |  |  |
| 257 | `FlwRefNum` | Follow-up Document Ref. Number | nVarChar | 100 | - |  |  |
| 258 | `VatJENum` | VAT Journal Entry Number | Int | 11 | - | -1 |  |
| 259 | `DpmVat` | Down Payment Tax LC | Num | 19.6 | - |  |  |
| 260 | `DpmVatFc` | Down Payment Tax FC | Num | 19.6 | - |  |  |
| 261 | `DpmVatSc` | Down Payment Tax SC | Num | 19.6 | - |  |  |
| 262 | `DpmAppVat` | Down Payment Applied Tax LC | Num | 19.6 | - |  |  |
| 263 | `DpmAppVatF` | Down Payment Applied Tax FC | Num | 19.6 | - |  |  |
| 264 | `DpmAppVatS` | Down Payment Applied Tax SC | Num | 19.6 | - |  |  |
| 265 | `InsurOp347` | 347 Insurance Operation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 266 | `IgnRelDoc` | Ignore Relevant Doc on Archive | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 267 | `BuildDesc` | Build Descriptor | nVarChar | 50 | - |  |  |
| 268 | `ResidenNum` | Residence Number | VarChar | 1 | - | 1 | `1` = Spanish Fiscal ID<br>`2` = VAT Registration Number<br>`3` = Passport<br>`4` = Fiscal ID Issued by the Country/Region of Residence<br>`5` = Certificate of Fiscal Residence<br>`6` = Other Document<br>`7` = Not Registered |
| 269 | `Checker` | Checker | Int | 11 | [OHEM](OHEM.md) |  |  |
| 270 | `Payee` | Payee | Int | 11 | [OHEM](OHEM.md) |  |  |
| 271 | `CopyNumber` | Copy Number | Int | 11 | - | 0 |  |
| 272 | `SSIExmpt` | SSI Exemption | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 273 | `PQTGrpSer` | Pur Quotation Group Series | Int | 11 | - |  |  |
| 274 | `PQTGrpNum` | Pur Quotation Group Number | Int | 11 | - |  |  |
| 275 | `PQTGrpHW` | Pur Quotation Group Manual | VarChar | 1 | - | N |  |
| 276 | `ReopOriDoc` | Reopen Origin. Order by Return | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 277 | `ReopManCls` | Reop. Man. Closed/Canc. Orders | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 278 | `DocManClsd` | Document Was Closed Manually | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`U` = Unknown |
| 279 | `ClosingOpt` | Closing Option | Int | 6 | - | 1 |  |
| 280 | `SpecDate` | Posting Date Specified by User | Date | 8 | - |  |  |
| 281 | `Ordered` | Payment Ordered | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 282 | `NTSApprov` | NTS Approved | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 283 | `NTSWebSite` | E-Tax Web Site | Int | 6 | [OTWS](OTWS.md) |  |  |
| 284 | `NTSeTaxNo` | E-Tax Number | nVarChar | 50 | - |  |  |
| 285 | `NTSApprNo` | NTS Approval Number | nVarChar | 50 | - |  |  |
| 286 | `PayDuMonth` | Start From | VarChar | 1 | - |  | `E` = Month End<br>`H` = Half Month<br>`Y` = Month Start<br>`N` = Selected Date |
| 287 | `ExtraMonth` | Number of Additional Months | Int | 6 | - |  |  |
| 288 | `ExtraDays` | Number of Additional Days | Int | 6 | - |  |  |
| 289 | `CdcOffset` | Cash Discount Offset | Int | 6 | - | 0 |  |
| 290 | `SignMsg` | Signature Input Message | Text | 16 | - |  |  |
| 291 | `SignDigest` | Signature Digest | Text | 16 | - |  |  |
| 292 | `CertifNum` | Certification Number | nVarChar | 50 | - |  |  |
| 293 | `KeyVersion` | Private Key Version | Int | 11 | - |  |  |
| 294 | `EDocGenTyp` | Electr. Doc. Generation Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later<br>`S` = Send<br>`R` = Send - Later |
| 295 | `ESeries` | Electronic Series | Int | 6 | [NNM4](NNM4.md) |  |  |
| 296 | `EDocNum` | Electronic Document Number | nVarChar | 50 | - |  |  |
| 297 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 298 | `OnlineQuo` | Create Online Quotation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 299 | `POSEqNum` | POS Equipment Number | nVarChar | 20 | - |  |  |
| 300 | `POSManufSN` | POS Manufacturer Serial Number | nVarChar | 20 | - |  |  |
| 301 | `POSCashN` | POS Cashier Number | Int | 11 | - |  |  |
| 302 | `EDocStatus` | Electronic Document Status | VarChar | 1 | - | C | `N` = New<br>`P` = Pending<br>`S` = Sent<br>`E` = Error<br>`C` = OK |
| 303 | `EDocCntnt` | Electronic Document Content | Text | 16 | - |  |  |
| 304 | `EDocProces` | Electronic Document Process | VarChar | 1 | - | C | `C` = CFD<br>`I` = CFDI |
| 305 | `EDocErrCod` | Electronic Document Error Code | nVarChar | 50 | - |  |  |
| 306 | `EDocErrMsg` | Electronic Document Error Msg | Text | 16 | - |  |  |
| 307 | `EDocCancel` | Electronic Document - Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 308 | `EDocTest` | Electronic Document - Testing | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 309 | `EDocPrefix` | Electronic Document - Prefix | nVarChar | 10 | - |  |  |
| 310 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 311 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 312 | `DpmAsDscnt` | Discount Document with Dpm | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 313 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 314 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 315 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 316 | `GTSRlvnt` | Relevant To GTS | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 317 | `BaseDisc` | Base Discount LC | Num | 19.6 | - |  |  |
| 318 | `BaseDiscSc` | Base Discount SC | Num | 19.6 | - |  |  |
| 319 | `BaseDiscFc` | Base Discount FC | Num | 19.6 | - |  |  |
| 320 | `BaseDiscPr` | Base Discount Percentage | Num | 19.6 | - |  |  |
| 321 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 322 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 323 | `SrvTaxRule` | Apply Service Tax Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 324 | `AnnInvDecR` | Annual Inv. Declaration Ref. | Int | 11 | - |  |  |
| 325 | `Supplier` | Supplier | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 326 | `Releaser` | Goods Distribution Approver | Int | 11 | [OHEM](OHEM.md) |  |  |
| 327 | `Receiver` | Goods Release Approver | Int | 11 | [OHEM](OHEM.md) |  |  |
| 328 | `ToWhsCode` | To Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 329 | `AssetDate` | Fixed Asset Value Date | Date | 8 | - |  |  |
| 330 | `Requester` | User Requesting Goods | nVarChar | 25 | - |  |  |
| 331 | `ReqName` | User Name | nVarChar | 155 | - |  |  |
| 332 | `Branch` | Branch | Int | 6 | [OUBR](OUBR.md) |  |  |
| 333 | `Department` | Department | Int | 6 | [OUDP](OUDP.md) |  |  |
| 334 | `Email` | E-Mail | nVarChar | 100 | - |  |  |
| 335 | `Notify` | Send Notification Needed | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 336 | `ReqType` | Requester Type User/Employee | Int | 11 | - | 12 | `12` = User<br>`171` = Employee |
| 337 | `OriginType` | Document Origin | VarChar | 1 | - | M | `M` = Manual<br>`R` = MRP<br>`S` = Sales Order<br>`D` = Document Generation Wizard |
| 338 | `IsReuseNum` | Is Reusing Document Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 339 | `IsReuseNFN` | Is Reusing Nota Fiscal Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 340 | `DocDlvry` | Document Delivery | VarChar | 1 | - |  | `0` = None<br>`1` = Create Online Document<br>`2` = Post to Ariba Network |
| 341 | `PaidDpm` | Paid by Down Payment | Num | 19.6 | - |  |  |
| 342 | `PaidDpmF` | Paid by Down Payment (FC) | Num | 19.6 | - |  |  |
| 343 | `PaidDpmS` | Paid by Down Payment (SC) | Num | 19.6 | - |  |  |
| 344 | `EnvTypeNFe` | Environment Type NF-e | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 345 | `AgrNo` | Agreement No. | Int | 11 | - |  |  |
| 346 | `IsAlt` | Is Alteration | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 347 | `AltBaseTyp` | Alteration Base Type | Int | 11 | - | -1 | `-1`<br>`13`<br>`18`<br>`163`<br>`165` |
| 348 | `AltBaseEnt` | Alteration Base Entry | Int | 11 | - |  |  |
| 349 | `AuthCode` | Authorization Code | nVarChar | 250 | - |  |  |
| 350 | `StDlvDate` | Start Delivery Date | Date | 8 | - |  |  |
| 351 | `StDlvTime` | Start Delivery Time | Int | 11 | - |  |  |
| 352 | `EndDlvDate` | End Delivery Date | Date | 8 | - |  |  |
| 353 | `EndDlvTime` | End Delivery Time | Int | 11 | - |  |  |
| 354 | `VclPlate` | Vehicle Plate | nVarChar | 20 | - |  |  |
| 355 | `ElCoStatus` | Elec. Comm. Status | nVarChar | 10 | - |  | `0` = Approved<br>`1` = Pending Approval<br>`2` = Rejected |
| 356 | `AtDocType` | AT Document Type | nVarChar | 10 | - |  |  |
| 357 | `ElCoMsg` | Elec. Comm. Message | nVarChar | 254 | - |  |  |
| 358 | `PrintSEPA` | Print SEPA Direct Debit Prenotification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 359 | `FreeChrg` | Free of Charge BP | Num | 19.6 | - |  |  |
| 360 | `FreeChrgFC` | Free of Charge BP FC | Num | 19.6 | - |  |  |
| 361 | `FreeChrgSC` | Free of Charge BP SC | Num | 19.6 | - |  |  |
| 362 | `NfeValue` | NF-e Value | Num | 19.6 | - |  |  |
| 363 | `FiscDocNum` | Fiscal Document Number | nVarChar | 100 | - |  |  |
| 364 | `RelatedTyp` | Related Type | Int | 11 | - | -1 | `-1`<br>`24` = Incoming Payment<br>`46` = Outgoing Payments |
| 365 | `RelatedEnt` | Related Entry | Int | 11 | - |  |  |
| 366 | `CCDEntry` | CCD Abs. Entry | Int | 11 | - |  |  |
| 367 | `NfePrntFo` | NF-e Printing Format | Int | 11 | - | 0 | `0` = No DANFE<br>`1` = Portrait<br>`2` = Landscape<br>`3` = Simplified<br>`4` = DANFE NFC-e<br>`5` = Mail |
| 368 | `ZrdAbs` | POS Daily Summary Number | Int | 11 | [OZRD](OZRD.md) |  |  |
| 369 | `POSRcptNo` | POS Receipt Number | Int | 11 | - |  |  |
| 370 | `FoCTax` | Free of Charge BP Tax | Num | 19.6 | - |  |  |
| 371 | `FoCTaxFC` | Free of Charge BP Tax FC | Num | 19.6 | - |  |  |
| 372 | `FoCTaxSC` | Free of Charge BP Tax SC | Num | 19.6 | - |  |  |
| 373 | `TpCusPres` | Type of End-User Presence | Int | 11 | [OBNI](OBNI.md) |  |  |
| 374 | `ExcDocDate` | Excise Doc. Date | Date | 8 | - |  |  |
| 375 | `FoCFrght` | Free of Charge Freight | Num | 19.6 | - |  |  |
| 376 | `FoCFrghtFC` | Free of Charge Freight FC | Num | 19.6 | - |  |  |
| 377 | `FoCFrghtSC` | Free of Charge Freight SC | Num | 19.6 | - |  |  |
| 378 | `InterimTyp` | Interim Type | Int | 6 | - | 0 | `0` = None<br>`1` = Exchange Rate Interim Document<br>`2` = Cash Discount Interim Document |
| 379 | `PTICode` | POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |
| 380 | `Letter` | Letter | VarChar | 1 | - |  | `A` = A<br>`B` = B<br>`C` = C<br>`E` = E<br>`M` = M<br>`R` = R<br>`T` = T<br>`X` = X<br>`-` = - |
| 381 | `FolNumFrom` | Folio Number From | Int | 11 | - |  |  |
| 382 | `FolNumTo` | Folio Number To | Int | 11 | - |  |  |
| 383 | `FolSeries` | Folio Series | Int | 11 | [OFNS](OFNS.md) |  |  |
| 384 | `SplitTax` | Split Payment Tax | Num | 19.6 | - |  |  |
| 385 | `SplitTaxFC` | Split Payment Tax FC | Num | 19.6 | - |  |  |
| 386 | `SplitTaxSC` | Split Payment Tax SC | Num | 19.6 | - |  |  |
| 387 | `ToBinCode` | To Bin Location | nVarChar | 228 | - |  |  |
| 388 | `PriceMode` | Price Mode | VarChar | 1 | - |  | `N` = Net<br>`G` = Gross<br>`M` = Net and Gross |
| 389 | `PoDropPrss` | PO Drop-Ship Process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 390 | `PermitNo` | Permit Number | nVarChar | 20 | - |  |  |
| 391 | `MYFtype` | MYF type | nVarChar | 2 | - |  | `S1` = MYF Wholesale Sales<br>`S2` = Retail Sales<br>`P1` = MYF Wholesale Purchases<br>`P3` = Other Expense Transactions |
| 392 | `DocTaxID` | Document Tax ID | nVarChar | 32 | - |  |  |
| 393 | `DateReport` | Date of Reporting | Date | 8 | - |  |  |
| 394 | `RepSection` | Reporting Section | nVarChar | 3 | - |  |  |
| 395 | `ExclTaxRep` | Exclude from Control Statement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 396 | `PosCashReg` | POS/Cash Register | Int | 11 | [OPCM](OPCM.md) |  |  |
| 397 | `DmpTransID` | Trans ID for Down Payment | nVarChar | 20 | - |  |  |
| 398 | `ECommerBP` | E-Commerce Operator | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 399 | `EComerGSTN` | GST Regn No of E-Commerce | nVarChar | 15 | - |  |  |
| 400 | `Revision` | Revision | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 401 | `RevRefNo` | Original Ref. No. | nVarChar | 100 | - |  |  |
| 402 | `RevRefDate` | Original Ref. Date | Date | 8 | - |  |  |
| 403 | `RevCreRefN` | Original Credit/Debit Ref. No. | nVarChar | 100 | - |  |  |
| 404 | `RevCreRefD` | Orign Credit/Debit Ref. Date | Date | 8 | - |  |  |
| 405 | `TaxInvNo` | Tax Invoice No. | nVarChar | 100 | - |  |  |
| 406 | `FrmBpDate` | From Vendor Date | Date | 8 | - |  |  |
| 407 | `GSTTranTyp` | GST Transaction Type | nVarChar | 2 | - |  | `--` = Bill of Supply<br>`GA` = GST Tax Invoice<br>`GD` = GST Debit Memo |
| 408 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`67` = Inventory Transfer |
| 409 | `BaseEntry` | Base Document Internal Key | Int | 11 | - |  |  |
| 410 | `ComTrade` | Commission Trade | VarChar | 1 | - | E | `E`<br>`S` = Sales Agent<br>`P` = Purchase Agent<br>`C` = Consignor |
| 411 | `UseBilAddr` | Determine GST by Using Bill to | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 412 | `IssReason` | Reason for issuing note | Int | 6 | - | 1 | `1` = Sales Return<br>`2` = Post sale discount<br>`3` = Deficiency in service<br>`4` = Correction in invoice<br>`5` = Change in POS<br>`6` = Finalization of Provisional Assessment<br>`7` = Others |
| 413 | `ComTradeRt` | Commission Trade Return | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 414 | `SplitPmnt` | A/P Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 415 | `SOIWizId` | SOI Wizard ID | Int | 11 | [OSOI](OSOI.md) |  |  |
| 416 | `SelfPosted` | Self Invoice Created [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 417 | `EnBnkAcct` | Encryption of Pay to Bank Acct | Text | 16 | - |  |  |
| 418 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 419 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 420 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |
| 421 | `EWBGenType` | E-Way Bill Generation Type | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later |
| 422 | `CtActTax` | Customer Accounting Tax | Num | 19.6 | - |  |  |
| 423 | `CtActTaxFC` | Customer Accounting Tax (FC) | Num | 19.6 | - |  |  |
| 424 | `CtActTaxSC` | Customer Accounting Tax (SC) | Num | 19.6 | - |  |  |
| 425 | `EDocType` | eDoc Type | VarChar | 1 | - | F | `F` = FE<br>`C` = FCE |
| 426 | `QRCodeSrc` | QR Code Source | Text | 16 | - |  |  |
| 427 | `AggregDoc` | Aggregate Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 428 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 429 | `ShipState` | Shipment State Code | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 430 | `ShipPlace` | Shipment Place Name | nVarChar | 60 | - |  |  |
| 431 | `CustOffice` | Customs Office Name | nVarChar | 60 | - |  |  |
| 432 | `FCI` | FCI Number | nVarChar | 36 | - |  |  |
| 433 | `NnSbCuAmnt` | WTax Non-Subject CU Amount | Num | 19.6 | - |  |  |
| 434 | `NnSbCuSC` | WTax Non-Subject CU Amount SC | Num | 19.6 | - |  |  |
| 435 | `NnSbCuFC` | WTax Non-Subject CU Amount FC | Num | 19.6 | - |  |  |
| 436 | `ExepCuAmnt` | WTax Exempt CU Amount | Num | 19.6 | - |  |  |
| 437 | `ExepCuSC` | WTax Exempt CU Amount SC | Num | 19.6 | - |  |  |
| 438 | `ExepCuFC` | WTax Exempt CU Amount FC | Num | 19.6 | - |  |  |
| 439 | `AddLegIn` | Additional Legal Information | nVarChar | 100 | - |  |  |
| 440 | `LegTextF` | Legal Text Format | Int | 11 | [OLTF](OLTF.md) |  |  |
| 441 | `IndFinal` | Indicator for Final Consumer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 442 | `DANFELgTxt` | DANFE Legal Text | Text | 16 | - |  |  |
| 443 | `PostPmntWT` | Post Payment Withholding Tax | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 444 | `QRCodeSPGn` | QR Code Source Generated from Stored Procedure | Text | 16 | - |  |  |
| 445 | `FCEPmnMean` | Use FCEs as Payment Means | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 446 | `ReqCode` | Requester Code | nVarChar | 50 | - |  |  |
| 447 | `NotRel4MI` | Not Relevant for Monthly Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 448 | `Rel4PPTax` | Relevant for Plastic Packaging Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 449 | `ConfrmedBy` | Confirmed By | Int | 11 | [OUSR](OUSR.md) |  |  |
| 450 | `ConfrmedOn` | Confirmed On | Date | 8 | - |  |  |
| 451 | `ReqID` | Requester ID | Int | 11 | - |  |  |
| 452 | `NonDdAmt` | Non-Deductible Amount | Num | 19.6 | - |  |  |
| 453 | `NonDdAmtSC` | Non-Deductible Amount (SC) | Num | 19.6 | - |  |  |
| 454 | `NonDdAmtFC` | Non-Deductible Amount (FC) | Num | 19.6 | - |  |  |
| 455 | `BookeTdsBP` | Book the eTDS to the Business Partner | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 456 | `AllocNum` | Allocation Number for IL | nVarChar | 50 | - |  |  |
| 457 | `DPayToAddr` | Digital Pay To Address | nVarChar | 50 | - |  |  |
| 458 | `DigPayment` | Digital Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 459 | `OperProfit` | Operating Profit | Num | 19.6 | - |  |  |
| 460 | `OperProfFC` | Operating Profit (FC) | Num | 19.6 | - |  |  |
| 461 | `OperProfSy` | Operating Profit (SC) | Num | 19.6 | - |  |  |
| 462 | `NetIncome` | Net Income | Num | 19.6 | - |  |  |
| 463 | `NetIncomFC` | Net Income (FC) | Num | 19.6 | - |  |  |
| 464 | `NetIncomSy` | Net Income (SC) | Num | 19.6 | - |  |  |
| 465 | `PDueMonEnd` | End On | VarChar | 1 | - |  | `E` = End of Month<br>`H` = Middle of Month<br>`Y` = Start of Month<br>`N` = None |
| 466 | `RShipToCod` | Ship-to Code for Return | nVarChar | 50 | - |  |  |
| 467 | `Address3` | Ship To for Return | nVarChar | 254 | - |  |  |
| 468 | `RShipToOW` | Ship-to Address Overwritten for Return | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 469 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |
| 470 | `ListNum` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 471 | `AplTaxOnFr` | Apply Only Taxes in First Installment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`T` = Tax Only |
| 472 | `DocEmail` | E-Mail | nVarChar | 254 | - |  |  |
| 473 | `SirenNo` | SIREN No. | nVarChar | 9 | - |  |  |
| 474 | `SiretNo` | SIRET No. | nVarChar | 32 | - |  |  |
| 475 | `CpyDtyStts` | Copy Duty Status from Base | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 476 | `RoutingCod` | Routing Code | nVarChar | 100 | - |  |  |
| 477 | `DpmSpAmnt` | Down Payment Split Amount LC | Num | 19.6 | - |  |  |
| 478 | `DpmSpAmtSC` | Down Payment Split Amount SC | Num | 19.6 | - |  |  |
| 479 | `DpmSpAmtFC` | Down Payment Split Amount FC | Num | 19.6 | - |  |  |
| 480 | `CmDpmPrcnt` | Credit Memo Down Payment Percent | Num | 19.6 | - |  |  |
| 481 | `Suffix` | Suffix | nVarChar | 20 | - |  |  |
| 482 | `CpyFthrCrd` | Copy Father Card from BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (13)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| AT_CARD | No | NumAtCard, CardCode |
| CUSTOMER | No | CardCode |
| NUM | No | DocNum, Instance, Segment, DocSubType, PIndicator |
| DOC_STATUS | No | DocStatus, CANCELED |
| FTHR_CARD | No | FatherCard, FatherType |
| SERIES | No | Series |
| OWNER_CODE | No | OwnerCode |
| DATE_PIND | No | DocDate, PIndicator |
| ESERIES | No | ESeries, EDocNum |
| STS_CNCL | No | InvntSttus, CANCELED, isIns |
| FOL_SERIES | No | FolSeries |
| PROJECT | No | Project |
