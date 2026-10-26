# RIT1 - Interest Rates

- **Tabla:** RIT1
- **Descripción:** Interest Rates
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RIT1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Object Code | nVarChar | 20 | [ORIT](ORIT.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Days` | Number of Tolerance Days | Int | 6 | - |  |  |
| 4 | `IntrstPrct` | Interest % | Num | 19.6 | - |  |  |
| 5 | `FixedSum` | Fixed Interest Amount | Num | 19.6 | - |  |  |
| 6 | `FixSumCurr` | Fixed Amount Currency | nVarChar | 3 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum |
