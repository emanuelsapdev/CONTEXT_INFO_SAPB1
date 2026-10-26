# UITM - Items

- **Tabla:** UITM
- **Descripción:** Items
- **Cantidad de campos:** 346
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UITM.html

## Campos (346)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 2 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 3 | `FrgnName` | Foreign Name | nVarChar | 200 | - |  |  |
| 4 | `ItmsGrpCod` | Item Group | Int | 6 | [OITB](OITB.md) | 100 |  |
| 5 | `CstGrpCode` | Customs Group | Int | 6 | [OARG](OARG.md) | -1 |  |
| 6 | `VatGourpSa` | Sales Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 7 | `CodeBars` | Bar Code | nVarChar | 254 | - |  |  |
| 8 | `VATLiable` | Tax Liable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `PrchseItem` | Purchasing Item | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `SellItem` | Sales Item | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `InvntItem` | Inventory Item | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 12 | `OnHand` | In Stock | Num | 19.6 | - |  |  |
| 13 | `IsCommited` | Qty Ordered by Customers | Num | 19.6 | - |  |  |
| 14 | `OnOrder` | Qty Ordered from Vendors | Num | 19.6 | - |  |  |
| 15 | `IncomeAcct` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `ExmptIncom` | Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `MaxLevel` | Maximum Inventory Level | Num | 19.6 | - |  |  |
| 18 | `DfltWH` | Default Warehouse | nVarChar | 8 | - |  |  |
| 19 | `CardCode` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 20 | `SuppCatNum` | Mfr Catalog No. | nVarChar | 50 | - |  |  |
| 21 | `BuyUnitMsr` | Purchasing UoM | nVarChar | 100 | - |  |  |
| 22 | `NumInBuy` | Items per Purchasing Unit | Num | 19.6 | - |  |  |
| 23 | `ReorderQty` | Required (Purchasing UoM) | Num | 19.6 | - |  |  |
| 24 | `MinLevel` | Minimum Inventory Level | Num | 19.6 | - |  |  |
| 25 | `LstEvlPric` | Last Evaluated Price | Num | 19.6 | - |  |  |
| 26 | `LstEvlDate` | Date of Last Reval. Price | Date | 8 | - |  |  |
| 27 | `CustomPer` | Customs Rate | Num | 19.6 | - |  |  |
| 28 | `Canceled` | Canceled Item [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `MnufctTime` | Production Date in Days | Int | 11 | - |  |  |
| 30 | `WholSlsTax` | Tax Rate for Wholesaler | VarChar | 1 | - |  |  |
| 31 | `RetilrTax` | Sales Tax in % | VarChar | 1 | - |  |  |
| 32 | `SpcialDisc` | Special Discount % | Num | 19.6 | - |  |  |
| 33 | `DscountCod` | Discount Code | Int | 6 | - |  |  |
| 34 | `TrackSales` | Follow-Up [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `SalUnitMsr` | Sales UoM | nVarChar | 100 | - |  |  |
| 36 | `NumInSale` | No. of Items per Sales Unit | Num | 19.6 | - |  |  |
| 37 | `Consig` | Consignment Goods Whse | Num | 19.6 | - |  |  |
| 38 | `QueryGroup` | Properties | Int | 11 | - | 0 |  |
| 39 | `Counted` | Quantity Counted in Inventory | Num | 19.6 | - |  |  |
| 40 | `OpenBlnc` | Initial Inventory | Num | 19.6 | - |  |  |
| 41 | `EvalSystem` | Valuation Method | VarChar | 1 | - |  | `A` = Moving Average<br>`S` = Standard<br>`F` = FIFO<br>`B` = Serial/Batch |
| 42 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 43 | `FREE` | Free [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `PicturName` | Picture | nVarChar | 200 | - |  |  |
| 45 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `BlncTrnsfr` | Balances Transferred [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `UserText` | Item Remarks | Text | 16 | - |  |  |
| 48 | `SerialNum` | Serial Number | nVarChar | 17 | - |  |  |
| 49 | `CommisPcnt` | % Commission for Item | Num | 19.6 | - |  |  |
| 50 | `CommisSum` | Total Commission for Item | Num | 19.6 | - |  |  |
| 51 | `CommisGrp` | Commission Group | Int | 6 | [OCOG](OCOG.md) | 0 |  |
| 52 | `TreeType` | BOM Type | VarChar | 1 | - | N | `N` = Not a BOM<br>`A` = Assembly<br>`S` = Sales<br>`P` = Production<br>`T` = Template |
| 53 | `TreeQty` | No. of Units | Num | 19.6 | - |  |  |
| 54 | `LastPurPrc` | Last Purchase Price | Num | 19.6 | - |  |  |
| 55 | `LastPurCur` | Last Purchase Currency | nVarChar | 3 | - |  |  |
| 56 | `LastPurDat` | Last Purchase Date | Date | 8 | - |  |  |
| 57 | `ExitCur` | Issue Currency | nVarChar | 3 | - |  |  |
| 58 | `ExitPrice` | Issue Price | Num | 19.6 | - |  |  |
| 59 | `ExitWH` | Release Warehouse | nVarChar | 8 | - |  |  |
| 60 | `AssetItem` | Fixed Asset Indicator | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `WasCounted` | Counted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `ManSerNum` | Serial No. Management | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `SHeight1` | Height 1 - Sales Unit | Num | 19.6 | - |  |  |
| 64 | `SHght1Unit` | Height 1 - UoM for Sales | Int | 6 | - |  |  |
| 65 | `SHeight2` | Height 2 - Sales Unit | Num | 19.6 | - |  |  |
| 66 | `SHght2Unit` | Height 2 - UoM for Sales | Int | 6 | - |  |  |
| 67 | `SWidth1` | Width 1 - Sales Unit | Num | 19.6 | - |  |  |
| 68 | `SWdth1Unit` | Width 1 - UoM for Sales | Int | 6 | - |  |  |
| 69 | `SWidth2` | Width 2 - Sales Unit | Num | 19.6 | - |  |  |
| 70 | `SWdth2Unit` | Width 2 - UoM for Sales | Int | 6 | - |  |  |
| 71 | `SLength1` | Length 1 - Sales Unit | Num | 19.6 | - |  |  |
| 72 | `SLen1Unit` | Length 1 - UoM for Sales | Int | 6 | - |  |  |
| 73 | `Slength2` | Length 2 - Sales Unit | Num | 19.6 | - |  |  |
| 74 | `SLen2Unit` | Length 2 - UoM for Sales | Int | 6 | - |  |  |
| 75 | `SVolume` | Volume - Sales Unit | Num | 19.6 | - |  |  |
| 76 | `SVolUnit` | Volume - UoM for Sales | Int | 6 | - |  |  |
| 77 | `SWeight1` | Weight 1 - Sales Unit | Num | 19.6 | - |  |  |
| 78 | `SWght1Unit` | Weight 1 - UoM for Sales | Int | 6 | - |  |  |
| 79 | `SWeight2` | Weight 2 - Sales Unit | Num | 19.6 | - |  |  |
| 80 | `SWght2Unit` | Weight 2 - UoM for Sales | Int | 6 | - |  |  |
| 81 | `BHeight1` | Height 1 - Purchasing Unit | Num | 19.6 | - |  |  |
| 82 | `BHght1Unit` | Height 1 - UoM for Purchasing | Int | 6 | - |  |  |
| 83 | `BHeight2` | Height 2 - Purchasing Unit | Num | 19.6 | - |  |  |
| 84 | `BHght2Unit` | Height 2 - UoM for Purchasing | Int | 6 | - |  |  |
| 85 | `BWidth1` | Width 1 - Purchasing Unit | Num | 19.6 | - |  |  |
| 86 | `BWdth1Unit` | Width 1 - UoM for Purchasing | Int | 6 | - |  |  |
| 87 | `BWidth2` | Width 2 - Purchasing Unit | Num | 19.6 | - |  |  |
| 88 | `BWdth2Unit` | Width 2 - UoM for Purchasing | Int | 6 | - |  |  |
| 89 | `BLength1` | Length 1 - Purchase Unit | Num | 19.6 | - |  |  |
| 90 | `BLen1Unit` | Length 1 - UoM for Purchasing | Int | 6 | - |  |  |
| 91 | `Blength2` | Length 2 - Purchasing Unit | Num | 19.6 | - |  |  |
| 92 | `BLen2Unit` | Length 2 - UoM for Purchasing | Int | 6 | - |  |  |
| 93 | `BVolume` | Volume - Purchasing Unit | Num | 19.6 | - |  |  |
| 94 | `BVolUnit` | Volume - UoM for Purchasing | Int | 6 | - |  |  |
| 95 | `BWeight1` | Weight 1 - Purchasing Unit | Num | 19.6 | - |  |  |
| 96 | `BWght1Unit` | Weight 1 - UoM for Purchasing | Int | 6 | - |  |  |
| 97 | `BWeight2` | Weight 2 - Purchasing Unit | Num | 19.6 | - |  |  |
| 98 | `BWght2Unit` | Weight 2 - UoM for Purchasing | Int | 6 | - |  |  |
| 99 | `FixCurrCms` | Currency of Fixed Commission | nVarChar | 3 | - |  |  |
| 100 | `FirmCode` | Manufacturer | Int | 6 | [OMRC](OMRC.md) | -1 |  |
| 101 | `LstSalDate` | Last Sale Date | Date | 8 | - |  |  |
| 102 | `QryGroup1` | Property 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 103 | `QryGroup2` | Property 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 104 | `QryGroup3` | Property 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 105 | `QryGroup4` | Property 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 106 | `QryGroup5` | Property 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 107 | `QryGroup6` | Property 6 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 108 | `QryGroup7` | Property 7 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `QryGroup8` | Property 8 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 110 | `QryGroup9` | Property 9 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 111 | `QryGroup10` | Property 10 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 112 | `QryGroup11` | Property 11 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `QryGroup12` | Property 12 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 114 | `QryGroup13` | Property 13 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 115 | `QryGroup14` | Property 14 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `QryGroup15` | Property 15 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `QryGroup16` | Property 16 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 118 | `QryGroup17` | Property 17 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 119 | `QryGroup18` | Property 18 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 120 | `QryGroup19` | Property 19 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 121 | `QryGroup20` | Property 20 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `QryGroup21` | Property 21 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `QryGroup22` | Property 22 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `QryGroup23` | Property 23 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 125 | `QryGroup24` | Property 24 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 126 | `QryGroup25` | Property 25 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 127 | `QryGroup26` | Property 26 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 128 | `QryGroup27` | Property 27 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 129 | `QryGroup28` | Property 28 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 130 | `QryGroup29` | Property 29 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 131 | `QryGroup30` | Property 30 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 132 | `QryGroup31` | Property 31 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 133 | `QryGroup32` | Property 32 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 134 | `QryGroup33` | Property 33 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 135 | `QryGroup34` | Property 34 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 136 | `QryGroup35` | Property 35 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 137 | `QryGroup36` | Property 36 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 138 | `QryGroup37` | Property 37 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 139 | `QryGroup38` | Property 38 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 140 | `QryGroup39` | Property 39 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 141 | `QryGroup40` | Property 40 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 142 | `QryGroup41` | Property 41 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 143 | `QryGroup42` | Property 42 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 144 | `QryGroup43` | Property 43 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 145 | `QryGroup44` | Property 44 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 146 | `QryGroup45` | Property 45 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 147 | `QryGroup46` | Property 46 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 148 | `QryGroup47` | Property 47 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 149 | `QryGroup48` | Property 48 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 150 | `QryGroup49` | Property 49 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 151 | `QryGroup50` | Property 50 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 152 | `QryGroup51` | Property 51 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 153 | `QryGroup52` | Property 52 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 154 | `QryGroup53` | Property 53 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 155 | `QryGroup54` | Property 54 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 156 | `QryGroup55` | Property 55 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 157 | `QryGroup56` | Property 56 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 158 | `QryGroup57` | Property 57 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 159 | `QryGroup58` | Property 58 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 160 | `QryGroup59` | Property 59 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 161 | `QryGroup60` | Property 60 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 162 | `QryGroup61` | Property 61 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 163 | `QryGroup62` | Property 62 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 164 | `QryGroup63` | Property 63 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 165 | `QryGroup64` | Property 64 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 166 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 167 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 168 | `ExportCode` | Data Export Code | nVarChar | 20 | - |  |  |
| 169 | `SalFactor1` | Sales Factor 1 | Num | 19.6 | - |  |  |
| 170 | `SalFactor2` | Sales Factor 2 | Num | 19.6 | - |  |  |
| 171 | `SalFactor3` | Sales Factor 3 | Num | 19.6 | - |  |  |
| 172 | `SalFactor4` | Sales Factor 4 | Num | 19.6 | - |  |  |
| 173 | `PurFactor1` | Purchasing Factor 1 | Num | 19.6 | - |  |  |
| 174 | `PurFactor2` | Purchasing Factor 2 | Num | 19.6 | - |  |  |
| 175 | `PurFactor3` | Purchasing Factor 3 | Num | 19.6 | - |  |  |
| 176 | `PurFactor4` | Purchasing Factor 4 | Num | 19.6 | - |  |  |
| 177 | `SalFormula` | Sales Formula | nVarChar | 40 | - |  |  |
| 178 | `PurFormula` | Purchasing Formula | nVarChar | 40 | - |  |  |
| 179 | `VatGroupPu` | Purchasing Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 180 | `AvgPrice` | Item Cost | Num | 19.6 | - |  |  |
| 181 | `PurPackMsr` | Packaging UoM (Purchasing) | nVarChar | 30 | - |  |  |
| 182 | `PurPackUn` | Quantity per Package (Purchasing) | Num | 19.6 | - |  |  |
| 183 | `SalPackMsr` | Packaging UoM (Sales) | nVarChar | 30 | - |  |  |
| 184 | `SalPackUn` | Quantity per Package (Sales) | Num | 19.6 | - |  |  |
| 185 | `SCNCounter` | SCN Counter | Int | 6 | - |  |  |
| 186 | `ManBtchNum` | Manage Batch No. [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 187 | `ManOutOnly` | Manage SNs Only on Exit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 188 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer<br>`G` = Fixed Assets Migration |
| 189 | `validFor` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 190 | `validFrom` | Active From | Date | 8 | - |  |  |
| 191 | `validTo` | Active To | Date | 8 | - |  |  |
| 192 | `frozenFor` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 193 | `frozenFrom` | Inactive From | Date | 8 | - |  |  |
| 194 | `frozenTo` | Inactive To | Date | 8 | - |  |  |
| 195 | `BlockOut` | Force Selection of Serial No. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 196 | `ValidComm` | Active Remarks | nVarChar | 30 | - |  |  |
| 197 | `FrozenComm` | Inactive Remarks | nVarChar | 30 | - |  |  |
| 198 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 199 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |
| 200 | `SWW` | Additional Identifier | nVarChar | 16 | - |  |  |
| 201 | `Deleted` | Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 202 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 203 | `ExpensAcct` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 204 | `FrgnInAcct` | Revenue Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 205 | `ShipType` | Shipping Type | Int | 6 | [OSHP](OSHP.md) |  |  |
| 206 | `GLMethod` | Set G/L Accounts By | VarChar | 1 | - | W | `W` = Warehouse<br>`C` = Item Group<br>`L` = Item Level |
| 207 | `ECInAcct` | Revenue Account - EU | nVarChar | 15 | - |  |  |
| 208 | `FrgnExpAcc` | Expense Account - Foreign | nVarChar | 15 | - |  |  |
| 209 | `ECExpAcc` | Expense Account - EU | nVarChar | 15 | - |  |  |
| 210 | `TaxType` | Tax Type | VarChar | 1 | - | Y | `Y` = Regular Tax<br>`U` = Use Tax<br>`N` = No Tax |
| 211 | `ByWh` | Manage Inventory by Warehouse | VarChar | 1 | - |  |  |
| 212 | `WTLiable` | WTax Liable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 213 | `ItemType` | Item Type | VarChar | 1 | - | I | `I` = Items<br>`L` = Labor<br>`T` = Travel<br>`F` = Fixed Assets |
| 214 | `WarrntTmpl` | Warranty Template | nVarChar | 20 | [OCTT](OCTT.md) |  |  |
| 215 | `BaseUnit` | Base Unit Name | nVarChar | 20 | - |  |  |
| 216 | `CountryOrg` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 217 | `StockValue` | Inventory Value | Num | 19.6 | - |  |  |
| 218 | `Phantom` | Phantom Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 219 | `IssueMthd` | Issue Method | VarChar | 1 | - |  | `B` = Backflush<br>`M` = Manual |
| 220 | `FREE1` | Yield in % | VarChar | 1 | - |  |  |
| 221 | `PricingPrc` | Pricing Percentage | Num | 19.6 | - |  |  |
| 222 | `MngMethod` | Management Method | VarChar | 1 | - | R | `A` = On Every Transaction<br>`R` = On Release Only |
| 223 | `ReorderPnt` | Reorder Point | Num | 19.6 | - |  |  |
| 224 | `InvntryUom` | Inventory UoM | nVarChar | 100 | - |  |  |
| 225 | `PlaningSys` | Planning Method | VarChar | 1 | - | N | `M` = MRP<br>`N` = None |
| 226 | `PrcrmntMtd` | Procurement Method | VarChar | 1 | - | B | `B` = Buy<br>`M` = Make |
| 227 | `OrdrIntrvl` | Order Interval | Int | 6 | [OCYC](OCYC.md) |  |  |
| 228 | `OrdrMulti` | Order Multiple | Num | 19.6 | - |  |  |
| 229 | `MinOrdrQty` | Minimum Order Quantity | Num | 19.6 | - |  |  |
| 230 | `LeadTime` | Lead Time | Int | 11 | - |  |  |
| 231 | `IndirctTax` | Indirect Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 232 | `TaxCodeAR` | Tax Code (A/R) | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 233 | `TaxCodeAP` | Tax Code (A/P) | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 234 | `OSvcCode` | Outgoing Service Code | Int | 11 | [OSCD](OSCD.md) | -1 |  |
| 235 | `ISvcCode` | Incoming Service Code | Int | 11 | [OSCD](OSCD.md) | -1 |  |
| 236 | `ServiceGrp` | Service Group | Int | 11 | [OSGP](OSGP.md) | -1 |  |
| 237 | `NCMCode` | NCM Code | Int | 11 | [ONCM](ONCM.md) | -1 |  |
| 238 | `MatType` | Material Type | nVarChar | 3 | [OMTP](OMTP.md) | 1 |  |
| 239 | `MatGrp` | Material Group | Int | 11 | [OMGP](OMGP.md) | -1 |  |
| 240 | `ProductSrc` | Product Source | nVarChar | 2 | [OPSC](OPSC.md) | 0 |  |
| 241 | `ServiceCtg` | Service Category | Int | 11 | [OSCG](OSCG.md) | -1 | `-1` |
| 242 | `ItemClass` | Service or Material | VarChar | 1 | - | 2 | `2` = Material<br>`1` = Service |
| 243 | `Excisable` | Excisable [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 244 | `ChapterID` | Chapter ID | Int | 11 | [OCHP](OCHP.md) | -1 |  |
| 245 | `NotifyASN` | Notification Available SNs | nVarChar | 40 | - |  |  |
| 246 | `ProAssNum` | Provisional Assessment No. | nVarChar | 20 | - |  |  |
| 247 | `AssblValue` | Assessable Value | Num | 19.6 | - |  |  |
| 248 | `DNFEntry` | DNF Code Entry | Int | 11 | [ODNF](ODNF.md) | -1 |  |
| 249 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 250 | `Spec` | Item Specification | nVarChar | 30 | - |  |  |
| 251 | `TaxCtg` | Tax Category | nVarChar | 4 | - |  |  |
| 252 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 253 | `Number` | Number | Int | 11 | - |  |  |
| 254 | `FuelCode` | Fuel | Int | 11 | [OBFI](OBFI.md) | -1 |  |
| 255 | `BeverTblC` | Beverage Table | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 256 | `BeverGrpC` | Beverage Group | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 257 | `BeverTM` | Beverage Brand | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 258 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 259 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 260 | `ToleranDay` | Tolerance Days | Int | 11 | - |  |  |
| 261 | `UgpEntry` | UoM Group | Int | 11 | [OUGP](OUGP.md) |  |  |
| 262 | `PUoMEntry` | Default Purchasing UoM | Int | 11 | [OUOM](OUOM.md) |  |  |
| 263 | `SUoMEntry` | Default Sales UoM | Int | 11 | [OUOM](OUOM.md) |  |  |
| 264 | `IUoMEntry` | Inventory UoM | Int | 11 | [OUOM](OUOM.md) |  |  |
| 265 | `IssuePriBy` | Issue Primarily By SnB or Bin | Int | 6 | - |  | `0` = Issue Primarily by Serial/Batch Number<br>`1` = Issue Primarily by Bin Location |
| 266 | `AssetClass` | Asset Class | nVarChar | 20 | [OACS](OACS.md) |  |  |
| 267 | `AssetGroup` | Asset Group | nVarChar | 15 | [OAGS](OAGS.md) |  |  |
| 268 | `InventryNo` | Inventory Number of Asset | nVarChar | 12 | - |  |  |
| 269 | `Technician` | Technician of Fixed Asset | Int | 11 | [OHEM](OHEM.md) |  |  |
| 270 | `Employee` | Employee of Fixed Asset | Int | 11 | [OHEM](OHEM.md) |  |  |
| 271 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 272 | `StatAsset` | Owned by Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 273 | `Cession` | Cession | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 274 | `DeacAftUL` | Deactivate After Useful Life | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 275 | `AsstStatus` | Asset Status | VarChar | 1 | - | N | `N` = New<br>`A` = Active<br>`I` = Inactive |
| 276 | `CapDate` | Capitalization Date | Date | 8 | - |  |  |
| 277 | `AcqDate` | Acquisition Date | Date | 8 | - |  |  |
| 278 | `RetDate` | Retirement Date | Date | 8 | - |  |  |
| 279 | `GLPickMeth` | G/L Account Pick Method | VarChar | 1 | - | A | `A` = General<br>`W` = Warehouse<br>`C` = Item Group |
| 280 | `NoDiscount` | No Discounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 281 | `MgrByQty` | Manage Asset by Quantity | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 282 | `AssetRmk1` | Asset Remark 1 | nVarChar | 100 | - |  |  |
| 283 | `AssetRmk2` | Asset Remark 2 | nVarChar | 100 | - |  |  |
| 284 | `AssetAmnt1` | Asset Amount 1 | Num | 19.6 | - |  |  |
| 285 | `AssetAmnt2` | Asset Amount 2 | Num | 19.6 | - |  |  |
| 286 | `DeprGroup` | Depreciation Group | nVarChar | 15 | [OADG](OADG.md) |  |  |
| 287 | `AssetSerNo` | Asset Serial Number | nVarChar | 32 | - |  |  |
| 288 | `CntUnitMsr` | Inventory Counting UoM Name | nVarChar | 100 | - |  |  |
| 289 | `NumInCnt` | No. of Items per Counting Unit | Num | 19.6 | - |  |  |
| 290 | `INUoMEntry` | Inventory Counting UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 291 | `OneBOneRec` | One Batch One Receipt | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 292 | `RuleCode` | Checking Rule Code | nVarChar | 2 | [ODCR](ODCR.md) |  |  |
| 293 | `ScsCode` | Scs Code | nVarChar | 10 | - |  |  |
| 294 | `SpProdType` | Special Product Type | nVarChar | 2 | - |  | `MT` = Cellular Phones<br>`IO` = Integrated Circuits |
| 295 | `IWeight1` | Weight 1 - Inventory | Num | 19.6 | - |  |  |
| 296 | `IWght1Unit` | Weight 1 - Inventory Unit | Int | 6 | - |  |  |
| 297 | `IWeight2` | Weight 2 - Inventory | Num | 19.6 | - |  |  |
| 298 | `IWght2Unit` | Weight 2 - Inventory Unit | Int | 6 | - |  |  |
| 299 | `CompoWH` | Component Warehouse | VarChar | 1 | - | B | `B` = From Bill of Materials Line<br>`P` = From Parent Item Document Line |
| 300 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 301 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 302 | `VirtAstItm` | Virtual Asset Item | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 303 | `SouVirAsst` | Source Virtual Asset Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 304 | `InCostRoll` | Include in Prod. Cost Rollup | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 305 | `PrdStdCst` | Production Std Cost | Num | 19.6 | - |  |  |
| 306 | `EnAstSeri` | Enforce Asset Serial Numbers | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 307 | `LinkRsc` | Linked Resource | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 308 | `OnHldPert` | Capital Goods On Hold Percent | Num | 19.6 | - |  |  |
| 309 | `onHldLimt` | Capital Goods on Hold Limit | Num | 19.6 | - |  |  |
| 310 | `PriceUnit` | Pricing Unit | Int | 11 | [OUOM](OUOM.md) |  |  |
| 311 | `GSTRelevnt` | GST Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 312 | `SACEntry` | SAC Entry | Int | 11 | [OSAC](OSAC.md) | -1 |  |
| 313 | `GstTaxCtg` | GST Tax Category | VarChar | 1 | - | R | `R` = Regular<br>`N` = Nil Rated<br>`E` = Exempt |
| 314 | `AssVal4WTR` | Assessable Value for WTR | Num | 19.6 | - |  |  |
| 315 | `ExcImpQUoM` | Default Excise Imported Quantity UoM | Int | 11 | - |  | `112` = Liters, m3<br>`168` = Tonne, metric ton (1000 kg)<br>`251` = Horsepower (1 hp = 0.75 kW)<br>`831` = Liters of anhydrous (pure) alcohol |
| 316 | `ExcFixAmnt` | Default Excise Fixed Amount | Num | 19.6 | - |  |  |
| 317 | `ExcRate` | Default Excise Rate | Num | 19.6 | - |  |  |
| 318 | `SOIExc` | SOI Excisable | VarChar | 1 | - | 4 | `1` = Excisable<br>`2` = Exemption of excises<br>`3` = Excises are paid to another authority<br>`4` = Not Excisable |
| 319 | `TNVED` | TNVED Code | nVarChar | 10 | - |  |  |
| 320 | `Imported` | Imported Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 321 | `AutoBatch` | Automatic Batch Creation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 322 | `CstmActing` | Customer Accounting | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 323 | `StdItemId` | Standard Item Identification | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 324 | `CommClass` | Commodity Classification | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 325 | `TaxCatCode` | Tax Category Code for GTS | nVarChar | 50 | [OTCC](OTCC.md) |  |  |
| 326 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 327 | `NVECode` | NVE Code | nVarChar | 6 | - |  |  |
| 328 | `CESTCode` | CEST Code | Int | 11 | [OCEST](OCEST.md) |  |  |
| 329 | `CtrSealQty` | Control Seal Qty | Num | 19.6 | - |  |  |
| 330 | `LegalText` | Legal Text | nVarChar | 250 | - |  |  |
| 331 | `QRCodeSrc` | QR Code Source | Text | 16 | - |  |  |
| 332 | `Traceable` | Traceable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 333 | `IfrsPsRev` | IFRS Posting for Revaluation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 334 | `PlPaTaxCat` | Plastic Packaging Tax Category | nVarChar | 2 | - |  |  |
| 335 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |
| 336 | `PPTExReSa` | Plastic Packaging Tax Exemption Reason for A/P or A/R | nVarChar | 2 | - |  |  |
| 337 | `PPTExRePr` | Plastic Package Tax Exemption Reason for Production | nVarChar | 2 | - |  |  |
| 338 | `ProdctType` | SAF-T Product Type | VarChar | 1 | - | P | `P` = Products<br>`S` = Services<br>`O` = Other<br>`I` = Taxes |
| 339 | `ProdTypeEx` | SAF-T Product Type | nVarChar | 10 | [OSPT](OSPT.md) | P |  |
| 340 | `SalUomNum` | Sales UoM Numerator | Num | 19.6 | - |  |  |
| 341 | `SalUomDen` | Sales UoM Denominator | Num | 19.6 | - |  |  |
| 342 | `BuyUomNum` | Buy UoM Numerator | Num | 19.6 | - |  |  |
| 343 | `BuyUomDen` | Buy UoM Denominator | Num | 19.6 | - |  |  |
| 344 | `IncUomNum` | Counting UoM Numerator | Num | 19.6 | - |  |  |
| 345 | `IncUomDen` | Counting UoM Denominator | Num | 19.6 | - |  |  |
| 346 | `NoApDisc` | Do Not Apply Discount | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (7)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode |
| ITEM_NAME | No | ItemName |
| TREE_TYPE | No | TreeType |
| COM_GROUP | No | CommisGrp |
| SALE | No | SellItem |
| PURCHASE | No | PrchseItem |
| INVENTORY | No | InvntItem |
