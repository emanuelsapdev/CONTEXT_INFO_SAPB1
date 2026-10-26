# PDN1 - Goods Receipt PO - Rows

- **Tabla:** PDN1
- **Descripción:** Goods Receipt PO - Rows
- **Cantidad de campos:** 343
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PDN1.html

## Campos (343)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OPDN](OPDN.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `TargetType` | Target Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`21` = Goods Return<br>`18` = A/P Invoice<br>`204` = A/P Down Payment<br>`234000032` = A/P Return Request |
| 4 | `TrgetEntry` | Target Document Internal ID | Int | 11 | - |  |  |
| 5 | `BaseRef` | Base Document Reference | nVarChar | 16 | - |  |  |
| 6 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`22` = Purchase Orders<br>`21` = Goods Return<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`540000006` = Purchase Quotation<br>`20` = Goods Receipt PO |
| 7 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 8 | `BaseLine` | Base Row | Int | 11 | - |  |  |
| 9 | `LineStatus` | Row Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 10 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 11 | `Dscription` | Item/Service Description | nVarChar | 200 | - |  |  |
| 12 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 13 | `ShipDate` | Row Delivery Date | Date | 8 | - |  |  |
| 14 | `OpenQty` | Remaining Open Quantity | Num | 19.6 | - |  |  |
| 15 | `Price` | Price | Num | 19.6 | - |  |  |
| 16 | `Currency` | Price Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 17 | `Rate` | Currency Rate | Num | 19.6 | - |  |  |
| 18 | `DiscPrcnt` | Discount % per Row | Num | 19.6 | - |  |  |
| 19 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 20 | `TotalFrgn` | Row Total (FC) | Num | 19.6 | - |  |  |
| 21 | `OpenSum` | Open Amount | Num | 19.6 | - |  |  |
| 22 | `OpenSumFC` | Open Amount (FC) | Num | 19.6 | - |  |  |
| 23 | `VendorNum` | Vendor Catalog No. | nVarChar | 50 | - |  |  |
| 24 | `SerialNum` | Serial Number | nVarChar | 17 | - |  |  |
| 25 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 26 | `SlpCode` | Sales Employee Code | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 27 | `Commission` | Commission Percentage | Num | 19.6 | - |  |  |
| 28 | `TreeType` | BOM Type | VarChar | 1 | - | N | `N` = Not a BOM<br>`A` = Assembly<br>`S` = Sales<br>`I` = Sales BOM Component<br>`P` = Production<br>`T` = Template |
| 29 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 30 | `TaxStatus` | Tax Definition | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 31 | `GrossBuyPr` | Gross Profit Base Price | Num | 19.6 | - |  |  |
| 32 | `PriceBefDi` | Unit Price | Num | 19.6 | - |  |  |
| 33 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 34 | `Flags` | Flags | Int | 11 | - | 0 |  |
| 35 | `OpenCreQty` | Credit Memo Amount | Num | 19.6 | - |  |  |
| 36 | `UseBaseUn` | Inventory UoM | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `SubCatNum` | BP Catalog No. | nVarChar | 50 | [OSCN](OSCN.md) |  |  |
| 38 | `BaseCard` | Base BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 39 | `TotalSumSy` | Row Total (SC) | Num | 19.6 | - |  |  |
| 40 | `OpenSumSys` | Open Amount (SC) | Num | 19.6 | - |  |  |
| 41 | `InvntSttus` | Warehouse Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 42 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 43 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 44 | `CodeBars` | Bar Code | nVarChar | 254 | - |  |  |
| 45 | `VatPrcnt` | Tax Rate per Row | Num | 19.6 | - |  |  |
| 46 | `VatGroup` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 47 | `PriceAfVAT` | Gross Price after Discount | Num | 19.6 | - |  |  |
| 48 | `Height1` | Height 1 | Num | 19.6 | - |  |  |
| 49 | `Hght1Unit` | Unit of Height 1 | Int | 6 | - |  |  |
| 50 | `Height2` | Height 2 | Num | 19.6 | - |  |  |
| 51 | `Hght2Unit` | Unit of Height 2 | Int | 6 | - |  |  |
| 52 | `Width1` | Width 1 | Num | 19.6 | - |  |  |
| 53 | `Wdth1Unit` | Unit of Width 1 | Int | 6 | - |  |  |
| 54 | `Width2` | Width 2 | Num | 19.6 | - |  |  |
| 55 | `Wdth2Unit` | Unit of Width 2 | Int | 6 | - |  |  |
| 56 | `Length1` | Length 1 | Num | 19.6 | - |  |  |
| 57 | `Len1Unit` | Unit of Length 1 | Int | 6 | - |  |  |
| 58 | `length2` | Length 2 | Num | 19.6 | - |  |  |
| 59 | `Len2Unit` | Unit of Length 2 | Int | 6 | - |  |  |
| 60 | `Volume` | Quantity | Num | 19.6 | - |  |  |
| 61 | `VolUnit` | Vol. Unit | Int | 6 | - |  |  |
| 62 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 63 | `Wght1Unit` | Unit of Weight 1 | Int | 6 | - |  |  |
| 64 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 65 | `Wght2Unit` | Unit of Weight 2 | Int | 6 | - |  |  |
| 66 | `Factor1` | Factor 1 | Num | 19.6 | - |  |  |
| 67 | `Factor2` | Factor 2 | Num | 19.6 | - |  |  |
| 68 | `Factor3` | Factor 3 | Num | 19.6 | - |  |  |
| 69 | `Factor4` | Factor 4 | Num | 19.6 | - |  |  |
| 70 | `PackQty` | Packing Quantity | Num | 19.6 | - |  |  |
| 71 | `UpdInvntry` | Whse Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 72 | `BaseDocNum` | Base Document No. | Int | 11 | - |  |  |
| 73 | `BaseAtCard` | Customer/Vendor Base Document | nVarChar | 200 | - |  |  |
| 74 | `SWW` | Additional Identifier | nVarChar | 16 | - |  |  |
| 75 | `VatSum` | Total Tax | Num | 19.6 | - |  |  |
| 76 | `VatSumFrgn` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 77 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 78 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 79 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 20 |  |
| 80 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 81 | `BlockNum` | Block Number | nVarChar | 100 | - |  |  |
| 82 | `ImportLog` | Import Log | nVarChar | 20 | - |  |  |
| 83 | `DedVatSum` | Deductible Tax Amount | Num | 19.6 | - |  |  |
| 84 | `DedVatSumF` | Deductible Tax Amount (FC) | Num | 19.6 | - |  |  |
| 85 | `DedVatSumS` | Deductible Tax Amount (SC) | Num | 19.6 | - |  |  |
| 86 | `IsAqcuistn` | Acquisition Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 87 | `DistribSum` | Distributed Amount | Num | 19.6 | - |  |  |
| 88 | `DstrbSumFC` | Distributed Amount (FC) | Num | 19.6 | - |  |  |
| 89 | `DstrbSumSC` | Distributed Amount (SC) | Num | 19.6 | - |  |  |
| 90 | `GrssProfit` | Row Gross Profit | Num | 19.6 | - |  |  |
| 91 | `GrssProfSC` | Row Gross Profit (SC) | Num | 19.6 | - |  |  |
| 92 | `GrssProfFC` | Row Gross Profit (FC) | Num | 19.6 | - |  |  |
| 93 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 94 | `INMPrice` | Item's Last Sales Price (OINM) | Num | 19.6 | - |  |  |
| 95 | `PoTrgNum` | PO Target No. | Int | 11 | - |  |  |
| 96 | `PoTrgEntry` | PO Target Internal ID | nVarChar | 11 | - |  |  |
| 97 | `DropShip` | Drop-Ship | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 98 | `PoLineNum` | PO Target Row No. | Int | 11 | - |  |  |
| 99 | `Address` | Address | nVarChar | 254 | - |  |  |
| 100 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 101 | `TaxType` | Tax Type | VarChar | 1 | - |  | `Y` = Regular Tax<br>`N` = No Tax<br>`U` = Use Tax |
| 102 | `OrigItem` | Original Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 103 | `BackOrdr` | Allow Backorder | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 104 | `FreeTxt` | Free Text | nVarChar | 100 | - |  |  |
| 105 | `PickStatus` | Pick Status | VarChar | 1 | - | N | `Y` = Picked<br>`N` = Not Picked<br>`R` = Released for Picking<br>`P` = Partially Picked |
| 106 | `PickOty` | Pick Quantity | Num | 19.6 | - |  |  |
| 107 | `PickIdNo` | Pick ID | Int | 11 | - |  |  |
| 108 | `TrnsCode` | Shipping Method | Int | 6 | [OSHP](OSHP.md) | -1 |  |
| 109 | `VatAppld` | Applied Tax | Num | 19.6 | - |  |  |
| 110 | `VatAppldFC` | Applied Tax (FC) | Num | 19.6 | - |  |  |
| 111 | `VatAppldSC` | Applied Tax (SC) | Num | 19.6 | - |  |  |
| 112 | `BaseQty` | Base Quantity | Num | 19.6 | - |  |  |
| 113 | `BaseOpnQty` | Base Open Quantity | Num | 19.6 | - |  |  |
| 114 | `VatDscntPr` | Tax Discount % | Num | 19.6 | - |  |  |
| 115 | `WtLiable` | WTax Liable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 116 | `DeferrTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `EquVatPer` | Equalization Tax % | Num | 19.6 | - |  |  |
| 118 | `EquVatSum` | Total Equalization Tax | Num | 19.6 | - |  |  |
| 119 | `EquVatSumF` | Total Equalization Tax (FC) | Num | 19.6 | - |  |  |
| 120 | `EquVatSumS` | Total Equalization Tax (SC) | Num | 19.6 | - |  |  |
| 121 | `LineVat` | Net Tax Amount | Num | 19.6 | - |  |  |
| 122 | `LineVatlF` | Net Tax Amount | Num | 19.6 | - |  |  |
| 123 | `LineVatS` | Net Tax Amount | Num | 19.6 | - |  |  |
| 124 | `unitMsr` | Unit | nVarChar | 100 | - |  |  |
| 125 | `NumPerMsr` | UoM Value | Num | 19.6 | - |  |  |
| 126 | `CEECFlag` | Correction Invoice Was/Should Be | VarChar | 1 | - | S | `W` = Was<br>`S` = Should Be |
| 127 | `ToStock` | Corr. Invoice Amt to Inventory | Num | 19.6 | - |  |  |
| 128 | `ToDiff` | Corr. Invoice Amount to Diff. | Num | 19.6 | - |  |  |
| 129 | `ExciseAmt` | Excise Amount | Num | 19.6 | - |  |  |
| 130 | `TaxPerUnit` | Tax per Unit | Num | 19.6 | - |  |  |
| 131 | `TotInclTax` | Total Including Tax | Num | 19.6 | - |  |  |
| 132 | `CountryOrg` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 133 | `StckDstSum` | Stock Distribution Sum | Num | 19.6 | - |  |  |
| 134 | `ReleasQtty` | Released Quantity | Num | 19.6 | - |  |  |
| 135 | `LineType` | Row Type | VarChar | 1 | - | R | `R` = Regular |
| 136 | `TranType` | Transaction Type | VarChar | 1 | - |  | `C` = Complete<br>`R` = Reject |
| 137 | `Text` | Text | Text | 16 | - |  |  |
| 138 | `OwnerCode` | Document Owner | Int | 11 | - |  |  |
| 139 | `StockPrice` | Item Cost | Num | 19.6 | - |  |  |
| 140 | `ConsumeFCT` | Consumer Sales Forecast | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 141 | `LstByDsSum` | Last Buy Distribute Sum | Num | 19.6 | - |  |  |
| 142 | `StckINMPr` | Stock Inm Price | Num | 19.6 | - |  |  |
| 143 | `LstBINMPr` | Last Buy Inventory Journal Pr. | Num | 19.6 | - |  |  |
| 144 | `StckDstFc` | Stock Distribution Sum (FC) | Num | 19.6 | - |  |  |
| 145 | `StckDstSc` | Stock Distribution Sum (SC) | Num | 19.6 | - |  |  |
| 146 | `LstByDsFc` | Last Buy Distribute Sum (FC) | Num | 19.6 | - |  |  |
| 147 | `LstByDsSc` | Last Buy Distribute Sum (SC) | Num | 19.6 | - |  |  |
| 148 | `StockSum` | Stock Sum | Num | 19.6 | - |  |  |
| 149 | `StockSumFc` | Stock Sum FC | Num | 19.6 | - |  |  |
| 150 | `StockSumSc` | Stock Sum SC | Num | 19.6 | - |  |  |
| 151 | `StckSumApp` | Stock Sum Applied | Num | 19.6 | - |  |  |
| 152 | `StckAppFc` | Stock Sum Applied FC | Num | 19.6 | - |  |  |
| 153 | `StckAppSc` | Stock Sum Applied SC | Num | 19.6 | - |  |  |
| 154 | `ShipToCode` | Ship-to Code | nVarChar | 50 | - |  |  |
| 155 | `ShipToDesc` | Ship-to Description | nVarChar | 254 | - |  |  |
| 156 | `StckAppD` | Stock Distrib. - Applied Sum | Num | 19.6 | - |  |  |
| 157 | `StckAppDFC` | Stock Dist. - Applied Sum (FC) | Num | 19.6 | - |  |  |
| 158 | `StckAppDSC` | Stock Dist. - Applied Sum (SC) | Num | 19.6 | - |  |  |
| 159 | `BasePrice` | Price for Total Calculation | VarChar | 1 | - | E | `E` = Exclude Tax<br>`I` = Include Tax |
| 160 | `GTotal` | Gross Total | Num | 19.6 | - |  |  |
| 161 | `GTotalFC` | Gross Total (FC) | Num | 19.6 | - |  |  |
| 162 | `GTotalSC` | Gross Total (SC) | Num | 19.6 | - |  |  |
| 163 | `DistribExp` | Distribute Freight | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 164 | `DescOW` | Description Overwritten | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 165 | `DetailsOW` | Details Overwritten | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 166 | `GrossBase` | Base Method for Gross Profit | Int | 6 | - |  |  |
| 167 | `VatWoDpm` | Tax Before DPM Applied | Num | 19.6 | - |  |  |
| 168 | `VatWoDpmFc` | Tax Before DPM Applied FC | Num | 19.6 | - |  |  |
| 169 | `VatWoDpmSc` | Tax Before DPM Applied SC | Num | 19.6 | - |  |  |
| 170 | `CFOPCode` | CFOP Code for Document | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 171 | `CSTCode` | CST Code for ICMS | nVarChar | 20 | - |  |  |
| 172 | `Usage` | Usage Code for Document | Int | 11 | [OUSG](OUSG.md) |  |  |
| 173 | `TaxOnly` | Tax Only | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 174 | `WtCalced` | Withholding Tax Calculated | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 175 | `QtyToShip` | Quantity to Ship | Num | 19.6 | - |  |  |
| 176 | `DelivrdQty` | Delivered Quantity | Num | 19.6 | - |  |  |
| 177 | `OrderedQty` | Ordered Quantity | Num | 19.6 | - |  |  |
| 178 | `CogsOcrCod` | COGS Distribution Rule Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 179 | `CiOppLineN` | Line Number of Opposite Line | Int | 11 | - | -1 |  |
| 180 | `CogsAcct` | COGS Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 181 | `ChgAsmBoMW` | Change Whs for Asm BoM Child | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 182 | `ActDelDate` | Actual Delivery Date | Date | 8 | - |  |  |
| 183 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 184 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 185 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 186 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 187 | `TaxDistSum` | Tax Distributed Amount | Num | 19.6 | - |  |  |
| 188 | `TaxDistSFC` | Tax Distributed Amount (FC) | Num | 19.6 | - |  |  |
| 189 | `TaxDistSSC` | Tax Distributed Amount (SC) | Num | 19.6 | - |  |  |
| 190 | `PostTax` | Post Tax in Price to Stock | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 191 | `Excisable` | Excisable [Yes/No] | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 192 | `AssblValue` | Assessable Value | Num | 19.6 | - |  |  |
| 193 | `RG23APart1` | RG23A Part1 Number | Int | 11 | - |  |  |
| 194 | `RG23APart2` | RG23A Part2 Number | Int | 11 | - |  |  |
| 195 | `RG23CPart1` | RG23C Part1 Number | Int | 11 | - |  |  |
| 196 | `RG23CPart2` | RG23C Part2 Number | Int | 11 | - |  |  |
| 197 | `CogsOcrCo2` | COGS Distribution Rule Code2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 198 | `CogsOcrCo3` | COGS Distribution Rule Code3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 199 | `CogsOcrCo4` | COGS Distribution Rule Code4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 200 | `CogsOcrCo5` | COGS Distribution Rule Code5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 201 | `LnExcised` | Line Excised | VarChar | 1 | - |  | `O` = Open<br>`C` = Closed<br>`P` = Copied to OEI |
| 202 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 203 | `StockValue` | Total COGS Value | Num | 19.6 | - |  |  |
| 204 | `GPTtlBasPr` | Total Base Price for Profit | Num | 19.6 | - |  |  |
| 205 | `unitMsr2` | Pur/Sal UoM if BaseUnit | nVarChar | 100 | - |  |  |
| 206 | `NumPerMsr2` | Pur/Sal UoM Value if Base Unit | Num | 19.6 | - |  |  |
| 207 | `SpecPrice` | Price Source Type | VarChar | 1 | - | N | `Y` = Special Prices for Business Partner<br>`N` = Manual<br>`W` = Active Price List, Discount Groups<br>`R` = Active Price List<br>`U` = Inactive Price List<br>`A` = Blanket Agreement<br>`P` = Period and Volume Discounts<br>`Q` = Period and Volume Discounts, Discount Groups<br>`V` = Inactive Price List, Discount Groups<br>`9` = Special Prices for Business Partner<br>`!` = Blanket Agreement<br>`0` = Period and Volume Discounts<br>`1` = Period and Volume Discounts, Discount Groups<br>`2` = Active Price List<br>`7` = Active Price List, Discount Groups<br>`5` = Inactive Price List<br>`6` = Inactive Price List, Discount Groups |
| 208 | `CSTfIPI` | CST for IPI Code | nVarChar | 20 | - |  |  |
| 209 | `CSTfPIS` | CST for PIS Code | nVarChar | 20 | - |  |  |
| 210 | `CSTfCOFINS` | CST for COFINS Code | nVarChar | 20 | - |  |  |
| 211 | `ExLineNo` | ExLineNo | nVarChar | 10 | - |  |  |
| 212 | `isSrvCall` | Created from Service Call | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 213 | `PQTReqQty` | Pur Quotation: Required Qty | Num | 19.6 | - |  |  |
| 214 | `PQTReqDate` | Pur Quotation: Required Date | Date | 8 | - |  |  |
| 215 | `PcDocType` | Purchase Confirmation Doc Type | Int | 11 | - | -1 | `-1` = No Type<br>`22` = Purchase Order<br>`540000006` = Purchase Quotation |
| 216 | `PcQuantity` | Purchase Confirmation Quantity | Num | 19.6 | - |  |  |
| 217 | `LinManClsd` | Line Was Closed Manually | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`U` = Unknown |
| 218 | `VatGrpSrc` | VAT Group Source | VarChar | 1 | - | N | `N` = Not Defined<br>`M` = Manually Entered<br>`D` = Determined |
| 219 | `NoInvtryMv` | Without Inventory Movement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 220 | `ActBaseEnt` | Actual Base Document Entry | Int | 11 | - |  |  |
| 221 | `ActBaseLn` | Actual Base Line Number | Int | 11 | - |  |  |
| 222 | `ActBaseNum` | Actual Base Document No. | Int | 11 | - |  |  |
| 223 | `OpenRtnQty` | Quantity Open for Return | Num | 19.6 | - |  |  |
| 224 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 225 | `AgrLnNum` | Agreement Row Number | Int | 11 | - |  |  |
| 226 | `CredOrigin` | Credit Origin | VarChar | 1 | [OBSI](OBSI.md) |  |  |
| 227 | `Surpluses` | Surpluses | Num | 19.6 | - |  |  |
| 228 | `DefBreak` | Defect and Breakup | Num | 19.6 | - |  |  |
| 229 | `Shortages` | Shortages | Num | 19.6 | - |  |  |
| 230 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) | 0 |  |
| 231 | `UomEntry2` | UoM Entry if Base Unit | Int | 11 | [OUOM](OUOM.md) | 0 |  |
| 232 | `UomCode` | UoM Code | nVarChar | 20 | - |  |  |
| 233 | `UomCode2` | UoM Code if Base Unit | nVarChar | 20 | - |  |  |
| 234 | `FromWhsCod` | From Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 235 | `NeedQty` | Consider Quantity of Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 236 | `PartRetire` | Partial Retirement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 237 | `RetireQty` | Retirement Quantity | Num | 19.6 | - |  |  |
| 238 | `RetireAPC` | Retirement APC | Num | 19.6 | - |  |  |
| 239 | `RetirAPCFC` | Retirement APC FC | Num | 19.6 | - |  |  |
| 240 | `RetirAPCSC` | Retirement APC SC | Num | 19.6 | - |  |  |
| 241 | `InvQty` | Quantity - Inventory UoM | Num | 19.6 | - |  |  |
| 242 | `OpenInvQty` | Open Quantity (Inventory UoM) | Num | 19.6 | - |  |  |
| 243 | `EnSetCost` | Enable Set Item Cost in Return | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 244 | `RetCost` | Return Cost in A/R Return | Num | 19.6 | - |  |  |
| 245 | `Incoterms` | Incoterms | Int | 11 | [ODCI](ODCI.md) |  |  |
| 246 | `TransMod` | Transport Mode | Int | 11 | [ODCI](ODCI.md) |  |  |
| 247 | `LineVendor` | Line Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 248 | `DistribIS` | Distribute Intrastat Freight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 249 | `ISDistrb` | Intrastat Distrib. Amount | Num | 19.6 | - |  |  |
| 250 | `ISDistrbFC` | Intrastat Distrib. Amount (FC) | Num | 19.6 | - |  |  |
| 251 | `ISDistrbSC` | Intrastat Distrib. Amount (SC) | Num | 19.6 | - |  |  |
| 252 | `IsByPrdct` | Item Is By-Product | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 253 | `ItemType` | Item Type | Int | 11 | - | 4 | `4` = Item |
| 254 | `PriceEdit` | Price Was Edited by User | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 255 | `PrntLnNum` | Parent Line Number | Int | 11 | - |  |  |
| 256 | `LinePoPrss` | Line PO Process | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 257 | `FreeChrgBP` | Free of Charge (BP) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 258 | `TaxRelev` | Tax Relevant Row | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 259 | `LegalText` | Legal Text | nVarChar | 254 | - |  |  |
| 260 | `ThirdParty` | Third Party | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 261 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 262 | `InvQtyOnly` | Change Qty (Inv. UoM) Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 263 | `UnencReasn` | Reason for Unencumbered ICMS | Int | 11 | - |  |  |
| 264 | `ShipFromCo` | Ship-From Code | nVarChar | 50 | - |  |  |
| 265 | `ShipFromDe` | Ship-From Description | nVarChar | 254 | - |  |  |
| 266 | `FisrtBin` | First Bin Location | nVarChar | 228 | - |  |  |
| 267 | `AllocBinC` | Allocated Bin Location Count | nVarChar | 11 | - |  |  |
| 268 | `ExpType` | Expense Type | nVarChar | 4 | [OEXD](OEXD.md) |  |  |
| 269 | `ExpUUID` | Expense UUID | nVarChar | 50 | - |  |  |
| 270 | `ExpOpType` | Expense Operation Type | VarChar | 1 | - |  | `P` = Professional Services<br>`R` = Renting Assets<br>`O` = Others<br>`D` = Disposal of Goods<br>`S` = Import of Goods and Services<br>`V` = Import by Virtual Transfer<br>`G` = Global Operations |
| 271 | `DIOTNat` | DIOT Nationality | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 272 | `MYFtype` | MYF type | nVarChar | 2 | - |  | `S1` = MYF Wholesale Sales<br>`S2` = Retail Sales<br>`P1` = MYF Wholesale Purchases<br>`P3` = Other Expense Transactions |
| 273 | `GPBefDisc` | Gross Price | Num | 19.6 | - |  |  |
| 274 | `ReturnRsn` | Return Reason | Int | 6 | - | -1 |  |
| 275 | `ReturnAct` | Return Action | Int | 6 | - | -1 |  |
| 276 | `StgSeqNum` | Stage Sequence Number | Int | 11 | - |  |  |
| 277 | `StgEntry` | Stage Entry | Int | 11 | [ORST](ORST.md) |  |  |
| 278 | `StgDesc` | Stage Description | nVarChar | 100 | - |  |  |
| 279 | `ItmTaxType` | Item GST Tax Category | nVarChar | 2 | - |  | `GR` = GST Regular<br>`GN` = GST Nil Rated<br>`GE` = GST Exempt<br>`NE` = Excisable<br>`NN` = Non-GST Non-Excisable |
| 280 | `SacEntry` | SAC Entry | Int | 11 | [OSAC](OSAC.md) |  |  |
| 281 | `NCMCode` | NCM Code | Int | 11 | [ONCM](ONCM.md) | -1 |  |
| 282 | `HsnEntry` | HSN Entry | Int | 11 | - |  |  |
| 283 | `OriBAbsEnt` | Original Base Document Internal ID | Int | 11 | - |  |  |
| 284 | `OriBLinNum` | Original Base Document Line Number | Int | 11 | - |  |  |
| 285 | `OriBDocTyp` | Original Base Document Type | Int | 11 | - |  |  |
| 286 | `IsPrscGood` | Is Prescribed Goods | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 287 | `IsCstmAct` | Apply Customer Accounting Tax Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`U` = Use |
| 288 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 289 | `ExtTaxRate` | External Tax Rate | Num | 19.6 | - |  |  |
| 290 | `ExtTaxSum` | External Tax Amount | Num | 19.6 | - |  |  |
| 291 | `TaxAmtSrc` | Tax Amount Source | VarChar | 1 | - | S | `S` = Internal System Calculation<br>`E` = External Calculation |
| 292 | `ExtTaxSumF` | External Tax Amount (FC) | Num | 19.6 | - |  |  |
| 293 | `ExtTaxSumS` | External Tax Amount (SC) | Num | 19.6 | - |  |  |
| 294 | `StdItemId` | Standard Item Identification | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 295 | `CommClass` | Commodity Classification | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 296 | `VatExEntry` | VAT Exemption AbsEntry | Int | 11 | [OVEB](OVEB.md) |  |  |
| 297 | `VatExLN` | VAT Exemption LineNum | Int | 6 | - |  |  |
| 298 | `NatOfTrans` | Nature of Transaction | Int | 11 | [ODCI](ODCI.md) |  |  |
| 299 | `ISDtCryImp` | Destination Country/Region for Import | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 300 | `ISDtRgnImp` | Destination Region for Import | Int | 11 | [ODCI](ODCI.md) |  |  |
| 301 | `ISOrCryExp` | Country/Region of Origin for Export | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 302 | `ISOrRgnExp` | Region of Origin for Export | Int | 11 | [ODCI](ODCI.md) |  |  |
| 303 | `NVECode` | NVE Code | nVarChar | 6 | - |  |  |
| 304 | `PoNum` | Customer's Purchase Order Number | nVarChar | 20 | - |  |  |
| 305 | `PoItmNum` | Customer's Purchase Order Item Number | Int | 11 | - |  |  |
| 306 | `IndEscala` | Indicator for Relevant Scale | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 307 | `CESTCode` | CEST Code | Int | 11 | [OCEST](OCEST.md) |  |  |
| 308 | `CtrSealQty` | Control Seal Quantity | Num | 19.6 | - |  |  |
| 309 | `CNJPMan` | CNPJ of Manufacturer | nVarChar | 14 | - |  |  |
| 310 | `UFFiscBene` | UF Fiscal Benefit Code | nVarChar | 10 | - |  |  |
| 311 | `CUSplit` | CU Split | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 312 | `LegalTIMD` | Legal Text from Item Master Data | nVarChar | 250 | - |  |  |
| 313 | `LegalTTCA` | Legal Text from Tax Code Attributes | nVarChar | 250 | - |  |  |
| 314 | `LegalTW` | Legal Text from Warehouse | nVarChar | 250 | - |  |  |
| 315 | `LegalTCD` | Legal Text from Tax Code Determination | nVarChar | 250 | - |  |  |
| 316 | `RevCharge` | Reverse Charge | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 317 | `ListNum` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 318 | `RecogAmt` | Deducted Tax Amount | Num | 19.6 | - |  |  |
| 319 | `RecogAmtSC` | Deducted Tax Amount (SC) | Num | 19.6 | - |  |  |
| 320 | `RecogAmtFC` | Deducted Tax Amount (FC) | Num | 19.6 | - |  |  |
| 321 | `RecogVatGr` | Deducted Tax Code | nVarChar | 8 | - |  |  |
| 322 | `RecogVatPr` | Deducted Tax % | Num | 19.6 | - |  |  |
| 323 | `NonDdAmt` | Non-Deductible Amount | Num | 19.6 | - |  |  |
| 324 | `NonDdAmtSC` | Non-Deductible Amount (SC) | Num | 19.6 | - |  |  |
| 325 | `NonDdAmtFC` | Non-Deductible Amount (FC) | Num | 19.6 | - |  |  |
| 326 | `PPTaxExRe` | Plastic Packaging Tax Exemption Reason | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 327 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |
| 328 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 329 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 330 | `OperProfit` | Row Operating Profit | Num | 19.6 | - |  |  |
| 331 | `OperProfFC` | Row Operating Profit (FC) | Num | 19.6 | - |  |  |
| 332 | `OperProfSy` | Row Operating Profit (SC) | Num | 19.6 | - |  |  |
| 333 | `NetIncome` | Row Net Income | Num | 19.6 | - |  |  |
| 334 | `NetIncomFC` | Row Net Income (FC) | Num | 19.6 | - |  |  |
| 335 | `NetIncomSy` | Row Net Income (SC) | Num | 19.6 | - |  |  |
| 336 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 337 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |
| 338 | `UoMNum2` | UoM Item Per Unit Numerator2 | Num | 19.6 | - |  |  |
| 339 | `UoMDen2` | UoM Item Per Unit Denominator2 | Num | 19.6 | - |  |  |
| 340 | `CSTfIBS` | CST for IBS Code | nVarChar | 20 | - |  |  |
| 341 | `CSTfCBS` | CST for CBS Code | nVarChar | 20 | - |  |  |
| 342 | `CSTfIS` | CST for IS Code | nVarChar | 20 | - |  |  |
| 343 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |

## Claves e índices (9)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| STATUS | No | LineStatus |
| CURRENCY | No | Currency |
| ACCOUNT | No | AcctCode |
| BASE_ENTRY | No | BaseEntry, BaseType, BaseLine |
| VIS_ORDER | No | DocEntry, VisOrder |
| OWNER_CODE | No | OwnerCode |
| ITM_WHS_OQ | No | ItemCode, WhsCode, OpenQty |
| PROJECT | No | Project |
