# SIVL1 - IVL Layer Level

- **Tabla:** SIVL1
- **Descripción:** IVL Layer Level
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SIVL1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransSeq` | Transaction Sequence No. | Int | 11 | [OIVL](OIVL.md) |  |  |
| 2 | `LayerID` | Layer ID | Int | 11 | - |  |  |
| 3 | `CalcPrice` | Calculated Price | Num | 19.6 | - |  |  |
| 4 | `Balance` | Stock Balance | Num | 19.6 | - |  |  |
| 5 | `TransValue` | Transaction Value | Num | 19.6 | - |  |  |
| 6 | `LayerInQty` | Receipt Quantity | Num | 19.6 | - |  |  |
| 7 | `LayerOutQ` | Issue Quantity | Num | 19.6 | - |  |  |
| 8 | `RevalTotal` | Inventory Revaluation Total | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TransSeq, LayerID |
