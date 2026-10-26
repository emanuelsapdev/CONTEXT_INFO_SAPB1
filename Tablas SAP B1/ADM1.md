# ADM1 - Administration Extension

- **Tabla:** ADM1
- **Descripción:** Administration Extension
- **Cantidad de campos:** 203
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADM1.html

## Campos (203)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CurrPeriod` | Free | nVarChar | 10 | - |  |  |
| 2 | `Street` | Street | nVarChar | 100 | - |  |  |
| 3 | `StreetF` | Street Foreign | nVarChar | 100 | - |  |  |
| 4 | `Block` | Block | nVarChar | 100 | - |  |  |
| 5 | `BlockF` | Block Foreign | nVarChar | 100 | - |  |  |
| 6 | `City` | City | nVarChar | 100 | - |  |  |
| 7 | `CityF` | City Foreign | nVarChar | 100 | - |  |  |
| 8 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 9 | `ZipCodeF` | Zip Code Foreign | nVarChar | 20 | - |  |  |
| 10 | `County` | County | nVarChar | 100 | - |  |  |
| 11 | `CountyF` | County Foreign | nVarChar | 100 | - |  |  |
| 12 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 13 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 14 | `IntrntAdrs` | Internet Address | nVarChar | 50 | - |  |  |
| 15 | `Code` | Code | Int | 11 | - | 1 |  |
| 16 | `AssType` | Assessee Type | nVarChar | 100 | - |  |  |
| 17 | `CompnyType` | Company Type | nVarChar | 100 | - |  |  |
| 18 | `NatureBiz` | Nature of Business | nVarChar | 100 | - |  |  |
| 19 | `TaxIdNum4` | Federal Tax ID 4 | nVarChar | 100 | - |  |  |
| 20 | `TaxIdNum5` | Federal Tax ID 5 | nVarChar | 100 | - |  |  |
| 21 | `TaxIdNum6` | Federal Tax ID 6 | nVarChar | 100 | - |  |  |
| 22 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 23 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 24 | `AddrTypeF` | Address Type Foreign | nVarChar | 100 | - |  |  |
| 25 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 26 | `StreetNoF` | Street No. Foreign | nVarChar | 100 | - |  |  |
| 27 | `Building` | Building/Floor/Room | nVarChar | 100 | - |  |  |
| 28 | `BuildingF` | Building/Floor/Room Foreign | nVarChar | 100 | - |  |  |
| 29 | `EccNo` | E.C.C. No. | nVarChar | 40 | - |  |  |
| 30 | `CERegNo` | C.E. Registration No. | nVarChar | 40 | - |  |  |
| 31 | `CERange` | C.E. Range | nVarChar | 60 | - |  |  |
| 32 | `CEDivision` | C.E. Division | nVarChar | 60 | - |  |  |
| 33 | `CeComRate` | C.E. Commisionerate | nVarChar | 60 | - |  |  |
| 34 | `MenuCode` | Manufacturer Code | nVarChar | 60 | - |  |  |
| 35 | `Jurisd` | Jurisdiction | nVarChar | 60 | - |  |  |
| 36 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 37 | `STDCode` | STD Code | Int | 11 | - |  |  |
| 38 | `STDCodeF` | STD Code Foreign | Int | 11 | - |  |  |
| 39 | `CompNature` | Nature of Company | Int | 11 | - | -1 |  |
| 40 | `EconActT` | Economic Activity Type | Int | 11 | - | -1 |  |
| 41 | `CredCOrig` | Credit Contribution Origin | VarChar | 1 | - |  |  |
| 42 | `IPIPeriod` | IPI Period | VarChar | 1 | - |  |  |
| 43 | `CoopAssocT` | Cooperative Association Type | Int | 11 | - | -1 |  |
| 44 | `DspIBPDoc` | Display Inactive Items in Doc. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 45 | `DspIITMDoc` | Display Inactive BPs in Doc. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 46 | `ProfTax` | Profit Taxation | Int | 11 | - | -1 |  |
| 47 | `CompQualif` | Company Qualification | Int | 11 | - | 1 |  |
| 48 | `DeclType` | Declarer Type | Int | 11 | - | 1 |  |
| 49 | `IPITaxCon` | IPI Tax Contributor | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 50 | `ISVATRegNo` | IS VAT Reg. No. of Trader | nVarChar | 100 | - |  |  |
| 51 | `ISVATRegEx` | IS VAT Reg. No. Extension | nVarChar | 10 | - |  |  |
| 52 | `ISObligLvl` | IS Degree of Obligation | VarChar | 1 | - |  |  |
| 53 | `ISTaxState` | IS Federal State of Tax Office | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 54 | `ISComDecID` | IS Company Declaration ID | nVarChar | 32 | - |  |  |
| 55 | `OKDPNum` | OKDP Number | nVarChar | 7 | - |  |  |
| 56 | `ISValidKey` | IS Validation Key Ident. | nVarChar | 35 | - |  |  |
| 57 | `ISDnsce` | IS Declaration Office | nVarChar | 10 | - |  |  |
| 58 | `ISDfltPath` | IS Default File Path | Text | 16 | - |  |  |
| 59 | `ISSimpProc` | IS Simplified Procedure | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 60 | `ISForceCmp` | IS Require All Data | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 61 | `ISCstRecSt` | IS Customs Section | nVarChar | 6 | - |  |  |
| 62 | `ISDfltInct` | IS Default Incoterms | Int | 11 | - |  |  |
| 63 | `ISDfCPEx` | IS Default Customs Proc. Exp. | Int | 11 | - |  |  |
| 64 | `ISDfCPIm` | IS Default Customs Proc. Imp. | Int | 11 | - |  |  |
| 65 | `ISDfNTEx` | IS Dflt Nat. of Trans. for Exp | Int | 11 | - |  |  |
| 66 | `ISDfNTIm` | IS Dflt Nature of Tran. Imp. | Int | 11 | - |  |  |
| 67 | `ISDfPortEx` | IS Default Port for Export | Int | 11 | - |  |  |
| 68 | `ISDfPortIm` | IS Default Port for Import | Int | 11 | - |  |  |
| 69 | `ISDfSPEx` | IS Default Stat. Proc. Export | Int | 11 | - |  |  |
| 70 | `ISDfSPIm` | IS Default Stat. Proc. Import | Int | 11 | - |  |  |
| 71 | `ISDfCSTEx` | IS Default State for Export | Int | 11 | [ODCI](ODCI.md) |  |  |
| 72 | `ISDfCSTIm` | IS Default State for Import | Int | 11 | [ODCI](ODCI.md) |  |  |
| 73 | `ISDfTMEx` | IS Default Transport Mode Exp. | Int | 11 | - |  |  |
| 74 | `ISDfTMIm` | IS Default Transport Mode Imp. | Int | 11 | - |  |  |
| 75 | `ISDeclDept` | Declaring Department | Int | 6 | - |  |  |
| 76 | `ISExlDocQt` | Excl. Docs w/ Qty Less Than | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `ISDocQtLm` | Document Quantity Limit | Num | 19.6 | - |  |  |
| 78 | `ISExlDocAm` | Excl. Docs w/ Amt Less Than | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `ISDocAmLm` | Document Amount Limit | Num | 19.6 | - |  |  |
| 80 | `ISDspNMass` | Always Display Net Mass Value | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 81 | `ImInfSup` | Immediate Information Supply | VarChar | 1 | - |  |  |
| 82 | `Free2` | Free2 | VarChar | 1 | - |  |  |
| 83 | `CommerReg` | Commercial Register | nVarChar | 60 | - |  |  |
| 84 | `DateOfInc` | Date of Incorporation | Date | 8 | - |  |  |
| 85 | `SPEDProf` | SPED Profile | nVarChar | 2 | - |  |  |
| 86 | `EnvTypeNFe` | Environment Type NFe | Int | 11 | - | -1 |  |
| 87 | `Opt4ICMS` | Opting for ICMS 115_03 | VarChar | 1 | - | N |  |
| 88 | `ISInstIntr` | IS Install Intrastat | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 90 | `PTLedgeGen` | Period Type for Ledger Gen. | VarChar | 1 | - | M | `Y` = Year<br>`Q` = Quarter<br>`M` = Month<br>`P` = Period |
| 91 | `BZStRegID` | BZSt Register ID | nVarChar | 6 | - |  |  |
| 92 | `BZStSendID` | BZSt Sender ID | nVarChar | 11 | - |  |  |
| 93 | `PostInVat` | Post Input VAT in A/P Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 94 | `EnbEATrns` | Enable EA for Transfer Doc. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `EnbEAInv` | Enable EA for Inv. Doc. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `AuthUser` | Authorized User | nVarChar | 100 | - |  |  |
| 97 | `AuthPwd` | Authorization Password | nVarChar | 100 | - |  |  |
| 98 | `UrlGoods` | URL for Goods Transport | nVarChar | 250 | - |  |  |
| 99 | `UrlInvType` | URL for Invoice Type | nVarChar | 250 | - |  |  |
| 100 | `ElGoodsFmt` | El. Doc. Format for Goods Trns | Int | 11 | [OLLF](OLLF.md) |  |  |
| 101 | `ElInvFmt` | El. Doc. Format for Invoice | Int | 11 | [OLLF](OLLF.md) |  |  |
| 102 | `ElDigiCert` | El. Digit. Cert. Path | Text | 16 | - |  |  |
| 103 | `TaxRptFrm` | Tax Wizard Reporting From | Date | 8 | - |  |  |
| 104 | `Suframa` | SUFRAMA | nVarChar | 100 | - |  |  |
| 105 | `EnbInItIQI` | Enable Inactive Items in IQI | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 106 | `EnbInItINC` | Enable Inactive Items in INC | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 107 | `ExtRevAct` | Extend Revenue Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 108 | `IsStartup` | Identify Startup Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `IsCUITMndt` | Block adding/updating BP without valid CUIT/CUIL | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 110 | `LnMlBrnch` | Allow Linking of Multiple Branches | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 111 | `DfBrnchPh` | Allow Different Branch in Phases | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 112 | `AplShipPch` | Apply Ship-to on Purchasing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `AsnBrnchBP` | Auto Assign Branches to BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 114 | `ApyPRinAT` | Apply PRJ in Automatic TRN | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 115 | `ApyDRinAT` | Apply DR in Automatic TRN | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `EnMlBrkInv` | Enable Multiple Broker Invoices for Landed Costs | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 117 | `PEFilePath` | Payment Bank File Path1 | Text | 16 | - |  |  |
| 118 | `EnableGDPR` | Enable Personal Data Protection Management | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 119 | `MTDLbltAct` | Outstanding Liabilities Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 120 | `MTDClmAct` | Outstanding Refunds Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 121 | `RmrksIncld` | Document Remarks Include | VarChar | 1 | - | Y | `Y` = Base Document Number<br>`N` = BP Reference Number<br>`E` = Manual Remarks Only |
| 122 | `VerfVatNo` | Verify VAT Numbers | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 123 | `VerfVatMxD` | Max. Days for VAT No. Verify | Int | 11 | - | 1 |  |
| 124 | `VerfVatAct` | Verify VAT Num For Doc Action | nVarChar | 100 | - | NNNNNNNNNNNNNNNNNNNNNNNNNNNNN |  |
| 125 | `CNPJOfIT` | CNPJ of IT Company | nVarChar | 14 | - |  |  |
| 126 | `CnPerson` | Contact Person | nVarChar | 60 | - |  |  |
| 127 | `Email` | E-Mail | nVarChar | 60 | - |  |  |
| 128 | `Telephone` | Phone Number | nVarChar | 50 | - |  |  |
| 129 | `ISUseDscSV` | Include Document Discount for Statistical Value | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 130 | `UrlRegSrv` | URL for Series Registration Service | nVarChar | 250 | - |  |  |
| 131 | `ElSersReg` | El. Doc. Format Series Registration | Int | 11 | - |  |  |
| 132 | `ELSersCncl` | El. Doc. Format Series Cancelation | Int | 11 | - |  |  |
| 133 | `ELSersFin` | El. Doc. Format Series Finalization | Int | 11 | - |  |  |
| 134 | `EnbEASer` | Enable Electronic Approval for Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 135 | `IntrFLines` | Intrastat Result File Num of Lines | Int | 11 | - | -1 |  |
| 136 | `CargoTrack` | Cargo Tracking & Tracing in EU | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 137 | `NoWrnLkUdf` | No Warning for Link-Type UDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 138 | `TaxComPosN` | Calculate Tax for Combined Positive and Negative Rows | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 139 | `ObjList` | Document | nVarChar | 11 | - | 13 | `1470000049` = Capitalization<br>`1470000071` = Depreciation Run<br>`1470000090` = Fixed Asset Transfer<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`234000031` = Return Request<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`14` = A/R Credit Memo<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`19` = A/P Credit Memo<br>`69` = Landed Costs<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Outgoing Payment<br>`76` = Postdated Deposit<br>`57` = Check for Payment<br>`30` = Journal Entry<br>`28` = Journal Voucher<br>`140000010` = Incoming Excise Invoice<br>`140000009` = Outgoing Excise Invoice<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`68` = Work Instructions<br>`202` = Production Order<br>`162` = Inventory Revaluation<br>`156` = Pick List<br>`1470000065` = Inventory Counting<br>`10000071` = Inventory Posting<br>`310000001` = Inventory Opening Balances<br>`191` = Service Call<br>`190` = Service Contract<br>`176` = Equipment Card<br>`88` = Entrada<br>`89` = Salida<br>`90` = Traspaso<br>`132` = Correction Invoice<br>`234000021` = Project Management Document |
| 140 | `RoundSums` | Automatic Rounding for Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 141 | `SplitTran1` | Split Transaction 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 142 | `SplitTran2` | Split Transaction 2 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 143 | `SplitTran3` | Split Transaction 3 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 144 | `EngKBCard` | Change to English Keyboard When Entering BP Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 145 | `EngKBItem` | Change to English Keyboard When Entering Item No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 146 | `SpltTrBOE1` | In Bill of Exchange Deposit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 147 | `MaxUOPay` | Under/Overpayment Amt Allowed | Num | 19.6 | - |  |  |
| 148 | `AllowFuPos` | Allow Future Posting Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 149 | `ErdOutMode` | Post Positive Exchange Rate Differences as Negatives | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 150 | `ErdIncMode` | Post Negative Exchange Rate Differences as Negatives | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 151 | `YearTrans` | Display Transaction in Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 152 | `ReconJeSer` | Reconciliation JE Series | Int | 6 | - | 0 |  |
| 153 | `ChkDupRef` | When Duplicated Customer Reference No. Occurs | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning Only<br>`B` = Block Release |
| 154 | `CpyCVRef` | Allow Copying Customer Reference No. to Target Doc. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 155 | `ReopOrder` | Reopen Doc. by Creating Returns/Goods Returns/Credit Memos Based on Doc. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 156 | `ForceReOrd` | Without User Confirmation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 157 | `RecomPkg` | Recommend Packaging Based on Item Master Data | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 158 | `orderblock` | Block documents with earlier Posting Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 159 | `Enitemcost` | Allow Setting Item Cost When Document is Not Based | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 160 | `ClosePQ` | Close Document When Its Base Purchase Request is Closed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 161 | `CpyPRPrice` | Copy Prices from Purchase Requests to Purchase Orders | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 162 | `EnSetCost` | Enable Setting Cost on All Document Rows by Default | VarChar | 1 | - | N |  |
| 163 | `DftPLChk` | Price List of Return Cost | VarChar | 1 | - | N |  |
| 164 | `DfltPLSel` | Default Price List Selection | Int | 6 | - | -1 |  |
| 165 | `BlockWHT08` | Block Payment in Local Currency in Case BP is Subjected to WHT Group Code '08' | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 166 | `PoDropPrss` | Activate Automatically for Drop-Ship Warehouse Lines | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 167 | `ShowCash` | Allow Cash Accounts Only for Cash Payment Means | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 168 | `PRUseBPTax` | Update Tax Code according to BP default Tax Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 169 | `EnblTtlEgD` | Apply Exchange Rate of Drawn Down Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 170 | `EnblUpdUDF` | Allow Update of User-Defined Fields When Document Rows Are Not Editable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 171 | `EnblDpmTax` | Enable Tax Calculation in Down Payment Invoices | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 172 | `ChkRefBP` | Check for Duplicate Under | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 173 | `ChkRefYear` | Check for Duplicate in Current Fiscal Year Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 174 | `BspDpmType` | Down Payment Type for BSP | VarChar | 1 | - | E | `E`<br>`R` = Down Payment Request<br>`I` = Down Payment Invoice |
| 175 | `ReopenByC` | Display Base Document Items in Procurement Confirmation Wizard When Target Documents Are Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 176 | `ForceReByC` | Without User Confirmation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 177 | `OpenSnB` | Open Serial/Batch Selection for Auto. Allocated Items Issued Primarily by Bin Location | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 178 | `BItmDscUpd` | Block Item Description Updated in the Copied Lines | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 179 | `DeferrTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 180 | `EnblExpns` | Manage Freight in Documents | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 181 | `RateBase` | Exchange Rate Base Date (A/P Documents) | VarChar | 1 | - | P | `P` = Posting Date<br>`T` = Document Date |
| 182 | `DispTrByDf` | Display All Transactions by Default | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 183 | `stampTax` | Default Stamp Tax | nVarChar | 8 | - |  |  |
| 184 | `DaysOrdCnc` | Default Days for Order Cancellation | Int | 11 | - | 30 |  |
| 185 | `ChkQunty` | Activate Automatic Availability Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 186 | `MxDcsInPmt` | Maximum No. of Documents in Payment | Int | 11 | - | 0 |  |
| 187 | `SameURLPmt` | Enable Same URL for Payment Service | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 188 | `ElPmtFmt` | Enable Payment Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 189 | `CpyRefDoc` | Copy Document References | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 190 | `ISEFMAbs` | EFM Template ID | Int | 11 | - |  |  |
| 191 | `CtlActSlct` | Allow Control Account Selection | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 192 | `SepDiscDpm` | Separate Discount % and DPM % Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 193 | `ISExlWoQty` | Exclude Document Row Marked as Without Qty Posting | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 194 | `DppNzbBP` | When Blocking or Cleaning Up a Business Partner with a Non-zero Balance | VarChar | 1 | - | W | `W` = Allow with Warning<br>`B` = Cancel Process |
| 195 | `CpyListNum` | Copy Price List from Base Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 196 | `GenAIModel` | GenAI Service Model | nVarChar | 100 | - |  |  |
| 197 | `GenAIKey` | SAP BTP Service Key | Text | 16 | - |  |  |
| 198 | `EnablGenAI` | Enable GenAI Service | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 199 | `IncUDTUDF` | Include User-Defined Tables and Fields in Query Generation with AI | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 200 | `MaxRetryNo` | Maximum Retries for Query Generation with AI | Int | 11 | - | 3 |  |
| 201 | `UsrAcctID` | User Account ID | nVarChar | 10 | - |  |  |
| 202 | `DpmEUSales` | Incl. DPM in EU Sales Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 203 | `ResourcGrp` | SAP BTP Resource Group | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
