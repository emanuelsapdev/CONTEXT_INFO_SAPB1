# CDPM - Dynamic Permission

- **Tabla:** CDPM
- **Descripción:** Dynamic Permission
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CDPM.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PermId` | Permission ID | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `ObjectType` | Object Type | Int | 11 | - |  |  |
| 4 | `ObjectKey` | Object ID | nVarChar | 200 | - |  |  |
| 5 | `Father` | Parent | Int | 11 | - |  |  |
| 6 | `PermOption` | Permission Option | Int | 6 | - | 0 | `0` = Full/Read/None<br>`1` = Full/None<br>`2` = Full/None/Saved Queries |
| 7 | `System` | System Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Hidden` | Hidden | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `SortOrder` | Sort Order | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PermId |
| OBJECT | No | ObjectType, Name |
