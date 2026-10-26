# ORIT - Dunning Interest Rate

- **Tabla:** ORIT
- **Descripción:** Dunning Interest Rate
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORIT.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Interest Code | nVarChar | 20 | - |  |  |
| 2 | `Name` | Interest Name | nVarChar | 50 | - |  |  |
| 3 | `IncPartPay` | Include Partially Paid Inv. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `DayInMonth` | Number of Days in Month | Int | 11 | - |  |  |
| 5 | `OrigRate` | Use Original Exchange Rate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
