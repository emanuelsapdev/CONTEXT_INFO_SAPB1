# PHA4 - Project Management - Stages - Documents

- **Tabla:** PHA4
- **Descripción:** Project Management - Stages - Documents
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PHA4.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [PHA1](PHA1.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 4 | `TYP` | Document Type | Int | 11 | - | -1 | `-1` = Please select<br>`112` = Document Draft<br>`30` = Manual Journal Entry<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`16` = Return<br>`203002` = A/R Down Payment Request<br>`203` = A/R Down Payment Invoice<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`13002` = A/R Reserve Invoice<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`204002` = A/P Down Payment Request<br>`204` = A/P Down Payment Invoice<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`18002` = A/P Reserve Invoice<br>`191` = Service Call<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`1470000113` = Purchase Request<br>`234000032` = Goods Return Request<br>`234000031` = Return Request |
| 5 | `DOCNUM` | Document Number | Int | 11 | - |  |  |
| 6 | `DocEntry` | Document Abs. Entry | Int | 11 | - |  |  |
| 7 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 8 | `Total` | Total | Num | 19.6 | - |  |  |
| 9 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 10 | `Status` | Line status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `AmountCat` | Category to which we will apply the amount from Total | VarChar | 1 | - |  | `I` = Invoiced<br>`O` = Open |
| 13 | `Categorize` | Category Open Amount/Invoiced A/R, A/P to which we will apply the amount from journal entry | nVarChar | 2 | - |  | Ignore<br>`OP` = Open Amount (A/P)<br>`OR` = Open Amount (A/R)<br>`IP` = Invoiced (A/P)<br>`IR` = Invoiced (A/R) |
| 14 | `Operation` | Operation which we will apply to the amount from the total | VarChar | 1 | - |  | Ignore<br>`A` = Add<br>`S` = Subtract |
| 15 | `Chargeable` | Chargeable [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `Charged` | Charged | Num | 19.6 | - |  |  |
| 17 | `ChargedQty` | Charged Quantity | Num | 19.6 | - |  |  |
| 18 | `DocType` | Document Type | VarChar | 1 | - | I | `I` = Item<br>`S` = Service |
| 19 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 20 | `PartTotal` | Partially Invoiced Total | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
| DOCUMENT | No | DocType, DocEntry, LineNum |
