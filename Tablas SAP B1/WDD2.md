# WDD2 - Documents for Approval - Terms

- **Tabla:** WDD2
- **Descripción:** Documents for Approval - Terms
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WDD2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WddCode` | Internal ID | Int | 11 | - |  |  |
| 2 | `CondId` | Condition No. | Int | 11 | - |  | `1` = Deviation from Credit Limit<br>`2` = Deviation from Commitment<br>`3` = Gross Profit %<br>`4` = Discount %<br>`5` = Deviation from Budget<br>`6` = Total Document |
| 3 | `opCode` | Ratio | Int | 6 | - |  | `1` = Greater than<br>`2` = Greater or Equal<br>`3` = Less than<br>`4` = Less or Equal<br>`5` = Equal<br>`6` = Does not Equal |
| 4 | `opValue` | Value | nVarChar | 40 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WddCode, CondId |
