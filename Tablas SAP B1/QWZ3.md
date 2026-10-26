# QWZ3 - Query Condition Fields

- **Tabla:** QWZ3
- **Descripción:** Query Condition Fields
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QWZ3.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Query Code | nVarChar | 8 | - |  |  |
| 2 | `Numerator` | Internal Number | Int | 11 | - |  |  |
| 3 | `OpenBrackt` | Open Brackets Counter | Int | 11 | - |  |  |
| 4 | `FileCode` | Table Name | nVarChar | 20 | - |  |  |
| 5 | `FieldAlias` | Field Alias | nVarChar | 30 | - |  |  |
| 6 | `Operation` | Operation | Int | 11 | - |  |  |
| 7 | `CondVal` | Cond. Val. | nVarChar | 254 | - |  |  |
| 8 | `CondEndVal` | Cond. and Val. | nVarChar | 254 | - |  |  |
| 9 | `CompareFld` | Compare Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `UseRes` | Use Res. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `CompTblIdx` | Compare Table Index | nVarChar | 20 | - |  |  |
| 12 | `CompFldNum` | Compare Field Number | nVarChar | 254 | - |  |  |
| 13 | `Relatship` | Relationship | Int | 11 | - |  |  |
| 14 | `ClosBrackt` | Close Brackets Counter | Int | 11 | - |  |  |
| 15 | `Free_Text` | Free Text | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Numerator |
