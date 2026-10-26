# MIN2 - Item Imformation of MI

- **Tabla:** MIN2
- **Descripción:** Item Imformation of MI
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MIN2.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MinvNum` | Monthly Invoice Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | nVarChar | 20 | - |  | `13` = A/R Invoice<br>`14` = A/R Credit Memo |
| 4 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 5 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 6 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 7 | `ItemName` | Item Name | nVarChar | 200 | - |  |  |
| 8 | `ItemPrice` | Item Price | Num | 19.6 | - |  |  |
| 9 | `ItemCurr` | Item Currency | nVarChar | 3 | - |  |  |
| 10 | `itemRate` | Currency Exchange Rate | Num | 19.6 | - |  |  |
| 11 | `ItemQuan` | Item Quantity | Num | 19.6 | - |  |  |
| 12 | `ItemType` | Item Type | VarChar | 1 | - | I | `I`<br>`E`<br>`D`<br>`R`<br>`T`<br>`S`<br>`P`<br>`W` |
| 13 | `ItemTotal` | Item Total | Num | 19.6 | - |  |  |
| 14 | `TaxAmount` | Tax Amount | Num | 19.6 | - |  |  |
| 15 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 16 | `Entry` | Monthly Invoice Entry | Int | 11 | [OMIN](OMIN.md) |  |  |
| 17 | `AbsEntry` | Document Entry | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Entry, DocType, AbsEntry, LineNum |
