# PYM1 - Currency Selection

- **Tabla:** PYM1
- **Descripción:** Currency Selection
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PYM1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PymCode` | Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 2 | `CurrCode` | Currency Code | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 3 | `CurrName` | Currency Name | nVarChar | 20 | - |  |  |
| 4 | `Choose` | Choose | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PymCode, CurrCode |
