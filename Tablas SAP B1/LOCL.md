# LOCL - Localizations Table

- **Tabla:** LOCL
- **Descripción:** Localizations Table
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/LOCL.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsKey` | Abs Key | Int | 11 | - |  |  |
| 2 | `LocCode` | Localization Code | nVarChar | 2 | - |  |  |
| 3 | `Name` | Name | nVarChar | 32 | - |  |  |
| 4 | `DfltLang` | Default Language | Int | 11 | - |  |  |
| 5 | `B5IColctn` | B5I Collection Name | nVarChar | 20 | - |  |  |
| 6 | `IncldInExp` | Include In export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `IncEnInExp` | Include English In Export | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LocCode |
| ABS_KEY | Yes | AbsKey |
