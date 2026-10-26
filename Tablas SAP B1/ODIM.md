# ODIM - Cost Accounting Dimension

- **Tabla:** ODIM
- **Descripción:** Cost Accounting Dimension
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODIM.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DimCode` | Dimension Code | Int | 6 | - |  |  |
| 2 | `DimName` | Dimension Name | nVarChar | 15 | - |  |  |
| 3 | `DimActive` | Activated? [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DimDesc` | Dimension Description | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DimCode |
| DIM_KEY | No | DimName |
