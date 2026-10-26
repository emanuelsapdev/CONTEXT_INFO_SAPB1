# CSHS - User-Defined Values

- **Tabla:** CSHS
- **Descripción:** User-Defined Values
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSHS.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormID` | Form ID | nVarChar | 100 | - |  |  |
| 2 | `ItemID` | Field | nVarChar | 52 | - |  |  |
| 3 | `ColID` | Column ID | nVarChar | 128 | - | -1 |  |
| 4 | `ActionT` | Action | Int | 6 | - | 0 | `0`<br>`1` = Valid Values<br>`2` = Query |
| 5 | `QueryId` | Query ID | Int | 11 | [OUQR](OUQR.md) |  |  |
| 6 | `IndexID` | Index | Int | 11 | - |  |  |
| 7 | `Refresh` | Refresh | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `FieldID` | Field | nVarChar | 60 | - |  |  |
| 9 | `FrceRfrsh` | Force Refresh | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `ByField` | By Field | VarChar | 1 | - | N | `Y` = When Field Changes<br>`N` = When Exiting Altered Column<br>`C` = When Column Value Changes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID |
| DETAILS | Yes | FormID, ItemID, ColID |
