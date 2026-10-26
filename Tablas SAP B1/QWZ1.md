# QWZ1 - Query Tables

- **Tabla:** QWZ1
- **Descripción:** Query Tables
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QWZ1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Query Code | nVarChar | 8 | - |  |  |
| 2 | `Numerator` | Internal Number | Int | 11 | - |  |  |
| 3 | `FileCode` | Table Name | nVarChar | 20 | - |  |  |
| 4 | `IsTemp` | Is Temp | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DoJoin` | Do Join | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `JoinToTbl` | Joined to Table | Int | 11 | - |  |  |
| 7 | `NumOfConds` | No. of Conds. | Int | 11 | - |  |  |
| 8 | `OuterJoin` | Outer Join | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `RightJoin` | Right Join | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Numerator |
