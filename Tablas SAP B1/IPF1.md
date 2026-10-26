# IPF1 - Landed Costs - Rows

- **Tabla:** IPF1
- **Descripción:** Landed Costs - Rows
- **Cantidad de campos:** 116
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IPF1.html

## Campos (116)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Landed Costs Internal ID | Int | 11 | [OIPF](OIPF.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`20` = Goods Receipt PO<br>`69` = Landed Costs<br>`18` = A/P Invoice |
| 4 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 5 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 6 | `Dscription` | Item Description | nVarChar | 200 | - |  |  |
| 7 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 8 | `PriceFOB` | Base Doc. Price | Num | 19.6 | - |  |  |
| 9 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 10 | `Rate` | Currency Price | Num | 19.6 | - |  |  |
| 11 | `Custom` | Projected Customs | Num | 19.6 | - |  |  |
| 12 | `CustomFC` | Projected Customs (FC) | Num | 19.6 | - |  |  |
| 13 | `Cost` | Expenditure | Num | 19.6 | - |  |  |
| 14 | `CostFC` | Freight (FC) | Num | 19.6 | - |  |  |
| 15 | `PriceAtWH` | Whse Price | Num | 19.6 | - |  |  |
| 16 | `PricAtWHFC` | Whse Price (FC) | Num | 19.6 | - |  |  |
| 17 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 18 | `TotalFrgn` | Row Total (FC) | Num | 19.6 | - |  |  |
| 19 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 20 | `UnitCode` | Volume UoM | Int | 6 | [OLGT](OLGT.md) |  |  |
| 21 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 22 | `UnitCode1` | Unit of Weight 1 | Int | 6 | [OWGT](OWGT.md) |  |  |
| 23 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 24 | `UnitCode2` | Unit of Weight 2 | Int | 6 | [OWGT](OWGT.md) |  |  |
| 25 | `CardCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 26 | `Reference` | Reference | nVarChar | 16 | - |  |  |
| 27 | `OrigLine` | Base Line Number | Int | 11 | - |  |  |
| 28 | `FactNoCust` | Factor Without Customs | Num | 19.6 | - |  |  |
| 29 | `FacWthCust` | Factor with Customs | Num | 19.6 | - |  |  |
| 30 | `PriceList` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 31 | `CostOH` | Cost Surcharge | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 32 | `StockEval` | Use for Inventory Valuation | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 33 | `UseBaseUn` | Inventory UoM | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 34 | `BlockNum` | Block No. | nVarChar | 100 | - |  |  |
| 35 | `ImportLog` | Import Log | nVarChar | 20 | - |  |  |
| 36 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 37 | `OrigRow` | Original Row | Int | 11 | - |  |  |
| 38 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 39 | `OrigWhs` | Original Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 40 | `ReleaseNum` | Release Number | Int | 11 | - |  |  |
| 41 | `VarCosts` | Variant Costs | Num | 19.6 | - |  |  |
| 42 | `ConstCosts` | Fixed Costs | Num | 19.6 | - |  |  |
| 43 | `VarCostsFR` | Variant Costs (FC) | Num | 19.6 | - |  |  |
| 44 | `CnstCostFR` | Fixed Costs (FC) | Num | 19.6 | - |  |  |
| 45 | `UserCustom` | User Expected Custom | Num | 19.6 | - |  |  |
| 46 | `UsrCusomFC` | User Expected Foreign Custom | Num | 19.6 | - |  |  |
| 47 | `FobValue` | Base Doc. Value Row Total (LC) | Num | 19.6 | - |  |  |
| 48 | `FobValueFC` | Base Doc. Value Row Total (FC) | Num | 19.6 | - |  |  |
| 49 | `TtlExpndLC` | Allocated Unit Costs Row Total | Num | 19.6 | - |  |  |
| 50 | `TtlExpndFC` | Allocated Unit Costs Row Total | Num | 19.6 | - |  |  |
| 51 | `TtlCustLC` | Allocated Unit Costs Row Total | Num | 19.6 | - |  |  |
| 52 | `TtlCustFC` | Allocated Unit Costs Row Total | Num | 19.6 | - |  |  |
| 53 | `TtlCostLC` | Row Ttl Cust + Alloc Costs LC | Num | 19.6 | - |  |  |
| 54 | `TtlCostFC` | Row Ttl Cust + Alloc Costs FC | Num | 19.6 | - |  |  |
| 55 | `TtlVolume` | Volume Row Total | Num | 19.6 | - |  |  |
| 56 | `TtlWeight` | Weight Row Total | Num | 19.6 | - |  |  |
| 57 | `BaseRowNum` | use IPF1_BASE_LINE_NUM instead | Int | 11 | - |  |  |
| 58 | `TtlCustSC` | Ttl Row Projected Customs (SC) | Num | 19.6 | - |  |  |
| 59 | `TtlExpndSC` | Allocated Costs Row Total (SC) | Num | 19.6 | - |  |  |
| 60 | `OriBAbsEnt` | Original Base Doc. Internal ID | Int | 11 | - | -1 |  |
| 61 | `OriBLinNum` | Original Base Doc. Row No. | Int | 11 | - | -1 |  |
| 62 | `TargetDoc` | Target Document Internal No. | Int | 11 | - |  |  |
| 63 | `FobValCurr` | Base Doc. Value Currency | nVarChar | 3 | - |  |  |
| 64 | `FobnLaC` | FOB and Included Costs (LC) | Num | 19.6 | - |  |  |
| 65 | `FobnLaCFC` | FOB and Included Costs (FC) | Num | 19.6 | - |  |  |
| 66 | `NumPerMsr` | UoM Value | Num | 19.6 | - |  |  |
| 67 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 68 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 69 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 70 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 71 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 72 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 73 | `OriBDocTyp` | Original Base Document Type | nVarChar | 11 | - | -1 | `-1`<br>`18` = A/P Invoice<br>`20` = Goods Receipt PO |
| 74 | `CustRate` | Custom Group Rate | Num | 19.6 | - |  |  |
| 75 | `LFixCost` | Locked Fixed Cost | Num | 19.6 | - |  |  |
| 76 | `LFixCostFC` | Locked Fixed Cost (FC) | Num | 19.6 | - |  |  |
| 77 | `LVarCost` | Locked Variable Cost | Num | 19.6 | - |  |  |
| 78 | `LVarCostFC` | Locked Variable Cost (FC) | Num | 19.6 | - |  |  |
| 79 | `CstmsRate` | Customs Rate | Num | 19.6 | - |  |  |
| 80 | `VatGroup` | VAT Code | nVarChar | 8 | - |  |  |
| 81 | `VatPrcnt` | VAT Rate per Row | Num | 19.6 | - |  |  |
| 82 | `VatSum` | Total of VAT | Num | 19.6 | - |  |  |
| 83 | `SnbType` | Batch or Serial Type | nVarChar | 20 | - | -1 | `-1`<br>`10000045` = Serial<br>`10000044` = Batch |
| 84 | `SnbAbsEnt` | SnB Abs. Entry | Int | 11 | - | -1 |  |
| 85 | `SysNumber` | System Number | Int | 11 | - |  |  |
| 86 | `DistNumber` | Distinct Number | nVarChar | 36 | - |  |  |
| 87 | `ExciseSum` | Sum of Excise | Num | 19.6 | - |  |  |
| 88 | `ExcisSumFC` | Sum of Excise - FC | Num | 19.6 | - |  |  |
| 89 | `ExcInStk` | Is Excise in Stock | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `CustomSum` | Sum of Customs Cost | Num | 19.6 | - |  |  |
| 91 | `CustSumFC` | Sum of Customs Cost in FC | Num | 19.6 | - |  |  |
| 92 | `CstmInStk` | Is Customs in Stock | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 93 | `CstmVatSum` | Sum of Customs Cost VAT | Num | 19.6 | - |  |  |
| 94 | `CstmVatFC` | Sum of Customs Cost VAT in FC | Num | 19.6 | - |  |  |
| 95 | `CstmVatStk` | Is Customs VAT in Stock | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 96 | `CCDEntry` | CCD Abs. Entry | Int | 11 | - |  |  |
| 97 | `CCDNumber` | Number of CCD | nVarChar | 20 | - |  |  |
| 98 | `ExcisSumSC` | Sum of Excise - SC | Num | 19.6 | - |  |  |
| 99 | `CustSumSC` | Sum of Customs Cost in SC | Num | 19.6 | - |  |  |
| 100 | `CstmVatSC` | Sum of Customs Cost VAT in SC | Num | 19.6 | - |  |  |
| 101 | `InvQty` | Inventory Quantity | Num | 19.6 | - |  |  |
| 102 | `CCDLineNum` | CCD Row Number | Int | 11 | - |  |  |
| 103 | `TtlVolCCM` | Volume Row Total per CCM | Num | 19.6 | - |  |  |
| 104 | `ExcImpQty` | Excise Imported Quantity | Num | 19.6 | - |  |  |
| 105 | `ExcFixAmnt` | Excise Fixed Amount | Num | 19.6 | - |  |  |
| 106 | `ExcRate` | Excise Rate | Num | 19.6 | - |  |  |
| 107 | `ExcAmntUoM` | Excise Amount UoM | Num | 19.6 | - |  |  |
| 108 | `ExcAmntAdV` | Excise Amount Ad Valorem | Num | 19.6 | - |  |  |
| 109 | `ExcImpQUoM` | Excise Imported Quantity UoM | Int | 11 | - |  | `112` = Liters, m3<br>`168` = Tonne, metric ton (1000 kg)<br>`251` = Horsepower (1 hp = 0.75 kW)<br>`831` = Liters of anhydrous (pure) alcohol |
| 110 | `ExcBasAmnt` | Excise Base Amount | Num | 19.6 | - |  |  |
| 111 | `LineNumV3` | Target VAT Row Number in IPF3 | Int | 11 | [IPF3](IPF3.md) |  |  |
| 112 | `FobVal2` | Corrected Base Doc. Value Row Total (LC) | Num | 19.6 | - | 0 |  |
| 113 | `FobVal2FC` | Corrected Base Doc. Value Row Total (FC) | Num | 19.6 | - | 0 |  |
| 114 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 115 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 116 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| BASE | No | BaseEntry, OrigLine |
| ITEM | No | BaseEntry, ItemCode |
| CURRENCY | No | Currency |
| BASE_LINE | No | BaseType, BaseEntry, OrigLine |
