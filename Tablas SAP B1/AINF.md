# AINF - Company Info

- **Tabla:** AINF
- **Descripción:** Company Info
- **Cantidad de campos:** 222
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AINF.html

## Campos (222)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Version` | Version | Int | 11 | - |  |  |
| 2 | `CompnyName` | Company Name | nVarChar | 200 | - |  |  |
| 3 | `Flags` | Flags | nVarChar | 50 | - | NNNNNNNNNNNNNNNNNNNNNNNNNNNNNN |  |
| 4 | `InfoL1` | Info L1 | Int | 11 | - |  |  |
| 5 | `InfoL2` | Info L2 | Int | 11 | - |  |  |
| 6 | `InfoA1` | Info A1 | nVarChar | 128 | - |  |  |
| 7 | `InfoA2` | Info A2 | nVarChar | 50 | - |  |  |
| 8 | `ACTStamp` | ACT Stamp | Int | 11 | - | 0 |  |
| 9 | `ADMStamp` | (( | Int | 11 | - | 0 |  |
| 10 | `RTTStamp` | RTT Stamp | Int | 11 | - | 0 |  |
| 11 | `CINFStamp` | CINF Stamp | Int | 11 | - | 0 |  |
| 12 | `LawsSet` | Laws Set | nVarChar | 3 | - |  |  |
| 13 | `EnblVatGrp` | Tax System | VarChar | 1 | - |  | `O` = One Tax<br>`L` = Tax per Row<br>`C` = Tax per BP |
| 14 | `EnblVTGPmn` | Use Tax Groups in Payments | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 15 | `VatOOS_O` | Tax Definition | nVarChar | 8 | - |  |  |
| 16 | `VatOOS_I` | Tax Exempt Revenue Account | nVarChar | 8 | - |  |  |
| 17 | `VatStnd_O` | Tax Standard O | nVarChar | 8 | - |  |  |
| 18 | `VatStnd_I` | Tax Standard I | nVarChar | 8 | - |  |  |
| 19 | `VatExmpt_O` | Tax Exempt O | nVarChar | 8 | - |  |  |
| 20 | `VatExmpt_I` | Tax Exempt I | nVarChar | 8 | - |  |  |
| 21 | `VatHalf_O` | Tax Definition | nVarChar | 8 | - |  |  |
| 22 | `VatHalf_I` | Tax Definition | nVarChar | 8 | - |  |  |
| 23 | `VatZrRt_O` | Tax Zero Rate O | nVarChar | 8 | - |  |  |
| 24 | `VatZrRt_I` | Tax Zero Rate I | nVarChar | 8 | - |  |  |
| 25 | `MaxActGrps` | Max. No. of Account Groups | Int | 11 | - |  |  |
| 26 | `EnblDctSrc` | Enable Deduction at Source | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 27 | `EnblRCN` | Enable Retail Chain Stores | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 28 | `EnblCorINV` | Enable Correction Invoice | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 29 | `EnblCshRep` | Enable Cash Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 30 | `EnblIRTRep` | Enable Interest Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 31 | `EnblTrnRep` | Enable Turnover Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 32 | `EnblVPMRep` | Enable Payments Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 33 | `EnblACTRep` | Enable Adv. Corp. Tax Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 34 | `EnblFTZ` | Enable Free Trade Zone | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 35 | `EnblSlfPCH` | Enable Self A/P Invoice | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 36 | `EnblPCHUpd` | Enable Purchase Trans. Update | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 37 | `EnblRsvINV` | Enable Reserve Invoice | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 38 | `EnblRTDnld` | Enable Rates Download | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 39 | `RTTDnldAdr` | Rates Download Web Address | nVarChar | 254 | - |  |  |
| 40 | `ZPrcCode` | Zero Center Code | nVarChar | 8 | - |  |  |
| 41 | `EnblExpns` | Enable Freight Management | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 42 | `EnblRtrRep` | Enable Returns Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 43 | `IsEC` | European Countries | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 44 | `EnblCshDsc` | Enable Cash Discounts | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No<br>`V` = No Tax Adjustment |
| 45 | `EnblLostCD` | Enable Lost Cash Discount | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 46 | `NumActLvls` | No. of Account Group Levels | Int | 11 | - |  |  |
| 47 | `EnblRealRD` | Enable Realized Rate Diff. | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 48 | `EnblVTGNoD` | Enable Tax on Down Payment | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 49 | `EnblGLManP` | Enable Manual Postings in Control Account | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 50 | `EnblOptVIP` | Enable Optional Tax in Payments | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 51 | `EnblActCrC` | Enable Account Currency Change | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 52 | `EnblFrnAct` | Enable Foreign Item Account | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 53 | `EnblECAct` | Enable EU Item Account | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 54 | `EnblECRpt` | Enable 349 Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 55 | `EnblRound` | Enable Rounding | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 56 | `EnblPrVatS` | Enable Print Tax Amount | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 57 | `EnblYrTrns` | Enable Year Transfer | VarChar | 1 | - |  | `Y` = Year Transfer<br>`N` = No<br>`A` = Data Archive |
| 58 | `EnblActTtl` | Enable Account Title | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 59 | `EnblDocWrn` | Enable No Base Doc. Alert | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 60 | `ActSegNum` | No. of Segments | Int | 6 | - | 0 |  |
| 61 | `EnbSgmnAct` | Enable Account Segmentation | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 62 | `SizeOfSeg0` | Size of Segment 0 | Int | 6 | - | 0 |  |
| 63 | `SizeOfSeg1` | Size of Segment 1 | Int | 6 | - | 0 |  |
| 64 | `SizeOfSeg2` | Size of Segment 2 | Int | 6 | - | 0 |  |
| 65 | `SizeOfSeg3` | Size of Segment 3 | Int | 6 | - | 0 |  |
| 66 | `SizeOfSeg4` | Size of Segment 4 | Int | 6 | - | 0 |  |
| 67 | `SizeOfSeg5` | Size of Segment 5 | Int | 6 | - | 0 |  |
| 68 | `SizeOfSeg6` | Size of Segment 6 | Int | 6 | - | 0 |  |
| 69 | `SizeOfSeg7` | Size of Segment 7 | Int | 6 | - | 0 |  |
| 70 | `SizeOfSeg8` | Size of Segment 8 | Int | 6 | - | 0 |  |
| 71 | `SizeOfSeg9` | Size of Segment 9 | Int | 6 | - | 0 |  |
| 72 | `Rprt1099` | 1099 Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 73 | `MultiAddss` | Multi Address | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 74 | `EnbDunning` | Enable Dunning | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 75 | `EnbQtyEDln` | Allow Qty in Delivery Note to Exceed Base Doc. Qty | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 76 | `Itw1Date` | Next Alert Date | Date | 8 | - |  |  |
| 77 | `Itw1Time` | Next Alert Time | Int | 11 | - |  |  |
| 78 | `Itw1Count` | ITW1 Counter | Int | 11 | - |  |  |
| 79 | `EnbPayRef` | Calculate Payment Ref. No. | VarChar | 1 | - |  | `Y` = Payment Reference No.<br>`N` = No<br>`I` = ISR Reference |
| 80 | `EnblDfrTax` | Enable Deferred Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 81 | `EnblClsPr` | Enable Period-End Closing | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 82 | `EnblTaxEL` | Enable Tax Exemption Letter | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 83 | `EnableBOE` | Enable Bills of Exchange | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `EnableWHT` | Enable WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `EnblEquVat` | Enable Equalization Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 86 | `EnblFAsset` | Enable Fixed Assets | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 87 | `EnblDoubt` | Enable Doubtful Debts | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 88 | `RateBase` | Base Date for Exchange Rate | VarChar | 1 | - | P | `P` = Posting Date<br>`T` = Document Date |
| 89 | `BOEStatClo` | Allow Closed Status for Bill of Exchange | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 90 | `ARDocsInWT` | Enable WTax in A/R Docs | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 91 | `BISBnkCnt` | BISR Bank Country/Region | nVarChar | 3 | - |  |  |
| 92 | `BISRBnkCd` | BISR Bank No. | nVarChar | 30 | - |  |  |
| 93 | `BISRBnkAc` | BISR Bank Account | nVarChar | 50 | - |  |  |
| 94 | `BISRBranch` | BISR Branch | nVarChar | 50 | - |  |  |
| 95 | `EnblBPConn` | Enable BP Cards Connection | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 96 | `EnblVATDat` | Enable VAT Date | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 97 | `EnblStAgRp` | Enable Stock Aging Report | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 98 | `EnblCARepo` | Enable Control Acct Reposting | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 99 | `EnblMatRev` | Enable Inventory Revaluation | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 100 | `EnblMBPRec` | Enable Multiple BPs Reconcil. | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 101 | `CshDscGros` | Cash Discount Flag For CN, HK | VarChar | 1 | - | N |  |
| 102 | `EnblTaxInv` | Enable Tax Invoices | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 103 | `EnblCorAct` | Enable Correspondence of Accts | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 104 | `EnblRuDIP` | Enable RU Delivery & Invoice | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 105 | `EnblCurDec` | Enable Decimal Places | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 106 | `EnblPayMtd` | Enable Payment Method on Inv. | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 107 | `EnblBaseUn` | Enable UoM on Invoice | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 108 | `EnblVATAna` | Enable VAT Analytics Report | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |
| 109 | `EnblExREnh` | Enable Frgn. Curr. Valuation | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 110 | `VATGrpCal` | Enable VAT Calculation by Grp | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 111 | `MaxChoose` | No. of Choose from List Rows | Int | 11 | - | 0 |  |
| 112 | `EnblInfla` | Enable Inflation | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 113 | `EnblLAWHT` | Enable Latin America WHT | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 114 | `EnblRTWHT` | Enable Rounding Type WHT | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 115 | `ChkQunty` | Enable Check Quantity In RDR | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `SriMngSys` | SRI Management System | VarChar | 1 | - | R | `A` = On Every Transaction<br>`R` = On Release Only |
| 117 | `BtchMngSys` | Batch Management System | VarChar | 1 | - | R | `A` = On Every Transaction<br>`R` = On Release Only |
| 118 | `SriCreatIn` | Auto SRI creation on receipt | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 119 | `EnblFolio` | Enable Folio Numbers | nVarChar | 2 | - |  | `N` = No<br>`CL` = Chile<br>`MX` = Mexico |
| 120 | `EnblDocSbT` | Enable Document Subtype | nVarChar | 2 | - |  | `N` = No<br>`CL` = Chile<br>`MX` = Mexico<br>`IN` = India |
| 121 | `IepsPayer` | IEPS Payers | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `DaysOrdCnc` | Default Days for Ord. Canc. | Int | 11 | - | 30 |  |
| 123 | `EnblLATaxS` | Enable Latin America Tax Sys | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 124 | `PercOfAcq` | Percent of Total Acquisition | Num | 19.6 | - |  |  |
| 125 | `MinBaseDoc` | Minimum Base Amount per Doc | Num | 19.6 | - |  |  |
| 126 | `EnblDpmJdt` | Create JE Rows in Down Pmnt | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 127 | `EnblDownP` | Down Payment | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 128 | `EnblNDdctC` | Enable Non Deduct VAT Per Card | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 129 | `DocNmMtd` | Enable Sharing Series | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No. |
| 130 | `DoFilter` | Data Ownership Indication | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 131 | `EnblOnPDCh` | Enable Opened Postdated Checks | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 132 | `EnblOnWnCr` | Open Window for Credit Voucher | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 133 | `EnblDefInx` | Enable Define Indexes | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 134 | `EnblMxComm` | Enable Max Commitment | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 135 | `EnblIndxOp` | Enable Index Option | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 136 | `EnblSbtCVo` | Enable Submit Credit Voucher | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 137 | `MinAmntOAP` | Minimum Amount for Appndix O&P | Num | 19.6 | - |  |  |
| 138 | `CredSumm` | Credit Card Summary | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 139 | `PostdChk` | Postdated Check | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 140 | `PostdCred` | Postdated Credit Voucher | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 141 | `CredVend` | Credit Vendors | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 142 | `WkoStatus` | Old Work Order Status | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 143 | `DispTrByDf` | Display Transactions by Dflt | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 144 | `stampTax` | Default Stamp Tax | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 145 | `MinAmntAL` | Minimum Amount for Annual List | Num | 19.6 | - |  |  |
| 146 | `BlockZeroQ` | Block Stock Negative Quantity | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 147 | `AutoCrIns` | Auto Create Customer Eq Card | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 148 | `EnbRepomo` | Enable Inflation for Cash Act | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 149 | `RFCValidat` | Enable RFC Validations | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 150 | `MxDcsInPmt` | Max. Number of Documents in Payment | Int | 11 | - | 0 |  |
| 151 | `RelStkNoPr` | Enable Stock Release without Item Cost | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 152 | `CashDisc` | Cash Discount In Document | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 153 | `EnableSMS` | Enable SMS | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 154 | `EnblIndic` | Enable Indicator | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 155 | `EnbFedTax` | Enable Federal Tax ID | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 156 | `EnblCounty` | Enable County | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 157 | `Language` | Language on Create Company | Int | 11 | - |  |  |
| 158 | `ChkIntgUpd` | Check Data Integrity On Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 159 | `ChkIntgCre` | Check Data Integrity On Create | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 160 | `BisBnkAcKy` | BISR Bank Account Key | Int | 11 | [DSC1](DSC1.md) |  |  |
| 161 | `EnbZeroDec` | Enable Print Check Show Zero Decimal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 162 | `EnbDecWord` | Show Check Decimal in Words | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 163 | `ChkWrdOnly` | Add the Word Only in Checks | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 164 | `EnBnkStmnt` | Bank Statement Processing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 165 | `CalcVatGrp` | Group Lines in VAT Calculation | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 166 | `TaxSysType` | Defines Tax Calculation System | VarChar | 1 | - |  | `A` = Preconfigured Formula with Jurisdiction Support<br>`B` = User-Defined Formula<br>`C` = Preconfigured Formula<br>`M` = Fixed Implementation with Jurisdiction Support<br>`S` = Fixed Implementation |
| 167 | `ESEnabled` | Is Event Sender enabled? | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`C` = Customize |
| 168 | `RateTotal` | Use rate for minor total calc. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 169 | `CompanyHis` | Create/Upgrade History | Text | 16 | - |  |  |
| 170 | `EnblAssVal` | Enable Assessable Value | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 171 | `CompanySta` | Company Status | VarChar | 1 | - | U | `V` = Valid<br>`I` = Invalid<br>`U` = Upgrading<br>`A` = Archived<br>`S` = Inventory Valuation Utility<br>`P` = Upgrade Simulation |
| 172 | `eFRTActLvs` | No. of Levels in Elect. FRT | Int | 11 | - |  |  |
| 173 | `TaxGrpType` | Defines Tax Grouping Type | VarChar | 1 | - | C | `C` = Code<br>`J` = Jurisdiction |
| 174 | `InstallNo` | Installation Number | nVarChar | 30 | - |  |  |
| 175 | `IsOldPA` | Is Old for PA | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 176 | `EnbNegDoc` | Enable Negative Total in Doc | VarChar | 1 | - |  |  |
| 177 | `Algo` | Encryption Algorithm | Int | 6 | - |  |  |
| 178 | `ArcComp` | Archived Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 179 | `UpdatedTF` | Is Updated Tax Formula | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 180 | `DARDBGUID` | Readonly DB GUID for Archiving | nVarChar | 32 | - |  |  |
| 181 | `NegStoLv` | Negative Inv.: Check Level | VarChar | 1 | - | I | `C` = Company<br>`W` = Warehouse<br>`I` = Item Setting |
| 182 | `SPNEnabled` | Enable Transact. Notification | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 183 | `PrsWkCntEb` | Personal Work Center Enabled | VarChar | 1 | - | N | `N` = No Cockpit<br>`Y` = Normal Style Cockpit<br>`F` = Fiori Style Cockpit |
| 184 | `DashbdEb` | Dashboard Enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 185 | `BoxEffDate` | Box: Effective From Date | Date | 8 | - |  |  |
| 186 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 187 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 188 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 189 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 190 | `CreatedBy` | Created By | VarChar | 1 | - | N | `N`<br>`P` = Solution Packager<br>`W` = Express Configuration Wizard |
| 191 | `B1SgtEb` | B1 Suggest: Enable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 192 | `IsHConEnv` | Is in High Concurrency Env | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 193 | `B1BuzzEb` | Enable Streamwork Widget | VarChar | 1 | - | N |  |
| 194 | `IMCEEnable` | IMCE Enable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 195 | `DKeyId` | Current Dynamic Key ID | nVarChar | 128 | - |  |  |
| 196 | `ResetDData` | Reset Dyn. Key Data to Default | VarChar | 1 | - | N |  |
| 197 | `ConvDifAct` | Enable Conversion Diff. Acct | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 198 | `BasEffDate` | Base Effective From Date | Date | 8 | - |  |  |
| 199 | `oldFxAss` | Has Used Old Fixed Assets | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 200 | `MaxRowsCFL` | Max. Rows for Choose from List | Int | 11 | - | 0 | `0` = Unlimited<br>`5000` = 5000<br>`10000` = 10000<br>`50000` = 50000<br>`100000` = 100000 |
| 201 | `ColSel` | Column Selection | Text | 16 | - |  |  |
| 202 | `EnblSPEDUF` | Enable SPED Related UDFs | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 203 | `DpmAffTot` | Down Payment Affects Total | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 204 | `AliasUpd` | Installation Date | nVarChar | 254 | - |  |  |
| 205 | `TrailDays` | Trial Days | Int | 6 | - |  |  |
| 206 | `TestComp` | Test Comp. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 207 | `DashConf` | Enable Side Bar | Text | 16 | - |  |  |
| 208 | `SideEnable` | Enable Side Bar | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 209 | `IsPALInit` | Is PAL Init. or Not | VarChar | 1 | - | N |  |
| 210 | `PANAVer` | Pervasive Version | Int | 11 | - | 0 |  |
| 211 | `ExpEnable` | Enable Expense Claim | VarChar | 1 | - | Y |  |
| 212 | `LastSsrDat` | Last SSR upload date | Date | 8 | - |  |  |
| 213 | `LastSsrHsh` | Last SSR upload date hash | nVarChar | 33 | - |  |  |
| 214 | `B1iTimeOut` | B1i Request Timeout | Int | 11 | - | 30 |  |
| 215 | `CpRfshEnbl` | Enable Cockpit Auto Refresh | VarChar | 1 | - | N |  |
| 216 | `CpRfshIntv` | Cockpit Refresh Interval | Int | 11 | - | 300 |  |
| 217 | `EnbMBFilt` | Enable Filtering Mechanism by Branch | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 218 | `CompnyGUID` | Company GUID | nVarChar | 40 | - |  |  |
| 219 | `ShutTime` | SAP Business One Shutdown Time | Int | 11 | - |  |  |
| 220 | `Migrated` | Migrated DB | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 221 | `Code` | Code | Int | 11 | - | 1 |  |
| 222 | `LastSsrTim` | Last SSR Upload Time | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Version, LogInstanc |
