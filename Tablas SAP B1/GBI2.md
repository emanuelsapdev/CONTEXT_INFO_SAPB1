# GBI2 - GBI Row 2 - G/L Account Master Records

- **Tabla:** GBI2
- **Descripción:** GBI Row 2 - G/L Account Master Records
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 4 | `AcctName` | Account Name | nVarChar | 200 | - |  |  |
| 5 | `StrucLevel` | Account Structure Level | Int | 11 | - |  |  |
| 6 | `EvalSign` | Evaluation Sign | VarChar | 1 | - |  |  |
| 7 | `AddField` | Possible Additional Fields | nVarChar | 60 | - |  |  |
| 8 | `AcctType` | Account Type | nVarChar | 20 | - |  |  |
| 9 | `MesurUnit` | Measurement Unit | nVarChar | 10 | - |  |  |
| 10 | `BlDirect` | Direction of Balance | nVarChar | 4 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
