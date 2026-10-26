# CCPD - Period-End Closing

- **Tabla:** CCPD
- **Descripción:** Period-End Closing
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CCPD.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PerAbs` | Period Code | Int | 11 | - |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `ProfitAct` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 5 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 6 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 7 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 8 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 9 | `Memo` | Row Details | nVarChar | 254 | - |  |  |
| 10 | `MarkLine` | Select | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `ActKeyLine` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `LocBalLine` | Current Balance | Num | 19.6 | - |  |  |
| 13 | `FcBalLine` | Balance (Account Currency) | Num | 19.6 | - |  |  |
| 14 | `SysBalLine` | Balance (SC) | Num | 19.6 | - |  |  |
| 15 | `ToPerAbs` | To Period Code | Int | 11 | - |  |  |
| 16 | `CtrlAct` | Control Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `PL_ACCOUNT` | P/L Account | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `Ref1_l` | Reference 1 for line | nVarChar | 100 | - |  |  |
| 19 | `Ref2_l` | Reference 2 for line | nVarChar | 100 | - |  |  |
| 20 | `Ref3_l` | Reference 3 for line | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PerAbs, Line_ID |
