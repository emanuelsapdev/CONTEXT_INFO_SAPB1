# ISW3 - Declaration Rows

- **Tabla:** ISW3
- **Descripción:** Declaration Rows
- **Cantidad de campos:** 80
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ISW3.html

## Campos (80)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizAbsEnt` | Wizard Run Key | Int | 11 | [OISW](OISW.md) |  |  |
| 2 | `Line` | Declaration Line | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `RowStatus` | Row Status | VarChar | 1 | - | O |  |
| 5 | `CardCode` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `ObjType` | Document Type | Int | 11 | - |  |  |
| 7 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 8 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 9 | `RecpType` | Receipt Type | VarChar | 1 | - |  |  |
| 10 | `DocBillDt` | Document Billing Date | Date | 8 | - |  |  |
| 11 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 12 | `BPCtry` | Sender or Receiver Country/Region | nVarChar | 3 | - |  |  |
| 13 | `TaxCodeExt` | Tax Code Extension | nVarChar | 12 | - |  |  |
| 14 | `NetMassSgn` | Net Mass Sign | VarChar | 1 | - | + | `+` = Positive<br>`-` = Negative |
| 15 | `NetMass` | Net Mass | Num | 19.6 | - |  |  |
| 16 | `NetMassUnt` | Net Mass Unit | nVarChar | 12 | - |  |  |
| 17 | `SupMassSgn` | Supplementary Mass Sign | VarChar | 1 | - | + | `+` = Positive<br>`-` = Negative |
| 18 | `SupplMass` | Supplementary Mass | Num | 19.6 | - |  |  |
| 19 | `SupplUnit` | Supplementary Unit | nVarChar | 50 | - |  |  |
| 20 | `ValueSgn` | Value Sign | VarChar | 1 | - | + | `+` = Positive<br>`-` = Negative |
| 21 | `Value` | Value | Num | 19.6 | - |  |  |
| 22 | `ValueFC` | Value in Foreign Currency | Num | 19.6 | - |  |  |
| 23 | `FCCurrency` | Foreign Currency | nVarChar | 3 | - |  |  |
| 24 | `StatValSgn` | Statistical Value Sign | VarChar | 1 | - |  | `+` = Positive<br>`-` = Negative |
| 25 | `StatVal` | Statistical Value | Num | 19.6 | - |  |  |
| 26 | `ReturnID` | Return Identifier | VarChar | 1 | - |  |  |
| 27 | `Include` | Include Line in Report | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 28 | `IsChanged` | Changed Line Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `DstRegCry` | Destination Country - Region | nVarChar | 3 | - |  |  |
| 30 | `DstRegSta` | Destination Region State | nVarChar | 12 | - |  |  |
| 31 | `OriRegCry` | Origin Region Country | nVarChar | 3 | - |  |  |
| 32 | `OriRegSta` | Origin Region State | nVarChar | 12 | - |  |  |
| 33 | `BpVATregNo` | VAT Registration No. | nVarChar | 32 | - |  |  |
| 34 | `CtryOrig` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 35 | `Incoterms` | Incoterms | nVarChar | 12 | - |  |  |
| 36 | `NatOfTrans` | Nature of Transaction | nVarChar | 50 | - |  |  |
| 37 | `TransMode` | Transport Mode | nVarChar | 12 | - |  |  |
| 38 | `PortEnEx` | Port of Entry or Exit | nVarChar | 50 | - |  |  |
| 39 | `CustProc` | Custom Procedure | nVarChar | 50 | - |  |  |
| 40 | `StatProc` | Statistical Procedure | nVarChar | 50 | - |  |  |
| 41 | `DomFrgID` | Domestic/Foreign Identifier | VarChar | 1 | - |  |  |
| 42 | `ItemType` | Item Type | VarChar | 1 | - | I | `I` = Item<br>`S` = Service<br>`N` = Item Not Relevant to Intrastat |
| 43 | `CommCode` | Commodity Code | nVarChar | 12 | - |  |  |
| 44 | `SerCode` | Service Code | nVarChar | 12 | - |  |  |
| 45 | `SerSupplM` | Service Supply Method | VarChar | 1 | - | I | `I` = Immediate<br>`R` = To More Resumptions |
| 46 | `SerPymMeth` | Service Payment Method | VarChar | 1 | - | A | `A` = Accredited to Bank Account<br>`B` = Bank Transfer<br>`X` = Other |
| 47 | `CorrDate` | Correction Date | Date | 8 | - |  |  |
| 48 | `CorrSgn` | Correction Sign | VarChar | 1 | - | + | `+` = Positive<br>`-` = Negative |
| 49 | `ReferDoc` | Referenced Document | Int | 11 | - |  |  |
| 50 | `ReferDocNo` | Referenced Document No. | Int | 11 | - |  |  |
| 51 | `ReferItem` | Referred Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 52 | `RefDocLine` | Referenced Document Line | Int | 11 | - |  |  |
| 53 | `ChgID` | Changed Data Record ID | nVarChar | 16 | - |  |  |
| 54 | `ChgUser` | Changed By | nVarChar | 50 | - |  |  |
| 55 | `ChgTimest` | Time Stamp of Change | Date | 8 | - |  |  |
| 56 | `Deleted` | Deleted Indicator | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 57 | `CstSecRc` | Custom Section | nVarChar | 6 | - |  |  |
| 58 | `CorrMonth` | Ref. Mo. of Summary to Correct | Int | 6 | - |  |  |
| 59 | `CorrYear` | Ref. Yr of Summary to Correct | Int | 6 | - |  |  |
| 60 | `CorrDeclNo` | No. of Declaration to Correct | Int | 11 | - |  |  |
| 61 | `CorRowNo` | Row No. Inside Sec. 3 to Correct | Int | 11 | - |  |  |
| 62 | `DeclRowNo` | Declaration File Row No. | Int | 11 | - |  |  |
| 63 | `CorrType` | Referred Type of Receipt | Int | 11 | - |  |  |
| 64 | `CntryPay` | State Code for Payment | nVarChar | 3 | - |  |  |
| 65 | `Triangular` | Triangular Trade | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 66 | `CardName` | Business Partner Name | nVarChar | 200 | - |  |  |
| 67 | `StatCode` | Statistical Code | nVarChar | 2 | - |  |  |
| 68 | `DocEntry` | Document Entry | Int | 11 | - |  |  |
| 69 | `NetValue` | Net Value | Num | 19.6 | - |  |  |
| 70 | `NetValueFC` | Net Value in FC | Num | 19.6 | - |  |  |
| 71 | `Freight` | Freight Sum | Num | 19.6 | - |  |  |
| 72 | `FreighFC` | Freight Sum in FC | Num | 19.6 | - |  |  |
| 73 | `RateFC` | Currency Rate for FC | Num | 19.6 | - |  |  |
| 74 | `Remarks` | Remarks | nVarChar | 250 | - |  |  |
| 75 | `ProtocolN` | Protocol Number | Int | 11 | - |  |  |
| 76 | `DropShip` | Drop-Ship | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `WhsZipCode` | Warehouse Zip Code | nVarChar | 20 | - |  |  |
| 78 | `ValBefDsc` | Value Before Discount | Num | 19.6 | - |  |  |
| 79 | `CoOQty` | Country of Origin Quantity | Num | 19.6 | - |  |  |
| 80 | `CoOLineNum` | CoO Line Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizAbsEnt, Line |
