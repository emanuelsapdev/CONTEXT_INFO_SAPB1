# QWZ2 - Query Result Fields

- **Tabla:** QWZ2
- **Descripción:** Query Result Fields
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QWZ2.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Query Code | nVarChar | 8 | - |  |  |
| 2 | `Numerator` | Internal Number | Int | 11 | - |  |  |
| 3 | `FileCode` | Table Name | nVarChar | 20 | - |  |  |
| 4 | `FieldAlias` | Field Alias | nVarChar | 10 | - |  |  |
| 5 | `Title` | Field Title | nVarChar | 30 | - |  |  |
| 6 | `SortOrder` | Sort Order | Int | 11 | - |  |  |
| 7 | `SortType` | Sort Type | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `GroupBy` | Group By | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `AgregType` | Agreggate Function | Int | 11 | - |  |  |
| 10 | `CalcField` | Calculation Field | nVarChar | 254 | - |  |  |
| 11 | `IsCalc` | Is Calculation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `TmpAlias` | New Alias in Res. Table | nVarChar | 11 | - |  |  |
| 13 | `TmpDescr` | New Description in Res. Table | nVarChar | 30 | - |  |  |
| 14 | `Fld2Alias` | Field 2 Number | nVarChar | 10 | - |  |  |
| 15 | `FileCode2` | Field 2 Table Name | nVarChar | 20 | - |  |  |
| 16 | `Agreg2Type` | Field 2 Aggregate Function | Int | 11 | - |  |  |
| 17 | `FldOp` | Formula Operation | Int | 11 | - |  |  |
| 18 | `FldCnstVal` | Field Const. Val. | nVarChar | 254 | - |  |  |
| 19 | `Fld2CnsVal` | Field 2 Const. Val. | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Numerator |
