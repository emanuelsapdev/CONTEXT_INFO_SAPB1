# WTQ14 - Inventory Transfer Request - Assembly - Rows

- **Tabla:** WTQ14
- **Descripción:** Inventory Transfer Request - Assembly - Rows
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTQ14.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | [OWTQ](OWTQ.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - | -1 |  |
| 3 | `ChildNum` | Child Number | Int | 11 | - | -1 |  |
| 4 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 6 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 7 | `TotalQty` | Total Quantity | Num | 19.6 | - |  |  |
| 8 | `OpenQty` | Remaining Open Quantity | Num | 19.6 | - |  |  |
| 9 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1250000001 |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `BaseChildN` | Base Child Number | Int | 11 | - | -1 |  |
| 12 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, ChildNum, LogInstanc, ObjectType |
