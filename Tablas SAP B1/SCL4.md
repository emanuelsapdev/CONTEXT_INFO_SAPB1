# SCL4 - Expense Documents

- **Tabla:** SCL4
- **Descripción:** Expense Documents
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCL4.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrcvCallID` | Service Call No. | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `Line` | Row | Int | 6 | - | -1 |  |
| 3 | `PartType` | Part Type | VarChar | 1 | - | I | `I` = Inventory<br>`N` = Travel/Labor |
| 4 | `DocAbs` | Document Internal Number | Int | 11 | - |  |  |
| 5 | `Object` | Document Type | nVarChar | 20 | - | 13 | `13` = A/R Invoice<br>`15` = Delivery<br>`16` = Returns<br>`67` = Inventory Transfer<br>`14` = A/R Credit Memo<br>`165` = A/R Correction Invoice<br>`0`<br>`17` = Sales Order<br>`23` = Sales Quotation<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`21` = Goods Return<br>`234000032` = Goods Return Request<br>`234000031` = Return Request |
| 6 | `DocPstDate` | Document Posting Date | Date | 8 | - |  |  |
| 7 | `ObjectType` | Object Type | nVarChar | 20 | - | 191 |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UserSign2` | User Signature 2 | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 13 | `DocNumber` | Document No. | Int | 11 | - |  |  |
| 14 | `Transfered` | Transfered | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 16 | `StckTrnDir` | Inventory Transaction Direction | VarChar | 1 | - |  | `T` = Transfer to Technician<br>`N` = Transfer from Technician |
| 17 | `Instance` | Instance | Int | 6 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrcvCallID, Line, PartType, DocAbs, Object |
