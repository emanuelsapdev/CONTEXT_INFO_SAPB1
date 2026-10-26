# SCL2 - Service Call Inventory Expenses

- **Tabla:** SCL2
- **Descripción:** Service Call Inventory Expenses
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCL2.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrcvCallID` | Service Call No. | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `Line` | Row | Int | 6 | - | -1 |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `TransToTec` | Transfer to Technican | Num | 19.6 | - |  |  |
| 6 | `Delivered` | Delivered | Num | 19.6 | - |  |  |
| 7 | `RetFromTec` | Returned from Technician | Num | 19.6 | - |  |  |
| 8 | `Returned` | Returned | Num | 19.6 | - |  |  |
| 9 | `Bill` | Bill | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `QtyToBill` | Quantity to Bill | Num | 19.6 | - |  |  |
| 11 | `QtyToInv` | Invoiced Qty | Num | 19.6 | - |  |  |
| 12 | `ObjectType` | Object Type | nVarChar | 20 | - | 191 |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 14 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 15 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 16 | `UserSign2` | User Signature 2 | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 18 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 19 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrcvCallID, Line |
