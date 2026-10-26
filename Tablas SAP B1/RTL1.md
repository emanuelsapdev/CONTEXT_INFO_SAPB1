# RTL1 - Resource Transaction Log

- **Tabla:** RTL1
- **Descripción:** Resource Transaction Log
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTL1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Log Entry ID | Int | 11 | - |  |  |
| 2 | `StdCostNum` | Resource Standard Cost Number | Int | 11 | - |  |  |
| 3 | `BaseLogEnt` | Base Log Entry ID | Int | 11 | [ORTL](ORTL.md) | -1 |  |
| 4 | `DocQty` | Doc. Quantity | Num | 19.6 | - |  |  |
| 5 | `Price` | Price | Num | 19.6 | - |  |  |
| 6 | `Total` | Total | Num | 19.6 | - |  |  |
| 7 | `OpenTotal` | Open Total | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry, StdCostNum, BaseLogEnt |
