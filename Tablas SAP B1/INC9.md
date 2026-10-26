# INC9 - Inventory Counting - Individual Counters - Row Counted Qty

- **Tabla:** INC9
- **Descripción:** Inventory Counting - Individual Counters - Row Counted Qty
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/INC9.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OINC](OINC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `CounterNum` | Counter Number | Int | 11 | - |  |  |
| 4 | `TotalQty` | Total Qty of Inventory UoM | Num | 19.6 | - |  |  |
| 5 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, CounterNum |
