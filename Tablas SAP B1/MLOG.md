# MLOG - MLOG

- **Tabla:** MLOG
- **Descripción:** MLOG
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MLOG.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `absId` |  | Int | 11 | - |  |  |
| 2 | `userCode` |  | nVarChar | 20 | - |  |  |
| 3 | `ipAddress` |  | nVarChar | 20 | - |  |  |
| 4 | `updateDate` |  | Date | 8 | - |  |  |
| 5 | `tableName` |  | nVarChar | 10 | - |  |  |
| 6 | `operation` |  | VarChar | 1 | - |  | `C` = Create<br>`U` = Update<br>`D` = Remove |
| 7 | `objGuid` |  | nVarChar | 36 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | absId |
