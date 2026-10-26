# WTQ10 - Inventory Transfer Request - Row Structure

- **Tabla:** WTQ10
- **Descripción:** Inventory Transfer Request - Row Structure
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTQ10.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | [OWTQ](OWTQ.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `AftLineNum` | After Row Number | Int | 11 | - |  |  |
| 4 | `OrderNum` | Order Number | Int | 11 | - |  |  |
| 5 | `LineType` | Row Type | VarChar | 1 | - |  | `T` = Text<br>`S` = Subtotal |
| 6 | `LineText` | Row Text | Text | 16 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1250000001 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineSeq |
| SECONDARY | Yes | DocEntry, AftLineNum, OrderNum |
