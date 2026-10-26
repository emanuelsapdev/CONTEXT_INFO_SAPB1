# GPA5 - Product Cost Adjustment - Recalculation of Product Cost

- **Tabla:** GPA5
- **Descripción:** Product Cost Adjustment - Recalculation of Product Cost
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA5.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `Selected` | Choose | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `LnType` | Choose | VarChar | 1 | - | O | `P` = Product Serial/Batch Line<br>`O` = Production Order Line |
| 5 | `ProdCode` | Product Code | nVarChar | 50 | - |  |  |
| 6 | `ProdDescr` | Product Description | nVarChar | 200 | - |  |  |
| 7 | `PODocAbs` | PO Document Abs. Entry | Int | 11 | - |  |  |
| 8 | `PODocNum` | PO Document Number | Int | 11 | - |  |  |
| 9 | `DocType` | Choose | VarChar | 1 | - | I | `I` = Issue for Production<br>`R` = Receipt from Production |
| 10 | `DocAbs` | Document Abs. Entry | Int | 11 | - |  |  |
| 11 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 12 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 13 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 14 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 15 | `ItemDescr` | Item Description | nVarChar | 200 | - |  |  |
| 16 | `DistNumber` | Batch Number | nVarChar | 36 | - |  |  |
| 17 | `SnBAbs` | SnB Abs. Entry | Int | 11 | - |  |  |
| 18 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers<br>`-1` |
| 19 | `LnQty` | Line Quantity | Num | 19.6 | - |  |  |
| 20 | `SnBQty` | Serial/Batch Quantity | Num | 19.6 | - |  |  |
| 21 | `LnCost` | Line Cost | Num | 19.6 | - |  |  |
| 22 | `DebCred` | Debited or Credited | VarChar | 1 | - | D | `D` = Debited<br>`C` = Credited |
| 23 | `LnTotal` | Line Total | Num | 19.6 | - |  |  |
| 24 | `SnBTotal` | SnB Total | Num | 19.6 | - |  |  |
| 25 | `SBAccTotal` | Serial/Batch Accumulated Total | Num | 19.6 | - |  |  |
| 26 | `SBAccQty` | Serial/Batch Accumulated Quantity | Num | 19.6 | - |  |  |
| 27 | `ACAccTotal` | Actual Cost Accumulated Total | Num | 19.6 | - |  |  |
| 28 | `ACAccQty` | Actual Cost Accumulated Quantity | Num | 19.6 | - |  |  |
| 29 | `Applied` | Applied Adjustment | Num | 19.6 | - |  |  |
| 30 | `Variance` | Variance to Apply | Num | 19.6 | - |  |  |
| 31 | `MRVAdjust` | MRV Adjustment | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
