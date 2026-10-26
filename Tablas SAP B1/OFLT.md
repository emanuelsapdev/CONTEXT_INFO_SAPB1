# OFLT - Report - Selection Criteria

- **Tabla:** OFLT
- **Descripción:** Report - Selection Criteria
- **Cantidad de campos:** 293
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFLT.html

## Campos (293)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormNum` | Form Number | nVarChar | 20 | - |  |  |
| 2 | `QueryStr` | Query | nVarChar | 250 | - |  |  |
| 3 | `ItmOrCrd` | Items or BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `CardInclud` | BP Area | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `CardFrom1` | From BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `CardTo1` | To BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 7 | `CardExclud` | Excluding BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `CardFrom2` | BP Rejected | nVarChar | 15 | - |  |  |
| 9 | `CardTo2` | BP Rejected | nVarChar | 15 | - |  |  |
| 10 | `ClienGroup` | Customer Group | Int | 6 | - |  |  |
| 11 | `VendGroup` | Vendor Group | Int | 6 | - |  |  |
| 12 | `ClntQryGrp` | Customer Properties | nVarChar | 250 | - |  |  |
| 13 | `VeQryGroup` | Vendor Properties | nVarChar | 250 | - |  |  |
| 14 | `ItmInclud` | Item Range | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `ItmFrom1` | From Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 16 | `ItmTo1` | To Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 17 | `ItmExclud` | Excluding Materials | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `ItmFrom2` | Item Rejected | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 19 | `ItmTo2` | Item Rejected | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 20 | `ItmGroup` | Item Group | Int | 6 | [OITB](OITB.md) |  |  |
| 21 | `ItQryGroup` | Item Properties | nVarChar | 250 | - |  |  |
| 22 | `WhsInclude` | Warehouse Range | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 23 | `WhsFrom1` | From Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 24 | `WhsTo1` | To Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 25 | `WhsExclude` | Excluding Warehouses | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `WhsFrom2` | Warehouse Rejected | nVarChar | 8 | - |  |  |
| 27 | `WhsTo2` | Warehouse Rejected | nVarChar | 8 | - |  |  |
| 28 | `FromAcct` | From Account | nVarChar | 15 | - |  |  |
| 29 | `ToAcct` | To Account | nVarChar | 15 | - |  |  |
| 30 | `GroupMask` | Group Mask | nVarChar | 12 | - |  |  |
| 31 | `FromDate` | From Posting Date | Date | 8 | - |  |  |
| 32 | `ToDate` | To Posting Date | Date | 8 | - |  |  |
| 33 | `FrmDueDate` | Due Date From | Date | 8 | - |  |  |
| 34 | `ToDueDate` | Due Date To | Date | 8 | - |  |  |
| 35 | `FromDate3` | From Date 3 | Date | 8 | - |  |  |
| 36 | `ToDate3` | To Date 3 | Date | 8 | - |  |  |
| 37 | `FromDate4` | From Date 4 | Date | 8 | - |  |  |
| 38 | `ToDate4` | To Date 4 | Date | 8 | - |  |  |
| 39 | `SourceType` | Original Journal | Int | 6 | - | -1 | `15` = Delivery<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt<br>`21` = Goods Returns<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Vendor Payment<br>`57` = Checks for Payment<br>`76` = Postdated Deposit<br>`-2` = Opening Balance<br>`-3` = Closing Balance<br>`30` = Journal Entry<br>`58` = Stock Update<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfers<br>`68` = Work Instructions<br>`162` = Inventory Valuation<br>`-1` = All Transactions |
| 40 | `FrmTrnsNum` | From Transaction No. | Int | 11 | - |  |  |
| 41 | `ToTrnsNum` | To Transaction No. | Int | 11 | - |  |  |
| 42 | `FromRef1` | From Reference 1 | nVarChar | 100 | - |  |  |
| 43 | `ToRef1` | To Reference 1 | nVarChar | 100 | - |  |  |
| 44 | `FromRef2` | From Reference 2 | nVarChar | 100 | - |  |  |
| 45 | `ToRef2` | To Reference 2 | nVarChar | 100 | - |  |  |
| 46 | `FrmTrnsCod` | From Transaction Code | nVarChar | 4 | - |  |  |
| 47 | `ToTrnsCod` | To Transaction Code | nVarChar | 4 | - |  |  |
| 48 | `FromSum` | From Amount | Num | 19.6 | - |  |  |
| 49 | `ToSum` | To Amount | Num | 19.6 | - |  |  |
| 50 | `FrmFRNAmnt` | From FC Amount | Num | 19.6 | - |  |  |
| 51 | `ToFRNAmnt` | To FC Amount | Num | 19.6 | - |  |  |
| 52 | `MemoIn` | Details Contained | nVarChar | 50 | - |  |  |
| 53 | `SortField1` | Sort Field 1 | Int | 6 | - | -1 |  |
| 54 | `Break1` | Subtotal by Sort 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `SortField2` | Sort Field 2 | Int | 6 | - | -1 |  |
| 56 | `Break2` | Subtotal by Sort 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `SortField3` | Sort Field 3 | Int | 6 | - | -1 |  |
| 58 | `Break3` | Subtotal by Sort 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `Display` | Display | VarChar | 1 | - | L | `L` = Postings Only<br>`T` = Totals Only<br>`B` = Postings + Totals |
| 60 | `PrntCutDat` | Print Date Selection Criteria | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 61 | `CheckBox0` | Check box 0 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `CheckBox1` | Check box 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `CheckBox2` | Check box 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `CheckBox3` | Check box 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 65 | `CheckBox4` | Check box 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `CheckBox5` | Check box 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 67 | `CheckBox6` | Check box 6 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 68 | `CheckBox7` | Check box 7 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 69 | `CheckBox8` | Check box 8 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `CheckBox9` | Check box 9 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 71 | `ShowZero` | Display Zero Balances | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 72 | `DateCheck` | Confirm Date Range | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `DueCheck` | Confirm Due Date Range | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `CutCheck` | Confirm Date Selectn Criteria | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `CutByObj` | Selection Criteria by Object | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `ObjectC1` | C1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `ObjectC2` | C2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `ObjectC3` | C3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `ObjectC4` | C4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 80 | `ObjectC5` | C5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `ObjectC6` | C6 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 82 | `ObjectC7` | C7 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 83 | `ObjectC8` | C8 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `ObjectC9` | C9 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `ObjectC10` | C10 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 86 | `ObjectC11` | C11 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 87 | `ObjectC12` | C12 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 88 | `ObjectC13` | C13 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `ObjectC14` | C14 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `ObjectC15` | C15 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 91 | `ObjectC16` | C16 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 92 | `FromAmount` | From Amount | Num | 19.6 | - |  |  |
| 93 | `ToAmount` | To Amount | Num | 19.6 | - |  |  |
| 94 | `FrmSalsMan` | From Sales Employee | Int | 11 | - |  |  |
| 95 | `ToSalsMan` | To Sales Employee | Int | 11 | - |  |  |
| 96 | `USER_CHK1` | User CheckBox 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 97 | `USER_CHK2` | User CheckBox 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 98 | `USER_CHK3` | User CheckBox 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 99 | `USER_CHK4` | System Currrency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 100 | `USER_CHK5` | System and Local Currency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 101 | `UseSort` | Sort | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 102 | `Sort1Up` | Sort1 | VarChar | 1 | - | Y | `Y` = Ascending<br>`N` = Descending |
| 103 | `Sort2Up` | Sort2 | VarChar | 1 | - | Y | `Y` = Ascending<br>`N` = Descending |
| 104 | `Sort3Up` | Sort3 | VarChar | 1 | - | Y | `Y` = Ascending<br>`N` = Descending |
| 105 | `FromAmnt2` | From Quantity Release | Num | 19.6 | - |  |  |
| 106 | `ToAmount2` | For Quantity Release | Num | 19.6 | - |  |  |
| 107 | `TaxDateFro` | Lower Limit for Tax Data | Date | 8 | - |  |  |
| 108 | `TaxDateTo` | Top Limit for Document Dates | Date | 8 | - |  |  |
| 109 | `FinancYear` | Start of Fiscal Year | Date | 8 | - |  |  |
| 110 | `BdgtScenar` | Budget Scenario | Int | 11 | - |  |  |
| 111 | `CompFolder` | Company Database | nVarChar | 200 | - |  |  |
| 112 | `CheckBox10` | Exapan Check Box 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `FROM_FC` | Foreign Currency from | Num | 19.6 | - |  |  |
| 114 | `TO_FC` | Foreign Currency to | Num | 19.6 | - |  |  |
| 115 | `FCCurrency` | Foreign Currency | nVarChar | 3 | - |  |  |
| 116 | `TaxCheck` | Confirm Document Date Range | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `DateType` | Selection Criteria Type | VarChar | 1 | - | R | `R` = Posting Date<br>`D` = Due Date<br>`T` = Document Date |
| 118 | `DateType2` | Selection Criteria Type | VarChar | 1 | - | R | `R` = Posting Date<br>`D` = Due Date<br>`T` = Document Date |
| 119 | `FromPrject` | From Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 120 | `ToProject` | To Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 121 | `TemplateId` | Template | Int | 11 | - | 0 |  |
| 122 | `ShowLeads` | Display Leads | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `MthDate` | Reconciliation Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `AccntntCod` | External Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 125 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 126 | `BlcNunFrom` | Block Number From | nVarChar | 100 | - |  |  |
| 127 | `BlcNunTo` | Block Number To | nVarChar | 100 | - |  |  |
| 128 | `ImpLogFrom` | Import Log From | nVarChar | 20 | - |  |  |
| 129 | `ImpLogTo` | Import Log To | nVarChar | 20 | - |  |  |
| 130 | `FolderNum` | Folder Number | VarChar | 1 | - | 1 |  |
| 131 | `MainField` | Main Field | Int | 6 | - | 23 |  |
| 132 | `TransMode` | Transaction Mode | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 133 | `MonthMode` | Month Totals Mode | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 134 | `CheckBox11` | Expan Check Box 11 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 135 | `FromIdc` | Indicator From | nVarChar | 2 | - |  |  |
| 136 | `ToIdc` | Indicator To | nVarChar | 2 | - |  |  |
| 137 | `IgnoreAdj` | Ignore Adjustments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 138 | `RefNumFrom` | From Reference No. | nVarChar | 254 | - |  |  |
| 139 | `RefNumTo` | To Reference No. | nVarChar | 254 | - |  |  |
| 140 | `PymNumfrom` | Payment No. From | Int | 11 | - |  |  |
| 141 | `PymNumTo` | To Payment No. | Int | 11 | - |  |  |
| 142 | `BankFrom` | From Bank Code | nVarChar | 30 | - |  |  |
| 143 | `BankTo` | To Bank Code | nVarChar | 30 | - |  |  |
| 144 | `DpstFrom` | From Deposit Code | Int | 11 | - |  |  |
| 145 | `DpstTo` | To Deposit Code | Int | 11 | - |  |  |
| 146 | `DpstType` | Deposit Type | VarChar | 1 | - |  |  |
| 147 | `ObjectC17` | Obj C17 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 148 | `ObjectC18` | Obj C18 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 149 | `ObjectC19` | Obj C19 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 150 | `ObjAbs` | Document Internal Number | Int | 11 | - |  |  |
| 151 | `AddBTF` | Add Journal Vouchers | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 152 | `FilePath` | File Path | Text | 16 | - |  |  |
| 153 | `DpsBnkActF` | From Deposit Bank Account | nVarChar | 50 | - |  |  |
| 154 | `DpsBnkActT` | To Deposit Bank Account | nVarChar | 50 | - |  |  |
| 155 | `FromKey` | From Key | Int | 11 | - |  |  |
| 156 | `ToKey` | To Key | Int | 11 | - |  |  |
| 157 | `ObjectC20` | Object C20 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 158 | `ObjectC21` | Object C21 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 159 | `ObjectC22` | Object C22 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 160 | `ObjectC23` | Object C23 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 161 | `ObjectC25` | Object C25 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 162 | `USER_CHK6` | Include CB in P/L Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 163 | `OcrChkDim2` | Checkbox for Dimension 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 164 | `OcrChkDim3` | Checkbox for Dimension 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 165 | `OcrChkDim4` | Checkbox for Dimension 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 166 | `OcrChkDim5` | Checkbox for Dimension 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 167 | `OcrFrom2` | From Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 168 | `OcrFrom3` | From Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 169 | `OcrFrom4` | From Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 170 | `OcrFrom5` | From Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 171 | `OcrTo2` | To Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 172 | `OcrTo3` | To Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 173 | `OcrTo4` | To Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 174 | `OcrTo5` | To Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 175 | `TaxAdjRep` | Object C24 | Text | 16 | - |  |  |
| 176 | `ObjectC26` | Object C26 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 177 | `CBFilter` | Closing Balances Filter | VarChar | 1 | - | 2 | `1` = Closing Balance of Life-to-Date<br>`2` = Closing Balance Before Selected Period Only |
| 178 | `OBIncluded` | Add Opening Balance for Period | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 179 | `OBFilter` | Opening Balances Filter | VarChar | 1 | - | 1 | `1` = Opening Balance from Start of Company Activity<br>`2` = Opening Balance from Start of Fiscal Year |
| 180 | `ExportCurr` | Export Currency | VarChar | 1 | - | L | `L` = Local Currency<br>`S` = System Currency |
| 181 | `CBIncluded` | Add Closing Balances | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 182 | `SlpFrom` | Slp From | nVarChar | 155 | - |  |  |
| 183 | `SlpTo` | Slp To | nVarChar | 155 | - |  |  |
| 184 | `CBUDF` | User-Defined Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 185 | `CBREF` | Reference Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 186 | `CheckBoxB` | Checkbox for Branch | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 187 | `FilterName` | Filter Name | nVarChar | 30 | - | _ |  |
| 188 | `JDTFixedF` | JE Fixed Fields | Int | 6 | - |  |  |
| 189 | `JDT1FixedF` | JE Line Fixed Fields | Int | 6 | - |  |  |
| 190 | `JDTUserF` | JE User Fields | Int | 6 | - |  |  |
| 191 | `JDT1UserF` | JE Line User Fields | Int | 6 | - |  |  |
| 192 | `BPFilter` | BP Filter Enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 193 | `AcctFltr` | Account Filter Enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 194 | `ZeroLCAmt` | Show Zero LC Amount Lines | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 195 | `SplitByBin` | Split By Bin Location | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 196 | `SplitBySnb` | Split By Batch/Serial | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 197 | `CheckBox12` | Check Box 12 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 198 | `CheckBox13` | Check Box 13 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 199 | `CheckBox14` | Check Box 14 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 200 | `CheckBox15` | Check Box 15 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 201 | `CheckBox16` | Check Box 16 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 202 | `CheckBox17` | Check Box 17 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 203 | `CheckBox18` | Check Box 18 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 204 | `CheckBox19` | Check Box 19 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 205 | `CheckBox20` | Check Box 20 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 206 | `CheckBox21` | Check Box 21 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 207 | `CheckBox22` | Check Box 22 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 208 | `CheckBox23` | Check Box 23 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 209 | `CheckBox24` | Check Box 24 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 210 | `CheckBox25` | Check Box 25 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 211 | `CheckBox26` | Check Box 26 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 212 | `CheckBox27` | Check Box 27 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 213 | `CheckBox28` | Check Box 28 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 214 | `CheckBox29` | Check Box 29 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 215 | `CheckBox30` | Check Box 30 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 216 | `CheckBox31` | Check Box 31 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 217 | `CheckBox32` | Check Box 32 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 218 | `CheckBox33` | Check Box 33 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 219 | `BatchFrom` | Batch From | nVarChar | 36 | - |  |  |
| 220 | `BatchTo` | Batch To | nVarChar | 36 | - |  |  |
| 221 | `BatAttr1F` | Batch Attr. 1 From | nVarChar | 36 | - |  |  |
| 222 | `BatAttr1T` | Batch Attr. 1 To | nVarChar | 36 | - |  |  |
| 223 | `BatAttr2F` | Batch Attr. 2 From | nVarChar | 36 | - |  |  |
| 224 | `BatAttr2T` | Batch Attr. 2 To | nVarChar | 36 | - |  |  |
| 225 | `SerialNoF` | Serial Number From | nVarChar | 36 | - |  |  |
| 226 | `SerialNoT` | Serial Number To | nVarChar | 36 | - |  |  |
| 227 | `MfrSerailF` | Mfr Serial Number From | nVarChar | 36 | - |  |  |
| 228 | `MfrSerailT` | Mfr Serial Number To | nVarChar | 36 | - |  |  |
| 229 | `LotNumberF` | Lot Number From | nVarChar | 36 | - |  |  |
| 230 | `LotNumberT` | Lot Number To | nVarChar | 36 | - |  |  |
| 231 | `BinLocFrom` | Bin Location From | nVarChar | 228 | - |  |  |
| 232 | `BinLocTo` | Bin Location To | nVarChar | 228 | - |  |  |
| 233 | `AltSrtCodF` | Alternative Sort Code From | nVarChar | 50 | - |  |  |
| 234 | `AltSrtCodT` | Alternative Sort Code To | nVarChar | 50 | - |  |  |
| 235 | `BinSbl1F` | Bin Sublevel 1 From | nVarChar | 50 | - |  |  |
| 236 | `BinSbl1To` | Bin Sublevel 1 To | nVarChar | 50 | - |  |  |
| 237 | `BinSbl2F` | Bin Sublevel 2 From | nVarChar | 50 | - |  |  |
| 238 | `BinSbl2To` | Bin Sublevel 2 To | nVarChar | 50 | - |  |  |
| 239 | `BinSbl3F` | Bin Sublevel 3 From | nVarChar | 50 | - |  |  |
| 240 | `BinSbl3To` | Bin Sublevel 3 To | nVarChar | 50 | - |  |  |
| 241 | `BinSbl4F` | Bin Sublevel 4 From | nVarChar | 50 | - |  |  |
| 242 | `BinSbl4To` | Bin Sublevel 4 To | nVarChar | 50 | - |  |  |
| 243 | `BinAttr1F` | Bin Attribute 1 From | nVarChar | 20 | - |  |  |
| 244 | `BinAttr1To` | Bin Attribute 1 To | nVarChar | 20 | - |  |  |
| 245 | `BinAttr2F` | Bin Attribute 2 From | nVarChar | 20 | - |  |  |
| 246 | `BinAttr2To` | Bin Attribute 2 To | nVarChar | 20 | - |  |  |
| 247 | `BinAttr3F` | Bin Attribute 3 From | nVarChar | 20 | - |  |  |
| 248 | `BinAttr3To` | Bin Attribute 3 To | nVarChar | 20 | - |  |  |
| 249 | `BinAttr4F` | Bin Attribute 4 From | nVarChar | 20 | - |  |  |
| 250 | `BinAttr4To` | Bin Attribute 4 To | nVarChar | 20 | - |  |  |
| 251 | `BinAttr5F` | Bin Attribute 5 From | nVarChar | 20 | - |  |  |
| 252 | `BinAttr5To` | Bin Attribute 5 To | nVarChar | 20 | - |  |  |
| 253 | `BinAttr6F` | Bin Attribute 6 From | nVarChar | 20 | - |  |  |
| 254 | `BinAttr6To` | Bin Attribute 6 To | nVarChar | 20 | - |  |  |
| 255 | `BinAttr7F` | Bin Attribute 7 From | nVarChar | 20 | - |  |  |
| 256 | `BinAttr7To` | Bin Attribute 7 To | nVarChar | 20 | - |  |  |
| 257 | `BinAttr8F` | Bin Attribute 8 From | nVarChar | 20 | - |  |  |
| 258 | `BinAttr8To` | Bin Attribute 8 To | nVarChar | 20 | - |  |  |
| 259 | `BinAttr9F` | Bin Attribute 9 From | nVarChar | 20 | - |  |  |
| 260 | `BinAttr9To` | Bin Attribute 9 To | nVarChar | 20 | - |  |  |
| 261 | `BinAttr10F` | Bin Attribute 10 From | nVarChar | 20 | - |  |  |
| 262 | `BinAttr10T` | Bin Attribute 10 To | nVarChar | 20 | - |  |  |
| 263 | `EnfBinFltr` | Enforced Bin Filter | VarChar | 1 | - | N | `E` = Enforced Bin Location<br>`U` = Unenforced Bin Location<br>`B` = Both<br>`N` = Bin not activated |
| 264 | `ExItemFrom` | Expand from Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 265 | `ExItemTo` | Expand to Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 266 | `ExBPFrom` | Expand from BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 267 | `ExBPTo` | Expand to BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 268 | `CheckBox34` | Check Box 34 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 269 | `CheckBox35` | Check Box 35 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 270 | `BlAgreem` | Checkbox for Blanket Agreement | VarChar | 1 | - | N |  |
| 271 | `BAFrom` | Blanket Agreement From | nVarChar | 8 | - |  |  |
| 272 | `BATo` | Blanket Agreement To | nVarChar | 8 | - |  |  |
| 273 | `AdjTrans` | Adjustment Transactions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 274 | `TitAcctLvl` | Title Account Level | Int | 11 | - | 2 |  |
| 275 | `CCDFrom1` | CCD Number from condition 1 | nVarChar | 40 | - |  |  |
| 276 | `CCDTo1` | CCD Number to Condition 1 | nVarChar | 40 | - |  |  |
| 277 | `CCDFrom2` | CCD Number from Condition 2 | nVarChar | 40 | - |  |  |
| 278 | `CCDTo2` | CCD Number to Condition 2 | nVarChar | 40 | - |  |  |
| 279 | `ArchJrnal` | Archiving Journal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 280 | `CardFrom3` | From BP | nVarChar | 15 | - |  |  |
| 281 | `CardTo3` | To BP | nVarChar | 15 | - |  |  |
| 282 | `OBBranch` | Divide Totals by Branch | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 283 | `AccumDbCr` | Accumulated Debit/Credit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 284 | `RscFrom1` | From Resource | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 285 | `RscTo1` | To Resource | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 286 | `RscGroup` | Resource Group | Int | 6 | [ORSB](ORSB.md) |  |  |
| 287 | `RouteStage` | Use Route Stage | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 288 | `ExRSTFrom` | From Route Stage | Int | 11 | [ORST](ORST.md) |  |  |
| 289 | `ExRSTTo` | To Route Stage | Int | 11 | [ORST](ORST.md) |  |  |
| 290 | `StgSeqNum` | Use Stage Sequence Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 291 | `ExSSNFrom` | From Stage Sequence Number | Int | 11 | - |  |  |
| 292 | `ExSSNTo` | To Stage Sequence Number | Int | 11 | - |  |  |
| 293 | `IsPostDate` | Posting date is used | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormNum, UserSign, FilterName |
