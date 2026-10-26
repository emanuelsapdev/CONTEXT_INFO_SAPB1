# MTH3V - Filter for Query MTH

- **Tabla:** MTH3V
- **Descripción:** Filter for Query MTH
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MTH3V.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `absEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `AcctCdeFrm` | Account Code From | nVarChar | 15 | - |  |  |
| 3 | `AcctCdeTo` | Account Code To | nVarChar | 15 | - |  |  |
| 4 | `IsInternal` | Reconciliation Type | VarChar | 1 | - | E | `I` = Internal<br>`E` = External |
| 5 | `IsCard` | Select BP or Account | VarChar | 1 | - | A | `A` = G/L Account<br>`C` = BP |
| 6 | `MatchNumFr` | Reconciliation No. From | Int | 11 | - |  |  |
| 7 | `MatchNumTo` | Reconciliation No. To | Int | 11 | - |  |  |
| 8 | `MthDateFrm` | Reconciliation Date From | Date | 8 | - |  |  |
| 9 | `MthDateTo` | Reconciliation Date To | Date | 8 | - |  |  |
| 10 | `MthAcctCod` | Account Code | nVarChar | 15 | - |  |  |
| 11 | `MatchNum` | Reconciliation No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MthAcctCod, IsInternal, MatchNum |
