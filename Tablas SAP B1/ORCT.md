# ORCT - Incoming Payments

- **Tabla:** ORCT
- **Descripción:** Incoming Payments
- **Cantidad de campos:** 200
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCT.html

## Campos (200)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | VarChar | 1 | - | C | `C` = Customer<br>`A` = Account<br>`S` = Vendor<br>`P` = P.L.A<br>`T` = Tax<br>`D` = TDS |
| 4 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`C` = Cancellation |
| 5 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original |
| 7 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 8 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 9 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 10 | `CardName` | Customer/Vendor Name | nVarChar | 200 | - |  |  |
| 11 | `Address` | Address | nVarChar | 254 | - |  |  |
| 12 | `DdctPrcnt` | Deduction Percent | Num | 19.6 | - |  |  |
| 13 | `DdctSum` | Total Deductions | Num | 19.6 | - |  |  |
| 14 | `DdctSumFC` | Total Deductions (FC) | Num | 19.6 | - |  |  |
| 15 | `CashAcct` | Cash Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `CashSum` | Cash Amount | Num | 19.6 | - |  |  |
| 17 | `CashSumFC` | Cash Amount (FC) | Num | 19.6 | - |  |  |
| 18 | `CreditSum` | Credit Amount | Num | 19.6 | - |  |  |
| 19 | `CredSumFC` | Credit Amount (FC) | Num | 19.6 | - |  |  |
| 20 | `CheckAcct` | Current Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `CheckSum` | Check Amount | Num | 19.6 | - |  |  |
| 22 | `CheckSumFC` | Check Amount (FC) | Num | 19.6 | - |  |  |
| 23 | `TrsfrAcct` | Transfer Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `TrsfrSum` | Transfer Amount | Num | 19.6 | - |  |  |
| 25 | `TrsfrSumFC` | Transfer Amount (FC) | Num | 19.6 | - |  |  |
| 26 | `TrsfrDate` | Transfer Date | Date | 8 | - |  |  |
| 27 | `TrsfrRef` | Intended Purpose | nVarChar | 27 | - |  |  |
| 28 | `PayNoDoc` | Non-Calculated Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `NoDocSum` | Non-Calculated Amount | Num | 19.6 | - |  |  |
| 30 | `NoDocSumFC` | Non-Calculated Amount (FC) | Num | 19.6 | - |  |  |
| 31 | `DocCurr` | Document Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 32 | `DiffCurr` | Enter in local currency | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 33 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 34 | `SysRate` | System Price | Num | 19.6 | - |  |  |
| 35 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 36 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 37 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 38 | `Ref2` | Reference 2 | nVarChar | 50 | - |  |  |
| 39 | `CounterRef` | Counter Reference | nVarChar | 50 | - |  |  |
| 40 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 41 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 42 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 43 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 44 | `ShowAtCard` | Display Customer Ref. No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `SpiltTrans` | Split Transaction Journal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `CreateTran` | Create Journal Entry | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 47 | `Flags` | Flags | Int | 11 | - | 0 |  |
| 48 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 49 | `DdctSumSy` | System Deduction Amount | Num | 19.6 | - |  |  |
| 50 | `CashSumSy` | Cash Amount (SC) | Num | 19.6 | - |  |  |
| 51 | `CredSumSy` | System Credit Amount | Num | 19.6 | - |  |  |
| 52 | `CheckSumSy` | Check Amount (SC) | Num | 19.6 | - |  |  |
| 53 | `TrsfrSumSy` | Transfer Amount (SC) | Num | 19.6 | - |  |  |
| 54 | `NoDocSumSy` | Non-Invoiced System Amount | Num | 19.6 | - |  |  |
| 55 | `DocTotalSy` | Document Total (SC) | Num | 19.6 | - |  |  |
| 56 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 24 | `24` = Incoming Payment |
| 57 | `StornoRate` | Cancellation Rate | Num | 19.6 | - |  |  |
| 58 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 59 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 60 | `ApplyVAT` | Tax Definition | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 62 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 63 | `confirmed` | Approved | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `ShowJDT` | Display Journal Entries | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 65 | `BankCode` | Bank Code for Bank Transfer | nVarChar | 30 | - |  |  |
| 66 | `BankAcct` | Account for Bank Transfer | nVarChar | 50 | - |  |  |
| 67 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer<br>`B` = BSP |
| 68 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 69 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 70 | `VatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 71 | `VatSum` | Tax Amount | Num | 19.6 | - |  |  |
| 72 | `VatSumFC` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 73 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 74 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 75 | `VatPrcnt` | Tax % | Num | 19.6 | - |  |  |
| 76 | `Dcount` | Discount % | Num | 19.6 | - |  |  |
| 77 | `DcntSum` | Discount Amount | Num | 19.6 | - |  |  |
| 78 | `DcntSumFC` | Discount Amount (FC) | Num | 19.6 | - |  |  |
| 79 | `DcntSumSy` | Discount Amount (SC) | Num | 19.6 | - |  |  |
| 80 | `SpltCredLn` | Split Vendor Credit Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `PrjCode` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 82 | `PaymentRef` | Payment Reference No. | nVarChar | 27 | - |  |  |
| 83 | `Submitted` | Submitted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `Status` | Created by Payment Run | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`C` = BoE Canceled |
| 85 | `PayMth` | Payment Method | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 86 | `BankCountr` | Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 87 | `FreightSum` | Freight Sum | Num | 19.6 | - |  |  |
| 88 | `FreigtFC` | Freight Sum (FC) | Num | 19.6 | - |  |  |
| 89 | `FreigtSC` | Freight Sum (SC) | Num | 19.6 | - |  |  |
| 90 | `BoeAcc` | Boe Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 91 | `BoeNum` | Bill of Exchange No. | Int | 11 | - |  |  |
| 92 | `BoeSum` | Bill of Exchange Amount | Num | 19.6 | - |  |  |
| 93 | `BoeSumFc` | Bill of Exchange Amount (FC) | Num | 19.6 | - |  |  |
| 94 | `BoeSumSc` | Bill of Exchange Amount (SC) | Num | 19.6 | - |  |  |
| 95 | `BoeAgent` | Bill of Exchange Agent | nVarChar | 32 | [OAGP](OAGP.md) |  |  |
| 96 | `BoeStatus` | Bill of Exchange Status | VarChar | 1 | - |  |  |
| 97 | `WtCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 98 | `WtSum` | WTax Amount | Num | 19.6 | - |  |  |
| 99 | `WtSumFrgn` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 100 | `WtSumSys` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 101 | `WtAccount` | WTax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 102 | `WtBaseAmnt` | WTax Taxable Amount | Num | 19.6 | - |  |  |
| 103 | `Proforma` | Proforma | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 104 | `BoeAbs` | Boe Key | Int | 11 | [OBOE](OBOE.md) |  |  |
| 105 | `BpAct` | BP Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 106 | `BcgSum` | Bank Charges Amount | Num | 19.6 | - |  |  |
| 107 | `BcgSumFC` | Bank Charges Amount (FC) | Num | 19.6 | - |  |  |
| 108 | `BcgSumSy` | Bank Charges Amount (SC) | Num | 19.6 | - |  |  |
| 109 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' |  |
| 110 | `PaPriority` | Payment Priority | VarChar | 1 | - | 6 | `1`<br>`2`<br>`3`<br>`4`<br>`5`<br>`6` |
| 111 | `PayToCode` | Pay To | nVarChar | 50 | - |  |  |
| 112 | `IsPaytoBnk` | Is Pay to Bank | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 113 | `PBnkCnt` | Pay to Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 114 | `PBnkCode` | Pay to Bank Code | nVarChar | 30 | - |  |  |
| 115 | `PBnkAccnt` | Pay to Bank Account No. | nVarChar | 50 | - |  |  |
| 116 | `PBnkBranch` | Pay to Bank Branch | nVarChar | 50 | - |  |  |
| 117 | `WizDunBlck` | Wizard Dunning Block | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 118 | `WtBaseSum` | WTax Base Sum | Num | 19.6 | - |  |  |
| 119 | `WtBaseSumF` | WTax Base Sum (FC) | Num | 19.6 | - |  |  |
| 120 | `WtBaseSumS` | WTax Base Sum (SC) | Num | 19.6 | - |  |  |
| 121 | `UndOvDiff` | Under/Overpayment Difference | Num | 19.6 | - |  |  |
| 122 | `UndOvDiffS` | Under/Overpayment Diff. (SC) | Num | 19.6 | - |  |  |
| 123 | `BankActKey` | Bank Account Internal ID | Int | 11 | [DSC1](DSC1.md) |  |  |
| 124 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 125 | `VatDate` | VAT Date | Date | 8 | - |  |  |
| 126 | `TransCode` | Transaction Code | nVarChar | 4 | [OTRC](OTRC.md) |  |  |
| 127 | `PaymType` | Payment Type | VarChar | 1 | - | N | `N`<br>`E` = Electronic<br>`P` = Mail<br>`T` = Telegraph<br>`X` = Express |
| 128 | `TfrRealAmt` | Transfer Real Amount | Num | 19.6 | - |  |  |
| 129 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 130 | `OpenBal` | Open Balance Amount | Num | 19.6 | - |  |  |
| 131 | `OpenBalFc` | Open Balance Amount (FC) | Num | 19.6 | - |  |  |
| 132 | `OpenBalSc` | Open Balance Amount (SC) | Num | 19.6 | - |  |  |
| 133 | `BcgTaxSum` | Bank Charge Tax Amount | Num | 19.6 | - |  |  |
| 134 | `BcgTaxSumF` | Bank Charge Tax Amount(FC) | Num | 19.6 | - |  |  |
| 135 | `BcgTaxSumS` | Bank Charge Tax Amount(SC) | Num | 19.6 | - |  |  |
| 136 | `TpwID` | Tax Payment Wizard ID | Int | 11 | - | 0 |  |
| 137 | `ChallanNo` | Challan No. | nVarChar | 32 | - |  |  |
| 138 | `ChallanBak` | Challan Bank Name | nVarChar | 60 | - |  |  |
| 139 | `ChallanDat` | Challan Received Date | Date | 8 | - |  |  |
| 140 | `WddStatus` | Authorization Status | VarChar | 1 | - | - | `-` = Without<br>`W` = Pending<br>`Y` = Approved<br>`N` = Rejected<br>`P` = Generated<br>`A` = Generated by Authorizer<br>`C` = Canceled |
| 141 | `BcgVatGrp` | Bank Charge Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 142 | `BcgVatPcnt` | Bank Charge Tax % | Num | 19.6 | - |  |  |
| 143 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 144 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 145 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 146 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 147 | `BSRCode` | BSR Code | nVarChar | 25 | - |  |  |
| 148 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 149 | `WTOnhldPst` | WTax On Hold, Posted | Num | 19.6 | - |  |  |
| 150 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 151 | `BuildDesc` | Build Descriptor | nVarChar | 50 | - |  |  |
| 152 | `ResidenNum` | Residence Number | VarChar | 1 | - | 1 | `1` = Spanish Fiscal ID<br>`2` = VAT Registration Number<br>`3` = Passport<br>`4` = Fiscal ID Issued by the Residence Country/Region<br>`5` = Certificate of Fiscal Residence<br>`6` = Other Document |
| 153 | `OperatCode` | Operation Code | VarChar | 1 | - |  | `A` = Summary Invoices Entry<br>`B` = Summary Receipts Entry<br>`C` = Invoice with Several VAT Rates<br>`D` = Correction Invoice<br>`E` = Due VAT Pending Invoice Issuance<br>`F` = Expenses Incurred by Travel Agent for Customers<br>`G` = Special Regulation for VAT Group<br>`H` = Special Regulation for Gold Investment<br>`I` = Reverse Charge Procedure<br>`J` = Unsummarized Receipts<br>`K` = Identification of Error Transactions<br>`N` = Service Invoicing by Travel Agencies on Behalf of Third Parties<br>`R` = Business Office Rental<br>`S` = Subsidies<br>`T` = Incoming Payments for Industrial and Intellectual Property Rights<br>`U` = Insurance Transactions<br>`V` = Purchases from Travel Agencies<br>`W` = Transactions Subject to Production, Service and Import Taxes in Ceuta and Melilla<br>`X` = Transactions with Entrepreneurs Issuing Receipts for Agricultural Compensation |
| 154 | `UndOvDiffF` | Under/Overpayment Diff. (FC) | Num | 19.6 | - |  |  |
| 155 | `MIEntry` | MI Entry Include this Payment | Int | 11 | - | 0 |  |
| 156 | `FreeText1` | Free Text 1 | nVarChar | 254 | - |  |  |
| 157 | `FreeText2` | Free Text 2 | nVarChar | 254 | - |  |  |
| 158 | `FreeText3` | Free Text 3 | nVarChar | 254 | - |  |  |
| 159 | `ShowDocNo` | Display Document No. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 160 | `TDSInterst` | TDS Interest | Num | 19.6 | - | 0 |  |
| 161 | `TDSCharges` | TDS Other Charges | Num | 19.6 | - | 0 |  |
| 162 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 163 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 164 | `MIType` | MI Type Include this Payment | nVarChar | 20 | - |  | `270` = A/R Monthly Invoice<br>`140000014` = A/P Monthly Invoice |
| 165 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 166 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 167 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 168 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 169 | `BPLCentPmt` | Centralized Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 170 | `DraftKey` | Payment Draft Internal ID | Int | 11 | [OPDF](OPDF.md) |  |  |
| 171 | `TDSFee` | TDS Fee | Num | 19.6 | - |  |  |
| 172 | `MinHeadCL` | Minor Head of Challan | Int | 11 | - |  | `200` = TDS Payable by Taxpayer<br>`400` = TDS Regular Assessment (Raised by IT Dept) |
| 173 | `SEPADate` | Requested SEPA Pmt Date | Date | 8 | - |  |  |
| 174 | `OwnerCode` | Payment Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 175 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 176 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 177 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 178 | `TDSType` | TDS Type | VarChar | 1 | - |  | `E` = eTDS<br>`D` = GST TDS<br>`C` = GST TCS |
| 179 | `DrNo` | Dr. No. | nVarChar | 32 | - |  |  |
| 180 | `PmntWTCert` | Payment by WT Certificate Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 181 | `EnPBnkAcct` | Encryption of Pay to Bank Acct | Text | 16 | - |  |  |
| 182 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 183 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 184 | `PriceMode` | Price Mode | VarChar | 1 | - |  | `N` = Net<br>`G` = Gross |
| 185 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 186 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 187 | `EnblDpmTax` | Enable Tax Calculation in Down Payment Invoices | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 188 | `SignMsg` | Signature Input Message | Text | 16 | - |  |  |
| 189 | `SignDigest` | Signature Digest | Text | 16 | - |  |  |
| 190 | `CertifNum` | Certification Number | nVarChar | 50 | - |  |  |
| 191 | `KeyVersion` | Private Key Version | Int | 11 | - |  |  |
| 192 | `QRCodeSPGn` | QR Code Source Generated from Stored Procedure | Text | 16 | - |  |  |
| 193 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 194 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 195 | `ElCoStatus` | Elec. Comm. Status | nVarChar | 10 | - |  | `0` = Approved<br>`1` = Pending Approval<br>`2` = Rejected |
| 196 | `ElCoMsg` | Elec. Comm. Message | nVarChar | 254 | - |  |  |
| 197 | `DigPayment` | Digital Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 198 | `AllocNum` | Allocation Number | nVarChar | 50 | - |  |  |
| 199 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `24` = Incoming Payment<br>`46` = Outgoing Payment |
| 200 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |

## Claves e índices (6)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | Yes | DocNum, PIndicator |
| CARD | No | CardCode |
| HANDWRITEN | No | Handwrtten |
| CANCELED | No | Canceled |
| SERIES | No | Series |
