# INC6 - Inventory Counting - Team Counter - Row UoM

- **Tabla:** INC6
- **Descripción:** Inventory Counting - Team Counter - Row UoM
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/INC6.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OINC](OINC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ChildNum` | Child Number | Int | 11 | - |  |  |
| 4 | `CounterNum` | Counter Number | Int | 11 | - |  |  |
| 5 | `UomQty` | UoM Counted Qty | Num | 19.6 | - |  |  |
| 6 | `InvtQty` | Counted Qty of Inventory UoM | Num | 19.6 | - |  |  |
| 7 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, ChildNum, CounterNum |
