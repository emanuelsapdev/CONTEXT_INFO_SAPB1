# IQI1 - Inventory Opening Balance - Rows

- **Tabla:** IQI1
- **Descripción:** Inventory Opening Balance - Rows
- **Cantidad de campos:** 41
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IQI1.html

## Campos (41)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | - |  |  |
| 2 | `DocLineNum` | Row Number in Document | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `InvntryUom` | Inventory UoM | nVarChar | 100 | - |  |  |
| 6 | `OnHandBef` | Quantity Stored in Warehouse | Num | 19.6 | - |  |  |
| 7 | `Price` | Price | Num | 19.6 | - |  |  |
| 8 | `Quantity` | Opening Balance | Num | 19.6 | - |  |  |
| 9 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 10 | `Rate` | Currency Price | Num | 19.6 | - |  |  |
| 11 | `IOffIncAcc` | Inventory Offset Increase Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `DOffDecAcc` | Inventory Offset Decrease Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 15 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 16 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 17 | `DocTotalSy` | Document Total (SC) | Num | 19.6 | - |  |  |
| 18 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `ObjType` | Object Type | nVarChar | 20 | - | 310000001 |  |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 24 | `BarCode` | Bar Code | nVarChar | 254 | - |  |  |
| 25 | `InvUoM` | Inventory UoM | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 26 | `InvUoMQty` | Inventory UoM Qty | Num | 19.6 | - |  |  |
| 27 | `BinEntry` | Bin Location Entry | Int | 11 | [OBIN](OBIN.md) |  |  |
| 28 | `FirmCode` | Manufacturer | Int | 6 | [OMRC](OMRC.md) |  |  |
| 29 | `SuppCatNum` | Mfr Catalog No. | nVarChar | 50 | - |  |  |
| 30 | `CardCode` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 31 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 32 | `Location` | Location | Int | 11 | - |  |  |
| 33 | `ItmsGrpCod` | Item Group | Int | 6 | [OITB](OITB.md) | 100 |  |
| 34 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 35 | `BinNegQty` | Allow Bin Negative Quantity | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 37 | `ActPrice` | Actual Price | Num | 19.6 | - |  |  |
| 38 | `PostValueL` | Posted Value LC | Num | 19.6 | - |  |  |
| 39 | `PostValueS` | Posted Value SC | Num | 19.6 | - |  |  |
| 40 | `PPTaxExRe` | Plastic Packaging Tax Exemption Reason | nVarChar | 2 | - |  |  |
| 41 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, DocLineNum |
| ITEM_CODE | No | ItemCode |
