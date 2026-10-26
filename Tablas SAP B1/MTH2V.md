# MTH2V - Bank Statements of External Reconciliation

- **Tabla:** MTH2V
- **Descripción:** Bank Statements of External Reconciliation
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MTH2V.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MthAcctCod` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `IsInternal` | Reconciliation Type | VarChar | 1 | - | E | `I` = Internal<br>`E` = External |
| 3 | `MatchNum` | Reconciliation No. | Int | 11 | - |  |  |
| 4 | `BnkAcctCod` | Account Code | nVarChar | 15 | - |  |  |
| 5 | `Sequence` | Sequence No. | Int | 11 | - |  |  |
| 6 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 7 | `Ref` | Reference | nVarChar | 27 | - |  |  |
| 8 | `DebAmount` | Debit Amount | Num | 19.6 | - |  |  |
| 9 | `Memo` | Details | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MthAcctCod, IsInternal, MatchNum, Sequence |
| SECONDARY | Yes | BnkAcctCod, Sequence |
