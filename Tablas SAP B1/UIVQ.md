# UIVQ - FIFO Queue Working Table

- **Tabla:** UIVQ
- **Descripción:** FIFO Queue Working Table
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIVQ.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TreeID` | Tree ID | Int | 11 | - | 0 |  |
| 2 | `ParentID` | Parent ID | Int | 11 | - | -1 |  |
| 3 | `LocType` | Location Type | Int | 6 | - |  |  |
| 4 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 5 | `TransSeq` | Transaction Sequence No. | Int | 11 | [UIVL](UIVL.md) |  |  |
| 6 | `LayerID` | Layer ID | Int | 11 | - |  |  |
| 7 | `OpenQty` | Open Quantity | Num | 19.6 | - |  |  |
| 8 | `OpenValue` | Open Value | Num | 19.6 | - |  |  |
| 9 | `ItemCode` | Item Code | nVarChar | 50 | [UITM](UITM.md) |  |  |
| 10 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 11 | `StockActio` | Stock Action Type | Int | 11 | - | -1 | `15` = Delivery<br>`16` = Returns<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt<br>`21` = Goods Return<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`-2` = Opening Balance<br>`58` = Inventory Update<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfer<br>`68` = Work Instructions<br>`-1` = All Transactions<br>`162` = Inventory Revaluation<br>`69` = Landed Costs |
| 12 | `RemMethod` | Quantity Removal Method | VarChar | 1 | - | U | `U` = Unspecified<br>`I` = Issue<br>`R` = Revaluation |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| TRANS_SEQ | Yes | TransSeq, LayerID |
| TreeOpenQt | No | TreeID, OpenQty |
