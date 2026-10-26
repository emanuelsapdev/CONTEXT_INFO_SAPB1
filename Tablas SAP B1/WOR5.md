# WOR5 - Production Order - Document Reference Information

- **Tabla:** WOR5
- **Descripción:** Production Order - Document Reference Information
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WOR5.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal Number | Int | 11 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - | 202 |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 5 | `RefDocEntr` | Referenced Internal Number | Int | 11 | - |  |  |
| 6 | `RefDocNum` | Referenced Document Number | Int | 11 | - |  |  |
| 7 | `ExtDocNum` | External Referenced Document Number | nVarChar | 100 | - |  |  |
| 8 | `RefObjType` | Referenced Object Type | nVarChar | 20 | - |  | `23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery Notes<br>`234000031` = Return Request<br>`16` = Return<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`165` = A/R Correction Invoice<br>`280` = A/R Tax Invoice<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`163` = A/P Correction Invoice<br>`281` = A/P Tax Invoice<br>`69` = Landed Costs<br>`24` = Incoming Payments<br>`46` = Outgoing Payments<br>`57` = Checks for Payment<br>`321` = Internal Reconciliation<br>`34` = Recurring Posting<br>`30` = Journal Entry<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`162` = Inventory Revaluation<br>`1470000065` = Inventory Counting<br>`10000071` = Inventory Posting<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`202` = Production Order<br>`13001` = Original Invoice<br>`-1` = External Document |
| 9 | `IssueDate` | Date of Issue | Date | 8 | - |  |  |
| 10 | `Remark` | Remarks | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| DOC_ENTRY | No | DocEntry |
