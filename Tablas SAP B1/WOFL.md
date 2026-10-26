# WOFL - Object Wizard Fields

- **Tabla:** WOFL
- **Descripción:** Object Wizard Fields
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WOFL.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjCode` | Object Code | Int | 11 | - |  |  |
| 2 | `FldIndex` | Field Index | Int | 6 | - |  |  |
| 3 | `FldNum` | Field Number | Int | 6 | - |  |  |
| 4 | `Editable` | Editable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Find` | Find | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `DispDescr` | Display Description | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjCode, FldIndex |
