# CHFL - Choose from List Format

- **Tabla:** CHFL
- **Descripción:** Choose from List Format
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CHFL.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjName` | Object Name | nVarChar | 20 | - |  |  |
| 2 | `FldIndex` | Field Index | Int | 6 | - |  |  |
| 3 | `FldNum` | Field No. | nVarChar | 60 | - |  |  |
| 4 | `DispName` | Displayed Name | nVarChar | 30 | - |  |  |
| 5 | `GroupBy` | Group By | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Visible` | Visible | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `DispDesc` | Show Type | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `SortOrder` | Sort Order | VarChar | 1 | - | A | `A` = Ascending<br>`D` = Descending |
| 9 | `VisIndex` | Visual Index | Int | 6 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjName, FldIndex |
