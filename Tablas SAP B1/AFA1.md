# AFA1 - Asset Document - Rows

- **Tabla:** AFA1
- **Descripción:** Asset Document - Rows
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AFA1.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [AFAD](AFAD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `LineTotal` | Line Total | Num | 19.6 | - |  |  |
| 7 | `TotalFrgn` | Line Total (FC) | Num | 19.6 | - |  |  |
| 8 | `TotalSys` | Line Total (SC) | Num | 19.6 | - |  |  |
| 9 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 10 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `NewItemCod` | New Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 13 | `Partial` | Partial | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `APC` | APC | Num | 19.6 | - |  |  |
| 15 | `NewAstCls` | New Asset Class | nVarChar | 20 | [OACS](OACS.md) |  |  |
| 16 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 17 | `TransType` | Transaction Type | nVarChar | 4 | - |  | `0` = Unknown<br>`110` = Acquisition<br>`115` = Subacquisition<br>`120` = Credit Memo<br>`130` = APC Write-Up<br>`210` = Full Retirement<br>`220` = Full Scrapping<br>`230` = Partial Retirement<br>`240` = Partial Scrapping<br>`310` = Full Transfer<br>`320` = Partial Transfer<br>`410` = Manual Ordinary Depreciation<br>`420` = Manual Unplanned Depreciation<br>`430` = Manual Special Depreciation<br>`440` = Appreciation<br>`510` = Change of Depreciation Type<br>`520` = Change of Useful Life<br>`530` = Change of Depreciation Start Date<br>`540` = Change of Salvage Value |
| 18 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, LogInstanc, ObjType |
