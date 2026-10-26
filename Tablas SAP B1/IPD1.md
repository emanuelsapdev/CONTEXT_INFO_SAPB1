# IPD1 - Inventory Posting Draft - Rows

- **Tabla:** IPD1
- **Descripción:** Inventory Posting Draft - Rows
- **Cantidad de campos:** 54
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IPD1.html

## Campos (54)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OIPD](OIPD.md) |  |  |
| 2 | `DocLineNum` | Row Number in Document | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `InvntryUom` | Inventory UoM | nVarChar | 100 | - |  |  |
| 6 | `OnHandBef` | Quantity Stored in Warehouse | Num | 19.6 | - |  |  |
| 7 | `Price` | Price | Num | 19.6 | - |  |  |
| 8 | `Quantity` | Quantity - Delta | Num | 19.6 | - |  |  |
| 9 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 10 | `Rate` | Currency Price | Num | 19.6 | - |  |  |
| 11 | `IOffIncAcc` | Inventory Offset Increase Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `DOffDecAcc` | Inventory Offset Decrease Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 15 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 16 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 17 | `DocTotalSy` | Document Total (SC) | Num | 19.6 | - |  |  |
| 18 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `ObjType` | Object Type | nVarChar | 20 | - | 10000071 |  |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 24 | `BarCode` | Bar Code | nVarChar | 254 | - |  |  |
| 25 | `InvUoM` | Inventory UoM | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 26 | `BinEntry` | Bin Location Entry | Int | 11 | [OBIN](OBIN.md) |  |  |
| 27 | `FirmCode` | Manufacturer | Int | 6 | [OMRC](OMRC.md) |  |  |
| 28 | `SuppCatNum` | Mfr Catalog No. | nVarChar | 50 | - |  |  |
| 29 | `CardCode` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 30 | `CountDate` | Count Date | Date | 8 | - |  |  |
| 31 | `CountTime` | Count Time | Int | 11 | - |  |  |
| 32 | `DiffPercnt` | Percentage Difference | Num | 19.6 | - |  |  |
| 33 | `BaseRef` | Base Document Reference | nVarChar | 16 | - |  |  |
| 34 | `BaseType` | Base Document Type | Int | 11 | - | 1470000065 | `-1`<br>`1470000065` = Inventory Counting |
| 35 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 36 | `BaseLine` | Base Row | Int | 11 | - |  |  |
| 37 | `CountQty` | Counted Quantity | Num | 19.6 | - |  |  |
| 38 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 39 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 40 | `CpyCount` | Copied Count | Int | 11 | - | 0 | `0`<br>`1` = Inventory Taker One<br>`2` = Two Takers - Taker 1<br>`3` = Two Takers - Taker 2<br>`4` = Two Takers - Items with Zero Difference |
| 41 | `BinNegQty` | Allow Bin Negative Quantity | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 43 | `UgpEntry` | UoM Group Entry | Int | 11 | [OUGP](OUGP.md) |  |  |
| 44 | `IUomEntry` | Inventory UoM Entry | nVarChar | 20 | [OUOM](OUOM.md) |  |  |
| 45 | `UomCode` | UoM Code for DI | nVarChar | 20 | - |  |  |
| 46 | `ItmsPerUnt` | Items per Unit for DI | Num | 19.6 | - |  |  |
| 47 | `UomQty` | UoM Counted Qty for DI | Num | 19.6 | - |  |  |
| 48 | `ActPrice` | Actual Price | Num | 19.6 | - |  |  |
| 49 | `PostValueL` | Posted Value LC | Num | 19.6 | - |  |  |
| 50 | `PostValueS` | Posted Value SC | Num | 19.6 | - |  |  |
| 51 | `PPTaxExRe` | Plastic Packaging Tax Exemption Reason | nVarChar | 2 | - |  |  |
| 52 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |
| 53 | `UomNum` | Uom Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 54 | `UomDen` | Uom Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, DocLineNum |
| ITEM_CODE | No | ItemCode |
