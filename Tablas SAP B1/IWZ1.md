# IWZ1 - Accounts Revaluation History

- **Tabla:** IWZ1
- **Descripción:** Accounts Revaluation History
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IWZ1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OIWZ](OIWZ.md) |  |  |
| 2 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 3 | `ActName` | Account Name | nVarChar | 200 | - |  |  |
| 4 | `ActFrmBlnc` | Account From Balance | Num | 19.6 | - |  |  |
| 5 | `ExecutLine` | Executed Row | VarChar | 1 | - | Y | `Y` = Executed Row<br>`N` = Filter Line |
| 6 | `ActRevCncl` | Account Revaluation Cancel | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 7 | `RevToAct` | Revaluate To Account | nVarChar | 15 | - |  |  |
| 8 | `ActDiffBal` | Account Difference Balance | Num | 19.6 | - |  |  |
| 9 | `RvCaclDate` | Reval. Acct Cancellation Date | Date | 8 | - |  |  |
| 10 | `ErrReason` | Error Reason | Int | 11 | - |  |  |
| 11 | `ActLastBal` | Account Last Reval Balance | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, AcctCode |
