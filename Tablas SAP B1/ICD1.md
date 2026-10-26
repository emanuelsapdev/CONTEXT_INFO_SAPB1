# ICD1 - Inventory Counting Draft - Rows

- **Tabla:** ICD1
- **Descripción:** Inventory Counting Draft - Rows
- **Cantidad de campos:** 43
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ICD1.html

## Campos (43)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OICD](OICD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemDesc` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `Freeze` | Item Freeze Status | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 7 | `InWhsQty` | In-Whse Qty on Count Date | Num | 19.6 | - |  |  |
| 8 | `Counted` | Counted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `CountQty` | Counted Quantity | Num | 19.6 | - |  |  |
| 10 | `CountQtyT1` | Counter 1 - Counted Quantity | Num | 19.6 | - |  |  |
| 11 | `CountQtyT2` | - | Num | 19.6 | - |  |  |
| 12 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 13 | `BarCode` | Bar Code | nVarChar | 254 | - |  |  |
| 14 | `InvUoM` | Inventory UoM | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `Difference` | Difference | Num | 19.6 | - |  |  |
| 16 | `DiffPercen` | Difference % | Num | 19.6 | - |  |  |
| 17 | `CountDate` | Count Date | Date | 8 | - |  |  |
| 18 | `CountTime` | Count Time | Int | 11 | - |  |  |
| 19 | `TargetRef` | Target Document Reference | nVarChar | 16 | - |  |  |
| 20 | `TargetType` | Target Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`10000071` = Inventory Posting |
| 21 | `TargetEntr` | Target Document Internal ID | Int | 11 | - |  |  |
| 22 | `TargetLine` | Target Document Row | Int | 11 | - |  |  |
| 23 | `ProjCode` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 24 | `OcrCode` | Distribution Rule Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 25 | `LineStatus` | Row Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 26 | `BinEntry` | Bin Location Entry | Int | 11 | [OBIN](OBIN.md) |  |  |
| 27 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 28 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 29 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 31 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 32 | `FirmCode` | Manufacturer | Int | 6 | [OMRC](OMRC.md) |  |  |
| 33 | `SuppCatNum` | Mfr Catalog No. | nVarChar | 50 | - |  |  |
| 34 | `PrefVendor` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 35 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 36 | `UgpEntry` | UoM Group Entry | Int | 11 | [OUGP](OUGP.md) |  |  |
| 37 | `IUomEntry` | Inventory UoM Entry | nVarChar | 20 | [OUOM](OUOM.md) |  |  |
| 38 | `CountDiff` | Counters' Diff. | Num | 19.6 | - |  |  |
| 39 | `CountDiffP` | Counters' Diff. (%) | Num | 19.6 | - |  |  |
| 40 | `UomCode` | UoM Code for DI | nVarChar | 20 | - |  |  |
| 41 | `UomQty` | UoM Counted Qty for DI | Num | 19.6 | - |  |  |
| 42 | `PPTaxExRe` | Plastic Packaging Tax Exemption Reason | nVarChar | 2 | - |  |  |
| 43 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
