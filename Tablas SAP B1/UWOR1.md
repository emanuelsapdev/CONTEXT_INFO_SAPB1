# UWOR1 - Production Order - Rows

- **Tabla:** UWOR1
- **Descripción:** Production Order - Rows
- **Cantidad de campos:** 46
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UWOR1.html

## Campos (46)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal Number | Int | 11 | [OWOR](OWOR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 4 | `BaseQty` | Base Quantity | Num | 19.6 | - |  |  |
| 5 | `PlannedQty` | Planned Quantity - Rows | Num | 19.6 | - |  |  |
| 6 | `IssuedQty` | Issued Quantity | Num | 19.6 | - |  |  |
| 7 | `IssueType` | Production Order Issue Type | VarChar | 1 | - |  | `M` = Manual<br>`B` = Backflush |
| 8 | `wareHouse` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 9 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 10 | `WipActCode` | WIP Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `CompTotal` | Total Completed Sum | Num | 19.6 | - |  |  |
| 12 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 13 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 15 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 16 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 17 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 18 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 19 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 20 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) | 0 |  |
| 21 | `UomCode` | UoM Code | nVarChar | 20 | - |  |  |
| 22 | `ItemType` | Item Type | Int | 11 | - | 4 | `4` = Item<br>`290` = Resource<br>`-18` = Text |
| 23 | `AdditQty` | Additional Quantity | Num | 19.6 | - |  |  |
| 24 | `LineText` | Row Text | Text | 16 | - |  |  |
| 25 | `PickStatus` | Pick Status | VarChar | 1 | - | N | `Y` = Picked<br>`N` = Not Picked<br>`R` = Release for Picking<br>`P` = Partially Picked |
| 26 | `PickQty` | Pick Quantity | Num | 19.6 | - |  |  |
| 27 | `PickIdNo` | Pick List ID Number | Int | 11 | - |  |  |
| 28 | `ReleaseQty` | Released Quantity | Num | 19.6 | - |  |  |
| 29 | `ResAlloc` | Resource Allocation | VarChar | 1 | - |  | `S` = On Start Date<br>`D` = On End Date<br>`F` = Start Date Forwards<br>`B` = End Date Backwards |
| 30 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 31 | `EndDate` | End Date | Date | 8 | - |  |  |
| 32 | `StageId` | Stage ID | Int | 11 | - |  |  |
| 33 | `BaseQtyNum` | Base Quantity Numerator | Num | 19.6 | - |  |  |
| 34 | `BaseQtyDen` | Base Quantity Denominator | Num | 19.6 | - |  |  |
| 35 | `ReqDays` | Required Days | Num | 19.6 | - | 0 |  |
| 36 | `RtCalcProp` | Routing Calculation Proportion | Num | 19.6 | - | 100 |  |
| 37 | `Status` | Stage Status | VarChar | 1 | - | P | `P` = Planned<br>`I` = In Progress<br>`C` = Complete |
| 38 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 39 | `AlwProcDoc` | Allow Procurement Doc. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `PoDocType` | Procmnt Doc. Type | Int | 11 | - |  |  |
| 41 | `PoDocNum` | Procmnt Doc. No. | Int | 11 | - |  |  |
| 42 | `PoDocEntry` | Procmnt Doc. Internal ID | Int | 11 | - |  |  |
| 43 | `PoLineNum` | Procmnt Doc. Row No. | Int | 11 | - |  |  |
| 44 | `PoQuantity` | Procmnt Quantity | Num | 19.6 | - |  |  |
| 45 | `PPTaxExRe` | Plastic Packaging Tax Exemption Reason | nVarChar | 2 | - |  |  |
| 46 | `PlPaWght` | Plastic Packaging Weight | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| VISORDER | Yes | DocEntry, VisOrder |
| ITEM_WHS | No | ItemCode, wareHouse |
