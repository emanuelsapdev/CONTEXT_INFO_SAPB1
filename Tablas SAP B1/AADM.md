# AADM - Administration - Log

- **Tabla:** AADM
- **Descripción:** Administration - Log
- **Cantidad de campos:** 647
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AADM.html

## Campos (647)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CompnyName` | Company Name | nVarChar | 200 | - |  |  |
| 2 | `CompnyAddr` | Address | nVarChar | 254 | - |  |  |
| 3 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 4 | `PrintHeadr` | Printing Header | nVarChar | 100 | - |  |  |
| 5 | `Phone1` | Telephone Number 1 | nVarChar | 50 | - |  |  |
| 6 | `Phone2` | Telephone Number 2 | nVarChar | 50 | - |  |  |
| 7 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 8 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 9 | `Manager` | Managing Director | nVarChar | 100 | - |  |  |
| 10 | `CompType` | Chart of Accounts Template | VarChar | 1 | - | U |  |
| 11 | `MainCurncy` | Local Currency | nVarChar | 3 | - |  |  |
| 12 | `SysCurrncy` | System Currency | nVarChar | 3 | - |  |  |
| 13 | `DispPosDeb` | Open Balance with Minus Sign | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `DefLengthU` | Standard Unit of Length | Int | 6 | - | 2 |  |
| 15 | `DefWeightU` | Default Weight UoM | Int | 6 | - | 2 |  |
| 16 | `DfltVendPM` | Default Payt Method for Vendor | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 17 | `DirectRate` | Direct/Indirect Rate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `MinAmnt347` | Minimum Amount for 347 Report | Num | 19.6 | - |  |  |
| 19 | `AutoITW` | Set Items - Warehouses | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `BankCountr` | Bank Country/Region | nVarChar | 3 | - |  |  |
| 21 | `TaxIdNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 22 | `RevOffice` | Tax Office | nVarChar | 100 | - |  |  |
| 23 | `FreeZoneNo` | Additional ID Number | nVarChar | 32 | - |  |  |
| 24 | `DdctFileNo` | Deduction File No. | nVarChar | 50 | - |  |  |
| 25 | `VatCharge` | Tax Collection | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 26 | `PayOutVat` | Tax Definition | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `VatPrcnt` | Tax Rate | Num | 19.6 | - |  |  |
| 28 | `DpsitPrcnt` | Advances on Corp. Income Tax % | Num | 19.6 | - |  |  |
| 29 | `IncomeTax` | Withholding Tax % | Num | 19.6 | - |  |  |
| 30 | `VendorDdct` | Withholding Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `CustmrDdct` | Customer's Deduction at Source | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `DdctPercnt` | Withholding Tax Deduction % | Num | 19.6 | - |  |  |
| 33 | `DdctExpire` | Withholding Tax Ded. in % - Ex | Date | 8 | - |  |  |
| 34 | `DdctOffice` | Withholding Tax Deduction - Of | nVarChar | 100 | - |  |  |
| 35 | `EURepSqntl` | Sequential Number of EU Sales | Int | 11 | - | 0 |  |
| 36 | `BoxRptSeq` | Box Report Sequential Number | Int | 11 | - | 0 |  |
| 37 | `WTLiable` | WTax Liable | VarChar | 1 | - | Y |  |
| 38 | `DfltCustPM` | Default Payt Method for Cust. | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 39 | `AllowFuPos` | Allow Future Posting Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `UseProdWip` | Use Product WIP Account | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 41 | `CurrPeriod` | Current Period | nVarChar | 10 | - |  |  |
| 42 | `XmlPath` | XML File Path | Text | 16 | - |  |  |
| 43 | `DflBnkKey` | Default Bank Key | Int | 11 | [ODSC](ODSC.md) |  |  |
| 44 | `BSInstled` | Bank Statement Installed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `UseShpdGd` | Use Shipped Goods Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `UseExtRpt` | Use Extended Reporting (OTRS) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `ERpPerType` | Period Type for Report Generation | VarChar | 1 | - | M | `Y` = Year<br>`Q` = Quarter<br>`B` = Bi-Monthly<br>`M` = Month<br>`P` = Period<br>`F` = Fiscal Year<br>`G` = Fiscal Quarter |
| 48 | `DfSVatExmp` | Sales Tax Group for Exempt | nVarChar | 8 | - |  |  |
| 49 | `DfPVatExmp` | Purchases Tax Group for Exempt | nVarChar | 8 | - |  |  |
| 50 | `Manager1` | General Manager | nVarChar | 100 | - |  |  |
| 51 | `Manager1F` | General Manager (For. Lang.) | nVarChar | 100 | - |  |  |
| 52 | `CCMask` | Mask Credit Card Number | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 53 | `ObligLimit` | Commitment Restriction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `CreditLimt` | Credit Restriction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `SalesLimit` | Restrict Sales | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `DlnLimit` | Restrict Deliv. Notes (PO) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `OrderLimit` | Restrict Orders | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `AddDlnBlnc` | Consider Del. Notes in Sales Restriction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `CreditDpst` | Credit Deposit Type | VarChar | 1 | - | N | `Y` = Manually<br>`N` = Automatically |
| 60 | `MultiLang` | Multi-Language Support Enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `DbVers` | Database Version | Int | 11 | - |  |  |
| 62 | `ApplVers` | Application Version | Int | 11 | - |  |  |
| 63 | `DflWebSite` | Default for Web Site | Text | 16 | - |  |  |
| 64 | `DflFTPSite` | Default for FTP Site | Text | 16 | - |  |  |
| 65 | `UseTax` | Use Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `RevisionPo` | Split Purchase Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 67 | `Reindex` | Rebuild Indexes | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 68 | `DllPath` | Path to Validation DLL | Text | 16 | - |  |  |
| 69 | `TaxIdValid` | Tax ID Mandatory Validation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `PchName` | Alternate Name for Purchase | nVarChar | 20 | - |  |  |
| 71 | `RpcName` | Alternate Name for A/P Credit | nVarChar | 20 | - |  |  |
| 72 | `PdnName` | Alternate Name for Goods Rcpt | nVarChar | 20 | - |  |  |
| 73 | `RpdName` | Alternate Name for Goods Rtn | nVarChar | 20 | - |  |  |
| 74 | `PorName` | Alternate Name for Purchase | nVarChar | 20 | - |  |  |
| 75 | `LevelWarn` | Alert Type for Whse Inventory | VarChar | 1 | - | W | `W` = Warning Only<br>`B` = Block<br>`N` = No Message |
| 76 | `CrdCommUse` | Set Commission by Customer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `ItmCommUse` | Set Commission by Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `SlpCommUse` | Set Commission by Sales Empl. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `DfCustTerm` | Default Payment Term for Cust. | Int | 6 | - | -1 |  |
| 80 | `DfVendTerm` | Default Payment Term for Vend. | Int | 6 | - | -1 |  |
| 81 | `SaleProfit` | Calc. Gross Profit per Trans. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 82 | `CostPrcLst` | Price List for Reval. Price | Int | 6 | - | -1 |  |
| 83 | `GrossBySal` | Gross Profit After Sale | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `TreePricOn` | Display Price for Parent Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `AddVat` | Calc. Tax in Sales Quotation | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 86 | `BaseFld` | Base Field | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 87 | `ClosedQuot` | Allow Closed Sales Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 88 | `UseCode` | User Conversion Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `Code1` | CODE1 | nVarChar | 8 | - |  |  |
| 90 | `Code2` | CODE2 | nVarChar | 8 | - |  |  |
| 91 | `Code3` | CODE3 | nVarChar | 8 | - |  |  |
| 92 | `Code4` | CODE4 | nVarChar | 8 | - |  |  |
| 93 | `Color` | Company Color | Int | 6 | - | 1 | `0` = Combined<br>`1` = Classic<br>`2` = Gray<br>`3` = Violet<br>`4` = Blue<br>`5` = Green<br>`6` = Yellow<br>`7` = Orange<br>`8` = Red<br>`9` = Brown |
| 94 | `SumDec` | Totals Accuracy | Int | 6 | - | 2 |  |
| 95 | `QtyDec` | Accuracy of Quantities | Int | 6 | - | 3 |  |
| 96 | `PriceDec` | Price Accuracy | Int | 6 | - | 2 |  |
| 97 | `RateDec` | Rate Accuracy | Int | 6 | - | 4 |  |
| 98 | `PercentDec` | Percentage Rate Accuracy | Int | 6 | - | 4 |  |
| 99 | `MeasureDec` | Measuring Accuracy for Units | Int | 6 | - | 3 |  |
| 100 | `DdAutoRun` | DD Auto Run | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 101 | `DdNextDue` | DD Next Due Date | Date | 8 | - |  |  |
| 102 | `DdHour` | DD Hour | Int | 6 | - |  |  |
| 103 | `CmpnyAddrF` | Address in Foreign Language | nVarChar | 254 | - |  |  |
| 104 | `DflTaxCode` | Default Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 105 | `PrintHdrF` | Letter Header in Foreign Lang. | nVarChar | 100 | - |  |  |
| 106 | `Phone1F` | Tel. No. 1 (Foreign Language) | nVarChar | 50 | - |  |  |
| 107 | `Phone2F` | Tel. No. 2 (Foreign Language) | nVarChar | 50 | - |  |  |
| 108 | `FaxF` | Fax Number (Foreign Lang.) | nVarChar | 50 | - |  |  |
| 109 | `ManagerF` | Managing Director (For. Lang.) | nVarChar | 100 | - |  |  |
| 110 | `TimeFormat` | Time Template | VarChar | 1 | - | 0 | `0` = 24H<br>`1` = 12H |
| 111 | `CigCup` | Cig and Cup Warning | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 112 | `DateFormat` | Date Template | VarChar | 1 | - | 0 | `0` = DD/MM/YY<br>`1` = DD/MM/CCYY<br>`2` = MM/DD/YY<br>`3` = MM/DD/CCYY<br>`4` = CCYY/MM/DD<br>`5` = DD/Month/YYYY<br>`6` = YY/MM/DD |
| 113 | `DateSep` | Date Separator | VarChar | 1 | - | / |  |
| 114 | `FcNoBlnc` | Foreign Currency Checking Account | VarChar | 1 | - | B | `B` = Block<br>`D` = No Message |
| 115 | `ChangeRdr` | Changed Existing Orders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 116 | `MultiCurr` | Multi-Currency Check | VarChar | 1 | - | B | `B` = Block<br>`D` = No Message |
| 117 | `PickParDlv` | Partial Deliv. Pick and Pack | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 118 | `MaxTaxIncr` | Maximum Increase of Tax Amount | Num | 19.6 | - |  |  |
| 119 | `ISRType` | ISR Type | Int | 6 | - | 2 | `1` = ISR<br>`2` = BISR<br>`3` = ISR+<br>`4` = BISR+ |
| 120 | `MaxTaxDecr` | Maximum Decrease of Tax Amount | Num | 19.6 | - |  |  |
| 121 | `RoundRmrk` | Display Rounding Remark | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 122 | `ISRBillerI` | ISR Biller ID | nVarChar | 9 | - |  |  |
| 123 | `UpdStamp` | Update Stamp | Int | 11 | - |  |  |
| 124 | `SysCNoEdit` | Block System Currency Editing | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 125 | `RefDNoEdit` | Block Updating of Posting Date | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 126 | `DfltWhs` | Default Warehouse | nVarChar | 8 | - |  |  |
| 127 | `TaxDNoEdit` | Free | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 128 | `DfSVatItem` | Tax Definition | nVarChar | 8 | - |  |  |
| 129 | `DfSVatServ` | Tax Definition | nVarChar | 8 | - |  |  |
| 130 | `DfPVatItem` | Tax Group for Purchase Item | nVarChar | 8 | - |  |  |
| 131 | `DfPVatServ` | Tax Group for Service Purchase | nVarChar | 8 | - |  |  |
| 132 | `DoBudget` | Calculate Budget | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 133 | `CustIdNum` | Customer ID | nVarChar | 6 | - | 0 |  |
| 134 | `BgtBlock` | Block Budget | VarChar | 1 | - | N | `B` = Only Annual Alert<br>`N` = Monthly Alert Only<br>`W` = Block |
| 135 | `BgtWarning` | Budget Alert | VarChar | 1 | - | A | `A` = Annual Alert<br>`M` = Monthly Alert |
| 136 | `BdgtPORDoc` | Block Purchase Orders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 137 | `BdgtAcctng` | Block Bookkeeping | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 138 | `BdgtDflt` | Default Budget Cost Assmt Mthd | Int | 11 | - | 1 |  |
| 139 | `ContInvnt` | Perpetual Inventory Management | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 140 | `InvntSystm` | Perpetual Inventory System | VarChar | 1 | - | A | `A` = Moving Average<br>`S` = Standard<br>`F` = FIFO |
| 141 | `ApplicIFRS` | Application of IFRS | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 142 | `StartYear` | Starting in Fiscal Year | Int | 6 | - |  |  |
| 143 | `According` | Report According To | Int | 6 | - | 1 | `1`<br>`2`<br>`3` |
| 144 | `MltpBrnchs` | Enable Multiple Branches | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 145 | `EnblSrvTax` | Enable Service Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 146 | `DftRCN` | Default for Retail Chains | Int | 11 | - | -6 |  |
| 147 | `RoundVat` | Round Tax Amounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 148 | `BdgtPDNDoc` | Block Deliv. Notes for Purch. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 149 | `IRSFileNo` | File Number in Income Tax | nVarChar | 9 | - |  |  |
| 150 | `DeferrTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 151 | `DflIntrst` | Min. Default Interest Amount | Num | 19.6 | - |  |  |
| 152 | `DfltSlp` | Sales Employee | Int | 6 | - | -1 |  |
| 153 | `DflCrCard` | Default Credit Card | Int | 6 | - |  |  |
| 154 | `DflBnkCode` | Default Bank No. | nVarChar | 30 | - |  |  |
| 155 | `DflBnkAcct` | Default Bank Account | nVarChar | 50 | - |  |  |
| 156 | `DflBranch` | Default Branch | nVarChar | 50 | - |  |  |
| 157 | `UsePaSys` | Use PA System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 158 | `Serv_Usr` | Service Code | nVarChar | 20 | - |  |  |
| 159 | `Serv_Pass` | Service Password | nVarChar | 20 | - |  |  |
| 160 | `ParamPath` | Parameter Folder Path | Text | 16 | - |  |  |
| 161 | `ExcelPath` | Excel Folder Path | Text | 16 | - |  |  |
| 162 | `TaxIdNum2` | Federal Tax ID 2 | nVarChar | 32 | - |  |  |
| 163 | `TaxIdNum3` | Federal Tax ID 3 | nVarChar | 32 | - |  |  |
| 164 | `DecSep` | Decimal Separator | VarChar | 1 | - | . |  |
| 165 | `ThousSep` | Thousands Separator | VarChar | 1 | - | , |  |
| 166 | `CurOnRight` | Display Currency on the Right | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 167 | `WarnByWhs` | Alert by Warehouse | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 168 | `DflBnkAcKy` | Default Bank Account No. | Int | 11 | [DSC1](DSC1.md) |  |  |
| 169 | `PriceSys` | Price System | VarChar | 1 | - | Y | `Y` = Whse<br>`N` = Item |
| 170 | `DftPVL` | Preferred Vendor Credit | Int | 11 | - | -1 |  |
| 171 | `useDdctTrc` | WTax Deduction - Hierarchy | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 172 | `useDocWrf` | Doc. Confirmation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 173 | `BtchStatus` | Default for Batch Status | VarChar | 1 | - | 0 | `0` = Released<br>`1` = Not Accessible<br>`2` = Locked |
| 174 | `OrderBatch` | Manage Orders in Batches | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 175 | `GLMethod` | Set G/L Account By | VarChar | 1 | - | W | `W` = Warehouse<br>`C` = Item Group<br>`L` = Item Level |
| 176 | `SetSriUniq` | Set Unique Serial No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 177 | `SriUniqFld` | Unique Serial No. | VarChar | 1 | - | 3 | `0` = None<br>`2` = Mfr Serial No.<br>`3` = Serial Number<br>`4` = Lot Number |
| 178 | `MaxHistory` | Max. History | Int | 11 | - | 99 |  |
| 179 | `TaxRateDet` | Tax Rate Determination | VarChar | 1 | - | P | `P` = Posting Date<br>`D` = Document Date |
| 180 | `RefreshQty` | Refresh in Whse Qty in DI | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 181 | `StockNoBas` | Stock No. Base | VarChar | 1 | - |  |  |
| 182 | `MaxCntRows` | Allowed Max Rows in Counting | Int | 11 | - | 10000 |  |
| 183 | `CentPmtInc` | Enable Incom. Centralized Payt | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 184 | `CentPmtOut` | Enable Outg. Centralized Payt | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 185 | `ChCtrAPAct` | Change Def. Recon. A/P Accts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 186 | `ChCtrARAct` | Change Def. Recon. A/R Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 187 | `PACUsrName` | PAC User Name | nVarChar | 100 | - |  |  |
| 188 | `PACPasswrd` | PAC Password | nVarChar | 100 | - |  |  |
| 189 | `CaredType` | BP Type Code | nVarChar | 2 | - |  | `01` = 01<br>`04` = 04<br>`15` = 15<br>`71` = 71<br>`73` = 73<br>`75` = 75 |
| 190 | `PBSNumber` | PBS Number | nVarChar | 8 | - |  |  |
| 191 | `PBSGroupNo` | PBS Group Number | nVarChar | 5 | - |  |  |
| 192 | `OrgNumber` | Organization Number | nVarChar | 100 | - |  |  |
| 193 | `ActSep` | Account Segments Separator | VarChar | 1 | - | - |  |
| 194 | `DspBokpWin` | Display Bookkeeping Window | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 195 | `SHandleWT` | Withholding Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 196 | `SDfltWT` | Default Withholding Tax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 197 | `IncresGlAc` | G/L Increase Account | nVarChar | 15 | [OACT](OACT.md) |  | `Y` = Yes<br>`N` = No |
| 198 | `PHandleWT` | Withholding Tax | VarChar | 1 | - |  |  |
| 199 | `PDfltWT` | Default Withholding Tax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 200 | `ExWTLiabl` | WTax Liable Expense | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 201 | `free84` | Free84 | VarChar | 1 | - |  |  |
| 202 | `AllowPostZ` | Allow Inb. Pstng W/o a Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 203 | `PostDiffR` | Display in Red Greater Than % | Num | 19.6 | - | 5 | `5` = Variance Percentage Default Value |
| 204 | `EnableRO` | Enable Release Only Snb in Pst | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 205 | `UalLastDel` | Last Delete Date on Table OUAL | Date | 8 | - |  |  |
| 206 | `UalKeepDay` | Days for keeping data on OUAL | Int | 11 | - | 30 |  |
| 207 | `NegAmount` | Use Negative Amounts | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 208 | `EnbDocOpt` | Enable Document Optimization | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 209 | `HldCode` | Holiday Name | nVarChar | 20 | [OHLD](OHLD.md) |  |  |
| 210 | `AlphaDoc` | Use Alphanum. ID for Document | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 211 | `EDocURL2` | El. Doc. Service URL 2 | nVarChar | 254 | - |  |  |
| 212 | `EnPriceMod` | Enable Separate Price Mode | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 213 | `TaaSEnable` | Enable Tax as a Service | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 214 | `TaaSUser` | TaaS User Name | nVarChar | 50 | - |  |  |
| 215 | `OrderBlock` | Order Block | VarChar | 1 | - |  |  |
| 216 | `RoundMthd` | Rounding Method | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 217 | `AdrsFromWH` | Use Whse Address in A/P Docs | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 218 | `OrderParty` | Ordering Party | nVarChar | 30 | - |  |  |
| 219 | `CrtfcateNO` | Certificate No. | nVarChar | 20 | - |  |  |
| 220 | `ExpireDate` | Expiration Date | Date | 8 | - |  |  |
| 221 | `NINum` | National Insurance No. | nVarChar | 20 | - |  |  |
| 222 | `TaaSPass` | TaaS User Password | nVarChar | 20 | - |  |  |
| 223 | `TaaSAutURL` | TaaS oAuth URL | nVarChar | 250 | - |  |  |
| 224 | `CfwAsnMust` | CFW Assignment Mandatory [Y/N] | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 225 | `CfwInDflt` | Incoming Payment Draft CF Item | Int | 11 | - |  |  |
| 226 | `CfwOutDflt` | Outgoing Payment Dflt CFW Item | Int | 11 | - |  |  |
| 227 | `TaaSURL` | TaaS Service URL | nVarChar | 250 | - |  |  |
| 228 | `TaaSSaleAc` | TaaS Default Sales Account | nVarChar | 15 | - |  |  |
| 229 | `TaxRegime` | Tax Regime | nVarChar | 100 | - |  |  |
| 230 | `AliasName` | Alias Name | Text | 16 | - |  |  |
| 231 | `DftJPELine` | Default Line For Local Area | VarChar | 1 | - |  |  |
| 232 | `RdrConfrmd` | Confirmed Sales Order | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 233 | `PorConfrmd` | Confirmed Purchase Order | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 234 | `TaaSPurcAc` | TaaS Default Purchase Account | nVarChar | 15 | - |  |  |
| 235 | `AdvImagePr` | Extended Image Processing | VarChar | 1 | - | N | `N` = Partial<br>`O` = Without<br>`Y` = Full |
| 236 | `ChfAcc` | Chief Accountant | Int | 11 | [OHEM](OHEM.md) |  |  |
| 237 | `TaxMethod` | Taxation Method | VarChar | 1 | - |  | `0` = On Shipment<br>`1` = On Payment |
| 238 | `CEO` | CEO | Int | 11 | [OHEM](OHEM.md) |  |  |
| 239 | `WllPprDsp` | Wallpaper Display | Int | 6 | - | 1 | `1` = Centralized<br>`2` = Full Screen<br>`3` = Tile |
| 240 | `WallPaper` | Wallpaper | Text | 16 | - |  |  |
| 241 | `RndToTDec` | Round VAT to Tenths | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 242 | `SDfltITWT` | Default Income Tax WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 243 | `PDfltITWT` | Default Income Tax WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 244 | `CheckFiles` | File Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 245 | `DsplyRates` | Display Rate Table on start up | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 246 | `DfActCurr` | Default Account Currency | VarChar | 1 | - | Y | `Y` = All Currencies<br>`N` = Local Currency |
| 247 | `defTaxVend` | Deferred Tax for Vendors | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 248 | `RcrFlag` | Display Transactions Scheduled for Today | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 249 | `RclFlag` | Display Recurring Transactions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 250 | `ContactLog` | Today's Activity Alert | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 251 | `ShowNewMsg` | Open Message on Arrival | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 252 | `OpenCdt` | Open Window for Credit Reference | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 253 | `AutoVat` | Automatic VAT Row Creation In | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 254 | `ConsumeFCT` | Consumer Forecast | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 255 | `ConsumeMtd` | Consumption Method | VarChar | 1 | - | B | `B` = Backward-Forward<br>`F` = Forward-Backward |
| 256 | `DaysBack` | Days Backward | Int | 11 | - | 7 |  |
| 257 | `DaysFwrd` | Days Forward | Int | 11 | - | 7 |  |
| 258 | `IsPAPrn` | Panama Printer Connected | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 259 | `ShowNewTsk` | Open Worklist on Task Arrival | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 260 | `TaxCodeCst` | Def. Tax Code (New Customers) | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 261 | `TaxCodeVnd` | Def. Tax Code (New Vendors) | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 262 | `State` | Status | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 263 | `CharMonth` | Number of Characters in Month | Int | 11 | - |  |  |
| 264 | `free83` | Free83 | VarChar | 1 | - |  |  |
| 265 | `ScreenLock` | Screen Lock Delay | Int | 6 | - | 30 |  |
| 266 | `OpenCredit` | Open Postdated Credit Vouchers Window | VarChar | 1 | - | N | `Y` = Always<br>`N` = No<br>`D` = By Date |
| 267 | `OpenDps` | Open Postdated Checks Window | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 268 | `AltBOEPost` | Active Alternative BOE Post | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 269 | `LDiscTotal` | Calc. Row Disc. from Tot. Pr. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 270 | `Code` | Code | Int | 11 | - | 1 |  |
| 271 | `DfltDunTrm` | Default Dunning Terms | nVarChar | 25 | [ODUT](ODUT.md) |  |  |
| 272 | `Profession` | Profession | nVarChar | 50 | - |  |  |
| 273 | `AlertPolFr` | Message Check Frequency | Int | 6 | - | 5 |  |
| 274 | `DfltCDP` | Default Closing Date Procedure | Int | 6 | - | -1 |  |
| 275 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 276 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 277 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 278 | `DflBCACode` | Default Bank Charges Alloc. | nVarChar | 3 | [OBCA](OBCA.md) |  |  |
| 279 | `IgrAllCash` | Ignore All Cash Flow Relevant | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 280 | `TaxPayerRf` | Unique Taxpayer Ref. (UTR) | nVarChar | 32 | - |  |  |
| 281 | `EmployerRf` | Employer's Reference | nVarChar | 32 | - |  |  |
| 282 | `PStatAutCh` | Period Status Automatic Change | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 283 | `PStatDelay` | Period Status Change Delay | Int | 6 | - | 1 |  |
| 284 | `RepBusType` | Reporting Business Type | nVarChar | 2 | - | 2 | `Y` = Yes<br>`N` = No<br>`1` = Industrial<br>`2` = Commercial<br>`3` = Service Provider<br>`4` = Contractor<br>`9` = Other<br>`99` = Report includes more than one business |
| 285 | `RepBusOthr` | Reporting Business Type Desc. | nVarChar | 32 | - |  |  |
| 286 | `BrachNum` | Branch Number | nVarChar | 4 | - |  |  |
| 287 | `BuisnesDsc` | Business Description | nVarChar | 50 | - |  | `Y` = Yes<br>`N` = No |
| 288 | `ReptMethod` | Reporting Method | nVarChar | 2 | - | 2 | `1` = Cash<br>`2` = Cumulative<br>`3` = US Dollar Regulation |
| 289 | `AcctMethod` | Accounting Method | nVarChar | 2 | - | 2 | `1` = Unilateral<br>`2` = Double |
| 290 | `Bookpitype` | Bookkeeping Type | nVarChar | 2 | - | 2 | `1` = Manual<br>`2` = Computerized<br>`3` = Mixed |
| 291 | `ActSoftNam` | Accounting Software Name | nVarChar | 100 | - |  |  |
| 292 | `OpnClsRmrk` | Copy Opening/Closing Remarks | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 293 | `TaxRndRule` | Default Tax Rounding Rule | VarChar | 1 | - |  | `R` = Round Off<br>`C` = Round Up<br>`F` = Round Down |
| 294 | `NegTax` | Allow Neg. Tax Amt in Returns | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 295 | `ZeroLine` | Allow Zero Amt Row in JE | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 296 | `GBOpenFile` | Open GBI File After Export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 297 | `GBIntface` | GBI enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 298 | `DfltCDPV` | Default A/P Closing Date Proc. | Int | 6 | - | -1 |  |
| 299 | `OnHldPert` | Capital Goods On Hold Percent. | Num | 19.6 | - |  |  |
| 300 | `WTRndRule` | Default WTax Rounding Rule | VarChar | 1 | - |  | `R` = Round Off<br>`C` = Round Up<br>`F` = Round Down |
| 301 | `GPPrcntSrv` | Default GP % in Service Doc. | Num | 19.6 | - |  |  |
| 302 | `DspFrznBP` | Display Inactive BPs in Rpt | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 303 | `DspFrznITM` | Display Inactive Items in Rpt | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 304 | `WTAccumAmt` | Accum. Amount for WTax on AP | Num | 19.6 | - |  |  |
| 305 | `NewDPRCus` | Hide Dpm Invoice | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 306 | `ServNature` | Service Nature | VarChar | 1 | - |  | `P` = Service Provider<br>`D` = Service Distributor |
| 307 | `PickLimit` | Restrict Pick List | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 308 | `WTAccAmtAR` | Accum. Amount for WTax on AR | Num | 19.6 | - |  |  |
| 309 | `UseProdPL` | Use Production P&L Accounts | VarChar | 1 | - | N | `N` = Use Balance Sheet Only<br>`Y` = Use Balance Sheet and Profit and Loss Account |
| 310 | `QueryDec` | Calculated Query Accuracy | Int | 6 | - |  |  |
| 311 | `ExRtDefTax` | Exchange Rate on Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 312 | `BoletoPath` | Boleto Path | Text | 16 | - |  |  |
| 313 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 314 | `MMLastImpD` | Last Import File Date | Date | 8 | - |  |  |
| 315 | `CpyExhRate` | Copy Exchange Rate in Copy To | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 316 | `MapService` | Map Service | Int | 11 | [OMPS](OMPS.md) | -1 |  |
| 317 | `ODWFreq` | Open Doc. Refresh Frequency | Int | 11 | - | 30 |  |
| 318 | `GTSOutPath` | GTS Outbound Path | Text | 16 | - |  |  |
| 319 | `UseMltDims` | Use Multidimensions | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 320 | `MDStyle` | Multidimensions Display Style | VarChar | 1 | - | U | `U` = Unified<br>`S` = Separate |
| 321 | `GTSInPath` | GTS Inbound Path | Text | 16 | - |  |  |
| 322 | `GTSSep` | GTS Separator | nVarChar | 10 | - |  |  |
| 323 | `GTSDftChk` | GTS Default Checker | Int | 11 | [OHEM](OHEM.md) |  |  |
| 324 | `GTSDftPye` | GTS Default Payee | Int | 11 | [OHEM](OHEM.md) |  |  |
| 325 | `GTSMaxAmt` | GTS Max. Amount | Num | 19.6 | - |  |  |
| 326 | `RspOverAmt` | Response to Exceeding Amount | VarChar | 1 | - | B | `B` = Block<br>`S` = Split |
| 327 | `DRBlock1` | Distribution Rule: Block 1 | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 328 | `DRBlock2` | Distribution Rule: Block 2 | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 329 | `DRBlock3` | Distribution Rule: Block 3 | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 330 | `DRBlock4` | Distribution Rule: Block 4 | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 331 | `DRBlock5` | Distribution Rule: Block 5 | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 332 | `PrjBlock` | Project Block | VarChar | 1 | - | N | `N` = Without Warning<br>`B` = Block Posting |
| 333 | `SimReport` | Simulation Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 334 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 335 | `BackOrder` | Pick and Pack Back Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 336 | `HQLocation` | Headquarters Location | VarChar | 1 | - | B | `B`<br>`C` = Continent<br>`M` = Madeira<br>`A` = Azores |
| 337 | `DigCrtPath` | Digital Certificate Path | Text | 16 | - |  |  |
| 338 | `DflWTS` | Default E-Tax Web Site | Int | 6 | - | -1 |  |
| 339 | `EnbApprDI` | Enable DI Approval Process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 340 | `ChBPSerie` | Verify Non-manual BP Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 341 | `ChItmSerie` | Verify Non-manual ITM Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 342 | `ETRTaxOffi` | ETR Tax Office | Int | 11 | [OTOF](OTOF.md) | 0 |  |
| 343 | `ETRTaxPers` | ETR Tax Person Type | VarChar | 1 | - |  | `T` = VAT Payer<br>`R` = Another Person Registered for Tax<br>`S` = Person required to submit a tax declaration/return according to section 78, paragraphs 3, 4, and 9<br>`D` = Taxable person according to section 3, subsection 5, when applying a tax deduction<br>`I` = Tax agent when importing goods according to section 69 |
| 344 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 345 | `PCN874RTyp` | PCN874 Report Type | VarChar | 1 | - | 1 | `1` = Registered Business<br>`6` = Finan. Institution/Non-Profit Org. |
| 346 | `BTWDecProv` | BTW Declaration Provider | nVarChar | 3 | - | BPL | `BPL` = BPL<br>`INT` = INT |
| 347 | `BTWDcPrvID` | BTW Declaration Provider ID | nVarChar | 100 | - |  |  |
| 348 | `BTWName` | BTW Name | nVarChar | 100 | - |  |  |
| 349 | `BTWStreet` | BTW Street | nVarChar | 100 | - |  |  |
| 350 | `BTWCity` | BTW City | nVarChar | 100 | - |  |  |
| 351 | `BTWZip` | BTW ZIP Code | nVarChar | 30 | - |  |  |
| 352 | `BTWPhone` | BTW Phone Number | nVarChar | 100 | - |  |  |
| 353 | `BTWOB` | BTW OB ID | Int | 11 | - | 1 |  |
| 354 | `BTWICP` | BTW ICL ID | Int | 11 | - | 1 |  |
| 355 | `BTWOBFmt` | BTW OB Mapping Format | Int | 11 | - |  |  |
| 356 | `BTWICPFmt` | BTW ICP Mapping Format | Int | 11 | - |  |  |
| 357 | `ETRPhoneNo` | ETR Telephone Number | nVarChar | 20 | - |  |  |
| 358 | `EDTestMode` | Electronic Document Test Mode | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 359 | `EDocGenTyp` | El. Doc. Default Gen. Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later |
| 360 | `EDocRptFmt` | El. Document Report Format | Int | 11 | - |  |  |
| 361 | `EDocPass` | El. Doc. Service Password | nVarChar | 100 | - |  |  |
| 362 | `EDProcess` | Electronic Document Process | VarChar | 1 | - | I | `C` = CFD<br>`I` = CFDI |
| 363 | `PAC` | PAC | nVarChar | 20 | [OPAC](OPAC.md) | XML |  |
| 364 | `NotifAlert` | Notification by Alert | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 365 | `NotifEmail` | Notification by E-Mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 366 | `EDocUDQCat` | Electronic Document UDQ Category | Int | 11 | - |  |  |
| 367 | `EOutputPth` | Ouput Directory for Electronic Documents | Text | 16 | - |  |  |
| 368 | `EDelDocFrm` | Electronic Delivery Doc. Export Format | Int | 11 | - |  |  |
| 369 | `EDocPmnFmt` | El. Doc. Payment Format | Int | 11 | - |  |  |
| 370 | `EDocURL1` | El. Doc. Service URL 1 | nVarChar | 254 | - |  |  |
| 371 | `ETRFaxNo` | ETR Fax Number | nVarChar | 20 | - |  |  |
| 372 | `ETRMgrPhn` | ETR Manager's Phone Number | nVarChar | 20 | - |  |  |
| 373 | `EDFormat` | Electronic Document Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 374 | `AIDFormat` | Annual Invoice Decl. Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 375 | `CrtLineRFQ` | Create Online Quotation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 376 | `DflJET` | Default JE Type | nVarChar | 60 | [OJET](OJET.md) |  |  |
| 377 | `OnlyPaidIn` | Display Only Paid Reserve Inv. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 378 | `PDDEnabled` | Payments Due Date Enabled | VarChar | 1 | - | N |  |
| 379 | `MaxDays4DD` | Max. Allowed Range for Due Dte | Int | 11 | - | 0 |  |
| 380 | `AutoAddUoM` | Auto. Add UoMs to Items | VarChar | 1 | - | Y | `Y` = Enabled<br>`N` = Disabled |
| 381 | `AutoAddPkg` | Auto. Add Pkgs to Items | VarChar | 1 | - | Y | `Y` = Enabled<br>`N` = Disabled |
| 382 | `BinActivat` | Has Whse Bin Activated [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 383 | `IssuePriBy` | Issue Primarily By SnB or Bin | Int | 6 | - | 0 | `0` = Issue Primarily By Serial/Batch Numbers<br>`1` = Issue Primarily By Bin Location |
| 384 | `InstFixAst` | Enable Fixed Assets | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 385 | `DeprecCalc` | Depreciation Calculation | VarChar | 1 | - | M | `M` = Month<br>`D` = Day |
| 386 | `FixAstMod` | Fixed Asset Mode | VarChar | 1 | - | P | `P` = Production<br>`T` = Transfer |
| 387 | `SopPath` | Solution Packager Exe. Path | Text | 16 | - |  |  |
| 388 | `NewAcctDe` | New G/L Account Determination | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 389 | `ClnZeroPln` | Clean Zero Price Row in ITM1 | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 390 | `CmdDisBoth` | Display Both Related Docs. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 391 | `CnclMaxDay` | Max. No. of Days For Cancel | Int | 11 | - |  |  |
| 392 | `AttachPath` | Attachment Path | Text | 16 | - |  |  |
| 393 | `ConfigPath` | Configuration Path | Text | 16 | - |  |  |
| 394 | `WrkshtPath` | Worksheet Path | Text | 16 | - |  |  |
| 395 | `ICDifExPe1` | Single Count Variance (%) | Num | 19.6 | - | 5 | `5` = Single Counting Type - Default Variance Percentage |
| 396 | `ICDifExPe2` | Multiple Count Max. Variance (%) | Num | 19.6 | - | 5 | `5` = Multiple Counting Type - Default Max Variance Percentage |
| 397 | `ClsZoDiffR` | Close Rows Cont. Zero Diff. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 398 | `ClsNoConfi` | Close Without Confirmation | VarChar | 1 | - | N | `Y` = Enabled<br>`N` = Disabled |
| 399 | `DTWPath` | DTW Exe. Path | Text | 16 | - |  |  |
| 400 | `DfltByEml` | Default by E-Mail | VarChar | 1 | - | E | `E` = E-Mail<br>`O` = Outlook E-Mail |
| 401 | `CreditDay1` | Credit Handling Day 1 | Int | 6 | - | 1 |  |
| 402 | `INVOBPrice` | Inventory OB Price Zero | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 403 | `SplitFBSh` | Split Fix Balance Sheet [Y/N] | VarChar | 1 | - | N |  |
| 404 | `NotifyRqr` | Notify Requester | VarChar | 1 | - | N |  |
| 405 | `DeactivFA` | Deactivate Asset When End Life | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 406 | `CshDctFA` | CM for Payment Cash Discount | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 407 | `SendAlert` | Send Internal Message | VarChar | 1 | - | N |  |
| 408 | `BdgtPRQDOC` | Block Purchase Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 409 | `IsReuseNum` | Enable Document Number Reuse | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 410 | `IsReuseNFN` | Enable Nota Fiscal No. Reuse | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 411 | `SIPLReport` | Show Inactive PL in Reports | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 412 | `SIPLDoc` | Show Inactive PL in Docs | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 413 | `SIPLSeting` | Show Inactive PL in Settings | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 414 | `PriceProcM` | On Change UoM Conversion Rules | VarChar | 1 | - | U | `R` = Remove UoM Prices<br>`U` = Update UoM Prices Accordingly<br>`L` = Keep Corresponding UoM Prices Unchanged<br>`K` = Keep All UoM Prices Unchanged |
| 415 | `ChkQtyINV` | Enable Check Quantity in INV | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 416 | `EnbAdvATP` | Enable Advanced ATP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 417 | `EnblCase` | Enable Case Sensitivity | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 418 | `EnbSupplC` | Enable Supplementary Code | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 419 | `MBAOnPer` | Allow Multiple BAs for Period | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 420 | `MBAOnAP` | Block Multiple BAs for AP Doc. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 421 | `MBAOnAR` | Block Multiple BAs for AR Doc. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 422 | `ApyBsActSP` | Apply Active Special Prices | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 423 | `ApyBsActPV` | Apply Active Period and Volume | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 424 | `ApyBsActPL` | Apply Active Price Lists | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 425 | `IsUpdNstdB` | Update Non-Std Based Prices | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 426 | `SnBDfltSB` | SnB Default Eval. System SB | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 427 | `OneBOneRec` | One Batch One Receipt | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 428 | `ReptCurrcy` | R6111 Report Currency | nVarChar | 2 | - | 1 | `1` = Amounts in NIS<br>`2` = Amounts in USD |
| 429 | `ICDifExPe3` | Multiple Count Vldt. Variance (%) | Num | 19.6 | - | 5 | `5` = Multiple Counting Type - Default Individual Counter Variance Percentage |
| 430 | `INCSingToV` | Copy Single Counter to Validt. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 431 | `POrCByINC` | Posting or Create Date by INC | VarChar | 1 | - | N | `Y` = Based on Posting Date<br>`N` = Based on Creation Date |
| 432 | `EnbNegPym` | Enable Negative Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 433 | `SirenNo` | Siren Number | nVarChar | 9 | - |  |  |
| 434 | `SEPACredID` | SEPA Creditor ID | nVarChar | 35 | - |  |  |
| 435 | `InstitCode` | Institution Code | nVarChar | 2 | - |  | `10` = Secretaria da Receita Federal do Brasil<br>`20` = Banco Central do Brasil (COSIF) |
| 436 | `ECDFormat` | ECD File Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 437 | `ApyDRinPEC` | Apply DR in Period End Closing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 438 | `ApyPRinPEC` | Apply PJ in Period End Closing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 439 | `TaxPyerSta` | TAX_PAYER_STATUS | nVarChar | 2 | - |  |  |
| 440 | `MaxINVRptR` | Allowed Rows in INC Trans Rpt | Int | 11 | - | 85000 |  |
| 441 | `DftResWhs` | Default Resource Warehouse | nVarChar | 8 | - |  |  |
| 442 | `AutoResWhs` | Auto Add All Warehouses to New Resources | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 443 | `InActRpt` | Inactive Reports | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 444 | `InActMkt` | Inactive Marketing Documents | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 445 | `InActPln` | Inactive Price Lists | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 446 | `StartFrom` | Start From | VarChar | 1 | - | 1 | `1` = Today<br>`2` = Month Start<br>`3` = Month End |
| 447 | `Months` | Months | Int | 6 | - | 1 |  |
| 448 | `Days` | Days | Int | 6 | - | 0 |  |
| 449 | `JEInFATran` | Always Create JE in Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 450 | `TPLId` | UI Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 451 | `TxtSrch` | Text Search | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 452 | `ApyIBtoACT` | Apply IBAN Vldt. to Bank Acct | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 453 | `JeUnGroup` | Journal Entry Split Lines | VarChar | 1 | - | N | `N` = No Split<br>`Y` = In Preview Only<br>`S` = Split<br>`T` = Split Except Tax Lines<br>`P` = Split Except Tax Lines in Journal Entry Preview Only |
| 454 | `IgnoreAdde` | Print Document Without Addenda | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 455 | `EnterAsTab` | Use Numeric Keypad ENTER Key as TAB Key | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 456 | `MouseOnly` | Document Operation by Mouse Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 457 | `PrjMngmnt` | Enable Project Management | VarChar | 1 | - | N | `Y`<br>`N` = No |
| 458 | `ElectrDocs` | Enable Electronic Documents | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 459 | `DotAsSep` | Use Dot Key As Separator | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 460 | `DoMngMth` | Data Ownership Management Method | nVarChar | 11 | - | D | `D` = Document Only<br>`B` = Business Partner Only<br>`A` = Business Partner and Document<br>`R` = Branch |
| 461 | `AlwBPNOwn` | Allow BP Without an Owner | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 462 | `EmptyPKL` | Create an Empty Pick List | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 463 | `ExcNInvItm` | Exclude Non-Inventory Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 464 | `PayRefCalc` | Payment Reference Calculation | Int | 6 | - | 1 | `1` = Payment Reference<br>`2` = Global Structured Creditor Reference |
| 465 | `MultiSched` | Multiple scheduling on Service Call | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 466 | `CloseWipV` | Close to Parent Item WIP Variance Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 467 | `onHldLimt` | Capital Goods on Hold Limit | Num | 19.6 | - |  |  |
| 468 | `EnbApUpDoc` | Enable Updating Doc Added/Updated via Approval Process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 469 | `EnbApUpDft` | Enable Updating Draft in Status Pending/Approved | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 470 | `EnPacking` | Display Packing Drawer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 471 | `BlockZeroQ` | Block Stock Negative Quantity | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 472 | `NegStoLv` | Negative Stock: Check Level | VarChar | 1 | - | I | `C` = Company<br>`W` = Warehouse<br>`I` = Item Setting |
| 473 | `EnUpdBAPln` | Enable Update BA Plan | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 474 | `BAOpPOR` | BA Option for Purchase Orders | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning<br>`B` = Block Posting |
| 475 | `BAOpPDN` | BA Option for GRPOs | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning<br>`B` = Block Posting |
| 476 | `BAOpAcctng` | BA Option for Accounting | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning<br>`B` = Block Posting |
| 477 | `AssgnOBAAP` | Assign only valid BA for AP | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 478 | `AssngOBAAR` | Assign only valid BA for AR | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 479 | `ApyToNewBP` | Apply Change Only to New BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 480 | `PrrConfrmd` | Goods Return Request Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 481 | `RrrConfrmd` | Return Request Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 482 | `DflSeries` | Default Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 483 | `EnblLC` | Enable Live Collaboration | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 484 | `DflAcct` | Default Account | nVarChar | 210 | [OACT](OACT.md) |  |  |
| 485 | `SmtpServer` | SMTP Server | nVarChar | 100 | - |  |  |
| 486 | `SmtpPort` | SMTP Port | nVarChar | 10 | - |  |  |
| 487 | `SmtpName` | SMTP User Name | nVarChar | 100 | - |  |  |
| 488 | `SmtpPasswd` | SMTP Password | nVarChar | 254 | - |  |  |
| 489 | `SmtpEncode` | SMTP Encoding | nVarChar | 100 | [OLNG](OLNG.md) | 3 | `3` = English |
| 490 | `SmtpAuthen` | SMTP Authentication | nVarChar | 100 | - | N | `N` = No Authentication<br>`L` = Login Authentication<br>`P` = Plain Password<br>`O` = OAuth 2.0 for Microsoft 365 |
| 491 | `TlsEncryp` | TLS Encryption | VarChar | 1 | - | N |  |
| 492 | `HtmlDirect` | HTML Direction Right to Left | VarChar | 1 | - | N |  |
| 493 | `IncSubject` | Include Subject in Msg Body | VarChar | 1 | - | N |  |
| 494 | `TenLevel` | Tenant Level Configuration | VarChar | 1 | - | N |  |
| 495 | `CreditDay2` | Credit Handling Day 2 | Int | 6 | - | 15 |  |
| 496 | `CdtPrvDays` | Vouchers from Last Days | Int | 11 | - | 1 |  |
| 497 | `AuImpRates` | Import Currency Rates Automatically | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 498 | `ValidateBa` | Validate Account Balance | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning Only<br>`B` = Block Posting |
| 499 | `ManRemark` | Mandatory Remark | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 500 | `ManRmkType` | Mandatory Remark Type | VarChar | 1 | - | H | `H` = Header Only<br>`R` = Rows Only<br>`B` = Rows and Header |
| 501 | `ManRmkAlt` | Mandatory Remark Alert Type | VarChar | 1 | - | B | `W` = Warning Only<br>`B` = Block Posting |
| 502 | `TMSrcPath` | Terms and Conditions Source Path | Text | 16 | - |  |  |
| 503 | `WRSrcPath` | Warranties Policy Source Path | Text | 16 | - |  |  |
| 504 | `RTSrcPath` | Returns Policy Source Path | Text | 16 | - |  |  |
| 505 | `TermsPath` | Terms and Conditions Target Path | Text | 16 | - |  |  |
| 506 | `WarrPath` | Warranties Policy Target Path | Text | 16 | - |  |  |
| 507 | `RetPath` | Returns Policy Target Path | Text | 16 | - |  |  |
| 508 | `EDocWSFrm` | El. Doc. WS Format | Int | 11 | - |  |  |
| 509 | `DspBUoM` | Display Batch Quantities By | VarChar | 1 | - | 0 | `0` = Document Row UoM<br>`1` = Inventory UoM |
| 510 | `EDocSName` | El. Doc. Sender Name | nVarChar | 200 | - |  |  |
| 511 | `EDocSEMail` | El. Doc. Sender E-Mail | nVarChar | 200 | - |  |  |
| 512 | `CpyRulToTx` | Copy Distribution Rules to Tax Related Rows | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 513 | `BpNoLock` | Business Partner Without Lock | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 514 | `SearchUrl` | Search Engine URL | nVarChar | 254 | - | http://www.google.com/search?q={SapName} {FormName} {MessageString} site:sap.com |  |
| 515 | `ExpDocLoc` | Export To Microsoft 365 or Locally | VarChar | 1 | - | 0 |  |
| 516 | `TenantId` | Tenant ID | nVarChar | 100 | - |  |  |
| 517 | `IntegUrl` | Integration Server URL | nVarChar | 254 | - | https://b1-scp-office.cfapps.sap.hana.ondemand.com/ |  |
| 518 | `EnableMTD` | Enable Making Tax Digital | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 519 | `PublicComp` | Public Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 520 | `EnableEWB` | Enable E-Way Bills | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 521 | `TspEntry` | Default Transporter | Int | 11 | - |  |  |
| 522 | `TspLine` | Default Transportation Line | Int | 11 | - |  |  |
| 523 | `EwbGenType` | Default EWB Generate Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later |
| 524 | `VolumeLic` | Use Volume Based Licensing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 525 | `Threshold` | Threshold for Customer Accounting | Num | 19.6 | - |  |  |
| 526 | `EnAuthUpt` | Enable Authorizer Update Draft | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 527 | `DfSVatExG` | Default Tax Code for Realized Exchange Rate Diff. Gain | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 528 | `DfSVatExL` | Default Tax Code for Realized Exchange Rate Diff. Loss | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 529 | `EnUpdBpAdr` | Enable Updating BP Address ID | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 530 | `PAutoDueDt` | Definition of Due Date To | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 531 | `PDuDtMonth` | Month of Due Date To | Int | 6 | - | 1 | `1` = January<br>`2` = February<br>`3` = March<br>`4` = April<br>`5` = May<br>`6` = June<br>`7` = July<br>`8` = August<br>`9` = September<br>`10` = October<br>`11` = November<br>`12` = December |
| 532 | `DriDownBOM` | Open Item Master Data of an Item Directly with Link Arrow | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 533 | `EnExtTax` | Enable External Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 534 | `DfDateFct` | Default Valid Date Factor | Int | 11 | - | 1 |  |
| 535 | `DfDateUnit` | Default Valid Date Unit | VarChar | 1 | - | M | `M` = Months<br>`W` = Weeks<br>`D` = Days |
| 536 | `EnMutiBP` | Enable Multiple BPs | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 537 | `AddBPToEC` | Add BP to Existing Equipment Card | VarChar | 1 | - | N |  |
| 538 | `EnAutoRsz` | Auto Resize User Forms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 539 | `QRMinSize` | Minimum | Int | 11 | - | 1 |  |
| 540 | `QRMaxSize` | Maximum | Int | 11 | - | 40 |  |
| 541 | `QRScale` | Scale | Int | 11 | - | 10 |  |
| 542 | `QRExpDays` | Expiration Days | Int | 11 | - | 10 |  |
| 543 | `QRExpir` | Expiration Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 544 | `QRCorrLvl` | Correction Level | VarChar | 1 | - | M | `L` = Low<br>`M` = Medium<br>`Q` = Quartile<br>`H` = High |
| 545 | `TaxCatVer` | Version of Tax Category Code | nVarChar | 20 | - | 32.0 |  |
| 546 | `EffPriDisc` | Effective Prices Consider Both Prices Before and After Discount Groups | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 547 | `CpyBaseAtc` | Copy Attachments from Base Document to Target Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 548 | `ItmDupBCD` | Duplicate Bar Codes While Duplicating Items | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 549 | `ItmDupPRC` | Duplicate Prices While Duplicating Items | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 550 | `AllowUpdat` | Allow Update Reference and UDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 551 | `BlkNegJLin` | Block Negative Lines | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 552 | `EnARWTLnMX` | Enable Sales WTax in Rows | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 553 | `PoARPayCat` | Post Sales Payment Category WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 554 | `AplyARExhR` | Apply Sales Exchange Rate to WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 555 | `EnAPWTLnMX` | Enable Purchasing WTax in Rows | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 556 | `PoAPPayCat` | Post Purchase Payment Category WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 557 | `AplyAPExhR` | Apply Purchasing Exchange Rate to WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 558 | `DispCtInBP` | Display Inactive Contact Persons in BP Master Data | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 559 | `UseDfltPL` | Use Default Price List | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 560 | `DfltCustPL` | Default Price List for Customer | Int | 6 | - |  |  |
| 561 | `DfltVendPL` | Default Price List for Vendor | Int | 6 | - |  |  |
| 562 | `EORINumber` | EORI Number | nVarChar | 17 | - |  |  |
| 563 | `SkipRutChk` | Skip check of RUT length | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 564 | `EnbUQAudit` | Enable Execution Audit Log for User-Defined Query | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 565 | `CpyBomAtc` | Copy Attachments from BOM | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 566 | `DnOvrwrAtc` | Don't overwrite attachments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 567 | `IsTAForMIS` | Enable Creation of Tax Adjustment for Monthly Invoice | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 568 | `AutTAApprS` | Tax Adjustment Is Approved Automatically | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 569 | `QutConfrmd` | Sales Quotation Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 570 | `PqtConfrmd` | Purchase Quotation Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 571 | `ShowFstMsg` | Show Only Part of Message | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 572 | `ShowMsgNum` | The Number of Message to Show | Int | 11 | - | 100 |  |
| 573 | `OmitDisAs` | Omit Disassembly Transactions in Batches and Serials Trace Report | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 574 | `DevMode` | Enable Development Mode or not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 575 | `BlockAtt` | Block Attachments from Running | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 576 | `TaxInLine` | Tax in Line | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 577 | `WebCliRO` | Launch Web Client in Read-Only Mode | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 578 | `EnGSTRtn` | Enable GST Returns | VarChar | 1 | - | N |  |
| 579 | `DefaultRut` | Default RUT Business Partner | nVarChar | 32 | - |  |  |
| 580 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 581 | `UpdPKLUDF` | Allow Updating of User-Defined Fields When Pick List is Closed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 582 | `DfPRtgLiab` | Liable Purchase Recognized Tax Group | nVarChar | 8 | - |  |  |
| 583 | `DfPRtgExmp` | Exempt Purchase Recognized Tax Group | nVarChar | 8 | - |  |  |
| 584 | `CSPFlag` | Customized CSP Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 585 | `WCCSP` | CSP Response Header | Text | 16 | - |  |  |
| 586 | `XAPCSPFlg` | XAPP Customized CSP Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 587 | `XAPPCSP` | XAPP CSP Response Header | Text | 16 | - |  |  |
| 588 | `BookeTdsBP` | Book the eTDS to the Business Partner | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 589 | `QIEnblFrom` | Qualified Invoice Enabled From | Date | 8 | - | 20231001 |  |
| 590 | `IsTAForMIP` | Enable Creation of Tax Adjustment for Monthly Invoice | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 591 | `AutTAApprP` | Tax Adjustment Is Approved Automatically | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 592 | `NaturalPer` | Natural Person | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 593 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 594 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 595 | `EnDflBnkAt` | Encryption of Default Bank Account | Text | 16 | - |  |  |
| 596 | `EnPathVali` | Enable Path Validation | VarChar | 1 | - | Y |  |
| 597 | `PathAllows` | Path Validation Allowlist | Text | 16 | - |  |  |
| 598 | `EnQryVali` | Enable Query Validation | VarChar | 1 | - | Y |  |
| 599 | `QryAllows` | Query Validation Allowlist | Text | 16 | - |  |  |
| 600 | `AtcEntry` | File Storage Entry | Int | 11 | - |  |  |
| 601 | `TMAbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 602 | `WRAbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 603 | `RTAbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 604 | `NDTaxWOAct` | Enable Non-Deductible Tax Without Account | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 605 | `EnConnStr` | Enable Default Connection String | VarChar | 1 | - | N |  |
| 606 | `EnXmlFilt` | Enable XML Filtered | VarChar | 1 | - | Y |  |
| 607 | `TrustEntit` | Trusted Entity | Text | 16 | - |  |  |
| 608 | `XmlSizeLim` | XML Size Limit | Int | 11 | - |  |  |
| 609 | `SwLicNum` | Software License Number | nVarChar | 8 | - |  |  |
| 610 | `UniFederal` | Unified Federal Pop Up | nVarChar | 156 | - |  |  |
| 611 | `UniTaxId` | Unified Federal Tax ID | nVarChar | 32 | - |  |  |
| 612 | `RCS` | RCS No. | nVarChar | 120 | - |  |  |
| 613 | `EnQryVlDI` | Enable Query Validation for DI API | VarChar | 1 | - | Y |  |
| 614 | `QryAllowDI` | Query Validation Allowlist in DI API | Text | 16 | - |  |  |
| 615 | `ReopPR` | Enable Reopening Items in Base Purchase Request When Target Purchase Order is Canceled | VarChar | 1 | - |  |  |
| 616 | `ForceRePR` | Always Reopen Base Document Items When Purchase Order Is Canceled. No Confirmation Message. | VarChar | 1 | - |  |  |
| 617 | `EIIThrsVal` | Threshold Value for e-Invoice | Num | 19.6 | - |  |  |
| 618 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 619 | `EnDigPymnt` | Enable Digital Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 620 | `EnUsDfVl` | Enable User-Defined Values | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 621 | `SameSite` | SameSite Response Header | Text | 16 | - |  |  |
| 622 | `MaxHisTime` | Max. History Time | Int | 11 | - |  |  |
| 623 | `MaxXMPSize` | Max. XML Parser Size | Num | 19.6 | - | 2147483647 |  |
| 624 | `EmailInApr` | Enable email notification in approval process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 625 | `ApprEmMthd` | Email notification method in approval process | VarChar | 1 | - | M | `M` = Mailer<br>`O` = MS365 |
| 626 | `AdvWarnDay` | Advance Warning Day | Int | 11 | - | 2 |  |
| 627 | `RlsCardCfg` | Relationship Map Card Configuration | Text | 16 | - |  |  |
| 628 | `EnAutClLac` | Close Landed Costs After Copying | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 629 | `OauCliId` | OAuth Client ID | Text | 16 | - |  |  |
| 630 | `OauCliSec` | OAuth Client Secret | Text | 16 | - |  |  |
| 631 | `SdEmDirect` | Send Email Directly on Adding Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 632 | `EmAttType` | Email Attachment Type | VarChar | 1 | - | W | `W` = Word<br>`E` = Excel<br>`P` = PDF |
| 633 | `BlockMime` | Block Executable Attachments Based on MIME Type | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 634 | `DnDupATC` | Do Not Duplicate Attachments When Duplicating Marketing Documents | VarChar | 1 | - | N |  |
| 635 | `NaviByInt` | Navigate by Internal Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 636 | `EnWebhook` | Enable Webhook | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 637 | `MaxHookCnt` | Webhook Maximum Number per Company | Int | 11 | - | 16 |  |
| 638 | `HookMsgTTL` | Webhook Message TTL in Hours | Int | 11 | - | 24 |  |
| 639 | `RetryTimes` | Webhook Retry Times | Int | 6 | - | 3 |  |
| 640 | `RetryIntvl` | Webhook Retry Interval in Seconds | Int | 6 | - | 2 |  |
| 641 | `ReqTimeout` | Webhook Request Timeout in Seconds | Int | 6 | - | 10 |  |
| 642 | `BatchLimit` | Webhook Message Batch Limit | Int | 6 | - | 1024 |  |
| 643 | `RetentionT` | Webhook Message Retention Time in Days | Int | 6 | - | 30 |  |
| 644 | `Suffix` | Suffix | nVarChar | 20 | - |  |  |
| 645 | `RoutingCd` | Routing Code | nVarChar | 100 | - |  |  |
| 646 | `CompanyID` | Company ID | nVarChar | 8 | - |  |  |
| 647 | `RoPermMsg` | Pop up permission override for read-only forms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
